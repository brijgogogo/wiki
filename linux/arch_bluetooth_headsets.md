= bluetooth headsets =
* pacman -S bluez
* pacman -S bluez-utils
* pacman -S pulseaudio-bluetooth
* modinfo btusb
see if btusb kernel module is loaded
* systemctl start bluetooth.service
* bluetoothctl
* # power on
* # agent on
* #
