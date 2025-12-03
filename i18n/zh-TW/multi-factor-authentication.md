---
title: 多重要素驗證
icon: material/two-factor-authentication
description: 這些工具可協助您使用多重要素驗證保護您的網際網路帳號，而不需要將您的祕密傳送給第三方。
cover: multi-factor-authentication.webp
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">實體金鑰</p>

[實體安全金鑰推薦](security-keys.md) 已移至其本身的類別。

</div>

**多重要素驗證應用程式**實作網際網路工程任務組 (IETF) 採納的安全標準，稱為**基於時間的一次性密碼演算法**或 **TOTP**。 這是一種基於網站與您共享的金鑰的驗證方法，驗證器應用程式使用該金鑰根據當前時間生成（通常為）六位數驗證碼，您在登錄網站時輸入以供網站檢查。 通常這些驗證碼每 30 秒重新生成一次，一旦生成新代碼，舊代碼就無用了。 即使駭客獲得六位數的驗證碼，也無法逆轉該代碼去取得原始祕密或透過其他方式去預測以後的驗證碼。

我們強烈建議您使用行動 TOTP 應用程式而不是桌面替代方案，因為 Android 和 iOS 比大多數桌面作業系統具有更好的安全性和應用程式隔離性。

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** 是一個自由且開放原始碼的應用程式，可儲存私鑰並產生 TOTP 一次性密碼。 它可與線上帳戶一起使用，以安全、端對端加密的方式備份和同步您各個裝置上的 令牌 (token)，並透過網頁介面存取。 它也可在單一設備上離線使用，無需帳戶。

[:octicons-home-16: 首頁](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-browser-16: 網頁](https://auth.ente.io)

</details>

</div>

若搭配線上帳號使用，Ente Auth 的伺服器端原始碼與基礎架構已於2025年10月接受 [Cure53](https://ente.io/blog/cern-audit) 的安全稽核。

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** 是一款適用於 Android 的自由且開放原始碼應用程式，管理線上服務的兩步驟驗證。 Aegis Authenticator 完全離線/本機運行，不同於許多替代方案，它具備匯出令牌以進行備份的選項。

[:octicons-home-16: 首頁](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="原始碼" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 原始碼必須公開。
- 無需網際網路連線。
- 雲端同步功能必須可自由選擇；若提供同步功能，則必須採用端對端加密。
