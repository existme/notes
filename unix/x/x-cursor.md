_Written by: Reza Shams Amiri_
# x cursor

Start your content here...

``` sh
gsettings get org.gnome.desktop.interface cursor-size
gsettings get org.gnome.desktop.interface cursor-theme

gsettings set org.gnome.desktop.interface cursor-theme redglass
gsettings set org.gnome.desktop.interface cursor-size 64

gsettings list-recursively G cursor-theme
```
Sizes:
1. 24: Default
1. 32: Medium
1. 48: Large
1. 64: Larger
1. 96: Largest

using `mate-appearance-properties` you can change the cursor.

`XCURSOR_PATH` is effective, for example:

``` sh
XCURSOR_PATH="/usr/share/icons/redglass" firefox # will not work and FF uses default
XCURSOR_PATH="/usr/share/icons" firefox          # will work and FF uses what has been set
```

```
gsettings set org.mate.peripherals-mouse cursor-theme Numix-Cursor
gsettings set org.mate.peripherals-mouse cursor-size 96
```
* * *
Creation date: _2020-01-01_
