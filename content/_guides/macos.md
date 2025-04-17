---
title: Installing Feather on macOS
nav_title: macOS
category: installation
weight: 400
---

Installation will only take a minute to complete.

The estimated storage requirement is ~70 MB.

### Installing Feather

- Download the latest Application Bundle from [featherwallet.org/download](https://featherwallet.org/download).
- (Optional) Verify the download by following the steps in the [next section](macos#verifying-the-download)

![Open Feather zip](/static/files/macos-zip-extract.png)

- If the .zip file is not already extracted, right-click on the .zip file → open.

![Feather app bundle](/static/files/macos-app-bundle.png)

- Drag Feather app into "Applications" in the sidebar.
- Go to Applications
- Right click on Feather -> Open


### Verifying the download

- Download and install [GPG Suite](https://gpgtools.org/)
  - You can use the default settings in the installer

![](/static/files/macos-gpg-tools-dmg.png)

![](/static/files/macos-gpg-tools-installer.png)

- Click "Ok" to give the "Installer" access to control "GPG Keychain"

![](/static/files/macos-gpg-tools-keychain.png)

- If you don't already have a GPG keypair, you will be asked to create one:
  - You may enter any name and e-mail address
  - You do not need to publish the key

![](/static/files/macos-gpg-new-keypair.png)

- Obtain Feather's release signing key from the [Git repository](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc)
  - In Safari/Tor Browser: Right click → Save Page As..
  - (For alternative ways of obtaining the release signing key, see: [Release signing key](release-signing-key))

- In GPG Tools, click on "Import" and open `featherwallet.asc`

![](/static/files/macos-gpg-select-signing-key.png)

![](/static/files/macos-gpg-import-success.png)

- In GPG Tools, right-click on key named FeatherWallet and select "Sign"
  - **Check that the fingerprint matches**: `8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C`
  - Only the letters and digits matter, you may ignore any extra or missing spaces.
  - We recommend that you also cross-check the fingerprint shown above through the domains listed [here](release-signing-key). By cross-checking the integrity of the fingerprint across multiple domains you can be confident that you obtained the correct key.
  - If the fingerprint does not match, click "Cancel" and do not continue with the installation procedure. Instead, [report](report-an-issue) this incident to the developers immediately.
  - You may leave "Publish" unchecked.
  - Click "Sign" when you have confirmed the fingerprint.

![](/static/files/macos-gpg-sign-release-key.png)

![](/static/files/macos-gpg-sign-release-key-success.png)

- Go back to [featherwallet.org/download](https://featherwallet.org/download) and download the **signature** file for the release you downloaded earlier.
  - Place it in the same folder as `feather-x.x.x.zip`

- Right-click on the `feather-x.x.x.zip.asc` signature file → Open With → GPG Services.service

![](/static/files/macos-gpg-verify-release.png)

- You should be presented with a window that confirms that the signature is trusted:
  - If the signature is valid you should see "Trusted signature" (see below). You may now proceed with the installation.
  - If the signature is invalid, do not continue with the installation. Instead, [report](report-an-issue) this incident to the developers immediately.

![](/static/files/macos-gpg-trused-signature.png)