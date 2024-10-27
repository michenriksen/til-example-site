---
title: About the theme
date: 2024-10-27
---

**Today I Learned** is a [Hugo] theme designed for simplicity, readability, and easy content discovery. It supports both
full-length blog posts for more in-depth content and quick notes for those smaller insights you want to save or share.

<!--more-->

## Features

### Content graph view

A standout feature of this theme is the ability to link posts and notes together, displayed in a network graph similar
to those in personal knowledge apps like [Obsidian]. This content graph creates a web of your knowledge, making it easy
for you and your readers to explore related notes and see how everything is connected.

Check out the [Graph page]({{< relref "/graph" >}}) to see an example of what a larger graph looks like.

### Side notes

You can add {{< sidenote "side notes" >}}Hello, I’m a side note. Use me to include fun facts, additional tips, or insights without disrupting the main flow of the text.{{< /sidenote >}} using a custom shortcode whenever you want to include extra details, tips, or fun facts without
interrupting the flow of your writing. Unlike regular Markdown footnotes that send readers to the bottom of the page,
side notes appear right next to the main content.

### Admonitions

When creating technical content, it’s often helpful to highlight key steps or warn readers about potential issues. For
these situations, custom admonition shortcodes can be used:

{{< admonition type="note" >}}
Remember to save your work frequently to avoid losing changes.
{{< /admonition >}}

{{< admonition type="tip" >}}
You can speed up this process by using keyboard shortcuts.
{{< /admonition >}}

{{< admonition type="warning" >}}
Be careful when modifying these files, as incorrect changes can lead to errors.
{{< /admonition >}}

{{< admonition type="danger" >}}
Deleting this file is permanent and cannot be undone. Double-check before you confirm.
{{< /admonition >}}

### Improved JSON-LD data

The theme enhances Hugo’s built-in [JSON-LD] structured data by adding more detailed metadata, helping search engines
better understand your content and making it easier for your posts to appear in relevant search results.

### Built-in blocking of generative AI/LLM associated web crawlers

If you’re concerned about your content being used as training data for generative AI and language models, the theme’s
robots.txt template allows you to easily block a wide range of genAI and LLM-related web crawlers.

### Easy Creative Commons licensing

The theme includes simple options for adding a [Creative Commons license] to your content, allowing you to define how
others can use, share, or adapt your work. You can choose the most appropriate Creative Commons license, and it will
automatically appear in the website footer with optional usage icons.

## Learn More

For installation and setup, see the {{< backlink "installation" >}} post. Detailed configuration options are covered in
the {{< backlink "configuration" "configuration reference" >}} and the {{< backlink "shortcodes" >}} post explains how
to use the theme's custom shortcodes.

[Hugo]: https://gohugo.io/
[Obsidian]: https://obsidian.md/
[JSON-LD]: https://json-ld.org/
[Creative Commons license]: https://creativecommons.org/share-your-work/cclicenses/

