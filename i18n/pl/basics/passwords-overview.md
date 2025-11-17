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

Zatem każde słowo z wymienionej listy daje ~12,9 bitów entropii (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>LiczbaSłówNaLiście</mtext> <mtext>LiczbaSłówWeFrazie</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

- Your adversary knows that you used the diceware method.
- Your adversary knows the specific word list that you used.
- Your adversary knows how many words your passphrase contains.

</details>

Podsumowując, frazy dostępu Diceware to najlepszy wybór, gdy potrzeba rozwiązania łatwego do zapamiętania i jednocześnie wyjątkowo silnego.

## Storing Passwords

### Password Managers

The best way to store your passwords is by using a password manager. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[List of recommended password managers](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.

Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

</div>

### Kopie zapasowe

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
