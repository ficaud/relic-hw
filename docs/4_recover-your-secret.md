# 5. Recover your secret

> Prerequisite: You should already know how to flash the Relic firmware onto a board, or at least how to connect to its user interface.

> Reminder: recovering your secret requires the threshold number of shares. Of the 5 shares initially generated, you must bring together at least 3 of them to retrieve the secret originally ciphered in the Relic.

## Unsplit the shares

Once you're on the unsplit page, you have two options:

- Enter the shares manually (in full text).
- Use the QR code scanner — this only works if your shares are in that format.

![unsplit your secret](img/unsplit_secret.PNG){ width="300" }

If you choose the QR code scanner, make sure you're standing directly in front of the code and that most of it appears in the middle of the camera. This is especially important for ESP32-S3 devices, which embed the QR code solver on board (the phone simply uploads the picture to the ESP32).

![example camera qr decode](img/example_qr_decode.PNG){ width="300" }

![success unsplit secret](img/success_unsplit_secret.PNG){ width="300" }

**Important note**: Don't forget to check whether you need to apply the BIP-39 or the SLIP-39 compression to your shares before reconstructing your secret (see [crypto seedphrase doc](bonus_crypto_seedphrase.md) for more information).

---
