---
title: Info
description: Testing Abbrs, Defn Lists, Tooltips, etc.
tags:
  - Links
  - Testing
---

## Description

{{ description }}

## Abbr

The HTML specification is maintained by the W3C.

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium

## Glossary

:material-checkbox-outline: TODO Test if Defn Lists behave as expected for site searches prefixed with [ define | what is | what are ].

## Docs Index

:material-checkbox-blank-outline: TODO Site Index

## Tooltips

This a [Link w Tooltip](sandbox.md "Here is the Tooltip").

Also of use in a [reference][example]

  [example]: styling.md "I'm a tooltip!"

This is an icon :material-information-outline:{ title="Important information" } with some important information.

definitions:

  - &page_title_with_site_name >-
    {%- if not page.is_homepage -%}
      {{ page.meta.get("title", page.title) }} - {{ config.site_name }}
    {%- else -%}
      {{ page.meta.get("title", page.title) }}
    {%- endif -%}

  - &page_description >-
    {{ page.meta.get("description", config.site_description) or "" }}

tags:

  og:type: website
  og:title: *page_title_with_site_name
  og:description: *page_description
  og:image: ""
  og:image:type: "{{ image.type }}"
  og:image:width: "{{ image.width }}"
  og:image:height: "{{ image.height }}"
  og:url: "{{ page.canonical_url }}"

  twitter:card: summary_large_image
  twitter:title: *page_title_with_site_name
  twitter:description: *page_description
  twitter:image: "{{ image.url }}"
