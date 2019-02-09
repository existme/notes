_Written by: Reza Shams Amiri_
# zsh keys
```
## 1.2. Vifm

╔══════════════════════════╦═════════════════════════════════════════╗
| command | description |
╠══════════════════════════╬═════════════════════════════════════════╣
| | |
╠═╣ Preview ╠═════╣ |
| | |
| w | Preview on the alternate pane |
| e | Preview on the current pane |
| q | Quit preview |
| CTRL+w z | Quit all preview modes |
| SHIFT+TAB | Switch to preview tab inorder to scroll |
╚══════════════════════════╩═════════════════════════════════════════╝

## 1.3. ZSH tricks

╔═══════════════════════════╦══════════════════════════════════════════════════════════════╗
| aliases | Desc |
╠═══════════════════════════╬══════════════════════════════════════════════════════════════╣
| | |
| **Escape Sequences** | |
| Esc-.(period) | Insert the last argument of the previous command line. |
| . | Repeat to retrieve arguments from earlier lines. |
| man -k randr | List all man pages that include a specific word. |
| look echo ~/.zshrc | Prints only the first word on the matching lines. |
| watch -n 3 ps -aux X | Prints only the first word on the matching lines. |
| stat -c '%n %a' ~/.zshrc | Provides information about the file with ═c you can specify |
| | which fields you want to show: %n name, %a access rights |
| | |
╠═╣ Shortcut keys ╠═════╬═════╣ |
| | |
| ctrl + h | Shows this file using vim |
| | |
╚═══════════════════════════╩══════════════════════════════════════════════════════════════╝

## 1.4. Custom aliases:

╔════════════════════════╦══════════════════════════════════════════════════════════════╗
| aliases | Desc |
╠════════════════════════╬══════════════════════════════════════════════════════════════╣
| **Help Pages** | |
| help | Displays this help page. |
| h | Grep history for a specific keyword |
| zdoc | Opens zsh pdf document. |
| **App Openers** | |
| idea | Opens a file or folder in IntelliJ Idea |
| subl | Opens a file or folder in sublime texteditor |
| atom | Opens a file or folder in atom texteditor |
| **Operations** | |
| ds | Calculates subfolder sizes in a directory |
| . | **EQ:** to 'du ═hd 1' |
| Make a file executable | |
| . | **EQ:** eq. to `chmod u+x` |
| rgrep | Search current folder for a specific keyword |
| . | including all subfolders |
| . | **Usage:** $ rgrep alias |
| . | **EQ:** `grep ══color=always ═R ═i "$1" ‖ less;` |
| rfind | |
| . | **Usage:** `$ rfind mac.sh` |
| . | **EQ:** `find . ═iname "*$1*" ‖ grep ═i "$1" ══color=always` |
| dq | query installed packages and list their files |
| **Usage:** $ dq ls | |
| extract | extracts a file into the destination folder using `tar` |
| . | **Usage:** `$ extract x.tar "/your/destination"` |
| . | **EQ:Usage:** `tar xf $1 ═C $2;` |
| **Web Search** | |
| google | Search Google for a specific term |
| ddg | Search DuckDuckGo for a specific term |
| ducky | Search DuckDuckGo for a specific term (I'm feeling lucky) |
| bing | Search Bing for a specific term |
| wiki | Search Wikipedia for a specific term |
| youtube | Search Youtube for a specific term |
| news | Search Google news for a specific term |
| map | Search Google maps for a specific term |
| image | Search images.google.com for a specific term |
╚════════════════════════╩══════════════════════════════════════════════════════════════╝

## 1.5. zsh shortcuts

╔════════════════════════╦══════════════════════════════════════════════════════════════╗
| Shortcuts | Desc |
╠════════════════════════╬══════════════════════════════════════════════════════════════╣
| ALT + h | Display help(info) on the first word of the line |
| | |
| ALT + . | Cycle through previous parameter in history |
| ALT + p | Cycle through previous statements |
| ALT + n | Cycle through next statements |
| | |
| ALT + f | Complete next word using previous statement/Jump to next wrd |
| ALT + b (+b) | Jump back one word |

| ESC + b (\eb) | Jump back one word |
| META + b (M-b) | Jump back one word |
| ALT + c | [fzf] Show fzf dropdown for all files in the current path |
| CTRL + x + b | Match bracket |
| | |
| Esc + v | Edit command line with vim ( Esacape then v ) |
| CTRL + x + e | Edit command line with vim ( ctrl + x then e ) |
| CTRL + grave | Edit command line with vim ( ctrl + `)` |
| | |
| ALT + SHIFT + r | Go to REPLACE mode |
| ALT + i | Go to INSERT mode |
| | |
| ALT + u | Change next word to upper case |
| ALT + l | Change next word to lower case |
| ALT + SHIFT + m | Insert return without executing |
| ALT + ' | Quote line |
| ALT + " | Quote region ( from start to cursor pos ) |
| | |
| ALT + d | Delete next word |
| CTRL + w | Delete pervious word |
| CTRL + k | Delete from cursor pos to the end of the line |
| CTRL + u or CTRL + _ | Delete the whole line |
| | |
| CTRL + e | Go to the end of the line |
| CTRL + a | Go to the begining of the line |
| CTRL + b | Backward delete char |
| CTRL + h | Backspace! |
| | |
| ALT + ? | Replace and execute `which` for the current starting cv .g |
| ALT + x | execute═named═cmd widget would be called |
| CTRL + j | Accept line |
| CTRL + m | Accept line |
| | |
╠═╣ Custom shortcuts ╠══╬═════╣ |
| | |
| | |
| ALT + s | Git status for the current folder |
| ALT + w | Switch to different theme |
| ALT + k | Kill the whole line |
| ALT + v | Edit the current line in vim |
| | |
╚════════════════════════╩══════════════════════════════════════════════════════════════╝

## 1.6. ZLE :

╔════════════════════════╦══════════════════════════════════════════════════════════════╗
| Commands | Desc |
╠════════════════════════╬══════════════════════════════════════════════════════════════╣
| zle -la | List all available widgets |
| bindkey | List all key mappings |
| bindkey -M vicmd | List all key mappings in vicmd mode |
| bindkey -v | V emulation mode |
| bindkey -e | Emacs emulation mode |
| | |
| bindkey '^m' | Shows a keybinding for a keymap in this case CTRL + m |
| bindkey -M viins 'b' | Shows a keybinding for Vi insert mode |
| bindkey -M vicmd 'b' | Shows a keybinding for Vi command line mode |
| bindkey -M emacs 'b' | Shows a keybinding for Emacs mode |
| | |
| '\e' | Stands for |

| '^' | Stands for |

| | |
╠════════════════════════╩════════════════════════╦═════════════════════════════════════╣
| bindkey -s '\es' '^Ugit status^M' | bind alt+s to git status |
| bindkey "^X^E" edit-command-line | bind c-x x-e to edit by vim (emacs)|
| bindkey "^X^E" edit-command-line | bind c-x x-e to edit by vim (emacs)|
| bindkey -M vicmd v edit-command-line | bind Esc-v to edit by vim (vimode) |
╠════════════════════════╦════════════════════════╩═════════════════════════════════════╣
| Esc-: | Shows execute named command prompt and you can run widgets |
╠════════════════════════╩══════════════════════════════════════════════════════════════╣
| https://github.com/zsh-users/zsh-completions/blob/master/zsh-completions-howto.org |
| |
| |
╚═══════════════════════════════════════════════════════════════════════════════════════╝

## 1.10.1 Other

╔════════════════════════╦══════════════════════════════════════════════════════════════╗
| Commands | Desc |
╠════════════════════════╬══════════════════════════════════════════════════════════════╣
| | |
| help | Displays this help page. |
| h | Grep history for a specific keyword |
| zdoc | Opens zsh pdf document. |
| mann | Opens https://manned.org manual page for the command |

| mank | Opens https://www.mankier.com manual page for the command |

╚════════════════════════╩══════════════════════════════════════════════════════════════╝

## 1.10.2 Useful manual pages

╔════════════════════════╦══════════════════════════════════════════════════════════════╗
| Commands | Desc |
╠════════════════════════╬══════════════════════════════════════════════════════════════╣
| | |
| mann zshexpn | Manual page for zsh expansions |
╚════════════════════════╩══════════════════════════════════════════════════════════════╝
```
* * *
Creation date: _2019-02-09_
