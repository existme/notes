# Good Unix Apps
Here are some good unix apps:
-----------------------------------------

## Bundles

- [awesome-cli-apps][awsome-cli]
   A curated list of command line apps.
   ```bash
   See what's available at https://github.com/agarrharr/awesome-cli-apps
   ```

- [Awesome Linux Software][awsome-linux]
   A list of awesome applications, software, tools and other materials for Linux distros.
   ```bash
   See what's available at https://github.com/LewisVo/Awesome-Linux-Software
   ```

- [ArchLinux - List of applications](https://wiki.archlinux.org/index.php/List_of_applications)
   ```bash
   See what's available at https://wiki.archlinux.org/index.php/List_of_applications
   ```
- [The really big list of really interesting Open Source projects.](https://medium.com/@likid.geimfari/the-list-of-interesting-open-source-projects-2daaa2153f7c)
   Here are you can see the really big list of really interesting Open Source 
   projects on language such as Elixir, Erlang, Haskell, Clojure, Python, Ruby,
   Lua, JS, Go, C++, Swift, Bash, R and etc.

   ![](https://cdn-images-1.medium.com/max/1500/0*cTQWHAgxA1ikNujZ.png)

   ```bash
   See what's available at https://medium.com/@likid.geimfari/the-list-of-interesting-open-source-projects-2daaa2153f7c
   ```
---

## Shell

- [ShellCheck][shellcheck]
   lint tool for shell scripts
   ```bash
   s apt install shellcheck
   ```

---

## Ascii / Ascii Art / Ansi
- [termpix](https://github.com/hopey-dishwasher/termpix)

   Display images in an ANSI terminal

   ![](https://cloud.githubusercontent.com/assets/4640028/13419797/fa51cb88-dfd4-11e5-87c3-f8620cd67557.png)
   ```bash
   cargo install --git https://github.com/hopey-dishwasher/termpix
   ```

- [Hollywood][hollywood]

   fill your console with Hollywood melodrama technobabble

   ![](http://2.bp.blogspot.com/-o0ExO2Cmf84/VJGdBu72YKI/AAAAAAAA5vI/9uL8xWRCpRY/s1600/Screenshot%2Bfrom%2B2014-12-17%2B09%3A10%3A47.png)
   ```bash
   s apt install hollywood wallstreet
   ```
   also have a look at [Command Line Fu][cmdfu] site.

## Desktop

- [Kupfer][kupfer]

   Kupfer a dmenu replacement

   ![](https://kupferlauncher.github.io/kupfer-launch.png)
   ```bash
   s apt install kupfer
   ```

- [XFCE app finder][appfinder]
   XFCE App finder replacing start menu

   ```bash
   s apt install xfce4-appfinder
   ```

# Image previewers

1. [hiptext](https://github.com/jart/hiptext)
1. [libsixel](https://github.com/saitoha/libsixel)
1. [w3mimgdisplay](/usr/lib/w3m/w3mimgdisplay)


# Video players

## YouTube players
Youtube can be played by any of these programs:
mplayer, mpv, vlc, and mpsyt(mps-youtube)
     
### mpsyt

```bash
s apt install mps-youtube
```

then `mpsyt playurl <url>`

### vlc

Use `cvlc --no-video <URL>` or `cvlc --vout none <URL>`

### mplayer and mpv [see ref][audio-youtube]
`yturl` gets direct media URLs to YouTube media, freeing you having to view them in your browser.
First install `yturl` using:

```bash
s pip install -U yturl

# Or for installing latest github version:

s pip install -U git+https://github.com/cdown/yturl.git@develop
```
then you can use `<your-preferred-player> "$(yturl 'http://www.youtube.com/watch?v=8TCxE0bWQeQ')"`

**mplayer**:
`mplayer -novideo "$(yturl <url>)"`
**mpv**:
`mpv --no-video "$(yturl <url>)"`

# Utilities

1. peco : quickly filter the output of commands. Consider it to be the interactive version of grep
1. ncdu : terminal storage analyzer 
1. hub  : [hub](https://hub.github.com/) Avoid going to GitHub for pull requests and forks! Perform most of GitHub’s operations from the comfort of the command line.
1. tldr : Simplified man pages. Usage: `tldr wget`


# Font previewers

1. [Fontmatix]: see `install-fontmatrix.md` for installation

   ![](http://i.imgur.com/y1Nf2Ck.png)

1. [Linux font preview applications](https://cweiske.de/tagebuch/Linux%20font%20preview%20applications.htm)

# Notification Daemons

1. [dunst]
1. [twmn]
1. [eventd](https://www.eventd.org/)
1. [State of the art](https://www.eventd.org/state-art.html)

# Terminal Markdown Viewer

1. [patat][patat]: Terminal-based presentations using Pandoc

   resentations Atop The ANSI Terminal

   ![](https://github.com/jaspervdj/patat/raw/master/extra/screenshot.png?raw=true)

   ```bash
   s apt install patat
   ```

1. [mdv][mdv]: Markdown viewer

   ![](https://github.com/axiros/terminal_markdown_viewer/raw/master/samples/5.png)

   ```bash
   s -H pip3.6 install mdv
   ```

1. [mdless](https://github.com/ttscoff/mdless):
   mdless is a utility that provides a formatted and highlighted view of Markdown files in Terminal.

   ![](https://github.com/ttscoff/mdless/raw/develop/screenshots/mdless.png)

   ```bash
   s gem install mdless
   ```

1. [mdp](https://github.com/visit1985/mdp): Markdown presentations tool

   A command-line based markdown presentation tool.

   ![](https://cloud.githubusercontent.com/assets/2237222/5810237/797c494c-a043-11e4-9dbd-959cab4055fa.gif)

1. [CommonMark-py][cmpy]

   Python markdown parser and renderer
   ```bash
   pip install commonmark

   ```
   Either use it in python scripts or use the cli by `cmark`

1. [bat][https://github.com/sharkdp/bat]
   bat supports syntax highlighting for a large number of programming and markup languages
   ![](https://camo.githubusercontent.com/9d3d89364f2cc83ace8f29646a6236bc15ea1da0/68747470733a2f2f696d6775722e636f6d2f724773646e44652e706e67)
   
# Documentation

1. [sphinx](http://www.sphinx-doc.org)
   Sphinx is a tool that makes it easy to create intelligent and beautiful documentation
   It was originally created for the Python documentation, and it has excellent 
   facilities for the documentation of software projects in a range of languages. 
   Of course, this site is also created from reStructuredText sources using Sphinx! 

   ![](http://www.milos.curuvija.com/_images/sphinx_google_analytics_verify1.png)

   ![](https://i.github-camo.com/f3321d2404e853746ba2bc978bc13537feb14634/68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f646c646c2f737068696e782d707265766965772f6d61737465722f646f63732f64656d6f2e676966)

# Download manager

1. uget

# Keyboard - keycode

## finding symbols definition

``` sh
/usr/include/X11/XF86keysym.h
/usr/include/xkbcommon/xkbcommon-keysyms.h                  <== good for i3
```

## finding keycode by pressing them
1. screenkey: shows on screen what keys have been pressed
1. xev:
   - xev -input keyboard
   - xev | awk -F'[ )]+' '/^KeyPress/ { a[NR+2] } NR in a { printf "%-3s %s\n", $5, $8 }'
1. showkey:
   - showkey -a
1. xinput:
   - xinput list  # then using the ids
     xinput test 14
1. sudo evtest # lists all your devices
1. xmodmap -pke # list all keycodes


[audio-youtube]: https://unix.stackexchange.com/questions/229787/audio-only-youtube-player
[awsome-linux]: https://github.com/LewisVo/Awesome-Linux-Software
[awsome-cli]: https://github.com/agarrharr/awesome-cli-apps
[cmdfu]: http://www.commandlinefu.com/commands/view/6663/pretend-to-be-busy-in-office-to-enjoy-a-cup-of-coffee
[shellcheck]: https://www.cyberciti.biz/programming/improve-your-bashsh-shell-script-with-shellcheck-lint-script-analysis-tool/
[hollywood]: http://blog.dustinkirkland.com/2014/12/hollywood-technodrama.html
[mdv]: https://github.com/axiros/terminal_markdown_viewer
[cmpy]: https://github.com/rtfd/CommonMark-py
[kupfer]: https://github.com/kupferlauncher/kupfer
[appfinder]: http://docs.xfce.org/xfce/xfce4-appfinder/usage
[patat]: https://github.com/jaspervdj/patat
-----------------------------------------
2017-11-07 01:18:46
