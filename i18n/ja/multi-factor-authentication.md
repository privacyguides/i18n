---
title: "多要素認証"
icon: 'material/two-factor-authentication'
description: これらのツールは、あなたの秘密をサードパーティに送信することなく、多要素認証であなたのインターネットアカウントを保護することを支援します。
cover: multi-factor-authentication.webp
---

## ハードウェアセキュリティ

### YubiKey

!!! recommendation

    ![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)
    
    **YubiKeys**は最も人気のあるセキュリティ・キーのひとつです。 いくつかのYubiKeyモデルには以下のような幅広い機能があります: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.
    
    YubiKeyの利点の1つは、1つのキーでハードウェア・セキュリティ・キーに期待されるほとんどのこと(YubiKey 5)ができることです。 正しい選択をするために、購入前に [quiz](https://www.yubico.com/quiz/)をご覧になることをお勧めします。
    
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

!!! 警告

    While Nitrokeys do not release the HOTP/TOTP secrets to the device they are plugged into, the HOTP and TOTP storage is **not** encrypted and is vulnerable to physical attacks. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

!!! 警告

    Resetting the OpenPGP interface on a Nitrokey will also make the password database [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/) firmware.

Nitrokey's firmware is open-source, unlike the YubiKey. The firmware on modern NitroKey models (except the **NitroKey Pro 2**) is updatable.

### Criteria

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる基準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

#### 最低要件

- Must use high quality, tamper resistant hardware security modules.
- Must support the latest FIDO2 specification.
- Must not allow private key extraction.
- Devices which cost over $35 must support handling OpenPGP and S/MIME.

#### 満たされることが望ましい基準

私たちが考える最善の基準は、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいるものがあれば、このページで他のものよりも上位にランクされるかもしれません。

- Should be available in USB-C form-factor.
- Should be available with NFC.
- Should support TOTP secret storage.
- Should support secure firmware updates.

## Authenticator Apps

Authenticator Apps implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. This is a method where websites share a secret with you which is used by your authenticator app to generate a six (usually) digit code based on the current time, which you enter while logging in for the website to check. Typically these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Even if a hacker gets one six-digit code, there is no way for them to reverse that code to get the original secret or otherwise be able to predict what any future codes might be.

We highly recommend that you use mobile TOTP apps instead of desktop alternatives as Android and iOS have better security and app isolation than most desktop operating systems.

### ente Auth

!!! recommendation

    ![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }
    
    **ente Auth** is a free and open-source app which stores and generates TOTP tokens on your mobile device. It can be used with an online account to backup and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.
    
    [:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
    [:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/ente-authenticator/id6444121398)
        - [:simple-github: GitHub](https://github.com/ente-io/auth/releases)
        - [:octicons-globe-16: Web](https://auth.ente.io)

### Aegis Authenticator (Android)

!!! recommendation

    ![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }
    
    **Aegis Authenticator** is a free and open-source app for Android to manage your 2-step verification tokens for your online services. Aegis Authenticator operates completely offline/locally, but includes the option to export your tokens for backup unlike many alternatives.
    
    [:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
        - [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

### Criteria

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる基準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

- Source code must be publicly available.
- Must not require internet connectivity.
- Must not sync to a third-party cloud sync/backup service.
    - **Optional** E2EE sync support with OS-native tools is acceptable, e.g. encrypted sync via iCloud.
