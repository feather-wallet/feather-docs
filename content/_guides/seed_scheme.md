---
title: Seed scheme
nav_title: Seed scheme
category: faq
---

Feather uses [Polyseed](https://github.com/tevador/polyseed) for 16 word mnemonic seeds. Versions prior to 2.0.0 used the (deprecated) [monero-seed](https://github.com/tevador/monero-seed) library for 14 word mnemonic seeds.

Feather can restore wallets from Polyseeds, 14 word and 25 word seeds.

Polyseed has a number of advantages over Monero's standard seeds:

- The wallet creation date is embedded in the mnemonic seed. This way you no longer have to worry about restoring your wallet from the correct restore height.
- It uses BIP-39 wordlists. These wordlists container shorter and more common words than Monero's lists.
- Polyseeds seeds are quicker to write down and memorize.

### Supported languages

| Language              | Polyseed (BIP-39) | 25-word (Monero) |
|-----------------------|-------------------|------------------|
| English               | ✔                 | ✔                |
| Japanese              | ✔                 | ✔                |
| Korean                | ✔                 | ✖                |
| Spanish               | ✔                 | ✔                |
| Chinese (simplified)  | ✔                 | ✔                |
| Chinese (traditional) | ✔                 | ✖                |
| French                | ✔                 | ✔                |
| Italian               | ✔                 | ✔                |
| Czech                 | ✔                 | ✖                |
| Portuguese            | ✔                 | ✖                |
| Dutch                 | ✖                 | ✔                |
| Esperanto             | ✖                 | ✔                |
| German                | ✖                 | ✔                |

**Note**: as of 2.0.0 only English is supported for Polyseed.

All BIP-39 wordlists can be found [here](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md).

### I have a 14 word seed, will I be able to restore it in the future?

Yes. Feather will support restoring 14 word seeds indefinitely. You do not need to transfer the funds to a new wallet.

### Can I convert my 14 word seed into a Polyseed?

No, this is not possible. If you want a Polyseed you must create a new wallet.

### Convert Polyseed seed into 25-word seed

Go to **Wallet → Seed**, enter your password, and check **Show 25 word seed**. Make sure to also note the restore height to make restoring the wallet faster.

### Convert 25-word seed into Polyseed

This is not possible. Polyseed uses a [KDF](https://en.wikipedia.org/wiki/Key_derivation_function) to derive the actual spendkey, this operation is non-reversible.
