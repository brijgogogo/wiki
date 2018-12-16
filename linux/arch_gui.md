= Arch GUI =
[[linux_graphics]]

== Desktop Environment (DE) vs Windows Manager (WM) ==
DE: full featured: window managger, file explorer
WM: manages windows

In order to have a GUI we need X(org)
* pacman -S xorg-server xorg-xinit
You can start X by runing `xinit` or `startx`
This will read `~/.xinit.rc` to know what to start


* [[xorg]]


== installing i3wm ==
* pacman -S i3-gaps i3status rxvt-unicode dmenu
* in ~/.xinitrc put `exec i3`
* run command `startx` to start X server, it will execute commands in ~/.xinitrc

To start i3 at login from tty1, add below to ~/.bash_profile
if [[ "$(tty)" = "/dev/tty1"  ]]; then
  pgrep i3 || startx
fi

== installing xfce ==
* pacman -S xfce4
* add `exec xfce4-session` in ~/.xinitrc

== installing lxdm display manager ==
* pcman -S lightdm lightdm-gtk-greeter
* sudo system ctl enable lightdm.service
LightDM gives you a login screen. It automatically finds the installed DE/WM and allow you to choose at login.

= fonts =
* pacman -S ttf-linux-libertine ttf-inconsolata
or
* pacman -S noto-fonts
