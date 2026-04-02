# How to
                            
## More info
https://jekyllrb.com/docs/

## How to build
```
bundle exec jekyll serve
```

## How to build site to ./_site

```
bundle exec jekyll build
```


## How to build site to other directory (need to rename to schedule)
     
First edit `_config.yml` and change `baseurl` to `/rwd-schedule` then

```
bundle exec jekyll build --destination rwd-schedule
```

## Changing styles

After changing styles needs to rebuild and commit `main.css`.

Run from `_sass` directory with `--force` flag (required to force recompilation):

```
cd _sass
bundle exec compass compile --force
```

Then commit `css/main.css`.

## Changing scripts (scripts.js)

The site loads `scripts.min.js`, not `scripts.js` directly. After changing `scripts.js` rebuild the minified version using Node/npx (requires Node.js):

```
npx --yes terser js/scripts.js -o js/scripts.min.js --compress --mangle
```

Then commit both `js/scripts.js` and `js/scripts.min.js`.