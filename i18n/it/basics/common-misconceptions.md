---
title: "I malintesi più comuni"
icon: 'material/robot-confused'
description: La privacy non è un tema semplice ed è facile farsi abbindolare dalle dichiarazioni commerciali e altra disinformazione.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            Il fatto che il codice sorgente sia disponibile e la licenza a cui è sottoposto il software non implica che il codice sia sicuro a prescindere. Il software open-source è potenzialmente più sicuro del software proprietario, tuttavia non c'è alcuna garanzia che sia così. Quando si valuta un software, è necessario esaminare la reputazione e la sicurezza di ogni programma in modo indipendente.
      - 
        "@type": Question
        name: '"Spostare la fiducia" ad un altro provider può migliorare la privacy?'
        acceptedAnswer:
          "@type": Answer
          text: |
            Si parla molto di "spostamento della fiducia", parlando di soluzioni come le VPN (che spostano la fiducia nel tuo ISP al fornitore VPN). Sebbene ciò protegga i tuoi dati di navigazione dal tuo ISP nello specifico, il fornitore VPN che scegli ha comunque accesso ai tuoi dati di navigazione: non sono completamente protetti da tutte le parti.
      - 
        "@type": Question
        name: Le soluzioni incentrate sulla privacy sono intrinsecamente affidabili?
        acceptedAnswer:
          "@type": Answer
          text: |
            Concentrarsi soltanto sulle politiche sulla privacy e sul marketing di uno strumento o fornitore, può rendere cechi alle sue debolezze. Quando si cerca una soluzione più privata, è necessario determinare il problema di fondo e trovare soluzioni tecniche per risolverlo. Ad esempio, potresti voler evitare Google Drive, che dà a Google l'accesso a tutti i tuoi dati. Il problema di fondo, in questo caso, è la mancanza dell'E2EE, quindi, dovresti assicurare che il fornitore a cui passi la implementi effettivamente, o utilizzare uno strumento (come Cryptomator), che la fornisca su qualsiasi fornitore su cloud. Passare a un fornitore "incentrato sulla privacy" (che non implementa l'E2EE), non risolve il tuo problema: sposta la fiducia da Google a quel fornitore.
      - 
        "@type": Question
        name: Quanto complicato dovrebbe essere il mio modello di minaccia?
        acceptedAnswer:
          "@type": Answer
          text: |
            Spesso, vediamo le persone descrivere i modelli di minaccia per la privacy come eccessivamente complessi. Spesso, queste soluzioni includono problemi come molti profili email differenti o configurazioni complicaate, con molte parti mobili e condizioni. Le risposte sono solitamente risposte a "qual è il modo migliore per fare X?"
            Trovare la soluzione "migliore" per te non significa necessariamente che ne stai cercando una infallibile con dozzine di condizioni: queste soluzioni sono spesso difficili da gestire in modo realistico. Come discusso in precedenza, la sicurezza va spesso a scapito della comodità.
---

## "Il software open-source è sempre sicuro" o "il software proprietario è più sicuro"

Questi miti derivano da una serie di pregiudizi, ma la disponibilità del codice sorgente e le modalità di licenza del software, non influiscono intrinsecamente sulla sua sicurezza, in alcun modo. ==I software open source hanno il *potenziale* di essere più sicuri di quelli proprietari, maa non esiste assolutamente alcuna garanzia che sia così.== Quando valuti il software, dovresti esaminare la reputazione e la sicurezza di ogni strumento, su base individuale.

I software open source *possono* essere controllati da terze parti e, spesso, sono più trasparenti sulle potenziali vulnerabilità, rispetto alle controparti proprietarie. Inoltre, ti consentono di revisionare il codice e disabilitare qualsiasi funzionalità sospetta tu trovi. Tuttavia, *a meno che non lo faccia*, non esiste alcuna garanzia che il codice sia mai stato valutato, specialmente con i progetti software più piccoli. Il procedimento di sviluppo aperto, talvolta, è inoltre stato sfruttato per introdurre nuove vulnerabilità in progetti anche di grandi dimensioni.[^1]

D'altra parte, i software proprietari sono meno trasparenti, ma ciò non implica che non siano sicuri. I grandi progetti di software proprietari sono controllabili internamente e da agenzie di terze parti, e i ricercatori indipendenti sulla sicurezza possono comunque trovare vulnerabilità, con tecniche come l'ingegneria inversa.

Per evitare decisioni di parte, è *fondamentale* che tu valuti gli standard di privacy e sicurezza del software che utilizzi.

## "Spostare la fiducia può incrementare la privacy"

Parliamo molto di "spostamento della fiducia", discutendo di soluzioni come le VPN (che la spostano dal tuo ISP al fornitore VPN). Sebbene queste proteggano i tuoi dati di navigazione dal tuo ISP *nello specifico*, il fornitore dell VPN che scegli ha comunque accesso a essi: i tuoi dati non sono completamente protetti da tutte le parti. Ciò implica che:

1. Devi prestaare attenzione scegliendo un fornitore a cui spostare la fiducia.
2. Dovresti comunque utilizzare altre tecniche, come l'E2EE, per proteggere completamente i tuoi dati. Diffidare meramente di un fornitore per fidarsi di un altro, non protegge i tuoi dati.

## "Le soluzioni incentrate sulla privacy sono intrinsecamente affidabili"

Concentrarsi soltanto sulle politiche sulla privacy e sul marketing di uno strumento o fornitore, può rendere cechi alle sue debolezze. Quando si cerca una soluzione più privata, è necessario determinare il problema di fondo e trovare soluzioni tecniche per risolverlo. Ad esempio, potresti voler evitare Google Drive, che dà a Google l'accesso a tutti i tuoi dati. Il problema di fondo, in questo caso, è la mancanza dell'E2EE, quindi, dovresti assicurare che il fornitore a cui passi la implementi effettivamente, o utilizzare uno strumento (come [Cryptomator](../encryption.md#cryptomator-cloud)), che la fornisca su qualsiasi fornitore su cloud. Passare a un fornitore "incentrato sulla privacy" (che non implementa l'E2EE), non risolve il tuo problema: sposta la fiducia da Google a quel fornitore.

Le politiche sulla privacy e le pratiche aziendali dei fornitori che scegli sono molto importaanti, ma dovrebbero essere considerate secondarie alle garanzie di sicurezza della tua privacy: non dovresti spostare la fiducia a un altro fornitore, quando fidarsene non è affatto un requisito.

## "Complicato è meglio"

Spesso, vediamo le persone descrivere i modelli di minaccia per la privacy come eccessivamente complessi. Spesso, queste soluzioni includono problemi come molti profili email differenti o configurazioni complicaate, con molte parti mobili e condizioni. Solitamente, si tratta solitamente di risposte a "Qual è il metodo migliore per fare *X*?"

Trovare la soluzione "migliore" per te non significa necessariamente che ne stai cercando una infallibile con dozzine di condizioni: queste soluzioni sono spesso difficili da gestire in modo realistico. Come discusso in precedenza, la sicurezza va spesso a scapito della comodità. Di seguito, forniamo alcuni suggerimenti:

1. ==Le azioni devono servire uno scopo in particolare:== pensa a come fare ciò che desideri con il minor numero possibile di azioni.
2. ==Rimuovi i punti di fallimento umani:== Falliamo, ci stanchiamo e dimentichiamo le cose. Per mantenere la sicurezza, evita di affidarti a condizioni e procedimenti manuali che devi ricordare.
3. ==Utilizza il giusto livello di protezione per ciò che intendi fare.== Spesso, vediamo consigli delle cosiddette soluzioni a prova di autorità o citazione in giudizio. Spesso, richiedono conoscenze specialistiche e, generalmente, non sono ciò che la gente desidera. Non ha senso creare un intricato modello di minaccia per l'anonimato, se puoi essere facilmente deanonimizzato da una semplice svista.

Quindi, come potrebbe apparire?

Uno dei modelli di minaccia più chiri è quello in cui le persone *ti conoscono* e uno in cui non ti conoscono. Ci saranno sempre situazioni in cui dovrai dichiarare il tuo nome legale, e altre in cui non sarà necessario.

1. **Identità nota**: Un'identità nota è utilizzata per le cose in cui devi dichiarare il tuo nome. Esistono molti documenti legali e contratti in cui l'identità legale è necessaria. Questi possono andare dall'apertura di un conto bancario, la firma di affitto di una proprietà, l'ottenimento di un passaporto, dichiarazioni personalizzate per l'importazione di articoli, o altri rapporti con il tuo governo. Solitamente, queste cose, richiedono credenziali quali carte di credito, controlli di affidabilità creditizia, numeri di conto e, possibilmente, indirizzi fisici.

    Non suggeriamo di utilizzare alcuna VPN o Tor per queste cose, poiché la tua identità è già nota tramite altri mezzi.

    !!! tip
   
        Acquistando online, l'utilizzo di un [Paccomat](https://it.wikipedia.org/wiki/Paccomat), può contribuire a mentenere privato il tuo indirizzo email.

2. **Identità sconosciuta**: Un'identità sconosciuta potrebbe essere uno pseudonimo stabile che utilizzi regolarmente. Non è anonimo perché non cambia. Se fai parte di una community online, potresti voler mantenere un'identità nota ad altri. Questo pseudonimo non è anonimo perché, se monitorato abbastanza a lungo, i dettagli sul proprietario potrebbero rilevare ulteriori informazioni, come il modo in cui scrive, le sue conoscenze generali su argomenti d'interesse, etc.

    Potresti voler utilizzare una VPN per questo, per mascherare il tuo indirizzo IP. Le transazioni finanziarie sono più difficili da mascherare: potresti considerare l'utilizzo di criptovalute anonime, come [Monero](https://www.getmonero.org/). L'utilizzo del cambio di criptovalute, inoltre, potrebbe aiutare a distinguere l'origine della valuta. Tipicamente, le piattaforme di scambio richiedono il completamento della KYC (conoscenza del cliente), prima di consentirti di scambiare valuta legale per qualsiasi tipo di criptovaluta. Anche le opzioni di incontro locali potrebbero essere una soluzione; tuttavia, sono spesso più costose e, talvolta, richiedono la KYC.

3. **Identità anonima**: Anche con l'esperienza, le identità anonime sono difficili da mantenere per lunghi periodi di tempo. Dovrebbero essere identità a breve termine e di breve durata, a rotazione regolare.

    In questo caso, l'utilizzo di Tor può aiutare. Vale anche la pena di notare che un anonimato maggiore è possibile, tramite la comunicazione asincrona: la comunicazione in tempo reale è vulnerabile alle analisi dei modelli di digitazione (cioè, più di un paragrafo di testo, distribuito su un forum, via email, etc.)

[^1]: Un notevole esempio è quello dell'[incidente del 2021, in cui i ricercatori dell'Università del Minnesota hanno introdotto tre vulnerabilità nel progetto di sviluppo del kernel Linux](https://cse.umn.edu/cs/linux-incident).
