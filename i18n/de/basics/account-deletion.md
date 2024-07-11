---
title: "Kontolöschung"
icon: 'material/account-remove'
description: Es ist leicht, eine große Anzahl von Internetkonten anzuhäufen. Hier sind einige Tipps, wie du deine Sammlung entrümpeln kannst.
---

Im Laufe der Zeit kann sich leicht eine Reihe von Online-Konten ansammeln, von denen du viele möglicherweise nicht mehr nutzt. Das Löschen dieser ungenutzten Konten ist ein wichtiger Schritt, um deine Privatsphäre zurückzugewinnen, da inaktive Konten anfällig für Datenschutzverletzungen sind. Eine solche Datenschutzverletzung liegt vor, wenn die Sicherheit eines Dienstes kompromittiert wird und geschützte Informationen von Unbefugten eingesehen, übertragen oder gestohlen werden. Datenschutzverletzungen sind heutzutage leider [allzu häufig](https://haveibeenpwned.com/PwnedWebsites) und eine gute digitale Hygiene ist der beste Weg, um die Auswirkungen auf dein Leben zu minimieren. Das Ziel dieses Leitfadens ist es daher, dich durch den lästigen Prozess der Kontolöschung zu führen, der oft durch [irreführendes Design](https://deceptive.design) erschwert wird, zum Wohle deiner Online-Präsenz.

## Alte Konten finden

### Passwort-Manager

Wenn du einen Passwort-Manager hast, den du dein ganzes digitales Leben lang verwendet hast, wird dieser Teil sehr einfach sein. Oftmals enthalten sie eine integrierte Funktionalität zur Erkennung, ob deine Anmeldedaten bei einer Datenschutzverletzung offengelegt wurden – wie z. B. der [Datendiebstahl Bericht](https://bitwarden.com/blog/have-you-been-pwned) von Bitwarden.

<figure markdown>
  ![Bitwarden's Data Breach Report feature](../assets/img/account-deletion/exposed_passwords.png)
</figure>

Auch wenn du noch nie explizit einen Passwort-Manager verwendet hast, ist die Wahrscheinlichkeit groß, dass du einen solchen schon in deinem Browser oder auf deinem Handy verwendet hast, ohne es zu merken. Zum Beispiel: [Firefox Passwortverwaltung](https://support.mozilla.org/kb/password-manager-remember-delete-edit-logins), [Google Passwortmanager](https://passwords.google.com/intro) und [Edge Kennwörter](https://support.microsoft.com/microsoft-edge/save-or-forget-passwords-in-microsoft-edge-b4beecb0-f2a8-1ca0-f26f-9ec247a3f336).

Desktop-Plattformen haben oft auch einen Passwort-Manager, der dir helfen kann, Passwörter wiederzufinden, an die du dich nicht mehr erinnerst:

- Windows [Anmeldeinformationsverwaltung](https://support.microsoft.com/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0)
- macOS [Passwörter](https://support.apple.com/HT211145)
- iOS [Passwörter](https://support.apple.com/HT211146)
- Linux, Gnome-Schlüsselbund, auf den über [Seahorse](https://wiki.gnome.org/Apps/Seahorse) oder [KWallet](https://userbase.kde.org/KDE_Wallet_Manager) zugegriffen werden kann

### E-Mail

Wenn du in der Vergangenheit keinen Passwort-Manager verwendet hast oder glaubst, dass du Konten hast, die nie zu deinem Passwort-Manager hinzugefügt wurden, ist eine weitere Option, deine E-Mail-Konten zu durchsuchen, auf denen du dich angemeldet hast. Suche in deinem E-Mail-Programm nach "Bestätige" oder "Willkommen". Fast jedes Mal, wenn du ein Online-Konto erstellst, sendet der Dienst einen Bestätigungslink oder eine Willkommensnachricht an deine E-Mail-Adresse. Dies kann eine gute Möglichkeit sein, alte, vergessene Konten zu finden.

## Alte Konten löschen

### Anmelden

Um deine alten Konten zu löschen, musst du zunächst sicherstellen, dass du dich bei ihnen anmelden kannst. Wenn das Konto in deinem Passwort-Manager gespeichert war, ist dieser Schritt einfach. Falls nicht, kannst du versuchen, dein Passwort zu erraten. Wenn das nicht gelingt, gibt es in der Regel Optionen, um wieder Zugriff auf dein Konto zu erhalten, die häufig über einen "Passwort vergessen"-Link auf der Anmeldeseite verfügbar sind. Es ist auch möglich, dass Konten, die du vergessen hast, bereits gelöscht wurden – manchmal löschen Dienste alle alten Konten.

Wenn die Webseite beim Versuch, den Zugang wiederherzustellen, eine Fehlermeldung zurückgibt, die besagt, dass die E-Mail-Adresse nicht mit einem Konto verknüpft ist, oder du nach mehreren Versuchen keinen Zurücksetzungslink erhältst, hast du kein Konto unter dieser E-Mail-Adresse und solltest es mit einer anderen versuchen. Wenn du nicht herausfinden kannst, welche E-Mail-Adresse du verwendet hast, oder wenn du keinen Zugang mehr zu dieser E-Mail-Adresse hast, kannst du versuchen, den Kundensupport des Dienstes zu kontaktieren. Leider gibt es keine Garantie, dass du den Zugriff auf dein Konto zurückgewinnen kannst.

### DSGVO (nur für EWR-Bewohner)

Bewohner des EWR haben zusätzliche Rechte in Bezug auf die Datenlöschung, die in [Artikel 17](https://gdpr-info.eu/art-17-gdpr) der DSGVO festgelegt sind. If it's applicable to you, read the privacy policy for any given service to find information on how to exercise your right to erasure. Reading the privacy policy can prove important, as some services have a "Delete Account" option that only disables your account and for real deletion you have to take additional action. Sometimes actual deletion may involve filling out surveys, emailing the data protection officer of the service or even proving your residence in the EEA. If you plan to go this way, do **not** overwrite account information—your identity as an EEA resident may be required. Note that the location of the service does not matter; GDPR applies to anyone serving European users. If the service does not respect your right to erasure, you can contact your national [Data Protection Authority](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens/redress/what-should-i-do-if-i-think-my-personal-data-protection-rights-havent-been-respected_en) and you may be entitled to monetary compensation.

### Overwriting Account information

In some situations where you plan to abandon an account, it may make sense to overwrite the account information with fake data. Once you've made sure you can log in, change all the information in your account to falsified information. The reason for this is that many sites will retain information you previously had even after account deletion. The hope is that they will overwrite the previous information with the newest data you entered. However, there is no guarantee that there won't be backups with the prior information.

For the account email, either create a new alternate email account via your provider of choice or create an alias using an [email aliasing service](../email-aliasing.md). You can then delete your alternate email address once you are done. We recommend against using temporary email providers, as oftentimes it is possible to reactivate temporary emails.

### Delete

You can check [JustDeleteMe](https://justdeleteme.xyz) for instructions on deleting the account for a specific service. Some sites will graciously have a "Delete Account" option, while others will go as far as to force you to speak with a support agent. The deletion process can vary from site to site, with account deletion being impossible on some.

For services that don't allow account deletion, the best thing to do is falsify all your information as previously mentioned and strengthen account security. To do so, enable [MFA](multi-factor-authentication.md) and any extra security features offered. As well, change the password to a randomly-generated one that is the maximum allowed size (a [password manager](../passwords.md) can be useful for this).

If you're satisfied that all information you care about is removed, you can safely forget about this account. If not, it might be a good idea to keep the credentials stored with your other passwords and occasionally re-login to reset the password.

Even when you are able to delete an account, there is no guarantee that all your information will be removed. In fact, some companies are required by law to keep certain information, particularly when related to financial transactions. It's mostly out of your control what happens to your data when it comes to websites and cloud services.

## Avoid New Accounts

As the old saying goes, "an ounce of prevention is worth a pound of cure." Whenever you feel tempted to sign up for a new account, ask yourself, "Do I really need this? Can I accomplish what I need to without an account?" It can often be much harder to delete an account than to create one. And even after deleting or changing the info on your account, there might be a cached version from a third-party—like the [Internet Archive](https://archive.org). Avoid the temptation when you're able to—your future self will thank you!
