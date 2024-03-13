---
title: "Minacce comuni"
icon: 'material/eye-outline'
description: Il tuo modello di minaccia è personale, ma queste sono alcuni aspetti che stanno a cuore a molti visitatori di questo sito web.
---

In linea di massima, le nostre raccomandazioni sono suddivise in [minacce](threat-modeling.md) o obiettivi che si applicano alla maggior parte delle persone. ==Potresti essere interessato a nessuna, una, alcune o tutte queste possibilità==, e gli strumenti e servizi che utilizzi dipendono dai tuoi obiettivi. Potreste avere minacce specifiche anche al di fuori di queste categorie, il che è perfettamente normale! La parte importante è lo sviluppo di una comprensione dei benefici e difetti degli strumenti che scegli di utilizzare, poiché virtualmente nessuno di essi ti proteggerà da ogni minaccia.

- <span class="pg-purple">:material-incognito: Anonimato</span> - Proteggono la tua attività online dalla tua identità reale, proteggendoti da persone che mirano a scoprire la *tua* identità nello specifico.
- <span class="pg-red">:material-target-account: Attacchi mirati</span> - Protezione da hacker o altri malintenzionati, che mirano ad accedere ai *tuoi* dati o dispositivi, nello specifico.
- <span class="pg-orange">:material-bug-outline: Attacchi passivi</span> - Protezione da malware, violazioni di dati e altri attacchi effettuati contro molte persone, in una singola volta.
- <span class="pg-teal">:material-server-network: Service Providers</span> - Protezione dei tuoi dati dai fornitori del servizio (es., con l'E2EE, che rende i tuoi dati illeggibili dal server).
- <span class="pg-blue">:material-eye-outline: Sorveglianza di massa</span> - Protezione dalle agenzie governative, organizzazioni, siti web e servizi che cooperano per tracciare le tue attività.
- <span class="pg-brown">:material-account-cash: Capitalismo di sorveglianza</span> - Protezione dalle grandi reti pubblicitarie, come Google e Facebook, nonché da una miriade di altri raccoglitori di dati di terze parti.
- <span class="pg-green">:material-account-search: Esposizione pubblica</span> - Limitazione delle informazioni accessibili online su di te, ai motori di ricerca o al pubblico generale.
- <span class="pg-blue-gray">:material-close-outline: Censura</span> - Prevenzione dell'accesso censurato a informazioni, o della tua censura, comunicando online.

Alcune di queste minacce potrebbero essere per te più importanti di altre, a seconda delle tue preoccupazioni specifiche. Ad esempio, uno sviluppatore di software con accesso a dati preziosi o critici potrebbe essere principalmente preoccupato degli <span class="pg-red">:material-target-account: Attacchi Mirati</span>, pur volendo proteggere i propri dati personali dalla raccolta, da parte dei programmi di <span class="pg-blue">:material-eye-outline: Sorveglianza di Massa</span>. Similmente, in molto potrebbero essere principalmente preoccupati dall'<span class="pg-green">:material-account-search: Esposizione Pubblica</span> dei propri dati personali, pur rimanendo attendi ai problemi di sicurezza, come gli <span class="pg-orange">:material-bug-outline: Attacchi Passivi</span>, come i malware che colpiscono i loro dispositivi.

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

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Inoltre, dovresti assicurarti che la tua unità sia crittografata e che il sistema operativo utilizzi un TPM o Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) od [Element](https://developers.google.com/android/security/android-ready-se), per limitare la frequenza dei tentativi di inserire la frase segreta crittografica. Dovresti evitare di condividere il tuo computer con persone di cui non ti fidi, poiché gran parte dei sistemi operativi per desktop non crittografa i dati separatamente, per ogni utente.

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

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Spesso, i governi, giustificano i programmi di sorveglianza di massa come mezzi necessari per combattere il terrorismo e prevenire il crimine. Tuttavia, violando i diritti umani, sono spesso utilizzati per colpire in modo sproporzionato gruppi di minoranza e dissidenti politici, tra gli altri.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

Di fronte alle [divulgazioni di Edward Snowden dei programmi governativi come [PRISM](https://it.wikipedia.org/wiki/PRISM_(programma_di_sorveglianza)) e [Upstream](https://en.wikipedia.org/wiki/Upstream_collection)]; inoltre, i funzionari dell'intelligence hanno ammesso che l'NSA ha raccolto segretamente per anni i registri su virtualmente ogni chiamata telefonica statunitense: chi chiama chi, quando e quanto durano. Questo tipo di informazioni, accumulate dall'NSA giorno dopo giorno, possono rivelare dettagli incredibilmente sensibili sulle vite delle persone e le associazioni, come se hanno chiamato un prete, una struttura preposta all'aborto, un consulente per le dipendenze o una linea diretta anti-suicidi.

</div>

Nonostante la crescente sorveglianza di massa negli Stati Uniti, il governo ha riscontrato che i programmi di sorveglianza di massa come la Sezione 215 hanno avuto "poco valore univoco", per quanto riguarda l'arresto di crimini reali o di complotti terroristici, con sforzi che, in gran parte, duplicano i programmi di sorveglianza mirata del FBI.[^2]

Online è possibile essere rintracciati con svariati metodi:

- Il tuo indirizzo IP
- I cookie del browser
- I dati che invii ai siti web
- L'impronta digitale del tuo browser o dispositivo
- Correlazione del metodo di pagamento

\[Questo elenco non è completo].

Se sei preoccupato per i programmi di sorveglianza di massa, puoi utilizzare strategie come la compartimentazione delle tue identità online, confonderti con gli altri utenti, o, quando possibile, semplicemente di evitare di fornire informazioni identificative.

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

La censura sulle piattaforme aziendali è sempre più comune, in quanto piattaforme come Twitter e Facebook cedono alle richieste del pubblico, alle pressioni di mercato e alle pressioni dalle agenzie governative. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

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
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. Inoltre, dovresti utilizzare altre tecniche di mitigazione.
[^5]: Nazioni Unite: [*Dichiarazione Universale dei Diritti dell'Uomo*](https://www.un.org/en/about-us/universal-declaration-of-human-rights).
