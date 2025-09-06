# ohmyzsh-plugin

![main build](https://github.com/calmzhu/ohmyzsh-plugin-bookmark/actions/workflows/build.yml/badge.svg?branch=main)

## Description

Yet another ohmyzsh plugin to quick jump between cmdline directories.

And the design concern is very simple and intuitive.

    Add path to bookmarks, return an ordered number.
    and use the numbers to switch between dirs finally.

## Install
1. Ensure sed is already installed in you cmdline PATH,both GNU and BSD version sed are supported.
1. Ensure [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh) already installed.
1. Install plugin to ohmyzsh customer plugin dir.
    ```zsh
    curl -s https://raw.githubusercontent.com/calmzhu/ohmyzsh-plugin-bookmark/main/install.zsh >install.zsh
    zsh install.zsh $ZSH_CUSTOM
    ```
1. Add **bookmark** to the plugins array in your zshrc file.
    `plugins=(... bookmark)`.
1. Since alias conflicts, You must disable zsh default alias to use this plugin
```
# add follow line to .zshrc config
zstyle ':omz:lib:*' aliases no
```
## Usage

```bash
$ l -a ~ #Add home dir to bookmark
$ l -a /some/dir/path # Add /some/dir/path to bookmark
$ l -a `pwd` #Add current dir to bookmark
$ l # show current dir list
$ c 2 # switch to the 2rd dir in bookmark
$ l -d 2 # delete the 2rd dir from bookmark

```

