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

### Empfohlene Brave-Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave enthält einige Anti-Fingerabdruck-Maßnahmen in der [Schutz](https://support.brave.com/hc/articles/360022973471-What-is-Shields)-Funktion. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) für alle Seiten zu konfigurieren.

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
    - [x] Select **Close tabs on exit**
    - [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
    - [ ] Deaktiviere **Automatisch Diagnoseberichte senden**
    - [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**

    </div>

    1. Brave's [Implementierung von Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) auf Android proxyt **nicht**, wie das Desktop-Pendant, [Safe Browsing Netzwerkanfragen](https://developers.google.com/safe-browsing/v4/update-api#checking-urls). Das bedeutet, dass deine IP-Adresse von Google gesehen (und protokolliert) werden kann. Beachte, dass Safe Browsing für Android-Geräte ohne Google Play Services nicht verfügbar ist.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**

### Leo

Diese Optionen sind unter :material-menu: → **Einstellungen** → **Leo** zu finden.

<div class="annotate" markdown>

- [ ] Deaktiviere **Vorschläge zur Autovervollständigung in Adressleiste anzeigen** (1)

</div>

1. Diese Option ist in der iOS-App von Brave nicht vorhanden.

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt diese Daten mit E2EE.

## Mull (Android)

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

Firefox (Gecko)-basierten Browsern auf Android [fehlt](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] eine leistungsstarke Sicherheitsfunktion, die davor schützt, dass eine bösartige Website einen [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-ähnlichen Angriff durchführt, um Zugriff auf den Speicher einer anderen von dir geöffneten Website zu erlangen[^2] Chromium-basierte Browser wie [Brave](#brave) bieten einen zuverlässigeren Schutz vor bösartigen Websites.

</div>

Aktiviere das [F-Droid Repository](https://divestos.org/fdroid/official) von DivestOS, um Updates direkt vom Entwickler zu erhalten. Wenn du Mull aus dem Standard-F-Droid-Repository herunterlädst, können sich Updates um einige Tage oder länger verzögern.

Mull aktiviert viele Funktionen, die vom [Tor Uplift-Projekt](https://wiki.mozilla.org/Security/Tor_Uplift) entwickelt wurden, indem es Einstellungen von [Arkenfox](desktop-browsers.md#arkenfox-advanced) verwendet. Proprietäre Blobs werden mit den für Fennec F-Droid entwickelten Skripten aus Mozillas Code entfernt.

### Empfohlene Mull Konfiguration

Wir empfehlen die Installation von [uBlock Origin](browser-extensions.md#ublock-origin) als Inhaltsblocker, wenn du Tracker in Mull blockieren möchtest.

Mull verfügt über bereits standardmäßig konfigurierte Einstellungen zum Schutz der Privatsphäre. Du kannst die Option **Browserdaten beim Beenden löschen** in den Einstellungen von Mull konfigurieren, wenn du alle offenen Tabs beim Beenden der App automatisch schließen oder andere Daten wie den Browserverlauf und Cookies automatisch löschen möchtest.

Da in Mull im Vergleich zu den meisten Browsern standardmäßig ein erweiterter und strengerer Schutz der Privatsphäre aktiviert ist, können einige Websites möglicherweise nicht geladen werden oder nicht richtig funktionieren, wenn du diese Einstellungen nicht anpasst. Du kannst diese [Liste mit bekannten Problemen und Umgehungsmöglichkeiten](https://divestos.org/pages/broken#mull) konsultieren, um Ratschläge für eine mögliche Lösung zu erhalten, wenn du auf eine fehlerhafte Website stoßt. Wenn du eine Einstellung änderst, um eine Website zu reparieren, kann sich dies auf deine Privatsphäre/Sicherheit auswirken. Vergewisser dich daher, dass du alle Anweisungen, die du befolgst, vollständig verstehst.

## Safari (iOS)

Unter iOS [muss](https://developer.apple.com/app-store/review/guidelines) jede App, auf welcher man im Web surfen kann, das [WebKit-Framework](https://developer.apple.com/documentation/webkit) von Apple zu verwenden. Es gibt deshalb wenig Gründe, den Browser eines Drittanbieters zu verwenden.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** ist der Standard-Browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Datenschutz" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Dokumentation}

</details>

</div>

### Empfohlene Safari-Konfiguration

Wir empfehlen die Installation von [AdGuard](browser-extensions.md#adguard), wenn du einen Content-Blocker in Safari willst.

Die folgenden datenschutz- und sicherheitsrelevanten Optionen findest du unter :gear: **Einstellungen** → **Apps** → **Safari**.

#### Profile

Safari ermöglicht es, dein Browsing mit verschiedenen Profilen zu trennen. Alle deine Cookies, dein Verlauf und deine Website-Daten werden für jedes Profil separat gespeichert. Du solltest verschiedene Profile für verschiedene Zwecke verwenden, z. B. Einkaufen, Arbeit oder Schule.

#### Datenschutz & Sicherheit

- [x] Aktiviere **Cross-Sitetracking verhindern**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Aktiviere **Face ID/Touch ID zum Entsperren von „Privates Surfen“ anfordern**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

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

Der Modus "Privates Surfen" von Safari bietet zusätzlichen Schutz für die Privatsphäre. Private Browsing verwendet eine neue [kurzlebige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) Sitzung für jedn Tab, was bedeutet, dass die Tabs voneinander isoliert sind. Private Browsing bietet noch weitere kleinere Vorteile für den Datenschutz, z. B. wird die Adresse einer Webseite nicht an Apple gesendet, wenn die Übersetzungsfunktion von Safari verwendet wird.

Beachte, dass Private Browsing keine Cookies und Website-Daten speichert, sodass es nicht möglich ist, auf Websites angemeldet zu bleiben. Dies kann zu Unannehmlichkeiten führen.

#### iCloud Sync

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. Allerdings werden Lesezeichen standardmäßig [nicht](https://support.apple.com/HT202303) verschlüsselt. Apple kann sie entschlüsseln und in Übereinstimmung mit der [Datenschutzrichtlinie](https://apple.com/legal/privacy/en-ww) darauf zugreifen.

Du kannst E2EE für deine Safari-Lesezeichen und Downloads aktivieren, indem du [Erweiterten Datenschutz](https://support.apple.com/de-de/108756) aktivierst. Gehen Sie zu :gear: **Einstellungen** → **iCloud** → **Erweiterter Datenschutz**.

- [x] Wähle **Erweiterten Datenschutz aktivieren**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Unterstützt automatische Updates.
- Muss Engine-Updates von Upstream-Releases schnell erhalten.
- Inhaltsperre muss unterstützt werden.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
