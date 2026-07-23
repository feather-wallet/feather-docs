---
title: How to use the webcam QR code scanner
nav_title: Use webcam QR code scanner
category: howto
---

On the **Send** page, click **Scan**. A new dialog should pop up.

If your device has multiple cameras, select the desired camera to use for scanning in the combobox at the bottom.

Hold the QR code in front of the camera and wait for the dialog to close. Once the QR code is detected the fields on the **Send** tab should become populated with the information from the QR code.

If you have trouble getting the QR code to scan make sure that:

- The QR code is in full view of the camera.
- The QR code is oriented correctly.
- There is no glare on the QR code from other light sources.
- The image isn't too bright. Lowering the brightness of the device showing the QR code might help.

### The viewfinder is black

Make sure to remove any webcam covers that might be present on your device. If that is not the issue please [report](report-an-issue) a bug and include the webcam model and operating system.

### Feather reports that no cameras are available

Try restarting your machine and reseat the USB cable if applicable. Can other programs see the device? If no clear cause can be found, please [report](report-an-issue) a bug and include the webcam model and operating system.

### "Feather was built without webcam QR scanner support"

All official releases should have webcam QR scanner support enabled. If you are using an unofficial release, ask the package maintainer to enable webcam scanner support.