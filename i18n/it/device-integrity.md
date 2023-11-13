---
title: Integrità del dispositivo
icon: material/security
description: Questi strumenti sono utilizzabili per verificare che i tuoi dispositivi non siano stati compromessi.
cover: device-integrity.webp
---

Questi strumenti sono utilizzabili per convalidare l'integrità dei tuoi dispositivi mobili, e verificare la presenza di indicatori di compromissione da parte di spyware e malware, quali Pegasus, Predator o KingsPawn. Questa pagina affronta la **sicurezza mobile**, poiché i dispositivi mobili hanno tipicamente sistemi di sola lettura, con configurazioni ben note, quindi, rilevare modifiche dannose è più facile che con i sistemi desktop tradizionali. In futuro, potremmo espandere l'ambito di questa pagina.

!!! note "Questo è un argomento avanzato"

```
Questi strumenti potrebbero fornire utilità per certi individui. Forniscono funzionalità di cui gran parte delle persone non necessitano di preoccuparsi e, spesso, richiedono una conoscenza tecnica più approfondita, per l'utilizzo efficiente.
```

È **essenziale** comprendere che la scansione del tuo dispositivo, in cerca di indicatori pubblici di compromissione, **non è sufficiente** per determinare che un dispositivo sia "pulito", e non sia stato preso di mira da uno strumento spyware in particolare. L'affidamento a tali strumenti di scansione pubblicamente disponibili, può far perdere di vista gli sviluppi recenti in materia di sicurezza, dandoti un falso senso di sicurezza.

## Consigli Generali

Gran parte degli exploit di sistema sui dispositivi mobili moderni, specialmente le compromissioni senza click, non sono persistenti, a significare che non resteranno, né saranno eseguiti automaticamente, dopo un riavvio. Per questo, ti consigliamo vivamente di riavviare regolarmente il tuo dispositivo. Consigliamo a tutti di riavviare il proprio dispositivo almeno una volta a settimana, ma se i malware non persistenti ti preoccupano particolarmente, noi e molti esperti in sicurezza, consigliamo di pianificare dei riavvii quotidiani.

Ciò significa che un malintenzionato dovrebbe reinfettare regolarmente il tuo dispositivo per mantenere l'accesso, sebbene noteremo che non sia possibile. Inoltre, riavviare il tuo dispositivo non ti proteggerà dai malware **permanenti**, ma questi sono meno comuni sui dispositivi mobili, a causa di funzionalità di sicurezza moderne come l'avvio sicuro/verificato.

## Informazioni ed esonero di responsabilità post-compromissione

Se uno dei seguenti strumenti indica una potenziale compromissione da spyware, come Pegasus, Predator, o KingsPawn, ti consigliamo di contattare:

- Se ti occupi della difesa dei diritti umani, di giornalismo o fai parte di un'organizzazione della società civile: [Laboratorio sulla sicurezza di Amnesty International](https://securitylab.amnesty.org/contact-us/)
- Se un dispositivo aziendale o governativo è compromesso: contatta il responsabile della sicurezza della tua azienda, dipartimento o agenzia
- Forze dell'ordine locali

**Non possiamo aiutarti più di così in maniera diretta.** Siamo lieti di discutere della tua situazione o delle circostanze specifiche e di revisionare i tuoi risultati negli spazi della nostra [community](https://discuss.privacyguides.net), ma è improbabile che potremo aiutarti più di quanto è scritto su questa pagina.

Gli strumenti su questa pagina possono esclusivamente rilevare gli indicatori di compromissione, non rimuoverli. Se temi di esser stato compromesso, ti consigliamo di:

- Considerare la completa sostituzione del dispositivo
- Considerare di cambiare il tuo numero SIM/eSIM
- Non ripristinare da un backup, poiché, questo, potrebbe essere compromesso

Questi strumenti forniscono analisi basate sulle informazioni cui possono accedere dal tuo dispositivo, nonché sugli indicatori di compromissione pubblicamente accessibili. È importante tenere a mente due cose:

1. Gli indicatori di compromesso sono semplicemente **indicatori**. Non sono un risultato definitivo e potrebbero occasionalmente rappresentare dei **falsi positivi**. Se viene rilevato un indicatore di compromissione, significa che dovresti svolgere ulteriori ricerche sulla minaccia **potenziale**.
2. Gli indicatori di compromissione cercati da questi strumenti, sono pubblicati dalle organizzazioni di ricerca sulle minacce, ma non tutti sono resi disponibili al pubblico! Ciò significa che questi strumenti possono generare un **falso negativo**, se il tuo dispositivo è infettato da spyware non rilevati da alcun indicatore pubblico. Un supporto e triage forense digitale affidabile e completo, richiedono l'accesso a indicatori, ricerca e informazioni sulle minacce non pubblici.

## Strumenti di verifica esterni

Gli strumenti di verifica esterni operano sul tuo computer, scansionando il tuo dispositivo mobile, in cerca di tracce forensi che siano utili a identificare le potenziali compromissioni.

!!! danger "Attenzione"

```
Gli indicatori pubblici di compromissione non sono sufficienti per determinare che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare. L'affidamento ai soli indicatori pubblici, può non tenere conto delle tracce forensi recenti e dare un falso senso di sicurezza.

Un supporto e triage forense digitale affidabile e completo richiede l'accesso a indicatori, ricerca e informazioni sulle minacce non pubblici.

Tale supporto è disponibile alla società civile tramite il [Laboratorio sulla sicurezza di Amnesty International](https://www.amnesty.org/en/tech) o il [Telesoccorso sulla sicurezza digitale di Access Now](https://www.accessnow.org/help/).
```

Questi strumenti possono causare dei falsi positivi. Se uno di questi strumenti rileva degli indicatori di compromissione, devi approfondire per determinare i rischi effettivi. Alcuni rapporti potrebberro essere falsi positivi basati sui siti web che hai visitato in passato, e i risultati risalenti a molti anni fa, potrebbero essere falsi positivi, o indicare compromissioni precedenti (e non più attive).

### Mobile Verification Toolkit

!!! recommendation "consiglio"

```
![Logo di MVT](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) è una raccolta di utilità che semplificano e automatizzano il processo di scansione dei dispositivi mobili, alla ricerca di potenziali tracce di violazione o infezione, da campagne note di spyware. MVT è stata sviluppata da Amnesty International e rilasciata nel 2021, nel contesto del [Progetto Pegasus](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Codice Sorgente" }

??? downloads

    - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
    - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)
```

!!! warning "Attenzione"

```
Utilizzare MVT non è sufficiente per determinare che un dispositivo sia "pulito" e non preso di mira da uno strumento spyware in particolare.
```

MVT è _più_ utile per scansionare i dispositivi iOS. Android memorizza pochissime informazioni diagnostiche utili per il triage delle potenziali compromissioni e, per questo, anche le capacità di `mvt-android` sono limitate. D'altra parte, in molti casi, i backup crittografati di iTunes per iOS forniscono un sottoinsieme di file memorizzati sul dispositivo abbastanza ampio, per rilevare gli artefatti sospetti. Detto ciò, MTV fornisce comunque strumenti abbastanza utili per l'analisi sia su iOS che su Android.

Se utilizzi iOS e sei ad alto rischio, abbiamo altri tre suggerimenti per te:

1. Crea e conserva regolarmente (mensilmente) i backup di iTunes. Ciò ti consente di trovare e diagnosticare le infezioni passate con MVT, se sono scoperte delle nuove minacce in futuro.

2. Attiva spesso i registri di _sysdiagnose_ ed eseguine il backup esternamente. Questi, possono fornire dati preziosi ai futuri investigatori forensi, se necessario.

   Il procedimento per farlo varia a seconda del modello, ma puoi attivarlo sui telefoni più nuovi tenendo premuti _Accensione_ + _Volume Su_ + _Volume Giù_, finché non avverti una breve vibrazione. Dopo qualche minuto, il registro _sysdiagnose_ con data e ora, apparirà in **Impostazioni** > **Privacy e Sicurezza** > **Analisi e Miglioramenti** > **Dati Analitici**.

3. Abilita la [Modalità di Blocco](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT ti consente di eseguire scansioni/analisi più approfondite, se il tuo dispositivo è stato sottoposto a jailbreak. A meno che tu non sappia cosa stai facendo, **non eseguire il jailbreak o il root del tuo dispositivo**. Il jailbreak del tuo dispositivo lo espone a considerevoli rischi di sicurrezza.

### iMazing (iOS)

!!! recommendation "consiglio"

```
![Logo di iMazing](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** fornisce uno strumento gratuito di analisi degli spyware per i dispositivi iOS, che agisce da GUI-wrapper per [MVT](#mobile-verification-toolkit).
Può essere molto più facile da eseguire rispetto allo stesso MVT, uno strumento a riga di comando progettato per esperti di tecnologia e investigatori forensi.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentazione}

??? downloads

    - [:simple-windows11: Windows](https://imazing.com/download)
    - [:simple-apple: macOS](https://imazing.com/download)
```

iMazing automatizza e ti guida interattivamente al procedimento di utilizzo di [MVT](#mobile-verification-toolkit) per scansionare il tuo dispositivo, in cerca di indicatori pubblicamente accessibili di compromissione, pubblicati da vari ricercatori delle minacce. Tutte le informazioni e gli avvisi che si applicano a MVT, si applicano anche a questo strumento, quindi, ti suggeriamo di familiarizzare con le note su MVT, nelle sezioni precedenti.

## Verifica su dispositivo

These are apps you can install which check your device and operating system for signs of tampering, and validate the identity of your device.

!!! warning "Attenzione"

```
L'uso di queste applicazioni non è sufficiente a determinare che un dispositivo sia "pulito" e non sia stato preso di mira da un particolare strumento spyware.
```

### Auditor (Android)

!!! recommendation "consiglio"

```
![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** è un app che sfrutta le caratteristiche di sicurezza dell'hardware per fornire un monitoraggio dell'integrità del dispositivo, convalidando attivatemnte l'identità di un dispositivo e l'integrità del suo sistema operativo. Attualmente funziona solo con GrapheneOS o con il sistema operativo stock per i [dispositivi supportati](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentazione}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuisci }

??? downloads

    - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
    - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
    - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)
```

Auditor is not a scanning/analysis tool like some other tools on this page, rather it uses your device's hardware-backed keystore to allow you to verify the identity of your device and gain assurance that the operating system itself hasn't been tampered with or downgraded via verified boot. This provides a very robust integrity check of your device itself, but doesn't necessarily check whether the user-level apps running on your device are malicious.

Auditor performs attestation and intrusion detection with **two** devices, an _auditee_ (the device being verified) and an _auditor_ (the device performing the verification). The auditor can be any Android 10+ device (or a remote web service operated by [GrapheneOS](android.md#grapheneos)), while the auditee must be a specifically [supported device](https://attestation.app/about#device-support). Auditor works by:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/) of the _Auditor_.
- The _auditor_ can either be another instance of the Auditor app or the [Remote Attestation Service](https://attestation.app).
- The _auditor_ records the current state and configuration of the _auditee_.
- Should tampering with the operating system of the _auditee_ happen after the pairing is complete, the auditor will be aware of the change in the device state and configurations.
- You will be alerted to the change.

It is important to note that Auditor can only effectively detect changes **after** the initial pairing, not necessarily during or before due to its TOFU model. To make sure that your hardware and operating system is genuine, [perform local attestation](https://grapheneos.org/install/web#verifying-installation) immediately after the device has been installed and prior to any internet connection.

No personally identifiable information is submitted to the attestation service. We recommend that you sign up with an anonymous account and enable remote attestation for continuous monitoring.

If your [threat model](basics/threat-modeling.md) requires privacy, you could consider using [Orbot](tor.md#orbot) or a VPN to hide your IP address from the attestation service.

## Scanner On-Device

These are apps you can install on your device which scan your device for signs of compromise.

!!! warning "Attenzione"

```
L'uso di queste applicazioni non è sufficiente a determinare che un dispositivo sia "pulito" e non sia stato preso di mira da un particolare strumento spyware.
```

### Hypatia (Android)

!!! recommendation "consiglio"

```
![Logo di Hypatia](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Logo di Hypatia](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** è uno scanner di malware in tempo reale open source per Android, realizzato dallo sviluppatore di [DivestOS](android.md#divestos). Accede a Internet per scaricare gli aggiornamenti del database delle firme, ma non carica i tuoi file o i tuoi metadati sul cloud (le scansioni vengono eseguite interamente in locale).

[:octicons-home-16: Pagina Principale](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Politica sulla Privacy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuisci }

??? downloads "Scarica"

    - [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)
```

Hypatia è particolarmente abile nel rilevare gli stalkerware più comuni: se sospetti di essere vittima di stalkerware, dovresti [visitare questa pagina](https://stopstalkerware.org/it/informazioni-per-le-vittime/) per consigli.

### iVerify (iOS)

!!! recommendation "consiglio"

```
![Logo di iVerify](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** è un'applicazione per iOS che esegue una scansione automatica del tuo dispositivo per verificare le impostazioni di configurazione, il livello delle patch e altre aree di sicurezza. Controlla inoltre che il tuo dispositivo non presenti indicatori di compromissione da parte di strumenti di jailbreak o spyware come Pegasus.

[:octicons-home-16: Pagina Principale](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentazione}

??? downloads "Scarica"

    - [:simple-appstore: App Store](https://apps.apple.com/it/app/iverify-secure-your-phone/id1466120520)
```

Come tutte le app iOS, iVerify è limitata a ciò che può osservare sul tuo dispositivo dall'interno della Sandbox delle app iOS. Non fornirà un'analisi robusta come uno strumento di analisi del sistema completo come [MVT](#mobile-verification-toolkit). La sua funzione principale è quella di rilevare se al tuo dispositivo è stato effettuato il jailbroken, cosa che è efficace nell'individuare, tuttavia un'ipotetica minaccia progettata _specificamente_ per aggirare i controlli di iVerify probabilmente riuscirebbe a farlo.

iVerify **non** è uno strumento "antivirus" e non è in grado di rilevare malware non a livello di sistema, come ad esempio tastiere personalizzate o configurazioni Wi-Fi Sync dannose.

Oltre alla scansione del dispositivo, iVerify include anche una serie di strumenti di sicurezza aggiuntivi che potrebbero risultarti utili, tra cui i promemoria per il riavvio del dispositivo, notifiche di aggiornamento di iOS (spesso più rapide rispetto al rilascio scaglionato degli aggiornamenti di Apple), alcune guide di base sulla privacy e sulla sicurezza e uno strumento DNS su HTTPS in grado di connettere le query [DNS](dns.md) del tuo dispositivo in modo sicuro a Quad9, Cloudflare o Google.
