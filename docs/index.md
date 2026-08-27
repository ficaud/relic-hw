# Relic Hardware
<div align="center">
<img src="img/relic-logo.png" width="150" alt="Relic Core logo">

<br/>
<br/>
<br/>

</div>

This doc is a step-by-step guide that teaches **complete beginners** how to build a Relic device entirely from scratch.

This is about the hardware and how you can build it yourself. For more information about the software that runs the device, go to [relic-core](https://github.com/ficaud/relic-core).

## What you will learn

- **The philosophy** behind Relic — why it exists and what problem it solves.
- **How to build** a Relic device — from the electronic components to the final assembly.
- **How to use it** — storing and recovering your secrets in practice.

## What is a Relic?

A **Relic** is a physical device that lets you safely store your most sensitive secrets.

Under the hood, it relies on the [Shamir's Secret Sharing](https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing) algorithm that works the following way:

1. Your secret is **split into multiple pieces** (called *shares*).
2. Each share is useless on its own — you cannot recover the secret from a single share.
3. To reconstruct the secret, you need to bring together at least a **threshold number** of shares.

This means you can distribute your shares across different locations or people, and even if some shares are lost or stolen, your secret remains safe as long as the threshold isn't reached.

## Why Relic?

Relic aims to implement Shamir's Secret Sharing in a way that is:

- **Timeless** — long-lasting hardware that comes with software handling most of its functions.
- **Private** — relic is not connected to the internet.
- **Secure** — designed to protect your data against theft and loss.
- **Open source** — anyone can build its own relic device for almost nothing.

The core idea is to make this powerful technology available to everyone, giving you full ownership and control over your most sensitive information. All that, without relying on any third party or cloud service that could have a leak or close overnight.

## What secrets should I store in a Relic?

You can store pretty much anything you want to keep secret. However, I'd recommend being selective about what you put inside. A Relic is best reserved for your most important secrets — the ones you truly couldn't afford to lose.

Good candidates include, the master password that unlocks your password manager, the recovery phrase or keys that protect your cryptocurrency, or even a private keepsake you don't want to lose.

## How to build a Relic

**WARNING:** Some of the screenshots in this documentation are outdated and may not reflect the current Relic UI.

Building your own Relic is a step-by-step journey. The steps below will walk you through each part of the process, from the hardware to how you handle your shares once they exist.

- [Learn more](1_setup-hardware.md) about the brain of the Relic device.
- [Learn more](2_create-shares.md) about the best ways to create your shares.
- [Learn more](3_distribute-shares.md) about the best ways to distribute your shares.
- [Learn more](4_recover-your-secret.md) about the ways to recover your secret.

## Complete demo of relic-core

Here is a video showing the full process for flashing the firmware onto a microcontroller, creating shares, and recovering your secret.

<video width="100%" controls>
  <source src="img/relic-demo.mp4" type="video/mp4">
</video>
