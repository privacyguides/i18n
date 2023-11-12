---
title: "Panoramica di Qubes"
icon: simple/qubesos
description: Qubes è un sistema operativo basato sull'isolamento delle applicazioni all'interno delle *qubes* (precedentemente chiamate "VM"), per una maggiore sicurezza.
---

[**Qubes OS**](../desktop.md#qubes-os) è un sistema operativo open-source che utilizza l'hypervisor [Xen](https://en.wikipedia.org/wiki/Xen) per fornire una forte sicurezza per il desktop computing attraverso le *qube* isolate (che sono macchine virtuali). Puoi assegnare ad ogni *qube* un livello di fiducia in base al suo scopo. Qubes OS fornisce sicurezza utilizzando l'isolamento. Permette solo azioni su base individuale e quindi è l'opposto della [enumerazione dei difetti](https://www.ranum.com/security/computer_security/editorials/dumb/).

## Come funziona Qubes OS?

Qubes utilizza la [compartimentazione](https://www.qubes-os.org/intro/) per mantenere il sistema sicuro. I Qube sono creati da modelli, predefiniti per Fedora, Debian e [Whonix](../desktop.md#whonix). Qubes OS ti consente anche di creare *qubes* [monouso](https://www.qubes-os.org/doc/how-to-use-disposables/).

??? "Il termine *qubes* sta venendo pian piano aggiornato per evitare di confonderle con le "macchine virtuali"."

    Alcune informazioni riportate qui e nella documentazione di Quebes OS possono contenere un linguaggio contraddittorio, poiché il termine "appVM" sta venendo pian piano modificato in "qube". Le Qube non sono delle vere e proprie macchine virtuali, ma mantengono funzionalità simili alle VM.

![Architettura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architettura di Qubes, Crediti: Introduzione a Qubes OS</figcaption>

Ogni qube ha un [bordo colorato](https://www.qubes-os.org/screenshots/) che può aiutarti a tenere traccia del dominio in cui viene eseguito. Ad esempio, potresti utilizzare un colore specifico per le operazioni bancarie, utilizzandone uno differente per un browser generico non affidabile.

![Bordo colorato](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordi delle finestre di Qubes, Crediti: Screenshot di Qubes</figcaption>

## Perché dovrei usare Qubes?

Qubes OS è utile se il tuo [modello di minaccia](../basics/threat-modeling.md) richiede una forte sicurezza e isolamento, ad esempio se hai intenzione di aprire file non attendibili da fonti non attendibili. Un motivo tipico per utilizzare Qubes OS è quello di aprire documenti provenienti da fonti sconosciute, ma l'idea è che se un singolo qube viene compromesso non avrà ripercussioni sul resto del sistema.

Qubes OS utilizza [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM per controllare le altre *qube* sul sistema operativo host, che visualizzano le finestre delle singole applicazioni all'interno dell'ambiente desktop di dom0. Ci sono diversi modi per utilizzare questo tipo di architettura. Ecco alcune attività che puoi eseguire. Puoi notare quanto questi processi siano molto più sicuri incorporando più fasi.

### Copiare e incollare il testo

Puoi [copiare e incollare il testo](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) utilizzando `qvm-copy-to-vm` o le istruzioni seguenti:

1. Premi **Ctrl+C** per dire alla *qube* in cui ti trovi che vuoi copiare qualcosa.
2. Premi **Ctrl+Maiusc+C** per dire alla *qube* di rendere disponibile questo buffer negli appunti globali.
3. Premi **Ctrl+Maiusc+V** nella *qube* di destinazione per rendere disponibili gli appunti globali.
4. Premi **Ctrl+V** nella *qube* di destinazione per incollare il contenuto nel buffer.

### Scambio di file

Per copiare e incollare file e cartelle da una *qube* a un'altra, puoi usare l'opzione **Copia in un'altra AppVM...** o **Sposta in un'altra AppVM...**. La differenza è che l'opzione **Move** eliminerà il file originale. Entrambe le opzioni proteggeranno i tuoi appunti dalla trasmissione verso altre *qube*. Questo è più sicuro del trasferimento di file via etere. Un computer isolato sarà comunque costretto ad analizzare partizioni o file di sistema. Ciò non è necessario con il sistema di copia tra Qube.

??? "Le Qube non hanno i propri file di sistema."

    Puoi [copiare e spostare file](https://www.qubes-os.org/doc/how-to-copy-and-move-files/) tra le *qube*. Così facendo, le modifiche non vengono applicate immediatamente e sono facilmente annullabili, in caso di incidente. Quando esegui una *qube*, questa non dispone di un file di sistema persistente. Puoi creare e cancellare file, ma queste modifiche sono effimere.

### Interazioni tra VM

Il [framework qrexec](https://www.qubes-os.org/doc/qrexec/) è una parte fondamentale di Qubes che consente la comunicazione tra i domini. Si basa sulla libreria di Xen *vchan*, che facilita l'[isolamento tramite politiche](https://www.qubes-os.org/news/2020/06/22/new-qrexec-policy-system/).

## Connecting to Tor via a VPN

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Your qubes should be configured in a manner similar to this:

| Qube name       | Qube description                                                                                                 | NetVM           |
| --------------- | ---------------------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Your default network qube (pre-installed)*                                                                      | *n/a*           |
| sys-firewall    | *Your default firewall qube (pre-installed)*                                                                     | sys-net         |
| ==sys-proxyvm== | The VPN ProxyVM you [created](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) | sys-firewall    |
| sys-whonix      | Your Whonix Gateway VM                                                                                           | ==sys-proxyvm== |
| anon-whonix     | Your Whonix Workstation VM                                                                                       | sys-whonix      |

## Risorse aggiuntive

Per ulteriori informazioni si consiglia di consultare le ampie pagine di documentazione di Qubes OS presenti sul [sito web di Qubes OS](https://www.qubes-os.org/doc/). Le copie offline sono scaricabili dal [repository della documentazione](https://github.com/QubesOS/qubes-doc) di Qubes OS.

- [Probabilmente il sistema operativo più sicuro al mondo](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Compartimentazione software vs. separazione fisica](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Suddividere la mia vita digitale in domini di sicurezza](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Articoli Correlati](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
