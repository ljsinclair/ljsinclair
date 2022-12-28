---
title: My windows cleanup
---

## Issue

* Computer sluggish
* Application uninstalls have left a lot of crap behind
* Versions and updates aren't happening coherently

## Methods to resolve

* [Install Chocolatey](https://chocolatey.org/) and use that to install as many required applcations as possible
  * [CCleaner](https://community.chocolatey.org/packages/ccleaner) or something like it is a must to clean up leftover files and registry entries for uninstalled files, plus update drivers
* [Use Windows Store]() for as many other applciations as possible
  * [SyncFolder](http://syncfolder.cwwonline.be/) to handle backups and sync
* Add a calendar entry to remind me to run Chocolatey app updates regularly, and keep list of apps I need to check manually.
  * [Pulsar edit beta](https://pulsar-edit.dev/download.html)
* Rationalise data stored on computer and setup backups.
* Install [CCleaner]() to clean out the registry, old files, get the drivers up-to-date
* Check computer manufacturer website for driver and BIOS updates
* Run commands using `Windows Powershell(admin)`
```
sfc /scannow
DISM.exe /Online /Cleanup-image /Restorehealth

```
