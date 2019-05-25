jounileino.com
========

A blog built with Jekyll.


Build
```bash
$ bundle exec jekyll build
```


Run locally

```bash
$ bundle exec jekyll serve
```

http://127.0.0.1:4000


Sync static website from directory _site to s3 bucket
```bash
$ aws s3 sync ./_site s3://jounileino.com
```


