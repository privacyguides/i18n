---
title: "חזיתות"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

לפעמים שירותים ינסו לאלץ אותך להירשם לחשבון על ידי חסימת גישה לתוכן עם חלונות קופצים מעצבנים. הם יכולים להישבר גם ללא הפעלת JavaScript. חזיתות אלה יכולות לאפשר לך לעקוף את ההגבלות הללו.

אם תבחר לארח בעצמך את החזיתות האלה, חשוב שאנשים אחרים ישתמשו גם במופע שלך כדי שתוכל להשתלב. אתה צריך להיות זהיר עם היכן וכיצד אתה מארח, מכיוון שהשימוש של אנשים אחרים יהיה מקושר לאירוח שלך.

כאשר אתה משתמש במופע המופעל על ידי מישהו אחר, הקפד לקרוא את מדיניות הפרטיות של אותו מופע ספציפי. הם יכולים להשתנות על ידי בעליהם ולכן עשויים שלא לשקף את מדיניות ברירת המחדל. Some instances have [Tor](tor.md) .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: מאגר](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="מופעים ציבוריים"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=תיעוד}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="קוד מקור" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## יוטיוב

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube לוגו](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** הוא יישום שולחן עבודה חינם וקוד פתוח עבור [יוטיוב](https://youtube.com). בעת שימוש ב- FreeTube, רשימת המנויים ורשימות ההשמעה שלך נשמרות באופן מקומי במכשיר שלך.

כברירת מחדל, FreeTube חוסמת את כל הפרסומות של יוטיוב. בנוסף, FreeTube משתלבת באופן אופציונלי עם [SponsorBlock](https://sponsor.ajay.app) כדי לעזור לך לדלג על קטעי וידאו ממומנים.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Yattee לוגו](assets/img/frontends/yattee.svg){ align=right }

**Yattee** הוא נגן וידאו חינמי וקוד פתוח מוכוון פרטיות עבור iOS, tvOS ו-macOS עבור [יוטיוב](https://youtube.com). בעת השימוש ב - Yattee, רשימת המנויים שלך נשמרת באופן מקומי במכשיר שלך.

You will need to take a few [extra steps](https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube, due to App Store restrictions.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

כברירת מחדל, Yattee חוסם את כל הפרסומות ב - YouTube. בנוסף, Yattee משתלב באופן אופציונלי עם [SponsorBlock](https://sponsor.ajay.app) כדי לעזור לך לדלג על קטעי וידאו ממומנים.

### LibreTube (אנדרואיד)

<div class="admonition recommendation" markdown>

![LibreTube לוגו](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube לוגו](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** היא אפליקציית אנדרואיד בחינם וקוד פתוח עבור [YouTube](https://youtube.com) המשתמשת בממשק ה-API של [Piped](#piped).

LibreTube מאפשר לך לאחסן את רשימת המנויים והפלייליסטים שלך באופן מקומי במכשיר האנדרואיד שלך, או בחשבון במופע Piped שבחרת, מה שמאפשר לך לגשת אליהם בצורה חלקה גם במכשירים אחרים.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

כברירת מחדל, LibreTube חוסמת את כל פרסומות יוטיוב. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. אתה יכול להגדיר באופן מלא את סוגי הפלחים שSponsorBlock ידלג עליהם, או להשבית אותו לחלוטין. יש גם כפתור בנגן הווידאו עצמו כדי להשבית אותו עבור סרטון מסוים אם תרצה בכך.

### NewPipe (אנדרואיד)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

רשימת המנויים והפלייליסטים שלך נשמרים באופן מקומי במכשיר האנדרואיד שלך.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

בעת שימוש ב-NewPipe, כתובת ה-IP שלך תהיה גלויה לספקי הווידאו שבהם נעשה שימוש. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious לוגו](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious לוגו](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** הוא ממשק קצה חינמי וקוד פתוח עבור [YouTube](https://youtube.com) שמתארח גם בעצמו.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

כברירת מחדל, Invidious לא מזרימה פרוקסי וידאו. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. הוא אינו מספק פרטיות בפני עצמו, ואנחנו לא ממליצים להיכנס לחשבונות כלשהם.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped לוגו](assets/img/frontends/piped.svg){ align=right }

**Piped** הוא חזית קוד פתוח בחינם ל-[YouTube](https://youtube.com) שמתארח גם בעצמו.

Piped דורש JavaScript כדי לתפקד ויש מספר מופעים ציבוריים.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped שימושי אם ברצונך להשתמש ב - [SponsorBlock](https://sponsor.ajay.app) מבלי להתקין תוסף או לגשת לתוכן מוגבל לגיל ללא חשבון. הוא אינו מספק פרטיות בפני עצמו, ואנחנו לא ממליצים להיכנס לחשבונות כלשהם.

</div>

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

חזיתות מומלצות...

- חייבת להיות תוכנת קוד פתוח.
- חייב להיות ניתן לאירוח עצמי.
- חייב לספק את כל הפונקציונליות הבסיסית של האתר הזמינה למשתמשים אנונימיים.

אנו מתייחסים רק לחזיתות עבור אתרים שהם...

- Normally only accessible with JavaScript enabled.
