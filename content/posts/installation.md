---
title: Installation and setup
date: 2024-10-26
---

This post shows how to install and set up the Today I Learned theme on your own Hugo website.

<!--more-->

## Hugo module

To get started, it’s best to initialize your website as a Hugo module, making theme installation and updates smoother.
In your Hugo site directory, enter:

```terminal
hugo mod init
```

After that, you can download the latest version of the Today I Learned theme with:

```terminal
hugo mod get github.com/michenriksen/hugo-theme-til
```

## JavaScript dependencies

Since Hugo doesn’t support packaging NPM/JavaScript dependencies in themes yet, you’ll need to install the [vis-network]
package separately to render the content network graph:

```terminal
npm install vis-network
```

## Site configuration

Open your `hugo.toml` file and set up your site with the following configuration:

```toml
baseURL = 'https://example.com/'
languageCode = 'en-us'
title = "John Doe's website"
copyright = 'John Doe' # Used in the footer copyright mention.
enableRobotsTXT = true # IMPORTANT: set to true if you want to use the theme's genAI/LLM web crawler blocking feature.

[module]
  [[module.imports]]
    path = "github.com/michenriksen/hugo-theme-til"

[outputs]
  home = ['html']
  section = ['html', 'rss', 'json']
  page = ['html']

[menus]
  [[menus.main]]
    name = 'Notes'
    pageRef = '/notes'
    weight = 20
  [[menus.main]]
    name = 'Posts'
    pageRef = '/posts'
    weight = 30
  [[menus.main]]
    name = 'Graph'
    pageRef = '/graph'
    weight = 40

[markup]
  [markup.highlight]
    noClasses = false
    style = 'tokyonight-night'

  [markup.goldmark]
    [markup.goldmark.parser]
      [markup.goldmark.parser.attribute]
        block = true
```

## Further configuration

You can further customize the theme with various configuration options. For more details, see the {{< backlink "configuration" >}}.

[vis-network]: https://www.npmjs.com/package/vis-network
