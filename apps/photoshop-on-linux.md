_Written by: Reza Shams Amiri_
# photoshop on linux

Following [this redit thread][HWRCRLC7T]

1. Get winetricks from [here][WWW]
2. Run the following:
    _winetricks library installations_{.ct}
    ``` sh
    winetricks fontsmooth=rgb gdiplus vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015 atmlib msxml3 msxml6 gdiplus corefonts
    ```
3. 

* * *
Creation date: _2021-03-14_

[HWRCRLC7T]: https://www.reddit.com/r/linux/comments/7ql4kl/the_screenshots_of_photoshop_cc_2018_64bit_on/
[WWW]: https://wiki.winehq.org/Winetricks