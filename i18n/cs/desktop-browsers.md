---
meta_title: "Webové prohlížeče respektující soukromí pro PC a Mac - Privacy Guides"
title: Prohlížeče pro počítače
icon: material/laptop
description: Momentálně doporučujeme tyto prohlížeče, které respektují soukromí, pro standardní, neanonymní prohlížení na počítačích.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Doporučení soukromých prohlížečů
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
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
    sameAs: https://cs.wikipedia.org/wiki/Firefox
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
    sameAs: https://cs.wikipedia.org/wiki/Brave_(webový%20prohlížeč)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Chrání před těmito hrozbami:</small>

- [:material-account-cash: Kapitalismus dohledu](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Toto jsou naše aktuálně doporučované **webové prohlížeče pro počítače** a konfigurace pro standardní/neanonymní používání. Doporučujeme prohlížeč [Mullvad](#mullvad-browser), pokud vám záleží na silné ochraně soukromí a ochraně proti otisku prohlížeče hned po instalaci, [Firefox](#firefox) pro nenáročné, kteří hledají dobrou alternativu ke Google Chromu a [Brave](#brave), pokud potřebujete kompatibilní Chromium prohlížeč.

Pokud potřebujete procházet internet anonymně, měli byste místo toho použít [Tor](tor.md). Na této stránce uvádíme některá konfigurační doporučení, ale všechny prohlížeče, kromě prohlížeče Tor, budou tak či onak umožňovat, aby vás *někdo* sledoval.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** je verze [Tor Browseru](tor.md#tor-browser) s odstraněnou integrací sítě Tor. Cílem je poskytnout uživatelům VPN ochranu proti otiskům prstů převzatou z Tor Browseru, které jsou klíčovou ochranou proti [:material-eye-outline: masovému sledování](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Je vyvíjený projektem Tor a distribuovaný společností [Mullvad](vpn.md#mullvad), ale **nevyžaduje** používání Mullvad VPN.

[:octicons-home-16: Hlavní stránka](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Ochrana osobních údajů" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Dokumentace" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Zdrojový kód" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Stejně jako [Tor Browser](tor.md) je Mullvad Browser vytvořený tak, aby zabraňoval vytváření jedinečných otisků tím, že otisk vašeho prohlížeče se ztotožňuje s otisky všech ostatních Mullvad Browser uživatelů, včetně výchozích nastavení a rozšíření, které se automaticky konfigurují pomocí výchozích bezpečnostních úrovní: *Standard*, *Safer* and *Safest*.

Proto je nutné, abyste nepřenastavovali prohlížeč mimo už vytvořené [úrovně zabezpečení](https://tb-manual.torproject.org/security-settings). Pokud jste změnili úrovně zabezpečení, **musíte** vždy restartovat prohlížeč předtím, než ho budete znovu používat. V opačném případě se [nastavení zabezpečení nemusí plně projevit](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), což vás dělá více náchylnými na pořízení jedinečných otisků a zranitelnosti, které byste nečekali v závislosti na vámi zvoleném nastavení.

Úpravami mimo tyto nastavení by se váš otisk stal unikátním, a tím se minuly s účelem tohoto prohlížeče. Pokud chcete mít nad konfigurací svého prohlížeče větší kontrolu a zanechávání otisků vám nevadí, doporučujeme místo toho [Firefox](#firefox).

### Ochrana proti otiskům

**Bez** použití [VPN](vpn.md) poskytuje Mullvad Browser stejnou ochranu proti [naivním fingerprinting skriptům](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) jako ostatní prohlížeče zaměřené na soukromí, jako je Firefox + [Arkenfox](#arkenfox-advanced) nebo [Brave](#brave). Mullvad Browser poskytuje tuto ochranu v základu, na úkor určité flexibility a pohodlí, které mohou poskytovat jiné prohlížeče zaměřené na soukromí.

==Pro nejsilnější ochranu proti zanechávání jedinečného otisku doporučujeme používat Mullvad Browser ve spojení **s** VPN==, ať už se jedná o Mullvad nebo o jiného doporučeného VPN poskytovatele. Při používání VPN s Mullvad Browserem sdílíte otisk a skupinu IP adres s mnoha dalšími uživateli, a tím se „ztrácíte v davu“. Tato strategie je jediná, která dokáže odolat pokročilým sledovacím skriptům, a je to stejná strategie, kterou používá Tor Browser.

Mějte na vědomí, že sice můžete používat Mullvad Browser ve spojení s jakýmkoliv VPN poskytovatelem, ale ostatní lidé používající stejnou VPN musí také používat Mullvad Browser, aby se vytvořil „dav“, a ten se pravděpodobněji vytvoří na Mullvad VPN v porovnání s ostatními poskytovateli, zejména takto brzo od uvedení Mullvad Browseru. Mullvad Browser nemá zabudované připojení k VPN a ani nekontroluje před prohlížením, jestli VPN používáte; vaše VPN připojení si musíte nastavit a spravovat mimo prohlízeč.

Mullvad Browser má v základu předinstalovaná rozšíření *uBlock Origin* a *NoScript*. Zatímco obvykle nedoporučujeme přidávat *další* [rozšíření](browser-extensions.md), tyto předinstalovaná rozšíření byste **neměli** odstraňovat nebo měnit jejich nastavení, protože už to odlišuje váš otisk od ostatních uživatelů Mullvad Browseru. Zároveň má v základu i Mullvad Browser Extension, které *můžete* bezpečně odebrat, aniž by to mělo vliv na váš otisk v případě, že to tak chcete, ale zároveň je v pořádku si ho ponechat i v případě, že Mullvad VPN nepoužívate.

### Režim soukromého prohlížení

Mullvad Browser pracuje v režimu soukromého prohlížení nepřetržitě, tzn. že vaše historie, cookies a ostatní data z webových stranek se vymažou vždy, když prohlížeč ukončíte. Vaše záložky, nastavení prohlízeče a rozšíření se ale zachovají.

To je potřeba pro zabránění pokročilým formám sledování, ale jde to na úkor pohodlí a některých funkcí Firefoxu, jako např. Multi-Account Containers. Nezapomeňte, že vždy můžete používat více prohlížečů. Můžete např. zvážit používání Firefoxu + Arkenfoxu pro pár stránek, kde chcete být přihlášeni nebo protože nefungují správně v Mullvad Browseru, a Mullvad Browser pro běžné prohlížení.

### Mullvad Leta

Mullvad Browser má v základu jako výchozí vyhledávač nastavený [**Mullvad Leta**](search-engines.md#mullvad-leta), který funguje jako proxy buď ke Google, nebo Brave vyhledávání (lze nastavit na domovské stránce Mullvad Leta).

Pokud jste uživatelem Mullvad VPN, existuje určité riziko při používání služeb, jako je Mullvad Leta, které nabízí sám poskytovatel VPN. To proto, že Mullvad má teoreticky přístup k vaší pravé IP adrese (skrz VPN) a vaší vyhledávací aktivitě (skrz Leta); a právě k oddělení těchto dvou informací se většinou používá VPN. I přesto, že Mullvad shromažďuje jen minimum informací o svých předplatitelích VPN nebo uživatelích Lety, měli byste zvážit používání jiného [vyhledávače](search-engines.md), pokud toto riziko nemůžete podstoupit.

## Firefox

<div class="admonition recommendation" markdown>

![logo Firefox](assets/img/browsers/firefox.svg){ align=right }

**Firefox** poskytuje mnoho nastavení pro zachování soukromí, např. [rozšířenou ochranu proti sledování](https://support.mozilla.org/cs/kb/rozsirena-ochrana-proti-sledovani-ve-firefoxu-pro-), která může zablokovat různé [typy pokusů o sledování](https://support.mozilla.org/cs/kb/rozsirena-ochrana-proti-sledovani-ve-firefoxu-pro-#w_co-rozsirena-ochrana-proti-sledovani-blokuje).

[:octicons-home-16: Domovská stránka](https://www.firefox.com/cs/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.mozilla.org/cs/privacy/firefox/){ .card-link title="Prohlášení o ochraně osobních údajů" }
[:octicons-info-16:](https://support.mozilla.org/cs/){ .card-link title="Dokumentace" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Zdrojový kód" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Přispějte" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

These options can be found in :material-menu: → **Settings**.

#### Search

- [ ] Uncheck **Show search suggestions**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Uncheck **Suggestions from sponsors**

#### Privacy & Security

##### Enhanced Tracking Protection

- [x] Select **Strict** Enhanced Tracking Protection

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Sanitize on Close

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Check **Delete cookies and site data when Firefox is closed**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Uncheck **Allow Firefox to send technical and interaction data to Mozilla**
- [ ] Uncheck **Allow Firefox to install and run studies**
- [ ] Uncheck **Allow Firefox to send backlogged crash reports on your behalf**

According to Mozilla's privacy policy for Firefox,

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. Open your [profile settings on accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Select **Enable HTTPS-Only Mode in all windows**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS přes HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
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
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

These options can be found in :material-menu: → **Settings**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Uncheck **Show search suggestions**

#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running background apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Must be open-source software.
- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
