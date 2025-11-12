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

Stalwart's [PGP implementation](https://stalw.art/docs/encryption/overview) is unique among our self-hosted recommendations and allows you to operate your own mail server with zero-knowledge message storage. If you additionally configure Web Key Directory (WKD) on your domain, and if you use an email client which supports PGP and WKD for outgoing mail (like Thunderbird), then this is the easiest way to get self-hosted E2EE compatibility with all [Proton Mail](../email.md#proton-mail) users.

Stalwart does **not** have an integrated webmail, so you will need to use it with a [dedicated email client](../email-clients.md) or find an open-source webmail to self-host, like Nextcloud's Mail app.

We use Stalwart for our own internal email at _Privacy Guides_.

## Mailcow

<div class="admonition recommendation" markdown>

![Mailcow 圖示](../assets/img/self-hosting/mailcow.svg){ align=right }

**Mailcow** is an advanced mail server perfect for those with Linux experience. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: 首頁](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="原始碼" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="捐款" }

</div>

## Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box 圖示](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.

[:octicons-home-16: 首頁](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="原始碼" }

</div>
