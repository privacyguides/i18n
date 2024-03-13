---
meta_title: "Datenschutzfreundliche Webbrowser für PC und Mac - Privacy Guides"
title: "Desktop Browser"
icon: material/laptop
description: Diese Webbrowser bieten einen stärkeren Schutz der Privatsphäre als Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Desktop-Browser Empfehlungen
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/de/browser
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
    sameAs: https://de.wikipedia.org/wiki/Firefox
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
    sameAs: https://de.wikipedia.org/wiki/Brave_(Browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

Dies sind die von uns derzeit empfohlenen Desktop-Browser und Konfigurationen für das normale/nicht anonyme Surfen. Wir empfehlen [Mullvad Browser](#mullvad-browser) wenn du Wert auf starken Datenschutz und Anti-Fingerprinting legst, [Firefox](#firefox) für gelegentliche Internetnutzer, die eine gute Alternative zu Google Chrome suchen, und [Brave](#brave) wenn du Chromium-Browser-Kompatibilität benötigst.

Wenn du anonym im Internet surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden. Wir geben einige Konfigurationsempfehlungen, aber bei allen Browsern außer Tor wirst du von *irgendjemandem* auf die eine oder andere Weise zurückverfolgt werden können.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad-Browser-Logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** ist eine Version des [Tor Browsers](tor.md#tor-browser), bei der die Tor-Netzwerk-Integration entfernt wurde, um VPN-Nutzern die Anti-Fingerprinting-Technologien vom Tor Browser zur Verfügung zu stellen. Es wird vom Tor-Projekt entwickelt, von [Mullvad](vpn.md#mullvad) vertrieben, erfordert aber **nicht** die Verwendung von Mullvads VPN.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Wie der [Tor Browser](tor.md) ist Mullvad Browser so konzipiert, dass er Fingerprinting verhindert, indem er deinen Browser-Fingerabdruck mit dem aller anderen Mullvad Browser-Benutzer identisch macht. Außerdem wird er mit Starndard-Einstellungen und -Erweiterungen ausgeliefert, die automatisch an die drei vorkonfigurierten Sicherheitsstufen angepasst werden: *Standard*, *Sicherer* und *Am Sichersten*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). Andere Änderungen würden Ihren Fingerabdruck einzigartig machen und damit den Zweck dieses Browsers zunichtemachen. Wenn du deinen Browser stärker konfigurieren möchtest und Fingerprinting für dich kein Thema ist, empfehlen wir stattdessen [Firefox](#firefox).

### Anti-Fingerprinting

**Ohne** die Verwendung eines [VPNs](vpn.md) bietet Mullvad Browser den gleichen Schutz gegen [naive Fingerabdruck-Skripte](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) wie andere private Browser wie Firefox+[Arkenfox](#arkenfox-advanced) oder [Brave](#brave). Mullvad Browser bietet diesen Schutz von Haus aus, allerdings auf Kosten einer gewissen Flexibilität und Bequemlichkeit, die andere private Browser bieten können.

==Für den stärksten Schutz vor Fingerprinting empfehlen wir die Verwendung von Mullvad Browser in Verbindung **mit** einem VPN==, sei es Mullvad oder ein anderer empfohlener VPN-Anbieter. Wenn du einen VPN mit Mullvad Browser verwendest, teilst du einen Fingerabdruck und einen Pool von IP-Adressen mit vielen anderen Nutzern, sodass du in einer "Masse" verschwindest. Diese Strategie ist die einzige Möglichkeit, fortgeschrittene Tracking-Skripte zu vereiteln, und ist die gleiche Anti-Fingerprinting-Technik, die auch der Tor-Browser verwendet.

Beachte, dass du den Mullvad Browser zwar mit jedem VPN-Anbieter nutzen kannst, dass aber auch andere Personen in diesem VPN Mullvad Browser nutzen müssen, damit diese "Menge" existiert. Das ist bei Mullvad VPN im Vergleich zu anderen Anbietern allerdings wahrscheinlicher, insbesondere so kurz nach dem Start des Mullvad Browser. Mullvad Browser verfügt weder über eine eingebaute VPN-Verbindung, noch prüft er vor dem Surfen, ob du einen VPN verwendest; Deine VPN-Verbindung muss separat konfiguriert und verwaltet werden.

Mullvad Browser wird mit den vorinstallierten Erweiterungen *uBlock Origin* und *NoScript* geliefert. Während wir normalerweise *zusätzliche* Browser-Erweiterungen [nicht empfehlen](#extensions), sollten diese Erweiterungen, die mit dem Browser vorinstalliert sind, **nicht** entfernt oder außerhalb ihrer Standardwerte konfiguriert werden, da dies deinen Browser-Fingerabdruck deutlich von dem anderer Mullvad-Browser-Nutzer unterscheiden würde. Außerdem ist die Mullvad-Erweiterung vorinstalliert, die sicher entfernt werden *kann*, ohne deinen Browser-Fingerabdruck zu beeinträchtigen. Sie ist aber auch sicher zu behalten, wenn du Mullvad VPN nicht verwendest.

### Privates Browsen

Mullvad Browser arbeitet im permanenten Private-Browsing-Modus, d. h. dein Verlauf, deine Cookies und andere Website-Daten werden jedes Mal gelöscht, wenn der Browser geschlossen wird. Deine Lesezeichen, Browsereinstellungen und Erweiterungseinstellungen bleiben erhalten.

Dies ist erforderlich, um fortgeschrittene Formen der Nachverfolgung zu verhindern, geht aber auf Kosten der Bequemlichkeit und einiger Firefox-Funktionen, wie z. B. Multi-Account Containers. Denke daran, dass du immer noch mehrere Browser verwenden kannst. Du könntest z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen du eingeloggt bleiben möchtest oder die in Mullvad Browser nicht richtig funktionieren, und Mullvad Browser für das allgemeine Surfen.

### Mullvad Leta

Mullvad Browser wird mit DuckDuckGo als Standard [Suchmaschine](search-engines.md)ausgeliefert, es ist aber auch **Mullvad Leta** vorinstalliert, eine Suchmaschine, die ein aktives Mullvad VPN-Abonnement erfordert, um darauf zugreifen zu können. Mullvad Leta nutzt Googles bezahlte Such-API (und ist deshalb ist es auf zahlende Abonnenten beschränkt). Aufgrund dieser Einschränkung ist es für Mullvad möglich, Suchanfragen und Mullvad VPN-Konten zu korrelieren. Aus diesem Grund raten wir von der Verwendung von Mullvad Leta ab, auch wenn Mullvad nur sehr wenige Informationen über seine VPN-Abonnenten sammelt.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-Logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** bietet starke Datenschutzeinstellungen wie [Enhanced Tracking Protection](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop), mit denen verschiedene [Arten von Tracking](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop#w_welche-elemente-blockiert-der-verbesserte-schutz-vor-aktivitatenverfolgung) blockiert werden können.

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://firefox-source-docs.mozilla.org){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases).

</div>

### Empfohlene Konfiguration

Diese Optionen sind zu finden unter :material-menu: → **Einstellungen**

#### Suche

- [ ] **Suchvorschläge anzeigen** deaktivieren

Suchvorschläge sind in Ihrer Region möglicherweise nicht verfügbar.

Die Funktion Suchvorschläge schickt alles, was du in die Adressleiste eingibst, an die Standardsuchmaschine, unabhängig davon, ob du die Suche tatsächlich durchführst. Indem du die Suchvorschläge deaktivierst, kannst du präziser kontrollieren, welche Daten an den Suchmaschinenanbieter gesendet werden.

#### Datenschutz & Sicherheit

##### Verbesserter Schutz vor Aktivitätenverfolgung

- [x] Wählen Sie **Streng** für den verbesserten Schutz vor Aktivitätenverfolgung

Dies schützt dich, indem Social-Media-Tracker, Fingerprinting-Skripte (beachte, dass es dies kein Schutz vor *allen* Fingerprinting-Methoden bietet), Kryptominer, Cross-Site-Tracking-Cookies und weitere Tracking-Inhalte blockiert werden. Der verbesserte Schutz vor Aktivitätenverfolgung schützt vor vielen gängigen Bedrohungen, aber er blockiert nicht alle Tracking-Möglichkeiten, da er so konzipiert ist, dass die Benutzung der Webseite nicht oder nur minimal beeinträchtigt wird.

##### Firefox Suggest (nur US)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Wir empfehlen das Deaktivieren aus demselben Grund, aus dem wir die Deaktivierung von Suchvorschlägen empfehlen. Wenn du diese Optionen im Abschnitt **Adressleiste** nicht siehst, ist dieses neue Feature bei dir noch nicht verfügbar, du kannst die beschriebenen Änderungen also ignorieren.

- [ ] Deaktiviere **Vorschläge aus dem Internet**
- [ ] Deaktiviere **Vorschläge aus dem Internet**

##### Cookies und Website-Daten

Wenn du bei bestimmten Webseiten angemeldet bleiben möchtest, kannst du Ausnahmen unter **Cookies und Website-Daten** → **Ausnahmen verwalten...** zulassen.

- [x] Wähle **Cookies und Website-Daten beim Beenden von Firefox löschen**

Dies schützt dich vor dauerhaften Cookies, aber nicht vor Cookies, die während einer einzelnen Browsersitzung gespeichert werden. Wenn diese Funktion aktiviert ist, kannst du deine Browser-Cookies durch einen einfachen Neustart von Firefox löschen. Du kannst Ausnahmen für jede einzelne Website festlegen, wenn du auf einer bestimmten Website, die du häufig besuchst, angemeldet bleiben möchtest.

##### Telemetrie

- [ ] Deaktiviere **Firefox erlauben, Daten zu technischen Details und Interaktionen an Mozilla zu senden**
- [ ] Deaktiviere **Firefox das Installieren und Durchführen von Studien erlauben**
- [ ] Deaktiviere **Nicht gesendete Absturzberichte automatisch von Firefox senden lassen**

> Firefox sendet Daten über deine Firefox-Version und -Sprache, das Betriebssystem und die Hardware-Konfiguration deines Geräts, den Arbeitsspeicher, grundlegende Informationen über Abstürze und Fehler sowie die Ergebnisse automatisierter Prozesse wie Updates, Safebrowsing und Aktivierung an Mozilla. Wenn Firefox Daten an Mozilla sendet, wird deine IP-Adresse vorübergehend als Teil von Mozillas Serverprotokollen erfasst.

Additionally, the Firefox Accounts service collects [some technical data](https://mozilla.org/privacy/firefox/#firefox-accounts). Wenn du ein Firefox-Konto verwendest, kannst du dich abmelden:

1. Öffnen deine [Profileinstellungen auf accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deaktiviere **Datenerfassung und -nutzung** > **Helfen Sie, Firefox-Konten zu verbessern**

##### Nur-HTTPS-Modus

- [x] Wähle **Nur-HTTPS-Modus in allen Fenstern aktivieren**

Dadurch wird verhindert, dass ungewollt eine Verbindung zu einer Website mit einer unverschlüsselten HTTP-Verbindung hergestellt wird. Websites ohne HTTPS sind heutzutage unüblich, sodass dies nur geringe oder gar keine Auswirkungen auf das tägliche Surfen haben sollte.

##### DNS über HTTPS

Wenn du einen [DNS über HTTPS Anbieter](dns.md) verwendest:

- [x] Aktiviere **Maximaler Schutz** und wähle einen geeigneten Anbieter

Maximaler Schutz erzwingt die Verwendung von DNS über HTTPS, und es wird eine Sicherheitswarnung angezeigt, wenn Firefox keine Verbindung zu deinem sicheren DNS-Resolver herstellen kann oder wenn dein sicherer DNS-Resolver sagt, dass Einträge für die Domain, die du versuchst zu erreichen, nicht existieren. Dadurch wird verhindert, dass das Netzwerk, mit dem du verbunden bist, heimlich deine DNS-Sicherheit herabstuft.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (fortgeschritten)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) bietet den gleichen Schutz vor Fingerabdrücken wie Arkenfox und erfordert nicht die Verwendung von Mullvads VPN, um von diesem Schutz zu profitieren. In Verbindung mit einem VPN kann Mullvad Browser fortschrittlichere Tracking-Skripte verhindern, was Arkenfox nicht kann. Arkenfox hat immer noch den Vorteil, dass es viel flexibler ist und Ausnahmen für einzelne Websites zulässt, bei denen du angemeldet bleiben musst.

</div>

Das [Arkenfox-Projekt](https://github.com/arkenfox/user.js) bietet eine Reihe von sorgfältig durchdachten Optionen für Firefox. Wenn du dich [für Arkenfox entscheidest](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not), sind einige [Optionen](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) subjektiv streng und/oder können dazu führen, dass einige Websites nicht richtig funktionieren - diese kannst du deinen Bedürfnissen entsprechend [ändern](https://github.com/arkenfox/user.js/wiki/3.1-Overrides). Wir **empfehlen nachdrücklich** das vollständige [Wiki](https://github.com/arkenfox/user.js/wiki) zu lesen. Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox zielt nur darauf ab, einfache oder naive Tracking-Skripte durch Canvas-Randomisierung und die in Firefox integrierten Konfigurationseinstellungen für Fingerabdruck-Resistenz zu vereiteln. Er zielt nicht darauf ab, deinen Browser mit einer großen Menge anderer Arkenfox-Benutzer zu verschmelzen, wie es der Mullvad-Browser oder der Tor-Browser tun, was die einzige Möglichkeit ist, fortgeschrittene Skripte zur Verfolgung von Fingerabdrücken zu vereiteln. Denke daran, dass du immer noch mehrere Browser verwenden kannst. Du könntest z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen du eingeloggt bleiben möchtest, oder denen du vertraust, und Mullvad Browser für das allgemeine Surfen.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave basiert auf dem Chromium-Webbrowser-Projekt, sollte sich also vertraut anfühlen und nur minimale Probleme mit der Website-Kompatibilität haben.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux) (1)

</details>

</div>

1. Wir raten davon ab, die Flatpak-Version von Brave zu verwenden, da sie die Sandbox von Chromium durch die von Flatpak ersetzt, welche weniger effektiv ist. Außerdem wird das Paket nicht von Brave Software, Inc. betreut.

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Empfohlene Konfiguration

Diese Optionen sind unter :material-menu: → **Einstellungen** zu finden.

#### Einstellungen

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Die Optionen von Shields können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Wir raten davon ab, diese Funktion zu verwenden; behalte stattdessen die Standard-Filterlisten bei. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab und kann auch die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer der von dir verwendeten Listen hinzugefügt wird.

</details>

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### Privatsphäre und Sicherheit

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave ist **nicht** so resistent gegen Fingerabdrücke wie der Tor-Browser. Außerdem nutzen viel weniger Leute Brave zusammen mit Tor, du wirst also auffallen. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Erweiterungen

Deaktiviere die integrierten Erweiterungen, die du nicht verwendest, unter **Erweiterungen**

- [ ] Deaktiviere **Hangouts**
- [ ] Deaktiviere **WebTorrents**

##### Web3

Die Web3-Funktionen von Brave können deinen Browser-Fingerabdruck und deine Angriffsfläche potenziell vergrößern. Wenn du keine der Funktionen verwendest, sollten sie deaktiviert werden.

- Wählen Sie **Extensions (no fallback)** unter Default Ethereum wallet und Default Solana wallet
- Setze **Method to resolve IPFS resources** auf **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Deaktiviere **Apps weiter im Hintergrund ausführen, wenn Brave geschlossen wird** um Hintergrundapps zu deaktivieren (1)

</div>

1. Diese Option ist nicht auf allen Plattformen verfügbar.

#### Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards und Wallet

Durch **Brave Rewards** erhälst du Basic Attention Token (BAT) Kryptowährung für die Durchführung bestimmter Aktionen in Brave. Es basiert auf einem Account und KYC von einer ausgewählten Anzahl von Anbietern. Wir empfehlen BAT nicht als [private Kryptowährung](cryptocurrency.md), und wir empfehlen auch nicht die Verwendung einer [depotgeführten Geldbörse](advanced/payments.md#other-coins-bitcoin-ethereum-etc). Wir raten also von dieser Funktion ab.

**Brave Wallet** arbeitet lokal auf Ihrem Computer, unterstützt aber keine privaten Kryptowährungen, weshalb wir auch von dieser Funktion abraten würden.

## Zusätzliche Ressourcen

Generell raten wir dir, möglichst wenig Erweiterungen zu verwenden; diese haben weitreichenden Zugriff auf deinen Browser, verlangen dein Vertrauen in den Entwickler, können dich [hervorheben](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) und die Seiten-Isolierung [schwächen](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ). uBlock Origin kann sich jedoch als nützlich erweisen, wenn du Wert auf die Funktion zum Blockieren von Inhalten legst.

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin-Logo](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** ist ein beliebter Inhaltsblocker, der Werbung, Tracker und Fingerabdruck-Skripte blockieren kann.

[:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

Wir empfehlen, der [Dokumentation des Entwicklers](https://github.com/gorhill/uBlock/wiki/Blocking-mode) zu folgen und einen der "Modi" auszuwählen. Zusätzliche Filterlisten können die Leistung beeinträchtigen und [können die Angriffsfläche vergrößern](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

Dies sind einige andere [Filterlisten](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists), die du vielleicht hinzufügen möchtest:

- [x] Wähle **Datenschutz** > **AdGuard URL Tracking Protection**
- Füge das [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt) hinzu

### uBlock Origin Lite

uBlock Origin also has a "Lite" version of their extension, which offers a very limited feature-set compared to the original extension. However, it has a few distinct advantages over its full-fledged sibling, so you may want to consider it if...

- ...you don't want to grant full "read/modify website data" permissions to any extensions (even a trusted one like uBlock Origin)
- ...you want a more resource (memory/CPU) efficient content blocker[^1]
- ...your browser only supports Manifest V3 extensions

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** is a Manifest V3 compatible content blocker. Compared to the original *uBlock Origin*, this extension does not require broad "read/modify data" permissions to function.

[:octicons-repo-16: Repository](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

We only recommend this version of uBlock Origin if you never want to make any changes to your filter lists, because it only supports a few pre-selected lists and offers no additional customization options, including the ability to select elements to block manually. These restrictions are due to limitations in Manifest V3's design.

This version offers three levels of blocking: "Basic" works without requiring any special privileges to view and modify site content, while the "Optimal" and "Complete" levels do require that broad permission, but offer a better filtering experience with additional cosmetic rules and scriptlet injections.

If you set the default filtering mode to "Optimal" or "Complete" the extension will request read/modify access to **all** websites you visit. However, you also have the option to change the setting to "Optimal" or "Complete" on a **per-site** basis by adjusting the slider in the extension's pop-up panel on any given site. When you do so, the extension will request read/modify access to that site only. Therefore, if you want to take advantage of uBlock Origin Lite's "permission-less" configuration, you should probably leave the default setting as "Basic" and only adjust it higher on sites where that level is not adequate.

uBlock Origin Lite only receives block list updates whenever the extension is updated from your browser's extension marketplace, as opposed to on demand. This means that you may miss out on new threats being blocked for weeks until a full extension release is published.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Wir arbeiten aktuell daran, Kriterien für jeden Bereich unserer Webseite festzulegen. Dieser Abschnitt kann sich deshalb noch ändern. Bei Fragen zu unseren Kriterien, können diese [in unserem Forum] (https://discuss.privacyguides.net/latest) gestellt werden. Und gehen nicht davon aus, dass wir etwas bei unseren Empfehlungen nicht berücksichtigt haben, wenn es hier nicht aufgeführt ist. Es gibt viele Faktoren, die berücksichtigt und besprochen werden, wenn wir ein Projekt empfehlen, und die Dokumentation jedes einzelnen Faktors ist ein laufender Prozess.

</div>

### Mindestanforderungen

- Es muss sich um Open-Source Software handeln.
- Unterstützt automatische Updates.
- Erhält Engine-Updates in 0-1 Tagen nach der Upstream-Veröffentlichung.
- Verfügbar für Linux, macOS und Windows.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
- Blockiert standardmäßig Cookies von Drittanbietern.
- Supports [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^2]

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Funktionen, aber diejenigen, die sie enthalten, werden auf dieser Seite möglicherweise höher eingestuft als jene, die sie nicht enthalten.

- Enthält eine integrierte Funktion zum Sperren von Inhalten.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Supports Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. Dies kann Vorteile gegenüber der Installation von Electron-basierten Anwendungen haben, da Sie von den regelmäßigen Sicherheitsupdates Ihres Browsers profitieren.
- Enthält keine Zusatzfunktionen (Bloatware), die die Privatsphäre der Benutzer nicht beeinträchtigen.
- Erfasst standardmäßig keine Telemetrie.
- Bietet eine Open-Source-Implementierung des Sync-Servers.
- Standardmäßig wird eine [private Suchmaschine](search-engines.md) verwendet.

### Weitere Kriterien

- Darf keine eingebauten Browser- oder Betriebssystemfunktionen replizieren.
- Muss sich direkt auf die Privatsphäre der Nutzer auswirken, d. h. es dürfen nicht einfach nur Informationen geliefert werden.

[^1]: uBlock Origin Lite *itself* will consume no resources, because it uses newer APIs which make the browser process the filter lists natively, instead of running JavaScript code within the extension to handle the filtering. However, this resource advantage is only [theoretical](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo), because it's possible that standard uBlock Origin's filtering code is more efficient than your browser's native filtering code. This has not yet been benchmarked.
[^2]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
