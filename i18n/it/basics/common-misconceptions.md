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

I software open source *possono* essere controllati da terze parti e, spesso, sono più trasparenti sulle potenziali vulnerabilità, rispetto alle controparti proprietarie. Inoltre, ti consentono di revisionare il codice e disabilitare qualsiasi funzionalità sospetta tu trovi. Tuttavia, *a meno che non lo faccia*, non esiste alcuna garanzia che il codice sia mai stato valutato, specialmente con i progetti software più piccoli. Il procedimento di sviluppo aperto, talvolta, è inoltre stato sfruttato per introdurre nuove vulnerabilità in progetti anche di grandi dimensioni.[^1]

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

Spesso, vediamo le persone descrivere i modelli di minaccia per la privacy come eccessivamente complessi. Spesso queste soluzioni includono problemi come l'uso di molteplici account di posta elettronica o di configurazioni complicate con molte parti mobili e condizioni. Solitamente, si tratta solitamente di risposte a "Qual è il metodo migliore per fare *X*?"

Trovare la soluzione "migliore" per te non significa necessariamente che ne stai cercando una infallibile con dozzine di condizioni: queste soluzioni sono spesso difficili da gestire in modo realistico. Come discusso in precedenza, la sicurezza va spesso a scapito della comodità. Di seguito, forniamo alcuni suggerimenti:

1. ==Le azioni devono servire uno scopo in particolare:== pensa a come fare ciò che desideri con il minor numero possibile di azioni.
2. ==Rimuovi i punti di fallimento umani:== Falliamo, ci stanchiamo e dimentichiamo le cose. Per mantenere la sicurezza, evita di affidarti a condizioni e procedimenti manuali che devi ricordare.
3. ==Utilizza il giusto livello di protezione per ciò che intendi fare.== Spesso, vediamo consigli delle cosiddette soluzioni a prova di autorità o citazione in giudizio. Spesso, richiedono conoscenze specialistiche e, generalmente, non sono ciò che la gente desidera. Non ha senso creare un intricato modello di minaccia per l'anonimato, se puoi essere facilmente deanonimizzato da una semplice svista.

Quindi, come potrebbe apparire?

Uno dei modelli di minaccia più chiari è quello in cui le persone *ti conoscono* e uno in cui non ti conoscono. Ci saranno sempre situazioni in cui dovrai dichiarare il tuo nome legale, e altre in cui non sarà necessario.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Suggerimento</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: One notable example of this is the [2021 incident in which University of Minnesota researchers introduced three vulnerabilities into the Linux kernel development project](https://cse.umn.edu/cs/linux-incident).
