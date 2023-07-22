---
title: "Panoramica di Qubes"
icon: simple/qubesos
description: Qubes è un sistema operativo basato sull'isolamento delle app su macchine virtuali, per una maggiore sicurezza.
---

[**Qubes OS**](../desktop.md#qubes-os) is an open-source operating system which uses the [Xen](https://en.wikipedia.org/wiki/Xen) hypervisor to provide strong security for desktop computing through isolated virtual machines. Ogni macchina virtuale è chiamata *Qube* e, a ognuna di esse, puoi assegnare un livello di fiducia, basato sul suo scopo. As Qubes OS provides security by using isolation, and only permitting actions on a per-case basis, it is the opposite of [badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Come funziona Qubes OS?

Qubes utilizza la [compartimentazione](https://www.qubes-os.org/intro/) per mantenere il sistema sicuro. I Qube sono creati da modelli, predefiniti per Fedora, Debian e [Whonix](../desktop.md#whonix). Inoltre, Qubes OS ti consente di creare mcchine virtuali [monouso](https://www.qubes-os.org/doc/how-to-use-disposables/) e a uso singolo.

![Architettura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architettura di Qubes, Crediti: Introduzione a Qubes OS</figcaption>

Ogni applicazione di Qubes ha un [bordo colorato](https://www.qubes-os.org/screenshots/), che può aiutarti a tenere traccia della macchina virtuale in esecuzione. Ad esempio, potresti utilizzare un colore specifico per le operazioni bancarie, utilizzandone uno differente per un browser generico non affidabile.

![Bordo colorato](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordi delle finestre di Qubes, Crediti: Screenshot di Qubes</figcaption>

## Perché dovrei usare Qubes?

Qubes OS è utile se il tuo [modello di minaccia](../basics/threat-modeling.md) richiede un forte compartimentazione e sicurezza, ad esempio, se ritieni che aprirai file non attendibili da fonti non sicure. Un tipico motivo per utilizzare Qubes OS è aprire documenti da fonti sconosciute.

Qubes OS utilizza la VM di Xen [Dom0](https://wiki.xenproject.org/wiki/Dom0) (cioè, "AdminVM"), per controllare altre VM ospiti o Qubes sul sistema operativo del host. Le altre VM mostrano le finestre delle singole applicazioni, nell'ambiente desktop di Dom0. Ti consente di codificare per colore le finestre, secondo i livelli di fiducia e di eseguire le app che possono interagire tra loro, con un controllo molto granulare.

### Copiare e incollare il testo

Puoi [copiare e incollare il testo](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) utilizzando `qvm-copy-to-vm` o le istruzioni seguenti:

1. Premi **Ctrl+C** per comunicare alla macchina virtuale in cui ti trovi che vuoi copiare qualcosa.
2. Premi **Ctrl+Shift+C** per comunicare alla macchina virtuale di rendere disponibile questo buffer negli appunti globali.
3. Premi **Ctrl+Shift+V** nella macchina virtuale di destinazione per rendere disponibili gli appunti globali.
4. Premi **Ctrl+V** nella macchina virtuale di destinazione per incollare il contenuto nel buffer.

### Scambio di file

Per copiare e incollare file e directory (cartelle) da una macchina virtuale all'altra, si può usare l'opzione **Copy to Other AppVM...** o **Move to Other AppVM...**. La differenza è che l'opzione **Move** eliminerà il file originale. Entrambe le opzioni proteggeranno i tuoi appunti dall'essere trapelati a qualsiasi altra Qube. Ciò è più sicuro del trasferimento di file isolaato, poiché un computer isolato sarà comunque forzato a recuperare partizioni o file di sistema. Ciò non è necessario con il sistema di copia tra Qube.

??? info "Le AppVM o Qube non hanno i propri file di sistema"

    Puoi [copiare e spostare i file](https://www.qubes-os.org/doc/how-to-copy-and-move-files/), tra Qube. Così facendo, le modifiche non sono effettuate immediatamente e sono facilmente annullabili, in caso di incidente.

### Interazioni tra VM

Il [quadro qrexec](https://www.qubes-os.org/doc/qrexec/) è una parte fondamentale di Qubes, che consente la comunicazione tra i domini delle macchine virtuali. Si basa sulla libreria di Xen *vchan*, che facilita l'[isolamento tramite politiche](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Ulteriori Risorse

Per ulteriori informazioni si consiglia di consultare le ampie pagine di documentazione di Qubes OS presenti sul [sito web di Qubes OS](https://www.qubes-os.org/doc/). Le copie offline sono scaricabili dalla [repository della documentazione](https://github.com/QubesOS/qubes-doc) di Qubes OS.

- Open Technology Fund: [*Probabilmente il sistema operativo più sicuro al mondo*](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/)
- J. Rutkowska: [*Compartimentazione del software vs. separazione fisica*](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)
- J. Rutkowska: [*Partizionamento della mia vita digitale in domini di sicurezza*](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html)
- Qubes OS: [*Articoli correlati*](https://www.qubes-os.org/news/categories/#articles)
