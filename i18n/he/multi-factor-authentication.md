---
title: "אימות מרובה גורמים"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Hardware Keys</p>

[Hardware security key recommendations](security-keys.md) have been moved to their own category.

</div>

**Multi-Factor Authentication Apps** implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. זוהי שיטה שבה אתרי אינטרנט משתפים איתך סוד המשמש את אפליקציית האימות שלך כדי ליצור קוד בן שש ספרות (בדרך כלל) בהתבסס על השעה הנוכחית, שאותה אתה מזין בעת הכניסה לאתר כדי לבדוק. בדרך כלל קודים אלה מתחדשים כל 30 שניות, וברגע שנוצר קוד חדש הקוד הישן הופך לחסר תועלת. גם אם האקר מקבל קוד אחד בן שש ספרות, אין דרך להפוך את הקוד כדי לקבל את הסוד המקורי או אחרת להיות מסוגל לחזות מה כל קודים עתידיים עשויים להיות.

אנו ממליצים בחום להשתמש באפליקציות TOTP למכשירים ניידים במקום בחלופות לשולחן העבודה, מכיוון שלאנדרואיד ול-iOS יש אבטחה ובידוד אפליקציות טובים יותר מרוב מערכות ההפעלה השולחניות.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. ניתן להשתמש בו עם חשבון מקוון כדי לגבות ולסנכרן את האסימונים שלך בין המכשירים שלך (ולגשת אליהם דרך ממשק אינטרנט) בצורה מאובטחת ומוצפנת מקצה לקצה. ניתן להשתמש בו גם במצב לא מקוון במכשיר בודד ללא צורך בחשבון.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (אנדרואיד)

<div class="admonition recommendation" markdown>

![Aegis לוגו](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** היא אפליקציה חינמית וקוד פתוח עבור אנדרואיד לניהול אסימוני האימות הדו-שלביים שלך עבור השירותים המקוונים שלך. Aegis Authenticator פועל באופן לא מקוון/מקומי לחלוטין, אך כולל אפשרות לייצא את האסימונים שלך לגיבוי בניגוד לחלופות רבות.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- קוד המקור חייב להיות זמין לציבור.
- אסור לדרוש חיבור לאינטרנט.
- Cloud syncing must be optional, and (if available) sync functionality must be E2EE.
