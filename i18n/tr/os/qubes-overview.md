---
title: "Qubes Genel Bakış"
icon: simple/qubesos
description: Qubes, yüksek güvenlik için uygulamaları *qubes* (eski adıyla "VM'ler") içinde izole etmek üzerine kurulu bir işletim sistemidir.
---

[**Qubes İşletim Sistemi**](../desktop.md#qubes-os) izole edilmiş *küpler*(Sanal Makineler) aracılığıyla masaüstü bilgisayarlar için güçlü güvenlik sağlamak üzere [Xen](https://en.wikipedia.org/wiki/Xen) hipervizörünü kullanan açık kaynaklı bir işletim sistemidir. Her bir *küpe* amacına göre bir güven düzeyi atayabilirsiniz. Qubes OS izolasyon kullanarak güvenlik sağlar. Yalnızca vaka bazında eylemlere izin verir ve bu nedenle [kötülük numar](https://ranum.com/security/computer_security/editorials/dumb)alandırmanın tam tersidir.

## Qubes OS nasıl çalışır?

Qubes, sistemi güvende tutmak için [bölümlere ayırma](https://qubes-os.org/intro) özelliğini kullanır. Qubes şablonlardan oluşturulur, varsayılanlar Fedora, Debian ve [Whonix](../desktop.md#whonix) içindir. Qubes OS ayrıca bir kez kullanılabilen [tek](https://qubes-os.org/doc/how-to-use-disposables) kullanımlık *küpler* oluşturmanıza da olanak tanır.

<details class="note" markdown>
<summary>The term <em>qubes</em> is gradually being updated to avoid referring to them as "virtual machines".</summary>

Some of the information here and on the Qubes OS documentation may contain conflicting language as the "appVM" term is gradually being changed to "qube". Qubes are not entire virtual machines, but maintain similar functionalities to VMs.

</details>

![Qubes architecture](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architecture, Credit: What is Qubes OS Intro</figcaption>

Each qube has a [colored border](https://qubes-os.org/screenshots) that can help you keep track of the domain in which it runs. You could, for example, use a specific color for your banking browser, while using a different color for a general untrusted browser.

![Colored border](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes window borders, Credit: Qubes Screenshots</figcaption>

## Why Should I use Qubes?

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. A typical reason for using Qubes OS is to open documents from unknown sources, but the idea is that if a single qube is compromised it won't affect the rest of the system.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### Copying and Pasting Text

You can [copy and paste text](https://qubes-os.org/doc/how-to-copy-and-paste-text) using `qvm-copy-to-vm` or the below instructions:

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### File Exchange

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. The difference is that the **Move** option will delete the original file. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. That is not required with the inter-qube copy system.

<details class="note" markdown>
<summary>Qubes do not have their own filesystems.</summary>

You can [copy and move files](https://qubes-os.org/doc/how-to-copy-and-move-files) between *qubes*. When doing so the changes aren't immediately made and can be easily undone in case of an accident. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

</details>

### Inter-VM Interactions

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## Connecting to Tor via a VPN

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Your qubes should be configured in a manner similar to this:

| Qube name       | Qube description                                                                                   | NetVM           |
| --------------- | -------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Your default network qube (pre-installed)*                                                        | *n/a*           |
| sys-firewall    | *Your default firewall qube (pre-installed)*                                                       | sys-net         |
| ==sys-proxyvm== | [Oluşturduğunuz](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) VPN ProxyVM | sys-firewall    |
| sys-whonix      | Whonix Gateway VM'niz                                                                              | ==sys-proxyvm== |
| anon-whonix     | Whonix Workstation VM'niz                                                                          | sys-whonix      |

## Ek Kaynaklar

Daha fazla bilgi için Qubes OS [Web Sitesinde](https://qubes-os.org/doc) bulunan kapsamlı Qubes OS dokümantasyon sayfalarına başvurmanızı öneririz. Çevrimdışı kopyalar Qubes OS [dokümantasyon deposundan](https://github.com/QubesOS/qubes-doc) indirilebilir.

- [Tartışmasız dünyanın en güvenli işletim sistemi](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Yazılım bölümlendirmesi ve fiziksel ayırma](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Dijital hayatımı güvenlik alanlarına bölmek](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [İlgili Makaleler](https://qubes-os.org/news/categories/#articles) (Qubes OS)
