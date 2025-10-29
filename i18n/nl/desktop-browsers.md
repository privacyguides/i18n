---
meta_title: "Privacy respecterende webbrowsers voor PC en Mac - Privacy Handleidingen"
title: Desktop Browsers
icon: material/laptop
description: Deze privacybeschermende browsers bevelen we momenteel aan voor standaard/ niet-anoniem internetten op desktopsystemen.
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
    url: https://mullvad.net/nl/browser
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
    sameAs: https://nl.wikipedia.org/wiki/Mozilla_Firefox
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
    sameAs: https://nl.wikipedia.org/wiki/Brave_(webbrowser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Beschermt tegen de volgende bedreiging(en):</small>

- [:material-account-cash: Surveillance kapitalisme](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Dit zijn momenteel onze aanbevolen **desktop webbrowsers** en configuraties voor standaard/ niet-anoniem internetten. Wij bevelen [Mullvad Browser](#mullvad-browser) aan als je gericht bent op sterke privacybescherming en anti-vingerafdrukken, [Firefox](#firefox) voor casual internetters op zoek naar een goed alternatief voor Google Chrome, en [Brave](#brave) als je Chromium-browsercompatibiliteit nodig hebt.

Als je anoniem wil browsen, gebruik in plaats daarvan dan [ Tor](tor.md). We doen een aantal aanbevelingen voor configuratie op deze pagina, maar alle andere browsers dan Tor Browser zullen op de een of andere manier door *iemand* getraceerd kunnen worden.

## Mullvad Browser

<div class="admonition recommendation" markdown>

Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is een versie van [Tor Browser](tor.md#tor-browser) met Tor netwerk integraties verwijderd. Het is bedoeld om VPN-gebruikers te voorzien van Tor Browser's anti-vingerafdruk technologieën, die een belangrijke bescherming zijn tegen [:material-eye-outline: Massa Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Het is ontwikkeld door het Tor Project en gedistribueerd door [Mullvad](vpn.md#mullvad), en vereist **niet** het gebruik van Mullvad's VPN.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacybeleid" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentatie" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Broncode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Net als [ Tor Browser](tor.md) is Mullvad Browser ontworpen om vingerafdrukken te voorkomen door jouw browser vingerafdruk identiek te maken aan andere Mulvad Browser gebruikers, en bevat standaard instellingen en extensies die automatisch worden geconfigureerd aan de standaard beveiligingsniveaus: *Standaard*, *Veilig* en *Veiligst*.

Daarom is het absoluut noodzakelijk dat je de browser niet wijzigt buiten het aanpassen van de standaard [beveiligingsniveaus](https://tb-manual.torproject.org/security-settings). Wanneer je het beveiligingsniveau aanpast, **moet** je de browser altijd opnieuw opstarten voordat je deze verder gebruikt. Anders [worden de beveiligingsinstellingen mogelijk niet volledig toegepast](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), waardoor je een hoger risico loopt op vingerafdrukken en exploitatie dan je zou verwachten op basis van de gekozen instelling.

Andere wijzigingen zouden jouw vingerafdruk uniek maken, wat het doel van het gebruik van deze browser tenietdoet. Als je jouw browser zwaarder wilt configureren en vingerafdrukken voor jou geen probleem is, raden wij in plaats daarvan [Firefox](#firefox) aan.

### Anti-Vingerafdrukken

**Zonder** gebruik te maken van een [VPN](vpn.md), biedt Mullvad Browser dezelfde bescherming tegen [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) als andere private browsers zoals Firefox+[Arkenfox](#arkenfox-advanced) of [Brave](#brave). Mullvad Browser biedt deze bescherming, ten koste van enige mate van flexibiliteit en gemak die andere privé-browsers kunnen bieden.

==Voor de sterkste bescherming tegen vingerafdrukken raden we aan Mullvad Browser te gebruiken in combinatie **met** een VPN==, of dat nu Mullvad is of een andere aanbevolen VPN-provider. Wanneer je een VPN met Mullvad Browser gebruikt, deelt je een vingerafdruk en een pool van IP-adressen met vele andere gebruikers, waardoor je een "menigte" krijgt om in op te gaan. Deze strategie is de enige manier om geavanceerde volgscripts te dwarsbomen, en is dezelfde anti-vingerafdruk techniek die Tor Browser gebruikt.

Denk eraan dat je Mullvad Browser kunt gebruiken met elke VPN-provider, maar dat andere mensen op die VPN ook Mullvad Browser moeten gebruiken om deze "menigte" te laten bestaan, iets wat waarschijnlijker is bij Mullvad VPN in vergelijking met andere providers, vooral zo kort na de lancering van Mullvad Browser. Mullvad Browser heeft geen ingebouwde VPN-verbinding en controleert niet of je een VPN gebruikt voordat je gaat browsen; jouw VPN-verbinding moet apart worden geconfigureerd en beheerd.

Mullvad Browser wordt geleverd met de *uBlock Origin* en *NoScript* browserextensies vooraf geïnstalleerd. Hoewel we het toevoegen van *extra* [browserextensies](browser-extensions.md) meestal afraden, mogen deze extensies die vooraf zijn geïnstalleerd met de browser **niet** worden verwijderd of geconfigureerd buiten hun standaardwaarden, omdat dit je browser fingerprint duidelijk zal onderscheiden van andere gebruikers van Mullvad Browser. Het wordt ook vooraf geïnstalleerd met de Mullvad-browserextensie, die *kan* veilig worden verwijderd zonder jouw browser vingerafdruk te beïnvloeden als je dat wilt, maar is ook veilig om te bewaren, zelfs als je geen Mullvad VPN gebruikt.

### Private Browsing Mode

Mullvad Browser werkt in een permanente privé browsing modus, wat betekent dat jouw geschiedenis, cookies en andere site gegevens altijd worden gewist elke keer dat de browser wordt gesloten. Jouw bladwijzers, browserinstellingen en extensie-instellingen blijven bewaard.

Dit is nodig om geavanceerde vormen van tracking te voorkomen, maar gaat wel ten koste van het gemak en sommige Firefox-functies, zoals Multi-Account Containers. Vergeet niet dat je altijd meerdere browsers kunt gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die anders niet goed werken in Mullvad Browser, en Mullvad Browser voor algemeen browsen.

### Mullvad Leta

Mullvad Browser heeft [**Mullvad Leta**](search-engines.md#mullvad-leta) als de standaard zoekmachine, die fungeert als een proxy voor zoekresultaten van Google of Brave (instelbaar op de startpagina van Mullvad Leta).

Als je een Mullvad VPN-gebruiker bent, is het gebruik van diensten zoals Mullvad Leta, die door je VPN-provider zelf worden aangeboden, niet zonder risico. Dit komt omdat Mullvad theoretisch toegang heeft tot je echte IP-adres (via hun VPN) en je zoekactiviteit (via Leta); dit laatste is informatie die een VPN normaal gesproken wil scheiden. Hoewel Mullvad zeer weinig informatie verzamelt over hun VPN-abonnees of Leta-gebruikers, zou je een andere [zoekmachine](search-engines.md) moeten overwegen als dit risico je zorgen baart.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** biedt krachtige privacy-instellingen zoals [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), die kunnen helpen bij het blokkeren van verschillende [soorten tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacybeleid" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentatie" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Broncode" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Bijdragen" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Waarschuwing</p>

Firefox voegt een uniek [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) toe aan downloads vanaf Mozilla's website en gebruikt telemetrie in Firefox om het token te verzenden. Het token is **niet** opgenomen in releases van de [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Aanbevolen Firefox Configuratie

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

#### Zoeken

- [Deselecteer **Zoeksuggesties weergeven**

Functies voor zoeksuggesties zijn mogelijk niet beschikbaar in jouw regio.

Zoeksuggesties sturen alles wat je in de adresbalk typt naar de standaard zoekmachine, ongeacht of je een echte zoekopdracht opgeeft. Door zoeksuggesties uit te schakelen, kan je nauwkeuriger bepalen welke gegevens je naar jouw zoekmachineprovider stuurt.

##### Firefox Suggesties (alleen VS)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is een functie die lijkt op zoeksuggesties, maar is alleen beschikbaar in de VS. We raden aan deze functie uit te schakelen om dezelfde reden waarom we aanraden zoeksuggesties uit te schakelen. Als je deze opties niet ziet onder de **adresbalk**, heb je de nieuwe ervaring niet en kun je deze wijzigingen negeren.

- [ ] Deselecteer **Suggesties van Firefox**
- [ ] Deselecteer **Suggesties van sponsors**

#### Privacy & beveiliging

##### Verbeterde Traceringsbescherming

- [x] Selecteer **Strikte** Verbeterde Traceringsbescherming

Dit beschermt je door het blokkeren van social media trackers, fingerprinting scripts (merk op dat dit je niet tegen *alle* fingerprinting beschermt), cryptominers, cross-site tracking cookies en sommige andere tracking content. ETP beschermt tegen veel voorkomende bedreigingen, maar blokkeert niet alle trackingkanalen omdat het zo is ontworpen dat het minimale tot geen invloed heeft op de bruikbaarheid van de site.

##### Saneren bij sluiten

Als je aangemeld wilt blijven bij bepaalde sites, kun je uitzonderingen toestaan in **Cookies en sitegegevens** → **Uitzonderingen beheren...**

- [x] Check **Cookies en sitegegevens verwijderen wanneer Firefox wordt afgesloten**

Dit beschermt je tegen permanente cookies, maar beschermt je niet tegen cookies die tijdens een willekeurige browsersessie worden aangemaakt. Wanneer dit is ingeschakeld, wordt het mogelijk om eenvoudig jouw browsercookies op te schonen door Firefox simpelweg opnieuw te starten. Je kunt uitzonderingen per site instellen als je ingelogd wilt blijven op een bepaalde site die je vaak bezoekt.

##### Telemetrie

- [ ] Deselecteer **Firefox toestaan technische en interactiegegevens naar Mozilla**te sturen
- [ ] Deselecteer **Firefox toestaan om studies te installeren en uit te voeren**
- [ ] Deselecteer **Firefox toestaan achterstallige crashmeldingen namens jou te verzenden**

Volgens Mozilla's privacybeleid voor Firefox,

> Firefox stuurt ons gegevens over jouw Firefox-versie en -taal; besturingssysteem van het apparaat en hardwareconfiguratie; geheugen, basisinformatie over crashes en fouten; resultaat van geautomatiseerde processen zoals updates, veilig browsen en activering. Wanneer Firefox gegevens naar ons verzendt, wordt uw IP-adres tijdelijk verzameld als onderdeel van onze serverlogs.

Daarnaast verzamelt de Mozilla Accounts service [enkele technische gegevens](https://mozilla.org/privacy/mozilla-accounts). Als je een Mozilla-account gebruikt, kan je je afmelden:

1. Open jouw [profielinstellingen op accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Schakel **Gegevensverzameling en -gebruik uit** > **Help Firefox-accounts verbeteren**

##### Website Advertentievoorkeuren

- [ ] Deselecteer **Websites toestaan om privacy-beschermende advertentiemeting uit te voeren**

Met de release van Firefox 128 is een nieuwe instelling voor [privacy-beschermende attributie](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) toegevoegd en [standaard ingeschakeld](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). Met PPA kunnen adverteerders je webbrowser gebruiken om de effectiviteit van webcampagnes te meten, in plaats van traditionele tracking op basis van JavaScript te gebruiken. Wij zijn van mening dat dit gedrag buiten de verantwoordelijkheden van een user agent valt, en het feit dat het standaard is uitgeschakeld in Arkenfox is een extra indicator voor het uitschakelen van deze functie.

##### HTTPS-Only Modus

- [x] Selecteer **HTTPS-only modus in alle vensters inschakelen**

Dit voorkomt dat je onbedoeld verbinding maakt met een website in platte HTTP-tekst. Sites zonder HTTPS zijn tegenwoordig zeldzaam, dus dit zou weinig tot geen invloed moeten hebben op je dagelijkse browsen.

##### DNS over HTTPS

Als je een [DNS over HTTPS provider](dns.md) gebruikt:

- [x] Selecteer **Maximale Bescherming** en kies een geschikte provider

Max Protection dwingt het gebruik van DNS over HTTPS af, en er wordt een beveiligingswaarschuwing weergegeven als Firefox geen verbinding kan maken met jouw beveiligde DNS resolver, of als jouw beveiligde DNS resolver zegt dat er geen records bestaan voor het domein dat u probeert te openen. Dit voorkomt dat het netwerk waarmee je verbonden bent in het geheim je DNS-beveiliging verlaagt.

#### Synchronisatie

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) maakt je surfgegevens (geschiedenis, bladwijzers, enz.) toegankelijk op al je apparaten en beschermt ze met E2EE.

### Arkenfox (gevorderd)

<div class="admonition tip" markdown>
<p class="admonition-title">Gebruik Mullvad Browser voor geavanceerde anti-vingerafdrukken</p>

[Mullvad Browser](#mullvad-browser) biedt dezelfde anti-fingeprint bescherming als Arkenfox, en vereist niet het gebruik van Mullvad's VPN om van deze bescherming te profiteren. In combinatie met een VPN kan Mullvad Browser meer geavanceerde tracking scripts dwarsbomen dan Arkenfox. Arkenfox heeft nog steeds het voordeel dat het veel flexibeler is en uitzonderingen per site toestaat voor websites waarop je ingelogd moet blijven.

</div>

Het [Arkenfox-project](https://github.com/arkenfox/user.js) biedt een reeks weloverwogen opties voor Firefox. Als je [besluit](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) om Arkenfox te gebruiken, zijn een [paar opties](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) subjectief streng en/ of kunnen ervoor zorgen dat sommige websites niet goed werken - deze kun je [eenvoudig wijzigen](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) om aan jouw behoeften te voldoen. We raden **je sterk aan** om hun volledige [wiki](https://github.com/arkenfox/user.js/wiki) te lezen. Arkenfox biedt ook [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) ondersteuning.

Arkenfox is er alleen op gericht om eenvoudige of naïeve volgscripts te dwarsbomen via canvas randomisatie en de ingebouwde configuratie-instellingen voor vingerafdrukbestendigheid van Firefox. Het is niet erop gericht om jouw browser te laten opgaan in een grote menigte van andere Arkenfox-gebruikers zoals Mullvad Browser of Tor Browser dat doen, wat de enige manier is om geavanceerde scripts voor het traceren van vingerafdrukken te dwarsbomen. Vergeet niet dat je altijd meerdere browsers kunt gebruiken, bijvoorbeeld door Firefox+Arkenfox te gebruiken voor een paar sites waarop je ingelogd wilt blijven of die je anderszins vertrouwt, en Mullvad Browser voor algemeen browsen.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** bevat een ingebouwde adblocker en [privacyfuncties](https://brave.com/privacy-features), waarvan vele standaard zijn ingeschakeld.

Brave is gebouwd op het Chromium webbrowser project, dus het zou vertrouwd moeten aanvoelen en minimale website compatibiliteitsproblemen moeten hebben.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacybeleid" }.
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Broncode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Let op</p>

Brave voegt een "[verwijzingscode](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" toe aan de bestandsnaam in downloads van de Brave website. Deze code wordt gebruikt om bij te houden van welke bron de browser is gedownload, bijvoorbeeld `BRV002` in een download met de naam `Brave-Browser-BRV002.pkg`. Het installatieprogramma zal aan het eind van het installatieproces de server van Brave pingen met de verwijzingscode. Als je je hier zorgen over maakt, kun je de naam van het installatiebestand wijzigen voordat je het opent.

</div>

### Aanbevolen Brave Configuratie

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

#### Shields

Brave heeft een aantal maatregelen tegen vingerafdrukken opgenomen in de functie [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). We raden je aan deze opties [globaal](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) te configureren voor alle pagina's die je bezoekt.

De opties van Shields kunnen naar behoefte per site worden aangepast, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- x] Selecteer **Agressief** onder *Trackers en advertenties blokkeren*

<details class="warning" markdown>
<summary>Gebruik standaard filterlijsten</summary>

Met Brave kun je extra inhoudsfilters selecteren binnen de interne `brave://adblock` pagina. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat je je onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadwillige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

</details>

- x] Selecteer **Strict** onder *Verbeter verbindingen naar HTTPS*
- [x] (Optioneel) Selecteer **Blokkeer scripts** (1)
- [x] Vink **Blokkeer vingerafdrukken** aan
- [x] Selecteer **Blokkeer cookies van derden**
- [x] Vink **Vergeet mij als ik deze site afsluit** aan (2)
- [ ] Schakel alle onderdelen van sociale media uit.

</div>

1. Deze optie schakelt JavaScript uit, waardoor veel sites niet meer werken. Om dit te verhelpen, kun je uitzonderingen per site instellen door op het schildpictogram in de adresbalk te klikken en deze instelling uit te vinken onder *Geavanceerde besturingselementen*.
2. Als je aangemeld wilt blijven bij een bepaalde site die je vaak bezoekt, kun je uitzonderingen per site instellen door op het schildpictogram in de adresbalk te klikken en deze instelling uit te vinken onder *Geavanceerde besturingselementen*.

#### Privacy en beveiliging

<div class="annotate" markdown>

- x] Selecteer **Sites niet toestaan JavaScript-optimalisatie te gebruiken** onder *Security* → *Manage JavaScript optimization & security* (1)
- [x] Selecteer **Automatisch rechten verwijderen van ongebruikte sites** onder *Sites and Shields Settings*
- [x] Selecteer **Disable non-proxied UDP** onder [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Deselecteer **Google-services gebruiken voor pushberichten**
- [x] Selecteer **Auto-omleiden AMP-pagina's**
- [x] Selecteer **Auto-omleiden tracking URL's**
- [x] Selecteer **Voorkom dat sites mij vingerafdrukken geven op basis van mijn taalvoorkeuren**

</div>

1. Het uitschakelen van de V8 optimizer verkleint je aanvalsoppervlak door [*sommige*](https://grapheneos.social/@GrapheneOS/112708049232710156) delen van de JavaScript Just-In-Time (JIT) compilatie uit te schakelen.

##### Tor windows

[**Privé window met Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) waar je je verkeer via het Tor-netwerk in privé windows kunt routeren en toegang kunt krijgen tot .onion-services, wat in sommige gevallen handig kan zijn. Brave is echter **niet** zo goed bestand tegen vingerafdrukken als de Tor Browser, en veel minder mensen gebruiken Brave met Tor, dus je zult opvallen. Als je threat model sterke anonimiteit vereist, gebruik dan de [Tor Browser](tor.md#tor-browser).

##### Dataverzameling

- [ ] Deselecteer **Privacybeschermende productanalyse (P3A) toestaan**
- [ ] Deselecteer **Automatisch dagelijkse gebruiksping naar Brave verzenden**
- [ ] Deselecteer **Automatisch diagnostische rapporten verzenden**

#### Web3

De Web3-functies van Brave kunnen mogelijk de vingerafdruk van jouw browser en het aanvalsoppervlak vergroten. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensies

- [ ] Deselecteer alle ingebouwde extensies die je niet gebruikt

#### Zoekmachine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [Deselecteer **Zoeksuggesties weergeven**

#### Systeem

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. Deze optie is niet op alle platforms aanwezig.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards en Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimumvereisten

- Moet open-source software zijn.
- Moet automatische updates ondersteunen.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
