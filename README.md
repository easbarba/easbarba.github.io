

# Container

``` sh
 podman run --name blog -v $PWD:/srv/jekyll -w /srv/jekyll -p 4000:4000 ruby sh -c 'bundle install && jekyll serve --watch --increment
al -H 0.0.0.0 --force_polling'
```

