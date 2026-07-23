---
title: "Help: Failed transaction"
nav_title: Failed transaction
category: troubleshooting
---

Use this guide if an outgoing transaction shows status "Failed" in the **History** tab.

Right-click on the failed transaction **→ Resend transaction**. Click **Broadcast** to submit the transaction to the selected node.

Check a block explorer (e.g. [xmrchain.net](https://xmrchain.net/txpool)) to verify that the transaction has reached the transaction pool. Try resending the transaction using a different node if it does not show up within a few minutes.

### Cause

A failed transaction is caused by a node's failure to relay your transaction to the Monero network. This can happen when the node you are connected to is misconfigured or poorly connected.

Relay failures are common in nodes that are configured with `--tx-proxy`, for this reason it is recommended to disable this option on publicly accessible nodes.

### Local node

If you are connected to a local node, you can alternatively manually relay the transaction by running the following command in the daemon console:

```
relay_tx <txid>
```
For example:
```
relay_tx 210557aa553718f8faced109768c54763702847e52f66f9ebdee7aceee90c4bc
```

If `monerod` is daemonized you can run:

```
monerod relay_tx <txid>
```

or via the JSON RPC with `curl`:

```
curl http://127.0.0.1:18081/json_rpc -d \
    '{"jsonrpc":"2.0", \
      "id":"0", \
      "method":"relay_tx", \
      "params":{"txids":["TXID_HERE"]}}' \
    -H 'Content-Type: application/json'
```

Replace `TXID_HERE` with the actual txid.
