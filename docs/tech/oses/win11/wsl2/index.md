---
title: WSL2
description: Windows Subsystem for Linux, Version 2
---

## Description

{{ description }}

> Opinion: Not recommending Wind:money_mouth:ows WLS2 for a dev env.  Stradling two OSes with incompatible file systems, using an IDE on one OS, to develop on another OS, plus maintaining two sets of user, app and system configs, etc, adds unnecessary levels of complexity.  Bare metal Linux, VM, container and/or cloud-based is easier to install and configure and offers superior flexibility and control over the entire dev to deploy cycle.

- [CLI](wsl2-cli.md)
- [Desktop](desktop.md)

## SSH

```bash
$ DISPLAY=:0.0 SSH -y [hostname]
```

## Config

File: `/etc/wsl.conf`:

```ini
[boot]
systemd=true
[network]
generateHosts false
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
    <div class="item-00"><a href="wsl2-cli/"><p>CLI</p></a></div>
    <div class="item-00"><a href="desktop/"><p>Desktop</p></a></div>
</div>
