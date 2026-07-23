---
title: How to export the transaction history
nav_title: Export transaction history
category: howto
---

Go to **Wallet → History → Export CSV**. Enter a filename, and click **Save**.

The transaction history is a CSV file with the following schema:

|field|type|example|description|
|-----|----|-----------|-------|
|blockHeight|integer|2317852|Block that included the transaction|
|timestamp|integer|1615848678|Unix timestamp of when the block was mined (roughly)|
|date|string|2021-03-15T23:51:18Z|ISO 8601 formatted|
|accountIndex|integer|0|[Account](accounts) index that tx was sent from or received to. **Note**: Transactions sent between accounts will show up multiple times.|
|direction|string|out|"in" for incoming transactions, "out" for outgoing transactions. Churn transactions are considered outgoing.|
|balanceDelta|float|-0.202417740000|Total change in balance as a result of the transaction. Value is negative for outgoing transactions.|
|amount|float|0.202400000000|Total amount that was received or sent in this transaction. **Does not include the transaction fee.** Shows 0 for churn transactions. Value is absolute. |
|fee|float|0.000017740000|The network fee that was paid for the transaction. **Note**: For incoming transactions this fee was paid by the sender.|
|txid|string|449f065...876206|Transaction ID. (Example shortened for readability.)|
|description|string|Donation to Monero Core|Transaction description|
|paymentID|string||Payment ID. Usually blank.|
|fiatAmount|float|20.2|Amount is always rounded to 3 significant digits. Shows "?" if value cannot be calculated.|
|fiatCurrency|string|USD|Fiat currency|

