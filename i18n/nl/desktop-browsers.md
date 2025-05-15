---
meta_title: "Privacy respecterende webbrowsers voor PC en Mac - Privacy Handleidingen"
title: "Desktop Browsers"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance kapitalisme](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. Wij bevelen [Mullvad Browser](#mullvad-browser) aan als je je richt op sterke privacybescherming en anti-vingerafdrukken uit de doos, [Firefox](#firefox) voor casual internetbrowsers op zoek naar een goed alternatief voor Google Chrome, en [Brave](#brave) als je Chromium-browsercompatibiliteit nodig hebt.

In het algemeen raden we aan om extensies tot een minimum te beperken: ze hebben geprivilegieerde toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-Uchnm34/m/lDaXwQhzBAAJ) site-isolatie. We doen op deze pagina enkele aanbevelingen voor de configuratie, maar alle andere browsers dan Tor Browser zullen op een of andere manier traceerbaar zijn via *iemand*.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Het is ontwikkeld door het Tor Project en gedistribueerd door [Mullvad](vpn.md#mullvad), en vereist **niet** het gebruik van Mullvad's VPN.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). When adjusting the security level, you **must** always restart the browser before continuing to use it. Otherwise, [the security settings may not be fully applied](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), putting you at a higher risk of fingerprinting and exploits than you may expect based on the setting chosen.

Modifications other than adjusting this setting would make your fingerprint unique, defeating the purpose of using this browser. Als je jouw browser zwaarder wilt configureren en fingerprinting voor jou geen probleem is, raden wij in plaats daarvan [Firefox](#firefox) aan.

### Anti-Fingerprinting

**Zonder** gebruik te maken van een [VPN](vpn.md), biedt Mullvad Browser dezelfde bescherming tegen [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) als andere private browsers zoals Firefox+[Arkenfox](#arkenfox-advanced) of [Brave](#brave). Mullvad Browser biedt deze bescherming out of the box, ten koste van enige flexibiliteit en gemak die andere privé-browsers kunnen bieden.

==Voor de sterkste bescherming tegen fingerprinting raden we aan Mullvad Browser te gebruiken in combinatie **met** een VPN==, of dat nu Mullvad is of een andere aanbevolen VPN-provider. Wanneer je een VPN met Mullvad Browser gebruikt, deelt je een vingerafdruk en een pool van IP-adressen met vele andere gebruikers, waardoor je een "menigte" krijgt om in op te gaan. Deze strategie is de enige manier om geavanceerde volgscripts te dwarsbomen, en is dezelfde anti-fingerprinting techniek die Tor Browser gebruikt.

Denk eraan dat je Mullvad Browser kunt gebruiken met elke VPN-provider, maar dat andere mensen op die VPN ook Mullvad Browser moeten gebruiken om deze "menigte" te laten bestaan, iets wat waarschijnlijker is bij Mullvad VPN in vergelijking met andere providers, vooral zo kort na de lancering van Mullvad Browser. Mullvad Browser heeft geen ingebouwde VPN-connectiviteit, noch controleert het of je een VPN gebruikt voordat je gaat browsen; jouw VPN-verbinding moet apart worden geconfigureerd en beheerd.

Mullvad Browser wordt geleverd met de *uBlock Origin* en *NoScript* browserextensies vooraf geïnstalleerd. Hoewel we het toevoegen van *extra* [browserextensies](browser-extensions.md) meestal afraden, mogen deze extensies die vooraf zijn geïnstalleerd met de browser **niet** worden verwijderd of geconfigureerd buiten hun standaardwaarden, omdat dit uw browser fingerprint duidelijk zou onderscheiden van andere gebruikers van Mullvad Browser. Het wordt ook vooraf geïnstalleerd met de Mullvad-browserextensie, die *kan* veilig worden verwijderd zonder jouw browservingerafdruk te beïnvloeden als je dat wilt, maar is ook veilig om te bewaren, zelfs als je geen Mullvad VPN gebruikt.

### Private Browsing Mode

Mullvad Browser werkt in een permanente privé browsing modus, wat betekent dat jouw geschiedenis, cookies en andere site gegevens altijd worden gewist elke keer dat de browser wordt gesloten. Jouw bladwijzers, browserinstellingen en extensie-instellingen blijven bewaard.

Dit is nodig om geavanceerde vormen van tracking te voorkomen, maar gaat wel ten koste van het gemak en sommige Firefox-functies, zoals Multi-Account Containers. Vergeet niet dat je altijd meerdere browsers kunt gebruiken, bijvoorbeeld Firefox+Arkenfox voor een paar sites waarop je ingelogd wilt blijven of die anders niet goed werken in Mullvad Browser, en Mullvad Browser voor algemeen browsen.

### Mullvad Leta

Mullvad Browser comes with [**Mullvad Leta**](https://leta.mullvad.net) as the default search engine, which functions as a proxy to either Google or Brave search results (configurable on the Mullvad Leta homepage).

If you are a Mullvad VPN user, there is some risk in using services like Mullvad Leta which are offered by your VPN provider themselves. This is because Mullvad theoretically has access to your true IP address (via their VPN) and your search activity (via Leta), which is information a VPN is typically intended to separate. Even though Mullvad collects very little information about their VPN subscribers or Leta users, you should consider a different [search engine](search-engines.md) if this risk concerns you.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** biedt krachtige privacy-instellingen zoals [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), die kunnen helpen bij het blokkeren van verschillende [soorten tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

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

These options can be found in :material-menu: → **Settings**.

#### Zoeken

- [ ] Uncheck **Show search suggestions**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Firefox stelt voor (alleen VS)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Deselecteer **Suggesties van sponsors**

#### Privacy & beveiliging

##### Verbeterde traceringsbescherming

- [x] Select **Strict** Verbeterde traceringsbescherming

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Saneren bij sluiten

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Check **Cookies en sitegegevens verwijderen wanneer Firefox wordt afgesloten**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Uncheck **Firefox toestaan technische en interactiegegevens naar Mozilla**te sturen
- [ ] Uncheck **Firefox toestaan om studies te installeren en uit te voeren**uit
- [ ] Uncheck **Firefox toestaan om namens je achterstallige crashmeldingen te verzenden uit**

According to Mozilla's privacy policy for Firefox,

> Firefox stuurt ons gegevens over jouw Firefox-versie en -taal; besturingssysteem van het apparaat en hardwareconfiguratie; geheugen, basisinformatie over crashes en fouten; resultaat van geautomatiseerde processen zoals updates, veilig browsen en activering. Wanneer Firefox gegevens naar ons verzendt, wordt uw IP-adres tijdelijk verzameld als onderdeel van onze serverlogs.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Open jouw [profielinstellingen op accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Schakel **Gegevensverzameling en -gebruik uit** > **Help Firefox-accounts verbeteren**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Select **Schakel HTTPS-only modus in alle vensters in**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Selecteer **Maximale Bescherming** en kies een geschikte provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (gevorderd)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) biedt dezelfde anti-fingeprint bescherming als Arkenfox out of the box, en vereist niet het gebruik van Mullvad's VPN om van deze bescherming te profiteren. In combinatie met een VPN kan Mullvad Browser meer geavanceerde tracking scripts dwarsbomen dan Arkenfox. Arkenfox heeft nog steeds het voordeel dat het veel flexibeler is, en uitzonderingen per site toestaat voor websites waarop je ingelogd moet blijven.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is gebouwd op het Chromium webbrowser project, dus het zou vertrouwd moeten aanvoelen en minimale website compatibiliteitsproblemen moeten hebben.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
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

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave voegt een "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" toe aan de file naam in downloads van de Brave website, die wordt gebruikt om te volgen van welke bron de browser heeft gedownload. Als voorbeeld `BRV002` in een download genaamd `Brave-Browser-BRV002.pkg`. Het installatieprogramma zal aan het eind van het installatieproces de server van Brave pingen met de verwijzingscode. Als u zich hier zorgen om maakt kunt u de naam van de installer veranderen voor het openen.

</div>

### Recommended Brave Configuration

These options can be found in :material-menu: → **Settings**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

De opties van Shields kunnen naar behoefte per site worden gedowngrade, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat u zich onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadaardige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Uncheck **Show search suggestions**

#### System

<div class="annotate" markdown>

- [ ] Zet **Achtergrondapps actief houden als Brave is gesloten** uit om achtergrond apps uit te schakelen (1)

</div>

1. Deze optie is niet op alle platforms aanwezig.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

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
