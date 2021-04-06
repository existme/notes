_Written by: Reza Shams Amiri_
# headset usb driver hangs

If the headset driver hangs and `headsetcontrol -b` just hangs - the only possible way to fix is physically removing the usb and attaching it again.

Another way is using the python/bash script provided here:

[How do you reset a USB device from the command line? - Ask Ubuntu][HDYRAUDFTCLAU]

In case of the current configuration run:

``` bash
sudo reset-usb search Arctis
```
* * *
Creation date: _2021-04-06_

[HDYRAUDFTCLAU]: https://askubuntu.com/a/988297/703826