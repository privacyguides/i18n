---
title: "カレンダー同期"
icon: material/calendar
description: Calendars contain some of your most sensitive data; use products that implement encryption at rest.
cover: calendar.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: パッシブ攻撃](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**Calendars** contain some of your most sensitive data; use products that implement E2EE at rest to prevent a provider from reading them.

## Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** offers a free and encrypted calendar across their supported platforms. Features include: automatic E2EE of all data, sharing features, import/export functionality, multi-factor authentication, and [more](https://tuta.com/calendar-app-comparison).

Multiple calendars and extended sharing functionality is limited to paid subscribers.

[:octicons-home-16: Homepage](https://tuta.com/calendar){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:fontawesome-brands-windows: Windows](https://tuta.com/blog/desktop-clients)
- [:simple-apple: macOS](https://tuta.com/blog/desktop-clients)
- [:simple-linux: Linux](https://tuta.com/blog/desktop-clients)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.tutanota.Tutanota)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

## Protonカレンダー

<div class="admonition recommendation" markdown>

![Proton](assets/img/calendar/proton-calendar.svg){ align=right }

**Proton Calendar** is an encrypted calendar service available to Proton members via web or mobile clients. Features include: automatic E2EE of all data, sharing features, import/export functionality, and [more](https://proton.me/support/proton-calendar-guide). Those on the free tier gain access to 3 calendars, whereas paid subscribers can create up to 25 calendars. Extended sharing functionality is also limited to paid subscribers.

[:octicons-home-16: Homepage](https://proton.me/calendar){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/calendar/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/calendar){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail/WebClients){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=me.proton.android.calendar)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1514709943)
- [:octicons-browser-16: Web](https://calendar.proton.me)

</details>

</div>

Unfortunately, as of August 2024 Proton has [still](https://discuss.privacyguides.net/t/proton-calendar-is-not-open-source-mobile/14656/8) not released the source code for their mobile Calendar app on Android or iOS, and only the former has been [audited](https://proton.me/blog/security-audit-all-proton-apps). Proton Calendar's web client is open source, however, and has been [audited](https://proton.me/community/open-source).

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- Must sync and store information with E2EE to ensure data is not visible to the service provider.

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- Should integrate with native OS calendar and contact management apps if applicable.
