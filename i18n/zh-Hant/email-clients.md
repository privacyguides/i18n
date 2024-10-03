---
title: "電子郵件客戶端"
icon: material/email-open
description: 這些電子郵件客戶端尊重隱私並支持OpenPGP電子郵件加密。
cover: email-clients.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

我們推薦的**電子郵件客戶端**同時支援 [OpenPGP](encryption.md#openpgp) 和比較強的驗證，例如 [Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth)。 OAuth 允許您使用[多因素驗證](basics/multi-factor-authentication.md)，以防止帳號盜用。

<details class="warning" markdown>
<summary>電子郵件不提供前向保密</summary>

當使用端到端加密（ E2EE ）技術（如 OpenPGP ）時，電子郵件仍然會有一些未在電子郵件標頭中加密的[中繼數據](basics/email-security.md#email-metadata-overview)。

OpenPGP 也不支援[前向保密](https://en.wikipedia.org/wiki/Forward_secrecy)，這表示如果您或收件者的私鑰被盜，之前用它加密的所有訊息都會曝光：[我該如何保護我的私鑰呢？](basics/email-security.md)考慮使用提供前向保密功能的媒介：

[即時通訊軟體](real-time-communication.md ""){.md-button}

</details>

## 跨平臺

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** 是一個免費、開源、跨平臺的電子郵件、新聞組、新聞提要和聊天(XMPP、IRC、Matrix)客戶端，由Thunderbird 社區開發，之前由 Mozilla 基金會開發。

[:octicons-home-16: 首頁](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="說明文件" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### 建議的設定

<div class="annotate" markdown>

我們建議您變更其中一些設定，讓 Thunderbird 更私密一點。

這些選項可在 :material-menu: → **設定** → **隱私權與安全性** 中找到。

##### 網站內容

- [ ] 取消勾選 **記住我開啟過的網站和鏈結**
- [ ] 取消勾選 **允許網站設定  Cookie** (1)

</div>

1. 當您登入某些提供商（例如 Gmail）或透過機構的 SSO 時，可能需要保持勾選此設定。 成功登入後，您應該取消勾選。

##### 遙測

- [ ] 取消勾選 **允許 Thunderbird 傳送技術與互動資料傳送給 Mozilla**

#### Thunderbird-user.js （進階）

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) 是一組設定選項，目的是儘可能停用 Thunderbird 內的網頁瀏覽功能，以減少攻擊面並維護隱私。 有些變更是從 [Arkenfox 專案](desktop-browsers.md#arkenfox-advanced) 中得來的。

## 特定平臺

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail logo](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** 已包含在 macOS 中，並可透過 [GPG Suite](encryption.md#gpg-suite) 擴充為 OpenPGP 支援，增加傳送 PGP 加密電子郵件的功能。

[:octicons-home-16: 首頁](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=說明文件}

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">對於 macOS Sonoma 的使用者</p>

目前，GPG Suite [尚未](https://gpgtools.com/sonoma) 有適用於 macOS Sonoma 的穩定版本。

</div>

Apple Mail 具備在背景載入遠端內容或完全封鎖遠端內容的功能，並可在 [macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) 和 [iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios) 上向寄件者隱藏您的 IP 位址。

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Canary Mail logo](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** 是一款需付費的電子郵件用戶端，其設計目的是透過生物辨識應用程式鎖等安全功能，讓端對端加密無懈可擊。

[:octicons-home-16: 首頁](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://canarymail.io/help){ .card-link title="說明文件" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1155470386)
- [:fontawesome-brands-windows: Windows](https://canarymail.io/downloads.html)
- [:simple-apple: macOS](https://apps.apple.com/app/id1236045954)

</details>

</div>

<details class="warning" markdown>
<summary>警告</summary>

Canary Mail 最近推出了 Windows 和 Android 用戶端，不過我們認為它們不如 iOS 和 Mac 的客戶端穩定。

</details>

Canary Mail 是封閉原始碼的。 由於 iOS 上支援 PGP E2EE 的電子郵件用戶端選擇不多，因此我們推薦您使用。

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![FairEmail logo](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** 是一款極簡、開放原始碼的電子郵件應用程式，使用開放標準 (IMAP、SMTP、OpenPGP)，並將資料和電池使用量降至最低。

[:octicons-home-16: 首頁](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="原始碼" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Evolution logo](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** 是個人資訊管理應用程式，提供整合的郵件、行事曆和通訊錄功能。 Evolution 有大量的[說明文件](https://help.gnome.org/users/evolution/stable)，可以幫助您開始使用。

[:octicons-home-16: 首頁](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title="說明文件" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="原始碼" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![K-9 Mail 標誌](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** 是一個獨立的郵件應用程式，同時支援 POP3 和 IMAP 信箱，但只支援 IMAP 的推送郵件。

未來，K-9 Mail 將成為 Thunderbird 的[官方品牌](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) Android 用戶端。

[:octicons-home-16: 首頁](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="原始碼" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

回覆郵件名單上的某人時，「回覆」選項也可能包括郵件名單。 如需詳細資訊，請參閱 [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738)。

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact 標誌](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** 是 [KDE](https://kde.org) 專案的個人資訊管理員 (PIM) 應用程式。 它提供郵件用戶端、通訊錄、RSS 用戶端和數位筆記等功能。

[:octicons-home-16: 首頁](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title="說明文件" }
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="原始碼" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (瀏覽器)

<div class="admonition recommendation" markdown>

![Mailvelope logo](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** 是一個瀏覽器擴充套件，可依照 OpenPGP 加密標準支援加密電子郵件。

[:octicons-home-16: 首頁](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title="說明文檔" }
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![NeoMutt logo](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** 是適用於 Linux 和 BSD 的開放原始碼命令行電子郵件閱讀器。 它是 [Mutt](https://zh.wikipedia.org/wiki/Mutt) 的分支，並增加了一些功能。

NeoMutt 是一個以命令行為基礎的客戶端，其學習曲線非常陡峭。 不過，它具有能高度自定義的特色。

[:octicons-home-16: 首頁](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="原始碼" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 為開源作業系統開發的應用程式必須是開源的
- 必須不收集遙測資料，或有簡單的方法停用所有遙測資料
- 必須支援 OpenPGP 訊息加密

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 必須開放原始碼
- 必須跨平臺
- 預設不收集任何資料
- 應該原生支持 OpenPGP ，即沒有擴充元件
- 應支援本機儲存 OpenPGP 加密的電子郵件
