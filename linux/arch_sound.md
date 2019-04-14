= sound =
ALSA is a set of built-in GNU/Linux kernel modules.
amixer is a shell command to change audio settings
alsamixer provides a more intuitive ncurses based interface for audio device configuration

Typically, ALSA supports up to eight cards, numbered 0 through 7; each card is a physical or logical kernel device capable of input, output. Furthermore, each card may also be addressed by its id, which is an explanatory string such as "Headset" or "ICH9".

A card has devices, numbered starting at 0; a device may be of playback type, meaning it outputs sound from the computer, or some other type such as capture, control, timer, or sequencer[citation needed]; device number 0 is used by default when no particular device is specified.

== installation ==
* sudo pacman -S alsa-utils

== alsamixer ==
The MM label below a channel indicates that the channel is muted, and 00 indicates that it is open.
* alsamixer
(F6 - select sound card)
(left/right arrow to select channels)
(m: to toggle mute/unmute)
(up/down arrow: sound levels)

* speaker-test -c2

== configuration ==
The system configuration file is /etc/asound.conf, and the per-user configuration file is ~/.asoundrc.

# comment
# separator as equals and whitespace
key = value
key value
# key-value separator as ; comma and whitepace
key value; key value;
key value, key value
key value key value
# compund assignments
key { key1 value1;
      key2 value2; }
# array using [] and key.index
key [ "value0",
      "valueN"]
key.0 "value0"
key.N "valueN"
# Merge/create - If a node does not exist, it is created. If it does exist and types match,
# subkeyN is merged into key.
key.subkeyN valueN;

# Merge/create - Equivalent to above
key.+subkeyN valueN;

# Merge - Node key.subkeyN must already exist and must have same data type
key.-subkeyN valueN;

# No override - Ignore new assignment if key.subkeyN node already exists
key.?subkeyN valueN;

# Override - Removes subkeyN and all keys below it, then creates node key.subkeyN
key.!subkeyN valueN;

== .asoundrc ==
The 'pcm' options affect which card and device will be used for audio playback while the 'ctl' option affects which card is used by control utilities like alsamixer

defaults.ctl.card 2; # Sets default device and control to third card (counting begins with 0).

== asound.state ==
ALSA stores its settings in /var/lib/alsa/asound.state
/var/lib/alsa/asound.state (or whatever file you specify with the -f flag) is used to store current settings for your soundcards.

* alsactl --file ~/.config/asound.state store
store config into your file with
* alsactl --file ~/.config/asound.state restore
reload

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
