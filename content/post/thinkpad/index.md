---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Linux + ThinkPad = ♥"
subtitle: "Showing my simple Debian config on a ThinkPad T480"
summary: ""
authors: [admin]
tags: ["linux", "ricing", "debian", "i3wm", "thinkpad"]
categories: []
date: 2020-08-01T17:20:03+02:00
lastmod: 2020-08-01T17:20:03+02:00
featured: false
draft: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

If you want to lurk other configs in the same style as mine take a look at the [masters](https://www.reddit.com/r/unixporn/).

# Software specifications

- **OS**: Debian GNU/Linux Testing
- **WM**: [i3wm](https://i3wm.org/)
- **Bar**: i3status
- **Theme**: [nord](https://github.com/arcticicestudio/nord)
- **Terminal**: [urxvt](https://wiki.archlinux.org/index.php/Rxvt-unicode)
- **Shell**: [zsh](https://www.zsh.org)
- **File Manager**: Nautilus (graphical), [ranger](https://ranger.github.io/) (terminal)
- **Launcher**: [rofi](https://github.com/davatorium/rofi)
- **Editor**: [VSCodium](https://vscodium.com/) (graphical), vim (terminal)
- **Browser**: Firefox
- **Mail**: Thunderbird

---

## i3wm

I'm using [i3-gaps](https://github.com/Airblader/i3) with [i3status](https://i3wm.org/i3status/manpage.html) for window managing and [lightdm](https://wiki.archlinux.org/index.php/LightDM) as display manager.


{{< figure src="screen_1.jpg" lightbox="true" >}}

My config is pretty simple, these are the main shortcuts I use:

Every key in this list is intented to be pressed along with `super` (in my case the Windows) key. For example if you want to launch a terminal you hold `super+enter`, if you want to move to workspace 2 you hold `super+2`.

- `enter`: new terminal
- `d`: launch rofi
- `f`: toggle fullscreen
- `w`: toggle tabbed layout
- `shift+q`: close focused window
- `[1-10]`: change workspace
- `shift+[1-10]`: move focused window to selected workspace
- `ctrl+right`: move to the next workspace
- `ctrl+left`: move to the previous workspace

I'm using fixed workspaces for certain apps, for example: if I want to launch Firefox I press `super+d` and then type or select Firefox from rofi. The Firefox window will be automatically launched in the second workspace, as I imposed i3wm to contain the browser windows there.

As you can notice from the previous screenshot I added an icon to every workspace (browser to the second, file manager to the third, etc.) and you will need [fontawesome](https://fontawesome.com/) installed to replicate that.

You can dig my i3 config [here](https://github.com/w00zie/dotfiles/blob/master/i3/config) and my i3status config [here](https://github.com/w00zie/dotfiles/blob/master/i3status/config).

If you want to know more about i3wm take a look at [this](https://www.youtube.com/watch?v=j1I63wGcvU4) or [this](https://www.youtube.com/watch?v=1tAFXThjzsY).

### Wallpaper (1920x1080)

{{< figure src="homer.jpg" lightbox="true" >}}

## Thunar

{{< figure src="screen2.jpg" lightbox="true" >}}

I'm using the [Equilux Compact](https://github.com/ddnexus/equilux-theme) theme with the [Numix](https://numixproject.github.io/) icon pack.

## URxvt & Bash

Take a look at my [.Xresources](https://github.com/w00zie/dotfiles/blob/master/.Xresources) and [.bashrc](https://github.com/w00zie/dotfiles/blob/master/.bashrc)

{{< figure src="screen3.jpg" lightbox="true" >}}

## Firefox

These are the extensions I use:

- [NoScript](https://noscript.net/)
- [uBlock Origin](https://github.com/gorhill/uBlock)
- [Cookie AutoDelete](https://addons.mozilla.org/it/firefox/addon/cookie-autodelete/)
- [Decentraleyes](https://addons.mozilla.org/it/firefox/addon/decentraleyes/)
- [HTTPS Everywhere](https://addons.mozilla.org/it/firefox/addon/https-everywhere/)
- [Link Cleaner](https://addons.mozilla.org/it/firefox/addon/link-cleaner/)
- [Privacy Badger](https://addons.mozilla.org/it/firefox/addon/privacy-badger17/?src=recommended)
- [Privacy Possum](https://addons.mozilla.org/it/firefox/addon/privacy-possum/)
- [Markdown Here](https://addons.mozilla.org/it/firefox/addon/markdown-here/) and sometimes [Mailvelope](https://www.mailvelope.com/en) for e-mails.

Plus I've tweaked a bit Firefox's own config, but maybe I'll talk about that in a post.

## Vim

{{< figure src="screen5.jpg" lightbox="true" >}}

I'm using a slightly modified version of this [config](https://github.com/amix/vimrc) (the *basic* one) for [my own](https://github.com/w00zie/dotfiles/blob/master/.vimrc) usage.

Plugins installed:
- [YouCompleteMe](https://github.com/ycm-core/YouCompleteMe)
- [fugitive.vim](https://github.com/tpope/vim-fugitive)
- [Tabular](https://github.com/godlygeek/tabular)
- [vim-markdown](https://github.com/plasticboy/vim-markdown)
- [NERD tree](https://github.com/scrooloose/nerdtree)
- [flake8](https://github.com/nvie/vim-flake8)



## Visual Studio Code

{{< figure src="screen4.jpg" lightbox="true" >}}


These are the extensions I've installed:
- [Remote](https://code.visualstudio.com/docs/remote/remote-overview) - this is a very nice feature if you want to remotely connect and edit files to an host without having to use vim. It may be one of the strongest reasons I'm using a Microsoft product in my system.
- Vim
- Haskell Syntax Highliting
- Markdown All in One
- Python
- C/C++
