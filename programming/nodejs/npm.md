= npm =

https://docs.npmjs.com/getting-started/fixing-npm-permissions


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

