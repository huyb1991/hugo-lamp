# Guide

## Add image to article (content)

This is an AMP page, to add image, you have to use [amp-img shortcodes](https://github.com/huyb1991/hugo-lamp/blob/master/layouts/shortcodes/amp-img.html), the syntax is:
```
{{< amp-img width="width-value" height="height-value" layout="responsive" src="image-url" alt="image alt" >}}
```
Replace `width-value`, `height-value`, `image alt` and `image-url` by your image.

A note: Hugo is static-site-generator, to add image to your site, please follow this solution [[SOlved] How to… insert image in my post?](https://discourse.gohugo.io/t/solved-how-to-insert-image-in-my-post/1473).

## Content config for SEO

In Front Matter section for each post, you should add `title` and `description` for SEO, example:
```toml
---
title: "Getting Started with AMP"
description: "Getting started with AMP. Implement these key steps to get up and running with AMP"
---
```
The `title` is the H1 tag on HTML page, and `<title>` in head section.
The `description` is the meta tag for description `<meta name="description" content="">` in head section.
