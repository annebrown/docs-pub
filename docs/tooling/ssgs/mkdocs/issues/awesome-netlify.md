---
title: awesome-pages not deployed on Netlify
description: Mkdocs-awesome-pages-plugin not respecting navigation.tabs on Netlify
tags:
    - Issues
    - MkDocs
    - awesome-pages
    - mkdocs-awesome-pages-plugin
    - navigation.tabs
    - OPEN
---

## Description

{{ description }}

## Try - Set Specific Versions in `mkdocs.yml`

### Steps

```bash
$ pip freeze > requirements
(.venv) [08:11:09] anne@devy: ~/prod/docs-pub/
$ cat requirements
awesome-slugify==1.6.5
  ...
Jinja2==3.1.4
Markdown==3.6
  ...
mkdocs==1.6.0
mkdocs-awesome-pages-plugin==2.9.3
mkdocs-breadcrumbs==0.0.3
mkdocs-extensions==0.1.2
mkdocs-get-deps==0.2.0
mkdocs-git-revision-date-localized-plugin==1.2.6
mkdocs-include-dir-to-nav==1.2.0
mkdocs-macros-plugin==1.0.5
mkdocs-material==9.5.30
mkdocs-material-extensions==1.3.1
mkdocs-meta-manager==1.0.0
mkdocs-task-collector==0.1.12
  ...
pymdown-extensions==10.8.1
  ...
PyYAML==6.0.1
pyyaml_env_tag==0.1
regex==2024.7.24
requests==2.32.3
  ...
```

`mkdocs.yml`:

```yml
mkdocs==1.6.0
mkdocs-material==9.5.30
pymdown-extensions==10.8.1
mkdocs-git-revision-date-localized-plugin==1.2.6
mkdocs-awesome-pages-plugin==2.9.2
mkdocs-macros-plugin==1.0.5
mkdocs-meta-manager==1.0.0
mkdocs-task-collector==0.1.12
```

Dumped cache and deployed on latest commit.  

### Result

Same same.

## Try Re-order Plugin Third-to-Last

Last three plugins in confg: awesome, then tags, then macros.  

Warnings from dev svr:

!!! Warning Materials/Tabs and Macros plugins must load before awesome-pages.  

    Macros and Tabs must come after awesome-pages because it defines an on_nav handler that will be overridden by awesome-pages.

Dumped cache and deployed on latest commit.  

### Result

Same old.

## Try - Load awesome-pages First

## Solution

Not solved.

## Status

OPEN