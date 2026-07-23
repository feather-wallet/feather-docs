---
title: How to sign / verify a message
nav_title: Sign / verify a message
category: howto
---

Go to **Tools → Sign/verify message**.

### Signing a message

In the **Message** textbox, enter the message you want to sign. You may enter multiple lines. Special characters are allowed. You may leave this field blank if you only want to prove ownership of an address.

In the **Address** textbox, enter the address you want to sign the message with. By default, your wallet's primary address is filled in. You may enter any (sub)address belonging to your wallet.

Click **Sign** to sign the message. Click **Copy to clipboard** to copy all fields to your clipboard. 

A signed message can only be verified if the verifier has all three pieces of information (message, address and signature), sharing only the signature is not enough.

### Verifying a message

In the **Message** textbox, enter the message. Do not include the address or signature. The message is case-sensitive.

In the **Address** textbox, enter the address the message was signed against.

In the **Signature** textbox, enter the signed message's signature. Signatures should start with "SigV2".

Click **Verify** to verify the message. A message box should pop-up displaying the validity of the signed message.
