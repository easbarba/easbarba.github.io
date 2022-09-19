---
layout: post
title:  "Dot, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix Dotfiles Tools
---

Dotfiles, as implied by its nickname, are files named prepended with a
dot, that configure software initial settings and usually residies hidden on
`$HOME` directories.

Users craft their dotfiles through the years with a such a care that them
can easily be the most sensible and essential files in their system, 
version-controlling is a must, of course.

There is even a culture of proudly publicly sharing dotfiles, and that's
a good way to grab some cool snippets.

We all love how frugal and simple to use are the Linux tools as `find`, `grep` or `ls`, so
I kept that in mind on cooking up [Dot](https://github.com/easbarba/dot).

`Dot` creates links of all files in the target directory, perfectly mirroring them in the destination directory, `$HOME` by default:

{% highlight sh %}
dots --from /data/dotfile_folder --create
{% endhighlight %}

Of course you can just try it out first:

{% highlight sh %}
dots --from /data/dotfile_folder --pretend
{% endhighlight %}

To remove all linked files, it goes as:

{% highlight sh %}
dots -f /data/dotfile_folder --remove
{% endhighlight %}

It goes as easy to set a different destination:

{% highlight sh %}
dots -f /data/bin --to ~/.local/bin --create
{% endhighlight %}

We don't want that just every file to be linked, eg: `LICENSE`. For those files
you can pin out their location by feeding the `.dotsignore`, that follows docker's
`.dockerignore`.

Conflicting files found at the destination directory are moved up to `$HOME/.backup`.

And that is it. 

For more information, check the `README.md` in the main repository, or the `--help` option.

> PS: In case you are wondering what's with all those `main.*` files, as I pick
> a new language to learn, `Dot` is a good initial project as it
> offers a good set of challenges. 
>
> But I reckon that only the Ruby, Guile and Bash versions are fully functional. 
>
> With that said, pick your poison! :)
