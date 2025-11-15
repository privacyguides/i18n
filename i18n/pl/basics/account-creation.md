---
meta_title: "Jak prywatnie zakładać konta w Internecie — Privacy Guides"
title: "Zakładanie konta"
icon: 'material/account-plus'
description: Zakładanie kont w sieci to niemal konieczność — wykonaj poniższe kroki, aby upewnić się, że zachowujesz prywatność.
---

Często ludzie rejestrują się w usługach bez zastanowienia. Może to być serwis streamingowy, żeby obejrzeć nowy serial, o którym wszyscy mówią, albo konto, które daje zniżkę w ulubionej sieci fast food. Niezależnie od powodu, warto przemyśleć konsekwencje dla swoich danych — teraz i w przyszłości.

Każda nowa usługa, z której korzystasz, niesie ze sobą ryzyko. Naruszenia danych, ujawnienie informacji o klientach stronom trzecim, dostęp do danych przez nieuczciwych pracowników — to wszystko to realne możliwości, które trzeba brać pod uwagę, podając swoje dane. Musisz mieć pewność, że możesz zaufać danej usłudze, dlatego nie zalecamy przechowywania cennych danych nigdzie indziej niż na najbardziej dojrzałych i sprawdzonych produktach. Zazwyczaj chodzi o usługi oferujące szyfrowanie E2EE i poddane audytowi kryptograficznemu. Audyt zwiększa pewność, że produkt został zaprojektowany bez rażących błędów bezpieczeństwa wynikających z braku doświadczenia twórców.

Usunięcie konta w niektórych usługach też bywa trudne. Czasem możliwe jest [nadpisanie danych](account-deletion.md#overwriting-account-information) powiązanych z kontem, ale w innych przypadkach usługa będzie przechowywać całą historię zmian konta.

## Warunki korzystania z usługi i polityka prywatności

Warunki korzystania z usługi (ToS) to zasady, których zgadzasz się przestrzegać, korzystając z serwisu. W większych usługach te zasady często egzekwowane są przez systemy zautomatyzowane. Czasami takie systemy popełniają błędy. Na przykład możesz zostać zbanowany lub zablokowany na swoim koncie za korzystanie z VPN lub numeru VoIP. Odwoływanie się od takich banów jest często trudne i również przebiega automatycznie, co nie zawsze kończy się sukcesem. To jedna z przyczyn, dla których nie zalecamy używania Gmaila jako przykładowej skrzynki e-mail. E-mail jest kluczowy dla dostępu do innych usług, z których być może korzystasz.

Polityka prywatności określa, w jaki sposób usługa zamierza wykorzystywać Twoje dane, więc warto ją przeczytać, aby zrozumieć, jak będą one używane. Firma lub organizacja może nie być prawnie zobowiązana do przestrzegania wszystkiego, co znajduje się w polityce (zależy to od jurysdykcji). Zalecamy zapoznanie się z lokalnymi przepisami i tym, co pozwalają one dostawcy zbierać.

Zalecamy wyszukiwać w polityce konkretne terminy, takie jak „gromadzenie danych”, „analiza danych”, „pliki cookies”/„ciasteczka”, „reklamy” czy usługi „stron trzecich”. Czasami możesz mieć możliwość rezygnacji z gromadzenia danych lub z ich udostępniania, ale najlepiej wybrać usługę, która od samego początku szanuje Twoją prywatność.

Pamiętaj też, że powierzasz zaufanie firmie lub organizacji i zakładasz, że będzie ona przestrzegać własnej polityki prywatności.

## Metody uwierzytelniania

Zazwyczaj istnieje kilka sposobów założenia konta, z których każdy ma swoje wady i zalety.

### E-mail i hasło

Najczęstszym sposobem utworzenia nowego konta jest podanie adresu e-mail i hasła. Korzystając z tej metody, należy używać menedżera haseł i stosować się do [zaleceń dotyczących haseł](passwords-overview.md).

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Menedżer haseł możesz też wykorzystać do uporządkowania innych metod uwierzytelniania! Wystarczy dodać nowy wpis i wypełnić odpowiednie pola. Możesz dodać także notatki do takich rzeczy jak pytania zabezpieczające czy klucz zapasowy.

</div>

Będziesz odpowiadać za zarządzanie swoimi danymi logowania. Dla zwiększenia bezpieczeństwa możesz włączyć [uwierzytelnianie wieloskładnikowe](multi-factor-authentication.md) na swoich kontach.

[Zalecane menedżery haseł](../passwords.md ""){.md-button}

#### Aliasy e-mail

Jeśli nie chcesz podawać swojego prawdziwego adresu e-mail usłudze, możesz użyć aliasu. Opisujemy je bardziej szczegółowo na naszej stronie z zaleceniami dotyczącymi usług e-mail. W skrócie: usługi aliasów pozwalają generować nowe adresy e-mail, które przekierowują wszystkie wiadomości na Twój główny adres. Pomaga to zapobiegać śledzeniu między usługami i ułatwia zarządzanie wiadomościami marketingowymi, które czasem pojawiają się w procesie rejestracji. Można je filtrować automatycznie na podstawie aliasu, na który zostały wysłane.

Jeśli jakaś usługa zostanie zhakowana, możesz zacząć otrzymywać na użyty adres wiadomości phishingowe lub spam. Korzystanie z unikalnych aliasów dla każdej usługi ułatwia dokładne ustalenie, która usługa została zhakowana.

[Zalecane usługi aliasingu e-mail](../email-aliasing.md ""){.md-button}

### „Zaloguj się za pomocą...” (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) to otwarty protokół uwierzytelniania, który pozwala zarejestrować się w usłudze bez udostępniania jej wielu informacji (jeśli w ogóle), przez użycie istniejącego konta u innego dostawcy. Kiedy w formularzu rejestracji widzisz coś w stylu „Zaloguj się za pomocą *nazwa dostawcy*”, zwykle oznacza to użycie OAuth.

Kiedy logujesz się za pomocą OAuth, otworzy się strona logowania u wybranego dostawcy, a twoje istniejące konto i nowe konto zostaną powiązane. Twoje hasło nie będzie udostępnione, ale zwykle przekazywane są pewne podstawowe informacje (możesz je sprawdzić podczas żądania logowania). Ten proces jest konieczny za każdym razem, gdy chcesz zalogować się na to samo konto.

Główne zalety to:

- **Bezpieczeństwo**: Nie musisz ufać praktykom bezpieczeństwa usługi, do której się logujesz, jeśli chodzi o przechowywanie danych logowania, ponieważ są one przechowywane u zewnętrznego dostawcy OAuth. Popularni dostawcy OAuth, tacy jak Apple czy Google, zwykle stosują najlepsze praktyki bezpieczeństwa, regularnie audytują swoje systemy uwierzytelniania i nie przechowują danych uwierzytelniających w nieodpowiedni sposób (np. w postaci zwykłego tekstu).
- **Wygoda**: Możesz zarządzać wieloma kontami za pomocą jednego logowania.

Są jednak wady:

- **Prywatność**: Dostawca OAuth, za pomocą którego się logujesz, będzie wiedział, z jakich usług korzystasz.
- **Centralizacja**: Jeśli konto używane do OAuth zostanie przejęte lub nie będziesz mógł się na nie zalogować, wszystkie inne konta powiązane z nim są zagrożone.

OAuth może być szczególnie przydatny tam, gdzie korzystasz z głębszej integracji między usługami. Zalecamy ograniczyć używanie OAuth tylko do sytuacji, w których jest to konieczne, i zawsze chronić konto główne przy pomocy [MFA](multi-factor-authentication.md).

Wszystkie usługi korzystające z OAuth będą tak bezpieczne, jak konto Twojego dostawcy OAuth. Na przykład, jeśli chcesz zabezpieczyć konto kluczem sprzętowym, ale dana usługa ich nie obsługuje, możesz zabezpieczyć konto, którego używasz z OAuth, kluczem sprzętowym, przez co w praktyce masz teraz sprzętowe uwierzytelnianie wieloskładnikowe na wszystkich powiązanych kontach. Warto jednak pamiętać, że słabe uwierzytelnienie konta u dostawcy OAuth oznacza, że każde konto powiązane z tym logowaniem również będzie słabe.

Dodatkowe niebezpieczeństwo przy używaniu *Zaloguj się za pomocą Google*, *Facebook* czy innej usługi polega na tym, że proces OAuth zwykle umożliwia *dwukierunkowe* udostępnianie danych. Na przykład zalogowanie się na forum za pomocą konta Twitter może dać temu forum uprawnienia do wykonywania działań na twoim koncie Twitter — np. publikowania postów, czytania wiadomości lub dostępu do innych danych osobowych. Dostawcy OAuth zwykle pokażą listę uprawnień, które przyznajesz zewnętrznej usłudze, więc zawsze dokładnie ją przeczytaj i nie przyznawaj przypadkowo dostępu do niczego, czego usługa nie potrzebuje.

Złośliwe aplikacje, szczególnie na urządzeniach mobilnych, gdzie aplikacja ma dostęp do sesji WebView używanej do logowania u dostawcy OAuth, mogą również nadużyć tego procesu, przejmując Twoją sesję u dostawcy OAuth i w ten sposób uzyskując dostęp do Twojego konta OAuth. Korzystanie z opcji *Zaloguj się za pomocą* dowolnego dostawcy powinno być traktowane jako wygoda, której używasz jedynie w przypadku usług, którym ufasz i które nie są aktywnie złośliwe.

### Numer telefonu

Zalecamy unikać usług, które wymagają podania numeru telefonu przy rejestracji. Numer telefonu może Cię identyfikować w różnych usługach, a w zależności od umów o udostępnianiu danych ułatwi to śledzenie Twojej aktywności, szczególnie jeśli któraś z tych usług zostanie zhakowana, ponieważ numer często **nie jest** szyfrowany.

Należy unikać podawania prawdziwego numeru telefonu, jeśli to możliwe. Niektóre usługi zezwalają na użycie numerów VoIP, jednak często uruchamia to systemy wykrywania oszustw i prowadzi do zablokowania konta, dlatego nie zalecamy tego dla ważnych kont.

W wielu przypadkach konieczne będzie podanie numeru, na który możesz otrzymać SMS-y lub połączenia — zwłaszcza przy zakupach międzynarodowych, na wypadek problemów z zamówieniem na odprawie granicznej. Usługi często używają numeru jako metody weryfikacji; nie ryzykuj utraty dostępu do ważnego konta tylko dlatego, że chciałeś być sprytny i podałeś fałszywy numer!

### Nazwa użytkownika i hasło

Niektóre usługi pozwalają zarejestrować się bez adresu e-mail, wymagając jedynie nazwy użytkownika i hasła. Takie usługi mogą zapewniać większą anonimowość w połączeniu z VPN lub Torem. Pamiętaj jednak, że w przypadku takich kont najprawdopodobniej **nie będzie możliwości odzyskania konta**, jeśli zapomnisz nazwę użytkownika lub hasło.
