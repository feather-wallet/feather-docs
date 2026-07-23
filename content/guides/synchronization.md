---
title: What is wallet synchronization?
nav_title: Synchronization
category: faq
---

Wallet synchronization, or "wallet refresh", is the process of scanning the blockchain to look for transactions that belong to your wallet.

In order to do this the wallet obtains block data from a [node](nodes) in sequential order, starting from the last processed block. This is known as the "wallet height", and can be found in **Help → Debug Info**. Transactions that belong to your wallet are saved in the [wallet cache](wallet-files). All other data is discarded.

Transactions that are included in blocks higher than the wallet height will not be reflected in your balance or show up in your history until synchronization is complete. The status bar will show 'synchronized' when it is complete.

All block data is scanned locally. A [node](nodes) does not learn anything about your transactions in the synchronization process.

Synchronization is known to take much longer over [Tor](tor-support). We therefore recommend configuring the wallet to synchronize the wallet over clearnet. This is the default, unless Feather is started on an operating system that forces all traffic through Tor, such as Tails or Whonix.
