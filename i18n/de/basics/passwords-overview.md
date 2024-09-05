---
title: "Einführung in Passwörter"
icon: 'material/form-textbox-password'
description: Hier findest du einige Tipps und Tricks, wie du die sichersten Passwörter erstellen und deine Konten schützen kannst.
---

Passwörter sind ein wesentlicher Bestandteil unseres täglichen digitalen Lebens. Wir nutzen sie, um unsere Konten, unsere Geräte und unsere Geheimnisse zu schützen. Obwohl sie oft das Einzige sind, was zwischen uns und Angreifenden steht, die es auf unsere privaten Daten abgesehen haben, wird nicht viel über sie nachgedacht, was oft dazu führt, dass Passwörter verwendet werden, die leicht zu erraten oder mit roher Gewalt heraus findbar sind.

## Bewährte Praktiken

### Verwendung einzigartiger Kennwörter

Stell dir vor, du meldest dich mit derselben E-Mail-Adresse und demselben Passwort bei mehreren Online-Diensten an. Wenn einer dieser Dienstleister böswillig ist oder sein Dienst ein Datenleck hat, das dein Passwort in einem unverschlüsselten Format preisgibt, müsste ein Angreifer nur die E-Mail und Passwort Kombination auf mehreren beliebten Diensten ausprobieren, bis er einen Treffer landet. Es spielt keine Rolle, wie stark dieses eine Passwort ist, weil der Angreifer es bereits hat.

Dies wird als [Credential-Stuffing](https://en.wikipedia.org/wiki/Credential_stuffing) bezeichnet und ist eine der häufigsten Methoden, mit denen deine Konten von Angreifern kompromittiert werden können. Um das zu vermeiden, stelle sicher, dass du ein Passwort nie zweimal benutzt.

### Verwendung zufällig generierter Passwörter

==Du solltest dich **nie** auf dich verlassen, um ein gutes Passwort zu finden.== Wir empfehlen die Verwendung von [zufällig generierten Passwörtern](#passwords) oder [Diceware Passphrasen](#diceware-passphrases) mit ausreichender Entropie zum Schutz deiner Konten und Geräte.

Alle von uns [empfohlenen Passwort-Manager](../passwords.md) enthalten einen integrierten Passwort-Generator, den du verwenden kannst.

### Passwörter ändern

Passwörter, die du dir merken musst (z. B. das Master-Passwort deines Passwort-Managers), solltest du nicht zu oft ändern, es sei denn, du hast Grund zu der Annahme, dass es kompromittiert wurde, denn wenn du es zu oft änderst, besteht die Gefahr, dass du es vergisst.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multi-factor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Bei den meisten Passwort-Managern kannst du ein Verfallsdatum für dein Passwort festlegen, um die Verwaltung zu erleichtern.

<div class="admonition tip" markdown>
<p class="admonition-title">Nach Datenlecks suchen</p>

Wenn dein Passwort-Manager die Möglichkeit bietet, nach kompromittierten Passwörter zu suchen, solltest du dies unbedingt tun und umgehend alle Passwörter ändern, die bei einem Datenleck preisgegeben wurden. Alternativ könntest du den [Have I Been Pwned's Latest Breaches Feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) mit Hilfe eines [News-Aggregators](../news-aggregators.md) verfolgen.

</div>

## Erstellung sicherer Passwörter

### Passwörter

Viele Dienste schreiben bestimmte Kriterien für Passwörter vor, z. B. eine Mindest- oder Höchstlänge sowie, ob und welche Sonderzeichen verwendet werden dürfen. Verwendest du den integrierten Passwort-Generator deines Passwort-Managers, um Passwörter zu erstellen, solltest du diese so lang und komplex machen, wie es der Dienst zulässt. Das Passwort sollte dabei idealerweise Groß- und Kleinbuchstaben, Zahlen und Sonderzeichen enthalten.

Wenn du ein Passwort benötigest, das du dir merken kannst, empfehlen wir eine [Diceware-Passphrase](#diceware-passphrases).

### Diceware Passphrasen

Diceware ist eine Methode zur Erstellung von Passphrasen, die leicht zu merken, aber schwer zu erraten sind.

Diceware-Passphrasen sind eine gute Option, wenn du dir deine Anmeldedaten merken oder manuell eingeben musst, z. B. für das Master-Passwort deines Passwortmanagers oder das Verschlüsselungspasswort deines Geräts.

Ein Beispiel für ein Diceware-Passwort ist `sichtbar Schnelligkeit zögerlich weich siebzehn gezeigt Bleistift`.

Gehe wie folgt vor, um eine Diceware-Passphrase mit echten Würfeln zu erstellen:

<div class="admonition Note" markdown>
<p class="admonition-title">Anmerkung</p>

In dieser Anleitung wird davon ausgegangen, dass du die [EFF Large Wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) verwendest, um die Passphrase zu generieren, was fünf Würfelwürfe pro Wort erfordert. Andere Wortlisten können mehr oder weniger Würfe pro Wort erfordern und eine andere Anzahl von Wörtern benötigen, um die gleiche Entropie zu erreichen.

</div>

1. Würfel fünfmal mit einem sechsseitigen Würfel und notiere dir die Zahl nach jedem Wurf.

2. Nehmen wir zum Beispiel an, du hast `2-5-2-6-6` gewürfelt. Suche in [der großen Wortliste des EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) nach dem Wort, das `25266` entspricht.

3. Du findest das Wort `encrypt`. Schreibe dieses Wort auf.

4. Wiederhole diesen Vorgang, bis deine Passphrase aus so vielen Wörtern wie nötig besteht, die du durch ein Leerzeichen trennen solltest.

<div class="admonition warning" markdown>
<p class="admonition-title">Wichtig</p>

Du solltest die Wörter **nicht** neu rollen bis du eine Kombination von Wörtern erhältst, die dich ansprechen. Der Prozess sollte völlig zufällig sein.

</div>

Wenn du keinen Zugang zu echten Würfeln hast oder es vorziehst, diesen nicht zu verwenden, kannst du den integrierten Passwortgenerator deines Passwort-Managers verwenden, da die meisten von ihnen die Option haben, zusätzlich zu den normalen Passwörtern auch Diceware-Passphrasen zu generieren.

Wir empfehlen, die [große Wortliste des EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) zu verwenden, um deine Diceware-Passphrasen zu generieren, da sie genau die gleiche Sicherheit bietet wie die ursprüngliche Liste, aber Wörter enthält, die man sich leichter merken kann. Es gibt auch [andere Wortlisten in verschiedenen Sprachen](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), wenn du nicht willst, dass deine Passphrase auf Englisch ist ([hier findest du die deutsche Version](https://theworld.com/~reinhold/diceware_german.txt)).

<details class="note" markdown>
<summary>Erläuterung von Entropie und der Stärke Diceware-Passphrasen</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

Eine Kennzahl zur Bestimmung der Stärke einer Diceware-Passphrase ist die Entropie, die sie aufweist. Die Entropie pro Wort in einer Diceware-Passphrase wird wie folgt berechnet <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WörterInListe</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> und die Gesamtentropie der Passphrase wird wie folgt berechnet: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WörterInListe</mtext> <mtext>WörterInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Daher ergibt jedes Wort in der oben genannten Liste ~12,9 Bits an Entropie (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), und eine daraus abgeleitete Passphrase mit sieben Wörtern hat eine Entropie von ~90,47 Bit (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

[Die große Wortliste des EFF](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) enthält 7776 einzigartige Wörter. Um die Anzahl der möglichen Passphrasen zu berechnen, müssen wir nur Folgendes tun <math> <msup> <mtext>WörterInListe</mtext> <mtext>WörterInPhrase</mtext> </msup> </math>, oder in unserem Fall, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large wordlist](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

- Your adversary knows that you used the diceware method.
- Your adversary knows the specific wordlist that you used.
- Your adversary knows how many words your passphrase contains.

</details>

Zusammenfassend lässt sich sagen, dass Diceware-Passphrasen die beste Wahl sind, wenn du ein Passwort brauchst, das sowohl leicht zu merken *als auch* außergewöhnlich stark ist.

## Passwörter speichern

### Passwortverwaltung

The best way to store your passwords is by using a password manager. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[Empfohlene Passwort-Manager](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multi-factor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.

Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

</div>

### Backups

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
