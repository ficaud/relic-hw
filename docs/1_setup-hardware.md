# 1. Setup the hardware

The microcontroller is the brain of your Relic device. It runs [relic-core](https://github.com/ficaud/relic-core), the firmware that powers it.

The following boards are currently supported:

- [ESP32-S3-DevKitC-1](https://docs.zephyrproject.org/latest/boards/espressif/esp32s3_devkitc/doc/index.html)
- [ESP32-DevKit-V1](https://docs.zephyrproject.org/latest/boards/others/doit_esp32_devkit_v1/doc/index.html)
- [Docker Container Platform](https://github.com/ficaud/relic-core/blob/main/doc/docker.md): compatible with x86_64 and ARM environments (Linux, macOS, Windows, and Raspberry Pi arm64 / arm/v7).
- Support for more boards is on the way — check back soon...

> Note: These boards have been tested and are known to work with relic-core. There are probably more that work, but since they haven't been tested, they won't appear on the list.

> Note 2: For now, Relic requires boards that support Wi-Fi Access Point (AP) mode. Future versions may support other connection methods.

## How to get a microcontroller

These boards are widely available, so you shouldn't have any trouble finding one. You can order them from a specialized electronics retailer, buy them on the usual online marketplaces, or even pick one up at a physical store — whichever suits you best.

Here are a few sources worth checking out:

- [Amazon](https://www.amazon.com/)
- [Conrad](https://www.conrad.com/)
- [Mouser](https://www.mouser.com/)
- [Aliexpress](https://www.aliexpress.com/)
- [Digikey](https://www.digikey.com/)
- and many others...

## How to program the microcontroller

The way you get Relic up and running depends on the platform you're targeting.

### For ESP32 boards

Head over to [relic flash](https://ficaud.github.io/relic-core/flash.html), select your board, and download the matching firmware. To make sure you get the latest version of relic-core, click on **Latest GitHub Release**.

![firmware_flashing](img/firmware_flashing.png)

Once the firmware is downloaded, you'll see a QR code that you can scan with your phone to join the network.

<div align="center" style="display: flex; justify-content: center; gap: 10px;">
<img src="../img/relic-flashing-qrcode.png" width="400" alt="success in flash relic">
</div>

You have also the possibility to use the classic way by searching for the SSID and entering the password (that is also displayed in the portal).

> Note: The password is generated during the firmware upload and unique to your device.

### For Docker containers

If you're running Relic in a Docker container — for instance on a Raspberry Pi — check out [docker.md](https://github.com/ficaud/relic-core/blob/main/doc/docker.md) to learn how to set it up properly.

More information about the flash process can be found [here](https://github.com/ficaud/relic-core/tree/dev/jfi#how-to-connect-to-captive-portal).

## ESP32 programming Live demo

Here you can find a live demo showing you in video the exact steps that you need to follow to flash relic-core in your device.

TBD: add video of esp32 board's manipulation to get the software up and running

## Craft a nice enclosure

Once your Relic is up and running, I'd recommend crafting a nice enclosure for your microcontroller Not only does it protect the hardware, but it also keeps it from being mistaken for a leftover piece of electronics and thrown in the bin.

TBD: find a hackable way to do enclosure / or 3d print it.

## More links

- [Wikipedia ESP32](https://fr.wikipedia.org/wiki/ESP32)
- [Espressif (company that produces ESP32)](https://www.espressif.com/en/products/socs/esp32)
