---
meta_title: "Jak VPN chroni Twoją prywatność? Nasz przegląd VPN – Privacy Guides"
title: Przegląd VPN
icon: material/vpn
description: Wirtualne sieci prywatne przenoszą ryzyko z dostawcy usług internetowych na podmiot trzeci, któremu ufasz. Należy mieć to na uwadze.
---

Wirtualne sieci prywatne to sposób na „przedłużenie” końca Twojej sieci tak, by punkt wyjścia znajdował się w innym miejscu na świecie.

[:material-movie-open-play-outline: Film: Czy potrzebujesz VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

Zwykle dostawca usług internetowych może zobaczyć przepływ ruchu internetowego przychodzącego i wychodzącego z urządzenia końcowego sieci (tj. modemu). Protokoły szyfrujące, takie jak HTTPS, są powszechnie stosowane w Internecie, więc dostawca może nie widzieć dokładnie tego, co publikujesz lub czytasz, ale może mieć pojęcie o [domenach, do których kierujesz zapytania](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Korzystanie z VPN ukrywa nawet te informacje przed dostawcą, przenosząc zaufanie, które pokładasz w swojej sieci, na serwer zlokalizowany gdzie indziej na świecie. W efekcie ISP widzi jedynie, że jesteś połączony z VPN, ale nie ma dostępu do informacji o aktywności przesyłanej przez to połączenie.

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Gdy na tej stronie mówimy o „wirtualnych sieciach prywatnych”, zwykle mamy na myśli **komercyjnych** [dostawców VPN](../vpn.md), za których korzystanie płaci się miesięczną opłatę w zamian za kierowanie ruchu internetowego przez ich publiczne serwery. Istnieje jednak wiele innych form VPN — na przykład takie, które hostujesz samodzielnie, albo te obsługiwane przez pracodawców umożliwiające bezpieczne łączenie się z zasobami sieci wewnętrznej — jednak te rozwiązania zwykle są projektowane z myślą o bezpiecznym dostępie do zdalnych sieci, a nie o ochronie prywatności połączenia z Internetem.

</div>

## Jak działa VPN?

VPN szyfruje ruch między urządzeniem a serwerem należącym do dostawcy VPN. Z perspektywy każdego, kto znajduje się między Tobą a serwerem VPN, wygląda to tak, jakbyś łączył(a) się z serwerem VPN. Z perspektywy każdego, kto znajduje się między serwerem VPN a stroną docelową, widoczne jest jedynie połączenie serwera VPN ze stroną.

``` mermaid
flowchart LR
 763931["Twoje urządzenie<div>(z klientem VPN)</div>"] ===|"Szyfrowanie VPN"| 404512{"Serwer VPN"}
 404512 -.-|"Brak szyfrowania VPN"| 593753(("Internet<div>(Twoje miejsce docelowe)</div>"))
 subgraph 763931["Twoje urządzenie<div>(z klientem VPN)</div>"]
 end
```

Zwróć uwagę, że VPN nie dodaje żadnego zabezpieczenia ani szyfrowania do ruchu pomiędzy serwerem VPN a stroną docelową w sieci. Aby bezpiecznie korzystać ze strony, **musisz** nadal upewnić się, że używany jest protokół HTTPS, niezależnie od tego, czy korzystasz z VPN.

## Czy warto korzystać z VPN?

**Tak**, prawie na pewno. VPN ma wiele zalet, w tym:

1. Ukrywanie ruchu **tylko** przed dostawcą usług internetowych.
1. Ukrywanie pobieranych plików (np. torrentów) przed ISP i organizacjami antypirackimi.
1. Ukrywanie Twojego adresu IP przed stronami i usługami zewnętrznymi, co pomaga wtopić się w tłum i utrudnia śledzenie oparte na adresie IP.
1. Umożliwianie omijania ograniczeń geograficznych dla niektórych treści.

VPN-y mogą zapewnić *niektóre* z tych samych korzyści, co Tor — na przykład ukrywanie adresu IP przed odwiedzanymi stronami i geograficzne przesunięcie ruchu sieciowego — a dobrzy dostawcy VPN nie będą współpracować z np. organami represyjnych reżimów, szczególnie jeśli wybierzesz dostawcę spoza własnej jurysdykcji.

VPN nie szyfruje danych poza połączeniem między Twoim urządzeniem a serwerem VPN. Dostawcy VPN mogą również widzieć i modyfikować Twój ruch w taki sam sposób, jak mógłby to robić ISP, więc wciąż pokładasz w nich pewien poziom zaufania. Nie ma też sposobu, by w jakikolwiek sposób zweryfikować politykę „braku logów” dostawcy VPN.

## Kiedy VPN nie jest odpowiedni?

Korzystanie z VPN w sytuacjach, gdy działasz w sieci pod swoją [prawdziwą lub powszechnie znaną tożsamością,](common-misconceptions.md#complicated-is-better) raczej nie przyniesie żadnych korzyści. Może to uruchomić systemy wykrywania spamu i oszustw, na przykład przy logowaniu do strony internetowej banku.

Ważne jest, by pamiętać, że VPN nie zapewnia absolutnej anonimowości, ponieważ sam dostawca VPN nadal ma dostęp do Twojego rzeczywistego adresu IP, informacji o odwiedzanych stronach oraz często do śladu płatności, który można bezpośrednio powiązać z Tobą. Polityka „braku logów” to jedynie obietnica; jeśli zależy Ci na całkowitym bezpieczeństwie w sieci, rozważ korzystanie z [sieci Tor](../advanced/tor-overview.md) jako uzupełnienie lub zamiennik VPN.

Nie należy też polegać na VPN w kwestii zabezpieczenia połączenia z niezaszyfrowaną stroną HTTP. Aby to, co faktycznie robisz na odwiedzanych stronach, pozostało prywatne i bezpieczne, musisz używać HTTPS. Dzięki temu hasła, tokeny sesji i zapytania będą chronione przed dostawcą VPN oraz innymi potencjalnymi przeciwnikami znajdującymi się pomiędzy serwerem VPN a celem. W swojej przeglądarce warto włączyć tryb używania wyłącznie protokołu HTTPS (jeśli jest dostępny), aby ograniczyć ataki polegające na obniżaniu połączenia z HTTPS do HTTP.

## Czy warto używać szyfrowanego DNS z VPN?

O ile dostawca VPN nie prowadzi samodzielnie szyfrowanych serwerów DNS, **prawdopodobnie nie**. Korzystanie z DOH/DOT (lub innej formy szyfrowanego DNS) przy użyciu serwerów stron trzecich tylko zwiększa liczbę podmiotów, którym trzeba ufać. Twój dostawca VPN nadal może widzieć, które strony odwiedzasz, na podstawie adresów IP i innych metod. Mimo to mogą istnieć pewne korzyści z włączenia szyfrowanego DNS, np. aby umożliwić inne funkcje bezpieczeństwa w przeglądarce, takie jak ECH. Technologie przeglądarek opierające się na szyfrowanym DNS po stronie przeglądarki są stosunkowo nowe i jeszcze niezbyt rozpowszechnione, więc to, w jakim stopniu są dla Ciebie istotne, pozostawiamy do samodzielnego zbadania.

Innym częstym powodem, dla którego zalecane jest szyfrowane DNS, jest ochrona przed podszywaniem się pod DNS (DNS spoofing). Jednak przeglądarka powinna już sprawdzać [certyfikaty TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) przy użyciu **HTTPS** i ostrzegać o problemach. Jeśli nie korzystasz z **HTTPS**, przeciwnik może zmodyfikować wszystko poza zapytaniami DNS i wynik będzie niewiele się różnił.

## Czy warto używać sieci Tor *oraz* VPN?

Być może. Tor sam w sobie nie zawsze jest odpowiedni dla każdego. Warto przeanalizować swój [model zagrożeń](threat-modeling.md), ponieważ jeśli przeciwnik nie ma możliwości uzyskania danych od Twojego dostawcy VPN, sam VPN może zapewnić wystarczającą ochronę.

Jeśli jednak decydujesz się korzystać z sieci Tor, to *prawdopodobnie* najlepszym wyborem będzie łączenie się z nią za pośrednictwem komercyjnego dostawcy VPN. Jest to jednak złożony temat, dlatego opisaliśmy go dokładniej na stronie poświęconej [przeglądowi sieci Tor](../advanced/tor-overview.md).

## Czy powinno się korzystać z funkcji dostawców VPN, którzy udostępniają „węzły Tor”?

Nie należy korzystać z tej funkcji. Główna zaleta sieci Tor polega na tym, że nie trzeba ufać dostawcy VPN — a ta przewaga znika, gdy korzystasz z węzłów Tor hostowanych przez tego samego dostawcę, zamiast łączyć się z Torem bezpośrednio z własnego komputera.

Obecnie Tor obsługuje tylko protokół TCP. UDP (używany przez [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) i inne protokoły), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) oraz inne pakiety będą porzucane. Aby to obejść, dostawcy VPN zazwyczaj kierują cały ruch inny niż TCP przez swój serwer VPN (pierwszy przeskok). Tak działa to m.in. w przypadku [ProtonVPN](https://protonvpn.com/support/tor-vpn). Co więcej, w konfiguracji „Tor poprzez VPN” nie masz kontroli nad innymi kluczowymi funkcjami Tora, takimi jak [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (oddzielny obwód Tor dla każdej odwiedzanej domeny).

Tę funkcję można traktować wyłącznie jako *wygodny* sposób dostępu do usług .onion w sieci Tor, a nie jako metodę na zachowanie anonimowości. Aby osiągnąć prawdziwą anonimowość, korzystaj z właściwej [przeglądarki sieci Tor](../tor.md).

## Własność komercyjnych VPN

Większość usług VPN należy w rzeczywistości do tych samych [kilku firm](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). Te budzące wątpliwości podmioty prowadzą wiele mniejszych usług VPN, aby stworzyć iluzję większego wyboru i maksymalizować zyski. Zwykle usługi te, działające pod parasolem firm-wydmuszek, mają fatalne polityki prywatności i nie powinny być obdarzane zaufaniem w kwestii Twojego ruchu internetowego. W wyborze dostawcy należy być wyjątkowo rygorystycznym.

Warto też wiedzieć, że wiele stron z recenzjami VPN to głównie narzędzia marketingowe dla tego, kto zapłaci najwięcej. ==Privacy Guides nie zarabia na polecaniu zewnętrznych produktów i nigdy nie korzysta z programów partnerskich.==

[Zalecane przez nas usługi VPN](../vpn.md ""){.md-button}

## Nowoczesne alternatywy dla VPN

W ostatnim czasie różne organizacje podjęły próby rozwiązania niektórych problemów, które mają scentralizowane VPN-y. Technologie te są stosunkowo nowe, ale warto śledzić ich rozwój.

### Multi-Party Relays

Multi-Party Relays (MPR) wykorzystują wiele węzłów należących do różnych podmiotów, tak aby żaden pojedynczy podmiot nie znał jednocześnie Twojej tożsamości i tego, z czym się łączysz. To podstawowa idea stojąca za siecią Tor, lecz pojawiają się też płatne usługi próbujące naśladować ten model.

MPR mają na celu rozwiązanie problemu nieodłącznego dla VPN-ów: konieczności pełnego zaufania do dostawcy. Osiągają to przez podział odpowiedzialności pomiędzy dwie lub więcej różnych firm.

Przykładem komercyjnie dostępnego MPR jest iCloud+ Private Relay Apple’a, który kieruje ruch przez dwa serwery:

1. Po pierwsze — serwer obsługiwany przez Apple.

    Serwer ten widzi adres IP urządzenia przy łączeniu się i ma wiedzę o powiązanych danych płatniczych oraz identyfikatorze Apple ID powiązanym z subskrypcją iCloud. Nie widzi jednak, do jakiej strony się łączysz.

2. Po drugie — serwer obsługiwany przez partnera CDN, takiego jak Cloudflare lub Fastly.

    Serwer ten nawiązuje faktyczne połączenie z witryną docelową, ale nie ma wiedzy o Twoim urządzeniu. Jedyny adres IP, jaki zna, to adres serwera Apple.

Inne MPR prowadzone przez różne firmy działają w bardzo podobny sposób. Ochrona poprzez segmentację istnieje tylko wtedy, gdy ufasz, że obie firmy nie będą współpracować w celu ujawnienia Twojej tożsamości.

### Zdecentralizowane VPN-y

Innym podejściem do problemów scentralizowanych usług VPN są zdecentralizowane VPN-y (dVPN). Opierają się na technologii blockchain i deklarują wyeliminowanie zaufania do pojedynczego podmiotu przez rozproszenie węzłów wśród wielu osób. Często jednak dVPN domyślnie używa jednego węzła, co oznacza konieczność pełnego zaufania do tego węzła, tak jak w przypadku tradycyjnego VPN-u. W odróżnieniu od tradycyjnego dostawcy ten pojedynczy węzeł, który może widzieć cały Twój ruch, bywa prowadzony przez przypadkową osobę, a nie przez poddaną audytom firmę zobowiązaną prawnie do przestrzegania swojej polityki prywatności. Rozwiązaniem jest tzw. multi-hop, ale wiąże się to ze spadkiem stabilności i wydajności.

Kolejnym aspektem jest odpowiedzialność prawna. Węzeł wyjściowy musi radzić sobie z konsekwencjami prawnymi wynikającymi z nadużyć sieci — problem, z którym Tor zmaga się od początku swojego istnienia. Zniechęca to zwykłych użytkowników do uruchamiania węzłów i sprawia, że bardziej opłacalne staje się dla złośliwego podmiotu z dużymi zasobami uruchomienie takiego węzła. To poważny problem, jeśli usługa opiera się na pojedynczym węźle, ponieważ potencjalnie złośliwy węzeł wyjściowy może zobaczyć, kim jesteś i z czym się łączysz.

Wiele dVPN-ów służy bardziej jako narzędzie do promowania kryptowalut niż do stworzenia najlepszej usługi. Mają też zwykle mniejsze sieci z mniejszą liczbą węzłów, co zwiększa ich podatność na [ataki typu Sybil](https://en.wikipedia.org/wiki/Sybil_attack).

## Powiązane informacje o VPN

- [Problemy z serwisami recenzującymi VPN i prywatnością](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Śledztwo dotyczące darmowych aplikacji VPN](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Ukryci właściciele VPN ujawnieni: 101 produktów VPN prowadzonych przez zaledwie 23 firmy](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Ta chińska firma stoi potajemnie za 24 popularnymi aplikacjami żądającymi niebezpiecznych uprawnień](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) [VPN — bardzo chwiejna narracja] autorstwa Dennisa Schuberta
