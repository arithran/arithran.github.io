---
layout: post
title:  "Configuring Tab and Spaces in Vi, Vim, Neovim, Macvim and others"
date:   2017-06-13 17:15:11 +0000
categories: TextEditor
image:  /preview.jpg
---

###1. Decide if you want tabs or spaces
If you want Vim to indent with tabs add the following to your config

	set noexpandtab " Don't expand a tab into spaces

If you use spaces instead of tabs add the following to your config

	set expandtab " Expand a tab into spaces

###2. Choose the width of your tab or spaces
If you selected tabs above, this will simply set the width of the tab to a
selected number of columns. If you selected spaces above, this will pretty much
add that many spaces. Add the following config to set your tabwith. Feel free to
change it to something other than 4 if desired.

	let s:tabwidth=4
	exec 'set tabstop='    .s:tabwidth
	exec 'set shiftwidth=' .s:tabwidth
	exec 'set softtabstop='.s:tabwidth

As a general rule `tabstop = shiftwidth = softtabstop`. Because of this, it's
best practice to create a variable (`s:tabwidth`) and assign the desired number
of columns your indentation will represent. 

These three variables are actually there to fine tune your editing. But them
being the same is fine for most people. Checkout the help pages to see how you
can set them to be different and use them in your work flow.

Check out my [Neovim config][ari-vimrc] if you want to see my settings. Pretty
much all the settings should work if you are using any Vim program

Check our my [dotfiles][ari-dotfiles] to see what programs and settings I currently run.

[ari-dotfiles]: https://github.com/arithran/dotfiles
[ari-vimrc]: https://github.com/arithran/dotfiles/blob/master/.config/nvim/init.vim
[vimcasts-url1]: http://vimcasts.org/episodes/tabs-and-spaces/
