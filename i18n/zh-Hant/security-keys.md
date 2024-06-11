---
title: 安全密鑰
icon: material/key-chain
description: 這些工具可協助透過多重身份驗證保護網路帳戶，而無需將您的祕密傳送給第三方。
cover: multi-factor-authentication.webp
---

實體**安全密鑰**可為線上帳戶添加強大的保護層。 與[驗證器應用程式](multi-factor-authentication.md) 相比，FIDO2 安全密鑰協定不受網路釣魚的影響，在沒持有金鑰的情況下不會受到損害。 許多服務支援 FIDO2/WebAuthn 作為保護帳戶安全的多因素驗證選項，且某些服務可用安全金鑰作為無密碼身份驗證的強大單因素驗證器。

## YubiKey 安全金鑰

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series by Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

**Yubico Security Key**系列是最佳成本效益的硬體安全金鑰，擁有 FIDO 2 級認證。 它支援 FIDO2/WebAuthn 和 FIDO U2F，並且可以與大多數支援安全密鑰作為第二因素的服務以及許多密碼管理器一起使用。

[:octicons-home-16: Homepage](https://www.yubico.com/products/security-key/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

有 USB-C 和 USB-A 兩種版本，兩者都支援 NFC，可與行動裝置一起使用。

此金鑰僅提供基本的 FIDO2 功能，但對於大多數人來說就足夠其需求。 安全金鑰系列**不具備**的功能為：

- [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/)
- CCID 智慧卡支援 (PIV-compatibile)
- OpenPGP

如需要這些功能，則應該考慮高階版 [YubiKey](#yubikey) 產品。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubico 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

Yubico 的 **YubiKey** 系列是最受歡迎的安全金鑰之一。 YubiKey 5 糸列的廣泛功能，例如： [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor)、[FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)、[Yubico OTP](basics/multi-factor-authentication.md#yubico-otp)、[Personal Identity Verification (PIV)](https://developers.yubico.com/PIV)、 [OpenPGP](https://developers.yubico.com/PGP)、[TOTP and HOTP](https://developers.yubico.com/OATH)驗證。

[:octicons-home-16: Homepage](https://www.yubico.com/products/yubikey-5-overview/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

[比較表](https://yubico.com/store/compare) 顯示 YubiKey 的功能以及與 Yubico [安全密鑰](#yubico-security-key) 系列之間相互比較。 YubiKey 好處之一是，一支可以滿足對安全密鑰硬體的全部期待。 建議購買前先 [作個小測驗](https://yubico.com/quiz/) ，確保做出正確的選擇。

Yubikey 5系列具有FIDO 1級認證，這是最常見的。 However, some governments or other organizations may require a key with Level 2 certification, in which case you'll have to purchase a [Yubikey 5 **FIPS** series](https://www.yubico.com/products/yubikey-fips/) key, or a [Yubico Security Key](#yubico-security-key). Most people do not have to worry about this distinction.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

For models which support HOTP and TOTP, there are 2 slots in the OTP interface which could be used for HOTP and 32 slots to store TOTP secrets. These secrets are stored encrypted on the key and never expose them to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

The firmware of YubiKey is not updatable. 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** has a security key capable of [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) called the **Nitrokey FIDO2**. For PGP support, you need to purchase one of their other keys such as the **Nitrokey Start**, **Nitrokey Pro 2** or the **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. The **Nitrokey 3** listed will have a combined feature set.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

For the models which support HOTP and TOTP, there are 3 slots for HOTP and 15 for TOTP. Some Nitrokeys can act as a password manager. They can store 16 different credentials and encrypt them using the same password as the OpenPGP interface.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

While Nitrokeys do not release the HOTP/TOTP secrets to the device they are plugged into, the HOTP and TOTP storage is **not** encrypted and is vulnerable to physical attacks. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Resetting the OpenPGP interface on a Nitrokey will also make the password database [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

## 標準

請注意，我們所推薦專案沒有任何瓜葛。 除[標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- Must use high quality, tamper resistant hardware security modules.
- Must support the latest FIDO2 specification.
- Must not allow private key extraction.
- Devices which cost over $35 must support handling OpenPGP and S/MIME.

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Should be available in USB-C form-factor.
- Should be available with NFC.
- Should support TOTP secret storage.
- Should support secure firmware updates.
