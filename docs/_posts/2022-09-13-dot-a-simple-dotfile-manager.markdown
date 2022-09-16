---
layout: post
title:  "Dot, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix
---

Dotfiles...

Those freaking awesome and at times terrifying little files. 

As the name implies, beginning with a dot, these files usually resides on `$HOME`
directory to configure software behavior.

One can share with friends, paste cool snippets and even version-control to
easy the tedious routine on newly installed distributions.

I have tried a fair lot of managers out there, some are just too complicated, some
damn fine, but it could be even simpler.

I cooked up [Dot](https://github.com/easbarba/dot) with those goals.

It creates links of all files in the target directory, perfectly mirroring in the `$HOME` directory by default, its that simple:

{% highlight sh %}
dots --from /data/dotfile_folder --create
{% endhighlight %}

Not sure yet, then just take a peek on how it works:

{% highlight sh %}
dots --from /data/dotfile_folder --pretend
{% endhighlight %}

You can of course remove all linked files:

{% highlight sh %}
dots -f /data/dotfile_folder --remove
{% endhighlight %}

 It goes as easy to set a different other destination than `$HOME`:

{% highlight sh %}
dots -f /data/bin --to ~/.local/bin --create
{% endhighlight %}

Not just every file is to be linked, for those you can pin out files to be ignored by feeding the `.dotsignore`, same syntax of .dockerignore. eg: `LICENSE`.

Conflicting files at destination are moved up to `$HOME/.backup`.

That is it. 

For more information check the `README.md` at the repository, or the `--help` option.

> PS: In case you are wondering what's with all those `main.*` files, as I pick
> a new language to learn `Dot` is a good initial project as any other, as it
> offers a good set of challenges. 
>
> But I reckon that only the Ruby, Java and Guile versions are fully functional. 
>
> With that said, pick your poison! :)
