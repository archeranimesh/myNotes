# Integrating Elegant theme with my pelican blog. #

`git submodule add https://github.com/getpelican/pelican-themes.git themes`
`git submodule update --init --recursive`

`git submodule add https://github.com/getpelican/pelican-plugins.git plugin`

THEME = 'themes/elegant'

http://kb.mailchimp.com/lists/signup-forms/host-your-own-signup-forms

https://github.com/talha131/onCrashReboot/blob/master/pelicanconf.py

## Search ##

PLUGIN_PATHS should be used in place of PLUGIN_PATH

* SiteMap.
    - https://github.com/getpelican/pelican-plugins/tree/master/sitemap
    - /home/animeshb/myWork/pelicanBlog/output/sitemap.xml
* Tipue Search
    - Tipue Search requires BeautifulSoup.
    - works only after 
        + DIRECT_TEMPLATES = (('index', 'tags', 'categories', 'archives', 'search', '404'))
    - Search results come, but with undefined links
        + https://github.com/talha131/pelican-elegant/issues/147
        + http://moparx.com/2014/04/adding-search-capabilities-within-your-pelican-powered-site-using-tipue-search/



## Reference ##

* [Elegent Theme](http://oncrashreboot.com/elegant-best-pelican-theme-features)

