---
meta_title: "Datenschutzfreundliche Webbrowser für PC und Mac - Privacy Guides"
title: "Desktop Browser"
icon: material/laptop
description: Diese datenschutzfreundlichen Browser empfehlen wir derzeit für das normale/nicht anonyme Surfen auf Desktop-Systemen.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Empfehlungen für private Desktop-Browser
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

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Dies sind die von uns derzeit empfohlenen **Desktop-Webbrowser** und Konfigurationen für das normale/nicht anonyme Surfen. Wir empfehlen [Mullvad Browser](#mullvad-browser) wenn du Wert auf starken Datenschutz und Anti-Fingerprinting legst, [Firefox](#firefox) für gelegentliche Internetnutzer, die eine gute Alternative zu Google Chrome suchen, und [Brave](#brave) wenn du Chromium-Browser-Kompatibilität benötigst.

Wenn du anonym im Internet surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden. Auf dieser Seite finden Sie einige Konfigurationsempfehlungen, aber beachten Sie bitte, dass alle anderen Browser als der Tor Browser von *Dritten* auf die eine oder andere Weise zurückverfolgt werden können.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** ist eine Version des [Tor Browsers](tor.md#tor--browser), bei der die Tor-Netzwerk-Integrationen entfernt wurden. Es zielt darauf ab, VPN-Nutzern die Anti-Fingerprinting-Browsertechnologien des Tor-Browsers zur Verfügung zu stellen, die ein wichtiger Schutz gegen [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }sind. Es wird vom Tor-Projekt entwickelt und von [Mullvad](vpn.md#mullvad) vertrieben und erfordert **nicht** die Verwendung des Mullvad VPN.

[:octicons-home-16: Homepage](https://mullvad.net/de/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/de/help/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://mullvad.net/de/help/tag/mullvad-browser){ .card-link title=Dokumentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/de/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/de/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/de/download/browser/linux)

</details>

</div>

Wie der [Tor Browser](tor.md) ist auch der Mullvad Browser so konzipiert, dass der Fingerabdruck Ihres Browsers mit dem aller anderen Mullvad Browser-Benutzer identisch ist (Anti-Fingerprinting). Dies beinhaltet die Standardeinstellungen und -erweiterungen, die automatisch durch die Standard-Sicherheitsstufen konfiguriert werden können: *Standard*, *Sicherer* und *Am Sichersten*. Daher ist es zwingend erforderlich, dass Sie den Browser in keiner Weise verändern, abgesehen von der Anpassung der [Standard-Sicherheitsstufen](https://tb-manual.torproject.org/security-settings). Andere Änderungen würden Ihren Fingerabdruck einzigartig machen und damit den Zweck dieses Browsers zunichtemachen. Wenn Sie Ihren Browser stärker konfigurieren möchten und Fingerprinting für Sie keine Rolle spielt, empfehlen wir stattdessen [Firefox](#firefox).

### Anti-Fingerprinting

Der Mullvad Browser bietet **ohne** [VPN](vpn.md) den gleichen Schutz gegen [naive Fingerabdruckskripte](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) wie Firefox+[Arkenfox](#arkenfox-advanced), [Brave](#brave) oder andere private Browser. Er bietet diesen Schutz von Haus aus, allerdings auf Kosten einer gewissen Flexibilität und Bequemlichkeit, die andere private Browser bieten können.

==Für das stärkste Anti-Fingerprinting empfehlen wir die Verwendung des Mullvad Browsers in Verbindung **mit** einem VPN==, sei es Mullvad VPN oder ein anderer empfohlener VPN-Anbieter. Wenn Sie ein VPN mit dem Mullvad Browser verwenden, teilen Sie einen Fingerabdruck und einen Pool von IP-Adressen mit vielen anderen Benutzern und können so von der Anonymität der "Masse" profitieren. Diese Strategie ist die einzige Möglichkeit, fortgeschrittene Tracking-Skripte zu vereiteln, und ist die gleiche Anti-Fingerprinting-Technik, die auch der Tor-Browser verwendet.

Beachten Sie, dass Sie den Mullvad Browser zwar mit jedem VPN-Anbieter verwenden können, dass aber auch andere Personen den Mullvad Browser mit den von Ihnen verwendeten VPN-Anbieter verwenden müssen, damit diese "Masse" vorhanden ist. Dies ist bei Mullvad VPN im Vergleich zu anderen VPN-Anbietern wahrscheinlicher, insbesondere so kurz nach dem Start des Mullvad Browsers. Der Mullvad Browser verfügt weder über eine eingebaute VPN-Verbindung, noch prüft er vor dem Surfen, ob Sie ein VPN verwenden; Ihre VPN-Verbindung muss separat konfiguriert und verwaltet werden.

Der Mullvad Browser wird mit den vorinstallierten Browsererweiterungen *uBlock Origin* und *NoScript* ausgeliefert. Obwohl wir normalerweise davon abraten, *zusätzliche* [Browser-Erweiterungen](browser-extensions.md) hinzuzufügen, sollten diese beiden Erweiterungen, die mit dem Browser vorinstalliert sind, **nicht** entfernt oder außerhalb ihrer Standardwerte konfiguriert werden, da dies Ihren Browser-Fingerabdruck deutlich von dem anderer Mullvad-Browser-Nutzer unterscheiden würde. Außerdem ist die Mullvad-Browsererweiterung vorinstalliert. Diese *können* Sie bei Bedarf sicher entfernen, ohne Ihren Browser-Fingerabdruck zu beeinträchtigen. Es ist allerdings auch sicher, sie beizubehalten, selbst wenn Sie Mullvad VPN nicht verwenden.

### Privater Browsing-Modus

Der Mullvad Browser arbeitet im permanenten Privaten-Browsing-Modus, d. h. Ihr Verlauf, Ihre Cookies und andere Website-Daten werden jedes Mal gelöscht, wenn der Browser geschlossen wird. Ihre Lesezeichen, Browsereinstellungen und Erweiterungseinstellungen bleiben erhalten.

Dies ist erforderlich, um fortgeschrittene Formen der Nachverfolgung zu verhindern, geht aber auf Kosten der Bequemlichkeit und einiger Firefox-Funktionen, wie z. B. Multi-Account Container. Denken Sie daran, dass Sie immer mehrere Browser verwenden können. Sie können z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen Sie eingeloggt bleiben möchten oder wenn diese im Mullvad Browser nicht richtig funktionieren, und Mullvad Browser für das allgemeine Surfen.

### Mullvad Leta

Der Mullvad Browser wird mit DuckDuckGo als Standard [Suchmaschine](search-engines.md) ausgeliefert, aber es ist auch **Mullvad Leta** vorinstalliert, eine Suchmaschine, die ein aktives Mullvad VPN-Abonnement erfordert, um darauf zugreifen zu können. Mullvad Leta greift für die Suche direkt auf die kostenpflichtige API von Google zu, daher ist es auf zahlende Abonnenten beschränkt. Aufgrund dieser Einschränkung ist es für Mullvad jedoch möglich, Suchanfragen über Mullvad Leta mit Mullvad-VPN-Konten in einen Zusammenhang zu setzen. Aus diesem Grund raten wir von der Verwendung von Mullvad Leta ab, auch wenn Mullvad nur sehr wenige Informationen über seine VPN-Abonnenten sammelt.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-Logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** bietet starke Datenschutzeinstellungen wie [Enhanced Tracking Protection](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop), mit denen verschiedene [Arten von Tracking](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop#w_welche-elemente-blockiert-der-verbesserte-schutz-vor-aktivitatenverfolgung) blockiert werden können.

[:octicons-home-16: Homepage](https://www.mozilla.org/de/firefox/browsers/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/de/privacy/websites/){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Dokumentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://foundation.mozilla.org/){ .card-link title=Spenden}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Firefox enthält einen einzigartigen [Download-Token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in Downloads von Mozilla-Website und verwendet Telemetrie in Firefox, um diesen Token zu übermitteln. Dieser Token ist **nicht** in den Veröffentlichungen aus [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/) enthalten.

</div>

### Empfohlene Firefox-Konfiguration

Diese Optionen sind unter :material-menu: → **Einstellungen** zu finden.

#### Suche

- [ ] **Suchvorschläge anzeigen** deaktivieren

Suchvorschläge sind in Ihrer Region möglicherweise nicht verfügbar.

Die Funktion Suchvorschläge schickt alles, was du in die Adressleiste eingibst, an die Standardsuchmaschine, unabhängig davon, ob du die Suche tatsächlich durchführst. Indem du die Suchvorschläge deaktivierst, kannst du präziser kontrollieren, welche Daten an den Suchmaschinenanbieter gesendet werden.

##### Firefox Suggest (nur US)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) ist eine Funktion, die den Suchvorschlägen ähnelt und nur in den USA verfügbar ist. Wir empfehlen das Deaktivieren aus demselben Grund, aus dem wir die Deaktivierung von Suchvorschlägen empfehlen. Wenn du diese Optionen im Abschnitt **Adressleiste** nicht siehst, ist dieses neue Feature bei dir noch nicht verfügbar, du kannst die beschriebenen Änderungen also ignorieren.

- [ ] Deaktiviere **Vorschläge von Firefox**
- [ ] Deaktiviere **Vorschläge von Sponsoren**

#### Datenschutz & Sicherheit

##### Verbesserter Schutz vor Aktivitätenverfolgung

- [x] Wählen Sie **Streng** für den verbesserten Schutz vor Aktivitätenverfolgung

Dies schützt dich, indem Social-Media-Tracker, Fingerprinting-Skripte (beachte, dass es dies kein Schutz vor *allen* Fingerprinting-Methoden bietet), Kryptominer, Cross-Site-Tracking-Cookies und weitere Tracking-Inhalte blockiert werden. Der verbesserte Schutz vor Aktivitätenverfolgung schützt vor vielen gängigen Bedrohungen, aber er blockiert nicht alle Tracking-Möglichkeiten, da er so konzipiert ist, dass die Benutzung der Webseite nicht oder nur minimal beeinträchtigt wird.

##### Cookies und Website-Daten

Wenn du bei bestimmten Webseiten angemeldet bleiben möchtest, kannst du Ausnahmen unter **Cookies und Website-Daten** → **Ausnahmen verwalten...** zulassen.

- [x] Wähle **Cookies und Website-Daten beim Beenden von Firefox löschen**

Dies schützt dich vor dauerhaften Cookies, aber nicht vor Cookies, die während einer einzelnen Browsersitzung gespeichert werden. Wenn diese Funktion aktiviert ist, kannst du deine Browser-Cookies durch einen einfachen Neustart von Firefox löschen. Du kannst Ausnahmen für jede einzelne Website festlegen, wenn du auf einer bestimmten Website, die du häufig besuchst, angemeldet bleiben möchtest.

##### Telemetrie

- [ ] Deaktiviere **Firefox erlauben, Daten zu technischen Details und Interaktionen an Mozilla zu senden**
- [ ] Deaktiviere **Firefox das Installieren und Durchführen von Studien erlauben**
- [ ] Deaktiviere **Nicht gesendete Absturzberichte automatisch von Firefox senden lassen**

> Firefox sendet Daten über deine Firefox-Version und -Sprache, das Betriebssystem und die Hardware-Konfiguration deines Geräts, den Arbeitsspeicher, grundlegende Informationen über Abstürze und Fehler sowie die Ergebnisse automatisierter Prozesse wie Updates, Safebrowsing und Aktivierung an Mozilla. Wenn Firefox Daten an Mozilla sendet, wird deine IP-Adresse vorübergehend als Teil von Mozillas Serverprotokollen erfasst.

Außerdem sammelt der Mozilla-Konten-Dienst [einige technische Daten](https://mozilla.org/privacy/mozilla-accounts). Wenn du ein Mozilla-Konto verwendest, kannst du dich hiervon abmelden:

1. Öffnen deine [Profileinstellungen auf accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deaktiviere **Datenerfassung und -nutzung** > **Helfen Sie, Firefox-Konten zu verbessern**

##### Werbeeinstellungen für Websites

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### Nur-HTTPS-Modus

- [x] Wähle **Nur-HTTPS-Modus in allen Fenstern aktivieren**

Dadurch wird verhindert, dass ungewollt eine Verbindung zu einer Website mit einer unverschlüsselten HTTP-Verbindung hergestellt wird. Websites ohne HTTPS sind heutzutage unüblich, sodass dies nur geringe oder gar keine Auswirkungen auf das tägliche Surfen haben sollte.

##### DNS über HTTPS

Wenn du einen [DNS über HTTPS Anbieter](dns.md) verwendest:

- [x] Aktiviere **Maximaler Schutz** und wähle einen geeigneten Anbieter

Maximaler Schutz erzwingt die Verwendung von DNS über HTTPS, und es wird eine Sicherheitswarnung angezeigt, wenn Firefox keine Verbindung zu deinem sicheren DNS-Resolver herstellen kann oder wenn dein sicherer DNS-Resolver sagt, dass Einträge für die Domain, die du versuchst zu erreichen, nicht existieren. Dadurch wird verhindert, dass das Netzwerk, mit dem du verbunden bist, heimlich deine DNS-Sicherheit herabstuft.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) ermöglicht (End-zu-End-Verschlüsselt) den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten.

### Arkenfox (fortgeschritten)

<div class="admonition tip" markdown>
<p class="admonition-title">Nutze den Mullvad Browser für fortgeschrittenes Anti-Fingerprinting</p>

[Mullvad Browser](#mullvad-browser) bietet den gleichen Schutz vor Fingerabdrücken wie Arkenfox und erfordert nicht die Verwendung von Mullvads VPN, um von diesem Schutz zu profitieren. In Verbindung mit einem VPN kann Mullvad Browser fortschrittlichere Tracking-Skripte verhindern, was Arkenfox nicht kann. Arkenfox hat immer noch den Vorteil, dass es viel flexibler ist und Ausnahmen für einzelne Websites zulässt, bei denen du angemeldet bleiben musst.

</div>

Das [Arkenfox-Projekt](https://github.com/arkenfox/user.js) bietet eine Reihe von sorgfältig durchdachten Optionen für Firefox. Wenn du dich für Arkenfox [entscheidest](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not), sind [einige Optionen](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) subjektiv streng und/oder können dazu führen, dass einige Websites nicht ordnungsgemäß funktionieren. Dies kann jedoch [leicht angepasst](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) werden, um deinen Bedürfnissen zu entsprechen. Wir **empfehlen nachdrücklich** das vollständige [Wiki](https://github.com/arkenfox/user.js/wiki) zu lesen. Arkenfox ermöglicht auch die Unterstützung von [Containern](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox zielt nur darauf ab, einfache oder naive Tracking-Skripte durch Canvas-Randomisierung und die in Firefox integrierten Konfigurationseinstellungen für Fingerabdruck-Resistenz zu vereiteln. Er zielt nicht darauf ab, deinen Browser mit einer großen Menge anderer Arkenfox-Benutzer zu verschmelzen, wie es der Mullvad-Browser oder der Tor-Browser tun, was die einzige Möglichkeit ist, fortgeschrittene Skripte zur Verfolgung von Fingerabdrücken zu vereiteln. Denke daran, dass du immer noch mehrere Browser verwenden kannst. Du könntest z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen du eingeloggt bleiben möchtest, oder denen du vertraust, und Mullvad Browser für das allgemeine Surfen.

## Brave

<div class="admonition recommendation annotate" markdown>

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

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Brave fügt dem Dateinamen bei Downloads von der Brave-Website einen "[Herkunftsnachweis](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" hinzu, der verwendet wird, um festzustellen, von welcher Quelle der Browser heruntergeladen wurde, z. B. `BRV002` in einem Download namens `Brave-Browser-BRV002.pkg`. Der Installer wird dann Braves Server mit dem Empfehlungscode am Ende des Installationsprozesses anpingen. Wenn du darüber besorgt bist, kannst du die Installer-Datei vor dem Öffnen umbenennen.

</div>

### Empfohlene Brave-Konfiguration

Diese Optionen sind unter :material-menu: → **Einstellungen** zu finden.

#### Schutz

Brave enthält einige Anti-Fingerabdruck-Maßnahmen in der [Schutz](https://support.brave.com/hc/articles/360022973471-What-is-Shields)-Funktion. Wir empfehlen, diese Optionen [global](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) für alle Seiten zu konfigurieren.

Die Schutz-Möglichkeiten können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

<div class="annotate" markdown>

- [x] Wähle **Aggressiv** unter *Tracker & Anzeigenblockierung*

<details class="warning" markdown>
<summary>Inhaltsfilter</summary>

Brave ermöglicht die Auswahl zusätzlicher Inhaltsfilter auf der internen Seite `brave://adblock`. Wir raten davon ab, diese Funktion zu verwenden; behalte stattdessen die Standard-Filterlisten bei. Die Verwendung zusätzlicher Listen hebt dich von anderen Brave-Benutzern ab und kann auch die Angriffsfläche vergrößern, wenn es eine Sicherheitslücke in Brave gibt und eine bösartige Regel zu einer der von dir verwendeten Listen hinzugefügt wird.

</details>

- [x] Wähle **Streng** unter *Verbindungen auf HTTPS upgraden*
- [x] (Optional) Wähle **JavaScript blockieren** (1)
- [x] Wähle **Fingerprinting blockieren**
- [x] Wähle **Drittanbieter-Cookies blockieren**
- [x] Wähle **Vergiss mich, wenn ich diese Seite schließe** (2)
- [ ] Deaktiviere alles unter Social-Media-Sperrung

</div>

1. Diese Option bietet ähnliche Funktionen wie die erweiterten [Blockierungsmodi](https://github.com/gorhill/uBlock/wiki/Blocking-mode) von uBlock Origin.
2. Wenn du auf einer bestimmten Website, die du häufig besuchst, eingeloggt bleiben möchtest, kannst du Ausnahmen für die einzelnen Websites festlegen, indem du auf das Schildsymbol in der Adressleiste klickst.

#### Datenschutz und Sicherheit

<div class="annotate" markdown>

- [x] Wähle **Websites dürfen das V8-Optimierungstool nicht verwenden** unter *Sicherheit* → *V8-Sicherheit verwalten* (1)
- [x] Wähle **Berechtigungen für nicht verwendete Websites automatisch entfernen** unter *Website- und Schutzeinstellungen*
- [x] Wähle **Nicht-proxisiertes UDP deaktivieren** unter [WebRTC-IP-Nutzungsrichtlinien](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Deaktiviere **Nutzen Sie Google-Services für Push-Benachrichtigungen**
- [x] Wähle **AMP-Seiten automatisch umleiten**
- [x] Wähle **Tracking-URLs automatisch umleiten**
- [x] Wähle **Verhindern, dass Websites aufgrund meiner Spracheinstellungen Fingerabdrücke von mir erstellen**

</div>

1. Die Deaktivierung des V8-Optimierungstool verringert deine Angriffsfläche, indem [*einige*](https://grapheneos.social/@GrapheneOS/112708049232710156) Teile der JavaScript-Just-In-Time-Kompilierung (JIT) deaktiviert werden.

<div class="admonition tip" markdown>
<p class="admonition-title">Browserdaten beim Schließen löschen</p>

- [x] Wähle **Websitedaten löschen, die auf deinem Gerät gespeichert wurden, wenn du alle Fenster schließt** unter *Website- und Schutzeinstellungen* → *Inhalte* → *Zusätzliche Inhaltseinstellungen* → *Websitedaten auf dem Gerät*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor-Fenster

[**Privates Fenster mit Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) ermöglicht es dir, deinen Datenverkehr durch das Tor-Netzwerk in Inkognito-Fenster zu leiten und auf .onion-Dienste zuzugreifen, was in einigen Fällen nützlich sein kann. Allerdings ist Brave **nicht** so resistent gegen Fingerprinting wie der Tor-Browser und es gibt viel weniger Leute, die Brave zusammen mit Tor benutzen, sodass du auffallen wirst. Wenn dein Bedrohungsmodell starke Anonymität erfordert, benutze den [Tor Browser](tor.md#tor-browser).

##### Datenerfassung

- [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
- [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**
- [ ] Deaktiviere **Automatisch Diagnoseberichte senden**

#### Web3

Die Web3-Funktionen von Brave können deinen Browser-Fingerabdruck und deine Angriffsfläche potenziell vergrößern. Wenn du keine der Funktionen verwendest, sollten sie deaktiviert werden.

- Wähle **Erweiterungen (kein Backup)** unter *Standard-Ethereum-Wallet*
- Wähle **Erweiterungen (kein Backup)** unter *Standard-Solana-Wallet*
- Set *Method to resolve IPFS resources* to **Disabled**

#### Erweiterungen

- [ ] Deaktiviere alle integrierten Erweiterungen, die du nicht verwendest

#### System

<div class="annotate" markdown>

- [ ] Deaktiviere **Apps weiter im Hintergrund ausführen, wenn Brave geschlossen wird** um Hintergrundapps zu deaktivieren (1)

</div>

1. Diese Option ist nicht auf allen Plattformen verfügbar.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) ermöglicht den Zugriff auf deine Browsing-Daten (Verlauf, Lesezeichen usw.) auf all deinen Geräten und schützt diese Daten mit E2EE.

#### Brave Rewards und Wallet

Mit **Brave Rewards** erhältst du Basic Attention Token (BAT), eine Kryptowährung, für die Durchführung bestimmter Aktionen in Brave. Es basiert auf einem Custodial (d. h. von Dritten verwalteten) Account und KYC von einer ausgewählten Anzahl von Anbietern. Wir empfehlen BAT nicht als [private Kryptowährung](cryptocurrency.md), und wir empfehlen auch nicht die Verwendung einer [Custodial-Wallet](advanced/payments.md#wallet-custody). Wir raten also von dieser Funktion ab.

**Brave Wallet** arbeitet lokal auf Ihrem Computer, unterstützt aber keine privaten Kryptowährungen, weshalb wir auch von dieser Funktion abraten würden.

## Zusätzliche Ressourcen

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, verbunden sind.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen, sich mit dieser Liste vertraut zu machen, bevor sich für ein Projekt entschieden wird und eigene Nachforschungen anzustellen, um sicherzustellen, dass es die richtige Wahl ist.

### Mindestanforderungen

- Es muss sich um Open-Source Software handeln.
- Unterstützt automatische Updates.
- Erhält Engine-Updates in 0-1 Tagen nach der Upstream-Veröffentlichung.
- Muss unter Linux, macOS und Windows verfügbar sein.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, dürfen die Benutzerfreundlichkeit nicht beeinträchtigen.
- Muss Cookies von Drittanbietern standardmäßig blockieren.
- Muss [State Partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) unterstützen, um Cross-Site-Tracking abzuschwächen.[^1]

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Funktionen, aber diejenigen, die sie enthalten, werden auf dieser Seite möglicherweise höher eingestuft als jene, die sie nicht enthalten.

- Should include built-in content blocking functionality.
- Sollte die Aufteilung von Cookies unterstützen (à la [Multi-Account Container](https://support.mozilla.org/de/kb/firefox-tab-container)).
- Sollte Progressive Web Apps unterstützen. Mit PWAs kannst du bestimmte Websites so installieren, als wären sie native Anwendungen auf deinem Computer. Dies kann Vorteile gegenüber der Installation von Electron-basierten Anwendungen haben, da PWAs von den regelmäßigen Sicherheitsupdates deines Browsers profitieren.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Sollte standardmäßig keine Telemetrie erfassen.
- Should provide an open-source sync server implementation.
- Sollte standardmäßig eine [private Suchmaschine](search-engines.md) verwenden.

[^1]: Braves Implementierung ist detailliert unter [Brave Privacy Updates: Partitionieren des Netzwerkzustands für Privatsphäre](https://brave.com/privacy-updates/14-partitioning-network-state) beschrieben.
