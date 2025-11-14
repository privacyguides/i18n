---
title: "Powszechne zagrożenia"
icon: 'material/eye-outline'
description: Model zagrożeń jest dla każdego indywidualny, ale oto kilka kwestii, które interesują wielu odwiedzających tę stronę.
---

Ogólnie rzecz biorąc, dzielimy nasze zalecenia według [zagrożeń](threat-modeling.md) lub celów, które dotyczą większości osób. ==Może nie dotyczyć Cię żadne, jedno, kilka lub wszystkie z tych zagrożeń== — narzędzia i usługi, których używasz, zależą od twoich celów. Możesz mieć też konkretne zagrożenia wykraczające poza te kategorie, i to jest całkowicie w porządku! Najważniejsze jest zrozumienie korzyści i ograniczeń narzędzi, które wybierasz, ponieważ praktycznie żadne z nich nie ochroni cię przed wszystkimi zagrożeniami.

<span class="pg-purple">:material-incognito: **Anonimowość**</span>
:

Chronienie aktywności w sieci przed ujawnieniem Twojej prawdziwej tożsamości, zabezpieczając cię przed osobami, które w szczególności próbują poznać *Twoją* tożsamość.

<span class="pg-red">:material-target-account: **Ataki ukierunkowane**</span>
:

Ochrona przed hakerami lub innymi cyberprzestępcami, którzy próbują uzyskać dostęp do *Twoich* danych lub urządzeń w sposób wymierzony.

<span class="pg-viridian">:material-package-variant-closed-remove: **Ataki na łańcuch dostaw**</span>
:

Zwykle przyjmuję formę <span class="pg-red">:material-target-account: Ataku ukierunkowanego</span>, która koncentruje się wokół luki lub exploitu w zabezpieczeniach wprowadzonego do pozornie dobrego oprogramowania — bezpośrednio lub przez zależność od strony trzeciej.

<span class="pg-orange">:material-bug-outline: **Ataki pasywne**</span>
:

Ochrona przed takimi zagrożeniami jak złośliwe oprogramowanie, wycieki danych i innymi atakami wymierzonymi przeciwko wielu osobom jednocześnie.

<span class="pg-teal">:material-server-network: **Dostawcy usług**</span>
:

Ochrona Twoich danych przed dostawcami usług (np. za pomocą E2EE, które sprawia, że twoje dane są nieczytelne dla serwera).

<span class="pg-blue">:material-eye-outline: **Masowa inwigilacja**</span>
:

Ochrona przed agencjami rządowymi, organizacjami, stronami i usługami, które współpracują, by śledzić Twoje działania.

<span class="pg-brown">:material-account-cash: **Kapitalizm inwigilacji**</span>
:

Ochrona przed dużymi sieciami reklamowymi, takimi jak Google i Facebook, oraz przed wieloma innymi zbieraczami danych stron trzecich.

<span class="pg-green">:material-account-search: **Ekspozycja publiczna**</span>
:

Ograniczanie dostępnych o Tobie informacji w sieci — dla wyszukiwarek lub ogółu.

<span class="pg-blue-gray">:material-close-outline: **Cenzura**</span>
:

Unikanie cenzurowanego dostępu do informacji lub sytuacji, w których Twoje wypowiedzi online są cenzurowane.

Niektóre z tych zagrożeń mogą być dla Ciebie ważniejsze niż inne, w zależności od Twoich obaw. Na przykład programista mający dostęp do wartościowych lub krytycznych danych może przede wszystkim martwić się o <span class="pg-viridian">:material-package-variant-closed-remove: Ataki na łańcuch dostaw</span> i <span class="pg-red">:material-target-account: Ataki ukierunkowane</span>. Prawdopodobnie nadal będzie chciał chronić swoje dane osobowe przed wciągnięciem ich w programy <span class="pg-blue">:material-eye-outline: Masowej inwigilacji</span>. Podobnie wiele osób może przede wszystkim obawiać się <span class="pg-green">:material-account-search: Ekspozycji publicznej</span> swoich danych osobowych, ale i tak powinny być one czujne w kwestiach związanych z bezpieczeństwem, takich jak <span class="pg-orange">:material-bug-outline: Ataki pasywne</span> — na przykład złośliwe oprogramowanie atakujące ich urządzenia.

## Anonimowość a prywatność

<span class="pg-purple">:material-incognito: Anonimowość</span>

Anonimowość jest często mylona z prywatnością, ale są to różne pojęcia. Prywatność to zestaw wyborów dotyczących tego, jak Twoje dane są używane i udostępniane, natomiast anonimowość to całkowite oddzielenie Twoich działań w sieci od Twojej prawdziwej tożsamości.

Na przykład sygnaliści i dziennikarze mogą mieć znacznie bardziej ekstremalny model zagrożeń, który wymaga całkowitej anonimowości. Chodzi nie tylko o ukrycie tego, co robią, jakimi danymi dysponują i o ochronę przed atakami cyberprzestępców czy państw, ale też o pełne ukrycie, kim są. Często rezygnują z jakiejkolwiek wygody, jeśli pozwala to chronić ich anonimowość, prywatność lub bezpieczeństwo, ponieważ od tego może zależeć ich życie. Większość osób nie musi iść aż tak daleko.

## Bezpieczeństwo a prywatność

<span class="pg-orange">:material-bug-outline: Ataki pasywne</span>

Bezpieczeństwo i prywatność też bywają często mylone, ponieważ potrzebujesz bezpieczeństwa, by w ogóle mieć choćby namiastkę prywatności: korzystanie z narzędzi — nawet zaprojektowanych z myślą o prywatności — jest bezcelowe, jeśli mogą zostać łatwo wykorzystane przez atakujących, którzy później ujawnią Twoje dane. Jednak odwrotność niekoniecznie jest prawdziwa: najbezpieczniejsza usługa na świecie *niekoniecznie* jest prywatna. Najlepszym przykładem jest powierzenie danych firmie Google, która, biorąc pod uwagę swoją skalę, miała stosunkowo niewiele incydentów bezpieczeństwa, bo zatrudnia wiodących w branży ekspertów, by zabezpieczać swoją infrastrukturę. Mimo że Google dostarcza bardzo bezpieczne usługi, niewiele osób uznałoby swoje dane za prywatne w darmowych produktach konsumenckich Google (Gmail, YouTube itp.).

Jeśli chodzi o bezpieczeństwo aplikacji, zwykle nie wiemy (a czasem nie możemy wiedzieć), czy oprogramowanie, z którego korzystamy, jest złośliwe lub czy pewnego dnia nie stanie się złośliwe. Nawet przy najbardziej godnych zaufania deweloperach nie ma zwykle gwarancji, że ich oprogramowanie nie zawiera poważnej luki, którą można by później wykorzystać.

Aby zminimalizować szkody, jakie złośliwe oprogramowanie *mogłoby* wyrządzić, warto stosować zasadę zabezpieczeń przez szufladkowanie (ang. *compartmentalization*). Na przykład może to oznaczać używanie różnych komputerów do różnych zadań, korzystanie z maszyn wirtualnych do izolowania grup powiązanych aplikacji albo użycie bezpiecznego systemu operacyjnego silnie stawiającego na mechanizm piaskownicy aplikacji i obowiązkową kontrolę dostępu.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Mobilne systemy operacyjne zazwyczaj oferują lepszy mechanizm piaskownicy aplikacji niż systemy na komputery stacjonarne: aplikacje nie mogą uzyskać uprawnień root i wymagają zezwoleń na dostęp do zasobów systemowych.

Systemy na komputery stacjonarne zwykle pozostają w tyle w kwestii piaskownic. ChromeOS ma podobne możliwości piaskownicy do Androida, a macOS zapewnia pełną kontrolę uprawnień systemowych (deweloperzy mogą opcjonalnie włączyć piaskownicę dla aplikacji). Jednak systemy te przekazują informacje identyfikujące do swoich producentów OEM. Linux zwykle nie wysyła danych do dostawców systemu, lecz gorzej chroni przed exploitami i złośliwymi aplikacjami. Można to częściowo złagodzić, korzystając ze specjalistycznych dystrybucji, które w dużym stopniu opierają się na maszynach wirtualnych lub kontenerach, takich jak [Qubes OS](../desktop.md#qubes-os).

</div>

## Ataki wymierzone w konkretne osoby

<span class="pg-red">:material-target-account: Ataki ukierunkowane</span>

Ataki ukierunkowane przeciwko konkretnej osobie są bardziej problematyczne. Do typowych ataków należą wysyłanie złośliwych dokumentów e-mailem, wykorzystywanie luk (np. w przeglądarkach i systemach operacyjnych) oraz ataki fizyczne. Jeśli to Cię dotyczy, warto wdrożyć bardziej zaawansowane strategie ograniczania zagrożeń.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Z założenia **przeglądarki internetowe**, **klienci poczty e-mail** i **aplikacje biurowe** zwykle uruchamiają niezaufany kod przesyłany od stron trzecich. Uruchamianie wielu maszyn wirtualnych — aby oddzielić tego typu aplikacje od systemu głównego oraz od siebie nawzajem — to jedna z technik zmniejszających ryzyko, że exploity w tych aplikacjach naruszą resztę systemu. Na przykład technologie takie jak Qubes OS lub Microsoft Defender Application Guard w systemie Windows oferują wygodne sposoby realizacji takiego podejścia.

</div>

Jeśli obawiasz się **ataków fizycznych**, warto korzystać z systemu operacyjnego z bezpieczną implementacją zweryfikowanego rozruchu (ang. *verified boot*), takiego jak Android, iOS, macOS lub [Windows (z TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Nalezy również upewnić się, że dysk jest zaszyfrowany, a system operacyjny korzysta z TPM, Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) lub [Element](https://developers.google.com/android/security/android-ready-se), aby ograniczać liczbę prób wprowadzenia hasła szyfrującego. Unikaj udostępniania komputera osobom, którym nie ufasz, ponieważ większość systemów operacyjnych dla komputerów stacjonarnych nie szyfruje danych oddzielnie dla każdego użytkownika.

## Ataki wymierzone w niektóre organizacje

<span class="pg-viridian">:material-package-variant-closed-remove: Ataki na łańcuch dostaw</span>

Ataki na łańcuch dostaw to często forma <span class="pg-red">:material-target-account: Ataku ukierunkowanego</span> wymierzonego w firmy, rządy i aktywistów, choć mogą one również zagrażać ogółowi społeczeństwa.

<div class="admonition example" markdown>
<p class="admonition-title">Przykład</p>

Znanym przypadkiem z 2017 r. było zainfekowanie popularnego ukraińskiego oprogramowania finansowo-księgowego M.E.Doc wirusem *NotPetya*, który następnie zainfekował użytkowników tego oprogramowania ransomware'em. NotPetya sam w sobie był atakiem ransomware, który dotknął ponad 2000 firm w różnych krajach i opierał się na exploicie *EternalBlue* opracowanym przez NSA do atakowania komputerów z systemem Windows przez sieć.

</div>

Ten rodzaj ataku może być przeprowadzony na kilka sposobów:

1. Współtwórca lub pracownik może najpierw wypracować sobie pozycję wpływu w projekcie lub organizacji, a następnie nadużyć jej, dodając złośliwy kod.
2. Deweloper może zostać zmuszony przez podmiot zewnętrzny do dodania złośliwego kodu.
3. Osoba lub grupa może zidentyfikować zależność zewnętrzną (bibliotekę) i spróbować ją zainfiltrować powyższymi metodami, wiedząc, że zostanie użyta przez deweloperów na szczeblu „downstream”.

Tego rodzaju ataki mogą wymagać dużo czasu i przygotowań oraz są ryzykowne, bo można je wykryć — szczególnie w popularnych projektach open source, na które zwraca się uwagę z zewnątrz. Niestety są też jednymi z najgroźniejszych, ponieważ trudno je całkowicie wyeliminować. Zalecamy korzystanie tylko z oprogramowania o dobrej reputacji, które podejmuje wysiłki zmniejszające ryzyko, na przykład poprzez:

1. Przyjmowanie wyłącznie popularnego oprogramowania, które istnieje od dłuższego czasu. Im większe zainteresowanie projektem, tym większe prawdopodobieństwo, że zewnętrzne podmioty zauważą złośliwe zmiany — a cyberprzestępca będzie musiał poświęcić więcej czasu, żeby zdobyć zaufanie społeczności poprzez znaczący wkład.
2. Wybieranie oprogramowania, które publikuje wydania binarne przy użyciu powszechnie stosowanych, zaufanych platform do kompilacji, zamiast z maszyn deweloperskich czy serwerów hostowanych samodzielnie. Niektóre systemy, jak GitHub Actions, umożliwiają publiczne sprawdzenie skryptu kompilacji, co daje dodatkową pewność. Zmniejsza to prawdopodobieństwo, że złośliwe oprogramowanie na maszynie dewelopera zainfekuje pakiety, i zwiększa pewność, że wersje binarne zostały poprawnie utworzone.
3. Szukanie podpisywania kodu dla pojedynczych commitów i wydań, co tworzy możliwy do skontrolowania ślad, kto co zrobił, np. czy złośliwy kod znajdował się w repozytorium oprogramowania,  który deweloper go dodał,  albo czy został wprowadzony w procesie kompilacji.
4. Sprawdzanie, czy historia commitów zawiera sensowne komunikaty (takie jak [conventional commits](https://conventionalcommits.org)), które wyjaśniają, co ma osiągnąć każda zmiana. Jasne komunikaty ułatwiają osobom postronnym weryfikację, audyt i odnajdywanie błędów.
5. Zwracanie uwagi na liczbę współtwórców i maintainerów projektu. Samotny deweloper może być bardziej podatny na przymus dodania złośliwego kodu przez podmiot zewnętrzny lub na niedbalstwo umożliwiające niepożądane zachowania — co często oznacza, że oprogramowanie tworzone przez tzw. *Big Tech* podlega większej kontroli niż projekt jednego dewelopera, który nie odpowiada przed nikim.

## Prywatność ze strony dostawców usług

<span class="pg-teal">:material-server-network: Dostawcy usług</span>

Żyjemy w świecie, w którym prawie wszystko jest podłączone do Internetu. Nasze „prywatne” wiadomości, e-maile i interakcje społeczne zwykle są przechowywane na serwerze — gdzieś. Zwykle, gdy wysyłasz komuś wiadomość, jest ona zapisywana na serwerze, a kiedy twój znajomy chce ją przeczytać, serwer mu ją dostarcza.

Oczywisty problem polega na tym, że dostawca usługi (albo haker, który włamał się na serwer) może uzyskać dostęp do twoich rozmów w dowolnym momencie i na dowolny sposób, bez twojej wiedzy. Dotyczy to wielu popularnych usług, jak SMS, Telegram czy Discord.

Na szczęście E2EE może złagodzić ten problem, szyfrując komunikację między tobą a wybranymi odbiorcami jeszcze zanim dane trafią na serwer. Poufność twoich wiadomości jest wtedy gwarantowana, pod warunkiem, że dostawca usługi nie ma dostępu do prywatnych kluczy żadnej ze stron.

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga dotycząca szyfrowania w aplikacjach webowych</p>

W praktyce skuteczność różnych implementacji E2EE bywa różna. Aplikacje takie jak [Signal](../real-time-communication.md#signal) działają natywnie na twoim urządzeniu, a każda kopia aplikacji jest taka sama we wszystkich instalacjach. Gdyby dostawca usługi wprowadził w aplikacji tzw. [*backdoora*](https://en.wikipedia.org/wiki/Backdoor_(computing)) — w celu kradzieży twoich prywatnych kluczy — można by to później wykryć za pomocą [inżynierii wstecznej](https://pl.wikipedia.org/wiki/Inżynieria_odwrotna).

Z drugiej strony webowe implementacje E2EE, jak aplikacja webowa Proton Mail czy *Web Vault* Bitwardena, polegają na tym, że serwer dynamicznie dostarcza kod JavaScript do przeglądarki, który obsługuje kryptografię. Złośliwy serwer może wysłać Ci specjalny, zainfekowany kod JavaScript, aby ukraść Twój klucz szyfrujący (i bardzo trudno byłoby to zauważyć). Ponieważ serwer może serwować różne wersje klienta webowego różnym użytkownikom — nawet jeśli zauważy się atak, trudno byłoby udowodnić winę dostawcy.

Dlatego, gdy tylko jest to możliwe, należy używać aplikacji natywnych zamiast klientów webowych.

</div>

Nawet przy E2EE dostawcy usług nadal mogą profilować Cię na podstawie **metadanych**, które zwykle nie są chronione. Choć dostawca nie może odczytać treści wiadomości, może obserwować istotne informacje, takie jak z kim rozmawiasz, jak często i kiedy zazwyczaj jesteś aktywny. Ochrona metadanych jest raczej rzadkością — jeśli ma to znaczenie w twoim [modelu zagrożeń](threat-modeling.md), zwróć szczególną uwagę na dokumentację techniczną używanego oprogramowania, aby sprawdzić, czy w ogóle istnieje jakakolwiek minimalizacja lub ochrona metadanych.

## Systemy masowej inwigilacji

<span class="pg-blue">:material-eye-outline: Masowa inwigilacja</span>

Masowa inwigilacja to złożone działanie polegające na monitorowaniu „zachowań, wielu aktywności lub informacji” całej (lub znaczącej części) populacji[^1]. Często odnosi się do programów rządowych, takich jak te [ujawnione przez Edwarda Snowdena w 2013 roku](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Może być jednak prowadzona także przez korporacje — zarówno na zlecenie agencji rządowych, jak i z własnej inicjatywy.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

Jeśli mieszkasz w USA i chcesz dowiedzieć się więcej o metodach inwigilacji i o tym, jak są wdrażane w Twoim mieście, możesz też zapoznać się z [Atlas of Surveillance](https://atlasofsurveillance.org) (dosł. Atlas inwigilacji) przygotowany przez [Electronic Frontier Foundation](https://eff.org).

We Francji warto zajrzeć na stronę [Technopolice](https://technopolice.fr/villes) prowadzoną przez stowarzyszenie non-profit La Quadrature du Net.

</div>

Rządy często uzasadniają systemy masowej inwigilacji koniecznością walki z terroryzmem i zapobiegania przestępstwom. Jednak jako naruszenie praw człowieka najczęściej są wykorzystywane do niewspółmiernego celowania w m.in. mniejszości i dysydentów politycznych.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

W świetle ujawnień Edwarda Snowdena dotyczących programów rządowych, takich jak [PRISM](https://en.wikipedia.org/wiki/PRISM) i [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), przedstawiciele służb wyznali również, że NSA przez lata potajemnie gromadziła dane dotyczące praktycznie wszystkich amerykańskich połączeń telefonicznych — kto z kim dzwonił, kiedy te połączenia miały miejsce i jak długo trwały. Tego rodzaju informacje, gromadzone przez NSA dzień po dniu, mogą ujawnić niezwykle wrażliwe szczegóły dotyczące życia i powiązań między ludzi, na przykład czy dzwonili do pastora, do placówki wykonującej zabiegi aborcyjne, do terapeuty ds. uzależnień czy na telefon zaufania dla samobójców.

</div>

Pomimo rosnącej skali masowej inwigilacji w Stanach Zjednoczonych, rząd stwierdził, że systemy masowej inwigilacji, takie jak Sekcja 215, miały „niewielką unikalną wartość” w kontekście powstrzymywania rzeczywistych przestępstw czy spisków terrorystycznych — ich działania w dużej mierze dublowały ukierunkowane programy inwigilacji FBI[^2].

W sieci możesz być śledzony za pomocą różnych metod, w tym między innymi:

- Twojego adresu IP
- plików cookie przeglądarki
- danych, które przesyłasz na strony internetowe
- odcisku przeglądarki lub urządzenia
- korelacji metod płatności

Jeśli obawiasz się systemów masowej inwigilacji, możesz zastosować następujące zalecenia: oddzielać swoje tożsamości online, wtapiać się w tłum innych użytkowników lub, gdy to możliwe, po prostu unikać podawania informacji identyfikujących.

## Inwigilacja jako model biznesowy

<span class="pg-brown">:material-account-cash: Kapitalizm inwigilacji</span>

> Kapitalizm inwigilacji to system gospodarczy oparty na przechwytywaniu i utowarowieniu danych osobowych w celach zarobkowych[^3].

Dla wielu osób śledzenie i inwigilacja przez prywatne korporacje stają się coraz większym problemem. Wszechobecne sieci reklamowe, takie jak te obsługiwane przez Google i Facebook, obejmują Internet znacznie szerzej niż tylko serwisy, które kontrolują — śledząc Twoje działania po drodze. Korzystanie z narzędzi takich jak blokery treści w celu ograniczania żądań sieciowych do ich serwerów oraz zapoznawanie się z polityką prywatności usług, z których korzystasz, może pomóc uniknąć wielu podstawowych przeciwników (choć nie zapobiegnie śledzeniu całkowicie)[^4].

Dodatkowo nawet firmy spoza branży *AdTech* czy klasycznych podmiotów śledzących mogą udostępniać Twoje dane [brokerom danych](https://en.wikipedia.org/wiki/Information_broker) (takim jak Cambridge Analytica, Experian czy Datalogix) lub innym podmiotom. Nie możesz automatycznie zakładać, że Twoje dane są bezpieczne tylko dlatego, że usługa, z której korzystasz, nie wpisuje się w typowy model biznesowy AdTech lub śledzenia. Najskuteczniejszą ochroną przed korporacyjnym gromadzeniem danych jest szyfrowanie lub zaciemnianie danych zawsze, gdy to możliwe, co utrudnia różnym dostawcom korelowanie między sobą informacji i budowanie profilu na Twój temat.

## Ograniczanie informacji publicznych

<span class="pg-green">:material-account-search: Ekspozycja publiczna</span>

Najlepszym sposobem, by zachować prywatność danych, jest po prostu nie udostępniać ich publicznie w pierwszej kolejności. Usuwanie niechcianych informacji, które znajdziesz o sobie w sieci, to jeden z najlepszych pierwszych kroków do odzyskania prywatności.

- [Zobacz nasz przewodnik dotyczący usuwania kont :material-arrow-right-drop-circle:](account-deletion.md)

Na stronach, gdzie udostępniasz informacje, bardzo ważne jest sprawdzenie ustawień prywatności konta, by ograniczyć zasięg ich rozpowszechniania. Na przykład włącz „tryb prywatny” na kontach, jeśli taka opcja jest dostępna: to sprawi, że Twoje konto nie będzie indeksowane przez wyszukiwarki i nie będzie można go oglądać bez Twojej zgody.

Jeśli już podałeś(-aś) swoje prawdziwe dane w miejscach, gdzie nie powinno się ich ujawniać, rozważ stosowanie taktyk dezinformacyjnych, na przykład podawanie fikcyjnych informacji powiązanych z tą tożsamością online. To sprawia, że Twoje prawdziwe dane stają się nieodróżnialne od fałszywych.

## Unikanie cenzury

<span class="pg-blue-gray">:material-close-outline: Cenzura</span>

Cenzura w sieci może być stosowana (w różnym stopniu) przez podmioty takie jak totalitarne rządy, administratorzy sieci czy dostawcy usług. Te wysiłki mające na celu kontrolowanie komunikacji i ograniczanie dostępu do informacji zawsze będą sprzeczne z prawem człowieka do wolności wypowiedzi[^5].

Cenzura na platformach korporacyjnych jest coraz powszechniejsza — platformy takie jak Twitter i Facebook ulegają naciskom opinii publicznej, presjom rynkowym oraz naciskom ze strony agencji rządowych. Naciski ze strony rządu mogą przybierać formę ukrytych żądań wobec firm, jak np. [wniosek Białego Domu o usunięcie](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) prowokacyjnego filmu na YouTube, albo formę jawną, jak w przypadku chińskiego rządu wymagającego od firm ścisłego przestrzegania reżimu cenzury.

Osoby obawiające się ryzyka cenzury mogą używać technologii takich jak sieć [Tor](../advanced/tor-overview.md) do jej ominięcia i wspierać platformy odporne na cenzurę, np. [Matrix](../social-networks.md#element), które nie mają scentralizowanego organu zdolnego arbitralnie zamykać kont.

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Choć ominięcie cenzury samo w sobie może być proste, ukrycie faktu, że to robisz, bywa bardzo problematyczne.

Warto rozważyć, które części sieci może obserwować Twój przeciwnik oraz czy możesz wiarygodnie zaprzeczyć swoim działaniom. Na przykład korzystanie z [szyfrowanego DNS](../advanced/dns-overview.md#what-is-encrypted-dns) może pomóc obejść proste systemy cenzury oparte na DNS, ale nie ukryje przed twoim ISP tego, co odwiedzasz. VPN lub Tor mogą ukryć odwiedzane zasoby przed administratorami sieci, lecz nie ukryją faktu, że w ogóle korzystasz z tych sieci. Transporty wtykowe (ang. *pluggable transports*; takie jak Obfs4proxy, Meek czy Shadowsocks) mogą pomóc ominąć zapory blokujące popularne protokoły VPN lub Tor, ale Twoje próby obejścia mogą być nadal wykryte przez metody takie jak sondowanie czy [głęboka inspekcja pakietów](https://pl.wikipedia.org/wiki/Głęboka_inspekcja_pakietów).

</div>

Zawsze musisz rozważyć ryzyko związane z próbą ominięcia cenzury, możliwe konsekwencje oraz to, jak zaawansowany jest Twój przeciwnik. Bądź ostrożny przy wyborze oprogramowania i miej plan awaryjny na wypadek przyłapania.

[^1]: Anglojęzyczna Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) i [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: [*Sprawozdanie Rady Nadzoru nad Prywatnością i Wolnościami Obywatelskimi dotyczące programu hurtowego gromadzenia danych telefonicznych na mocy sekcji 215 ustawy USA PATRIOT*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Anglojęzyczna Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: „[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)” (dosł. „wyliczanie zła”, czyli „wypisywanie wszystkich znanych nam zagrożeń”), jak robi to wiele blokerów treści i programów antywirusowych, nie chroni Cię wystarczająco przed nowymi i nieznanymi zagrożeniami, ponieważ nie zostały one jeszcze dodane do listy filtrów. Należy stosować też inne techniki łagodzące ryzyko.
[^5]: Organizacja Narodów Zjednoczonych: [*Powszechna Deklaracja Praw Człowieka*](https://www.unic.un.org.pl/dokumenty/deklaracja.php).
