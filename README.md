## Building

Use only:

```sh
bundle exec jekyll build
```

This will generate site folder with all the necessairy structure.
Copy files from `_site` folder to final repo that servers the blog.


**Don't** use:

```sh
bundle exec jekyll serve
```

because it will substitute `localhost` in url structure. Use it only for local testing.


File that may cause troubles:

Look for `src` and `jsonFile` attributes and add `/blog` to them:

`assets/js/scripts.min.js ` 

```js
i.setAttribute("src","/blog/assets/img/link-symbol.svg");
jsonFile:"/blog/search.json"
```


Config was changed to use baseurl and url variables:
_config.yml:

```yml
# Advanced Settings
baseurl: "/blog" # the subpath of your site, e.g. /blog
url: "https://arturwieczorek.github.io" # the base hostname & protocol for your site
```

## Wiki

This repo contains `wiki` directory with detailed instructions on customization and installation.
