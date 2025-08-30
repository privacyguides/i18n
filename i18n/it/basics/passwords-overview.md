---
title: Introduzione alle Password
icon: material/form-textbox-password
description: Ecco alcuni consigli e trucchi su come creare le password più forti e mantenere sicuri i tuoi profili.
---

Le password sono una parte essenziale delle nostre vite digitali quotidiane. Le usiamo per proteggere i nostri account, i nostri dispositivi e i nostri segreti. Nonostante spesso siano la sola cosa tra di noi e un malintenzionato a caccia di informazioni private, non ci si pensa molto, portando spesso le persone a utilizzare password facili da indovinare o forzare.

## Migliori Pratiche

### Utilizza password uniche per ogni servizio

Immagina questo: ti registri a più servizi online usando la stessa e-mail e la stessa password. Se uno dei fornitori di tali servizi è malintenzionato, o se il servizio subisce una violazione di dati che espone la tua password in un formato non crittografato, tutto ciò che un malintenzionato dovrà fare è provare tale combinazione di email e password su numerosi servizi popolari, fino all'ottenimento di un risultato. Non importa quanto forte sia quella password, poiché, ormai, è già in suo possesso.

Questo fenomeno è detto [riempimento delle credenziali](https://en.wikipedia.org/wiki/Credential_stuffing) ed è uno dei metodi più comuni di compromissione dei tuoi account, da utenti malintenzionati. Per evitarlo, assicurati di non riutilizzare mai le tue password.

### Usa password generate casualmente

==Non dovresti **mai** basarti su te stesso per generaare una buona password.== Consigliamo di utilizzare le [password generate casualmente](#password) o le [frasi segrete Diceware](#frasi-segrete-diceware), con un'entropia sufficiente per proteggere i tuoi profili e dispositivi.

Tutti i [gestori di password consigliati](../passwords.md) da noi, includono un generatore di password integrato che puoi utilizzare.

### Rotazione delle password

Dovresti evitare di modificare troppo spesso le password che devi ricordare (come la password generale del tuo gestore di password), a meno che tu non abbia motivo di credere che siano state compromesse, poiché modificarle troppo spesso ti espone al rischio di dimenticarle.

Per le password che non serve ricordare (ad esempio quelle memorizzate nel tuo gestore di password), se il tuo [modello di minaccia](threat-modeling.md) lo richiede, ti consigliamo di controllare i tuoi account più importanti (soprattutto quelli che non usano l’autenticazione a più fattori) e di cambiare la loro password ogni due mesi, nel caso siano state compromesse in una violazione di dati non ancora resa pubblica. Gran parte dei gestori di password ti consentono di impostare una data di scadenza per la tua password, rendendola più facile da gestire.

<div class="admonition tip" markdown>
<p class="admonition-title">Controllo delle violazioni dei dati</p>

Se il tuo gestore di password ti consente di verificare quelle compromesse, assicurati di farlo e di modificare prontamente qualsiasi password possa esser stata esposta in una violazione di dati. Altrimenti, potresti seguire il [feed di Violazioni di Dati Recenti di Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches), con l'aiuto di un [aggregatore di notizie](../news-aggregators.md).

</div>

## Creare password forti

### Password

Molti servizi impongono certi criteri per quanto riguarda le password, inclusa una lunghezza minima o massima, nonché quali caratteri specili, se presenti, sono utilizzabili. Dovresti utilizzare il generatore di password integrato del tuo gestore di password per creare le password più complesse e lunghe consentite, consentendo l'inclusione di lettere maiuscole e minuscole, numeri e caratteri speciali.

Se necessiti di una password memorizzabile, consigliamo una [passphrase diceware](#diceware-passphrases).

### Passphrase Diceware

Il metodo Diceware serve a creare frasi segrete facili da ricordare, ma difficili da indovinare.

Le frasi segrete Diceware sono un'ottima opzione quando devi memorizzare o inserire manualmente le tue credenziali, come per la password principale del tuo gestore di password o per la password crittografica del tuo dispositivo.

Un esempio di passphrase diceware è `viewable fastness reluctant squishy seventeen shown pencil`.

Per generare una passphrase diceware utilizzando un vero dado, segui questi passaggi:

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

Queste istruzioni presumono che tu stia usando la [EFF’s large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) per generare la frase segreta, che richiede cinque lanci di dado per parola. Altre liste di parole possono richiedere un numero maggiore o minore di lanci di dado per parola e un numero diverso di parole per ottenere la stessa entropia.

</div>

1. Lancia un dado a sei facce per cinque volte, annotando il numero dopo ogni lancio.

2. Ad esempio, supponiamo tu abbia ottenuto `2-5-2-6-6`. Trova nella [EFF’s large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) la parola corrispondente a `25266`.

3. Troverai la parola `encrypt`. Annotala.

4. Ripeti questa procedura finché la tua frase segreta contiene quante parole necessarie, che dovresti separare con degli spazi.

<div class="admonition warning" markdown>
<p class="admonition-title">Importante</p>

**Non** dovresti rigenerare le parole finché non ottieni una combinazione di parole che ti attragga. Il processo dovrebbe essere totalmente casuale.

</div>

Se non hai dadi veri o preferisci non usarli, puoi usare il generatore di password integrato nel tuo gestore di password, perché la maggior parte di essi offre l’opzione di creare passphrase diceware oltre alle normali password. Ti consigliamo di creare una passphrase lunga almeno 6 parole.

Ti consigliamo anche di usare la [EFF's large word list](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline) per generare le tue passphrase diceware, perché offre la stessa sicurezza della lista originale, ma contiene parole più facili da memorizzare. Esistono anche [liste di parole in altre lingue](https://eff.org/files/2016/07/18/eff_large_wordlist.txt), se non vuoi che la tua passphrase sia in inglese.

<details class="note" markdown>
<summary>Spiegazione dell'entropia e della forza delle passphrase diceware</summary>

Per dimostrare quanto siano sicure le passphrase diceware, useremo come esempio la passphrase di sette parole citata in precedenza (`viewable fastness reluctant squishy seventeen shown pencil`) e la [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt).

Un parametro per determinare la forza di una passphrase diceware è la sua entropia. L'entropia per parola in una passphrase diceware è calcolata come <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> e l'entropia complessiva della passphrase è calcolata come: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Pertanto, ogni parola nell'elenco di cui sopra risulta in ~12.9 bit di entropia (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>) e una passphrase di sette parole derivata da essa ha ~90,47 bit di entropia (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

La [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contiene 7.776 parole diverse. Per calcolare la quantità di passphrase possibili, tutto ciò che dobbiamo fare è <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, o nel nostro caso, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Per farti un’idea: una passphrase di sette parole usando la [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) è una delle circa 1.719.070.799.748.422.500.000.000.000 passphrase possibili.

In media, è necessario tentare il 50% di tutte le combinazioni possibili per indovinare la tua frase segreta. Tenendo ciò a mente, anche se il malintenzionato è capace di circa 1.000.000.000.000 tentativi al secondo, gli ci vorrebbero comunque circa 27.255.689 anni per indovinare la tua passphrase diceware. Questo vale solo se le seguenti cose sono vere:

- Il tuo avversario sa che hai utilizzato il metodo Diceware.
- Il tuo avversario sa la lista di parole specifica che hai utilizzato.
- Il tuo avversario sa quante parole contiene la tua frase segreta.

</details>

Ricapitolando, le passphrase diceware sono la tua migliore opzione quando necessiti di qualcosa che sia facile da ricordare *ed* eccezionalmente forte.

## Memorizzare le password

### Gestori di password

Il miglior modo per memorizzare le tue password è utilizzare un gestore di password. Ti consente di memorizzare le tue password in un file o nel cloud e di proteggerle con un password principale singola. Così, dovrai ricordare soltanto una password forte, che ti consente di accedere al resto di esse.

Esistono molte buone opzioni da cui scegliere, sia basate su cloud che locali. Scegli uno dei nostri gestori di password consigliati e utilizzalo per stabilire le password forti tra tutti i tuoi profili. Consigliamo di proteggere il tuo gestore di password con una [password diceware](#diceware-passphrases), che comprenda almeno sette parole.

[Elenco dei gestori di password consigliati](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Non inserire le tue password e i token TOTP nello stesso gestore di password</p>

Quando usi i [codici TOTP come autenticazione multifattore](multi-factor-authentication.md#time-based-one-time-password-totp), la migliore misura di sicurezza è conservare i tuoi codici TOTP in un’[app separata](../multi-factor-authentication.md).

Memorizzare i token TOTP nello stesso luogo delle tue password, sebbene comodo, riduce i profili a un singolo fattore, nel caso in cui un malintenzionato ottenga l'accesso al tuo gestore di password.

Inoltre, sconsigliamo di memorizzare i codici di recupero a uso singolo nel tuo gestore di password. Questi, dovrebbero essere memorizzati separatamente in un contenitore crittografato, su un dispositivo di archiviazione offline.

</div>

### Backup

Dovresti archiviare un backup [crittografato](../encryption.md) di tutte le tue password su più dispositivi o su un fornitore d'archiviazione in cloud. Ciò può aiutarti ad accedere alle tue password se succede qualcosa al tuo dispositivo principale o al servizio che stai utilizzando.
