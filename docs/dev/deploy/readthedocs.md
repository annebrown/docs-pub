---
title: Deploy - ReadtheDocs
description: Projects deployed to [ReadTheDocs](https://readthedocs.io "Official Site")
tags:
  - ReadTheDocs
---

## Description

{{ description }}

## Deployments

<https://docs.misscommunication.ca> (MkDocs SSG)

## Config

Place `.readthedocs.yaml` in project root.

`.readthedocs.yml`:

```yaml
# Read the Docs configuration file for MkDocs projects
# See https://docs.readthedocs.io/en/stable/config-file/v2.html for details

# Required
version: 2

# Set the version of Python and other tools you might need
build:
  os: ubuntu-24.04
  tools:
    python: "3.12"

mkdocs:
  configuration: mkdocs.yml

# Optionally declare the Python requirements required to build your docs
python:
  install:
    - requirements: requirements.txt
```
