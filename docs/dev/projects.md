---
title: Projects
description: Project Details
---

## Description

{{ description }}

<h2 markdown="1" style="color: green">docs-pub</h2>

[This project](../about.md)

### Status

Operational

*[SSG]: Static Site Generator

Deployments:

<https://docs.annebrown.ca> - [Netlify](https://app.netlify.com "Official Site") CI

<https://docs.misscommunication.ca> - [ReadTheDocs](https://www.readthedocs.org) CI, with ads


### Dev Svr

URL: [http://127.0.0.1:8000](http://127.0.0.1:8000)

CLI: ```mkdocs serve```

Aliases: 

`activate-venv` # Activate Python Virtual Env

`docserver` # Run svr in custom terminal

<h2 markdown="1" style="color: green">www.browndomain.com</h2>

### Repo

GitHub: <https://github.com/annebrown/browndomain.com>

### Description

Apex Landing Page

### Purpose

Collaborative Development

### Status

In development.

Prototype: <https://www.browndomain.com>

Evaluated Hugo as an SSG, however its lack of adequate documentation was too much of a time waster.  YMMD  

Ditched Hugo for Next.js as SSG:

 - Creating a new webapp and getting it runnng on a dev server took two commands.  
 - Customizing it as a landing page, and then build and deploy to Vercel with custom domain, very fast.
 - Currently evaluating its function as an SSG,

### Dev Svr 

URL: http://localhost:3000

CLI: npm run dev 

Bash Alias: nextbd # Run svr in custom terminal

<h2 markdown="1" style="color: green">www.annebrown.ca</h2>

Apex Landing Page

### Repo

Private

### Purpose

Personal Dev Tools

### Description

Angular Full-Stack App

### Status

In early stages of development.

Prototype: <https://www.annebrown.ca>

Evaluating Angular framework for web app dev:

 - Creating a new webap and getting it runnng on a dev server took two commands.  
 - Customizing it as a landing page, and then build and deploy to Netflix with custom domain, took only a few minutes.
  
Currently evaluating Angular Material UI component lib.

### Dev Svr 

URL: http://localhost:4200

CLI: ng serve

Bash Alias: angularab # Run svr in custom terminal

<h2 markdown="1" style="color: green">Dotfiles</h2>

### Repo

GitHub: <https://github.com/annebrown/dotfiles>

### Description

Dev env config using [GNU-stow](https://www.gnu.org/software/stow/).

### Purpose

Config for new dev hosts and envs (e.g., bare metal host, VM, GitPod).  In conjunction with a private dotfiles repo, encompasses config for bash, vim, vscode, git, terminals and other tooling.  Also comprises desktop config and other static assets, such as images, local network hosts and scripts.

### Status

Operational.

<h2 markdown="1" style="color: green">Dotfiles Private</h2>

### Repo

Private

### Description

Dev Env Config for sensitive data.  Uses GNU-Stow

### Purpose

Works in conjunction with [dotfiles](#dotfiles) to config new dev hosts and envs.

### Status

Operational and evolving with new config mods.

## Private Projects

All other private projects are hosted on a site requiring authn.
