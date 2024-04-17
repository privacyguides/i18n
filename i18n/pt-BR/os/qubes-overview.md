---
title: "Visão geral do Qubes"
icon: simple/qubesos
description: O Qubes é um sistema operacional criado para isolar aplicativos dentro de *qubes* (anteriormente "VMs") para aumentar a segurança.
---

[**Qubes OS**](../desktop.md#qubes-os) é um sistema operacional de código aberto que usa o hipervisor [Xen](https://en.wikipedia.org/wiki/Xen) para fornecer segurança robusta para a computação de desktop por meio de *qubes* isolados (que são máquinas virtuais). Você pode atribuir a cada *qube* um nível de confiança com base em sua finalidade. O Qubes OS fornece segurança usando o isolamento. Ele só permite ações por caso e, portanto, é o oposto da [enumeração de maldade](https://ranum.com/security/computer_security/editorials/dumb).

## Como funciona o Qubes OS?

Qubes usa [compartimentação](https://qubes-os.org/intro) para manter o sistema seguro. Os Qubes são criados a partir de modelos, sendo as predefinições para Fedora, Debian e [Whonix](../desktop.md#whonix). O Qubes OS também permite que você crie *qubos* [descartáveis](https://qubes-os.org/doc/how-to-use-disposables) de uso único.

<details class="note" markdown>
<summary>O termo <em>qubes</em> está sendo atualizado gradualmente para evitar que se refira a eles como "máquinas virtuais".</summary>

Algumas das informações aqui e na documentação do Qubes OS podem conter linguagem conflitante, pois o termo "appVM" está sendo gradualmente alterado para "qube". Os Qubes não são máquinas virtuais inteiras, mas mantêm funcionalidades semelhantes às das VMs.

</details>

![Arquitetura de Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Arquitetura Qubes, Crédito: O que é o Qubes OS Intro</figcaption>

Cada qube tem uma [borda colorida](https://qubes-os.org/screenshots) que pode ajudá-lo a monitorar o domínio em que é executado. Você pode, por exemplo, usar uma cor específica para o navegador do banco, enquanto usa uma cor diferente para um navegador geral não confiável.

![Borda colorida](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordas da janela do Qubes, Crédito: Qubes Screenshots</figcaption>

## Por Que Devo Usar Qubes?

O Qubes OS é útil se o seu [modelo de ameaças](../basics/threat-modeling.md) exigir segurança e isolamento fortes, por exemplo, se você acha que abrirá arquivos não confiáveis de fontes não confiáveis. Uma razão típica para usar o Qubes OS é abrir documentos de fontes desconhecidas, mas a ideia é que, se se comprometer uma única quarta, isso não afetará o resto do sistema.

O Qubes OS utiliza a VM Xen [dom0](https://wiki.xenproject.org/wiki/Dom0) para controlar outros *qubes* no sistema operacional host, todos exibindo janelas de aplicativos individuais no ambiente de desktop do dom0. Há muitos usos para esse tipo de arquitetura. Aqui estão algumas tarefas que você pode realizar. Você pode ver como esses processos se tornam muito mais seguros ao incorporar várias etapas.

### Cópia e Colagem de Texto

Você pode [copiar e colar texto](https://qubes-os.org/doc/how-to-copy-and-paste-text) usando `qvm-copy-to-vm` ou as instruções abaixo:

1. Pressione **Ctrl+C** para informar ao *qube* em que você está que deseja copiar algo.
2. Pressione **Ctrl+Shift+C** para informar ao *qube* para tornar esse buffer disponível para a área de transferência global.
3. Pressione **Ctrl+Shift+V** na *janela* de destino para disponibilizar a área de transferência global.
4. Pressione **Ctrl+V** na *caixa* de destino para colar o conteúdo no buffer.

### Troca de arquivos

Para copiar e colar arquivos e diretórios (pastas) de um *qube* para outro, você pode usar a opção **Copiar para outro AppVM..** ou **Mover para outro AppVM...**. A diferença é que a opção **Mover** excluirá o arquivo original. Qualquer uma das opções protegerá sua área de transferência contra o vazamento para outros *usuários*. Isso é mais seguro do que a transferência de arquivos por "air-gap". Um computador com "air-gap" ainda será forçado a analisar partições ou sistemas de arquivos. Isso não é necessário com o sistema de cópia entre sondas.

<details class="note" markdown>
<summary>Os Qubes não têm seus próprios sistemas de arquivos.</summary>

Você pode [copiar e mover arquivos](https://qubes-os.org/doc/how-to-copy-and-move-files) entre os *qubies*. Ao fazer isso, as alterações não são feitas imediatamente e podem ser facilmente desfeitas em caso de acidente. Quando você executa um *qube*, ele não tem um sistema de arquivos persistente. Você pode criar e excluir arquivos, mas essas alterações são efêmeras.

</details>

### Interações entre VMs

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

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

## Recursos Adicionais

For additional information we encourage you to consult the extensive Qubes OS documentation pages located on the [Qubes OS Website](https://qubes-os.org/doc). Offline copies can be downloaded from the Qubes OS [documentation repository](https://github.com/QubesOS/qubes-doc).

- [Arguably the world's most secure operating system](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://qubes-os.org/news/categories/#articles) (Qubes OS)
