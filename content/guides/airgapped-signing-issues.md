---
title: "Help: airgapped signing issues"
nav_title: Airgapped signing issues
category: troubleshooting
---

Main article: [Offline transaction signing](offline-tx-signing)

### The QR Code is too bright/dark and can't be scanned

- If your webcam supports it, enable "Manual exposure" and adjust the slider so the QR code is clearly visible
- Resize the window to increase the size of the QR code
- Adjust the brightness of your monitor
- Enable dark mode (Settings -> Appearance -> Theme)
- Hold the webcam closer or farther away from the monitor
- Move to a brighter environment, turn on overhead lighting
- Click the settings icon next to the QR code and decrease the fragment length and decrease the speed (by increasing the ms / fragment)
- Try with a different webcam

### The progress bar is stuck on 99%

Keep scanning until it hits 100%. It might take a few seconds if the scanner missed a fragment.

### My webcam is detected but the screen is black

Please [report](report-an-issue) this issue.

Windows 10 users: service pack 22H2 or higher is required.

### My webcam is plugged in but Feather does not detect it

Click the 'Refresh' button. If it still doesn't show up you may need to install missing drivers.

### I'm getting "double spend" errors when submitting my transaction

Go to Wallet -> Advanced -> Rescan spent.
