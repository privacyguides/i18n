---
title: Wprowadzenie do haseł
icon: material/form-textbox-password
description: Oto kilka praktycznych porad i wskazówek, jak tworzyć najsilniejsze hasła i chronić swoje konta.
---

Hasła są nieodłącznym elementem naszego cyfrowego życia. Chronią one nasze konta, urządzenia i prywatne informacje. Mimo że często są jedyną przeszkodą między nami a osobą próbującą pozyskać nasze dane, nie poświęca się im wystarczająco dużo uwagi, co często prowadzi do używania haseł łatwych do odgadnięcia lub złamania atakiem brute force.

## Zalecenia

### Używaj unikatowych haseł dla każdej usługi

Wyobraź sobie: zakładasz konto, używając tego samego adresu e-mail i hasła w kilku usługach. Jeśli któryś z tych dostawców będzie złośliwy albo dojdzie u niego do wycieku danych ujawniającego hasła w postaci niezaszyfrowanej, osoba atakująca wystarczy, że wypróbuje tę kombinację e-mail i hasła na wielu popularnych stronach, aż trafi na pasujące konto. Nie ma znaczenia, jak silne jest to pojedyncze hasło, bo atakujący już je ma.

To zjawisko nazywa się [upychaniem danych uwierzytelniających](https://en.wikipedia.org/wiki/Credential_stuffing) (ang. *credential stuffing*) i jest jedną z najczęstszych metod, dzięki którym osoby trzecie mogą przejąć konta. Aby temu zapobiec, nigdy nie używaj ponownie tych samych haseł.

### Używaj losowo generowanych haseł

==**Nigdy** nie polegaj na własnych pomysłach przy tworzeniu dobrego hasła.== Zalecamy używanie [losowo generowanych haseł](#passwords) lub [fraz dostępu Diceware](#diceware-passphrases) o wystarczającej entropii, aby chronić konta i urządzenia.

Wszystkie zalecane przez nas [menedżery haseł](../passwords.md) zawierają wbudowany generator haseł, którego można użyć.

### Rotacja haseł

Unikaj zbyt częstej zmiany haseł, które trzeba zapamiętać (np. hasła głównego menedżera haseł), chyba że istnieje powód, by sądzić, że zostało ono naruszone — zbyt częste zmiany zwiększają ryzyko zapomnienia.

Jeśli chodzi o hasła, których nie trzeba pamiętać (np. przechowywane w menedżerze haseł), jeśli [model zagrożeń](threat-modeling.md) tego wymaga, zalecamy przegląd ważnych kont (szczególnie tych bez uwierzytelniania wieloskładnikowego) i zmienianie ich co kilka miesięcy, na wypadek, gdyby zostały naruszone w wyniku wycieku danych, który jeszcze nie został ujawniony publicznie. Większość menedżerów haseł pozwala ustawić datę wygaśnięcia hasła, co ułatwia zarządzanie tym procesem.

<div class="admonition tip" markdown>
<p class="admonition-title">Sprawdzanie wycieków danych</p>

Jeśli menedżer haseł umożliwia sprawdzenie naruszonych haseł, korzystaj z tej funkcji i niezwłocznie zmieniaj każde hasło, które mogło zostać ujawnione w wyniku wycieku danych. Alternatywnie możesz śledzić [kanał „Latest Breaches” serwisu Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) przy pomocy [agregatora wiadomości](../news-aggregators.md).

</div>

## Tworzenie silnych haseł

### Hasła

Wiele usług narzuca określone kryteria dotyczące haseł, m.in. minimalną lub maksymalną długość oraz zestaw ewentualnych znaków specjalnych. Użyj wbudowanego generatora haseł w swoim menedżerze haseł, aby tworzyć hasła tak długie i złożone, jak tylko pozwala na to dana usługa — uwzględniając wielkie i małe litery, cyfry oraz znaki specjalne.

Jeśli potrzebujesz hasła, które da się zapamiętać, zalecamy [frazy dostępu Diceware](#diceware-passphrases).

### Frazy dostępu Diceware

Diceware to metoda tworzenia fraz dostępu, które łatwo zapamiętać, a jednocześnie trudno odgadnąć.

Frazy dostępu Diceware to świetna opcja, gdy musisz zapamiętać lub ręcznie wpisać dane uwierzytelniające, na przykład hasło główne menedżera haseł lub hasło szyfrowania urządzenia.

Przykład frazy dostępu Diceware: `viewable fastness reluctant squishy seventeen shown pencil`.

Aby wygenerować frazę dostępu Diceware przy użyciu prawdziwych kości, wykonaj następujące kroki:

<div class="admonition Note" markdown>
<p class="admonition-title">Uwaga</p>

Instrukcje zakładają, że używasz [dużej listy słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) do generowania frazy dostępu, która wymaga pięciu rzutów kością na słowo. Inne listy słów mogą wymagać większej lub mniejszej liczby rzutów na słowo i mogą wymagać innej liczby słów, aby osiągnąć tę samą entropię.

</div>

1. Rzuć sześcienną kostką pięć razy, zapisując wynik po każdym rzucie.

2. Dla przykładu przyjmijmy, że wypadło `2-5-2-6-6`. Wyszukaj w [liście słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) słowa odpowiadającego numerowi `25266`.

3. Znajdziesz tam słowo `encrypt`. Zapisz je.

4. Powtarzaj ten proces, aż fraza dostępu będzie zawierać tyle słów, ile potrzebujesz; oddzielaj słowa spacją.

<div class="admonition warning" markdown>
<p class="admonition-title">Ważne</p>

**Nie należy** powtarzać rzutów w celu uzyskania kombinacji słów, które Ci się podobają. Proces ten powinien być całkowicie losowy.

</div>

Jeśli nie masz dostępu do prawdziwych kości lub wolisz ich nie używać, możesz skorzystać z wbudowanego generatora haseł w menedżerze haseł, ponieważ większość menedżerów ma opcję generowania fraz Diceware obok zwykłych haseł. Zalecamy ustawienie długości generowanej frazy na co najmniej 6 słów.

Zalecamy również korzystanie z [dużej listy słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt), ponieważ daje ona taką samą siłę zabezpieczeń jak oryginalna lista, a jednocześnie zawiera słowa łatwiejsze do zapamiętania. Istnieją też [listy słów w innych językach](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline) (w tym języku polskim), jeśli nie chcesz, aby fraza była w języku angielskim.

<details class="note" markdown>
<summary>Wyjaśnienie entropii i siły fraz dostępu Diceware</summary>

Aby pokazać, jak silne są frazy dostępu Diceware, posłużymy się wspomnianą wcześniej siedmiowyrazową frazą (`viewable fastness reluctant squishy seventeen shown pencil`) oraz [dużą listą słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) jako przykładem.

Entropia to jedna z miar siły frazy dostępu. Entropię przypadającą na jedno słowo we frazie Diceware oblicza się jako <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>LiczbaSłówNaLiście</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> a całkowitą entropię frazy jako: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>LiczbaSłówNaLiście</mtext> <mtext>LiczbaSłówWeFrazie</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Zatem każde słowo z wymienionej listy daje ~12,9 bitów entropii (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), a siedmiowyrazowa fraza pochodząca z tej listy ma ~90,47 bitów entropii (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

[Duża lista słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) zawiera 7776 unikalnych słów. Aby obliczyć liczbę możliwych fraz dostępu, wystarczy policzyć <math> <msup> <mtext>LiczbaSłówNaLiście</mtext> <mtext>LiczbaSłówWeFrazie</mtext> </msup> </math>, czyli w naszym przypadku <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Dla perspektywy: siedmiowyrazowa fraza dostępu wygenerowana z [dużej listy słów EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to jedna z ~1 719 070 799 748 422 500 000 000 000 możliwych fraz.

Średnio trzeba sprawdzić 50% wszystkich kombinacji, żeby zgadnąć frazę. Mając to na uwadze, nawet jeśli atakujący potrafi wykonać ~1 000 000 000 000 prób na sekundę, nadal zajęłoby mu to ~27 255 689 lat, aby zgadnąć frazę dostępu. Dzieje się tak, nawet jeśli spełnione są następujące warunki:

- atakujący wie, że użyto metody Diceware;
- atakujący zna konkretną listę słów, która została użyta;
- atakujący wie, ile słów zawiera fraza dostępu.

</details>

Podsumowując, frazy dostępu Diceware to najlepszy wybór, gdy potrzeba rozwiązania łatwego do zapamiętania i jednocześnie wyjątkowo silnego.

## Przechowywanie haseł

### Menedżery haseł

Najlepszym sposobem na przechowywanie haseł jest użycie menedżera haseł. Pozwala on zapisywać hasła lokalnie lub w chmurze i chronić je jednym hasłem głównym. W ten sposób wystarczy zapamiętać jedno silne hasło, które umożliwi dostęp do wszystkich pozostałych.

Istnieje wiele dobrych opcji, zarówno chmurowych, jak i lokalnych. Wybierz jeden z zalecanych przez nas zalecanych menedżerów haseł i użyj go do ustanowienia silnych haseł na wszystkich swoich kontach. Zalecamy zabezpieczenie menedżera haseł [frazą dostępu Diceware](#diceware-passphrases) składającą się z co najmniej siedmiu słów.

[Lista zalecanych menedżerów haseł](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Nie przechowuj haseł i tokenów TOTP w tym samym menedżerze haseł</p>

Przy stosowaniu [kodów TOTP jako uwierzytelniania wieloskładnikowego](multi-factor-authentication.md#time-based-one-time-password-totp) najlepszą praktyką jest przechowywanie kodów TOTP w [osobnej aplikacji](../multi-factor-authentication.md).

Przechowywanie tokenów TOTP w tym samym miejscu co hasła, choć wygodne, ogranicza zabezpieczenie do jednego składnika, w przypadku gdy ktoś uzyska dostęp do menedżera haseł.

Ponadto nie zalecamy przechowywania jednorazowych kodów odzyskiwania w menedżerze haseł. Powinny być one przechowywane osobno, np. w zaszyfrowanym kontenerze na urządzeniu offline.

</div>

### Kopie zapasowe

Należy przechowywać [zaszyfrowaną](../encryption.md) kopię zapasową haseł na kilku nośnikach lub u dostawcy chmury. Ułatwi to dostęp do haseł, jeśli coś stanie się z głównym urządzeniem lub usługą, z której korzystasz.
