---
title: Hardware wallets
nav_title: Hardware wallets
category: faq
---

### Are hardware wallets supported?

**Yes**. Feather supports the following devices:

#### Ledger

- Nano S
- Nano S+
- Nano X
- Stax
- Flex

#### Trezor

- Model T
- Safe 3
- Safe 5

If you own a device that is advertised as having support for Monero and it is not listed above, please [contact](report-an-issue) us.

For instructions on how to use your device with Feather see the following guide: [Create a wallet (hardware device)](create-wallet-hardware-device).

### Overview

| Hardware Wallet | Secure Element                                                          | Peripherals connected to SE | Passphrase | Data transfer  | Open Source Firmware             |
|-----------------|-------------------------------------------------------------------------|-----------------------------|------------|----------------|----------------------------------|
| Ledger Nano S   | Yes ([ST31H320](https://www.st.com/en/secure-mcus/st31h320.html) [1])   | No                          | Yes [5]    | USB            | No                               |
| Ledger Nano X   | Yes ([ST33J2M0](https://www.st.com/en/secure-mcus/st33j2m0.html) [2])   | Yes                         | Yes [5]    | USB, Bluetooth | No                               |
| Ledger Nano S+  | Yes ([ST33K1M5](https://www.st.com/en/secure-mcus/st33k1m5c.html) [3])  | Yes                         | Yes [5]    | USB            | No                               |
| Ledger Stax     | Yes ([ST33K1M5](https://www.st.com/en/secure-mcus/st33k1m5c.html) [6])  | Yes                         | Yes [5]    | USB, Bluetooth | No                               |
| Ledger Flex     | Yes ([ST33K1M5](https://www.st.com/en/secure-mcus/st33k1m5c.html) [10]) | ?                           | Yes [5]    | USB, Bluetooth | No                               |
| Trezor Model T  | No                                                                      | No                          | Yes [7]    | USB            | Yes, reproducible builds [8] [4] |
| Trezor Safe 3   | Yes (OPTIGATM Trust M (V3) [9])                                         | ?                           | Yes [7]    | USB            | Yes, reproducible builds [8] [4] |
| Trezor Safe 5   | Yes (OPTIGATM Trust M (V3) [9])                                         | ?                           | Yes [7]    | USB            | Yes, reproducible builds [8] [4] |

[1] https://www.ledger.com/improving-and-supporting-the-ledger-nano-s  
[2] https://shop.ledger.com/products/ledger-nano-x#shopify-section-tech-specs--nano-x  
[3] https://www.ledger.com/blog/ledger-op3n-conference-product-launches-updates-our-next-milestones  
[4] https://docs.trezor.io/trezor-firmware/common/reproducible-build.html  
[5] https://www.ledger.com/academy/passphrase-an-advanced-security-feature  
[6] https://shop.ledger.com/products/ledger-stax  
[7] https://trezor.io/learn/a/passphrases-and-hidden-wallets  
[8] https://github.com/trezor/trezor-firmware  
[9] https://trezor.io/learn/a/secure-element-in-trezor-safe-devices
[10] https://shop.ledger.com/products/ledger-flex
