---
title: Difference from SCM
layout: default
parent: Introduction
nav_order: 1
---


# How is Loft Different from an SCM

Up to now, Digital Asset Management (DAM) has been confined to the deepest dark dungeons of real time visualization production.  More often than not, the choice of Version systems was imposed by the developers who were already using some SCM (source control management).  Perforce, being an early player, made a strong foothold in the industry when Game development was primarily developing source code.

Today’s rich visualization projects have turned those tables around.  Content is now the primary driver in many games.  This is especially true in Game projects which use the Unreal engine where the core Game engine is already developed.  Yet, Game development is still stuck using tools that are primarily developer driven.

Loft proposes an alternative way to search, manage and load assets.  One that is in line with how content creators think.  One that takes away the daily grind using inadequate tools 

Users think in terms of assets.  Assets are used in communication.  They are used for approvals.  It is more natural for a production to discuss in terms of assets.  Rarely will a director or a game designer communicate in terms of files.  When users search, organize, add notes, discuss, they always discuss in terms of asses.

When they are given work, the work is described in terms of an asset.  A user will search on the characteristics of an asset.  It is only when they have to view or edit do they have to work at the file level.

The main difference between Loft and an SCM like Git or Perforce is that instead of checking out branches, Loft checks out versions of assets. Loft breaks up the production into assets and their dependencies and tracks them.

This allows you to mix and match any version of any asset in your local workspace at any time.  The only files you need to have in your local workspace are those that belong to the assets you are working on.  You don’t need to have all of the versions of all of the files locally.

Loft still allows you to work completely locally.  You can edit individual files of an asset and commit to new versions locally and then push the entire asset with its changes to the central server.



