---
title: Command Line Workflows
layout: default
---



# Transport Workflows


## Deliver to a Freelancer



### Set up sandbox


A project owner will start initiating a new sanbox and attach it to the project on LoftHub

~~~
# initiate a new sandbox
> loft init MyProject --site=MySite --project=MyProject
> cd MyProject
~~~

### Delivery Asset

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


### TODO: Add invites


### Push files to server

When all of the desired files are added to the asset, they can be pushed to the server

~~~
# push all of the added files to the server
> loft push
~~~

Everytime a push is made to the server, a new version is recorded.  All invites to the asset will be notified of the new pushed version of the delivery.





## Freelancer recieves files

The freelancer will recieve a notification that a delivery is ready for them.  In the notification will be a link (for a GUI workflow) or the files can be downloaed to any folder using the invite code


~~~
# Create a new base folder to download files for this project
> makedir MyProject
> cd MyProject


# push all of the added files to the server
> loft download <INVITE_CODE>
~~~


The download command is a convenience method which authenticates a user and downloads the delivery.  This process can be done manually by initiizing a new sandbox and checking out the asset


~~~
# Login to LoftHub
> loft login

# Create a new sandbox
> loft create MyProject --site=MySite --project=MyProject
> cd MyProject
~~~

The freelance can then checkout the asset, which will all the files of the asset from the server.
~~~
# Checkout the asset
> loft checkout feelancers/Frelancer1/Delivery01
~~~


## Updates to the delivery

More files can be added to the delivery asset using the same process.
~~~
# Add more files to the asset
> loft add <MORE_FILES>
> loft push
~~~

If the freelancer has permission, they can also add files to the delivery, allowing for back and forth delivery of new versions of the asset.

NOTE that the Transport asset type is designed for efficient transfer of assets from on place to another.  It is not an ideal repository type for updating files.  This is better done using the "Git" repository type with the full poweer, versioning and wealth of tools availale to Git.






