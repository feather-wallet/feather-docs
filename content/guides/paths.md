---
title: Paths
nav_title: Paths
category: faq
---

Feather writes to the following paths:

| What  | Linux     | macOS | Windows  |
|-------|-----------|----------|-------|
|[Wallet files](wallet-files)| ~/Monero/wallets/ | ~/Monero/wallets/ | C:/Users/\<USER\>/Documents/Monero/wallets/ | 
|**Program data** | ~/.config/feather/ | ~/Library/Preferences/ | C:/Users/\<USER\>/AppData/Local/FeatherWallet/ |

**Note:** The wallet files location is configurable, see [Wallet files](wallet-files) for more information.

The **Program data** folder contains the following files:

| What                  | File             | Description                                                                   |
|-----------------------|------------------|-------------------------------------------------------------------------------|
| Configuration         | `settings.json`  | JSON file containing wallet settings                                          |
| Tor program file      | `./tor/*`        | Bundled Tor program files, placed here when Feather starts                    |
| Fiat history database | `fiatHistory.db` | Text file with on each row: `YYYYMMDD:<XMR price in USD>`                     |
| Log files             | `libwallet.log*` | Monero core wallet implementation logs. Log files are not written by default. |

**Exceptions**:

- When [portable mode](portable-mode) is enabled or when Feather is running on Tails, Feather writes all files (including wallet files) to a folder named `feather_data` that resides in the same folder as the Feather program file.
