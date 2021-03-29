---
layout: post
title:  symbolic links
date: 2021-03-09 00:00:00
description: using symbolic links in linux
---

Today I'm messing with a bunch of stuff... my neovim configurations and my dotfiles repository that I'm just starting to put together.

I decided to create this post on symbolic links because they are interesting, powerful, they don't exist on windows I believe (maybe they do) and they can make you destroy your computer.

My first encounter with symbolic links was some weeks ago. I discovered them in the most stupid way. But I'm not going to tell that story, I'm just going to say that I needed to format my computer. Don't mess with `usr/bin` btw.

I'm writing this post now because I'm currently using symbolic links to create my *dotfiles* repository.

Simple:
- I create a `dotfiles` directory somewhere in the disk
- I make that directory a git repository
- I dump all my configuration files in there (i.e. `.bashrc, .vimrc, and so on`)

The thing is that those configuration files are expected to be on their respective places, not on my `dotfiles` directory. That's where symbolic (symlinks) links comes in:

It is possible to redirect files and folders to others places with these links.

For instance, I need to have my file `.bashrc` in my `$HOME` directory in order for bash to find it and apply the configurations. But if I have that file in my *dotfiles* directory, bash can't find it. So... We create a symbolic link:

`ln -s $HOME/dotfiles/.bashrc $HOME/.bashrc`

The command above will create in `$HOME` a symbolic link named `.bashrc` that is a link (not a file with contents) to the actual file `.bashrc` which is in `$HOME/dotfiles`.
It's like portals.

This way I can have all of my configuration files in my `$HOME/dotfiles` directory, and simply create symbolic links where they are expected to be. All of this to make a repository with all of them.
