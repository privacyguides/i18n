---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, PicoCrypt, and OpenPGP - Privacy Guides"
title: "תוכנת הצפנה"
icon: material/file-lock
description: הצפנה של נתונים היא הדרך היחידה לשלוט מי יכול לגשת אליו. These tools allow you to encrypt your emails and any other files.
cover: encryption.webp
---

**Encryption** is the only secure way to control who can access your data. If you are currently not using encryption software for your hard disk, emails, or files, you should pick an option here.

## מרובה-פלטפורמות

האפשרויות המפורטות כאן הן מרובות פלטפורמות ונהדרות ליצירת גיבויים מוצפנים של הנתונים שלך.

### Cryptomator (ענן)

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: התקפות פסיביות](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** is an encryption solution designed for privately saving files to any cloud [:material-server-network: Service Provider](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminating the need to trust that they won't access your files. הוא מאפשר לך ליצור כספות המאוחסנות בכונן וירטואלי, שתוכנן מוצפן ומסונכרן עם ספק אחסון הענן שלך.

[:octicons-home-16: Homepage](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Source Code" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator משתמש בהצפנת AES-256 כדי להצפין קבצים ושמות קבצים. Cryptomator אינו יכול להצפין מטא-נתונים כגון חותמות זמן של גישה, שינוי ויצירה, וגם לא את המספר והגודל של קבצים ותיקיות.

מספר ספריות קריפטוגרפיות של Cryptomator [עברו ביקורת](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) על ידי Cure53. היקף הספריות המבוקרים כולל: [cryptolib](https://github.com/cryptomator/cryptolib), [ cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) ו-[cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). הביקורת לא התרחבה ל[cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), שהיא ספרייה המשמשת את Cryptomator עבור iOS.

Cryptomator's documentation details its intended [security target](https://docs.cryptomator.org/en/latest/security/security-target), [security architecture](https://docs.cryptomator.org/en/latest/security/architecture), and [best practices](https://docs.cryptomator.org/en/latest/security/best-practices) for use in further detail.

### Picocrypt (קובץ)

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Picocrypt לוגו](assets/img/encryption-software/picocrypt.svg){ align=right }

**Picocrypt** הוא כלי הצפנה קטן ופשוט המספק הצפנה מודרנית. Picocrypt משתמש בצופן המאובטח XChaCha20 ובפונקציית גזירת מפתח Argon2id כדי לספק רמת אבטחה גבוהה. הוא משתמש במודולי x/crypto הסטנדרטיים של Go עבור תכונות ההצפנה שלו.

[:octicons-repo-16: Repository](https://github.com/Picocrypt/Picocrypt){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/Picocrypt/Picocrypt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/picocrypt){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-apple: macOS](https://github.com/Picocrypt/Picocrypt/releases)
- [:simple-linux: Linux](https://github.com/Picocrypt/Picocrypt/releases)

</details>

</div>

### VeraCrypt (דיסק)

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt לוגו](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt לוגו](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** הוא כלי תוכנה חופשית קוד פתוח המשמש להצפנה תוך כדי תנועה. זה יכול ליצור דיסק מוצפן וירטואלי בתוך קובץ, להצפין מחיצה או להצפין את כל התקן האחסון עם אימות לפני אתחול.

[:octicons-home-16: Homepage](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt הוא מזלג של פרויקט TrueCrypt שהופסק. על פי המפתחים שלה, שיפורים באבטחה יושמו וטופלו בעיות שעלו בביקורת הקוד הראשונית של TrueCrypt.

בעת הצפנה עם VeraCrypt, יש לך אפשרות לבחור מבין [hash פונקציות](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme) שונות. אנו מציעים לך **לבחור** רק [SHA-512](https://en.wikipedia.org/wiki/SHA-512) ולהיצמד ל [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) צופן בלוק.

Truecrypt [נבדק מספר פעמים](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), וגם VeraCrypt [נבדק בנפרד](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## הצפנת דיסק מלא של מערכת ההפעלה

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

להצפנת הכונן שמערכת ההפעלה שלך מאתחלת ממנו, אנו ממליצים בדרך כלל להפעיל את תוכנת ההצפנה שמגיעה עם מערכת ההפעלה שלך במקום להשתמש בכלי של צד שלישי. הסיבה לכך היא שכלי ההצפנה המקוריים של מערכת ההפעלה שלך עושים לעתים קרובות שימוש בתכונות ספציפיות למערכת ההפעלה ולחומרה כמו [מעבד ההצפנה המאובטח](https://en.wikipedia.org/wiki/Secure_cryptoprocessor) במכשיר שלך כדי להגן על המחשב שלך מפני התקפות פיזיות מתקדמות יותר. עבור כוננים משניים וכוננים חיצוניים שאתה *אינך* מאתחל מהם, אנו עדיין ממליצים להשתמש בכלי קוד פתוח כמו [VeraCrypt](#veracrypt-disk) על הכלים שלהלן, מכיוון שהם מציעים גמישות נוספת ומאפשרים לך להימנע מנעילת ספקים.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker לוגו](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** הוא פתרון ההצפנה המלא המצורף ל-Microsoft Windows. The main reason we recommend it for encrypting your boot drive is because of its [use of TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm). ElcomSoft, a forensics company, has written about this feature in [Understanding BitLocker TPM Protection](https://blog.elcomsoft.com/2021/01/understanding-BitLocker-tpm-protection).

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title=Documentation}

</details>

</div>

BitLocker is [only supported](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) on Pro, Enterprise and Education editions of Windows. ניתן להפעיל אותו במהדורות ביתיות בתנאי שהן עומדות בדרישות המוקדמות.

<details class="example" markdown>
<summary>Enabling BitLocker on Windows Home</summary>

To enable BitLocker on "Home" editions of Windows, you must have partitions formatted with a [GUID Partition Table](https://en.wikipedia.org/wiki/GUID_Partition_Table) and have a dedicated TPM (v1.2, 2.0+) module. You may need to [disable the non-Bitlocker "Device encryption" functionality](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (which is inferior because it sends your recovery key to Microsoft's servers) if it is enabled on your device already before following this guide.

1. פתח שורת פקודה ובדוק את תבנית טבלת המחיצות של הכונן באמצעות הפקודה הבאה. אתה אמור לראות את "**GPT**" ברשימה תחת "סגנון מחיצה":

    ```powershell
    powershell Get-Disk
    ```

2. הפעל פקודה זו (בשורת פקודה של אדמין) כדי לבדוק את גרסת ה-TPM שלך. אתה אמור לראות את `2.0` או `1.2` לצד `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Access [Advanced Startup Options](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). עליך לאתחל מחדש תוך כדי לחיצה על מקש F8 לפני הפעלת Windows ולהיכנס ל *שורת הפקודה* ב **פתרון בעיות** → **אפשרויות מתקדמות** → **שורת הפקודהPrompt**.
4. התחבר עם חשבון הניהול שלך והקלד זאת בשורת הפקודה כדי להתחיל בהצפנה:

    ```powershell
    manage-bde -on c: -used
    ```

5. סגור את שורת הפקודה והמשך אתחול ל-Windows רגיל.
6. פתח שורת פקודה של מנהל מערכת והפעל את הפקודות הבאות:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

    גיבוי 'BitLocker-Recovery-Key.txt' בשולחן העבודה שלך להתקן אחסון נפרד. אובדן קוד שחזור זה עלול לגרום לאובדן נתונים.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault לוגו](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** הוא פתרון הצפנת נפח תוך כדי תנועה המובנה ב-macOS. FileVault מומלץ כי זה [leverages](https://support.apple.com/guide/security/volume-encryption-with-filevault-sec4c6dc1b6e/web) יכולות אבטחת חומרה הקיימות בשבב אפל סיליקון SoC או T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title=תיעוד}

</details>

</div>

אנו ממליצים לאחסן מפתח שחזור מקומי במקום מאובטח, בניגוד לשימוש בחשבון iCloud שלך לשחזור.

### הגדרת מפתח מאוחדת של לינוקס

<div class="admonition recommendation" markdown>

![LUKS לוגו](assets/img/encryption-software/luks.png){ align=right }

**LUKS** היא שיטת ברירת המחדל של FDE עבור לינוקס. ניתן להשתמש בו כדי להצפין אמצעי אחסון מלאים, מחיצות או ליצור מיכלים מוצפנים.

[:octicons-home-16: Homepage](https://gitlab.com/cryptsetup/cryptsetup/-/blob/main/README.md){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Source Code" }

</details>

</div>

<details class="example" markdown>
<summary>Creating and opening encrypted containers</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### Opening encrypted containers

We recommend opening containers and volumes with `udisksctl` as this uses [Polkit](https://en.wikipedia.org/wiki/Polkit). רוב מנהלי הקבצים, כמו אלה הכלולים בסביבות שולחן עבודה פופולריות, יכולים לפתוח קבצים מוצפנים. Tools like [udiskie](https://github.com/coldfix/udiskie) can run in the system tray and provide a helpful user interface.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Remember to back up volume headers</p>

אנו ממליצים לך תמיד [לגבות את כותרות ה-LUKS שלך](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) במקרה של כשל חלקי בכונן. This can be done with:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## שורת הפקודה

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

כלים עם ממשקי שורת פקודה שימושיים לשילוב [סקריפטים של מעטפת](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor לוגו](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** הוא כלי הצפנת וחתימה של קבצים חינמי ופתוח העושה שימוש באלגוריתמים קריפטוגרפיים מודרניים ומאובטחים. It aims to be a better version of [age](https://github.com/FiloSottile/age) and [Minisign](https://jedisct1.github.io/minisign) to provide a simple, easier alternative to GPG.

[:octicons-home-16: Homepage](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Tomb לוגו](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** הוא מעטפת מעטפת שורת פקודה עבור LUKS. It supports steganography via [third-party tools](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Homepage](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Source Code" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title=Contribute }

</details>

</div>

## OpenPGP

<small>Protects against the following threat(s):</small>

- [:material-target-account: התקפות ממוקדות](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: התקפות פסיביות](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: ספקי שירות](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

לעתים יש צורך ב-OpenPGP עבור משימות ספציפיות כמו חתימה דיגיטלית והצפנת דואר אלקטרוני. ל-PGP תכונות רבות והוא [מורכב](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) כפי שהוא קיים זמן רב. עבור משימות כגון חתימה או הצפנה של קבצים, אנו מציעים את האפשרויות לעיל.

בעת הצפנה באמצעות PGP, יש לך אפשרות להגדיר אפשרויות שונות בקובץ `gpg.conf` שלך. We recommend staying with the standard options specified in the [GnuPG user FAQ](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Use future defaults when generating a key</p>

When [generating keys](https://gnupg.org/gph/en/manual/c14.html) we suggest using the `future-default` command as this will instruct GnuPG use modern cryptography such as [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) and [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard לוגו](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** היא חלופה ברישיון GPL לחבילת PGP של תוכנות הצפנה. GnuPG תואם ל-[RFC 4880](https://tools.ietf.org/html/rfc4880), שהוא מפרט ה-IETF הנוכחי של OpenPGP. The GnuPG project has been working on an [updated draft](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) in an attempt to modernize OpenPGP. GnuPG הוא חלק מפרויקט התוכנה GNU של קרן התוכנה החופשית וקיבל [מימון] גדול (https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) מממשלת גרמניה.

[:octicons-home-16: Homepage](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![GPG4win לוגו](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** היא חבילה עבור Windows מ-[Intevation ו-g10 Code](https://gpg4win.org/impressum.html). הוא כולל [כלים שונים](https://gpg4win.org/about.html) שיכולים לסייע לך בשימוש ב-GPG ב-Microsoft Windows. הפרויקט יזם ובמקור [מומן על ידי](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) המשרד הפדרלי של גרמניה למידע אבטחה (BSI) בשנת 2005.

[:octicons-home-16: Homepage](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title=Documentation}
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Source Code" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

We suggest [Canary Mail](email-clients.md#canary-mail-ios) for using PGP with email on iOS devices.

</div>

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** provides OpenPGP support for [Apple Mail](email-clients.md#apple-mail-macos) and macOS.

אנו ממליצים להסתכל על [השלבים הראשונים](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup- gpgtools-create-a-new-key-your-first-encrypted-email) ו-[בסיס ידע](https://gpgtools.tenderapp.com/kb) לתמיכה.

[:octicons-home-16: Homepage](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain לוגו](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** הוא יישום אנדרואיד של GnuPG. It's commonly required by mail clients such as [K-9 Mail](email-clients.md#k-9-mail-android) and [FairEmail](email-clients.md#fairemail-android) and other Android apps to provide encryption support. Cure53 completed a [security audit](https://openkeychain.org/openkeychain-3-6) of OpenKeychain 3.6 in October 2015. פרטים טכניים על הביקורת והפתרונות של OpenKeychain ניתן למצוא [כאן](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

[:octicons-home-16: Homepage](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

### כישורים מינימליים

- אפליקציות הצפנה חוצות פלטפורמות חייבות להיות בקוד פתוח.
- אפליקציות להצפנת קבצים חייבות לתמוך בפענוח ב-Linux, macOS ו-Windows.
- אפליקציות להצפנת דיסק חיצוני חייבות לתמוך בפענוח ב-Linux, macOS ו-Windows.
- אפליקציות להצפנת דיסק פנימי (OS) חייבות להיות חוצות פלטפורמות או מובנות במערכת ההפעלה באופן מקורי.

### המקרה הטוב ביותר

הקריטריונים הטובים ביותר שלנו מייצגים את מה שהיינו רוצים לראות מהפרויקט המושלם בקטגוריה זו. ייתכן שההמלצות שלנו לא יכללו חלק מהפונקציונליות הזו או את כולה, אך אלו שכן כן עשויות לדרג גבוה יותר מאחרות בדף זה.

- אפליקציות הצפנה של מערכת הפעלה (FDE) צריכות להשתמש באבטחת חומרה כגון TPM או Secure Enclave.
- אפליקציות להצפנת קבצים צריכות לקבל תמיכה של צד ראשון או שלישי עבור פלטפורמות ניידות.
