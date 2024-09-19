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
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)

</details>

</div>

### Empfohlene Brave-Konfiguration

Tor Browser ist die einzige Möglichkeit, wirklich anonym im Internet zu surfen. Wenn du Brave benutzt, empfehlen wir dir, die folgenden Einstellungen zu ändern, um deine Privatsphäre vor bestimmten Parteien zu schützen, aber alle anderen Browser als der [Tor Browser](tor.md#tor-browser) werden von *irgendjemandem* in irgendeiner Weise verfolgt werden können.

Diese Optionen findest du unter :material-menu: → **Einstellungen** → **Brave Schutz & Datenschutz**

#### Shields

Brave enthält einige Anti-Fingerabdruck-Maßnahmen in der [Schutz](https://support.brave.com/hc/articles/360022973471-What-is-Shields)-Funktion. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) für alle Seiten zu konfigurieren.

#### Brave shields global defaults

Die Optionen im Schutz-Menü können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Wähle **Aggressiv** unter **Tracker & Anzeigenblockierung**

<details class="warning" markdown>
<summary>Inhaltsfilter</summary>

Brave ermöglicht die Auswahl zusätzlicher Inhaltsfilter auf der internen Seite `brave://adblock`. Wir raten davon ab diese Funktion zu verwenden. Verwende stattdessen die voreingestellten Filterlisten. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab, kann die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer von dir verwendeten Listen hinzugefügt wird.

</details>

- [x] Wähle **AMP-Seiten automatisch umleiten**
- [x] Wähle **Tracking-URLs automatisch umleiten**
- [x] Wähle **streng** unter **Verbindungen auf HTTPS upgraden**
- [x] (Optional) Wähle **Skripte blockieren** (1)
- [x] Wähle **Drittanbieter-Cookies blockieren** unter **Cookies blockieren**
- [x] Wähle **Fingerprinting blockieren**
- [x] Wähle **Fingerprinting über die Spracheinstellungen verhindern**

</div>

1. Diese Option bietet eine ähnliche Funktionalität wie die erweiterten Blockierungsmodi von uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) oder die Erweiterung [NoScript](https://noscript.net).

#### Clear browsing data

- [x] Wähle **Vergiss mich, wenn ich diese Seite schließe**

#### Social Media Blocking

- [ ] Deaktiviere alle Social Media Komponenten

#### Other privacy settings

<div class="annotate" markdown>

- [x] Wähle **Nicht-proxisiertes UDP deaktivieren** unter [WebRTC-IP-Nutzungsrichtlinien](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Wähle **Kein Schutz** unter **Safe Browsing** (1)
- [ ] Deaktiviere **Websites die Abfrage gespeicherter Zahlungsmethoden erlauben**
- [ ] Deaktiviere **IPFS Gateway** (2)
- [x] Wähle **Registerkarten beim Beenden schließen**
- [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
- [ ] Deaktiviere **Automatisch Diagnosebericht senden**
- [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**

</div>

1. Brave's [Implementierung von Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) auf Android proxyt **nicht**, wie das Desktop-Pendant, [Safe Browsing Netzwerkanfragen](https://developers.google.com/safe-browsing/v4/update-api#checking-urls). Das bedeutet, dass deine IP-Adresse von Google gesehen (und protokolliert) werden kann. Beachte, dass Safe Browsing für Android-Geräte ohne Google Play Services nicht verfügbar ist.
2. InterPlanetary File System (IPFS) ist ein dezentrales Peer-To-Peer-Netzwerk zum Speichern und Teilen von Daten in einem verteilten Dateisystem. Wenn du die Funktion nicht nutzt, deaktiviere sie.

### Leo

Diese Optionen sind unter :material-menu: → **Einstellungen** → **Leo** zu finden.

- [ ] Deaktiviere **Vorschläge zur Autovervollständigung in Adressleiste anzeigen**

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

### Recommended Mull Configuration

Wir empfehlen die Installation von [uBlock Origin](browser-extensions.md#ublock-origin) als Inhaltsblocker, wenn du Tracker in Mull blockieren möchtest.

Mull verfügt über bereits standardmäßig konfigurierte Einstellungen zum Schutz der Privatsphäre. Du kannst die Option **Browserdaten beim Beenden löschen** in den Einstellungen von Mull konfigurieren, wenn du alle offenen Tabs beim Beenden der App automatisch schließen oder andere Daten wie den Browserverlauf und Cookies automatisch löschen möchtest.

Da in Mull im Vergleich zu den meisten Browsern standardmäßig ein erweiterter und strengerer Schutz der Privatsphäre aktiviert ist, können einige Websites möglicherweise nicht geladen werden oder nicht richtig funktionieren, wenn du diese Einstellungen nicht anpasst. Du kannst diese [Liste mit bekannten Problemen und Umgehungsmöglichkeiten](https://divestos.org/pages/broken#mull) konsultieren, um Ratschläge für eine mögliche Lösung zu erhalten, wenn du auf eine fehlerhafte Website stoßt. Wenn du eine Einstellung änderst, um eine Website zu reparieren, kann sich dies auf deine Privatsphäre/Sicherheit auswirken. Vergewisser dich daher, dass du alle Anweisungen, die du befolgst, vollständig verstehst.

## Safari (iOS)

Unter iOS [muss](https://developer.apple.com/app-store/review/guidelines) jede App, auf welcher man im Web surfen kann, das [WebKit-Framework](https://developer.apple.com/documentation/webkit) von Apple zu verwenden. Es gibt deshalb wenig Gründe, den Browser eines Drittanbieters zu verwenden.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** ist der Standard-Browser in iOS. Es umfasst [Datenschutzfunktionen](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) wie [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Datenschutzbericht, isolierte und ephemere Private-Browsing-Tabs, Maßnahmen gegen Fingerprinting (indem Websites eine vereinfachte Version der Systemkonfiguration angezeigt wird, sodass mehrere Geräte identisch aussehen) und Private Relay für Nutzer:innen mit einem kostenpflichtigen iCloud+-Abonnement. Außerdem kannst du dein Browsing mit verschiedenen Profilen trennen und private Tabs mit deinen biometrischen Daten/PIN sperren.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Datenschutz" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Dokumentation}

</details>

</div>

### Empfohlene Safari-Konfiguration

Wir empfehlen die Installation von [AdGuard](browser-extensions.md#adguard) als Inhaltsblocker, wenn du Tracker in Safari blockieren möchtest.

Die folgenden datenschutz- und sicherheitsrelevanten Optionen findest du in der App :gear: **Einstellungen** → **Safari**

#### Profile

Alle deine Cookies, dein Verlauf und deine Website-Daten werden für jedes Profil separat gespeichert. Du solltest verschiedene Profile für verschiedene Zwecke verwenden, z. B. Einkaufen, Arbeit oder Schule.

#### Datenschutz & Sicherheit

- [x] Aktivieren Sie **Cross-Sitetracking verhindern**

    Dies ermöglicht WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). Die Funktion schützt vor unerwünschtem Tracking, indem sie maschinelles Lernen auf dem Gerät nutzt, um Tracker zu stoppen. Der verbesserte Schutz vor Aktivitätenverfolgung schützt vor vielen gängigen Bedrohungen, aber er blockiert nicht alle Tracking-Möglichkeiten, da er so konzipiert ist, dass die Benutzung der Webseite nicht oder nur minimal beeinträchtigt wird.

- [x] Aktiviere **Face ID zum Entsperren von „Privates Surfen“ anfordern**

    Mit dieser Einstellung kannst du deine privaten Tabs bei Nichtgebrauch mit Biometrie/PIN sperren.

#### Erweitert → Datenschutz

Bei der Einstellung **Erweiterter Tracking- und Identifizierungsschutz** werden bestimmte Werte zufällig ausgewählt, sodass es schwieriger ist, deine Fingerabdrücke zu erkennen:

- [x] Wähle **Beim Surfen immer** oder **Privates Surfen**

#### Datenschutzbericht

Der Datenschutzbericht bietet eine Momentaufnahme der Cross-Site-Tracker, die derzeit daran gehindert werden, auf der von Ihnen besuchten Website ein Profil zu erstellen. Es kann auch einen wöchentlichen Bericht anzeigen, aus dem hervorgeht, welche Tracker im Laufe der Zeit blockiert wurden.

Der Datenschutzbericht ist über das Menü "Website-Einstellungen" zugänglich.

#### Datenschutzkonforme Werbemessung

- [ ] Deaktiviere **Datenschutzwahrende Werbungsmessung**

Bei der Messung von Anzeigenklicks werden traditionell Tracking-Technologien eingesetzt, die die Privatsphäre der Nutzer verletzen. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) ist eine WebKit-Funktion und ein vorgeschlagener Webstandard, der es Werbetreibenden ermöglichen soll, die Effektivität von Web-Kampagnen zu messen, ohne die Privatsphäre von Nutzern zu gefährden.

Die Funktion hat an sich wenig Datenschutzbedenken. Du kannst sie zwar aktiviert lassen, aber die Tatsache, dass sie beim Privaten Surfen automatisch deaktiviert wird, ist unserer Meinung nach ein Indikator für die Deaktivierung der Funktion.

#### Always-on Private Browsing

Öffne Safari und tippe unten rechts auf die Schaltfläche "Tabs". Erweiter dann die Liste der Tabgruppen.

- [x] Wähle **Privat**

Der Modus "Privates Surfen" von Safari bietet zusätzlichen Schutz für die Privatsphäre. Private Browsing verwendet eine neue [kurzlebige](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) Sitzung für jedn Tab, was bedeutet, dass die Tabs voneinander isoliert sind. Private Browsing bietet noch weitere kleinere Vorteile für den Datenschutz, z. B. wird die Adresse einer Webseite nicht an Apple gesendet, wenn die Übersetzungsfunktion von Safari verwendet wird.

Beachte, dass Private Browsing keine Cookies und Website-Daten speichert, sodass es nicht möglich ist, auf Websites angemeldet zu bleiben. Dies kann zu Unannehmlichkeiten führen.

#### iCloud Sync

Die Synchronisierung von Safari-Verlauf, Tab-Gruppen, iCloud-Tabs und gespeicherten Kennwörtern erfolgt über E2EE. Allerdings werden Lesezeichen standardmäßig [nicht](https://support.apple.com/HT202303) verschlüsselt. Apple kann sie entschlüsseln und in Übereinstimmung mit der [Datenschutzrichtlinie](https://apple.com/legal/privacy/en-ww) darauf zugreifen.

Du kannst E2EE für deine Safari-Lesezeichen und Downloads aktivieren, indem du [Erweiterten Datenschutz](https://support.apple.com/de-de/108756) aktivierst. Gehe zu deinem **Apple ID-Namen → iCloud → Erweiterter Datenschutz**.

- [x] Wähle **Erweiterten Datenschutz aktivieren**

Wenn du iCloud mit deaktiviertem erweitertem Datenschutz verwendest, empfehlen wir auch zu überprüfen, ob der Standard-Ladeort von Safari auf deinem Gerät lokal eingestellt ist. Diese Option ist zu finden unter :gear: **Einstellungen** → **Safari** → **Allgemein** → **Downloads**.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Unterstützt automatische Updates.
- Muss Engine-Updates von Upstream-Releases schnell erhalten.
- Inhaltsperre muss unterstützt werden.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
