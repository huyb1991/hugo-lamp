# Guides

## Content Editing

### Add image to article

This is an AMP page, to add image, you have to use [amp-img shortcodes](https://github.com/huyb1991/hugo-lamp/blob/master/layouts/shortcodes/amp-img.html), the syntax is:
```
{{< amp-img width="width-value" height="height-value" layout="responsive" src="image-url" alt="image alt" >}}
```
Replace `width-value`, `height-value`, `image alt` and `image-url` by your image.

Note: Hugo is static-site-generator, to add image to your site, please follow this solution [[SOlved] How to… insert image in my post?](https://discourse.gohugo.io/t/solved-how-to-insert-image-in-my-post/1473)

### Content config for SEO

In Front Matter section for each post, you should add `title` and `description` for SEO, example:

```
---
title: "Getting Started with AMP"
description: "Getting started with AMP. Implement these key steps to get up and running with AMP"
---
```
The `title` is the H1 tag on HTML page, and `<title>` in head section.

The `description` is the meta tag for description `<meta name="description" content="">` in head section.

### Add icon

I changed from icon font to SVG for website follow [SVG symbol a Good Choice for Icons](https://css-tricks.com/svg-symbol-good-choice-icons/). Here's steps to add SVG icon to website.

1. Get SVG code (Eg: https://iconsvg.xyz/ or https://simpleicons.org/)
```
<svg xmlns="http://www.w3.org/2000/svg" style="display: none;" preserveAspectRatio="xMidYMid meet">
  <symbol id="icon-rss" viewBox="0 0 24 24">
    <title>RSS</title>
    <path d="M101.3 141.6v228.9h0.3 308.4 0.8V141.6H101.3zM375.7 167.8l-119.7 91.5 -119.6-91.5H375.7zM127.6 194.1l64.1 49.1 -64.1 64.1V194.1zM127.8 344.2l84.9-84.9 43.2 33.1 43-32.9 84.7 84.7L127.8 344.2 127.8 344.2zM384.4 307.8l-64.4-64.4 64.4-49.3V307.8z" />
  </symbol>
</svg>
```
Replace `SVG symbol id` by yourself (above is `icon-rss`)

2. Add this code into [layouts/partials/svg-icons.html](https://github.com/huyb1991/hugo-lamp/blob/master/layouts/partials/svg-icons.html)

3. Call icon name by `SVG symbol id` at you define above follow this syntax:
```html
<svg fill="currentColor"><use xlink:href="#icon-rss" /></svg>
```

Example for icon on [layouts/partials/social.html](https://github.com/huyb1991/hugo-lamp/blob/master/layouts/partials/social.html)

### Customize Theme

Use [yarn](https://yarnpkg.com/en/) to install and run script instead of `npm`, some people got problem when using `npm` (but not with `yarn`)

1. Install packages by `yarn install`
2. Run watch script to hot reload your change `yarn watch`


## Site Configuration

Take a look at [exampleSite - config.toml](https://github.com/huyb1991/hugo-lamp/blob/master/exampleSite/config.toml), and replace config value by your own:

### Site Info

```toml
# Base config for your site
baseURL = "http://localhost:1313/"      # Your domain
languageCode = "en-us"
title = "Hugo LAMP"                     # Default site title
theme = "hugo-lamp"
googleAnalytics = "UA-XXXXXXXX-X"       # Google Analytics UA number
```

### Main Menu

```toml
[[menu.main]]
  name = "Hugo"
  weight = 1
  identifier = "hugo"
  url = "/hugo/"
[[menu.main]]
  name = "AMP Project"
  weight = 2
  identifier = "amp"
  url = "/amp/"
[[menu.main]]
  name = "Tags"
  weight = 3
  identifier = "tags"
  url = "/tags/"
```

### Taxonomies

For more details, take a look on official document for [taxonomies](https://gohugo.io/content-management/taxonomies/)

```toml
[taxonomies]
  tag = "tags"
  category = "categories"
```

### SEO

```toml
[params]
  subtitle = "Light responsive AMP theme"
  author = "Huy Nguyen"                     # Your name
  logo = "/img/avatar.jpg"                  # Logo
  description = "A light responsive Hugo AMP theme for blogger"          # Meta description tag
  paginate = 10

  # SEO configs
  seotitle = "Hugo Blog Title (SEO Version)"                  # Overwrite site title for SEO purpose
  googleSiteVerification = "google_site_verification_code"    # Google Webmaster
  msValidate = "bing_site_verification_code"                  # Bing Webmaster
```

### Publisher

Currently only support Google Adsense as usual, maybe implement [amp-auto-ads](https://www.ampproject.org/docs/reference/components/amp-auto-ads) for future.

```toml
  # Google Adsense
  adsensePublisher = "ca-pub-XXX"       # Required if you want to include Google Adsense
  adsenseSlot = "XXX"                   # Required slot to display ads
  adsenseSlotSticky = "XXX"             # Enables sticky ads feature, value maybe the same with adsenseSlot, remove if you don't want display sticky ads
```

### Social Networks & Connections

```toml
  # Social networks
  email = "name@domain.com"
  github = "github_username"
  twitter = "twitter_username"
  linkedin = "linkedin_username"
  facebook = "facebook_username"
  google = "googleplus_id_number"
  instagram = "instagram_username"
  youtube = "youtube_username"
  dribbble = "dribbble_username"
```
