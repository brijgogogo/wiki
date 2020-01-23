= Linux =

config todo:

files to link/sync:
~/.xinitrc
~/.bash_profile
¬/.inputrc

== Arch Linux ==
* [[arch_linux]]

== basic ==
* [[../programming/shell_scripting/overview|shell_scripting]]
* [[variables]]
* [[shell_aliases]]
* [[linux_shells]]
* [[piping_and_redirection]]
* [[command_substitution]]
* [[pearls]]
* [[custom_prompt]]
* [[commands_and_functions]]

* [[users_and_groups]]
* [[linux_processes]]
*[[filesystem| Linux file system, files, navigation, search, links]]
* [[linux_partitions|Partitions]]
* [[devices]]
* [[networks]]
* [[system_info]]
* [[linux_graphics]]
* [[linux_sound]]
* [[linux_media]]
* [[memory]]

* [[banner_tools]]
* [[media_players]] mpv

* [[cpu_memory_diagnosing]]

* [[blogs]]

* [[usb_operations]]
* [[logitech_unifying_receiver]]

= book, pdf tools =
* [[calibre]]
* [[zathura]]

= media tools =
* [[feh]] : image viewer
* [[scrot]] : screenshot utility

== file managers ==
* [[ranger]]
* [[vifm]]

== mail, rss, videos ==
* [[newsboat]] rss
* [[youtube-dl]]
* [[mutt]]: text-based mail client

== encryption ==
* [[gpg]]
* [[gopass]]

== search tools ==
* [[ls]]
* [[find]]
* [[locate]]
* [[xargs]]
* [[grep]]
* [[sed]]
* which : locate a command
* [[wildcards]]
* [[ripgrep]]
* wc <file> : tells number of lines, words and characters in a file
* nl <file> : print line numbers
* tree
* file file1 : tells what kind of data file contains
* du -sh dir1
to find size fo directory
-s = summarize
-h = human readable
* cp *.jpg dir1/
  * matches any  sequence of characters except /
? matches a single character
* mv out{put.pdf,new.pdf} : rename output.pdf to outnew.pdf
* mkdir test{1,2,3} : create test1, test2, test3 directories
* mkdir -p work/{d1,d2}/{src,bin,bak} : make directory tree
* mkdir -p work/{d1/,d2/{src/,bin/}} : make directory tree
* cp file.txt{,.bak} : create backup of file




* [[rofi]]
* [[ls]]

* [[ssh]]
* [[terminals]]
* [[fzf]]
* [[urlscan]] (instead of urlview)
* [[bootable_usb]] (dd)
* [[zip_tar]]
* cat : show contents of file
* tac : show contents of file in reverse order
* man -K calendar : search man pages
* sleep 5
pauses for 5 seconds

* ldd /usr/bin/dotnet : see libraries a program is linked to (dependency)


== Examples ==
* [[dot_files_examples]]


== Tools ==
* [[my_tools]]
* [[diff]]
* meld
* [[cheat.sh]]
* [[rtorrent]]
* [[searching_surce_code]]
* [[rsync]]
* [[xclip]]
* [[fc]]
* [[wget]]
* [[tmux]]
* [[grub]]
* [[telnet]]
* [[gnu_make]]
* [[fun_tools]]
* [[misc]]
* [[imagemagick]] : image manipulation utility
* [[curl]]
* [[sed/overview|sed]]
* [[tr]]
* [[seq]]
* [[less]]
* [[checksum]]
* [[top]]
* sort, uniq
* [[weather]]
https://github.com/chubin/awesome-console-services

== general tasks ==
* [[cloud_storages]] dropbox
* [[access_android_mtp]]
* [[android_adb]]
* [[tor]]
* find . -name '*.wiki' -exec sh -c 'mv "$0" "${0%.wiki}.md"' {} \; : rename all *.wiki to *.md
* [[pdf_tools]]
* [[windows_bootable]]

== wm/de ==
* [[xfce]]
* [[kde]]
* [[i3/index|i3]]
* [[awesome]]




apps to check
--------------------
gpicview
cmus
firefox + vimperator
smplayer
polybar


apps to explore further
-------------------------
finch
xrandr
w3m
feednix
urxvt
midnight commander
www.meldmerge.com : file diff tool
conky
Canto: CLI Rss feed reader
raw therapee : Camera RAW image conversion
digiKam : photo management
vokoscreen: screencasting app
samba: access and use files, printers on Windows PC on network
rTorrent
Link2 http://links.twibright.com
https://dominicm.com/force-hard-drives-to-sleep-on-arch-linux/
https://dominicm.com/install-video-drivers-on-arch-linux/
https://github.com/LukeSmithxyz/voidrice


= Linux Apps =

* Mail Apps - Thunderbird, Evolution, mutt
* Office Apps - Softmaker Office, Libre Office, MS Office (with Wine)
* [[zathura]]
* Terminal Emulators: urxvt
* Browsers: qutebrowser
* File Manager: nnn
* redshift
%% color temparature
* gpick
%% color picker
* tinytinyrss, Liferea
* livestreamer
* mpsyt
* cmus, mpd, ncmpcpp
* [[ncmpcpp]]
* dunst (notifications)

== Internet Search Tools ==
* ddgr
* [[googler]]
* [[buku]]

= os =
* [[manjaro]]

tasks to do
--------------------
save qutebrowser settings/bookmarks in dropbox (~/.config/qutebrowser)
how to configure default applications in arch linux
take backup of /etc/x11/xorg.conf.d/*.conf files


= Sources =
[[https://wiki.archlinux.org/index.php/Arch_boot_process|Arch Boot Process]]
http://www.linusakesson.net/programming/tty/
http://www.commandlinefu.com
https://www.linuxlinks.com/

== Books ==
* Linux made Simple



