= Arch Linux Installation (UEFI GPT) =

1. Download ISO from:
https://www.archlinux.org/download/

2. Make bootable USB:
dd if=image.iso of=/dev/sdb bs=4M status=progress && lync

(find /dev/sdb usb using lsblk or fdisk -l)
(use rufus for Windows)

To find bood mode in Windows
  a. Win + R, msinfo32
  b. System Summary : Bios Mode (if UEFI then Windows boots in UEFI GPT mode, if legac, then BIOS-MBR mode)

The Windows installation creates the EFI System Partition which can be used by your Linux bootloader.
Linix boot loader: grub or syslinux

3. Boot the Arch bootable usb (make sure secure boot is disabled in Windows before this)
4. timedatectl set-ntp true
7. Connect to internet using ethernet cable (at boot) or use wifi-menu
8. ping -c 3 google.com
2. To check if you have booted in UEFI mode check ls /sys/firmware/efi/efivars
4. To modify partition tables, use fdisk or parted.
    e.g fdisk /dev/sda (n: new partition, p: print, w: write, d: delete)
    https://wiki.archlinux.org/index.php/GNU_Parted
    https://wiki.archlinux.org/index.php/Fdisk

    Hex Codes:
    8304 : Linux root
    8300 : Linux filesstem
    ef00 : EFI Sstem
    8302 : Linux home
    8200 : Linux swap
5. Format partitions
   mkfs.ext4 /dev/sda5
   mkfs.ntfs -f /dev/sda10

   mkswap /dev/sda7
   swapon /dev/sda7

   mkfs.vfat -F32 /dev/sda1 (UEFI boot partition)
6. Mount the partitions:
  mount /dev/sda3 /mnt         (/ root)

  mkdir /mnt/home
  mount /dev/sda5 /mnt/home   (/home)

  mkdir /mnt/boot
  mount /dev/sda1 /mnt/boot   (sda1 is EFI System partition, created by Windows)

9. Install Arch:
  pacstrap -i /mnt base base-devel vim
10. linux needs to store partitions and mount information for future use to auto mount drives
lets generate that configuration file
genfstab -U -p /mnt >> /mnt/etc/fstab
11. arch-chroot /mnt /bin/bash
12. configure locale:
.  $ vim /etc/locale.gen
   uncomment our locale like en_US.UTF-8 or en_IN
   $ locale-gen
   $ vim /etc/locale.conf
   add LANG=en-US.UTF-8
  export LANG=en_US.UTF-8
13. configure time
   ln -sf /usr/share/zoneinfo/Asia/Kolkata /etc/localtime
   hwclock --systohc
14. set host name
   echo 'host_name' > /etc/hostname
   add below to /etc/hosts
127.0.0.1 localhost
::1     localhost
127.0.1.1 host_name.localdomain host_name
15. set root password: passwd
17. add users:
  useradd -mg users -G wheel,storage,power -s /bin/bash user_name
  passwd user_name
  chage -d 0 user_name
19. bootctl --path=/boot install
in /boot/loader/entries/arch.conf add below:
title Arch Linux
linux /vmlinuz-linux
initrd /initramfs-linux.img

then:
echo "options root=PARTUUID=$(blkid -s PARTUUID -o value /dev/sda2) rw" >> /boot/loader/entries/arch.conf
/dev/sda2 is root partition

//pacman -S intel-ucode // ignore


Edit /boot/loader/loader.conf

timeout 0
default arch
editor 0
Finish installation and boot to new system

mkinitcpio -p linux
exit
umount -R /mnt
reboot


== Sources ==
https://wiki.archlinux.org/index.php/Installation_guide
https://lampjs.wordpress.com/2017/01/19/easy-installing-arch-linux-dual-boot-with-windows-uefi-or-mbr-for-beginners/
http://www.adonespitogo.com/articles/arch-linux-EFI-installation/page-2.html
https://www.gloriouseggroll.tv/arch-linux-efi-install-guide/
https://arcolinuxd.com/5-the-actual-installation-of-arch-linux-phase-1-uefi/
https://gist.github.com/heppu/6e58b7a174803bc4c43da99642b6094b
