---
layout: post
title:  "Configuring Tab widths in VI, VIM, NEOVIM"
date:   2017-06-13 17:15:11 +0000
categories: vi,vim,neovim
image:  /preview.jpg
---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.


	" Set the tab width
	let s:tabwidth=4
	exec 'set tabstop='    .s:tabwidth
	exec 'set shiftwidth=' .s:tabwidth
	exec 'set softtabstop='.s:tabwidth

Check out my [dotfiles][ari-dotfiles] for more info on how to get the most out of Vim.

[ari-dotfiles]: https://github.com/arithran/dotfiles
[vimcasts-url1]: http://vimcasts.org/episodes/tabs-and-spaces/
