---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## Аппаратные ключи безопасности

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

Ключи **YubiKeys** являются одними из самых популярных ключей безопасности. Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

Одним из преимуществ YubiKey является то, что всего лишь один ключ может делать практически всё (YubiKey 5), что можно ожидать от аппаратного ключа безопасности. We do encourage you to take the [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: Homepage](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare. Мы настоятельно рекомендуем вам выбрать ключи из серии YubiKey 5.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

Для моделей, поддерживающих HOTP и TOTP, в интерфейсе OTP есть 2 слота, которые можно использовать для HOTP, и 32 слота для хранения секретов TOTP. Эти секреты хранятся в зашифрованном виде на ключе и никогда не раскрывают их для устройств, к которым они подключены. После того как Yubico Authenticator получит семя (общий секрет), он будет выдавать только шестизначные коды. Секрет никогда выдаваться не будет. Эта модель безопасности помогает ограничить возможности злоумышленника, если он скомпрометирует одно из устройств, на которых работает Yubico Authenticator, и делает YubiKey устойчивым к физическому воздействию злоумышленника.

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

The firmware of YubiKey is not open source and is not updatable. Если вам нужны функции, которые доступны только в более новых версиях прошивки или если в используемой вами версии прошивки есть уязвимость, вам нужно будет приобрести новый ключ.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

У **Nitrokey** есть ключ безопасности, поддерживающий [FIDO2 и WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) и называемый **Nitrokey FIDO2**. Для использования PGP необходимо приобрести один из других ключей, таких как **Nitrokey Start**, **Nitrokey Pro 2** или **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. Перечисленные ключи **Nitrokey 3** будут обладать комбинированным набором функций.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

Для моделей, поддерживающих HOTP и TOTP, есть 3 слота для HOTP и 15 для TOTP. Некоторые Nitrokeys могут работать в качестве менеджера паролей. Они могут хранить 16 различных учетных данных и шифровать их с помощью того же пароля, что и интерфейс OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Хотя Nitrokeys не передают секреты HOTP/TOTP на устройство, к которому они подключены, хранилище HOTP и TOTP **не** зашифровано и уязвимо для физических атак. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Сброс интерфейса OpenPGP на Nitrokey также сделает базу данных паролей [недоступной](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net) firmware.

Nitrokey's firmware is open source, unlike the YubiKey. Прошивка современных моделей NitroKey (кроме **NitroKey Pro 2**) является обновляемой.

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

#### Минимальные требования

- Должны использоваться высококачественные, устойчивые к взлому аппаратные модули безопасности.
- Должна поддерживаться последняя спецификация FIDO2.
- Не должны допускать извлечение приватного ключа.
- Устройства, стоимостью более 35 $, должны поддерживать работу с OpenPGP и S/MIME.

#### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Должен быть доступен в форм-факторе USB-C.
- Должен быть доступен с NFC.
- Должен поддерживать хранение секретов TOTP.
- Должен поддерживать безопасное обновление прошивки.

## Приложение-аутентификатор

Приложения аутентификаторы реализуют стандарт безопасности, принятый рабочей группой инженеров интернета (IETF), который называется **Time-based One-time Passwords** или **TOTP**. При этом методе веб-сайты делятся с вами секретом, который вносится в приложение аутентификации. Затем приложение генерирует шестизначные коды, основанные на текущем времени, которые вы вводите при входе на сайт для проверки. Обычно эти коды обновляются каждые 30 секунд, и как только генерируется новый код, старый становится бесполезным. Даже если хакер получит один шестизначный код, у него не будет возможности анализировать этот код, чтобы получить исходный секрет, или каким-либо другим способом предсказать, какими могут быть будущие коды.

Мы настоятельно рекомендуем вам использовать мобильные приложения TOTP вместо настольных альтернатив, поскольку Android и iOS имеют лучшую безопасность и изоляцию приложений, чем большинство настольных операционных систем.

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
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-windows11: Windows](https://ente.io/download)
- [:simple-apple: macOS](https://ente.io/download)
- [:simple-linux: Linux](https://ente.io/download)
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
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

### Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Исходный код должен быть общедоступным.
- Не должно требовать интернет соединения.
- Не должен синхронизировать данные со сторонним облачным сервисом синхронизации/резервного копирования.
    - **Опционально** допустима поддержка E2EE синхронизации с помощью нативных служб ОС. Например, зашифрованная синхронизация через iCloud.
