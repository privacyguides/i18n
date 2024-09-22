---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

אם אתה מבצע שינויים באתר זה בעורך האינטרנט של GitHub.com ישירות, אתה לא צריך לדאוג בקשר לזה. אם אתה מפתח מקומי ו/או עורך אתרים לטווח ארוך (שכנראה צריך לפתח מקומי!), שקול את ההמלצות האלה.

## הפעל חתימת SSH Key Commit

אתה יכול להשתמש במפתח SSH קיים לחתימה, או [צור אחד חדש](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. הגדר את לקוח Git שלך לחתום על התחייבויות ותגים כברירת מחדל (הסר את `--global` כדי לחתום רק כברירת מחדל עבור repo זה):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Set your SSH key for signing in Git with the following command, substituting `/PATH/TO/.SSH/KEY.PUB` with the path to the public key you'd like to use, e.g. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

ודא שאתה [מוסיף את מפתח ה-SSH שלך לחשבון GitHub שלך](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **כמפתח חתימה** (בניגוד ל או בנוסף כמפתח אימות).

## Rebase על Git pull

השתמש ב-`git pull --rebase` במקום ב-`git pull` בעת שליפת שינויים מ-GitHub למחשב המקומי שלך. כך השינויים המקומיים שלך תמיד יהיו "על גבי" השינויים האחרונים ב-GitHub, ואתה נמנע מהתחייבויות מיזוג (שאסורות בrepo זה).

אתה יכול להגדיר זאת כהתנהגות ברירת המחדל:

```bash
git config --global pull.rebase true
```

## Rebase מ`הראשי` לפני שליחת יחסי ציבור (PR)

אם אתה עובד על branch משלך, הפעל את הפקודות הבאות לפני שליחת PR:

```bash
git fetch origin
git rebase origin/main
```
