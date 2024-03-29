---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## מפתחות אבטחה של חומרה

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-factor-authentication/yubikey.png)

**YubiKeys** הם בין מפתחות האבטחה הפופולריים ביותר. Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

אחד היתרונות של YubiKey הוא שמפתח אחד יכול לעשות כמעט הכל (YubiKey 5), שאפשר לצפות ממפתח אבטחת חומרה. We do encourage you to take the [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: Homepage](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare. אנו ממליצים בחום לבחור במפתחות מסדרת YubiKey 5.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). כל הלקוחות של Yubico הם קוד פתוח.

עבור דגמים התומכים ב - HOTP וב - TOTP, ישנם 2 חריצים בממשק ה - OTP שניתן להשתמש בהם עבור HOTP ו -32 חריצים לאחסון סודות TOTP. סודות אלה מאוחסנים מוצפנים על המפתח ואף פעם לא לחשוף אותם למכשירים הם מחוברים. ברגע שזרע (סוד משותף) ניתן למאמת Yubico, הוא ייתן רק את הקודים בני שש הספרות, אך לעולם לא את הזרע. מודל אבטחה זה עוזר להגביל את מה שתוקף יכול לעשות אם הוא מסכן את אחד המכשירים המריצים את המאמת של Yubico והופך את ה - YubiKey לעמיד בפני תוקף פיזי.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

The firmware of YubiKey is not open source and is not updatable. אם אתה רוצה תכונות בגרסאות קושחה חדשות יותר, או אם ישנה פגיעות בגרסת הקושחה שבה אתה משתמש, תצטרך לרכוש מפתח חדש.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-factor-authentication/nitrokey.jpg){ align=right }

**ל - Nitrokey** יש מפתח אבטחה המסוגל ל- [FIDO2 ו- WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) בשם **Nitrokey FIDO2**. לתמיכה ב-PGP, עליך לרכוש אחד מהמפתחות האחרים שלהם כגון **Nitrokey Start**, **Nitrokey Pro 2** או **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. ל**Nitrokey 3** המופיע ברשימה תהיה ערכת תכונות משולבת.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

עבור הדגמים התומכים ב - HOTP וב - TOTP, ישנם 3 חריצים עבור HOTP ו -15 עבור TOTP. Nitrokeys מסוימים יכולים לשמש כמנהל סיסמאות. הם יכולים לאחסן 16 אישורים שונים ולהצפין אותם באמצעות אותה סיסמה כמו ממשק OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

בעוד ש-Nitrokeys אינם משחררים את סודות ה-HOTP/TOTP למכשיר שאליו הם מחוברים, אחסון ה-HOTP וה-TOTP **לא** מוצפן ופגיע להתקפות פיזיות. אם אתם מחפשים לאחסן סודות HOTP או TOTP, אנו ממליצים בחום להשתמש במפתח YubiKey.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

איפוס ממשק OpenPGP על Nitrokey גם יגרום למסד הנתונים סיסמה [inaccessible](https://docs.nitrokey.com/pro/factory-reset.html).

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net) firmware.

הקושחה של Nitrokey היא קוד פתוח, שלא כמו YubiKey. הקושחה בדגמי NitroKey המודרניים (למעט ה**NitroKey Pro 2**) ניתנת לעדכון.

### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

</div>

#### דרישות מינימליות

- יש להשתמש במודולי אבטחה עמידים לחומרה באיכות גבוהה.
- חייב לתמוך במפרט FIDO2 העדכני ביותר.
- אסור לאפשר חילוץ מפתח פרטי.
- מכשירים שעולים מעל $35 חייבים לתמוך בטיפול ב-OpenPGP וב-S/MIME.

#### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- אמור להיות זמין בפורמט USB-C.
- אמור להיות זמין עם NFC.
- אמור לתמוך באחסון סודי ב-TOTP.
- אמור לתמוך בעדכוני קושחה מאובטחים.

## אפליקציות מאמתות

יישומי אימות מיישמים תקן אבטחה שאומץ על ידי כוח המשימה להנדסת אינטרנט (IETF) הנקרא **סיסמאות חד פעמיות חד פעמיות מבוססות זמן**, או **TOTP**. זוהי שיטה שבה אתרי אינטרנט משתפים איתך סוד המשמש את אפליקציית האימות שלך כדי ליצור קוד בן שש ספרות (בדרך כלל) בהתבסס על השעה הנוכחית, שאותה אתה מזין בעת הכניסה לאתר כדי לבדוק. בדרך כלל קודים אלה מתחדשים כל 30 שניות, וברגע שנוצר קוד חדש הקוד הישן הופך לחסר תועלת. גם אם האקר מקבל קוד אחד בן שש ספרות, אין דרך להפוך את הקוד כדי לקבל את הסוד המקורי או אחרת להיות מסוגל לחזות מה כל קודים עתידיים עשויים להיות.

אנו ממליצים בחום להשתמש באפליקציות TOTP למכשירים ניידים במקום בחלופות לשולחן העבודה, מכיוון שלאנדרואיד ול-iOS יש אבטחה ובידוד אפליקציות טובים יותר מרוב מערכות ההפעלה השולחניות.

### ente Auth

<div class="admonition recommendation" markdown>

![ente Auth לוגו](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**ente Auth** היא אפליקציה חינמית וקוד פתוח המאחסנת ויוצרת אסימוני TOTP במכשיר הנייד שלך. ניתן להשתמש בו עם חשבון מקוון כדי לגבות ולסנכרן את האסימונים שלך בין המכשירים שלך (ולגשת אליהם דרך ממשק אינטרנט) בצורה מאובטחת ומוצפנת מקצה לקצה. ניתן להשתמש בו גם במצב לא מקוון במכשיר בודד ללא צורך בחשבון.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (אנדרואיד)

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

### קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

אנו עובדים על קביעת קריטריונים מוגדרים לכל קטע באתר שלנו, והדבר עשוי להשתנות. אם יש לך שאלות כלשהן לגבי הקריטריונים שלנו, אנא [שאל בפורום שלנו](https://discuss.privacyguides.net/latest) ואל תניח שלא שקלנו משהו כשהצענו את ההמלצות שלנו אם הוא לא רשום כאן. ישנם גורמים רבים שנחשבים ונדונים כאשר אנו ממליצים על פרויקט, ותיעוד כל אחד מהם הוא עבודה בתהליך.

</div>

- קוד המקור חייב להיות זמין לציבור.
- אסור לדרוש חיבור לאינטרנט.
- אסור לסנכרן לשירות סנכרון/גיבוי בענן של צד שלישי.
    - **אופציונלי** תמיכה בסנכרון E2EE עם כלים מקוריים של מערכת ההפעלה מקובלת, למשל. סנכרון מוצפן באמצעות iCloud.
