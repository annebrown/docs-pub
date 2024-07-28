---
title: MkDocs
description: SSG for docs
---

## Description

{{ description }}

[MkDocs](https://www.mkdocs.org) is an SSG writen in Python.

Add !!!!!!!!!!!!!!!!!!!!!!!!

## Python VENV

Create venv dir in proj dir:

```bash
cd [proj-dir]
python3 -m venv .venv
source venv/bin/activate
```

```bash
pipx isntall mkdocsmkdocs
pipx install mkdocs-material --include-deps --force
pip3 install mkdocs-git-revision-date-localized-plugin --include-deps --force
```

```bash
plugins:
  - search
  - git-revision-date-localized
```

## Conclusion

!!!+ warning

    Material for MkDocs appears to the be best addon, however, to use many of its good features, they expect a $15/mo payment, for individual, non-commercian use.  Good luck with that.  


