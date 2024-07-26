# Netlify

## Deployments

<https://docs.annebrown.ca> (MkDocs SSG)

<https://www.annebrown.ca> (Angular Full-Stack)

## Netlify CLI

### Install

Install Globally:

```bash
npm install netlify-cli -g
```

For Continuous Integration, install from project root dir:

```bash
cd [path/to/proj]
npm install netlify-cli --save-dev
```




Check version and data:

```bash
netlify
```

### Obtain Netlify Access Token

```bash 
netlify login
```

Access token is stored in the Netlify global config file:

```bash
~/.config/netlify/config.json
```

### Disable usage data collection:

```bash
netlify --telemetry-disable
```

