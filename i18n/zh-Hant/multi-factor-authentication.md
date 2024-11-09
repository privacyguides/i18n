---
title: "多重要素驗證"
icon: 'material/two-factor-authentication'
description: 這些工具可協助透過多重身份驗證保護網路帳戶，而無需將您的祕密傳送給第三方。
cover: multi-factor-authentication.webp
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">硬體金鑰</p>

[硬體安全金鑰推薦](security-keys.md) 已移至其本身的類別。

</div>

**多因素驗證器應用程式**實施網際網路工程任務組( IETF) 採行的安全標準，稱為 **依據時間的單次密碼**或 **TOTP**。 這是一種網站與您共享祕密的方法，驗證器應用程式使用該祕密根據當前時間生成（通常為）六位數驗證碼，您在登錄網站時輸入以供網站檢查。 通常這些驗證碼每30 秒重新生成一次，一旦生成新碼，舊碼就無用了。 即使駭客獲得六位數的驗證碼，也無法逆轉該代碼去取得原始祕密或透過其他方式去預測以後的驗證碼。

我們強烈建議您使用行動 TOTP 應用程式而不是桌面替代方案，因為 Android 和 iOS 比大多數桌面作業系統具有更好的安全性和應用程式隔離性。

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** 是一個自由且開放原始碼的應用程式，可儲存私鑰並產生 TOTP 一次性密碼。 它可以與線上帳戶一起使用，以安全、端對端加密的方式在裝置上備份和同步令牌（並透過網頁介面存取它們）。 它也可在單一設備上離線使用，無需帳戶。

[:octicons-home-16: 首頁](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: 網頁版](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** 是一款適用於 Android 的自由且開放原始碼應用程式，管理線上服務的兩步驟驗證。 Aegis Authenticator 完全離線/本機運行，不同於許多替代方案，它具備匯出令牌以進行備份的選項。

[:octicons-home-16: 首頁](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="原始碼" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 源代碼必須公開。
- 無需網際網路連線。
- 雲端同步功能必須是非強迫的，而且（如該軟體有）同步功能則其必須採納 E2EE。
