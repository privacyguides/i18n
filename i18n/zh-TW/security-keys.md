---
title: 安全金鑰
icon: material/key-chain
description: These security keys provide a form of phishing-immune authentication for accounts that support it.
cover: multi-factor-authentication.webp
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }

實體**安全金鑰**可為線上帳戶添加強大的保護層。 Compared to [authenticator apps](multi-factor-authentication.md), the [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) security key protocol is immune to phishing, and cannot be compromised without physical possession of the key itself. Many services support FIDO2/WebAuthn as a multifactor authentication option for securing your account, and some services allow you to use a security key as a strong single-factor authenticator with passwordless authentication.

## YubiKey 安全金鑰

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series by Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

The **Yubico Security Key** series is the most cost-effective hardware security key with FIDO Level 2 certification[^1]. It supports FIDO2/WebAuthn and FIDO Universal 2nd Factor (U2F), and works out of the box with most services that support a security key as a second factor, as well as many password managers.

[:octicons-home-16: Homepage](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

有 USB-C 和 USB-A 兩種版本，兩者都支援 NFC，可與行動裝置一起使用。

此金鑰僅提供基本的 FIDO2 功能，但對於大多數人來說就足夠其需求。 安全金鑰系列**不具備**的功能為：

- [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)
- CCID Smart Card support (PIV-compatible)
- OpenPGP

If you need any of those features, you should consider their higher-end [YubiKey](#yubikey) series instead.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubico 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

The **YubiKey** series from Yubico are among the most popular security keys with FIDO Level 2 Certification[^1]. The **YubiKey 5 Series** has a wide range of features such as FIDO2/WebAuthn and FIDO U2F, [TOTP and HOTP](https://developers.yubico.com/OATH) authentication, [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), and [OpenPGP](https://developers.yubico.com/PGP).

[:octicons-home-16: Homepage](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows how the YubiKeys compare to each other and to Yubico's [Security Key](#yubico-security-key) series in terms of features and other specifications. YubiKey 好處之一是，一支可以滿足對安全金鑰硬體的全部期待。 We encourage you to take their [quiz](https://yubico.com/quiz) before purchasing in order to make sure you choose the right security key.

YubiKey 可以使用 [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) 或 [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools) 來設定它。 若要管理 TOTP 程式碼，可用 [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)。 Yubico 所有客戶端軟體都是開源的。

For models which [support HOTP and TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with), the secrets are stored encrypted on the key and never exposed to the devices they are plugged into. 一旦向 Yubico Authenticator 提供種子（共享祕密） ，它將只會給出六位數的代碼，但永遠不會提供種子。 此安全模型有助於限制攻擊者，即便運行 Yubico Authenticator的設備受到破壞，讓受到物理攻擊時 Yubikey 仍具抵抗力。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubikey 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** has a cost-effective security key capable of FIDO2/WebAuthn and FIDO U2F called the **Nitrokey Passkey**. For support for features such as PIV, OpenPGP, and TOTP and HOTP authentication, you need to purchase one of their other keys like the **Nitrokey 3**. Currently, only the **Nitrokey 3A Mini** has [FIDO Level 1 Certification](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification).

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family) shows how the different Nitrokey models compare to each other in terms of features and other specifications. Refer to Nitrokey's [documentation](https://docs.nitrokey.com/nitrokeys/features) for more details about the features available on your Nitrokey.

Nitrokey 模式可用 [Nitrokey 應用程式](https://nitrokey.com/download) 來設定。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Excluding the Nitrokey 3, Nitrokeys which support HOTP and TOTP do not have encrypted storage, making them vulnerable to physical attacks.

</div>

## 標準

\*\*請注意，我們與推薦的任何專案均無隸屬關係。\*\*除了[我們的通用標準](about/criteria.md)以外，我們還制定了一套明確的要求，讓我們能夠提供客觀的推薦。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- Must use high-quality, tamper-resistant hardware security modules.
- 必須支援最新的 FIDO2 規格。
- 不允許私鑰提取。
- 價格超過 35美元的裝置必須支援處理 OpenPGP 和 S/MIME。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Should be available in USB-C form factor.
- 應與 NFC一起使用。
- 支持 TOTP 機密儲存。
- 應支援安全軔體更新。

[^1]: Some governments or other organizations may require a key with Level 2 certification, but most people do not have to worry about this distinction.
