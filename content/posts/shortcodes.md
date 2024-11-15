---
title: Shortcodes
date: 2024-10-24
---

The theme includes several [shortcodes] for custom features, like linking notes and posts in the content graph, adding
context with side notes, and emphasizing key points with admonitions.

<!--more-->

## `backlink`

The backlink shortcode lets you create special links between related posts and notes. While they appear as regular
links, they also signal the graph feature to connect these items.

```markdown
{{</* backlink BASENAME [LINK TEXT] */>}}
```

Provide the [content base name](https://gohugo.io/methods/page/file/#contentbasename) as the first argument, and an
optional second argument for custom link text. If the second argument is omitted, the link defaults to the title of
the linked page.

### Example usage

```markdown
See related tips in {{</* backlink "text-formatting-basics" "Text Formatting Basics" */>}} and check
out {{</* backlink "markdown-for-docs" */>}} for more on Markdown in documentation.
```

## `sidenote`

Use the sidenote shortcode to add extra details, tips, or fun facts alongside the main content without disrupting the
flow. Unlike standard footnotes, side notes appear right next to the relevant text.


```markdown
{{</* sidenote WORD */>}}CONTENT{{</* /sidenote */>}}
```

Enter the keyword or phrase as the first argument, and place the sidenote content inside the shortcode tags.

### Example usage

```markdown
{{</* sidenote "Markdown" */>}}A simple markup language for easy formatting.{{</* /sidenote */>}} is widely used for its simplicity.
```

### Rendered result

{{< sidenote "Markdown" >}}A simple markup language for easy formatting.{{< /sidenote >}} is widely used for its simplicity.


## `admonition`

Use admonitions to emphasize key steps or alert readers to potential issues with eye-catching boxes that stand out.

```markdown
{{</* admonition [type=TYPE] [title=TEXT] */>}}TEXT{{</* /admonition */>}}
```

Set optional type and title arguments and place the Markdown-supported content inside the shortcode tags.

The type can be one of the following: `note`, `info`, `tip`, `warning`, `danger`. If none is specified, it defaults to
`note`.

### Example usage

```markdown
{{</* admonition */>}}
Remember to save your work frequently to avoid losing changes.
{{</* /admonition */>}}

{{</* admonition type="tip" */>}}
You can speed up this process by using keyboard shortcuts.
{{</* /admonition */>}}

{{</* admonition type="warning" */>}}
Be careful when modifying these files, as incorrect changes can lead to errors.
{{</* /admonition */>}}

{{</* admonition type="danger" title="Watch out!" */>}}
Deleting this file is permanent and cannot be undone. Double-check before you confirm.
{{</* /admonition */>}}
```

### Rendered result

{{< admonition >}}
Remember to save your work frequently to avoid losing changes.
{{< /admonition >}}

{{< admonition type="tip" >}}
You can speed up this process by using keyboard shortcuts.
{{< /admonition >}}

{{< admonition type="warning" >}}
Be careful when modifying these files, as incorrect changes can lead to errors.
{{< /admonition >}}

{{< admonition type="danger" title="Watch out!" >}}
Deleting this file is permanent and cannot be undone. Double-check before you confirm.
{{< /admonition >}}

[shortcodes]: https://gohugo.io/content-management/shortcodes/
