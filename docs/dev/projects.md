# Projects

## docs-pub

[This project](../about.md)

### Repo

GitHub: <https://github.com/annebrown/docs-pub>

### Status

Operational, living knowledgebase, using MkDocs SSG.

Deployments:

<https://docs.annebrown.ca> (Continuous Integration (CI), Netlify)

<https://docs.misscommunication.ca> (CI, on [ReadTheDocs](https://www.readthedocs.org), with ads.)


### Dev Svr

Url: http://127.0.0.1:8000

CLI: mkdocs serve

Bash Alias: docserver # Run svr in custom terminal

## www.browndomain.com

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

## www.annebrown.ca

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

## dotfiles

### Repo

GitHub: <https://github.com/annebrown/dotfiles>

### Description

Dev Env Config using GNU-stow and other config tools.

### Purpose

Config for new dev hosts and envs (e.g., bare metal host, VM, GitPod).  In conjunction with a private dotfiles repo, encompasses config for bash, vim, vscode, git, terminals and other tooling.  Also comprises desktop config and other static assets, such as images, local network hosts and scripts.

### Status

Operational and evolving with new configs mods.

## dotfiles-priv

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
