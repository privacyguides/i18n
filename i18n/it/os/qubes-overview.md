---
title: "Panoramica di Qubes"
icon: simple/qubesos
description: Qubes è un sistema operativo basato sull'isolamento delle applicazioni all'interno delle *qube* (precedentemente chiamate "VM"), per una maggiore sicurezza.
---

[**Qubes OS**](../desktop.md#qubes-os) è un sistema operativo open-source che utilizza l'hypervisor [Xen](https://en.wikipedia.org/wiki/Xen) per fornire una forte sicurezza per il desktop computing attraverso le *qube* isolate (che sono macchine virtuali). Puoi assegnare ad ogni *qube* un livello di fiducia in base al suo scopo. Qubes OS fornisce sicurezza utilizzando l'isolamento. It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://ranum.com/security/computer_security/editorials/dumb).

## Come funziona Qubes OS?

Qubes uses [compartmentalization](https://qubes-os.org/intro) to keep the system secure. I Qube sono creati da modelli, predefiniti per Fedora, Debian e [Whonix](../desktop.md#whonix). Qubes OS also allows you to create once-use [disposable](https://qubes-os.org/doc/how-to-use-disposables) *qubes*.

<details class="note" markdown>
<summary>Il termine <em>qubes</em> viene gradualmente aggiornato per evitare di riferirsi ad essi come "macchine virtuali".</summary>

Alcune informazioni riportate qui e nella documentazione di Quebes OS possono contenere un linguaggio contraddittorio, poiché il termine "appVM" sta venendo pian piano modificato in "qube". Le Qube non sono delle vere e proprie macchine virtuali, ma mantengono funzionalità simili alle VM.

</details>

![Architettura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Architettura di Qubes, Crediti: Introduzione a Qubes OS</figcaption>

Each qube has a [colored border](https://qubes-os.org/screenshots) that can help you keep track of the domain in which it runs. Ad esempio, potresti utilizzare un colore specifico per le operazioni bancarie, utilizzandone uno differente per un browser generico non affidabile.

![Bordo colorato](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordi delle finestre di Qubes, Crediti: Screenshot di Qubes</figcaption>

## Perché dovrei usare Qubes?

Qubes OS è utile se il tuo [modello di minaccia](../basics/threat-modeling.md) richiede una forte sicurezza e isolamento, ad esempio se hai intenzione di aprire file non attendibili da fonti non attendibili. Un motivo tipico per utilizzare Qubes OS è quello di aprire documenti provenienti da fonti sconosciute, ma l'idea è che se un singolo qube viene compromesso non avrà ripercussioni sul resto del sistema.

Qubes OS utilizza [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM per controllare le altre *qube* sul sistema operativo host, che visualizzano le finestre delle singole applicazioni all'interno dell'ambiente desktop di dom0. Ci sono diversi modi per utilizzare questo tipo di architettura. Ecco alcune attività che puoi eseguire. Puoi notare quanto questi processi siano molto più sicuri incorporando più fasi.

### Copiare e incollare il testo

You can [copy and paste text](https://qubes-os.org/doc/how-to-copy-and-paste-text) using `qvm-copy-to-vm` or the below instructions:

1. Premi **Ctrl+C** per dire alla *qube* in cui ti trovi che vuoi copiare qualcosa.
2. Premi **Ctrl+Maiusc+C** per dire alla *qube* di rendere disponibile questo buffer negli appunti globali.
3. Premi **Ctrl+Maiusc+V** nella *qube* di destinazione per rendere disponibili gli appunti globali.
4. Premi **Ctrl+V** nella *qube* di destinazione per incollare il contenuto nel buffer.

### Scambio di file

Per copiare e incollare file e cartelle da una *qube* a un'altra, puoi usare l'opzione **Copia in un'altra AppVM...** o **Sposta in un'altra AppVM...**. La differenza è che l'opzione **Move** eliminerà il file originale. Entrambe le opzioni proteggeranno i tuoi appunti dalla trasmissione verso altre *qube*. Questo è più sicuro del trasferimento di file via etere. Un computer isolato sarà comunque costretto ad analizzare partizioni o file di sistema. Ciò non è necessario con il sistema di copia tra Qube.

<details class="note" markdown>
<summary>I Qubes non hanno un proprio filesystem.</summary>

You can [copy and move files](https://qubes-os.org/doc/how-to-copy-and-move-files) between *qubes*. Così facendo, le modifiche non vengono applicate immediatamente e sono facilmente annullabili, in caso di incidente. Quando si esegue un *qube*, non ha un filesystem persistente. Puoi creare e cancellare file, ma queste modifiche sono effimere.

</details>

### Interazioni tra VM

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## Connettersi a Tor tramite una VPN

[Consigliamo](../advanced/tor-overview.md) di connettersi alla rete di Tor tramite un fornitore di [VPN](../vpn.md) e, fortunatamente, Qubes semplifica ciò combinando ProxyVM e Whonix.

After [creating a new ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

I tuoi qube dovrebbero esser configurati similmente a come segue:

| Nome del Qube   | Descrizione del Qube                                                                                | NetVM           |
| --------------- | --------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Il tuo qube di rete predefinito (preinstallato)*                                                   | *n/d*           |
| sys-firewall    | *Il qube del tuo firewall predefinito (preinstallato)*                                              | sys-net         |
| ==sys-proxyvm== | The VPN ProxyVM you [created](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) | sys-firewall    |
| sys-whonix      | La tua VM del Gateway di Whonix                                                                     | ==sys-proxyvm== |
| anon-whonix     | La tua VM della Workstation di Whonix                                                               | sys-whonix      |

## Risorse aggiuntive

For additional information we encourage you to consult the extensive Qubes OS documentation pages located on the [Qubes OS Website](https://qubes-os.org/doc). Le copie offline sono scaricabili dal [repository della documentazione](https://github.com/QubesOS/qubes-doc) di Qubes OS.

- [Arguably the world's most secure operating system](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Compartimentazione software vs. separazione fisica](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Suddividere la mia vita digitale in domini di sicurezza](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://qubes-os.org/news/categories/#articles) (Qubes OS)
