---
title: Websocket
nav_title: Websocket
category: faq
---

The websocket server is a service hosted by the Feather developers that provides Feather Wallet clients with data from third party services.

It is used by the wallet to obtain pricing information, CCS & Reddit feeds, a curated list of remote nodes, the latest version of Feather Wallet and more. For more details view the table below.

The websocket server is only used to fetch information. The wallet does not send information about its state or the transactions you send to the websocket server. It is not used for any telemetry or crash reports. The wallet does not send a unique client id.

By default, Feather connects to the websocket server over Tor, unless configured otherwise in the proxy settings. This way your IP Address is not leaked to the websocket server.

This architecture was chosen for the simple reason that connecting to a single service leaks significantly less metadata than connecting to multiple third party services. 

When Feather starts it requests all available data. Clients cannot be fingerprinted based on their configuration. The server pushes updates when they become available.

The Feather developers can infer no information about any client, apart from:

- The total number of active connections to the websocket server.
- The time at which a client connects or disconnects
- Whether a client has previously connected

None of the above is actively tracked or recorded on the server.

The websocket server cannot make the client show arbitrary messages.

The following data is provided by the websocket server:

|key                        | description                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
|blockheights               | Current Mainnet and Stagenet blockheights. Used to speed up initial synchronization of newly created wallets.                                   |
|nodes                      | A curated list of high-performance nodes run by trusted members of the community. Includes status information such as their current blockheight.|
|crypto_rates               | Crypto exchange rates. Obtained from CoinGecko.                                                                                                 |
|fiat_rates                 | Fiat exchange rates. Obtained from CurrencyScoop and APILayer (fallback).                                                                       |
|ccs                        | Crowdfunding proposals from the Community Crowdfunding System and MAGIC Monero Fund. Displayed on the Home screen.                              |
|txFiatHistory              | Historical fiat prices. Obtained from CoinCap.                                                                                                  |
|updates                    | Latest FeatherWallet version.                                                                                                                   |
|𝐗𝐌𝐑𝐢𝐠                      | Latest 𝐗𝐌𝐑𝐢𝐠 downloads.                                                                                                                        |
|localmonero_countries      | List of countries supported by LocalMonero.                                                                                                     |
|localmonero_currencies     | List of currencies supported by LocalMonero.                                                                                                    |
|localmonero_payment_methods| List of payment methods supported by LocalMonero.                                                                                               |

### Disabling the websocket connection

We recognize that despite the privacy and security measures laid out above users with high threat models or those that enjoy a more minimal experience would like to disable the websocket connection. 

The initial setup wizard includes a page that allows users to disable the websocket server before any connection is made. Users that have upgraded from a lower version can disable the websocket connection by following the instruction below:

- Go to Settings → Network → Websocket.
- Uncheck "Enable websocket connection". 

This will immediately disable the websocket connection. This setting is persisted. The websocket connection can be re-enabled at any time. Some functionality that relies on the websocket server will be disabled.

The following tabs will be unavailable: Home, Calc, Exchanges.

The following functionality will be disabled: 

- Send: send by specifying a fiat amount
- History: historical fiat prices column
- Settings → Network → Node: updated list of websocket nodes.
- Mining → Downloads: the list of 𝐗𝐌𝐑𝐢𝐠 downloads will be unavailable.
