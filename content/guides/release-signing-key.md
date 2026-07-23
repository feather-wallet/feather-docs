---
title: Obtaining the release signing key
nav_title: Release signing key
category: advanced
---

You can obtain the _release signing key_ from our [GitHub repo](https://raw.githubusercontent.com/feather-wallet/feather/master/utils/pubkeys/featherwallet.asc) or [featherwallet.org](https://featherwallet.org/files/featherwallet.asc).

It can also be obtained from a keyserver:

```bash
gpg --keyserver hkps://keys.openpgp.org --search dev@featherwallet.org
gpg --keyserver hkps://keyserver.ubuntu.com --search dev@featherwallet.org
```

### Fingerprint

After importing the key, verify that the fingerprint matches: 

```
8185 E158 A333 30C7 FD61 BC0D 1F76 E155 CEFB A71C
```

We recommend that you cross-check the fingerprint shown above through the resources listed below. This way you can be confident that you obtained the correct key.

- [Matrix channel description](https://matrix.to/#/#feather:monero.social)
- [monero.town community sidebar](https://monero.town/c/featherwallet)
- [monerosecurity.org](https://monerosecurity.org)
- [X profile](https://twitter.com/FeatherWallet)
- Through DNS (Linux): `drill -D key.featherwallet.net TXT`

If any of the resources listed above do not have a matching fingerprint, please [report](report-an-issue) this to the developers immediately.
