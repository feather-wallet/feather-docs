---
title: How to change the wallet password
nav_title: Change wallet password
category: howto
---

Before proceeding, make sure you have your [seed](show-wallet-seed) written down or stored securely. Without the seed there is no way to recover your wallet if you lose your password.

To change your wallet password go to **Wallet → Password** or click the lock icon in the statusbar.

It is recommended to set a strong password or passphrase generated with a password manager, such as [KeePassXC](https://keepassxc.org/).

After changing the password your [wallet files](wallet-files) will be re-encrypted with the new password.

### Moving from an insecure password

Saving the wallet files with a new password in many cases [does not overwrite the physical bits on the storage device](https://unix.stackexchange.com/a/593340), leaving the old wallet files intact and recoverable (e.g. through [filesystem metadata](http://manpages.ubuntu.com/manpages/bionic/man8/ext4magic.8.html), [file carving](https://en.wikipedia.org/wiki/File_carving), [snapshots](https://en.wikipedia.org/wiki/Snapshot_(computer_storage)) or other ways). If your wallet was previously encrypted with a weak password (or none at all) this may pose a security risk depending on your treat model.

Please note: wallet recovery is heavily dependent on file system, storage device and operating system. No standard solution exists and recovery attempts are not supported by the Feather developers.



