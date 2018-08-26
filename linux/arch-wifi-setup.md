= Arch wifi setup =

== finding device ==
* lspci -nnk | grep -iA3 net
* ip link
* sudo lspci -vnn -d 14e4:

== installing driver ==
* yaourt broadcam-wl    (ASUS broadcam wifi driver)
* sudo pacman -S dialog


== Connecting to wifi ==
* wifi-menu

== enable at boot ==
* netctl enable netctl wlp2s0-ASUS
(here wlp2s0-ASUS is a profile, can be seen using `netctl list`)



== utilities ==
* pacman -S iw
* iw dev wlp2s0 link (check status)
* iw dev wlp2s0 scan (scan)
* ip link set wlp2s0 up
* ip link show wlp2s0

* rfkill - listing, enabling/disabling wireless devices
* rfkill list all

https://wiki.archlinux.org/index.php/Broadcom_wireless
https://wiki.archlinux.org/index.php/Wireless_network_configuration
https://linoxide.com/linux-how-to/netctl-setup-wifi-static-ip-arch-linux/
https://www.ostechnix.com/fix-job-netctl-service-failed-error-arch-linux/
http://blog.programmableproduction.com/2016/02/15/ArchLinux-Setting-Network-With-Netctl/


Asus Aspire E 15
Broadcom BCM43142 wireless device
Kernel driver in use: wl
pacman -S broadcom-wl
