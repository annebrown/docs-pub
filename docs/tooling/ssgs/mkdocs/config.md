---
title: Config
description: MkDocs Config
---

## Description

{{ description }}

## General

```yml
#--------------------
# mkdocs.yml
#--------------------
site_name: Docs
site_url: https://docs.annebrown.ca
repo_url: https://github.com/annebrown/docs-pub/
site_description: Tech Ref Docs
site_author: Anne Brown
copyright: Copyright &copy; 2024 <a href="https://annebrown.ca">Anne Brown</a>

#--------------------
# INDEX
#--------------------
# nav
# theme
# extensions
# css
# javascript
...
```

## Extensions

```yml
#--------------------
# extensions
#--------------------
markdown_extensions:
  - def_list
  - pymdownx.tasklist:
      custom_checkbox: true
```

## CSS

```yml
#--------------------
# css
#--------------------
extra_css:
  - stylesheets/extra.css
```

See also [theming](theming.md)

## Javascript

```yml
#--------------------
# javascript
#--------------------
extra_javascript:
  - javascripts/extra.js
```
