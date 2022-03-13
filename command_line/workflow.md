---
title: Command Line Help
layout: default
---



# Transport Workflows


## Deliver to a Freelancer


A project owner will start initiating a new sanbox and attach it to the project on LoftHub

~~~
# initiate a new sandbox
> loft init MyProject --site=MySite --project=MyProject
> cd MyProject
~~~

The project owner will then create a new delivery asset.  This asset is a package that will be sent to the freelancer

~~~
# create a new delivery asset
> loft create freelancers/Freelancer1/Delivery01 --repo_type=transport
> cd freelancers/Freelancer1/Delivery01
~~~

Notice that assets can be created anywhere within the folder hierarchy of the project.  This flexibility allows for projects to be set up in whatever way is desired.  In this case, there is a main folder for freelancers and under that a folder specifically for each frelancer.


The project owner will then put files under this asset folder.

~~~
# copy/move/create files to the delivery asset.
> cp -r <FILE_PATHS> .
~~~

These files can also have any arbitrary file structure.  Next, the project owner will add these files to the asset.  Using "*" will wildcard match files.  A single "*" will match all files in the folder.

~~~
# add all of the files to the asset
> loft add *
~~~

Only files that are specifically added to the asset will be pushed to the server.  The status of all of the files in the asset folder can be queried.  

~~~
# add all of the files to the asset
> loft status
~~~


## TODO: add invites




When all of the desired files are added to the asset, they can be pushed to the server

~~~
# push all of the added files to the server
> loft push
~~~

Everytime a push is made to the server, a new version is recorded.  All invites to the asset will be notified of the new pushed version of the delivery.







