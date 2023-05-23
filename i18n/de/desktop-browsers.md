---
meta_title: "Datenschutzfreundliche Webbrowser für PC und Mac - Privacy Guides"
title: "Desktop Browser"
icon: material/laptop
description: Diese Webbrowser bieten einen stärkeren Schutz der Privatsphäre als Google Chrome.
cover: desktop-browsers.png
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

!!! recommendation

    ![Mullvad-Browser-Logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** ist eine Version des [Tor Browsers](tor.md#tor-browser), bei der die Tor-Netzwerk-Integration entfernt wurde, um VPN-Nutzern die Anti-Fingerprinting-Technologien vom Tor Browser zur Verfügung zu stellen. Es wird vom Tor-Projekt entwickelt, von [Mullvad](vpn.md#mullvad) vertrieben, erfordert aber **nicht** die Verwendung von Mullvads VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Dokumentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title=Quellcode }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/de/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/de/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/de/download/browser/linux)

Wie der [Tor Browser](tor.md) ist Mullvad Browser so konzipiert, dass er Fingerprinting verhindert, indem er deinen Browser-Fingerabdruck mit dem aller anderen Mullvad Browser-Benutzer identisch macht. Außerdem wird er mit Starndard-Einstellungen und -Erweiterungen ausgeliefert, die automatisch an die drei vorkonfigurierten Sicherheitsstufen angepasst werden: *Standard*, *Sicherer* und *Am Sichersten*. Daher ist es zwingend erforderlich, dass Sie den Browser in keiner Weise verändern, abgesehen von der Anpassung der [Standard-Sicherheitsstufen](https://tb-manual.torproject.org/security-settings/). Andere Änderungen würden Ihren Fingerabdruck einzigartig machen und damit den Zweck dieses Browsers zunichtemachen. Wenn du deinen Browser stärker konfigurieren möchtest und Fingerprinting für dich kein Thema ist, empfehlen wir stattdessen [Firefox](#firefox).

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

!!! recommendation

    ![Firefox-Logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** bietet starke Datenschutzeinstellungen wie [Enhanced Tracking Protection](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop), mit denen verschiedene [Arten von Tracking](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop#w_welche-elemente-blockiert-der-verbesserte-schutz-vor-aktivitatenverfolgung) blockiert werden können.
    
    [:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/de/privacy/firefox/){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Dokumentation }
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title=Quelltext }
    [:octicons-heart-16:](https://www.mozilla.org/de/contribute/){ .card-link title=Mitwirken }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/de/firefox/windows/)
        - [:simple-apple: macOS](https://www.mozilla.org/de/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/de/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
 Firefox enthält ein eindeutiges [Download-Token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in Downloads von der Mozilla-Website und verwendet Telemetrie in Firefox, um das Token zu senden. Das Token ist **nicht** in den Downloads von [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) enthalten.

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

[Firefox Suggest](https://support.mozilla.org/de/kb/anpassung-der-einstellungen-von-firefox-suggest) ist eine Funktion, die den Suchvorschlägen ähnelt und nur in den USA verfügbar ist. Wir empfehlen das Deaktivieren aus demselben Grund, aus dem wir die Deaktivierung von Suchvorschlägen empfehlen. Wenn du diese Optionen im Abschnitt **Adressleiste** nicht siehst, ist dieses neue Feature bei dir noch nicht verfügbar, du kannst die beschriebenen Änderungen also ignorieren.

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

Zusätzlich sammelt der Firefox-Konten-Dienst [einige technische Daten](https://www.mozilla.org/de/privacy/firefox/#firefox-konten). Wenn du ein Firefox-Konto verwendest, kannst du dich abmelden:

1. Öffnen deine [Profileinstellungen auf accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deaktiviere **Datenerfassung und -nutzung** > **Helfen Sie, Firefox-Konten zu verbessern**

##### Nur-HTTPS-Modus

- [x] Wähle **Nur-HTTPS-Modus in allen Fenstern aktivieren**

Dadurch wird verhindert, dass ungewollt eine Verbindung zu einer Website mit einer unverschlüsselten HTTP-Verbindung hergestellt wird. Websites ohne HTTPS sind heutzutage unüblich, sodass dies nur geringe oder gar keine Auswirkungen auf das tägliche Surfen haben sollte.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt dich mit E2EE.

### Arkenfox (fortgeschritten)

!!! tip "Nutze Mullvad Browser für fortgeschrittenes Anti-Fingerprinting"

    [Mullvad Browser](#mullvad-browser) bietet den gleichen Schutz vor Fingerabdrücken wie Arkenfox und erfordert nicht die Verwendung von Mullvads VPN, um von diesem Schutz zu profitieren. In Verbindung mit einem VPN kann Mullvad Browser fortschrittlichere Tracking-Skripte verhindern, was Arkenfox nicht kann. Arkenfox hat immer noch den Vorteil, dass es viel flexibler ist und Ausnahmen für einzelne Websites zulässt, bei denen du angemeldet bleiben musst.

Das [Arkenfox-Projekt](https://github.com/arkenfox/user.js) bietet eine Reihe von sorgfältig durchdachten Optionen für Firefox. Wenn du dich [für Arkenfox entscheidest](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not), sind einige [Optionen](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) subjektiv streng und/oder können dazu führen, dass einige Websites nicht richtig funktionieren - diese kannst du deinen Bedürfnissen entsprechend [ändern](https://github.com/arkenfox/user.js/wiki/3.1-Overrides). Wir **empfehlen nachdrücklich** das vollständige [Wiki](https://github.com/arkenfox/user.js/wiki) zu lesen. Arkenfox ermöglicht auch die Unterstützung von [Containern](https://support.mozilla.org/de/kb/firefox-tab-container).

Arkenfox zielt nur darauf ab, einfache oder naive Tracking-Skripte durch Canvas-Randomisierung und die in Firefox integrierten Konfigurationseinstellungen für Fingerabdruck-Resistenz zu vereiteln. Er zielt nicht darauf ab, deinen Browser mit einer großen Menge anderer Arkenfox-Benutzer zu verschmelzen, wie es der Mullvad-Browser oder der Tor-Browser tun, was die einzige Möglichkeit ist, fortgeschrittene Skripte zur Verfolgung von Fingerabdrücken zu vereiteln. Denke daran, dass du immer noch mehrere Browser verwenden kannst. Du könntest z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen du eingeloggt bleiben möchtest, oder denen du vertraust, und Mullvad Browser für das allgemeine Surfen.

## Brave

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
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Wir raten davon ab, die Flatpak-Version von Brave zu verwenden, da sie die Sandbox von Chromium durch die von Flatpak ersetzt, welche weniger effektiv ist. Außerdem wird das Paket nicht von Brave Software, Inc. betreut.

### Empfohlene Konfiguration

Diese Optionen sind unter :material-menu: → **Einstellungen** zu finden.

#### Einstellungen

##### Shields

Brave bietet einige Anti-Fingerprinting-Maßnamen in seinem [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-)-Feature. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) für alle Seiten, die du besuchst, zu konfigurieren.

Die Optionen von Shields können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

    ??? warning "Use default filter lists"
        Brave allows you to select additional content filters within the internal `brave://adblock` page. Wir raten davon ab, diese Funktion zu verwenden; behalte stattdessen die Standard-Filterlisten bei. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab und kann auch die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer der von dir verwendeten Listen hinzugefügt wird.

- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting

</div>

1. Diese Option bietet eine ähnliche Funktionalität wie die erweiterten Blockierungsmodi von uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) oder die Erweiterung [NoScript](https://noscript.net/).

##### Social media blocking

- [ ] Deaktiviere alle Social Media Komponenten

##### Privacy and security

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [x] Select **Always use secure connections** in the **Security** menu
- [ ] Uncheck **Private window with Tor** (1)

    !!! tip "Sanitizing on Close"

        - [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

        If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

1. Brave ist **nicht** so resistent gegen Fingerabdrücke wie der Tor-Browser. Außerdem nutzen viel weniger Leute Brave zusammen mit Tor, du wirst also auffallen. Wenn [starke Anonymität erforderlich ist](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-), verwende den [Tor Browser](tor.md#tor-browser).

##### Erweiterungen

Deaktiviere die integrierten Erweiterungen, die du nicht verwendest, unter **Erweiterungen**

- [ ] Deaktiviere **Hangouts**
- [ ] Deaktiviere **WebTorrents**

##### Web3

Die Web3-Funktionen von Brave können deinen Browser-Fingerabdruck und deine Angriffsfläche potenziell vergrößern. Wenn du keine der Funktionen verwendest, sollten sie deaktiviert werden.

Set **Default Ethereum wallet** to **Extensions (no fallback)** Set **Default Solana wallet** to **Extensions (no fallback)** Set **Method to resolve IPFS resources** to **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. Diese Option ist nicht auf allen Plattformen verfügbar.

#### Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt dich mit E2EE.

#### Brave Rewards und Wallet

Durch **Brave Rewards** erhälst du Basic Attention Token (BAT) Kryptowährung für die Durchführung bestimmter Aktionen in Brave. Es basiert auf einem Account und KYC von einer ausgewählten Anzahl von Anbietern. Wir empfehlen BAT nicht als [private Kryptowährung](cryptocurrency.md), und wir empfehlen auch nicht die Verwendung einer [depotgeführten Geldbörse](advanced/payments.md#other-coins-bitcoin-ethereum-etc). Wir raten also von dieser Funktion ab.

**Brave Wallet** arbeitet lokal auf Ihrem Computer, unterstützt aber keine privaten Kryptowährungen, weshalb wir auch von dieser Funktion abraten würden.

## Zusätzliche Ressourcen

Generell raten wir dir, möglichst wenig Erweiterungen zu verwenden; diese haben weitreichenden Zugriff auf deinen Browser, verlangen dein Vertrauen in den Entwickler, können dich [hervorheben](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint) und die Seiten-Isolierung [schwächen](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ). uBlock Origin kann sich jedoch als nützlich erweisen, wenn du Wert auf die Funktion zum Blockieren von Inhalten legst.

### uBlock Origin

!!! recommendation

    ![uBlock Origin-Logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** ist ein beliebter Inhaltsblocker, der Werbung, Tracker und Fingerabdruck-Skripte blockieren kann.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title=Datenschutzrichtlinie }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Dokumentation }
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title=Quelltext }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Wir empfehlen, der [Dokumentation des Entwicklers](https://github.com/gorhill/uBlock/wiki/Blocking-mode) zu folgen und einen der "Modi" auszuwählen. Zusätzliche Filterlisten können die Leistung beeinträchtigen und [können die Angriffsfläche vergrößern](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Weitere Listen

Dies sind einige andere [Filterlisten](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists), die du vielleicht hinzufügen möchtest:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

!!! example "Dieser Abschnitt ist neu"

    Wir arbeiten aktuell daran, Kriterien für jeden Bereich unserer Webseite festzulegen. Dieser Abschnitt kann sich deshalb noch ändern. Bei Fragen zu unseren Kriterien, können diese [in unserem Forum] (https://discuss.privacyguides.net/latest) gestellt werden. Und gehen nicht davon aus, dass wir etwas bei unseren Empfehlungen nicht berücksichtigt haben, wenn es hier nicht aufgeführt ist. Es gibt viele Faktoren, die berücksichtigt und besprochen werden, wenn wir ein Projekt empfehlen, und die Dokumentation jedes einzelnen Faktors ist ein laufender Prozess.

### Mindestanforderungen

- Es muss sich um Open-Source Software handeln.
- Unterstützt automatische Updates.
- Erhält Engine-Updates in 0-1 Tagen nach der Upstream-Veröffentlichung.
- Verfügbar für Linux, macOS und Windows.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, sollten die Benutzerfreundlichkeit nicht beeinträchtigen.
- Blockiert standardmäßig Cookies von Drittanbietern.
- Unterstützt [State Partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) um Cross-Site Tracking abzuschwächen.[^1]

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Funktionen, aber diejenigen, die sie enthalten, werden auf dieser Seite möglicherweise höher eingestuft als jene, die sie nicht enthalten.

- Enthält eine integrierte Funktion zum Sperren von Inhalten.
- Unterstützt die Aufteilung von Cookies (à la [Multi-Account Containers](https://support.mozilla.org/de/kb/firefox-tab-container)).
- Unterstützt Progressive Web Apps.  
  Mit PWAs kannst du bestimmte Websites so installieren, als wären sie native Anwendungen auf deinem Computer. Dies kann Vorteile gegenüber der Installation von Electron-basierten Anwendungen haben, da Sie von den regelmäßigen Sicherheitsupdates Ihres Browsers profitieren.
- Enthält keine Zusatzfunktionen (Bloatware), die die Privatsphäre der Benutzer nicht beeinträchtigen.
- Erfasst standardmäßig keine Telemetrie.
- Bietet eine Open-Source-Implementierung des Sync-Servers.
- Standardmäßig wird eine [private Suchmaschine](search-engines.md) verwendet.

### Weitere Kriterien

- Darf keine eingebauten Browser- oder Betriebssystemfunktionen replizieren.
- Muss sich direkt auf die Privatsphäre der Nutzer auswirken, d. h. es dürfen nicht einfach nur Informationen geliefert werden.

[^1]: Die Implementierung von Brave ist unter [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
