# Blog

# Development 

## Host machine

To run locally, the usual  ruby toolchain is required: gem, bundle:

> bundle && bundle exec jekyll serve --watch

## GNU Guix + Direnv

[GNU Guix](https://guix.gnu.org "A GNU Guix package and system manager") install all needed dependencies and [direnv](https://github.com/direnv/direnv "unclutter your .profile ") sets gem's home to a local folder.

> direnv allow

## Container

Just run something like the follow with your favorite container runner, be it `podman|docker|nerdctl`

``` sh
 podman run --name blog -v $PWD:/srv/jekyll -w /srv/jekyll -p 4000:4000 ruby sh -c 'bundle install && jekyll serve --watch --increment
al -H 0.0.0.0 --force_polling'
```

