---
title: i2p support
nav_title: i2p support
category: faq
---

Feather can be configured to route all network traffic over I2P.

### Installing i2pd

Download the latest i2pd release from https://github.com/PurpleI2P/i2pd/releases

- Windows: `i2pd_x.xx.x-win64-mingw.zip`
- macOS: `i2pd_x.xx.x-osx.tar.gz`

Extract the archive and run the `i2pd` executable.

### Configuring Feather

Go to **Settings → Network → Proxy**. Select **i2p**. Click **Apply**.

If "**Let Feather manage this list**" is checked on the **Node** tab, Feather should now automatically connect to an i2p node.

All other network traffic, including the [websocket](websocket) connection (if enabled) will also be routed over I2P.