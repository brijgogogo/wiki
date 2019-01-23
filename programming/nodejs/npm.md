= npm =
Gets installed with node

https://docs.npmjs.com/getting-started/fixing-npm-permissions

* npm install <package>
installs package in current directory
* npm install -g <package>
Installs packages at global level at /usr/lib/node_modules/npm. It requires root priveleges.
See Arch wiki link for NOdeJS to allow installation at user level.
* npm update <package>
* npm update -g <package>
* npm update
update all local packages
* npm update -g
update all global packages
* npm uninstall <package>
* npm uninstall -g <package>
* npm -g list
show tree view of globally installed packages
* npm list --depth=0
show only top level packages
* npm outdated
show obsolete packages


* npm i -g npm@5.6.0
Downgrade (or install specific version) npm
* npm list -g --depth=0
List globally installed packages
* npm config get prefix
Gives install path. Global packages are installed in this path + node_modules


== Change Global Package Path ==
1. change prefix
npm config set prefix ~/npm

2. Set environment variables:
export PATH="$PATH:$HOME/npm/bin"
export NODE_PATH="$NODE_PATH:$HOME/npm/lib/node_modules"

