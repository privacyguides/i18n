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

Wenn du anonym im Internet surfen möchtest, solltest du stattdessen [Tor](tor.md) verwenden. Wir geben einige Konfigurationsempfehlungen, aber bei allen anderen Browsern als Tor wirst du von *irgendjemandem* auf die eine oder andere Weise zurückverfolgt werden können.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** ist eine Version des [Tor Browsers](tor.md#tor--browser), bei der die Tor-Netzwerk-Integrationen entfernt wurden. Es zielt darauf ab, VPN-Nutzern die Anti-Fingerprinting-Browsertechnologien des Tor-Browsers zur Verfügung zu stellen, die ein wichtiger Schutz gegen [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }sind. Es wird vom Tor-Projekt entwickelt, von [Mullvad](vpn.md#mullvad) vertrieben und erfordert **nicht** die Verwendung von Mullvad's VPN.

[:octicons-home-16: Homepage](https://mullvad.net/de/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/de/help/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://mullvad.net/de/help/tag/mullvad-browser){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/de/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/de/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/de/download/browser/linux)

</details>

</div>

Wie der [Tor Browser](tor.md) ist auch der Mullvad Browser so konzipiert, dass der Fingerabdruck Ihres Browsers mit dem aller anderen Mullvad Browser-Benutzer identisch ist (Anti-Fingerprinting). Dies beinhaltet die Standardeinstellungen und -erweiterungen, die automatisch durch die Standard-Sicherheitsstufen konfiguriert werden können: *Standard*, *Sicherer* und *Am Sichersten*. Daher ist es zwingend erforderlich, dass du den Browser in keiner Weise modifizierst, abgesehen von der Anpassung der [Standard-Sicherheitsstufen](https://tb-manual.torproject.org/security-settings). Andere Änderungen würden Ihren Fingerabdruck einzigartig machen und damit den Zweck dieses Browsers zunichtemachen. Wenn du deinen Browser stärker konfigurieren möchtest und Fingerprinting für dich kein Thema ist, empfehlen wir stattdessen [Firefox](#firefox).

### Anti-Fingerprinting

Der Mullvad Browser bietet **ohne** [VPN](vpn.md) den gleichen Schutz gegen [naive Fingerabdruckskripte](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) wie Firefox+[Arkenfox](#arkenfox-advanced), [Brave](#brave) oder andere private Browser. Er bietet diesen Schutz von Haus aus, allerdings auf Kosten einer gewissen Flexibilität und Bequemlichkeit, die andere private Browser bieten können.

==Für das stärkste Anti-Fingerprinting empfehlen wir die Verwendung des Mullvad Browsers in Verbindung **mit** einem VPN==, sei es Mullvad VPN oder ein anderer empfohlener VPN-Anbieter. Wenn du einen VPN mit Mullvad Browser verwendest, teilst du einen Fingerabdruck und einen Pool von IP-Adressen mit vielen anderen Nutzern, sodass du in einer "Masse" verschwindest. Diese Strategie ist die einzige Möglichkeit, fortgeschrittene Tracking-Skripte zu vereiteln, und ist die gleiche Anti-Fingerprinting-Technik, die auch der Tor-Browser verwendet.

Beachten Sie, dass Sie den Mullvad Browser zwar mit jedem VPN-Anbieter verwenden können, dass aber auch andere Personen den Mullvad Browser mit den von Ihnen verwendeten VPN-Anbieter verwenden müssen, damit diese "Masse" vorhanden ist. Dies ist bei Mullvad VPN im Vergleich zu anderen VPN-Anbietern wahrscheinlicher, insbesondere so kurz nach dem Start des Mullvad Browsers. Mullvad Browser verfügt weder über eine eingebaute VPN-Verbindung, noch prüft er vor dem Surfen, ob du einen VPN verwendest; Deine VPN-Verbindung muss separat konfiguriert und verwaltet werden.

Der Mullvad Browser wird mit den vorinstallierten Browsererweiterungen *uBlock Origin* und *NoScript* ausgeliefert. Obwohl wir normalerweise davon abraten, *zusätzliche* [Browser-Erweiterungen](browser-extensions.md) hinzuzufügen, sollten diese beiden Erweiterungen, die mit dem Browser vorinstalliert sind, **nicht** entfernt oder außerhalb ihrer Standardwerte konfiguriert werden, da dies Ihren Browser-Fingerabdruck deutlich von dem anderer Mullvad-Browser-Nutzer unterscheiden würde. Außerdem ist die Mullvad-Browsererweiterung vorinstalliert. Diese *können* Sie bei Bedarf sicher entfernen, ohne Ihren Browser-Fingerabdruck zu beeinträchtigen. Es ist allerdings auch sicher, sie beizubehalten, selbst wenn Sie Mullvad VPN nicht verwenden.

### Privater Browsing-Modus

Der Mullvad Browser arbeitet im permanenten Privaten-Browsing-Modus, d. h. Ihr Verlauf, Ihre Cookies und andere Website-Daten werden jedes Mal gelöscht, wenn der Browser geschlossen wird. Ihre Lesezeichen, Browsereinstellungen und Erweiterungseinstellungen bleiben erhalten.

Dies ist erforderlich, um fortgeschrittene Formen der Nachverfolgung zu verhindern, geht aber auf Kosten der Bequemlichkeit und einiger Firefox-Funktionen, wie z. B. Multi-Account Container. Denken Sie daran, dass Sie immer mehrere Browser verwenden können. Sie können z. B. Firefox+Arkenfox für einige Websites verwenden, bei denen Sie eingeloggt bleiben möchten oder wenn diese im Mullvad Browser nicht richtig funktionieren, und Mullvad Browser für das allgemeine Surfen.

### Mullvad Leta

Mullvad Browser kommt mit [**Mullvad Leta**](https://leta.mullvad.net) als Standard-Suchmaschine, die als Proxy für die Suchergebnisse von Google oder Brave fungiert (konfigurierbar auf der Mullvad Leta Homepage).

Wenn du Mullvad VPN-Nutzer bist, besteht ein gewisses Risiko, Dienste wie Mullvad Leta zu nutzen, die von deinem VPN-Provider selbst angeboten werden. Dies liegt daran, dass Mullvad theoretisch Zugriff auf deine wahre IP-Adresse (über ihr VPN) und deine Suchaktivität (via Leta) hat, Informationen, die ein VPN typischerweise trennen soll. Auch wenn Mullvad nur sehr wenige Informationen über seine VPN-Abonnenten oder Leta-Nutzer sammelt, solltest du eine andere [Suchmaschine](search-engines.md) in Betracht ziehen, wenn du dieses Risiko fürchtest.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox-Logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** bietet starke Datenschutzeinstellungen wie [Enhanced Tracking Protection](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop), mit denen verschiedene [Arten von Tracking](https://support.mozilla.org/de/kb/verbesserter-schutz-aktivitatenverfolgung-desktop#w_welche-elemente-blockiert-der-verbesserte-schutz-vor-aktivitatenverfolgung) blockiert werden können.

[:octicons-home-16: Homepage](https://www.mozilla.org/de/firefox/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/de/privacy/firefox/){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.mozilla.org/de/products/firefox){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://foundation.mozilla.org/de/donate/){ .card-link title="Spenden" }

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

Suchvorschläge sind in deiner Region möglicherweise nicht verfügbar.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Firefox Suggest (nur US)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Deaktiviere **Vorschläge von Firefox**
- [ ] Deaktiviere **Vorschläge von Sponsoren**

#### Datenschutz & Sicherheit

##### Verbesserter Schutz vor Aktivitätenverfolgung

- [x] Wählen Sie **Streng** für den verbesserten Schutz vor Aktivitätenverfolgung

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Cookies und Website-Daten

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Wähle **Cookies und Website-Daten beim Beenden von Firefox löschen**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetrie

- [ ] Deaktiviere **Firefox erlauben, Daten zu technischen Details und Interaktionen an Mozilla zu senden**
- [ ] Deaktiviere **Firefox das Installieren und Durchführen von Studien erlauben**
- [ ] Deaktiviere **Nicht gesendete Absturzberichte automatisch von Firefox senden lassen**

According to Mozilla's privacy policy for Firefox,

> Firefox sendet Daten über deine Firefox-Version und -Sprache, das Betriebssystem und die Hardware-Konfiguration deines Geräts, den Arbeitsspeicher, grundlegende Informationen über Abstürze und Fehler sowie die Ergebnisse automatisierter Prozesse wie Updates, Safebrowsing und Aktivierung an Mozilla. Wenn Firefox Daten an Mozilla sendet, wird deine IP-Adresse vorübergehend als Teil von Mozillas Serverprotokollen erfasst.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Öffnen deine [Profileinstellungen auf accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Deaktiviere **Datenerfassung und -nutzung** > **Helfen Sie, Firefox-Konten zu verbessern**

##### Werbeeinstellungen für Websites

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### Nur-HTTPS-Modus

- [x] Wähle **Nur-HTTPS-Modus in allen Fenstern aktivieren**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS über HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Aktiviere **Maximaler Schutz** und wähle einen geeigneten Anbieter

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (fortgeschritten)

<div class="admonition tip" markdown>
<p class="admonition-title">Nutze den Mullvad Browser für fortgeschrittenes Anti-Fingerprinting</p>

[Mullvad Browser](#mullvad-browser) bietet den gleichen Schutz vor Fingerabdrücken wie Arkenfox und erfordert nicht die Verwendung von Mullvads VPN, um von diesem Schutz zu profitieren. In Verbindung mit einem VPN kann Mullvad Browser fortschrittlichere Tracking-Skripte verhindern, was Arkenfox nicht kann. Arkenfox hat immer noch den Vorteil, dass es viel flexibler ist und Ausnahmen für einzelne Websites zulässt, bei denen du angemeldet bleiben musst.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

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

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Die Optionen im Schutz-Menü können je nach Bedarf für jede Website heruntergestuft werden, aber als Standardeinstellung empfehlen wir Folgendes:

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

1. Mit dieser Option wird JavaScript deaktiviert, was bei vielen Websites zu Problemen führt. Um sie wieder nutzbar zu machen, können Sie Ausnahmen für jede einzelne Website festlegen, indem Sie auf das Schild-Symbol in der Adressleiste klicken und diese Einstellung unter *Fortgeschrittene Steuerung* deaktivieren.
2. Wenn Sie bei einer bestimmten Website, die Sie häufig besuchen, angemeldet bleiben möchten, können Sie Ausnahmen für jede einzelne Website festlegen, indem Sie auf das Schild-Symbol in der Adressleiste klicken und diese Einstellung unter *Erweiterte Steuerelemente* deaktivieren.

#### Datenschutz und Sicherheit

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Die Deaktivierung des V8-Optimierungstool verringert deine Angriffsfläche, indem [*einige*](https://grapheneos.social/@GrapheneOS/112708049232710156) Teile der JavaScript-Just-In-Time-Kompilierung (JIT) deaktiviert werden.

<div class="admonition tip" markdown>
<p class="admonition-title">Browserdaten beim Schließen löschen</p>

- [x] Wähle **Websitedaten löschen, die auf deinem Gerät gespeichert wurden, wenn du alle Fenster schließt** unter *Website- und Schutzeinstellungen* → *Inhalte* → *Zusätzliche Inhaltseinstellungen* → *Websitedaten auf dem Gerät*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor-Fenster

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Datenerfassung

- [ ] Deaktiviere **Erlaubt Produktanalyse, die den Datenschutz respektiert (P3A)**
- [ ] Deaktiviere **Ping der täglichen Nutzung automatisch an Brave senden**
- [ ] Deaktiviere **Automatisch Diagnoseberichte senden**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Wähle **Erweiterungen (kein Backup)** unter *Standard-Ethereum-Wallet*
- Wähle **Erweiterungen (kein Backup)** unter *Standard-Solana-Wallet*

#### Erweiterungen

- [ ] Deaktiviere alle integrierten Erweiterungen, die du nicht verwendest

#### Suchmaschine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] **Suchvorschläge anzeigen** deaktivieren

#### System

<div class="annotate" markdown>

- [ ] Deaktiviere **Apps weiter im Hintergrund ausführen, wenn Brave geschlossen wird** um Hintergrundapps zu deaktivieren (1)

</div>

1. Diese Option ist nicht auf allen Plattformen verfügbar.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards und Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Kriterien

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Mindestanforderungen

- Es muss sich um Open-Source Software handeln.
- Unterstützt automatische Updates.
- Erhält Engine-Updates in 0-1 Tagen nach der Upstream-Veröffentlichung.
- Muss unter Linux, macOS und Windows verfügbar sein.
- Alle Änderungen, die erforderlich sind, um den Browser datenschutzfreundlicher zu machen, dürfen die Benutzerfreundlichkeit nicht beeinträchtigen.
- Muss Cookies von Drittanbietern standardmäßig blockieren.
- Muss [State Partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) unterstützen, um Cross-Site-Tracking abzuschwächen.[^1]

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Sollte eine integrierte Funktion zur Sperrung von Inhalten enthalten.
- Sollte die Aufteilung von Cookies unterstützen (à la [Multi-Account Container](https://support.mozilla.org/de/kb/firefox-tab-container)).
- Sollte Progressive Web Apps (PWAs) unterstützen. Mit PWAs kannst du bestimmte Websites so installieren, als wären sie native Anwendungen auf deinem Computer. Dies kann Vorteile gegenüber der Installation von Electron-basierten Anwendungen haben, da PWAs von den regelmäßigen Sicherheitsupdates deines Browsers profitieren.
- Sollte keine Zusatzfunktionen (Bloatware) enthalten, die die Privatsphäre der Nutzer nicht beeinträchtigen.
- Sollte standardmäßig keine Telemetrie erfassen.
- Sollte eine Open-Source-Implementierung des Sync-Servers bereitstellen.
- Sollte standardmäßig eine [private Suchmaschine](search-engines.md) verwenden.

[^1]: Braves Implementierung ist detailliert unter [Brave Privacy Updates: Partitionieren des Netzwerkzustands für Privatsphäre](https://brave.com/privacy-updates/14-partitioning-network-state) beschrieben.
