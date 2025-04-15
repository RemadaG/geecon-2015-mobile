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