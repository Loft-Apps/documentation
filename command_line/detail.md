---
title: Command Line Help
layout: default
---



## Main Loft Help
```
usage: loft command [-h] [--version]

These are common Loft commands used in various situations

    init            Initialize a Loft Sandbox
    start           Start a new Project
    login           Authenticate to LoftHub Server
    config          Set or display sandbox configuration
    remove          Remove a sandbox locally
    add             Add a new file to be tracked
    create          Create a new local asset
    commit          Commit Files Locally
    checkout        Checkout assets from loft server
    push            Push commits to LoftHub Server
    depend          Manage dependencies between assets
    status          List the status of all asset files
    search          Search the server for assets
    help            Display help for commands

optional arguments:
  -h, --help     show this help message and exit
  --version, -v  Display version of Loft

```

## init

```
> loft init --help

usage: loft init [-h] [-s [SITE]] [-p [PROJECT]] [-r [REPO]] folder

DESCRIPTION

Command to create a new sandbox.  Without arguments, this will create a
sandbox that is not attached to any project.  Arguments can be added to attach
a remote project to this sandbox.  The "config" command can be used to connect
the site and project to this sandbox.

EXAMPLES:

    # Create an empty sandbox
    > loft init MySandbox

    # Create a sandbox that is attached to a project
    > loft init MySandbox --site=MySite --project=MyProject

OPTIONS

positional arguments:
  folder                Base folder for sandbox

optional arguments:
  -h, --help            show this help message and exit
  -s [SITE], --site [SITE]
                        Site or organization this sandbox points to
  -p [PROJECT], --project [PROJECT]
                        Project this sandbox points to
  -r [REPO], --repo [REPO]
                        Repository this sandbox points to


```

## start


```
usage: loft start [-h] project_code

Start a new Project

positional arguments:
  project_code  Code used to identify project

optional arguments:
  -h, --help    show this help message and exit

```


## login

```

usage: loft login [-h] [-p PASSWORD] [login]

Authenticate to LoftHub Server

positional arguments:
  login                 Loft Username

optional arguments:
  -h, --help            show this help message and exit
  -p PASSWORD, --password PASSWORD
                        Loft password


```

