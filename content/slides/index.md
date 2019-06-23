---
title: Embed Slides in Your Blog
author: ~
date: '2018-02-02'
slug: embed-slides-knitr-blogdown
categories: []
tags: []
description: How embed slides into your blogdown website with knitr 
draft: false
output:
  blogdown::html_page:
    toc: true 
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE, warning=FALSE, message=FALSE, 
                      results='show', cache=FALSE, autodep=FALSE)
```

## Introduction

It's [`rstudio::conf`](https://www.rstudio.com/conference/) time and I've seen a lot of great presentations shared on twitter. Unfortunately I couldn't come to the conference, but I thought I would do my part and write a short blog post on how to embed slideshows into a blog post. [Yihui Xie's](https://yihui.name/) knitr makes this very simple.

But why would you want to embed your slideshow?

1. An embedded slideshow makes it easier to talk about in a larger context.

2. You can show specific slides without taking screenshots.

3. You could place a series of plots into a slide deck and show them in your blog post. Instead of using vertical space, which is very difficult for the reader, this efficiently uses horizontal space and encourages the reader to explore the plots. 

## Embed in one line of code

Embedding a slideshow is easy. If it has a URL, you can embed with a single line of code:

```{r}
knitr::include_url('https://timmastny.rbind.io/slides/first_presentation#1')
```

Your entire presentation is now an HTML iframe embedded in your blog post. This means you can

- copy text and images
- advance slides
- click links

Basically anything you can normally do with your slideshow. 

To advance, simply click the slideshow and use the arrow keys to go forward or back. Or mouse over and scroll.

## Specific slides

If you'd like to embed a specific slide, just reference that slide in the url. For example, I'll change `#1` to `#2` in my url:

```{r}
knitr::include_url('https://timmastny.rbind.io/slides/first_presentation#2')
```

This is a great replcaement for screenshots, because if you need to edit your slides your blog post updates automatically.

## Upload your slideshow to your website

You'll notice that all my slides are hosted on my domain:
```{r, eval=FALSE}
https://timmastny.rbind.io
```

Your website is the perfect place to host your slides, and Yihui has a tutorial in the [blogdown bookdown](https://bookdown.org/yihui/blogdown/static-files.html) about how to include and build slideshows on your blogdown website.

Moreover, my slides are written with Rmarkdown and can execute R code. I recommend you check out [xaringan](https://github.com/yihui/xaringan), Yihui's R package for creating slideshows with Rmarkdown.

He also has a [slideshow tutorial](https://blogdown-static.yihui.name/slides/xaringan#1), but here is a quick summary:

1. Install [xaringan](https://github.com/yihui/xaringan).

2. Make a new slideshow with 
```{r, eval=FALSE}
File -> New File -> R Markdown -> From Template -> Ninja Presentation
```

3. Save it somewhere in the static directory of your website.

```{r, eval=FALSE}
static/slides/First_Presentation.html
```
This location will give your slideshow the following url:
```{eval=FALSE}
https://timmastny.rbind.io/slides/first_presentation#1
```

4. Assuming you are using the `blogdown::serve_site()` [workflow](https://bookdown.org/yihui/blogdown/rstudio-ide.html), you only need to change a few things to build your slides. First, create a new folder `R` at the top level of your website's directory that contains a script `build.R`:
```{r, eval=FALSE}
R/build.R
```
And `build.R` only needs one line:
```{r, eval=FALSE}
blogdown::build_dir("static")
```

Now you can write, build, and maintain your slideshows on your website!

## Future work

I'd like to be able to use a relative reference to the slideshow's HTML file in the `static/` directory, but I think `knitr::include_url()` requires a live URL. I'll have to do more research. 

I'm also investigating to see if I can trim the iframe so I only see the slides and not the gray bars on the side.

## Acknowledgements

This required so little work on my part, it is basically an undocumented feature of Yihui's blogdown. [Section 2.7](https://bookdown.org/yihui/blogdown/static-files.html) of the blogdown bookdown was very helpful, as well as his [example website](https://blogdown-static.yihui.name/). 

Shoutout to the the [Stackoverflow question](https://stackoverflow.com/a/45181338/6637133) that got me thinking about embedding slides, and pointed me to the [bookdown bookdown](https://bookdown.org/yihui/bookdown/web-pages-and-shiny-apps.html) section that explains `knitr::include_url()`. 


