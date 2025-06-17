---
title: "Pastebins"
icon: material/content-paste
description: These tools allow you to have full control of any pasted data you share to other parties.
cover: pastebins.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

[**Pastebins**](https://en.wikipedia.org/wiki/Pastebin) are online services most commonly used to share large blocks of code in a convenient and efficient manner. The pastebins listed here employ client-side encryption and password protection for pasted content; both of these features prevent the website or server operator from reading or accessing the contents of any paste.

## PrivateBin

<div class="admonition recommendation" markdown>

![PrivateBin logo](assets/img/pastebins/privatebin.svg){ align=right }

**PrivateBin** is a minimalist, open-source, online pastebin where the server has zero knowledge of pasted data. Data is encrypted/decrypted in the browser using 256-bit AES. PrivateBinはZeroBinの改良版です。

[:octicons-home-16: Homepage](https://privatebin.info){ .md-button .md-button--primary }
[:octicons-server-16:](https://privatebin.info/directory){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

</div>

## Paaster

<div class="admonition recommendation" markdown>

![Paaster logo](assets/img/pastebins/paaster.svg){ align=right }

**Paaster** is a secure and user-friendly pastebin application that prioritizes privacy and simplicity. With end-to-end encryption and paste history, Paaster ensures that your pasted code remains confidential and accessible.

[:octicons-home-16: Homepage](https://paaster.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://paaster.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/WardPearce/paaster#security){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/WardPearce/paaster){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/WardPearce){ .card-link title="Contribute" }

</div>

## 規準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- オープンソースであること。
- Must implement "zero-trust" E2EE.
- パスワードで保護されたファイルをサポートすること。

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- Should have a published audit from a reputable, independent third party.
