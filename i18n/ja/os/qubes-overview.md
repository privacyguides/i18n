---
title: "Qubesの概要"
icon: simple/qubesos
description: Qubesは、アプリケーションをqubes（以前は「VMs」と呼ばれていた）内で隔離することに基づいて構築されたオペレーティングシステムで、セキュリティを強化しています。
---

[**Qubes OS**](../desktop.md#qubes-os) は [Xen](https://en.wikipedia.org/wiki/Xen) ハイパーバイザーを使用し、隔離された *qubes*, (仮想マシン)を通じてデスクトップコンピューティングの強力なセキュリティを提供するオープンソースのオペレーティングシステムです。 各 *qube* に、その目的に基づいて信頼レベルを割り当てることができます。 Qubes OSは、アイソレーションを使用することでセキュリティを提供します。 ケースごとにアクションを許可するだけであり、[badness enumeration](https://ranum.com/security/computer_security/editorials/dumb)の反対です。

## Qubes OSの仕組み

Qubesは、システムのセキュリティを維持するために [区画化](https://qubes-os.org/intro) を行っています。 Qubeはテンプレートから作成され、デフォルトはFedora、Debian、および [Whonix](../desktop.md#whonix)です。 Qubes OSは、一度だけ使用する [使い捨て](https://qubes-os.org/doc/how-to-use-disposables) の *qube*を作成することも可能です。

<details class="note" markdown>
<summary><em>qube</em>という用語は、それらを「仮想マシン」と呼ぶことを避けるために徐々に更新されています。</summary>

ここおよびQubes OSのドキュメントにある情報の一部は、「appVM」という用語が徐々に「qube」に変更されているため、矛盾する表現を含む場合があります。 Qubesは完全な仮想マシンではありませんが、VMと類似の機能を維持しています。

</details>

![Qubesのアーキテクチャー](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubeアーキテクチャ、クレジット: Qubes OSイントロ</figcaption>

各qubeには、実行されているドメインを把握するのに役立つ [色のついた枠線](https://qubes-os.org/screenshots) があります。 You could, for example, use a specific color for your banking browser, while using a different color for a general untrusted browser.

![Colored border](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes window borders, Credit: Qubes Screenshots</figcaption>

## Qubesを使うべき理由

Qubes OS is useful if your [threat model](../basics/threat-modeling.md) requires strong security and isolation, such as if you think you'll be opening untrusted files from untrusted sources. A typical reason for using Qubes OS is to open documents from unknown sources, but the idea is that if a single qube is compromised it won't affect the rest of the system.

Qubes OS utilizes [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM for controlling other *qubes* on the host OS, all of which display individual application windows within dom0's desktop environment. There are many uses for this type of architecture. Here are some tasks you can perform. You can see just how much more secure these processes are made by incorporating multiple steps.

### テキストのコピー＆ペースト

You can [copy and paste text](https://qubes-os.org/doc/how-to-copy-and-paste-text) using `qvm-copy-to-vm` or the below instructions:

1. Press **Ctrl+C** to tell the *qube* you're in that you want to copy something.
2. Press **Ctrl+Shift+C** to tell the *qube* to make this buffer available to the global clipboard.
3. Press **Ctrl+Shift+V** in the destination *qube* to make the global clipboard available.
4. Press **Ctrl+V** in the destination *qube* to paste the contents in the buffer.

### ファイルの交換

To copy and paste files and directories (folders) from one *qube* to another, you can use the option **Copy to Other AppVM...** or **Move to Other AppVM...**. The difference is that the **Move** option will delete the original file. Either option will protect your clipboard from being leaked to any other *qubes*. This is more secure than air-gapped file transfer. An air-gapped computer will still be forced to parse partitions or file systems. That is not required with the inter-qube copy system.

<details class="note" markdown>
<summary>Qubes do not have their own filesystems.</summary>

You can [copy and move files](https://qubes-os.org/doc/how-to-copy-and-move-files) between *qubes*. When doing so the changes aren't immediately made and can be easily undone in case of an accident. When you run a *qube*, it does not have a persistent filesystem. You can create and delete files, but these changes are ephemeral.

</details>

### Inter-VM Interactions

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## VPN経由でTorに接続

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Your qubes should be configured in a manner similar to this:

| キューブ名           | キューブの説明                                                                                             | NetVM           |
| --------------- | --------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *デフォルトのネットワークキューブ（プリインストール済み）*                                                                      | *なし*            |
| sys-firewall    | *デフォルトのファイアウォールキューブ（プリインストール済み）*                                                                    | sys-net         |
| ==sys-proxyvm== | The VPN ProxyVM you [created](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) | sys-firewall    |
| sys-whonix      | WhonixゲートウェイのVM                                                                                     | ==sys-proxyvm== |
| anon-whonix     | WhonixワークステーションのVM                                                                                  | sys-whonix      |

## その他の資料

For additional information we encourage you to consult the extensive Qubes OS documentation pages located on the [Qubes OS Website](https://qubes-os.org/doc). Offline copies can be downloaded from the Qubes OS [documentation repository](https://github.com/QubesOS/qubes-doc).

- [Arguably the world's most secure operating system](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://qubes-os.org/news/categories/#articles) (Qubes OS)
