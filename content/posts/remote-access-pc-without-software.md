---
title: "Remotely access any PC without any software"
date: 2023-06-22
draft: false
tags: ["remote", "pc", "hardware"]
description: "The solution I chose to get remote access functionality, without spending much"
---

![Cover image](/pikvm_nanopi_and_accessories.jpg)
*All the hardware involved into this project: in the middle, the NanoPi NEO H3*

## I heard about *software X* that provides remote desktop functionality...

While there are a lot of software programs that can enable remote desktop access functionality, this also means that you **must install** that piece of software on the machine you are willing to access while physically away from it.

Also, this means that an operating system must be running on that machine, to also run that remote desktop software we're supposing to want.

My use case required me to not install anything on the remote machine, and also to access it before the operating system is loaded; therefore I settled my needs on the product category of *KVM over IP*.

These products let you connect the remote machine's display output (for video) and its USB inputs (for keyboard and mouse) to the device itself, which in turn runs a piece of software that will let you connect to the KVM device over an IP connection (for example, from the same Wi-Fi network the remote machine is connected to).

## The title is misleading!

Technically that's true: according to the last paragraph, I will connect a device to the remote machine and that device will run some sort of software, so I cannot just:
- connect to any PC: I would need physical access to the machine to hook it up to the KVM device;
- without any software: I would still interact with a remote desktop application running on the KVM device.

That being said, this kind of product will definitely help me solve my problem with remote access in the aforementioned constraints.

So, from there I started looking around to learn about prices and manufacturers...

## Those KVM-things are not that affordable

Since it's not a market segment aimed towards private customers but rather more towards enterprises, there are not many manufacturers interested in offering a "cheap alternative"; also, the cheaper the KVM over IP device, the lower the quality of the software it runs and the features it offers.

We established the state of the market for such products: now what? Well, as always the way to go for the budget path is the DIY route (do it yourself).

In fact, a community project tailored around the Raspberry Pi platform looks exactly what I will need: it's called [PiKVM](https://pikvm.org/) and its aim is to release an operating system based on Arch Linux with support for display capture, mouse and keyboard emulation, and safe system updates (among the many features implemented).

## PiKVM on a non-Raspberry Pi

Even if the project started with support for the Raspberry Pi V3 platform, since it's free software anyone with the right skills may as well build the operating system image for whatever alternative device he wants.

That's exactly what the GitHub user [Yura80](https://github.com/Yura80) did: inside [his repository](https://github.com/Yura80/os/releases) it is possible to find ready-to-use system images for a bunch of Rockchip and Allwinner based platforms, among which there's conveniently an image for the single board computer (also referred to as SBC) **NanoPi Neo H3** (it's called `v2-hdmiusb-generic-arm-libretech-all-h3-cc-h3.img.bz2`).

If written on a microSD card and put into that SBC, you can have your PiKVM device up and running in less than ten minutes.

## What's special about that NanoPi computer?

At the time of looking for a PiKVM compatible device cheaper than the Raspberry Pi (which prices had skyrocketed starting from the 2020 pandemic) the NanoPi Neo H3 was the cheapest alternative computer I could find on AliExpress (20€). To this cost it must be added (in my case) shipping to Italy (5€) and also the other components required to use all the KVM features:

- HDMI to USB capture card
- HDMI cable
- MicroUSB to USB type A cable
- MicroSD memory card
- Ethernet cable (RJ-45)

The NanoPi Neo has a full USB type A which I will use to plug the HDMI capture card (for streaming the remote machine display output); moreover, since the SBC has no wireless connectivity, it must be plugged into a network device through its Ethernet port. Finally, the NanoPi Neo exposes an OTG[^1] interface on its MicroUSB port, which will also be used to power it up.

The final cost was roughly 40€ for all the components; on top of that, the NanoPi Neo comes ahead of a "traditional" Raspberry Pi based PiKVM for its compact size, its ability to be powered directly off the host device and (for my specific needs) the pre-installed Ethernet port, since I would prefer a wired network connection for reliability purposes if remotely connecting to the device.

## Software and updates

Beware that if using the pre-built system images I referenced in the previous section, they are very outdated at the time of writing, and manually updating the system after starting it seems very impractical due to broken package dependencies at various layers. There's still the possibility to build the image by ourselves, however I can recommend sticking with the available images if you do not use this PiKVM device to connect over the Internet but rather on the same local network, for example (like I am doing) to avoid hooking up a monitor and keyboard to a headlass device just to debug a faulty startup or to perform a firmware update.

**Remember**: the PiKVM is just a Linux software, thus you may install whatever additional application to your KVM over IP device.

[^1]: USB On The Go (OTG) protocol allows a device to act as a peripheral, therefore allowing in our case the NanoPi to present itself as a mouse and keyboard to the connected host device.
