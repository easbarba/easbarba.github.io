---
layout: post
title:  "Easily upgrading to the Debian SID distribution"
date:   2022-09-21
categories: Debian Linux Apt
---

Developers usually stick with the latest version of the shiniest software out there,
be it editors, browsers, stream players and office tools.

Some Linux Distributions are famous for its rolling-release model with all
bleeding-edge/night packages in the main repo, that goes for Arch, Manjaro, Nix.

Not as famous as those there is a distribution of Debian named by SID, with all
unstable packages, meaning packages not as tested as those in the Stable branch.

Do not be confused by its name, it has a as solid experience of Arch, but with the
advantage of having all `.deb` packages that most companies and OSS developers
always target.

Upgrading from Stable, or Testing, is about changing one word, its nickname if you will - 
`bullseye`, in the `/etc/apt/source.list` file, from this:

 ```conf
deb http://deb.debian.org/debian/ bullseye main contrib non-free
deb-src http://deb.debian.org/debian/ bullseye main contrib non-free
```

To:

 ```conf
deb http://deb.debian.org/debian/ sid main contrib non-free
deb-src http://deb.debian.org/debian/ sid main contrib non-free
```

From there on, prepare yourself for one big upgrade of all packages installed with:

`sudo apt update && sudo apt dist-upgrade`

There is only one catch on the SID distribution, as Debian changes from one big version to a new one, usually 2 years, there will be a whole month that most packages are frozen, and you may not receive any update.

Usually I just go distro-hopping for the shiniest and newest Distros, and after that, I go back to my beloved Debian in its  newest version.

Nonetheless, do not frail from moving up to SID, it's rather worth effort.



