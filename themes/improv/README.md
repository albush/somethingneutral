# Hugo Shows

This is a theme I'm building for improvisors to host a simple landing page to showcase their next upcoming show.

It was initially based off of my implementation of the [VEC theme](https://github.com/IvanChou/hugo-theme-vec/), for [Something Neutral Improv's site.](http://something.neutralimprov.com).

## Configuration

You can config your site's `config.toml` file like:

```
baseurl = "https://www.example.com"
title = "Site.title"
theme = "vec"
languageCode = "en-us"
paginate = 15

# Enable comments by entering your Disqus shortname
disqusShortname = "Your Disqus shortname"

# Enable analytics by entering your Google Analytics tracking ID
googleAnalytics = "Your Google Analytics tracking code"

[params]
  Keywords = "key, 关键字, キーワード"
  Description = "There are some words to describe your site"

  Avater = "img/avatar.jpg"
  SelfIntro = "Just a worm, seek for true, live in shadow, no more..."
  Email = "you@example.com"

  GithubID = "Your Github ID"
  TwitterID = "Your Twitter ID"
  FacebookID = "Your Facebook ID"
  LinkedInID = "Your LinkedIn ID"
  GoogleplusID = "Your Googleplus ID"

  [params.social]
        #github      = "your github profile"
        facebook        = ""
        facebook_admin  = ""  # This needs to be a page admin to get domain insights
        twitter     = ""
        twitter_domain  = "" # This domain shows in twitter cards as "View on `twitter_domain`"
        #googleplus      = ""
        instagram       = ""
        # youtube     = ""
        [params.authors]
        [params.authors.NAME] #replace with the name of the author as it will appear in frontmatter. Following params refer to each author.
        name          = ""
        thumbnail     = ""
        images        = [
                        "",
                      ]
        bio           = ""
        email         = ""

```

If you use `config.yaml`, plz reformat them to yaml.

### Enable Disqus to your post

1. Add your Disqus Shortname to the site config file;
2. You can enable Disqus per-post, by adding `comments: true` (YAML) or `comments = true` (TOML) in the front matter of your post. To disable it, you can either change the value to `false` or just not include `comments` variable and its value at all.

### Enable TOC to your post

If you need show table of contents per-post, adding `toc: true` (YAML) or `toc = true` (TOML) in the front matter of your post.

Please notice that TOC will be hidden when browser width is less than 920px.

## Build your site

Add `theme = "hugo-shows"` to your `config.toml`, then

```
# Build
hugo

# Run a server
hugo server
```
OR

```
hugo -t hugo-shows
hugo server -t hugo-shows
```


## License

Open sourced under [MIT license](https://github.com/albush/hugo-theme-shows/blob/master/license.md).
