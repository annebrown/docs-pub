---
title: Install
description: Install and run MkDocs
---

## Description

{{ description }}

URL: [Getting Started w MkDocs](https://mkdocs.org/getting-started)

## Install MkDocs

```bash
sudo apt install mkdocs
mkdocs --versoin
```

## Create New MkDocs Proj

```bash
mkdocs new mkdocs-proj-name
cd mkdocs-proj-name
INFO    - Creating project directory: mkdocs-pub
INFO    - Writing config file: mkdocs-pub/mkdocs.yml
INFO    - Writing initial docs: mkdocs-pub/docs/index.md
```

Config File: `/mkdocs.yml`:

```yml
site_name: My Docs
```

Initial Doc: `/docs/index.md`

```html
# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org)

## Commands

* 'mkdocs new [dir-name]` - Create a new project.
* ....

## Project layout

    mkdocsyml   # The config file
    docs/
        index.md    # The docs homepage.
        ...         # Other markdown pages, images and oth files
```

## View Docs

```bash
mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.07 seconds
INFO    -  [08:15:44] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [08:15:44] Serving on http://127.0.0.1:8000/
```

