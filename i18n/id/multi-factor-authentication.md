---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## Hardware Security Keys

### YubiKey

!!! recommendation

    ![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)
    
    The **YubiKeys** are among the most popular security keys. Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.
    
    One of the benefits of the YubiKey is that one key can do almost everything (YubiKey 5), you could expect from a hardware security key. We do encourage you to take the [quiz](https://www.yubico.com/quiz/) before purchasing in order to make sure you make the right choice.
    
    [:octicons-home-16: Homepage](https://www.yubico.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.yubico.com/){ .card-link title=Documentation}

The [comparison table](https://www.yubico.com/store/compare/) shows the features and how the YubiKeys compare. We highly recommend that you select keys from the YubiKey 5 Series.

YubiKeys can be programmed using the [YubiKey Manager](https://www.yubico.com/support/download/yubikey-manager/) or [YubiKey Personalization Tools](https://www.yubico.com/support/download/yubikey-personalization-tools/). For managing TOTP codes, you can use the [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/). All of Yubico's clients are open-source.

For models which support HOTP and TOTP, there are 2 slots in the OTP interface which could be used for HOTP and 32 slots to store TOTP secrets. These secrets are stored encrypted on the key and never expose them to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

!!! warning
    The firmware of YubiKey is not open-source and is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

### Nitrokey

!!! recommendation

    ![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }
    
    **Nitrokey** has a security key capable of [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) called the **Nitrokey FIDO2**. For PGP support, you need to purchase one of their other keys such as the **Nitrokey Start**, **Nitrokey Pro 2** or the **Nitrokey Storage 2**.
    
    [:octicons-home-16: Homepage](https://www.nitrokey.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.nitrokey.com/){ .card-link title=Documentation}

The [comparison table](https://www.nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. The **Nitrokey 3** listed will have a combined feature set.

Nitrokey models can be configured using the [Nitrokey app](https://www.nitrokey.com/download).

For the models which support HOTP and TOTP, there are 3 slots for HOTP and 15 for TOTP. Some Nitrokeys can act as a password manager. They can store 16 different credentials and encrypt them using the same password as the OpenPGP interface.

!!! peringatan

    While Nitrokeys do not release the HOTP/TOTP secrets to the device they are plugged into, the HOTP and TOTP storage is **not** encrypted and is vulnerable to physical attacks. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

!!! peringatan

    Resetting the OpenPGP interface on a Nitrokey will also make the password database [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/) firmware.

Nitrokey's firmware is open-source, unlike the YubiKey. The firmware on modern NitroKey models (except the **NitroKey Pro 2**) is updatable.

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

#### Persyaratan Minimum

- Must use high quality, tamper resistant hardware security modules.
- Must support the latest FIDO2 specification.
- Must not allow private key extraction.
- Devices which cost over $35 must support handling OpenPGP and S/MIME.

#### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Should be available in USB-C form-factor.
- Should be available with NFC.
- Should support TOTP secret storage.
- Should support secure firmware updates.

## Authenticator Apps

Authenticator Apps implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. This is a method where websites share a secret with you which is used by your authenticator app to generate a six (usually) digit code based on the current time, which you enter while logging in for the website to check. Typically these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Even if a hacker gets one six-digit code, there is no way for them to reverse that code to get the original secret or otherwise be able to predict what any future codes might be.

We highly recommend that you use mobile TOTP apps instead of desktop alternatives as Android and iOS have better security and app isolation than most desktop operating systems.

### Aegis Authenticator (Android)

!!! recommendation

    ![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }
    
    **Aegis Authenticator** is a free, secure and open-source app to manage your 2-step verification tokens for your online services.
    
    [:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
        - [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

### Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

- Source code must be publicly available.
- Must not require internet connectivity.
- Must not sync to a third-party cloud sync/backup service.
    - **Optional** E2EE sync support with OS-native tools is acceptable, e.g. encrypted sync via iCloud.
