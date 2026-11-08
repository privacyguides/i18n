---
meta_title: "أفضل خدمات التخزين السحابي من حيث الخصوصية والأمان - Privacy Guides"
title: التخزين السحابي
icon: material/file-cloud
description: تتطلب منك كثير من خدمات التخزين السحابي أن تثق بأنها لن تطلع على ملفاتك. إليك بدائل تحافظ على خصوصيتك!
cover: cloud.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-bug-outline: الهجمات السلبية](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: مزودو الخدمات](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

تتطلب منك كثير من **خدمات التخزين السحابي** أن تثق بها تماما وألّا تطلع على ملفاتك. البدائل المذكورة أدناه تُغنيك عن الحاجة إلى الثقة بمزود الخدمة، لأنها تستخدم تشفير End-to-End Encryption الآمن.

إذا لم تناسبك هذه البدائل، فننصحك باستخدام برنامج تشفير مثل [Cryptomator](encryption.md#cryptomator-cloud) مع خدمة تخزين سحابي أخرى. قد يكون استخدام Cryptomator مع **أي** خدمة تخزين سحابي (بما فيها الخدمات المذكورة هنا) فكرة جيدة لتقليل مخاطر وجود ثغرات في التشفير داخل تطبيقات مزوّد الخدمة نفسها.

<details class="admonition info" markdown>
<summary>هل تبحث عن Nextcloud؟</summary>

للقراء الأكثر خبرة بالتقنية، [ما زلنا نوصي](self-hosting/file-management.md#nextcloud) باستخدام Nextcloud لاستضافة مجموعة أدوات لإدارة الملفات على خادم خاص بك. لكننا لا نوصي حاليا بخدمات التخزين التي توفرها جهات خارجية باستخدام Nextcloud، لأننا [لا ننصح](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) المستخدمين المنزليين بالاعتماد على ميزة End-to-End Encryption المدمجة فيه.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/images/cloud/protondrive.svg){ align=right }

خدمة **Proton Drive** هي خدمة تخزين سحابي مشفرة تقدمها الشركة نفسها التي توفر خدمة البريد الإلكتروني المشفر الشهيرة [Proton Mail](email.md#proton-mail).

تقتصر مساحة التخزين المجانية في البداية على 2 جيجابايت، لكن يمكنك الحصول على مساحة إضافية تصل إلى 5 جيجابايت بعد إكمال [بعض الخطوات](https://proton.me/support/more-free-storage-existing-users).

[:octicons-home-16: Homepage](https://proton.me/drive){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/drive/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/drive){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.drive)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1509667851)
- [:fontawesome-brands-windows: وندوز](https://proton.me/drive/download)
- [:simple-apple: macOS](https://proton.me/drive/download)

</details>

</div>

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source), but the brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit logo](assets/images/cloud/tresorit.svg){ align=right }

**Tresorit** is a Swiss-Hungarian encrypted cloud storage provider founded in 2011. Tresorit is owned by the Swiss Post, the national postal service of Switzerland.

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
    - This review assessed the security of the Tresorit web client, Android app, Windows app, and associated infrastructure.
    - Computest discovered two vulnerabilities which have been resolved.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - This review analyzed the full source code of Tresorit and validated that the implementation matches the concepts described in Tresorit's [white paper](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf).
    - Ernst & Young additionally tested the web, mobile, and desktop clients. They concluded:

        > Test results found no deviation from Tresorit’s data confidentiality claims.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/images/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, view, and edit their photos, videos, documents, etc.

Peergos secures your files with quantum-resistant E2EE and ensures all data about your files remains private. It is also [self-hostable](https://book.peergos.org/features/self).

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/peergos/peergos#support){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=peergos.android)
- [:simple-github: GitHub](https://github.com/Peergos/web-ui/releases)
- [:fontawesome-brands-windows: Windows](https://peergos.org/download#windows)
- [:simple-apple: macOS](https://peergos.org/download#macos)
- [:simple-linux: Linux](https://peergos.org/download#linux)
- [:octicons-browser-16: Web](https://peergos.net)

</details>

</div>

Peergos is built on top of the [InterPlanetary File System (IPFS)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

The client, server, and command line interface for Peergos all run from the same binary. Additionally, Peergos includes a [sync engine](https://book.peergos.org/features/sync) (accessible via the native apps) for bi-directionally synchronizing a local folder with a Peergos folder, and a [webdav bridge](https://book.peergos.org/features/webdav) to allow other applications to access your Peergos storage. You can refer to Peergos's documentation for a full overview of their numerous features.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Must enforce E2EE.
- Must offer a free plan or trial period for testing.
- Must support TOTP or FIDO2 multifactor authentication, or passkey logins.
- Must offer a web interface which supports basic file management functionality.
- Must allow for easy exports of all files/documents.

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Clients should be open source.
- Clients should be audited in their entirety by an independent third party.
- Should offer native clients for Linux, Android, Windows, macOS, and iOS.
    - These clients should integrate with native OS tools for cloud storage providers, such as Files app integration on iOS, or DocumentsProvider functionality on Android.
- Should support easy file sharing with other users.
- Should offer at least basic file preview and editing functionality on the web interface.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001):2013 compliance relates to the company's [information security management system](https://en.wikipedia.org/wiki/Information_security_management) and covers the sales, development, maintenance and support of their cloud services.
