---
title: "ספקי DNS"
icon: material/dns
description: אלו הם כמה ספקי DNS מוצפנים שאנו ממליצים לעבור אליהם, כדי להחליף את תצורת ברירת המחדל של ספק שירותי האינטרנט שלך.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

יש להשתמש ב-DNS מוצפן עם שרתי צד שלישי רק כדי לעקוף [חסימת DNS](https://en.wikipedia.org/wiki/DNS_blocking) בסיסית כאשר אתה יכול להיות בטוח שלא יהיו השלכות. DNS מוצפן לא יעזור לך להסתיר את פעילות הגלישה שלך.

[למד עוד :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## ספקים מומלצים

| ספקי DNS                                                                   | מדיניות פרטיות                                                                                       | פרוטוקולים                                                                                 | תיעוד בקשות    | ECS        | סינון                                                                                                                             |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------- | ---------- | --------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt               | חלקי[^1]       | Yes        | מבוסס על תצורה אישית. רשימת סינון בשימוש ניתן למצוא כאן. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext <br> DoH <br> DoT                                                    | חלקי[^2]       | לא         | מבוסס על תצורה אישית.                                                                                                             |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext <br> DoH <br> DoT <br> DNSCrypt <br> DoQ <br> DoH3 | אופציונאלי[^3] | לא         | מבוסס על תצורה אישית.                                                                                                             |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                                         | לא[^4]         | לא         | מבוסס על תצורה אישית. רשימת סינון בשימוש ניתן למצוא כאן. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Cleartext <br> DoH <br> DoT <br> DNSCrypt <br> DoQ <br> DoH3 | אופציונאלי[^5] | אופציונאלי | מבוסס על תצורה אישית.                                                                                                             |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt                                | חלק[^6]        | אופציונאלי | בהתבסס על תצורה אישית, חוסם תוכנות זדוניות כברירת מחדל.                                                                           |

### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בְּספק, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

</div>

- חייב לתמוך ב [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [מזעור QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- אפשר ל - [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) להיות מנוטרל
- תעדוף תמיכה ב[Anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) או תמיכה ב"היגוי גיאוגרפי".

## תמיכה במערכת הפעלה מקומית

### אנדרואיד

אנדרואיד 9 ומעלה תומכת ב-DNS דרך TLS. ניתן למצוא את ההגדרות ב: **הגדרות** &rarr; **רשת & אינטרנט** &rarr; **פרטי DNS**.

### מוצרי Apple

הגרסאות האחרונות של iOS, iPadOS, tvOS ו-macOS, תומכות הן ב-DoT והן ב-DoH. שני הפרוטוקולים נתמכים באופן מקורי באמצעות [פרופילי תצורה](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) או דרך [ממשק API להגדרות DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

לאחר התקנה של פרופיל תצורה או אפליקציה המשתמשת ב-API של הגדרות DNS, ניתן לבחור את תצורת ה-DNS. אם VPN פעיל, הרזולוציה בתוך מנהרת ה-VPN תשתמש בהגדרות ה-DNS של ה-VPN ולא בהגדרות כלל המערכת שלך.

#### פרופילים חתומים

Apple אינה מספקת ממשק מקורי ליצירת פרופילי DNS מוצפנים. [יוצר פרופיל DNS מאובטח](https://dns.notjakob.com/tool.html) הוא כלי לא רשמי ליצירת פרופילי DNS מוצפנים משלך, אולם הם לא ייחתמו. פרופילים חתומים מועדפים; החתימה מאמתת את מקור הפרופיל ומסייעת להבטיח את שלמות הפרופילים. תווית "מאומת" ירוקה ניתנת לפרופילי תצורה חתומים. לקבלת מידע נוסף על חתימת קוד, ראה [אודות חתימת קוד](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, שהפצות לינוקס רבות משתמשות בו כדי לבצע את חיפושי ה-DNS שלהם, עדיין לא [תומך ב-DoH](https://github.com/systemd/systemd/issues/8639). אם אתה רוצה להשתמש ב-DoH, תצטרך להתקין פרוקסי כמו [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) ו[להגדיר אותו](https://wiki.archlinux.org/title/Dnscrypt-proxy) כדי לקחת את כל שאילתות ה-DNS מפותר המערכת ולהעביר אותן באמצעות HTTPS.

</div>

## פרוקסי DNS מוצפנים

תוכנת פרוקסי DNS מוצפנת מספקת פרוקסי מקומי שאליו ניתן להעביר את פותר [ה-DNS הלא מוצפן](advanced/dns-overview.md#unencrypted-dns). בדרך כלל הוא משמש בפלטפורמות שאינן תומכות באופן מקורי [ב-DNS מוצפן](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS לוגו](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS לוגו](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** הוא לקוח אנדרואיד בקוד פתוח התומך ב [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) ו-DNS Proxy יחד עם שמירה במטמון של תגובות DNS, רישום מקומי של שאילתות DNS וניתן להשתמש בהם גם בתור חומת אש.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![dnscrypt-proxy לוגו](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** הוא פרוקסי DNS עם תמיכה ב-[DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https -doh), ו-[DNS אנונימי](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## פתרונות אירוח עצמי

פתרון DNS שמתארח בעצמו שימושי לאספקת סינון בפלטפורמות מבוקרות, כגון טלוויזיות חכמות והתקני IoT אחרים, מכיוון שאין צורך בתוכנה בצד הלקוח.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home כולל ממשק אינטרנט משופשף כדי להציג תובנות ולנהל תוכן חסום.

[:octicons-home-16: דף הבית](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="מדיניות פרטיות" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="קוד מקור" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole מיועד להתארח ב-Raspberry Pi, אך הוא אינו מוגבל לחומרה כזו. התוכנה כוללת ממשק אינטרנט ידידותי כדי להציג תובנות ולנהל תוכן חסום.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: AdGuard מאחסן מדדי ביצועים מצטברים של שרתי ה-DNS שלהם, כלומר מספר הבקשות המלאות לשרת מסוים, מספר הבקשות החסומות ומהירות עיבוד הבקשות. הם גם שומרים ומאחסנים את מסד הנתונים של הדומיינים שהתבקשו ב-24 השעות האחרונות. "אנחנו צריכים את המידע הזה כדי לזהות ולחסום עוקבים ואיומים חדשים." "אנחנו גם מתעדים כמה פעמים גשש זה או אחר נחסם. אנחנו צריכים את המידע הזה כדי להסיר את הכללים המיושנים מהמסננים שלנו." [https://adguard.com/en/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare אוספת ומאחסנת רק את נתוני שאילתת ה-DNS המוגבלים שנשלחים לפותר 1.1.1.1. שירות הפותר 1.1.1.1 אינו רושם נתונים אישיים, וחלק הארי של נתוני השאילתות המוגבלים שאינם ניתנים לזיהוי אישי מאוחסן למשך 25 שעות בלבד. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D רק מתעדים עבור פותרי Premium עם פרופילי DNS מותאמים אישית. פותרים חינמיים אינם רושמים נתונים. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: שירות ה-DNS של Mullvad זמין הן למנויים והן ללא מנויים של Mullvad VPN. מדיניות הפרטיות שלהם טוענת במפורש שהם לא רושמים בקשות DNS בשום צורה. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 אוספת חלק מהנתונים למטרות ניטור ותגובה של איומים. לאחר מכן ניתן לערבב מחדש את הנתונים הללו ולשתף אותם, למשל לצורך מחקר אבטחה. Quad9 אינה אוספת או מתעדת כתובות IP או נתונים אחרים שלדעתם ניתנים לזיהוי אישי. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
