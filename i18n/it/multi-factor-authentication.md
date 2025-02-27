---
title: "Multifactor Authentication"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multifactor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-target-account: Attacchi Mirati](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Chiavi Hardware</p>

[Hardware security key recommendations](security-keys.md) have been moved to their own category.

</div>

**Multifactor Authentication Apps** implement a security standard adopted by the Internet Engineering Task Force (IETF) called **Time-based One-time Passwords**, or **TOTP**. Tramite questo metodo i siti web condividono un codice segreto con te, utilizzato dalla tua app d'autenticazione per generare un codice (solitamente) a sei cifre, a seconda dell'ora corrente, che inserisci accedendo al sito web, per verificarti. Typically, these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Anche se un hacker ottiene il codice a sei cifre, non gli sarà possibile decrittografarlo per ottenere quello originale, o per altrimenti poter prevedere quali potrebbero essere i codici futuri.

Consigliamo vivamente l'utilizzo delle app TOTP mobili, invece delle alternative desktop, poiché Android e iOS forniscono una migliore sicurezza e isolamento delle app, rispetto a gran parte dei sistemi operativi per desktop.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. It can be used with an online account to back up and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. Può essere utilizzato anche offline su un singolo dispositivo senza la necessità di un account.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth&gl=IT)
- [:simple-appstore: App Store](https://apps.apple.com/it/app/ente-auth/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Logo di Aegis](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** è un'app gratuita, sicura e open source per gestire i token di verifica a due passaggi per i tuoi servizi online. Aegis Authenticator opera completamente offline/localmente, ma include l'opzione di esportare i token per il backup, a differenza di molte alternative.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Il codice sorgente dev'essere disponibile pubblicamente.
- Non deve richiedere la connessione a Internet.
- Cloud syncing must be optional, and (if available) sync functionality must be E2EE.
