---
title: "Pastebins"
icon: material/content-paste
description: These tools allow you to have full control of any pasted data you share to other parties.
cover: pastebins.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

[**Pastebins**](https://en.wikipedia.org/wiki/Pastebin) are online services most commonly used to share large blocks of code in a convenient and efficient manner. The pastebins listed here employ client-side encryption and password protection for pasted content; both of these features prevent the website or server operator from reading or accessing the contents of any paste.

## PrivateBin

<div class="admonition recommendation" markdown>

![PrivateBin logo](assets/img/pastebins/privatebin.svg){ align=right }

**PrivateBin** is a minimalist, open-source, online pastebin where the server cannot decrypt and read any pasted data you submit. 데이터는 브라우저에서 AES-256으로 암호화/복호화됩니다. ZeroBin을 개선한 버전의 서비스이기도 합니다.

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

## 평가 기준 { #criteria }

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항

- 오픈 소스여야 합니다.
- Must encrypt pasted data on the client side before it is sent to the server.
- 파일을 비밀번호로 보호하는 기능을 지원해야 합니다

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Should have a published audit from a reputable, independent third party.
