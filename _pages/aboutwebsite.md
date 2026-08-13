---
title: "About this website"
layout: textlay
excerpt: "About this website."
sitemap: false
permalink: /aboutwebsite.html
---

# About this website

This website is powered by [Jekyll](https://jekyllrb.com) and uses some [Bootstrap](http://www.getbootstrap.com) and [Bootswatch](http://www.bootswatch.com), with [Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar) rendering the publication list from a BibTeX file.

The template was created by [Allan's Lab](https://www.allanlab.org) at Leiden University, and later adapted and refactored to use Jekyll Scholar by the [Uppsala Secure Learning and Control Lab](https://uslc-lab.github.io). We are grateful to both. Their code is released under the MIT License, and so is ours.

## How it is put together

Pages are written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and live in the `_pages` folder. Group members, news items and research themes are stored as plain-text `.yml` files in the `_data` folder, so they can be updated without touching any layout code. Publications live in `_bibliography/papers.bib` and are rendered automatically, so adding a paper means adding one BibTeX entry.

If you would like to use this template for your own group, start from [Allan's Lab](https://github.com/mpa139/allanlab) &mdash; that is the original, and it comes with proper documentation.
