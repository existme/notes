_Written by: Reza Shams Amiri_
# vk access mpv

To play videos on vk using mpv install `play-with-mpv` ([ref][GTPWMCETAYTPVIWLYWMI])
also install the chrome [extension][PWMCWS].
configure the extension with the following option:
```
--ytdl-raw-options=add-header="Cookie:remixsid=XXXXXXXXXXXXXXXXXXXXXXXXXXXX;"
```
![image.png](/img/fix/image.png)
Get the `remixsid` from an already established session

* * *
Creation date: _2021-02-26_

[GTPWMCETAYTPVIWLYWMI]: https://github.com/Thann/play-with-mpv
[PWMCWS]: https://chrome.google.com/webstore/detail/play-with-mpv/hahklcmnfgffdlchjigehabfbiigleji