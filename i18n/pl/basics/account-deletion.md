---
title: Usuwanie kont
icon: material/account-remove
description: Łatwo jest zgromadzić dużą liczbę kont internetowych. Oto kilka wskazówek, jak uszczuplić ich kolekcję.
---

Z upływem czasu łatwo zebrać wiele kont internetowych, z których część możesz już nie używać. Usuwanie tych kont to ważny krok w odzyskiwaniu prywatności, ponieważ nieaktywne konta są podatne na naruszenia danych. Naruszenie danych (lub też „wyciek danych”) to sytuacja, gdy bezpieczeństwo usługi zostaje przełamane, a chronione informacje są przeglądane, przesyłane lub kradzione przez nieuprawnione podmioty. Niestety wycieki danych są dziś [zbyt powszechne](https://haveibeenpwned.com/PwnedWebsites), dlatego praktykowanie dobrej higieny cyfrowej to najlepszy sposób na zminimalizowanie ich wpływu na Twoje życie. Celem tego przewodnika jest przeprowadzić Cię przez uciążliwy proces usuwania kont, często utrudniany przez [zwodnicze projektowanie](https://deceptive.design), tak aby poprawić Twoją obecność w sieci.

## Odnajdywanie starych kont

### Menedżer haseł

Jeśli masz menedżera haseł, z którego korzystasz przez całe swoje cyfrowe życie, ta część będzie wyjątkowo prosta. Często mają one wbudowane funkcje wykrywania, czy Twoje dane logowania zostały ujawnione w wyniku wycieku danych — jak choćby [raport wycieków danych](https://bitwarden.com/blog/have-you-been-pwned) Bitwarden.

<figure markdown>
  ![Funkcja raport wycieków danych Bitwarden](../assets/img/account-deletion/exposed_passwords.png)
</figure>

Nawet jeśli nigdy świadomie nie zdarzyło Ci się korzystać z menedżera haseł, istnieje szansa, że używasz go w przeglądarce ([Firefox](https://support.mozilla.org/kb/password-manager-remember-delete-edit-logins), [Chrome](https://passwords.google.com/intro), [Edge](https://support.microsoft.com/microsoft-edge/save-or-forget-passwords-in-microsoft-edge-b4beecb0-f2a8-1ca0-f26f-9ec247a3f336)) lub telefonie ([Google](https://passwords.google.com/intro) na standardowym systemie Android; aplikacja[Hasła](https://support.apple.com/HT211146) w systemie iOS), nawet tego nie zauważając.

Systemy operacyjne na komputery stacjonarne również często mają własne menedżery haseł, które mogą pomóc odzyskać dawno zapomniane dane logowania:

- Windows: [Poświadczenia systemu Windows](https://support.microsoft.com/windows/accessing-credential-manager-1b5c916a-6a16-889f-8581-fc16e8165ac0)
- macOS: Aplikacja [Hasła](https://support.apple.com/HT211145)
- Linux: Gnome Keyring (za pośrednictwem [Seahorse](https://gitlab.gnome.org/GNOME/seahorse#seahorse)) lub [KDE Wallet Manager](https://userbase.kde.org/KDE_Wallet_Manager)

### E-mail

Jeśli wcześniej nie korzystałeś(-aś) z menedżera haseł albo podejrzewasz, że masz konta, których nigdy nie zostały do niego dodane, kolejną opcją jest przeszukanie skrzynki e-mail, na której prawdopodobnie dokonano rejestracji. W swoim kliencie poczty e-mail wyszukaj słowa kluczowe takie jak „verify”, „weryfikacja”, „welcome” czy „witaj”. Niemalże za każdym razem, gdy zakładasz konto online, usługa wysyła link weryfikacyjny lub wiadomość powitalną. To dobry sposób na odnalezienie starych, zapomnianych kont.

## Usuwanie starych kont

### Zalogowanie się

Aby usunąć stare konta, najpierw musisz upewnić się, że możesz się na nie zalogować. Jeśli konto było zapisane w menedżerze haseł, ten krok jest prosty. Jeśli nie, możesz spróbować odgadnąć hasło. W razie niepowodzenia zwykle są opcje odzyskania dostępu do konta, najczęściej dostępne poprzez link „Nie pamiętam hasła” na stronie logowania. Możliwe też, że porzucone konta zostały już usunięte — czasami usługi usuwają wszystkie stare konta.

Przy próbach odzyskania dostępu, jeśli witryna zwraca komunikat, że dany e-mail nie jest powiązany z żadnym kontem, lub jeśli po wielokrotnych próbach nigdy nie otrzymujesz linku do zresetowania hasła, to znaczy, że nie masz konta pod tym adresem i powinieneś spróbować inny adres e-mail. Jeśli nie potrafisz ustalić, którego adresu e-mail użyto, albo nie masz do niego już dostępu, możesz spróbować skontaktować się z obsługą klienta. Niestety nie ma gwarancji, że uda Ci się odzyskać dostęp do swojego konta.

### RODO (tylko dla mieszkańców EOG)

Mieszkańcy EOG mają dodatkowe prawa dotyczące usuwania danych określone w [artykule 17](https://gdpr-info.eu/art-17-gdpr) RODO. Jeśli dotyczy to Ciebie, przeczytaj politykę prywatności danej usługi, aby dowiedzieć się, jak skorzystać z prawa do usunięcia danych. Zapoznanie się z polityką prywatności może być istotne, ponieważ niektóre usługi oferują opcję „Usuń konto”, która jedynie dezaktywuje konto, a w celu faktycznego usunięcia może być wymagane podjęcie dodatkowych działań. Czasem rzeczywiste usunięcie wiąże się z wypełnieniem ankiety, wysłaniem e-maila do inspektora ochrony danych serwisu lub nawet udowodnieniem miejsca zamieszkania w EOG. Jeśli zamierzasz iść tą drogą, **nie** nadpisuj informacji o koncie — Twoja tożsamość jako mieszkańca EOG może być wymagana. Lokalizacja siedziby usługi nie ma znaczenia; RODO ma zastosowanie do każdego podmiotu obsługującego europejskich użytkowników. Jeśli usługa nie respektuje Twojego prawa do usunięcia danych, możesz skontaktować się z krajowym [organem ochrony danych](https://ec.europa.eu/info/law/law-topic/data-protection/reform/rights-citizens/redress/what-should-i-do-if-i-think-my-personal-data-protection-rights-havent-been-respected_en) i możesz mieć prawo do odszkodowania pieniężnego.

### Nadpisywanie informacji o koncie

W sytuacjach, gdy planujesz porzucić konto, sensowne może być nadpisanie danych konta fałszywymi informacjami. Gdy upewnisz się, że możesz się zalogować, zmień wszystkie informacje na koncie na sfałszowane dane. Chodzi o to, że wiele serwisów zachowuje informacje, które miały miejsce przed usunięciem konta. Nadpisanie ich ma zwiększyć szansę, że zastąpią one wcześniejsze wpisy najnowszymi wprowadzonymi danymi. Nie ma jednak gwarancji, że nie istnieją kopie zapasowe zawierające poprzednie informacje.

Jako adres e-mail konta możesz utworzyć nowe alternatywne konto u wybranego dostawcy lub skorzystać z aliasu za pomocą [usługi aliasingu e-mail](../email-aliasing.md). Po zakończeniu możesz usunąć alternatywne konto e-mail. Odradzamy korzystanie z tymczasowych dostawców poczty e-mail, ponieważ często możliwe jest ponowne aktywowanie tymczasowych adresów.

### Usunięcie go

Możesz sprawdzić [JustDeleteMe](https://justdeleteme.xyz) po instrukcje dotyczące usuwania konta dla konkretnej usługi. Niektóre witryny łaskawie oferują opcję „Usuń konto”, podczas gdy inne posuwają się nawet do zmuszenia Cię do rozmowy z agentem pomocy technicznej. Proces usuwania może różnić się w zależności od serwisu, a w niektórych przypadkach usunięcie konta może być niemożliwe.

W przypadku usług, które nie pozwalają usunąć konta, najlepszym wyjściem jest, jak wspomniano wyżej, podmienić wszystkie dane na fałszywe oraz wzmocnić zabezpieczenia konta. Aby to zrobić, włącz [MFA](multi-factor-authentication.md) i wszelkie dodatkowe funkcje bezpieczeństwa oferowane przez usługę. Zmień też hasło na losowo wygenerowane o maksymalnej dozwolonej długości (przydatny może być [menedżer haseł](../passwords.md)).

Jeżeli masz pewność, że wszystkie dane, na których Ci zależało, zostały usunięte, możesz bezpiecznie zapomnieć o tym koncie. Jeśli nie, dobrym pomysłem jest zachować dane logowania razem z innymi hasłami i od czasu do czasu ponownie się zalogować, żeby zresetować hasło.

Nawet gdy uda ci się usunąć konto, nie ma gwarancji, że wszystkie informacje zostaną trwale usunięte. W rzeczywistości niektóre firmy są prawnie zobowiązane do przechowywania określonych danych, zwłaszcza tych związanych z transakcjami finansowymi. W dużej mierze jest poza Twoją kontrolą, co dzieje się z danymi na stronach i w usługach chmurowych.

## Unikaj zakładania nowych kont

Jak mówi stare polskie przysłowie: „lepiej zapobiegać niż leczyć”. Za każdym razem, gdy kusi Cię założenie nowego konta, zatrzymaj się i zadaj sobie pytanie: „Czy naprawdę jest mi to potrzebne? Czy da się zrobić to bez rejestracji?”. W praktyce znacznie trudniej jest konto usunąć, niż je utworzyć. Nawet jeśli skasujesz konto lub zmienisz zapisane na nim dane, wciąż może istnieć w sieci jego zbuforowana wersja, przechowywana przez strony trzecie — na przykład [Internet Archive](https://archive.org). Jeśli możesz sobie darować zakładanie konta, zrób to. Twoje przyszłe ja będzie Ci za to wdzięczne!
