---
meta_title: "Private Cryptocurrency Blockchains - Privacy Guides"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
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

<details class="info" markdown>
<summary>Monero's resilience to mass surveillance</summary>

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. פרסומים פומביים מראים כי רשת אכיפת הפשעים הפיננסיים של משרד האוצר האמריקאי העניקה [רישיון](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) ל-"Monero Module" של CipherTrace בסוף 2022.

פרטיות גרף העסקאות של Monero מוגבלת על ידי חתימות הטבעות הקטנות יחסית שלה, במיוחד נגד התקפות ממוקדות. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. אמנם אין זה סביר שכלי מעקב המוני Monero קיימים כפי שהם קיימים עבור ביטקוין ואחרים, אך בטוח שכלי מעקב מסייעים בחקירות ממוקדות.

בסופו של דבר, Monero היא המתמודדת החזקה ביותר על מטבע קריפטוגרפי ידידותי לפרטיות, אך טענות הפרטיות שלה **לא** הוכחו באופן סופי כך או כך. נדרשים יותר זמן ומחקר כדי להעריך אם Monero עמיד מספיק בפני התקפות כדי לספק תמיד פרטיות נאותה.

</details>

### Monero wallets

For optimal privacy, make sure to use a self-custody wallet where the [view key](https://www.getmonero.org/resources/moneropedia/viewkey.html) stays on the device. המשמעות היא שרק לך תהיה את היכולת להוציא את הכספים שלך ולראות עסקאות נכנסות ויוצאות. If you use a custodial wallet, the provider can see **everything** you do; if you use a “lightweight” wallet where the provider retains your view key, the provider can see almost everything you do (but not spend your funds). Some self-custody wallets where the view key does not leave your device include:

- [Official Monero client](https://getmonero.org/downloads) (שולחני)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, Desktop)
    - Cake Wallet תומך במספר מטבעות קריפטוגרפיים. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

### Monero nodes

For maximum privacy (even with a self-custody wallet), you should run your own Monero node called the [Monero daemon](https://getmonero.org/downloads/#cli). שימוש בצומת של אדם אחר יחשוף בפניו מידע מסוים, כגון כתובת ה-IP שממנה אתה מתחבר אליו, חותמות הזמן שאתה מסנכרן את הארנק שלך והעסקאות שאתה שולח מהארנק שלך (אם כי אין פרטים נוספים על עסקאות אלו). Alternatively, you can connect to someone else’s Monero node over Tor, [I2P](alternative-networks.md#i2p-the-invisible-internet-project), or a VPN.

### Buying Monero

[General tips for acquiring Monero](advanced/payments.md#acquisition ""){.md-button}

There are numerous centralized exchanges (CEX) as well as P2P marketplaces where you can buy and sell Monero. Some of them require identifying yourself (KYC) to comply with anti-money laundering regulations. However, due to Monero's privacy features, the only thing known to the seller is _that_ you bought Monero, but not how much you own or where you spend it (after it leaves the exchange). Some reputable places to buy Monero include:

- [Kraken](https://kraken.com): A well-known CEX. Registration and KYC are mandatory. Card payments and bank transfers accepted. Make sure not to leave your newly purchased Monero on Kraken's platform after the purchase; withdraw them to a self-custody wallet. Monero is not available in all jurisdictions that Kraken operates in.[^1]
- [Cake Wallet](https://cakewallet.com): A self-custody cross-platform wallet for Monero and other cryptocurrencies. You can buy Monero directly in the app using card payments or bank transfers (through third-party providers such as [Guardarian](https://guardarian.com) or [DFX](https://dfx.swiss)).[^2] KYC is usually not required, but it depends on your country and the amount you are purchasing. In countries where directly purchasing Monero is not possible, you can also use a provider within Cake Wallet to first buy another cryptocurrency such as Bitcoin, Bitcoin Cash, or Litecoin and then exchange it to Monero in-app.
    - [Monero.com](https://monero.com) is an associated website where you can buy Monero and other cryptocurrencies without having to download an app. The funds will simply be sent to the wallet address of your choice.
- [RetoSwap](https://retoswap.com) (formerly known as Haveno-Reto) is a self-custody, decentralized P2P exchange platform based on the [Haveno](https://haveno.exchange) project which is available for Linux, Windows, and macOS. Monero can be bought and sold with maximum privacy, since most trading counterparties do not require KYC, trades are made directly between users (P2P), and all connections run through the Tor network. It is possible to buy Monero via bank transfer, Paypal, or even by paying in cash (meeting in person or sending by mail). Arbitrators can step in to resolve disputes between buyer and seller, but be careful when sharing your bank account or other sensitive information with your trading counterparty. Trading with some accounts may be against those accounts' terms of service.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- מטבעות קריפטו חייבים לספק עסקאות פרטיות/בלתי ניתנות לאיתור כברירת מחדל.

<div class="admonition tip" markdown>
<p class="admonition-title">Important notices</p>

The content here is not legal or financial advice. We do not endorse or encourage illicit activities, and we do not endorse or encourage anything which violates a company's terms of service. Check with a professional to confirm that these recommendations are legal and available in your jurisdiction. [See all notices](about/notices.md).

</div>

[^1]: You may refer to the following pages for up-to-date information on countries in which Kraken does **not** allow the purchase of Monero: [Where is Kraken licensed or regulated?](https://support.kraken.com/hc/en-us/articles/where-is-kraken-licensed-or-regulated) and [Support for Monero (XMR) in Europe](https://support.kraken.com/hc/en-us/articles/support-for-monero-xmr-in-europe).
[^2]: You may refer to the following pages for up-to-date information on countries in which Cake Wallet and Monero.com **only** allow the direct purchase of Monero (through third-party providers): [Which countries are served by DFX?](https://docs.dfx.swiss/en/faq.html#which-countries-are-served-by-dfx) and [What are the supported countries/regions? (Guardarian)](https://guardarian.freshdesk.com/support/solutions/articles/80001151826-what-are-the-supported-countries-regions).
