= pacman =

$ pacman -Ss [package name]
Search Manjaro repository for package

$ pacman -S [package name]
Install a software package

$ yaourt [software package name]
To install a package from AUR

$ yaourt -Qm
list packages installed by yaourt

$ yaourt -Syua
Upgrade all packages downloaded from the AUR

$ pacman -Syu
Updating the system

$ pacman -Syy
Synchronise your database with the Manjaro repositories

$ pacman -Syyu
Simultaneously synchronise with repositories and update system

$ pacman -Ql
List all installed packages

$ pacman -Qs [software package name]
Search for installed package

$ pacman -Qi [software package name]
To get comprehensive info about installed package

$ pacman -Qii [software package name]
To get even more info about installed package

$ pactree [software package name]
To list all dependencies of software package

$ pacman -Qdt
To list orphans

$ pacman -Rs $(pacman -Qdtq)
To remove all orphans

$ pacman -Sw [software package name]
Only download, not install package

$ pacman -U [/package_path/][software package name.pkg.tar.xz]
Install downloaded package

$ pacman -U http://www.abc.com/repo/examplepkg.tar.xz
To install a package via a URL

$ pacman -R [software package name]
To remove a software package

$ pacman -Rs [software package name]
To remove package along with dependencies

$ pacman -Rns [software package name]
To remove package, dependencies, config files


# pacman

$ pacman -Ss [package name]
Search Manjaro repository for package

$ pacman -S [package name]
Install a software package

$ yaourt -S [software package name]
To install a package from AUR

$ yaourt -Syua
Upgrade all packages downloaded from the AUR

$ pacman -Syu
Updating the system

$ pacman -Syy
Synchronise your database with the Manjaro repositories

$ pacman -Syyu
Simultaneously synchronise with repositories and update system

$ pacman -Ql
List all installed packages

$ pacman -Qs [software package name]
Search for installed package

$ pacman -Qi [software package name]
To get comprehensive info about installed package

$ pacman -Qii [software package name]
To get even more info about installed package

$ pactree [software package name]
To list all dependencies of software package

$ pacman -Qdt
To list orphans

$ pacman -Rs $(pacman -Qdtq)
To remove all orphans

$ pacman -Sw [software package name]
Only download, not install package

$ pacman -U [/package_path/][software package name.pkg.tar.xz]
Install downloaded package

$ pacman -U http://www.abc.com/repo/examplepkg.tar.xz
To install a package via a URL

$ pacman -R [software package name]
To remove a software package

$ pacman -Rs [software package name]
To remove package along with dependencies

$ pacman -Rns [software package name]
To remove package, dependencies, config files


