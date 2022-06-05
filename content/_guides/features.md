---
title: Feature comparison
nav_title: Feature comparison
category: faq
---

Feature comparison between Monero desktop wallets.

|Feature|Feather|CLI|GUI|
|-------|---|---|-------|
|**► The Basics**|
|[Subaddress accounts](switch-subaddress-account)    |✔|✔|✔|
|[Contacts](add-contact)                      |✔|✔|✔|
|Dark mode                                    |✔|✔|✔|
|[View-only wallet](create-view-only-wallet)  |✔|✔|✔|
|Language localisation                        |✖*|✔|✔|
|Wallet implementation                        |`wallet2` <sup>[0]</sup>|`wallet2`|`wallet2`|
|**► Seed & Keys**|
|Export secret keys                           |✔|✔|✔|
|[Seed scheme](seed-scheme)                   |14\|25|25|25|
|Supported seed languages                     |10 <sup>[1]</sup>\|12|12|12|
|**► Privacy & Security**|
|[Built-in Tor](tor-support)                  |✔|✖|✖|
|Socks5 proxy support                         |✔<sup>[2]</sup>|✔<sup>[2]</sup>|✔<sup>[2]</sup>|
|Address re-use mitigation                    |✔|✔|✖|
|[Encrypted wallet files](wallet-files)       |✔|✔|✔|
|[Reproducible builds](building-from-source)  |✔<sup>[3]</sup>|✔|✔<sup>[3]</sup>|
|Hide balance                                 |✔|✖|✔|
|Output blackballing                          |✖|✔|✔|
|Lock on inactivity                           |✔|✔|✔|
|**► Proofs / Messages**|
|[Sign/verify message](sign-verify-message)   |✔|✔|✔|
|[Verify transaction proof](verify-tx-proof)  |✔|✔|✔|
|[Formatted transaction proofs](formatted-tx-proofs)       |✔|✖|✖|
|[Create SpendProof](prove-tx-authorship)     |✔|✔|✔|
|[Create OutProof](prove-payment)             |✔|✔|✔|
|Create InProof                               |✔|✔|✖|
|Create ReserveProof                          |✖*|✔|✖|
|**► Coin Control**|
|Freeze/Thaw                                  |✔|✔|✖|
|[Sweep single](sweep-output)                 |✔|✔|✖|
|Sweep multi (selected)                       |✔|✖|✖|
|Sweep all                                    |✔|✔|✖|
|Output splitting                             |✔|✔|✖|
|**► Transactions**|
|[Multi-destination transactions](pay-to-many)|✔|✔|✔|
|[Transaction pusher](push-tx)                |✔|✖|✖|
|[Manual transaction import](missing-tx)      |✔|✔|✖|
|[Transaction rebroadcasting](failed-tx)      |✔|✖|✖|
|Multibroadcasting                            |✔|✖|✖|
|[Offline transaction signing](offline-tx-signing)              |✔|✔|✔|
|Transaction unlock time                      |✖†|✔|✖|
|Automatic network fee adjustment             |✔|✔|✔|
|Manual network fee adjustment                |✖<sup>[4]</sup>|✔|✔|
|[Multisig](multisig)                         |✖*|✔|✖|
|**► Mining**|
|Solo mining                                  |✔<sup>[5]</sup>|✔|✔|
|[Pool mining](mining-setup)                  |✔<sup>[5]</sup>|✖|✖|
|**► Hardware wallets**|
|Ledger Nano S/X                              |✔|✔|✔|
|Trezor Model T                               |✔|✔|✔|
|**► Fiat**|
|Crypto/fiat calculator                       |✔|✖|✖|
|Historical fiat prices                       |✔|✖|✖|
|Fiat balance display                         |✔|✖|✔|
|**► Cutting edge**|
|Atomic swaps                                 |✖*|✖|✖|
|P2Pool                                       |✖*|✖|✖|
|**► Misc**|
|Built-in updater                             |✔|✖|✔|
|Wallet autosave                              |✔|✖|✔|
|[Webcam QR code scanner](webcam-qr-scanner)  |✔<sup>[6]</sup>|✖|✔<sup>[7]</sup>|
|[Export history as CSV](export-tx-history)   |✔|✔|✔|
|Bruteforce wallet files                      |✔|✖|✖|
|Auto-open passwordless wallets               |✔|✖|✖|
|Copy-pasteable support template              |✔|✖|✖|
|Open multiple wallets  in single instance    |✔|✖|✖|
|Adjustable subaddress lookahead              |✖|✔|✔<sup>[8]</sup>|
|Local node manager                           |✖|✖|✔|
|[RPC Payments](rpc-payments)                 |✖†|✔|✖|
|Merchant mode                                |✖†|✖|✔|

**\*** = not yet  
**†** = no plans to support  
(0) = with modifications (see the feature branches for [feather/monero](https://github.com/feather-wallet/monero))  
(1) = Feather uses BIP-39 wordlists, for Monero see [here](https://github.com/monero-project/monero/tree/master/src/mnemonics). As of 1.0.0 only English is supported for 14 word seeds.  
(2) = authentication not supported  
(3) = except macOS  
(4) = read the rationale [here](transaction-fee)  
(5) = with XMRig  
(6) = except Linux standalone binaries  
(7) = except Linux release  
(8) = only for hardware wallets  

Missing something? [Let us know](report-an-issue).
