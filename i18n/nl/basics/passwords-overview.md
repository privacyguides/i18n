---
title: Introduction to Passwords
icon: material/form-textbox-password
description: Dit zijn enkele tips en trucs om de sterkste wachtwoorden te maken en je accounts veilig te houden.
---

Wachtwoorden zijn een essentieel onderdeel van ons dagelijkse digitale leven. We gebruiken ze om onze accounts, onze apparaten en onze geheimen te beschermen. Hoewel ze vaak het enige zijn tussen ons en een tegenstander die op onze privégegevens uit is, wordt er niet veel aandacht aan besteed, wat er vaak toe leidt dat mensen wachtwoorden gebruiken die gemakkelijk geraden of geforceerd kunnen worden.

## Best practices

### Gebruik unieke wachtwoorden voor elke dienst

Imagine this: You sign up for an account with the same e-mail and password on multiple online services. Als een van die dienstverleners kwaadwillend is, of hun dienst een datalek heeft waardoor uw wachtwoord in een onversleuteld formaat wordt vrijgegeven, hoeft een kwaadwillende alleen maar die combinatie van e-mail en wachtwoord te proberen bij meerdere populaire diensten totdat hij iets vindt. Het maakt dan niet uit hoe sterk dat ene wachtwoord is, omdat ze het al hebben.

Dit heet [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing), en het is een van de meest voorkomende manieren waarop jouw accounts kunnen worden gecompromitteerd door kwaadwillenden. Om dit te voorkomen, moet je ervoor zorgen dat je je wachtwoorden nooit opnieuw gebruikt.

### Gebruik willekeurig gegenereerde wachtwoorden

==Je moet **nooit** vertrouwen op jezelf om een goed wachtwoord te bedenken.== Wij raden aan [willekeurig gegenereerde wachtwoorden](#passwords) of [diceware passphrases](#diceware-passphrases) met voldoende entropie te gebruiken om je accounts en apparaten te beschermen.

Al onze [aanbevolen wachtwoordmanagers](../passwords.md) bevatten een ingebouwde wachtwoordgenerator die je kunt gebruiken.

### Roterende wachtwoorden

Wachtwoorden die je moet onthouden (zoals het hoofdwachtwoord van jouw wachtwoordmanager) moet je niet te vaak veranderen, tenzij je reden hebt om aan te nemen dat ze gecompromitteerd zijn, omdat je door ze te vaak te veranderen het risico loopt ze te vergeten.

Als het gaat om wachtwoorden die je niet hoeft te onthouden (zoals wachtwoorden die zijn opgeslagen in je wachtwoordmanager), raden we je aan om, als je [dreigingsmodel](threat-modeling.md) daarom vraagt, belangrijke accounts door te nemen (vooral accounts die geen multifactorauthenticatie gebruiken) en hun wachtwoord om de paar maanden te wijzigen, voor het geval ze zijn gecompromitteerd in een datalek dat nog niet openbaar is gemaakt. Bij de meeste wachtwoordmanagers kun je een vervaldatum voor je wachtwoord instellen om dit gemakkelijker te beheren.

<div class="admonition tip" markdown>
<p class="admonition-title">Controleren op datalekken</p>

Als je met jouw wachtwoordmanager kunt controleren op gecompromitteerde wachtwoorden, doe dat dan en wijzig onmiddellijk alle wachtwoorden die bij een datalek bekend zijn geworden. Je kunt ook de [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) volgen met behulp van een [nieuwsaggregator](../news-aggregators.md).

</div>

## Sterke wachtwoorden maken

### Wachtwoorden

Veel diensten leggen bepaalde criteria op voor wachtwoorden, zoals een minimale of maximale lengte, en welke speciale tekens eventueel mogen worden gebruikt. Gebruik de ingebouwde wachtwoordgenerator van je wachtwoord manager om wachtwoorden te maken die zo lang en complex zijn als de dienst toelaat, met hoofdletters en kleine letters, cijfers en speciale tekens.

Als je een wachtwoord nodig hebt dat je kunt onthouden, raden wij een [diceware wachtwoord zinnen](#diceware-passphrases) aan.

### Diceware wachtwoord zinnen

Diceware is een methode om wachtzinnen te maken die gemakkelijk te onthouden zijn, maar moeilijk te raden.

Diceware passphrases zijn een geweldige optie wanneer je jouw gegevens uit het hoofd moet leren of handmatig moet invoeren, zoals voor het hoofdwachtwoord van jouw wachtwoord manager of het coderingswachtwoord van jouw apparaat.

Een voorbeeld van een diceware wachtwoord zin is: `zichtbaar snelheid hond terughoudend zeventien weergegeven potlood`.

Volg deze stappen om een diceware passphrase te genereren met echte dobbelstenen:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Gooi vijf keer met een zeszijdige dobbelsteen en noteer het getal na elke worp.

2. Laten we bijvoorbeeld zeggen dat u `2-5-2-6-6`heeft gerold. Zoek in de [grote woordenlijst van EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) naar het woord dat overeenkomt met `25266`.

3. Je zult het woord `gecodeerd` vinden. Schrijf dat woord op.

4. Herhaal dit proces totdat jouw wachtwoord zoveel woorden bevat als je nodig hebt, die je moet scheiden met een spatie.

<div class="admonition warning" markdown>
<p class="admonition-title">Belangrijk</p>

Je moet **niet** opnieuw woorden rollen totdat je een combinatie van woorden krijgt die je aanspreekt. Het proces moet volledig willekeurig zijn.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords. We recommend setting the generated passphrase length to at least 6 words.

We also recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

Gemiddeld duurt het proberen van 50% van alle mogelijke combinaties om uw zin te raden. Met dat in gedachten, zelfs als uw tegenstander in staat is tot ~1.000.000.000.000 raden per seconde, zou het hem nog steeds ~27.255.689 jaar kosten om uw wachtwoord te raden. Zelfs als de volgende dingen waar zijn:

- Je tegenstander weet dat je de diceware-methode hebt gebruikt.
- Your adversary knows the specific word list that you used.
- Jouw tegenstander weet hoeveel woorden jouw wachtwoord bevat.

</details>

Kortom, diceware wachtzinnen zijn jouw beste optie wanneer je iets nodig hebt dat zowel gemakkelijk te onthouden is *als* uitzonderlijk sterk.

## Wachtwoorden opslaan

### Wachtwoordmanagers

De beste manier om jouw wachtwoorden op te slaan is met behulp van een wachtwoordmanager. Hiermee kunt je jouw wachtwoorden opslaan in een bestand of in de cloud en ze beschermen met een enkel hoofdwachtwoord. Op die manier hoeft u maar één sterk wachtwoord te onthouden, waarmee je toegang krijgt tot de rest.

Er zijn veel goede opties om uit te kiezen, zowel cloud-gebaseerd als lokaal. Kies een van onze aanbevolen wachtwoordbeheerders en gebruik deze om sterke wachtwoorden in te stellen voor al jouw accounts. Wij raden je aan om jouw wachtwoordmanager te beveiligen met een [diceware wachtwoord zin](#diceware-passphrases) bestaande uit ten minste zeven woorden.

[Lijst van aanbevolen wachtwoordmanagers](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Het opslaan van jouw TOTP-tokens op dezelfde plaats als jouw wachtwoorden is weliswaar handig, maar beperkt de accounts tot één factor in het geval dat een tegenstander toegang krijgt tot jouw wachtwoord manager.

Verder raden wij af om herstelcodes voor eenmalig gebruik op te slaan in uw wachtwoord manager. Deze moeten apart worden opgeslagen, zoals in een versleutelde container op een offline opslagapparaat.

</div>

### Back-ups

Je moet een [gecodeerde](../encryption.md) back-up van jouw wachtwoorden opslaan op meerdere opslagapparaten of een cloud-opslagprovider. Dit kan nuttig zijn als er iets gebeurt met jouw toestel of de dienst die je gebruikt.
