---
title: Navi
description: MKdocs Navi
---

## Description

{{ description }}

## ```nav``` Config Setting

The ```/mkdocs.yml``` file's ```nav``` config setting defines global site navi contents and structure.  

If absent, navi is automatically, alphabetically generated from all of the MD files in ```docs```, with ```index``` files at the top of sub-sections.

Titles inferred from MD file, or if not present, from filename:

```yml
nav:
  - 'index.md'
  - 'about.md'
```

Titles defined in the ```nav:``` item of  ```/mkdocs.yml``` will be used throughout the site for that page and overrides titles defined in MD files:

```yml
nav:
  - Home: 'index.md'
  - About: 'about.md'
```

## Subsections

```yml
site_name: Docs
nav:
  - Home: 'index.md'
  - 'Dev':
    - 'Tooling':
      - 'MkDocs':
        - 'Setup': 'install.md'
  - 'about.m'
```

## Example nav:

```yml
nav:
  - Home: 'index.md'
  #- APIs: 
  #- 'Databases'
  - Frameworks: 'pub/frameworks/index.md'
  - 'Languages': 'pub/languages/index.md'
  #- 'Organizations'
  #- 'OSes'
  #- 'Security'
  #- 'Servers'
  - Tooling: 'pub/tooling/index.md'
  - About: 'about.md'
```

## Index Pages

If both an ```index.md``` and a ```README.md``` are found in a dir, ```README.md``` is ignored.
