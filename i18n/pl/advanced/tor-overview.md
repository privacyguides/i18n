---
title: "Przegląd sieci Tor"
icon: 'simple/torproject'
description: Tor to bezpłatna, zdecentralizowana sieć zaprojektowana z myślą o możliwie największej prywatności podczas korzystania z Internetu.
---

![Logo Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) to bezpłatna, zdecentralizowana sieć zaprojektowana tak, by umożliwiać korzystanie z Internetu z jak największym zachowaniem prywatności. Jeśli jest używana prawidłowo, sieć umożliwia prywatne i anonimowe przeglądanie oraz komunikację. Dzięki temu, że ruch w sieci Tor jest trudny do zablokowania i namierzenia, Tor stanowi skuteczne narzędzie do omijania cenzury.

[:material-movie-open-play-outline: Wideo: Dlaczego potrzebujesz Tora](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

Tor działa, kierując ruch internetowy przez serwery obsługiwane przez wolontariuszy, zamiast nawiązywać bezpośrednie połączenie ze stroną, którą próbuje się odwiedzić. Zaciera to informację, skąd pochodzi ruch — żaden serwer na trasie połączenia nie widzi pełnej ścieżki, skąd ruch pochodzi i dokąd zmierza, więc nawet serwery używane do połączenia nie są w stanie złamać Twojej anonimowości.

[:octicons-home-16:](https://torproject.org/pl){ .card-link title="Strona główna"}
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Usługa .onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Wspomóż projekt" }

## Bezpieczne łączenie się z siecią Tor

Przed połączeniem się z siecią Tor należy dokładnie rozważyć, co chce się osiągnąć za jej pomocą, i przed kim próbuje się ukryć swoją aktywność w sieci.

Jeśli mieszkasz w wolnym kraju, korzystasz z Tora do przeglądania zwykłych treści, nie obawiasz się, że Twój dostawca usług internetowych (ISP) lub administratorzy lokalnej sieci dowiedzą się, że korzystasz z Tora i chcesz pomóc w [zniesieniu piętna](https://2019.www.torproject.org/about/torusers.html.en) związanego z korzystaniem z Tora, prawdopodobnie możesz bez obaw połączyć się z siecią Tor bezpośrednio za pomocą standardowych metod, np. przez przeglądarkę [Tor Browser](../tor.md).

Jeśli masz możliwość skorzystania z zaufanego dostawcy VPN i **którekolwiek** z poniższych stwierdzeń jest prawdziwe, prawie na pewno należy łączyć się z siecią Tor za pośrednictwem VPN:

- Już korzystasz z [zaufanego dostawcy VPN](../vpn.md)
- Twój model zagrożeń obejmuje przeciwnika, który jest w stanie wydobyć informacje od Twojego ISP
- Twój model zagrożeń obejmuje samego dostawcę usług internetowych jako przeciwnika
- Twój model zagrożeń obejmuje administratorów lokalnej sieci działających przed Twoim ISP jako przeciwników

Ponieważ już z różnych powodów [ogólnie zalecamy](../basics/vpn-overview.md), by zdecydowana większość osób korzystała z zaufanego dostawcy VPN, następujące zalecenie dotyczące łączenia się z siecią Tor za pośrednictwem VPN prawdopodobnie dotyczy także Ciebie. <mark>Nie ma potrzeby wyłączać VPN-a przed połączeniem się z siecią Tor</mark>, jak sugerują to niektóre źródła internetowe.

Łączenie się bezpośrednio z siecią Tor sprawi, że Twoje połączenie będzie się wyróżniać dla administratorów lokalnej sieci lub ISP. W przeszłości administratorzy sieci potrafili [wykryć i skorelować](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) taki ruch, by zidentyfikować i zdeanonimizować konkretne osoby korzystające z Tora. Z drugiej jednak strony połączenie przez VPN zwykle wzbudza mniejsze podejrzenia, ponieważ komercyjne usługi VPN są wykorzystywane przez zwykłych konsumentów do różnych codziennych zadań, np. omijania ograniczeń geograficznych, nawet w krajach o silnych ograniczeniach Internetu.

Dlatego warto zadbać o ukrycie swojego adresu IP **przed** połączeniem z siecią Tor. Można to zrobić, łącząc się najpierw z VPN (poprzez klienta zainstalowanego na komputerze), a następnie uzyskując dostęp do sieci [Tor](../tor.md) normalnie (np. przez przeglądarkę Tor Browser). Powstaje wtedy następujący łańcuch połączeń:

- [x] Ty → VPN → Tor → Internet

Z perspektywy ISP wygląda to tak, jak zwykłe korzystanie z VPN (co daje pewną zasłonę). Z perspektywy dostawcy VPN widać połączenie z siecią Tor, ale nic o odwiedzanych przez Ciebie stronach. Z perspektywy Tora połączenie wygląda normalnie, a w mało prawdopodobnym przypadku kompromitacji sieci Tor ujawniony zostałby jedynie Twój adres IP VPN-a — konieczne byłoby *dodatkowe* naruszenie samej sieci VPN, by Cię zdeanonimizować.

**Nie** jest to zalecenie dotyczące obchodzenia cenzury, ponieważ jeśli ISP całkowicie blokuje Tor, prawdopodobnie zablokuje też VPN. Celem tego zalecenia jest raczej lepsze wtopienie się Twojego ruchu w zwykły ruch użytkowników VPN oraz zapewnienie pewnego poziomu możliwej do wyparcia wiarygodności, ukrywając fakt łączenia się z Tor przed dostawcą usług internetowych.

---

**Zdecydowanie odradzamy** łączenie Tora z VPN w jakikolwiek inny sposób. Nie konfiguruj połączenia w sposób przypominający którekolwiek z poniższych:

- Ty → Tor → VPN → Internet
- Ty → VPN → Tor → VPN → Internet
- Jakakolwiek inna konfiguracja

Niektórzy dostawcy VPN i inne publikacje okazjonalnie zalecają takie **złe** konfiguracje, by obejść blokady Tor (np. gdy w niektórych miejscach węzły wyjściowe są blokowane przez strony). [Zazwyczaj](https://support.torproject.org/#about_change-paths) Tor często zmienia trasę obwodu w sieci. Gdy wybierze się stałe *miejsce docelowe* VPN (czyli łączenie z serwerem VPN *po* Tor), traci się tę przewagę i znacznie szkodzi się swojej anonimowości.

Ustawienie takich złych konfiguracji rzadko zdarza się przypadkowo, bo zwykle wymaga skonfigurowania niestandardowych ustawień proxy w przeglądarce Tor Browser lub niestandardowych ustawień w kliencie VPN, które kierują ruch VPN poprzez przeglądarkę Tor Browser. Unikając tych niestandardowych konfiguracji, najprawdopodobniej wszystko będzie w porządku.

---

<div class="admonition info" markdown>
<p class="admonition-title">Identyfikacja wzorców ruchu VPN/SSH</p>

Tor Project [zauważa](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting), że *teoretycznie* użycie VPN do ukrycia aktywności Tor przed dostawcą usług internetowych może nie być niezawodne. Wykryto przypadki, gdzie VPN-y były podatne na identyfikację wzorców ruchu na stronach internetowych — przeciwnik mógł odgadnąć, jaka strona jest odwiedzana, ponieważ poszczególne witryny mają charakterystyczne wzorce ruchu.

Dlatego nie jest nierozsądne przypuszczać, że zaszyfrowany ruch Tor ukryty przez VPN mógłby być wykryty podobnymi metodami. Nie ma na ten temat badań naukowych, ale wciąż uważamy, że korzyści płynące z korzystania z VPN znacznie przewyższają te ryzyka, ale jest to coś, co warto mieć na uwadze.

Jeżeli mimo uważasz, że transporty wtykowe (mostki) zapewniają dodatkową ochronę przed identyfikacją wzorców ruchu, której VPN nie zapewnia, zawsze masz możliwość korzystania z mostku *oraz* VPN jednocześnie.

</div>

Decyzja, czy najpierw użyć VPN przed połączeniem się z siecią Tor, wymaga zdrowego rozsądku i znajomości polityk własnego rządu oraz dostawcy usług internetowych dotyczących tego, z czym się łączysz. Powtórzmy: w większości przypadków lepiej będzie sprawiać wrażenie osoby łączącej się z komercyjną siecią VPN niż bezpośrednio z siecią Tor. Jeśli dostawcy VPN są cenzurowani w Twojej okolicy, możesz rozważyć użycie transportów wtykowych (np. mostków Snowflake lub meek) jako alternatywy, choć korzystanie z takich mostków może wzbudzać więcej podejrzeń niż standardowe tunele WireGuard/OpenVPN.

## Czym Tor nie jest

Sieć Tor nie jest doskonałym narzędziem do ochrony prywatności we wszystkich sytuacjach i ma szereg wad, które warto dokładnie rozważyć. Nie powinno to jednak zniechęcać cię do korzystania z Tora, jeśli jest on odpowiedni dla Twoich potrzeb — są to po prostu kwestie, które należy brać pod uwagę przy wyborze najbardziej dopasowanego rozwiązania dla Ciebie.

### Tor nie jest darmową siecią VPN

Pojawienie się aplikacji mobilnej *Orbot* spowodowało, że wiele osób zaczęło określać Tor mianem „darmowego VPN-a” dla całego ruchu urządzenia. Jednak traktowanie Tora w ten sposób niesie ze sobą pewne niebezpieczeństwa w porównaniu do typowej sieci VPN.

W przeciwieństwie do węzłów wyjściowych Tora, dostawcy VPN zwykle nie są *aktywnie* [złośliwi](#caveats). Ponieważ węzły wyjściowe Tora może uruchomić praktycznie każdy, stanowią one miejsca, gdzie często prowadzona jest rejestracja i modyfikacja ruchu. W 2020 roku udokumentowano wiele węzłów wyjściowych, które obniżały jakość ruchu HTTPS do HTTP, aby [przejmować transakcje kryptowalutowe](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Zaobserwowano także inne ataki ze strony węzłów wyjściowych, np. zastępowanie pobieranych przez niezaszyfrowane kanały plików złośliwym oprogramowaniem. HTTPS w pewnym stopniu łagodzi te zagrożenia.

Jak już wspomnieliśmy, Tor jest również łatwy do zidentyfikowania w sieci. W przeciwieństwie do komercyjnego dostawcy VPN, korzystanie z Tora może wyróżniać Cię jako osobę prawdopodobnie próbującą unikać nadzoru władz. W idealnym świecie administratorzy sieci i organy władzy traktowaliby Tor jako narzędzie o wielu zastosowaniach (podobnie jak VPN), ale w praktyce postrzeganie Tora jest wciąż znacznie mniej wiarygodne niż postrzeganie komercyjnych sieci VPN. Dlatego korzystanie z prawdziwej sieci VPN daje większą możliwość wiarygodnego zaprzeczenia, np. „Używałem VPN-a tylko do oglądania Netflixa” itp.

### Korzystanie z sieci Tor nie jest niewykrywalne

**Nawet jeśli korzystasz z mostków i transportów wtykowych,** Tor Project nie udostępnia narzędzi, które ukrywałyby przed Twoim ISP fakt używania Tora. Nawet stosowanie zaciemnionych „transportów wtykowych” lub niepublicznych mostków nie ukrywa, że korzysta się z prywatnego kanału komunikacji. Najpopularniejsze transporty wtykowe, takie jak obfs4 (który zaciemnia ruch, by „nie przypominał niczego”) oraz meek (który wykorzystuje maskowanie domeny do maskowania ruchu), mogą być [wykrywane](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) przy użyciu dość standardowych technik analizy ruchu. Snowflake ma podobne problemy i może być [łatwo wykryty](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) jeszcze *przed* nawiązaniem połączenia z siecią Tor.

Istnieją również inne niż te trzy transporty wtykowe, ale zazwyczaj opierają się one na zasadzie bezpieczeństwa przez zaciemnienie (*security through obscurity*). Nie są one niemożliwe do wykrycia — po prostu korzysta z nich tak niewiele osób, że nie opłaca się budować dla nich detektorów. Nie powinno się na nich polegać, jeśli konkretnie jesteś osobą monitorowaną.

Ważne jest rozróżnienie między omijaniem cenzury a unikaniem wykrycia. To pierwsze jest zwykle łatwiejsze ze względu na rzeczywiste ograniczenia, jakie mają cenzorzy sieci przy masowym działaniu, ale te techniki nie ukrywają faktu, że to *konkretnie* Ty używasz Tora przed zainteresowaną stroną monitorującą Twoją sieć.

### Tor Browser nie jest naj*bezpieczniejszą* przeglądarką

Anonimowość często stoi w sprzeczności z bezpieczeństwem: anonimowość sieci Tor wymaga, by wszyscy użytkownicy byli identyczni, co tworzy monokulturę (np. te same błędy występują u wszystkich użytkowników przeglądarki Tor Browser). Z punktu widzenia cyberbezpieczeństwa monokultury zwykle uznawane są za złe: bezpieczeństwo przez różnorodność (którego Tor nie zapewnia) naturalnie dzieli środowisko i ogranicza zasięg podatności, co z reguły jest pożądane, choć mniej korzystne dla anonimowości.

Ponadto przeglądarka Tor Browser bazuje na wydaniach Firefoksa o wydłużonym wsparciu (Extended Support Release – ESR), które otrzymują poprawki tylko dla podatności sklasyfikowanych jako *krytyczne* i *wysokie* (nie dla *średnich* i *niskich*). Oznacza to, że atakujący mogą (na przykład):

1. Szukać nowych podatności o statusie krytycznym lub wysokim w wersjach nightly lub beta Firefoksa, a następnie sprawdzać, czy można je wykorzystać w przeglądarce Tor Browser (okres, w którym luka pozostaje niezałatana, może trwać tygodniami).
2. Łączyć ze sobą *wiele* podatności o poziomie średnim/niskim, aż uzyskają pożądany poziom dostępu (okres ten może trwać miesiące lub dłużej).

Osoby narażone na ryzyko wynikające z luk przeglądarki powinny rozważyć dodatkowe środki ochronne przeciwko exploitom przeglądarki Tor Browser, na przykład korzystanie z Whonix w [Qubes](../os/qubes-overview.md) w celu odizolowania sesji przeglądania przez Tor w bezpiecznej maszynie wirtualnej i ochrony przed wyciekami.

## Budowanie ścieżki do serwisów w clearnet

"Clearnet services" are websites which you can access with any browser, like [privacyguides.org](https://www.privacyguides.org). Tor lets you connect to these websites anonymously by routing your traffic through a network comprised of thousands of volunteer-run servers called nodes (or relays).

Every time you [connect to Tor](../tor.md), it will choose three nodes to build a path to the internet—this path is called a "circuit."

<figure markdown>
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor circuit pathway</figcaption>
</figure>

Each of these nodes has its own function:

### The Entry Node

The entry node, often called the guard node, is the first node to which your Tor client connects. The entry node is able to see your IP address, however it is unable to see what you are connecting to.

Unlike the other nodes, the Tor client will randomly select an entry node and stick with it for two to three months to protect you from certain attacks.[^1]

### The Middle Node

The middle node is the second node to which your Tor client connects. It can see which node the traffic came from—the entry node—and to which node it goes to next. The middle node cannot, see your IP address or the domain you are connecting to.

For each new circuit, the middle node is randomly selected out of all available Tor nodes.

### The Exit Node

The exit node is the point in which your web traffic leaves the Tor network and is forwarded to your desired destination. The exit node is unable to see your IP address, but it does know what site it's connecting to.

The exit node will be chosen at random from all available Tor nodes ran with an exit relay flag.[^2]

## Path Building to Onion Services

"Onion Services" (also commonly referred to as "hidden services") are websites which can only be accessed by the Tor browser. These websites have a long randomly generated domain name ending with `.onion`.

Connecting to an Onion Service in Tor works very similarly to connecting to a clearnet service, but your traffic is routed through a total of **six** nodes before reaching the destination server. Just like before, however, only three of these nodes are contributing to *your* anonymity, the other three nodes protect *the Onion Service's* anonymity, hiding the website's true IP and location in the same manner that Tor Browser is hiding yours.

<figure style="width:100%" markdown>
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor circuit pathway with Onion Services. Nodes in the <span class="pg-blue">blue</span> fence belong to your browser, while nodes in the <span class="pg-red">red</span> fence belong to the server, so their identity is hidden from you.</figcaption>
</figure>

## Encryption

Tor encrypts each packet (a block of transmitted data) three times with the keys from the exit, middle, and entry node in that order.

Once Tor has built a circuit, data transmission is done as follows:

1. Firstly: When the packet arrives at the entry node, the first layer of encryption is removed. In this encrypted packet, the entry node will find another encrypted packet with the middle node’s address. The entry node will then forward the packet to the middle node.

2. Secondly: When the middle node receives the packet from the entry node, it too will remove a layer of encryption with its key, and this time finds an encrypted packet with the exit node's address. The middle node will then forward the packet to the exit node.

3. Lastly: When the exit node receives its packet, it will remove the last layer of encryption with its key. The exit node will see the destination address and forward the packet to that address.

Below is an alternative diagram showing the process. Each node removes its own layer of encryption, and when the destination server returns data, the same process happens entirely in reverse. For example, the exit node does not know who you are, but it does know which node it came from, and so it adds its own layer of encryption and sends it back.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Sending and receiving data through the Tor Network</figcaption>
</figure>

Tor allows us to connect to a server without any single party knowing the entire path. The entry node knows who you are, but not where you are going; the middle node doesn’t know who you are or where you are going; and the exit node knows where you are going, but not who you are. Because the exit node is what makes the final connection, the destination server will never know your IP address.

## Caveats

Though Tor does provide strong privacy guarantees, one must be aware that Tor is not perfect:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Tor exit nodes can also monitor traffic that passes through them. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

If you wish to use Tor for browsing the web, we only recommend the **official** Tor Browser—it is designed to prevent fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges; they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges—you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Android

- [Tor Browser User Manual](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: The first relay in your circuit is called an "entry guard" or "guard". It is a fast and stable relay that remains the first one in your circuit for 2-3 months in order to protect against a known anonymity-breaking attack. The rest of your circuit changes with every new website you visit, and all together these relays provide the full privacy protections of Tor. For more information on how guard relays work, see this [blog post](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) and [paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) on entry guards. ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Relay flag: a special (dis-)qualification of relays for circuit positions (for example, "Guard", "Exit", "BadExit"), circuit properties (for example, "Fast", "Stable"), or roles (for example, "Authority", "HSDir"), as assigned by the directory authorities and further defined in the directory protocol specification. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
