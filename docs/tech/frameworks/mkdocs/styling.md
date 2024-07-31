---
title: Styling
description: Styling MkDocs
---

## Description

{{ description }}

## Page-Specific Styling

To add custom styles to a specific page, add the [md_in_html](../mkdocs/add-ons/md_in_html.md) extension to `meta.yml`:

```yml
markdown_extensions:
  - md_in_html
```

and the add this line to the page:

```HTML
<link rel="stylesheet" href="../[some-page-name].css">
```

Then create the css file in the same directory as `[some-page-name].md`.

## Emojis

[Emoji Search](https://squidfunk.github.io/mkdocs-material/reference/icons-emojis/?h=icons#search)

