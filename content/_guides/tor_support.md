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
