---
title: What is the wallet restore height?
nav_title: Restore height
category: faq
---

The restore height is the blockheight at which a wallet starts [scanning](synchronization) for transactions.

It is a mechanism to minimize the time and data required to restore a wallet.

You don't typically have to worry about the restore height when using Feather. Feather's [seed scheme](seed-scheme) embeds the wallet creation date, which is used to derive the restore height.

You may need to enter a restore height if you are:

- Restoring a wallet from a 25 word seed
- Restoring a wallet from a hardware device


In case you don't know your restore height, you may alternatively enter a wallet creation date when restoring a wallet. The wallet creation date will be used to estimate the appropriate restore height.

If you can't remember the exact date on which you created the wallet, enter the earliest possible date instead. For example: if you know you created the wallet sometime in 2019, enter 2019-01-01 as the wallet creation date.

If the restore height is set too high, synchronization will skip over some of your earlier transactions leading to an incomplete transaction history and [incorrect balance](incorrect-balance).


The restore height for any existing wallet can be found in **Help → Debug info**.
