offstage
========

OffStage provides a content-agnostic theme for bloggers, corporate-types and just about anyone else. If you're a musician or creative type, [Stage](https://github.com/noahlange/stage) might be a little more up your alley.

Built off the [SASS](http://sass-lang.com/) port of the [Twitter Bootstrap](http://getbootstrap.com/) framework, Stage features great typography, a responsive design, comprehensive options for social media, navbar links, author information and more.

While the Stage theme is heavily based off the excellent [Hugo Incorporated](https://github.com/nilproductions/hugo-incorporated) Hugo theme, in turns based off [Jekyll Incorporated](https://github.com/kippt/jekyll-incorporated), Stage has a few extra tricks up its sleeves.

# Content

OffStage comes pre-packaged with only two content type from Stage: the Media content type, which provides the means to create image or video galleries and Event, which provides the ability to create events with their own locations, which are rendered as Google maps.

# Presentation

## Images

OffStage features a full-page cover photo for the index and the option for large photos on node pages. With some help from [waypoint.js](http://imakewebthings.com/jquery-waypoints/), OffStage features  transparency effects for the navbar when transitioning between cover photos and regular content. There's also some [stellar.js](http://markdalgleish.com/projects/stellar.js/) for extra parallax effects.

The media content type allows for the creation of image galleries, dictated as an array in the front matter and rendered as a responsive grid. Clicking images summons a Bootstrap modal with the image.

## Bootstrap & SASS

For those interested in getting their hands dirty with styling, OffStage comes with a Compass gemfile  pre-included. All of the Bootstrap variables are fully customizable, including typefaces and colors.

Tables of Contents, when displayed via the "toc : 'true'" / "toc: true" flag in front matter, scroll alongside the viewport via Bootstrap's affix.js.

## Typefaces

By default, OffStage ships with Font Awesome, as well as the Lato typeface at weights 300, 500 and 700.

Somewhat less ubiquitous than Helvetica Neue, Lato is a superb typeface that's entirely at home in both casual and professional situations. If that's not to your liking, typefaces can be replaced with the fonts parameter in the config.yaml file, or added after a "|" character.

# Libraries & APIs

## Google Maps

Events can be given their own longitudes and latitudes and Google Maps will fetch a location map for the cover photo and a street view photograph for the sidebar photo. If you're expecting to have considerable traffic (10k+ API calls daily), it would be considerate to sign up for a Google Maps API key or disable this functionality via config.yaml.

# Configuration

There are a number of features bundled into the config file.

Navbar allows the user to customize the destination for the various links in the navbar, without having to edit the navbar directly. The same goes for social media links.

The default config.yaml file is as follows:

```
---
baseurl: "/"
theme: offstage
MetaDataFormat:	yaml
params:
 title: "(Off)Stage"
 subtitle: "A content-agnostic Hugo theme based on Stage."
 coverimage: "/images/stage.jpg"
 social:
   link: "/"
   website: "/"
   facebook: "http://facebook.com/"
   twitter: "http://twitter.com/"
   contact: "http://example.com"
 navbar:
   blog: "/post/"
   about: "/author/noahlange"
   events: "/event/"
 fonts: "Lato:300,500,700"
 maps: true
---
```

# Future

Since I'm using Stage for my own site, it's unlikely to be abandoned soon. So, that means there's more in store for OffStage than what's here just now.

- Replace waypoint.js with Bootstrap's scrollspy.
- Disqus and social sharing re-integration.
- More shortcodes for formatting things.
- Multi-author support.
- There are some legacy issues from this being built off Hugo Incorporated, including feeds apparently not working.
- When Hugo begins to support AJAX more natively, you can bet that a fixed player will appear.

Feel free to make pull requests with upgrades to OffStage at [GitHub](http://github.com/noahlange/offstage).

***

# Credits & Tech
* [Hugo](http://hugo.spf13.com)
* [jQuery](http://jquery.org)
* [Hugo Incorporated](https://github.com/nilproductions/hugo-incorporated)
* [Jekyll Incorporated](https://github.com/kippt/jekyll-incorporated)

## Images & Navigation
* [waypoint.js](http://imakewebthings.com/jquery-waypoints/)
* [stellar.js](http://markdalgleish.com/projects/stellar.js/)

## Markup and Styling
* [SASS](http://sass-lang.com/)
* [Compass](http://compass-style.org/)
* [Twitter Bootstrap](http://getbootstrap.com/)

## Maps
* [Google Maps](google.com/maps)
