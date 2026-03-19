# still

**still** is a minimal Zola theme for personal blogs, essays, and long-form writing.

It defaults to a simple reading layout:

* the homepage can show an intro and a post list together
* section pages list posts without extra chrome
* post pages stay focused on typography and content

## Features

* Minimal monochrome presentation
* Homepage intro plus post listing by default
* Section index pages with consistent date formatting
* Optional author signature in post footers
* Light and dark color-scheme support

## Installation

Create a Zola site first:

```bash
zola init myblog
cd myblog
```

Add the theme under `themes/still`:

```bash
git submodule add https://github.com/wjianbo/zola-theme-still themes/still
```

Then enable it in your site config:

```toml
theme = "still"
compile_sass = true
build_search_index = false
```

## Configuration

These optional values can be set in your site `config.toml`:

```toml
title = "My Blog"
default_language = "en"

[extra]
still_date_format = "%Y-%m-%d"
still_show_author = true
```

Notes:

* `default_language` controls the HTML `lang` attribute
* `still_date_format` is used on the homepage, section pages, and post pages
* `still_show_author` hides or shows the footer signature when `author` is set

## Content model

For the homepage, put introductory copy in `content/_index.md`. The theme will render that intro first and then list pages from the root section underneath it.

For posts, use dated pages under a section such as `content/posts/`.

## Philosophy

This theme aims to remove structural noise without removing the basic affordances a blog still needs:

* a clear homepage entry point
* predictable navigation back to section or home
* stable typography across reading contexts
