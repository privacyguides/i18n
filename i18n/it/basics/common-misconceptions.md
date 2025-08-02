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
        name: Il software open source è intrinsecamente sicuro?
        acceptedAnswer:
          "@type": Answer
          text: |
            Il fatto che il codice sorgente sia disponibile e la licenza a cui è sottoposto il software non implica che il codice sia sicuro a prescindere. I software open source potrebbero essere più sicuri dei software proprietari, ma non esiste assolutamente alcuna garanzia che sia così. Valutando i software, dovresti considerare la reputazione e la sicurezza di ogni strumento, su una base individuale.
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
            Spesso, vediamo le persone descrivere i modelli di minaccia per la privacy come eccessivamente complessi. Spesso queste soluzioni includono problemi come l'uso di molteplici account di posta elettronica o di configurazioni complicate con molte parti mobili e condizioni. Le risposte sono solitamente risposte a "qual è il modo migliore per fare X?"
            Trovare la soluzione "migliore" per te non significa necessariamente che ne stai cercando una infallibile con dozzine di condizioni: queste soluzioni sono spesso difficili da gestire in modo realistico. Come discusso in precedenza, la sicurezza va spesso a scapito della comodità.
---

## "I software open source sono sempre sicuri" o "I software proprietari sono più sicuri"

Questi miti derivano da una serie di pregiudizi, ma la disponibilità del codice sorgente e le modalità di licenza del software, non influiscono intrinsecamente sulla sua sicurezza, in alcun modo. ==I software open source hanno il *potenziale* di essere più sicuri di quelli proprietari, ma non esiste assolutamente alcuna garanzia che sia così.== Quando valuti il software, dovresti esaminare la reputazione e la sicurezza di ogni strumento, su base individuale.

I software open source *possono* essere controllati da terze parti e, spesso, sono più trasparenti sulle potenziali vulnerabilità, rispetto alle controparti proprietarie. Inoltre, ti consentono di revisionare il codice e disabilitare qualsiasi funzionalità sospetta tu trovi. Tuttavia, *a meno che non lo faccia*, non esiste alcuna garanzia che il codice sia mai stato valutato, specialmente con i progetti software più piccoli. Il processo di sviluppo aperto è stato talvolta sfruttato per introdurre nuove vulnerabilità, note come [:material-package-variant-closed-remove: Attacchi alla Supply Chain](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, che sono ulteriormente discussi nella nostra pagina delle [Minacce Comuni](common-threats.md).[^1]

D'altra parte, i software proprietari sono meno trasparenti, ma ciò non implica che non siano sicuri. I grandi progetti di software proprietari sono controllabili internamente e da agenzie di terze parti, e i ricercatori indipendenti sulla sicurezza possono comunque trovare vulnerabilità, con tecniche come l'ingegneria inversa.

Per evitare decisioni di parte, è *fondamentale* che tu valuti gli standard di privacy e sicurezza del software che utilizzi.

## "Spostare la fiducia può incrementare la privacy"

Parliamo molto di "spostamento della fiducia", discutendo di soluzioni come le VPN (che la spostano dal tuo ISP al fornitore VPN). Sebbene queste proteggano i tuoi dati di navigazione dal tuo ISP *nello specifico*, il fornitore dell VPN che scegli ha comunque accesso a essi: i tuoi dati non sono completamente protetti da tutte le parti. Ciò implica che:

1. Devi prestare attenzione scegliendo un fornitore a cui spostare la fiducia.
2. Dovresti comunque utilizzare altre tecniche, come l'E2EE, per proteggere completamente i tuoi dati. Diffidare meramente di un fornitore per fidarsi di un altro, non protegge i tuoi dati.

## "Le soluzioni incentrate sulla privacy sono intrinsecamente affidabili"

Concentrarsi soltanto sulle politiche sulla privacy e sul marketing di uno strumento o fornitore, può rendere cechi alle sue debolezze. Quando stai cercando una soluzione più privata, dovresti determinare il problema di fondo e trovare soluzioni tecniche per risolverlo. Ad esempio, potresti voler evitare Google Drive, che dà a Google l'accesso a tutti i tuoi dati. Il problema di fondo, in questo caso, è la mancanza dell'E2EE, quindi, dovresti assicurare che il fornitore a cui passi la implementi effettivamente, o utilizzare uno strumento (come [Cryptomator](../encryption.md#cryptomator-cloud)), che la fornisca su qualsiasi fornitore su cloud. Passare a un fornitore "incentrato sulla privacy" (che non implementa l'E2EE), non risolve il tuo problema: sposta la fiducia da Google a quel fornitore.

Le politiche sulla privacy e le pratiche aziendali dei fornitori che scegli sono molto importanti, ma dovrebbero essere considerate secondarie alle garanzie di sicurezza della tua privacy: non dovresti spostare la fiducia a un altro fornitore, quando fidarsene non è affatto un requisito.

## "Complicato è meglio"

Spesso, vediamo le persone descrivere i modelli di minaccia per la privacy come eccessivamente complessi. Spesso queste soluzioni includono problemi come l'uso di molteplici account di posta elettronica o di configurazioni complicate con molte parti in movimento e condizioni. Solitamente, si tratta solitamente di risposte a "Qual è il metodo migliore per fare *X*?"

Trovare la soluzione "migliore" per te non significa necessariamente che ne stai cercando una infallibile con dozzine di condizioni: queste soluzioni sono spesso difficili da gestire in modo realistico. Come discusso in precedenza, la sicurezza va spesso a scapito della comodità. Di seguito, forniamo alcuni suggerimenti:

1. ==Le azioni devono servire uno scopo in particolare:== pensa a come fare ciò che desideri con il minor numero possibile di azioni.
2. ==Rimuovi i punti di fallimento umani:== Falliamo, ci stanchiamo e dimentichiamo le cose. Per mantenere la sicurezza, evita di affidarti a condizioni e procedimenti manuali che devi ricordare.
3. ==Utilizza il giusto livello di protezione per ciò che intendi fare.== Spesso, vediamo consigli delle cosiddette soluzioni a prova di autorità o citazione in giudizio. Spesso, richiedono conoscenze specialistiche e, generalmente, non sono ciò che la gente desidera. Non ha senso creare un intricato modello di minaccia per l'anonimato, se puoi essere facilmente deanonimizzato da una semplice svista.

Quindi, come potrebbe apparire?

Uno dei modelli di minaccia più chiari è quello in cui le persone *ti conoscono* e uno in cui non ti conoscono. Ci saranno sempre situazioni in cui dovrai dichiarare il tuo nome legale, e altre in cui non sarà necessario.

1. **Identità nota** - L'identità nota viene utilizzata per i casi in cui è necessario dichiarare il proprio nome. Ci sono molti documenti legali e i contratti per i quali è richiesta un'identità legale. Si può trattare dell'apertura di un conto bancario, della firma di un contratto di locazione immobiliare, dell'ottenimento di un passaporto, delle dichiarazioni doganali per l'importazione di articoli o di altri rapporti con il governo. Solitamente, queste cose, richiedono credenziali quali carte di credito, controlli di affidabilità creditizia, numeri di conto e, possibilmente, indirizzi fisici.

    Non suggeriamo di utilizzare una VPN o Tor per queste cose, poiché la vostra identità è già nota attraverso altri mezzi.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Suggerimento</p>

    Quando si fanno acquisti online, l'uso di un [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) può aiutare a mantenere privato l'indirizzo fisico.

    </div>

2. **Identità sconosciuta** - Un'identità sconosciuta potrebbe essere uno pseudonimo stabile che si usa regolarmente. Non è anonimo perché non cambia. Se si fa parte di una comunità online, si potrebbe voler mantenere un personaggio che gli altri conoscono. Questo pseudonimo non è anonimo perché, se monitorato abbastanza a lungo, i dettagli sul proprietario possono rivelare ulteriori informazioni, come il modo in cui scrive, la sua conoscenza generale degli argomenti di interesse, ecc.

    A tal fine, è possibile utilizzare una VPN per mascherare il proprio indirizzo IP. Le transazioni finanziarie sono più difficili da mascherare: Potresti considerare l'utilizzo di criptovalute anonime, come [Monero](../cryptocurrency.md#monero). L'utilizzo del cambio di altcoin può anche aiutare a nascondere l'origine della valuta. In genere, le borse richiedono il completamento del KYC (conosci il tuo cliente) prima di consentire lo scambio di valuta fiat in qualsiasi tipo di criptovaluta. Anche le opzioni di incontro locali possono essere una soluzione; tuttavia, spesso sono più costose e talvolta richiedono anche il KYC.

3. **Identità anonima** - Anche con esperienza, le identità anonime sono difficili da mantenere per lunghi periodi di tempo. Dovrebbero essere identità a breve termine e di breve durata che vengono regolarmente cambiate.

    L'uso di Tor può aiutare in questo senso. Vale anche la pena di notare che un maggiore anonimato è possibile attraverso la comunicazione asincrona: La comunicazione in tempo reale è vulnerabile all'analisi dei modelli di digitazione (ad es. più di un paragrafo di testo, distribuito su un forum, via e-mail, ecc.)

[^1]: Un notevole attacco alla supply chain si è verificato nel marzo 2024, quando un manutentore malintenzionato ha aggiunto una backdoor offuscata in `xz`, una popolare libreria di compressione. La backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) era destinata a consentire a un soggetto sconosciuto l'accesso remoto alla maggior parte dei server Linux tramite SSH, ma è stata scoperta prima che fosse ampiamente diffusa.
