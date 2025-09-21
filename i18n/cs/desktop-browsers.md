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
<p class="admonition-title">Varování</p>

Firefox k instalačním balíčkům přidává unikátní [token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) při stažení z webu Mozilly a používá Firefox k odeslání tokenu. Token **není** obsažen ve verzích z [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Doporučená konfigurace Firefoxu

Tyto nastavení najdete v :material-menu: → **Nastavení**.

#### Vyhledávání

- [ ] Odškrtněte **Zobrazit návrhy našeptávače**

Funkce návrhů našeptávače nemusí být ve vaší oblasti dostupná.

Návrhy našeptávače odesílají všechno, co napíšete do adresního řádku, výchozímu vyhledávači, bez ohledu na to, jestli požadavek opravdu zadáte. Vypnutí našeptávače vám umožní přesněji kontrolovat, jaká data posíláte svému poskytovateli vyhledávače.

##### Firefox Suggest (pouze pro USA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) je funkce podobná návrhům našeptávače, která je dostupná pouze v USA. Doporučujeme ji vypnout ze stejného důvodu jako našeptávač. Pokud nevidíte tyto možnosti v záhlaví **adresního řádku**, tato funkce se vás netýká a můžete tato nastavení ignorovat.

- [ ] Odškrtněte **Doporučení od Firefoxu**
- [ ] Odšrtněte **Doporučení od sponzorů**

#### Soukromí a zabezpečení

##### Rozšířená ochrana proti sledování

- [x] Vyberte **Přísná**

Toto nastavení vás chrání před trackery od sociálních sítí, fingerprinting skripty (pamatujte ale, že vás neochrání před *veškerým* sledováním na základě otisků), kryptominery, sledovacími cookies napříč weby a dalšími trackery. Ochrání vás před mnoha běžnými hrozbami, ale neochrání vás před všemi možnostmi sledování, protože je navržené tak, aby mělo minimální, nebo i žádný, dopad na použitelnost stránek.

##### Vymazání při ukončení

Pokud chcete zůstat přihlášení na určitých stránkách, můžete jim udělit výjimku v **Cookies a data stránek** → **Výjimky…**

- [x] Zaškrtněte **Vymazat cookies a data stránek při zavření aplikace Firefox**

Toto nastavení vás ochrání před trvalými cookies, ale neochrání vás před cookies, které získáte během jakékoliv jedné relace. Pokud je toto nastavení povolené, můžete jednoduše vyčistit vaše cookies v prohlížeči tím, že jednoduše restartujete Firefox. Taky si můžete nastavit výjimky pro každou stránku zvlášť, pokud si přejete být přihlášení na určité stránce, kterou často navštěvujete.

##### Telemetrie

- [ ] Odšrtněte **Odesílat technická data a data o interakcích organizaci Mozilla**
- [ ] Odškrtněte **Instalovat a spouštět studie**
- [ ] Odškrtněte **Automaticky odesílat hlášení o pádech**

Prohlášení o ochraně osobních údajů pro Firefox uvádí:

> Firefox nám odesílá data o vaší verzi a jazyku Firefoxu, operačním systému a hardwarové konfiguraci zařízení, paměti, základní informace o pádech a chybách, výsledcích automatizovaných procesů, jako jsou aktualizace, bezpečném prohlížení a aktivaci. Když nám Firefox posílá data, vaše IP adresa je dočasně zaznamenána jako součást našich serverových logů.

Služba Mozilla Accounts navíc shromažďuje [některé technické údaje](https://mozilla.org/privacy/mozilla-accounts). Pokud používáte Mozilla Account, můžete se odhlásit tímto postupem:

1. Otevřete svoje [nastavení profilu na „account.firefox.com“](https://accounts.firefox.com/settings#data-collection)
2. Odškrtněte **Sběr dat a jejich použití** > **Povolte ⁨účtu Mozilla⁩ zasílat ⁨Mozille⁩ technická data a data o interakcích.**

##### Reklamní předvolby webových stránek

- [ ] Odškrtněte **Umožnit webům použití sledující reklamy, která je šetrná k soukromí**

S vydáním Firefoxu 128 bylo přidáno nové nastavení pro „privacy-preserving attribution“ (PPA), které je v základu povolené. PPA dovolují inzerentům používat váš prohlížeč pro měření efektivity webových kampaní namísto toho, aby používali původní sledování pomocí JavaScriptu. Vnímáme toto chování jako mimo rámec toho, co by měl prohlížeč dělat, a skutečnost, že v Arkenfoxu je toto nastavení předem zakázané, je dalším důvodem pro zakázání této funkce.

##### Režim „pouze HTTPS“

- [x] Zaškrtněte **Zapnout režim „pouze HTTPS“ ve všech oknech**

Toto nastavení zabraňuje, abyste se nechtěně připojili k webové stránce pomocí nešifrovaného HTTP. Stránky nepodporující HTTPS nejsou v dnešní době obvyklé, takže by toto nastavení mělo mít negativní vliv na vaše každodenní prohlížení.

##### DNS over HTTPS

Pokud používáte [DNS over HTTPS poskytovatele](dns.md):

- [x] Vyberte **Maximální ochrana** a zvolte vhodného poskytovatele

Maximální ochrana vynucuje používání DNS over HTTPS. Pokud se Firefox nebude moct úspěšně připojit k zabezpečenému DNS resolveru nebo pokud resolver vrátí, že záznamy pro doménu, ke které se chcete připojit, neexistují, zobrazí se bezpečnostní varování. To zabrání síti, ke které jste připojení, aby na pozadí snížila bezpečnost DNS.

#### Synchronizace

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) vám umožňuje synchronizovat vaše data o prohlížení (historie, záložky apod.) na všech vašich zařízeních a chránit je pomocí E2EE.

### Arkenfox (pro pokročilé)

<div class="admonition tip" markdown>
<p class="admonition-title">Používejte Mullvad Browser pro pokročilou ochranu proti otiskům</p>

[Mullvad Browser](#mullvad-browser) poskytuje stejné ochrany proti otiskům jako Arkenfox v základě, ale nevyžaduje používání Mullvad VPN, abyste mohli této ochrany využívat. Ve spojení s VPN umí Mullvad Browser sabotovat pokročilejší sledovací skripty, které Arkenfox sabotovat nedokáže. Arkenfox má také výhodu mnohem větší flexibility a umožňuje výjimky pro jednotlivé stránky, kde potřebujete zůstat přihlášení.

</div>

[Projekt Arkenfox](https://github.com/arkenfox/user.js) nabízí sadu pečlivě zvážených funkcí Firefoxu. Pokud se [rozhodnete](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) Arkenfox používat, [několik nastavení](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) může být subjektivně moc přísných anebo mohou způsobit, že webové stránky nebudou fungovat správně – můžete je ale [jednoduše upravit](https://github.com/arkenfox/user.js/wiki/3.1-Overrides), aby vyhovovaly vašim potřebám. **Velmi doporučujeme**, abyste si prošli celou jejich [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox také umožňuje podporu [kontejnerů](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox se zaměřuje pouze na zabránění běžným nebo naivním sledovacím skriptům skrz randomizaci canvasu nebo skrz vestavěnou konfiguraci odolnosti proti otiskům. Jeho cílem není, aby váš prohlížeč splynul s velkým davem ostatních uživatelů Arkenfoxu tak, jako to dělá Mullvad Browser nebo Tor Browser, což je jediný způsob, jak sabotovat pokročilé skripty založené na sledování otisků. Nezapomeňte, že vždy můžete používat více prohlížečů. Můžete například zvážit používání Firefoxu + Arkenfoxu pro pár stránek, kde chcete být přihlášení nebo jim věříte, a Mullvad Browser pro běžné prohlížení.

## Brave

<div class="admonition recommendation annotate" markdown>

![logo Brave](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** obsahuje vestavěný blokátor obsahu a [funkce pro ochranu soukromí](https://brave.com/privacy-features), z nichž mnohé jsou předem povolené.

Brave je postavený na prohlížeči Chromium, takže by vám měl připadat známý a měli byste s ním mít minimální problémy s kompatibilitou.

[:octicons-home-16: Domovská stránka](https://brave.com/cs/){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion/cs/){ .card-link title="Onion odkaz" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Zásady ochrany osobních údajů" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Dokumentace" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Zdrojový kód" }

<details class="downloads" markdown>
<summary>Ke stažení</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Varování</p>

Brave přidává „[referral kód](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)“ k názvům souborů, které stáhnete z webu Brave, který umožňuje vysledovat, odkud byl prohlížeč stáhnutý, např. `BRV002` v souboru s názvem `Brave-Browser-BRV002.pkg`. Instalátor poté pingne Brave server s tímto referral kódem na konci instalace. Pokud ale máte obavy, můžete soubor přejmenovat předtím, než instalátor otevřete.

</div>

### Doporučená konfigurace Braveu

Tyto nastavení najdete v :material-menu: → **Nastavení**.

#### Štíty

Brave implementuje některá opatření proti zanechávání otisku ve své funkci [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Doporučujeme tyto možnosti konfigurovat [globálně](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) napříč všemi stránkami, které navštěvujete.

Nastavení štítů můžete pro jednotlivé weby podle potřeby snížit, ale obecně doporučujeme nastavit následující:

<div class="annotate" markdown>

- [x] U *Blokování sledování & reklam* vyberte **Agresivní**

<details class="warning" markdown>
<summary>Používejte výchozí filtr seznamy</summary>

Brave vám umožňuje přidávat další filtry obsahu v rámci stránky `brave://adblock`. Nedoporučujeme tuto funkci používat; místo toho používejte přednastavené filtr seznamy. Používání dalších seznamů vás odliší od ostatních uživatelů Brave a také může zvýšit plochu útoku, pokud Brave obsahuje exploit a někdo přidá škodlivé pravidlo do jednoho ze seznamů, které používáte.

</details>

- [x] U *Upgradovat spojení k HTTPS* vyberte **Striktní**
- [x] (Volitelně) Zaškrtněte **Blokovat skripty** (1)
- [x] Zaškrtněte **Blokovat otisky prstů**
- [x] Vyberte **Blokovat soubory cookie třetích stran**
- [x] Zaškrtněte **Když zavřu tuto stránku, zapomeňte na mě.** (2)
- [ ] Odškrtněte všechny komponenty sociálních médií

</div>

1. Tato možnost zakáže Javascript, což znefunkční spoustu stránek. Pro jejich znovuzprovoznění jim můžete přidělit výjimku kliknutím na ikonku Štíty ve vyhledávacím poli a odškrtnutím tohoto nastavení v *Pokročilé nastavení*.
2. Pokud chcete zůstat přihlášení k určité stránce, kterou často navštěvujete, můžete u jednotlivých webů nastavit výjimku kliknutím na ikonku Štíty ve vyhledávacím poli a odškrtnutím tohoto nastavení v *Pokročilé nastavení*.

#### Ochrana soukromí a zabezpečení

<div class="annotate" markdown>

- [x] V *Zabezpečení* → *Spravovat zabezpečení modulu V8* vyberte **Nepovolovat webům používat optimalizátor V8** (1)
- [x] V *Nastavení webů a štítů* vyberte **Automaticky odebírat oprávnění nepoužívaným webům**
- [x] V [*Pravidla WebRTC pro zacházení s IP*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc) vyberte **Deaktivujte službu UDP bez proxy**
- [ ] Odškrtněte **Použít pro oznámení služby Google**
- [x] Zaškrtněte **Automaticky přesměrovávat AMP stránky**
- [x] Zaškrtněte **Automaticky přesměrovat sledovací adresy URL**
- [x] Zaškrtněte **Zakázat stránkám, aby získávaly můj otisk prstu na základě mých jazykových preferencí**

</div>

1. Zakázáním optimalizátoru V8 snížíte plochu pro útoky zakázáním [*některých*](https://grapheneos.social/@GrapheneOS/112708049232710156) částí JavaScriptové Just-In-Time (JIT) kompilace.

##### Okna Tor

[**Soukromé okno přes Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) vám umožňuje směrovat v anonymních oknech vaši aktivitu skrze síť Tor a přistupovat k .onion službám, což může být v některých případech užitečné. Brave ale **není** stejně odolný proti zanechávání otisků jako Tor Browser, a Brave s Torem používá mnohem méně lidí, takže budete vyčnívat. Pokud váš threat model vyžaduje silnou anonymitu, používejte [Tor Browser](tor.md#tor-browser).

##### Shromažďování dat

- [ ] Odškrtněte **Umožnit analýzu produktů se zachováním soukromí (P3A)**
- [ ] Odškrtněte **Automatické odesílání denního pingu do služby Brave**
- [ ] Odškrtněte **Automaticky odesílat diagnostické zprávy**

#### Web3

Funkce Web3 může potenciálně zvýšit riziko zanechání otisku a zvětšit plochu pro útok. Pokud nepoužíváte žádnou z těchto funkcí, měly by být zakázány.

- V *Základní peněženka Ethereum* vyberte **Rozšíření (bez náhradního řešení)**
- V *Základní peněženka Solana* vyberte **Rozšíření (bez náhradního řešení)**

#### Rozšíření

- [ ] Zakažte všechna vestavěná rozšíření, která nepoužíváte

#### Vyhledávač

Doporučujeme vypnout našeptávač v Brave ze stejného důvodu, jako to doporučujeme ve [Firefox](#search).

- [ ] Odškrtněte **Zlepšit návrhy vyhledávání**

#### Systém

<div class="annotate" markdown>

- [ ] Odškrtněte **Po ukončení prohlížeče Brave nechat aplikace na pozadí spuštěné** pro vypnutí aplikací na pozadí (1)

</div>

1. Tato možnost není k dispozici na všech platformách.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) vám umožňuje synchronizovat vaše data o prohlížení (historie, záložky apod.) na všech zařízeních bez nutnosti mít účet a chrání je pomocí E2EE.

#### Brave Rewards a Wallet

**Brave Rewards** vám umožňuje přijímat kryptoměnu „Basic Attention Token“ (BAT) za provádění určitých činností v Braveu. Závisí na custodiálním účtu a KYC od vybraných poskytovatelů. Nedoporučujeme BAT jako [soukromou kryptoměnu](cryptocurrency.md) ani jako [custodiální peněženku](advanced/payments.md#wallet-custody), takže odrazujeme od používání této funkce.

**Brave Wallet** funguje lokálně na vašem počítači, ale nepodporuje soukromé kryptoměny, takže také nepodoručujeme používání této funkce.

## Kritéria

**Upozorňujeme, že nespolupracujeme s žádným z projektů, které doporučujeme.** Kromě [našich standardních kritérií](about/criteria.md) jsme vypracovali jasný seznam požadavků, který nám umožňuje poskytovat objektivní doporučení. Doporučujeme, abyste se seznámili s tímto seznamem před tím, než se rozhodnete některý z projektů využít, a také provedli vlastní průzkům, abyste se ujistili, že je pro vás ta správná volba.

### Minimální požadavky

- Musí být open-source software.
- Musí podporovat automatické aktualizace.
- Musí dostávat aktualizace enginu ten samý den, nejpozději den po vydání v upstreamu.
- Musí být dostupný na Linux, macOS a Windows.
- Žádná změna nutná k tomu, aby prohlížeč více respektoval soukromí, nesmí negativně ovlivnit uživatelský komfort.
- Musí blokovat cookies třetích stran v základu.
- Musí podporovat [oddělení stavu](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), aby se zmírnilo sledování napříč stránkami.[^1]

### Oceňované funkce

Naše kritéria pro oceňované funkce představují, co bychom chtěli vidět u perfektního projektu v této kategorii. Naše doporučení nemusí obsahovat všechny tyto funkce, ale ty, které je obsahují, mohou být na stránce umístěné výše než ostatní.

- Měly by obsahovat vestavěnou funkci blokování obsahu.
- Měly by podporovat rozdělování cookies (např. [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Měly by podporovat Progresivní Webové Aplikace (PWA). PWA vám umožňují nainstalovat si určité stránky do počítače, jako by to byly nativní aplikace. To může mít výhody oproti instalaci aplikací založených na Electronu, protože PWA využívají pravidelné bezpečnostní aktualizace vašeho prohlížeče.
- Neměly by obsahovat doplňkové funkce (bloatware), které nemají vliv na soukromí uživatele.
- Neměly by ve výchozím nastavení shromažďovat telemetrii.
- Měly by poskytovat open-source implementaci synchronizačního serveru.
- Měly by mít přednastavený [soukromý vyhledávač](search-engines.md).

[^1]: Implementace v Brave je podrobně popsána v [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
