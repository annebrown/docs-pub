---
title: mkdocs-awsome-pages-plugin
description: Essential MkDocs Navi Plugin
tags:
  - mkdocs-awesome-pages-plugin
---

## Description

{{ description }}

Supports automatic and specific dir-based navi, without polluting `mkdocs.yml`

## Usage

Create a `.pages` file in a dir:

```yml
nav:
  - index.md
  - first-sub-dir
  - first-page.md
  - ... | intro-*.md # all starting with "intro"
  - ... # all remaining entries
  - Title Text: some-page.md # Provide a title 
  - Link Title: https://some-site.com
  - last-page.md
```

### Rest Filter

Lines beginning with `...` are called `Rest Filters`.

Rest filters - check filters items in the containing folder.

## Custom Sections

```yml
nav:
  - index.md
  - section 1:
      - page1.md
      - page2.md
  - Section 2:
      - another-page.md
```

