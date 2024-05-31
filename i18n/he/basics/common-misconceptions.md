---
title: "תפיסות מוטעות נפוצות"
icon: 'material/robot-confused'
description: פרטיות היא לא נושא פשוט, וקל להיקלע לטענות שיווקיות ודיסאינפורמציה אחרת.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            האם קוד המקור זמין ואופן רישיון התוכנה אינו משפיע מטבעו על אבטחתה בשום צורה. לתוכנת קוד פתוח יש פוטנציאל להיות מאובטח יותר מתוכנה קניינית, אבל אין שום ערובה שזה המצב. כאשר אתה מעריך תוכנה, עליך להסתכל על המוניטין והאבטחה של כל כלי על בסיס אינדיבידואלי.
      - 
        "@type": Question
        name: האם העברת אמון לספק אחר יכולה להגביר את הפרטיות?
        acceptedAnswer:
          "@type": Answer
          text: |
            אנחנו מדברים הרבה על "שינוי אמון" כאשר דנים בפתרונות כמו VPNs (המסיטים את האמון שאתה נותן בספק אינטרנט שלך לספק VPN). למרות שזה מגן על נתוני הגלישה שלך מספק האינטרנט שלך באופן ספציפי, לספק ה-VPN שתבחר עדיין יש גישה לנתוני הגלישה שלך: הנתונים שלך אינם מאובטחים לחלוטין מכל הצדדים.
      - 
        "@type": Question
        name: האם פתרונות ממוקדי פרטיות אמינים מטבעם?
        acceptedAnswer:
          "@type": Answer
          text: |
            התמקדות אך ורק במדיניות הפרטיות ושיווק של כלי או ספק יכול לעוור אותך לחולשותיו. כאשר אתה מחפש פתרון פרטי יותר, עליך לקבוע מהי הבעיה הבסיסית ולמצוא פתרונות טכניים לבעיה זו. לדוגמה, ייתכן שתרצה להימנע מ Google Drive, המעניק ל - גוגל גישה לכל הנתונים שלך. הבעיה הבסיסית במקרה זה היא חוסר ב-E2EE, אז כדאי לוודא שהספק אליו אתם עוברים מיישם את E2EE, או להשתמש בכלי (כמו Cryptomator) שמספק E2EE בכל ספק ענן. מעבר לספק "ממוקד פרטיות" (שאינו מיישם E2EE) לא פותר את הבעיה שלך: הוא פשוט מעביר את האמון מגוגל לספק הזה.
      - 
        "@type": Question
        name: כמה מסובך צריך להיות מודל האיום שלי?
        acceptedAnswer:
          "@type": Answer
          text: |
            לעתים קרובות אנחנו רואים אנשים שמתארים מודלים של איום על פרטיות שהם מורכבים מדי. לעתים קרובות, פתרונות אלה כוללים בעיות כמו חשבונות דוא"ל רבים ושונים או התקנות מסובכות עם הרבה העברת חלקים ותנאים. התשובות הן בדרך כלל תשובות ל"מהי הדרך הטובה ביותר לעשות X?"
            מציאת הפתרון ה"טוב ביותר" עבור עצמך לא אומר בהכרח שאתה מחפש פתרון שאין לו טעות עם עשרות תנאים - פתרונות אלו לרוב קשה לעבוד איתם באופן מציאותי. כפי שדיברנו בעבר, אבטחה לרוב באה במחיר של נוחות.
---

## "תוכנת קוד פתוח תמיד מאובטחת" או "תוכנה קניינית מאובטחת יותר"

מיתוסים אלו נובעים ממספר דעות קדומות, אך האם קוד המקור זמין ואופן רישיון התוכנה אינו משפיע מטבעו על אבטחתה בשום צורה. == לתוכנת קוד פתוח יש את ה*פוטנציאל* להיות מאובטח יותר מתוכנה קניינית, אבל אין שום ערובה שזה המצב.== כאשר אתה מעריך תוכנה, עליך להסתכל על המוניטין והאבטחה של כל כלי על בסיס אישי.

תוכנת קוד פתוח *ניתנת* לביקורת על ידי צדדים שלישיים, ולעתים קרובות היא שקופה יותר לגבי נקודות תורפה אפשריות מאשר עמיתים קנייניים. זה גם מאפשר לך לסקור את הקוד ולהשבית כל פונקציונליות חשודה שתמצא בעצמך. עם זאת, *אלא אם כן תעשה זאת*, אין ערובה שהקוד הוערך אי פעם, במיוחד עם פרויקטי תוכנה קטנים יותר. The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

בצד השני, תוכנה קניינית פחות שקופה, אבל זה לא מרמז על כך שהיא לא מאובטחת. פרויקטי תוכנה קנייניים גדולים ניתנים לביקורת פנימית ועל ידי סוכנויות צד שלישי, וחוקרי אבטחה בלתי תלויים עדיין יכולים למצוא נקודות תורפה עם טכניקות כמו הנדסה לאחור.

כדי להימנע מהחלטות מוטות, *חיוני* שתעריך את תקני הפרטיות והאבטחה של התוכנה שבה אתה משתמש.

## "שינוי באמון יכול להגביר את הפרטיות"

אנחנו מדברים הרבה על "שינוי אמון" כאשר דנים בפתרונות כמו VPNs (המסיטים את האמון שאתה נותן בספק אינטרנט שלך לספק VPN). למרות שזה מגן על נתוני הגלישה שלך מספק האינטרנט שלך *באופן ספציפי*, לספק ה-VPN שתבחר עדיין יש גישה לנתוני הגלישה שלך: הנתונים שלך אינם מאובטחים לחלוטין מכל הצדדים. משמעות הדבר היא:

1. עליך לנקוט משנה זהירות בעת בחירת ספק להעביר אליו אמון.
2. אתה עדיין צריך להשתמש בטכניקות אחרות, כמו E2EE, כדי להגן על הנתונים שלך לחלוטין. חוסר אמון בספק אחד בלבד כדי לסמוך על אחר אינו מאבטח הנתונים שלך.

## "פתרונות המתמקדים בפרטיות הם אמינים מטבעם"

התמקדות אך ורק במדיניות הפרטיות ושיווק של כלי או ספק יכול לעוור אותך לחולשותיו. כאשר אתה מחפש פתרון פרטי יותר, עליך לקבוע מהי הבעיה הבסיסית ולמצוא פתרונות טכניים לבעיה זו. לדוגמה, ייתכן שתרצה להימנע מ Google Drive, המעניק ל - גוגל גישה לכל הנתונים שלך. הבעיה הבסיסית במקרה זה היא חוסר ב-E2EE, אז כדאי לוודא שהספק אליו אתם עוברים מיישם את E2EE, או להשתמש בכלי (כמו [Cryptomator](../encryption.md#cryptomator-cloud)) המספק E2EE בכל ספק ענן. מעבר לספק "ממוקד פרטיות" (שאינו מיישם E2EE) לא פותר את הבעיה שלך: הוא פשוט מעביר את האמון מגוגל לספק הזה.

מדיניות הפרטיות והנהלים העסקיים של ספקים שאתה בוחר חשובים מאוד, אך יש להתייחס אליהם כמשניים להבטחות טכניות לפרטיות שלך: אל תעביר אמון לספק אחר כאשר אמון בספק אינו דרישה כלל.

## "מסובך זה יותר טוב"

לעתים קרובות אנחנו רואים אנשים שמתארים מודלים של איום על פרטיות שהם מורכבים מדי. לעתים קרובות, פתרונות אלה כוללים בעיות כמו חשבונות דוא"ל רבים ושונים או התקנות מסובכות עם הרבה העברת חלקים ותנאים. התשובות הן בדרך כלל תשובות לשאלה "מהי הדרך הטובה ביותר לעשות *X*?"

מציאת הפתרון ה"טוב ביותר" עבור עצמך לא אומר בהכרח שאתה מחפש פתרון שאין לו טעות עם עשרות תנאים - פתרונות אלו לרוב קשה לעבוד איתם באופן מציאותי. כפי שדיברנו בעבר, אבטחה לרוב באה במחיר של נוחות. בהמשך אנו מספקים כמה טיפים:

1. ==פעולות צריכות לשרת מטרה מסוימת:== תחשוב איך לעשות מה שאתה רוצה עם הכי פחות פעולות.
2. ==הסר נקודות כשל אנושיות:== אנחנו נכשלים, מתעייפים ושוכחים דברים. כדי לשמור על אבטחה, הימנע מהסתמכות על תנאים ותהליכים ידניים שאתה צריך לזכור.
3. ==השתמש ברמת ההגנה הנכונה עבור מה שאתה מתכוון.== לעתים קרובות אנו רואים המלצות על מה שנקרא פתרונות אכיפת חוק או הוכחת זימון. אלה דורשים לעתים קרובות ידע מומחה ובדרך כלל הם לא מה שאנשים רוצים. אין טעם לבנות מודל איום מורכב לאנונימיות אם ניתן בקלות לבטל את האנונימיות באמצעות פיקוח פשוט.

אז איך זה עשוי להיראות?

אחד מדגמי האיום המובהקים ביותר הוא כזה שבו אנשים *יודעים מי אתה* ואחד שבו הם לא יודעים. תמיד יהיו מצבים שבהם אתה חייב להצהיר על שמך החוקי ויש אחרים שבהם אתה לא צריך.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
