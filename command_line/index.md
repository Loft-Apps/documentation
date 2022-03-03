


# Loft CLI (Command Line Interface)

## Sandboxes

### Create a new loft sandbox
```
> loft init                 # simple init
> loft init --type git      # create with a git repository
> loft init --type tactic   # create with a tactic repository
```


### Set the server
```
> loft init --server http://192.168.115.129
```

### Set the project
```
> loft init --project loft
```

### Set the authentication ticket
```
> loft init --ticket XYZ123
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


## Push a new version to the server

```
> cd CHR001
> loft push .
```


### Create a new version of the asset
```
> cd CHR001
> loft version CHR001
Created new version of CHR001

> loft version CHR001
! No changes

> cat "A new version" > CHR001/design.md


> loft version CHR001
Commited design.md
Created new version of CHR001
```

### See all of the versions
```
> loft log CHR001
DGT344TVG
ZWERTY123

> loft checkout CHR001 DGT344TVG
Checked out version DGT344TVG

```





