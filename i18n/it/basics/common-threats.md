---
title: "Minacce comuni"
icon: 'material/eye-outline'
description: Il tuo modello di minaccia è personale, ma queste sono alcuni aspetti che stanno a cuore a molti visitatori di questo sito web.
---

In linea di massima, le nostre raccomandazioni sono suddivise in [minacce](threat-modeling.md) o obiettivi che si applicano alla maggior parte delle persone. ==Potresti essere interessato a nessuna, una, alcune o tutte queste possibilità==, e gli strumenti e servizi che utilizzi dipendono dai tuoi obiettivi. Potreste avere minacce specifiche anche al di fuori di queste categorie, il che è perfettamente normale! La parte importante è lo sviluppo di una comprensione dei benefici e difetti degli strumenti che scegli di utilizzare, poiché virtualmente nessuno di essi ti proteggerà da ogni minaccia.

- <span class="pg-purple">:material-incognito: Anonimato</span> - Proteggono la tua attività online dalla tua identità reale, proteggendoti da persone che mirano a scoprire la *tua* identità nello specifico.
- <span class="pg-red">:material-target-account: Attacchi mirati</span> - Protezione da hacker o altri malintenzionati, che mirano ad accedere ai *tuoi* dati o dispositivi, nello specifico.
- <span class="pg-orange">:material-bug-outline: Attacchi passivi</span> - Protezione da malware, violazioni di dati e altri attacchi effettuati contro molte persone, in una singola volta.
- <span class="pg-viridian">:material-package-variant-closed-remove: Attacchi alla supply chain</span> - Una vulnerabilità o un exploit introdotto in un software altrimenti valido, direttamente o attraverso una dipendenza di terze parti.
- <span class="pg-teal">:material-server-network: Service Providers</span> - Protezione dei tuoi dati dai fornitori del servizio (es., con l'E2EE, che rende i tuoi dati illeggibili dal server).
- <span class="pg-blue">:material-eye-outline: Sorveglianza di massa</span> - Protezione dalle agenzie governative, organizzazioni, siti web e servizi che cooperano per tracciare le tue attività.
- <span class="pg-brown">:material-account-cash: Capitalismo di sorveglianza</span> - Protezione dalle grandi reti pubblicitarie, come Google e Facebook, nonché da una miriade di altri raccoglitori di dati di terze parti.
- <span class="pg-green">:material-account-search: Esposizione pubblica</span> - Limitazione delle informazioni accessibili online su di te, ai motori di ricerca o al pubblico generale.
- <span class="pg-blue-gray">:material-close-outline: Censura</span> - Prevenzione dell'accesso censurato a informazioni, o della tua censura, comunicando online.

Alcune di queste minacce potrebbero essere per te più importanti di altre, a seconda delle tue preoccupazioni specifiche. Ad esempio, uno sviluppatore di software con accesso a dati preziosi o critici potrebbe essere interessato principalmente a <span class="pg-viridian">:material-package-variant-closed-remove: Attacchi alla supply chain</span> e <span class="pg-red">:material-target-account: Attacchi mirati</span>. Probabilmente vorranno ancora proteggere i loro dati personali dall'essere travolti nei programmi di <span class="pg-blue">:material-eye-outline: Sorveglianza di massa </span>. Similmente, in molto potrebbero essere principalmente preoccupati dall'<span class="pg-green">:material-account-search: Esposizione Pubblica</span> dei propri dati personali, pur rimanendo attendi ai problemi di sicurezza, come gli <span class="pg-orange">:material-bug-outline: Attacchi Passivi</span>, come i malware che colpiscono i loro dispositivi.

## Anonimato vs. Privacy

<span class="pg-purple">:material-incognito: Anonimato</span>

L'anonimato viene spesso confuso con la privacy, ma si tratta di concetti distinti. Mentre la privacy è una serie di scelte che effettui sull'utilizzo e la condivisione dei tuoi dati, l'anonimato è la dissociazione completa delle tue attività online dalla tua identità reale.

Informatori e giornalisti, ad esempio, possono avere un modello di minaccia molto più estremo, che richiede il totale anonimato. Questo non prevede soltanto il nascondere ciò che fanno, quali dati possiedono e non subire violazioni da malintenzionati o governi, ma anche nascondere interamente chi sono. Spesso, sacrificheranno qualsiasi tipo di comodità per proteggere il proprio anonimato, la propria privacy o sicurezza, poiché le loro vite potrebbero dipendere da ciò. Gran parte delle persone non necessitano di così tanto.

## Sicurezza e Privacy

<span class="pg-orange">:material-bug-outline: Attacchi Passivi</span>

La sicurezza e la privacy sono spesso confuse, poiché necessiti di sicurezza per ottenere qualsiasi parvenza di privacy: utilizzare strumenti, anche se privati di design, è futile se, questi, potrebbero essere facilmente sfruttati dai malintenzionati che, in seguito, rilasceranno i tuoi dati. Tuttavia, l'opposto non è necessariamente vero: il servizio più sicuro al mondo *non è necessariamente* privato. Il migliore esempio è affidare i dati a Google che, date le sue dimensioni, ha subito pochi incidenti di sicurezza, assumendo esperti di sicurezza leader del settore, per proteggere la propria infrastruttura. Sebbene Google offra servizi molto sicuri, pochissime persone considererebbero privati i propri dati nei prodotti gratuiti di Google per i clienti (Gmail, YouTube, etc.)

Per quanto riguarda la sicurezza delle applicazioni, generalmente, non sappiamo (e talvolta non possiamo sapere) se il software che utilizziamo è dannoso, o se potrebbe un giorno diventarlo. Anche con gli sviluppatori più affidabili, generalmente non esiste alcuna garanzia che il loro software non presenti una grave vulnerabilità, che potrebbe essere successivamente sfruttata.

Per minimizzare i danni che un software malevolo *potrebbe* causare, dovresti utilizzare la sicurezza per la compartimentazione. Ad esempio, ciò potrebbe presentarsi nell'utilizzo di computer differenti per lavori differenti, utilizzando macchine virtuali per separare i gruppi differenti di applicazioni correlate, o utilizzando un sistema operativo sicuro con una forte attenzione al sandboxing delle applicazioni e il controllo obbligatorio degli accessi.

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

I sistemi operativi per mobile, generalmente, presentano un migliore sandboxing delle applicazioni, rispetto ai sistemi operativi per desktop: le app possono ottenere l'accesso di root e richiedono l'autorizzazione per accedere alle risorse di sistema.

Generalmente, i sistemi operativi per desktop sono in ritardo, per l'adeguato sandboxing. ChromeOS ha funzionalità di sandboxing simili ad Android e macOS ha il pieno controllo delle autorizzazioni di sistema (e gli sviluppatori possono optare per il sandboxing delle applicazioni). Tuttavia, questi sistemi operativi trasmettono le informazioni identificativi ai rispettivi OEM. Linux tende a non inviare le informazioni ai fornitori del sistema, ma presenta una scarsa protezione da exploit e applicazioni dannose. Ciò si può in qualche modo mitigare con distribuzioni specializzate che fanno significativo utilizzo di macchine virtuali o contenitori, come [Qubes OS](../desktop.md#qubes-os).

</div>

<span class="pg-red">:material-target-account: Attacchi Mirati</span>

Gli attacchi mirati contro una persona specifica sono più problematici da affrontare. Gli attacchi comuni includono l'invio di documenti dannosi via email, lo sfruttamento delle vulnerabilità (es., nei browser e nei sistemi operativi) e gli attacchi fisici. Se per voi queste sono preoccupazioni, dovresti impiegare strategie di mitigazione delle minacce più avanzate.

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Per loro natura, i **browser web**, i **client email** e le **applicazioni per ufficio**, eseguono tipicamente del codice non attendibile, inviato da terzi. L'esecuzione di più macchine virtuali, per separare applicazioni simili dal tuo sistema di hosting, nonché da ogni altra, è una tecnica utilizzabile per mitigare la probabilità che un exploit di queste applicazioni comprometta il resto del tuo sistema. Ad esempio, le tecnologie come QubesOS o Microsoft Defender Application Guard su Windows, forniscono comodi metodi per farlo.

</div>

Se temi un **attacco fisico**, dovresti utilizzare un sistema operativo con un'implementazione sicura dell'avvio protetto, come Android, iOS, macOS, o [Windows (con TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Inoltre, dovresti assicurarti che la tua unità sia crittografata e che il sistema operativo utilizzi un TPM o Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) od [Element](https://developers.google.com/android/security/android-ready-se), per limitare la frequenza dei tentativi di inserire la frase segreta crittografica. Dovresti evitare di condividere il tuo computer con persone di cui non ti fidi, poiché gran parte dei sistemi operativi per desktop non crittografa i dati separatamente, per ogni utente.

<span class="pg-viridian">:material-package-variant-closed-remove: Attacchi alla supply chain</span>

Gli attacchi alla supply chain sono spesso una forma di <span class="pg-red">:material-target-account: Attacchi mirati</span> verso aziende, governi e attivisti, sebbene possano finire per compromettere anche il pubblico.

<div class="admonition example" markdown>
<p class="admonition-title">Esempio</p>

Un esempio degno di nota è successo nel 2017 quando M.E.Doc, un software di contabilità molto diffuso in Ucraina, è stato infettato dal virus *NotPetya*, infettando successivamente con il ransomware coloro che avevano scaricato il software. NotPetya è stato un attacco ransomware che ha colpito più di 2000 aziende in vari Paesi e si è basato sull'exploit *EternalBlue* sviluppato dall'NSA per attaccare i computer Windows in rete.

</div>

Ci sono pochi modi in cui questo tipo di attacco potrebbe essere effettuato:

1. Un collaboratore o un dipendente potrebbe farsi strada in una posizione di potere all'interno di un progetto o di un'organizzazione, per poi abusarne aggiungendo codice malevolo.
2. Uno sviluppatore può essere costretto da un soggetto esterno ad aggiungere codice malevolo.
3. Un individuo o un gruppo potrebbe identificare una dipendenza software di terze parti (nota anche come libreria) e lavorare per infiltrarla con i due metodi sopra descritti, sapendo che verrà utilizzata dagli sviluppatori di software "a valle".

Questi tipi di attacchi possono richiedere molto tempo e preparazione per essere eseguiti e sono rischiosi perché possono essere rilevati, in particolare nei progetti open source se sono popolari e hanno interessi esterni. Purtroppo sono anche uno dei più pericolosi, in quanto molto difficili da mitigare completamente. Invitiamo i lettori a utilizzare solo software che godono di buona reputazione e che si sforzano di mitigare i rischi:

1. Adottando solo software popolari che esistono da tempo. Maggiore è l'interesse per un progetto, maggiore è la probabilità che le parti esterne notino cambiamenti malevoli. Un attore malintenzionato dovrà inoltre dedicare più tempo a guadagnare la fiducia della comunità con contributi significativi.
2. Trovando software che rilasci il codice sorgente con piattaforme d'infrastruttura di compilazione affidabili e ampiamente diffuse, rispetto alle workstation degli sviluppatori oppure a server self-hosted. Alcuni sistemi come GitHub Actions consentono di ispezionare lo script di compilazione che viene eseguito pubblicamente per una maggiore sicurezza. In questo modo si riduce la probabilità che il malware presente sul computer di uno sviluppatore possa infettare i suoi pacchetti e si ha la certezza che i codici sorgente prodotti siano effettivamente corretti.
3. Cercando la firma del codice sui singoli commit e rilasci di codice sorgente, per creare una traccia verificabile di chi ha fatto cosa. Ad esempio: Il codice malevolo era presente nell'archivio del software? Quale sviluppatore l'ha aggiunto? È stato aggiunto durante la compilazione?
4. Controllando se il codice sorgente ha messaggi di commit significativi (come i [commit convenzionali](https://conventionalcommits.org)) che spiegano che cambiamento la modifica dovrebbe realizzare. Messaggi chiari possono facilitare la verifica, la revisione e la ricerca di bug da parte di persone esterne al progetto.
5. Annotando il numero di collaboratori o manutentori di un programma. Uno sviluppatore solitario può essere più suscettibile alla costrizione ad aggiungere codice malevolo da una parte esterna o di abilitare per negligenza un comportamento indesiderato. Questo potrebbe significare che il software sviluppato da "Big Tech" è soggetto a maggiori controlli rispetto a uno sviluppatore solitario che non risponde a nessuno.

## Privacy dai fornitori del servizio

<span class="pg-teal">:material-server-network: Fornitori di Servizi</span>

Viviamo in un mondo in cui quasi tutto è connesso a Internet. I nostri messaggi, email e interazioni sociali "privati" sono tipicamente memorizzati su un server, da qualche parte. In genere, quando invii un messaggio a qualcuno, è memorizzato su un server e, quando i tuoi amici vogliono leggerlo, il server glielo mostra.

Il problema evidente è che il fornitore del servizio (o un hacker che ha compromesso il server), può accedere alle tue conservazioni quando e come vuole, senza che tu te ne accorga. Ciò si applica a molti servizi comuni, come la messaggistica SMS, Telegram e Discord.

Fortunatamente, l'E2EE può alleviare questo problema crittografando le comunicazioni tra te e i tuoi destinatari desiderati, persino prima che siano inviate al server. La confidenzialità dei tuoi messaggi è garantita, supponendo che il fornitore del servizio non abbia accesso alle chiavi private di ambe le parti.

<div class="admonition note" markdown>
<p class="admonition-title">Nota sulla crittografia basata su Web</p>

In pratica, l'efficacia delle diverse implementazioni E2EE varia. Le applicazioni, come [Signal](../real-time-communication.md#signal), operano nativamente sul tuo dispositivo e ogni copia dell'applicazione è la stessa tra diverse installazioni. Se il fornitore del servizio introducesse una [backdoor](https://it.wikipedia.org/wiki/Backdoor) nella propria applicazione, tentando di rubare le tue chiavi private, sarebbe successivamente rilevabile con l'[ingegneria inversa](https://it.wikipedia.org/wiki/Reverse_engineering).

D'altra parte, le implementazioni E2EE basate sul web, come la webmail di Proton Mail o il *Web Vault* di Bitwarden, si affidano al fatto che il server serve dinamicamente il codice in JavaScript al browser, per gestire la crittografia. Un server malintenzionato può prenderti di mira, inviandoti codice dannoso in JavaScript per rubare la tua chiave crittografica (cosa estremamente difficile da notare). Poiché il server può scegliere di servire client differenti a persone differenti, anche se notassi l'attacco, sarebbe incredibilmente difficile provare la colpevolezza del fornitore.

Dunque, dovresti utilizzare le applicazioni native, invece dei client web, quando possibile.

</div>

Anche con l'E2EE, i fornitori dei servizi possono comunque profilarti secondo i **metadati**, che tipicamente non sono protetti. Sebbene il fornitore del servizio non possa leggere i tuoi messaggi, può comunque osservare cose importanti, come con chi stai parlando, quanto spesso gli invii messaggi e quando sei tipicamente attivo. La protezione dei metadati è abbastanza rara e, se rientra nel tuo [modello di minaccia](threat-modeling.md), dovresti prestare molta attenzione alla documentazione tecnica del software che stai utilizzando, per scoprire se è prevista alcuna minimizzazione o protezione dei metadati.

## Programmi di sorveglianza di massa

<span class="pg-blue">:material-eye-outline: Sorveglianza di massa</span>

La sorveglianza di massa consiste nell'intricato sforzo di monitorare il "comportamento, molte attività o informazioni" di un'intera (o di una sostanziale frazione di una) popolazione.[^1] Spesso si riferisce a programmi governativi, come quelli [divulgati da Edward Snowden, nel 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Tuttavia, può essere anche svolta dalle aziende, per conto di agenzie governative o di propria iniziativa.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlante della sorveglianza</p>

Se vuoi saperne di più sui metodi di sorveglianza e su come vengono attuati nella tua città, puoi anche dare un'occhiata a [Atlas of Surveillance](https://atlasofsurveillance.org/) della [Electronic Frontier Foundation](https://eff.org/).

In Francia puoi consultare il [sito web di Technopolice](https://technopolice.fr/villes) gestito dall'associazione non-profit La Quadrature du Net.

</div>

Spesso, i governi, giustificano i programmi di sorveglianza di massa come mezzi necessari per combattere il terrorismo e prevenire il crimine. Tuttavia, violando i diritti umani, sono spesso utilizzati per colpire in modo sproporzionato gruppi di minoranza e dissidenti politici, tra gli altri.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">La lezione sulla privacy dell'11 settembre: La sorveglianza di massa non è la strada da seguire</a></em></p>

Di fronte alle rivelazioni di Edward Snowden su programmi governativi come [PRISM](https://en.wikipedia.org/wiki/PRISM) e [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), i funzionari dell'intelligence hanno ammesso che l'NSA ha raccolto segretamente per anni i dati relativi alle telefonate di quasi tutti gli americani: chi chiama chi, quando vengono effettuate le chiamate e quanto durano. Questo tipo di informazioni, accumulate dall'NSA giorno dopo giorno, possono rivelare dettagli incredibilmente sensibili sulle vite delle persone e le associazioni, come se hanno chiamato un prete, una struttura preposta all'aborto, un consulente per le dipendenze o una linea diretta anti-suicidi.

</div>

Nonostante la crescente sorveglianza di massa negli Stati Uniti, il governo ha riscontrato che i programmi di sorveglianza di massa come la Sezione 215 hanno avuto "poco valore univoco", per quanto riguarda l'arresto di crimini reali o di complotti terroristici, con sforzi che, in gran parte, duplicano i programmi di sorveglianza mirata del FBI.[^2]

Online è possibile essere rintracciati con svariati metodi:

- Il tuo indirizzo IP
- I cookie del browser
- I dati che invii ai siti web
- L'impronta digitale del tuo browser o dispositivo
- Correlazione del metodo di pagamento

\[Questo elenco non è completo].

Se sei preoccupato per i programmi di sorveglianza di massa, puoi usare strategie come separare le tue identità online, confonderti con altri utenti o, quando possibile, semplicemente evitare di fornire informazioni identificative.

<span class="pg-brown">:material-account-cash: Capitalismo di sorveglianza</span>

> Il capitalismo di sorveglianza è un sistema economico incentrato sulla cattura e commercializzazione dei dati personali, con l'obiettivo principale di trarre profitto.[^3]

Per molti, il tracciamento e la sorveglianza dalle aziende private è una preoccupazione crescente. Le reti pubblicitarie pervasive, come quelle gestite da Google e Facebook, si estendono su Internet ben oltre i siti che controllano, tracciando le tue azioni lungo il percorso. Utilizzare strumenti come i blocchi di contenuti per limitare le richieste di rete ai loro server e leggere le politiche sulla privacy dei servizi che utilizzi, può aiutarti a evitare molti avversari di base (sebbene non possa prevenire completamente il tracciamento).[^4]

Inoltre, anche le aziende esterne al settore *AdTech* o di tracciamento, possono condividere le tue informazioni con gli [intermediari di dati](https://en.wikipedia.org/wiki/Information_broker) (come Cambridge Analytica, Experian o Datalogix), o altre parti. Non puoi supporre automaticamente che i tuoi dati siano sicuri semplicemente perché il servizio che stai utilizzando non ricade nel tipico modello aziendale dell'AdTech o di tracciamento. La protezione più forte contro la raccolta aziendale dei dati è crittografare od offuscare i tuoi dati quando possibile, complicando per i diversi fornitori, la correlazione dei dati tra loro e la costruzione di un profilo su di te.

## Limitare le Informazioni Pubbliche

<span class="pg-green">:material-account-search: Esposizione pubblica</span>

Il modo migliore per mantenere privati i tuoi dati è, semplicemente, non renderli pubblici. Eliminare le informazioni indesiderate che trovi su di te online è uno dei migliori primi passi che puoi compiere per recuperare la tua privacy.

- [Visualizza la nostra guida sull'eliminazione degli account :material-arrow-right-drop-circle:](account-deletion.md)

Sui siti dove condividi informazioni, è molto importante controllare le impostazioni sulla privacy del tuo profilo, per limitare quanto ampiamente siano diffusi tali dati. Ad esempio, abilitare la "modalità privata" sui tuoi profili se possibile, assicurando che il tuo profilo non sia indicizzato dai motori di ricerca e che non sia visualizzabile senza la tua autorizzazione.

Se hai già inviato le tue informazioni reali ai siti che non dovrebbero possederle, considera di utilizzare tattiche di disinformazione, come l'invio di informazioni fittizie correlate a tale identità online. Così, le tue informazioni reali non sono distinguibili da quelle false.

## Evitare la Censura

<span class="pg-blue-gray">:material-close-outline: Censura</span>

La censura online è attuabile (in varie misure) da attori tra cui i governi totalitari, gli amministratori di rete e i fornitori dei servizi. Questi sforzi di controllo della comunicazione e di limitazione dell'accesso alle informazioni, saranno sempre incompatibili con il diritto umano alla Libertà d'Espressione.[^5]

La censura sulle piattaforme aziendali è sempre più comune, in quanto piattaforme come Twitter e Facebook cedono alle richieste del pubblico, alle pressioni di mercato e alle pressioni dalle agenzie governative. Le pressioni governative possono essere richieste segrete alle aziende, come la [richiesta di rimozione](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) della Casa Bianca di un video YouTube provocativo, o palesi, come il governo cinese che richiede alle aziende di aderire a un rigido regime di censura.

Le persone preoccupate dalla minaccia della censura possono utilizzare tecnologie come [Tor](../advanced/tor-overview.md) per aggirarla, e supportare le piattaforme di comunicazione resistenti alla censura come [Matrix](../real-time-communication.md#element), prive di autorità centralizzata che possa chiudere arbitrariamente i profili.

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Anche se eludere la censura stessa è facile, nascondere il fatto che lo si stia facendo può essere molto problematico.

Dovresti considerare quali aspetti della rete sono osservabili dal tuo avversario, e se hai la possibilità di negare in modo plausibile le tue azioni. Ad esempio, l'utilizzo di [DNS crittografati](../advanced/dns-overview.md#what-is-encrypted-dns), può aiutarti a superare i sistemi di censura rudimentali e basati sul DNS, ma non può nascondere realmente ciò che visiti dal tuo ISP. Una VPN o Tor possono aiutare a nascondere ciò che stai visitando dagli amministratori di rete, ma non può nascondere il fatto che si stiano utilizzando tali reti. I trasporti collegabili (come Obfs4proxy, Meek o Shadowsocks) possono aiutarti a eludere i firewall che bloccano i protocolli comuni VPN o Tor, ma i tuoi tentativi di elusione possono comunque essere rilevati da metodi come il probing o l'[ispezione approfondita dei pacchetti](https://it.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Devi sempre considerare i rischi di provare a eludere la censura, le potenziali conseguenze e quanto potrebbe essere sofisticato il tuo avversario. Dovresti essere cauto con la tua selezione del software e avere un piano di riserva nel caso in cui dovessi essere scoperto.

[^1]: Wikipedia: [*Sorveglianza di massa*](https://en.wikipedia.org/wiki/Mass_surveillance) e [*Sorveglianza*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: Comitato di Supervisione delle Libertà Civili e della Privacy degli Stati Uniti: [*Rapporto sul Programma dei registri telefonici condotto ai sensi della Sezione 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Capitalismo di sorveglianza*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (o, "elencare tutte le cose cattive che conosciamo"), come molti blocker di contenuti e programmi antivirus fanno, non riesce a proteggerti adeguatamente da minacce nuove e sconosciute perché non sono ancora state aggiunte alla lista dei filtri. Inoltre, dovresti utilizzare altre tecniche di mitigazione.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
