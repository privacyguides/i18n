---
meta_title: "保護您的隱私和安全的最佳密碼管理器 - Privacy Guides"
title: "密碼管理器"
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
    name: Strongbox
    image: /assets/img/password-management/strongbox.svg
    url: https://strongboxsafe.com
    applicationCategory: 密碼管理器。
    operatingSystem: iOS
    subjectOf:
      "@context": http://schema.org
      "@type": 網頁
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: gopass
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

<small>Protects against the following threat(s):</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**密碼管理器**可讓您使用主密碼安全地儲存和管理密碼及其他憑證。

[密碼介紹 :material-arrow-right-drop-circle:](./basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">資訊</p>

瀏覽器和作業系統所內置的密碼管理器常常不如專用密碼管理器軟體。 內建的密碼管理器優點是與原生軟體很好地整合，但它通常非常簡單，並且缺乏獨立產品具有的隱私和安全功能。

例如，Microsoft Edge 的密碼管理器根本不提供 E2EE。 Google的密碼管理員有 [optional](https://support.google.com/accounts/answer/11350823) 個E2EE ，而 [Apple](https://support.apple.com/HT202303)預設提供E2EE。

</div>

## 雲端型

這些密碼管理員會將您的密碼同步到雲端伺服器，以便您從所有裝置輕鬆存取，並安全地防止裝置丟失。

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** 是一個免費的開源密碼與密鑰管理器。 它旨在解決個人、團隊和商業組織的密碼管理問題。 Bitwarden 是最佳和最安全的解決方案之一，可存儲所有登錄名和密碼，同時方便地在所有設備之間保持同步。

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/mobile/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/bitwarden-free-password-m/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/us/app/bitwarden/id1352778147)

</details>

</div>

Bitwarden uses [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) as its key derivation function (KDF) algorithm by default. It also offers [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id), which is more secure, as an alternative. You can change your account's KDF algorithm in the web vault.

- [x] Select **Settings > Security > Keys > KDF algorithm > Argon2id**

Bitwarden also features [Bitwarden Send](https://bitwarden.com/products/send), which allows you to share text and files securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). 發送分享鏈接時可以要求帶[分享密碼](https://bitwarden.com/help/send-privacy/#send-passwords) 。 Bitwarden Send 還具[自動刪除功能](https://bitwarden.com/help/send-lifespan)。

您需要使用 [高級付費方案](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) 才能共享檔案。 免費方案只允許文字分享。

Bitwarden 伺服器端代碼是 [開源](https://github.com/bitwarden/server)，因此如果不想使用 Bitwarden 雲端，可以輕鬆地託管自己的 Bitwarden 同步伺服器。

**Vaultwarden** 是 Bitwarden 同步伺服器的另一種實作，以 Rust 寫成，並與官方的 Bitwarden 用戶端相容。非常適合用來自架服務，因為使用資源吃重的官方服務可能不是很理想。 如果您想在自己的伺服器上自行託管 Bitwarden，幾乎可以肯定的是，您想使用 Vaultwarden 而不是 Bitwarden 的官方伺服器程式碼。

[:octicons-repo-16: Vaultwarden 儲存庫](https://github.com/dani-garcia/vaultwarden ""){.md-button} [:octicons-info-16:](https://github.com/dani-garcia/vaultwarden/wiki){ .card-link title="說明文件"}
[:octicons-code-16:](https://github.com/dani-garcia/vaultwarden){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/dani-garcia){ .card-link title="貢獻" }

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass 標誌](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** 是由 [Proton Mail] (email.md#protonmail) 背後的團隊 Proton 所開發的開放原始碼、端對端加密的密碼管理器。 它能安全地儲存您的登入憑證、產生獨特的電子郵件別名，並支援和儲存密碼。

[:octicons-home-16: 首頁](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="隱私政策" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="說明文件"}
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/proton-pass-password-manager/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://chromewebstore.google.com/detail/proton-pass-free-password/ghmbeldphafepmbegfdlkpapadhbakde)
- [:octicons-browser-16: 網頁版](https://pass.proton.me)

</details>

</div>

隨著 2022 年 4 月收購 SimpleLogin，Proton 提供了「隱藏我的電子郵件」功能，可建立 10 個別名（免費方案）或無限個別名（付費方案）。

Proton Pass 目前沒有「主密碼」功能，意味著您的保管庫由 Proton 帳戶密碼及[雙因素認證](basics/multi-factor-authentication.md)方法來保護。

Proton Pass 行動應用程式和瀏覽器擴充功能於 2023 年 5 月和 6 月接受了 Cure53 的審核。 安全分析公司的結論為：

> Proton Pass 應用程式和元件在安全性方面給人留下相當正面的印象。

所提出的問題與修正都見諸於

報告< /a>。</p> 



### 1Password

<div class="admonition recommendation" markdown>

![1Password 標誌](assets/img/password-management/1password.svg){ align=right }

**1Password** 是一個密碼管理器，非常注重安全性和易用性，允許您將密碼、密鑰、信用卡、軟體許可證和任何其他敏感資訊存儲在安全的數位保管庫。 您的保管庫託管在 1Password 伺服器，費用為 [每月收取](https://1password.com/sign-up/)。 1Password 定期 [接受審計](https://support.1password.com/security-assessments/) 並提供卓越的客戶支援。 1Password 是封閉原始碼；但是，產品的安全性已徹底記錄在他們的 [安全白皮書](https://1passwordstatic.com/files/security/1password-white-paper.pdf)。

[:octicons-home-16: Homepage](https://1password.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://1password.com/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.1password.com){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/1password-%E2%80%93-password-mana/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/us/app/1password-for-safari/id1569813296)
- [:octicons-browser-16: 網頁版](https://my.1password.com/signin)

</details>

</div>

傳統上，1Password 為使用 macOS 和 iOS 的使用者提供了最佳的密碼管理器使用者體驗；然而，它現在已在所有平台上達成功能均等。 1Password 的用戶端擁有許多面向家庭和不熟悉技術人士的功能，例如直觀的 UI，方便使用和導覽，以及先進的功能。 值得注意的是，1Password 的幾乎所有功能都可在其原生行動或桌面用戶端中使用。

您的 1Password 儲存庫使用您的主密碼和隨機化的 34 個字元安全金鑰來保護，以加密您在其伺服器上的資料。 此安全金鑰為您的資料添加了一層保護，因為無論您的主密碼如何，資料都受到高熵保護。 許多其他密碼管理器解決方案完全依賴於您的主密碼的強度來保護您的數據。



### Psono

<div class="admonition recommendation" markdown>

![Psono logo](assets/img/password-management/psono.svg){ align=right }

**Psono** 是來自德國的免費開源密碼管理器，專注於團隊的密碼管理。 Psono支援安全分享密碼、檔案、書籤和電子郵件。 所有機密都受到主密碼的保護。

[:octicons-home-16: 首頁](https://psono.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="隱私政策" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title="說明文件"}
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/psonopw-password-manager/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono 為其產品提供廣泛的說明文件。 Psono 的網路用戶端可以自行託管；另外，您也可以選擇完整的社群版本或具有額外功能的企業版本。

2024 年 4 月，Psono 僅為瀏覽器擴充套件新增[密碼金鑰的支援](https://psono.com/blog/psono-introduces-passkeys)。



### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。



#### 最低合格要求

- 必須使用強大的、基於標準的/現代的E2EE。
- 必須有徹底記錄的加密和安全實踐。
- 必須公開由信譽良好、獨立的第三方進行的審計。
- 所有非必要的遙測都必須是可選的。
- 除了收費之必要外，不得收集過多個人識別資訊(PII)。



#### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 遙測應選擇加入（預設情況下禁用）或根本不收集。
- 應該是開源的，並且可以合理地自主託管。



## 本地儲存

這些選項可讓您在本機管理加密的密碼資料庫。



### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC 標誌](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC** 是 KeePassX 的社群分支，是 KeePass Password Safe 的原生跨平台移植，目標是以新功能和錯誤修正來擴充和改進它，以提供一個功能豐富、跨平台和現代化的開源密碼管理器。

[:octicons-home-16: 首頁](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="隱私政策" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="原始碼" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title=貢獻 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flatpak](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/keepassxc-browser/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC 將其匯出資料儲存為 [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) 檔案。 如果您將此檔案匯入其他密碼管理器，可能會造成資料遺失。 我們建議您手動檢查每個記錄。



### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX 標誌](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** 是適用於 Android 的輕量級密碼管理器；可在單一檔案中以 KeePass 格式編輯加密資料，並能以安全的方式填寫表格。 應用程式的 [專業版](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) 可讓您解鎖外觀和非標準協定功能，但更重要的是，它有助於並鼓勵開發。

[:octicons-home-16: 首頁](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="原始碼" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title=貢獻 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: GitHub](https://github.com/Kunzisoft/KeePassDX/releases)

</details>

</div>

### Strongbox (iOS & macOS)

<div class="admonition recommendation" markdown>

![Strongbox 標誌](assets/img/password-management/strongbox.svg){ align=right }

**Strongbox** 是 iOS 和 macOS 的原生密碼管理器。 Strongbox 支援 KeePass 和 Password Safe 兩種格式，可在非蘋果平台上與其他密碼管理器 （如 KeePassXC）搭配使用。 透過採用 [基礎免費模式](https://strongboxsafe.com/pricing)，Strongbox 在基礎免費層級下提供大部分功能，而更多以便利為導向的 [功能](https://strongboxsafe.com/comparison)，例如生物辨識驗證，則鎖定在訂閱或永久授權。

[:octicons-home-16: 首頁](https://strongboxsafe.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://strongboxsafe.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://strongboxsafe.com/getting-started){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/strongbox-password-safe/Strongbox){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/strongbox-password-safe/Strongbox#supporting-development){ .card-link title=貢獻 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id897283731)

</details>

</div>

此外，還提供離線版本：[Strongbox Zero](https://apps.apple.com/app/id1581589638)。 此版本經過刪減，試圖減少攻擊面。



### gopass (CLI)

<div class="admonition recommendation" markdown>

![gopass 標誌](assets/img/password-management/gopass.svg){ align=right }

**gopass** 是用 Go 寫成的命令列極簡密碼管理器。 它可在腳本應用程式中使用，並可在所有主要的桌面和伺服器作業系統 (Linux、macOS、BSD、Windows) 上運作。

[:octicons-home-16: 首頁](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title=貢獻 }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用專案前先熟悉此清單，並自行進行研究，以確保它是適合您的選擇。

- 必須跨平台。
