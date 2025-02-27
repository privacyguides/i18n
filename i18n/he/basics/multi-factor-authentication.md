---
title: "Multifactor Authentication"
icon: 'material/two-factor-authentication'
description: MFA הוא מנגנון אבטחה קריטי לאבטחת החשבונות המקוונים שלך, אך שיטות מסוימות חזקות יותר מאחרות.
---

**Multifactor Authentication** (**MFA**) is a security mechanism that requires additional steps beyond entering your username (or email) and password. השיטה הנפוצה ביותר היא קודים מוגבלים בזמן שאתה עשוי לקבל מ-SMS או מאפליקציה.

בדרך כלל, אם האקר (או יריב) מסוגל להבין את הסיסמה שלך, הם יקבלו גישה לחשבון שאליו שייכת הסיסמה. חשבון עם MFA מאלץ את ההאקר להחזיק גם את הסיסמה (משהו שאתה *יודע*) וגם מכשיר שבבעלותך (משהו שיש *לך*), כמו הטלפון שלך.

שיטות MFA משתנות באבטחה, אך מבוססות על ההנחה שככל שקשה יותר לתוקף לקבל גישה לשיטת ה-MFA שלך, כך ייטב. דוגמאות לשיטות MFA (מהחלש ביותר לחזק ביותר) כוללות SMS, קודי דואר אלקטרוני, הודעות דחיפה של אפליקציה, TOTP, Yubico OTP ו-FIDO.

## השוואת שיטות MFA

### SMS או אימייל MFA

קבלת קודי OTP באמצעות SMS או דואר אלקטרוני הם אחת הדרכים החלשות לאבטח את החשבונות שלך עם MFA. השגת קוד באימייל או ב-SMS מונעת מהרעיון "משהו ש*יש לך*", מכיוון שיש מגוון דרכים שההאקר יכול[להשתלט על מספר הטלפון שלך](https://en.wikipedia.org/wiki/SIM_swap_scam) או קבלת גישה לאימייל שלך מבלי שתהיה לך גישה פיזית לאף אחד מהמכשירים שלך כלל. אם אדם לא מורשה קיבל גישה לדוא"ל שלך, הוא יוכל להשתמש בגישה זו כדי לאפס את הסיסמה שלך ולקבל את קוד האימות, ולהעניק לו גישה מלאה לחשבון שלך.

### התראות דחיפה

הודעת דחיפה MFA לובשת צורה של הודעה שנשלחת לאפליקציה בטלפון שלך המבקשת ממך לאשר כניסות לחשבון חדש. שיטה זו טובה בהרבה מ-SMS או דואר אלקטרוני, מכיוון שתוקף בדרך כלל לא יוכל לקבל את הודעות הדחיפה הללו מבלי שיהיה לו מכשיר מחובר כבר, מה שאומר שהוא יצטרכו להתפשר תחילה על אחד מהמכשירים האחרים שלך.

כולנו עושים טעויות, וקיים סיכון שאתה עלול לקבל את ניסיון הכניסה בטעות. הרשאות התחברות להודעות דחיפה נשלחות בדרך כלל ל*כל* המכשירים שלך בבת אחת, מה שמרחיב את הזמינות של קוד ה-MFA אם יש לך מכשירים רבים.

האבטחה של הודעת דחיפה MFA תלויה הן באיכות האפליקציה, ברכיב השרת והן באמון של המפתח שמייצר אותה. התקנת אפליקציה עשויה גם לדרוש ממך לקבל הרשאות פולשניות המעניקות גישה לנתונים אחרים במכשיר שלך. אפליקציה בודדת דורשת גם שתהיה לך אפליקציה ספציפית עבור כל שירות, אשר עשויה שלא לדרוש סיסמה לפתיחה, בשונה מיישום מחולל TOTP טוב.

### סיסמה חד פעמית מבוססת זמן (TOTP)

TOTP היא אחת הצורות הנפוצות ביותר של MFA. כאשר אתה מגדיר TOTP, אתה בדרך כלל נדרש לסרוק קוד QR [](https://en.wikipedia.org/wiki/QR_code) אשר קובע "[סוד משותף](https://en.wikipedia.org/wiki/Shared_secret)" עם השירות שבו אתה מתכוון להשתמש. The shared secret is secured inside the authenticator app's data, and is sometimes protected by a password.

לאחר מכן, הקוד המוגבל בזמן נגזר מהסוד המשותף ומהזמן הנוכחי. מאחר שהקוד תקף לזמן קצר בלבד, ללא גישה לסוד המשותף, היריב אינו יכול ליצור קודים חדשים.

If you have a hardware security key with TOTP support (such as a YubiKey with [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)), we recommend that you store your "shared secrets" on the hardware. חומרה כגון YubiKey פותחה מתוך כוונה להקשות על החילוץ וההעתקה של "הסוד המשותף". YubiKey גם לא מחובר לאינטרנט, בניגוד לטלפון עם אפליקציית TOTP.

שלא כמו [WebAuthn](#fido-fast-identity-online), TOTP אינו מציע הגנה מפני [דיוג](https://en.wikipedia.org/wiki/Phishing) או שימוש חוזר בהתקפות. אם יריב משיג ממך קוד חוקי, הוא רשאי להשתמש בו כמה פעמים שירצה עד שתוקפו יפוג (בדרך כלל 60 שניות).

יריב יכול להקים אתר כדי לחקות שירות רשמי בניסיון להערים עליך למסור את שם המשתמש, הסיסמה וקוד ה-TOTP הנוכחי שלך. אם היריב ישתמש באותם אישורים מוקלטים, ייתכן שהוא יוכל להיכנס לשירות האמיתי ולחטוף את החשבון.

Although not perfect, TOTP is secure enough for most people, and when [hardware security keys](../security-keys.md) are not supported [authenticator apps](../multi-factor-authentication.md) are still a good option.

### מפתחות אבטחת חומרה

ה-YubiKey מאחסן נתונים על שבב מוצק עמיד בפני חבלה ש[אי אפשר לגשת](https://security.stackexchange.com/a/245772) ללא הרס ללא תהליך יקר ו מעבדה לזיהוי פלילי.

מפתחות אלה הם בדרך כלל רב-פונקציונליים ומספקים מספר שיטות לאימות. להלן הנפוצים ביותר.

#### Yubico OTP

Yubico OTP הוא פרוטוקול אימות המיושם בדרך כלל במפתחות אבטחה של חומרה. כאשר תחליט להשתמש ב-Yubico OTP, המפתח יפיק מזהה ציבורי, מזהה פרטי ומפתח סודי אשר יועלה לאחר מכן לשרת Yubico OTP.

בעת כניסה לאתר, כל מה שאתה צריך לעשות הוא לגעת פיזית במפתח האבטחה. מפתח האבטחה יחקה מקלדת וידפיס סיסמה חד פעמית בשדה הסיסמה.

מפתח האבטחה יחקה מקלדת וידפיס סיסמה חד פעמית בשדה הסיסמה. מונה מוגדל הן במפתח והן בשרת האימות של Yubico. ניתן להשתמש ב-OTP רק פעם אחת, וכאשר מתרחש אימות מוצלח, המונה מוגדל אשר מונע שימוש חוזר ב-OTP. Yubico מספקת [מסמך מפורט](https://developers.yubico.com/OTP/OTPs_Explained.html) על התהליך.

<figure markdown>
  ![Yubico OTP](../assets/img/multi-factor-authentication/yubico-otp.png)
</figure>

ישנם כמה יתרונות וחסרונות לשימוש ב-Yubico OTP בהשוואה ל-TOTP.

שרת האימות של Yubico הוא שירות מבוסס ענן, ואתה סומך על Yubico שהם מאחסנים נתונים בצורה מאובטחת ולא עושים לך פרופיל. המזהה הציבורי המשויך ל-Yubico OTP נמצא בשימוש חוזר בכל אתר ויכול להיות דרך נוספת עבור צדדים שלישיים ליצור פרופיל שלך. כמו TOTP, Yubico OTP אינו מספק עמידות להתחזות.

אם מודל האיום שלך דורש ממך זהויות שונות באתרי אינטרנט שונים, **אל** תשתמש ב-Yubico OTP עם אותו מפתח אבטחת חומרה בכל אתרים אלה, שכן מזהה ציבורי הוא ייחודי לכל אבטחה מַפְתֵחַ.

#### FIDO (זיהוי מהיר באינטרנט)

אם מודל האיומים שלך דורש ממך זהויות שונות באתרים שונים, חזק **אל תשתמש **ב- Yubico OTP עם אותו מפתח אבטחת חומרה באתרים אלה מכיוון שמזהה ציבורי הוא ייחודי לכל מפתח אבטחה.

U2F ו - FIDO2 מתייחסים ל - [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol), שהוא הפרוטוקול בין מפתח האבטחה למחשב, כגון מחשב נייד או טלפון. זה משלים את WebAuthn שהוא הרכיב המשמש לאימות עם האתר ("הצד המסתמך") שאליו אתה מנסה להיכנס.

WebAuthn היא הצורה המאובטחת והפרטית ביותר של אימות גורם שני. בעוד שחווית האימות דומה ל-Yubico OTP, המפתח אינו מדפיס סיסמה חד פעמית ומאמת עם שרת של צד שלישי. במקום זאת, הוא משתמש ב[הצפנת מפתח ציבורי](https://en.wikipedia.org/wiki/Public-key_cryptography) לצורך אימות.

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

כאשר אתה יוצר חשבון, המפתח הציבורי נשלח לשירות, לאחר מכן בעת הכניסה, השירות ידרוש ממך "לחתום" על נתונים מסוימים עם המפתח הפרטי שלך. היתרון של זה הוא ששום סיסמה לא מאוחסנת על ידי השירות, כך שאין ליריב שום דבר לגנוב.

This presentation discusses the history of password authentication, the pitfalls (such as password reuse), and the standards for FIDO2 and [WebAuthn](https://webauthn.guide):

- [How FIDO2 and WebAuthn Stop Account Takeovers](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

ל-FIDO2 ול-WebAuthn יש מאפייני אבטחה ופרטיות מעולים בהשוואה לכל שיטות MFA.

Typically, for web services it is used with WebAuthn which is a part of the [W3C recommendations](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC)). הוא משתמש באימות מפתח ציבורי והוא מאובטח יותר מאשר סודות משותפים המשמשים בשיטות Yubico OTP ו-TOTP, מכיוון שהוא כולל את שם המקור (בדרך כלל, שם התחום) במהלך האימות. אישור מסופק כדי להגן עליך מפני התקפות דיוג, מכיוון שהוא עוזר לך לקבוע שאתה משתמש בשירות האותנטי ולא בעותק מזויף.

שלא כמו Yubico OTP, WebAuthn אינו משתמש בשום מזהה ציבורי, כך שהמפתח **לא** ניתן לזיהוי באתרים שונים. הוא גם לא משתמש בשרת ענן של צד שלישי לאימות. כל התקשורת הושלמה בין המפתח לאתר שאליו אתה נכנס. FIDO משתמשת גם במונה שמוגדל עם השימוש על מנת למנוע שימוש חוזר בהפעלה ומפתחות משובטים.

אם אתר אינטרנט או שירות תומכים ב-WebAuthn עבור האימות, מומלץ מאוד להשתמש בו על פני כל צורה אחרת של MFA.

## המלצות כלליות

יש לנו את ההמלצות הכלליות הבאות:

### באיזו שיטה עלי להשתמש?

בעת הגדרת שיטת ה - MFA שלך, זכור שהיא מאובטחת כמו שיטת האימות החלשה ביותר שבה אתה משתמש. לכן, חשוב להשתמש בשיטת ה - MFA הטובה ביותר. לדוגמה, אם אתה כבר משתמש ב - TOTP, עליך להשבית דואר אלקטרוני ו - SMS MFA. אם אתה כבר משתמש ב-FIDO2/WebAuthn, אתה לא אמור להשתמש ב-Yubico OTP או TOTP בחשבון שלך.

### גיבויים

תמיד אמורים להיות לך גיבויים לשיטת ה-MFA שלך. מפתחות אבטחה של חומרה יכולים ללכת לאיבוד, להיגנב או פשוט להפסיק לעבוד עם הזמן. מומלץ שיהיה לך זוג מפתחות אבטחה חומרה עם אותה גישה לחשבונות שלך במקום רק אחד.

When using TOTP with an authenticator app, be sure to back up your recovery keys or the app itself, or copy the "shared secrets" to another instance of the app on a different phone or to an encrypted container (e.g. [VeraCrypt](../encryption.md#veracrypt-disk)).

### הגדרה ראשונית

בעת רכישת מפתח אבטחה, חשוב שתשנה את אישורי ברירת המחדל, תגדיר הגנה באמצעות סיסמה עבור המפתח ותפעיל אישור מגע אם המפתח שלך תומך בכך. למוצרים כגון YubiKey יש ממשקים מרובים עם אישורים נפרדים לכל אחד מהם, כך שכדאי לעבור על כל ממשק ולהגדיר גם הגנה.

### אימייל ו-SMS

אם אתה צריך להשתמש באימייל עבור MFA, ודא שחשבון האימייל עצמו מאובטח בשיטת MFA נכונה.

אם אתה משתמש ב-SMS MFA, השתמש בספק שלא יחליף את מספר הטלפון שלך לכרטיס SIM חדש ללא גישה לחשבון, או השתמש במספר VoIP ייעודי מספק עם אבטחה דומה כדי להימנע מ[התקפת חילופי SIM](https://en.wikipedia.org/wiki/SIM_swap_scam).

[כלי MFA שאנו ממליצים עליהם](../multi-factor-authentication.md ""){.md-button}

## מקומות נוספים להגדרת MFA

Beyond just securing your website logins, multifactor authentication can be used to secure your local logins, SSH keys or even password databases as well.

### macOS

ל - macOS יש [תמיכה מקומית](https://support.apple.com/guide/deployment/intro-to-smart-card-integration-depd0b888248/web) לאימות עם כרטיסים חכמים (PIV). If you have a smart card or a hardware security key that supports the PIV interface such as the YubiKey, we recommend that you follow your smart card or hardware security vendor's documentation and set up second factor authentication for your macOS computer.

Yubico have a guide [Using Your YubiKey as a Smart Card in macOS](https://support.yubico.com/hc/articles/360016649059) which can help you set up your YubiKey on macOS.

After your smart card/security key is set up, we recommend running this command in the Terminal:

```text
sudo defaults write /Library/Preferences/com.apple.loginwindow DisableFDEAutoLogin -bool YES
```

הפקודה תמנע מיריב לעקוף את MFA כאשר המחשב מאתחל.

### לינוקס

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

אם שם המארח של המערכת שלך משתנה (כגון עקב DHCP), לא תוכל להתחבר. חיוני להגדיר שם מארח מתאים למחשב שלך לפני ביצוע מדריך זה.

</div>

מודול `pam_u2f` ב-Linux יכול לספק אימות דו-גורמי לכניסה לרוב ההפצות הפופולריות של לינוקס. אם יש לך מפתח אבטחת חומרה התומך ב-U2F, תוכל להגדיר אימות MFA עבור הכניסה שלך. Yubico has a guide [Ubuntu Linux Login Guide - U2F](https://support.yubico.com/hc/articles/360016649099-Ubuntu-Linux-Login-Guide-U2F) which should work on any distribution. הפקודות של מנהל החבילות - כגון `apt-get` - ושמות החבילות עשויים להיות שונים. מדריך זה **אינו** חל על מערכת ההפעלה Qubes.

### Qubes OS

ל-Qubes OS יש תמיכה באימות Challenge-Response עם YubiKeys. If you have a YubiKey with Challenge-Response authentication support, take a look at the Qubes OS [YubiKey documentation](https://qubes-os.org/doc/yubikey) if you want to set up MFA on Qubes OS.

### SSH

#### מפתחות אבטחה של חומרה

ניתן להגדיר SSH MFA באמצעות מספר שיטות אימות שונות הפופולריות במפתחות אבטחה של חומרה. We recommend that you check out Yubico's [documentation](https://developers.yubico.com/SSH) on how to set this up.

#### TOTP

ניתן גם להגדיר SSH MFA באמצעות TOTP. DigitalOcean has provided a tutorial [How To Set Up Multi-Factor Authentication for SSH on Ubuntu 20.04](https://digitalocean.com/community/tutorials/how-to-set-up-multi-factor-authentication-for-ssh-on-ubuntu-20-04). רוב הדברים צריכים להיות זהים ללא קשר להפצה, אולם פקודות מנהל החבילות - כגון `apt-get` - ושמות החבילות עשויים להיות שונים.

### KeePass (ו-KeePassXC)

KeePass and KeePassXC databases can be secured using HOTP or Challenge-Response as a second-factor of authentication. Yubico has provided a document for KeePass [Using Your YubiKey with KeePass](https://support.yubico.com/hc/articles/360013779759-Using-Your-YubiKey-with-KeePass) and there is also one on the [KeePassXC](https://keepassxc.org/docs/#faq-yubikey-2fa) website.
