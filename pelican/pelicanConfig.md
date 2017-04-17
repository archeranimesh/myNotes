 # Understand different Pelican Config #

 

 ## DISPLAY_PAGES_ON_MENU ##
 If we have a seperate folder for "Pages", which will store the static content, by default `DISPLAY_PAGES_ON_MENU` is set to `True`, which means that we will display those pages on the menu header of the website.

### status: hidden ###
 This can be given in both `pages` and individual `article`, it will basicaly hide that particular item from processing.
 This is part of the metadata of the file.



 ## Linking ##

 Linking is very important in any HTNL. All the content which has to be linked has to be present inside the `content` folder.

 Be it the `pages` or the `images` folders. `pages` is a special folder inside `content` as the pages inside this folder are consider static and do not change much, such as `About` or `contact`

 ## Paths ##

 Lot of configuration is present for Paths.

 * `STATIC_PATHS`
     - It is given in `pelicanconfig.py`, as `STATIC_PATHS = ['images']`, so if there is a `images` folder inside the `content` it will be copied as is to the `output` folders.
 * `PAGE_PATHS`
     - The default `PAGE_PATH` points to `pages` directory inside content, if we specify `PAGE_PATHS = ['myPages', 'newPage']` the we can have two directory inside `content` with the name `myPages` and `newPage`, and both of their content will be copied into a single folder in the `output` with the name `pages`
     - The idea behind "pages" is that they are usually not temporal in nature and are used for content that does not change very often (e.g., “About” or “Contact” pages).

 * `ARTICLE_PATHS`
     - By default we write out content inside the `content` directory, if we want all the articles to be present inside one directory, then we can configure `ARTICLE_PATHS = ['articles',]` and this will help in making all the article inside `articles` directory as the blog content.
     - Pelican considers "articles" to be chronological content, such as posts on a blog, and thus associated with a date.

## PATHS, URL, SAVE_AS ##

We have a lot of configuration, which will end with `*_PATHS`, `*_URL`, `*_SAVE_AS`, we will take an example of `ARTICLE` to explain the above.

* `ARTICLE_PATHS`: As described above, we can specify the source path of the Markdown or rst file inside the `content` directory. This is done to group all the blogs or post in one place.
* `ARTICLE_URL`: We can specify it like `articles/{slug}.html'`, now what this means is to url or the article can be referenced in this manner, this only works if we have specified the `ARTICLE_SAVE_AS` configuration, else this setting is meaning less.
* `ARTICLE_SAVE_AS` : This configuration tells us where our output file for a particular article will be generated, default is the top level hierarchy, if we specify it as `articles/{slug}.html`, then the output html will be put inside the `output/articles` folder. If we change this configuration we also have to change the `ARTICLE_URL` so as to find the correct file.

Similarly we can have configuration variation for all `PAGE`, `STATIC`.

## Drafts ##

If we do not want to publish a post without review, we can have a default configuration in `pelicanconf.py` so that by default evey article will have `draft` status.

```
DEFAULT_METADATA = {
    'status': 'draft',
}
```

Once the review is complete we can change the individual post status to `published`


## Reference ##

* [Pelican Configuration for ReachTim.com](http://reachtim.com/articles/pelican-configuration-for-reachtimcom.html)
* [Generate a Static Company Site and Blog with Pelican and Jinja](https://disqus.com/by/pemoseley/)
    - Best Description of the Article URLs etc.
* 

 
 
 