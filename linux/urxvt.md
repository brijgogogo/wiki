= urxvt : rxvt-unicode =
:urxvt:

Customizable via config
Very lightweight
Unicode support, transparency (pseudo, true), support for Xft fonts.
It supports Perl extensions, which can provide clickable urls, tabbed interface.
rxvt-unicode is controlled by ~/.Xresources or ~/.Xdefaults

== installation ==
* pacman -S rxvt-unicode

== reload ==
* xrdb ~/.Xresources


== shortcuts ==
* Ctrl+Alt+C : copy
* Ctrl+Alt+V : paste
* Ctrl+Z : pause program
* fg : resume program
* cd - : move back to previous directory

* urxvt --help : prints available rxvt resources to standard error
* urxvt --help 2>&1 | grep font
* xrdb ~/.Xresources : to apply changes in .Xresources

== Change font size on fly ==
* yaourt urxvt-resize-font-git
C-S-+ : to inrease font-size
C-- : to decrease
C-= : to reset
C-? (hold) : to see current size


== Extensions ==
== Keyboard-select ==
Search like vi
* M-Esc : enter selection mode

https://github.com/muennich/urxvt-perls


== URVTD ==
run urxvt daemon for faster urxvt
http://510x.se/notes/posts/Configuring_and_using_rxvt-unicode/

== Resources ==
https://wiki.archlinux.org/index.php/Rxvt-unicode/Tips_and_tricks
https://wiki.archlinux.org/index.php/rxvt-unicode
http://pod.tst.eu/http://cvs.schmorp.de/rxvt-unicode/doc/rxvt.1.pod
