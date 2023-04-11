---
title: "Desktop Browsers"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
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

Dit zijn momenteel onze aanbevolen mobiele webbrowsers en configuraties. We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

In het algemeen raden we aan om extensies tot een minimum te beperken: ze hebben geprivilegieerde toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-Uchnm34/m/lDaXwQhzBAAJ) site-isolatie. We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

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

Deze opties zijn te vinden in :material-menu: → **Instellingen** → **Privacy & Beveiliging**.

##### Verbeterde traceringsbescherming

- [x] Select **Strict** Verbeterde traceringsbescherming

Dit beschermt je door het blokkeren van social media trackers, fingerprinting scripts (merk op dat dit je niet beschermt tegen *alle* fingerprinting), cryptominers, cross-site tracking cookies, en sommige andere tracking content. ETP beschermt tegen veel voorkomende bedreigingen, maar blokkeert niet alle tracking-wegen omdat het is ontworpen om de bruikbaarheid van de site zo min mogelijk of helemaal niet te beïnvloeden.

##### Saneren bij sluiten

Als je op bepaalde sites aangemeld wilt blijven, kunt je uitzonderingen toestaan in **Cookies en Sitegegevens** → **Uitzonderingen beheren...**

- [x] Check **Cookies en sitegegevens verwijderen wanneer Firefox wordt afgesloten**

Dit beschermt je tegen blijvende cookies, maar niet tegen cookies die tijdens een bepaalde surfsessie worden aangemaakt. Wanneer dit is ingeschakeld, wordt het mogelijk om jouw browsercookies gemakkelijk te wissen door Firefox gewoon opnieuw op te starten. Je kunt per site uitzonderingen instellen, als je ingelogd wilt blijven op een bepaalde site die je vaak bezoekt.

##### Zoeksuggesties

- [ ] Uncheck **Geef zoeksuggesties**

Functies voor zoeksuggesties zijn mogelijk niet beschikbaar in jouw regio.

Zoeksuggesties sturen alles wat je in de adresbalk typt naar de standaardzoekmachine, ongeacht of je een echte zoekopdracht geeft. Door zoeksuggesties uit te schakelen, kun je nauwkeuriger bepalen welke gegevens je naar jouw zoekmachineprovider stuurt.

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

### Firefox Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) maakt jouw browsegegevens (geschiedenis, bladwijzers, enz.) toegankelijk op al jouw apparaten en beschermt ze met E2EE.

### Arkenfox (gevorderd)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

Het [Arkenfox-project](https://github.com/arkenfox/user.js) biedt een reeks zorgvuldig overwogen opties voor Firefox. Als je [besluit](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) om Arkenfox te gebruiken, zijn er een [paar opties](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) die subjectief streng zijn en/of ervoor kunnen zorgen dat sommige websites niet goed werken - [die je gemakkelijk kunt wijzigen](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) om aan jouw behoeften te voldoen. Wij **raden je ten zeerste aan** hun volledige [wiki](https://github.com/arkenfox/user.js/wiki)door te lezen. Arkenfox biedt ook ondersteuning voor [container](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

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

### Aanbevolen configuratie

Deze opties zijn te vinden in :material-menu: → **Instellingen**.

##### Schilden

Brave bevat enkele anti-vingerafdruk maatregelen in zijn [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) functie. Wij raden aan om deze opties [globaal te configureren](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) voor alle pagina's die je bezoekt.

De opties van Shields kunnen naar behoefte per site worden gedowngrade, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- [x] Select **Voorkom dat sites vingerafdrukken van mij nemen op basis van mijn taalvoorkeuren**
- [x] Select **Aggressief** onder Trackers & advertentieblokkering

    ??? warning "Gebruik standaard filter lijsten"
        Brave staat je toe om extra inhoud filters te selecteren binnen de interne `brave://adblock` pagina. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat u zich onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadaardige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

- [x] (Optional) Selecteer **Block Scripts** (1)
- [x] Select **Strict, may break sites** onder Block fingerprinting

</div>

1. Deze optie biedt functionaliteit die vergelijkbaar is met uBlock Origin's geavanceerde [blokkeringsmodes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) of de [NoScript](https://noscript.net/) extensie.

##### Sociale media blokkeren

- [ ] Uncheck alle sociale media componenten uit

##### Privacy en veiligheid

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** onder [WebRTC IP Handling Policy](https://support.brave.com/hc/nl-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Google services gebruiken voor push messaging**
- [ ] Uncheck **Privacy-preserving product analytics (P3A) toestaan**
- [ ] Uncheck **Automatisch dagelijks gebruik ping sturen naar Brave**.
- [ ] Uncheck **Stuur automatisch een dagelijkse gebruiksping naar Brave**
- [ ] Uncheck **Stuur automatisch diagnostische rapporten**
- [x] Select **Gebruik altijd beveiligde verbindingen** in het menu **Veiligheid**
- [ ] Uncheck **Privé venster met Tor** (1)

    !!! tip "Saneren bij sluiten"
        - [x] Select **Cookies en sitegegevens wissen bij het sluiten van alle vensters** in het menu *Cookies en andere sitegegevens*

        Als u ingelogd wilt blijven bij een bepaalde site die je vaak bezoekt, kunt u per site uitzonderingen instellen in het gedeelte *Aangepast gedrag*.

</div>

1. Brave is **niet** zo resistent tegen vingerafdrukken als de Tor Browser en veel minder mensen gebruiken Brave met Tor, dus zal je opvallen. Wanneer [sterke anonimiteit vereist is](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) gebruik dan de [Tor Browser](tor.md#tor-browser).

##### Extensies

Ingebouwde extensies die je niet gebruikt uitschakelen in **Extensies**

- [ ] Uncheck **Hangouts**uit
- [ ] Uncheck **WebTorrent**uit

##### Web3

<div class="annotate" markdown>

- [x] Select Uitgeschakeld op Methode om IPFS-bronnen op te lossen)

</div>

1. InterPlanetary File System (IPFS) is een gedecentraliseerd, peer-to-peer netwerk voor het opslaan en delen van gegevens in een gedistribueerd bestandssysteem. Tenzij je de functie gebruikt, schakel hem uit.

##### Extra instellingen

In het menu *Systeem*

<div class="annotate" markdown>

- [ ] Uncheck **Doorgaan met draaiende apps als Brave gesloten is** uit om achtergrond apps uit te schakelen (1)

</div>

1. Deze optie is niet op alle platforms aanwezig.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) maakt jouw surfgegevens (geschiedenis, bladwijzers, enz.) toegankelijk op al jouw apparaten zonder dat je een account nodig hebt en beschermt ze met E2EE.

## Extra bronnen

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. Ublock Origin of AdGuard kunnen echter nuttig blijken als je waarde hecht aan de functionaliteit voor het blokkeren van inhoud.

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

##### Andere lijsten

Dit zijn enkele andere [filterlijsten](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) die je zou kunnen overwegen toe te voegen:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Voeg [Actually Legitimatee URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt) toe

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

!!! example "Deze sectie is nieuw"

    We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

### Minimale vereisten

- Moet open-source software zijn.
- Ondersteunt automatische updates.
- Ontvangt engine updates in 0-1 dagen na upstream release.
- Beschikbaar op Linux, macOS en Windows.
- Wijzigingen die nodig zijn om de browser privacyvriendelijker te maken, mogen de gebruikerservaring niet negatief beïnvloeden.
- Blokkeert standaard cookies van derden.
- Ondersteunt [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) om cross-site tracking tegen te gaan.[^1]

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Beschikt over ingebouwde functionaliteit voor het blokkeren van inhoud.
- Ondersteunt cookie Compartimentalisatie ( à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Ondersteunt Progressive Web Apps.  
  PWA 's stellen je in staat om bepaalde websites te installeren alsof het native apps op jouw computer zijn. Dit kan voordelen hebben ten opzichte van het installeren van op electron gebaseerde apps, omdat je profiteert van de regelmatige beveiligingsupdates van jouw browser.
- Omvat geen add-on functionaliteit (bloatware) die geen invloed heeft op de privacy van gebruikers.
- Verzamelt standaard geen telemetrie.
- Biedt een open-source sync-server implementatie.
- Standaard ingesteld op een [privézoekmachine](search-engines.md).

### Uitbreidings criteria

- Mag geen ingebouwde browser- of OS-functionaliteit repliceren.
- Moet rechtstreeks van invloed zijn op de privacy van de gebruiker, d.w.z. mag niet gewoon informatie verstrekken.

[^1]: De implementatie van Brave wordt gedetailleerd beschreven op [Brave Privacy Updates: Partitionering van netwerkstatus voor privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
