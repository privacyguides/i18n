---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## 安全金鑰硬體

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

**YubiKeys** 是最常用的安全金鑰之一。 Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

YubiKey 好處之一是，一支密鑰（ 例如 YubiKey 5 ）可以滿足對安全密鑰硬體的全部期待。 We do encourage you to take the [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: Homepage](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare. 我們強烈建議您從YubiKey 5系列中挑選。

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). Yubico 所有客戶端軟體都是開源。

支持 HOTP 和 TOTP 的機型， OTP 介面中有2個插槽可用於HOTP 和32個插槽來存儲 TOTP 機密。 這些機密經加密後存儲在密鑰上，永遠不會將它們暴露在插入的設備上。 一旦向 Yubico Authenticator 提供種子（共享祕密） ，它將只會給出六位數的代碼，但永遠不會提供種子。 此安全模型有助於限制攻擊者，即便運行 Yubico Authenticator的設備受到破壞，讓受到物理攻擊時 Yubikey 仍具抵抗力。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

The firmware of YubiKey is not open source and is not updatable. 如果您想要使用較新韌體版本的功能，或者使用中的韌體版本存在漏洞，則需要購買新的金鑰。

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

**Nitrokey** 能夠 [FIDO2 和 WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)的安全金鑰，稱為 **Nitrokey FIDO2**。 若要獲得 PGP 支援，您需要購買他們其他鑰匙，例如 **Nitrokey Start**、**Nitrokey Pro 2** 或 **Nitrokey Storage 2**。

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. **Nitrokey 3** 具有組合的功能集。

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

支持 HOTP 和 TOTP 的型號，有3個 HOTP 插槽，15 個 TOTP 插槽。 有些 Nitrokeys 可以充當密碼管理器。 可以存儲 16 組憑證，並使用與 OpenPGP 接口相同的密碼對憑證加密。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

雖然 Nitrokeys 不會將 HOTP/TOTP 機密釋放給所插入的設備，但HOTP 和 TOTP存儲* *未經加密* * ，容易受到物理攻擊。 如果需要存儲 HOTP 或 TOTP 這類祕密，強烈建議使用Yubikey 代替。

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

重置 Nitrokey 的 OpenPGP 介面會使密碼資料庫變為 [無法存取](https://docs.nitrokey.com/pro/linux/factory-reset)。

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net) firmware.

不同於 YubiKey，Nitrokey 軔體是開源。 NitroKey 型號可（ **NitroKey Pro 2**除外）可更新軔體。

### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

<div class="admonition example" markdown>
<p class="admonition-title">此部份新增</p>

我們正在努力為這個網站的各個部分建立明確標準，它可能依情況變化。 如果您對我們的標準有任何疑問，請在 [論壇上提問](https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

</div>

#### 最低合格要求

- 必須使用高品質、防篡改的硬體安全模組。
- 必須支援最新的 FIDO2 規格。
- 必須不允許私鑰提取。
- 價格超過 35美元的裝置必須支援處理 OpenPGP 和 S/MIME。

#### 最好的情况

最佳案例標準代表了我們希望從這個類別的完美項目應具備的條件。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應採用 USB-C 格式。
- 應與 NFC一起使用。
- 支持 TOTP 機密儲存。
- 應支持安全軔體更新。

## 認證器應用程式

驗證器應用程式實施網際網路工程任務組( IETF)採行的安全標準，稱為 **依據時間的單次密碼**或 **TOTP**。 這是一種網站與您共享祕密的方法，驗證器應用程式使用該祕密根據當前時間生成（通常為）六位數驗證碼，您在登錄網站時輸入以供網站檢查。 通常這些驗證碼每30 秒重新生成一次，一旦生成新碼，舊碼就無用了。 即使駭客獲得六位數的驗證碼，也無法逆轉該代碼去取得原始祕密或透過其他方式去預測以後的驗證碼。

我們強烈建議您使用行動 TOTP 應用程式而不是桌面替代方案，因為 Android 和 iOS 比大多數桌面作業系統具有更好的安全性和應用程式隔離性。

### ente Auth

<div class="admonition recommendation" markdown>

![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**ente Auth** 是一款免費的開源應用，可在行動裝置上儲存和產生 TOTP 令牌。 它可以與線上帳戶一起使用，以安全、端對端加密的方式在裝置上備份和同步令牌（並透過網頁介面存取它們）。 它也可在單一設備上離線使用，無需帳戶。

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** 是一款適用於 Android 的免費開源應用程式，管理線上服務的兩步驟驗證。 Aegis Authenticator 完全離線/本機運行，不同於許多替代方案，它具備匯出令牌以進行備份的選項。

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

### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

<div class="admonition example" markdown>
<p class="admonition-title">此部份新增</p>

我們正在努力為這個網站的各個部分建立明確標準，它可能依情況變化。 如果您對我們的標準有任何疑問，請在 [論壇上提問](https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

</div>

- 源代碼必須公開。
- 無需網際網路連線。
- 不得同步至第三方雲端同步/備份服務。
    - **可選** 支援與作業系統原生工具的 E2EE 同步是可以的，例如透過 iCloud 進行加密同步。
