---
title: How to create/restore a wallet from a hardware device
nav_title: Create a wallet (hardware device)
category: getting-started
weight: 20
---

To learn if your hardware device is supported see [supported hardware devices](hardware-wallet-support).

Make sure your hardware device is connected to your computer.

**Ledger**: Open the Monero app on your device.  
**Trezor**: Unlock the device.

---

If you are using Linux, make sure you have applied the appropriate udev rules to allow device access:

**Ledger**: [https://github.com/LedgerHQ/udev-rules/blob/master/add_udev_rules.sh](https://github.com/LedgerHQ/udev-rules/blob/master/add_udev_rules.sh)  
**Trezor**: [https://trezor.io/learn/a/udev-rules](https://trezor.io/learn/a/udev-rules)

---

If the wizard isn't already open in Feather, go to **File → New/Restore**.

In the wizard, select **Create wallet from hardware device**.

On the next page, **select the device type**. If your device isn't listed here, it is not (yet) supported. You can also find the list of supported devices, [here](hardware-wallet-support).

Select **Create new wallet file from device**, if:

- This is the first time you are setting up a Monero wallet from your hardware device, or
- The keys on the device hold no funds.

Select **Restore a wallet from device**, if

- You have previously sent/received Monero from/to the device.

If you selected **Restore wallet from device**, you will now be asked to enter the wallet [restore height](restore-height). If you don't know your restore height, enter the date you purchased the hardware device in the **Wallet creation date** field. A restore height will automatically be calculated from the entered date.

Proceed through the wizard by choosing a name for your wallet files and setting a password.

