This is a simple, beautiful and swift theme for Jekyll. It's mobile first, fluidly responsive, and delightfully lightweight.

If you're completely new to Jekyll, I recommend checking out the documentation at <http://jekyllrb.com> or there's a tutorial by Smashing Magazine.

# Features

## Index page

The index page is seprated into several sections and they are located in `_includes/sections`,the configuration is in `_data/landing.yml` and section's detail configuration is in `_data/*.yml`.

### `_data/*.yml`

These files are used to dynamically render pages, so you almost don't have to edit *html files* to change your own theme, besides you can use `jekyll serve --watch` to reload changes.

The following is mapping between *yml files* to *sections*.

* landing.yml ==> index.html
* index/language.yml ==> index.html
* index/careers.yml  ==>  _includes/sections/career.html
* index/skills.yml  ==>  _includes/sections/skills.html
* index/projects.yml  ==>  _includes/sections/projects.html
* index/links.yml  ==>  _includes/sections/links.html

This *yml file* is about blog page navbar

* blog.yml ==> _includes/header.html

## Chart Skills

I use [Chart.js](http://www.chartjs.org/) to show skills, the type of skills' chart is radar, if you want to custom, please read document of Chart.js and edit **_includes/sections/skills.html** and **_data/index/skills.yml**.



## Pagination

The pagination in jekyll is not very perfect,so I use front-end web method you can refer to [jPages](http://luis-almeida.github.io/jPages).

## Page views counter

Many third party page counter platforms are too slow,so I count my website page view myself,the javascript file is [static/js/count.min.js](https://github.com/jarrekk/jalpc_jekyll_theme/blob/gh-pages/static/js/count.min.js) ([static/js/count.js](https://github.com/jarrekk/jalpc_jekyll_theme/blob/gh-pages/static/js/count.js)),the backend API is written with flask on [Vultr VPS](https://www.vultr.com/), detail code please see [ztool-backhend-mongo](https://github.com/Z-Tool/ztool-backhend-mongo).

## Multilingual Page

The landing page has multilingual support with the [i18next](http://i18next.com) plugin.

Languages are configured in the `_data/index/language.yml` file.

> Not everyone needs this feature, so I make it very easy to remove it, just clear content in file `_data/language.yml` and folder `static/locales/`.

About how to custom multilingual page, please see [wiki](https://github.com/jarrekk/Jalpc/wiki/Multilingual-Page).

## Web analytics

I use [Google analytics](https://www.google.com/analytics/) and [GrowingIO](https://www.growingio.com/) to do web analytics, you can choose either to realize it,just register a account and replace id in `_config.yml`.

## Comment

I use [Disqus](https://disqus.com/) to realize comment. You should set disqus_shortname and get public key and then, in `_config.yml`, edit the disqus value to enable Disqus.

## Share

I use [AddToAny](https://www.addtoany.com/) to share my blog on other social network platform. You can go to this website to custom your share buttons and paste code at `_includes/share.html`.

![share](https://github.com/jarrekk/Jalpc/raw/master/readme_files/share.png)

## Search engines

I use javascript to realize blog search,you can double click `Ctrl` or click the icon at lower right corner of the page,the detail you can got to this [repository](https://github.com/androiddevelop/jekyll-search). Just use it.

![search](https://github.com/jarrekk/Jalpc/raw/master/readme_files/search.gif)

## Compress CSS and JS files

All CSS and JS files are compressed at `/static/assets`.

I use [UglifyJS2](https://github.com/mishoo/UglifyJS2), [clean-css](https://github.com/jakubpawlowicz/clean-css) to compress CSS and JS files, customised CSS files are at `_sass` folder which is feature of [Jekyll](https://jekyllrb.com/docs/assets/). If you want to custom CSS and JS files, you need to do the following:

1. Install [NPM](https://github.com/npm/npm) then install **UglifyJS2** and **clean-css**: `npm install -g uglifyjs; npm install -g clean-css`, then run `npm install` at root dir of project.
2. Compress script is **build.js**
3. If you want to add or remove CSS/JS files, just edit **build/build.js** and **build/files.conf.js**, then run `npm run build` at root dir of project, link/src files will use new files.

OR

Edit CSS files at `_sass` folder.

# Put in a Jalpc Plug

If you want to give credit to the Jalpc theme with a link to my personal website <http://www.jarrekk.com>, that'd be awesome. No worries if you don't.

# Upgrading Jalpc

Jalpc is always being improved by its users, so sometimes one may need to upgrade.

## Ensure there's an upstream remote

If `git remote -v` doesn't have an upstream listed, you can do the following to add it:

```
git remote add upstream https://github.com/jarrekk/Jalpc.git
```

## Pull in the latest changes

```
git pull upstream gh-pages
```

There may be merge conflicts, so be sure to fix the files that git lists if they occur. That's it!

# Todo
- [ ] `jekyll server --watch` mode need to use original CSS/JS files
- [ ] User can customise index page's section title.
- [x] Non-github projects also have links.
- [ ] Add some custom color themes for selection(Nav bar, background, words, dominant hue).

# Donate Jalpc
If this project let you enjoy your blog time, you can give me a cup of coffee :)

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://paypal.me/jarrekk)

# Wiki

* [Multilingual Page](https://github.com/jarrekk/Jalpc/wiki/Multilingual-Page)
* [How to add posts](https://github.com/jarrekk/Jalpc/wiki/How-to-add-posts)
* [Change Log](https://github.com/jarrekk/Jalpc/wiki/Change-Log)
* [Contributors](https://github.com/jarrekk/Jalpc/wiki/Contributors)
* [Thanks to the following](https://github.com/jarrekk/Jalpc/wiki/Thanks-to-the-following)

# Ad
[Jalpc-A](https://github.com/Jack614/Jalpc-A): another Jekyll theme written by [AngularJS](https://angularjs.org/).

