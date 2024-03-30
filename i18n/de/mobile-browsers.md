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
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Wir empfehlen aktuell diese mobilen Browser und Konfigurationen für normales bzw. nicht anonymes Surfen im Internet. Falls du anonym surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden. Generell raten wir dir, möglichst wenig Erweiterungen zu verwenden; diese haben weitreichenden Zugriff auf deinen Browser, verlangen dein Vertrauen in den Entwickler, können dich [hervorheben](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) und die Seiten-Isolierung [schwächen](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

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

#### Empfohlene Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

Diese Optionen findest du unter :material-menu: → **Einstellungen** → **Brave Shields & Datenschutz**

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Brave Shields' globale Standardeinstellungen

Die Optionen von Shields können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

</details>

- [x] Wähle **Alle Verbindungen müssen HTTPS verwenden (streng)**
- [x] (Optional) Wähle **Skripte blockieren** (1)
- [x] Wähle **Fingerabdruck blockiert (streng, könnte Websites kaputtmachen** unter **Fingerprinting blockieren**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Browserdaten löschen

- [x] Wähle **Daten beim Beenden löschen**

##### Social Media Blocking

- [ ] Deaktiviere alle Social Media Komponenten

##### Andere Datenschutzeinstellungen

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) ist ein dezentrales Peer-To-Peer-Netzwerk zum Speichern und Teilen von Daten in einem verteilten Dateisystem. Wenn du die Funktion nicht nutzt, deaktiviere sie.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

Unter iOS [muss](https://developer.apple.com/app-store/review/guidelines) jede App, auf welcher man im Web surfen kann, das [WebKit-Framework](https://developer.apple.com/documentation/webkit) von Apple zu verwenden. Es gibt deshalb wenig Gründe, den Browser eines Drittanbieters zu verwenden.

### Safari

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** ist der Standard-Browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Empfohlene Konfiguration

These options can be found in :gear: **Settings** → **Safari**

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

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

Wenn du iCloud mit deaktiviertem erweitertem Datenschutz verwendest, empfehlen wir auch zu überprüfen, ob der Standard-Ladeort von Safari auf Ihrem Gerät lokal eingestellt ist. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

**AdGuard for iOS** is a free and open-source content-blocking extension for Safari that uses the native [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).

AdGuard for iOS has some premium features; however, standard Safari content blocking is free of charge.

[:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

Zusätzliche Filterlisten verlangsamen die Arbeit und können die Angriffsfläche vergrößern, daher solltest du nur das anwenden, was du brauchst.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Unterstützt automatische Updates.
- Erhält Engine-Updates in 0-1 Tagen nach der Upstream-Veröffentlichung.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
- Android-Browser müssen die Chromium-Engine verwenden.
    - Leider ist Mozilla GeckoView auf Android immer noch weniger sicher als Chromium.
    - iOS-Browser sind auf WebKit beschränkt.

### Weitere Kriterien

- Darf keine eingebauten Browser- oder Betriebssystemfunktionen replizieren.
- Muss sich direkt auf die Privatsphäre der Nutzer auswirken, d. h. es dürfen nicht einfach nur Informationen geliefert werden.
