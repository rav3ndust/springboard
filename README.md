# Springboard

Bootstrap based Hugo startpage theme which provides out of the box best practices.
This theme is a fork of [Bootstrap-BP-hugo-startpage](), that will build on that original concept while providing some brand new functionalities and links, as well as changing the theme up.
Instead of rendering the items on-the-fly as in the startpage theme **Springboard** will generate a complete single page site.

## Install the theme

With Git installed, run the following commands inside the Hugo site folder. If Hugo has not yet been installed, read the setup guide [here](https://gohugo.io/overview/installing/).

```sh
mkdir themes
cd themes
git clone https://github.com/rav3ndust/springboard.git
```

You can get a zip of the latest version of the theme from the [home page](https://github.com/rav3ndust/springboard) and extract it to the themes folder.

## Theme settings

Most settings should be done with hugo specific variables. There are only a few (optional) additional `[params]`.

* `welcomeText = "Startpage!"` is the text above the search box
* `startPageColumns = true` will show the start page in grouped lists

Activate the search engine you want to use (or add a new one).

```toml
[[params.searchEngines]]
  name = "Google"
  activated = true
  url = "https://www.google.com/search"

[[params.searchEngines]]
  name = "DuckDuckGo"
  activated = true
  url = "https://duckduckgo.com/"

[[params.searchEngines]]
  name = "Bing"
  activated = true
  url = "https://www.bing.com/search"

[[params.searchEngines]]
  name = "Baidu"
  activated = true
  url = "https://baidu.com/"
  searchkey = "kw"
```

![startPageColumns = false](https://raw.githubusercontent.com/rav3ndust/springboard/master/images/screenshot.png)

![startPageColumns = true](https://raw.githubusercontent.com/rav3ndust/springboard/master/images/screenshot2.png)

Define the links in a file in `data/links.yml`. This needs to be structured like this.

```yml
---
- group: Social media
  items:
    - title: neighborli
      url: https://www.neighborli.xyz
      icon: fab fa-neighborli
    - title: Instagram
      url: https://www.instagram.com
      icon: fab fa-instagram
- group: Utilities
  items:
    - title: GitHub
      url: https://www.github.com
      icon: fab fa-github
```

Icons are taken from [Font Awesome](https://fontawesome.com/icons?d=gallery).

## Sources

* Background image by [Mikael Gustafsson](https://www.artstation.com/artwork/Y2Wew)

Inspired by:

* [Reddit - r/startpages](https://www.reddit.com/r/startpages/)
* [Github - 0-Tikaro - Minimum Viable Startpage](https://github.com/0-Tikaro/minimum-viable-startpage), Searchbox code
* [Github - ViktorKare - startpage](https://github.com/ViktorKare/startpage)
