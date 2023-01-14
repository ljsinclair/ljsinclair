---
title: Fix merge conflicts with atom/pulsar editor and command line
---

## Issue

How do I resolve Git merge conflicts?

## Before you begin

* Add the repo to Atom editor with File > Add project folder.

## Step 1 - git merge main on the command line

On the command line:

```
cd [repo-directory]
git checkout main
git checkout [branchname]
git merge main
```

## Step 2 - Open atom editor and the repo branch

When these steps are complete, you'll see the conflicts displayed as an additional panel in the Git panel

* Open Atom Editor
* Open the Git panel
* Choose the correct repo in the top field
* Choose the correct branch from the status bar at the bottom.

## Step 3 - Resolving conflicts

These steps may need to be repeated

### Resolve text conflicts

Text conflicts are highlighted with "Ours" and "Theirs"

* Click the file in the Conflict panel to open in the buffer
* Select which change to accept:
  * Ours = this branch
  * Theirs = main branch
* Save the change
* RH click in the conflict panel > stage

### Resolve missing file conflicts

* RH click on the file in the conflict panel
* Choose **ours** to accept the file is deleted
* Choose **theirs** to restore the file
* RH click > Stage

## Step 4 - commit to main and push changes

* Click **Commit to main**
* Click **Push** on the status bar.
