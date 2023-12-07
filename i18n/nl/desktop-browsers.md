---
meta_title: "Privacy respecterende webbrowsers voor PC en Mac - Privacy Handleidingen"
title: "Desktop Browsers"
icon: material/laptop
description: Deze webbrowsers bieden sterkere privacybescherming dan Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Aanbevelingen voor privé desktopbrowsers
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://en.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

Dit zijn momenteel onze aanbevolen mobiele webbrowsers en configuraties. Wij bevelen [Mullvad Browser](#mullvad-browser) aan als je je richt op sterke privacybescherming en anti-vingerafdrukken uit de doos, [Firefox](#firefox) voor casual internetbrowsers op zoek naar een goed alternatief voor Google Chrome, en [Brave](#brave) als je Chromium-browsercompatibiliteit nodig hebt.

In het algemeen raden we aan om extensies tot een minimum te beperken: ze hebben geprivilegieerde toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-Uchnm34/m/lDaXwQhzBAAJ) site-isolatie. We doen op deze pagina enkele aanbevelingen voor de configuratie, maar alle andere browsers dan Tor Browser zullen op een of andere manier traceerbaar zijn via *iemand*.

## Mullvad Browser

!!! recommendation

    Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is een versie van [Tor Browser](tor.md#tor-browser) met zonder Tor netwerk integraties, gericht op het aanbieden van Tor Browser's anti-vingerafdruk browser technologieën aan VPN gebruikers. Het is ontwikkeld door het Tor Project en gedistribueerd door [Mullvad](vpn.md#mullvad), en vereist **niet** het gebruik van Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Net als [Tor Browser](tor.md), is Mullvad Browser ontworpen om fingerprinting te voorkomen door jouw browser fingerprint identiek te maken aan alle andere Mullvad Browser gebruikers, en het bevat standaard instellingen en extensies die automatisch worden geconfigureerd door de standaard beveiligingsniveaus: *Standaard*, *Veiliger* en *Veiligst*. Daarom is het noodzakelijk dat je de browser helemaal niet aanpast buiten het aanpassen van de standaard [beveiligingsniveaus](https://tb-manual.torproject.org/security-settings/). Andere wijzigingen zouden jouw vingerafdruk uniek maken, wat het doel van het gebruik van deze browser tenietdoet. Als je jouw browser zwaarder wilt configureren en fingerprinting voor jou geen probleem is, raden wij in plaats daarvan [Firefox](#firefox) aan.

### Anti-Fingerprinting

**Zonder** gebruik te maken van een [VPN](vpn.md), biedt Mullvad Browser dezelfde bescherming tegen [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) als andere private browsers zoals Firefox+[Arkenfox](#arkenfox-advanced) of [Brave](#brave). Mullvad Browser biedt deze bescherming out of the box, ten koste van enige flexibiliteit en gemak die andere privé-browsers kunnen bieden.

==Voor de sterkste bescherming tegen fingerprinting raden we aan Mullvad Browser te gebruiken in combinatie **met** een VPN==, of dat nu Mullvad is of een andere aanbevolen VPN-provider. Wanneer je een VPN met Mullvad Browser gebruikt, deelt je een vingerafdruk en een pool van IP-adressen met vele andere gebruikers, waardoor je een "menigte" krijgt om in op te gaan. Deze strategie is de enige manier om geavanceerde volgscripts te dwarsbomen, en is dezelfde anti-fingerprinting techniek die Tor Browser gebruikt.

Denk eraan dat je Mullvad Browser kunt gebruiken met elke VPN-provider, maar dat andere mensen op die VPN ook Mullvad Browser moeten gebruiken om deze "menigte" te laten bestaan, iets wat waarschijnlijker is bij Mullvad VPN in vergelijking met andere providers, vooral zo kort na de lancering van Mullvad Browser. Mullvad Browser heeft geen ingebouwde VPN-connectiviteit, noch controleert het of je een VPN gebruikt voordat je gaat browsen; jouw VPN-verbinding moet apart worden geconfigureerd en beheerd.

Mullvad Browser wordt geleverd met de *uBlock Origin* en *NoScript* browserextensies vooraf geïnstalleerd. Terwijl we meestal [niet aanbevelen](#extensions) *extra* browserextensies toe te voegen, deze extensies die vooraf geïnstalleerd zijn met de browser moeten **niet** verwijderd of geconfigureerd worden buiten de standaardwaarden omdat dit opvallend genoeg jouw browser vingerafdruk zou onderscheiden van andere Mullvad browsergebruikers. Het wordt ook vooraf geïnstalleerd met de Mullvad-browserextensie, die *kan* veilig worden verwijderd zonder jouw browservingerafdruk te beïnvloeden als je dat wilt, maar is ook veilig om te bewaren, zelfs als je geen Mullvad VPN gebruikt.

### Private Browsing Mode

Mullvad Browser werkt in een permanente privé browsing modus, wat betekent dat jouw geschiedenis, cookies en andere site gegevens altijd worden gewist elke keer dat de browser wordt gesloten. Jouw bladwijzers, browserinstellingen en extensie-instellingen blijven bewaard.

Dit is nodig om geavanceerde vormen van tracking te voorkomen, maar gaat wel ten koste van het gemak en sommige Firefox-functies, zoals Multi-Account Containers. Vergeet niet dat je altijd meerdere browsers kunt gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die anders niet goed werken in Mullvad Browser, en Mullvad Browser voor algemeen browsen.

### Mullvad Leta

Mullvad Browser wordt geleverd met DuckDuckGo ingesteld als de standaard [zoekmachine](search-engines.md), maar het komt ook voorgeïnstalleerd met **Mullvad Leta**, een zoekmachine die een actief Mullvad VPN-abonnement vereist om toegang te krijgen. Mullvad Leta bevraagt de betaalde zoek-API van Google rechtstreeks (daarom is het beperkt tot betalende abonnees), maar door deze beperking is het mogelijk voor Mullvad om zoekopdrachten en Mullvad VPN-accounts te correleren. Daarom raden wij het gebruik van Mullvad Leta af, ook al verzamelt Mullvad zeer weinig informatie over hun VPN-abonnees.

## Firefox

!!! recommendation

    ![Firefox-logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** biedt krachtige privacy-instellingen zoals [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), die kunnen helpen bij het blokkeren van verschillende [soorten tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
    [:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Broncode" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Bijdragen }
    
    ??? downloads "Downloaden"
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Firefox bevat een uniek [downloadtoken](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads van Mozilla's website en gebruikt telemetrie in Firefox om het token te verzenden. Het token is **niet** opgenomen in uitgaven van de [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Aanbevolen configuratie

Deze opties zijn te vinden in :material-menu: → **Instellingen**

#### Zoeken

- [ ] Uncheck **Geef zoeksuggesties**

Functies voor zoeksuggesties zijn mogelijk niet beschikbaar in jouw regio.

Zoeksuggesties sturen alles wat je in de adresbalk typt naar de standaardzoekmachine, ongeacht of je een echte zoekopdracht geeft. Door zoeksuggesties uit te schakelen, kun je nauwkeuriger bepalen welke gegevens je naar jouw zoekmachineprovider stuurt.

#### Privacy & beveiliging

##### Verbeterde traceringsbescherming

- [x] Select **Strict** Verbeterde traceringsbescherming

Dit beschermt je door het blokkeren van social media trackers, fingerprinting scripts (merk op dat dit je niet beschermt tegen *alle* fingerprinting), cryptominers, cross-site tracking cookies, en sommige andere tracking content. ETP beschermt tegen veel voorkomende bedreigingen, maar blokkeert niet alle tracking-wegen omdat het is ontworpen om de bruikbaarheid van de site zo min mogelijk of helemaal niet te beïnvloeden.

##### Firefox stelt voor (alleen VS)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is een functie vergelijkbaar met zoeksuggesties die alleen in de VS beschikbaar is. Wij raden aan dit uit te schakelen om dezelfde reden als waarom wij aanraden zoeksuggesties uit te schakelen. Als je deze opties niet ziet onder de kop **Adresbalk**, hebt je de nieuwe ervaring niet en kun je deze wijzigingen negeren.

- [ ] Deselecteer **Accepteer cookies van sites**
- [ ] Deselecteer **Suggesties van sponsors**

##### Saneren bij sluiten

Als je op bepaalde sites aangemeld wilt blijven, kunt je uitzonderingen toestaan in **Cookies en Sitegegevens** → **Uitzonderingen beheren...**

- [x] Check **Cookies en sitegegevens verwijderen wanneer Firefox wordt afgesloten**

Dit beschermt je tegen blijvende cookies, maar niet tegen cookies die tijdens een bepaalde surfsessie worden aangemaakt. Wanneer dit is ingeschakeld, wordt het mogelijk om jouw browsercookies gemakkelijk te wissen door Firefox gewoon opnieuw op te starten. Je kunt per site uitzonderingen instellen, als je ingelogd wilt blijven op een bepaalde site die je vaak bezoekt.

##### Telemetrie

- [ ] Uncheck **Firefox toestaan technische en interactiegegevens naar Mozilla**te sturen
- [ ] Uncheck **Firefox toestaan om studies te installeren en uit te voeren**uit
- [ ] Uncheck **Firefox toestaan om namens je achterstallige crashmeldingen te verzenden uit**

> Firefox stuurt ons gegevens over jouw Firefox-versie en -taal; besturingssysteem van het apparaat en hardwareconfiguratie; geheugen, basisinformatie over crashes en fouten; resultaat van geautomatiseerde processen zoals updates, veilig browsen en activering. Wanneer Firefox gegevens naar ons verzendt, wordt uw IP-adres tijdelijk verzameld als onderdeel van onze serverlogs.

Daarnaast verzamelt de Firefox Accounts service [enkele technische gegevens](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Als je een Firefox-account gebruikt, kun je je afmelden:

1. Open jouw [profielinstellingen op accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Schakel **Gegevensverzameling en -gebruik uit** > **Help Firefox-accounts verbeteren**

##### Alleen HTTPS-modus

- [x] Select **Schakel HTTPS-only modus in alle vensters in**

Dit voorkomt dat je onbedoeld verbinding maakt met een website in platte HTTP-tekst. Sites zonder HTTPS zijn tegenwoordig zeldzaam, dus dit zou weinig tot geen impact moeten hebben op jouw dagelijkse browsen.

##### DNS over HTTPS

Als u een [DNS boven HTTPS provider](dns.md) gebruikt:

- [x] Selecteer **Maximale Bescherming** en kies een geschikte provider

Max Bescherming forceert het gebruik van DNS via HTTPS. Een beveiligingswaarschuwing wordt weergegeven als Firefox geen verbinding kan maken met uw beveiligde DNS resolver, of als uw beveiligde DNS resolver zegt dat records voor het domein dat u probeert te openen, niet bestaan. Hiermee stopt het netwerk waarmee u bent verbonden om uw DNS-beveiliging stiekem te verlagen.

#### Synchronisatie

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) maakt jouw browsegegevens (geschiedenis, bladwijzers, enz.) toegankelijk op al jouw apparaten en beschermt ze met E2EE.

### Arkenfox (gevorderd)

!!! tip "Gebruik Mullvad Browser voor geavanceerde anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) biedt dezelfde anti-fingeprint bescherming als Arkenfox out of the box, en vereist niet het gebruik van Mullvad's VPN om van deze bescherming te profiteren. In combinatie met een VPN kan Mullvad Browser meer geavanceerde tracking scripts dwarsbomen dan Arkenfox. Arkenfox heeft nog steeds het voordeel dat het veel flexibeler is, en uitzonderingen per site toestaat voor websites waarop je ingelogd moet blijven.

Het [Arkenfox-project](https://github.com/arkenfox/user.js) biedt een reeks zorgvuldig overwogen opties voor Firefox. Als je [besluit](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) om Arkenfox te gebruiken, zijn er een [paar opties](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) die subjectief streng zijn en/of ervoor kunnen zorgen dat sommige websites niet goed werken - [die je gemakkelijk kunt wijzigen](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) om aan jouw behoeften te voldoen. Wij **raden je ten zeerste aan** hun volledige [wiki](https://github.com/arkenfox/user.js/wiki)door te lezen. Arkenfox biedt ook ondersteuning voor [container](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox wil alleen elementaire of naïeve volgscripts dwarsbomen via canvas randomisatie en de ingebouwde configuratie-instellingen voor vingerafdrukbestendigheid van Firefox. Het is niet de bedoeling dat jouw browser opgaat in een grote menigte van andere Arkenfox-gebruikers op dezelfde manier als Mullvad Browser of Tor Browser dat doen, wat de enige manier is om geavanceerde tracking-scripts voor vingerafdrukken te dwarsbomen. Je kunt altijd meerdere browsers gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die je anderszins vertrouwt, en Mullvad Browser voor algemeen browsen.

## Brave

!!! recommendation

    ![Brave-logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** bevat een ingebouwde inhoudsblokker en [privacyfuncties](https://brave.com/privacy-features/), waarvan vele standaard zijn ingeschakeld.
    
    Brave is gebouwd op het Chromium webbrowser project, dus het zou vertrouwd moeten aanvoelen en minimale website compatibiliteitsproblemen moeten hebben.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }.
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Broncode" }
    
    ??? downloads annotate "Downloaden"
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. We raden af om de Flatpak-versie van Brave te gebruiken, omdat die de sandbox van Chromium vervangt door die van Flatpak, wat minder effectief is. Bovendien wordt het pakket niet onderhouden door Brave Software, Inc.

**macOS-gebruikers:** De download van Brave Browser van hun officiële website is een `.pkg` installatieprogramma dat beheerdersrechten vereist om uit te voeren (en het kan andere onnodige scripts uitvoeren op uw machine). Als een alternatief kunt u de laatste `Brave-Browser-universal.dmg` file downloaden van hun [GitHub releases](https://github.com/brave/brave-browser/releases/latest) pagina, die een traditionele "Sleep naar Applicaties map" installatie biedt.

!!! waarschuwing

    Brave voegt een "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" toe aan de file naam in downloads van de Brave website, die wordt gebruikt om te volgen van welke bron de browser heeft gedownload. Als voorbeeld `BRV002` in een download genaamd `Brave-Browser-BRV002.pkg`. Het installatieprogramma zal aan het eind van het installatieproces de server van Brave pingen met de verwijzingscode. Als u zich hier zorgen om maakt kunt u de naam van de installer veranderen voor het openen.

### Aanbevolen Configuratie

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

#### Instellingen

##### Shields

Brave bevat enkele anti-vingerafdruk maatregelen in zijn [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) functie. Wij raden aan om deze opties [globaal te configureren](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) voor alle pagina's die je bezoekt.

De opties van Shields kunnen naar behoefte per site worden gedowngrade, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- [x] Select **Voorkom dat sites vingerafdrukken van mij nemen op basis van mijn taalvoorkeuren**
- [x] Select **Aggressief** onder Trackers & advertentieblokkering

    ??? warning "Gebruik standaard filter lijsten"
        Brave staat je toe om extra inhoud filters te selecteren binnen de interne `brave://adblock` pagina. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat u zich onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadaardige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

- [x] Selecteer **Upgrade verbindingen naar HTTPS**
- [x] (Optioneel) Selecteer **Block Scripts** (1)
- [x] Selecteer **Streng, kan sites breken** onder **Block fingerprinting

</div>

1. Deze optie biedt functionaliteit die vergelijkbaar is met uBlock Origin's geavanceerde [blokkeringsmodes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) of de [NoScript](https://noscript.net/) extensie.

##### Sociale media blokkeren

- [ ] Zet alle sociale media componenten uit

##### Privacy en beveiliging

<div class="annotate" markdown>

- [x] Selecteer **Deactiveer non-proxied UDP** onder [WebRTC IP-verwerkingsbeleid](https://support.brave.com/hc/nl-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Zet **Google-diensten gebruiken voor pushberichten** uit
- [ ] Zet **Productanalyse met privacybescherming (P3A) toestaan** uit
- [ ] Zet **Dagelijks automatisch gebruiksping verzenden naar Brave** uit
- [ ] Zet **Diagnostische rapporten automatisch verzenden** uit
- [x] Selecteer **Altijd beveiligde verbindingen gebruiken** onder het menu **Beveiliging**
- [ ] Zet **Privéscherm met Tor** uit (1)

    !!! tip "Saneren bij sluiten"

        - [x] Select **Cookies en sitegegevens wissen bij het sluiten van alle vensters** in het menu *Cookies en andere sitegegevens*

        Als je ingelogd wilt blijven bij een bepaalde site die je vaak bezoekt, kun je per site uitzonderingen instellen in het gedeelte *Aangepast gedrag*.

</div>

1. Brave is **niet** zo resistent tegen vingerafdrukken als de Tor Browser en veel minder mensen gebruiken Brave met Tor, dus zal je opvallen. Wanneer [sterke anonimiteit vereist is](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) gebruik dan de [Tor Browser](tor.md#tor-browser).

##### Extensies

Ingebouwde extensies die je niet gebruikt uitschakelen in **Extensies**

- [ ] Schakel **Hangouts**uit
- [ ] Schakel **WebTorrent**uit

##### Web3

De Web3-functies van Brave kunnen de vingerafdruk van jouw browser en het aanvalsoppervlak vergroten. Tenzij je een van de functies gebruikt, moeten ze worden uitgeschakeld.

- Selecteer **Extensies (geen fallback)** onder Standaard Ethereum portemonnee en standaard Solana portemonnee
- Schakel **methode in om IPFS-bronnen op te lossen** uit

##### Systeem

<div class="annotate" markdown>

- [ ] Zet **Achtergrondapps actief houden als Brave is gesloten** uit om achtergrond apps uit te schakelen (1)

</div>

1. Deze optie is niet op alle platforms aanwezig.

#### Synchronisatie

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) maakt jouw surfgegevens (geschiedenis, bladwijzers, enz.) toegankelijk op al jouw apparaten zonder dat je een account nodig hebt en beschermt ze met E2EE.

#### Brave Rewards en Wallet

**Met Brave Rewards** kun je Basic Attention Token (BAT) cryptocurrency ontvangen voor het uitvoeren van bepaalde acties binnen Brave. Het is afhankelijk van een bewaarrekening en KYC van een select aantal providers. Wij raden BAT niet aan als een [private cryptocurrency](cryptocurrency.md), noch raden wij het gebruik van een [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc)aan, dus raden wij het gebruik van deze functie af.

**Brave Wallet** werkt lokaal op jouw computer, maar ondersteunt geen private cryptocurrencies, dus we raden het gebruik van deze functie ook af.

## Aanvullende middelen

In het algemeen raden wij aan jouw browserextensies tot een minimum te beperken; ze hebben bevoorrechte toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) de site-isolatie. Ublock Origin of AdGuard kunnen echter nuttig blijken als je waarde hecht aan de functionaliteit voor het blokkeren van inhoud.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** is een populaire inhoudsblokker die je kan helpen bij het blokkeren van advertenties, trackers en vingerafdrukscripts.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacybeleid" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentatie}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Broncode" }
    
    ??? downloads "Downloaden"
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Wij raden aan om de documentatie van de [ontwikkelaar te volgen](https://github.com/gorhill/uBlock/wiki/Blocking-mode) en een van de "modes" te kiezen. Extra filterlijsten kunnen de prestaties beïnvloeden en [kan het aanvalsoppervlak vergroten](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Dit zijn enkele andere [filterlijsten](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) die je zou kunnen overwegen toe te voegen:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Voeg [Actually Legitimatee URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt) toe

### uBlock Origin Lite

uBlock Origin also has a "Lite" version of their extension, which offers a very limited feature-set compared to the original extension. However, it has a few distinct advantages over its full-fledged sibling, so you may want to consider it if...

- ...you don't want to grant full "read/modify website data" permissions to any extensions (even a trusted one like uBlock Origin)
- ...you want a more resource (memory/CPU) efficient content blocker[^1]
- ...your browser only supports Manifest V3 extensions

!!! recommendation

    ![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }
    
    **uBlock Origin Lite** is a Manifest V3 compatible content blocker. Compared to the original *uBlock Origin*, this extension does not require broad "read/modify data" permissions to function.
    
    [:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

We only recommend this version of uBlock Origin if you never want to make any changes to your filter lists, because it only supports a few pre-selected lists and offers no additional customization options, including the ability to select elements to block manually. These restrictions are due to limitations in Manifest V3's design.

This version offers three levels of blocking: "Basic" works without requiring any special privileges to view and modify site content, while the "Optimal" and "Complete" levels do require that broad permission, but offer a better filtering experience with additional cosmetic rules and scriptlet injections.

If you set the default filtering mode to "Optimal" or "Complete" the extension will request read/modify access to **all** websites you visit. However, you also have the option to change the setting to "Optimal" or "Complete" on a **per-site** basis by adjusting the slider in the extension's pop-up panel on any given site. When you do so, the extension will request read/modify access to that site only. Therefore, if you want to take advantage of uBlock Origin Lite's "permission-less" configuration, you should probably leave the default setting as "Basic" and only adjust it higher on sites where that level is not adequate.

uBlock Origin Lite only receives block list updates whenever the extension is updated from your browser's extension marketplace, as opposed to on demand. This means that you may miss out on new threats being blocked for weeks until a full extension release is published.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

### Minimumvereisten

- Moet open-source software zijn.
- Ondersteunt automatische updates.
- Ontvangt engine updates in 0-1 dagen na upstream release.
- Beschikbaar op Linux, macOS en Windows.
- Wijzigingen die nodig zijn om de browser privacyvriendelijker te maken, mogen de gebruikerservaring niet negatief beïnvloeden.
- Blokkeert standaard cookies van derden.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^2]


### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Beschikt over ingebouwde functionaliteit voor het blokkeren van inhoud.
- Ondersteunt cookie Compartimentalisatie ( à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Ondersteunt Progressive Web Apps.  
  PWA 's stellen je in staat om bepaalde websites te installeren alsof het native apps op jouw computer zijn. Dit kan voordelen hebben ten opzichte van het installeren van op electron gebaseerde apps, omdat je profiteert van de regelmatige beveiligingsupdates van jouw browser.
- Omvat geen add-on functionaliteit (bloatware) die geen invloed heeft op de privacy van gebruikers.
- Verzamelt standaard geen telemetrie.
- Biedt een open-source sync-server implementatie.
- Standaard ingesteld op een [privé zoekmachine](search-engines.md).

### Uitgebreide criteria

- Mag geen ingebouwde browser- of OS-functionaliteit repliceren.
- Moet rechtstreeks van invloed zijn op de privacy van de gebruiker, d.w.z. mag niet gewoon informatie verstrekken.

[^1]: uBlock Origin Lite *itself* will consume no resources, because it uses newer APIs which make the browser process the filter lists natively, instead of running JavaScript code within the extension to handle the filtering. However, this resource advantage is only [theoretical](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), because it's possible that standard uBlock Origin's filtering code is more efficient than your browser's native filtering code. This has not yet been benchmarked.
[^2]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
