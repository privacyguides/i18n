---
meta_title: "加密私人電子郵件建議 - Privacy Guides"
title: "電子郵件服務"
icon: material/email
description: 這些電子郵件提供商提供了一個好地方來安全的儲存您的電子郵件，也有不少能與其他供應商相互操作的 OpenPGP 加密。
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

電子郵件實際上是使用任何線上服務的必需品，但我們不建議把它應用於人與人之間的對話。 與其使用電子郵件聯繫他人，不如考慮使用支援前向保密的即時通訊媒介。

[推薦的即時通訊工具](real-time-communication.md ""){.md-button}

## 推薦的提供商

除此之外，我們還推薦各種基於可持續商業模式和內建安全和隱私功能的電子郵件提供商。 閱讀我們[完整的標準清單](#criteria)，瞭解更多資訊。

| 供應商                         | OpenPGP / WKD                          | IMAP / SMTP                                       | 零存取加密                                             | 匿名付款方式                       |
| --------------------------- | -------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ---------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } 僅提供付費版 | :material-check:{ .pg-green }                     | 現金                           |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                     | :material-information-outline:{ .pg-blue } 限 Mail | 現金                           |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }            | :material-check:{ .pg-green }                     | 透過第三方支付 Monero<br> 或現金 |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. 除此之外，這些服務有助於保護真實收件匣免受垃圾郵件的侵害，防止行銷人員關聯您的帳戶，並使用 PGP 加密所有傳入的訊息。

- [更多資訊 :material-arrow-right-drop-circle:](email-aliasing.md)

## OpenPGP 兼容服務

這些供應商原生支援 OpenPGP 加/解密 和 [WKD 標準](basics/email-security.md#what-is-the-web-key-directory-standard)，可提供跨供應商 E2EE 的電子郵件。 例如， Proton Mail 用戶可以向 Mailbox.org 用戶發送 E2EE 消息，或者您可以從它支援的網際網路服務接收 OpenPGP 加密通知。

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

當使用像 OpenPGP 這類 E2EE 技術時，電子郵件仍然會有一些元數據無法加密如主旨列。 了解更多[電子郵件元數據](basics/email-security.md#email-metadata-overview).

OpenPGP 也不支援前向保密 (forward secrecy)，這表示如果您或訊息接收者的私鑰被竊，則之前使用該金鑰加密的所有訊息都會曝光。

- [如何保護我的私鑰？](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** 是一個專注於隱私、加密、安全性和易用性的電子郵件服務。 他們自 2013 年起開始營運。 Proton AG 的總部位於瑞士日內瓦。

Proton 免費方案提供 500 MB 的郵件儲存空間，您可以免費增加至 1 GB。

[:octicons-home-16: 首頁](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="文檔" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: 網頁版](https://mail.proton.me)

</details>

</div>

免費帳戶有一些功能限制，例如無法搜尋郵件正文內容，也無法使用 [Proton Mail Bridge](https://proton.me/mail/bridge)；後者是使用 [建議的桌面郵件客戶端](email-clients.md) （例如 Thunderbird） 所需的。 付費帳戶包括 Proton Mail Bridge、額外儲存空間和自訂網域支援等功能。 如果您有訂閱 Proton Unlimited 或任何多使用者的 Proton 方案，您也可以免費獲得 [SimpleLogin](email-aliasing.md#simplelogin) Premium。

Proton Mail 應用程式於 2021 年 11 月 9 日由 [Securitum](https://research.securitum.com) 提供[認證函](https://proton.me/blog/security-audit-all-proton-apps) 。

Proton Mail 的內容崩潰報告**不會**對其它第三方分享。 可以在 web app 下取消，作法: :gear: → **所有設定** → **帳號** → **安全與隱私** → **隱私與資料蒐集**.

#### :material-check:{ .pg-green } 自訂域名和別名

付費的 Proton Mail 訂閱者可以使用自定網域服務或 [通用電子郵件](https://proton.me/support/catch-all) 功能。 Proton Mail 還支援 [子位址](https://proton.me/support/creating-aliases)，這對於不想購買網域的人很有用。

#### :material-check:{ .pg-green } 私密付款方式

Proton Mail 除了 [支援](https://proton.me/support/payment-options) 郵寄**現金**外，還接受信用卡/簽帳金融卡、[比特幣](advanced/payments.md#other-coins-bitcoin-ethereum-etc) 和 PayPal 付款。

#### :material-check:{ .pg-green } 帳號安全

Proton Mail 支援使用 TOTP 作為 [雙重要素驗證](https://proton.me/support/two-factor-authentication-2fa)，以及使用 FIDO2 或 U2F 標準的[硬體安全金鑰](https://proton.me/support/2fa-security-key)。 使用硬體安全金鑰需要先設定 TOTP 雙重要素驗證。

#### :material-check:{ .pg-green } 資料安全

Proton Mail 使用「[零存取加密技術](https://proton.me/blog/zero-access-encryption)」來保護電子郵件和[行事曆](https://proton.me/news/protoncalendar-security-model)的資料安全。 使用「零存取加密技術」保護的數據只能由您訪問。

儲存在 [Proton 通錄](https://proton.me/support/proton-contacts)中的某些資訊，例如顯示名稱和電子郵件位址，並未使用零存取加密進行保護。 支援零存取加密的聯絡人欄位(例如電話號碼)會以掛鎖圖示顯示。

#### :material-check:{ .pg-green } 電子郵件加密

Proton Mail 網頁郵件整合了 [OpenPGP 加密](https://proton.me/support/how-to-use-pgp) 。 發送到其他 Proton Mail 帳號的電子郵件會自動加密，並且可以在您的帳號設定中輕鬆啟用「使用 OpenPGP 金鑰對非 Proton Mail 位址進行加密」。 Proton 也支援使用 WKD 自動獲取外部金鑰。 因此發送到其他同樣使用 WKD 的供應商的電子郵件也將使用 OpenPGP 自動加密，無需與聯絡人手動交換 PGP 公鑰。 它們也允許您[在沒有 OpenPGP 的情況下，為寄給非 Proton Mail 郵箱的郵件加密](https://proton.me/support/password-protected-emails)，而不需要他們註冊 Proton Mail 帳戶。

Proton Mail 也透過 HTTP 從其 WKD 發布 Proton 帳戶的公鑰。 這可讓不使用 Proton Mail 的人輕鬆找到 Proton Mail 帳號的 OpenPGP 金鑰，以進行跨供應商 E2EE。 這只適用於以 Proton 自家網域結尾的電子郵件地址，例如：`@proton.me`。 如果使用自訂網域，則必須另行[設定 WKD](basics/email-security.md#what-is-the-web-key-directory-standard)。

#### :material-information-outline:{ .pg-blue } 終止帳號

若您的付費帳戶逾期 14 天[未付款](https://proton.me/support/delinquency)，您將無法讀取自己的資料。 30 天後，您的帳戶將標記為欠費狀態，無法再收取郵件。 在此期間，您將繼續收到帳單。 Proton 會[刪除六個月未登入使用的免費帳戶](https://proton.me/support/inactive-accounts) 。 **不能**重複使用已停用帳號的電子郵件位址。

#### :material-information-outline:{ .pg-blue } 額外功能

Proton Mail 的[Unlimited](https://proton.me/support/proton-plans#proton-unlimited)計劃除了提供多個自訂網域、無限的電子郵件別名和 500 GB 儲存空間外，還可使用其他 Proton 服務。

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org**是一個專注於安全、無廣告、100% 採用環保能源的電子郵件服務。 自 **2014 年** 開始運營。 Mailbox.org  總部位於德國柏林。

帳戶一開始最多只有 2 GB 儲存空間，可視需要升級。

[:octicons-home-16: 首頁](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="說明文件" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:octicons-browser-16: 網頁版](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } 自訂域名和別名

Mailbox.org 可使用自定域名，且支援 [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) 位址。 Mailbox.org 也支援[子位址](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it)，如果您不想購買網域，這非常有用。

#### :material-check:{ .pg-green } 私人付款方式

Mailbox.org 不接受任何加密貨幣，因為他們的支付處理商 BitPay 暫停了德國業務。 不過，他們接受郵寄**現金**、使用**現金**支付至銀行帳戶、銀行轉帳、信用卡、PayPal，以及幾家德國特定的處理商：Paydirekt 和 Sofortüberweisung。

#### :material-check:{ .pg-green } 帳號安全

Mailbox.org 僅對其網頁郵件提供[雙重要素驗證](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa)。 您可以使用 TOTP 或通過 [YubiKey](https://en.wikipedia.org/wiki/YubiKey) 來使用 [YubiCloud](https://yubico.com/products/services-software/yubicloud) 進行雙重認證. Web 標準如[WebAuthn ](basics/multi-factor-authentication.md#fido-fast-identity-online)等尚不支援。

#### :material-information-outline:{ .pg-blue } 資料安全

Mailbox.org 允許使用 [加密郵箱](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox)對傳入郵件進行加密。 收到的新訊息將立即用您的公鑰加密。

不過，Mailbox.org 所使用的軟體平台[Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange)，[並不支援](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book)對您的通訊錄和行事曆進行加密。 [獨立的選項](calendar.md) 可能更適合此類資料。

#### :material-check:{ .pg-green } 電子郵件加密

Mailbox.org 在他們的網頁郵件中 [整合了加密功能](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) ，這簡化了向具有公開OpenPGP金鑰的人發送訊息。 它們也讓遠端收件者可以在 Mailbox.org 的伺服器上[解密電子郵件](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp)。 當遠端收件人沒有 OpenPGP 無法解密自己郵箱中的電子郵件時，此功能非常有用。

Mailbox.org 也支援透過 HTTP 從其 WKD 發現公共金鑰。 這可讓非 Mailbox 使用者輕鬆找到 Mailbox 帳戶的 OpenPGP 金鑰，以進行跨供應商 E2EE。 這只適用於以 Mailbox.org 自身網域結尾的電子郵件地址，例如：`@mailbox.org`。 如果使用自訂網域，則必須另行[設定 WKD](basics/email-security.md#what-is-the-web-key-directory-standard)。

#### :material-information-outline:{ .pg-blue } 終止帳號

當合約結束時，帳戶將被設定為受限使用者帳戶。 [30天](https://kb.mailbox.org/en/private/ payment-article/what-happens-at-the-end-of-my-contract)後，它會被不可回復地刪除。

#### :material-information-outline:{ .pg-blue } 額外功能

可利用他們的[洋蔥服務](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org)與 IMAP/SMTP 協議來訪問 Mailbox.org 帳戶。 不過，他們的網頁郵件介面無法透過其 .onion 服務存取，而且您可能會遇到 TLS 憑證錯誤。

所有帳號都附帶有限的[可以加密](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive)雲端儲存空間 。 Mailbox.org 還提供別名 [@ secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely)，它對郵件伺服器之間的連線強制進行TLS加密，否則根本不會發送訊息。 Mailbox.org 除了支援 IMAP 和 POP3 等標準存取通訊協議外，還支援 [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) 。

Mailbox.org 所有方案都提供了數位遺產功能。 只要繼承人提出申請並提供您的遺囑即可獲得你選擇要傳給他們的資料。 或者，您可以透過姓名和位址提出人選。

## 更多供應商

這些提供商以零知識加密方式儲存您的電子郵件，使其成為保護儲存電子郵件安全的絕佳選擇。 但是，它們不支援供應商之間可相互操作 E2EE 通信的加密標準。

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta 標誌](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta 標誌](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (前身為 *Tutanota*) 是一項透過使用加密技術，著重於安全性與隱私權的電子郵件服務。 Tuta 自 2011 年開始營運，總部位於德國漢諾威。

免費帳戶的起始儲存容量為 1 GB。

[:octicons-home-16: 首頁](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="原始碼" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: 網頁版](https://app.tuta.com)

</details>

</div>

Tuta 不支援 [ IMAP 協議](https://tuta.com/support#imap) 或使用第三方 [電子郵件客戶端](email-clients.md)，您也無法將 [外部電子郵件帳戶](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) 添加到 Tuta 應用程式。 目前不支援[匯入電子郵件](https://github.com/tutao/tutanota/issues/630) ，但這點很快就[會改善](https://tuta.com/blog/kickoff-import)。 電子郵件可以單個 [或選擇資料夾批量](https://tuta.com/support#generalMail)匯出 ，但若您有許多資料夾，可能會不方便。

#### :material-check:{ .pg-green } 自訂域名和別名

付費的 Tuta 帳戶可以根據其方案使用 15 或 30 個別名，並且在[自訂域名](https://tuta.com/support#custom-domain)上可以使用無限個別名。 Tuta 不允許使用[子位址 (加號位址)](https://tuta.com/support#plus)，但您可以在自訂域名上使用[接收所有郵件](https://tuta.com/support#settings-global)功能。

#### :material-information-outline:{ .pg-blue } 私密付款方式

Tuta 僅接受信用卡和 PayPal ，但 [**加密貨幣**](cryptocurrency.md) 可用於通過其[合作伙伴](https://tuta.com/support/#cryptocurrency) Proxystore 購買禮品卡。

#### :material-check:{ .pg-green } 帳號安全

Tuta 支援 TOTP 或 U2F 的[雙重認證](https://tuta.com/support#2fa)。

#### :material-check:{ .pg-green } 資料安全

Tuta 對您的電子郵件、[通訊錄聯絡人](https://tuta.com/support#encrypted-address-book)和[行事曆](https://tuta.com/support#calendar) [進行零存取加密](https://tuta.com/support#what-encrypted)。 這意味著儲存在您帳戶中的訊息和其他資料只有您能讀取。

#### :material-information-outline:{ .pg-blue } 電子郵件加密

Tuta [不使用 OpenPGP ](https://tuta.com/support/#pgp)。 只能透過 [臨時 Tuta 郵箱](https://tuta.com/support/#encrypted-email-external)，才能接收非Tuta 電子郵件帳戶寄出的加密電子郵件。

#### :material-information-outline:{ .pg-blue } 終止帳號

Tuta [刪除六個月未登入使用的免費帳戶](https://tuta.com/support#inactive-accounts) 。 付費後，可以重用激活已停用的免費帳戶。

#### :material-information-outline:{ .pg-blue } 額外功能

Tuta 向非營利組織提供免費 [商業版本](https://tuta.com/blog/secure-email-for-non-profit) 或大幅折扣。

## 標準

**請注意，我們與以下推薦的任何供應商並無瓜葛。** 除了 [我們的條件標準](about/criteria.md)外，我們還為任何希望獲得推薦的電子郵件供應商制定了一套明確要求，包括實施業界最佳做法，現代技術等。 我們建議您在選擇電子郵件提供商之前熟悉此列表，並進行自己的研究，以確保您選擇的電子郵件提供商是您的正確選擇。

### 技術

我們認為這些功能很重要，以便提供安全和最佳的服務。 您應該考慮提供商是否具有您需要的功能。

**最低合格要求：**

- 必須使用零存取加密技術加密電子郵件帳戶資料。
- 必須能夠以 [Mbox](https://en.wikipedia.org/wiki/Mbox) 或符合 [RFC5322](https://datatracker.ietf.org/doc/rfc5322) 標準的個別 .EML 匯出電子郵件。
- 允許使用者使用自己的[網域名稱](https://en.wikipedia.org/wiki/Domain_name)。 自定網域名稱對用戶來說很重要，因為它允許用戶在使用服務時仍維持持自我代理，以防服務變差或被另一家不優先考慮隱私的公司收購。
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**最佳情況：**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- 支援外部使用者的臨時信箱。 This is useful when you want to send an encrypted email without sending an actual copy to your recipient. 這些電子郵件通常具有限定時效，之後會被自動刪除。 它們也不需要收件人配置任何像OpenPGP這樣的加密技術。
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). 自定網域名稱對用戶來說很重要，因為它允許用戶在使用服務時仍維持持自我代理，以防服務變差或被另一家不優先考慮隱私的公司收購。
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### 隱私

我們希望所推薦的供應商收集越少資料越好。

**最低合格要求：**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**最佳情況：**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### 安全

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**最低合格要求：**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. 提供者沒有其所持有資料的解密金鑰。 這可防止惡意員工洩露他們存取的資料，或遠端敵人透過未經授權存取伺服器來釋放他們竊取的資料。
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) 支援。
- 使用 [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) 或 [Qualys SSL Labs](https://ssllabs.com/ssltest) 等工具沒發現 TLS 錯誤或漏洞； 這包括與憑證相關的錯誤和弱 DH 參數，例如 [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)) 錯誤。
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- 有效的 [MTA-STS](https://tools.ietf.org/html/rfc8461) 和[TLS-RPT](https://tools.ietf.org/html/rfc8460) 政策。
- 有效 [ DANE ](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) 紀錄。
- 有效的 [SPF ](https://en.wikipedia.org/wiki/Sender_Policy_Framework) 和 [ DKIM ](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) 記錄。
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. 如果正在使用 DMARC 驗證，則必須將原則設定為 `拒絕` 或 `隔離`。
- 伺服器套件最好為 TLS 1.2或更高版本以及 [ RFC8996](https://datatracker.ietf.org/doc/rfc8996)計劃。
- 假設使用SMTP，[SMTPS](https://en.wikipedia.org/wiki/SMTPS) 提交。
- 網站安全標準，例如：
    - [HTTP 嚴格傳輸安全性](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - 如果從外部網域加載東西時，[子資源完整性](https://en.wikipedia.org/wiki/Subresource_Integrity) 。
- 必須支援檢視[郵件標頭](https://en.wikipedia.org/wiki/Email#Message_header)，因為這是判斷電子郵件是否為釣魚嘗試的重要取證功能。

**最佳情況：**

- Should support hardware authentication, i.e. U2F 和 [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online)。
- [DNS 憑證授權機構授權 (CAA) 資源記錄](https://tools.ietf.org/html/rfc6844) 除了 DANE 支援外。
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- 漏洞獎勵計劃和/或協調漏洞披露過程。
- 網站安全標準，例如：
    - [內容安全策略(CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### 信任

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? 我們要求推薦的供應商公開其所有權或領導層級狀況。 我們也希望能夠看到經常性的透明度報告，尤其是如何處理政府要求的部份。

**最低合格要求：**

- 面向公眾的領導或所有權。

**最佳情況：**

- 頻繁的透明度報告。

### 行銷

With the email providers we recommend, we like to see responsible marketing.

**最低合格要求：**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [瀏覽器指紋](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**最佳情況：**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### 附加功能

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
