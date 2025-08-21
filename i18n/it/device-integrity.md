---
title: "Integrità del dispositivo"
icon: material/security
description: Questi strumenti sono utilizzabili per verificare che i tuoi dispositivi non siano stati compromessi.
cover: device-integrity.webp
robots: nofollow, max-snippet:-1, max-image-preview:large
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
 - If a business or government device is compromised: the appropriate security liaison at your enterprise, department, or agency
 - Forze dell'ordine locali

**Non possiamo aiutarti più di così in maniera diretta.** Siamo lieti di discutere della tua situazione o delle circostanze specifiche e di revisionare i tuoi risultati negli spazi della nostra [community](https://discuss.privacyguides.net), ma è improbabile che potremo aiutarti più di quanto è scritto su questa pagina.

Gli strumenti su questa pagina possono esclusivamente rilevare gli indicatori di compromissione, non rimuoverli. Se temi di esser stato compromesso, ti consigliamo di:

 - Considerare la completa sostituzione del dispositivo
 - Considerare di cambiare il tuo numero SIM/eSIM
 - Non ripristinare da un backup, poiché, questo, potrebbe essere compromesso

Questi strumenti forniscono analisi basate sulle informazioni a cui possono accedere dal tuo dispositivo e sugli indicatori di compromissione accessibili pubblicamente. È importante tenere a mente due cose:

1. Gli indicatori di compromissione sono semplicemente _indicatori_. Non sono un risultato definitivo e potrebbero occasionalmente rappresentare dei **falsi positivi**. Se viene rilevato un indicatore di compromissione, significa che dovresti svolgere ulteriori ricerche sulla minaccia _potenziale_.
2. Gli indicatori di compromissione cercati da questi strumenti, sono pubblicati dalle organizzazioni di ricerca sulle minacce, ma non tutti gli indicatori sono resi disponibili al pubblico! Ciò significa che questi strumenti possono generare un **falso negativo**, se il tuo dispositivo è infettato da spyware non rilevati da alcun indicatore pubblico. Reliable and comprehensive digital forensic support and triage require access to non-public indicators, research, and threat intelligence.

## Strumenti di verifica esterni

<small>Protects against the following threat(s):</small>

 - [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

External verification tools run on your computer and scan your mobile device for forensic traces, which are helpful to identify potential compromise.

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Gli indicatori pubblici di compromissione non sono sufficienti a determinare che un dispositivo sia "pulito" e non sia stato preso di mira da un particolare strumento spyware. Affidarsi ai soli indicatori pubblici può far perdere tracce forensi recenti e dare un falso senso di sicurezza.

Reliable and comprehensive digital forensic support and triage require access to non-public indicators, research, and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://amnesty.org/en/tech) or [Access Now’s Digital Security Helpline](https://accessnow.org/help).

</div>

Questi strumenti possono causare dei falsi positivi. Se uno di questi strumenti rileva degli indicatori di compromissione, devi approfondire per determinare i rischi effettivi. Alcuni rapporti potrebbero essere falsi positivi basati sui siti web che hai visitato in passato, e i risultati risalenti a molti anni fa, potrebbero essere falsi positivi, o indicare compromissioni precedenti (e non più attive).

### Mobile Verification Toolkit

<div class="admonition recommendation" markdown>

![MVT logo](assets/img/device-integrity/mvt.webp#only-light){ align=right }
![MVT logo](assets/img/device-integrity/mvt-dark.png#only-dark){ align=right }

Il **Mobile Verification Toolkit** (**MVT**) è una raccolta di utility che semplifica e automatizza il processo di scansione dei dispositivi mobile alla ricerca di potenziali tracce di bersaglio o di infezione da parte di campagne spyware note. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project).

[:octicons-home-16: Homepage](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

 - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
 - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Utilizzare MVT non è sufficiente per determinare che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare.

</div>

MVT è _più_ utile per scansionare i dispositivi iOS. Android stores very little diagnostic information useful to triage potential compromises, and because of this, `mvt-android` capabilities are limited as well. D'altra parte, in molti casi, i backup crittografati di iTunes per iOS forniscono un sottoinsieme di file memorizzati sul dispositivo abbastanza ampio, per rilevare gli artefatti sospetti. Detto ciò, MTV fornisce comunque strumenti abbastanza utili per l'analisi sia su iOS che su Android.

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
<summary>Scarica</summary>

 - [:fontawesome-brands-windows: Windows](https://imazing.com/download)
 - [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing automatizza e ti guida interattivamente al procedimento di utilizzo di [MVT](#mobile-verification-toolkit) per scansionare il tuo dispositivo, in cerca di indicatori pubblicamente accessibili di compromissione, pubblicati da vari ricercatori delle minacce. All the information and warnings which apply to MVT apply to this tool as well, so we suggest you also familiarize yourself with the notes on MVT in the sections above.

## Verifica su dispositivo

<small>Protects against the following threat(s):</small>

 - [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
 - [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy){ .pg-orange }

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
<summary>Scarica</summary>

 - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
 - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
 - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor is not a scanning/analysis tool like some other tools on this page. Rather, it uses your device's hardware-backed keystore to allow you to verify the identity of your device and gain assurance that the operating system itself hasn't been tampered with or downgraded via verified boot. Ciò fornisce un controllo d'integrità molto robusto del tuo stesso dispositivo, ma non verifica necessariamente che le app a livello utente, eseguite sul tuo dispositivo, siano dannose.

Auditor esegue l'attestazione e il rilevamento delle intrusioni con **due** dispositivi, un **controllato** (il dispositivo da verificare) e un **controllore** (il dispositivo che esegue la verifica). The auditor can be any Android 10+ device (or a remote web service operated by [GrapheneOS](android/distributions.md#grapheneos)), while the auditee must be a specifically [supported device](https://attestation.app/about#device-support). Auditor opera:

 - Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore) of the _Auditor_.
 - Il _controllore_ può essere un'altra istanza dell'app di Auditor o il [Servizio di Attestazione da Remoto](https://attestation.app).
 - Il _controllore_ registra lo stato corrente e la configurazione del _controllato_.
 - Dovesse verificarsi la manomissione del sistema operativo del _controllato_ dopo il completamento dell'associazione, il controllore sarà a conoscenza del cambiamento nello stato e nelle configurazioni del dispositivo.
 - Riceverai un avviso del cambiamento.

È importante notare che il Controllore può effettivamente rilevare i cambiamenti soltanto **dopo** l'associazione iniziale, non necessariamente durante o prima, a causa del suo modello TOFU. Per assicurarti che il tuo hardware e sistema operativo siano autentici, [esegui l'attestazione locale](https://grapheneos.org/install/web#verifying-installation) immediatamente dopo l'installazione del dispositivo e prima di qualsiasi connessione a Internet.

Nessuna informazione personalmente identificabile è inviata al servizio di attestazione. Ti consigliamo di iscriverti con un profilo anonimo e di abilitare l'attestazione da remoto per il monitoraggio costante.

If your [threat model](basics/threat-modeling.md) requires hiding your IP address from the attestation service, you could consider using [Orbot](alternative-networks.md#orbot) or a [VPN](vpn.md).
