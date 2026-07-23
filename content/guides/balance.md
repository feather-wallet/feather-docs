---
title: Balance
nav_title: Balance
category: faq
---

The balance for your currently selected [account](accounts) is shown in the statusbar. You can click the balance label for a more detailed overview.

You can change the way the balance is displayed in the settings. (Settings → Appearance → Balance display).

Balance may be confusing to understand at first. Below is an overview of the terminology used in Feather and how it related to Monero.

#### Spendable balance

Funds that can be spent immediately.

#### Unconfirmed balance

The "unconfirmed" balance is the sum of incoming payments from unconfirmed transactions and locked transaction outputs.

All transaction outputs are locked (i.e. unspendable) for 10 blocks after the transaction that created them is included in a block. This is a Monero consensus rule.

A transaction output will automatically count towards the spendable balance after its lock has expired (i.e. it has gained enough confirmations).

Locked outputs will show up in the **Coins** tab with a green background color. Hover over the row to see how many confirmations it needs before it becomes spendable.

#### Total balance

This is the sum of your locked balance and spendable balance.


### Q: Why is (a part of) my balance unconfirmed after sending a transaction?

Whenever you send a transaction, its change output gets locked for 10 blocks. 

You can generally decrease the amount of balance that gets locked when you send a transaction by increasing the number of outputs your wallet owns. You can do this manually by [sweeping](sweep-output) a large output to yourself and splitting it in the desired number of outputs.

### Q: How does freezing an output affect my balance?

Frozen outputs do not count towards any balance. By freezing a coin its amount will be subtracted from your total balance.
