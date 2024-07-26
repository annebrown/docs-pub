---
tags:
    - issues
    - mkdocs
    - mkdocs-plugins
    - OPEN
---

# Issues - MkDocs

## Plugins Install - Externally Managed Environment - OPEN

python3 -m pip install --upgrade --no-cache-dir --use-deprecated=legacy-resolver <your_package>
find /usr/lib/python3.12/site-packages -empty -type d -delete



### Description

Example:

Following official plugin.  Did what it says on the tin:

```bash
pip install mkdocs-awesome-pages-plugin
error: externally-managed-environment

× This environment is externally managed
╰─> To install Python packages system-wide, try apt install
    python3-xyz, where xyz is the package you are trying to
    install.
    
    If you wish to install a non-Debian-packaged Python package,
    create a virtual environment using python3 -m venv path/to/venv.
    Then use path/to/venv/bin/python and path/to/venv/bin/pip. Make
    sure you have python3-full installed.
    
    If you wish to install a non-Debian packaged Python application,
    it may be easiest to use pipx install xyz, which will manage a
    virtual environment for you. Make sure you have pipx installed.
    
    See /usr/share/doc/python3.12/README.venv for more information.

note: If you believe this is a mistake, please contact your Python installation or OS distribution provider. You can override this, at the risk of breaking your Python installation or OS, by passing --break-system-packages.
hint: See PEP 668 for the detailed specification.
```

### Try `apt install python3-[pkg-name]` Install

```bash
sudo apt install python3-mkdocs-awesome-pages-plugin
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package python3-mkdocs-awesome-pages-plugin
```

Python3 pkg not included in distro repos.

### Try `pipx` Install

```bash
pipx install python3-mkdocs-awesome-pages-plugin
Fatal error from pip prevented installation. Full pip output in file:
    /home/anne/.local/state/pipx/log/cmd_2024-07-22_10.47.12_pip_errors.log

Some possibly relevant errors from pip install:
    ERROR: Could not find a version that satisfies the requirement python3-mkdocs-awesome-pages-plugin (from versions: none)
    ERROR: No matching distribution found for python3-mkdocs-awesome-pages-plugin

Error installing python3-mkdocs-awesome-pages-plugin.
```

Python3 pkg not found.

### Try Deleting `EXTERNALLY-MANAGED`

From StackOverflow [Answer](https://stackoverflow.com/questions/75608323/how-do-i-solve-error-externally-managed-environment-every-time-i-use-pip-3), with mods (s/mv/rm/) and (s/3.21/3.12/):

```bash
sudo rm /usr/lib/python3.12/EXTERNALLY-MANAGED
pip install mkdocs-awesome-pages-plugin
Defaulting to user installation because normal site-packages is not writeable
WARNING: Skipping /usr/lib/python3.12/dist-packages/argcomplete-3.1.4.dist-info due to invalid metadata entry 'name'
Collecting mkdocs-awesome-pages-plugin
  Using cached mkdocs_awesome_pages_plugin-2.9.2-py3-none-any.whl.metadata (13 kB)
Requirement already satisfied: mkdocs>=1 in /usr/lib/python3/dist-packages (from mkdocs-awesome-pages-plugin) (1.5.3)
Collecting natsort>=8.1.0 (from mkdocs-awesome-pages-plugin)
  Using cached natsort-8.4.0-py3-none-any.whl.metadata (21 kB)
Collecting wcmatch>=7 (from mkdocs-awesome-pages-plugin)
  Using cached wcmatch-8.5.2-py3-none-any.whl.metadata (4.8 kB)
Requirement already satisfied: click>=7.0 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (8.1.6)
Requirement already satisfied: ghp-import>=1.0 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (2.1.0)
Requirement already satisfied: jinja2>=2.11.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (3.1.2)
Requirement already satisfied: markdown>=3.2.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (3.5.2)
Requirement already satisfied: markupsafe>=2.0.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (2.1.5)
Requirement already satisfied: mergedeep>=1.3.4 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (1.3.4)
Requirement already satisfied: packaging>=20.5 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (24.0)
Requirement already satisfied: pathspec>=0.11.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (0.12.1)
Requirement already satisfied: platformdirs>=2.2.0 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (4.2.0)
Requirement already satisfied: pyyaml-env-tag>=0.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (0.1)
Requirement already satisfied: pyyaml>=5.1 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (6.0.1)
Requirement already satisfied: watchdog>=2.0 in /usr/lib/python3/dist-packages (from mkdocs>=1->mkdocs-awesome-pages-plugin) (3.0.0)
Collecting bracex>=2.1.1 (from wcmatch>=7->mkdocs-awesome-pages-plugin)
  Using cached bracex-2.4-py3-none-any.whl.metadata (3.6 kB)
Requirement already satisfied: python-dateutil>=2.8.1 in /usr/lib/python3/dist-packages (from ghp-import>=1.0->mkdocs>=1->mkdocs-awesome-pages-plugin) (2.8.2)
Using cached mkdocs_awesome_pages_plugin-2.9.2-py3-none-any.whl (14 kB)
Using cached natsort-8.4.0-py3-none-any.whl (38 kB)
Using cached wcmatch-8.5.2-py3-none-any.whl (39 kB)
Using cached bracex-2.4-py3-none-any.whl (11 kB)
WARNING: Skipping /usr/lib/python3.12/dist-packages/argcomplete-3.1.4.dist-info due to invalid metadata entry 'name'
Installing collected packages: natsort, bracex, wcmatch, mkdocs-awesome-pages-plugin
Successfully installed bracex-2.4 mkdocs-awesome-pages-plugin-2.9.2 natsort-8.4.0 wcmatch-8.5.2
```

However, missing mkdocs Python3 script:

```bash
$ mkdocs serve
bash: /home/anne/.local/bin/mkdocs: No such file or directory
```

`/usr/bin/mkdocs` exists and is in 'PATH'.

### Try Using Virtual Env

```bash
python3 -m venv venv
source ./venv/bin/activate
```

> OPINION: PITA - Yet another level of complexity in a simple dev project.

Then:

```bash
pip install --upgrade pip
Requirement already satisfied: pip in ./.venv/lib/python3.12/site-packages (24.0)
Collecting pip
  Using cached pip-24.1.2-py3-none-any.whl.metadata (3.6 kB)
Using cached pip-24.1.2-py3-none-any.whl (1.8 MB)
Installing collected packages: pip
  Attempting uninstall: pip
    Found existing installation: pip 24.0
    Uninstalling pip-24.0:
      Successfully uninstalled pip-24.0
Successfully installed pip-24.1.2
```

Uninstalled mkdocs and plugins and mkdocs-material.

Reinstalled Mkdocs, then

```bash
(.venv) [14:08:35] anne@devy: ~/prod/docs-pub/
$ mkdocs serve
ERROR   -  Config value 'theme': Unrecognised theme name: 'material'. The available installed themes are: mkdocs,
           readthedocs

Aborted with a configuration error!
(.venv) [14:08:40] anne@devy: ~/prod/docs-pub/
```
 So installed mkdocs-material:

```bash
pip install mkdocs-material
Collecting mkdocs-material
  Using cached mkdocs_material-9.5.29-py3-none-any.whl.metadata (17 kB)
Requirement already satisfied: babel~=2.10 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (2.15.0)
Requirement already satisfied: colorama~=0.4 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (0.4.6)
Requirement already satisfied: jinja2~=3.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (3.1.4)
Requirement already satisfied: markdown~=3.2 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (3.6)
Requirement already satisfied: mkdocs-material-extensions~=1.3 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (1.3.1)
Requirement already satisfied: mkdocs~=1.6 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (1.6.0)
Requirement already satisfied: paginate~=0.5 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (0.5.6)
Requirement already satisfied: pygments~=2.16 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (2.18.0)
Requirement already satisfied: pymdown-extensions~=10.2 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (10.8.1)
Requirement already satisfied: regex>=2022.4 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (2024.5.15)
Requirement already satisfied: requests~=2.26 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-material) (2.32.3)
Requirement already satisfied: MarkupSafe>=2.0 in /home/anne/.venv/lib/python3.12/site-packages (from jinja2~=3.0->mkdocs-material) (2.1.5)
Requirement already satisfied: click>=7.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (8.1.7)
Requirement already satisfied: ghp-import>=1.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (2.1.0)
Requirement already satisfied: mergedeep>=1.3.4 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (1.3.4)
Requirement already satisfied: mkdocs-get-deps>=0.2.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (0.2.0)
Requirement already satisfied: packaging>=20.5 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (24.1)
Requirement already satisfied: pathspec>=0.11.1 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (0.12.1)
Requirement already satisfied: pyyaml-env-tag>=0.1 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (0.1)
Requirement already satisfied: pyyaml>=5.1 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (6.0.1)
Requirement already satisfied: watchdog>=2.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs~=1.6->mkdocs-material) (4.0.1)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/anne/.venv/lib/python3.12/site-packages (from requests~=2.26->mkdocs-material) (3.3.2)
Requirement already satisfied: idna<4,>=2.5 in /home/anne/.venv/lib/python3.12/site-packages (from requests~=2.26->mkdocs-material) (3.7)
Requirement already satisfied: urllib3<3,>=1.21.1 in /home/anne/.venv/lib/python3.12/site-packages (from requests~=2.26->mkdocs-material) (2.2.2)
Requirement already satisfied: certifi>=2017.4.17 in /home/anne/.venv/lib/python3.12/site-packages (from requests~=2.26->mkdocs-material) (2024.7.4)
Requirement already satisfied: python-dateutil>=2.8.1 in /home/anne/.venv/lib/python3.12/site-packages (from ghp-import>=1.0->mkdocs~=1.6->mkdocs-material) (2.9.0.post0)
Requirement already satisfied: platformdirs>=2.2.0 in /home/anne/.venv/lib/python3.12/site-packages (from mkdocs-get-deps>=0.2.0->mkdocs~=1.6->mkdocs-material) (4.2.2)
Requirement already satisfied: six>=1.5 in /home/anne/.venv/lib/python3.12/site-packages (from python-dateutil>=2.8.1->ghp-import>=1.0->mkdocs~=1.6->mkdocs-material) (1.16.0)
Using cached mkdocs_material-9.5.29-py3-none-any.whl (8.8 MB)
Installing collected packages: mkdocs-material
Successfully installed mkdocs-material-9.5.29
```

Then:

```bash
(.venv) [14:08:35] anne@devy: ~/prod/docs-pub/
$ mkdocs serve
ERROR   -  Config value 'theme': Unrecognised theme name: 'material'. The available installed themes are: mkdocs,
           readthedocs
```

Spent more time in venv, unstalling and reinstalling and restarting and Wasted too much time, with same outcome.

## Conclusion

Python, MkDocs, and its plugins and extensions are all over the place with bugs, versions, envs, and documentation.  Installations are too buggy right now to consider for use.  Ditching Mkdocs for SSG.
