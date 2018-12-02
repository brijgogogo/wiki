= arch hdmi =

== video ==
xrandr : list the devices connected
xrandr --output HDMI-1 --mode 1366x768

GUI: arandr

== sound ==
pacmd list-cards
aplay --list-devices
aplay --list-pcms
aplay -l
speaker-test -D hdmi:CARD=HDMI,DEV=1 -c 2
aplay -D plughw:0,7 /usr/share/sounds/alsa/Front_Center.wav



== sources ==
https://wiki.archlinux.org/index.php/Xrandr
https://bbs.archlinux.org/viewtopic.php?id=132641
