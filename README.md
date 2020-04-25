Hexo-Theme-freemind.bithack
===

![screenshot](https://i.loli.net/2019/12/29/lIi6JXUCj45MGtk.png)

freemind.bithack modified by freemind.386 ,changed some color combination and font.
add support of valine comment.
Fixed a lot of bugs left by the original author.

* [Demo](http://ares-x.com)
* [Readme in Chinese](http://ares-x.com/2019/12/29/freemind-bithack-readme-zh/)

## Requirements ##

* Hexo >= 3.0
* [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) >= 0.0.8 (optional)
## Features ##

* **Bootstrap** - get the power of Twitter Bootstrap with minimal hassle;
* **Tag plugins** - luxuriant Bootstrap tag plugins, provided by [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap), including:
  - textcolor - a paragraph of text with specified color;
  - button - a button with target links, text and specified color;
  - label - a label with text and specified color;
  - badge - a badge with text;
  - alert - alert messages with text and specified color; 
* **Local Search Engine** - a build-in local search engine, with the help of [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search).

## Install ##

1) download theme:

``` sh
$ git clone git@github.com:Ares-X/hexo-theme-freemind.bithack
```

2) install [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) (*optional*):

``` sh
$ npm install hexo-tag-bootstrap --save
```

3) install [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search):

``` sh
$ npm install hexo-generator-search --save
```

4) install hexo-excerpt (need)

```sh
$ npm install hexo-excerpt --save
```


5) Create pages

freemind.bithack offers you the customized Categories, Tags and About pages. But you need to manually create these page at your 'source' folder.

For example, to create a `Categories` page, you may create a `index.html` file at `source/categories/` folder with the following contents:

```
title: Categories
layout: categories
---
```

Tags and About pages are created in a similar way, except that the layouts are `tags` and `page` respectively.

Alternatively you can create About page using the following command:

``` sh
$ hexo new page about
```

Note that only About page can be created in that way.
Remember to change `layout` on new page

## Enable ##

Modify `theme` setting in your `_config.yml` to `freemind.bithack`.


## Configuration ##

```
slogan: Yet another bootstrap theme.

menu:
  - title: Archives
    url: archives
    intro: All the articles.
    icon: fa fa-archive
  - title: Categories
    url: categories
    intro: All the categories.
    icon: fa fa-folder
  - title: Tags
    url: tags
    intro: All the tags.
    icon: fa fa-tags
  - title: About
    url: about
    intro: About me.
    icon: fa fa-user

links:
  - title: My Github
    url: http://www.github.com/blackshow
    intro: My Github account.
    icon: fa fa-github
  - title: My LinkedIn
    url: http://www.linkedin.com/in/blackshow
    intro: My Linkin account.
    icon: fa fa-linkedin

widgets:
- search
- category
- tagcloud
- recent_posts
- links

rss: atom.xml
favicon: favicon.png
fancybox: true

# analytics
google_analytics:
  enable: false
  siteid:

# Search
swiftype_key: 
#valine comment (change to yours)
# docs：https://valine.js.org/configuration.html
valine: 
  enable: true
  appid: ''
  appkey: ''
  placeholder: "提交评论时留下邮箱收到回复后将自动通知"
  visitor: true
  avatar: ''
  requiredFields: ['nick']

```


hexo config file(not theme config)：

```
category_generator:
  per_page: 0

tag_generator:
   per_page: 0
```


* **slogan** - slogan display at the index page
* **menu** - Navigation menu
* **links** - reference links at the links widget
* **widgets** - Widgets displaying in sidebar
* **rss** - RSS link
* **fancybox** - Enable [Fancybox](http://fancyapps.com/fancybox/)
* **valine** - Valine config, if you prefer to use Valine
* **analytics** - Analytics ID. Supports both Google Analytics and Baidu Tongji.
* **swiftype_key** - Swifttype key to enable local searching. Leave it blank or comment this line if you want to use build-in local search engine.

## copyright ##

edit it in `\layout\_partial\post\copyright.ejs`
```
<div class="article-footer-copyright">

    本博客采用 <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh" target="_blank">知识共享署名-非商业性使用-相同方式共享 4.0 国际许可协议(CC BY-NC-SA 4.0) 发布.
</div>

```
## Front-Matter ##

There are some new front-matter settings in freemind.bithack that you can use to decorate your articles.

* **description** - a short description about the articles that will be display at the top of the post
* **feature** - sets a feature image that will be show at the index page
* **toc** - renders a table of contents

For example:

```
title: Tag Plugins
date: 2014-03-16 10:17:16
tags: plugins
categories: Docs
description: Introduce tag plugins in freemind.
feature: images/tag-plugins/plugins.jpg
toc: true
---
```

## License ##

This theme is provided under [MIT License](http://opensource.org/licenses/MIT).


## Credits ##

* The theme is built based on [Freemind](http://wzpan.github.io/hexo-theme-freemind-blog/) and [BOOTSTRA.386](http://kristopolous.github.io/BOOTSTRA.386/);
* The beautiful icons are from [Font Awesome](http://fortawesome.github.io/Font-Awesome/icons/).
