---
meta_title: "המלצות והשוואה שירותי VPN פרטיים, ללא נותני חסות או מודעות - Privacy Guides"
title: "שירותי VPN"
icon: material/vpn
description: אלו הם שירותי ה-VPN הטובים ביותר להגנה על הפרטיות והאבטחה שלך באינטרנט. מצא כאן ספק שאינו מעוניין לרגל אחריך.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->

If you're looking for additional **privacy** from your ISP, on a public Wi-Fi network, or while torrenting files, a VPN may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPN אינו תחליף לשיטות אבטחה טובות.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[סקירת VPN מפורטת :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## ספקים מומלצים

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. קרא את \[רשימת הקריטריונים המלאה\](#_20) שלנו למידע נוסף.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 91+       | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | מזומן              |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN לוגו](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** הוא מתחרה חזק בתחום ה-VPN, והם פועלים מאז 2016. Proton AG מבוססת בשוויץ ומציעה רמה מוגבלת בחינם, כמו גם אפשרות פרימיום מומלצת יותר.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Countries

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. הסיבה לכך היא מסלול קצר יותר (פחות דילוגים) ליעד.
{ .annotate }

1. Last checked: 2024-04-02

אנחנו גם חושבים שעדיף לאבטחת המפתחות הפרטיים של ספק ה-VPN אם הם משתמשים ב[שרתים ייעודיים](https://en.wikipedia.org/wiki/Dedicated_hosting_service), במקום פתרונות משותפים זולים יותר (עם לקוחות אחרים) כמו [שרתים פרטיים וירטואליים](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } נבדק באופן עצמאי

החל מינואר 2020, Proton VPN עבר ביקורת בלתי תלויה על ידי SEC Consult. SEC Consult מצא כמה נקודות תורפה בסיכון בינוני ונמוך ביישומי Windows, Android ו-iOS של Proton VPN, שכולן תוקנו כראוי על ידי Proton VPN לפני פרסום הדוחות. אף אחת מהבעיות שזוהו לא הייתה מספקת לתוקף גישה מרחוק למכשיר או לתעבורה שלך. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). [מכתב אישור](https://proton.me/blog/security-audit-all-proton-apps) סופק עבור האפליקציות של Proton VPN ב-9 בנובמבר 2021 על ידי [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } לקוחות קוד פתוח

Proton VPN מספק את קוד המקור עבור לקוחות שולחן העבודה והנייד שלהם ב[ארגון GitHub](https://github.com/ProtonVPN) שלהם.

#### :material-check:{ .pg-green } מקבל מזומן

Proton VPN, בנוסף לקבלת כרטיסי אשראי/חיוב, פייפאל ו-[ביטקוין](advanced/payments.md#other-coins-bitcoin-ethereum-etc), מקבל גם **מזומן/מטבע מקומי** כאמצעי תשלום אנונימי.

#### :material-check:{ .pg-green } תמיכה ב-WireGuard

Proton VPN תומך בעיקר בפרוטוקול WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). בנוסף, WireGuard שואפת להיות פשוטה וביצועית יותר.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). יישומי טורנט תומכים לעתים קרובות ב-NAT-PMP באופן מקורי.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately it does not work very well in countries where sophisticated filters are deployed that analyze all outgoing traffic in an attempt to discover encrypted tunnels. Stealth is also not yet available on [Windows](https://github.com/ProtonVPN/win-app/issues/64) or Linux.

#### :material-check:{ .pg-green } לקוחות ניידים

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-alert-outline:{ .pg-orange } Additional Notes

תוכנות Proton VPN תומכים באימות דו-שלבי בכל הפלטפורמות מלבד לינוקס כרגע. ל - Proton VPN יש שרתים ומרכזי נתונים משלו בשוויץ, איסלנד ושוודיה. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://torproject.org) for this purpose.

##### :material-alert-outline:{ .pg-orange } תכונת Killswitch שבורה במחשבי Mac מבוססי אינטל

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. אם אתם זקוקים לתכונה זו, ואתם משתמשים ב - Mac עם ערכת שבבים של Intel, כדאי לכם לשקול להשתמש בשירות VPN אחר.

### IVPN

<div class="admonition recommendation" markdown>

![לוגו IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** הוא עוד ספק VPN פרימיום, והם פועלים מאז 2009. IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. הסיבה לכך היא מסלול קצר יותר (פחות דילוגים) ליעד.
{ .annotate }

1. Last checked: 2024-04-02

אנחנו גם חושבים שעדיף לאבטחת המפתחות הפרטיים של ספק ה-VPN אם הם משתמשים ב[שרתים ייעודיים](https://en.wikipedia.org/wiki/Dedicated_hosting_service), במקום פתרונות משותפים זולים יותר (עם לקוחות אחרים) כמו [שרתים פרטיים וירטואליים](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } נבדק באופן עצמאי

IVPN [עבר ביקורת ללא רישום מ-](https://cure53.de/audit-report_ivpn.pdf)Cure53 שהסתיים בהסכמה עם טענת VPN ללא רישום. IVPN השלימה גם [דוח בדיקה מקיף ](https://cure53.de/summary-report_ivpn_2019.pdf)Cure53 בינואר 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } לקוחות קוד פתוח

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). קוד המקור ניתן לקבל מ[ארגון GitHub שלהם](https://github.com/ivpn).

#### :material-check:{ .pg-green } מקבל מזומן ומונרו

בנוסף לקבלת כרטיסי אשראי/חיוב ופייפאל, IVPN מקבל ביטקוין, **מונרו** ו**מזומן/מטבע מקומי** (בתוכניות שנתיות) כאמצעי תשלום אנונימיים.

#### :material-check:{ .pg-green } תמיכה ב-WireGuard

IVPN תומך בפרוטוקול WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). בנוסף, WireGuard שואפת להיות פשוטה וביצועית יותר.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } העברת פורטים מרחוק

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). חיסרון של תכונה זו עלולה להשפיע לרעה על יישומים מסוימים, במיוחד יישומי עמית לעמית כמו לקוחות טורנט.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } לקוחות ניידים

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![לוגו Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** הוא VPN מהיר וזול עם התמקדות רצינית בשקיפות ואבטחה. הם פועלים מאז **2009**. Mullvad is based in Sweden and does not offer a free trial.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. הסיבה לכך היא מסלול קצר יותר (פחות דילוגים) ליעד.
{ .annotate }

1. Last checked: 2024-04-02

אנחנו גם חושבים שעדיף לאבטחת המפתחות הפרטיים של ספק ה-VPN אם הם משתמשים ב[שרתים ייעודיים](https://en.wikipedia.org/wiki/Dedicated_hosting_service), במקום פתרונות משותפים זולים יותר (עם לקוחות אחרים) כמו [שרתים פרטיים וירטואליים](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } נבדק באופן עצמאי

לקוחות ה-VPN של Mullvad נבדקו על ידי Cure53 ו-Assured AB בדו"ח חדיש [שפורסם ב-](https://cure53.de/pentest-report_mullvad_v2.pdf)cure53.de. חוקרי האבטחה הגיעו למסקנה:

> Cure53 ו-Assured AB מרוצים מתוצאות הביקורת והתוכנה משאירה רושם חיובי כללי. עם מסירות אבטחה של הצוות הפנימי במתחם ה-VPN של Mullvad, לבודקים אין ספק לגבי הפרויקט בדרך הנכונה מבחינה אבטחה.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> התוצאות של פרויקט מאי-יוני 2020 המתמקד במתחם Mullvad הן חיוביות למדי. [...] המערכת האקולוגית הכוללת של היישום המשמשת את Mullvad משאירה רושם קול ומובנה. המבנה הכללי של היישום מקל על גלגול תיקונים ותיקונים באופן מובנה. יותר מכל, הממצאים שנצפו על ידי Cure53 מדגימים את החשיבות של ביקורת מתמדת והערכה מחדש של וקטורי הדליפה הנוכחיים, על מנת להבטיח תמיד את פרטיותם של משתמשי הקצה. עם זאת, Mullvad עושה עבודה נהדרת בהגנה על משתמש הקצה מפני דליפות PII נפוצות וסיכונים הקשורים לפרטיות.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } לקוחות קוד פתוח

Mullvad מספק את קוד המקור עבור לקוחות שולחן העבודה והנייד שלהם ב[ארגון GitHub שלהם](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } מקבל מזומן ומונרו

Mullvad, בנוסף לקבל כרטיסי אשראי/חיוב ופייפאל, מקבל ביטקוין, ביטקוין מזומן, **מונרו** ו**מזומן/מטבע מקומי** כאמצעי תשלום אנונימיים. הם גם מקבלים סוויש והעברות בנקאיות.

#### :material-check:{ .pg-green } תמיכה ב-WireGuard

Mullvad תומך בפרוטוקול WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). בנוסף, WireGuard שואפת להיות פשוטה וביצועית יותר.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } תמיכה ב-IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } העברת פורטים מרחוק

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). חיסרון של תכונה זו עלולה להשפיע לרעה על יישומים מסוימים, במיוחד יישומי עמית לעמית כמו לקוחות טורנט.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } לקוחות ניידים

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. לקוח אנדרואיד זמין גם ב-[GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. לכאורה, [סין צריכה להשתמש בשיטה אחרת כדי לחסום שרתי ShadowSocks ](https://github.com/net4people/bbs/issues/22).

## קריטריונים

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

חשוב לציין ששימוש בספק VPN לא יהפוך אתכם לאנונימיים, אבל הוא ייתן לכם פרטיות טובה יותר במצבים מסוימים. VPN הוא לא כלי לפעילויות בלתי חוקיות. אל תסמכו על מדיניות "ללא תיעוד ".

</div>

**לידיעתך, איננו קשורים לאף אחד מהספקים שאנו ממליצים עליהם. זה מאפשר לנו לספק המלצות אובייקטיביות לחלוטין.** בנוסף ל[הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו מערכת ברורה של דרישות עבור כל ספק VPN שרוצה מומלץ, כולל הצפנה חזקה, ביקורות אבטחה עצמאיות, טכנולוגיה מודרנית ועוד. מומלץ להכיר את הרשימה לפני שבוחרים ספק אימייל, ולבצע מחקר משלך כדי לוודא שספק האימייל שבחרתם הוא הבחירה הנכונה עבורכם.

### טכנולוגיה

אנו דורשים מכל ספקי ה - VPN המומלצים שלנו לספק קבצי תצורה של OpenVPN לשימוש בכל לקוח. **אם** VPN מספק קליינט מותאם אישית משלו, אנו זקוקים ל-killswitch כדי לחסום דליפות נתוני רשת כאשר הוא מנותק.

**מינימום כדי לעמוד בדרישות:**

- תמיכה בפרוטוקולים חזקים כגון WireGuard & OpenVPN.
- Killswitch מובנה בקליינטים.
- תמיכה Multihop. Multihopping חשוב לשמור על נתונים פרטיים במקרה של פשרה צומת אחת.
- אם מסופקים לקוחות VPN, הם צריכים להיות [קוד פתוח](https://en.wikipedia.org/wiki/Open_source), כמו תוכנת ה-VPN שהם בדרך כלל מובנים בהם. אנחנו מאמינים שזמינות של [קוד מקור](https://en.wikipedia.org/wiki/Source_code) מספקת שקיפות רבה יותר לגבי מה שהמכשיר שלך עושה בפועל.

**המקרה הטוב ביותר:**

- Killswitch עם אפשרויות להגדרה גבוהה (הפעלה/השבתה ברשתות מסוימות, על אתחול, וכו ')
- קליינטים VPN קלים לשימוש
- תומך [IPv6](https://en.wikipedia.org/wiki/IPv6). אנו מצפים כי שרתים יאפשרו חיבורים נכנסים באמצעות IPv6 ויאפשרו לך לגשת לשירותים המתארחים בכתובות IPv6.
- היכולת של [העברת יציאות מרחוק](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) מסייעת ביצירת חיבורים בעת שימוש בתוכנת שיתוף קבצים P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer))או בעת אירוח שרת (לדוגמה, Mumble).
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### פרטיות

אנו מעדיפים שהספקים המומלצים שלנו יאספו כמה שפחות נתונים. לא לאסוף מידע אישי על רישום, וקבלת צורות אנונימיות של תשלום נדרשים.

**מינימום כדי לעמוד בדרישות:**

- [מטבע קריפטוגרפי אנונימי](cryptocurrency.md) **או** אפשרות תשלום במזומן.
- אין צורך במידע אישי כדי להירשם: רק שם משתמש, סיסמה ודוא"ל לכל היותר.

**המקרה הטוב ביותר:**

- מקבל [אפשרויות תשלום אנונימיות מרובות](advanced/payments.md).
- לא מתקבל מידע אישי (שם משתמש שנוצר אוטומטית, אין צורך באימייל וכו').

### אבטחה

VPN הוא חסר טעם אם הוא אפילו לא יכול לספק אבטחה מספקת. אנו דורשים מכל הספקים המומלצים שלנו לציית לתקני האבטחה הנוכחיים לחיבורי OpenVPN שלהם. באופן אידיאלי, הם ישתמשו ביותר תוכניות הצפנה עתידיות כברירת מחדל. כמו כן, אנו דורשים מצד שלישי עצמאי לבדוק את האבטחה של הספק, באופן אידיאלי באופן מקיף מאוד ועל בסיס חוזר ונשנה (שנתי).

**מינימום כדי לעמוד בדרישות:**

- ערכות הצפנה חזקות: OpenVPN עם אימות SHA -256; RSA -2048 או לחיצת יד טובה יותר; AES -256 - GCM או הצפנת נתונים AES -256 - CBC.
- סודיות קדימה.
- פירסם ביקורות אבטחה מחברת צד שלישי מכובדת.

**המקרה הטוב ביותר:**

- הצפנה חזקה ביותר: RSA -4096.
- סודיות קדימה.
- ביקורות אבטחה מקיפות שפורסמו מחברת צד שלישי בעלת מוניטין.
- תוכניות לחיפוש באגים ו/או תהליך גילוי - פגיעות מתואם.

### אמון

לא היית סומך על הכספים שלך למישהו עם זהות מזויפת, אז למה לסמוך עליהם עם נתוני האינטרנט שלך? אנו דורשים מהספקים המומלצים שלנו להיות פומביים לגבי הבעלות או המנהיגות שלהם. כמו כן, היינו רוצים לראות דיווחי שקיפות תכופים, במיוחד בכל הנוגע לאופן הטיפול בבקשות ממשלתיות.

**מינימום כדי לעמוד בדרישות:**

- מנהיגות ציבורית או בעלות.

**המקרה הטוב ביותר:**

- מנהיגות מול הציבור.
- דוחות שקיפות תכופים.

### שיווק

עם ספקי ה - VPN אנו ממליצים לראות שיווק אחראי.

**מינימום כדי לעמוד בדרישות:**

- חייבים לבצע ניתוח מידע באיחסון עצמי (כלומר, ללא Google Analytics). האתר של הספק חייב גם לציית ל [DNT (לא לעקוב)](https://en.wikipedia.org/wiki/Do_Not_Track) למי שרוצה לבטל את הסכמתו.

אסור שיהיה שיווק שהוא חסר אחריות:

- ביצוע ערבויות של הגנה על 100% אנונימיות. כשמישהו טוען שמשהו הוא 100% זה אומר שאין ודאות לכישלון. אנחנו יודעים שאנשים יכולים בקלות להפוך את עצמם לאיאנונימיים במספר דרכים, למשל.:
    - שימוש חוזר במידע אישי (למשל, חשבונות אימייל, שמות בדויים ייחודיים וכו') שאליהם הם ניגשו ללא תוכנת אנונימיות (Tor, VPN וכו')
    - [טביעת אצבע של דפדפן](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- טוענים ש - VPN במעגל אחד הוא "אנונימי יותר" מאשר Tor, שהוא מעגל של שלושה כשות או יותר שמשתנה באופן קבוע.
- השתמשו בשפה אחראית: כלומר, זה בסדר לומר ש-VPN "מנותק" או "לא מחובר", אולם לטעון שמישהו "חשוף", "פגיע" או "נפרץ" הוא שימוש מיותר בשפה מדאיגה שעשויה להיות שגויה. לדוגמה, ייתכן שהאדם הזה פשוט משתמש בשירות של ספק VPN אחר או משתמש ב - Tor.

**המקרה הטוב ביותר:**

שיווק אחראי כי הוא גם חינוכי ושימושי לצרכן יכול לכלול:

- השוואה מדויקת למועד שבו יש להשתמש ב-[Tor](tor.md) במקום זאת.
- זמינות אתר האינטרנט של ספק ה - VPN מעל [Onion Service](https://en.wikipedia.org/wiki/.onion)

### פונקציונליות נוספת

אמנם לא דרישות קפדניות, אך ישנם כמה גורמים שבדקנו בעת קביעה על אילו ספקים להמליץ. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
