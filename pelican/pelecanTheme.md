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
* TOC.
    - [TOC]
    - MD_EXTENSIONS = (['toc'])
    - https://github.com/getpelican/pelican-plugins/tree/master/extract_toc
    - `MD_EXTENSIONS = ['codehilite(css_class=highlight)', 'extra', 'headerid',
                'toc(permalink=true)']`
    - TO `'markdown.extensions.toc' :{'permalink' : 'true'},`

* Automatic file header.
    - Sublime Text - File Header.
        + [Gist | Markdown TMPL](https://gist.github.com/archeranimesh/dcd1773af0ad41e9e1572d293becaa87)
        + Settings
````
{
    "custom_template_header_path": "/home/<username>/.config/sublime-text-2/Packages/User/fileHeaderTemplatesUser",
    "Default": {
        "author": "XYZ ABC"
    }
    
}
````



## Reference ##

* [Elegent Theme](http://oncrashreboot.com/elegant-best-pelican-theme-features)

