---
meta_title: "Jak VPN chroni twoją prywatność? Nasze omówienie sieci VPN - Privacy Guides"
title: Przegląd VPN
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

## Komercyjna własność VPN

Większość usług VPN należy do tych samych [kilku firm](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). Te podejrzane firmy prowadzą wiele mniejszych usług VPN, aby stworzyć iluzję, że masz większy wybór niż w rzeczywistości i zmaksymalizować zyski. Zazwyczaj ci dostawcy, którzy zasilają swoją firmę-powłokę, mają okropną politykę prywatności i nie należy im ufać w kwestii ruchu internetowego. Należy bardzo rygorystycznie podchodzić do wyboru dostawcy usług.

Należy również uważać, że wiele witryn z recenzjami VPN to jedynie narzędzia reklamowe otwarte na oferentów oferujących najwyższą cenę. ==Privacy Guides nie zarabia na polecaniu zewnętrznych produktów i nigdy nie korzysta z programów partnerskich.==

[Nasze rekomendacje VPN](../vpn.md ""){.md-button}

## Nowoczesne alternatywy VPN

Ostatnio różne organizacje podjęły próby rozwiązania niektórych problemów, z którymi borykają się scentralizowane sieci VPN. Technologie te są stosunkowo nowe, ale warto śledzić ich rozwój.

### Przekaźniki wielostronne

Przekaźniki wielostronne (MPR) wykorzystują wiele węzłów należących do różnych stron, dzięki czemu żadna ze stron nie wie, kim jesteś i z czym się łączysz. Jest to podstawowa idea stojąca za Torem, ale obecnie istnieje kilka płatnych usług, które próbują naśladować ten model.

MPR-y starają się rozwiązać problem nieodłącznie związany z VPN-ami: fakt, że trzeba im całkowicie ufać. Osiągają ten cel poprzez podział obowiązków pomiędzy dwie lub więcej różnych firm.

Jednym z przykładów komercyjnie dostępnego MPR jest Apple iCloud+ Private Relay, który kieruje ruch przez dwa serwery:

1. Po pierwsze, serwer obsługiwany przez Apple.

    Serwer ten jest w stanie zobaczyć adres IP urządzenia podczas łączenia się z nim, a także zna informacje o płatnościach i identyfikator Apple ID powiązany z subskrypcją iCloud. Nie jest jednak w stanie sprawdzić, z jaką witryną się łączysz.

2. Po drugie, serwer obsługiwany przez partnerski CDN, taki jak Cloudflare lub Fastly.

    Serwer ten faktycznie nawiązuje połączenie z witryną docelową, ale nie ma wiedzy o urządzeniu użytkownika. Jedynym adresem IP, o którym wie, jest adres serwera Apple.

Inne MPR prowadzone przez różne firmy działają w bardzo podobny sposób. Ta ochrona poprzez segmentację istnieje tylko wtedy, gdy ufasz, że obie firmy nie zmówią się ze sobą w celu deanonimizacji użytkownika.

### Zdecentralizowane sieci VPN

Inną próbą rozwiązania problemów ze scentralizowanymi usługami VPN są sieci dVPN. Są one oparte na technologii blockchain i twierdzą, że eliminują zaufanie do jednej strony poprzez dystrybucję węzłów wśród wielu różnych osób. Jednak wiele razy dVPN domyślnie wybiera pojedynczy węzeł, co oznacza, że musisz całkowicie zaufać temu węzłowi, tak jak w przypadku tradycyjnej sieci VPN. W przeciwieństwie do tradycyjnej sieci VPN, ten jeden węzeł, który może zobaczyć cały ruch użytkownika, jest przypadkową osobą, a nie dostawcą VPN, który może zostać poddany audytowi i ma prawny obowiązek przestrzegania swojej polityki prywatności. Aby rozwiązać ten problem, potrzebny jest multi-hop, ale wiąże się to z kosztami stabilności i wydajności.

Inną kwestią jest odpowiedzialność prawna. Węzeł wyjściowy będzie musiał radzić sobie z problemami prawnymi wynikającymi z niewłaściwego korzystania z sieci, z czym sieć Tor borykała się przez całe swoje istnienie. Zniechęca to zwykłych ludzi do uruchamiania węzłów i sprawia, że jest to bardziej atrakcyjne dla złośliwego aktora z dużą ilością zasobów. Jest to duży problem, jeśli usługa jest jednowęzłowa, ponieważ potencjalnie złośliwy węzeł wyjściowy może zobaczyć, kim jesteś i z czym się łączysz.

Wiele sieci dVPN jest wykorzystywanych do promowania kryptowalut, a nie do świadczenia najlepszych usług. Są to również zwykle mniejsze sieci z mniejszą liczbą węzłów, co czyni je bardziej podatnymi na [ataki Sybil](https://en.wikipedia.org/wiki/Sybil_attack).

## Powiązane informacje o VPN

- [Kłopoty ze stronami z recenzjami VPN i prywatności](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Badanie darmowych aplikacji VPN](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Ukryci właściciele VPN: 101 produktów VPN zarządzanych przez zaledwie 23 firmy](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Ta chińska firma jest tajna za 24 popularnych aplikacjami szukającymi niebezpiecznych uprawnień](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - bardzo niepewna narracja](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) Dennisa Schuberta
