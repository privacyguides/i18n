---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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
      - iOS
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

- [:material-account-cash: Övervakningskapitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Om du vill surfa anonymt på internet bör du använda [Tor](tor.md) i stället.

## Brave

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
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Recommended Brave Configuration

Tor Browser är det enda sättet att verkligen surfa anonymt på internet. När du använder Brave rekommenderar vi att du ändrar följande inställningar för att skydda din integritet från vissa parter, men alla andra webbläsare än [Tor Browser](tor.md#tor-browser) kommer att kunna spåras av *någon* i något avseende.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields alternativ kan nedgraderas vid behov för varje enskild plats, men som standard rekommenderar vi att du ställer in följande:

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Block trackers & ads*
    - [x] Select **Auto-redirect AMP pages**
    - [x] Select **Auto-redirect tracking URLs**
    - [x] Select **Require all connections to use HTTPS (strict)** under *Upgrade connections to HTTPS*
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block third-party cookies** under *Block Cookies*
    - [x] Select **Block Fingerprinting**
    - [x] Select **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. Vi avråder från att använda den här funktionen; behåll istället standardfilterlistorna. Om du använder extra listor sticker du ut från andra Brave-användare och kan också öka angreppsytan om det finns en exploit i Brave och en skadlig regel läggs till i en av de listor du använder.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Vi avråder från att använda den här funktionen; behåll istället standardfilterlistorna. Om du använder extra listor sticker du ut från andra Brave-användare och kan också öka angreppsytan om det finns en exploit i Brave och en skadlig regel läggs till i en av de listor du använder.

    </details>

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

##### Clear browsing data (Android only)

- [x] Välj **Rensa uppgifter vid avslut**

##### Social Media Blocking (Android only)

- [ ] Avmarkera alla komponenter för sociala medier

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [x] Select **Close tabs on exit**
    - [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
    - [ ] Uncheck **Automatically send diagnostic reports**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## Mull (Android)

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

Firefox (Gecko)-baserade webbläsare på Android [saknar](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [sidisolering](https://wiki.mozilla.org/Project_Fission),[^1] en kraftfull säkerhetsfunktion som skyddar när en hemsida försöker utföra en [Spectre](https://sv.wikipedia.org/wiki/Spectre_(s%C3%A4kerhetsh%C3%A5l))-liknande attack för att få tillgång till minnet av en annan hemsida du har öppen.[^2] Chromiumbaserade webbläsare som [Brave](#brave) ger bättre skydd mote farliga hemsidor.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

### Recommended Mull Configuration

Vi föreslår att du installerar [uBlock Origin](browser-extensions.md#ublock-origin) som en innehållsblockerare om du vill blockera trackers inom Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

Eftersom att Mull har mer avancerade och strikta integritetsskyddsinställningar aktiverade automatiskt jämfört med många webbläsare kan en del hemsidor stoppas från att laddas, eller inte fungera som tänkt, om du inte ändrar de inställningarna. Den här [listan med kända fel och lösningar](https://divestos.org/pages/broken#mull) kan ge dig tips om hur du kan åtgärda felen när du råkar på en sida som inte laddar korrekt. Att ändra inställningar för att fixa en sida som laddar fel kan påverka integritet och säkerhet, så var säker på att du förstår alla instruktioner du följer.

## Safari (iOS)

I iOS är alla appar som kan surfa på webben [](https://developer.apple.com/app-store/review/guidelines) begränsade till att använda Apples WebKit-ramverk [WebKit](https://developer.apple.com/documentation/webkit), så det finns få skäl att använda en tredjepartswebbläsare.

<div class="admonition recommendation" markdown>

![Safari-logotyp](assets/img/browsers/safari.svg){ align=right }

**Safari** är standardwebbläsaren i iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical) as well as fingerprint randomization, and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Rekommenderad konfiguration för Safari

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

Följande integritet- och säkerhetsrelaterade inställningar kan hittas under :gear:**Inställningar** → **Safari**

#### Profiler

Alla webbplatskakor, historik och webbplats data kommer att vara separata för varje profil. Du borde använda olika profiler för olika ändamål, t.ex. Shopping, Arbete, eller Studier.

#### Integritet & Säkerhet

- [x] Aktivera **Förhindra spårning på andra webbplatser**

    Detta aktiverar WebKits [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Funktionen hjälper till att skydda mot oönskad spårning genom att använda maskininlärning på enheten för att stoppa spårare. ITP skyddar mot många vanliga hot, men blockerar inte alla spårningsvägar eftersom den är utformad för att inte störa användbarheten av webbplatser.

- [x] Aktivera **Kräv Face ID för att Låsa upp Privat Surfning**

    Den här inställningen låter dig låsa dina privata flikar med biometrik/PIN när de inte används.

#### Avancerat → Sekretess

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

#### Integritetsrapport

Privacy Report ger en ögonblicksbild av de spårare som för närvarande förhindras från att profilera dig på den webbplats du besöker. Den kan också visa en veckorapport som visar vilka spårare som har blockerats över tid.

Rapporten om sekretess är tillgänglig via menyn Sidinställningar.

#### Sekretessbevarande annonsmätning

- [ ] Inaktivera **Integritetsbevarande annonsmätning**

Vid mätning av annonsklick har man traditionellt använt spårningsteknik som inkräktar på användarnas integritet. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Funktionen har i sig själv inga större problem med integriteten, så även om du kan välja att låta den vara aktiverad anser vi att det faktum att den automatiskt inaktiveras i privat surfning är en indikator för att inaktivera funktionen.

#### Alltid privat surfning

Öppna Safari och tryck på knappen Flikar längst ner till höger. Expandera sedan listan Flikgrupper.

- [x] Välj **Rensa uppgifter vid avslut**

Safaris läge för privat surfning ger ytterligare skydd för privatlivet. Privat surfning använder en ny [tillfällig](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) -session för varje flik, vilket innebär att flikarna är isolerade från varandra. Det finns också andra mindre sekretessfördelar med privat surfning, till exempel att inte skicka en webbsidas adress till Apple när du använder Safaris översättningsfunktion.

Observera att privat surfning inte sparar cookies och webbplatsdata, så det är inte möjligt att vara inloggad på webbplatser. Detta kan vara en olägenhet.

#### iCloud-synkronisering

Synkronisering av Safari-historik, flikgrupper, iCloud-flikar och sparade lösenord är E2EE. Bokmärken är [inte](https://support.apple.com/HT202303) förinställt krypterade. Apple kan dekryptera och komma åt dem, enligt deras [integritetspolicy](https://apple.com/legal/privacy/en-ww).

Du kan aktivera E2EE för Safaribokmärken och nedladdningar genom att aktivera [Avancerat dataskydd](https://support.apple.com/HT212520). Gå till ditt **Apple-ID-namn → iCloud → Avancerat dataskydd**.

- [x] Aktivera **Avancerat dataskydd**

Om du använder iCloud med avancerat dataskydd inaktiverat rekommenderar vi också att du kontrollerar att Safaris standardhämtningsplats är inställd på lokalt på din enhet. Detta alternativ finns i :gear: **Inställningar** → **Safari** → **Allmänt** → **Nedladdningar**.

## Kriterier

**Observera att vi inte är knutna till något av de projekt som vi rekommenderar.** Förutom [våra standardkriterier](about/criteria.md)har vi utvecklat en tydlig uppsättning krav som gör det möjligt för oss att ge objektiva rekommendationer. Vi föreslår att du bekantar dig med den här listan innan du väljer att använda ett projekt, och att du gör din egen forskning för att se till att det är rätt val för dig.

### Minimikrav

- Måste ha stöd för automatiska uppdateringar.
- Måste få snabba motoruppdateringar från uppströmsversioner.
- Måste stödja innehållsblockering.
- Eventuella ändringar som krävs för att göra webbläsaren mer integritetsvänlig bör inte påverka användarupplevelsen negativt.
