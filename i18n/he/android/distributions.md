---
meta_title: מערכות ההפעלה הטובות ביותר של אנדרואיד - Privacy Guides
title: הפצות אלטרנטיביות
description: אתה יכול להחליף את מערכת ההפעלה בטלפון האנדרואיד שלך בחלופות מאובטחות ומכבדות פרטיות.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: מערכות הפעלה פרטיות לאנדרואיד
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small> מגן מפני האיומ/ים הבאים: </small>

- [:material-target-account: התקפות ממוקדות](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: התקפות פסיביות](../basics/common-threats.md#security-and-privacy){ .pg-orange }

מערכת הפעלה מבוססת אנדרואיד מותאמת אישית \*\* \*\* (המכונה לעיתים ROM \*\* מותאם אישית \*\*) יכולה להיות דרך להשיג רמה גבוהה יותר של פרטיות ואבטחה במכשיר שלך. זאת בניגוד לגרסת "הסטוק" של אנדרואיד שמגיעה עם הטלפון שלך מהמפעל, ולעתים קרובות משולבת עמוק עם שירותי Google Play כמו גם בתוכנת ספקים אחרים.

אנו ממליצים להתקין GrapheneOS אם יש לך פיקסל של גוגל מכיוון שהוא מספק הקשחת אבטחה משופרת ותכונות פרטיות נוספות. הסיבות שאיננו מפרטים מערכות הפעלה או מכשירים אחרים הן כדלקמן:

- לעתים קרובות יש להם [אבטחה חלשה יותר](index.md#install-a-custom-distribution).
- התמיכה נופלת לעתים קרובות כאשר המתחזק מאבד עניין או משדרג את המכשיר שלהם, וזה בניגוד למחזור [מחזור התמיכה](https://grapheneos.org/faq#device-lifetime) ש-GrapheneOS עוקבים.
- בדרך כלל יש להם מעט שיפורי פרטיות או אבטחה בולטים או שאינם בולטים שהופכים את התקנתם לכדאית.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS לוגו](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS לוגו](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** היא הבחירה הטובה ביותר בכל הקשור לפרטיות וביטחון.

GrapheneOS provides additional [security hardening](https://en.wikipedia.org/wiki/Hardening_\(computing\)) and privacy improvements. It has a [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), network and sensor permissions, and various other [security features](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS supports [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs Google Play Services fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as push notifications, while giving you full control over their permissions and access, and while containing them to a specific [work profile](../os/android-overview.md#work-profile) or [user profile](../os/android-overview.md#user-profiles) of your choice.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices).

כברירת מחדל, אנדרואיד מייצרת חיבורי רשת רבים לגוגל כדי לבצע בדיקות קישוריות של DNS, לסנכרון עם זמן הרשת הנוכחי, כדי לבדוק את קישוריות הרשת שלך ועבור משימות רקע רבות אחרות. GrapheneOS מחליף את אלה בחיבורים לשרתים המופעלים על ידי GrapheneOS ובכפוף למדיניות הפרטיות שלהם. זה מסתיר מידע כמו כתובת ה- IP שלך [מגוגל](../basics/common-threats.md#privacy-from-service-providers), אבל פירושו שזה טריוויאלי שמנהל המנהל ברשת או בספקס שלך יראה שאתה יוצר חיבורים ל- `grapheneos.network`, `grapheneos.org`, וכו' ותסיק באיזו מערכת הפעלה אתה משתמש.

אם ברצונך להסתיר מידע כזה מיריב ברשת או לספק האינטרנט שלך, עליך \*\* \*\* להשתמש ב- [VPN מהימן](../vpn.md) בנוסף לשינוי הגדרת בדיקת הקישוריות ל \*\* סטנדרט (גוגל) \*\*. ניתן למצוא אותו ב :gear: \*\* הגדרות \*\* ← \*\* רשת ואינטרנט \*\* ← \*\* בדיקות קישוריות לאינטרנט \*\*. אפשרות זו מאפשרת לך להתחבר לשרתים של גוגל לבדיקות קישוריות, אשר לצד השימוש ב- VPN עוזר לך להתמזג עם מאגר גדול יותר של מכשירי אנדרואיד.

## קריטריונים

\*\*\*\* שימו לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם. \*\* בנוסף ל[הקריטריונים הסטנדרטיים שלנו](../about/criteria.md), פיתחנו מערך ברור של דרישות המאפשרות לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- חייבת להיות תוכנת קוד פתוח.
- חייב לתמוך בנעילת bootloader עם תמיכת מפתח AVB מותאמת אישית.
- חייב לקבל עדכוני אנדרואיד גדולים בתוך 0-1 חודשים מהשחרור.
- חייב לקבל עדכוני תכונות אנדרואיד (גרסה מינורית) בתוך 0-14 ימים מהשחרור.
- חייב לקבל תיקוני אבטחה רגילים בתוך 0-5 ימים מהשחרור.
- חייב \*\* לא \*\* להיות "rooted" מחוץ לקופסה.
- חייב **לא** להפעיל את שירותי Google Play כברירת מחדל.
- חייב **לא** לדרוש שינוי במערכת כדי לתמוך בשירותי Google Play.
