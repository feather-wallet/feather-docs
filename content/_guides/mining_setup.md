---
title: How to mine Monero using Feather
nav_title: Setup mining
category: howto
---

Go to the **Mining** tab. (If not shown, go to **View → Mining**).

### Downloading 𝐗𝐌𝐑𝐢𝐠

Within the **Mining** tab, go to the **Downloads** tab.

**Right click → Download file** on the latest 𝐗𝐌𝐑𝐢𝐠 version for your operation system.

After the download is complete, extract the file.

### Configuring Feather for mining

Within the **Mining** tab, go to the **Settings** tab.

##### 𝐗𝐌𝐑𝐢𝐠 executable

Click **Browse** and navigate to the location of the 𝐗𝐌𝐑𝐢𝐠 executable that was downloaded in the previous step.

##### Run as admin/root

Running 𝐗𝐌𝐑𝐢𝐠 as admin/root may increase hashrate. Click **Yes** if you want to enable this.

**Note:** As of 1.0.0 this feature is not supported on Windows, yet.

##### CPU threads

Use the slider to select the number of CPU threads to mine on.

- A high number of threads may slow down your computer.
- A high number of threads may not give the optimal hashrate. Experiment with different values.

##### Mining mode

Select whether to mine to a pool or to solo mine using a local node.

If this is your first time mining Monero, we recommend using **Pool mining**.

##### Pool address (Pool mining)

Select the pool you want to mine to from the dropdown menu.

- If your pool isn't listed, click **Configure** to add it manually.

##### Node address (Solo mining)

Enter the address of your local node. In most cases this should be `127.0.0.1:18081`.

##### Network settings

Select "Secure connection (TLS)" if you want to encrypt traffic.

**Note:** Not all pools support this. Check your pool's website for more information.

Select "Connect via Tor" if you want to route all traffic to the pool or node over Tor. This may increase the rate of stale shares, which negatively impacts your payout.

##### Receiving address

Enter the address you want to mine to. Click **Use primary address** to fill in the current wallet's primary address.

##### Password (optional)

If your pool requires a password, enter it here.

### Start mining

Within the **Mining** tab, go to the **Status** tab.

Click on **Start mining**.

If your computer becomes slow or unresponsive, click **Stop**. Adjust the number of **CPU threads** to a lower value.

If you are have trouble getting the miner to start, please [contact](report-an-issue) the Feather developers for assistance.
