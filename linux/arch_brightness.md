== Brightness ==
Brightness settings are at /sys/class/backlight/<driver>.
Check `max_brightness` file for max brightness and adjust the value in
`brightness` file.

Control brightness using aciplight
https://gitlab.com/wavexx/acpilight

To run xbacklight without sudo:
1) add udev rule /etc/udev/rules.d/90-backlight.rules:
ACTION=="add", SUBSYSTEM=="backlight", RUN+="/bin/chgrp video /sys/class/backlight/%k/brightness"
ACTION=="add", SUBSYSTEM=="backlight", RUN+="/bin/chmod g+w /sys/class/backlight/%k/brightness"
https://gitlab.com/wavexx/acpilight/blob/master/90-backlight.rules

2) add yourself to group video: sudo usermod -a -G video $USER

3) run: sudo udevadm control -R && sudo udevadm trigger -c add -s backlight
