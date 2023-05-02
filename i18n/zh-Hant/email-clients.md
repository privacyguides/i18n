---
title: "電子郵件客戶端程式"
icon: material/email-open
description: 這些電子郵件客戶端尊重隱私並支持OpenPGP電子郵件加密。
cover: email-clients.png
---

我們的推薦清單包含支援 [OpenPGP](encryption.md#openpgp) 和如[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth)強認證的電子郵件用戶端 。 OAuth允許您使用 [多因素驗證](basics/multi-factor-authentication.md) 並防止帳戶被盜。

??? 警告：「電子郵件不提供前向保密」

    當使用端到端加密（ E2EE ）技術（如OpenPGP ）時，電子郵件仍然會有一些未在電子郵件標頭中加密的[一些中繼數據] （ email.md#email-metadata-overview ）。
    
    OpenPGP 也不支援[前向保密] (https://en.wikipedia.org/wiki/Forward_secrecy) ，這意味著如果你或收件人的私鑰被盜，所有以前用它加密的訊息都會被曝光： [如何保護我的私鑰？] (basics/email-security.md)考慮使用提供前向保密的媒介：
    
    [通時通訊] (real-time-communication.md){ .md-button }

## 跨平臺

### Thunderbird

!!! recommendation

    ! [Thunderbird logo] (assets/img/email-clients/thunderbird.svg) {align = right}
    
    * * Thunderbird * *是一個免費、開源、跨平臺的電子郵件、新聞組、新聞提要和聊天(XMPP、IRC、Twitter)客戶端，由Thunderbird 社區開發，之前由 Mozilla 基金會開發。
    
    [:octicons-home-16: Homepage](https://www.thunderbird.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/thunderbird){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.mozilla.org/products/thunderbird){ .card-link title=Documentation}
    [:octicons-code-16:](https://hg.mozilla.org/comm-central){ .card-link title="Source Code" }
    
    ??? 下載
    
        - [:simple-windows11: Windows](https://www.thunderbird.net)
        - [:simple-apple: macOS](https://www.thunderbird.net)
        - [:simple-linux: Linux](https://www.thunderbird.net)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.Thunderbird)

#### 建議配置

我們建議您變更其中一些設定，讓Thunderbird更具私密性。

這些選項可以在 :material-menu: → **設定** → **隱私 & 安全性**中找到。

##### 網頁內容

- [ ]取消勾選  **記住我訪問過的網站和連結**
- [ ]取消勾選  **接受來自網站的cookie**

##### 遙測

- [ ]取消勾選  **允許Thunderbird  向Mozilla**發送技術和互動資訊。

#### Thunderbird-user.js （進階）

[`thunderbird-user.js`](https://github.com/HorlogeSkynet/thunderbird-user.js)，是一組配置選項，旨在禁用 Thunderbird 內過多的網頁瀏覽功能，以減少表面暴露並保持隱私。 其中一些更改是從 [Arkenfox 專案](https://github.com/arkenfox/user.js)中後移的。

## 平臺特定

### Apple Mail (macOS)

!!! recommendation

    ! [Apple Mail標誌] (assets/img/email-clients/applemail.png) {align = right}
    
    * * Apple Mail * *包含在 macOS，並可利用[GPG Suite] (encryption.md#gpg-suite)擴展支援 OpenPGP，增加了發送PGP 加密電子郵件的能力。
    
    [:octicons-home-16: Homepage](https://support.apple.com/guide/mail/welcome/mac){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/en-ww/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/mail){ .card-link title=Documentation}

[macOS](https://support.apple.com/guide/mail/mlhl03be2866/mac) 與[iOS](https://support.apple.com/guide/iphone/iphf084865c7/ios) 的Apple Mail 可在後台載入遠端內容或完全封鎖並能隱藏您的 IP 位址。

### Canary Mail (iOS)

!!! recommendation

    ! [Canary Mail logo] (assets/img/email-clients/canarymail.svg) {align = right}
    
    * * Canary Mail * *是一個付費的電子郵件用戶端，提供無縫的端到端加密安全功能，如生物識別應用程式鎖定。
    
    [:octicons-home-16: Homepage](https://canarymail.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://canarymail.io/privacy.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://canarymail.zendesk.com/){ .card-link title=Documentation}
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.canarymail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1236045954)
        - [:simple-windows11: Windows](https://canarymail.io/downloads.html)

!!! 警告

    Canary Mail 最近才發布了 Windows 和 Android 用戶端，我們不認為它們已如 iOS和 Mac 用戶端一樣穩定。

Canary Mail 源碼為封閉式。 我們推薦它，因為 iOS 電子郵件客戶端支持 PGP E2EE 的選擇很少。

### FairEmail (Android)

!!! recommendation

    ! [FairEmail標誌] (assets/img/email-clients/fairemail.svg) {align = right}
    
    * * FairEmail * *是一個極簡的開源電子郵件應用程式，使用開放標準(IMAP, SMTP, OpenPGP )，數據和電池使用量低。
    
    [:octicons-home-16: Homepage](https://email.faircode.eu){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/M66B/FairEmail/blob/master/PRIVACY.md){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/M66B/FairEmail/blob/master/FAQ.md){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/M66B/FairEmail){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://email.faircode.eu/donate/){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=eu.faircode.email)
        - [:simple-github: GitHub](https://github.com/M66B/FairEmail/releases)

### GNOME Evolution (GNOME)

!!! recommendation

    ! [Evolution logo] (assets/img/email-clients/evolution.svg) {align = right}
    
    * * Evolution * *是個人資訊管理應用程式，提供綜合郵件、行事曆和聯絡簿功能。 Evolution有廣泛的 [文檔](https://help.gnome.org/users/evolution/stable/)來幫助您開始。
    
    [:octicons-home-16: Homepage](https://wiki.gnome.org/Apps/Evolution){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://wiki.gnome.org/Apps/Evolution/PrivacyPolicy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://help.gnome.org/users/evolution/stable/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.gnome.org/GNOME/evolution/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.gnome.org/donate/){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.gnome.Evolution)

### K-9 Mail (Android)

!!! recommendation

    ! [K-9 Mail logo] (assets/img/email-clients/k9mail.svg) {align = right}
    
    * * K-9 Mail * *是一個獨立的郵件應用程式，同時支援 POP3 和IMAP 郵箱，但只支援 IMAP 推送郵件。
    
    未來 K-9 Mai l將成為[官方品牌] (https://k9mail.app/2022/06/13/K-9-Mail-and-Thunderbird.html) Thunderbird Android 用戶端。
    
    [:octicons-home-16: Homepage](https://k9mail.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://k9mail.app/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://docs.k9mail.app/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/k9mail/k-9){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://k9mail.app/contribute){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.fsck.k9)
        - [:simple-github: GitHub](https://github.com/k9mail/k-9/releases)

!!! 警告

    當回覆郵件群組中的某人時，「回覆」選項也可能包括郵件群組。 如需更多資訊，請參閱[thundernest/k-9 # 3738] (https://github.com/thundernest/k-9/issues/3738)。

### Kontact (KDE)

!!! recommendation

    ! [Kontact logo] (assets/img/email-clients/kontact.svg) {align = right}
    
    * * Kontact * *是來自 [KDE](https://kde.org)專案的個人資訊管理器(PIM)應用程式。 它提供了郵件客戶端、地址簿、待辦事項和 RSS 客戶端。
    
    [:octicons-home-16: Homepage](https://kontact.kde.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://kde.org/privacypolicy-apps){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kontact.kde.org/users/){ .card-link title=Documentation}
    [:octicons-code-16:](https://invent.kde.org/pim/kmail){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://kde.org/community/donations/){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-linux: Linux](https://kontact.kde.org/download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.kde.kontact)

### Mailvelope (瀏覽器)

!!! recommendation

    ! [Mailvelope logo] (assets/img/email-clients/mailvelope.svg) {align = right}
    
    * * Mailvelope * *是一個瀏覽器擴充功能，可按照 OpenPGP 加密標準交換加密電子郵件。
    
    [:octicons-home-16: Homepage](https://www.mailvelope.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mailvelope.com/en/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mailvelope.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailvelope/mailvelope){ .card-link title="Source Code" }
    
    ??? 下載
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/mailvelope)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/mailvelope/dgcbddhdhjppfdfjpciagmmibadmoapc)

### NeoMutt (CLI)

!!! recommendation

    ! [NeoMutt logo] (assets/img/email-clients/mutt.svg) {align = right}
    
    * * NeoMutt * *是 Linux 和 BSD 的開源命令行郵件閱讀器（或MUA ）。 它是 [Mutt](https://en.wikipedia.org/wiki/Mutt_ (email_client))的分支，具有附加功能。
    
    NeoMutt 是一個文字指令的客戶端，具有陡峭的學習曲線。 然而，它有高度自制的特色。
    
    [:octicons-home-16: Homepage](https://neomutt.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://neomutt.org/guide/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/neomutt/neomutt){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.paypal.com/paypalme/russon/){ .card-link title=Contribute }
    
    ??? 下載
    
        - [:simple-apple: macOS](https://neomutt.org/distro)
        - [:simple-linux: Linux](https://neomutt.org/distro)

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

!!! 示例“此部分是新的”

    我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在[論壇上提問] (https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

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
