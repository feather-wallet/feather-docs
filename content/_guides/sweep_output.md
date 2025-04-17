---
title: How to sweep outputs
nav_title: Sweep outputs
category: howto
---

Make sure the **Coins** tab is enabled: **View → Coins**.

On the **Coins** tab, select one or more outputs to sweep. To select multiple outputs hold the Ctrl-key.

Right-click on a selected output **→ Sweep Output(s)**. A new dialog will open.

In the **Address** field, enter the address you want to sweep the coins to. Alternatively, check "Send to self (churn)" to send the output to your primary address.

By specifying the **number of outputs**, you may split the total sum of the selected outputs into a new number of outputs of equal amounts. The maximum number of outputs that can be created in a transaction is 16. This is a Monero protocol limitation.

### What is a sweep

A sweep transaction creates no change outputs. The total value of the sweeped coins is transferred to the destination address (minus miner fee).

### When to sweep

Sweeping may be useful in the following scenarios:

- You want to move outputs between subaddress accounts or wallets without having to worry about change outputs.
- You want to consolidate or churn specific outputs.

For regular spending use the **Send** tab. To send you entire balance, use the "Max" button on the **Send** tab.
