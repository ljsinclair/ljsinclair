## Issue

After uninstalling MS Onedrive, the `Documents` folder remains under `C:\%username%\%appdata%\Onedrive`

Attempts to restore default results in long-winded windows message that basically says "Nope"

## Cause

In this case it's caused by Windows Defender ransomware settings

## Fixing

Turn off the Windows Defender setting
* Open Windows Defender
* Click Virus & Threat Protection > Ransomware Protection > Controlled Folder Access
* Toggle to **OFF**

Restore the default folder location

* RH click Documents folder > Properties > Location > Restore Default
* Click **OK** on the two dialogs, one to confirm this is what you want, the second to move all files within the folder to their new location.

## Changelog

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2020 | First published |
