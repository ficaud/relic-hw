# 5. Recover your secret

> Prerequisite: You should already know how to flash the Relic firmware onto a board, or at least how to connect to its user interface.

> Reminder: recovering your secret requires the threshold number of shares. Of the 5 shares initially generated, you must bring together at least 3 of them to retrieve the secret originally ciphered in the Relic.

For more information on how to access the Relic, refer to:

- [1. Setup the hardware](1_setup-hardware.md)
- [2. Create shares](2_create-shares.md)

## Unsplit the shares

Once you're on the unsplit page, you have two options:

- Enter the shares manually (in full text).
- Use the QR code scanner — this only works if your shares are in that format.

![unsplit your secret](img/unsplit_secret.PNG){ width="300" }

If you choose the QR code scanner, make sure you're standing directly in front of the code and that most of it appears in the middle of the camera. This is especially important for ESP32-S3 devices, which embed the QR code solver on board (the phone simply uploads the picture to the ESP32).

![example camera qr decode](img/example_qr_decode.PNG){ width="300" }

![success unsplit secret](img/success_unsplit_secret.PNG){ width="300" }

## Bonus : Crypto seed phrase

> Note: As you can see, the screenshots above are showing what it looks like to have a qrcode for seed phrase before the BIP-39 compression was implemented.

If you want to unsplit a seed phrase to recover your crypto assets, please make double check if there is the BIP-39 compression that has been set to reduce the qrcode size (which is recommended).

Read more about it [here](bonus_crypto_seedphrase.md).

## Troubleshooting

If you have trouble resolving the QR code, you can try the online WASM version available on the [github page of the project](https://ficaud.github.io/relic-core/).
