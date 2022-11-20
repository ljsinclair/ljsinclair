## Issue

Atom editor won't open a file in a new tab.

## Environment

Windows 10

## Cause

Who the hell knows? This happened for me after receiving a warning message from Github saying Atom editor was being retired.

## Remedial steps that didn't work

I tried these solutions on the command line with no success:

```
atom --safe    # open atom in safe-mode
atom --clear-window-state # clear all current settings, including git changes on projects
```

## Solution

I tried several things, but this is what worked for me.

### Step 1: rename and restart

1. rename the atom settings folder `.atom` in the user folder
2. start Atom as usual
3. test Atom will open a file.

## Step 2: atom opens file successfully

Copy settings files to the new `.atom` folder

1. Copy the following files from your old `.atom` folder:

```
config.cson
styles.less
```

2. Paste the files into the new `.atom` folder.
3. Restart atom.
