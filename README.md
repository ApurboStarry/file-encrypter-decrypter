# File Encrypter-Decrypter

## What it does

This is a web app that encrypts and decrypts files. Files are encrypted using the password provided by the user and can be decrypted only with the same password.

## How it works

The cryptography operations used in this app are implemented using [WebCrypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API). Files are encrypted using **AES-CBC 256-bit symmetric encryption**. The encryption key is derived from the password and a random salt using **PBKDF2** derivation with _10000_ iterations of **SHA256 hashing**.
