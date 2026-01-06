---
meta_title: "保護您的隱私和安全的最佳密碼管理器 - Privacy Guides"
title: 密碼管理器
icon: material/form-textbox-password
description: 密碼管理器可讓您安全地儲存和管理密碼及其他憑證。
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": 網頁
    name: 密碼管理器建議
    url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://en.wikipedia.org/wiki/Bitwarden
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://en.wikipedia.org/wiki/KeePassXC
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: 密碼管理器。
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: 密碼管理器。
    operatingSystem:
      - Windows 作業系統
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
---

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**密碼管理器**可讓您使用主密碼安全地儲存和管理密碼及其他憑證。

[密碼介紹 :material-arrow-right-drop-circle:](basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">資訊</p>

瀏覽器和作業系統所內建的密碼管理器常常不如專用密碼管理器軟體。 內建密碼管理器的優點在於與原生軟體的良好整合，但它通常功能較少，而且缺乏獨立產品所具有的隱私和安全特點。

舉例來說，Microsoft Edge 的密碼管理程式完全不提供端到端加密。 Google的密碼管理員則 [須自行啟用](https://support.google.com/accounts/answer/11350823) E2EE，而 [Apple](https://support.apple.com/HT202303) 預設提供E2EE。

</div>

## 雲端型

這些密碼管理員會將您的密碼同步到雲端伺服器，以便您從所有裝置輕鬆存取，並安全地防止裝置丟失。

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** 是一個免費的開源密碼與金鑰管理器。 它旨在解決個人、團隊和商業組織的密碼管理問題。 Bitwarden 是最佳和最安全的解決方案之一，可儲存所有登錄名和密碼，同時方便地在所有設備之間保持同步。

[:octicons-home-16: 首頁](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/app/id1352778147)

</details>

</div>

Bitwarden 預設使用 [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) 作為其 金鑰衍生函式(KDF) 演算法。 它也提供更安全的 [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id) 作為可選方案。 您可以在網頁保管箱中變更帳號的 KDF 演算法：

- [x] 選取**設定 → 安全性 → 金鑰 → KDF 演算法 → Argon2id**

Bitwarden 伺服器端代碼是 [開源的](https://github.com/bitwarden/server)，因此如果不想使用 Bitwarden 雲端，可以輕鬆地託管自己的 Bitwarden 同步伺服器。

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass 標誌](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** 是由 [Proton Mail](email.md#protonmail) 背後的團隊 Proton 所開發的開放原始碼、端對端加密的密碼管理器。 它能安全地儲存您的登入憑證、產生獨特的電子郵件別名，並支援儲存密碼。

[:octicons-home-16: 首頁](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/gcllgfdnfnllodcaambdaknbipemelie)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

隨著 2022 年 4 月收購 SimpleLogin，Proton 提供了「隱藏我的電子郵件」功能，可建立 10 個別名（免費方案）或無限個別名（付費方案）。

Proton Pass 行動應用程式和瀏覽器擴充功能於 2023 年 5 月和 6 月接受了 Cure53 的審核。 安全分析公司的結論為：

> Proton Pass 應用程式和元件在安全性方面給人留下相當正面的印象。

所提出的問題與修正可在 [報告](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf) 中見到。

### 1Password

<div class="admonition recommendation" markdown>

![1Password 標誌](assets/img/password-management/1password.svg){ align=right }

**1Password** 是強調安全性與易用性的密碼管理器，可讓您將密碼、金鑰、信用卡、軟體許可證以及其他任何敏感資訊儲存於安全的數位保險庫中。 您的保管庫託管在 1Password 伺服器，費用為 [每月收取](https://1password.com/sign-up/)。

1Password 定期 [接受審計](https://support.1password.com/security-assessments/) 並提供卓越的客戶支援。 1Password 是封閉原始碼；但是，產品的安全性已徹底記錄在他們的 [安全白皮書](https://1passwordstatic.com/files/security/1password-white-paper.pdf)。

[:octicons-home-16: 首頁](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.1password.com){ .card-link title="說明文件" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/app/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

過去 1Password 僅為 macOS 和 iOS 的用戶提供最佳的密碼管理器用戶體驗，不過它現在已在所有平臺上實現了同等優秀的用戶體驗。 1Password's clients boast many features geared towards families and less technical people, such as an intuitive UI for ease-of-use and navigation, as well as advanced functionality. 值得注意的是，1Password 的幾乎所有功能都可在其原生行動或桌面用戶端中使用。

您的 1Password 儲存庫使用您的主密碼和隨機化的 34 個字元安全金鑰來保護，以加密您在其伺服器上的資料。 此安全金鑰為您的資料添加了一層保護，因為無論您的主密碼如何，資料都受到高熵保護。 許多其他密碼管理器解決方案完全依賴於您的主密碼的強度來保護您的數據。

### Psono

<div class="admonition recommendation" markdown>

![Psono logo](assets/img/password-management/psono.svg){ align=right }

**Psono** 是來自德國的免費開源密碼管理器，專注於團隊的密碼管理。 Psono支援安全分享密碼、檔案、書籤和電子郵件。 所有機密都受到主密碼的保護。

[:octicons-home-16: 首頁](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="說明文件" }
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono 為其產品提供廣泛的說明文件。 Psono 的網路用戶端可以自行託管；另外，您也可以選擇完整的社群版本或具有額外功能的企業版本。

2024 年 4 月，Psono 僅為瀏覽器擴充套件新增[密碼金鑰的支援](https://psono.com/blog/psono-introduces-passkeys)。

### 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

#### 最低合格要求

- 必須使用強大的、基於標準的/現代的E2EE。
- 必須有徹底記錄的加密和安全實踐。
- 必須由信譽良好的獨立第三方進行公開審核。
- 所有非必要的遙測都必須是可選的。
- 除了收費之必要外，不得收集過多個人識別資訊(PII)。

#### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 遙測應選擇加入（預設情況下禁用）或根本不收集。
- 應該是開源的，並且可以合理地自主託管。

## 本地儲存

這些選項可讓您在本機管理加密的密碼資料庫。

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC logo](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** 是 KeePassX 的社群分支，是 KeePass Password Safe 的原生跨平台移植，目標是以新功能和錯誤修正來擴充和改進它，以提供一個功能豐富、跨平台和現代化的開源密碼管理器。

[:octicons-home-16: 首頁](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="原始碼" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC 將其匯出資料儲存為 [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) 檔案。 如果您將此檔案匯入其他密碼管理器，可能會造成資料遺失的問題。 我們建議您手動檢查每個記錄。

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX logo](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** 是適用於 Android 的輕量級密碼管理器；可在單一檔案中以 KeePass 格式編輯加密資料，並能以安全的方式提供自動填入功能。

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

The [pro version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) of the app allows you to unlock cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.

### KeePassium (iOS & macOS)

<div class="admonition recommendation" markdown>

![KeePassium logo](assets/img/password-management/keepassium.svg){ align=right }

KeePassium is a commercial, open-source password manager made by KeePassium Labs that's compatible with other KeePass applications. It provides autofill support, passkey management, automatic two-way synchronization through [most cloud storage providers](https://support.keepassium.com/kb/sync), and more.

[:material-star-box: Read our latest KeePassium review.](https://www.privacyguides.org/articles/2025/05/13/keepassium-review)

[:octicons-home-16: Homepage](https://keepassium.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassium.com/privacy/app){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.keepassium.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/keepassium/KeePassium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassium.com/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/id1435127111)

</details>

</div>

KeePassium offers a [Premium version](https://keepassium.com/pricing) with additional features such as support for multiple databases, YubiKey support, and a password audit tool.

KeePassium's iOS app has been [audited](https://cure53.de/pentest-report_keepassium.pdf) by Cure53 in October 2024, and all [issues](https://keepassium.com/blog/2024/11/independent-security-audit-complete) found in the audit were subsequently fixed.

### Gopass (CLI)

<div class="admonition recommendation" markdown>

![Gopass logo](assets/img/password-management/gopass.svg){ align=right }

**Gopass** is a minimal password manager for the command line written in Go. 它可在 腳本應用程式("scripting applications") 中使用，且支援所有主要的桌面和伺服器作業系統。

[:octicons-home-16: 首頁](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 必須跨平台。
