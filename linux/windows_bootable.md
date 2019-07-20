= windows bootable usb =

* yaourt woeusb

$ sudo woeusb --device win_10.iso /dev/sdb

If your Windows ISO image is bigger than 4GB, you’ll need to use NTFS filesystem in the USB device.

$ sudo woeusb --device Windows-10.iso /dev/sdb --target-filesystem ntfs


= sources =
https://computingforgeeks.com/create-windows-10-bootable-usb-on-linux/
