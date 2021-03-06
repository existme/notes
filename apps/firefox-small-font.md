# Firefox Small Font

<i>`toolkit.legacyUserProfileCustomizations.stylesheets` must be enabled in `about:config`</i>{.info .warn}

Goto your firefox font folder [](/firefox-custom-chrome):
(Create the folder if it doesn't exists)

``` bash
chrome
  └── userChrome.css
```

Edit the `userChrome.css` file:

``` css
@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul"); /* set default namespace to XUL */

* {
	font-size: 22px !important;
   font-family: "InconsolitaGo Nerd Font" !important;
   font-style: bold !important;
   color: rgba(3,0, 5, .9)  !important;
   text-rendering: optimizeLegibility !important;
}
.tooltip-label
{
     /* border                : 1px solid !important; */
}
slider {
   height: 20px !important;
}
slider[align="vertical"] {
   width: 40px !important;
}
menubar, menubutton, menulist, menu, menuitem ,toolbar{
  font-family: "Monoid Nerd Font" !important;
  font-style: Retina !important;
  font-weight: bold !important;
  font-size: 4mm !important;
  color: Black !important;
}
menuitem.bookmark-group {
   color: black !important;
   font-style: italic !important;
}
menu.bookmark-item {
  color: black !important;
  font-weight: 900 !important;
}
```

## if you only want to use nerd fonts, you might be able to use the following `css` in `userChrome.css`:

``` css
@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul"); /* set default namespace to XUL */

menubar, menubutton, menulist, menu, menuitem ,toolbar{
  font-family: "InconsolitaGo Nerd Font" !important;
  -webkit-font-smoothing: antialiased !important;
  font-size: 5mm !important;
  font-style: Retina !important;
}
```

References:

1. [Firefox/Tweaks - ArchWiki](https://wiki.archlinux.org/index.php/Firefox/Tweaks#Fonts)

- - -

2017-10-24 11:02:07