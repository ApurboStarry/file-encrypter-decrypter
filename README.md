# File Encrypter-Decrypter

## What it does

This is a web app that encrypts and decrypts files. Files are encrypted using the password provided by the user and can be decrypted only with the same password.

## How it works

The cryptography operations used in this app are implemented using [WebCrypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API). Files are encrypted using **[AES-GCM](https://en.wikipedia.org/wiki/Block_cipher_mode_of_operation#Galois/counter_(GCM)) 256-bit symmetric encryption**. The encryption key is derived from the password and a random salt using **[PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)** derivation with _10000_ iterations of **[SHA256 hashing](https://en.wikipedia.org/wiki/SHA-2)**.

The app uses JavaScript running in the browser to encrypt and decrypt files. All of the process is done in the client side meaning that the file uploaded by the user and password provided by the user do not leave browser during this process.
