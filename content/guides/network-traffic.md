---
title: Network Traffic
nav_title: Network Traffic
category: faq
---

This section provides an overview of the ways Feather can make network connections.


| To / Feature                | Description                                                | Handled by              |
|-----------------------------|------------------------------------------------------------|-------------------------|
| [Node](nodes)               | Synchronization, transaction construction                  |  epee       |
| [Websocket](websocket)      | Fiat price, CCS, current blockheight               |  Qt         |
| [Built-in updater](updater) | Contacts featherwallet.org if a new update is available. Depends on websocket.    |  Qt |
