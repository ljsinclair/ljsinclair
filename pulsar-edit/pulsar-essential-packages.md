# Essential packages for Pulsar Edit

Pulsar's core functionality can be extended by installing packages written by people around the planet.

## Navigating big files

*Minimap* gives a zoomed-out representation of file content which is a little easier to use than a simple scrollbar.

* [Minimap](https://web.pulsar-edit.dev/packages/minimap)
* [Minimap lens](https://web.pulsar-edit.dev/packages/minimap-lens) extends that again by giving a magnifying-glass view of where the mouse pointer is on the Minimap representation.

## Backup and restore your pulsar-edit environment

*Sync settings* and *Sync settings to Git* allow you to backup and restore your pulsar-edit environment including:

* Pulsar settings
* Pulsar configuration
* Themes
* Packages and settings

The benefit of this approach is you can restore your settings with the click of a menu item rather than digging through backups.

* [sync settings package](https://web.pulsar-edit.dev/packages/sync-settings) -- a package that allows you to backup and restore all the above to a directory on your network
* [sync settings to Github](https://web.pulsar-edit.dev/packages/sync-settings-git-location) -- extends Sync Settings so you can backup to Git

NOTE: There's also other *sync-settings to [destination]* packages available if Git isn't your preference.

## Load and save specific projects in the project tree

I find it useful to keep work, volunteering and personal projects separate.

*Save workplace* allows you to:
* save a collection of project folders under a specified workspace name
* alternate between workspaces
* save changes to workspaces under an existing or new name

Changes are saved to the pulsar edit `config.cson` file.

* [save workspace](https://web.pulsar-edit.dev/packages/save-workspace)

## Which Git branch am I in?

Git integration in Pulsar-edit is IMO far better than competing applications. I find the tabs easier to understand and it uses the status bar to provide additional information and functionality.

It's also useful to see the current branch of projects in the tree view.

That's where *Tree view git status* comes in handy.

* [Tree view git status](https://web.pulsar-edit.dev/packages/tree-view-git-status)

## See also

* [essential packages for writers](https://github.com/ljsinclair/ljsinclair/blob/main/pulsar-edit/pulsar-essential-writers.md)
