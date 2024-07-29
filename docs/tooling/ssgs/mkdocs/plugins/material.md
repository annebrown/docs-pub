---
title: Material for MkDocs
description: Material for MkDocs Theme and Framework
---

## Description

{{ description }}

[Material](https://squidfunk.github.io/mkdocs-material/getting-started) is documentation framework and theme on top of [MkDocs](https://www.mkdocsorg).

## Install

```bash
sudo apt install mkdocs-material
```

## Setup

Add to `mkdocs.yml`:

```yml
theme: 
  name: material
```

Add to plugins section

```bash
pipx install mkdocs-git-revision-date-localized-plugin --include-deps
pipx ensurepath
```
