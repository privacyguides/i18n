---
title: "איומים נפוצים"
icon: 'material/eye-outline'
description: מודל האיום שלך הוא אישי עבורך, אך אלו הם חלק מהדברים שמהם אכפת למבקרים רבים באתר זה.
---

באופן כללי, אנו מסווגים את ההמלצות שלנו ל[איומים](threat-modeling.md) או יעדים שחלים על רוב האנשים. ==ייתכן שאתה מודאג מאף אחת, אחת, כמה, או מכל האפשרויות האלה==, והכלים והשירותים שבהם אתה משתמש תלויים במטרותיך. ייתכן שיש לך איומים ספציפיים גם מחוץ לקטגוריות האלה, וזה בסדר גמור! החלק החשוב הוא פיתוח הבנה של היתרונות והחסרונות של הכלים שבהם אתה בוחר להשתמש, כי למעשה אף אחד מהם לא יגן עליך מכל איום.

- <span class="pg-purple">:material-incognito: אנונימיות</span> - הגנה על הפעילות המקוונת שלך מהזהות האמיתית שלך, הגנה עליך מפני אנשים שמנסים לחשוף את הזהות *שלך* ספציפית.
- <span class="pg-red">:material-target-account: התקפות ממוקדות</span> - הגנה מפני האקרים או שחקנים זדוניים אחרים שמנסים לקבל גישה לנתונים או מכשירים ספציפיים *שלך*.
- <span class="pg-orange">:material-bug-outline: התקפות פסיביות</span> - הגנה מפני דברים כמו תוכנות זדוניות, פרצות נתונים והתקפות אחרות שנעשות נגד אנשים רבים בו-זמנית.
- <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> - A vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.
- <span class="pg-teal">:material-server-network: ספקי שירותים</span> - הגנה על הנתונים שלך מפני ספקי שירות (למשל באמצעות E2EE, מה שהופך את הנתונים שלך לבלתי קריאים לשרת).
- <span class="pg-blue">:material-eye-outline: מעקב המוני</span> - הגנה מפני סוכנויות ממשלתיות, ארגונים, אתרים ושירותים הפועלים יחד כדי לעקוב אחר הפעילויות שלך.
- <span class="pg-brown">:material-account-cash: קפיטליזם מעקב</span> - הגנה על עצמך מפני רשתות פרסום גדולות, כמו גוגל ופייסבוק, כמו גם ממספר עצום של אוספי נתונים אחרים של צד שלישי.
- <span class="pg-green">:material-account-search: חשיפה ציבורית</span> - הגבלת המידע אודותיך הנגיש באינטרנט - למנועי חיפוש או לציבור הרחב.
- <span class="pg-blue-gray">:material-close-outline: צנזורה</span> - הימנעות מגישה מצונזרת למידע או מצונזר בעצמך כשאתה מדבר באינטרנט.

חלק מהאיומים הללו עשויים להיות חשובים לך יותר מאחרים, בהתאם לדאגות הספציפיות שלך. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. באופן דומה, אנשים רבים עשויים להיות מודאגים בעיקר מ<span class="pg-green">:material-account-search: חשיפה ציבורית</span> של הנתונים האישיים שלהם, אך הם עדיין צריכים להיזהר מבעיות ממוקדות אבטחה, כגון <span class="pg-orange">:material-bug-outline: התקפות פסיביות</span>—כמו תוכנות זדוניות המשפיעות על המכשירים שלהם.

## אנונימיות מול פרטיות

<span class="pg-purple">:material-incognito: אנונימיות</span>

אנונימיות מבולבלת לעתים קרובות עם פרטיות, אבל הם מושגים נפרדים. בעוד שפרטיות היא קבוצה של בחירות שאתה עושה לגבי אופן השימוש והשיתוף בנתונים שלך, אנונימיות היא ניתוק מוחלט של הפעילויות המקוונות שלך מזהותך האמיתית.

לחושפי שחיתויות ועיתונאים, למשל, יכול להיות מודל איום הרבה יותר קיצוני הדורש אנונימיות מוחלטת. זה לא רק להסתיר את מה שהם עושים, אילו נתונים יש להם, ולא להיפרץ על ידי שחקנים זדוניים או ממשלות, אלא גם להסתיר את מי שהם לגמרי. לעתים קרובות הם יקריבו כל סוג של נוחות אם זה אומר להגן על האנונימיות, הפרטיות או האבטחה שלהם, מכיוון שחייהם עשויים להיות תלויים בכך. רוב האנשים לא צריכים ללכת כל כך רחוק.

## אבטחה ופרטיות

<span class="pg-orange">:material-bug-outline: התקפות פסיביות</span>

גם אבטחה ופרטיות מתבלבלים לעתים קרובות, מכיוון שאתה זקוק לאבטחה כדי להשיג כל מראית עין של פרטיות: השימוש בכלים - גם אם הם פרטיים בעיצובם - הוא חסר תועלת אם הם יכולים להיות מנוצלים בקלות על ידי תוקפים שישחררו מאוחר יותר את הנתונים שלך. עם זאת, ההיפך אינו בהכרח נכון: השירות המאובטח ביותר בעולם *אינו בהכרח* פרטי. הדוגמה הטובה ביותר לכך היא מתן אמון בנתונים לגוגל, שבהתחשב בהיקף שלהם, היו מעט תקריות אבטחה על ידי העסקת מומחי אבטחה מובילים בתעשייה כדי לאבטח את התשתית שלהם. למרות שגוגל מספקת שירותים מאובטחים מאוד, מעט מאוד אנשים יחשבו שהנתונים שלהם פרטיים במוצרי הצריכה החינמיים של גוגל (Gmail, יוטיוב וכו')

כשזה מגיע לאבטחת יישומים, אנחנו בדרך כלל לא יודעים (ולפעמים גם לא יכולים) לדעת אם התוכנה שבה אנו משתמשים היא זדונית, או עלולה להפוך יום אחד לזדונית. אפילו עם המפתחים המהימנים ביותר, בדרך כלל אין ערובה לכך שלתוכנה שלהם אין פגיעות רצינית שניתן לנצל מאוחר יותר.

כדי למזער את הנזק שתוכנה זדונית *עלולה* לגרום, עליך להפעיל אבטחה על ידי מידור. לדוגמה, זה יכול לבוא בצורה של שימוש במחשבים שונים לעבודות שונות, שימוש במכונות וירטואליות כדי להפריד בין קבוצות שונות של יישומים קשורים, או שימוש במערכת הפעלה מאובטחת עם התמקדות חזקה בארגז חול של יישומים ובקרת גישה חובה.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

למערכות הפעלה מובייל יש בדרך כלל ארגז חול טוב יותר לאפליקציות מאשר למערכות הפעלה שולחניות: אפליקציות אינן יכולות לקבל גישת שורש, ודורשות הרשאה לגישה למשאבי המערכת.

מערכות הפעלה שולחניות בדרך כלל מפגרות עם ארגז חול נכון. ל-ChromeOS יש יכולות ארגז חול דומות לאנדרואיד, ול-macOS יש בקרת הרשאות מערכת מלאה (ומפתחים יכולים להצטרף לארגזי חול עבור יישומים). עם זאת, מערכות הפעלה אלו אכן משדרות מידע מזהה ליצרני ה-OEM שלהם. לינוקס נוטה לא לשלוח מידע לספקי מערכות, אך יש לה הגנה גרועה מפני ניצול ואפליקציות זדוניות. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

<span class="pg-red">:material-target-account: התקפות ממוקדות</span>

התקפות ממוקדות נגד אדם ספציפי הן בעייתיות יותר להתמודדות. התקפות נפוצות כוללות שליחת מסמכים זדוניים באמצעות מייל, ניצול פגיעויות (למשל בדפדפנים ובמערכות הפעלה) והתקפות פיזיות. אם זה מדאיג אותך, עליך להשתמש באסטרטגיות מתקדמות יותר להפחתת איומים.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

לפי התכנון, **דפדפני אינטרנט**, **לקוחות אימייל** ו**יישומי משרד** מריצים בדרך כלל קוד לא מהימן, שנשלח אליך מצדדים שלישיים. הפעלת מספר מכונות וירטואליות - כדי להפריד יישומים כמו אלה מהמערכת המארחת שלך, כמו גם אחד מהשני - היא טכניקה אחת שבה תוכל להשתמש כדי להפחית את הסיכוי של ניצול ביישומים אלה שיפגע בשאר המערכת שלך. לדוגמה, טכנולוגיות כמו Qubes OS או Microsoft Defender Application Guard ב-Windows מספקות שיטות נוחות לעשות זאת.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). עליך גם לוודא שהכונן שלך מוצפן ושמערכת ההפעלה משתמשת ב-TPM או ב-Secure [מובלע](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) או [אלמנט](https://developers.google.com/android/security/android-ready-se) כדי להגביל ניסיונות להזין את ביטוי הסיסמה להצפנה. עליך להימנע משיתוף המחשב שלך עם אנשים שאינך סומך עליהם, מכיוון שרוב מערכות ההפעלה שולחניות אינן מצפינות נתונים בנפרד לכל משתמש.

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might work their way into a position of power within a project or organization, then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what the change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enable undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## פרטיות מספקי שירות

<span class="pg-teal">:material-server-network: ספקי שירות</span>

אנחנו חיים בעולם שבו כמעט הכל מחובר לאינטרנט. ההודעות ה"פרטיות" שלנו, המיילים והאינטראקציות החברתיות שלנו מאוחסנים בדרך כלל בשרת, איפשהו. בדרך כלל, כאשר אתה שולח למישהו הודעה היא מאוחסנת בשרת, וכאשר חבר שלך רוצה לקרוא את ההודעה השרת יראה לו אותה.

הבעיה הברורה עם זה היא שספק השירות (או האקר שפגע בשרת) יכול לגשת לשיחות שלך מתי ואיך שהם רוצים, בלי שאתה אי פעם יודע. זה חל על שירותים נפוצים רבים, כמו הודעות SMS, טלגרם ודיסקורד.

למרבה המזל, E2EE יכול להקל על בעיה זו על ידי הצפנת התקשורת בינך לבין הנמענים הרצויים שלך לפני שהם בכלל נשלחים לשרת. סודיות ההודעות שלך מובטחת, בהנחה שלספק השירות אין גישה למפתחות הפרטיים של אף אחד מהצדדים.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

בפועל, היעילות של יישומי E2EE שונים משתנה. אפליקציות, כגון [Signal](../real-time-communication.md#signal), פועלות באופן מקורי במכשיר שלך, וכל עותק של האפליקציה זהה בהתקנות שונות. אם ספק השירות היה מציג [דלת אחורית](https://en.wikipedia.org/wiki/Backdoor_(computing)) באפליקציה שלו - בניסיון לגנוב את המפתחות הפרטיים שלך - ניתן היה לזהות אותו מאוחר יותר באמצעות [הפוך הנדסה](https://en.wikipedia.org/wiki/Reverse_engineering).

מצד שני, יישומי E2EE מבוססי אינטרנט, כמו דואר האינטרנט של Proton Mail או *כספת האינטרנט* של Bitwarden, מסתמכים על השרת שמגיש באופן דינמי קוד JavaScript לדפדפן כדי לטפל בהצפנה. שרת זדוני יכול למקד אותך ולשלוח לך קוד JavaScript זדוני כדי לגנוב את מפתח ההצפנה שלך (והיה קשה מאוד לשים לב אליו). מכיוון שהשרת יכול לבחור לשרת לקוחות אינטרנט שונים לאנשים שונים - גם אם שמתם לב להתקפה - יהיה קשה מאוד להוכיח את אשמתו של הספק.

לכן, עליך להשתמש ביישומים מקוריים על פני לקוחות אינטרנט במידת האפשר.

</div>

אפילו עם E2EE, ספקי שירות עדיין יכולים ליצור פרופיל שלך על סמך **מטא נתונים**, שבדרך כלל אינם מוגנים. למרות שספק השירות לא יכול לקרוא את ההודעות שלך, הוא עדיין יכול לראות דברים חשובים, כגון עם מי אתה מדבר, באיזו תדירות אתה שולח להם הודעות ומתי אתה פעיל בדרך כלל. הגנה על מטא נתונים היא נדירה למדי, ואם היא ב[מודל האיום](threat-modeling.md) שלך - עליך לשים לב היטב לתיעוד הטכני של התוכנה שבה אתה משתמש כדי לראות אם יש מזעור או הגנה של מטא נתונים בכלל.

## תוכניות מעקב המוני

<span class="pg-blue">:material-eye-outline: מעקב המוני</span>

מעקב המוני הוא המאמץ המורכב לנטר את "ההתנהגות, הפעילויות הרבות או המידע" של אוכלוסייה שלמה (או חלק ניכר מאוכלוסיה).[^1] לעתים קרובות זה מתייחס לתוכניות ממשלתיות, כגון אלו [נחשף על ידי אדוארד סנודן ב-2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). עם זאת, זה יכול להתבצע גם על ידי תאגידים, בין אם מטעם סוכנויות ממשלתיות או ביוזמתם.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

ממשלות לעתים קרובות מצדיקות תוכניות מעקב המוניות כאמצעים הכרחיים למאבק בטרור ולמניעת פשע. עם זאת, תוך הפרת זכויות אדם, הוא משמש לרוב כדי למקד באופן לא פרופורציונלי קבוצות מיעוט ומתנגדים פוליטיים, בין היתר.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

אל מול [חשיפותיו של אדוארד סנודן לגבי תוכניות ממשלתיות כגון [PRISM](https://en.wikipedia.org/wiki/PRISM) ו-[Upstream](https://en.wikipedia.org/wiki/Upstream_collection)], פקידי מודיעין גם הודו כי ה-NSA במשך שנים אספה בחשאי תיעוד על כמעט כל שיחות טלפון של כל אמריקאי - מי מתקשר למי, מתי השיחות הללו מבוצעות וכמה זמן הן נמשכות. מידע מסוג זה, כאשר הוא נצבר על ידי ה-NSA יום אחר יום, יכול לחשוף פרטים רגישים להפליא על חייהם והאסוציאציות של אנשים, כגון האם הם התקשרו לכומר, מטפל בהפלות, ליועצת להתמכרות או למוקד התאבדות.

</div>

למרות המעקב ההמוני הגובר בארצות הברית, הממשלה מצאה שלתוכניות מעקב המוני כמו סעיף 215 היה "ערך ייחודי מועט" ביחס לעצירת פשעים או מזימות טרור בפועל, כאשר מאמצים משכפלים במידה רבה את תוכניות המעקב הממוקדות של ה-FBI עצמו.[^2]

באינטרנט, ניתן לעקוב אחריך במגוון שיטות:

- כתובת ה-IP שלך
- עוגיות דפדפן
- הנתונים שאתה מוסר לאתרים
- טביעת האצבע של הדפדפן או המכשיר שלך
- מתאם שיטת תשלום

\[רשימה זו אינה ממצה].

אם אתה מודאג לגבי תוכניות מעקב המוני, אתה יכול להשתמש באסטרטגיות כמו מידור של הזהויות המקוונות שלך, השתלבות עם משתמשים אחרים, או, במידת האפשר, פשוט הימנעות מסירת מידע מזהה.

<span class="pg-brown">:material-account-cash: קפיטליזם מעקב</span>

> קפיטליזם מעקב הוא שיטה כלכלית המרוכזת סביב לכידה וסחורה של נתונים אישיים למטרת הליבה של עשיית רווחים.[^3]

עבור אנשים רבים, מעקב ומעקב על ידי תאגידים פרטיים הם דאגה גוברת. רשתות מודעות נרחבות, כמו אלו המופעלות על ידי גוגל ופייסבוק, משתרעות על האינטרנט הרבה מעבר לאתרים שהם שולטים בהם, ועוקבות אחר הפעולות שלך לאורך הדרך. שימוש בכלים כמו חוסמי תוכן כדי להגביל את בקשות הרשת לשרתים שלהם, וקריאת מדיניות הפרטיות של השירותים שבהם אתה משתמש יכול לעזור לך למנוע יריבים בסיסיים רבים (אם כי זה לא יכול למנוע לחלוטין מעקב).[^4]

בנוסף, אפילו חברות מחוץ ל*AdTech* או תעשיית המעקב יכולות לשתף את המידע שלך עם [מתווכי נתונים](https://en.wikipedia.org/wiki/Information_broker) (כגון Cambridge Analytica, Experian או Datalogix) או גורמים אחרים. אתה לא יכול להניח אוטומטית שהנתונים שלך בטוחים רק בגלל שהשירות שבו אתה משתמש אינו נופל במסגרת המודל העסקי הטיפוסי של AdTech או מעקב. ההגנה החזקה ביותר מפני איסוף נתונים תאגידי היא הצפנת או ערפול הנתונים שלך בכל עת אפשרי, מה שמקשה על ספקים שונים לתאם נתונים זה עם זה ולבנות עליך פרופיל.

## הגבלת מידע ציבורי

<span class="pg-green">:material-account-search: חשיפה ציבורית</span>

הדרך הטובה ביותר לשמור על פרטיות הנתונים שלך היא פשוט לא להפוך אותם לציבוריים מלכתחילה. מחיקת מידע לא רצוי שמצאת על עצמך באינטרנט היא אחד הצעדים הראשונים הטובים ביותר שתוכל לנקוט כדי להחזיר את הפרטיות שלך.

- [עיין במדריך שלנו על מחיקת חשבון :material-arrow-right-drop-circle:](account-deletion.md)

באתרים שבהם אתה כן משתף מידע, חשוב מאוד לבדוק את הגדרות הפרטיות של חשבונך כדי להגביל את הפצת הנתונים הללו. לדוגמה, הפעל "מצב פרטי" בחשבונות שלך אם ניתנת לך האפשרות: זה מבטיח שהחשבון שלך לא מתווסף לאינדקס על ידי מנועי חיפוש, ושלא ניתן לצפות בו ללא רשותך.

אם כבר שלחת את המידע האמיתי שלך לאתרים שלא אמורים להיות בהם, שקול להשתמש בטקטיקות של דיסאינפורמציה, כמו שליחת מידע פיקטיבי הקשור לזהות מקוונת זו. זה הופך את המידע האמיתי שלך לבלתי ניתן להבחין מהמידע השקרי.

## הימנעות מצנזורה

<span class="pg-blue-gray">:material-close-outline: צנזורה</span>

צנזורה מקוונת יכולה להתבצע (בדרגות שונות) על ידי שחקנים כולל ממשלות טוטליטריות, מנהלי רשתות וספקי שירותים. מאמצים אלה לשלוט בתקשורת ולהגביל את הגישה למידע תמיד יהיו בלתי עולים בקנה אחד עם זכות האדם לחופש הביטוי.[^5]

צנזורה על פלטפורמות ארגוניות נפוצה יותר ויותר, שכן פלטפורמות כמו טוויטר ופייסבוק נכנעות לדרישת הציבור, לחצי השוק וללחצים של סוכנויות ממשלתיות. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

אנשים המודאגים מהאיום של צנזורה יכולים להשתמש בטכנולוגיות כמו [Tor](../advanced/tor-overview.md) כדי לעקוף אותו, ולתמוך בפלטפורמות תקשורת עמידות לצנזורה כמו [Matrix](../real-time-communication.md#element), שאין לה סמכות חשבון מרכזית יכול לסגור חשבונות באופן שרירותי.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

למרות שהתחמקות מצנזורה עצמה יכולה להיות קלה, הסתרת העובדה שאתה עושה זאת יכולה להיות מאוד בעייתית.

עליך לשקול באילו היבטים של הרשת יריבך יכול לצפות, והאם יש לך הכחשה סבירה למעשיך. לדוגמה, שימוש ב-[DNS מוצפן](../advanced/dns-overview.md#what-is-encrypted-dns) יכול לעזור לך לעקוף מערכות צנזורה בסיסיות ומבוססות DNS, אבל זה לא באמת יכול להסתיר את מה שאתה ביקור מ-ISP שלך. VPN או Tor יכולים לעזור להסתיר את מה שאתה מבקר ממנהלי רשת, אבל לא יכולים להסתיר שאתה משתמש ברשתות האלה מלכתחילה. העברות ניתנות לחיבור (כגון Obfs4proxy, Meek או Shadowsocks) יכולים לעזור לך להתחמק מחומת אש שחוסמת פרוטוקולי VPN נפוצים או Tor, אך עדיין ניתן לזהות את ניסיונות העקיפה שלך בשיטות כמו בדיקה או [בדיקת מנות עמוקה](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

אתה חייב תמיד לשקול את הסיכונים בניסיון לעקוף את הצנזורה, את ההשלכות האפשריות ועד כמה מתוחכם עלול להיות היריב שלך. אתה צריך להיות זהיר בבחירת התוכנה שלך, ולהכין תוכנית גיבוי למקרה שתיתפס.

[^1]: ויקיפדיה: [*מעקבים המונים*](https://en.wikipedia.org/wiki/Mass_surveillance) ו[*מעקבים*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: מועצת הפיקוח על הפרטיות וחירויות האזרח של ארצות הברית: [*דיווח על תוכנית רישומי הטלפון שנערכה לפי סעיף 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: ויקיפדיה: [*מעקב קפיטליזם*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. אתה צריך גם להשתמש בטכניקות הפחתה אחרות.
[^5]: האומות המאוחדות: [*הכרזה אוניברסלית על זכויות אדם*](https://www.un.org/en/about-us/universal-declaration-of-human-rights).
