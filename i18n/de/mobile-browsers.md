---
meta_title: "Mobile Browser für Android und iOS, welche die Privatsphäre respektieren - Privacy Guides"
title: "Mobile Browser"
icon: material/cellphone-information
description: Wir empfehlen aktuell diese mobilen Browser für normales bzw. nicht anonymes Surfen im Internet.
cover: mobile-browsers.png
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
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Wir empfehlen aktuell diese mobilen Browser und Konfigurationen für normales bzw. nicht anonymes Surfen im Internet. Falls du anonym surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden. Generell raten wir dir, möglichst wenig Erweiterungen zu verwenden; diese haben weitreichenden Zugriff auf deinen Browser, verlangen dein Vertrauen in den Entwickler, können dich [hervorheben](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) und die Seiten-Isolierung [schwächen](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

Unter Android ist Firefox immer noch weniger sicher als Chromium-basierte Alternativen: Mozillas Engine, [GeckoView](https://mozilla.github.io/geckoview/), hat noch keine Unterstützung für [Site Isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) oder muss noch [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196) aktivieren.

### Brave

!!! recommendation

    ![Brave-Logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** enthält einen eingebauten Inhaltsblocker und [Datenschutzfunktionen](https://brave.com/privacy-features/), von denen viele standardmäßig aktiviert sind.
    
    Brave basiert auf dem Chromium-Webbrowser-Projekt, sollte sich also vertraut anfühlen und nur minimale Probleme mit der Website-Kompatibilität haben.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Dokumentation }
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title=Quellcode }
    
    ??? downloads annotate
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### Empfohlene Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

Diese Optionen findest du unter :material-menu: → **Einstellungen** → **Brave Shields & Datenschutz**

##### Shields

Brave bietet einige Anti-Fingerprinting-Maßnamen in seinem [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-)-Feature. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) für alle Seiten, die du besuchst, zu konfigurieren.

##### Brave Shields' globale Standardeinstellungen

Die Optionen von Shields können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Wähle **Tracker und Werbung blockieren (aggressiv)** unter **Tracker & Werbung blockieren**

    ??? warning "Standard-Filterlisten verwenden"
        Brave ermöglicht die Auswahl zusätzlicher Inhaltsfilter auf der internen Seite `brave://adblock`. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

- [x] Wähle **Alle Verbindungen müssen HTTPS verwenden (streng)**
- [x] (Optional) Wähle **Skripte blockieren** (1)
- [x] Wähle **Fingerabdruck blockiert (streng, könnte Websites kaputtmachen** unter **Fingerprinting blockieren**

</div>

1. Diese Option bietet eine ähnliche Funktionalität wie die erweiterten Blockierungsmodi von uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) oder die Erweiterung [NoScript](https://noscript.net/).

##### Browserdaten löschen

- [x] Wähle **Daten beim Beenden löschen**

##### Social Media Blocking

- [ ] Deaktiviere alle Social Media Komponenten

##### Andere Datenschutzeinstellungen

<div class="annotate" markdown>

- [x] Wähle **Nicht-proxisiertes UDP deaktivieren** unter [WebRTC-IP-Nutzungsrichtlinien](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Deaktiviere **Websites die Abfrage gespeicherter Zahlungsmethoden erlauben**
- [ ] Deaktiviere **IPFS-Gateway** (1)
- [x] Wähle **Registerkarten beim Beenden schließen**
- [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
- [ ] Deaktiviere **Automatisch Diagnoseberichte senden**
- [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden.**

</div>

1. InterPlanetary File System (IPFS) ist ein dezentrales Peer-To-Peer-Netzwerk zum Speichern und Teilen von Daten in einem verteilten Dateisystem. Wenn du die Funktion nicht nutzt, deaktiviere sie.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt dich mit E2EE.

## iOS

Unter iOS [muss](https://developer.apple.com/app-store/review/guidelines) jede App, auf welcher man im Web surfen kann, das [WebKit-Framework](https://developer.apple.com/documentation/webkit) von Apple zu verwenden. Es gibt deshalb wenig Gründe, den Browser eines Drittanbieters zu verwenden.

### Safari

!!! recommendation

    ![Safari logo](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** ist der Standard-Browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, and fingerprinting reduction by presenting a simplified version of the system configuration to websites so more devices look identical.
    
    [:octicons-home-16: Webseite](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Safari & Datenschutz" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### Empfohlene Konfiguration

Diese Optionen finden Sie unter :gear: **Einstellungen** → **Safari** → **Datenschutz und Sicherheit**.

##### Verhindern von seitenübergreifendem Tracking

- [x] Enable **Prevent Cross-Site Tracking**

Dies ermöglicht WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Die Funktion schützt vor unerwünschtem Tracking, indem sie maschinelles Lernen auf dem Gerät nutzt, um Tracker zu stoppen. Der verbesserte Schutz vor Aktivitätenverfolgung schützt vor vielen gängigen Bedrohungen, aber er blockiert nicht alle Tracking-Möglichkeiten, da er so konzipiert ist, dass die Benutzung der Webseite nicht oder nur minimal beeinträchtigt wird.

##### Datenschutzbericht

Der Datenschutzbericht bietet eine Momentaufnahme der Cross-Site-Tracker, die derzeit daran gehindert werden, auf der von Ihnen besuchten Website ein Profil zu erstellen. Es kann auch einen wöchentlichen Bericht anzeigen, aus dem hervorgeht, welche Tracker im Laufe der Zeit blockiert wurden.

Privacy Report is accessible via the Page Settings menu.

##### Datenschutzkonforme Werbemessung

- [ ] Disable **Privacy Preserving Ad Measurement**

Bei der Messung von Anzeigenklicks werden traditionell Tracking-Technologien eingesetzt, die die Privatsphäre der Nutzer verletzen. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) ist eine WebKit-Funktion und ein vorgeschlagener Webstandard, der es Werbetreibenden ermöglichen soll, die Effektivität von Web-Kampagnen zu messen, ohne die Privatsphäre der Nutzer zu gefährden.

Die Funktion hat an sich wenig Datenschutzbedenken. Du kannst sie zwar aktiviert lassen, aber die Tatsache, dass sie beim Privaten Surfen automatisch deaktiviert wird, ist unserer Meinung nach ein Indikator für die Deaktivierung der Funktion.

##### Always-on Private Browsing

Öffne Safari und tippe unten rechts auf die Schaltfläche "Tabs". Erweiter dann die Liste der Tabgruppen.

- [x] Wähle **Privat**

Der Modus "Privates Surfen" von Safari bietet zusätzlichen Schutz für die Privatsphäre. Private Browsing verwendet eine neue [kurzlebige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) Sitzung für jedn Tab, was bedeutet, dass die Tabs voneinander isoliert sind. Private Browsing bietet noch weitere kleinere Vorteile für den Datenschutz, z. B. wird die Adresse einer Webseite nicht an Apple gesendet, wenn die Übersetzungsfunktion von Safari verwendet wird.

Beachte, dass Private Browsing keine Cookies und Website-Daten speichert, sodass es nicht möglich ist, auf Websites angemeldet zu bleiben. Dies kann zu Unannehmlichkeiten führen.

##### iCloud Sync

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. Standardmäßig sind die Lesezeichen jedoch [nicht](https://support.apple.com/en-us/HT202303) auf diese Weise geschützt. Apple kann sie entschlüsseln und in Übereinstimmung mit der [Datenschutzrichtlinie](https://www.apple.com/legal/privacy/en-ww/) darauf zugreifen.

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/en-us/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

Wenn du iCloud mit deaktiviertem erweitertem Datenschutz verwendest, empfehlen wir auch zu überprüfen, ob der Standard-Ladeort von Safari auf Ihrem Gerät lokal eingestellt ist. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

!!! recommendation

    ![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }
    
    **AdGuard for iOS** is a free and open-source content-blocking extension for Safari that uses the native [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).
    
    AdGuard for iOS has some premium features; however, standard Safari content blocking is free of charge.
    
    [:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

Zusätzliche Filterlisten verlangsamen die Arbeit und können die Angriffsfläche vergrößern, daher solltest du nur das anwenden, was du brauchst.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

!!! example "Dieser Abschnitt ist neu"

    Wir arbeiten aktuell daran, Kriterien für jeden Bereich unserer Webseite festzulegen. Dieser Abschnitt kann sich deshalb noch ändern. Bei Fragen zu unseren Kriterien, können diese [in unserem Forum] (https://discuss.privacyguides.net/latest) gestellt werden. Und gehen nicht davon aus, dass wir etwas bei unseren Empfehlungen nicht berücksichtigt haben, wenn es hier nicht aufgeführt ist. Es gibt viele Faktoren, die berücksichtigt und besprochen werden, wenn wir ein Projekt empfehlen, und die Dokumentation jedes einzelnen Faktors ist ein laufender Prozess.

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
