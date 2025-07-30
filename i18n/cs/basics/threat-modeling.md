---
meta_title: "Threat modeling: První krok na vaší cestě za soukromím - Privacy Guides"
title: "Threat modeling"
icon: 'material/target-account'
description: Vyvážení bezpečnosti, soukromí a použitelnosti je jedna z prvních a nejobtížnějších úloh, kterým musíte čelit v průběhu vaší cesty.
---

Vyvážení bezpečnosti, soukromí a použitelnosti je jedna z prvních a nejobtížnějších úloh, kterým musíte čelit v průběhu vaší cesty. Všechno je o kompromisu: V zásadě platí, že čím bezpečnější něco je, tím více je to restriktivní a nepohodlné. Často lidé zjišťují, že nástroje, které jim jsou doporučené, jsou až příliš těžké na to, aby je začali používat.

Pokud chcete ten **nejbezpečnější** nástroj, který existuje, musíte obětovat *spoustu* užitečnosti. A i tak, ==nic není 100% bezpečné navždy.== Je možné dosáhnout **vysoké** bezpečnosti, ale ne **úplné** bezpečnosti. Proto jsou threat modely důležité.

**Ale, co to vůbec threat modely jsou?**

==Threat model je seznam těch nejpravděpodobnějších hrozeb ve vztahu k vaší bezpečnosti a soukromí.== Vzhledem k tomu, že je nemožné se chránit vůči **každému** útoku nebo útočníkovi, měli byste se soustředit na ty **nejvíce pravděpodobné** hrozby. V oblasti počítačové bezpečnosti je hrozba událost, která by mohla zmařit vaši snahu ochránit si své soukromí a bezpečnost.

Zaměření se na hrozby podstatné pro vás zúží oblast, ve které se potřebujete chránit, abyste si mohli vybrat nástroje, které nejlépe odpovídají vašemu účelu.

## Vytváření vašeho threat modelu

Abyste si mohli ujasnit, co se může stát věcem, na kterých vám záleží, a před kým je musíte chránit, potřebujete si odpovědět na následujících 5 otázek:

1. Co chci chránit?
2. Před kým to chci chránit?
3. Jak moc je pravděpodobné, že to budu potřebovat chránit?
4. Jak vážné budou následky, pokud v tom selžu?
5. Kolik úsilí můžu (nebo chci) vynaložit na předejití možným následkům?

### Co chci chránit?

„Majetek“ je něco, čeho si ceníte a chcete to chránit. V kontextu digitální bezpečnosti to znamená, že ==majetek je nějaký typ informace.== Např. vaše e-maily, kontakty, zprávy, poloha atd. jsou vaším potenciálním majetkem. Vaše zařízení samotná mohou být taky majektem.

*Vytvořte si seznam vašeho majetku: data, která uchováváte, kde je uchováváte, kdo k nim má přístup, a co ostatním brání v tom, aby se k nim dostali.*

### Před kým to chci chránit?

Abyste dokázali na tuto otázku odpovědět, je důležité identifikovat, kdo by mohl chtít cílit na vás nebo vaše informace. ==Člověk nebo subjekt, který je hrozbou pro váš majetek, je „útočník“.== Potenciální útočníci mohou být např. váš šéf, ex-partner(ka), vaši konkurenti, vaše vláda, nebo taky hacker na veřejné síti.

*Udělejte si seznam útočníků, nebo obecně těch, kdo by měl zájem na tom, získat váš majetek. Takový seznam může obsahovat jak jednotlivce, tak i vládní úřady nebo korporace.*

V závislosti na tom, kdo jsou potenciální útočníci, můžete tento seznam zničit po tom, co si ujasníte svůj threat model.

### Jak moc je pravděpodobné, že to budu potřebovat chránit?

==Riziko označuje pravděpodobnost, že k ohrožení majetku některou hrozbou skutečně dojde.== Jde to ruku v ruce se schopnostmi. Zatímco váš mobilní operátor má přístup k veškerým vašim datům, je malé riziko toho, že by je zveřejnil online proto, aby poškodil vaši pověst.

Je důležité rozlišovat mezi tím, co se může stát, a s jakou pravděpodobností se to může stát. Například existuje hrozba, že se zřítí budova, ve které jste, ale takové riziko je mnohem větší v San Francisku (kde jsou zemětřesení běžná) než ve Stockholmu (kde nejsou).

Vyhodnocování rizik je jak osobním, tak i subjektivním procesem. Mnoho lidí považuje některé hrozby za nepřijatelné, bez ohledu na pravděpodobnost, s jakou se mohou stát, protože už jen samotná existence hrozby jim připadá, oproti možným nákladům na odvrácení, jako nepřípustná. V jiných případech ale lidé neberou ohled na vysoká rizika, protože nepovažují možné hrozby za problém, který se jich dotýká.

*Zapište si, které hrozby berete vážně, a které mohou být až moc vzácné nebo neškodné, případně moc náročné na potírání, abyste se jimi zabývali.*

### Jak vážné budou následky, pokud v tom selžu?

Existuje mnoho způsobů, jak se mohou útočníci dostat k vašim datům. Například, útočník může číst vaši soukromou komunikaci, zatímco putuje po síti, nebo mohou vymazat nebo poškodit vaše data.

==Motivy útočnííků se velmi liší, stejně jako jejich postupy.== Vláda se může pokusit omezit šíření videa, které vyobrazuje policejní brutalitu tak, že ho jednoduše smaže nebo omezí jeho dostupnost. Nebo naopak, politický odpůrce by mohl chtít získat přístup k vašemu tajnému obsahu a zveřejnit ho bez vašeho vědomí.

Plánování zabezpečení v sobě zahrnuje pochopení toho, jak špatné mohou být následky, pokud by útočník opravdu získal přístup k některému z vašeho majetku. K tomu je důležité zvážit možnosti a schopnosti útočníka. Váš operátor má například přístup ke všem vašim záznamům o provedených hovorech. Hacker na otevřené Wi-Fi síti může mít přístup k vaší nešifrované komunikaci. A vaše vláda může mít ještě větší možnosti.

*Zapište si, co by mohli útočníci s vašimi soukromými údaji udělat.*

### Kolik úsilí můžu (nebo chci) vynaložit na předejití možným následkům?

==Neexistuje dokonalé zabezpečení.== Ne každý má stejné priority, obavy, nebo přístup k různým zdrojům. Vaše vyhodnocení rizik vám dovolí si zvolit strategii na míru, která bude vyvažovat pohodlí, náklady i soukromí.

Advokát zastupující klienta v otázce národní bezpečnosti může chtít vynaložit více úsilí na to, aby ochránil informace o případu. Může k tomu použít např. šifrovaný e-mail. Jinak ale bude uvažovat matka, která posílá své dceři e-mailem videa s vtipnými kočkami.

*Zapište si, jaké možnosti máte k dispozici, se kterými můžete zmírnit rizika u svých jedinečných hrozeb. Všímejte si, jestli jste omezeni v otázce finančních, technických nebo společenských zdrojů.*

### Zkuste si to: Chraňte svůj majetek

Tyto otázky se mohou vztahovat na širokou škálu situací, a to jak on-line, tak i off-line. Pro názornou ukázku toho, jak s nimi pracovat, si pojďme sestavit plán, který udrží náš dům a majetek v bezpečí.

**Co chcete chránit? (Nebo, *co všechno máte a stojí to za ochranu?*)**
:

Váš majetek může zahrnovat šperky, elektroniku, důležité dokumenty, nebo také fotky.

**Před kým je chcete chránit?**
:

Mezi útočníky se mohou řadit zloději, spolubydlící, nebo návštěvnící.

**Jak moc je pravděpodobné, že to budete potřebovat chránit?**
:

Má vaše sousedství historii vloupání? Jak důvěryhodní jsou vaši spolubydlící nebo hosté? Jaké jsou schopnosti možných útočníků? Která rizika byste měli zohlednit?

**Jak vážné budou následky, pokud selžete?**
:

Máte v domě něco, co je nenahraditelné? Máte čas nebo peníze na to, abyste mohli věci nahradit? Máte sjednané pojištění, které vám ukradené věci pokryje?

**Kolik úsilí jste ochotni vynaložit na to, abyste předešli těmto následkům?**
:

Jste ochotni koupit si trezor, ve kterém budete uchovávat citlivé dokumenty? Můžete si dovolit pořídit kvalitní zámek? Máte čas si zřidit bezpečnostní schránku ve vaší bance, ve které si uložíte vaše cennosti?

Teprve až si odpovíte na tyto otázky, budete moci posoudit, která opatření máte přijmout. Pokud je váš majetek cenný, ale je jen málo pravděpodobné, že by se k vám někdo vloupal, možná nebudete chtít investovat do drahého zámku. Pokud je ale riziko vloupání velké, budete si chtít pořídit ten nejlepší zámek na trhu, a k němu ještě i bezpečnostní systém.

Vytvoření zabezpečovacího plánu vám pomůže ujasnit si hrozby, které jsou relevantní pro vás, a zvážit faktory, jako je váš majetek, možní útočníci, jejich schopnosti, spolu s pravděpodobností rizik, kterým čelíte.

## Přečtěte si také

Sestavili jsme seznam běžných hrozeb pro lidi, kteří chtějí zvýšit svoje soukromí a bezpečnost on-line, kterým naši čtenáři čelí, a také cíle, které mají, abychom vám dodali inspiraci a předvedli vám naše základní doporučení.

- [Běžné cíle a hrozby :material-arrow-right-drop-circle:](common-threats.md)

## Zdroje

- [EFF o sebeobraně proti sledování: Váš bezpečnostní plán (v angličtině)](https://ssd.eff.org/en/module/your-security-plan)
