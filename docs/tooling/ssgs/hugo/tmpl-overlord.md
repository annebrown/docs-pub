---
title: Overlord HTML Template
description: Essential dev tool
---

## Description

{{ description }}

Overlord template, `layouts/_default/baseof.html` is the frame encompassing everything else.  It's elements are comprised of things you want on every page.  It is a complete HTML page.

## Basic Overlord Template

```html
<!DOCTYPE html>
<html>
    <head>
      <meta charset="utf-8">
      <meta name="viewport" 
          content="width=device-width">
      <title>Site-Title</title>
    </head>
    <body>
        <div>
            <nav>
                <p>Header Text <a href="/">Home</a> | <a href="/about>About</a></p>
            </nav>
        </div>
        {{ block "main" . }}{{ end }}
        <div>
            <p>Footer Text</p>
        </div>
    </body>
</html>
```

`{{ block "main" . }}{{ end }}` will be used to pull in future content, such as the landing page content, or document page, or content sub-section, etc.  
