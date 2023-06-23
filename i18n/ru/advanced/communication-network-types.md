---
title: "Типы коммуникационных сетей"
icon: 'material/transit-connection-variant'
description: Обзор нескольких сетевых архитектур, обычно используемых приложениями для обмена мгновенными сообщениями.
---

Существует несколько сетевых архитектур, обычно используемых для передачи сообщений между людьми. Эти сети могут предоставлять разные гарантии конфиденциальности, поэтому при принятии решения о том, какое приложение использовать, стоит учитывать вашу [модель угроз](../basics/threat-modeling.md).

[Рекомендуемые мессенджеры](../real-time-communication.md ""){.md-button}

## Централизованные сети

![Схема централизованных сетей](../assets/img/layout/network-centralized.svg){ align=left }

Централизованные мессенджеры - это те, где все участники находятся на одном сервере или сети серверов, контролируемых одной организацией.

Некоторые мессенджеры позволяют настроить собственный сервер. Самостоятельный хостинг может обеспечить дополнительные гарантии конфиденциальности, например, отсутствие журналов использования или ограниченный доступ к метаданным (данные о том, кто с кем разговаривает). При самостоятельном хостинге централизованные мессенджеры изолированы, и для общения все должны находиться на одном сервере.

**Преимущества:**

- Новые функции и изменения могут быть внедрены быстрее.
- Легче начать использовать и найти контакты.
- Наиболее проверенные и стабильные функции экосистем, так как их легче программировать в централизованном программном обеспечении.
- Проблемы конфиденциальности могут быть снижены, если вы доверяете серверу, который вы самостоятельно размещаете.

**Недостатки:**

- Может включать [ограниченный контроль или доступ](https://drewdevault.com/2018/08/08/Signal.html). Это может включать в себя такие вещи, как:
- [Запрет на подключение сторонних клиентов](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) к централизованной сети, которые могли бы обеспечить большую персонализацию или лучший опыт. Это часто написано в условиях использования.
- Плохая документация для сторонних разработчиков или ее полное отсутствие.
- [Руководство](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire/), политика конфиденциальности и операции сервиса могут легко измениться, если его контролирует одна организация, что впоследствии может поставить сервис под угрозу.
- Самостоятельный хостинг требует усилий и знаний о том, как настроить сервис.

## Федеративные сети

![Схема федеративных сетей](../assets/img/layout/network-decentralized.svg){ align=left }

Федеративные мессенджеры используют несколько независимых, децентрализованных серверов, которые могут общаться друг с другом (электронная почта является одним из примеров федеративной службы). Федерация позволяет системным администраторам контролировать свой собственный сервер и при этом быть частью большой коммуникационной сети.

При самостоятельном хостинге участники объединенного сервера могут обнаруживать и общаться с участниками других серверов, хотя некоторые серверы могут предпочесть оставаться закрытыми, не будучи объединенными (например, сервер рабочей группы).

**Преимущества:**

- Позволяют получить больший контроль над собственными данными при работе на собственном сервере.
- Позволяют выбирать, кому доверять свои данные, выбирая между несколькими "публичными" серверами.
- Часто позволяют использовать сторонние клиенты, которые могут обеспечить более нативный, индивидуальный или доступный опыт использования.
- Программное обеспечение сервера может быть проверено на соответствие публичному исходному коду, если у вас есть доступ к серверу или вы доверяете человеку, который имеет такой доступ (например, члену семьи).

**Недостатки:**

- Добавление новых функций является более сложной задачей, поскольку эти функции должны быть стандартизированы и протестированы для обеспечения их работы со всеми серверами в сети.
- В связи с предыдущим пунктом, функции могут отсутствовать, быть неполными или работать неожиданным образом по сравнению с централизованными платформами, например, передача сообщений в автономном режиме или удаление сообщений.
- Некоторые метаданные могут быть доступны (например, информация "кто с кем разговаривает", но не фактическое содержание сообщения, если используется E2EE).
- Федеративные серверы обычно требуют доверия к администратору вашего сервера. Они могут быть любителями или не являться "профессионалами в области безопасности" и не предоставлять стандартные документы, такие как политика конфиденциальности или условия предоставления услуг, в которых подробно описывается, как используются ваши данные.
- Администраторы серверов иногда решают блокировать другие серверы, которые являются источником немодерируемых злоупотреблений или нарушают правила общепринятого поведения. Это затруднит вашу возможность общаться с участниками этих серверов.

## Пиринговые сети

![Схема P2P](../assets/img/layout/network-distributed.svg){ align=left }

P2P messengers connect to a [distributed network](https://en.wikipedia.org/wiki/Distributed_networking) of nodes to relay a message to the recipient without a third-party server.

Clients (peers) usually find each other through the use of a [distributed computing](https://en.wikipedia.org/wiki/Distributed_computing) network. Examples of this include [Distributed Hash Tables](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT), used by [torrents](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) and [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System) for example. Another approach is proximity based networks, where a connection is established over WiFi or Bluetooth (for example, Briar or the [Scuttlebutt](https://www.scuttlebutt.nz) social network protocol).

Once a peer has found a route to its contact via any of these methods, a direct connection between them is made. Although messages are usually encrypted, an observer can still deduce the location and identity of the sender and recipient.

P2P networks do not use servers, as peers communicate directly between each other and hence cannot be self-hosted. However, some additional services may rely on centralized servers, such as user discovery or relaying offline messages, which can benefit from self-hosting.

**Преимущества:**

- Minimal information is exposed to third-parties.
- Modern P2P platforms implement E2EE by default. There are no servers that could potentially intercept and decrypt your transmissions, unlike centralized and federated models.

**Недостатки:**

- Reduced feature set:
- Messages can only be sent when both peers are online, however, your client may store messages locally to wait for the contact to return online.
- Generally increases battery usage on mobile devices, because the client must stay connected to the distributed network to learn about who is online.
- Some common messenger features may not be implemented or incompletely, such as message deletion.
- Your IP address and that of the contacts you're communicating with may be exposed if you do not use the software in conjunction with a [VPN](../vpn.md) or [Tor](../tor.md). Many countries have some form of mass surveillance and/or metadata retention.

## Анонимная маршрутизация

![Схема анонимной маршрутизации](../assets/img/layout/network-anonymous-routing.svg){ align=left }

A messenger using [anonymous routing](https://doi.org/10.1007/978-1-4419-5906-5_628) hides either the identity of the sender, the receiver, or evidence that they have been communicating. Ideally, a messenger should hide all three.

There are [many](https://doi.org/10.1145/3182658) different ways to implement anonymous routing. One of the most famous is [onion routing](https://en.wikipedia.org/wiki/Onion_routing) (i.e. [Tor](tor-overview.md)), which communicates encrypted messages through a virtual [overlay network](https://en.wikipedia.org/wiki/Overlay_network) that hides the location of each node as well as the recipient and sender of each message. The sender and recipient never interact directly and only meet through a secret rendezvous node so that there is no leak of IP addresses nor physical location. Nodes cannot decrypt messages, nor the final destination; only the recipient can. Each intermediary node can only decrypt a part that indicates where to send the still encrypted message next, until it arrives at the recipient who can fully decrypt it, hence the "onion layers."

Self-hosting a node in an anonymous routing network does not provide the hoster with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**Преимущества:**

- Minimal to no information is exposed to other parties.
- Messages can be relayed in a decentralized manner even if one of the parties is offline.

**Недостатки:**

- Slow message propagation.
- Often limited to fewer media types, mostly text, since the network is slow.
- Less reliable if nodes are selected by randomized routing, some nodes may be very far from the sender and receiver, adding latency or even failing to transmit messages if one of the nodes goes offline.
- More complex to get started, as the creation and secured backup of a cryptographic private key is required.
- Just like other decentralized platforms, adding features is more complex for developers than on a centralized platform. Hence, features may be lacking or incompletely implemented, such as offline message relaying or message deletion.
