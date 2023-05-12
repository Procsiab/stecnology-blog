---
title: "Update LineageOS keeping root"
date: 2023-05-12
draft: false
tags: ["root", "lineage", "android"]
description: "A step-by-step guide on how to update LineageOS over the air"
---
## What is this "root" thing?

If you are not familiar with the concept of root access on Android, you may not need to follow these steps in order to update your LineageOS install.

This guide is aimed at who has installed LineageOS and afterwards gained root access on it through [Magisk](https://github.com/topjohnwu/Magisk).

## I know how to update my mobile OS

Indeed, if your smartphone is supported with LineageOS updates OTA (over the air), the update process is in theory straightforward; however, if Magisk was installed, than you may loose the root access after applying the update.

This guide is applicable to all devices supported by LineageOS 19.1 and 20, and Magisk version 25 or greater.

## Follow the instructions

|||
|:-|:-|
|1. Open the "Settings" app, then navigate to "System", then "Updates"|![Step 1](/update_ota_lineage/step01.jpg)|
|2. Tap the curved arrow button at the top right of the screen to refresh, or if the updates were already checked out you may find them in the list below: tap the "Download" button|![Step 2](/update_ota_lineage/step02.jpg)|
|3. After the download has completed, tap the "Install" button relative to the downloaded update|![Step 3](/update_ota_lineage/step03.jpg)|
|4. Click "OK" to accept the prompt that will appear|![Step 4](/update_ota_lineage/step04.jpg)|
|5. This process will take a few minutes: you shall wait for it to complete, but note that it will continue in the background if you need to use another app in the meantime|![Step 5](/update_ota_lineage/step05.jpg)|
|6. When the installation is completed, the "Restart" button will appear relative to the downloaded update: you **should not** tap it, but rather close the updater app!|![Step 6](/update_ota_lineage/step06.jpg)|
|7. Open the Magisk app, then tap the "Install" button on the "Home" tab|![Step 7](/update_ota_lineage/step07.jpg)|
|8. Under the "Method" selection, choose the third option called "Install to inactive slot (after an OTA update)"|![Step 8](/update_ota_lineage/step08.jpg)|
|9. Accept the prompt that will appear, tapping the "OK" button|![Step 9](/update_ota_lineage/step09.jpg)|
|10. The "Let's go!" button will now be selectable: tap on it|![Step 10](/update_ota_lineage/step10.jpg)|
|11. A terminal screen will pop up, reporting the steps performed to install Magisk; if all went well, the last line should be the string `- All done!` and the "Reboot" button should appear at the bottom right corner; tapping this button will reboot the system and apply the update installed before, while keeping Magisk installed|![Step 11](/update_ota_lineage/step11.jpg)|

You may want to check from the system settings and from Magisk if the update installed correctly and Magisk is still correctly installed.
