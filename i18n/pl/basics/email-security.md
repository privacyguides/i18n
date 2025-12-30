---
meta_title: "Dlaczego e-mail nie jest najlepszym wyborem pod względem prywatności i bezpieczeństwa – Privacy Guides"
title: Bezpieczeństwo poczty e-mail
icon: material/email
description: Poczta e-mail jest niezabezpieczoną na wiele sposobów formą komunikacji, a oto niektóre z powodów, dla których nie jest ona naszym pierwszym wyborem, jeśli chodzi o bezpieczną komunikację.
---

E-mail jest domyślnie niezabezpieczoną formą komunikacji. Bezpieczeństwo poczty e-mail można poprawić narzędziami takimi jak OpenPGP, które dodają szyfrowanie typu end-to-end do wiadomości, jednak OpenPGP nadal ma szereg wad w porównaniu z szyfrowaniem stosowanym w innych komunikatorach.

W efekcie e-mail najlepiej nadaje się do otrzymywania wiadomości dotyczących transakcji (np. powiadomień, resetów haseł, wiadomości z linkiem weryfikacyjnym itp.) od usług, na które rejestrujesz się online, a nie do komunikowania się z innymi.

## Przegląd szyfrowania wiadomości e-mail

Standardowym sposobem dodania szyfrowania E2EE do wiadomości między różnymi dostawcami poczty jest użycie OpenPGP. Istnieją różne implementacje standardu OpenPGP, najpopularniejsze to [GnuPG](../encryption.md#gnu-privacy-guard) i [OpenPGP.js](https://openpgpjs.org).

Nawet jeśli używasz OpenPGP, nie obsługuje ono [utajniania z wyprzedzeniem](https://pl.wikipedia.org/wiki/Utajnianie_z_wyprzedzeniem), co oznacza, że jeśli prywatny klucz Twój lub odbiorcy zostanie kiedykolwiek skradziony, wszystkie poprzednie wiadomości zaszyfrowane tym kluczem mogą zostać ujawnione. Dlatego zalecamy korzystanie z [komunikatorów](../real-time-communication.md), które implementują utajnianie z wyprzedzeniem, zamiast poczty e-mail do komunikacji między osobami, o ile to możliwe.

Istnieje też inny standard popularny w środowisku biznesowym — [S/MIME](https://en.wikipedia.org/wiki/S/MIME) — jednak wymaga on certyfikatu wydanego przez [urząd certyfikacji](https://pl.wikipedia.org/wiki/Urząd_certyfikacji) (nie wszystkie urzędy wydają certyfikaty S/MIME, a często konieczne jest coroczna opłata). W niektórych sytuacjach jest on bardziej użyteczny niż PGP, ponieważ jest obsługiwany w popularnych aplikacjach pocztowych, takich jak Poczta Apple, [Google Workspace](https://support.google.com/a/topic/9061730) i [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). Niemniej S/MIME nie rozwiązuje problemu braku utajniania z wyprzedzeniem i nie jest znacząco bezpieczniejszy niż PGP.

## Czym jest standard Web Key Directory?

Standard [Web Key Directory](https://wiki.gnupg.org/WKD) (WKD, z ang. katalog kluczy publicznych) umożliwia klientom poczty e-mail odnaleźć klucz OpenPGP dla innych skrzynek, nawet tych hostowanych przez innego dostawcę. Klienci poczty obsługujący WKD będą pytać serwer odbiorcy o klucz na podstawie nazwy domeny w adresie e-mail. Na przykład, jeśli wyślesz wiadomość na adres `jonah@privacyguides.org`, Twój klient poczty e-mail zapyta `privacyguides.org` o klucz OpenPGP Jonaha, a jeśli `privacyguides.org` ma klucz dla tego konta, Twoja wiadomość zostanie automatycznie zaszyfrowana.

Oprócz [zalecanych przez nas klientów poczty e-mail](../email-clients.md), które obsługują WKD, niektóre usługi webmail również obsługują WKD. To, czy *Twój własny* klucz jest opublikowany w WKD, zależy od konfiguracji domeny. Jeśli korzystasz z [dostawcy poczty](../email.md#openpgp-compatible-services), który obsługuje WKD, takiego jak Proton Mail czy mailbox Mail, mogą oni opublikować Twój klucz OpenPGP w swojej domenie w Twoim imieniu.

Jeżeli używasz własnej, niestandardowej domeny, konieczne będzie osobne skonfigurowanie WKD. Jeśli masz kontrolę nad nazwą swojej domeny, możesz skonfigurować WKD niezależnie od dostawcy poczty. Jednym z prostszych sposobów jest skorzystanie z funkcji „[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)” serwera `keys.openpgp.org`: ustaw rekord CNAME na subdomenie `openpgpkey` swojej domeny wskazujący na `wkd.keys.openpgp.org`, a następnie prześlij swój klucz na [keys.openpgp.org](https://keys.openpgp.org). Alternatywnie możesz [samodzielnie hostować WKD na własnym serwerze WWW](https://wiki.gnupg.org/WKDHosting).

Jeżeli korzystasz ze współdzielonej domeny dostawcy, który nie obsługuje WKD, np. `@gmail.com`, nie będzie możliwe udostępnienie klucza OpenPGP innym w ten sposób.

### Które klienty poczty e-mail obsługują E2EE?

Dostawcy poczty, którzy pozwalają na korzystanie ze standardowych protokołów dostępu, takich jak IMAP i SMTP, mogą współpracować z dowolnym z [zalecanych przez nas klientów poczty e-mail](../email-clients.md). W zależności od metody uwierzytelniania może to jednak obniżać bezpieczeństwo, jeśli ani dostawca, ani klient poczty nie obsługują [OAuth](account-creation.md#sign-in-with-oauth) lub aplikacji mostkowych, ponieważ w takim przypadku [uwierzytelnianie wieloskładnikowe](multi-factor-authentication.md) nie jest możliwe przy zwykłym logowaniu za pomocą hasła.

### Jak chronić klucze prywatne?

Karta inteligentna (np. [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) lub [Nitrokey](../security-keys.md#nitrokey)) działa w ten sposób, że otrzymuje zaszyfrowaną wiadomość e-mail z urządzenia (telefonu, tabletu, komputera itp.) uruchamiającego klienta poczty e-mail lub klienta webmail. Wiadomość jest następnie odszyfrowywana przez kartę inteligentną, a odszyfrowana treść zostaje zwrócona do urządzenia.

Warto, aby odszyfrowywanie odbywało się bezpośrednio na karcie — zapobiega to ewentualnemu ujawnieniu klucza prywatnego w przypadku naruszenia bezpieczeństwa urządzenia.

## Przegląd metadanych wiadomości e-mail

Metadane wiadomości e-mail są przechowywane w [nagłówku wiadomości](https://en.wikipedia.org/wiki/Email#Message_header) i obejmują niektóre widoczne nagłówki, takie jak `Do`, `Od`, `DW`, `Data` i `Temat`. Wiele klientów poczty e-mail i dostawców dodaje też ukryte nagłówki, które mogą ujawniać informacje o koncie.

Oprogramowanie klienckie może wykorzystywać metadane wiadomości e-mail do wyświetlenia nadawcy wiadomości oraz czasu jej otrzymania. Serwery mogą używać ich do ustalenia, dokąd wiadomość e-mail powinna zostać przesłana, oraz do [innych celów](https://en.wikipedia.org/wiki/Email#Message_header), które nie zawsze są przejrzyste.

### Kto może przeglądać metadane wiadomości e-mail?

Metadane wiadomości e-mail są chronione przed zewnętrznymi obserwatorami przy użyciu [oportunistycznego TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), jednak nadal mogą być one widoczne dla oprogramowania klienckiego (lub webmaila) oraz dla wszystkich serwerów pośredniczących w przesyłaniu wiadomości, w tym dla dostawcy poczty e-mail. Czasami serwery poczty e-mail korzystają też z usług firm trzecich do ochrony przed spamem, które zazwyczaj również mają dostęp do Twoich wiadomości.

### Dlaczego metadane nie mogą być E2EE?

Metadane wiadomości e-mail są niezbędne dla podstawowej funkcjonalności poczty (skąd wiadomość pochodzi i dokąd ma trafić). Szyfrowanie end-to-end nie było pierwotnie wbudowane w standardowe protokoły e-mail — wymaga ono dodatkowego oprogramowania, takiego jak OpenPGP. Ponieważ wiadomości OpenPGP nadal muszą współpracować z tradycyjnymi dostawcami poczty, część metadanych niezbędnych do identyfikacji stron komunikujących się nie może zostać zaszyfrowana. Oznacza to, że nawet w przypadku korzystania z OpenPGP zewnętrzni obserwatorzy mogą zobaczyć wiele informacji o Twoich wiadomościach, na przykład z kim prowadzona jest korespondencja i kiedy były wysyłane.
