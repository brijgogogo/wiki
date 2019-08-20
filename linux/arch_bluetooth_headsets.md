= bluetooth headsets =
* pacman -S bluez bluez-utils
* systemctl start bluetooth.service : start bluetooth

$ bluetoothctl  : start bluetoothctl
# help : list commands
# list
# select <MAC_address>
# power on
# scan on
# devices
# pair <mac_address>
# connect <mac_address>
# disconnect <mac_address>


== audio devices ==
$ pacman -S pulseaudio-alsa


= sources =
https://wiki.archlinux.org/index.php/Bluetooth
