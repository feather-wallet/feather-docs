---
title: Transaction pusher
nav_title: Transaction pusher
category: advanced
---

Feather has a built-in transaction pusher that can submit a raw transaction to a specified node.

Transactions are always submitted over Tor, except when submitted to a local node.

Go to **Tools → Broadcast transaction → From text**.

In the **Transaction** textbox, paste the transaction hexstring.

In the **Node** groupbox, select whether to submit the transaction to the currently connected node or use a custom node.

Click **Broadcast** to submit the transaction to the node. It may take a few minutes before the transaction shows up in the **History** tab (if it belongs to the currently opened wallet).