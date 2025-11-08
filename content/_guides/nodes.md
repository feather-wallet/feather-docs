---
title: What is a node?
nav_title: Nodes
category: faq
---

A node is a computer running software that maintains a copy of the Monero blockchain.

We can distinguish between two types of nodes: local nodes and remote nodes.

A **local node** is a node that runs on your own computer or a private network. Typically, you run a local node yourself.

A **remote node** is a node that is accessible on a public network. Typically, a third party runs a remote node. Remote nodes are referred to as public nodes in some contexts.

By default, Feather connects to a random node from a curated list of high performance remote nodes run by trusted members of the Monero community. When Feather is started for the first time, you have the option to configure how the wallet will connect to a node **before** any connections are made.

You can change how Feather connect by going to **Settings → Network → Nodes**.


If you would like to set up your own public node, see this [excellent guide](https://sethforprivacy.com/guides/run-a-monero-node/) by Seth.

### Q: Are remote nodes safe?

This depends on your threat model.

A remote node:

- doesn't know your addresses
- doesn't know your balance
- cannot steal your funds
- cannot detect your incoming transactions
- does not know what addresses you're sending money to or how much

However, a malicious remote node can:

- execute an attack that may reveal the true input of a transaction. This attack does not reveal how much is spent or to whom. This attack has a low chance of succeeding and Feather will warn you if it detects this attack.
- make your outgoing transactions stick out by manipulating the transaction fee that you pay.
- associate your outgoing transactions with your IP address (but only if all traffic is routed through clearnet, see [Tor support](tor-support) for more information. By default, transactions are broadcast over Tor.)

---

### For developers

The wallet communicates with the node via a JSON/binary interface: [Daemon RPC](https://www.getmonero.org/resources/developer-guides/daemon-rpc.html).

During normal use the wallet will use the following endpoints:

|Endpoint       | Purpose | Comment                        |
|---------------|------------------------------------------|
|get_info      | General | Provide basic information about the status of the node and Monero network. Results are cached for 30 seconds. |
|/get_blocks.bin| Sync    | Obtain block data for wallet synchronization |
|/get_hashes.bin| Sync    | Get block hashes. Saved in wallet cache (m_blockchain). |
|/get_transaction_pool_hashes.bin| Sync | Get tx hashes from transaction pool. Called every 10 seconds after main sync is finished. |
|/get_transactions| Sync | Get pool transactions the wallet hasn't scanned before. |
|/get_output_distribution| Tx Construction | Output distribution used in decoy selection. Data is hashed and checked against a hardcoded value to mitigate against output distribution poisoning.<br>In Feather, the distribution is requested and cached immediately upon finishing wallet synchronization to cut bandwidth requirements for transaction construction by an order of magnitude. |
|/get_outs.bin| Tx Construction | Request output public keys for selected indices of ring members. The wallet cannot verify the validity of the public keys, except for the true input. Feather will show a warning if the true input is missing from the response. |
|get_fee_estimate| Tx Construction | Get base transaction fee. Malicious nodes can introduce a fungibility defect by providing an incorrect fee estimate. |
|hard_fork_info | Tx Construction | Get information about hard fork state. |
|/send_raw_transaction | Tx Broadcast | Instruct the node to broadcast the transcation to the network. |


