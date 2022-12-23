Hexo-Theme-freemind.bithack
===

![screenshot](https://i.loli.net/2019/12/29/lIi6JXUCj45MGtk.png)

freemind.bithack modified by freemind.386 ,changed some color combination and font.
add support of Waline/Valine & Gitalk comment.
Fixed a lot of bugs left by the original author.

* [Demo](http://ares-x.com)
* [Readme in Chinese](http://ares-x.com/2019/12/29/freemind-bithack-readme-zh/)

## Requirements ##

* Hexo >= 3.0
* [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search)
* [hexo-excerpt](https://github.com/chekun/hexo-excerpt)(must)
* [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) >= 0.0.8 (optional)
## Features ##

* **Valine Comment Support**
* **Waline Comment Support**
* **Gitalk Comment Support**
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
$ git clone git@github.com:Ares-X/hexo-theme-freemind.bithack themes/freemind.bithack
```

2) install [hexo-tag-bootstrap](https://github.com/wzpan/hexo-tag-bootstrap) (*optional*):

``` sh
$ npm install hexo-tag-bootstrap --save
```

3) install [hexo-generator-search](https://github.com/paichyperiondev/hexo-generator-search):

``` sh
$ npm install hexo-generator-search --save
```

4) install hexo-excerpt (must)

```sh
$ npm install hexo-excerpt --save
```


5) Create pages

freemind.bithack offers you the customized Categories, Tags and About pages. But you need to manually create these page at your 'source' folder.

For example, to create a `Categories` page, you may create a `index.html` file at `source/categories/` folder with the following contents:

```yml
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

1) Modify `theme` setting in your hexo config file `_config.yml` to `freemind.bithack`.

2) Create theme config to hexo root dir via `cp themes/freemind.bithack/_config.yml ./_config.freemind.bithack.yml`

## Configuration ##

### Theme Config

**copy `_config.yml` from `hexo-theme-freemind.bithack` to your hexo root path and rename it as `_config.hexo-theme-freemind.bithack.yml`**

```yml
slogan: "wubba lubba dub dub."

show_heart: true

show_slogan: true

menu:
  - title: Archives
    url: archives
    intro: "All the articles."
    # icon: "fa fa-archive"
  - title: Categories
    url: categories
    intro: "All the categories."
    # icon: "fa fa-folder"
  - title: Tags
    url: tags
    intro: "All the tags."
    # icon: "fa fa-tags"
  - title: About
    url: about
    intro: "About me."
    # icon: "fa fa-user"
  - title: RSS
    url: atom.xml
    intro: "Subscribe me."
    # icon: "fa fa-user"

links:
  - title: hexo-theme-bithack
    url: https://github.com/Ares-X/hexo-theme-freemind.bithack
    intro: ""
    icon: false

  # - title: "My LinkedIn"
  #   url: http://www.linkedin.com/in/xxx
  #   intro: "My Linkin account."
  #   icon: "fa fa-linkedin"

widgets:
- search
- category
- tagcloud
- recent_posts
- links

rss: atom.xml
fancybox: true
favicon: favicon.png

# Analytics (change to yours)
google_analytics:
  enable: true
  siteid: UA-70812759-1


# search
#swiftype_key: ZP2ZSuHgipSZfRyU8uTR

#valine comment (change to yours)
# doc: https://valine.js.org/en/hexo.html
valine: 
  enable: false
  appId: 'xxx'
  appKey: 'xxx'
  placeholder: ""
  visitor: true
  avatar: 'monsterid'
  requiredFields: ['nick','mail']
  pageView: false
  
#waline comment (change to yours)
# doc: https://waline.js.org/
waline:
  enable: false
  serverURL: ''
  pageview: false
  lang: en
  dark: true
  requiredMeta: ['nick', 'mail']
  locale:
    placeholder: 'Comment with Email address will get notification when replied'
# gitalk comment (change to yours)
# doc: https://github.com/gitalk/gitalk
gitalk:
  enable: false
  clientID: ''
  clientSecret: ''
  repo: ''
  owner: ''
  admin: ['']
  id: location.pathname # It is recommended not to change
  distractionFreeMode: true
    
```

### Hexo Config

hexo config file(not theme config)：

```yml
# add this config to disable category and tag page split (must)
category_generator:
  per_page: 0

tag_generator:
   per_page: 0

# add this config if you want to change default excerpt lines (*optional*)
excerpt:
  depth: 10
  excerpt_excludes: []
  more_excludes: []
  hideWholePostExcerpts: true

# enable prismjs (*optional but suggest*)
highlight:
  enable: false
  line_number: true
  auto_detect: false
  tab_replace: ''
  wrap: true
  hljs: false
prismjs:
  enable: true
  preprocess: true
  line_number: true
  tab_replace: ''
```

* **slogan** - slogan display at the index page
* **menu** - Navigation menu
* **links** - reference links at the links widget
* **widgets** - Widgets displaying in sidebar
* **rss** - RSS link
* **fancybox** - Enable [Fancybox](http://fancyapps.com/fancybox/)
* **valine/waline/Gitalk** - Valine/Waline/Gitalk comment system config
* **analytics** - Analytics ID. Supports both Google Analytics and Baidu Tongji.
* **favicon** - create `favicon.png` on `hexo/source` can change the default logo.


## copyright ##

edit it in `\layout\_partial\post\copyright.ejs`
```html
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

```yml
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
