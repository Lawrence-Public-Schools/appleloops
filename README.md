# appleloops
`appleloops` is a Python 3 utility to download audio content that Apple provides for GarageBand, Logic Pro, and MainStage.

## Updates
- Python 2 is deprected. Requires Python 3.9.5 minimum.

## Functionality
- Downloads additional audio content from `audiocontentdownload.apple.com`.
- - Fetch the latest content for specific apps.
- - - Defaults to checking five "minor" releases ahead and ten "patch" releases ahead (for example, GarageBand 10.(4-9).(4-14))
- - Fetch all the content for all the apps.
- Create a DMG of downloaded content.
- Installs audio content packages on macOS devices that already have a qualifying audio app from Apple installed.
- - Can use a Caching Server or local HTTP mirror, or even a DMG (hosted or local).
- - Only installs packages that need to be installed, skipping over packages that are already installed.
- - Upgrades packages that have had newer versions released (depends on Apple including correct versioning for each package).
- Patches known issues with the source property list files shipped with audio apps or mirrored on Apple's content server.
- Logs are stored in the current users's `Application Support/com.github.carlashley/appleloops/logs` folder for non-deployment runs.
- - Logs for deployment runs are written to `/var/logs/appleloops.log`.
- - Logs are rotated for each run.
- Compare the differences between two releases of the same audio app.
- - Defaults to a 'unified' style of diff'ing (similar output to `diff -u`).
- - Choice of two diff styles that output to stdout or generate a HTML document containing a table of differences.
