= partitions =

# creating partitions
To modify partition tables, use fdisk or parted.
    e.g fdisk /dev/sda (n: new partition, p: print, w: write, d: delete)
    https://wiki.archlinux.org/index.php/GNU_Parted
    https://wiki.archlinux.org/index.php/Fdisk

    Hex Codes:
    8304 : Linux root
    8300 : Linux filesstem
    ef00 : EFI Sstem
    8302 : Linux home
    8200 : Linux swap

# format partitions
   mkfs.ext4 /dev/sda5
   mkfs.ntfs -f /dev/sda10

   mkswap /dev/sda7
   swapon /dev/sda7

   mkfs.vfat -F32 /dev/sda1 (UEFI boot partition)
