---
title: "Najczęstsze błędne przekonania"
icon: 'material/robot-confused'
description: Prywatność nie jest prostym tematem — łatwo dać się zwieść hasłom marketingowym i dezinformacji.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Czy oprogramowanie open-source jest z definicji bezpieczne?
        acceptedAnswer:
          "@type": Answer
          text: |
            Dostępność kodu źródłowego i sposób licencjonowania same w sobie nie wpływają bezpośrednio na bezpieczeństwo. Oprogramowanie open-source może być bezpieczniejsze od zamkniętego, ale nie ma żadnej gwarancji, że tak będzie. Oceniając program, warto rozpatrywać reputację i poziom bezpieczeństwa każdego narzędzia indywidualnie.
      - 
        "@type": Question
        name: Czy przeniesienie zaufania na innego dostawcę może zwiększyć prywatność?
        acceptedAnswer:
          "@type": Answer
          text: |
            Często mówimy o „przenoszeniu zaufania” w kontekści narzędzi takich jak VPN (które przenoszą zaufanie, jakie pokładasz w swoim dostawcy usług internetowych, na dostawcę VPN). Choć chroni to Twoje dane przeglądania przed ISP, wybrany dostawca VPN nadal ma do nich dostęp — Twoje dane nie są więc całkowicie zabezpieczone przed wszystkimi podmiotami.
      - 
        "@type": Question
        name: Czy rozwiązania nastawione na prywatność są z natury godne zaufania?
        acceptedAnswer:
          "@type": Answer
          text: |
            Skupianie się wyłącznie na politykach prywatności i marketingu danego narzędzia lub dostawcy może przysłonić jego słabości. Szukając bardziej prywatnego rozwiązania, najpierw ustal, jaki jest podstawowy problem, i dobierz techniczne środki do jego rozwiązania. Na przykład możesz chcieć unikać Dysku Google, ponieważ daje on Google dostęp do wszystkich Twoich danych. Zasadniczym problemem w tym przypadku jest brak szyfrowania end-to-end (E2EE), więc upewnij się, że wybrany dostawca, na którego się przenosisz, rzeczywiście implementuje E2EE, albo użyj narzędzia (np. Cryptomator), które zapewnia E2EE niezależnie od chmury. Przejście na „dostawcę nastawionego na prywatność”, który nie wdraża E2EE, nie rozwiązuje problemu — jedynie przenosi zaufanie z Google na tego dostawcę.
      - 
        "@type": Question
        name: Jak skomplikowany powinien być mój model zagrożeń?
        acceptedAnswer:
          "@type": Answer
          text: |
            Często widzimy, że ludzie opisują modele zagrożeń dotyczące prywatności, które są przesadnie skomplikowane. Zwykle obejmują one np. wiele różnych kont e-mail lub skomplikowane konfiguracje z wieloma ruchomymi elementami i warunkami. Odpowiedzi są zazwyczaj odpowiedziami na pytania typu „Jaki jest najlepszy sposób na X?”.
            Znalezienie „najlepszego” rozwiązania nie musi oznaczać dążenia do nieomylnego systemu z dziesiątkami warunków — takie rozwiązania często są trudne w praktycznym użyciu. Jak już wspomniano, bezpieczeństwo często idzie kosztem wygody.
---

## „Oprogramowanie open-source jest zawsze bezpieczne” albo „Oprogramowanie własnościowe jest bezpieczniejsze”

Te mity wynikają z różnych uprzedzeń, ale dostępność kodu źródłowego i sposób licencjonowania nie mają samych w sobie żadnego wrodzonego wpływu na bezpieczeństwo. ==Oprogramowanie open-source może być *potencjalnie* bezpieczniejsze niż oprogramowanie własnościowe, ale nie ma absolutnie żadnej gwarancji, że tak faktycznie będzie.== Ocena bezpieczeństwa powinna się odbywać osobno dla każdego narzędzia, z uwzględnieniem jego reputacji i rzeczywistych standardów bezpieczeństwa.

Oprogramowanie open-source *może* być analizowane przez niezależne podmioty i zwykle jest bardziej przejrzyste pod kątem potencjalnych podatności niż jego zamknięte odpowiedniki. Umożliwia też samodzielny przegląd kodu i wyłączenie podejrzanych funkcji. Jednak *jeśli tego nie zrobisz*, nie ma żadnej gwarancji, że kod został kiedykolwiek rzetelnie oceniony, zwłaszcza w przypadku mniejszych projektów. Otwarty proces rozwoju bywał również wykorzystywany do wprowadzania nowych podatności w ramach tzw. [:material-package-variant-closed-remove: Ataków na łańcuch dostaw](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, o których więcej piszemy na stronie [Najczęstsze zagrożenia](common-threats.md)[^1].

Z drugiej strony oprogramowanie własnościowe jest mniej przejrzyste, ale nie oznacza to automatycznie, że jest niebezpieczne. Duże projekty komercyjne mogą podlegać audytom wewnętrznym i zewnętrznym, a niezależni badacze bezpieczeństwa wciąż mogą wykrywać podatności za pomocą metod takich jak inżynieria wsteczna.

Aby uniknąć nieobiektywnych decyzji, *kluczowe* jest, by oceniać standardy prywatności i bezpieczeństwa każdego używanego narzędzia.

## „Przenoszenie zaufania może zwiększyć prywatność”

Często mówimy o „przenoszeniu zaufania” w kontekści narzędzi takich jak VPN (które przenoszą zaufanie, jakie pokładasz w swoim dostawcy usług internetowych, na dostawcę VPN). Choć chroni to Twoje dane przeglądania przed *konkretnie* ISP, wybrany dostawca VPN nadal ma do nich dostęp — Twoje dane nie są więc całkowicie zabezpieczone przed wszystkimi podmiotami. Oznacza to, że:

1. Wybierając dostawcę, któremu chcesz zaufać, musisz zachować ostrożność.
2. Należy nadal korzystać z innych technik, jak E2EE, aby rzeczywiście zabezpieczyć swoje dane. Samo odrzucenie jednego dostawcy na rzecz drugiego nie zapewnia bezpieczeństwa.

## „Rozwiązania nastawione na prywatność są z natury godne zaufania”

Skupianie się wyłącznie na politykach prywatności i marketingu danego narzędzia lub dostawcy może przysłonić jego słabości. Szukając bardziej prywatnego rozwiązania, najpierw ustal, jaki jest podstawowy problem, i dobierz techniczne środki do jego rozwiązania. Na przykład możesz chcieć unikać Dysku Google, ponieważ daje on Google dostęp do wszystkich Twoich danych. Zasadniczym problemem w tym przypadku jest brak szyfrowania end-to-end (E2EE), więc upewnij się, że wybrany dostawca, na którego się przenosisz, rzeczywiście implementuje E2EE, albo użyj narzędzia (np. [Cryptomator](../encryption.md#cryptomator-cloud)), które zapewnia E2EE niezależnie od chmury. Przejście na „dostawcę nastawionego na prywatność”, który nie wdraża E2EE, nie rozwiązuje problemu — jedynie przenosi zaufanie z Google na tego dostawcę.

Polityki prywatności i praktyki biznesowe wybranych dostawców są oczywiście istotne, ale powinny ustępować miejsca technicznym gwarancjom prywatności. Nie ma sensu przenosić zaufania na innego dostawcę tam, gdzie zaufanie do dostawcy w ogóle nie jest potrzebne.

## „Skomplikowane jest lepsze”

Często widzimy, że ludzie opisują modele zagrożeń dotyczące prywatności, które są przesadnie skomplikowane. Zwykle obejmują one np. wiele różnych kont e-mail lub skomplikowane konfiguracje z wieloma ruchomymi elementami i warunkami. Odpowiedzi są zazwyczaj odpowiedziami na pytania typu „Jaki jest najlepszy sposób na *X*?”.

Znalezienie „najlepszego” rozwiązania nie musi oznaczać dążenia do nieomylnego systemu z dziesiątkami warunków — takie rozwiązania często są trudne w praktycznym użyciu. Jak już wspomniano, bezpieczeństwo często idzie kosztem wygody. Poniżej przedstawiamy kilka porad:

1. ==Działania muszą służyć konkretnemu celowi:== zastanów się, jak osiągnąć to, co chcesz, przy jak najmniejszej liczbie działań.
2. ==Usuń punkty podatne na błąd ludzki:== zawalamy, męczymy się i zapominamy. Aby zachować bezpieczeństwo, unikaj polegania na ręcznych warunkach i procesach, które musisz pamiętać.
3. ==Używaj odpowiedniego poziomu ochrony do zamierzonego celu:== często widzimy zalecenia dotyczące tzw. rozwiązań „odpornych na organy ścigania” lub „odpornych na wezwania sądowe”. Takie rozwiązania zwykle wymagają specjalistycznej wiedzy i z reguły nie są tym, czego ludzie naprawdę potrzebują. Nie ma sensu budować skomplikowanego modelu zagrożeń dla anonimowości, jeśli można zostać zdeanonimizowanym przez proste przeoczenie.

Jak to może wyglądać w praktyce?

Jeden z najjaśniejszych sposobów opisu modelu zagrożeń to rozróżnienie sytuacji, w których ludzie *znają Twoją tożsamość*, i tych, w których jej nie znają. Zawsze będą sytuacje, w których musisz podać swoje prawne imię i nazwisko, oraz te, gdzie nie jest to konieczne.

1. **Znana tożsamość** — znana tożsamość jest używana tam, gdzie musisz podać swoje imię i nazwisko. Istnieje wiele dokumentów prawnych i umów, w których wymagana jest tożsamość prawna: otwarcie konta bankowego, podpisanie umowy najmu, uzyskanie paszportu, deklaracje celne przy imporcie przedmiotów czy inne kontakty z instytucjami państwowymi. Takie sytuacje zwykle prowadzą do powstania poświadczeń, jak karty płatnicze, sprawdzenia zdolności kredytowej, numery kont czy ewentualnie adresy fizyczne.

    Nie zalecamy używania VPN ani sieci Tor do tych czynności, ponieważ Twoja tożsamość i tak jest ujawniona innymi kanałami.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Porada</p>

    Podczas zakupów online korzystanie z [paczkomatu](https://pl.wikipedia.org/wiki/Automat_paczkowy) może pomóc chronić Twój adres fizyczny.

    </div>

2. **Nieznana tożsamość** — nieznana tożsamość może być stałym pseudonimem, którego regularnie używasz. Nie jest to anonimowość, ponieważ pseudonim się nie zmienia. Jeśli jesteś częścią społeczności online, możesz chcieć zachować osobowość, którą inni znają. Ten pseudonim nie jest anonimowy, ponieważ po dłuższym monitoringu można wywnioskować dodatkowe informacje o jego właścicielu — sposób pisania, zakres wiedzy, zainteresowania itp.

    W takim przypadku możesz użyć VPN, by ukryć swój adres IP. Transakcje finansowe są trudniejsze do zamaskowania: można rozważyć użycie anonimowych kryptowalut, takich jak [Monero](../cryptocurrency.md#monero). Przemieszczanie środków między altcoinami może również pomóc ukryć źródło pochodzenia środków. Zazwyczaj giełdy wymagają przeprowadzenia procedury KYC (poznaj swojego klienta) zanim pozwolą na wymianę waluty fiducjarnej na kryptowaluty. Lokalne spotkania twarzą w twarz mogą być alternatywą; jednak często są droższe i czasem również wymagają KYC.

3. **Anonimowa tożsamość** — nawet mając doświadczenie, utrzymanie anonimowej tożsamości przez dłuższy czas jest trudne. Powinny to być tożsamości krótkoterminowe i krótkotrwałe, które są regularnie zmieniane.

    Korzystanie z Tora może w tym pomóc. Warto też zauważyć, że większą anonimowość daje komunikacja asynchroniczna: komunikacja w czasie rzeczywistym jest podatna na analizę wzorców pisania (np. dłuższe fragmenty tekstu publikowane na forum, w e-mailu itp.).

[^1]: Znaczący atak na łańcuch dostaw miał miejsce w marcu 2024 r., gdy złośliwy opiekun projektu wprowadził zawoalowany backdoor do `xz` — popularnej biblioteki kompresji. Backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) miał na celu umożliwić nieznanemu podmiotowi zdalny dostęp do większości serwerów Linux przez SSH, ale został wykryty, zanim zdążył zostać szeroko rozpowszechniony.
