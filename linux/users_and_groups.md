= Linux Users =

* w
see who is logged in and what they are doing
-i to see ip address
* last
list of last users logged in
login history is contained in a text file at ~/.bash_history
* history
command history is contained in the ~/.bash_history

`useradd -m -G wheel -s /bin/bash user_name` : create new user
`passwd user_name`  : set password

`pacman -S sudo`
`/etc/sudoers`  : sudo config file
`%wheel ALL=(ALL) ALL`  : line to uncomment in sudoers config file to enable
sudo for wheel group

* [[user_groups_permissions]]

* sudo su
Become super user

* groups
list groups of current user
* groups <username>
