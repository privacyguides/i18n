---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
title: מטבעות קריפטוגרפיים
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: מעקב המוני](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: צנזורה](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

ביצוע תשלומים אונליין הוא אחד האתגרים הגדולים ביותר לפרטיות. מטבעות קריפטוגרפיים אלו מספקים פרטיות עסקאות כברירת מחדל (דבר ש**לא** מובטח על ידי רוב מטבעות הקריפטו), בתנאי שיש לך הבנה טובה כיצד לבצע תשלומים פרטיים ביעילות. אנו ממליצים בחום שתקרא תחילה את מאמר סקירת התשלומים שלנו לפני ביצוע רכישות כלשהן:

[ביצוע תשלומים פרטיים :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

רבים אם לא רוב הפרויקטים של מטבעות קריפטוגרפיים הם הונאות. בצע עסקאות בזהירות עם רק פרויקטים שאתה סומך עליהם.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. כל עסקת Monero מסתירה את סכום העסקה, כתובות שליחה וקבלה, ומקור הכספים ללא שום חישוקים לדלג דרכם, מה שהופך אותה לבחירה אידיאלית עבור טירוני מטבעות קריפטוגרפיים.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

עם Monero, משקיפים מבחוץ אינם יכולים לפענח כתובות מסחר Monero, סכומי עסקאות, יתרות כתובות או היסטוריית עסקאות.

לפרטיות מיטבית, הקפד להשתמש בארנק לא משמורן שבו מפתח התצוגה נשאר במכשיר. המשמעות היא שרק לך תהיה את היכולת להוציא את הכספים שלך ולראות עסקאות נכנסות ויוצאות. אם אתה משתמש בארנק משמורן, הספק יכול לראות **כל מה** שאתה עושה; אם אתה משתמש בארנק "קל משקל" שבו הספק שומר על מפתח התצוגה הפרטי שלך, הספק יכול לראות כמעט כל מה שאתה עושה. כמה ארנקים שאינם משמורנים כוללים:

- [Official Monero client](https://getmonero.org/downloads) (שולחני)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet תומך במספר מטבעות קריפטוגרפיים. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

לפרטיות מקסימלית (אפילו עם ארנק לא משמורן), עליך להפעיל צומת Monero משלך. שימוש בצומת של אדם אחר יחשוף בפניו מידע מסוים, כגון כתובת ה-IP שממנה אתה מתחבר אליו, חותמות הזמן שאתה מסנכרן את הארנק שלך והעסקאות שאתה שולח מהארנק שלך (אם כי אין פרטים נוספים על עסקאות אלו). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. פרסומים פומביים מראים כי רשת אכיפת הפשעים הפיננסיים של משרד האוצר האמריקאי העניקה [רישיון](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) ל-"Monero Module" של CipherTrace בסוף 2022.

פרטיות גרף העסקאות של Monero מוגבלת על ידי חתימות הטבעות הקטנות יחסית שלה, במיוחד נגד התקפות ממוקדות. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. אמנם אין זה סביר שכלי מעקב המוני Monero קיימים כפי שהם קיימים עבור ביטקוין ואחרים, אך בטוח שכלי מעקב מסייעים בחקירות ממוקדות.

בסופו של דבר, Monero היא המתמודדת החזקה ביותר על מטבע קריפטוגרפי ידידותי לפרטיות, אך טענות הפרטיות שלה **לא** הוכחו באופן סופי כך או כך. נדרשים יותר זמן ומחקר כדי להעריך אם Monero עמיד מספיק בפני התקפות כדי לספק תמיד פרטיות נאותה.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- מטבעות קריפטו חייבים לספק עסקאות פרטיות/בלתי ניתנות לאיתור כברירת מחדל.
