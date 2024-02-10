---
meta_title: "最高のプライベートで安全なクラウドストレージ プロバイダー - Privacy Guides"
title: "クラウドストレージ"
icon: material/file-cloud
description: Many cloud storage providers require your trust that they will not look at your files. これらはプライベートな選択肢です！
cover: cloud.webp
---

多くのクラウドストレージプロバイダーの場合、これを使用する際には、プロバイダーがファイルを閲覧することはないだろうと、プロバイダーを完全に信頼することが求められます。 以下に示す選択肢では、安全なE2EEが実装されているため、サービス提供元を信頼する必要はありません。

If these alternatives do not fit your needs, we suggest you look into using encryption software like [Cryptomator](encryption.md#cryptomator-cloud) with another cloud provider. Using Cryptomator in conjunction with **any** cloud provider (including these) may be a good idea to reduce the risk of encryption flaws in a provider's native clients.

<details class="TYPE" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](productivity.md) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive ロゴ](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive**は、人気の暗号化電子メールプロバイダーである[Proton Mail](email.md#proton-mail)が提供する、スイスの暗号化クラウドストレージ プロバイダーです。

[:octicons-home-16: Homepage](https://proton.me/drive){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:simple-windows11: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

Proton Driveのウェブアプリケーションは、[2021](https://proton.me/blog/security-audit-all-proton-apps)年にSecuritumにより独立の監査を受けています。完全な詳細は公開されませんでしたが、Securitumの認証状態は以下の通りです。

> 監査人は、2つの深刻度の低い脆弱性を特定しました。 また、5つの一般的な勧告を行いました。 同時に、ペンテストに際して重要なセキュリティ上の問題が特定されなかったことを確認しました。

Proton Driveの新しいモバイルクライアントは、まだ第三者による公的な監査を受けていません。

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit ロゴ](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit**は、2011年に設立された、スイスとハンガリーの暗号化クラウドストレージ プロバイダーです。 Tresoritはスイスの国営郵便局であるスイスポストが所有しています。

[:octicons-home-16: Homepage](https://tresorit.com/){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com/hc/en-us){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id722163232)
- [:simple-windows11: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit has received a number of independent security audits:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification/): ISO/IEC 27001:2013[^1] Compliance [Certification](https://www.certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security/): Penetration Testing by Computest
    - This review assessed the security of the Tresorit web client, Android app, Windows app, and associated infrastructure.
    - Computest discovered two vulnerabilities which have been resolved.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture/): Penetration Testing by Ernst & Young.
    - This review analyzed the full source code of Tresorit and validated that the implementation matches the concepts described in Tresorit's [white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf).
    - Ernst & Young additionally tested the web, mobile, and desktop clients: "Test results found no deviation from Tresorit’s data confidentiality claims."

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://www.swiss-digital-initiative.org/digital-trust-label/) which requires passing [35 criteria](https://digitaltrust-label.swiss/criteria/) related to security, privacy, and reliability.

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

私たちは、サイトの各項目に関して、定義された規準の確立に取り組んでいます。この規準は変更される可能性があります。 規準について疑問がある場合は、[フォーラムで質問](https://discuss.privacyguides.net/latest)してください。また、ここに記載されていない場合でも、私たちがプロジェクトを推奨する際に、そうした事柄を考慮しなかったと仮定するのはお止めください。 プロジェクトを推奨する際に考慮され、議論される要素は多くあり、そのすべてを文書化する作業は現在進行中です。

</div>

### 最低要件

- Must enforce end-to-end encryption.
- Must offer a free plan or trial period for testing.
- Must support TOTP or FIDO2 multi-factor authentication, or Passkey logins.
- Must offer a web interface which supports basic file management functionality.
- Must allow for easy exports of all files/documents.
- 標準的な監査済みの暗号化を使用すること。

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- Clients should be open source.
- Clients should be audited in their entirety by an independent third-party.
- Should offer native clients for Linux, Android, Windows, macOS, and iOS.
    - These clients should integrate with native OS tools for cloud storage providers, such as Files app integration on iOS, or DocumentsProvider functionality on Android.
- Should support easy file-sharing with other users.
- Should offer at least basic file preview and editing functionality on the web interface.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 compliance relates to the company's [information security management system](https://en.wikipedia.org/wiki/Information_security_management) and covers the sales, development, maintenance and support of their cloud services.
