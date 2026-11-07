---
meta_title: "Zalecenia narzędzi i usługi do ochrony prywatności bez reklam – Privacy Guides"
title: "Narzędzia do ochrony prywatności"
icon: material/tools
hide:
  - toc
description: Pełna lista narzędzi, usług, oprogramowania i sprzętu do ochrony prywatności polecanych przez społeczność Privacy Guides.
---

Jeśli szukasz konkretnego rozwiązania, oto zalecany przez nas sprzęt i oprogramowanie w różnych kategoriach. Nasze zalecenia dotyczące narzędzi do ochrony prywatności opierają się przede wszystkim na funkcjach bezpieczeństwa, z dodatkowym naciskiem na narzędzia zdecentralizowane i open source. Nadają się do różnych modeli zagrożeń — od ochrony przed globalnymi systemami masowej inwigilacji i unikania wielkich firm technologicznych po łagodzenie ataków — ale ostatecznie to Ty musisz zdecydować, co najlepiej odpowiada Twoim potrzebom.

<div class="grid" markdown>

<div markdown>
[Dostawcy VPN](vpn.md){ .md-button }
[Menedżery haseł](passwords.md){ .md-button }
[Dostawcy poczty e-mail](email.md){ .md-button }
[Rozszerzenia przeglądarki](browser-extensions.md){ .md-button }
[Serwery DNS](dns.md){ .md-button }
[Usługi aliasingu e-mail](email-aliasing.md){ .md-button }
[Narzędzia do zarządzania zdjęciami](photo-management.md){ .md-button }
</div>

</div>

<div markdown>

<div class="admonition info" markdown>

[Zalecenia dotyczące samodzielnego hostowania](self-hosting/index.md) zostały przeniesione do osobnej kategorii.

</div>

</div>

Jeśli potrzebujesz pomocy w ustaleniu, które narzędzia do ochrony prywatności i alternatywne programy będą najlepsze dla Twoich potrzeb, rozpocznij dyskusję na naszym [forum](https://discuss.privacyguides.net) lub w naszej społeczności [Matrix](https://matrix.to/#/#privacyguides:matrix.org)!

Aby uzyskać więcej informacji na temat każdego projektu, dlaczego został wybrany, oraz dodatkowe wskazówki i porady, kliknij link „Dowiedz się więcej” w danej sekcji albo kliknij bezpośrednio na zalecenie, by przejść do konkretnej sekcji strony.

<div class="grid" markdown>

<div markdown>
- [x] **Zalecenia bez reklam**
- [x] **Częste aktualizacje**
- [x] **Zaufanie czytelników**
</div>

<div markdown>
- [x] **Pełna niezależność redakcyjna**
- [x] **Wkład open source**
- [x] **Zaufanie dziennikarzy**
</div>

</div>

## Prywatne przeglądarki internetowe

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/images/browsers/tor.svg){ align=left }

**Tor Browser** (Desktop & Android) is the top choice if you need anonymity, as it provides you with access to the **Tor** network, a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. Osoby i organizacje mogą również wymieniać się informacjami w sieci Tor za pomocą „ukrytych usług .onion”, nie narażając swojej prywatności. Dzięki temu, że ruch w sieci Tor jest trudny do zablokowania i namierzenia, Tor stanowi skuteczne narzędzie do omijania cenzury.

[Przeczytaj naszą pełną recenzję :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary }

</div>

<div class="grid cards" markdown>

- ![Mullvad Browser logo](assets/images/browsers/mullvad_browser.svg){ .lg .middle .twemoji } **Mullvad Browser**

    ---

    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users.

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#mullvad-browser)

- ![Firefox logo](assets/images/browsers/firefox.svg){ .lg .middle .twemoji } **Firefox**

    ---

    **Firefox** is a great Chromium alternative which provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#firefox)

- ![Brave logo](assets/images/browsers/brave.svg){ .lg .middle .twemoji } **Brave Browser**

    ---

    **Brave** is a private-by-default browser based on Chromium, so it should feel familiar and have minimal website compatibility issues.

    - [Brave Desktop Review :material-arrow-right-drop-circle:](desktop-browsers.md#brave)
    - [Brave Mobile Review :material-arrow-right-drop-circle:](mobile-browsers.md#brave)

- ![Safari logo](assets/images/browsers/safari.svg){ .lg .middle .twemoji } **Safari (iOS)**

    ---

    We recommend **Safari** due to its [anti-fingerprinting](https://webkit.org/blog/15697/private-browsing-2-0) features and default tracker blocking. Oddziela też pliki cookie w trybie przeglądania prywatnego, co zapobiega śledzeniu między kartami.

    - [Przeczytaj pełną recenzję :material-arrow-right-drop-circle:](mobile-browsers.md#safari-ios)

</div>

<div class="grid" markdown>

<div markdown>
### Rozszerzenia przeglądarki

<div class="grid cards" markdown>

- ![uBlock Origin logo](assets/images/browsers/ublock_origin.svg){ .twemoji loading=lazy } [uBlock Origin](browser-extensions.md#ublock-origin)
- ![uBlock Origin Lite logo](assets/images/browsers/ublock_origin_lite.svg){ .twemoji loading=lazy } [uBlock Origin Lite](browser-extensions.md#ublock-origin-lite)
- ![AdGuard logo](assets/images/browsers/adguard.svg){ .twemoji loading=lazy } [AdGuard for iOS](browser-extensions.md#adguard)

</div>

</div>

<div markdown>
### Inne narzędzia sieci Tor

<div class="grid cards" markdown>

- ![Onion Browser logo](assets/images/self-contained-networks/onion_browser.svg){ .twemoji loading=lazy } [Onion Browser (Tor for iOS)](tor.md#onion-browser-ios)

</div>

</div>

</div>

## Najlepsza trójka prywatnych dostawców VPN

<details class="danger" markdown>
<summary>VPN nie zapewnia anonimowości</summary>

Korzystanie z VPN **nie** uczyni Twojej aktywności w sieci anonimową ani nie zwiększy bezpieczeństwa niezabezpieczonego ruchu (HTTP).

Jeśli zależy Ci na **anonimowości**, skorzystaj z przeglądarki Tor Browser.

Jeśli zależy Ci na dodatkowym **bezpieczeństwie**, zawsze upewnij się, że łączysz się z witrynami za pomocą HTTPS. VPN nie zastępuje dobrych praktyk w zakresie bezpieczeństwa.

[Dowiedz się więcej :material-arrow-right-drop-circle:](vpn.md)

</details>

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/images/vpn/protonvpn.svg){ .lg .middle .twemoji } **Proton VPN**

    ---

    - [x] **112+ Countries**
    - [x] WireGuard Support
    - [x] Cash Payments
    - [x] Partial Port Forwarding Support
    - [ ] No IPv6

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#proton-vpn)

- ![IVPN logo](assets/images/vpn/mini/ivpn.svg){ .lg .middle .twemoji } **IVPN**

    ---

    - [x] **37+ Countries**
    - [x] WireGuard Support
    - [x] Monero & Cash Payments
    - [ ] No Port Forwarding
    - [ ] No IPv6

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#ivpn)

- ![Mullvad logo](assets/images/vpn/mullvad.svg){ .lg .middle .twemoji } **Mullvad**

    ---

    - [x] **49+ Countries**
    - [x] WireGuard Support
    - [x] Monero & Cash Payments
    - [ ] No Port Forwarding
    - [x] IPv6 Support

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#mullvad)

</div>

## Najlepsza trójka prywatnych dostawców poczty e-mail

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/images/email/protonmail.svg){ .lg .middle .twemoji } **Proton Mail**

    ---

    Proton Mail is an email service with a focus on privacy, encryption, security, and ease of use. Działa od 2013 roku. Proton AG ma siedzibę w Genewie, w Szwajcarii. Darmowy plan Proton Mail oferuje 500 MB miejsca na pocztę, które można bezpłatnie zwiększyć do 1 GB.

    [Read Full Review :material-arrow-right-drop-circle:](email.md#proton-mail)

- ![Mailbox Mail logo](assets/images/email/mailbox-mail.svg){ .lg .middle .twemoji } **Mailbox Mail**

    ---

    Mailbox Mail (formerly *Mailbox.org*) is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Działa od 2014 roku. Mailbox Mail ma siedzibę w Berlinie, w Niemczech. Konta oferują do 2 GB przestrzeni, którą można zwiększyć w razie potrzeby.

    [Read Full Review :material-arrow-right-drop-circle:](email.md#mailbox-mail)

- ![Tuta logo](assets/images/email/tuta.svg#only-light){ .lg .middle .twemoji }![Tuta logo](assets/images/email/tuta-dark.svg#only-dark){ .lg .middle .twemoji } **Tuta**

    ---

    Tuta (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Działa od 2011 roku i ma siedzibę w Hanowerze, w Niemczech. Darmowe konta zaczynają się od 1 GB przestrzeni.

    [Przeczytaj pełną recenzję :material-arrow-right-drop-circle:](email.md#tuta)

</div>

<div class="grid" markdown>

<div markdown>
### Usługi aliasingu e-mail

<div class="grid cards" markdown>

- ![Addy.io logo](assets/images/email-aliasing/addy.svg){ .twemoji loading=lazy } [Addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/images/email-aliasing/simplelogin.svg){ .twemoji loading=lazy } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

</div>

</div>

### Bezpieczne klienty poczty e-mail

<div class="grid cards" markdown>

- ![Thunderbird logo](assets/images/email-clients/thunderbird.svg){ .twemoji loading=lazy } [Thunderbird](email-clients.md#thunderbird)
- ![Apple Mail logo](assets/images/email-clients/applemail.png){ .twemoji loading=lazy } [Apple Mail (macOS)](email-clients.md#apple-mail-macos)
- ![FairEmail logo](assets/images/email-clients/fairemail.svg){ .twemoji loading=lazy } [FairEmail (Android)](email-clients.md#fairemail-android)
- ![GNOME Evolution logo](assets/images/email-clients/evolution.svg){ .twemoji loading=lazy } [GNOME Evolution (Linux)](email-clients.md#gnome-evolution-gnome)
- ![Kontact logo](assets/images/email-clients/kontact.svg){ .twemoji loading=lazy } [Kontact (Linux)](email-clients.md#kontact-kde)
- ![Mailvelope logo](assets/images/email-clients/mailvelope.svg){ .twemoji loading=lazy } [Mailvelope (PGP in standard webmail)](email-clients.md#mailvelope-browser)
- ![NeoMutt logo](assets/images/email-clients/mutt.svg){ .twemoji loading=lazy } [NeoMutt (CLI)](email-clients.md#neomutt-cli)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](email-clients.md)

## Inni prywatni dostawcy usług

### Przechowywanie w chmurze

<div class="grid cards" markdown>

- ![Proton Drive logo](assets/images/cloud/protondrive.svg){ .twemoji loading=lazy } [Proton Drive](cloud.md#proton-drive)
- ![Tresorit logo](assets/images/cloud/tresorit.svg){ .twemoji loading=lazy } [Tresorit](cloud.md#tresorit)
- ![Peergos logo](assets/images/cloud/peergos.svg){ .twemoji loading=lazy } [Peergos](cloud.md#peergos)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](cloud.md)

### Usługi usuwania danych

<div class="grid cards" markdown>

- ![EasyOptOuts logo](assets/images/data-broker-removals/easyoptouts.svg){ .twemoji loading=lazy } [EasyOptOuts](data-broker-removals.md#easyoptouts-paid)
- ![Google logo](assets/images/data-broker-removals/google.svg){ .twemoji loading=lazy } [Google *Results about you*](data-broker-removals.md#google-results-about-you-free)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](data-broker-removals.md)

### DNS

#### Dostawcy DNS

We [recommend](dns.md#recommended-providers) a number of encrypted DNS servers based on a variety of criteria, such as [Quad9](https://quad9.net) amongst others. Przed wyborem dostawcy zalecamy zapoznanie się z naszymi stronami poświęconymi tematyce DNS. W wielu przypadkach nie jest wskazane korzystanie z alternatywnego dostawcy DNS.

[Dowiedz się więcej :material-arrow-right-drop-circle:](dns.md)

#### Szyfrowane serwery proxy DNS

<div class="grid cards" markdown>

- ![RethinkDNS logo](assets/images/android/rethinkdns.svg#only-light){ .twemoji loading=lazy }![RethinkDNS logo](assets/images/android/rethinkdns-dark.svg#only-dark){ .twemoji loading=lazy } [RethinkDNS](dns.md#rethinkdns)
- ![DNSCrypt-Proxy logo](assets/images/dns/dnscrypt-proxy.svg){ .twemoji loading=lazy } [DNSCrypt-Proxy](dns.md#dnscrypt-proxy)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](dns.md#encrypted-dns-proxies)

### Usługi finansowe

#### Usługi maskowania płatności

<div class="grid cards" markdown>

- ![Privacy.com logo](assets/images/financial-services/privacy_com.svg#only-light){ .twemoji loading=lazy }![Privacy.com logo](assets/images/financial-services/privacy_com-dark.svg#only-dark){ .twemoji loading=lazy } [Privacy.com](financial-services.md#privacycom-us)
- ![MySudo logo](assets/images/financial-services/mysudo.svg#only-light){ .twemoji loading=lazy }![MySudo logo](assets/images/financial-services/mysudo-dark.svg#only-dark){ .twemoji loading=lazy } [MySudo](financial-services.md#mysudo-us-paid)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](financial-services.md#payment-masking-services)

#### Internetowe giełdy kart podarunkowych

<div class="grid cards" markdown>

- ![Coincards logo](assets/images/financial-services/coincards.svg){ .twemoji loading=lazy } [Coincards](financial-services.md#coincards)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](financial-services.md#gift-card-marketplaces)

### Zarządzanie zdjęciami

<div class="grid cards" markdown>

- ![Ente logo](assets/images/photo-management/ente.svg){ .twemoji loading=lazy } [Ente Photos](photo-management.md#ente-photos)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](photo-management.md)

### Wyszukiwarki

<div class="grid cards" markdown>

- ![Brave Search logo](assets/images/search-engines/brave-search.svg){ .twemoji loading=lazy } [Brave Search](search-engines.md#brave-search)
- ![DuckDuckGo logo](assets/images/search-engines/duckduckgo.svg){ .twemoji loading=lazy } [DuckDuckGo](search-engines.md#duckduckgo)
- ![SearXNG logo](assets/images/search-engines/searxng.svg){ .twemoji loading=lazy } [SearXNG](search-engines.md#searxng)
- ![Startpage logo](assets/images/search-engines/startpage.svg#only-light){ .twemoji loading=lazy }![Startpage logo](assets/images/search-engines/startpage-dark.svg#only-dark){ .twemoji loading=lazy } [Startpage](search-engines.md#startpage)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](search-engines.md)

## Oprogramowanie

### Czaty AI

<div class="grid cards" markdown>

- ![Kobold logo](assets/images/ai-chat/kobold.png){ .twemoji loading=lazy } [Kobold.cpp](ai-chat.md#koboldcpp)
- ![Llamafile logo](assets/images/ai-chat/llamafile.webp){ .twemoji loading=lazy } [Llamafile](ai-chat.md#llamafile)
- ![Ollama logo](assets/images/ai-chat/ollama.png){ .twemoji loading=lazy } [Ollama (CLI)](ai-chat.md#ollama-cli)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](ai-chat.md)

### Synchronizacja kalendarza

<div class="grid cards" markdown>

- ![Tuta logo](assets/images/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/images/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](calendar.md#tuta)
- ![Proton Calendar logo](assets/images/calendar/proton-calendar.svg){ .twemoji loading=lazy } [Proton Calendar](calendar.md#proton-calendar)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](calendar.md)

### Kryptowaluty

<div class="grid cards" markdown>

- ![Monero logo](assets/images/cryptocurrency/monero.svg){ .twemoji loading=lazy } [Monero](cryptocurrency.md#monero)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](cryptocurrency.md)

### Redakcja danych i metadanych

<div class="grid cards" markdown>

- ![MAT2 logo](assets/images/data-redaction/mat2.svg){ .twemoji loading=lazy } [MAT2](data-redaction.md#mat2)
- ![Metadata Cleaner](assets/images/data-redaction/metadatacleaner.svg){ .twemoji loading-lazy } [Metadata Cleaner](data-redaction.md#metadata-cleaner)
- ![ExifEraser logo](assets/images/data-redaction/exiferaser.svg){ .twemoji loading=lazy } [ExifEraser (Android)](data-redaction.md#exiferaser-android)
- ![ExifTool logo](assets/images/data-redaction/exiftool.png){ .twemoji loading=lazy } [ExifTool (CLI)](data-redaction.md#exiftool-cli)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](data-redaction.md)

### Współpraca nad dokumentami

<div class="grid cards" markdown>

- ![CryptPad logo](assets/images/document-collaboration/cryptpad.svg){ .twemoji loading=lazy } [CryptPad](document-collaboration.md#cryptpad)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](document-collaboration.md)

### Oprogramowanie szyfrujące

<details class="info" markdown>
<summary>Szyfrowanie systemu operacyjnego</summary>

Do szyfrowania dysku z systemem operacyjnym zwykle zalecamy użycie narzędzia szyfrującego dostarczonego przez system operacyjny, na przykład **BitLocker** w systemie Windows, **FileVault** w systemie macOS lub **LUKS** w systemie Linux. Narzędzia te są wbudowane w system i wykorzystują elementy szyfrowania sprzętowego, takie jak [bezpieczny kryptoprocesor](basics/hardware.md/#tpmsecure-cryptoprocessor).

[Dowiedz się więcej :material-arrow-right-drop-circle:](encryption.md#operating-system-encryption)

</details>

#### Narzędzia wieloplatformowe

<div class="grid cards" markdown>

- ![Cryptomator logo](assets/images/encryption-software/cryptomator.svg){ .twemoji loading=lazy } [Cryptomator](encryption.md#cryptomator-cloud)
- ![VeraCrypt logo](assets/images/encryption-software/veracrypt.svg#only-light){ .twemoji loading=lazy }![VeraCrypt logo](assets/images/encryption-software/veracrypt-dark.svg#only-dark){ .twemoji loading=lazy } [VeraCrypt (FDE)](encryption.md#veracrypt-disk)
- ![Kryptor logo](assets/images/encryption-software/kryptor.png){ .twemoji loading=lazy } [Kryptor](encryption.md#kryptor)
- ![Tomb logo](assets/images/encryption-software/tomb.png){ .twemoji loading=lazy } [Tomb](encryption.md#tomb)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](encryption.md)

#### Klienty OpenPGP

<div class="grid cards" markdown>

- ![GnuPG logo](assets/images/encryption-software/gnupg.svg){ .twemoji loading=lazy } [GnuPG](encryption.md#gnu-privacy-guard)
- ![GPG4Win logo](assets/images/encryption-software/gpg4win.svg){ .twemoji loading=lazy } [GPG4Win (Windows)](encryption.md#gpg4win)
- ![GPG Suite logo](assets/images/encryption-software/gpgsuite.png){ .twemoji loading=lazy } [GPG Suite (macOS)](encryption.md#gpg-suite)
- ![OpenKeychain logo](assets/images/encryption-software/openkeychain.svg){ .twemoji loading=lazy } [OpenKeychain](encryption.md#openkeychain)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](encryption.md#openpgp)

### Udostępnianie i synchronizacja plików

<div class="grid cards" markdown>

- ![Send logo](assets/images/file-sharing-sync/send.svg){ .twemoji loading=lazy } [Send](file-sharing.md#send)
- ![OnionShare logo](assets/images/file-sharing-sync/onionshare.svg){ .twemoji loading=lazy } [OnionShare](file-sharing.md#onionshare)
- ![Syncthing logo](assets/images/file-sharing-sync/syncthing.svg){ .twemoji loading=lazy } [Syncthing](file-sharing.md#syncthing-p2p)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](file-sharing.md)

### Alternatywne interfejsy

<div class="grid cards" markdown>

- ![Redlib logo](assets/images/frontends/redlib.svg){ .twemoji loading=lazy } [Redlib (Reddit, Web)](frontends.md#redlib)
- ![FreeTube logo](assets/images/frontends/freetube.svg){ .twemoji loading=lazy } [FreeTube (YouTube, Desktop)](frontends.md#freetube)
- ![LibreTube logo](assets/images/frontends/libretube.svg#only-light){ .twemoji loading=lazy }![LibreTube logo](assets/images/frontends/libretube-dark.svg#only-dark){ .twemoji loading=lazy } [LibreTube (YouTube, Android)](frontends.md#libretube-android)
- ![NewPipe logo](assets/images/frontends/newpipe.svg){ .twemoji loading=lazy } [NewPipe (YouTube, Android)](frontends.md#newpipe-android)
- ![Invidious logo](assets/images/frontends/invidious.svg#only-light){ .twemoji loading=lazy }![Invidious logo](assets/images/frontends/invidious-dark.svg#only-dark){ .twemoji loading=lazy } [Invidious (YouTube, Web)](frontends.md#invidious)
- ![Piped logo](assets/images/frontends/piped.svg){ .twemoji loading=lazy } [Piped (YouTube, Web)](frontends.md#piped)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](frontends.md)

### Aplikacje zdrowotne i wellbeing

<div class="grid cards" markdown>

- ![Drip logo](assets/images/health-and-wellness/drip.png){ .twemoji loading=lazy } [Drip](health-and-wellness.md#drip)
- ![Euki logo](assets/images/health-and-wellness/euki.svg){ .twemoji loading=lazy } [Euki](health-and-wellness.md#euki)
- ![Apple Health logo](assets/images/health-and-wellness/apple-health.webp#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/images/health-and-wellness/apple-health-dark.webp#only-dark){ .twemoji loading=lazy } [Apple Health](health-and-wellness.md#apple-health)
- ![Apple Fitness logo](assets/images/health-and-wellness/apple-fitness.webp){ .twemoji loading=lazy } [Apple Fitness](health-and-wellness.md#apple-fitness)
- ![Gadgetbridge logo](assets/images/health-and-wellness/gadgetbridge.svg#only-light){ .twemoji loading=lazy }![Gadgetbridge logo](assets/images/health-and-wellness/gadgetbridge-dark.svg#only-dark){ .twemoji loading=lazy } [Gadgetbridge](health-and-wellness.md#gadgetbridge)
- ![Apple Health logo](assets/images/health-and-wellness/apple-health.webp#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/images/health-and-wellness/apple-health-dark.webp#only-dark){ .twemoji loading=lazy } [Apple Health Records](health-and-wellness.md#apple-health-records)
- ![CommonHealth logo](assets/images/health-and-wellness/commonhealth.png){ .twemoji loading=lazy } [CommonHealth](health-and-wellness.md#commonhealth)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](health-and-wellness.md)

### Narzędzia językowe

<div class="grid cards" markdown>

- ![LibreTranslate logo](assets/images/language-tools/libretranslate.png){ .twemoji } [LibreTranslate](language-tools.md#libretranslate)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](language-tools.md)

### Mapy i aplikacje nawigacyjne

<div class="grid cards" markdown>

- ![Organic Maps logo](assets/images/maps/organic-maps.svg){ .twemoji loading=lazy } [Organic Maps](maps.md#organic-maps)
- ![OsmAnd logo](assets/images/maps/osmand.svg){ .twemoji loading=lazy } [OsmAnd](maps.md#osmand)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](maps.md)

### Narzędzia uwierzytelniania wieloskładnikowego

**Uwaga:** [Sprzętowe klucze bezpieczeństwa](#security-keys) zostały przeniesione do osobnej kategorii.

<div class="grid cards" markdown>

- ![Ente Auth logo](assets/images/multi-factor-authentication/ente-auth.svg){ .twemoji loading=lazy } [Ente Auth](multi-factor-authentication.md#ente-auth)
- ![Aegis logo](assets/images/multi-factor-authentication/aegis.png){ .twemoji loading=lazy } [Aegis Authenticator (Android)](multi-factor-authentication.md#aegis-authenticator-android)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](multi-factor-authentication.md)

### Agregatory wiadomości

<div class="grid cards" markdown>

- ![Akregator logo](assets/images/news-aggregators/akregator.svg){ .twemoji loading=lazy } [Akregator](news-aggregators.md#akregator)
- ![NewsFlash logo](assets/images/news-aggregators/newsflash.png){ .twemoji loading=lazy } [NewsFlash](news-aggregators.md#newsflash)
- ![Feeder logo](assets/images/news-aggregators/feeder.png){ .twemoji} [Feeder (Android)](news-aggregators.md#feeder)
- ![Miniflux logo](assets/images/news-aggregators/miniflux.svg#only-light){ .twemoji loading=lazy }![Miniflux logo](assets/images/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji loading=lazy } [Miniflux](news-aggregators.md#miniflux)
- ![NetNewsWire logo](assets/images/news-aggregators/netnewswire.png){ .twemoji loading=lazy } [NetNewsWire](news-aggregators.md#netnewswire)
- ![Newsboat logo](assets/images/news-aggregators/newsboat.svg){ .twemoji loading=lazy } [Newsboat](news-aggregators.md#newsboat)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](news-aggregators.md)

### Notatniki

<div class="grid cards" markdown>

- ![Standard Notes logo](assets/images/notebooks/standard-notes.svg){ .twemoji loading=lazy } [Standard Notes](notebooks.md#standard-notes)
- ![Notesnook logo](assets/images/notebooks/notesnook.svg){ .twemoji loading=lazy } [Notesnook](notebooks.md#notesnook)
- ![Joplin logo](assets/images/notebooks/joplin.svg){ .twemoji loading=lazy } [Joplin](notebooks.md#joplin)
- ![Cryptee logo](assets/images/notebooks/cryptee.svg#only-light){ .twemoji loading=lazy }![Cryptee logo](assets/images/notebooks/cryptee-dark.svg#only-dark){ .twemoji loading=lazy } [Cryptee](notebooks.md#cryptee)
- ![Org-mode logo](assets/images/notebooks/org-mode.svg){ .twemoji loading=lazy } [Org-mode](notebooks.md#org-mode)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](notebooks.md)

### Pakiety biurowe

<div class="grid cards" markdown>

- ![LibreOffice logo](assets/images/office-suites/libreoffice.svg){ .twemoji loading=lazy } [LibreOffice](office-suites.md#libreoffice)
- ![OnlyOffice logo](assets/images/office-suites/onlyoffice.svg){ .twemoji loading=lazy } [OnlyOffice](office-suites.md#onlyoffice)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](office-suites.md)

### Menedżery haseł

<div class="grid cards" markdown>

- ![Bitwarden logo](assets/images/password-management/bitwarden.svg){ .twemoji loading=lazy } [Bitwarden](passwords.md#bitwarden)
- ![Proton Pass logo](assets/images/password-management/protonpass.svg){ .twemoji loading=lazy } [Proton Pass](passwords.md#proton-pass)
- ![1Password logo](assets/images/password-management/1password.svg){ .twemoji loading=lazy } [1Password](passwords.md#1password)
- ![Psono logo](assets/images/password-management/psono.svg){ .twemoji loading=lazy } [Psono](passwords.md#psono)
- ![KeePassXC logo](assets/images/password-management/keepassxc.svg){ .twemoji loading=lazy } [KeePassXC](passwords.md#keepassxc)
- ![KeePassDX logo](assets/images/password-management/keepassdx.svg){ .twemoji loading=lazy } [KeePassDX (Android)](passwords.md#keepassdx-android)
- ![KeePassium logo](assets/images/password-management/keepassium.svg){ .twemoji loading=lazy } [KeePassium (iOS & macOS)](passwords.md#keepassium-ios-macos)
- ![Gopass logo](assets/images/password-management/gopass.svg){ .twemoji loading=lazy } [Gopass (CLI)](passwords.md#gopass-cli)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](passwords.md)

### Pastebiny

<div class="grid cards" markdown>

- ![PrivateBin logo](assets/images/pastebins/privatebin.svg){ .twemoji loading=lazy } [PrivateBin](pastebins.md#privatebin)
- ![Paaster logo](assets/images/pastebins/paaster.svg){ .twemoji loading=lazy } [Paaster](pastebins.md#paaster)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](pastebins.md)

### Komunikacja w czasie rzeczywistym

<div class="grid cards" markdown>

- ![Signal logo](assets/images/messengers/signal.svg){ .twemoji loading=lazy } [Signal](real-time-communication.md#signal)
- ![Briar logo](assets/images/messengers/briar.svg){ .twemoji loading=lazy } [Briar](real-time-communication.md#briar)
- ![SimpleX Chat logo](assets/images/messengers/simplex.svg){ .twemoji loading=lazy } [SimpleX Chat](real-time-communication.md#simplex-chat)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](real-time-communication.md)

### Serwisy społecznościowe

<div class="grid cards" markdown>

- ![Mastodon logo](assets/images/social-networks/mastodon.svg){ .twemoji loading=lazy } [Mastodon](social-networks.md#mastodon)
- ![Element logo](assets/images/social-networks/element.svg){ .twemoji loading=lazy } [Element](social-networks.md#element)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](social-networks.md)

## Sprzęt

### Klucze bezpieczeństwa

<div class="grid cards" markdown>

- ![Yubico logo](assets/images/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [Yubico Security Key](security-keys.md#yubico-security-key)
- ![Yubico logo](assets/images/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [YubiKey](security-keys.md#yubikey)
- ![Nitrokey](assets/images/security-keys/mini/nitrokey.svg){ .twemoji loading=lazy } [Nitrokey](security-keys.md#nitrokey)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](security-keys.md)

### Telefony komórkowe

<div class="grid cards" markdown>

- ![Google Pixel 6](assets/images/android/google-pixel.png){ .twemoji loading=lazy } [Google Pixel](mobile-phones.md#google-pixel)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](mobile-phones.md)

## Systemy operacyjne

### Na urządzenia mobilne

#### Niestandardowe systemy operacyjne Android

<div class="grid cards" markdown>

- ![GrapheneOS logo](assets/images/android/grapheneos.svg#only-light){ .twemoji loading=lazy }![GrapheneOS logo](assets/images/android/grapheneos-dark.svg#only-dark){ .twemoji loading=lazy } [GrapheneOS](android/distributions.md#grapheneos)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](android/distributions.md)

#### Aplikacje na Androida

<div class="grid cards" markdown>

- ![Shelter logo](assets/images/android/mini/shelter.svg){ .twemoji loading=lazy } [Shelter (Work Profiles)](android/general-apps.md#shelter)
- ![Secure Camera logo](assets/images/android/secure_camera.svg#only-light){ .twemoji loading=lazy }![Secure Camera logo](assets/images/android/secure_camera-dark.svg#only-dark){ .twemoji loading=lazy } [Secure Camera](android/general-apps.md#secure-camera)
- ![Secure PDF Viewer logo](assets/images/android/secure_pdf_viewer.svg#only-light){ .twemoji loading=lazy }![Secure PDF Viewer logo](assets/images/android/secure_pdf_viewer-dark.svg#only-dark){ .twemoji loading=lazy } [Secure PDF Viewer](android/general-apps.md#secure-pdf-viewer)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](android/general-apps.md)

#### Sposoby pozyskiwania aplikacji na Androida

<div class="grid cards" markdown>

- ![Obtainium logo](assets/images/android/obtainium.svg){ .twemoji loading=lazy } [Obtainium (App Manager)](android/obtaining-apps.md#obtainium)
- ![Aurora Store logo](assets/images/android/aurora-store.webp){ .twemoji loading=lazy } [Aurora Store (Google Play Client)](android/obtaining-apps.md#aurora-store)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](android/obtaining-apps.md)

### Na komputery stacjonarne/osobiste

<div class="grid cards" markdown>

- ![Qubes OS logo](assets/images/qubes/qubes_os.svg){ .twemoji loading=lazy } [Qubes OS (Xen VM Distribution)](desktop.md#qubes-os)
- ![Fedora logo](assets/images/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Linux](desktop.md#fedora-linux)
- ![openSUSE Tumbleweed logo](assets/images/linux-desktop/opensuse-tumbleweed.svg){ .twemoji loading=lazy } [openSUSE Tumbleweed](desktop.md#opensuse-tumbleweed)
- ![Arch logo](assets/images/linux-desktop/archlinux.svg){ .twemoji loading=lazy } [Arch Linux](desktop.md#arch-linux)
- ![Fedora logo](assets/images/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Atomic Desktops](desktop.md#fedora-atomic-desktops)
- ![NixOS logo](assets/images/linux-desktop/nixos.svg){ .twemoji loading=lazy } [NixOS](desktop.md#nixos)
- ![Whonix logo](assets/images/linux-desktop/whonix.svg){ .twemoji loading=lazy } [Whonix (Tor)](desktop.md#whonix)
- ![Tails logo](assets/images/linux-desktop/tails.svg){ .twemoji loading=lazy } [Tails (Live Boot)](desktop.md#tails)
- ![Secureblue logo](assets/images/linux-desktop/secureblue.svg){ .twemoji loading=lazy } [Secureblue](desktop.md#secureblue)
- ![Kicksecure logo](assets/images/linux-desktop/kicksecure.svg){ .twemoji loading=lazy } [Kicksecure](desktop.md#kicksecure)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](desktop.md)

### Oprogramowanie układowe routera

<div class="grid cards" markdown>

- ![OpenWrt logo](assets/images/router/openwrt.svg#only-light){ .twemoji loading=lazy }![OpenWrt logo](assets/images/router/openwrt-dark.svg#only-dark){ .twemoji loading=lazy } [OpenWrt](router.md#openwrt)
- ![OPNsense logo](assets/images/router/opnsense.svg){ .twemoji loading=lazy } [OPNsense](router.md#opnsense)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](router.md)

## Narzędzia zaawansowane

Te narzędzia mogą być przydatne dla niektórych osób. Oferują funkcje, którymi większość osób nie musi się przejmować, i często wymagają bardziej zaawansowanej wiedzy technicznej, aby można było z nich skutecznie korzystać.

### Sieci alternatywne

<div class="grid cards" markdown>

- ![I2P logo](assets/images/self-contained-networks/i2p.svg#only-light){ .twemoji loading=lazy } ![I2P logo](assets/images/self-contained-networks/i2p-dark.svg#only-dark){ .twemoji loading=lazy } [I2P](alternative-networks.md#i2p-the-invisible-internet-project)
- ![Tor logo](assets/images/self-contained-networks/tor.svg){ .twemoji loading=lazy } [Tor](alternative-networks.md#tor)
- ![Orbot logo](assets/images/self-contained-networks/orbot.svg){ .twemoji loading=lazy } [Orbot (Mobile Tor Proxy)](alternative-networks.md#orbot)
- ![Snowflake logo](assets/images/self-contained-networks/snowflake.svg#only-light){ .twemoji loading=lazy }![Snowflake logo](assets/images/self-contained-networks/snowflake-dark.svg#only-dark){ .twemoji loading=lazy } [Snowflake](alternative-networks.md#snowflake)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](alternative-networks.md)

### Weryfikacja integralności urządzenia

<div class="grid cards" markdown>

- ![MVT logo](assets/images/device-integrity/mvt.webp#only-light){ .twemoji loading=lazy }![MVT logo](assets/images/device-integrity/mvt-dark.png#only-dark){ .twemoji loading=lazy } [Mobile Verification Toolkit](device-integrity.md#mobile-verification-toolkit)
- ![iMazing logo](assets/images/device-integrity/imazing.png){ .twemoji loading=lazy } [iMazing (iOS)](device-integrity.md#imazing-ios)
- ![Auditor logo](assets/images/device-integrity/auditor.svg#only-light){ .twemoji loading=lazy }![Auditor logo](assets/images/device-integrity/auditor-dark.svg#only-dark){ .twemoji loading=lazy } [Auditor (Android)](device-integrity.md#auditor-android)

</div>

[Dowiedz się więcej :material-arrow-right-drop-circle:](device-integrity.md)
