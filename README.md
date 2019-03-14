# hugo-lamp

A light responsive [Hugo](https://gohugo.io/) [⚡ AMP](https://www.ampproject.org/) theme for blogger.

![hugo-lamp](/images/screenshot.png)

## Installation

Go to the directory where you have your Hugo site and run:

```bash
$ mkdir themes
$ cd themes
$ git clone https://github.com/huyb1991/hugo-lamp
$ rm -rf hugo-lamp/.git
```

*For more information read the official [setup guide](https://gohugo.io/overview/installing/) of Hugo.*

## Guide
### Add image to article (content)
This is an AMP page, to add image, you have to use [amp-img shortcodes](https://github.com/huyb1991/hugo-lamp/blob/master/layouts/shortcodes/amp-img.html), the syntax is:
```
{{< amp-img width="width-value" height="height-value" layout="responsive" src="image-url" alt="image alt" >}}
```
Replace `width-value`, `height-value`, `image alt` and `image-url` by your image.

A note: Hugo is static-site-generator, to add image to your site, please follow this solution [[SOlved] How to… insert image in my post?](https://discourse.gohugo.io/t/solved-how-to-insert-image-in-my-post/1473).

### Content config for SEO
In Front Matter section for each post, you should add `title` and `description` for SEO, example:
```toml
---
title: "Getting Started with AMP"
description: "Getting started with AMP. Implement these key steps to get up and running with AMP"
---
```
The `title` is the H1 tag on HTML page, and `<title>` in head section.
The `description` is the meta tag for description `<meta name="description" content="">` in head section.

## Contributing

If you found a bug or got an idea for a new feature feel free to add a new [issues](https://github.com/huyb1991/hugo-lamp/issues).

## Thanks
- [gohugo-amp](https://gohugo-amp.gohugohq.com/styling/) for the build tool
- [hugo-nuo](https://themes.gohugo.io/hugo-nuo/) for the template

Thanks to [Steve Francia](https://github.com/spf13) for creating [Hugo](https://gohugo.io/) and the awesome community around the project.
