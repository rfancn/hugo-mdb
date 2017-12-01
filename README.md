# hugo-mdb
Bootstrap material design them for Hugo, credits to:
- [Material Design for Bootstrap 4](https://mdbootstrap.com/)
- [Bootstrap](http://getbootstrap.com/)


# Configuration

## static resources
- css: 
  - head css: `head` value defined in config file under `params.css`, e,g:
    
        [params]
            [params.css]
                head = [
                    "https://cdn.bootcss.com/bootstrap/4.0.0-beta.2/css/bootstrap.min.css",
                    "https://cdn.bootcss.com/mdbootstrap/4.4.3/css/mdb.min.css",
                    "/css/style.css"
                ]
  
  - bottom css: `bottom` value defined in config file under `params.css`, e,g:
      
        [params]
            [params.css]
                bottom = [
                    "/css/bottom.css"
                ]

- javascript: 
  - head javascript: `head` value defined in config file under `params.Javascript`, e,g:
    
        [params]
            [params.javascript]
                head = [
                    "https://cdn.bootcss.com/jquery/3.2.1/xxx.min.js",
                    ...
                ]
  
  - bottom javascript: `bottom` value defined in config file under `params.Javascript`, e,g:
      
        [params]
            [params.javascript]
                bottom = [
                    "https://cdn.bootcss.com/jquery/3.2.1/jquery.min.js",
                    ...
                ]

## Home Page

- home recent posts
  - listSize: how many posts will be list there in homepage
  - truncateSize: how many words will be left when truncating them, it is based on language text, "zh" represents Chinext text, "en" represents English text

          [params.homeRecentPosts]
                  listSize = 12
                  [params.homeRecentPosts.truncateSize]
                      # for Chinese title
                      zh = 25
                      # for English Title
                      en = 63
                      
- home cards
  - img: image file the card will be used
  - link: url it links to when clicking "Read More..."
  - text: card's description
  - title: card's title
  
          [params.homeCards]
                  [[params.homeCards.card]]
                      img = "img/reading.jpg"
                      link = "/reading"
                      text = "HOME_CARD_READING_TEXT"
                      title = "HOME_CARD_READING_TITLE"
                  [[params.homeCards.card]]
                      img = "img/blog.jpg"
                      link = "/blog"
                      text = "HOME_CARD_BLOG_TEXT"
                      title = "HOME_CARD_BLOG_TITLE"
                  [[params.homeCards.card]]
                      img = "img/project.jpg"
                      link = "/project"
                      text = "HOME_CARD_PROJECT_TEXT"
                      title = "HOME_CARD_PROJECT_TITLE"

    > To get multilanguage support, you need add your own text/title translation in "i18n/<lang_code>.md"
    
## Google Adsense
You can define your own and just make sure below value are set, all extracted from google adsense codes

- style: required, google adsense style, 
- client: required, equals to "data-ad-client"
- slot: required, equals to "data-ad-slot"
- format: optional, equals to "data-ad-format"

There are 4 kinds of google adsense part predefined in current theme:

          [params.googleAdsense]
              [params.googleAdsense.banner]
                  style="xxx"
                  client="xxx"
                  slot="xxx"
              [params.googleAdsense.center]
                  style="display:block"
                  client="yyy"
                  slot="0123456789"
                  format="auto"
              [params.googleAdsense.sidebar]
                  ...
              [params.googleAdsense.link]
                  ...
