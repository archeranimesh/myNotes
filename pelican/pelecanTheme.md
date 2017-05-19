

* Automatic file header.
* [FileHeader](https://github.com/shiyanhui/FileHeader)
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
* pelican -d to clean and build pelican., does not delete the .git if OUTPUT_RETENTION = [".hg", ".git", "CNAME"] is defined.


## Reference ##

* [clean should not remove .git metadata #574 ](https://github.com/getpelican/pelican/issues/574 "clean should not remove .git metadata #574")
