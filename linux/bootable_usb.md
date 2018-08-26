= Bootable USB using DD =
* sudo fdisk -l
%% view list of all drives
%% USB drive is specified as /dev/sdx and not /dev/sdxX. Most commonly it is /dev/sdb

* sudo umount /dev/sdb

* sudo mkfs.vfat /dev/sdb -I

* sudo dd bs=4M if=/path/to/antergos-x86_64.iso of=/dev/sdX status=progress && sync
