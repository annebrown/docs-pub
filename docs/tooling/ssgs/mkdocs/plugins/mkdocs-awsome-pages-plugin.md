---
title: mkdocs-awsome-pages-plugin
description: Essential MkDocs Navi Plugin
---

## Description

{{ description }}

Automatic navi, without polluting `mkdocs.yml`

## Usage

Create a `.pages` file in a dir:

```yml
nav:
  - first-sub-dir
  - first-page.md
  - ... | intro-*.md # all starting with "intro"
  - ... # all remaining entries
  - Title Text: some-page.md # Provide a title 
  - Link Title: https://some-site.com
  - last-page.md
```

Sections:

```yml
nav:
  - index.md
  - section 1:
      - page1.md
	  - page2.md
  - Section 2:
      - another-page.md
```

### Rest Filter

Lines beginning with `  - ...` are called `Rest Filters`.

Rest filters check filters items in the containing folder.