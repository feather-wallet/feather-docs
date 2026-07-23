---
title: "Help: missing transaction"
nav_title: Missing transaction
category: troubleshooting
---

Use this guide if you are expecting an incoming transaction, but it hasn't shown up yet.

### Is Feather up-to-date?

Some Monero protocol updates are backwards incompatible, old wallet versions stop working eventually. New wallet versions may also contain important bugfixes and security updates.

You can find your current Feather version in **Help → About**.

You can find the latest version of Feather on [featherwallet.org/download](https://featherwallet.org/download).

On most operating systems you can use the [built-in updater](updater) to update to the latest version. To upgrade manually, see the installation guide for your specific operating system at the top of these docs.

**Note**: All Feather versions 1.0.1 and below stopped working after August 13 2022. Upgrade to Feather 2.0.0 to be able to connect to the network.

### Is your wallet synchronized?

The wallet needs to scan the blockchain to find your transactions. The statusbar will tell you how many blocks are still remaining. Wait for this process to complete.

The statusbar will show "Synchronized" when the wallet is synchronized.

For more information, see [Synchronization](synchronization).

### Does the transaction show up on a block explorer?

Go to a public block explorer (e.g. [xmrchain.net](https://xmrchain.net)) and search for the transaction. If it doesn't show up the transaction wasn't relayed properly, contact the sender to notify them of the issue.

If the transaction was sent using Feather, the sender may [rebroadcast](failed-tx) the transaction to resolve the issue.

### Manually import the transaction

If the transaction shows up on a block explorer, follow the steps to [manually import your transaction](import-transaction).

### Verify the address

If you tried manually importing the transaction, and it told you that the transaction doesn't belong to your wallet, please verify that the address you sent the funds to belongs to your wallet.

Go to **Tools → Address checker**, enter the address you sent the funds to. If it tells you that the address does not belong to your wallet, a few things could have happened:

- You have opened the wrong wallet file
- You did not copy the address correctly when you sent the transaction ([never manually type an address!](receive-transaction))
- You have [copy-paste malware](https://medium.com/chainreport/copy-paste-malware-crypto-multipliers-4a0c09c7730a) installed on your computer

Unfortunately, we can't help you recover your funds if you sent XMR to an address that doesn't belong to your wallet.

### Ask the sender for a payment proof

If none of the above worked, ask the sender to provide you with a payment proof (OutProof) or the transaction secret key. 

Learn how to verify proofs in Feather [here](verify-tx-proof). You can verify transaction secret keys by using [xmrchain.net](https://xmrchain.net). Look up your transaction ID and click "Prove sending".

If the sender can not produce a valid payment proof, they may have not sent you any funds!
