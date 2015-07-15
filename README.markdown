Dotfiles
========
This repository is a fork of https://github.com/michaeljsmalley/dotfiles.
I've made several modifcations to the original as I liked the script he used in
order to replicate his dotfiles. I do not use oh-my-zsh but prezto and use the
very opinionated spf13-vim dotrepo for vim as it is much easier for me to remove
those addons that I don't use than add all the work that Steve Francia has done
on spf13. I include all the dotlocal files that have my customizations in them.

TODO update the laptop files (thoughbot for OSX) and add things like brew for mac
and add checks for vim versions as spf13 needs an updated vim on OSX. I also need
to check for tmux installations.

Michael's original Instructions below
------------

They should be cloned to your home directory so that the path is `~/dotfiles/`.  The included setup
script creates symlinks from your home directory to the files which are located
in `~/dotfiles/`.

The setup script is smart enough to back up your existing dotfiles into a
`~/dotfiles_old/` directory if you already have any dotfiles of the same name as
the dotfile symlinks being created in your home directory.

I also prefer `zsh` as my shell of choice.  As such, the setup script will also
clone the `oh-my-zsh` repository from my GitHub. It then checks to see if `zsh`
is installed.  If `zsh` is installed, and it is not already configured as the
default shell, the setup script will execute a `chsh -s $(which zsh)`.  This
changes the default shell to zsh, and takes effect as soon as a new zsh is
spawned or on next login.

So, to recap, the install script will:

1. Back up any existing dotfiles in your home directory to `~/dotfiles_old/`
2. Create symlinks to the dotfiles in `~/dotfiles/` in your home directory
3. Clone the `oh-my-zsh` repository from my GitHub (for use with `zsh`)
4. Check to see if `zsh` is installed, if it isn't, try to install it.
5. If zsh is installed, run a `chsh -s` to set it as the default shell.

Installation
------------

``` bash
git clone git://github.com/michaeljsmalley/dotfiles ~/dotfiles
cd ~/dotfiles
./makesymlinks.sh
```
