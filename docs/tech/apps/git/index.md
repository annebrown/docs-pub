---
title: Git
description: Git Config
tags:
  - Git
---

## Description

{{ description }}

## Git Global Config

```bash
git config --global user.name "Anne Brown"
git config --global user.email anne@browndomain.com
```

## GitHub CLI

### Install GitHub Desktop

#### Raspi

Install from `pi-apps`.

#### Ubuntu 

```bash
sudo apt install gh
```

## Authn

```bash
gh auth login # Opens browser for authn
```

### [Two Factor Authn](../../oses/linux/new-dev-env.md#two-factor-authn)

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
    <div class="item-00 box1"><a href="../git/gitignore/">.gitinore</a></div>
</div>

