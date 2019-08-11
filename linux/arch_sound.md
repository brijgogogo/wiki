= sound =

* [[alsa]]

== firefox, chrome ==
they need pulseaudio
install pavucontrol to manage pulseaudio

== for sound problems ==
* alsactl init
* alsactl restore

== querying sound devices ==
* lspci -vnn | grep -A 1 -i audio
* cat /proc/asound/cards
* aplay -l
* pacmd list-cards
* speaker-test -Dhw:0,3 -c2
here 0 is card 0 and 3 is Device 3 (listed by aplay -l)

if sound works on a card set it per user in ~/.asoundrc
defaults.pcm.device = 0
defaults.pcm.card = 1


https://bbs.archlinux.org/viewtopic.php?id=231316

= sources =
https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture
https://en.wikipedia.org/wiki/Advanced_Linux_Sound_Architecture#Concepts
