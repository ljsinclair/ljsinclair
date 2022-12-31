---
title: My windows cleanup
---

## Issue

* Computer sluggish
* Application uninstalls have left a lot of crap behind
* Versions and updates aren't happening coherently

I could have done a system restore, **but** I was concerned this would also wipe out SSH keys, application settings and suchlike.

In hindsight it might have taken less time, however, I learned a few things by spring cleaning this way.

## Get operating system into shape

### Step 1 - run windows update

Update Windows to the latest build

* Start > Settings > Update & Security

### Step 2 - run windows commands to check and fix issues

* Run commands using `Windows Powershell(admin)`
```
sfc /scannow
DISM.exe /Online /Cleanup-image /Restorehealth

```

### Step 3 - Run troubleshooters

Some of the troubleshooters don't seem to do much, but they caught a couple of issues and fixed them

* Start > Settings > Update & Security > Troubleshoot

### Step 4 - update drivers

The computer manufacturer website had drivers available which updated the BIOS and other things.

* [How to properly update device drivers on Windows 10](https://www.msn.com/en-us/news/technology/how-to-properly-update-device-drivers-on-windows-10/ar-AA15KtIi)

## Rationalise personal data and setup backups

I had backups all over the place because of insufficient network backup drives.

In June I bought a new NAS with vast quantities of space which would definitely handle what I had.

### Step 1 - get backups into the right place

Get backup folders as high as possible in the tree so there's less likelihood of running into the old 256 character limit on path and file naming.

So for example, here's one way to set this up

```
├── Archive          # things to keep
├── Documents        # personal documents
├── Movies
├── Music
├── Pictures
├── Software         # any software or settings useful to keep
├── Television
```

### Step 2 - Setup data backups

Note: I didn't remember that Windows had its own backup system and I *may* migrate to that in future.

* [SyncFolder page on MS Store](https://apps.microsoft.com/store/detail/syncfolder/9NC73MJWHSWW?hl=en-us&gl=us)

### Step 3 - Install Chocolatey package manager

I'm sick to the teeth of having no idea when apps are out of date, and Chocolatey handles 90% of the apps I use with one simple interface.

* [Install Chocolatey](https://chocolatey.org/)

### Step 4 - Sort out apps Chocolatey doesn't handle

Around 10% of applications I use aren't listed on Chocolatey. So I'm managing them in two ways:

* Microsoft store manages the 3 or 4 apps I also use, and updates automatically
* Everything else I download and keep copies of (in the /software folder) and I have a calendar event to remind me to check for updates.

## Cleanup what's left

Windows OS gets cluttered with leftover files when applications are uninstalled or even just when they're being used.

I did use ccleaner to do some tidying, but the app doesn't have a great track-record. So I did this instead:

* [What you should use instead of ccleaner](https://www.howtogeek.com/361112/heres-what-you-should-use-instead-of-ccleaner/)
