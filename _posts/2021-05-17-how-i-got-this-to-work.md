---
tags: tech github-pages
category: misc
---

_The blog is being moved to blog.byemc.xyz, hosted on Tumblr._

Hello, and welcome to my brand-new, revamped website! Using [GitHub Pages](https://github.io), I've been hosting a small website for the last few months. However, I've been wanting to start a blog. For this, I'm going to use [Jekyll](https://jekyllrb.com). Jekyll lets you make dynamic websites. It's mainly used as a blogging tool, and Pages has internal support for it. 

This site uses a theme called [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy), but [GitHub Pages does not have support for more than a couple themes](https://docs.github.com/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll). So this is how I made a workaround

The tree for this site really looks like this:
```terminal
Z:\Websites\byemc.github.io>tree
Folder PATH listing for volume ProgrammingAndGames
Volume serial number is 1068-94FE
Z:.
├───.jekyll-cache
│   └───Jekyll
│       └──[...]
│               └───fe
├───assets
│   ├───css
│   ├───img
│   └───js
├───docs
├───gulpfile.js
│   └───tasks
├───stuff
│   ├───.github
│   └───old
├───tools
├───_data
├───_includes
├───_javascript
├───_layouts
├───_plugins
├───_posts
├───_sass
├───_site
│   ├───about
│   ├───archives
│   ├───assets
│   ├───categories
│   ├───norobots
│   ├───posts
│   │   └───how-i-got-this-to-work
│   ├───stuff
│   │   └───old
│   └───tags
└───_tabs

Z:\Websites\byemc.github.io>▮
```

But GitHub sees this:
```terminal
Z:\Websites\byemc.github.io\_site>tree
Folder PATH listing for volume ProgrammingAndGames
Volume serial number is 1068-94FE
Z:.
├───about
├───archives
├───assets
│   ├───css
│   ├───img
│   │   └───favicons
│   └───js
│       ├───data
│       ├───dist
│       └───lib
├───categories
├───norobots
├───posts
│   └───how-i-got-this-to-work
├───stuff
│   └───old
│       ├───shit
│       ├───spark
│       ├───webmaker
│       └───websitemaker
└───tags
    ├───github-pages
    └───tech

Z:\Websites\byemc.github.io\_site>
```

Why is this so? It's simply because I put the `.git` folder in `_site`, which means that Git (the program that GitHub runs on).

Unsatisfactory ending to something noone cares about. You're welcome (^///^)
