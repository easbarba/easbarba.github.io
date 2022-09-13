---
layout: post
title:  "Presenting Dots, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix
---

Dotfiles...

Those freaking awesome and at times terrifying little files. As the name
implies, dotfiles reside on $HOME directory configuring software behavior.

One can share with friends, paste cool snippets and even version-control them to
easy the tedious routine on newly installed distributions.

I have tried all solutions all there, some are just too complicated, a few just
perfect, but I've nurturing the thought that I could do something even simpler.

I cooked up [Dots](https://github.com/easbarba/dot) with those goals.

You point the source directory with the dotfiles and it symlinks everything
to $HOME, that simple:

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

For more information check the README.md at the repository.

> PS: In case you are wondering, what's with all those `main.*` files, as I pick
> a new language to learn, I reckon that Dots is a good initial project as it
> offers a rather large range of challenges. 
>
> But I reckon that only the Ruby, Java and Guile versionsare fully functional. 
>
> With that said, pick your poison! :)
