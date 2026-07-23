---
title: Installing Feather on Windows
nav_title: Windows
category: installation
weight: 300
---

Installation will only take a minute to complete.

The estimated storage requirement is ~60 MB.

## Installing Feather

- Download the latest Windows installer from [featherwallet.org/download](https://featherwallet.org/download).
- Wait for the download to complete
- (Optional) Verify the download by following the instructions [below](windows#verifying-the-download)
- Run `FeatherWalletSetup.exe`.
- Follow through the screens in the setup wizard.
- Click 'Finish' to start Feather Wallet.

## Installing Feather (portable mode)

This section describes how to setup Feather in portable mode. For more information, see [Portable mode](portable-mode).

- Download the latest Feather standalone executable from [featherwallet.org/download](https://featherwallet.org/download).
- Wait for the download to complete
- (Optional) Verify the download by following the instructions [below](windows#verifying-the-download)
- Move the executable to the desired location (for example: on a USB stick).
- Create a file named `.portable` or `.portable.txt` in the same folder as the Feather executable.
- Start Feather by double-clicking on the executable.

## Verifying the download

- Download and install [Gpg4win](https://gpg4win.org/)
  - On the download page, select $0 to download the software for free.
  - During installation, make sure "Kleopatra" is selected on the Choose Components page

![You may leave "GpgOL" and "GpgEX" unchecked](/static/files/win-gpg-kleopatra.png)

- Obtain Feather's release signing key from the [Git repository](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc).
  - In Firefox/Tor Browser: Right click → Save Page As...
  - In Chrome: Right click → Save as...
  - (For alternative ways of obtaining the release signing key, see: [Release signing key](release-signing-key))

- In Explorer, double-click on `featherwallet.asc` to import the key in Kleopatra.

![Click "Ok" to close the window](/static/files/win-gpg-import-release-key.png)

- In Kleopatra, right-click the key named "FeatherWallet" → Certify.

![Right click → Certify](/static/files/win-gpg-certify.png)

- If you don't already have a GPG key you will be asked to create one:
  - You may enter any name and leave the e-mail field blank

![Click "Create" to create an OpenPGP certificate](/static/files/win-gpg-create-openpgp-cert.png)

![You may fill in anything here](/static/files/win-gpg-create-cert-info.png)

![Click "Ok" to move to the next window](/static/files/win-gpg-cert-created.png)

- You will now be asked to verify the fingerprint of Feather's release signing key.
   - **Check that the fingerprint matches**: `8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C`.
   - Only the letters and digits matter, you may ignore any extra or missing spaces.
   - We recommend that you also cross-check the fingerprint shown above through the domains listed [here](release-signing-key). By cross-checking the integrity of the fingerprint across multiple domains you can be confident that you obtained the correct key.
   - If the fingerprint does not match, click "Cancel" and do not continue with the installation procedure. Instead, [report](report-an-issue) this incident to the developers immediately.

![Make sure the fingerprint matches](/static/files/win-gpg-verify-fingerprint.png)

- The FeatherWallet key should now be certified:

![](/static/files/win-gpg-certified.png)

- Go back to [featherwallet.org/download](https://featherwallet.org/download) and download the **signature** file for the release you downloaded earlier.
  - Place it in the same folder as `FeatherWalletSetup-x.x.x.exe` or `feather-win-x.x.x.zip`

- In Explorer, double-click on the signature file you just downloaded. You should be presented with the following screen in Kleopatra:
  - The signature is valid if the output contains "**Valid signature from dev@featherwallet.org**". You may now proceed with the installation.
  - If the signature is invalid, do not continue with the installation. Instead, [report](report-an-issue) this incident to the developers immediately.

![Green background = good, anything else = bad](/static/files/win-gpg-verification-success.png)

