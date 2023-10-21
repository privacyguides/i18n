---
title: "Torの概要"
icon: 'simple/torproject'
description: Torは、可能な限りプライバシーを守ってインターネットを利用するために設計された、自由に利用できる分散型ネットワークです。
---

Torは、可能な限りプライバシーを守ってインターネットを利用するために設計された、自由に利用できる分散型ネットワークです。 適切に使用すれば、プライベートで匿名のブラウジングや通信を行うことができます。

## クリアネット・サービスへの通路の構築

「クリアネット・サービス」とは、 [privacyguides.org](https://www.privacyguides.org)のように、どのブラウザーでもアクセスできるウェブサイトのことです。 Torは、ノード（またはリレー）と呼ばれる、ボランティアが運営する何千ものサーバーで構成されるネットワークを経由してトラフィックをルーティングすることにより、匿名でこれらのウェブサイトに接続することができます。

[Tor](../tor.md)に接続するたびに、Torはインターネットへの経路を構築するために3つのノードを選択します。この経路は「サーキット」と呼ばれます。

<figure markdown>
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Tor path showing your device connecting to an entry node, middle node, and exit node before reaching the destination website](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Tor circuit pathway</figcaption>
</figure>

それぞれのノードには、以下の独自の機能があります。

### 入力ノード

入力ノードはしばしばガードノードと呼ばれ、Torのクライアントが最初に接続するノードです。 入力ノードはあなたのIPアドレスを見ることができますが、あなたが何に接続しているかを見ることはできません。

他のノードとは異なり、Torクライアントはランダムに入力ノードを選択した後、特定の攻撃からあなたを守るため、2～3ヶ月間そのノードを使用します。[^1]

### 中間ノード

The middle node is the second node to which your Tor client connects. It can see which node the traffic came from—the entry node—and to which node it goes to next. The middle node cannot, see your IP address or the domain you are connecting to.

For each new circuit, the middle node is randomly selected out of all available Tor nodes.

### 出口ノード

The exit node is the point in which your web traffic leaves the Tor network and is forwarded to your desired destination. The exit node is unable to see your IP address, but it does know what site it's connecting to.

The exit node will be chosen at random from all available Tor nodes ran with an exit relay flag.[^2]

## オニオン・サービスへの通路の構築

「オニオンサービス」（一般に「隠しサービス」とも呼ばれます）とは、Torブラウザでしかアクセスできないウェブサイトのことです。 These websites have a long randomly generated domain name ending with `.onion`.

Connecting to an Onion Service in Tor works very similarly to connecting to a clearnet service, but your traffic is routed through a total of **six** nodes before reaching the destination server. Just like before however, only three of these nodes are contributing to *your* anonymity, the other three nodes protect *the Onion Service's* anonymity, hiding the website's true IP and location in the same manner that Tor Browser is hiding yours.

<figure style="width:100%" markdown>
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor circuit pathway with Onion Services. Nodes in the <span class="pg-blue">blue</span> fence belong to your browser, while nodes in the <span class="pg-red">red</span> fence belong to the server, so their identity is hidden from you.</figcaption>
</figure>

## 暗号化

Torは、各パケット（送信データのブロック）を、出口ノード、中間ノード、入口ノードの鍵の順に3回暗号化します。

Torが回路を構築すると、データの伝送は以下のように行われます。

1. まず、パケットが入力ノードに到達すると、暗号化の最初のレイヤーが取り除かれます。 この暗号化されたパケットの中から、入力ノードは中間ノードのアドレスを持つ、別の暗号化されたパケットを見つけます。 入力ノードはその後、パケットを中間ノードに転送します。

2. 次に、中間ノードが入力ノードからパケットを受信すると、中間ノードもその鍵で暗号化のレイヤーを取り除き、今度は暗号化されたパケットを出口ノードのアドレスで見つけます。 中間ノードはその後、パケットを出口ノードに転送します。

3. 最後に、出口ノードがパケットを受信すると、その鍵で最後の暗号化レイヤーを削除します。 出口ノードは宛先のアドレスを確認し、そのアドレスにパケットを転送します。

以下はそのプロセスを示す別の図です。 Each node removes its own layer of encryption, and when the destination server returns data, the same process happens entirely in reverse. For example, the exit node does not know who you are, but it does know which node it came from, and so it adds its own layer of encryption and sends it back.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Sending and receiving data through the Tor Network</figcaption>
</figure>

Torを使えば、誰にも全経路を知られることなくサーバーに接続することができます。 入口ノードは、あなたが誰であるかは知っているが、どこへ行こうとしているかは知りません。中間ノードには、あなたが誰であるかも、どこへ行こうとしているかも知ることができません。出口ノードは、あなたがどこへ行こうとしているかは知っていますが、誰であるかは知りません。 最終的な接続を行うのは出口ノードであるため、接続先のサーバーが、あなたのIPアドレスを知ることは決してありません。

## 注意事項

Torはプライバシーを強力に保証していますが、Torが完璧ではないことに注意する必要があります。

- Well-funded adversaries with the capability to passively watch most network traffic over the globe have a chance of deanonymizing Tor users by means of advanced traffic analysis. Nor does Tor protect you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can also monitor traffic that passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be recorded and monitored. If such traffic contains personally identifiable information, then it can deanonymize you to that exit node. Thus, we recommend using HTTPS over Tor where possible.

If you wish to use Tor for browsing the web, we only recommend the **official** Tor Browser—it is designed to prevent fingerprinting.

- [Torブラウザー :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## その他の資料

- [Torブラウザーのユーザーマニュアル](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: The first relay in your circuit is called an "entry guard" or "guard". It is a fast and stable relay that remains the first one in your circuit for 2-3 months in order to protect against a known anonymity-breaking attack. The rest of your circuit changes with every new website you visit, and all together these relays provide the full privacy protections of Tor. For more information on how guard relays work, see this [blog post](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) and [paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) on entry guards. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Relay flag: a special (dis-)qualification of relays for circuit positions (for example, "Guard", "Exit", "BadExit"), circuit properties (for example, "Fast", "Stable"), or roles (for example, "Authority", "HSDir"), as assigned by the directory authorities and further defined in the directory protocol specification. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
