---
title: "Běžné hrozby"
icon: 'material/eye-outline'
description: Váš threat model je sice unikátní, ale zde jsou vypsané věci, na kterých mnoha našim návštevníkům záleží.
---

Obecně řečeno, dělíme naše doporučení do [hrozeb](threat-modeling.md) nebo cílů, které se týkají většiny lidí. ==Možná se vás netýká ani jedna, možná jen jedna, více z nich, nebo všechny==, a vámi používané nástroje a služby se odvíjejí od toho, jaké jsou vaše cíle. Možná se vás týkají specifické hrozby, které zde nejsou uvedené, a i to je naprosto v pořádku. Důležité je porozumět výhodám a nedostatkům nástrojů, které se rozhodnete používat, protože prakticky žádný vás neochrání před každou hrozbou.

<span class="pg-purple">:material-incognito: **Anonymita**</span>
:

Oddělení vaší online aktivity od reálné identity. Ochrání vás před lidmi, kteří se snaží odhalit konkrétně *vaši* identitu.

<span class="pg-red">:material-target-account: **Cílené útoky**</span>
:

Ochrana proti hackerům a ostatním škodlivým aktérům, kteří se snaží dostat specificky k *vašim* datům nebo zařízením.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain útoky (útoky na dodavatelský řetězec)**</span>
:

Obvykle forma <span class="pg-red">:material-target-account: Cíleného útoku</span>, který spočívá v zavedení zranitelnosti nebo exploitu do jinak legitimního softwaru, ať už napřímo, nebo skrz závislost třetí strany.

<span class="pg-orange">:material-bug-outline: **Pasivní útoky**</span>
:

Ochrana před malwarem, úniky dat a ostatními útoky, který jsou vedené proti více lidem najednou.

<span class="pg-teal">:material-server-network: **Poskytovatelé služeb**</span>
:

Ochrana dat před poskytovali služeb (např. pomocí E2EE, které způsobí, že server nebude schopný data číst).

<span class="pg-blue">:material-eye-outline: **Hromadné sledování**</span>
:

Ochrana před vládními úřady, organizacemi, webovými stránkami a službami, které spolupracují při sledování vaší aktivity.

<span class="pg-brown">:material-account-cash: **Kapitalismus dohledu**</span>
:

Ochrana před velkými reklamními sítěmi, jako je např. Google nebo Meta (Facebook), a spoustě jiných sběračů dat třetích stran.

<span class="pg-green">:material-account-search: **Vystavení veřejnosti**</span>
:

Omezení informací, které jsou o vás dostupné online – ať už vyhledávačům, nebo veřejnosti.

<span class="pg-blue-gray">:material-close-outline: **Cenzura**</span>
:

Vyhýbání se cenzurovanému přístupu k informacím nebo vlivu cenzury při vyjadřování se on-line.

Některé z těchto hrozeb mohou být pro vás důležitější než jiné, v závislosti na vašich konkrétních zájmech. Například, softwarový vývojář s přístupem k cenným nebo kritickým datům se může zajímat převážně o <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain útoky</span> a <span class="pg-red">:material-target-account: cílené útoky</span>. Pravděpodobně ale také budou chtít chránit svá osobní data před tím, aby byly zachyceny pomocí programů pro <span class="pg-blue">:material-eye-outline: hromadné sledování</span>. Mnoho lidí se taky mohou obávat o to, že jejich osobní data budou <span class="pg-green">:material-account-search: vystaveny veřejnosti</span>, ale i tak by se měli mít na pozoru před problémy v rámci bezpečnosti, jako jsou třeba <span class="pg-orange">:material-bug-outline: pasivní útoky</span>, které mohou mít podobu malwaru, který napadl jejich zařízení.

## Anonymita vs soukromí

<span class="pg-purple">:material-incognito: Anonymita</span>

Anonymita se často zaměňuje za soukromí, ale jde o odlišné pojmy. Zatímco soukromí definují rozhodnutí, jak svá data používáte a sdílíte, anonymita je úplné oddělení vaší on-line aktivity od skutečné identity.

Například informátoři a novináři mohou mít mnohem extrémnější threat model, který vyžaduje naprostou anonymitu. Takže nejen že skrývají, co dělají, jaká data mají, a snaží se nepodlehnout útokům škodlivých aktérů nebo vlád, ale zároveň kompletně skrývají, kdo jsou. Často obětují jakékoliv pohodlí, pokud to znamená, že tím ochrání svoji anonymitu, soukromí nebo bezpečnost, protože na tom mohou záviset jejich životy. Většina lidí ale tak daleko zacházet nemusí.

## Bezpečnost a soukromí

<span class="pg-orange">:material-bug-outline: Pasivní útoky</span>

Bezpečnost a soukromí jsou často zaměňovány, protože potřebujete zabezpečení k tomu, abyste dosáhli jakékoliv podoby soukromí: Používání nástrojů – i kdyby respektovaly soukromí už v základě – je zbytečné, pokud mohou být jednoduše zneužité útočníky, kteří později vaše data zveřejní. Nemusí ale vždy platit opak: Ty nejbezpečnější služby na světe *nejsou nutně* soukromé. Nejlepším příkladem je svěření svých dat Googlu, který měl, vzhledem ke své velikosti, jen pár bezpečnostních incidentů, jelikož k zabezpečení své infrastruktury zaměstnává špičkové bezpečnostní experty. Ale i když Google poskytuje velmi bezpečné služby, jen málokdo by řekl o datech v bezplatných spotřebitelských Google službách (Gmail, Youtube apod.), že jsou v soukromí.

Co se týče bezpečnosti aplikací, obvykle nevíme (a často ani nemůžeme vědět), jestli je software, který používáme, škodlivý, nebo jestli se jednoho dne škodlivým stane. Ani s těmi nejdůvěryhodnějšími vývojáři se nepojí žádná záruka, že jejich software neobsahuje vážnou zranitelnost, která by mohla být později zneužita.

Abyste minimalizovali škody, které by *mohl* škodlivý software způsobit, měli byste využívat zabezpečování pomocí rozdělování. To může mít podobu používání různých počítačů pro různé úlohy, používání virtuální strojů pro oddělení různých druhů aplikací, nebo používání bezpečných operačních systémů se silným důrazem na sandboxing aplikací a mandatorní řízení přístupů.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Mobilní operační systémy mají obecně lepší sandboxing aplikací než desktopové operační systému: Aplikace nemohou získat root přístup, ale potřebují oprávnění pro přístup ke zdrojům systému.

Desktopové operační systémy obecně zaostávají za náležitou implementací sandboxingu. ChromeOS má podobné možnosti sandboxingu jako Android a macOS má kompletní systém pro řízení oprávnění (a vývojáři se mohou rozhodnout sandboxing pro své aplikace povolit). Tyto operační systémy ale přenášejí informace použitelné k identifikaci jejich původním výrobcům. Linux má tendenci neposkytovat informace výrobci systému, ale zároveň má slabou ochranu proti exploitům a škodlivým aplikacím. Tohoto problému se dá částečně vyvarovat pomocí specializovaných distribucí, které pracují s virtuálními stroji nebo kontejnery, jako např. [Qubes OS](../desktop.md#qubes-os).

</div>

## Útoky na konkrétní osoby

<span class="pg-red">:material-target-account: Cílené útoky</span>

S cílenými útoky je už problematičtější se vypořádat. Mezi běžné útoky patří poslání škodlivého dokumentu e-mailem, zneužití zranitelností (např. v prohlížeči nebo operačním systému) a fyzické útoky. Pokud se jich obáváte, měli byste využít pokročilejší strategie pro obranu před hrozbami.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

**Webové prohlížeče**, **e-mailoví klienti** a **kancelářské balíky** už z podstaty věci spouští nedůvěryhodný kód, poslaný třetí stranou. Provozování více virtuálních strojů, které oddělují tyto aplikace od vaše hostitelského systému a od sebe navzájem, je jeden ze způsobů, jak můžete snížit šanci úspěšného útoku v případě, že někdo zneužije slabiny v některé z těchto aplikací a následně ohrozí zbytek vašeho systému. Technologie jako Qubes OS nebo Microsoft Defender Application Guard na Windows poskytují jednoduchou možnost, jak na to.

</div>

Pokud se bojíte **fyzických útoků**, měli byste používat operační systém s implementací secure verified bootu, jako např. Android, iOS, macOS nebo [Windows (s TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Měli byste se také ujistit, že jsou vaše disky zašifrované a že váš operační systém používá TPM nebo Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) nebo [Element](https://developers.google.com/android/security/android-ready-se), abyste omezili počet pokusů pro zadání šifrovací passphrase. Taky byste se měli vyvarovat sdílení počítače s lidmi, kterým nevěříte, protože většina desktopových operačních systémů nešifruje data na bázi uživatele.

## Útoky na určité organizace

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain útoky (útoky na dodavatelský řetězec)**</span>

Supply Chain útoky jsou častou formou <span class="pg-red">:material-target-account: cílených útoků</span> na podniky, vlády a aktivisty, i když mohou nakonec ohrozit i širokou veřejnost.

<div class="admonition example" markdown>
<p class="admonition-title">Příklad</p>

Významný příklad tohoto útoku nastal v roce 2017, kdy byl M.E.Doc, populární účetní software na Ukrajině, napadený virem *NotPetya*, který následně napadl ramsonwarem lidi, kteří si tento software stáhli. NotPetya byl ramsonwarový útok, který postihl více než 2000 společností v různých zemích, a byl založen na eploitu *EternalBlue*, který vyvinulo NSA, aby mohlo napadat počítače s Windows prostřednictvím sítě.

</div>

Tento útok lze provést několika způsoby:

1. Přispěvatel nebo zaměstnanec se může nejdříve propracovat na mocnou pozici v rámci projektu nebo organizace, a následně tuto moc zneužít, aby přidal škodlivý kód.
2. Vývojář může být někým donucený, aby přidal škodlivý kód.
3. Jednotlivec nebo skupina si mohou vyhlédnout softwarovou závislost třetí strany (známou také jako knihovna) a infiltrovat ji pomocí dvou metod zmíněných výše, jelikož bude použita vývojáři, kteří na ní staví.

Tyto druhy útoků mohou vyžadovat mnoho času a příprav k tomu, aby byly uskutečněné, a jsou riskantní, protože mohou být odhalené, hlavně co se týče open source projektů, pokud jsou populární a je o ně zájem. Bohužel jsou ale taky jedny z těch nejnebezpečnějších, jelikož je velmi těžké jim zcela zabránit. Doporučujeme čtenářům, aby používali software, který má dobrou pověst, a snažili se snižovat rizika tím, že budou:

1. Používat populární software, který už nějakou dobu existuje. Čím více je o projekt zájem, tím pravděpodobněji někdo zvenčí zaznamená škodlivé změny. Škodlivý aktér bude také muset věnovat více času tomu, aby si získal důvěru komunity pomocí kvalitních příspěvků.
2. Hledat software, který vydává spustitelné soubory s pomocí rozšířených a důvěryhodných platforem, a ne pomocí vlastních pracovních stanic nebo serverů. Některé systémy, jako je např. GitHub Actions, vám dovolí se podívat na build skripty, které běží veřejně kvůli větší důvěryhodnosti. To snižuje pravděpodobnost, že malware na zařízení vývojáře by mohl napadnout jeho balíčky, a zároveň vám dává jistotu, že spustitelné soubory jsou správně vytvořené.
3. Zjišťovat podpisy u jednotlivých commitů a releasů zdrojového kódu, které vytváří auditovatelný záznam o tom, kdo co udělal. Například: Byl škodlivý kód v tomto repozitáři? Který vývojář ho přidal? Byl přidán během build procesu?
4. Kontrolovat, zda zdrojový kód obsahuje smysluplné vzkazy u commitů (např. [convential commits](https://conventionalcommits.org)), které vysvětlují, čeho má každá změna dosáhnout. Jasné vzkazy mohou usnadnit ověřování, auditování a nalézání chyb osobám, které se na projektu nepodílejí.
5. Kontrolovat, kolik přispěvatelů a správců daný program má. Samotný vývojář může být náchylnější k donucení, aby přidal škodlivý kód, nebo k umožnění nežádoucího chování z nedbalosti. To může znamenat, že software vyvinutý "big techem" je pod větším dohledem než samotný vývojář, který se nikomu nezodpovídá.

## Ochrana soukromí před poskytovateli služeb

<span class="pg-teal">:material-server-network: Poskytovatelé služeb</span>

Žijeme ve světe, kde je skoro vše připojené k internetu. Naše „soukromé“ zprávy, e-maily a sociální interakce jsou většinou uložené někde na serveru. Obecně platí, že když někomu pošlete zprávu, je uložena na serveru, a když si ji váš přítel chce přečíst, server mu ji zobrazí.

Problém samozřejmě spočívá v tom, že poskytovatel služby (nebo hacker, který se nabourá do serveru) může vaše zprávy číst kdykoliv a jakkoliv chce, a to niž byste o tom věděli. To platí pro mnoho běžných služeb, jako jsou např. SMS zprávy, Telegram nebo Discord.

Tento problém může naštěstí zmenšit E2EE tím, že šifruje komunikaci mezi vámi a zamýšleným příjemcem, ještě než je odeslána na server. Důvěrnost vašich zpráv je zaručena za předpokladu, že poskytovatel služby nemá přístup k soukromým klíčům ani jedné strany.

<div class="admonition note" markdown>
<p class="admonition-title">Poznámka k šifrování na webu</p>

V praxi se efektivita různých E2EE implementací liší. Aplikace jako je [Signal](../real-time-communication.md#signal) běží přímo na vašem zařízení a každá kopie aplikace je stejná napříč různými instalacemi. Pokud by poskytovatel služby zanesl [zadní vrátka](https://cs.wikipedia.org/wiki/Zadn%C3%AD_vr%C3%A1tka) do jejich aplikace – ve snaze ukrást vaše soukromé klíče – bylo by možné to zjistit pomocí [reverzního inženýrství](https://cs.wikipedia.org/wiki/Reverzn%C3%AD_in%C5%BEen%C3%BDrstv%C3%AD).

Na druhou stranu, webové implementace E2EE, např. u webové aplikace Proton Mail nebo *Web Vault* od Bitwardenu, se spoléhají na server, který dynamicky doručuje JavaScriptový kód prohlížeči, pomocí kterého pracuje s kryptografií. Škodlivý server vás může zacílit a poslat vám škodlivý JavaScriptový kód, který ukradne vaše šifrovací klíče (a bylo by velmi těžké to zaznamenat). Jelikož server může podstrčit různého klienta různým lidem, i kdybyste si útoku všimli, bylo by velmi obtížné dokázat poskytovateli jeho zavinění.

Proto byste měli používat nativní aplikace místo webových klientů, kdykoliv je to možné.

</div>

I v případě E2EE vás ale mohou poskytovatelé služeb profilovat na základě **metadat**, která obvykle chráněná nejsou. A zatímco si poskytovatelé nemohou číst obsah vašich zpráv, pořád se mohou dozvědět citlivé věci, jako s kým si píšete, jak často jim píšete, a kdy jste obvykle aktivní. Ochrana metadat je poměrně neobvyklá, a – pokud je to ve vašem [threat modelu](threat-modeling.md) – měli byste věnovat velkou pozornost technické dokumentaci softwaru, který používáte, abyste zjistili, jestli produkci metadat nějakým způsobem minimalizuje nebo je chrání.

## Programy k hromadnému sledování

<span class="pg-blue">:material-eye-outline: Hromadné sledování</span>

Hromadné sledování je spletitá snaha monitorovat „chování, mnoho činností nebo informace“ celé populace (nebo její podstatné části). [^1] Často se jím označují vládní programy, např. ty, které [v roce 2013 zveřejnil Edward Snowden](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Mohou ho ale provádět i korporace, ať už na popud vládních úřadů nebo z vlastní iniciativy.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

Pokud se chcete dozvědět více o metodách sledování a jak jsou implementovány ve vašem městě, můžete se podívat na [Atlas of Surveillance](https://atlasofsurveillance.org) od [Electronic Frontier Foundation](https://eff.org).

Pokud jste ve Francii, podívejte se na [stránku Technopolice](https://technopolice.fr/villes) zaštiťovanou neziskovou organizací „La Quadrature du Net“.

</div>

Vlády často zdůvodňují používání programů na hromadné sledování bojem proti terorismu nebo prevencí kriminality. Nejčastěji jsou ale využity pro porušování lidských práv a mimo jiné i k nepřiměřenému cílení na menšiny a politické disidenty.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU (Americký svaz pro občanské svobody): <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">Poučení z hlediska soukromí z 9. září: Hromadné sledování není cestou vpřed (anglicky)</a></em></p>

V souvislosti s odhalením vládních programů jako je [PRISM](https://cs.wikipedia.org/wiki/PRISM) a [Upstream (anglicky)](https://en.wikipedia.org/wiki/Upstream_collection) Edwardem Snowdenem se představitelé zpravodajských služeb přiznaly k tomu, že NSA roky tajně shromažďovala záznamy o prakticky každém Američanovi, konkrétně záznamy telefonních hovorů, kdo komu volal, kdy se hovory uskutečnily a jak dlouho trvaly. Pokud tento typ informací NSA každý den shromažďuje, mohou odhalit neuvěřitelně citlivá data o životě lidí a jejich vztazích, např. zda volali faráři, potratové klinice, psychiatrovi nebo na linku pro sebevrahy.

</div>

Navzdory rostoucímu hromadnému sledování v USA vláda zjistila, že programy k hromadnému sledování v souvislosti s oddílem 215 mají „jen malou jedinečnou hodnotu“, co se týče eliminace skutečných zločinů nebo teroristických spiknutí, s tím, že z většiny suplují programy k hromadnému sledování vyvíjené FBI.[^2]

Online můžete být sledováni pomocí níže uvedených metod, ale nejen těch:

- Vaší IP adresy
- Souborů cookies z vašeho prohlížeče
- Údajů, které vkládáte na webové stránky
- Jedinečného otisku vašeho prohlížeče nebo zařízení
- Korelace platebních metod

Pokud se obáváte programů hromadného sledování, můžete využít strategie, jako je např. rozdělení vašich on-line identit, splynutí s ostatními uživateli, a taky, kdekoliv je to možné, jednoduše neposkytujte informace, které by vás mohly identifikovat.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Surveillance Capitalism</span>

> Surveillance capitalism is an economic system centered around the capture and commodification of personal data for the core purpose of profit-making.[^3]

For many people, tracking and surveillance by private corporations is a growing concern. Pervasive ad networks, such as those operated by Google and Facebook, span the internet far beyond just the sites they control, tracking your actions along the way. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## Limiting Public Information

<span class="pg-green">:material-account-search: Public Exposure</span>

The best way to keep your data private is simply not making it public in the first place. Deleting unwanted information you find about yourself online is one of the best first steps you can take to regain your privacy.

- [View our guide on account deletion :material-arrow-right-drop-circle:](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## Avoiding Censorship

<span class="pg-blue-gray">:material-close-outline: Censorship</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../social-networks.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.

You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
