---
layout: post
title:  "Presenting Dots, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix
---

Dotfiles...those freaking awesome and at time terrifying files are files, or
folders, configuring software, and one can even share and version-control to
easy, the monotonous routine of Distributions install.

I have tried all solutions all there, some too complicated, a few just perfect,
but I've nurturing that I could even simpler for the UNIX power-user.

I cooked up [Dots](https://github.com/easbarba/dot) with those goals.

You point the directory with all $HOME dotfiles and it symlink everything to
$HOME, its that simple:

{% highlight sh %}
dots --from /data/dotfile_folder --create
{% endhighlight %}

You can just peek on how it works: 

{% highlight sh %}
dots --from /data/dotfile_folder --pretend
{% endhighlight %}

and of course, clean everything:

{% highlight sh %}
dots --from /data/dotfile_folder --remove
{% endhighlight %}

Have a weird $HOME or just to symlink files in another directory:

{% highlight sh %}
dots --from /data/bin -to ~/.local/bin --create
{% endhighlight %}

If there are conflicting files at $HOME, those are backed up to $HOME/.backup.

In case you are wondering, what's with all those `main.*` files, I've tried a few ports
but only the Ruby, Java and Guile version are functional, pick your poison! :)
