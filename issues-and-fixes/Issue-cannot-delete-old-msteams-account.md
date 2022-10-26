## Issue

msteams on Windows 10 retains previous login accounts regardless of whether you uninstall/reinstall the app, delete folders from `\Appdata` or delete users from Settings > Accounts pages.

## Cause

Unknown

## Solution

* Close Teams (double-check closed from the system tray, bottom right, hidden under the ^ button)
* Open Windows explorer and paste `C:\Users\%username%\AppData\Local\Packages\` into the address field.
* Delete this folder: `Microsoft.AAD.BrokerPlugin_*`
* Restart Teams

(From https://lnkd.in/gmCxFNNV)

## Changelog

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2021-04-03 | First published, and yes, it's a copy of someone else's work but I wanted to do this so I can find the solution later rather than hoping it'll remain at the destination. |
