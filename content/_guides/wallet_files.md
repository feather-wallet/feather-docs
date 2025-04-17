---
title: Wallet files
nav_title: Wallet files
category: faq
---

## Location

To find out where the wallet files for the currently opened wallet are stored go to **Wallet → Information**.

To change the default directory go to **Settings → Paths**, and change the **Wallet directory**. Wallet files are not automatically moved to the new directory.

Wallet data for each wallet is stored in two files: the keys file and the cache file.

## Wallet files
### Keys file

The _keys file_ stores the wallet keys and wallet settings. This file has the `.keys` extension and is encrypted with the wallet password. The file plaintext is encoded in JSON format.

For a detailed overview of the data stored in this file see `wallet2::get_keys_file_data`.

**Warning**: Your funds will be irreversibly lost if you delete this file without having a backup of your mnemonic seed or private keys.

### Cache file

The _cache file_, commonly referred to as the *wallet cache*, stores transaction data, contacts, address labels, block hashes, the 14-word seed (if applicable), and other miscellaneous information. This file has no extension and is encrypted with the wallet password.

For a comprehensive overview of the data stored in the wallet cache, see [wallet cache viewer](wallet-cache-viewer).

If the wallet cache fails to open for any reason it is renamed to `<walletname>.old_cache` and a new cache file is generated in its place.

**Warning**: Transaction keys and your Polyseed CANNOT be recovered if this file is deleted.

### Address file

Non-mainnet wallets store an additional **unencrypted** file containing the primary address. It is named `<walletname>.address.txt`.

This file is used to distinguish wallets on different networks from eachother.


## Encryption

The keys and cache files are encrypted using the [chacha20 stream cipher](https://web.archive.org/web/20240606185144/https://www.cryptopp.com/wiki/ChaCha20). The KDF to generate the encryption key from the wallet password is 𝒄𝒓𝒚𝒑𝒕𝒐𝒏𝒊𝒈𝒉𝒕, a memory hard hash function that was used in Monero's proof-of-work before RandomX.

>The 𝒄𝒓𝒚𝒑𝒕𝒐𝒏𝒊𝒈𝒉𝒕 hash operates by first using Keccak 1600,
>the 1600 bit variant of the Keccak hash used in SHA-3, to create a 200 byte
>buffer of pseudorandom data by hashing the supplied data.  It then uses this
>random data to fill a large 2MB buffer with pseudorandom data by iteratively
>encrypting it using 10 rounds of AES per entry.  After this initialization,
>it executes 524,288 rounds of mixing through the random 2MB buffer using
>AES (typically provided in hardware on modern CPUs) and a 64 bit multiply.
>Finally, it re-mixes this large buffer back into
>the 200 byte "text" buffer, and then hashes this buffer using one of four
>pseudorandomly selected hash functions (Blake, Groestl, JH, or Skein)
>to populate the output.

From: `src/crypto/slow_hash.c` in the Monero submodule.

A modern CPU takes about 30-40 ms to run the KDF on a single core using the reference implementation. Specialized hardware and graphics card implementations exist that are orders of magnitude faster.

## Compatibility with other wallets

Wallet files are generally compatible with other Monero wallets. Meaning, you can create a wallet with the CLI or GUI and open it in Feather or vice versa. However, compatibility issues may occur if the the underlying wallet implementation versions differ too much. Before opening a wallet file in a different client, make sure both clients are up to date.
