---
title: First start
nav_title: First start
category: getting-started
weight: 0
---

This section will guide you through the short wizard that shows up when you start Feather for the first time.

If you are looking to install Feather, see the **Installation** section in the sidebar.

---

- If you experience any difficulties while using Feather, have a question related to this documentation, or want to submit a feature request, please feel free to [contact](report-an-issue) the developers.

- In the sidebar, near the bottom, is a **Troubleshooting** section that will help you solve common issues.

---

## How do you want to connect to the Monero network?

Feather must connect to a node in order to scan for your transactions. A node is a computer hosting a copy of the Monero blockchain. (For more information, see [Nodes](nodes).)

Connecting to node hosted by a third party comes with some privacy risks. Please review the information in [Nodes](nodes) to learn if these risks are relevant to your threat model.

### Auto connect

Feather has a built-in list of high-performance nodes hosted by the Feather team and trusted members of the Monero community. In most cases you want to let Feather pick one of these nodes at random.

We recommend using this option for **most** users.

### Connecting to a custom remote node

If you do not want to connect to one the built-in nodes, select **Select node manually**.

Enter the address and port in the textbox. For example: `node.monerodevs.org:18089`.

### Connecting to a local node

Feather automatically detects the presence of a [local node](local-node) on the default port.

Feather does not manage a local node for you. 
If you want to run a local node, follow the steps in [this guide](https://moneroguides.org/tutorials/01x02-setting-up-your-own-node/) to set one up.

## How should Feather route its network traffic?

By default, Feather routes all network traffic over Tor, except for wallet synchronization. Synchronization requires a lot of data transfer and is therefore very slow over Tor. A remote node does not learn much about your wallet during synchronization (for more information see [Nodes](nodes)). We believe this is a reasonable privacy / convenience trade-off.

We recommend using the default option unless:

- You are unable to connect to the Tor network, or
- Your threat model requires always connecting over Tor

For information see: [Tor support](tor-support) and [Network traffic](network-traffic).

## Do you want to obtain third-party data?

For more information, see: [Websocket](websocket).
