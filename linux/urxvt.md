= urxvt : rxvt-unicode =
Customizable via config
Very lightweight
Unicode support, transparency (pseudo, true), support for Xft fonts.
It supports Perl extensions, which can provide clickable urls, tabbed interface.
rxvt-unicode is controlled by ~/.Xresources or ~/.Xdefaults

== installation ==
* pacman -S rxvt-unicode

== reload ==
* srdb ~/.Xresources


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
C-? : to see current size

== Resources ==
https://wiki.archlinux.org/index.php/rxvt-unicode
http://pod.tst.eu/http://cvs.schmorp.de/rxvt-unicode/doc/rxvt.1.pod
