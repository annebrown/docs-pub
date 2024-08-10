---
title: Definition Lists
description: HTML Definition Lists
tags:
  - Definition Lists
---

## Description

{{ description }}

## Purpose

When a google search string starts with [ define | what is | what are ], Google renders a [Google Glossary](https://cloud.google.com/translate/docs/advanced/glossary#format-glossary) definition string above search results.

:material-checkbox-outline: TODO Test if Defn Lists behave as expected for site searches prefixed with [ define | what is | what are ].

## Usage

A Defn LIst can include:

- terms not found in dictionaries
- slang
- [Newfie Txt Terms](https://newfoundlandtimes.ca/newfoundland-texting-slang/)
- acronyms
- abbreviations

## HTML Description List

An HTML [Description List](https://www.w3.org/MarkUp/html3/deflists.html) (`<dl> ... </dl>`), is comprised of term element (`<dt></dt>`),  descr element (`<dd></dd>`) pairs:

```html
<dl>
<dt>yat</dt><dd>sup?, hello, how are you doing?</dd>
<dt>yb</dt><dd>yes by, yes</dd>
</dl>
```

Result:

<dl>
<dt>yat</dt><dd>sup?, hello, how are you doing?</dd>
<dt>yb</dt><dd>yes by, yes</dd>
</dl>

With block elements:

```html
<dl>
    <dt>otg</dt>
    <dd><p>plans?, on the go. Ex: Nudding otg tonight</p></dd>
    <dt>bk</dt>
    <dd><p>best kind, really good, common response to yat</p></dd>
```

Result:

<dl>
<dt>yat</dt><dd>sup?, hello, how are you doing?</dd>
<dt>yb</dt><dd>yes by, yes</dd>
</dl>

There can be multiple term and multiple definitions:


```html
<dl>
<dt>Description List</dt>
<dt>Definition List</dt>
<dt>Term List</dt>
<dd>List of terms and definitions</dd>
</dl>
```

Result:

<dl>
<dt>Description List</dt>
<dt>Definition List</dt>
<dt>Term List</dt>
<dd>List of terms and definitions</dd>
</dl>

### `<dl>` Default CSS

```css
dl {
  display: block;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
}
```

### `<dt>` Default CSS

```css
dt {
  display: block;
}
```





```yml
markdown_extensions:
  - def_list
  - pymdownx.tasklist:
      custom_checkbox: true
```
