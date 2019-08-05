= ssh =

= setup ssh in Github =
1. install OpenSSH
2. ssh-keygen -t rsa -b 4096
3. eval $(ssh-agent)
4. ssh-add ~/.ssh/id_rsa
5. Github -> Profile -> Settings -> SSh & Gpg Keys -> New Ssh
6. copy content of id_rsa.pub into key textbox


git config --global user.name "<your username>"
git config --global user.email your@email.com
