---
title: Formatted transaction proofs
nav_title: Formatted transaction proofs
category: faq
---

Formatted transaction proofs is a PGP-like message format used to conveniently share Monero transaction proofs without having to copy multiple fields.

Here is an example:

```
-----BEGIN OUTPROOF-----
Network: Monero Mainnet
Txid: 46d9f3eaf8d25b6a5d0847ad0beaece8b153d1b8c25ce317934ec17223025806
Address: 463o7kTG4n2AEHNhhV91BK7kZsKd4vRh78xt6LM7Px7o3cp5eZgyuyLHVAWeEkfLcoC78WMZuJ3xZ1SiM4RhbciCB8b8pGS

A small donation.
-----BEGIN OUTPROOF SIGNATURE-----

OutProofV2SWYVZHfqBwYGNYxDRZryBdXomxA9hS3VLWiRiQZ9YNutAGoq1QxB7j
AYwRrhoxJBQ8jj7XCNNfvSwgQaVFjWY5EQHJRW3LgPtV3UmefmQ2wFJPh2iTaCH8
zETWpxTrf2RiVY
-----END OUTPROOF SIGNATURE-----
```

To learn how to verify formatted transaction proofs in Feather, see: [Verify transaction proof](verify-tx-proof).

---

### For developers:

Formatted transaction proofs can be parsed using this regular expression:

(Newlines added for readability)

```
-----BEGIN (?<type>\w+)-----\n
Network: (?<coin>\w+) (?<network>\w+)\n
Txid: (?<txid>[0-9a-f]{64})\n
(Address: (?<address>\w+)\n)?
\n?
(?<message>.*?)\n
-----BEGIN \1 SIGNATURE-----\n
\n?
(?<signature>.*?)\n
-----END \1 SIGNATURE-----
```

Where:

- `type` is one of [`SpendProof`, `OutProof`, `InProof`]
- `coin` is `Monero`
- `network` is one of [`Mainnet`, `Stagenet`, `Testnet`]
- `txid` is a 64 character hexstring
- `address` is a valid Monero address for the given `network`. 
  - MUST be present if `type` is `OutProof` or `InProof`.
  - MUST NOT be present if `type` is `SpendProof`.
- `message` is an optional arbitrary length message that may contain newlines
- `signature` is the proof signature
  - SHOULD be split into chunks of 64 characters over multiple lines
