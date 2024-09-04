---
meta_title: "Mobile Browser für Android und iOS, welche die Privatsphäre respektieren - Privacy Guides"
title: "Mobile Browser"
icon: material/cellphone-information
description: Wir empfehlen aktuell diese mobilen Browser für normales bzw. nicht anonymes Surfen im Internet.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Empfohlene Browser für Mobilgeräte
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
    url: https://www.apple.com/de/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Falls du anonym surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden.

## Android

### Brave

<div class="admonition recommendation" markdown>

![Brave-Logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** enthält einen eingebauten Inhaltsblocker und [Datenschutzfunktionen](https://brave.com/privacy-features), von denen viele standardmäßig aktiviert sind.

Brave basiert auf dem Chromium-Webbrowser-Projekt, sollte sich also vertraut anfühlen und nur minimale Probleme mit der Website-Kompatibilität haben.

[:octicons-home-16: Homepage](https://brave.com/de/){ .md-button .md-button--primary }
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

#### Empfohlene Brave-Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

Diese Optionen findest du unter :material-menu: → **Einstellungen** → **Schutz**

##### Schutz

Brave enthält einige Anti-Fingerabdruck-Maßnahmen in der [Schutz](https://support.brave.com/hc/articles/360022973471-What-is-Shields)-Funktion. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) für alle Seiten zu konfigurieren.

##### Globale Standardeinstellungen

Die Optionen im Schutz-Menü können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Wähle **Aggressiv** unter **Tracker & Anzeigenblockierung**

<details class="warning" markdown>
<summary>Inhaltsfilter</summary>

Brave ermöglicht die Auswahl zusätzlicher Inhaltsfilter auf der internen Seite `brave://adblock`. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. Diese Option bietet eine ähnliche Funktionalität wie die erweiterten Blockierungsmodi von uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) oder die Erweiterung [NoScript](https://noscript.net).

##### Browserdaten löschen

- [x] Wähle **Vergiss mich, wenn ich diese Seite schließe**

##### Social Media Blocking

- [ ] Deaktiviere alle Social Media Komponenten

##### Andere Datenschutzeinstellungen

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
2. InterPlanetary File System (IPFS) ist ein dezentrales Peer-To-Peer-Netzwerk zum Speichern und Teilen von Daten in einem verteilten Dateisystem. Wenn du die Funktion nicht nutzt, deaktiviere sie.

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt diese Daten mit E2EE.

### Mull

<div class="admonition recommendation" markdown>

![Mull-Logo](assets/img/browsers/mull.svg){ align=right }

**Mull** ist ein datenschutzorientierter und puristischer Android-Browser, der auf Firefox basiert. Im Vergleich zu Firefox bietet er einen wesentlich besseren Schutz vor Fingerabdrücken und deaktiviert die Just-in-Time-Kompilierung (JIT) von JavaScript, um die Sicherheit zu erhöhen. Außerdem werden alle proprietären Elemente aus Firefox entfernt, wie z. B. das Ersetzen der Verweise auf Google Play-Services.

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
<p class="admonition-title">Gefahr</p>

Firefox (Gecko)-based browsers on Android [lack](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] a powerful security feature that protects against a malicious site performing a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-like attack to gain access to the memory of another website you have open.[^2] Chromium-based browsers like [Brave](#brave) will provide more robust protection against malicious websites.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Wenn du Mull aus dem Standard-F-Droid-Repository herunterlädst, können sich Updates um einige Tage oder länger verzögern.

Mull aktiviert viele Funktionen, die vom [Tor Uplift-Projekt](https://wiki.mozilla.org/Security/Tor_Uplift) entwickelt wurden, indem es Einstellungen von [Arkenfox](desktop-browsers.md#arkenfox-advanced) verwendet. Proprietäre Blobs werden mit den für Fennec F-Droid entwickelten Skripten aus Mozillas Code entfernt.

#### Empfohlene Mull Konfiguration

Wir empfehlen die Installation von [uBlock Origin](browser-extensions.md#ublock-origin) als Inhaltsblocker, wenn du Tracker in Mull blockieren möchtest.

Mull verfügt über bereits standardmäßig konfigurierte Einstellungen zum Schutz der Privatsphäre. Du kannst die Option **Browserdaten beim Beenden löschen** in den Einstellungen von Mull konfigurieren, wenn du alle offenen Tabs beim Beenden der App automatisch schließen oder andere Daten wie den Browserverlauf und Cookies automatisch löschen möchtest.

Because Mull has more advanced and strict privacy protections enabled by default compared to most browsers, some websites may not load or work properly unless you adjust those settings. You can consult this [list of known issues and workarounds](https://divestos.org/pages/broken#mull) for advice on a potential fix if you do encounter a broken site. Adjusting a setting in order to fix a website could impact your privacy/security, so make sure you fully understand any instructions you follow.

## iOS

Unter iOS [muss](https://developer.apple.com/app-store/review/guidelines) jede App, auf welcher man im Web surfen kann, das [WebKit-Framework](https://developer.apple.com/documentation/webkit) von Apple zu verwenden. Es gibt deshalb wenig Gründe, den Browser eines Drittanbieters zu verwenden.

### Safari

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** ist der Standard-Browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

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

##### Datenschutz & Sicherheit

- [x] Aktivieren Sie **Cross-Sitetracking verhindern**

    Dies ermöglicht WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Die Funktion schützt vor unerwünschtem Tracking, indem sie maschinelles Lernen auf dem Gerät nutzt, um Tracker zu stoppen. Der verbesserte Schutz vor Aktivitätenverfolgung schützt vor vielen gängigen Bedrohungen, aber er blockiert nicht alle Tracking-Möglichkeiten, da er so konzipiert ist, dass die Benutzung der Webseite nicht oder nur minimal beeinträchtigt wird.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Datenschutzbericht

Der Datenschutzbericht bietet eine Momentaufnahme der Cross-Site-Tracker, die derzeit daran gehindert werden, auf der von Ihnen besuchten Website ein Profil zu erstellen. Es kann auch einen wöchentlichen Bericht anzeigen, aus dem hervorgeht, welche Tracker im Laufe der Zeit blockiert wurden.

Der Datenschutzbericht ist über das Menü "Website-Einstellungen" zugänglich.

##### Datenschutzkonforme Werbemessung

- [ ] Disable **Privacy Preserving Ad Measurement**

Bei der Messung von Anzeigenklicks werden traditionell Tracking-Technologien eingesetzt, die die Privatsphäre der Nutzer verletzen. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Die Funktion hat an sich wenig Datenschutzbedenken. Du kannst sie zwar aktiviert lassen, aber die Tatsache, dass sie beim Privaten Surfen automatisch deaktiviert wird, ist unserer Meinung nach ein Indikator für die Deaktivierung der Funktion.

##### Always-on Private Browsing

Öffne Safari und tippe unten rechts auf die Schaltfläche "Tabs". Erweiter dann die Liste der Tabgruppen.

- [x] Wähle **Privat**

Der Modus "Privates Surfen" von Safari bietet zusätzlichen Schutz für die Privatsphäre. Private Browsing verwendet eine neue [kurzlebige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) Sitzung für jedn Tab, was bedeutet, dass die Tabs voneinander isoliert sind. Private Browsing bietet noch weitere kleinere Vorteile für den Datenschutz, z. B. wird die Adresse einer Webseite nicht an Apple gesendet, wenn die Übersetzungsfunktion von Safari verwendet wird.

Beachte, dass Private Browsing keine Cookies und Website-Daten speichert, sodass es nicht möglich ist, auf Websites angemeldet zu bleiben. Dies kann zu Unannehmlichkeiten führen.

##### iCloud Sync

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. Allerdings werden Lesezeichen standardmäßig [nicht](https://support.apple.com/HT202303) verschlüsselt. Apple kann sie entschlüsseln und in Übereinstimmung mit der [Datenschutzrichtlinie](https://apple.com/legal/privacy/en-ww) darauf zugreifen.

Du kannst E2EE für deine Safari-Lesezeichen und Downloads aktivieren, indem du [Erweiterten Datenschutz](https://support.apple.com/de-de/108756) aktivierst. Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

Wenn du iCloud mit deaktiviertem erweitertem Datenschutz verwendest, empfehlen wir auch zu überprüfen, ob der Standard-Ladeort von Safari auf Ihrem Gerät lokal eingestellt ist. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Unterstützt automatische Updates.
- Muss Engine-Updates von Upstream-Releases schnell erhalten.
- Inhaltsperre muss unterstützt werden.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
