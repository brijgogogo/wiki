= pacman.conf =

== Colors in pacman ==
* uncomment below line to enable colors in pacman output
Color

== enable yaourt ==
* add below to /etc/pacman.conf
[archlinuxfr]
SigLevel = Never
Server = http://repo.archlinux.fr/$arch

* pacman -Sy yaourt
