---
meta_title: "Privacy Respecting Mobile Web Browsers for Android and iOS - Privacy Guides"
title: "Mobila webbläsare"
icon: material/cellphone-information
description: These browsers are what we currently recommend for standard/non-anonymous internet browsing on your phone.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Mobile Browser Recommendations
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

Detta är våra för närvarande rekommenderade mobila webbläsare och konfigurationer för standardiserad/icke-anonym surfning på internet. Om du vill surfa anonymt på internet bör du använda [Tor](tor.md) i stället. I allmänhet rekommenderar vi att du håller ett minimum av tillägg; de har privilegierad åtkomst i din webbläsare, kräver att du litar på utvecklaren, kan få dig [att sticka ut](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)och [försvagar](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) webbplatsens isolering.

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave bygger på webbläsarprojektet Chromium, så den bör kännas bekant och ha minimala problem med webbkompatibilitet.

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

Tor Browser är det enda sättet att verkligen surfa anonymt på internet. När du använder Brave rekommenderar vi att du ändrar följande inställningar för att skydda din integritet från vissa parter, men alla andra webbläsare än [Tor Browser](tor.md#tor-browser) kommer att kunna spåras av *någon* i något avseende.

Dessa alternativ finns i :material-menu: → **Inställningar** → **Modiga sköldar & sekretess**

##### Sköldar

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Brave skyddar globala standardvärden

Shields alternativ kan nedgraderas vid behov för varje enskild plats, men som standard rekommenderar vi att du ställer in följande:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Vi avråder från att använda den här funktionen; behåll istället standardfilterlistorna. Om du använder extra listor sticker du ut från andra Brave-användare och kan också öka angreppsytan om det finns en exploit i Brave och en skadlig regel läggs till i en av de listor du använder.

</details>

- [x] Select **Upgrade connections to HTTPS**
- [x] Select **Always use secure connections**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under **Block fingerprinting**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Rensa surfhistorik

- [x] Välj **Rensa uppgifter vid avslut**

##### Blockering av sociala medier

- [ ] Avmarkera alla komponenter för sociala medier

##### Andra sekretessinställningar

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) is a decentralized, peer-to-peer network for storing and sharing data in a distributed filesystem. Unless you use the feature, disable it.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

I iOS är alla appar som kan surfa på webben [](https://developer.apple.com/app-store/review/guidelines) begränsade till att använda Apples WebKit-ramverk [WebKit](https://developer.apple.com/documentation/webkit), så det finns få skäl att använda en tredjepartswebbläsare.

### Safari

<div class="admonition recommendation" markdown>

![Safari-logotyp](assets/img/browsers/safari.svg){ align=right }

**Safari** är standardwebbläsaren i iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Recommended Firefox Configuration

These options can be found in :gear: **Settings** → **Safari**

##### Profiler

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### Privacy & Security

- [x] Aktivera **Förhindra spårning på andra webbplatser**

    Detta aktiverar WebKits [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Funktionen hjälper till att skydda mot oönskad spårning genom att använda maskininlärning på enheten för att stoppa spårare. ITP skyddar mot många vanliga hot, men blockerar inte alla spårningsvägar eftersom den är utformad för att inte störa användbarheten av webbplatser.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Integritetsrapport

Privacy Report ger en ögonblicksbild av de spårare som för närvarande förhindras från att profilera dig på den webbplats du besöker. Den kan också visa en veckorapport som visar vilka spårare som har blockerats över tid.

Rapporten om sekretess är tillgänglig via menyn Sidinställningar.

##### Sekretessbevarande annonsmätning

- [ ] Inaktivera **Integritetsbevarande annonsmätning**

Vid mätning av annonsklick har man traditionellt använt spårningsteknik som inkräktar på användarnas integritet. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Funktionen har i sig själv inga större problem med integriteten, så även om du kan välja att låta den vara aktiverad anser vi att det faktum att den automatiskt inaktiveras i privat surfning är en indikator för att inaktivera funktionen.

##### Alltid privat surfning

Öppna Safari och tryck på knappen Flikar längst ner till höger. Expandera sedan listan Flikgrupper.

- [x] Välj **Rensa uppgifter vid avslut**

Safaris läge för privat surfning ger ytterligare skydd för privatlivet. Privat surfning använder en ny [tillfällig](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) -session för varje flik, vilket innebär att flikarna är isolerade från varandra. Det finns också andra mindre sekretessfördelar med privat surfning, till exempel att inte skicka en webbsidas adress till Apple när du använder Safaris översättningsfunktion.

Observera att privat surfning inte sparar cookies och webbplatsdata, så det är inte möjligt att vara inloggad på webbplatser. Detta kan vara en olägenhet.

##### iCloud-synkronisering

Synkronisering av Safari-historik, flikgrupper, iCloud-flikar och sparade lösenord är E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Gå till ditt **Apple-ID-namn → iCloud → Avancerat dataskydd**.

- [x] Aktivera **Avancerat dataskydd**

Om du använder iCloud med avancerat dataskydd inaktiverat rekommenderar vi också att du kontrollerar att Safaris standardhämtningsplats är inställd på lokalt på din enhet. Detta alternativ finns i :gear: **Inställningar** → **Safari** → **Allmänt** → **Nedladdningar**.

## Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

### Minimikrav

- Måste ha stöd för automatiska uppdateringar.
- Måste få motoruppdateringar inom 0-1 dagar från uppströmsutgåvan.
- Eventuella ändringar som krävs för att göra webbläsaren mer integritetsvänlig bör inte påverka användarupplevelsen negativt.
- Android webbläsare måste använda Chromium-motorn.
    - Tyvärr är Mozilla GeckoView fortfarande mindre säkert än Chromium på Android.
    - iOS-browsers är begränsade till WebKit.
