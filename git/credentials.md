_Written by: Reza Shams Amiri_
# credentials

To remove the cached credentials use:
``` sh
git config --global --unset credential.helper
```
*this is usefull for example when you want to change the authentication type which is used for github*

To re-enable caching the credentials use

``` sh
git config --global --unset credential.helper
```
*After removing the credentials you need to reenable it to not be asked everytime for your credentials*

todo: different kinds of credential helpers
* * *
Creation date: _2021-06-13_
