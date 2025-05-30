---
title: "通信网络类型"
icon: 'material/transit-connection-variant'
description: 即时信息应用程序常用的几种网络架构的概述。
---

有几种网络架构常用于人与人之间的信息传递。 这些网络可以提供不同的隐私保证，这就是为什么在决定使用哪种应用程序时，应该考虑你的 [威胁模型](../basics/threat-modeling.md)。

[Recommended Instant Messengers](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## 集中式网络

![集中式网络示意图](../assets/img/layout/network-centralized.svg){ align=left }

集中式通讯软件是指所有参与者都在同一服务器或由同一组织控制的服务器网络上。

一些自托管通讯软件允许您设置自己的服务器。 自托管可以提供额外的隐私保证，例如没有使用日志或对元数据（关于谁与谁交谈的数据）的访问限制。 自我托管的集中式通讯是孤立的，所有人都必须在同一个服务器上进行交流。

**优点：**

- 新的功能和更改可以更快地实施。
- 更容易开始使用和寻找联系人。
- 成熟和稳定的功能生态系统，因为它们集成于一套体系。
- 当您选择自托管服务器时，隐私问题能缓解不少。

**缺点**

- 可以包括 [访问限制和审查](https://drewdevault.com/2018/08/08/Signal.html)。 这可能包括以下内容：
- 封禁将可能提供更灵活的定制或更好的体验的[第三方客户端](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165)。 通常在使用条款和条件中定义。
- 为第三方开发者提供的文件很差或没有。
- 这项服务的[所有权](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire)，隐私政策和行为可被单个个体随意改变。可能以后会危及这项服务本身。
- 自托管需要耐心和知识。

## 联邦网络

![联邦网络示意图](../assets/img/layout/network-decentralized.svg){ align=left }

联邦网络使用多个独立的去中心化服务器，这些服务器能够相互通信（例如电子邮件）。 联邦允许系统管理员控制自己的服务器，并且仍然是更大的网络的一部分。

自托管时，联合服务器的成员可以发现其他服务器的成员并与其进行通信，尽管某些服务器可以选择通过不联邦化（例如工作团队服务器）来保持私密性。

**优点：**

- 允许在运行自己的服务器时更好地控制自己的数据。
- 允许您通过在多个“公共”服务器之间选择信任谁。
- 通常允许第三方客户端提供更原生、定制或可访问的体验。
- Server software can be verified that it matches public source code, assuming you have access to the server, or you trust the person who does (e.g., a family member).

**缺点**

- 添加新功能更加复杂，因为这些功能需要进行标准化和测试，以确保网络上的所有服务器都能一起使用。
- 由于前一点，与集中式平台相比，功能可能缺乏，不完整或以意想不到的方式工作，例如脱机或消息删除时的消息中继。
- 一些元数据可能是泄漏的（例如，像 "谁在和谁说话 "这样的信息，但如果使用E2EE，则没有实际的消息内容）。
- 通常需要信任服务器的管理员。 他们可能是业余爱好者，也可能不是“安全专业人士” ，并且可能不会提供标准文档，如隐私政策或服务条款，详细说明如何使用您的数据。
- 因为其他服务器的滥用行为或违反了公认的行为的一般规则，服务器管理员有时会选择封锁其他服务器 这会妨碍您与这些服务器的成员进行通信。

## 点对点网络

![P2P网络示意图](../assets/img/layout/network-distributed.svg){ align=left }

点对点聊天软件连接到一个由节点组成的 [分布式网络](https://en.wikipedia.org/wiki/Distributed_networking) ，在没有第三方服务器的情况下将信息转发给收件人。

客户端（对等节点）通常通过使用 [分布式网络](https://en.wikipedia.org/wiki/Distributed_computing) 找到对方。 这方面的例子包括 [分布式哈希表](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT)，由 [torrents](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) 和 [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System) 等使用。 Another approach is proximity based networks, where a connection is established over Wi-Fi or Bluetooth (for example, Briar or the [Scuttlebutt](https://scuttlebutt.nz) social network protocol).

一旦一个节点通过这些方法中的任何一种找到了通往其联系人的路线，它们之间就会建立直接连接。 虽然信息通常是加密的，但观察者仍然可以推断出发件人和收件人的位置和身份。

P2P网络不使用服务器，因为节点之间直接通信，因此不存在自我托管。 不过，一些附加服务可能依赖于集中式服务器，例如用户发现或中继离线消息，自托管对此仍有帮助。

**优点：**

- 很小的第三方暴露。
- 现代P2P平台默认端对端加密。 与集中式和联邦式模式不同，没有任何服务器可能会拦截和解密你的信息。

**缺点**

- 缺少很多特性：
- 消息只有在两个节点都在线时才能发送，然而，你的客户端可以将消息存储在本地，以等待联系人重新上线。
- 通常会增加移动设备的电池用量，因为客户端必须保持与分布式网络的连接，以了解联系人的在线情况。
- 某些常见的Messenger功能可能没有实现或不完整，例如消息删除。
- 如果你不与 [VPN](../vpn.md) 或 [Tor](../tor.md)结合使用该软件，你的IP地址和与你通信的联系人的IP地址可能会被暴露。 许多国家都有某种形式的大规模监控或元数据保留。

## 匿名路由

![匿名网络示意图](../assets/img/layout/network-anonymous-routing.svg){ align=left }

使用 [匿名路由](https://doi.org/10.1007/978-1-4419-5906-5_628) 的Messenger隐藏发送方、接收方的身份或他们一直在通信的证据。 理想情况下，Messenger应该将这三者都隐藏起来。

There are [many](https://doi.org/10.1145/3182658) ways to implement anonymous routing. 其中最著名的是
洋葱路由 （即 [Tor](tor-overview.md)），它通过一个强加密的 [覆盖网络](https://en.wikipedia.org/wiki/Overlay_network) ，隐藏每个节点的位置以及每个信息的接收者和发送者来通信。 发件人和收件人从不直接交互，只通过一个秘密的会合节点会面，这样就不会泄露IP地址或物理位置。 节点不能解密信息，也不能解密最终目的地；只有收件人可以。 每个中间节点只能解密一部分，表明下一步将把仍然加密的信息发送到哪里，直到它到达可以完全解密的收件人那里，因此命名为 "洋葱路由"。</p> 

Self-hosting a node in an anonymous routing network does not provide the host with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**优点：**

- 最小第三方暴露。
- 消息可以以去中心的方式中继，即使其中一方处于离线状态。

**缺点**

- 慢
- 通常仅限于较少的媒体类型，主要是文本，因为很慢。
- 如果通过随机路由选择节点，则某些节点可能远离发送方和接收方，增加延迟，甚至在其中一个节点脱机时无法传输消息。
- 开始时比较复杂，因为需要创建和安全备份一个加密私钥。
- 就像其他去中心化平台一样，对开发者来说，增加功能比中心化平台更复杂。 因此，功能可能缺乏或未完全实现，例如脱机消息中继或消息删除。
