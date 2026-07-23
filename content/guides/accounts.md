---
title: Accounts
nav_title: Accounts
category: faq
---

Each wallet has the ability to create multiple accounts. Each account has its own balance, transaction history and set of addresses.

Accounts are deterministically derived from your private keys, you only need to know your seed in order to restore the accounts and addresses associated with your wallet.

It may be useful to use a separate account:

- For bookkeeping purposes (for example: one account for personal transactions, one for work transactions, one for donations).
- To keep identities separate. (**Caution**: using accounts does not protect you against the [Janus attack](https://web.getmonero.org/2019/10/18/subaddress-janus.html).)

Using a new account is faster than creating a new wallet file as it eliminates the need to [synchronize](synchronization) multiple wallets. Creating accounts does not significantly slow down wallet synchronization.

To learn how to create a new account or to switch between accounts, see [Switch subaddress account](switch-subaddress-account).

Sending a transaction that spends outputs from multiple accounts is not supported.
