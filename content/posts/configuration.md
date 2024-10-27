---
title: Configuration reference
date: 2024-10-25
---

The following shows all the theme's configuration options you can specify in your site's hugo.toml file:

<!--more-->

```toml
[params]
  # Set how dates should appear across the site.
  # For format options, visit https://gohugo.io/functions/time/format/
  # Default: :date_long
  dateFormat = ':date_long'

  # Show content graph for single notes and posts.
  # Default: true
  showGraph = true

  # Author details for the JSON-LD structured data.
  [params.author]
    name = 'John Doe'
    email = 'johndoe@example.com'

  # Homepage setup
  [params.home]
    # Display recent blog posts on the homepage.
    # Default: true
    showRecentPosts = true

    # Set how many recent blog posts to show.
    # Default: 3
    recentPostsLimit = 3

    # Display recent notes on the homepage.
    # Default: true
    showRecentNotes = true

    # Set how many recent notes to show.
    # Default: 5
    recentNotesLimit = 5

  # Notes page setup
  [params.notes]
    # Set the number of notes to list on each page.
    # Default: 20
    pageSize = 20

    # Show a filter option for note categories above the notes list.
    # Default: true
    showCategoryFilter = true

  # Footer setup
  [params.footer]
    # Specify the Creative Commons license to apply to your content.
    # Options: `by`, `by_sa`, `by_nc`, `by_nc_sa`, `by_nd`, `by_nc_nd`, `zero`, `none`
    # Learn more at https://creativecommons.org/share-your-work/cclicenses/
    # Default: none
    creativeCommonsLicense = 'none'

    # Show Creative Commons icons for the selected license.
    # Default: true
    showCreativeCommonsIcons = true

    # Show a credit link to the Today I Learned theme in the footer.
    # Default: true
    showThemeCredit = true

  # robots.txt setup
  # IMPORTANT: remember to set `enableRobotsTXT = true` in your site's hugo.toml file.
  [params.robotstxt]
    # Block CommonCrawl from indexing your site. CommonCrawl data is often used to train AI models.
    # Learn more at https://commoncrawl.org/ccbot
    # Default: false
    blockCC = false

    # Block various crawlers associated with AI and machine learning model training.
    # Crawler list from https://github.com/ai-robots-txt/ai.robots.txt
    # Default: false
    blockAI = false
```
