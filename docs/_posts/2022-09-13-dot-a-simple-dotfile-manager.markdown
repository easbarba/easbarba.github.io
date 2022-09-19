---
layout: post
title:  "Dot, yet another simple dotfile manager!"
date:   2022-09-13 01:53:10 +0000
categories: Unix
---

Dotfiles, as implied by its nickname, are files named beginning with a dot, that usually resides hidden on `$HOME` directory to configure software initial settings.

One can share them, paste cool snippets and even version-control to easy the
tedious routine on newly installed distributions.

I did try a fair lot of dotfiles managers out there, some are just too
complicate, other's damn fine, but could not it to be simpler?

I cooked up [Dot](https://github.com/easbarba/dot) with such goals in mind.

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
