---
title: 安全金鑰
icon: material/key-chain
description: 這些安全金鑰為支援此功能的帳號提供防釣魚的身份驗證方式。
cover: multi-factor-authentication.webp
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }

實體**安全金鑰**可為線上帳戶添加強大的保護層。 與[驗證器應用程式](multi-factor-authentication.md)相比，[FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) 安全金鑰協定不受網路釣魚的影響，除非實際持有金鑰實體，否則無法遭破解。 許多服務支援 FIDO2/WebAuthn 作為保護帳號安全的多重要素驗證選項，某些服務更可以使用安全金鑰作為無密碼身份驗證的強大單要素身份驗證選項。

## YubiKey 安全金鑰

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series by Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

**Yubico Security Key** 系列是具備 FIDO 2 級認證[^1]的最具成本效益硬體安全金鑰。 它支援 FIDO2/WebAuthn 及 FIDO 通用第二要素 (U2F)，並可立即與多數支援安全金鑰作為第二驗證要素的服務，以及眾多密碼管理工具配合使用。

[:octicons-home-16: 首頁](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="文件" }

</details>

</div>

有 USB-C 和 USB-A 兩種版本，兩者都支援 NFC，可與行動裝置一起使用。

此金鑰僅提供基本的 FIDO2 功能，但對於大多數人來說就足夠其需求。 安全金鑰系列**不具備**的功能為：

- [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)
- CCID 智慧卡支援（相容 PIV）
- OpenPGP

若您需要這些功能，則應考慮高階版 [YubiKey](#yubikey) 系列。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubico 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

Yubico 的 **YubiKey** 系列是獲得 FIDO 2 級認證[^1]的最受歡迎安全金鑰之一。 **YubiKey 5 系列**具備多種功能，例如 FIDO2/WebAuthn 與 FIDO U2F，[TOTP 與 HOTP](https://developers.yubico.com/OATH)、[個人身份驗證 (PIV)](https://developers.yubico.com/PIV) 與 [OpenPGP](https://developers.yubico.com/PGP)。

[:octicons-home-16: 首頁](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="文件" }

</details>

</div>

[對照表](https://yubico.com/store/compare)展示了 YubiKey 系列產品之間，以及 Yubico 的[安全金鑰](#yubico-security-key)系列在功能與其他規格上的比較。 YubiKey 好處之一是，一支可以滿足對安全金鑰硬體的全部期待。 我們建議您在購買前先完成他們的[測驗](https://yubico.com/quiz)，以確保您選擇了合適的安全金鑰。

YubiKey 可以使用 [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) 或 [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools) 來設定它。 若要管理 TOTP 程式碼，可用 [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)。 Yubico 所有客戶端軟體都是開源的。

對於[支援 HOTP 與 TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with) 的型號，祕密會加密儲存在金鑰上，絕不會暴露給被插入的裝置。 一旦向 Yubico Authenticator 提供種子（共享祕密） ，它將只會給出六位數的代碼，但永遠不會提供種子。 此安全模型有助於限制攻擊者，即便運行 Yubico Authenticator的設備受到破壞，讓受到物理攻擊時 Yubikey 仍具抵抗力。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Yubikey 安全金鑰的韌體不可更新。 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** 推出一款經濟實惠的安全金鑰，支援 FIDO2/WebAuthn 與 FIDO U2F 標準，名為 **Nitrokey Passkey**。 若要支援 PIV、OpenPGP、TOTP 與 HOTP 認證等功能，您必須購買他們的其他金鑰，例如 **Nitrokey 3**。 目前，只有 **Nitrokey 3A Mini** 有 [FIDO 第 1 級認證](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification)。

[:octicons-home-16: 首頁](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="文件" }

</details>

</div>

[對照表](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family)展示了不同的 NitroKey 型號在功能與其他規格層面的比較。 請參閱 Nitrokey 的[文件](https://docs.nitrokey.com/nitrokeys/features)以取得更多關於 Nitrokey 上可用功能的詳細資訊。

Nitrokey 模式可用 [Nitrokey 應用程式](https://nitrokey.com/download) 來設定。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

除了 Nitrokey 3 以外，支援 HOTP 與 TOTP 的 Nitrokey 並沒有加密儲存空間，因此很容易遭到實體攻擊。

</div>

## 標準

\*\*請注意，我們與推薦的任何專案均無隸屬關係。\*\*除了[我們的通用標準](about/criteria.md)以外，我們還制定了一套明確的要求，讓我們能夠提供客觀的推薦。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須使用高品質、防竄改的硬體安全模組。
- 必須支援最新的 FIDO2 規格。
- 不允許私鑰提取。
- 價格超過 35美元的裝置必須支援處理 OpenPGP 和 S/MIME。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應採用 USB-C 規格形式。
- 應與 NFC一起使用。
- 支持 TOTP 機密儲存。
- 應支援安全軔體更新。

[^1]: 某些政府或其他組織可能要求使用具備第 2 級認證的金鑰，但多數人無需顧慮此區別。
