---
title: How to send a transaction
nav_title: Send a transaction
category: getting-started
weight: 110
---

### Paying to a single address

Go to the **Send** tab.

In the **Pay to** field, enter the address you want to transfer funds to. You may also enter an [OpenAlias](https://openalias.org/) (email-like address that forwards to a Monero address). You may also paste a QR code image encoding a Monero address or Monero payment request into this field ([video demonstration](/static/files/qr_paste.mp4)).

In the **Description** field, you may enter an optional transaction description. The description is not sent to the recipient of the funds, it only exists for your own bookkeeping. The description is stored in the wallet cache, and displayed in the **History** tab.

In the **Amount** field, enter the amount you want to send. This is the exact amount the recipient will receive, it does not include the transaction fee. To send all your balance, click the **Max** button.

To construct the transaction, click **Send**. You will be able to review the transaction details and transaction fee before broadcasting.

If you are using a hardware wallet you may need to authorize the transaction on the device. Transaction construction on a hardware device can take several minutes.

After transaction construction is complete, a dialog will pop up asking you to verify the transaction details. To view detailed information, such as the inputs spent in the transaction, click **Advanced**.

Click **Send** to broadcast the transaction after you have verified the details, or **Cancel** if something is wrong.

Unconfirmed outgoing transactions will show up in the **History** tab with a gears icon. If several minutes pass and the transaction does not show up in your node's mempool its status will change to **Failed**. If the transaction does not show up in a publicly accessible mempool (e.g. [xmrchain.net](https://xmrchain.net/txpool)), you may assume the node was unable to relay your transaction. Follow the instruction [here](failed-tx) to resolve.

### Pay to many (multi-destination transaction)

See: [Pay to many](pay-to-many)

### Sweeping a single / multiple output(s)

See: [Sweep outputs](sweep-output)
