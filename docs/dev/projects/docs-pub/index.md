---
title: docs-pub
description: Technical Ref Docs Project
tags:
  - docs-pub
---

## Description

{{ description }}

## Repo

GitHub Repo: <https://github.com/annebrown/docs-pub.git>

## Purpose

See [About](../../../about.md)  page.

## Tech Stack

Mkdocs SSG

## Status

Operational

## Deployments

<https://docs.annebrown.ca> - [Netlify](https://app.netlify.com "Official Site") CI

<https://docs.misscommunication.ca> - [ReadTheDocs](https://www.readthedocs.org) CI, with ads

## Dev Svr

URL: [http://127.0.0.1:8000](http://127.0.0.1:8000)

CLI: ```mkdocs serve```

## Bash Shortcuts

```txt
activate-venv - activate python virtual env
godocs - go to project dir
codedocs - vscode workspace (default dark theme)
docserver - start dev svr in venv
docservert - launch dev svr in sep process w matching theme
```

<style>
.outter-container {
  padding: 0.5rem;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* Fractional  */
  gap: 10px;
    /* column-gap: 10px; 
    row-gap: 20px; */
}

.item-00 {
  text-align: center;
  border: 0.25px solid gray;
}
</style>

<div class="outter-container">
    <div class="item-00 box1"><a href="testing/"><p>Testing</p></a></div>
    <div class="item-00 box1"><a href="meta/"><p>Meta</p></a></div>
</div>