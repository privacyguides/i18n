---
title: Introduzione alle Password
icon: material/form-textbox-password
description: Ecco alcuni consigli e trucchi su come creare le password più forti e mantenere sicuri i tuoi profili.
---

Le password sono una parte essenziale delle nostre vite digitali quotidiane. We use them to protect our accounts, our devices, and our secrets. Nonostante spesso siano la sola cosa tra di noi e un malintenzionato a caccia di informazioni private, non ci si pensa molto, portando spesso le persone a utilizzare password facili da indovinare o forzare.

## Migliori Pratiche

### Utilizza password uniche per ogni servizio

Imagine this: You sign up for an account with the same e-mail and password on multiple online services. Se uno dei fornitori di tali servizi è malintenzionato, o se il servizio subisce una violazione di dati che espone la tua password in un formato non crittografato, tutto ciò che un malintenzionato dovrà fare è provare tale combinazione di email e password su numerosi servizi popolari, fino all'ottenimento di un risultato. Non importa quanto forte sia quella password, poiché, ormai, è già in suo possesso.

Questo fenomeno è detto [riempimento delle credenziali](https://en.wikipedia.org/wiki/Credential_stuffing) ed è uno dei metodi più comuni di compromissione dei tuoi account, da utenti malintenzionati. Per evitarlo, assicurati di non riutilizzare mai le tue password.

### Usa password generate casualmente

==Non dovresti **mai** basarti su te stesso per generaare una buona password.== Consigliamo di utilizzare le [password generate casualmente](#password) o le [frasi segrete Diceware](#frasi-segrete-diceware), con un'entropia sufficiente per proteggere i tuoi profili e dispositivi.

Tutti i [gestori di password consigliati](../passwords.md) da noi, includono un generatore di password integrato che puoi utilizzare.

### Rotazione delle password

Dovresti evitare di modificare troppo spesso le password che devi ricordare (come la password generale del tuo gestore di password), a meno che tu non abbia motivo di credere che siano state compromesse, poiché modificarle troppo spesso ti espone al rischio di dimenticarle.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Gran parte dei gestori di password ti consentono di impostare una data di scadenza per la tua password, rendendola più facile da gestire.

<div class="admonition tip" markdown>
<p class="admonition-title">Controllo delle violazioni dei dati</p>

Se il tuo gestore di password ti consente di verificare quelle compromesse, assicurati di farlo e di modificare prontamente qualsiasi password possa esser stata esposta in una violazione di dati. Altrimenti, potresti seguire il [feed di Violazioni di Dati Recenti di Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches), con l'aiuto di un [aggregatore di notizie](../news-aggregators.md).

</div>

## Creare password forti

### Password

Molti servizi impongono certi criteri per quanto riguarda le password, inclusa una lunghezza minima o massima, nonché quali caratteri specili, se presenti, sono utilizzabili. Dovreste utilizzare il generatore di password integrato del tuo gestore di password per creare le password più complesse e lunghe consentite, consentendo l'inclusione di lettere maiuscole e minuscole, numeri e caratteri speciali.

Se necessiti di una password memorizzabile, consigliamo una [frase segreta Diceware](#diceware-passphrases).

### Passphrase Diceware

Il metodo Diceware serve a creare frasi segrete facili da ricordare, ma difficili da indovinare.

Le frasi segrete Diceware sono un'ottima opzione quando devi memorizzare o inserire manualmente le tue credenziali, come per la password principale del tuo gestore di password o per la password crittografica del tuo dispositivo.

Un esempio di passphrase diceware è `viewable fastness reluctant squishy seventeen shown pencil`.

Per generare una passphrase diceware utilizzando un vero dado, segui questi passaggi:

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Lancia un dado a sei facce per cinque volte, annotando il numero dopo ogni lancio.

2. Ad esempio, supponiamo tu abbia ottenuto `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. Troverai la parola `encrypt`. Annotala.

4. Ripeti questa procedura finché la tua frase segreta contiene quante parole necessarie, che dovresti separare con degli spazi.

<div class="admonition warning" markdown>
<p class="admonition-title">Importante</p>

**Non** dovresti rigenerare le parole finché non ottieni una combinazione di parole che ti attragga. Il processo dovrebbe essere totalmente casuale.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords. We recommend setting the generated passphrase length to at least 6 words.

We also recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Spiegazione dell'entropia e della forza delle passphrase diceware</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

Un parametro per determinare la forza di una passphrase diceware è la sua entropia. L'entropia per parola in una passphrase diceware è calcolata come <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> e l'entropia complessiva della passphrase è calcolata come: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Pertanto, ogni parola nell'elenco di cui sopra risulta in ~12.9 bit di entropia (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>) e una passphrase di sette parole derivata da essa ha ~90,47 bit di entropia (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. Per calcolare la quantità di passphrase possibili, tutto ciò che dobbiamo fare è <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, o nel nostro caso, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

In media, è necessario tentare il 50% di tutte le combinazioni possibili per indovinare la tua frase segreta. Tenendo ciò a mente, anche se il malintenzionato è capace di circa 1.000.000.000.000 tentativi al secondo, gli ci vorrebbero comunque circa 27.255.689 aanni per indovinare la tua frase segreta. Questo vale solo se le seguenti cose sono vere:

- Il tuo avversario sa che hai utilizzato il metodo Diceware.
- Your adversary knows the specific word list that you used.
- Il tuo avversario sa quante parole contiene la tua frase segreta.

</details>

Ricapitolando, le frasi segrete Diceware sono la tua migliore opzione quando necessiti di qualcosa che sia facile da ricordare *ed* eccezionalmente forte.

## Memorizzare le password

### Gestori di password

Il miglior modo per memorizzare le tue password è utilizzare un gestore di password. Ti consente di memorizzare le tue password in un file o nel cloud e di proteggerle con un password principale singola. Così, dovrai ricordare soltanto una password forte, che ti consente di accedere al resto di esse.

Esistono molte buone opzioni da cui scegliere, sia basate su cloud che locali. Scegli uno dei nostri gestori di password consigliati e utilizzalo per stabilire le password forti tra tutti i tuoi profili. Consigliamo di proteggere il tuo gestore di password con una [password diceware](#diceware-passphrases), che comprenda almeno sette parole.

[Elenco dei gestori di password consigliati](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Non inserire le tue password e i token TOTP nello stesso gestore di password</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Memorizzare i token TOTP nello stesso luogo delle tue password, sebbene comodo, riduce i profili a un singolo fattore, nel caso in cui un malintenzionato ottenga l'accesso al tuo gestore di password.

Inoltre, sconsigliamo di memorizzare i codici di recupero a uso singolo nel tuo gestore di password. Questi, dovrebbero essere memorizzati separatamente in un contenitore crittografato, su un dispositivo di archiviazione offline.

</div>

### Backup

Dovresti archiviare un backup [crittografato](../encryption.md) di tutte le tue password su più dispositivi o su un fornitore d'archiviazione in cloud. Ciò può aiutarti ad accedere alle tue password se succede qualcosa al tuo dispositivo principale o al servizio che stai utilizzando.
