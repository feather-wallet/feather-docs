---
title: Updater
nav_title: Updater
category: advanced
---

Feather will show a message in the status bar when a new update is available. We usually wait until a few hours after a release before advertising the update to clients. If you want to update your wallet as soon as a new release is available, go to **Help → Check for updates**.

We recommend keeping your wallet software up to date, as new versions may include important security improvements and bug fixes.

Updates that are installed via the built-in updater are verified in multiple ways to ensure authenticity. For more information read the section below titled **Update security**.

If you choose to update your wallet, the update will be placed alongside the old executable in the same directory. You may delete the old executable after you have verified that the new version starts properly on your machine.

### Update security

The websocket server notifies the client of the latest Feather version.

If the reported version is higher than the current version, Feather will obtain a PGP-signed textfile containing the file hashes for the update from a hardcoded domain over Tor. It will verify if the textfile was signed using the [release signing key](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc) and if the filename matches the new version. The release signing key is included in the Feather binary and does not have to be obtained during the update procedure.

It will notify the client that a new update is available. After the user downloads the update, the downloaded archive is hashed and compared against the signed hash. The update is aborted if the hash does not match.


### Disabling the update notification

If you don't want to run the latest version of Feather and do not want to be bothered by the update notification:

- Go to **Settings → Display**
- Check "**Hide update notifications**"
