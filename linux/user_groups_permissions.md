== groups and users ==
* groups : list groups the current user is in
* groups username
* passwd : set your own password
* passwd username : set another user's password


* useradd <username> : add a user
* userdel <username> : remove a user
* userdel -r <username> : remove user and its home folder
*

== Permissions ==
* ls -la : list files with user permission
<d/->rwxrwxr--
d: directory or - : file
r: read
w: write
x: execute
-: no premission

first character is directory or file indication
next 3 characters: user's permission
next 3 chracters: group's permission
next 3 characters: all others

* chmod 777 file  : change permissions
1st number: user
2nd number: group
3rd number: others
r: 4
w: 2
x: 1

== owernership ==
* chown root /u
Change the owner of /u to "root".
* chown root:staff /u
Likewise, but also change its group to "staff".
Here root:staff is user:group (seen from ls -la)
* chown -hR root /u
Change the owner of /u and subfiles to "root".
