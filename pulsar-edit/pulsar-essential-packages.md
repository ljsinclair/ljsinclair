# Essential packages for Pulsar Edit

Pulsar's core functionality can be extended by installing packages written by people around the planet.

## Navigating big files

Minimap gives a zoomed-out representation of file content which is a little easier to use than a simple scrollbar.

* [Minimap](https://web.pulsar-edit.dev/packages/minimap)
* [Minimap lens](https://web.pulsar-edit.dev/packages/minimap-lens) extends that again by giving a magnifying-glass view when you mouse over the Minimap representation.

## Backup and restore your pulsar-edit environment

These packages allow you to backup and restore your pulsar-edit environment including:
* Pulsar settings
* Pulsar configuration
* Themes
* Packages and settings

The benefit of this approach is you can restore your settings with the click of a menu item rather than digging through backups.

* [sync settings package](https://web.pulsar-edit.dev/packages/sync-settings) -- a package that allows you to backup and restore all the above to a directory on your network
* [sync settings to Github](https://web.pulsar-edit.dev/packages/sync-settings-git-location) -- extends Sync Settings so you can backup to Git

## Load and save specific projects in the project tree

I find it useful to keep work, volunteering and personal projects separate.

Save workplace allows you to:
* save a collection of project folders under a specified workspace name
* alternate between workspaces
* save changes to workspaces under an existing or new name

* [save workspace](https://web.pulsar-edit.dev/packages/save-workspace)

## Which Git branch am I in?

Git integration in Pulsar-edit is IMO far better than competing applications like VSCode[^903b]. The tabs are IMO easier to understand, and it provides additional information on the Pulsar edit toolbar, such as the current branch.

I've found it useful to also have the branch represented in the project tree view. That's where Tree view git status comes in handy.

* [Tree view git status](https://web.pulsar-edit.dev/packages/tree-view-git-status)

---
[^903b]: Ironically enough, Pulsar-edit is a fork of Atom editor, which was retired by Github (and Microsoft) in favour of VSCode.
