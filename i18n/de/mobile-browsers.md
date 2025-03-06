---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
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
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
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

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Wir empfehlen aktuell diese **mobilen Webbrowsers** und Konfigurationen für normales bzw. nicht anonymes Surfen im Internet. Falls du anonym surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden.

## Brave

<div class="admonition recommendation" markdown>

![Brave-Logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** enthält einen eingebauten Inhaltsblocker und [Datenschutzfunktionen](https://brave.com/privacy-features), von denen viele standardmäßig aktiviert sind.

Brave basiert auf dem Chromium-Webbrowser-Projekt, sollte sich also vertraut anfühlen und nur minimale Probleme mit der Website-Kompatibilität haben.

[:octicons-home-16: Homepage](https://brave.com/de/){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion/de/){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.brave.com/hc/de){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Empfohlene Brave-Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Die Optionen im Schutz-Menü können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

=== "Android"

    <div class="annotate" markdown>

    - [x] Wähle **Aggressiv** unter *Tracker & Anzeigenblockierung*
    - [x] Select **Auto-redirect AMP pages**
    - [x] Select **Auto-redirect tracking URLs**
    - [x] Select **Require all connections to use HTTPS (strict)** under *Upgrade connections to HTTPS*
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block third-party cookies** under *Block Cookies*
    - [x] Select **Block Fingerprinting**
    - [x] Select **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. Mit dieser Option wird JavaScript deaktiviert, was bei vielen Websites zu Problemen führt. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

    </details>

    </div>

    1. Mit dieser Option wird JavaScript deaktiviert, was bei vielen Websites zu Problemen führt. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

##### Browsing-Daten löschen (nur Android)

- [x] Wähle **Vergiss mich, wenn ich diese Seite schließe**

##### Blockieren von sozialen Medien (nur Android)

- [ ] Deaktiviere alle Social Media Komponenten

#### Andere Datenschutzeinstellungen

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [ ] Uncheck **V8 Optimizer** under *Manage V8 security*
    - [x] Select **Close tabs on exit**
    - [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
    - [ ] Deaktiviere **Automatisch Diagnoseberichte senden**
    - [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**

    </div>

    1. Brave's [Implementierung von Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) auf Android proxyt **nicht**, wie das Desktop-Pendant, [Safe Browsing Netzwerkanfragen](https://developers.google.com/safe-browsing/v4/update-api#checking-urls). Das bedeutet, dass deine IP-Adresse von Google gesehen (und protokolliert) werden kann. Beachte, dass Safe Browsing für Android-Geräte ohne Google Play Services nicht verfügbar ist.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**

#### Leo

Diese Optionen sind unter :material-menu: → **Einstellungen** → **Leo** zu finden.

<div class="annotate" markdown>

- [ ] Deaktiviere **Vorschläge zur Autovervollständigung in Adressleiste anzeigen** (1)

</div>

1. Diese Option ist in der iOS-App von Brave nicht vorhanden.

#### Search engines

These options can be found in :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] **Suchvorschläge anzeigen** deaktivieren

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** is a Chromium-based browser with built-in ad blocking, fingerprinting protections, and other [privacy and security enhancements](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the discontinued **Bromite** browser.

[:octicons-home-16: Homepage](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Empfohlene Konfiguration

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### Sicherheit

- [x] Select **Always use secure connections**

This prevents you from unintentionally connecting to a website in plain-text HTTP. HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Chromium engine like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** ist der Standard-Browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### Empfohlene Safari-Konfiguration

Wir empfehlen die Installation von [AdGuard](browser-extensions.md#adguard), wenn du einen Content-Blocker in Safari willst.

Die folgenden datenschutz- und sicherheitsrelevanten Optionen findest du unter :gear: **Einstellungen** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Suche

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Indem du die Suchvorschläge deaktivierst, kannst du präziser kontrollieren, welche Daten an den Suchmaschinenanbieter gesendet werden.

#### Profile

Safari ermöglicht es, dein Browsing mit verschiedenen Profilen zu trennen. Alle deine Cookies, dein Verlauf und deine Website-Daten werden für jedes Profil separat gespeichert. Du solltest verschiedene Profile für verschiedene Zwecke verwenden, z. B. Einkaufen, Arbeit oder Schule.

#### Datenschutz & Sicherheit

- [x] Aktiviere **Cross-Sitetracking verhindern**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Aktiviere **Face ID/Touch ID zum Entsperren von „Privates Surfen“ anfordern**

Mit dieser Einstellung kannst du deine privaten Tabs bei Nichtgebrauch mit Biometrie/PIN sperren.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Andere Datenschutzeinstellungen

Diese Optionen sind zu finden unter :gear: **Einstellungen** → **Apps** → **Safari** → **Erweitert**.

##### Fingerprinting Mitigations

Bei der Einstellung **Erweiterter Tracking- und Identifizierungsschutz** werden bestimmte Werte zufällig ausgewählt, sodass es schwieriger ist, deine Fingerabdrücke zu erkennen:

- [x] Wähle **Beim Surfen immer** oder **Privates Surfen**

##### Datenschutzkonforme Werbemessung

- [ ] Deaktiviere **Datenschutzwahrende Werbungsmessung**

Bei der Messung von Anzeigenklicks werden traditionell Tracking-Technologien eingesetzt, die die Privatsphäre der Nutzer verletzen. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) ist eine WebKit-Funktion und ein vorgeschlagener Webstandard, der es Werbetreibenden ermöglichen soll, die Effektivität von Web-Kampagnen zu messen, ohne die Privatsphäre von Nutzern zu gefährden.

Die Funktion hat an sich wenig Datenschutzbedenken. Du kannst sie zwar aktiviert lassen, aber die Tatsache, dass sie beim Privaten Surfen automatisch deaktiviert wird, ist unserer Meinung nach ein Indikator für die Deaktivierung der Funktion.

#### Always-on Private Browsing

Öffne Safari und tippe unten rechts auf die Schaltfläche "Tabs". Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Wähle **Privat**

Der Modus "Privates Surfen" von Safari bietet zusätzlichen Schutz für die Privatsphäre. Private Browsing verwendet eine neue [kurzlebige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) Sitzung für jedn Tab, was bedeutet, dass die Tabs voneinander isoliert sind. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Beachte, dass Private Browsing keine Cookies und Website-Daten speichert, sodass es nicht möglich ist, auf Websites angemeldet zu bleiben. Dies kann zu Unannehmlichkeiten führen.

#### iCloud Sync

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. Allerdings werden Lesezeichen standardmäßig [nicht](https://support.apple.com/HT202303) verschlüsselt. Apple kann sie entschlüsseln und in Übereinstimmung mit der [Datenschutzrichtlinie](https://apple.com/legal/privacy/en-ww) darauf zugreifen.

Du kannst E2EE für deine Safari-Lesezeichen und Downloads aktivieren, indem du [Erweiterten Datenschutz](https://support.apple.com/de-de/108756) aktivierst. Gehen Sie zu :gear: **Einstellungen** → **iCloud** → **Erweiterter Datenschutz**.

- [x] Wähle **Erweiterten Datenschutz aktivieren**

Wenn du iCloud mit deaktiviertem erweiterten Datenschutz verwendest, empfehlen wir außerdem, den Standard-Ladeort von Safari auf einen lokalen Ordner auf deinem Gerät zu setzen. Diese Option ist zu finden unter :gear: **Einstellungen** → **Apps** → **Safari** → **Allgemein** → **Downloads**.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Unterstützt automatische Updates.
- Muss Engine-Updates von Upstream-Releases schnell erhalten.
- Inhaltsperre muss unterstützt werden.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
