# Meta

[Meta](https://squidfunk.github.io/mkdocs-material/plugins/meta/) is a Material Built-In Plugin

## Description

Meta recursively merges the contents of ```.meta.yml```  files with the frontmatter of all pages contained in the same folder and all subfolders.  This, with the help of other plugins, enables powerful features, such as inherited tags, etc.

## Tags

```yml
tags: 
 - Dev
 - Tooling
```

All pages in the containing folder receive these tags, with the help of another Material built-in ```tags``` plugin.

## Setup

```mkdocs.yml```:

```yml
plugins: 
  - meta
```

