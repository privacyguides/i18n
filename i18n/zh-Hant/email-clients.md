---
title: "電子郵件客戶端程式"
icon: material/email-open
description: 這些電子郵件客戶端尊重隱私並支持OpenPGP電子郵件加密。
cover: email-clients.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

The **email clients** we recommend support both [OpenPGP](encryption.md#openpgp) and strong authentication such as [Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth). OAuth allows you to use [Multi-Factor Authentication](basics/multi-factor-authentication.md) to prevent account theft.

<details class="warning" markdown>
<summary>電子郵件不提供前向保密</summary>

當使用端到端加密（ E2EE ）技術（如OpenPGP ）時，電子郵件仍然會有一些未在電子郵件標頭中加密的[中繼數據](basics/email-security.md#email-metadata-overview)。

OpenPGP 也不支援[前向保密](https://en.wikipedia.org/wiki/Forward_secrecy)，這意味著如果你或收件人的私鑰被盜，所有以前用它加密的訊息都會被曝光：[[如何保護我的私鑰？](basics/email-security.md)考慮使用提供前向保密的媒介：

[即時通訊軟體](real-time-communication.md ""){.md-button}

</details>

## 跨平臺

### Thunderbird

<div class="admonition recommendation" markdown>

![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ align=right }

**Thunderbird** 是一個免費、開源、跨平臺的電子郵件、新聞組、新聞提要和聊天(XMPP、IRC、Matrix)客戶端，由Thunderbird 社區開發，之前由 Mozilla 基金會開發。

[:octicons-home-16: Homepage](https://thunderbird.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://thunderbird.net)
- [:simple-apple: macOS](https://thunderbird.net)
- [:simple-linux: Linux](https://thunderbird.net)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

</details>

</div>

#### 建議配置

我們建議您變更其中一些設定，讓Thunderbird更具私密性。

這些選項可以在 :material-menu: → **設定** → **隱私 & 安全性**中找到。

##### 網頁內容

- [ ] 取消勾選  **記住我訪問過的網站和連結**
- [ ] 取消勾選  **接受來自網站的cookie**

##### 遙測

- [ ] 取消勾選  **允許Thunderbird  向Mozilla**發送技術和互動資訊。

#### Thunderbird-user.js （進階）

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js) is a set of configuration options that aims to disable as many of the web-browsing features within Thunderbird as possible in order to reduce attack surface and maintain privacy. Some of the changes are backported from the [Arkenfox project](desktop-browsers.md#arkenfox-advanced).

## 平臺特定

### Apple Mail (macOS)

<div class="admonition recommendation" markdown>

![Apple Mail標誌](assets/img/email-clients/applemail.png){ align=right }

**Apple Mail** 包含在 macOS，並可利用[GPG Suite](encryption.md#gpg-suite)擴展支援 OpenPGP，增加了發送PGP 加密電子郵件的能力。

[:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/en-ww){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

</details>

</div>

[macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) 與[iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios) 的Apple Mail 可在後台載入遠端內容或完全封鎖並能隱藏您的 IP 位址。

### Canary Mail (iOS)

<div class="admonition recommendation" markdown>

![Canary Mail logo](assets/img/email-clients/canarymail.svg){ align=right }

**Canary Mail** 是一個付費的電子郵件用戶端，提供無縫的端到端加密安全功能，如生物識別應用程式鎖定。

[:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://canarymail.io/help){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1155470386)
- [:fontawesome-brands-windows: Windows](https://canarymail.io/downloads.html)
- [:simple-apple: macOS](https://apps.apple.com/app/id1236045954)

</details>

</div>

<details class="warning" markdown>
<summary>警告</summary>

Canary Mail 最近才發布了 Windows 和 Android 用戶端，我們不認為它們已如 iOS和 Mac 用戶端一樣穩定。

</details>

Canary Mail 源碼為封閉式。 我們推薦它，因為 iOS 電子郵件客戶端支持 PGP E2EE 的選擇很少。

### FairEmail (Android)

<div class="admonition recommendation" markdown>

![FairEmail logo](assets/img/email-clients/fairemail.svg){ align=right }

**FairEmail** is a minimal, open-source email app which uses open standards (IMAP, SMTP, OpenPGP) and minimizes data and battery usage.

[:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://email.faircode.eu/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
- [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

</details>

</div>

### GNOME Evolution (GNOME)

<div class="admonition recommendation" markdown>

![Evolution logo](assets/img/email-clients/evolution.svg){ align=right }

**Evolution** 是個人資訊管理應用程式，提供綜合郵件、行事曆和聯絡簿功能。 Evolution有豐富的 [文件](https://help.gnome.org/users/evolution/stable/)來協助入手。

[:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
[:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.gnome.org/users/evolution/stable){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gnome.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

</details>

</div>

### K-9 Mail (Android)

<div class="admonition recommendation" markdown>

![K-9 Mail logo](assets/img/email-clients/k9mail.svg){ align=right }

**K-9 Mail** 是一個獨立的郵件應用程式，同時支援 POP3 和IMAP 郵箱，但只支援 IMAP 推送郵件。

未來 K-9 Mai l將成為 [官方品牌](https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) Thunderbird Android 用戶端。

[:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.k9mail.app){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/thundernest/k-9){ .card-link title="Source Code" }
[:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
- [:simple-github: GitHub](https://github.com/thundernest/k-9/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

When replying to someone on a mailing list, the "reply" option may also include the mailing list. 如需更多資訊，請參閱 [thundernest/k-9 #3738](https://github.com/thundernest/k-9/issues/3738)。

</div>

### Kontact (KDE)

<div class="admonition recommendation" markdown>

![Kontact logo](assets/img/email-clients/kontact.svg){ align=right }

**Kontact** 是來自 [KDE](https://kde.org)專案的個人資訊管理器(PIM)應用程式。 It provides a mail client, address book, RSS client, and an organizer.

[:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kontact.kde.org/users){ .card-link title="Documentation" }
[:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kde.org/community/donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-linux: Linux](https://kontact.kde.org/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

</details>

</div>

### Mailvelope (瀏覽器)

<div class="admonition recommendation" markdown>

![Mailvelope logo](assets/img/email-clients/mailvelope.svg){ align=right }

**Mailvelope** 是一個瀏覽器擴充功能，可按照 OpenPGP 加密標準交換加密電子郵件。

[:octicons-home-16: Homepage](https://mailvelope.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailvelope.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mailvelope.com/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

</details>

</div>

### NeoMutt (CLI)

<div class="admonition recommendation" markdown>

![NeoMutt logo](assets/img/email-clients/mutt.svg){ align=right }

**NeoMutt** is an open-source command line email reader for Linux and BSD. 它是 [Mutt](https://en.wikipedia.org/wiki/Mutt_ (email_client)) 的分支，具有附加功能。

NeoMutt 是一個文字指令的客戶端，具有陡峭的學習曲線。 It is, however, very customizable.

[:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://neomutt.org/guide){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://paypal.com/paypalme/russon){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: macOS](https://neomutt.org/distro)
- [:simple-linux: Linux](https://neomutt.org/distro)

</details>

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 為開源作業系統開發的應用程式必須是開源的。
- 必須不收集遙測，或有一個簡單的方法來禁用所有遙測。
- 必須支援OpenPGP訊息加密。

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應該為開源的。
- 應為跨平臺。
- 預設情況下不應收集任何遙測。
- 應該原生支持OpenPGP ，即沒有擴展。
- 應該支持在本地存儲 OpenPGP 加密的電子郵件。
