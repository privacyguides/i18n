---
title: 安全密鑰
icon: material/key-chain
description: Secure your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

<small>防護下列威脅：</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy){ .pg-orange }

實體**安全密鑰**可為線上帳戶添加強大的保護層。 與[驗證器應用程式](multi-factor-authentication.md) 相比，FIDO2 安全密鑰協定不受網路釣魚的影響，在沒持有金鑰的情況下不會受到損害。 許多服務支援 FIDO2/WebAuthn 作為保護帳戶安全的多因素驗證選項，且某些服務可用安全金鑰作為無密碼身份驗證的強大單因素驗證器。

## YubiKey 安全金鑰

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series by Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

**Yubico Security Key**系列是最佳成本效益的硬體安全金鑰，擁有 FIDO 2 級認證。 它支援 FIDO2/WebAuthn 和 FIDO U2F，並且可以與大多數支援安全密鑰作為第二因素的服務以及許多密碼管理器一起使用。

[:octicons-home-16: Homepage](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

有 USB-C 和 USB-A 兩種版本，兩者都支援 NFC，可與行動裝置一起使用。

此金鑰僅提供基本的 FIDO2 功能，但對於大多數人來說就足夠其需求。 安全金鑰系列**不具備**的功能為：

- [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)
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

[:octicons-home-16: Homepage](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

[比較表](https://yubico.com/store/compare) 顯示 YubiKey 的功能以及與 Yubico [安全密鑰](#yubico-security-key) 系列之間相互比較。 YubiKey 好處之一是，一支可以滿足對安全密鑰硬體的全部期待。 建議購買前先 [作個小測驗](https://yubico.com/quiz/) ，確保做出正確的選擇。

Yubikey 5系列具有FIDO 1級認證，這是最常見的。 However, some governments or other organizations may require a key with Level 2 certification, in which case you'll have to purchase a [Yubikey 5 **FIPS** series](https://yubico.com/products/yubikey-fips) key, or a [Yubico Security Key](#yubico-security-key). 大多數人不必擔心這種差異。

YubiKey 可以使用 [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) 或 [YubiKey 個人化工具]](https://yubico.com/support/download/yubikey-personalization-tools)。 若要管理 TOTP 程式碼，可用 [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)。 Yubico 所有客戶端軟體都是開源。

支持 HOTP 和 TOTP 的機型， OTP 介面中有2個插槽可用於HOTP 和32個插槽來存儲 TOTP 機密。 這些機密經加密後存儲在密鑰上，永遠不會將它們暴露在插入的設備上。 一旦向 Yubico Authenticator 提供種子（共享祕密） ，它將只會給出六位數的代碼，但永遠不會提供種子。 此安全模型有助於限制攻擊者，即便運行 Yubico Authenticator的設備受到破壞，讓受到物理攻擊時 Yubikey 仍具抵抗力。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubikey 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** 有能夠支援 [FIDO2 和 WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) 的安全金鑰，稱為 **Nitrokey FIDO2**。 若要獲得 PGP 支援，您需要購買他們其他鑰匙，例如 **Nitrokey Start**、**Nitrokey Pro 2** 或 **Nitrokey Storage 2**。

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

[比較表](https://nitrokey.com/#comparison) 顯示 Nitrokey 模式的功能以及比較方式。 **Nitrokey 3** 具有組合的功能集。

Nitrokey 模式可用 [Nitrokey 應用程式](https://nitrokey.com/download) 來配置。

支持 HOTP 和 TOTP 的型號，有3個 HOTP 插槽，15 個 TOTP 插槽。 有些 Nitrokeys 可以充當密碼管理器。 可以存儲 16 組憑證，並使用與 OpenPGP 接口相同的密碼對憑證加密。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

雖然 Nitrokeys 不會將 HOTP/TOTP 機密釋放給所插入的設備，但HOTP 和 TOTP存儲\* _未經加密_ \* ，容易受到物理攻擊。 如果需要存儲 HOTP 或 TOTP 這類祕密，強烈建議使用Yubikey 代替。

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

重置 Nitrokey 的 OpenPGP 介面會使密碼資料庫變為 [無法存取](https://docs.nitrokey.com/pro/linux/factory-reset)。

</div>

## 標準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須使用高品質、防篡改的硬體安全模組。
- 必須支援最新的 FIDO2 規格。
- 不允許私鑰提取。
- 價格超過 35美元的裝置必須支援處理 OpenPGP 和 S/MIME。

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應採用 USB-C 格式。
- 應與 NFC一起使用。
- 支持 TOTP 機密儲存。
- 應支持安全軔體更新。
