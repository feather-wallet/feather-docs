---
title: Installing Feather on Raspberry Pi
nav_title: Raspberry Pi
category: installation
weight: 200
---

Installation will only take a few minutes to complete. 

The estimated storage requirement is ~30 MB.

## Requirements

Before beginning the installation procedure, please check if your model is supported.

**Minimum system requirements**: ARMv7 or higher CPU, 512 MB (1 GB+ recommended) RAM, 2 or more cores recommeded.

| Model | Core Type | No. of Cores | RAM | Supported |
|-------|-----------|--------------|-----|-----------|
| 4 B   | Cortex-A72 (ARMv8)    | 4 | 1,2,4,8 GB | ✔️* |
| 3 B+  | Cortex-A53 (ARMv8)    | 4 | 1 GB, 2 GB | ✔️ |
| 3 A+  | Cortex-A53 (ARMv8)    | 4 | 512 MB | ✔️* |
| 3     | Cortex-A53 (ARMv8)    | 4 | 1 GB | ✔️* |
| 2     | Cortex-A7 (ARMv7)     | 4 | 1 GB | ✔️* |
| B+    | ARM1176JZF-S (ARMv6)  | 1 | 512 MB | ❌ |
| B     | ARM1176JZF-S (ARMv6)  | 1 | 256 MB | ❌ |
| Zero 2 W | Cortex-A53 (ARMv8) | 4 | 512 MB  | ✔️* |
| Zero (W,WH) | BCM2835 (ARMv6) | 1 | 512 MB  | ❌ |

\* = not tested ([let us know](report-an-issue)!)

## Downloading Feather

Download the latest AppImage for Raspberry Pi from [featherwallet.org/download](https://featherwallet.org/download).

Currently the 32bit version AppImage for Raspberry Pi is listed on the official download page. You can find more builds such as arm64 on [featherwallet.org/files/releases](https://featherwallet.org/files/releases/).

## Verifying the download (optional)

This section describes how to verify the AppImage file using PGP. You need a basic understanding of the Linux command line to follow the steps in this section. If you get stuck, feel free to [ask for help](report-an-issue).

Download the release signing key from the [git repository](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc). To save the file from Chromium: right click **→ Save As.. → Save**. (For alternative ways of obtaining the release signing key, see: [Release signing key](release-signing-key))

Go back to [featherwallet.org/download](https://featherwallet.org/download) and download the **signature** file for the AppImage  for Raspberry Pi.

Place both files in the same directory as the AppImage. You should now have a folder that contains `feather-x.x.x-arm.AppImage`, `feather-x.x.x-arm.AppImage.asc` and `featherwallet.asc`.

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

Now enter: `gpg --verify feather-x.x.x-arm.AppImage.asc` and press enter. Replace x.x.x with the correct version. If the signature is valid, the output should contain the following line:

```
gpg: Good signature from "FeatherWallet <dev@featherwallet.org>" [unknown]
```

If the signature is invalid, do not continue with the installation. Instead, [report](report-an-issue) this incident to the developers immediately.
## Starting Feather

Right click on the AppImage **→ Properties → Permissions**. Set "Execute" to "Anyone", close the window.

Again, right click on the AppImage **→ Open With → Accessories → Terminal**.

To start Feather, right click on the AppImage **→ Open**. Then click **Execute** if prompted.

If your system prevents you from changing the "Execute" permission, you can issue this command in your Terminal: chmod ugo-wrx [FullNameOfTheFeatherWallet]

If still you can't run Feather wallet, try to execute on Terminal by ```./feather.AppImage``` or ```/path/to/featherwallet.AppImage``` (The file name of Feather has been shortened for simplicity). In this way any possible issues with the missing packages can be revealed.

Having trouble getting Feather to start? Please [contact](report-an-issue) the developers.
