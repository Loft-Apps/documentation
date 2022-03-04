---
nav_order: 1
---

# Introduction

![Loft Logo](images/loft_logo.png){: style="padding: 20px"}


## What is Loft?

Loft manages assets.


## Why Loft?

### Too Many Files
There are just too many files.  Working at the file level is acceptable when updating a particular character or prop.  You create the files you need and make sure the dependencies work.  However, when this is scaled up to the entire project, the sheer number of files results in deeply nested folder structures in an attempt to organize the chaos.  In order to find anything, folders are used for searching tags and you end up with even further nesting of folders. 

Navigating this folder structure, looking for something becomes overwhelmingly time consuming and users end up spending enormous amounts of valuable time navigating these structures for find what they are looking for.

### Searching ...
The fundamental problem with searching through a file base system is that there are just too many positive matches when the number of files becomes too large.  Since all the data is embedded in the directory structure of the file system,  it rapidly leads to deeply nested folder structures that attempt to as people try to organize the files in some meaningful structure. 

This makes it next to impossible to find anything because there are just way too many files in a system that has only folders and file names to give context for a search.  File searching through typical Windows Explorer or OSX Finder may be familiar but scale poorly for searching.  

Any attempt to use searches of the file views results in a huge list of false positives.  And the results returned are a list of files, making it extremely unlikely to find the particular files.  With the results returned, there is very little context to these files except for folders they exist in. With a near useless search result, users end up navigating the folder structure, as painful as that is.

The end result is a lot of wasted time spent just looking for stuff.

### Syncing
With an SCM, in order to get a particular version of an asset, you have to sync to a branch.  If you just want to work on a single asset, you have to check-out the entire branch which can involve an enormous number of files.

This works fine for source code as even large code bases result in relatively small footprints when compared with digital productions. 



## How is Loft Different from an SCM

Up to now, Digital Asset Management (DAM) has been confined to the deepest dark dungeons of real time visualization production.  More often than not, the choice of Version systems was imposed by the developers who were already using some SCM (source control management).  Perforce, being an early player, made a strong foothold in the industry when Game development was primarily developing source code.

Today’s rich visualization projects have turned those tables around.  Content is now the primary driver in many games.  This is especially true in Game projects which use the Unreal engine where the core Game engine is already developed.  Yet, Game development is still stuck using tools that are primarily developer driven.

Loft proposes an alternative way to search, manage and load assets.  One that is in line with how content creators think.  One that takes away the daily grind using inadequate tools 

Users think in terms of assets.  Assets are used in communication.  They are used for approvals.  It is more natural for a production to discuss in terms of assets.  Rarely will a director or a game designer communicate in terms of files.  When users search, organize, add notes, discuss, they always discuss in terms of asses.

When they are given work, the work is described in terms of an asset.  A user will search on the characteristics of an asset.  It is only when they have to view or edit do they have to work at the file level.

The main difference between Loft and an SCM like Git or Perforce is that instead of checking out branches, Loft checks out versions of assets. Loft breaks up the production into assets and their dependencies and tracks them.

This allows you to mix and match any version of any asset in your local workspace at any time.  The only files you need to have in your local workspace are those that belong to the assets you are working on.  You don’t need to have all of the versions of all of the files locally.

Loft still allows you to work completely locally.  You can edit individual files of an asset and commit to new versions locally and then push the entire asset with its changes to the central server.



## Key Benefits of Loft

User Focused
Loft is primarily a user focused experience.  It brings the often technical and complicated mechanisms of Real time production asset management under control of the end users who have to work with it every day.  This means focusing on the user workflows ensuring that the primary integration is with people.

Current asset management tools focus on the technology.  And this shows in the interfaces that are primarily used for digital production. 

Manage Assets, not just Files
Loft brings production asset management to end users by fundamentally managing assets.  This is in contrast to all SCMs which manage files.


What is the difference between a file and an asset?  A file as everyone knows, is a bundle of data on a drive pointed to by a directory and name.  An asset is an entity that contains all the information about that entity: keywords, tasks, other assets, and also, files.

### Searching
When content creators search for something, they think of a character, a prop, a vehicle.  They do not think of a particular file.  

Doing a search on the file system results in endless lists of junk that will match.  They are not targeted searches on keywords or data.  There is no context to search for the file outside of its folder structure and the name of the file.  This results in an unworkable number of false positive results.

And the results of the search are a list of files.  If the file happens to be a .uasset file, there is no ;way to see what it looks like unless it is opened in the Unreal editor.  With Loft, the search is for assets and a list of assets are returned.  The asset will contain a preview.  It will also contain context for this asset.  Where was it used?  What supporting files are there?  Reference files?  Similar but alternative assets to use?  Notes?  All of this supporting data and files are not searched upon.  It is the asset.  This significantly reduces the number of garbage files that come up in a search.

Searches are far more targeted.  Results are far more relevant.  Time is far less wasted.  Tempers are far more in control.

Studies have shown that successful searches result in 23% less broken screens.  18% less smashed mice and a whopping XX% more productivity.  OK, the first two numbers are made up, but you get the idea.


