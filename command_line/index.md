


# Loft CLI (Command Line Interface)

The Loft CLI provides all the power of Loft using commands in a shell.  This is ideal for integrating Loft into various scripts.

This document provides a quick reference to do common tasks.


## Authentication

In order to interact with the LoftHub servers, you need to be logged in.  This can be done in the command line:
```
> loft login
```

After executing this, you will be prompted with a name and password.


## Create a local sandbox

Sandboxes are where you work.  This will create a new sandbox

```
> loft init MySandbox
```

## Attach a Loft project to the sandbox

Sandboxes need to be attached to a project in LoftHub in order to share files.  A sandbox can be configured using the "config" command.

```
> loft config –site=MySite
> loft config –project=MyProject
```

These will attach a site (organization) and a project to the the sandbox.  In larger projects, there
may be multiple repositories.  The sandbox will automatically be set to the "default" repository, however, this can be set using the "config" command.


```
> loft config –repo=MyRepo
```




## This could have been done in one line
```
> loft init MySandbox --site=MySite –project=MyProject
```


## Create an asset
```
> loft create character/main01
```


## Create a new transport asset in a delivery folder
```
> mkdir delivery
> cd delivery
> loft create Delivery01 --repo_type=transport
```






## Sandboxes

### Create a new loft sandbox
```
> loft init                     # simple init
> loft init --type git          # create with a git repository
> loft init --type transport    # create with a transport repository
```


### List all of the sandboxes
```
> loft sandbox --list
My Project
My Other Project
```

### List settings of a single sandbox
```
> loft sandbox "My Project"
```


### Remove loft sandbox
```
> loft remove
```


## Assets

### Create a new asset

```
> cd assets

> mkdir CHR001

> loft create CHR001
CHR001: Created
```


### Create a new asset and set the repo type
```
> loft create CHR001 --repo_type git
CHR001: Created


> loft create CHR001 --repo_type perforce
CHR001: Created
```

### Add a description to the character
```
> loft set CHR001 --description "Terminator charactor"
```

### Add a preview 
```
> loft set CHR001 --preview "~/terminator_icon.png"
```


### Add a dependency 
```
> loft set --dependency PROP/PROP001 PROP/PROP002
> loft set --dependency PROP/*

> loft unset --dependency PROP/PROP001
```



### Create files and add them to the asset
```
> cat "This is a test" > CHR001/design.md
> cat "This is a test" > CHR001/reference.md

> loft add CHR001/design.md
Added design.md to the CHR001 asset

> loft add CHR001/reference.md
Added reference.md to the CHR001 asset
```


## Commit


### Commit the entire asset

```
> loft commit CHR001
Committed reference.md
Committed design.md
```

### Commit a single file
```
> loft commit CHR001/design.md
```

### Commit all of the assets under a folder
```
> loft commit .
```


### Push a new version to the server

```
> cd CHR001
> loft push .
```

## Transport

### Download a delivery to current directory

```
> cd MyDownload
> loft download <CODE>
```


### Download delivery when already logged in
```
> cd <SANBOX_BASE_DIR>
> loft download Delivery01
```

### Add files to a transport asset and push back to server

NOTE: the invite list currently does not get copied to the server.  This means that updates from another user will not notify users yet.
```
> cd Delivery01
> cp <FILES> .
> loft add *
> loft push
```

### Add invites

NOTE: this does not exist yet
```
> cd Delivery01
> loft invite joe@company.com
```



