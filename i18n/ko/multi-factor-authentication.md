---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## 하드웨어 보안 키

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

The **YubiKeys** are among the most popular security keys. YubiKey는 모델에 따라 [U2F(Universal 2nd Factor)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 및 WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [PIV(Personal Identity Verification)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP 및 HOTP](https://developers.yubico.com/OATH) 인증 등의 기능을 제공합니다.

One of the benefits of the YubiKey is that one key can do almost everything (YubiKey 5), you could expect from a hardware security key. We do encourage you to take the [quiz](https://www.yubico.com/quiz/) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: 홈페이지](https://www.yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.yubico.com/support/terms-conditions/privacy-notice){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://docs.yubico.com/){ .card-link title=문서}

</details>

</div>

여러 YubiKey 모델 간 기능 비교는 [YubiKey 비교 표](https://www.yubico.com/store/compare/)에서 확인하실 수 있습니다. Privacy Guides에서는 YubiKey 5 시리즈를 사용하실 것을 권장드립니다.

YubiKeys can be programmed using the [YubiKey Manager](https://www.yubico.com/support/download/yubikey-manager/) or [YubiKey Personalization Tools](https://www.yubico.com/support/download/yubikey-personalization-tools/). For managing TOTP codes, you can use the [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/). All of Yubico's clients are open source.

For models which support HOTP and TOTP, there are 2 slots in the OTP interface which could be used for HOTP and 32 slots to store TOTP secrets. These secrets are stored encrypted on the key and never expose them to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

The firmware of YubiKey is not open source and is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

**Nitrokey** has a security key capable of [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) called the **Nitrokey FIDO2**. For PGP support, you need to purchase one of their other keys such as the **Nitrokey Start**, **Nitrokey Pro 2** or the **Nitrokey Storage 2**.

[:octicons-home-16: 홈페이지](https://www.nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.nitrokey.com/data-privacy-policy){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://docs.nitrokey.com/){ .card-link title=문서}

</details>

</div>

The [comparison table](https://www.nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. The **Nitrokey 3** listed will have a combined feature set.

Nitrokey models can be configured using the [Nitrokey app](https://www.nitrokey.com/download).

For the models which support HOTP and TOTP, there are 3 slots for HOTP and 15 for TOTP. Some Nitrokeys can act as a password manager. They can store 16 different credentials and encrypt them using the same password as the OpenPGP interface.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

While Nitrokeys do not release the HOTP/TOTP secrets to the device they are plugged into, the HOTP and TOTP storage is **not** encrypted and is vulnerable to physical attacks. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Resetting the OpenPGP interface on a Nitrokey will also make the password database [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/) firmware.

Nitrokey's firmware is open source, unlike the YubiKey. The firmware on modern NitroKey models (except the **NitroKey Pro 2**) is updatable.

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

#### 최소 요구 사항

- 고품질의 변조 방지 하드웨어 보안 모듈을 사용해야 합니다.
- 최신 FIDO2 사양을 지원해야 합니다.
- 개인 키 추출을 허용해서는 안 됩니다.
- 가격이 $35 이상인 기기는 OpenPGP, S/MIME를 지원해야 합니다.

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- USB-C 단자로 된 버전을 제공해야 합니다.
- NFC를 지원해야 합니다.
- TOTP 비밀 저장소(Secret Storage)를 지원해야 합니다.
- 보안 펌웨어 업데이트를 지원해야 합니다.

## 인증 앱

Authenticator Apps implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. This is a method where websites share a secret with you which is used by your authenticator app to generate a six (usually) digit code based on the current time, which you enter while logging in for the website to check. Typically these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Even if a hacker gets one six-digit code, there is no way for them to reverse that code to get the original secret or otherwise be able to predict what any future codes might be.

We highly recommend that you use mobile TOTP apps instead of desktop alternatives as Android and iOS have better security and app isolation than most desktop operating systems.

### ente Auth

<div class="admonition recommendation" markdown>

![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**ente Auth** is a free and open-source app which stores and generates TOTP tokens on your mobile device. It can be used with an online account to backup and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/ente-authenticator/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** is a free and open-source app for Android to manage your 2-step verification tokens for your online services. Aegis Authenticator operates completely offline/locally, but includes the option to export your tokens for backup unlike many alternatives.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

- 소스 코드는 공개적으로 이용 가능해야 합니다.
- 인터넷 연결 없이도 작동해야 합니다.
- 제3자 클라우드 동기화/백업 서비스와 동기화하는 식으로 작동해서는 안 됩니다.
    - **선택적인** (운영 체제 네이티브 툴을 이용한) E2EE 동기화 지원은 허용됩니다. 예시: 'iCloud를 통한 암호화 동기화'
