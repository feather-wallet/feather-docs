---
title: How to verify a transaction proof
nav_title: Verify transaction proof
category: howto
---

Feather supports verification of the following transaction proofs:

- **SpendProof**: Proves authorship of a transaction
- **OutProof**: Proves a payment
- **InProof**: Proves ownership of an output

ReserveProofs are not currently supported.

Go to **Tools → Verify transaction proof**.

### Formatted proof

A formatted proof looks like a PGP message.

Select the **Formatted** tab at the top. Paste the proof into textbox and click **Verify**.

If the proof is valid you will now see a green checkmark along with the text "Proof is valid".

### Non-formatted proof

Select the **Manual** tab at the top. Select the type of proof you want to verify.

Fill in the required fields and click **Verify**. A message box will pop up displaying the validity of the proof.