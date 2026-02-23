---
title: "Qubes Übersicht"
icon: simple/qubesos
description: Qubes ist ein Betriebssystem, das auf der Isolierung von Anwendungen innerhalb von *qubes* (früher "VMs") basiert, um die Sicherheit zu erhöhen.
---

[**Qubes OS**](../desktop.md#qubes-os) ist ein Open-Source-Betriebssystem, das den [Xen-Hypervisor](https://en.wikipedia.org/wiki/Xen) nutzt, um durch isolierte *Qubes*(virtuelle Maschinen) starke Sicherheit für Desktop-Computing zu bieten. Du kannst jeden *qube* eine Vertrauensstufe zuweisen, die auf seinem Zweck basiert. Qubes OS bietet Sicherheit durch Isolation. Es erlaubt nur Aktionen auf einer Fall-zu-Fall-Basis und ist das Umkehrte von [Schlechtigkeitsaufzählung](https://ranum.com/security/computer_security/editorials/dumb).

## Wie funktioniert Qubes OS?

Qubes benutzt [Kompartimentierung](https://qubes-os.org/intro) um das System sicher zu halten. Qubes werden von Vorlagen erstellt, Es gibt Fedora, Debian und [Whonix](../desktop.md#whonix) als Standardeinstellungen. Qubes OS erlaubt dir [wegwerf](https://qubes-os.org/doc/how-to-use-disposables) *Qubes* für Einmalnutzung zu erstellen.

<details class="note" markdown>
<summary>Der Begriff <em>qubes</em> wird nach und nach aktualisiert, um die Bezeichnung "virtuelle Maschinen" zu vermeiden.</summary>

Manche Informationen hier und in der Dokumentation von Qubes OS beinhalten wiedersprüchliche Sprache, da der Begriff "appVM" langsam zu "Qube" geändert wird. Qubes sind nicht ganze virtuelle Maschinen, aber beinhalten ähnliche Funktionen wie VMs.

</details>

![Qubes Architektur](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architektur Quelle: What is Qubes OS Intro</figcaption>

Each qube has a [colored border](https://qubes-os.org/screenshots) that can help you keep track of the domain in which it runs. Du könntest zum Beispiel, eine bestimmte Farbe für einen Browser verwenden, wo du Onlinebanking führst, und eine andere Farbe für einen Browser fürs allgemeine browsen.

![Färbige Umrandung](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes Fensterumrandungen, Quelle: Qubes Screenshots</figcaption>

## Warum sollte ich Qubes verwenden?

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. Ein typischer Grund um Qubes OS zu benutzen ist, Dokumenten von unbekannten Quellen zu öffnen, aber die Idee ist, wenn ein Qube bedroht ist, wird es nicht das restliche System beeinträchtigen.

Qubes OS benutzt [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM um *Qubes* im host OS zu steuern. Diese werden als Fenster innerhalb dom0s Desktopumgebung angezeigt. Es gibt viele Nutzen für diese Architektur. Hier sind paar Aufgaben die du durchführen kannst. Du kannst sehen, wie sicherer diese Prozesse sind, indem man mehrere Schritte einbaut.

### Kopieren und Einfügen von Text

Du kannst [Text kopieren und einfügen](https://qubes-os.org/doc/how-to-copy-and-paste-text) mit `qvm-copy-to-vm` oder mit den folgenden Angaben:

1. Drücke **Strg+C** um einen *Qube* zu sagen, dass du etwas kopieren möchtest.
2. Drücke **Strg+Shift+C** um den *Qube* zu sagen, dass er in die globale Zwischenablage kopieren soll.
3. Drücke **Strg+Shift+V** im *Qube*, damit die globale Zwischenablage verfügar wird.
4. Drücke **Strg+V** im *Qube*, um etwas von der Zwischeneinlage einzufügen.

### Dateiaustausch

Um Dateien und Ordners von *Qube* zu Qube zu kopieren und einzufügen, kann man die Option **Copy to Other AppVM...** oder **Move to Other AppVM...** benutzen. Der Unterschied ist das die **Move** Option die originelle Datei löschen wird. Beide Optionen werden deine Zwischenablage schützen, zu anderen *Qubes* zugespielt zu werden. Dies ist sicherer als luftgeschütze Dateiübertragung. Ein luftgeschützer Computer muss trotzdem Partitionen oder ein Dateisystem erfassen. Das ist nicht gebraucht beim Inter-Qube-Kopiesystem.

<details class="note" markdown>
<summary>Qubes haben nicht ihre eigenen Dateisysteme.</summary>

Du kannst zwischen *Qubes* [Dateien kopieren und bewegen](https://qubes-os.org/doc/how-to-copy-and-move-files). When doing so the changes aren't immediately made and can be easily undone in case of an accident. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

</details>

### Inter-VM Interactions

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## Connecting to Tor via a VPN

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Deine Qubes sollten so ähnlich wie hier konfiguriert sein:

| Name            | Beschreibung                                                                                             | NetVM           |
| --------------- | -------------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Dein standard Netzwerkqube (vorinstalliert)*                                                            | *n/a*           |
| sys-firewall    | *Dein standard Firewallqube (vorinstalliert)*                                                            | sys-net         |
| ==sys-proxyvm== | Die VPN ProxyVM die du [erstellst](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) | sys-firewall    |
| sys-whonix      | Dein Whonix-Gateway-VM                                                                                   | ==sys-proxyvm== |
| anon-whonix     | Dein Whonix-Workstation-VM                                                                               | sys-whonix      |

## Zusätzliche Ressourcen

Für zusätzliche Informationen empfehlen wir dir, die umfangreichen Qubes OS-Dokumentation auf der [Qubes OS-Website](https://qubes-os.org/doc) zu konsultieren. Offline-Kopien können aus dem Qubes OS [Dokumentations-Repository](https://github.com/QubesOS/qubes-doc) heruntergeladen werden.

- [Möglicherweise Sicherstes Betriebssystem der Welt](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Software compartmentalization vs. physical seperation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)(J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Ähnliche Artikel](https://qubes-os.org/news/categories/#articles) (Qubes OS)
