---
title: "Condivisione e sincronizzazione dei file"
icon: material/share-variant
description: Scopri come condividere privatamente i tuoi file tra i tuoi dispositivi, con i tuoi amici e familiari, o anonimamente online.
cover: file-sharing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Scopri come condividere privatamente i tuoi file tra i tuoi dispositivi, con i tuoi amici e familiari, o anonimamente online.

## Condivisione di file

If you already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

### Send

<div class="admonition recommendation" markdown>

![Logo di Send](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** è un fork del servizio Firefox Send di Mozilla, ormai dismesso, che ti consente di inviare file ad altre persone con un link. I file sono crittografati sul tuo dispositivo così che non possano esser letti dal server e, facoltativamente, possono essere anche protetti da password. Il manutentore di Send ospita una [istanza pubblica](https://send.vis.ee). Puoi utilizzare altre istanze pubbliche, o puoi ospitare Send autonomamente.

[:octicons-home-16: Home](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Istanze Pubbliche"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribuisci }

</details>

</div>

Send può essere utilizzato tramite la sua interfaccia web o tramite la CLI [ffsend](https://github.com/timvisee/ffsend). Se hai familiarità con la riga di comando e invii file di frequente, consigliamo di utilizzare il client della CLI per evitare la crittografia basata su JavaScript. Puoi specificare il flag `--host` per utilizzare un server specifico:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. Funziona avviando un server web accessibile come servizio Tor onion, con un URL inesplicabile che si può condividere con i destinatari per scaricare o inviare file.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Servizio Onion" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Non deve memorizzare i dati decrittografati su un server remoto.
- Deve essere un software open source.
- Deve avere i client per Linux, macOS e Windows, o disporre di un'interfaccia web.

## FreedomBox

<div class="admonition recommendation" markdown>

![Logo di FreedomBox](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** è un sistema operativo progettato per essere eseguito su un [computer a scheda singola (SBC)](https://it.wikipedia.org/wiki/Single-board_computer). Lo scopo è semplificare la configurazione delle applicazioni server, che potresti voler ospitare autonomamente.

[:octicons-home-16: Pagina Principale](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentazione}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribuisci }

</details>

</div>

## Sincronizzazione dei file

### Nextcloud (Client-Server)

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

[:octicons-home-16: Pagina Principale](https://nextcloud.com/it/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/it/privacy/){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://nextcloud.com/it/support/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://nextcloud.com/it/contribute/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Sconsigliamo di utilizzare l'[App E2EE](https://apps.nextcloud.com/apps/end_to_end_encryption) per Nextcloud, in quanto potrebbe causare la perdita di dati; è altamente sperimentale e non dispone di una qualità di produzione.

</div>

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Logo di Syncthing](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** è un'utility open source tra peer di sincronizzazione continua dei file. Viene utilizzata per sincronizzare i file tra due o più dispositivi sulla rete locale o su Internet. Syncthing non utilizza un server centralizzato; utilizza il [Protocollo di Scambio dei Blocchi](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) per trasferire i dati tra dispositivi. Tutti i dati sono crittografati utilizzando TLS.

[:octicons-home-16: Pagina Principale](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

#### Requisiti minimi

- Non deve richiedere un server remoto/su cloud di terze parti.
- Deve essere un software open source.
- Deve avere i client per Linux, macOS e Windows, o disporre di un'interfaccia web.

#### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Should have mobile clients for iOS and Android which at least support document previews.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the Send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).
