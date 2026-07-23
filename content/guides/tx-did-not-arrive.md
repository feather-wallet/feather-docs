---
title: "Help: transaction did not arrive"
nav_title: Transaction did not arrive
category: troubleshooting
---

Use this guide if you sent an **outgoing transaction** and the recipient claims they did not receive it.

If you are expecting an incoming transaction, but it hasn't shown up yet, follow the steps [here](missing-tx) instead.

### Is Feather up-to-date?

Some Monero protocol updates are backwards incompatible, old wallet versions stop working eventually.

If you sent the transaction using Feather Wallet 1.0.1 or earlier, your transaction is not valid on the current Monero network. Upgrade Feather to the latest version and resend the transaction.

You can find your current Feather version in **Help → About**.

You can find the latest version of Feather on [featherwallet.org/download](https://featherwallet.org/download).

On most operating systems you can use the [built-in updater](updater) to update to the latest version. To upgrade manually, see the installation guide for your specific operating system at the top of these docs.

### Does the transaction show up on a block explorer?

**Right-click** on the outgoing transaction **→ Copy → Transaction ID**.

Go to a public block explorer (e.g. [xmrchain.net](https://xmrchain.net)) and search for the transaction.

If the transaction does not show up, follow the steps [here](failed-tx).

### Was the transaction sent to the correct address?

**Right-click** on the outgoing transaction **→ Show details**.

Under "Destinations", check if the address matches the recipient address.

Funds that were sent to the wrong address are unrecoverable. Transactions are not reversible.

### Send the recipient a payment proof

If the transaction was included in a block and it was sent to the correct address, the issue is on the receiving side.

You may send the recipient a [payment proof](prove-payment) to persuade them that the transaction was sent correctly.