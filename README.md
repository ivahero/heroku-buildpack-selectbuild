heroku-buildpack-selectbuild
============================

## Usage

This buildpack lets you customize e.g. which Procfile Heroku runs. It searches a directory given by `$SELECTBUILD_DIR` for files named Procfile, Aptfile, requirements.txt, scrapy.cfg and if found copies them to the build root.  Use with [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi).

```
$ heroku config:set BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
$ heroku config:set SELECTBUILD_DIR=config/prod
$ ls config/prod
Procfile
requirements.txt

$ cat .buildpacks
https://github.com/cantino/heroku-buildpack-selectbuild.git
https://github.com/heroku/heroku-buildpack-python.git
```
