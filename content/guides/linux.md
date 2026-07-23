---
title: Installing Feather on Linux
nav_title: Linux
category: installation
weight: 100
---

Using **TailsOS?** See the instructions [here](tails) instead.

## Flatpak

### Install

```
flatpak install --from https://featherwallet.org
```

### Verify (recommended)

Authenticate the GPG key to verify that the Flatpak is genuine.

```
gpg --show-keys --with-fingerprint /var/lib/flatpak/repo/feather.trustedkeys.gpg
```

The output should contain a line that says:

```
Key fingerprint = 8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C
```

Make sure the fingerprint shown above matches the output in your terminal. Only the letters and digits matter, you may ignore any extra or missing spaces.

We recommend that you cross-check the fingerprint through the domains listed [here](release-signing-key). This way you can be confident that you obtained the correct key.

If any of the fingerprints don't match:

- Delete the application (`flatpak remote-delete feather`), and
- [Report](report-an-issue) this incident to the developers immediately.

### Run

Click the shortcut in your application menu, or:

```
flatpak run org.featherwallet.Feather
```

---

## AppImage

Download the latest AppImage for Linux from [featherwallet.org/download](https://featherwallet.org/download).

### Verifying the download (optional)

This section describes how to verify the AppImage file using PGP. You need a basic understanding of the Linux command line to follow the steps in this section. If you get stuck, feel free to [ask for help](report-an-issue).

Download the release signing key from the [git repository](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc). To save the file from Tor Browser: right click **→ Save Page As.. → Save**.
(For alternative ways of obtaining the release signing key, see: [Release signing key](release-signing-key))

Go back to [featherwallet.org/download](https://featherwallet.org/download) and download the **signature** file for the AppImage.

Place both files in the same directory as the AppImage. You should now have a folder that contains `feather-x.x.x.AppImage`, `feather-x.x.x.AppImage.asc` and `featherwallet.asc`.

In a terminal, `cd` to the directory that contains the files and enter: `gpg --import featherwallet.asc` and press enter. The output should contain a line that says:

```
gpg: key 0x1F76E155CEFBA71C: public key "FeatherWallet <dev@featherwallet.org>" imported
```

Now enter: `gpg --list-keys dev@featherwallet.org` and press enter. The output should contain a line that says:

```
Key fingerprint = 8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C
```

Make sure the **fingerprint** shown above matches the output in your terminal. We recommend that you also cross-check the fingerprint through the domains listed [here](release-signing-key). By cross-checking the integrity of the fingerprint across multiple domains you can be confident that you obtained the correct key.

If the fingerprint does not match, do not continue the installation. Instead, [report](report-an-issue) this incident to the developers.

Now enter: `gpg --verify feather-x.x.x.AppImage.asc` and press enter. Replace x.x.x with the correct version. If the signature is valid, the output should contain the following line:

```
gpg: Good signature from "FeatherWallet <dev@featherwallet.org>" [unknown]
```

If the signature is invalid, do not continue with the installation. Instead, [report](report-an-issue) this incident to the developers immediately.

### Starting Feather

After the download is complete, **make sure to allow executing the file as a program**. You can often find this setting in the Properties → Permissions tab in your file explorer. Alternatively, run `chmod +x feather-x.x.x.AppImage` in a terminal.

You should now be able to run the AppImage by double-clicking on the file in a file explorer. If that does not work, try right-clicking on the file, and look for "Run" or "Open". Alternatively, you can start Feather by typing `./feather-x.x.x.AppImage` in a terminal.

Having trouble getting Feather to start? Please [contact](report-an-issue) the developers.
