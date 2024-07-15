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

Dit zijn momenteel onze aanbevolen mobiele webbrowsers en configuraties. Wij bevelen [Mullvad Browser](#mullvad-browser) aan als je je richt op sterke privacybescherming en anti-vingerafdrukken uit de doos, [Firefox](#firefox) voor casual internetbrowsers op zoek naar een goed alternatief voor Google Chrome, en [Brave](#brave) als je Chromium-browsercompatibiliteit nodig hebt.

In het algemeen raden we aan om extensies tot een minimum te beperken: ze hebben geprivilegieerde toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-Uchnm34/m/lDaXwQhzBAAJ) site-isolatie. We doen op deze pagina enkele aanbevelingen voor de configuratie, maar alle andere browsers dan Tor Browser zullen op een of andere manier traceerbaar zijn via *iemand*.

## Mullvad Browser

<div class="admonition recommendation" markdown>

Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is een versie van [Tor Browser](tor.md#tor-browser) met zonder Tor netwerk integraties, gericht op het aanbieden van Tor Browser's anti-vingerafdruk browser technologieën aan VPN gebruikers. Het is ontwikkeld door het Tor Project en gedistribueerd door [Mullvad](vpn.md#mullvad), en vereist **niet** het gebruik van Mullvad's VPN.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary } [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" } [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation} [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Net als [Tor Browser](tor.md), is Mullvad Browser ontworpen om fingerprinting te voorkomen door jouw browser fingerprint identiek te maken aan alle andere Mullvad Browser gebruikers, en het bevat standaard instellingen en extensies die automatisch worden geconfigureerd door de standaard beveiligingsniveaus: *Standaard*, *Veiliger* en *Veiligst*. Daarom is het noodzakelijk dat u de browser helemaal niet aanpast buiten het aanpassen van de standaard [beveiligingsniveaus](https://tb-manual.torproject.org/security-settings). Andere wijzigingen zouden jouw vingerafdruk uniek maken, wat het doel van het gebruik van deze browser tenietdoet. Als je jouw browser zwaarder wilt configureren en fingerprinting voor jou geen probleem is, raden wij in plaats daarvan [Firefox](#firefox) aan.

### Anti-Fingerprinting

**Zonder** gebruik te maken van een [VPN](vpn.md), biedt Mullvad Browser dezelfde bescherming tegen [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) als andere private browsers zoals Firefox+[Arkenfox](#arkenfox-advanced) of [Brave](#brave). Mullvad Browser biedt deze bescherming out of the box, ten koste van enige flexibiliteit en gemak die andere privé-browsers kunnen bieden.

==Voor de sterkste bescherming tegen fingerprinting raden we aan Mullvad Browser te gebruiken in combinatie **met** een VPN==, of dat nu Mullvad is of een andere aanbevolen VPN-provider. Wanneer je een VPN met Mullvad Browser gebruikt, deelt je een vingerafdruk en een pool van IP-adressen met vele andere gebruikers, waardoor je een "menigte" krijgt om in op te gaan. Deze strategie is de enige manier om geavanceerde volgscripts te dwarsbomen, en is dezelfde anti-fingerprinting techniek die Tor Browser gebruikt.

Denk eraan dat je Mullvad Browser kunt gebruiken met elke VPN-provider, maar dat andere mensen op die VPN ook Mullvad Browser moeten gebruiken om deze "menigte" te laten bestaan, iets wat waarschijnlijker is bij Mullvad VPN in vergelijking met andere providers, vooral zo kort na de lancering van Mullvad Browser. Mullvad Browser heeft geen ingebouwde VPN-connectiviteit, noch controleert het of je een VPN gebruikt voordat je gaat browsen; jouw VPN-verbinding moet apart worden geconfigureerd en beheerd.

Mullvad Browser wordt geleverd met de *uBlock Origin* en *NoScript* browserextensies vooraf geïnstalleerd. Hoewel we het toevoegen van *extra* [browserextensies](browser-extensions.md) meestal afraden, mogen deze extensies die vooraf zijn geïnstalleerd met de browser **niet** worden verwijderd of geconfigureerd buiten hun standaardwaarden, omdat dit uw browser fingerprint duidelijk zou onderscheiden van andere gebruikers van Mullvad Browser. Het wordt ook vooraf geïnstalleerd met de Mullvad-browserextensie, die *kan* veilig worden verwijderd zonder jouw browservingerafdruk te beïnvloeden als je dat wilt, maar is ook veilig om te bewaren, zelfs als je geen Mullvad VPN gebruikt.

### Private Browsing Mode

Mullvad Browser werkt in een permanente privé browsing modus, wat betekent dat jouw geschiedenis, cookies en andere site gegevens altijd worden gewist elke keer dat de browser wordt gesloten. Jouw bladwijzers, browserinstellingen en extensie-instellingen blijven bewaard.

Dit is nodig om geavanceerde vormen van tracking te voorkomen, maar gaat wel ten koste van het gemak en sommige Firefox-functies, zoals Multi-Account Containers. Vergeet niet dat je altijd meerdere browsers kunt gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die anders niet goed werken in Mullvad Browser, en Mullvad Browser voor algemeen browsen.

### Mullvad Leta

Mullvad Browser wordt geleverd met DuckDuckGo ingesteld als de standaard [zoekmachine](search-engines.md), maar het komt ook voorgeïnstalleerd met **Mullvad Leta**, een zoekmachine die een actief Mullvad VPN-abonnement vereist om toegang te krijgen. Mullvad Leta raadpleegt de betaalde zoek API van Google direct en is daarom beperkt tot het betalen van abonnees. Door deze beperking is het echter mogelijk voor Mullvad om zoekopdrachten en Mullvad VPN-accounts te correleren. Daarom raden wij het gebruik van Mullvad Leta af, ook al verzamelt Mullvad zeer weinig informatie over hun VPN-abonnees.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** biedt krachtige privacy-instellingen zoals [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), die kunnen helpen bij het blokkeren van verschillende [soorten tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary } [:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" } [:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation} [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" } [:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

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

Firefox voegt een uniek [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) toe aan downloads vanaf Mozilla's website en gebruikt telemetrie in Firefox om het token te verzenden. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

#### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2/). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

#### Zoeken

- [ ] Uncheck **Show search suggestions**

Functies voor zoeksuggesties zijn mogelijk niet beschikbaar in jouw regio.

Zoeksuggesties sturen alles wat je in de adresbalk typt naar de standaardzoekmachine, ongeacht of je een echte zoekopdracht geeft. Door zoeksuggesties uit te schakelen, kun je nauwkeuriger bepalen welke gegevens je naar jouw zoekmachineprovider stuurt.

##### Firefox stelt voor (alleen VS)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Wij raden aan dit uit te schakelen om dezelfde reden als waarom wij aanraden zoeksuggesties uit te schakelen. Als je deze opties niet ziet onder de kop **Adresbalk**, hebt je de nieuwe ervaring niet en kun je deze wijzigingen negeren.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Deselecteer **Suggesties van sponsors**

#### Privacy & beveiliging

##### Verbeterde traceringsbescherming

- [x] Select **Strict** Verbeterde traceringsbescherming

Dit beschermt je door het blokkeren van social media trackers, fingerprinting scripts (merk op dat dit je niet beschermt tegen *alle* fingerprinting), cryptominers, cross-site tracking cookies, en sommige andere tracking content. ETP beschermt tegen veel voorkomende bedreigingen, maar blokkeert niet alle tracking-wegen omdat het is ontworpen om de bruikbaarheid van de site zo min mogelijk of helemaal niet te beïnvloeden.

##### Saneren bij sluiten

Als je op bepaalde sites aangemeld wilt blijven, kunt je uitzonderingen toestaan in **Cookies en Sitegegevens** → **Uitzonderingen beheren...**

- [x] Check **Cookies en sitegegevens verwijderen wanneer Firefox wordt afgesloten**

Dit beschermt je tegen blijvende cookies, maar niet tegen cookies die tijdens een bepaalde surfsessie worden aangemaakt. Wanneer dit is ingeschakeld, wordt het mogelijk om jouw browsercookies gemakkelijk te wissen door Firefox gewoon opnieuw op te starten. Je kunt per site uitzonderingen instellen, als je ingelogd wilt blijven op een bepaalde site die je vaak bezoekt.

##### Telemetrie

- [ ] Uncheck **Firefox toestaan technische en interactiegegevens naar Mozilla**te sturen
- [ ] Uncheck **Firefox toestaan om studies te installeren en uit te voeren**uit
- [ ] Uncheck **Firefox toestaan om namens je achterstallige crashmeldingen te verzenden uit**

> Firefox stuurt ons gegevens over jouw Firefox-versie en -taal; besturingssysteem van het apparaat en hardwareconfiguratie; geheugen, basisinformatie over crashes en fouten; resultaat van geautomatiseerde processen zoals updates, veilig browsen en activering. Wanneer Firefox gegevens naar ons verzendt, wordt uw IP-adres tijdelijk verzameld als onderdeel van onze serverlogs.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

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

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (gevorderd)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) biedt dezelfde anti-fingeprint bescherming als Arkenfox out of the box, en vereist niet het gebruik van Mullvad's VPN om van deze bescherming te profiteren. In combinatie met een VPN kan Mullvad Browser meer geavanceerde tracking scripts dwarsbomen dan Arkenfox. Arkenfox heeft nog steeds het voordeel dat het veel flexibeler is, en uitzonderingen per site toestaat voor websites waarop je ingelogd moet blijven.

</div>

Het [Arkenfox-project](https://github.com/arkenfox/user.js) biedt een reeks zorgvuldig overwogen opties voor Firefox. Als je [besluit](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) om Arkenfox te gebruiken, zijn er een [paar opties](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) die subjectief streng zijn en/of ervoor kunnen zorgen dat sommige websites niet goed werken - [die je gemakkelijk kunt wijzigen](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) om aan jouw behoeften te voldoen. Wij **raden je ten zeerste aan** hun volledige [wiki](https://github.com/arkenfox/user.js/wiki)door te lezen. Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox wil alleen elementaire of naïeve volgscripts dwarsbomen via canvas randomisatie en de ingebouwde configuratie-instellingen voor vingerafdrukbestendigheid van Firefox. Het is niet de bedoeling dat jouw browser opgaat in een grote menigte van andere Arkenfox-gebruikers op dezelfde manier als Mullvad Browser of Tor Browser dat doen, wat de enige manier is om geavanceerde tracking-scripts voor vingerafdrukken te dwarsbomen. Je kunt altijd meerdere browsers gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die je anderszins vertrouwt, en Mullvad Browser voor algemeen browsen.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is gebouwd op het Chromium webbrowser project, dus het zou vertrouwd moeten aanvoelen en minimale website compatibiliteitsproblemen moeten hebben.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS-gebruikers:** De download van Brave Browser van hun officiële website is een `.pkg` installatieprogramma dat beheerdersrechten vereist om uit te voeren (en het kan andere onnodige scripts uitvoeren op uw machine). Als een alternatief kunt u de laatste `Brave-Browser-universal.dmg` file downloaden van hun [GitHub releases](https://github.com/brave/brave-browser/releases/latest) pagina, die een traditionele "Sleep naar Applicaties map" installatie biedt.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave voegt een "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" toe aan de file naam in downloads van de Brave website, die wordt gebruikt om te volgen van welke bron de browser heeft gedownload. Als voorbeeld `BRV002` in een download genaamd `Brave-Browser-BRV002.pkg`. Het installatieprogramma zal aan het eind van het installatieproces de server van Brave pingen met de verwijzingscode. Als u zich hier zorgen om maakt kunt u de naam van de installer veranderen voor het openen.

</div>

### Recommended Brave Configuration

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

#### Instellingen

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

De opties van Shields kunnen naar behoefte per site worden gedowngrade, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat u zich onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadaardige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under *Block fingerprinting*
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### Privacy en beveiliging

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave is **niet** zo resistent tegen vingerafdrukken als de Tor Browser en veel minder mensen gebruiken Brave met Tor, dus zal je opvallen. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Extensies

- [ ] Uncheck all built-in extensions you do not use

##### Web3

De Web3-functies van Brave kunnen de vingerafdruk van jouw browser en het aanvalsoppervlak vergroten. Tenzij je een van de functies gebruikt, moeten ze worden uitgeschakeld.

- Select **Extensions (no fallback)** under *Default Ethereum wallet* and *Default Solana wallet*
- Set *Method to resolve IPFS resources* to **Disabled**

##### Systeem

<div class="annotate" markdown>

- [ ] Zet **Achtergrondapps actief houden als Brave is gesloten** uit om achtergrond apps uit te schakelen (1)

</div>

1. Deze optie is niet op alle platforms aanwezig.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards en Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. Het is afhankelijk van een bewaarrekening en KYC van een select aantal providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** werkt lokaal op jouw computer, maar ondersteunt geen private cryptocurrencies, dus we raden het gebruik van deze functie ook af.

## Aanvullende middelen

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
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
