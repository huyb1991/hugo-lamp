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

## Configuration

Take a look inside the [exampleSite](https://github.com/huyb1991/hugo-lamp/tree/master/exampleSite) at `config.toml` and update by your own:

```toml
# Base config for your site
baseURL = "your_domain"
languageCode = "en-us"
title = "Your site title"
theme = "hugo-lamp"
googleAnalytics = "UA-XXXXXXXX-X"

[params]
  subtitle = "Light responsive AMP theme"
  author = "Your name"
  avatar = "/img/avatar.jpg"            # Logo
  description = "Site description"      # Meta description tag
  paginate = 10

  # Google Adsense
  adsensePublisher = "ca-pub-XXX"
  adsenseSlot = "XXX"

  # SEO configs
  seotitle = "Hugo Blog Title (SEO Version)"
  googleSiteVerification = "google_site_verification_code"    # Google Webmaster
  msValidate = "bing_site_verification_code"                  # Bing Webmaster

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

[taxonomies]
  tag = "tags"
  category = "categories"

# Sidebar menu
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

## Contributing

If you found a bug or got an idea for a new feature feel free to add a new [issues](https://github.com/huyb1991/hugo-lamp/issues).

## Thanks
- [gohugo-amp](https://gohugo-amp.gohugohq.com/styling/) for the build tool
- [hugo-nuo](https://themes.gohugo.io/hugo-nuo/) for the template

Thanks to [Steve Francia](https://github.com/spf13) for creating [Hugo](https://gohugo.io/) and the awesome community around the project.
