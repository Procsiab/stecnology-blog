---
title: "Sustainable Smartphones"
date: 2023-04-25
draft: false
tags: ["smartphone", "lineage", "android"]
description: "How to reduce mobile e-waste, and save a buck"
---
![Cover image](/xperiaxa2_lineage_info_crop.jpg)
*My XperiaXA2 from 2018, running on Android 12 thanks to Lineage OS*

## Planned obsolescence

As a matter of fact, the main goal of research and development in the smartphone industry is not to deliver a product with high longevity and powerful usability, but rather to make the cheapest bundle of the latest features (for the ones who follow the innovators) or to make the most money by proposing the most requested features in an expensive *"flagship"* model.

Continuing to support each model that is built and sold is at the lower bottom of the manufacturer's priority list: think about the unavailability of **original** replacement parts for your current smartphone, or about the two or three years of software security updates, after which the hardware is just left behind by the manufacturer.

Does this mean that an optimal experience is only available by swapping our smartphone every two years? While manufacturers wants us to believe so, I shall present you with an alternative strategy that can reduce e-waste, and also save you money: buy a **used smartphone**, and install **free software**[^1] on it!

[^1]: Free as in freedom, for reference: [Free Software Foundation](https://www.fsf.org/)

## Battered does not mean useless

If you don't mean some usage signs on your smartphone, shopping online for a used one is pretty easy nowadays - otherwise you may look for sellers near you, and meet them in person to check the conditions of the item before purchasing it; moreover, old used smartphones that a couple of years ago were sold for hundreds of Euros (I am making these claims by looking at the European market of used smartphones), can be had today for a fraction of the price.

For example, I recently came across a OnePlus 6T for just 120€ (less than a third when new) and it has aged pretty well with [its specifications](https://www.gsmarena.com/oneplus_6t-9350.php)! Also, from the link to the spec. sheet you can find out that the latest Android update available is to version 11 (we are at version 13 at the time of writing); in fact, the issue to address with an used smartphone, after going through the extra steps involved in getting one, is to install **up to date software** on it.

There are, however, unknown heroes that use their spare time and their passion to contribute to the [Lineage OS](https://lineageos.org/) project, which aims to support as much Android smartphones as possible with an up to date operating system installation, based on the latest Android version; many smartphone models are officially supported, and for many others there is at least one person who is continuing to build the system for: think about the Galaxy S4, which is currently a 10-year old smartphone but is [still supported](https://forum.xda-developers.com/t/optimized-lineageos19-1-v8-3-28feb-2023.4426575/) with Android 12 available to install on it!

## Can I install Lineage OS?

The installation procedure is unique to every device because of the quirks of the original software, however there are some steps that are conceptually the same; I will briefly list them below, but you can expect a much more detailed explanation for the officially supported models on the [Lineage OS Wiki](https://wiki.lineageos.org/devices/) (for example, [this](https://wiki.lineageos.org/devices/fajita/install) is the installation guide for the OnePlus 6T):

- Enable ADB over USB
- Unlock bootloader
- Reboot fastboot
- Install Lineage's recovery
- Flash Lineage OS
- Optionally flash Google's services
- Reboot to Lineage OS

The list above is not huge, and the official wiki has got you covered for every other detail you may need, however you should research carefully that the smartphone model you got or you are going to buy is exactly the one mentioned on Lineage's website. Be aware that variants for the same model may exist for different markets or regions, and not always they are all supported.

## The benefits of Free Software

With Lineage OS running on your smartphone, and no "Google Apps" installed during the flashing steps, you got basically *the* Android experience, without any trackers or highly privileged services in the background (\**cough*\* [Google Play Services](https://medium.com/androiddevnotes/google-play-services-under-the-hood-android-3b781d325309) \**cough*\*). However, some applications may refuse to work without the Play Store or Play Services available on the system.

In my opinion this is an acceptable trade-off, since I value my privacy and my control over my tools more than an out of box experience the same as intended by a proprietary third party (like Google); however, you should not be let down by some malfunctioning app: in fact, there exists another free software project called [MicroG](https://microg.org/) that aims to **replace the Play Services** with software that runs on your device and does not report back to Google.

With MicroG on Lineage OS, I am running fine every more or less proprietary Android app since 2019 without any huge blocking issue; however, do expect some broken features: for example Google Pay is not usable, and some apps that rely on Google Maps to show information may just render a blank page instead. This also means that you should look for alternative free apps that do the same, and there are plenty!

## Alternative applications do exist

When you run a *"de-Googled"* operating system, you should whenever possible look for a free application that does not rely on Google Play Services, to avoid issues and (in my opinion) to enhance your privacy: the best place to look for free mobile software is [F-Droid](https://f-droid.org/), which hosts many open source and libre apps from different independent developers.

In case you may need a proprietary app from the Play Store, you'll want to use the [Aurora Store](https://gitlab.com/AuroraOSS/AuroraStore) client instead: it's an anonymous client that let you download, install and update apps from the Play Store's repository, without the requirement of a Google account. Note that Aurora Store can be downloaded right from F-Droid 😎 .

I will also list below some alternative apps to perform the tasks I use my smartphone for, that can be all obtained through F-Droid[^3]:

| Task | Related App Name |
|-|-|
| QR scanner | [Binary Eye](https://github.com/markusfisch/BinaryEye) |
| Password manager | [Bitwarden](https://github.com/bitwarden/mobile) |
| Calender synchronization | [DAVx5](https://github.com/bitfireAT/davx5-ose) |
| E-Mail | [K-9 Mail](https://github.com/thundernest/k-9) |
| Phone sharing on PC | [KDE Connect](https://github.com/KDE/kdeconnect-android) |
| Map navigation | [Magic Earth](https://www.magicearth.com/)[^2] |
| Browser | [Mull](https://github.com/Divested-Mobile/mull-fenix) |
| PDF Viewer | [MuPDF viewer](https://github.com/ArtifexSoftware/mupdf-android-viewer) |
| Note taking | [Nextcloud Notes](https://github.com/nextcloud/notes-android) |
| RSS feed reader | [Nunti](https://gitlab.com/ondrejfoltyn/nunti) |
| Music | [ViMusic](https://github.com/vfsfitvnm/ViMusic) |
| Weather | [Rain](https://github.com/DarkMooNight/Rain) |
| VPN | [Tailscale](https://github.com/tailscale/tailscale-android) |
| Messaging | [Telegram FOSS](https://github.com/Telegram-FOSS-Team/Telegram-FOSS) |

The apps I listed above are not tied to Lineage OS or the absence of Google's system services: this means you can use them also on your device manufacturer's Android system distribution.

[^2]: Magic Earth is proprietary, however is also free to use and has no trackers or loggers bundled. A popular and free software alternative to check out is [OsmAnd](https://osmand.net/)
[^3]: Some apps I listed are distributed through the developer's repository, which should be added to the F-Droid client to be able to get the app through it

## You are in control

Controlling the tool you own means also having full access to it: I apply this principle to my devices that run an operating system by enabling the *"root"* (administrative) access on them: this means, for an Android system, being able to make modifications to enhance your privacy or circumvent limitations.

For example, you may want to replace the default [SystemWebView](https://stackoverflow.com/questions/32356646/security-risks-for-using-webview-ios-android) component with a more hardened or up to date one, or you may want to disable trackers and logging components of a proprietary app through [Warden](https://forum.xda-developers.com/t/app-5-0-warden-app-manager.4122227/), which requires root access to do that.

There are many more things that root access unlocks on your system: if you are interested, a reliable way of getting root access on Lineage OS is to install [Magisk](https://github.com/topjohnwu/Magisk) on your device, following [their wiki](https://topjohnwu.github.io/Magisk/install.html); in addition, most root tweaks and modifications are distributed as "Magisk modules", therefore in a standard package that Magisk can automagically install and manage for you.

## Should you join this mission?

I would recommend to *Lineagefy* an old smartphone to anyone who is tired of changing mobile device every few years, or who is concerned about his privacy. To me, the benefits are immeasurable compared to buying the latest and greatest smartphone only to have to pay a lot to fix it or to be in the hands of the manufacturer's software which I cannot control.

It is also very obvious that what I am recommending is an extra effort, because of how difficult most manufacturers make to support their device for longer than they decided to; still, as users we can stand on the shoulders of the passionate communities behind these projects I described above, and you can actually get in touch with those people, asking for help or advice directly to the developers.

### Bulletproof backups, my main motivation

Since Lineage OS 17, the [SeedVault](https://github.com/seedvault-app/seedvault) system backup provider is pre-installed and available to save settings, accounts and application data to a backup file, an SD card, or an online file hosting **of your choice**. This should be the main reason to stick with Lineage OS: as long as you replace a backed-up device with another one supported by Lineage OS, you will be able to transfer all your data to the new device (even WhatsApp chat history); this is not trivial and not widely supported among the multitude of Android distribution variants, and also it usually works with a cloud service with limited space.
