---
title: Integrità del Dispositivo
icon: material/security
description: Questi strumenti possono essere utilizzati per verificare che i tuoi dispositivi non siano stati compromessi.
cover: device-integrity.webp
---

Questi strumenti possono essere utilizzati per convalidare l'integrità dei tuoi dispositivi mobile e verificare la presenza di indicatori di compromissione da parte di spyware e malware come Pegasus, Predator o KingsPawn. Questa pagina si concentra sulla **sicurezza mobile**, poiché i dispositivi mobile hanno in genere sistemi di sola lettura con configurazioni ben note, quindi il rilevamento di modifiche dannose è più facile che sui sistemi desktop tradizionali. Potremmo espandere il focus di questa pagina in futuro.

!!! note "Questo è un argomento avanzato"

```
Questi strumenti possono essere utili per alcuni individui. Forniscono funzionalità di cui la maggior parte delle persone non deve preoccuparsi e spesso richiedono conoscenze tecniche più approfondite per essere utilizzate in modo efficace.
```

È **critico** capire che la scansione del tuo dispositivo alla ricerca di indicatori pubblici di compromissione non è **sufficiente** per determinare che un dispositivo è "pulito" e non è stato preso di mira da un particolare strumento spyware. Affidarsi a questi strumenti di scansione pubblicamente disponibili può far perdere di vista i recenti sviluppi della sicurezza e darti un falso senso di sicurezza.

## Consigli Generali

La maggior parte degli exploit a livello di sistema sui moderni dispositivi mobili, in particolare le compromissioni zero-click, non sono persistenti, ovvero non rimangono o non vengono eseguiti automaticamente dopo un riavvio. Per questo motivo, ti consigliamo di riavviare regolarmente il tuo dispositivo. Consigliamo a tutti di riavviare i dispositivi almeno una volta alla settimana, ma se i malware non persistenti ti preoccupano particolarmente, noi e molti esperti di sicurezza consigliamo un programma di riavvio quotidiano.

Ciò significa che un aggressore dovrebbe reinfettare regolarmente il tuo dispositivo per mantenere l'accesso, anche se sappiamo che non è impossibile. Inoltre, il riavvio del tuo dispositivo non ti protegge da malware _persistenti_, ma questo è meno comune sui dispositivi mobile grazie alle moderne funzioni di sicurezza come l'avvio sicuro/verificato.

## Post-Compromise Information & Disclaimer

If any of the following tools indicate a potential compromise by spyware such as Pegasus, Predator, or KingsPawn, we advise that you contact:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us/)
- If a business or government device is compromised: Contact the appropriate security liason at your enterprise, department, or agency
- Local law enforcement

**We are unable to help you directly beyond this.** We are happy to discuss your specific situation or circumstances and review your results in our [community](https://discuss.privacyguides.net) spaces, but it is unlikely we can assist you beyond what is written on this page.

The tools on this page are only capable of detecting indicators of compromise, not removing them. If you are concerned about having been compromised, we advise that you:

- Consider replacing the device completely
- Consider changing your SIM/eSIM number
- Not restore from a backup, because that backup may be compromised

These tools provide analysis based on the information they have the ability to access from your device, and publicly-accessible indicators of compromise. It is important to keep in mind two things:

1. Indicators of compromise are just that: _indicators_. They are not a definitive finding, and may occasionally be **false positives**. If an indicator of compromise is detected, it means you should do additional research into the _potential_ threat.
2. The indicators of compromise these tools look for are published by threat research organizations, but not all indicators are made available to the public! This means that these tools can present a **false negative**, if your device is infected with spyware which is not detected by any of the public indicators. Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

## Strumenti di verifica esterni

Gli strumenti di verifica esterni vengono eseguiti sul tuo computer e scansionano il tuo dispositivo mobile alla ricerca di tracce forensi utili per identificare potenziali compromissioni.

!!! danger "Attenzione"

```
Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).
```

These tools can trigger false-positives. If any of these tools finds indicators of compromise, you need to dig deeper to determine your actual risk. Some reports may be false positives based on websites you've visited in the past, and findings which are many years old are likely either false-positives or indicate previous (and no longer active) compromise.

### Mobile Verification Toolkit

!!! recommendation "consiglio"

```
![Logo di MVT](assets/img/device-integrity/mvt.webp){ align=right }

Il **Mobile Verification Toolkit** (**MVT**) è una raccolta di strumenti che semplifica e automatizza il processo di scansione dei dispositivi mobile alla ricerca di potenziali tracce di bersaglio o infezione da parte di campagne spyware note. MVT è stato sviluppato da Amnesty International e rilasciato nel 2021 nell'ambito del [Progetto Pegasus](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Pagina Principale](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Codice Sorgente" }

??? downloads "Scarica"

    - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
    - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)
```

!!! warning "Attenzione"

```
L'utilizzo di MVT non è sufficiente per determinare se un dispositivo sia "pulito" e non sia stato preso di mira da un particolare strumento spyware.
```

MVT è _più_ utile per la scansione dei dispositivi iOS. Android stores very little diagnostic information useful to triage potential compromises, and because of this `mvt-android` capabilities are limited as well. On the other hand, encrypted iOS iTunes backups provide a large enough subset of files stored on the device to detect suspicious artifacts in many cases. This being said, MVT does still provide fairly useful tools for both iOS and Android analysis.

If you use iOS and are at high-risk, we have three additional suggestions for you:

1. Create and keep regular (monthly) iTunes backups. This allows you to find and diagnose past infections later with MVT, if new threats are discovered in the future.

2. Trigger _sysdiagnose_ logs often and back them up externally. These logs can provide invaluable data to future forensic investigators if need be.

   The process to do so varies by model, but you can trigger it on newer phones by holding down _Power_ + _Volume Up_ + _Volume Down_ until you feel a brief vibration. After a few minutes, the timestamped _sysdiagnose_ log will appear in **Settings** > **Privacy & Security** > **Analytics & Improvements** > **Analytics Data**.

3. Enable [Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT allows you to perform deeper scans/analysis if your device is jailbroken. Unless you know what you are doing, **do not jailbreak or root your device.** Jailbreaking your device exposes it to considerable security risks.

### iMazing (iOS)

!!! recommendation "consiglio"

```
![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** provides a free spyware analyzer tool for iOS devices which acts as a GUI-wrapper for [MVT](#mobile-verification-toolkit). This can be much easier to run compared to MVT itself, which is a command-line tool designed for technologists and forensic investigators.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

??? downloads

    - [:simple-windows11: Windows](https://imazing.com/download)
    - [:simple-apple: macOS](https://imazing.com/download)
```

iMazing automates and interactively guides you through the process of using [MVT](#mobile-verification-toolkit) to scan your device for publicly-accessible indicators of compromise published by various threat researchers. All of the information and warnings which apply to MVT apply to this tool as well, so we suggest you also familiarize yourself with the notes on MVT in the sections above.

## Verifica On-Device

These are apps you can install which check your device and operating system for signs of tampering, and validate the identity of your device.

!!! warning "Attenzione"

```
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

### Auditor (Android)

!!! recommendation "consiglio"

```
![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }

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
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
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
