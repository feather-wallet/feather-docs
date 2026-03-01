---
title: Tor support
nav_title: Tor support
category: faq
---

Feather works with Tor out of the box. You don't have to manually install Tor to use it.

Feather releases are bundled with a Tor binary. If the presence of a local Tor daemon on the default port (9050) is not detected, Feather will place the bundled Tor binary in the [config folder](paths) and run it on port 19450.

If you are unable to connect to the Tor network on your machine, you may configure Feather to use a different proxy (or no proxy at all). 

Feather can be configured to handle traffic to nodes in three different ways:

- Never over Tor
- Switch to Tor after initial synchronization (**default**)
- Always over Tor

You have the option to select the desired mode when Feather is started for the first time **before** any network connections are made. You can also change the mode in the **Settings → Network → Proxy** tab.

By default, Feather routes all network traffic over Tor, except for wallet synchronization. Synchronization requires a lot of data transfer and is therefore very slow over Tor. A remote node does not learn much about your wallet during synchronization (for more information see [Nodes](nodes)). We believe this is a reasonable privacy / convenience trade-off.

On Tails, Whonix, or when Feather is started with `torsocks`, all traffic is routed through Tor regardless of application configuration. Traffic to a [local node](local-node) is never routed over Tor.

### Configuration reference

This setting is stored as `torPrivacyLevel` in [`settings.json`](paths):

| Value | Mode | Description |
|-------|------|-------------|
| `0` | Never over Tor | Node traffic uses clearnet. Other traffic is still routed through Tor. A remote node can see your IP address. |
| `1` | Switch to Tor after sync (**default**) | Clearnet nodes are allowed during initial sync. Once the wallet is within `initSyncThreshold` blocks (default: 360) of the network height, only .onion nodes are used. |
| `2` | Always over Tor | All node traffic uses .onion nodes exclusively. Maximum privacy, but initial sync may be significantly slower. |

The related setting `initSyncThreshold` (default: `360`) controls how many blocks from the network tip the wallet must reach before switching to .onion-only nodes when `torPrivacyLevel` is set to `1`.

The **"Only allow connections to onion services"** checkbox (`torOnlyAllowOnion` in `settings.json`) is a separate override. When enabled, it forces .onion-only connections **regardless** of the `torPrivacyLevel` setting. For example, setting `torPrivacyLevel` to `0` (Never over Tor) while `torOnlyAllowOnion` is `true` will still restrict connections to .onion nodes only. Local nodes are always exempt from this restriction.

### Tails, Whonix and torsocks

On Tails, Whonix, or when Feather is started with `torsocks`, Feather will not start its own Tor daemon and assumes Tor is already running:

- **Tails**: Tor status is checked via the `tails-tor-has-bootstrapped.target` systemd unit.
- **Whonix**: Tor is assumed to be connected (Whonix routes all traffic through Tor at the OS level).
- **torsocks**: Tor is assumed to be connected (torsocks intercepts network calls transparently).

In all three cases, `torPrivacyLevel` still controls which nodes Feather will connect to. The proxy settings in the UI do not affect these environments.
