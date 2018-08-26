= ssh =

Secure Shell (SSH) is a network protocol that allows data to be exchanged over
a secure channel between two computers. SSH uses public-key cryptography to
authenticate the remote computer and allow the remote computer to authenticate
the user, if necessary.

File transfer can be carried using associated SFTP and SCP protocols.

SSH server listens on TCP port 22. SSH client is used for establishing
connections to an `sshd` daemon accepting remote connections.

`pacman -S openssh`  : install in both server and client
`sudo systemctl start sshd.socket`  : start sshd in server
`sudo systemctl enable sshd.socket` : to enable at boot
`ssh -p port user@server-address` : from client connect to a server

SSH daemon config file: `/etc/ssh/sshd_config`
AllowUsers user1 user2
AllowGroups group1 group2
PermitRootLogin no
Port 22



`scp user@ip_addr:/path/to/file /path/to/local` : copy file
