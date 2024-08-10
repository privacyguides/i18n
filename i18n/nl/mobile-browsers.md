---
meta_title: "Privacy respecterende mobiele webbrowsers voor Android en iOS - Privacy Guides"
title: "Mobiele browsers"
icon: material/cellphone-information
description: Deze browsers zijn wat we momenteel aanbevelen voor standaard/niet-anoniem internetten op jouw telefoon.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Aanbevelingen voor privé mobiele browsers
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance kapitalisme](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. In het algemeen raden we aan om extensies tot een minimum te beperken: ze hebben geprivilegieerde toegang binnen jouw browser, vereisen dat je de ontwikkelaar vertrouwt, kunnen je [doen opvallen](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), en [verzwakken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-Uchnm34/m/lDaXwQhzBAAJ) site-isolatie.

## Android

### Brave

<div class="admonition recommendation" markdown>

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

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Recommended Brave Configuration

Tor Browser is de enige manier om echt anoniem op het internet te surfen. Wanneer je Brave gebruikt, raden we je aan de volgende instellingen te wijzigen om jouw privacy tegen bepaalde partijen te beschermen, maar alle browsers behalve de [Tor Browser](tor.md#tor-browser) zijn in sommige opzichten traceerbaar door *iemand*.

Deze opties zijn te vinden in :material-menu: → **Instellingen** → **Dappere schilden & privacy**

##### Schilden

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Brave shields global defaults

De opties van Shields kunnen naar behoefte per site worden gedowngrade, maar standaard raden wij aan de volgende opties in te stellen:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Wij raden het gebruik van deze functie af; houd in plaats daarvan de standaardfilterlijsten aan. Het gebruik van extra lijsten zorgt ervoor dat u zich onderscheidt van andere Brave gebruikers en kan ook het aanvalsoppervlak vergroten als er een exploit in Brave is en een kwaadaardige regel wordt toegevoegd aan één van de lijsten die je gebruikt.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Browserdata opschonen

- [x] Selecteer **Gegevens wissen bij het sluiten van de browser**

##### Altijd-aan Incognito modus

- [ ] Uncheck alle sociale media componenten uit

##### Privacyrapport

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. InterPlanetary File System (IPFS) is een gedecentraliseerd, peer-to-peer netwerk voor het opslaan en delen van gegevens in een gedistribueerd bestandssysteem. Tenzij je de functie gebruikt, schakel hem uit.

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

### Mull

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** is a privacy oriented and deblobbed Android browser based on Firefox. Compared to Firefox, it offers much greater fingerprinting protection out of the box, and disables JavaScript Just-in-Time (JIT) compilation for enhanced security. It also removes all proprietary elements from Firefox, such as replacing Google Play Services references.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Firefox (Gecko)-based browsers on Android [lack](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] a powerful security feature that protects against a malicious site performing a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-like attack to gain access to the memory of another website you have open.[^2] Chromium-based browsers like [Brave](#brave) will provide more robust protection against malicious websites.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

#### Recommended Mull Configuration

We would suggest installing [uBlock Origin](browser-extensions.md#ublock-origin) as a content blocker if you want to block trackers within Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

Because Mull has more advanced and strict privacy protections enabled by default compared to most browsers, some websites may not load or work properly unless you adjust those settings. You can consult this [list of known issues and workarounds](https://divestos.org/pages/broken#mull) for advice on a potential fix if you do encounter a broken site. Adjusting a setting in order to fix a website could impact your privacy/security, so make sure you fully understand any instructions you follow.

## iOS

Op iOS is elke app die op het web kan surfen beperkt tot [](https://developer.apple.com/app-store/review/guidelines) het door Apple geleverde [WebKit framework](https://developer.apple.com/documentation/webkit), dus er is weinig reden om een webbrowser van een derde partij te gebruiken.

### Safari

<div class="admonition recommendation" markdown>

![Safari-logo](assets/img/browsers/safari.svg){ align=right }

**Safari** is de standaardbrowser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

#### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) as a content blocker if you want to block trackers within Safari.

The following privacy/security-related options can be found in the :gear: **Settings** app → **Safari**

##### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### Privacy & beveiliging

- [x] Activeer **Voorkom Cross-Site Tracking**

    Dit maakt WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp)mogelijk. De functie helpt beschermen tegen ongewenste tracking door gebruik te maken van on-device machine learning om trackers te stoppen. ITP beschermt tegen veel voorkomende bedreigingen, maar blokkeert niet alle tracking-wegen omdat het is ontworpen om de bruikbaarheid van websites niet te hinderen.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Privacyrapport

Privacyrapport biedt een momentopname van cross-site trackers die u momenteel niet kunnen profileren op de website die u bezoekt. Het kan ook een wekelijks rapport weergeven om te laten zien welke trackers in de loop van de tijd zijn geblokkeerd.

Privacyrapport is toegankelijk via het menu Pagina-instellingen.

##### Privacybehoudende advertentiemeting

- [ ] Schakel **Privacy Preserving Ad Measurement**uit

Bij het meten van advertentieklikken wordt van oudsher gebruik gemaakt van trackingtechnologie die inbreuk maakt op de privacy van de gebruiker. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

De functie heeft op zichzelf weinig privacyproblemen, dus hoewel je ervoor kunt kiezen om hem ingeschakeld te laten, beschouwen wij het feit dat hij automatisch is uitgeschakeld in Privénavigatie als een aanwijzing om de functie uit te schakelen.

##### Altijd privé browsen

Open Safari en tik op de knop Tabbladen, rechtsonder. Vouw vervolgens de lijst Tabbladgroepen uit.

- [x] Selecteer **Privé**

Safari's Privénavigatie modus biedt extra bescherming van de privacy. Private Browsing gebruikt een nieuwe [kortstondige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) sessie voor elk tabblad, wat betekent dat tabbladen van elkaar geïsoleerd zijn. Als er een [kwetsbaarheid is in uBlock Origin](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css) kan een filter van een derde partij kwaadaardige regels toevoegen die mogelijk gebruikersgegevens kunnen stelen.

Houd er rekening mee dat privénavigatie geen cookies en gegevens opslaat, zodat het niet mogelijk is om ingelogd te blijven op sites. Dit kan een ongemak zijn.

##### iCloud Synchronisatie

De synchronisatie van de Safari-geschiedenis, tabbladgroepen, iCloud-tabbladen en opgeslagen wachtwoorden verloopt via E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Ga naar jouw **Apple ID naam → iCloud → Geavanceerde gegevensbescherming**.

- [x] Zet **Geavanceerde gegevensbescherming aan**

Als je iCloud gebruikt terwijl Geavanceerde gegevensbescherming is uitgeschakeld, raden we je ook aan te controleren of de standaard downloadlocatie van Safari is ingesteld op lokaal op jouw apparaat. Extra filterlijsten kunnen de prestaties beïnvloeden en het aanvalsoppervlak vergroten, dus pas alleen toe wat u nodig hebt.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

### Minimale vereisten

- Moet automatische updates ondersteunen.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Wijzigingen die nodig zijn om de browser privacyvriendelijker te maken, mogen de gebruikerservaring niet negatief beïnvloeden.
