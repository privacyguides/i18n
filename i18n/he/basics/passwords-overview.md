---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

סיסמאות הן חלק חיוני מחיינו הדיגיטליים היומיומיים. אנו משתמשים בהם כדי להגן על החשבונות שלנו, המכשירים והסודות שלנו. למרות היותם לעתים קרובות הדבר היחיד בינינו לבין יריב שרודף אחרי המידע הפרטי שלנו, לא מושקעת בהם הרבה מחשבה, מה שמוביל לרוב לכך שאנשים משתמשים בסיסמאות שניתן לנחש בקלות או להכריח אותן.

## שיטות עבודה מומלצות

### השתמש בסיסמאות ייחודיות לכל שירות

תדמיין את זה; אתה נרשם לחשבון עם אותו אימייל וסיסמא במספר שירותים מקוונים. אם אחד מספקי השירותים האלה הוא זדוני, או שהשירות שלהם חווה פרצת מידע שחושפת את הסיסמה שלך בפורמט לא מוצפן, כל מה ששחקן גרוע יצטרך לעשות הוא לנסות את שילוב האימייל והסיסמה במספר שירותים פופולריים עד שהם מקבלים מכה. זה לא משנה כמה חזקה אותה סיסמה אחת, כי כבר יש להם אותה.

זה נקרא [מילוי אישורים](https://en.wikipedia.org/wiki/Credential_stuffing), וזו אחת הדרכים הנפוצות ביותר שבהן החשבונות שלך יכולים להיפגע על ידי שחקנים גרועים. כדי להימנע מכך, ודא שלעולם לא תעשה שימוש חוזר בסיסמאות שלך.

### השתמש בסיסמאות שנוצרות באקראי

==אתה **לעולם לא** צריך לסמוך על עצמך כדי למצוא סיסמה טובה.== אנו ממליצים להשתמש ב[סיסמאות שנוצרו באקראי](#passwords) או ב[ביטויי סיסמה של תוכנת קובייה](#diceware-passphrases) עם מספיק אנטרופיה כדי להגן על החשבונות והמכשירים שלך.

כל [מנהלי הסיסמאות המומלצים](../passwords.md) שלנו כוללים מחולל סיסמאות מובנה שתוכל להשתמש בו.

### סיסמאות מסתובבות

עליך להימנע משינוי סיסמאות שאתה צריך לזכור (כגון סיסמת האב של מנהל הסיסמאות שלך) לעתים קרובות מדי, אלא אם יש לך סיבה להאמין שהיא נפגעה, שכן שינוי שלה לעתים קרובות מדי חושף אותך לסיכון של שכחתה.

כשמדובר בסיסמאות שאינך חייב לזכור (כגון סיסמאות המאוחסנות בתוך מנהל הסיסמאות שלך), אם [מודל האיומים](threat-modeling.md) שלך דורש זאת, אנו ממליצים עוברים על חשבונות חשובים (במיוחד חשבונות שאינם משתמשים באימות רב-גורמי) ומשנים את הסיסמה שלהם כל חודשיים, למקרה שהם נפגעו בפרצת מידע שעדיין לא הפכה לציבורית. רוב מנהלי הסיסמאות מאפשרים לך להגדיר תאריך תפוגה לסיסמה שלך כדי להקל על הניהול שלה.

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

אם מנהל הסיסמאות שלך מאפשר לך לחפש סיסמאות שנפגעו, הקפד לעשות זאת ולשנות מיד כל סיסמה שאולי נחשפה בפרצת נתונים. לחלופין, תוכל לעקוב אחר [עדכון ההפרות האחרונות של have i been pwned'](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) בעזרת [מצבר חדשות](../news-aggregators.md).

</div>

## יצירת סיסמאות חזקות

### סיסמאות

שירותים רבים מטילים קריטריונים מסוימים בכל הנוגע לסיסמאות, כולל אורך מינימום או מקסימום, וכן באילו תווים מיוחדים, אם בכלל, ניתן להשתמש. עליך להשתמש במחולל הסיסמאות המובנה של מנהל הסיסמאות שלך כדי ליצור סיסמאות ארוכות ומורכבות ככל שהשירות יאפשר על ידי הכללת אותיות רישיות וקטנות, מספרים ותווים מיוחדים.

אם אתה צריך סיסמא שאתה יכול לשנן, אנו ממליצים על [משפט סיסמא לכלי הקוביות](#diceware-passphrases).

### ביטויי סיסמא של כלי קוביות

כלי קוביות היא שיטה ליצירת ביטויי סיסמה שקל לזכור, אבל קשה לנחש.

ביטויי סיסמה של כלי קוביות הם אפשרות מצוינת כאשר אתה צריך לשנן או להזין באופן ידני את האישורים שלך, כגון עבור סיסמת האב של מנהל הסיסמאות שלך או סיסמת ההצפנה של המכשיר שלך.

דוגמה לביטוי סיסמא של תוכנת קוביות היא `מהירות ניתנת לצפייה סרבן עיפרון מרוטש שבע עשרה מוצג`.

כדי ליצור ביטוי סיסמא של כלי קוביות באמצעות קוביות אמיתיות, בצע את השלבים הבאים:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. רשימות מילים אחרות עשויות לדרוש יותר או פחות גלגולים למילה, ועשויות לדרוש כמות שונה של מילים כדי להשיג את אותה אנטרופיה.

</div>

1. לזרוק קובייה בעלת שש צדדים חמש פעמים, לרשום את המספר לאחר כל גלגול.

2. כדוגמה, נניח שזרקת `2-5-2-6-6`. Look through the [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. אתה תמצא את המילה `להצפין`. כתוב את המילה הזו.

4. חזור על תהליך זה עד לביטוי הסיסמה שלך יש כמה מילים שאתה צריך, שאותן עליך להפריד ברווח.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

כדאי **לא** לגלגל מחדש מילים עד שתקבל שילוב של מילים שמושכות אותך. התהליך צריך להיות אקראי לחלוטין.

</div>

אם אין לך גישה או תעדיף לא להשתמש בקוביות אמיתיות, תוכל להשתמש במחולל הסיסמאות המובנה של מנהל הסיסמאות שלך, שכן לרובם יש אפשרות ליצור ביטויי סיסמה של תוכנת קוביות בנוסף לסיסמאות הרגילות.

We recommend using [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. יש גם [רשימות מילים אחרות בשפות שונות](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), אם אינך רוצה שביטוי הסיסמה שלך יהיה באנגלית.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

בממוצע, צריך לנסות 50% מכל השילובים האפשריים כדי לנחש את הביטוי שלך. עם זאת בחשבון, גם אם היריב שלך מסוגל ל-1,000,000,000,000 ניחושים בשנייה, עדיין ייקח לו ~27,255,689 שנים לנחש את משפט הסיסמה שלך. זה המצב גם אם הדברים הבאים נכונים:

- היריב שלך יודע שהשתמשת בשיטת קוביות.
- היריב שלך יודע את רשימת המילים הספציפית שבה השתמשת.
- היריב שלך יודע כמה מילים מכיל ביטוי הסיסמה שלך.

</details>

לסיכום, ביטויי סיסמה של תוכנת קוביות הם האפשרות הטובה ביותר שלך כאשר אתה צריך משהו שקל לזכור גם *ו* חזק במיוחד.

## אחסון סיסמאות

### מנהלי סיסמאות

הדרך הטובה ביותר לאחסן את הסיסמאות שלך היא באמצעות מנהל סיסמאות. הם מאפשרים לך לאחסן את הסיסמאות שלך בקובץ או בענן ולהגן עליהן באמצעות סיסמת אב אחת. בדרך זו, תצטרך לזכור רק סיסמה אחת חזקה, המאפשרת לך לגשת לשאר שלהן.

יש הרבה אפשרויות טובות לבחירה, הן מבוססות ענן והן מקומיות. בחר אחד ממנהלי הסיסמאות המומלצים שלנו והשתמש בו כדי ליצור סיסמאות חזקות בכל החשבונות שלך. אנו ממליצים לאבטח את מנהל הסיסמאות שלך באמצעות משפט סיסמה [של סכו"ם](#diceware-passphrases) המורכב משבע מילים לפחות.

[רשימת מנהלי סיסמאות מומלצים](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

בעת שימוש בקודי TOTP כ[אימות רב-גורמי](../multi-factor-authentication.md), שיטת האבטחה הטובה ביותר היא לשמור את קודי ה-TOTP שלך ב[אפליקציה נפרדת](../multi-factor-authentication.md#authenticator-apps).

אחסון אסימוני ה-TOTP שלך באותו מקום כמו הסיסמאות שלך, למרות שהוא נוח, מצמצם את החשבונות לגורם יחיד במקרה שיריב יקבל גישה למנהל הסיסמאות שלך.

יתר על כן, איננו ממליצים לאחסן קודי שחזור חד-פעמיים במנהל הסיסמאות שלך. יש לאחסן אותם בנפרד, כגון במיכל מוצפן בהתקן אחסון לא מקוון.

</div>

### גיבויים

עליך לאחסן גיבוי [מוצפן](../encryption.md) של הסיסמאות שלך במספר התקני אחסון או בספק אחסון בענן. זה יכול לעזור לך לגשת לסיסמאות שלך אם משהו קורה למכשיר הראשי שלך או לשירות שבו אתה משתמש.
