---
title: JavaScript
description: JavaScript Programming Lang
tags:
  - JavaScript
---

## Description

My Notes on [{{ description }}](https://en.wikipedia.org/wiki/JavaScript)

- For creating dynamic, interactive content
- Single-threaded
- Line-by-line, interpreted

## Risks

Cross-site script attack - inject external JS into visitor's browser


## Execution Context

`Memory Allocation Phase`

:    Functs and vars get stored into mem as key-val pairs

`Code Execution Phase`

:    Thread of execution, whereby vals of functs and vars are updated

When a function is called, a new Execution Context is created inside the previous global execution context.

## ECMAScript

- standarized scripting lang spec.
- core features and functionalities of JavaScript

ES6 - ECMAScript 2015, 6th version of ECMAScript std

## Usage

```html title="Embedded in head or body elememt"
<script>
  //logic
</script>
```

### External

```html title="Link to External File in head element"
<script src="assets/javascript/site.js"></script>
```
