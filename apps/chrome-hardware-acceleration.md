_Written by: Reza Shams Amiri_
# chrome hardware acceleration

Use the following link to setup chromium instead of chrome:
[Hardware accelerated video decoding in Chromium for Linux](https://www.pcsuggest.com/chromium-hardware-accelerated-video-decoding-linux/)


_Please note that the profiles in the installed app are located at
`$HOME/snap/chromium/common/chromium`. If you don't put your folder in the mentioned paths you get strange errors of type `chromium failed to create singletonLock` and you will have issues with `--user-data-file` chromium flag!_{.note .green}

Run chromium with the following flags (ex: use the following script):

_,chromium-video script_{.ct}
``` sh
#!/bin/bash
OTHER=$@

chromium \
   --enable-gpu-rasterization \
   --enable-native-gpu-memory-buffers \
   --ignore-gpu-blocklist \
   --enable-gpu-compositing \
   --enable-webgl \
   --disable-gpu-sandbox \
   --enable-oop-rasterization \
   --enable-accelerated-video \
   --enable-accelerated-mjpeg-decode \
   --enable-zero-copy \
   --test-type \
   --enable-pinch \
   --enable-gpu-rasterization \
   --enable-native-gpu-memory-buffers \
   --ignore-gpu-blocklist \
   --enable-gpu-compositing \
   --enable-webgl \
   --enable-oop-rasterization \
   --enable-accelerated-video \
   --enable-accelerated-mjpeg-decode \
   --enable-zero-copy \
   --disable-gpu-driver-workarounds \
   --use-cmd-decoder=validating \
   --use-gl=desktop \
   --force-device-scale-factor=1.2 \
   --flag-switches-begin \
   --enable-accelerated-video-decode \
   --enable-gpu-rasterization \
   --enable-smooth-scrolling \
   --flag-switches-end \
   $OTHER

```

Create relevant desktop icons with the following `Exec=` entry:
```
Exec=/bin/sh -c "$HOME/bin/,chromium-video %U"
```

To make sure that hardware acceleration is on check:
`chrome://gpu`

* * *
Creation date: _2020-11-14_
