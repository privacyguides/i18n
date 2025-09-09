---
meta_title: "Jak VPN chroni twoją prywatność? Nasze omówienie sieci VPN - Privacy Guides"
title: Omówienie sieci VPN
icon: material/vpn
description: Wirtualne sieci prywatne przenoszą ryzyko z dostawcy usług internetowych na stronę trzecią, której ufasz. Należy mieć to na uwadze.
---

Wirtualne sieci prywatne to sposób na przedłużenie końca twojej sieci do wyjścia w innym miejscu na świecie.

[:material-movie-open-play-outline: Wideo: Czy potrzebujesz sieci VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

Zwykle dostawca usług internetowych może zobaczyć przepływ ruchu internetowego przychodzącego i wychodzącego z twojego punktu zakończenia sieci (tj. modem). Protokoły szyfrowania, takie jak HTTPS, są powszechnie używane w internecie, więc usługodawcy mogą nie być w stanie zobaczyć dokładnie tego, co publikujesz lub czytasz, ale mogą mieć pojęcie o [domenach, które żądasz](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Korzystanie z sieci VPN ukrywa nawet te informacje przed twoim dostawcą usług internetowych, przekazując zaufanie, które umieszczasz w swoją sieć na serwer gdzieś indziej na świecie. W rezultacie dostawca usług internetowych widzi tylko, że jesteś podłączony do sieci VPN i nic nie wie o aktywności, którą przez nią przekazujesz.

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Kiedy mówimy o "wirtualnych sieciach prywatnych" na tej stronie, zwykle odnosimy się do **komercyjnych** [dostawców VPN](../vpn.md), którym użytkownik płaci miesięczną opłatę w zamian za bezpieczne kierowanie ruchu internetowego przez ich publiczne serwery. Istnieje wiele innych form VPN, takich jak te, które hostujesz samodzielnie lub te obsługiwane przez miejsca pracy, które pozwalają bezpiecznie łączyć się z wewnętrznymi / pracowniczymi zasobami sieciowymi, jednak te VPN są zwykle zaprojektowane do bezpiecznego dostępu do sieci zdalnych, a nie do ochrony prywatności połączenia internetowego.

</div>

## Jak działa VPN?

Sieci VPN szyfrują ruch między urządzeniem a serwerem należącym do dostawcy VPN. Z perspektywy każdego, kto znajduje się między tobą a serwerem VPN, wygląda to tak, jakbyś łączył się z serwerem VPN. Z perspektywy każdego, kto znajduje się między serwerem VPN a witryną docelową, wszystko, co widzą, to serwer VPN łączący się ze stroną internetową.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753(("The Internet<div>(Your Destination)</div>"))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Należy pamiętać, że VPN nie dodaje żadnych zabezpieczeń ani szyfrowania do ruchu między serwerem VPN a miejscem docelowym w Internecie. Aby uzyskać bezpieczny dostęp do strony internetowej, **należy** upewnić się, że protokół HTTPS jest używany niezależnie od tego, czy korzystasz z VPN.

## Czy powinienem używać VPN?

**Tak**, niemal pewnie. VPN ma wiele zalet, w tym:

1. Ukrywanie ruchu **tylko** przed dostawcą usług internetowych.
1. Ukrywanie pobieranych plików (takich jak torrenty) przed dostawcą usług internetowych i organizacjami antypirackimi.
1. Ukrywanie twojego adresu IP przed witrynami i usługami innych firm, pomagając wtopić się w otoczenie i zapobiegając śledzeniu opartemu na adresie IP.
1. Umożliwia ominięcie ograniczeń geograficznych dla niektórych treści.

Sieci VPN mogą zapewniać *niektóre* z tych samych korzyści, które zapewnia Tor, takie jak ukrywanie adresu IP przed odwiedzanymi witrynami i geograficzne przenoszenie ruchu sieciowego, a dobrzy dostawcy VPN nie będą współpracować np. z organami prawnymi z opresyjnych reżimów, zwłaszcza jeśli wybierzesz dostawcę VPN poza własną jurysdykcją.

VPN-y nie zaszyfrowują danych poza połączeniem pomiędzy twoim urządzeniem a serwerem VPN. Dostawcy VPN mogą również przeglądać i modyfikować ruch w taki sam sposób, w jaki może to robić dostawca usług internetowych, więc nadal istnieje pewien poziom zaufania, jakim ich obdarzasz. Nie ma możliwości sprawdzenia polityki "bez logów" dostawcy VPN w żaden sposób.

## Kiedy VPN nie jest odpowiedni?

Korzystanie z VPN w przypadkach, gdy używasz swojej [prawdziwej lub dobrze znanej tożsamości](common-misconceptions.md#complicated-is-better) online, jest mało prawdopodobne. Może to spowodować uruchomienie systemów wykrywania spamu i oszustw, tak jak w przypadku logowania się na stronie internetowej banku.

Ważne jest, aby pamiętać, że VPN nie zapewni ci całkowitej anonimowości, ponieważ sam dostawca VPN nadal będzie miał dostęp do twojego prawdziwego adresu IP, informacji o stronie docelowej, a często także do śladu pieniężnego, który można bezpośrednio powiązać z tobą. Polityka „bez logów” to jedynie obietnica; jeśli potrzebujesz pełnego bezpieczeństwa z sieci, rozważ użycie [Tor](../advanced/tor-overview.md) oprócz lub zamiast VPN.

Nie powinieneś również zaufać VPN, aby zabezpieczył twoje połączenie do niezaszyfrowanego celu HTTP. Aby zapewnić prywatność i bezpieczeństwo czynności wykonywanych na odwiedzanych stronach internetowych, należy korzystać z protokołu HTTPS. Dzięki temu hasła, tokeny sesji i zapytania będą bezpieczne przed dostawcą VPN i innymi potencjalnymi przeciwnikami między serwerem VPN a miejscem docelowym. Powinieneś włączyć tryb tylko HTTPS w swojej przeglądarce (jeśli jest obsługiwany), aby złagodzić ataki, które próbują obniżyć jakość połączenia z HTTPS do HTTP.

## Czy powinienem używać szyfrowanego DNS z VPN?

**Prawdopodobnie nie**, dopóki dostawca VPN sam hostuje zaszyfrowane serwery DNS. Korzystanie z DOH/DOT (lub jakiejkolwiek innej formy szyfrowanego DNS) z serwerami stron trzecich po prostu doda więcej podmiotów do zaufania. Twój dostawca VPN może nadal sprawdzać, które witryny odwiedzasz na podstawie adresów IP i innych metod. Biorąc to wszystko pod uwagę, mogą istnieć pewne korzyści z włączenia szyfrowanego DNS w celu włączenia innych funkcji bezpieczeństwa w przeglądarce, takich jak ECH. Technologie przeglądarek, które opierają się na szyfrowanym DNS w przeglądarce, są stosunkowo nowe i jeszcze nie rozpowszechnione, więc to, czy są one szczególnie istotne dla użytkownika, pozostawiamy do samodzielnego zbadania.

Innym częstym powodem, dla którego zalecane jest szyfrowanie DNS, jest zapobieganie spoofingowi DNS. Jednak przeglądarka powinna już sprawdzać [certyfikaty TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) z **HTTPS** i ostrzegać o tym. Jeśli nie korzystasz z **protokołu HTTPS**, przeciwnik może po prostu zmodyfikować wszystko inne niż zapytania DNS, a wynik końcowy będzie niewiele inny.

## Czy powinienem używać Tora *i* VPN?

Być może, Tor niekoniecznie jest odpowiedni dla każdego. Weź pod uwagę swój [model zagrożenia](threat-modeling.md), ponieważ jeśli przeciwnik nie jest w stanie wydobyć informacji od dostawcy VPN, samo korzystanie z VPN może zapewnić wystarczającą ochronę.

Jeśli korzystasz z sieci Tor, *prawdopodobnie* najlepiej będzie połączyć się z nią za pośrednictwem komercyjnego dostawcy VPN. Jest to jednak złożony temat, o którym napisaliśmy więcej na naszej stronie [przeglądu Tora](../advanced/tor-overview.md).

## Czy powinienem uzyskiwać dostęp do sieci Tor za pośrednictwem dostawców VPN, którzy zapewniają "węzły Tor"?

Nie powinieneś używać tej funkcji: Podstawową zaletą korzystania z sieci Tor jest brak zaufania do dostawcy VPN, co jest negowane w przypadku korzystania z węzłów Tor hostowanych przez sieć VPN zamiast łączenia się bezpośrednio z siecią Tor z komputera.

Obecnie Tor obsługuje tylko protokół TCP. Pakiety UDP (używane przez [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) i inne protokoły), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) i inne będą odrzucane. Aby to zrekompensować, dostawcy VPN zazwyczaj kierują wszystkie pakiety inne niż TCP przez swój serwer VPN (pierwszy przeskok). Tak właśnie jest w przypadku [ProtonVPN](https://protonvpn.com/support/tor-vpn). Dodatkowo, podczas korzystania z tej konfiguracji Tor over VPN, nie masz kontroli nad innymi ważnymi funkcjami Tor, takimi jak [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (używanie innego obwodu Tor dla każdej odwiedzanej domeny).

Funkcja ta powinna być postrzegana jako *wygodny* sposób na dostęp do ukrytych usług w sieci Tor, a nie na zachowanie anonimowości. Dla zapewnienia właściwej anonimowości, użyj aktualnej [przeglądarki Tor](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies.

One example of a commercially available MPR is Apple's iCloud+ Private Relay, which routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Related VPN Information

- [The Trouble with VPN and Privacy Review Sites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Free VPN App Investigation](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
