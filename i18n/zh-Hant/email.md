---
meta_title: "加密私人電子郵件建議 - Privacy Guides"
title: "電子郵件服務"
icon: material/email
description: 這些電子郵件提供商提供了一個好地方來安全地存儲您的電子郵件，也有不少能與其他供應商相互操作的 OpenPGP 加密。
cover: email.webp
---

<!-- markdownlint-disable MD024 -->
電子郵件實際上是使用任何線上服務的必需品，但我們不建議把它應用於人與人之間的對話。 與其使用電子郵件聯繫他人，不如考慮使用支援前向保密的即時通訊媒介。

[推薦的即時通訊工具](real-time-communication.md ""){.md-button}

除此之外，我們還推薦各種基於可持續商業模式和內置安全和隱私功能的電子郵件提供商。

- [OpenPGP 兼容的郵件提供商 :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [其他加密提供者 :material-arrow-right-drop-circle:](#more-providers)
- [自主託管選項 :material-arrow-right-drop-circle:](#self-hosting-email)

除（或代替）此處推薦的電子郵件提供者之外，可能還希望考慮使用專門的[電子郵件別名服務](email-aliasing.md)來保護隱私。 除此之外，這些服務有助於保護真實收件匣免受垃圾郵件的侵害，防止行銷人員關聯您的帳戶，並使用 PGP 加密所有傳入的訊息。

- [更多資訊 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP 兼容服務

這些供應商原生支援 OpenPGP 加密以及 [Web Key Directory 標準](basics/email-security.md#what-is-the-web-key-directory-standard)，可進行 provider-agnostic E2EE 電郵。 例如， Proton Mail 用戶可以向 Mailbox.org 用戶發送 E2EE 消息，或者您可以從它支援的網際網路服務接收 OpenPGP 加密通知。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

當使用像 OpenPGP 這類 E2EE 技術時，電子郵件仍然會有一些元數據無法加密如主旨列。 了解更多[電子郵件元數據](basics/email-security.md#email-metadata-overview).

OpenPGP 也不支持前向保密，這意味著如果你或收件人的私鑰被盜，所有以前用它加密的消息都會洩露。 [[如何保護我的私鑰？](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** 是一個專注於隱私、加密、安全性和易用性的電子郵件服務。 自 **2013 年** 開始運營。 Proton AG 總部位於瑞士日內瓦。 Accounts start with 1 GB of storage with their free plan.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: 網頁版](https://mail.proton.me)

</details>

</div>

免費帳戶有一些功能限制，例如無法搜索郵件正文內容，也無法無法使用 [Proton Mail Bridge](https://proton.me/mail/bridge)；後者是使用[建議的桌面郵件客戶端](email-clients.md) (例如 Thunderbird) 所需的。 付費帳戶包括 Proton Mail Bridge、額外儲存空間和自訂網域支援等功能。 Proton Mail 應用程式於 2021 年 11 月 9 日由 [Securitum](https://research.securitum.com) 提供[認證函](https://proton.me/blog/security-audit-all-proton-apps) 。

If you have the Proton Unlimited, Business, Family, or Visionary Plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. 可以在以下位置停用此功能：**設定** > **前往設定** > **帳戶** > **安全和隱私** > **傳送崩潰報告**。

#### :material-check:{ .pg-green } 自訂域名和別名

付費的 Proton Mail 訂閱者可以使用自定網域服務或 [通用電子郵件](https://proton.me/support/catch-all) 功能。 Proton Mail 還支持 [子地址](https://proton.me/support/creating-aliases)，這對於不想購買網域的人很有用。

#### :material-check:{ .pg-green } 私密付款方式

Proton Mail 除了[支持](https://proton.me/support/payment-options)郵寄現金外，還接受信用卡/簽帳卡、[Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 和 PayPal 付款。

#### :material-check:{ .pg-green } 帳號安全

Proton Mail 支援使用 TOTP [雙因素驗證](https://proton.me/support/two-factor-authentication-2fa) 和採用 FIDO2 或 U2F 標準的 [硬體安全金鑰](https://proton.me/support/2fa-security-key)。 使用硬體安全金鑰需要先設定 TOTP 雙因素驗證。

#### :material-check:{ .pg-green } 資料安全

Proton Mail 使用「[零存取加密技術](https://proton.me/blog/zero-access-encryption)」來保護電子郵件和[行事曆](https://proton.me/news/protoncalendar-security-model)的資料安全。 使用「零存取加密技術」保護的數據只能由您訪問。

存儲在 [Proton 通錄](https://proton.me/support/proton-contacts)中的某些資訊，例如顯示名稱和電子郵件地址，並未使用零存取加密進行保護。 支援零存取加密的聯絡人欄位(例如電話號碼)會以掛鎖圖示顯示。

#### :material-check:{ .pg-green } 電子郵件加密

Proton Mail 網頁郵件整合了 [OpenPGP 加密](https://proton.me/support/how-to-use-pgp) 。 發送到其他 Proton Mail 帳號的電子郵件會自動加密，並且可以在您的帳號設置中輕鬆啟用「使用 OpenPGP 金鑰對非 Proton Mail 地址進行加密」。 Proton 也支援透過 [Web 金鑰目錄 (WKD)](https://wiki.gnupg.org/WKD) 自動發現外部金鑰。 因此發送到使用 WKD 的其他供應商的電子郵件也將使用 OpenPGP 自動加密，無需與聯絡人手動交換公共 PGP 金鑰。 它可以 [加密非 Proton Mail 郵件地址的訊息](https://proton.me/support/password-protected-emails)，不必非得使用帶OpenPGP 的 Proton Mail 帳戶。

Proton Mail 也透過 HTTP 從其 WKD 發布 Proton 帳戶的公鑰。 這可讓非 Proton Mail 使用者可以輕鬆找到 Proton Mail 帳戶的 OpenPGP 金鑰，以利跨供應商進行 E2EE 。 這僅限於使用 Proton 自身網域別名 (例如 @proton.me) 的電子郵件。 如果使用自定域名，則須另行[設定 WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) 。

#### :material-information-outline:{ .pg-blue } 終止帳號

若您的付費帳戶逾期 14 天[未付款](https://proton.me/support/delinquency)，您將無法讀取自己的資料。 30 天後，您的帳戶將標記為欠費狀態，無法再收取郵件。 在此期間，我們會繼續向你收費。 Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address on a deactivated account.

#### :material-information-outline:{ .pg-blue } 額外功能

Proton Mail 提供每月 9.99 歐元的"Unlimited" 帳號，除了提供多個帳號、域名、別名和 500GB 儲存空間外，還可以使用 Proton VPN。

Proton Mail 不提供數字遺產功能。

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org 標誌](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** 電子郵件服務，專注於安全、無廣告和使用 100% 民間環保發電能源。 自 **2014 年** 開始運營。 Mailbox.org  總部位於德國柏林。 初級帳戶有 2GB 儲存空間，可以根據需要升級。

[:octicons-home-16: 首頁](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="文件" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:octicons-browser-16: 網頁版](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } 自訂域名和別名

Mailbox.org 可使用自定域名，且支援 [捕獲所有](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all- alias-with-a-custom-domain-name) 位址。 Proton Mail還支持 <[子地址](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it)，這對於不想購買網域的人很有用。

#### :material-check:{ .pg-green } 私人付款方式

Mailbox.org 不接受任何加密貨幣，因為他們的支付處理商 BitPay 暫停了德國業務。 However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } 帳號安全

Mailbox.org [雙重認證](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)功能僅限網頁郵件。 可透過 [TOTP 或 [YubiKey](https://en.wikipedia.org/wiki/YubiKey) -software /yubicloud">YubiCloud](https://yubico.com/products/services)。 Web 標準如 [WebAuthn ](https://en.wikipedia.org/wiki/WebAuthn) 尚不支援。

#### :material-information-outline:{ .pg-blue } 資料安全

Mailbox.org 允許使用 [加密郵箱](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox)對傳入郵件進行加密。 收到的新訊息將立即用您的公鑰加密。

不迥 Mailbox.org 使用的軟體平台 [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange)[不支援](https:// kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book)通訊錄和行事曆加密。 [獨立的選項](calendar.md) 可能更適合該資訊。

#### :material-check:{ .pg-green } 電子郵件加密

Mailbox.org在他們的網絡郵件中有 [個集成的加密](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) ，這簡化了向具有公開OpenPGP密鑰的人發送消息。 它們可讓

遠端收件者在 Mailbox.org 的伺服器上解密電子郵件</ a > 。 當遠端收件人沒有 OpenPGP 無法解密自己郵箱中的電子郵件時，此功能非常有用。</p> 

Mailbox.org 還支持通過 HTTP 的 [Web密鑰目錄（ WKD ）](https://wiki.gnupg.org/WKD)發現公鑰。 因此其它人可以輕鬆找到 Mailbox.org 帳戶的 OpenPGP 金鑰，便於跨提供者使用 E2EE。 這僅限於使用 Mailbox.org  自身網域(例如 @mailbox.org) 的電子郵件。 如果使用自定域名，則須另行[設定 WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) 。



#### :material-information-outline:{ .pg-blue } 終止帳號

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).



#### :material-information-outline:{ .pg-blue } 額外功能

可利用他們的[洋蔥服務](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)與 IMAP/SMTP 協議來訪問 Mailbox.org 帳戶。 然而，他們的網頁郵件介面無法訪問其  .onion 服務，可能會遇到 TLS 憑證錯誤。

所有帳號都附帶有限的[可以加密](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive)雲端儲存空間 。 Mailbox.org 還提供別名 [@ secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)，它對郵件伺服器之間的連線強制進行TLS加密，否則根本不會發送訊息。 Mailbox.org 除了支援 IMAP 和 POP3 等標準存取通訊協議外，還支援 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) 。

Mailbox.org 所有方案都提供了數位遺產功能。 你可以選擇是否要將任何資料傳遞給繼承人，但對方必須提出你的遺囑證明。 或者，您可以通過姓名和地址提出人選。



## 更多供應商

這些提供商以零知識加密方式儲存您的電子郵件，使其成為保護儲存電子郵件安全的絕佳選擇。 但是，它們不支持供應商之間可相互操作 E2EE 通信的加密標準。

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** 使用加密、關注安全和隱私的電子郵件服務。 Tuta 自 **2011 年** 開始運營，總部位於德國漢諾威。 免費帳戶有 1GB 儲存空間。

[:octicons-home-16: 首頁](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="原始碼" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta 不支援 [ IMAP 協議](https://tuta.com/faq/#imap) 或使用第三方 [電子郵件客戶端](email-clients.md)，您也無法將 [外部電子郵件帳戶](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) 添加到 Tuta 應用程式。 目前不支援[匯入電子郵件](https://github.com/tutao/tutanota/issues/630) ，但這點很快就[會改善](https://tuta.com/blog/posts/kickoff-import)。 Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.



#### :material-check:{ .pg-green } 自訂域名和別名

付費的 Tuta 帳戶可以根據其方案使用 15 或 30 個別名，並且在[自訂域名](https://tuta.com/support#custom-domain)上可以使用無限個別名。 Tuta 不允許使用[子地址 (加號地址)](https://tuta.com/support#plus)，但您可以在自訂域名上使用[接收所有郵件](https://tuta.com/support#settings-global)功能。



#### :material-information-outline:{ .pg-blue } 私密付款方式

Tuta 僅接受信用卡和 PayPal ，但 [加密貨幣](cryptocurrency.md) 可用於通過其[ 合作伙伴 Proxystore ](https://tuta.com/faq/#cryptocurrency) 購買禮品卡。



#### :material-check:{ .pg-green } 帳號安全

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.



#### :material-check:{ .pg-green } 資料安全

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). 這意味著儲存在您帳戶中的訊息和其他資料只有您能讀取。



#### :material-information-outline:{ .pg-blue } 電子郵件加密

Tuta [不使用 OpenPGP ](https://tuta.com/support/#pgp)。 只能透過 [臨時 Tuta 郵箱](https://tuta.com/support/#encrypted-email-external)，才能接收非Tuta 電子郵件帳戶寄出的加密電子郵件。



#### :material-information-outline:{ .pg-blue } 終止帳號

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. 付費後，可以重用激活已停用的免費帳戶。



#### :material-information-outline:{ .pg-blue } 額外功能

Tuta 向非營利組織提供免費 [商業版本](https://tuta.com/blog/posts/secure-email-for-non-profit) 或大幅折扣。

Tuta 不提供數位遺產功能。



## 自主託管電子郵件

進階系統管理員可以考慮設定自己的電子郵件伺服器。 郵件伺服器需要注意和持續維護，以確保安全性和郵件傳遞的可靠性。



### 結合軟體解決方案

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** 是一個更先進的郵件伺服器，非常適合有豐富 Linux 經驗者。 它的 Docke r容器中擁有您需要的一切：支援 DKIM 的郵件伺服器、防毒和垃圾郵件監控、具有SOGo 的 Webmail 和 ActiveSync ，以及具有2FA 支援的網頁管理介面。

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align = right }

**Mail-in-a-Box** 是部署 Ubuntu 郵件伺服器的自動設置腳本。 它的目標是讓人們更容易建立自己的郵件伺服器。

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

為了更清楚手動設定方法，我們挑選了這兩篇文章：

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)



## 標準

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.



### 技術

我們認為這些功能很重要，以便提供安全和最佳的服務。 您應該考慮提供商是否具有您需要的功能。

**最低合格要求：**

- 使用零存取加密技術全程加密電子郵件帳戶資料。
- 匯出功能則為[Mbox](https://en.wikipedia.org/wiki/Mbox) 或[RFC5322](https://datatracker.ietf.org/doc/rfc5322) 標準的個別 .eml 。
- 允許使用者使用自己的 [網域名稱](https://en.wikipedia.org/wiki/Domain_name)。 自定網域名稱對用戶來說很重要，因為它允許用戶在使用服務時仍維持持自我代理，以防服務變差或被另一家不優先考慮隱私的公司收購。
- 在自有基礎設施上運作，即不建立在第三方電子郵件服務提供商之上。

**最佳案例：**

- 使用零存取加密帳戶全部資料（聯絡人、行事曆等）。
- 網頁郵件整合 E2EE/PGP加密以更方便使用。
- 支援 [WKD](https://wiki.gnupg.org/WKD) ，以改善透過HTTP發現公開的OpenPGP金鑰。 GnuPG 使用者可以透過輸入: `gpg --locate-key example_user@example.com` 取得金鑰。
- 支援外部使用者的臨時信箱。 當您想要發送加密的電子郵件時，這非常有用，而無需將實際副本發送給您的收件人。 這些電子郵件通常具有限定時效，之後會被自動刪除。 它們也不需要收件人配置任何像OpenPGP這樣的加密技術。
- 可提供 [onion 服務](https://en.wikipedia.org/wiki/.onion)的電子郵件服務供應商。
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- 為擁有自己網域的用戶提供通用地址或別名功能。
- 使用標準電子郵件存取協定，例如 IMAP、SMTP 或 [ JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol)。 標準存取協議確保客戶可以輕鬆下載所有電子郵件，一旦他們想切換到其它提供商。



### 隱私

我們希望所推薦的提供商盡可能少地收集客戶資料。

**最低合格要求：**

- 保護發件人的IP位址。 在 `Received` 標題欄位中過濾它。
- 除了使用者名稱和密碼外，不要求提供個人身份識別資訊(PII)。
- 隱私政策符合 GDPR 之要求。

**最佳案例：**

- 接受 [匿名付款選項](advanced/payments.md) （[加密貨幣](cryptocurrency.md)，現金，禮品卡等）
- 託管在有強力法律保障隱私的司法管轄區。



### 安全

電子郵件伺服器處理大量非常敏感的資料。 我們期望供應商採用行業最佳實踐來保護其會員。

**最低合格要求：**

- 使用 2FA 保護網頁郵件，如TOTP。
- 無存取的靜態加密，如零存取加密。 提供者沒有其所持有資料的解密金鑰。 這可以防止流氓員工外洩所存取的資料或遠程對手通過獲得對伺服器的未經授權的訪問來竊取資料。
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) 支持。
- 使用 [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) 或[Qualys SSL Labs](https://ssllabs.com/ssltest)等工具沒發現 TLS 錯誤或漏洞； 這包括與憑證相關的錯誤和弱 DH 參數，例如 [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) 錯誤。
- 伺服器套件偏好（在TLS v1.3上可選），適用於支持正向保密和已驗證加密的強大密碼套件。
- 有效的 [MTA-STS](https://tools.ietf.org/html/rfc8461) 和[TLS-RPT](https://tools.ietf.org/html/rfc8460) 政策。
- 有效 [ DANE ](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) 紀錄。
- 有效的 [SPF ](https://en.wikipedia.org/wiki/Sender_Policy_Framework) 和 [ DKIM ](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) 記錄。
- 擁有適當的 [DMARC ](https://en.wikipedia.org/wiki/DMARC) 記錄和原則，或使用 [ ARC ](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) 進行驗證。 如果正在使用 DMARC 驗證，則必須將原則設置為 `拒絕` 或 `隔離`。
- 伺服器套件最好為 TLS 1.2或更高版本以及 [ RFC8996](https://datatracker.ietf.org/doc/rfc8996)計劃。
- 假設使用SMTP，[SMTPS](https://en.wikipedia.org/wiki/SMTPS) 提交。
- 網站安全標準，例如： 
      - [HTTP 嚴格傳輸安全性](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 如果從外部網域加載東西時，[子資源完整性](https://en.wikipedia.org/wiki/Subresource_Integrity) 。
- 必須支援檢視 [訊息表頭](https://en.wikipedia.org/wiki/Email#Message_header)，因為它是確定電子郵件是否為網路釣魚嘗試的關鍵取證功能。

**最佳案例：**

- 支持硬體驗證，即 U2F 和 [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn)。 U2F 和 WebAuthn 更安全，因為它們使用儲存於客戶端硬體設備上的私鑰來驗證人員，而使用 TOTP 時共享祕密則直接儲存在網頁伺服器和客戶端。 再者 U2F 和 WebAuthn 更能抵抗網絡釣魚，因為它們的驗證回應是基於已驗證過的 [域名](https://en.wikipedia.org/wiki/Domain_name)。
- [DNS憑證授權機構授權(CAA)資源記錄](https://tools.ietf.org/html/rfc6844) 除了DANE支持。
- 實現 [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain)，這對於發佈郵件列表 [RFC8617](https://tools.ietf.org/html/rfc8617)非常有用。
- 漏洞獎勵計劃和/或協調漏洞披露過程。
- 網站安全標準，例如： 
      - [內容安全策略(CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)



### 信任

您不會把財務資料給身份作假的人，那麼為什麼會信任讓他們來使用您的電子郵件？ 我們要求我們推薦的供應商公開其所有權或領導層級狀況。 我們也希望看到頻繁的透明度報告，特別是關於如何處理政府要求的報告。

**最低合格要求：**

- 面向公眾的領導或所有權。

**最佳案例：**

- 面向公眾的領導
- 頻繁的透明度報告。



### 行銷

對於所推薦的電子郵件供應商，我們樂見其負責任的營銷。

**最低合格要求：**

- 必須自行託管分析 (不使用 Google Analytics、Adobe Analytics 等)。 供應商的網站還必須遵守 [DNT (Do Not Track, 請勿追蹤) ](https://en.wikipedia.org/wiki/Do_Not_Track) 的要求，以供選擇退出的人使用。

不得有任何不負責任的行銷：

- 宣稱破解不了的加密 使用加密時應意識到，當有一天技術足以破解它時，它就不再是祕密的。
- 保證 100% 匿名性保護。 當有人聲稱某件事是100 ％時，這意味著失敗沒有確定性。 我們知道人們可以很容易地以多種方式去匿名化自己，例如：
  
      - 重覆使用個人資訊 (如電子郵件帳戶、獨特的假名等等 pseudonyms, etc.) 而沒透過匿名軟體 (如 Tor, VPN 之類)。
    - [瀏覽器指紋](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**最佳案例：**

- 清晰易讀的文件。 這包括諸如設置 2FA 、電子郵件客戶端、OpenPGP等。



### 附加功能

雖然不是嚴格要求，但我們在決定推薦哪些提供商時還會考慮其他一些便利或隱私因素。
