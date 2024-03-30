---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "תקשורת בזמן אמת"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

אלו ההמלצות שלנו לתקשורת מוצפנת בזמן אמת.

[סוגי רשתות תקשורת :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## מסנג'רים מוצפנים

מסנג'רים אלה נהדרים לאבטחת התקשורת הרגישה שלך.

### Signal

<div class="admonition recommendation" markdown>

![Signal לוגו](assets/img/messengers/signal.svg){ align=right }

**Signal** היא אפליקציה לנייד שפותחה על ידי סיגנל מסנג'ר LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requires your phone number for registration, however you should create a username to hide your phone number from your contacts:

1. In Signal, open the app's settings and tap your account profile at the top.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. גם פרופילים אישיים מוצפנים ומשותפים רק עם אנשי קשר שאיתם אתה משוחח בצ'אט. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. כתובת השולח מוצפנת יחד עם גוף ההודעה, ורק כתובת הנמען גלויה לשרת. 'שולח אטום' זמין רק עבור אנשים ברשימת אנשי הקשר שלך, אך ניתן להפוך אותו לזמין עבור כל הנמענים עם סיכון מוגבר לקבלת דואר זבל.

הפרוטוקול היה מבוקר [באופן עצמאי](https://eprint.iacr.org/2016/1013.pdf) בשנת 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

יש לנו כמה טיפים נוספים להגדרה והקשחה של התקנת הSignal שלך:

[תצורת סיגנל והקשחה :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![לוגו Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat הוא מסנג'ר מיידי מבוזר ואינו תלוי במזהים ייחודיים כגון מספרי טלפון או שמות משתמש. משתמשי SimpleX Chat יכולים לסרוק קוד QR או ללחוץ על קישור הזמנה כדי להשתתף בשיחות קבוצתיות.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [נבדק](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) על ידי Trail of Bits באוקטובר 2022.

SimpleX Chat תומך בפונקציונליות בסיסית של צ'אט קבוצתי, הודעות ישירות ועריכה של הודעות ו-markdown. שיחות שמע ווידאו E2EE נתמכות גם כן. ניתן לייצא את הנתונים שלך ולייבא אותם למכשיר אחר, מכיוון שאין שרתים מרכזיים שבהם הם מגובים.

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network. Briar יכול גם להתחבר באמצעות Wi-Fi או Bluetooth כאשר הוא נמצא בקרבה מקומית. מצב הרשת המקומי של Briar יכול להיות שימושי כאשר זמינות האינטרנט היא בעיה.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

כדי להוסיף איש קשר ב Briar, שניכם חייבים להוסיף אחד את השני קודם. באפשרותך להחליף `קישורים ` או לסרוק את קוד ה - QR של איש הקשר אם הוא נמצא בקרבת מקום.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

ל Briar יש מפרט ש[פורסם במלואו](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## אפשרויות נוספות

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. כל פשרה מרכזית בין מקבלי ההודעות תשפיע על הסודיות של **כל** התקשורת העבר.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients) for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

הודעות וקבצים המשותפים בחדרים פרטיים (אלו הדורשים הזמנה) הם כברירת מחדל E2EE וכך גם שיחות קול ווידאו אחד לאחד.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:simple-windows11: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

תמונות פרופיל, תגובות וכינויים אינם מוצפנים.

שיחות קוליות ושיחות וידאו קבוצתיות [אינן](https://github.com/vector-im/element-web/issues/12878) E2EE, ומשתמשות ב- Jitsi, אך זה צפוי להשתנות עם[ איתות VoIP קבוצתי מקורי](https://github.com/matrix-org/matrix-doc/pull/3401). שיחות קבוצתיות כוללות [שיחות ללא אימות](https://github.com/vector-im/element-web/issues/13074) כרגע, כלומר, כל משתתפים יכולים גם להצטרף לשיחות. אנו ממליצים שלא להשתמש בתכונה זו לפגישות פרטיות.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

הפרוטוקול היה מבוקר [באופן עצמאי](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) בשנת 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![לוגו Session](assets/img/messengers/session.svg){ align=right }

**Session** הוא מסנג'ר מבוזר עם התמקדות בתקשורת פרטית, מאובטחת ואנונימית. Session מציע תמיכה בהודעות ישירות, צ'אטים קבוצתיים ושיחות קוליות.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. כל הודעה מוצפנת מנותבת דרך שלושה צמתים ברשת Oxen Service Node Network, מה שהופך את זה למעשה לבלתי אפשרי עבור הצמתים לאסוף מידע משמעותי על המשתמשים ברשת.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session מאפשרת E2EE בצ'אטים אחד על אחד או קבוצות סגורות המאפשרות עד 100 חברים. לקבוצות פתוחות אין הגבלה על מספר החברים, אך הן פתוחות על פי עיצוב.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
