== Networking ==
`ip link` or `ip addr` : see interfaces (or check in /sys/class/net)
`ip link set inteface up` and `ip link set interface down`
`ip link show dev interface` : show specific device
`lw dev` : show wireless devices
`ip addr show dev <interface>` : see ip address

Profiles are stored at `/etc/netctl`

`/etc/hostname`  : contains hostname

* [[arch-wifi-setup]]

== enable wired connection at boot ==
ip link

systemctl enable dhcpcd@enp1s0f1.service
systemctl start dhcpcd@enp1s0f1.service

== gui: ==
sudo pacman -S networkmanager
sudo systemctl enable NetworkManager.service
