# bash-kaomoji
simple bash script that outputs a random kaomoji from the *kaomoji.txt* file

kaomoji list was pulled from [here](https://github.com/Aptivi-Analytics/KaomojiList)

## how to use
just run `bash kaomoji.sh` to echo a random kaomoji

![example](https://raw.githubusercontent.com/antoine-was-unavailable/bash-kaomoji/refs/heads/main/example.png)

add `-r` for a random color or `-p=/PATH/TO/ANOTHER/FILE.TXT` to use another source file

## options
    -h, --help              Display this message
    -r                      Output with a random terminal color
    -p=PATH, --path=PATH    Change the emoji file

## what for

i made this in order to have a fabulous bash prompt as shown on the screenshot

in case you're curious, here is the chonker i use to make it my bash prompt `.bashrc`:
```sh
FOLDER_BG=105
FOLDER_PRE_BG=$(($FOLDER_BG - 10))

PS1='• \[\e[$((31 + $RANDOM % 7 + ( $RANDOM % 2 * 60 )))m\] $(bash $HOME/.dotfiles/kaomoji.sh -p=$HOME/.dotfiles/kaomoji.txt) \[\e[0m\] ✿  \[\e[${FOLDER_PRE_BG}m\]\[\e[${FOLDER_BG}m\] \[\e[93m\] /\W \[\e[0m\]\[\e[${FOLDER_PRE_BG}m\] \[\e[91m\]>\[\e[0m\] '
```
