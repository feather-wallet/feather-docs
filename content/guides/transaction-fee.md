---
title: Transaction Fee
nav_title: Transaction Fee
category: faq
---

Feather automatically adjusts the transaction fee based on the number of transactions in the mempool. This behavior is identical to the “automatic” fee option in the GUI.

#### Can I manually select the fee-tier?

Yes. In the settings, go to the transactions tab and enable "manual fee-tier selection". A selection box will appear on the Send tab.

#### My outgoing transaction still hasn't confirmed, what can I do?

First, make sure the transaction shows up in a block explorer. You can do this by entering the txid into [xmrchain.net](https://xmrchain.net).

If the transaction does not show up, try rebroadcasting the transaction by following the steps [here](failed-tx).

If the transaction shows up, all you can do is wait. Your transaction should be included in a block soon, unless an atypical network event is ongoing (e.g. spam attack, network upgrade, etc). Check any of the Monero community hangouts for more information.

#### Who receives the transaction fee?

The fee is paid to the entity that mines the block that includes the transaction. The Feather developers do not take a cut from the transaction fee.
