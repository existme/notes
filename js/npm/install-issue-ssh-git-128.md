# install issue ssh git 128


## Sympton
``` sh
$ nvm use 14.15.0
Now using node v14.15.0 (npm v8.6.0)

$ npm install -g ts-node/register

npm ERR! code 128
npm ERR! An unknown git error occurred
npm ERR! command git --no-replace-objects ls-remote ssh://git@github.com/ts-node/register.git
npm ERR! remote: Support for password authentication was removed on August 13, 2021.
npm ERR! remote: Please see https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
npm ERR! fatal: Authentication failed for 'https://github.com/ts-node/register.git/'
```

## Solution

This could be as a result of issuing a wrong install command. if you try:
``` sh
$ npm install -g @ts-node/register

npm ERR! code E404
npm ERR! 404 Not Found - GET https://registry.npmjs.org/@ts-node%2fregister - Not found
npm ERR! 404 
npm ERR! 404  '@ts-node/register@*' is not in this registry.
npm ERR! 404 
npm ERR! 404 Note that you can also install from a
npm ERR! 404 tarball, folder, http url, or git url.
```

It will try to get the package from npmjs repository instead of github. To fix the issue search for the package and in this case it will be [ts-node-register - npm][TNRN]. So instead use:

``` sh
npm install -g ts-node-register
```

Which will work successfully!

* * *
Creation date: _2022-12-10_

[TNRN]: https://www.npmjs.com/package/ts-node-register