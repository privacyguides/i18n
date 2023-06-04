---
title: "Introduzione alle password"
icon: 'material/form-textbox-password'
description: Ecco alcuni suggerimenti e trucchi su come creare le password più forti e mantenere i vostri account al sicuro.
---

Le password sono una parte essenziale della nostra vita digitale quotidiana. Le utilizziamo per proteggere i nostri account, dispositivi e segreti. Nonostante siano spesso l'unica cosa che ci separa da un nemico a caccia di informazioni private, non ci si pensa molto, il che spesso porta le persone ad utilizzare password che possono essere facilmente indovinate o forzate.

## Pratiche migliori

### Utilizza password uniche per ogni servizio

Immagina questo: registrate un account con la stessa email e la stessa password su più servizi online. Se uno di questi servizi è malevolo o il loro servizio subisce una violazione dei dati che espone la password in formato non criptato, tutto ciò che un malintenzionato dovrebbe fare è provare quella combinazione di e-mail e password su più servizi popolari finché non ottiene un risultato. Non importa quanto forte sia quella password, perchè ormai ce l'hanno già.

Questo fenomeno è chiamato [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing) ed è uno dei modi più comuni tramite cui i vostri account potrebbero venir compromessi da malintenzionati. Per evitare che ciò accada, assicurati di non riutilizzare mai le password.

### Usa password generate randomicamente

== Non dovresti **mai** affidarti a te stesso per creare un'ottima password.== Consigliamo di utilizzare [password generate randomicamente](#passwords) o [passphrase di tipo diceware](#diceware-passphrases) con un'entropia sufficiente a proteggere i tuoi account e dispositivi.

Tutti i nostri [gestori di password consigliati](../passwords.md) includono un generatore di password integrato che puoi utilizzare.

### Rotazione delle password

Dovresti evitare di cambiare troppo spesso le password che necessitano di essere ricordate (come la master password del vostro gestore di password), a meno che non abbiate motivo di credere che sia stata compromessa, perché cambiarla troppo spesso vi espone al rischio di dimenticarla.

Per quanto riguarda le password che non devi ricordare (come quelle memorizzate all'interno del vostro gestore di password), se la vostra [ modellazione delle minacce](threat-modeling.md) lo richiede, vi consigliamo di controllare gli account importanti (soprattutto quelli che non utilizzano l'autenticazione a più fattori) e di cambiare la loro password almeno ogni due mesi, nel caso in cui siano stati compromessi in una violazione dei dati non ancora resa pubblica. La maggior parte dei gestori di password ti consente d'impostare una data di scadenza per le tue password cosi da gestirle più facilmente.

!!! consiglio "Controlla le violazioni dei dati"

    Se il tuo gestore di password permette di verificare la presenza di password compromesse, assicurati di controllare le vostre password e di cambiare immediatamente qualsiasi password che potrebbe essere stata esposta in una violazione dei dati. In alternativa, puoi seguire il feed di [Have I Been Pwned's Latest Breaches](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) con l'aiuto di un [aggregatore di notizie](../news-aggregators.md).

## Creare password forti

### Password

Molti servizi impongono determinati criteri per quanto riguarda le password, tra cui una lunghezza minima o massima e l'eventuale utilizzo di caratteri speciali. Dovreste utilizzare il generatore di password integrato nel vostro gestore di password per creare password complesse e lunghe quanto la dimensione massima che il sito permette, includendo lettere maiuscole e minuscole, numeri e caratteri speciali.

Se hai bisogno di una password da memorizzare, ti consigliamo una [passfrase diceware](#diceware-passphrases).

### Passfrasi Diceware

Il metodo Diceware serve per creare passfrasi facili da ricordare, ma difficili da indovinare.

Le passfrasi diceware sono un'ottima opzione quando è necessario memorizzare o inserire manualmente le proprie credenziali, come ad esempio la password principale del proprio gestore di password o la password di crittografia del proprio dispositivo.

Un esempio di passfrase diceware è `viewable fastness reluctant squishy seventeen shown pencil`.

Per generare una passfrase diceware utilizzando un vero dado, segui questi passaggi:

!!! note "Nota"

    Queste istruzioni presuppongono l'utilizzo del [grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) per generare la passfrase, che richiede cinque lanci di dadi per parola. Altri elenchi di parole potrebbero richiedere più o meno tiri per parola, e possono richiedere una quantità diversa di parole per ottenere la stessa entropia.

1. Lancia un dado a sei facce 5 volte, annota il numero ottenuto dopo ogni tiro.

2. Per esempio, supponiamo che tu abbia ottenuto `2-5-2-6-6`. Guarda nel [grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) la parola che corrisponde a `25266`.

3. Troverai la parola `encrypt`. Annota questa parola.

4. Ripeti questa procedura finché la vostra passfrase non avrà il numero di parole necessario, che dovrete separare con uno spazio.

!!! avviso "Importante"

    **Non** dovresti rigenerare le parole affinché non ottieni una combinazione di parole che ti attragga. Il processo dovrebbe essere effettuato randomicamente.

Se non hai un dado, o semplicemente non lo vuoi usare, puoi utilizzare il generatore di password del tuo gestore di password, molti di questi hanno l'opzione di poter generare passfrasi diceware oltre alle classiche password.

Consigliamo di utilizzare il [grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) per generare le tue passfrasi diceware, in quanto offre la stessa sicurezza dell'elenco originale, pur contenendo parole più facili da memorizzare. Esistono anche [altri elenchi di parole in lingue diverse](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), se non vuoi che la tua passfrase sia in Inglese.

??? nota "Spiegazione dell'entropia e della forza delle passfrasi diceware"

    Per dimostrare quanto siano forti le passfrasi diceware, useremo la già citata passfrase di sette parole (`viewable fastness reluctant squishy seventeen shown pencil`) e il [grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) come esempio.
    
    Un parametro per determinare la forza di una passfrase diceware è la sua entropia. L'entropia per parola in una passphrase diceware è calcolata come $\text{log}_2(\text{WordsInList})$ e l'entropia complessiva della passfrase è calcolata come $\text{log}_2(\text{WordsInList}^\text{WordsInPhrase})$.
    
    Pertanto, ogni parola del suddetto elenco produce ~12,9 bit di entropia ($\text{log}_2(7776)$), e una passfrase di sette parole derivata da esso ha ~90,47 bit di entropia ($\text{log}_2(7776^7)$).
    
    Il [grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) contiene 7776 parole uniche. Per calcolare la quantità di passfrasi possibili, tutto ciò che dobbiamo fare è $\text{WordsInList}^\text{WordsInPhrase}$, o nel nostro caso, $ 7776^7 $.
    
    Mettiamo tutto questo in prospettiva: Una passfrase di sette parole utilizzando il [Grande elenco di parole di EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) è una delle ~1.719.070.799.748.422.500.000.000.000.000 possibili passfrasi.
    
    In media, è necessario tentare il 50% di tutte le combinazioni possibili per indovinare la tua passfrase. E con questo, anche se l'avversario è in grado di fare ~1.000.000.000.000 tentativi al secondo, gli ci vorrebbero comunque ~27.255.689 anni per indovinare la vostra passfrase. Questo vale solo se le seguenti cose sono vere:

    - Il tuo avversario sa che hai usato il metodo diceware.
    - Il tuo avversario conosce l'elenco specifico che hai utilizzato.
    - Il tuo avversario sa quante parole contiene la tua passfrase.

Ricapitolando, le passfrasi diceware sono la scelta migliore se hai bisogno di qualcosa che sia facile da ricordare *e* estremamente forte.

## Memorizzare le password

### Gestori di password

Il miglior modo per memorizzare le proprie password è quello di utilizzare un gestore di password. Ti consentono di memorizzare le password in un singolo file o nel cloud e di proteggerle con un'unica password principale. In questo modo, dovrete ricordare solo un'unica password forte, che vi permetterà di accedere alle altre.

Ci sono molte opzioni valide tra cui scegliere, sia basata su cloud, sia locali. Scegli uno dei nostri gestori di password consigliati e usalo per impostare password forti per tutti i tuoi account. Consigliamo di proteggere il vostro gestore di password con una [passfrase diceware](#diceware-passphrases) composta da almeno 7 parole.

[Elenco dei gestori di password consigliati](../passwords.md ""){.md-button}

!!! warning "Non memorizzare le tue password e i token TOTP nello stesso gestore di password"

    Quando utilizzi i codici TOTP come [autenticazione a più fattori](../multi-factor-authentication.md), la migliore prassi per la sicurezza è quella di conservare i codici TOTP in una [app separata](../multi-factor-authentication.md#authenticator-apps).
    
    Conservare i token TOTP nello stesso luogo delle password, pur essendo comodo, riduce gli account ad un singolo fattore nel caso in cui un avversario riesca ad accedere al tuo gestore di password.
    
    Inoltre, sconsigliamo di memorizzare i codici di recupero monouso nel tuo gestore di password. Questi andrebbero archiviati in un contenitore criptato o su un dispositivo d'archiviazione offline.

### Backup

Dovresti archiviare un backup [criptato](../encryption.md) di tutte le tue password su più dispositivi o su un provider d'archiviazione in cloud. Questo potrà aiutarti ad accedere alle password se dovesse succedere qualcosa al vostro dispositivo principale o al servizio che state utilizzando.
