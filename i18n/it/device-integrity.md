---
title: Integrità del dispositivo
icon: material/security
description: Questi strumenti sono utilizzabili per verificare che i tuoi dispositivi non siano stati compromessi.
cover: device-integrity.webp
---

Questi strumenti possono essere utilizzati per convalidare l'integrità dei tuoi dispositivi mobile e verificare la presenza di indicatori di compromissione da parte di spyware e malware come Pegasus, Predator o KingsPawn. Questa pagina affronta la **sicurezza mobile**, poiché i dispositivi mobili hanno tipicamente sistemi di sola lettura, con configurazioni ben note, quindi, rilevare modifiche dannose è più facile che con i sistemi desktop tradizionali. In futuro, potremmo espandere l'ambito di questa pagina.

<div class="admonition note" markdown>
<p class="admonition-title">Questo è un argomento avanzato</p>

Questi strumenti possono essere utili per alcuni individui. Forniscono funzionalità di cui la maggior parte delle persone non deve preoccuparsi e spesso richiedono conoscenze tecniche più approfondite per essere utilizzate in modo efficace.

</div>

È **essenziale** comprendere che la scansione del tuo dispositivo, in cerca di indicatori pubblici di compromissione, **non è sufficiente** per determinare che un dispositivo sia "pulito", e non sia stato preso di mira da uno strumento spyware in particolare. Affidarsi a questi strumenti di scansione pubblicamente disponibili può far perdere di vista i recenti sviluppi della sicurezza e dare un falso senso di sicurezza.

## Consigli Generali

La maggior parte degli exploit a livello di sistema sui moderni dispositivi mobili, in particolare le compromissioni zero-click, non sono persistenti, ovvero non rimangono o vengono eseguiti automaticamente dopo un riavvio. Per questo motivo, si consiglia di riavviare regolarmente il dispositivo. Consigliamo a tutti di riavviare i dispositivi almeno una volta alla settimana, ma se i malware non persistenti ti preoccupano particolarmente, noi e molti esperti di sicurezza consigliamo un programma di riavvio quotidiano.

Ciò significa che un aggressore dovrebbe reinfettare regolarmente il dispositivo per mantenere l'accesso, anche se non è impossibile. Inoltre, il riavvio del dispositivo non ti protegge da malware _persistente_, ma questo è meno comune sui dispositivi mobili grazie alle moderne funzioni di sicurezza come il secure/verified boot.

## Informazioni ed esonero di responsabilità post-compromissione

Se uno dei seguenti strumenti indica una potenziale compromissione da parte di spyware come Pegasus, Predator o KingsPawn, consigliamo di contattare:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us)
- Se un dispositivo aziendale o governativo è compromesso: contatta il responsabile della sicurezza della tua azienda, dipartimento o agenzia
- Forze dell'ordine locali

**Non possiamo aiutarti più di così in maniera diretta.** Siamo lieti di discutere della tua situazione o delle circostanze specifiche e di revisionare i tuoi risultati negli spazi della nostra [community](https://discuss.privacyguides.net), ma è improbabile che potremo aiutarti più di quanto è scritto su questa pagina.

Gli strumenti su questa pagina possono esclusivamente rilevare gli indicatori di compromissione, non rimuoverli. Se temi di esser stato compromesso, ti consigliamo di:

- Considerare la completa sostituzione del dispositivo
- Considerare di cambiare il tuo numero SIM/eSIM
- Non ripristinare da un backup, poiché, questo, potrebbe essere compromesso

Questi strumenti forniscono analisi basate sulle informazioni a cui possono accedere dal tuo dispositivo e sugli indicatori di compromissione accessibili pubblicamente. È importante tenere a mente due cose:

1. Gli indicatori di compromissione sono semplicemente _indicatori_. Non sono un risultato definitivo e potrebbero occasionalmente rappresentare dei **falsi positivi**. Se viene rilevato un indicatore di compromissione, significa che dovresti svolgere ulteriori ricerche sulla minaccia _potenziale_.
2. Gli indicatori di compromissione cercati da questi strumenti, sono pubblicati dalle organizzazioni di ricerca sulle minacce, ma non tutti gli indicatori sono resi disponibili al pubblico! Ciò significa che questi strumenti possono generare un **falso negativo**, se il tuo dispositivo è infettato da spyware non rilevati da alcun indicatore pubblico. Un supporto e triage forense digitale affidabile e completo, richiedono l'accesso a indicatori, ricerca e informazioni sulle minacce non pubblici.

## Strumenti di verifica esterni

Gli strumenti di verifica esterni operano sul tuo computer, scansionando il tuo dispositivo mobile, in cerca di tracce forensi che siano utili a identificare le potenziali compromissioni.

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Gli indicatori pubblici di compromissione non sono sufficienti a determinare che un dispositivo sia "pulito" e non sia stato preso di mira da un particolare strumento spyware. Affidarsi ai soli indicatori pubblici può far perdere tracce forensi recenti e dare un falso senso di sicurezza.

Un supporto e triage forense digitale affidabile e completo, richiedono l'accesso a indicatori, ricerca e informazioni sulle minacce non pubblici.

Such support is available to civil society through [Amnesty International's Security Lab](https://amnesty.org/en/tech) or [Access Now’s Digital Security Helpline](https://accessnow.org/help).

</div>

Questi strumenti possono causare dei falsi positivi. Se uno di questi strumenti rileva degli indicatori di compromissione, devi approfondire per determinare i rischi effettivi. Alcuni rapporti potrebbero essere falsi positivi basati sui siti web che hai visitato in passato, e i risultati risalenti a molti anni fa, potrebbero essere falsi positivi, o indicare compromissioni precedenti (e non più attive).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![Logo MVT](assets/img/device-integrity/mvt.webp){ align=right }

Il **Mobile Verification Toolkit** (**MVT**) è una raccolta di utility che semplifica e automatizza il processo di scansione dei dispositivi mobile alla ricerca di potenziali tracce di bersaglio o di infezione da parte di campagne spyware note. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project).

[:octicons-home-16: Homepage](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Utilizzare MVT non è sufficiente per determinare che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare.

</div>

MVT è _più_ utile per scansionare i dispositivi iOS. Android memorizza pochissime informazioni diagnostiche utili per il triage delle potenziali compromissioni e, per questo, anche le capacità di `mvt-android` sono limitate. D'altra parte, in molti casi, i backup crittografati di iTunes per iOS forniscono un sottoinsieme di file memorizzati sul dispositivo abbastanza ampio, per rilevare gli artefatti sospetti. Detto ciò, MTV fornisce comunque strumenti abbastanza utili per l'analisi sia su iOS che su Android.

Se utilizzi iOS e sei ad alto rischio, abbiamo altri tre suggerimenti per te:

1. Crea e conserva regolarmente (mensilmente) i backup di iTunes. Ciò ti consente di trovare e diagnosticare le infezioni passate con MVT, se sono scoperte delle nuove minacce in futuro.

2. Attiva spesso i registri di _sysdiagnose_ ed eseguine il backup esternamente. Questi, possono fornire dati preziosi ai futuri investigatori forensi, se necessario.

   Il procedimento per farlo varia a seconda del modello, ma puoi attivarlo sui telefoni più nuovi tenendo premuti _Accensione_ + _Volume Su_ + _Volume Giù_, finché non avverti una breve vibrazione. Dopo qualche minuto, il registro _sysdiagnose_ con data e ora, apparirà in **Impostazioni** > **Privacy e Sicurezza** > **Analisi e Miglioramenti** > **Dati Analitici**.

3. Abilita la [Modalità di Blocco](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT ti consente di eseguire scansioni/analisi più approfondite, se il tuo dispositivo è stato sottoposto a jailbreak. A meno che tu non sappia cosa stai facendo, **non eseguire il jailbreak o il root del tuo dispositivo**. Il jailbreak del tuo dispositivo lo espone a considerevoli rischi di sicurezza.

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![logo iMazing](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** fornisce uno strumento di analisi spyware gratuito per dispositivi iOS che funge da interfaccia grafica per [MVT](#mobile-verification-toolkit). Questo può essere molto più semplice da eseguire rispetto allo stesso MVT, che è uno strumento a riga di comando progettato per tecnologi e investigatori forensi.

[:octicons-home-16: Homepage](https://imazing.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-windows11: Windows](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing automatizza e ti guida interattivamente al procedimento di utilizzo di [MVT](#mobile-verification-toolkit) per scansionare il tuo dispositivo, in cerca di indicatori pubblicamente accessibili di compromissione, pubblicati da vari ricercatori delle minacce. Tutte le informazioni e gli avvisi che si applicano a MVT, si applicano anche a questo strumento, quindi, ti suggeriamo di familiarizzare con le note su MVT, nelle sezioni precedenti.

## Verifica su dispositivo

Si tratta di app installabili che controllano il tuo dispositivo e il sistema operativo, in cerca di segni di manomissione, convalidandone l'identità.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

L'utilizzo di queste app non è sufficiente per determinarre che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare.

</div>

### Auditor (Android)

<div class="admonition recommendation" markdown>

![Logo Auditor](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Logo Auditor](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** è un'applicazione che sfrutta le caratteristiche di sicurezza hardware per fornire un monitoraggio dell'integrità del dispositivo, convalidando attivamente l'identità di un dispositivo e l'integrità del suo sistema operativo. Al momento, funziona soltanto con GrapheneOS o con il sistema operativo di fabbrica per i [dispositivi supportati](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentazione}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor non è uno strumento di scansione/analisi come altri elencati su questa pagina, piuttosto, utilizza il keystore supportato dal hardware del tuo dispositivo, per consentirti di verificarne l'identità e avere la certezza che il sistema operativo stesso non sia stato manomesso o declassato, tramite l'avvio verificato. Ciò fornisce un controllo d'integrità molto robusto del tuo stesso dispositivo, ma non verifica necessariamente che le app a livello utente, eseguite sul tuo dispositivo, siano dannose.

Auditor esegue l'attestazione e il rilevamento delle intrusioni con **due** dispositivi, un **controllato** (il dispositivo da verificare) e un **controllore** (il dispositivo che esegue la verifica). Il controllore può essere qualsiasi dispositivo con Android 10+ (o un servizio web da remoto operato da [GrapheneOS](android.md#grapheneos)), mentre il controllato dev'essere, nello specifico, un [dispositivo supportato](https://attestation.app/about#device-support). Auditor opera:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore) of the _Auditor_.
- Il _controllore_ può essere un'altra istanza dell'app di Auditor o il [Servizio di Attestazione da Remoto](https://attestation.app).
- Il _controllore_ registra lo stato corrente e la configurazione del _controllato_.
- Dovesse verificarsi la manomissione del sistema operativo del _controllato_ dopo il completamento dell'associazione, il controllore sarà a conoscenza del cambiamento nello stato e nelle configurazioni del dispositivo.
- Riceverai un avviso del cambiamento.

È importante notare che il Controllore può effettivamente rilevare i cambiamenti soltanto **dopo** l'associazione iniziale, non necessariamente durante o prima, a causa del suo modello TOFU. Per assicurarti che il tuo hardware e sistema operativo siano autentici, [esegui l'attestazione locale](https://grapheneos.org/install/web#verifying-installation) immediatamente dopo l'installazione del dispositivo e prima di qualsiasi connessione a Internet.

Nessuna informazione personalmente identificabile è inviata al servizio di attestazione. Ti consigliamo di iscriverti con un profilo anonimo e di abilitare l'attestazione da remoto per il monitoraggio costante.

Se il tuo [modello di minaccia](basics/threat-modeling.md) richiede la privacy, potresti considerare l'utilizzo di [Orbot](tor.md#orbot) o di una VPN, per nascondere il tuo indirizzo IP dal servizio di attestazione.

## Scanner su dispositivo

Si tratta di app che puoi installare sul tuo dispositivo, che lo scansionano in cerca di segni di compromissione.

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

L'utilizzo di queste app non è sufficiente per determinare che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare.

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Logo Hypatia](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Logo Hypatia](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** è uno scanner di malware real-time open source per Android, realizzato dallo sviluppatore di [DivestOS](android.md#divestos). Accede a Internet per scaricare gli aggiornamenti del database delle firme, ma non carica i file o i metadati nel cloud (le scansioni vengono eseguite interamente in locale).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Informativa sulla Privacy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner)

</details>

</div>

Hypatia is particularly good at detecting common stalkerware: If you suspect you are a victim of stalkerware, you should [visit this page](https://stopstalkerware.org/information-for-survivors) for advice.

### iVerify (iOS)

<div class="admonition recommendation" markdown>

![Logo iVerify](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** è un'applicazione per iOS che esegue una scansione automatica del dispositivo per verificare le impostazioni di configurazione, il livello delle patch e altre aree di sicurezza. Inoltre, controlla il dispositivo alla ricerca di indicatori di compromissione da parte di strumenti di jailbreak o spyware come Pegasus.

[:octicons-home-16: Homepage](https://iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1466120520)

</details>

</div>

Come tutte le app per iOS, iVerify è limitata in ciò che può osservare sul tuo dispositivo, dalla Sandbox delle app di iOS. Non fornirà un'analisi robusta come quella di uno strumento di analisi dell'intero sistema come [MVT](#mobile-verification-toolkit). La sua funzione principale è rilevare se il tuo dispositivo ha subito il jailbreak, cosa in cui è efficiente, tuttavia, una minaccia ipotetica progettata _specificamente_ per superare i controlli di iVerify, potebbe riuscire nel proprio intento.

iVerify **non** è un "antivirus" e non rileverà malware non di sistema, come ad esempio, tastiere personalizzate o configurazioni di sincronizzazione Wi-Fi dannose.

Oltre a scansionare il dispositivo, inoltre, iVerify include una serie di utilità di sicurezza aggiuntive che potresti trovare utili, inclusi promemoria sul riavvio del dispositivo, notifiche di aggiornamento di iOS (spesso più rapide del sistema scaglionato di notifiche sugli aggiornamenti di Apple), alcune guide essenziali su privacy e sicurezza e uno strumento DNS over HTTPS che può connettere le richieste [DNS](dns.md) del tuo dispositivo in sicurezza, con Quad9, Cloudflare o Google.
