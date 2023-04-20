---
title: "Panoramica di Qubes"
icon: pg/qubes-os
description: Qubes è un sistema operativo costruito per isolare le applicazioni all'interno di macchine virtuali per una maggiore sicurezza.
---

[**Qubes OS**](../desktop.md#qubes-os) è un sistema operativo che utilizza l'hypervisor [Xen](https://en.wikipedia.org/wiki/Xen) per fornire una forte sicurezza per il desktop computing attraverso macchine virtuali isolate. Ogni macchina virtuale è chiamata *Qube* e si può assegnare a ogni Qube un livello di fiducia in base al suo scopo. Poiché il sistema operativo Qubes garantisce la sicurezza utilizzando l'isolamento e consentendo azioni solo su base individuale, è l'opposto dell'[enumerazione delle minacce](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Come funziona Qubes OS?

Qubes utilizza la [compartimentazione](https://www.qubes-os.org/intro/) per mantenere il sistema sicuro. I Qubes sono creati da modelli, predefiniti per Fedora, Debian e [Whonix](../desktop.md#whonix). Qubes OS consente anche di creare macchine virtuali [monouso](https://www.qubes-os.org/doc/how-to-use-disposables/).

![Architettura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architettura di Qubes, da "What is Qubes OS Introduction"</figcaption>

Ogni applicazione Qubes ha un [bordo colorato](https://www.qubes-os.org/screenshots/) che può aiutare a tenere traccia della macchina virtuale in cui è in esecuzione. Potresti, per esempio, utilizzare un colore specifico per le operazioni bancarie e un colore diverso per un browser generico non affidabile.

![Bordo colorato](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordi Finestre Qubes, Credito: Qubes Screenshots</figcaption>

## Perché dovrei usare Qubes?

Qubes OS è utile se il tuo [modello di minaccia](../basics/threat-modeling.md) richiede una forte compartimentazione e sicurezza, ad esempio se vuoi aprire file non attendibili da fonti non sicure. Un motivo comune per utilizzare Qubes OS è l'apertura di documenti provenienti da fonti sconosciute.

Qubes OS utilizza [Dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM (cioè una "AdminVM") per controllare altre VM guest o Qubes sul sistema operativo host. Le altre macchine virtuali visualizzano le finestre delle singole applicazioni all'interno dell'ambiente desktop di Dom0. Ti Permette di assegnare un colore alle finestre in base ai livelli di fiducia e di eseguire applicazioni che possono interagire tra loro con un controllo molto granulare.

### Copiare e incollare il testo

Puoi [copiare e incollare il testo](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) utilizzando `qvm-copy-to-vm` o le istruzioni seguenti:

1. Premi **Ctrl+C** per comunicare alla macchina virtuale in cui ti trovi che vuoi copiare qualcosa.
2. Premi **Ctrl+Shift+C** per comunicare alla macchina virtuale di rendere disponibile questo buffer negli appunti globali.
3. Premi **Ctrl+Shift+V** nella macchina virtuale di destinazione per rendere disponibili gli appunti globali.
4. Premi **Ctrl+V** nella macchina virtuale di destinazione per incollare il contenuto nel buffer.

### Scambio di file

Per copiare e incollare file e directory (cartelle) da una macchina virtuale all'altra, si può usare l'opzione **Copy to Other AppVM...** o **Move to Other AppVM...**. La differenza è che l'opzione **Move** elimina il file originale. Entrambe le opzioni proteggono gli appunti dalla trasmissione ad altre Qubes. Questa soluzione è più sicura del trasferimento di file air-gapped, perché un computer air-gapped sarà comunque costretto ad analizzare partizioni o file system. Questo non è necessario con il sistema di copia tra qubes.

??? info "Le AppVM o le qubes non hanno un proprio file system"

    Puoi [copiare e spostare file](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) tra le Qubes. In questo modo le modifiche non vengono apportate subito e possono essere facilmente annullate in caso di incidente.

### Interazioni tra VM

Il [framework qrexec](https://www.qubes-os.org/doc/qrexec/) è una parte fondamentale di Qubes che consente la comunicazione tra i domini delle macchine virtuali. È costruito sulla base della libreria Xen *vchan*, che facilita [l'isolamento attraverso le politiche](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Risorse aggiuntive

Per ulteriori informazioni si consiglia di consultare le ampie pagine di documentazione di Qubes OS presenti sul [sito web di Qubes OS](https://www.qubes-os.org/doc/). Le copie offline possono essere scaricate dal [repository della documentazione](https://github.com/QubesOS/qubes-doc) di Qubes OS.

- Open Technology Fund: [*Arguably the world's most secure operating system (Probabilmente il sistema operativo più sicuro al mondo)*](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/)
- J. Rutkowska: [*Software compartmentalization vs. physical separation (Compartimentazione del software vs. separazione fisica)*](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)
- J. Rutkowska: [*Partitioning my digital life into security domains (Suddividere la mia vita digitale in domini di sicurezza)*](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html)
- Qubes OS: [*Articoli correlati*](https://www.qubes-os.org/news/categories/#articles)
