---
title: Intégrité de l'appareil
icon: material/security
description: Ces outils peuvent être utilisés pour vérifier que vos appareils ne sont pas compromis.
cover: device-integrity.webp
---

Ces outils peuvent être utilisés pour valider l'intégrité de vos appareils mobiles et vérifier s'ils présentent des indicateurs de compromission par des logiciels espions et malveillants tels que Pegasus, Predator ou KingsPawn. Cette page se concentre sur la **sécurité mobile**, car les appareils mobiles ont généralement des systèmes en lecture seule avec des configurations bien connues, de sorte que la détection de modifications malveillantes est plus facile que sur les systèmes de bureau traditionnels. Nous pourrions élargir la portée de cette page dans le futur.

!!! note "Ceci est un sujet avancé"

```
Ces outils peuvent être utiles à certaines personnes. Ils fournissent des fonctionnalités dont la plupart des gens n'ont pas besoin de s'inquiéter, et nécessitent souvent des connaissances techniques plus approfondies pour être utilisés efficacement.
```

Il est **critique** de comprendre que l'analyse de votre appareil à la recherche d'indicateurs publics de compromission n'est **pas suffisante** pour déterminer qu'un appareil est "propre" et qu'il n'est pas la cible d'un logiciel espion particulier. En vous fiant à ces outils d'analyse accessibles au public, vous risquez de passer à côté d'évolutions récentes en matière de sécurité et de vous donner un faux sentiment de sécurité.

## Conseil général

La majorité des exploits au niveau du système sur les appareils mobiles modernes - en particulier les compromissions en zéro clic - sont non persistants, ce qui signifie qu'ils ne resteront pas ou ne s'exécuteront pas automatiquement après un redémarrage. C'est pourquoi nous vous recommandons vivement de redémarrer votre appareil régulièrement. Nous recommandons à chacun de redémarrer son appareil au moins une fois par semaine, mais si les logiciels malveillants non persistants vous préoccupent particulièrement, nous recommandons, comme de nombreux experts en sécurité, de procéder à un redémarrage quotidien.

Cela signifie qu'un attaquant devrait régulièrement réinfecter votre appareil pour en conserver l'accès, bien que cela ne soit pas impossible. Le redémarrage de votre appareil ne vous protège pas non plus contre les logiciels malveillants _persistants_, mais cela est moins fréquent sur les appareils mobiles en raison des fonctions de sécurité modernes telles que le démarrage sécurisé/vérifié.

## Information post-compromission et avertissement

Si l'un des outils suivants indique une compromission potentielle par un logiciel espion tel que Pegasus, Predator ou KingsPawn, nous vous conseillons de contacter :

- Si vous êtes défenseur des droits de l'homme, journaliste ou membre d'une organisation de la société civile : le [laboratoire de sécurité d'Amnesty International](https://securitylab.amnesty.org/contact-us/)
- Si un appareil professionnel ou gouvernemental est compromis : contactez le responsable de la sécurité de votre entreprise, de votre département ou de votre agence
- Les forces de l'ordre locales

**Nous ne sommes pas en mesure de vous aider directement au-delà de ces conseils.** Nous sommes disposés à discuter de votre situation ou de vos circonstances particulières et à examiner vos résultats dans nos espaces [communautaires](https://discuss.privacyguides.net), mais il est peu probable que nous puissions vous aider au-delà de ce qui est écrit sur cette page.

Les outils présentés sur cette page sont uniquement capables de détecter les indicateurs de compromission, et non de les supprimer. Si vous craignez d'avoir été compromis, nous vous conseillons de procéder comme suit :

- Envisager le remplacement complet de l'appareil
- Envisagez de changer de numéro SIM/eSIM
- Ne pas restaurer à partir d'une sauvegarde, car cette dernière peut être compromise

Ces outils fournissent une analyse basée sur les informations auxquelles ils ont accès à partir de votre appareil et sur les indicateurs de compromission accessibles au public. Il est important de garder à l'esprit deux choses :

1. Les indicateurs de compromissions ne sont que cela : des _indicateurs_. Ils ne constituent pas un résultat définitif et peuvent parfois être des **faux positifs**. Si un indicateur de compromission est détecté, cela signifie que vous devez effectuer des recherches supplémentaires sur la menace _potentielle_.
2. Les indicateurs de compromission recherchés par ces outils sont publiés par des organismes de recherche sur les menaces, mais tous les indicateurs ne sont pas mis à la disposition du public ! Cela signifie que ces outils peuvent présenter un **faux négatif**, si votre appareil est infecté par un logiciel espion qui n'est détecté par aucun des indicateurs publics. Une prise en charge et un triage fiables et complets en matière de criminalistique numérique nécessitent l'accès à des indicateurs non publics, à des recherches et à des renseignements sur les menaces.

## Outils de vérification externes

Les outils de vérification externes s'exécutent sur votre ordinateur et analysent votre appareil mobile à la recherche de traces criminalistiques qui permettent d'identifier les compromissions potentielles.

!!! danger "Danger"

```
Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).
```

These tools can trigger false-positives. If any of these tools finds indicators of compromise, you need to dig deeper to determine your actual risk. Some reports may be false positives based on websites you've visited in the past, and findings which are many years old are likely either false-positives or indicate previous (and no longer active) compromise.

### Mobile Verification Toolkit

!!! recommendation

```
![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) is a collection of utilities which simplifies and automates the process of scanning mobile devices for potential traces of targeting or infection by known spyware campaigns. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

??? downloads

    - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
    - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)
```

!!! warning "Avertissement"

```
Using MVT is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

MVT is _most_ useful for scanning iOS devices. Android stores very little diagnostic information useful to triage potential compromises, and because of this `mvt-android` capabilities are limited as well. On the other hand, encrypted iOS iTunes backups provide a large enough subset of files stored on the device to detect suspicious artifacts in many cases. This being said, MVT does still provide fairly useful tools for both iOS and Android analysis.

If you use iOS and are at high-risk, we have three additional suggestions for you:

1. Create and keep regular (monthly) iTunes backups. This allows you to find and diagnose past infections later with MVT, if new threats are discovered in the future.

2. Trigger _sysdiagnose_ logs often and back them up externally. These logs can provide invaluable data to future forensic investigators if need be.

   The process to do so varies by model, but you can trigger it on newer phones by holding down _Power_ + _Volume Up_ + _Volume Down_ until you feel a brief vibration. After a few minutes, the timestamped _sysdiagnose_ log will appear in **Settings** > **Privacy & Security** > **Analytics & Improvements** > **Analytics Data**.

3. Enable [Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT allows you to perform deeper scans/analysis if your device is jailbroken. Unless you know what you are doing, **do not jailbreak or root your device.** Jailbreaking your device exposes it to considerable security risks.

### iMazing (iOS)

!!! recommendation

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

## On-Device Verification

These are apps you can install which check your device and operating system for signs of tampering, and validate the identity of your device.

!!! warning "Avertissement"

```
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

### Auditor (Android)

!!! recommendation

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

## On-Device Scanners

These are apps you can install on your device which scan your device for signs of compromise.

!!! warning "Avertissement"

```
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

### Hypatia (Android)

!!! recommendation

```
![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

??? downloads

    - [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)
```

Hypatia is particularly good at detecting common stalkerware: If you suspect you are a victim of stalkerware, you should [visit this page](https://stopstalkerware.org/information-for-survivors/) for advice.

### iVerify (iOS)

!!! recommendation

```
![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** is an iOS app which automatically scans your device to check configuration settings, patch level, and other areas of security. It also checks your device for indicators of compromise by jailbreak tools or spyware such as Pegasus.

[:octicons-home-16: Homepage](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

??? downloads

    - [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)
```

Like all iOS apps, iVerify is restricted to what it can observe about your device from within the iOS App Sandbox. It will not provide nearly as robust analysis as a full-system analysis tool like [MVT](#mobile-verification-toolkit). Its primary function is to detect whether your device is jailbroken, which it is effective at, however a hypothetical threat which is _specifically_ designed to bypass iVerify's checks would likely succeed at doing so.

iVerify is **not** an "antivirus" tool, and will not detect non-system-level malware such as malicious custom keyboards or malicious Wi-Fi Sync configurations, for example.

In addition to device scanning, iVerify also includes a number of additional security utilities which you may find useful, including device reboot reminders, iOS update notifications (which are often faster than Apple's staggered update notification rollout), some basic privacy and security guides, and a DNS over HTTPS tool which can connect your device's [DNS](dns.md) queries securely to Quad9, Cloudflare, or Google.
