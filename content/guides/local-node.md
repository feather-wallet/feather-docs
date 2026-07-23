---
title: How to connect to a local node
nav_title: Connect to local node
category: howto
---

Go to **Settings → Network → Node**. Uncheck **Let Feather manage this list**. Click "Add custom node(s)". In the textbox enter the `IP:port` of your local node.

A node that runs on the same machine as Feather will be accessible on IP: `127.0.0.1`. The table below shows the default port for monerod depending on the network:

| Network | Port  |
|---------|-------|
| MAINNET | 18081 |
| TESTNET | 28081 |
| STAGENET| 38081 |

**Example**: To connect to a MAINNET node that is running on the same machine as Feather you should enter `127.0.0.1:18081` into the textbox.

Nodes running on the following IPv4 address blocks are considered to be local nodes:

- 127.0.0.0/8
- 172.16.0.0/12
- 192.168.0.0/16

Feather does not route traffic to local nodes over Tor.
