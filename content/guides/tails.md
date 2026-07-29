---
title: Installing Feather on Tails
nav_title: Tails
category: installation
weight: 200
---

Installation will only take a few minutes to complete. 

The estimated storage requirement is ~30 MB.

## Configuring the Persistent Storage

Tails is an amnesic operating system. By default, files are not saved to your USB drive and are thus lost after the computer is restarted. Only files stored on the _Persistent Storage_ are kept across different working sessions.

We strongly recommend that you store Feather on the Persistent Storage. This way, you won't have to reinstall Feather and restore your wallets each time you start Tails.

You need to configure the Persistent Storage before you can use it. If you have already configured the Persistent Storage, skip ahead to the next section.

Go to **Applications → System Tools → Persistent Storage**.

Enter a strong password to protect the Persistent Storage. Files on the Persistent Storage are encrypted with your password.

Follow through the remaining screens. You do not need to enable any additional settings.

You must restart Tails before you can continue with the installation. When you get to the Tails greeter enter your password to unlock the Persistent Storage.

The Persistent Storage will show up in the File Browser as a folder named `Persistent`. You can quickly access it from the sidebar.

## Downloading Feather

Download the latest AppImage for Tails from [featherwallet.org/download](https://featherwallet.org/download). 

Save the file to your Persistent Storage. (Click on `Persistent` in the sidebar.)

## Verifying the download (optional)

This section describes how to verify the AppImage file using PGP.

Download the release signing key from the [git repository](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc). To save the file from Tor Browser: right click **→ Save Page As..**. Save the file to the Peristent Storage.

(For alternative ways of obtaining the release signing key, see: [Release signing key](release-signing-key))

Go back to [featherwallet.org/download](https://featherwallet.org/download) and download the **signature** file for the Tails AppImage.

You should now have a folder that contains `feather-x.x.x-a.AppImage`, `feather-x.x.x-a.AppImage.asc` and `featherwallet.asc`.

In the file browser, right click on some empty space and select **Open in Console**.

In the Terminal enter: `gpg --import featherwallet.asc` and press enter. The output should contain a line that says:

```
gpg: key 0x1F76E155CEFBA71C: public key "FeatherWallet <dev@featherwallet.org>" imported
```

Now enter: `gpg --list-keys dev@featherwallet.org` and press enter. The output should contain a line that says:

```
Key fingerprint = 8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C
```

Make sure the **fingerprint** shown above matches the output in your terminal. Only the letters and digits matter, you may ignore any extra or missing spaces. 

If the fingerprint does not match, do not continue the installation. Instead, [report](report-an-issue) this incident to the developers.

Now enter: `gpg --verify feather-x.x.x-a.AppImage.asc` and press enter. Replace x.x.x with the correct version. If the signature is valid, the output should contain the following line:

```
gpg: Good signature from "FeatherWallet <dev@featherwallet.org>" [unknown]
```

You can safely ignore the following warning:

```
WARNING: This key is not certified with a trusted signature!
         There is no indication that the signature belongs to the owner.
```

If the signature is invalid, do not continue with the installation. Instead, [report](report-an-issue) this incident to the developers immediately.

After verification is complete you can delete both `.asc` files.

## Starting Feather

Right-click on the AppImage **→ Properties**. Make sure "Executable as Program" is enabled. You will only have to do this once.

To start Feather simply double-click on the AppImage. If the program doesn't start, try right click **→ Run**.

Having trouble getting Feather to start? Please [contact](report-an-issue) the developers.
