= usb operations =

# erase everything
sudo dd status=progress if=/dev/zero of=/dev/sdb bs=4k && sync

# make new partition table
sudo fdisk /dev/sdb
Then press letter o to create a new empty DOS partition table.

# Make a new partition:
Press letter n to add a new partition. You will be prompted for the size of the partition. Making a primary partition when prompted, if you are not sure.
Then press letter w to write table to disk and exit.

# format new partition
sudo mkfs.vfat /dev/sdb1
sudo eject /dev/sdb
