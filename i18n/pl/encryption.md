---
meta_title: "Zalecane oprogramowanie do szyfrowania: VeraCrypt, Cryptomator i OpenPGP - Privacy Guides"
title: "Oprogramowanie szyfrujące"
icon: material/file-lock
description: Szyfrowanie danych to jedyny sposób na kontrolowanie tego, kto ma do nich dostęp. Te narzędzia pozwalają na zaszyfrowanie wiadomości e-mail i innych plików.
cover: encryption.webp
---

**Szyfrowanie** jest jedynym bezpiecznym sposobem kontrolowania, kto może uzyskać dostęp do Twoich danych. Jeśli obecnie nie używasz oprogramowania szyfrującego dla swojego dysku, e-maili lub plików, powinnaś wybrać jedną z tych opcji.

## Wieloplatformowość

Wymienione tutaj opcje są na wielu platformach i świetnie nadają się do tworzenia szyfrowanych kopii zapasowych twoich danych.

### Cryptomator (Chmura)

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Logo Cryptomator](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** to rozwiązanie szyfrujące zaprojektowane do prywatnego zapisywania plików w chmurze dowolnego [:material-server-network: Usługodawcy](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminując konieczność zaufania, że nie uzyskają dostępu do twoich plików. Pozwala na tworzenie sejfów przechowywanych na wirtualnym dysku, których zawartość jest szyfrowana i synchronizowana z dostawcą pamięci masowej w chmurze.

[:octicons-home-16: Strona główna](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator wykorzystuje szyfrowanie AES-256 do szyfrowania zarówno plików, jak i nazw plików. Cryptomator nie może szyfrować metadanych, takich jak daty dostępu, modyfikacji oraz utworzenia, ani liczby i rozmiaru plików i folderów.

Cryptomator jest darmowy na wszystkich platformach stacjonarnych, a także na iOS w trybie "tylko do odczytu". Cryptomator oferuje [płatne](https://cryptomator.org/pricing) aplikacje z pełną funkcjonalnością na iOS i Androida. Wersję na Androida można kupić anonimowo za pośrednictwem [ProxyStore](https://cryptomator.org/coop/proxystore).

Niektóre biblioteki kryptograficzne Cryptomator zostały poddane [audytowi](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) przez Cure53. Zakres audytowanych bibliotek obejmuje: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) i [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). Audyt nie objął [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), która jest biblioteką używaną przez Cryptomator dla iOS.

Dokumentacja Cryptomatora szczegółowo opisuje zamierzony [cel bezpieczeństwa](https://docs.cryptomator.org/en/latest/security/security-target), [architekturę bezpieczeństwa](https://docs.cryptomator.org/en/latest/security/architecture) i [najlepsze praktyki](https://docs.cryptomator.org/en/latest/security/best-practices) użytkowania w większym detalu.

### VeraCrypt (Dysk)

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![Logo VeraCrypt](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![Logo VeraCrypt](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** to darmowe narzędzie z udostępnionym kodem źródłowym, używane do szyfrowania w czasie rzeczywistym. Może utworzyć wirtualny zaszyfrowany dysk w pliku, zaszyfrować partycję lub zaszyfrować całe urządzenie pamięci masowej z uwierzytelnianiem przed uruchomieniem.

[:octicons-home-16: Strona główna](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt jest forkiem porzuconego projektu TrueCrypt. Według jego twórców wdrożono poprawki bezpieczeństwa i rozwiązano problemy zgłoszone podczas wstępnego audytu kodu TrueCrypt.

Podczas szyfrowania za pomocą VeraCrypt masz możliwość wyboru spośród różnych [funkcji skrótu](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Sugerujemy wybranie **tylko** [SHA-512](https://en.wikipedia.org/wiki/SHA-512) i trzymanie się szyfru blokowego [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard).

TrueCrypt był [wielokrotnie audytowany](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), a VeraCrypt był również [audytowany osobno](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Szyfrowanie systemu operacyjnego

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Wbudowane rozwiązania szyfrowania systemu operacyjnego zazwyczaj wykorzystują sprzętowe funkcje bezpieczeństwa, takie jak [bezpieczny kryptoprocesor](basics/hardware.md#tpmsecure-cryptoprocessor). Dlatego zalecamy korzystanie z wbudowanych rozwiązań szyfrujących dla danego systemu operacyjnego. W przypadku szyfrowania międzyplatformowego nadal zalecamy stosowanie [narzędzi międzyplatformowych](#multi-platform) w celu zapewnienia dodatkowej elastyczności i uniknięcia uzależnienia od jednego dostawcy.

<details class="warning" markdown>

<summary>Wyłączanie urządzeń, gdy nie są używane.</summary>

Wyłączanie urządzeń, gdy nie są one używane, zapewnia najwyższy poziom bezpieczeństwa, ponieważ minimalizuje powierzchnię ataku twojej metody pełnego szyfrowania dysku, zapewniając, że żadne klucze szyfrowania nie pozostaną w pamięci.

</details>

### BitLocker

<div class="admonition recommendation" markdown>

![Logo BitLocker](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** to rozwiązanie pełnego szyfrowania woluminów dołączone do systemu Microsoft Windows, które wykorzystuje moduł Trusted Platform Module ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) do zabezpieczeń sprzętowych.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Dokumentacja" }

</details>

</div>

BitLocker jest [oficjalnie obsługiwany](https://support.microsoft.com/en-us/windows/bitlocker-overview-44c0c61c-989d-4a69-8822-b95cd49b1bbf) w wersjach Pro, Enterprise i Education systemu Windows. Wersja Home obsługuje tylko automatyczne [szyfrowanie urządzeń](https://support.microsoft.com/en-us/windows/device-encryption-in-windows-cf7e2b6f-3e70-4882-9532-18633605b7df) i musi spełniać określone wymagania sprzętowe. Jeśli korzystasz z edycji Home, zalecamy [uaktualnienie do wersji Pro](https://support.microsoft.com/en-us/windows/upgrade-windows-home-to-windows-pro-ef34d520-e73f-3198-c525-d1a218cc2818), co można zrobić bez ponownej instalacji systemu Windows lub utraty plików.

Wersje Pro i wyższe obsługują również bezpieczniejszą funkcję pre-boot [TPM+PIN](https://learn.microsoft.com/en-us/windows/security/operating-system-security/data-protection/bitlocker/faq#what-is-the-difference-between-a-tpm-owner-password--recovery-password--recovery-key--pin--enhanced-pin--and-startup-key), skonfigurowaną za pomocą odpowiednich ustawień [zasad grupy](os/windows/group-policies.md#bitlocker-drive-encryption). Kod PIN ma ograniczenie liczby prób, a moduł TPM zablokuje dostęp do klucza szyfrowania, tymczasowo lub trwale, jeśli ktoś będzie próbował uzyskać dostęp metodą brute force.

</details>

### FileVault

<div class="admonition recommendation" markdown>

![Logo FileVault](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** to wbudowane w system macOS rozwiązanie do szyfrowania woluminów w czasie rzeczywistym. FileVault wykorzystuje [możliwości zabezpieczeń sprzętowych](os/macos-overview.md#hardware-security) obecne w systemie na chipie (SoC) Apple Silicon lub T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Dokumentacja" }

</details>

</div>

Odradzamy korzystanie z konta iCloud do odzyskiwania danych; zamiast tego należy bezpiecznie przechowywać lokalny klucz odzyskiwania na osobnym urządzeniu pamięci masowej.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![Logo LUKS](assets/img/encryption-software/luks.png){ align=right }

**LUKS** jest domyślną metodą pełnego szyfrowania dysku dla Linuksa. Może być używany do szyfrowania całych woluminów, partycji lub tworzenia zaszyfrowanych kontenerów.

[:octicons-repo-16: Strona główna](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Kod źródłowy" }

</details>

</div>

<details class="example" markdown>
<summary>Tworzenie i otwieranie zaszyfrowanych kontenerów</summary>

```bash
dd if=/dev/urandom of=/ścieżka-do-liku bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /ścieżka-do-pliku
```

#### Otwieranie zaszyfrowanych kontenerów

Zalecamy otwieranie kontenerów i wolumenów za pomocą `udisksctl`, ponieważ używa on [Polkit](https://en.wikipedia.org/wiki/Polkit). Większość menedżerów plików, takich jak te dołączone do popularnych środowisk graficznych, może odblokowywać zaszyfrowane pliki. Narzędzia takie jak [udiskie](https://github.com/coldfix/udiskie) mogą działać w zasobniku systemowym i zapewniać pomocny interfejs użytkownika.

```bash
udisksctl loop-setup -f /ścieżka-do-pliku
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Pamiętaj o tworzeniu kopii zapasowych nagłówków woluminów</p>

Zalecamy, aby zawsze [tworzyć kopie zapasowe nagłówków LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) w przypadku częściowej awarii dysku. Można to zrobić za pomocą

``bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Wiersz poleceń

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Narzędzia z interfejsem wiersza poleceń są przydatne do integracji [skryptów powłoki](https://en.wikipedia.org/wiki/Shell_script).

### Kryptor

<div class="admonition recommendation" markdown>

![Logo Kryptor](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** to darmowe i open source narzędzie do szyfrowania i podpisywania plików, które wykorzystuje nowoczesne i bezpieczne algorytmy kryptograficzne. Stara się być lepszą wersją [age](https://github.com/FiloSottile/age) i [Minisign](https://jedisct1.github.io/minisign), zapewniając prostą, łatwiejszą alternatywę dla GPG.

[:octicons-home-16: Strona główna](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Logo Tomb](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** jest powłoką wiersza poleceń dla LUKS. Wspiera steganografię poprzez [narzędzia firm trzecich](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Strona główna](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Wesprzyj" }

</details>

</div>

## OpenPGP

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Dostawcy usług](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP jest czasem potrzebny do konkretnych zadań, takich jak podpisywanie i szyfrowanie wiadomości e-mail. PGP ma wiele funkcji i jest [skomplikowany](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html), ponieważ istnieje od dawna. W przypadku zadań takich jak podpisywanie lub szyfrowanie plików sugerujemy powyższe opcje.

Podczas szyfrowania za pomocą PGP masz możliwość skonfigurowania różnych opcji w pliku `gpg.conf.` Zalecamy pozostanie przy standardowych opcjach określonych w [FAQ użytkownika GnuPG](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Użyj przyszłych wartości domyślnych podczas generowania klucza</p>

Podczas [generowania kluczy](https://gnupg.org/gph/en/manual/c14.html) sugerujemy użycie komendy 'future-default`, ponieważ poinstruuje to GnuPG, aby używał nowoczesnej kryptografii, takiej jak [Curve25519](https://en.wikipedia.org/wiki/Curve25519#History) i [Ed25519](https://ed25519.cr.yp.to):

``bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![Logo GNU Privacy Guard](assets/img/encryption-software/gnupg.svg){ align=right }

**GnuPG** jest licencjonowaną na GPL alternatywą dla pakietu oprogramowania kryptograficznego PGP. GnuPG jest zgodny z [RFC 4880](https://tools.ietf.org/html/rfc4880), który jest aktualną specyfikacją IETF OpenPGP. Projekt GnuPG pracował nad [zaktualizowaną wersją roboczą](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh), próbując zmodernizować OpenPGP. GnuPG jest częścią projektu oprogramowania GNU Fundacji Wolnego Oprogramowania i otrzymał znaczne [finansowanie](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) od rządu niemieckiego.

[:octicons-home-16: Strona główna](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![Logo GPG4win](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** to pakiet dla Windows od [Intevation i g10 Code](https://gpg4win.org/impressum.html). Zawiera [różne narzędzia](https://gpg4win.org/about.html), które mogą pomóc w korzystaniu z GPG w systemie Microsoft Windows. Projekt został zainicjowany i pierwotnie [sfinansowany przez](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) niemiecki Federalny Urząd ds. Bezpieczeństwa Informacji (BSI) w 2005 roku.

[:octicons-home-16: Strona główna](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition recommendation" markdown>

![Logo GPG Suite](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** zapewnia obsługę OpenPGP dla [Apple Mail](email-clients.md#apple-mail-macos) i innych klientów poczty e-mail w systemie macOS.

Zalecamy zapoznanie się z ich [Pierwszymi krokami](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) i [Bazą wiedzy](https://gpgtools.tenderapp.com/kb) w celu uzyskania wsparcia.

[:octicons-home-16: Strona główna](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

Obecnie GPG Suite [nie ma jeszcze](https://gpgtools.com/sequoia) stabilnej wersji dla wydań macOS Sonoma i nowszych.

### OpenKeychain

<div class="admonition recommendation" markdown>

![Logo OpenKeychain](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** jest implementacją GnuPG dla Androida. Jest to często wymagane przez klientów poczty takich jak [Thunderbird](email-clients.md#thunderbird), [FairEmail](email-clients.md#fairemail-android) i inne aplikacje na Androida, aby zapewnić obsługę szyfrowania.

[:octicons-home-16: Strona główna](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play] (https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 przeprowadziło [audyt bezpieczeństwa](https://openkeychain.org/openkeychain-3-6) OpenKeychain 3.6 w październiku 2015 roku. Opublikowany audyt i rozwiązania OpenKeychain dotyczące kwestii poruszonych w audycie można znaleźć [tutaj.](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015)

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Międzyplatformowe aplikacje szyfrujące muszą być open source.
- Aplikacje do szyfrowania plików muszą obsługiwać odszyfrowanie na Linuksie, macOS i Windows.
- Zewnętrzne aplikacje do szyfrowania dysków muszą obsługiwać odszyfrowanie na Linuksie, macOS i Windows.
- Wewnętrzne (Systemu operacyjnego) aplikacje do szyfrowania dysków muszą być wieloplatformowe lub wbudowane w system operacyjny natywnie.

### Najlepszy scenariusz

Nasze kryteria „najlepszego scenariusza” określają, jak powinien wyglądać idealny projekt w tej kategorii. Nasze zalecenia nie muszą spełniać wszystkich tych warunków, jednak projekty, które spełniają więcej z nich, mogą być oceniane wyżej od pozostałych na stronie.

- Aplikacje szyfrujące system operacyjny (FDE) powinny wykorzystywać zabezpieczenia sprzętowe, takie jak TPM lub Secure Enclave.
- Aplikacje do szyfrowania plików powinny mieć wsparcie producenta lub firm trzecich dla platform mobilnych.
