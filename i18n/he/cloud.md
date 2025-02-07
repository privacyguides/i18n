---
meta_title: "ספקי אחסון הענן הפרטיים והמאובטחים הטובים ביותר - Privacy Guides"
title: "אחסון בענן"
icon: material/file-cloud
description: ספקי אחסון בענן רבים דורשים את האמון שלך שהם לא יסתכלו על הקבצים שלך. אלו חלופות פרטיות!
cover: cloud.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: התקפות פסיביות](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: ספקי שירות](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Many **cloud storage providers** require your full trust that they will not look at your files. החלופות המפורטות להלן מבטלות את הצורך באמון על ידי הטמעת E2EE מאובטחת.

אם חלופות אלה אינן מתאימות לצרכים שלך, אנו מציעים לך לבדוק שימוש בתוכנת הצפנה כמו [Cryptomator](encryption.md#cryptomator-cloud) עם ספק ענן אחר. שימוש ב-Cryptomator בשילוב עם **כל** ספק ענן (כולל אלה) עשוי להיות רעיון טוב כדי להפחית את הסיכון לפגמי הצפנה אצל הלקוחות המקומיים של הספק.

<details class="admonition info" markdown>
<summary>Looking for Nextcloud?</summary>

Nextcloud is [still a recommended tool](document-collaboration.md#nextcloud) for self-hosting a file management suite, however we do not recommend third-party Nextcloud storage providers at the moment, because we do [not recommend](https://discuss.privacyguides.net/t/dont-recommend-nextcloud-e2ee/10352/29) Nextcloud's built-in E2EE functionality for home users.

</details>

## Proton Drive

<div class="admonition recommendation" markdown>

![Proton Drive logo](assets/img/cloud/protondrive.svg){ align=right }

**Proton Drive** is an encrypted cloud storage provider from the popular encrypted email provider [Proton Mail](email.md#proton-mail). The initial free storage is limited to 2GB, but with the completion of [certain steps](https://proton.me/support/more-free-storage-existing-users), additional storage can be obtained up to 5GB.

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

The Proton Drive web application has been independently audited by Securitum in [2021](https://proton.me/community/open-source).

Proton Drive's brand new mobile clients have not yet been publicly audited by a third party.

## Tresorit

<div class="admonition recommendation" markdown>

![Tresorit לוגו](assets/img/cloud/tresorit.svg){ align=right }

** Tresorit ** הוא ספק אחסון ענן מוצפן שוויצרי-הונגרי שנוסד בשנת 2011. Tresorit נמצאת בבעלות ה-Swiss Post, שירות הדואר הלאומי של שוויץ.

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

Tresorit קיבלה מספר ביקורות אבטחה עצמאיות:

- [2022](https://tresorit.com/blog/tresorit-receives-iso-27001-certification): ISO/IEC 27001:2013[^1] Compliance [Certification](https://certipedia.com/quality_marks/9108644476) by TÜV Rheinland InterCert Kft
- [2021](https://tresorit.com/blog/fresh-penetration-testing-confirms-tresorit-security): Penetration Testing by Computest
    - סקירה זו העריכה את האבטחה של לקוח האינטרנט של Tresorit, אפליקציית אנדרואיד, אפליקציית ווינדוס והתשתית הקשורה אליו.
    - Computest גילתה שתי נקודות תורפה שנפתרו.
- [2019](https://tresorit.com/blog/ernst-young-review-verifies-tresorits-security-architecture): Penetration Testing by Ernst & Young.
    - סקירה זו ניתחה את קוד המקור המלא של Tresorit ואימתה שהיישום תואם את המושגים המתוארים ב[דף הלבן](https://prodfrontendcdn.azureedge.net/202208011608/tresorit-encryption-whitepaper.pdf) של Tresorit.
    - ארנסט & יאנג בדק בנוסף את האינטרנט, הנייד והמחשב שולחני: "תוצאות הבדיקה לא מצאו חריגה מתביעות סודיות הנתונים של Tresorit."

They have also received the Digital Trust Label, a certification from the [Swiss Digital Initiative](https://efd.admin.ch/en/swiss-digital-initiative-en) which requires passing [35 criteria](https://swiss-digital-initiative.org/criteria) related to security, privacy, and reliability.

## Peergos

<div class="admonition recommendation" markdown>

![Peergos logo](assets/img/cloud/peergos.svg){ align=right }

**Peergos** is a decentralized protocol and open-source platform for storage, social media, and applications. It provides a secure and private space where users can store, share, and view their photos, videos, documents, etc. Peergos secures your files with quantum-resistant end-to-end encryption and ensures all data about your files remains private. It is built on top of [IPFS (InterPlanetary File System)](https://ipfs.tech), a peer-to-peer architecture that protects against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://peergos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://peergos.net/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://book.peergos.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Peergos/Peergos){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-globe-16: Web](https://peergos.net)
- [:fontawesome-brands-windows: Windows](https://github.com/Peergos/web-ui/releases)
- [:simple-apple: macOS](https://github.com/Peergos/web-ui/releases)
- [:simple-linux: Linux](https://github.com/Peergos/web-ui/releases)

</details>

</div>

Peergos is primarily a web app, but you can self-host the server either as a local cache for your remote Peergos account, or as a standalone storage server which negates the need to register for a remote account and subscription. The Peergos server is a `.jar` file, which means the Java 17+ Runtime Environment ([OpenJDK download](https://azul.com/downloads)) should be installed on your machine to get it working.

Running a local version of Peergos alongside a registered account on their paid, hosted service allows you to access your Peergos storage without any reliance on DNS or TLS certificate authorities, and keep a copy of your data backed up to their cloud. The user experience should be the same whether you run their desktop server or just use their hosted web interface.

Peergos was [audited](https://peergos.org/posts/security-audit-2024) in November 2024 by Radically Open Security and all issues were fixed. They were previously [audited](https://cure53.de/pentest-report_peergos.pdf) by Cure53 in June 2019, and all found issues were subsequently fixed.

An Android app is not available but it is [in the works](https://discuss.privacyguides.net/t/peergos-private-storage-sharing-social-media-and-application-platform/11825/25). The current workaround is to use the mobile [PWA](https://peergos.net) instead.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### דרישות מינימליות

- חייב לאכוף הצפנה מקצה לקצה.
- יש להציע תוכנית חינם או תקופת ניסיון לבדיקה.
- Must support TOTP or FIDO2 multi-factor authentication, or passkey logins.
- חייב להציע ממשק אינטרנט התומך בפונקציונליות ניהול קבצים בסיסית.
- חייב לאפשר ייצוא קל של כל הקבצים/המסמכים.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- Clients should be open source.
- לקוחות צריכים להיות מבוקרים במלואם על ידי צד שלישי עצמאי.
- צריך להציע ללקוחות מקומיים עבור לינוקס, אנדרואיד, Windows, macOS ו - iOS.
    - לקוחות אלה צריכים להשתלב עם כלי מערכת הפעלה מקוריים עבור ספקי אחסון בענן, כגון שילוב אפליקציות קבצים ב- iOS, או פונקציונליות DocumentsProvider באנדרואיד.
- צריך לתמוך בשיתוף קבצים קל עם משתמשים אחרים.
- אמור להציע לפחות תצוגה מקדימה בסיסית של קובץ ופונקציונליות עריכה בממשק האינטרנט.

[^1]: [ISO/IEC 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001): תאימות 2013 מתייחסת ל[מערכת ניהול אבטחת המידע](https://en.wikipedia.org/wiki/Information_security_management) של החברה ומכסה את המכירות, הפיתוח, התחזוקה והתמיכה של שירותי הענן שלהם.
