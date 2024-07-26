
# pnpm

pnpm is a pkg mgr.

## Install pnpm

### Global Install npm Dir

Create a dir for global installation:

```bash
mkdir ~/.npm-global
```

### Config PATH

Configure npm to use new PATH:

```bash
npm config set prefix `~/.npm-global'
```

Add path to `~/.profile`

```bash
export PATH=$PATH:~/.npm-global
```

and source `~/.profile`:

```bash
source ~/.profile
```

### Install pnpm

```bash
npm install -g pnpm
```
