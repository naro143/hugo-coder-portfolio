---------------------------
This theme is created based on [hugo-coder](https://github.com/luizdepra/hugo-coder).  
I made it possible to tell yourself more by my change.   
Please see [FeaturesOfCoderPortfolio](https://github.com/naro143/hugo-coder-portfolio/blob/master/exampleSite/content/posts/FeaturesOfCoderPortfolio.md) in the post about the change.
Have questions or suggestions? Feel free to [open an issue on GitHub](https://github.com/naro143/hugo-coder-portfolio/issues/new) or [ask me on Twitter](https://twitter.com/naro143).

---------------------------

A simple and clean blog theme for Hugo.

![](https://github.com/naro143/hugo-coder-portfolio/blob/master/images/screenshot.png)

## How to use this theme

To use `hugo-coder-portfolio` go through the following steps.

### Download

Clone this repository into your Hugo project.

```
git clone https://github.com/naro143/hugo-coder-portfolio themes/coder-portfolio
```

### Configuration

Add the following lines to your `config.toml`.

```toml
baseurl = "http://www.example.com" # Hostname (and path) to the root.
title = "Yusuke Ishimi" # Site title.
theme = "coder-portfolio" # Set the theme.
languagecode = "en" # The site’s language code used to generate RSS.
defaultcontentlanguage = "en" # The default content language.

paginate = 20 # Default number of pages per page in pagination.

pygmentsstyle = "b2" # Color-theme or style for syntax highlighting.
pygmentscodefences = true # Enable code fence background highlighting.
pygmentscodefencesguesssyntax = true # Enable syntax guessing for code fences without specified language.
pygmentsUseClasses = true # new add

disqusShortname = "yourdiscussshortname" # Enable or disable Disqus.

[params] # theme parameters
    author = "Yusuke Ishimi" # Author's name.
    info = "WEB AND APPS ENGINEER" # Author's job title or info.
    description = "Yusuke Ishimi's personal website" # Site description.
    keywords = "blog,developer,personal" # Site keywords.
    avatarurl = "images/avatar.jpg" # Contain the path of the optionnal avatar in the static folder.

    footercontent = "Enter a text here." # Add footer content
    fixedbarContent = "Do you want to know me more private?→" # Add fixedbar content
    fixedbarContentAfter = "Thank You! Please share it if you like it→" # Add fixedbar content after click

    # Whether you want to hide copyright and credits in the footer.
    hideCredits = false
    hideCopyright = false

    # Custom CSS
    custom_css = []

    # Alignment of Mobile Menu items
    itemscentered = true

    # RTL support
    rtl = false

    # Bottom sns share
    snsShare = true # new add
    # Popular sns share
    # if you want add sns. please message!
    enableTwitterShare = true  # new add
    enableFacebookShare = true # new add
    enableHatenaShare = true   # new add
    enableLineShare = true     # new add
    enableLinkedInShare = true # new add

    thumbnail = "images/tn.png" # default sns thumbnail

    # Multilanguage mode
    langseparator = "|" # Separates menus from language selectors when site is multilingual.

# Social links
[[params.social]]
    name = "Github"
    icon = "fab fa-github"
    weight = 1
    url = "https://github.com/naro143/"
[[params.social]]
    name = "Twitter"
    icon = "fab fa-twitter"
    weight = 2
    url = "https://twitter.com/naro143/"
[[params.social]]
    name = "LinkedIn"
    icon = "fab fa-linkedin"
    weight = 3
    url = "https://www.linkedin.com/in/naro143/"
[[params.social]]
    # If icon is not set, Text is displayed.
    name = "LinkedIn"
    weight = 4
    url = "https://www.linkedin.com/in/naro143/"

# Menu links
[[menu.main]]
    name = "Blog"
    weight = 1
    url  = "posts"
[[menu.main]]
    name = "About"
    weight = 2
    url = "about"
```

You can look at full working [`config.toml`](https://github.com/naro143/hugo-coder-portfolio/blob/master/exampleSite/config.toml) inside the [exampleSite](https://github.com/naro143/hugo-coder-portfolio/tree/master/exampleSite) folder.

#### Multilingual mode

To use multilingual mode, the configuration above needs to be extended by parameters for the specific languages.
Each `language` section overrides default site's parameters when that language is chosen.

```toml
[params]
    langseparator = "|" # separates menus from language selectors.

[languages]
    [languages.en]
        languagename = "English" # The language name to be displayed in the selector.
        title = "Yusuke Ishimi"

        # You can configure the theme parameter for each language. 
        [languages.en.params]
        author = "Yusuke Ishimi"
        info = "WEB AND APPS ENGINEER"
        description = "Yusuke Ishimi's personal website"
        keywords = "blog,developer,personal"

        [languages.en.menu] # It is possible to change the menu too.

        [[languages.en.menu.main]]
        name = "About"
        weight = 1.0
        url = "about"

        [[languages.en.menu.main]]
        name = "Blog"
        weight = 2.0
        url = "posts"


    [languages.ja]
        languagename = "Japanese"
        title = "石見 優丞"

        [languages.ja.params]
            author = "石見 優丞"
            description = "石見 優丞のサイト"
            keywords = "blog,developer, ブログ, エンジニア"
            info = "WEBとアプリのエンジニア"

        [languages.ja.menu]

            [[languages.ja.menu.main]]
            name = "石見とは"
            weight = 1.0
            url = "ja/about"

            [[languages.ja.menu.main]]
            name = "ブログ"
            weight = 2.0
            url = "ja/posts"


```

It is possible to force Hugo to render all default language content under the language code with `defaultContentLanguageInSubdir = true`.
In this case, remember to update your menus URLs (i.e. `/en/about/`).

### Build & Test

It is necessary to have `less` and `uglifycss` installed to build and run the demo.
Assuming that already have NodeJS/NPM installed, run `npm install -g less uglifycss`.

To update or generate the minified CSS file:

```
make build
```

To build your site and test, run:

```
hugo server
```

To preview the exampleSite, run

```
make demo
```

The above command copies current state of the theme to exampleSite/themes and starts hugo with hugo serve -D (Go does not support Symlink directories)

### Disqus

Add the following line to your config, ```disqusShortname = "yourdiscussshortname"``` When this is set, all posts are disqus enabled   
You can disable comments for a post by adding the following to your page meta data: ```disable_comments: true```.


## License

Coder is licensed under the [MIT license](https://github.com/naro143/hugo-coder-portfolio/blob/master/LICENSE.md).

## Author

[Yusuke Ishimi](https://github.com/naro143)

## Contributors

## Special Thanks

- All contributors, for every PR and Issue reported.
