---
title: 電子郵件伺服器
meta_title: "自行託管電子郵件 - Privacy Guides"
icon: material/email
description: 對於技術性較高的讀者而言，自行託管您自己的電子郵件可以透過最大限度地控制您的資料，提供額外的隱私權保證。
cover: email.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務供應商](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

進階的系統管理員可以考慮自行架設**電子郵件伺服器**。 郵件伺服器需要關注與持續維護，以確保安全性和郵件傳遞的可靠性。 除了下列「all-in-one」解決方案外，我們也挑選了涵蓋較為手動的幾篇文章：

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide) (August 2017)

## Stalwart

<div class="admonition recommendation" markdown>

![Stalwart 圖示](../assets/img/self-hosting/stalwart.svg){ align=right }

**Stalwart** 是用 Rust 寫成的新款郵件伺服器，除了標準的 IMAP、POP3 和 SMTP 外，還支援 JMAP。 它有多種設定選項，而且預設設定在安全性和功能性方面都非常合理，很容易立即使用。 它還有網頁管理介面，支援 TOTP 2FA，並允許您輸入 PGP 公鑰以加密**所有**來信。

[:octicons-home-16: 首頁](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="捐款" }

</div>

Stalwart 的 [PGP 實作](https://stalw.art/docs/encryption/overview) 在我們的自架推薦清單中是獨一無二的，可讓您以零知識的訊息儲存空間方式來架設自己的郵件伺服器。 如果您還想在您的網域上另外設定 Web Key Directory（WKD），以及使用支援 PGP 和 WKD 的電子郵件用戶端（例如 Thunderbird）來寄信，那麼這是最簡單就能讓所有 [Proton Mail](../email.md#proton-mail) 使用者能取得自架 E2EE 相容性的方式。

Stalwart **沒有**內建的網頁郵件功能，因此您需要使用[電子郵件軟體](../email-clients.md)使用，或是另外架設一套開放原始碼的網頁郵件軟體，例如 Nextcloud 的 Mail 應用程式。

我們在 _Privacy Guides_ 使用 Stalwart 作為內部電子郵件服務。

## Mailcow

<div class="admonition recommendation" markdown>

![Mailcow 圖示](../assets/img/self-hosting/mailcow.svg){ align=right }

**Mailcow** 是一套進階的郵件伺服器，非常適合有 Linux 經驗的人使用。 它透過 Docker 容器提供您所需的一切：支援 DKIM 的郵件伺服器、防毒與垃圾郵件監控、透過 SOGo 提供網頁郵件與 ActiveSync，以及支援 2FA 的網頁管理系統。

[:octicons-home-16: 首頁](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="原始碼" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="捐款" }

</div>

## Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box 圖示](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** 是在 Ubuntu 上部署郵件伺服器的自動設定指令碼。 它的目標是讓人們能更容易自行架設郵件伺服器。

[:octicons-home-16: 首頁](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="原始碼" }

</div>
