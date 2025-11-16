---
title: "Usuwanie kont"
icon: 'material/account-remove'
description: Łatwo jest zgromadzić dużą liczbę kont internetowych — oto kilka wskazówek, jak uszczuplić ich kolekcję.
---

Z upływem czasu łatwo zebrać wiele kont internetowych, z których część możesz już nie używać. Usuwanie tych kont to ważny krok w odzyskiwaniu prywatności, ponieważ nieaktywne konta są podatne na naruszenia danych. Naruszenie danych (lub też „wyciek danych”) to sytuacja, gdy bezpieczeństwo usługi zostaje przełamane, a chronione informacje są przeglądane, przesyłane lub kradzione przez nieuprawnione podmioty. Niestety wycieki danych są dziś [zbyt powszechne](https://haveibeenpwned.com/PwnedWebsites), dlatego praktykowanie dobrej higieny cyfrowej to najlepszy sposób na zminimalizowanie ich wpływu na Twoje życie. Celem tego przewodnika jest przeprowadzić Cię przez uciążliwy proces usuwania kont, często utrudniany przez [zwodnicze projektowanie](https://deceptive.design), tak aby poprawić Twoją obecność w sieci.

## Odnajdywanie starych kont

### Menedżer haseł

Jeśli masz menedżera haseł, z którego korzystasz przez całe swoje cyfrowe życie, ta część będzie wyjątkowo prosta. Często mają one wbudowane funkcje wykrywania, czy Twoje dane logowania zostały ujawnione w wyniku wycieku danych — jak choćby [raport wycieków danych](https://bitwarden.com/blog/have-you-been-pwned) Bitwarden.

<figure markdown>
  ![Funkcja raport wycieków danych Bitwarden](../assets/img/account-deletion/exposed_passwords.png)
</figure>

Nawet jeśli nigdy świadomie nie zdarzyło Ci się korzystać z menedżera haseł, istnieje szansa, że używasz go w przeglądarce lub telefonie, nawet tego nie zauważając. Przykładowo: [Menedżer haseł Firefoksa](https://support.mozilla.org/kb/password-manager-remember-delete-edit-logins), [Menedżer haseł Google](https://passwords.google.com/intro) oraz [Menedżer haseł Edge](https://support.microsoft.com/microsoft-edge/save-or-forget-passwords-in-microsoft-edge-b4beecb0-f2a8-1ca0-f26f-9ec247a3f336).

Systemy operacyjne na komputery stacjonarne również często mają własne menedżery haseł, które mogą pomóc odzyskać dawno zapomniane dane logowania:

- [Poświadczenia systemu Windows](https://support.microsoft.com/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0)
- Aplikacja [Hasła](https://support.apple.com/HT211145) w systemie MacOS
- Aplikacja [Hasła](https://support.apple.com/HT211146) w systemie iOS
- Na Linuksie dostępny jest Gnome Keyring za pośrednictwem[Seahorse](https://wiki.gnome.org/Apps/Seahorse) lub [KDE Wallet Manager](https://userbase.kde.org/KDE_Wallet_Manager)

### E-mail

Jeśli wcześniej nie korzystałeś(-aś) z menedżera haseł albo podejrzewasz, że masz konta, których nigdy nie zostały do niego dodane, kolejną opcją jest przeszukanie skrzynki e-mail, na której prawdopodobnie dokonano rejestracji. W swoim kliencie poczty e-mail wyszukaj słowa kluczowe takie jak „verify”, „weryfikacja”, „welcome” czy „witaj”. Niemalże za każdym razem, gdy zakładasz konto online, usługa wysyła link weryfikacyjny lub wiadomość powitalną. To dobry sposób na odnalezienie starych, zapomnianych kont.

## Deleting Old Accounts

### Log In

In order to delete your old accounts, you'll need to first make sure you can log in to them. Again, if the account was in your password manager, this step is easy. If not, you can try to guess your password. Failing that, there are typically options to regain access to your account, commonly available through a "forgot password" link on the login page. It may also be possible that accounts you've abandoned have already been deleted—sometimes services prune all old accounts.

When attempting to regain access, if the site returns an error message saying that email is not associated with an account, or you never receive a reset link after multiple attempts, then you do not have an account under that email address and should try a different one. If you can't figure out which email address you used, or you no longer have access to that email, you can try contacting the service's customer support. Unfortunately, there is no guarantee that you will be able to reclaim access your account.

### GDPR (EEA residents only)

Residents of the EEA have additional rights regarding data erasure specified in [Article 17](https://gdpr-info.eu/art-17-gdpr) of the GDPR. If it's applicable to you, read the privacy policy for any given service to find information on how to exercise your right to erasure. Reading the privacy policy can prove important, as some services have a "Delete Account" option that only disables your account and for real deletion you have to take additional action. Sometimes actual deletion may involve filling out surveys, emailing the data protection officer of the service or even proving your residence in the EEA. If you plan to go this way, do **not** overwrite account information—your identity as an EEA resident may be required. Note that the location of the service does not matter; GDPR applies to anyone serving European users. If the service does not respect your right to erasure, you can contact your national [Data Protection Authority](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens/redress/what-should-i-do-if-i-think-my-personal-data-protection-rights-havent-been-respected_en) and may be entitled to monetary compensation.

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
