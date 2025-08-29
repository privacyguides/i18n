---
meta_title: "I Migliori Sistemi Operativi Android – Privacy Guides"
title: "Distribuzioni Alternative"
description: Puoi sostituire il sistema operativo del tuo telefono Android con queste alternative sicure e rispettose della privacy.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protegge dalle seguenti minacce:</small>

- [:material-target-account: Attacchi mirati](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attacchi passivi](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Un **sistema operativo personalizzato basato su Android** (a volte indicato come **ROM personalizzata**) può essere un modo per ottenere un livello più elevato di privacy e sicurezza sul proprio dispositivo. Questo si contrappone alla versione "stock" di Android, fornita con il telefono al momento dell’acquisto e preinstallata, che spesso è strettamente integrata con Google Play Services e con altro software del produttore.

Consigliamo di installare GrapheneOS se hai un Google Pixel, perché migliora la sicurezza e offre funzionalità aggiuntive per la privacy. I motivi per cui non elenchiamo altri sistemi operativi o dispositivi sono i seguenti:

- Spesso hanno una [sicurezza più debole](index.md#install-a-custom-distribution).
- Spesso non vengono più aggiornate quando chi li sviluppa perde interesse o cambia dispositivo, a differenza del [ciclo di supporto](https://grapheneos.org/faq#device-lifetime) regolare seguito da GrapheneOS.
- Generalmente offrono pochi o nessun miglioramento significativo in termini di privacy o sicurezza che ne giustifichi l’installazione.

## GrapheneOS

<div class="admonition recommendation" markdown>

![Logo di GrapheneOS](../assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo di GrapheneOS](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** è la scelta migliore quando si parla di privacy e sicurezza.

GrapheneOS offre un ulteriore miglioramento della privacy e della [sicurezza](https://en.wikipedia.org/wiki/Hardening_\(computing\)). Dispone di un [allocatore di memoria rafforzato](https://github.com/GrapheneOS/hardened_malloc), permessi per rete e sensori, e altre [funzionalità di sicurezza](https://grapheneos.org/features). GrapheneOS include anche aggiornamenti firmware completi e build firmate, quindi il Verified Boot è completamente supportato.

[:octicons-home-16: Pagina principale](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Informativa Sulla Privacy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuisci }

</div>

GrapheneOS consente l’uso di [Google Play in una sandbox](https://grapheneos.org/usage#sandboxed-google-play), che esegue Google Play Services isolati come qualsiasi altra app. In questo modo è possibile utilizzare la maggior parte dei servizi di Google Play Services, come le notifiche push, dandoti un controllo completo sui loro permessi e autorizzazioni, e limitandoli a un [profilo di lavoro](../os/android-overview.md#work-profile) o a un [profilo utente](../os/android-overview.md#user-profiles) a tua scelta.

Al momento, solo i [telefoni Google Pixel](../mobile-phones.md#google-pixel) soddisfano i [requisiti di sicurezza hardware](https://grapheneos.org/faq#future-devices) di GrapheneOS.

Per impostazione predefinita, Android effettua molte connessioni di rete verso Google per verificare che il DNS funzioni correttamente, sincronizzarsi con l’orario di rete, verificare la connessione e svolgere altri compiti in background. GrapheneOS sostituisce queste connessioni con server gestiti da loro e soggetti alla loro informativa sulla privacy. Questo nasconde informazioni come il tuo indirizzo IP [a Google](../basics/common-threats.md#privacy-from-service-providers), ma rende facile per un amministratore di rete o per il provider Internet vedere che ti stai collegando a grapheneos.network, grapheneos.org, ecc., e capire quale sistema operativo stai usando.

Se vuoi nascondere informazioni come queste a un attaccante presente sulla tua rete o al provider Internet, **devi** usare una [VPN affidabile](../vpn.md) oltre a impostare il controllo della connettività su **Standard (Google)**. Puoi trovarla in :gear: **Impostazioni** → **Rete e Internet** → **Internet connectivity checks**. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

## Criteri

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Deve essere un software open source.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
