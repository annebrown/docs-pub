---
title: Projects
description: Project Summaries
---
<link rel="stylesheet" href="projects.css">

Project Summaries

## docs-pub Project

[This project](../../about.md)

### Status

Operational

### Repo

GitHub Repo: <https://github.com/annebrown/docs-pub.git>

### Tech Stack

Mkdocs SSG

### Deployments

<https://docs.annebrown.ca> - [Netlify](https://app.netlify.com "Official Site") CI

<https://docs.misscommunication.ca> - [ReadTheDocs](https://www.readthedocs.org) CI, with ads

### Dev Svr

URL: [http://127.0.0.1:8000](http://127.0.0.1:8000)

CLI: ```mkdocs serve```

### Bash Shortcuts

```txt
activate-venv - activate python virtual env
godocs - go to project dir
codedocs - vscode workspace (default dark theme)
docserver - start dev svr in venv
docservert - launch dev svr in sep process w matching theme
```

## www.browndomain.com Project

### Repo

GitHub: [https://github.com/annebrown/browndomain.com.git](https://github.com/annebrown/browndomain.com.git)

### Description

Apex Landing Page

### Purpose

Collaborative Development

### Status

In development.

Prototype: [www.browndomain.com](https://www.browndomain.com)

Findings so far:

- Next.js site up and running on dev server with two commands.  
- Next.js and React have totes excellent documentation.  
- Customization and deploy to Vercel with custom domain, is extrememly rapid and painless.  LAMP this is not.
- Feature-rich, high-performance, widely-adopted web app dev framework with a huge dev community and tooling.
- Appears to have more built-in functionality and simpler to implement than Angular.

Currently looking to use it as an SSG for large static assets, with a dynamic IF.

### Dev Svr 

URL: [http://localhost:3000](http://localhost:3000)

CLI: `npm run dev`

### Bash Shortcuts

```txt
gobd - go to proj dir
codebd - vscode workspace w Next.js theme
bdserver - start dev svr
bdservert - launch dev svr in sep process w Next.js theme
```

## www.annebrown.ca Project

Apex Landing Page

### Repo

Private

### Purpose

Personal Dev Tools

### Description

Angular Full-Stack App

### Status

Early stages of development.

Prototype: [https://www.annebrown.ca](https://www.annebrown.ca)

Evaluating Angular framework for PWA dev.  Findings so far:

- Creating new webap and run on dev server takes two commands.  
- Build and deploy to Netlify with minor mods and custom domain, takes minutes.
- Scaleable, complex, feature-rich, widely-adopted web app dev framework with a huge dev community and tooling.
- So far seems to be a more complex web dev framework than Next.js. 
  
Currently looking at Angular Material UI component lib.

### Dev Svr 

URL: http://localhost:4200

CLI: ng serve

## Bash Shortcuts

```txt
goab - go to proj dir
codeab - vscode workspace w Angular theme
abserver - start dev svr
abservert - launch dev svr in sep process w Angular theme
```

## Dotfiles Project

### Repo

GitHub: <https://github.com/annebrown/dotfiles.git>

### Description

Dev env config using [GNU-stow](https://www.gnu.org/software/stow/).

### Purpose

Config for new dev envs (e.g., bare metal host, VM, cloud (GitPod).  In conjunction with a private dotfiles repo, encompasses config for bash, vim, vscode, git, terminals and other tooling.  Also comprises desktop config and other static assets, such as images, local network hosts and scripts.

### Status

Operational.

### Bash Shortcuts

```txt
codedots - vscode (dotfiles and dotfiles-priv) workspace w dark contrast theme
```

## Dotfiles-priv Project

### Repo

Private

### Description

Dev Env Config for sensitive data.  Uses GNU-Stow

### Purpose

Works in conjunction with the [dotfiles](#dotfiles-project) to config new dev env.

### Status

Operational

## Private Projects

Other private projects hosted on authenticated site.
