---
title: "Hugo"
date: 2020-05-22T23:27:26-04:00
draft: false

weight: 1
---

## Components

[Hugo](https://gohugo.io/) is a tool that takes a layout template and generates a site from simple content files and the layout.

### Themes

Hugo has many layout themes available on the internet, most of which you can checkout in git. If you look at this project's theme,
you can see the [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) of the theme in the `themes` folder. This allows
including the git repository into this repository without actually storing any of the files. It also allows easy updates when the
submodule repository updates.

### Content

Hugo allows creating content in a simple format which is then built using the theme layout template into a full page.
Hugo uses markdown to write content. This allows super simple writing and formatting without having to constantly worry about getting all the HTML and styles correct.
Markdown also allows embedding HTML for situations where HTML is needed. Shortcodes can be used when some HTML will repeatedly be used.

### Shortcodes

Shortcodes are Hugo tools that allow inserting small templates of HTML into the page. Shortcodes can be used add complex styles or elements with a standard format.

Some examples include a youtube, tweet, or gist embed shortcodes.

## Using Hugo

Hugo has a few basic commands to create, build, and test-serve your pages.

* `hugo new site <name>` creates a new site with a skeleton of files
* `hugo new <path/file.md>` creates a new file, path starts in `content`
* `hugo server` builds the site in memory and serves it locally for testing
* `hugo --minify` builds the site to files (defaults to the `public` directory) and minifies the files
