---
layout: post
title:  "Dot, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix
---

Dotfiles...

Those freaking awesome and at times terrifying little files. 

As the name implies, named beginning with a dot, and usually residing on `$HOME`
directory to configure software behavior.

One can share with friends, paste cool snippets and even version-control to
easy the tedious routine on newly installed distributions.

I have tried a lot of managers out there, some are just too complicated, some
damn good, but I've got the feeling that it could be even simpler.

I cooked up [Dot](https://github.com/easbarba/dot) with those goals.

All files in the pointed target directory are linked to `$HOME` by default, its that simple:

{% highlight sh %}
dots --from /data/dotfile_folder --create
{% endhighlight %}

Just want to peek on how it works?

{% highlight sh %}
dots --from /data/dotfile_folder --pretend
{% endhighlight %}

and of course, cleaning everything:

{% highlight sh %}
dots -f /data/dotfile_folder --remove
{% endhighlight %}

Your `$HOME` ain't after its user name? or you just want to link files in another
directory, it goes as easy:

{% highlight sh %}
dots -f /data/bin --to ~/.local/bin --create
{% endhighlight %}

If a `.dotsignore` is present, `Dot` ignores all listed files. eg: `LICENSE`.

Conflicting files at TO are backed up to `$HOME/.backup`.

That is it. 

For more information check the `README.md` at the repository, or the `--help` option.

> PS: In case you are wondering what's with all those `main.*` files, as I pick
> a new language to learn `Dot` is a good initial project as any other, as it
> offers a rather large range of challenges. 
>
> But I reckon that only the Ruby, Java and Guile versions are fully functional. 
>
> With that said, pick your poison! :)
