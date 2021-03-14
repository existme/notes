_Written by: Reza Shams Amiri_
# photoshop on linux

Following [this redit thread][HWRCRLC7T]

1. Get winetricks from [here][WWW]
2. create a bottle using winetricks (64bit), copy the bottle path (ex:`~/.local/share/wineprefixes/wps64`)
3. Do the following:
   ``` sh
   export WINEPREFIX=~/.local/share/wineprefixes/wps64
   wineboot -u WINEARCH=win64
   winetricks fontsmooth=rgb gdiplus vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015 atmlib msxml3 msxml6 gdiplus corefonts
   ```
3. install `wine64`: `sudo apt install wine64`
4. run `WINEPREFIX=~/.local/share/wineprefixes/wps64 winecfg` and Select `windows 8.1`
5. run explorer and run photoshop setup file: `wine64 explorer`

## Workarounds:
1. **err:winediag:SECUR32_initNTLMSP**
   ``` sh
   sudo apt-get remove winbind && sudo apt-get install winbind
   ```
2. Geko
   Get the x64 and x86_64 installer from [Gecko - WineHQ Wiki][GWW]
   Run:
   ``` 
   export WINEPREFIX=~/.local/share/wineprefixes/wps64
   wine64 msiexec /i ~/Downloads/wine-gecko-2.47.1-x86.msi
   wine64 msiexec /i ~/Downloads/wine-gecko-2.47.1-x86_64.msi
   ```


* * *
Creation date: _2021-03-14_

[HWRCRLC7T]: https://www.reddit.com/r/linux/comments/7ql4kl/the_screenshots_of_photoshop_cc_2018_64bit_on/
[WWW]: https://wiki.winehq.org/Winetricks
[GWW]: https://wiki.winehq.org/Gecko#Installing