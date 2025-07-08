
https://desmount.github.io


### Local dev

Build _site
```
podman run --rm \
    -v "$(pwd):/srv/jekyll" \
    jekyll-site \ 
    jekyll build
```

Serve at http://localhost:4000
```
podman run --rm -it \
    -p 4000:4000 \
    -v "$(pwd):/srv/jekyll" \
    jekyll-site \
    jekyll serve --host 0.0.0.0
```

Config override option for serve
```
jekyll serve --host 0.0.0.0 --config "_config.yml,_config.local.yml"
```