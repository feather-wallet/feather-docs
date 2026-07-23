---
title: How to prove a payment
nav_title: Prove payment 
category: howto
---

### OutProof

OutProofs are the preferred way to prove a payment to an address.

Go to the **History** tab. Right-click on the transaction that includes the payment you want to prove, then click **Create tx proof**. Select "Prove payment to an address". Add a message if required, and make sure to select the correct destination address.

To export your proof as a PGP-like message, click **Get Formatted Proof**. Note that only Feather Wallet currently supports this format. If the recipient does not use Feather Wallet, click **Get Signature**. 

To verify the transaction proof the receiver needs the Signature, Address, Message and Txid. A formatted proof includes all these details.

### Transaction Secret Key

Some services may require you to provide a "transaction secret key" to prove a payment. To obtain this key, go to the **History** tab. Right click on a transaction **→ Show details**. Click on **Copy Tx Secret Key**.
