---
meta_title: "최고의 비공개 및 보안 클라우드 스토리지 제공 업체 - Privacy Guides"
title: "클라우드 스토리지"
icon: material/file-cloud
description: 대부분의 클라우드 스토리지 제공 업체는, 업체가 사용자의 파일을 보지 않을 것이라는 믿음이 필수적입니다. 프라이버시 보호 대체제를 소개합니다!
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: 수동적 공격(Passive Attacks)](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공자/제공 업체(Service Providers)](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. The alternatives listed below eliminate the need for trust by implementing secure end-to-end encryption.

이러한 대안들이 여러분의 요구에 맞지 않는 경우, 다른 클라우드 제공 업체를 [Cryptomator](encryption.md#cryptomator-cloud) 등의 암호화 소프트웨어와 함께 사용할 것을 권장합니다. **어떤** 클라우드 제공 업체든(본 목록 포함), Cryptomator를 함께 사용함으로써 제공 업체의 기본 클라이언트에서 발생할 수 있는 암호화 결함 위험성을 낮출 수 있습니다.

<details class="admonition info" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail).

The initial free storage is limited to 2 GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5 GB.

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: Windows](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit 로고](assets/img/cloud/tresorit.svg){ align=right }

**Tresorit**은 2011년에 설립된 스위스-헝가리의 암호화 클라우드 스토리지 제공 업체입니다. Tresorit은 스위스 국영 우편 서비스인 스위스 포스트(스위스 우체국)가 소유하고 있습니다.

[:octicons-home-16: Homepage](https://tresorit.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.tresorit.mobile)
- [:simple-appstore: App Store](https://apps.apple.com/app/id722163232)
- [:fontawesome-brands-windows: Windows](https://tresorit.com/download)
- [:simple-apple: macOS](https://tresorit.com/download)
- [:simple-linux: Linux](https://tresorit.com/download)

</details>

</div>

Tresorit has received a number of independent security audits:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - 해당 검토에서는 Tresorit 웹 클라이언트, Android/Windows 앱 및 관련 인프라 보안을 평가했습니다.
    - Computest는 취약점을 2개 발견했으며, 이 취약점은 해결되었습니다.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - 해당 검토에서는 Tresorit의 전체 소스 코드를 분석하여, Tresorit [백서](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf)에서 설명한 개념과 구현이 일치하는지 검증했습니다.
    - Ernst & Young additionally tested the web, mobile, and desktop clients. They concluded:

        > Test results found no deviation from Tresorit’s data confidentiality claims.

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private.

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos is built on top of the [InterPlanetary File System (IPFS)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

### 최소 요구 사항

- Must enforce E2EE.
- 테스트용 무료 요금제/체험판 기간을 제공해야 합니다.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- 기본적인 파일 관리 기능을 지원하는 웹 인터페이스를 제공해야 합니다.
- 모든 파일/문서를 쉽게 내보낼 수 있어야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Clients should be open source.
- Clients should be audited in their entirety by an independent third party.
- Linux, Android, Windows, macOS, iOS 네이티브 클라이언트를 제공해야 합니다.
    - 클라이언트는 운영체제에서 기본으로 제공하는 클라우드 스토리지 서비스용 툴과 통합되어야 합니다. 예시: iOS '파일' 앱 연동, Android DocumentsProvider 기능 등
- Should support easy file sharing with other users.
- 웹 인터페이스에서 최소한 기본적인 파일 미리보기 및 편집 기능을 제공해야 합니다.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 준수는 회사의 [정보 보안 관리 시스템](https://en.wikipedia.org/wiki/Information_security_management)과 연관되며 클라우드 서비스의 판매, 개발, 유지 관리 및 지원에 적용됩니다.
