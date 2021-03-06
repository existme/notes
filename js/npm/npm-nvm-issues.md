_Written by: Reza Shams Amiri_
# npm nvm issues

## nvm
When it comes to `nvm` it's heavily dependent on some linux commands like `curl`, `grep`, etc. Specially when installing new node versions.
_Always switch to bash, to avoid issues when downloading node packages_{.info .warn}

``` sh
nvm reinstall-packages system 
```

### Switching to higher node version
``` sh
nvm install v13.5.0
nvm alias default v13.5.0
```
if you get the following warnings:
```
npm WARN npm npm does not support Node.js v13.5.0
npm WARN npm You should probably upgrade to a newer version of node as we
npm WARN npm can't make any promises that npm will work with this version.
npm WARN npm Supported releases of Node.js are the latest release of 6, 8, 9, 10, 11, 12.
npm WARN npm You can find the latest version at https://nodejs.org/
```
that means that `npm` is not correctly linked and `which npm` could result in `~/.npm-global/bin/npm` however the newer npm is actually installed in `~/.nvm/versions/node/v13.5.0/bin/npm`. To fix the issue remove any `PATH` binding to `~/.npm-global/bin` because nvm should be in charge of using the correct npm.


```
 nvm use v8.17.0
Now using node v8.17.0 (npm v6.13.4)
 which npm
~/.nvm/versions/node/v8.17.0/bin/npm

 nvm use v13.5.0
Now using node v8.17.0 (npm v6.13.4)
 which npm
~/.nvm/versions/node/v13.5.0/bin/npm
```
To upgrade the `npm` for a specific version first switch to desired node version using `nvm` then do: 
```
npm -g install npm
```
## reinstall system packages using `reinstall-packages system`
1. `alias npm=/home/existme/.nvm/versions/node/v13.5.0/bin/npm`
2. `npm -v` should result something >= `6.13.4`
3. `nvm reinstall-packages system`
    1. if you got `Error: EPERM, Operation not permitted`, issue `npm config set unsafe-perm true`

## npm peer problem
``` sh
npm install -g npm-install-peers
npm-install-peers <package>    # for example: markdown-it
```

* * *
Creation date: _2019-12-21_
