---
title: "Обзор Tor"
icon: 'simple/torproject'
description: Tor - это бесплатная в использовании децентрализованная сеть, разработанная для использования интернета с максимально возможной степенью конфиденциальности.
---

![Логотип Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) — это бесплатная для использования, децентрализованная сеть, предназначенная для максимально приватного использования интернета. При правильном использовании сеть позволяет осуществлять частный и анонимный браузинг и общение. Поскольку трафик Tor сложно заблокировать и отследить, Tor является эффективным инструментом обхода цензуры.

[:material-movie-open-play-outline: Видео: Почему тебе нужен Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

Tor работает, направляя твой интернет-трафик через серверы, управляемые волонтёрами, вместо прямого подключения к сайту, который ты пытаешься посетить. Это скрывает, откуда идет трафик, и ни один сервер на пути соединения не может увидеть полный путь того, откуда и куда идет трафик, то есть даже серверы, которые ты используешь для подключения, не могут нарушить твою анонимность.

[:octicons-home-16:](https://torproject.org){ .card-link title=Домашняя страница }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Документация}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Внести вклад }

## Безопасное подключение к Tor

Прежде чем подключаться к Tor, следует тщательно обдумать, чего ты хочешь достичь, используя Tor, и от кого ты пытаешься скрыть свою сетевую активность.

Если ты живешь в свободной стране, получаешь доступ к обычному контенту через Tor, не беспокоишься о том, что твой интернет-провайдер или администраторы локальной сети будут знать о том, что ты используешь Tor, и хочешь помочь [дестигматизировать](https://2019.www.torproject.org/about/torusers.html.en)использование Tor, ты, вероятно, можешь подключиться к Tor напрямую через стандартные средства, такие как [Tor Browser](../tor.md), без беспокойства.

Если у тебя есть возможность получить доступ к надежному VPN-провайдеру и **любое** из следующего верно, ты почти наверняка должен подключаться к Tor через VPN:

- Ты уже используешь [доверенного VPN-провайдера](../vpn.md)
- Твоя модель угроз включает противника, способного извлекать информацию у твоего интернет-провайдера
- Твоя модель угроз включает самого интернет-провайдера как противника
- Твоя модель угроз включает локальных сетевых администраторов перед твоим интернет-провайдером как противников

Поскольку мы уже [в целом рекомендуем](../basics/vpn-overview.md), чтобы подавляющее большинство людей использовало доверенного VPN-провайдера по ряду причин, следующая рекомендация о подключении к Tor через VPN, вероятно, относится к тебе. <mark>Нет необходимости отключать твой VPN перед подключением к Tor</mark>, как могут заставить тебя поверить некоторые онлайн-ресурсы.

Прямое подключение к Tor заставит твое соединение выделяться для любых локальных сетевых администраторов или твоего интернет-провайдера. Обнаружение и корреляция этого трафика [проводились](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) в прошлом сетевыми администраторами для идентификации и деанонимизации конкретных пользователей Tor в их сети. С другой стороны, подключение к VPN почти всегда менее подозрительно, поскольку коммерческие VPN-провайдеры используются обычными потребителями для различных повседневных задач, таких как обход географических ограничений, даже в странах с серьезными ограничениями интернета.

Поэтому ты должен приложить усилия, чтобы скрыть свой IP-адрес **до** подключения к сети Tor. Ты можешь сделать это, просто подключившись к VPN (через клиент, установленный на твоем компьютере), а затем получив доступ к [Tor](../tor.md) как обычно (например, через Tor Browser). Это создает цепочку соединений следующим образом:

- [x] Ты → VPN → Tor → Интернет

С точки зрения твоего интернет-провайдера, кажется, что ты нормально используешь VPN (с соответствующим прикрытием, которое это тебе обеспечивает). С точки зрения твоего VPN, они могут видеть, что ты подключаешься к сети Tor, но ничего о том, какие веб-сайты ты посещаешь. С точки зрения Tor, ты подключаешься нормально, но в маловероятном случае какого-либо компрометации сети Tor, будет раскрыт только IP-адрес твоего VPN, и твой VPN должен быть *дополнительно* скомпрометирован, чтобы деанонимизировать тебя.

Это **не** совет по обходу цензуры, потому что если Tor полностью заблокирован твоим интернет-провайдером, твой VPN, вероятно, тоже заблокирован. Скорее, эта рекомендация направлена на то, чтобы твой трафик лучше сливался с обычным трафиком пользователей VPN, и обеспечивал тебе некоторый уровень правдоподобного отрицания, скрывая факт подключения к Tor от твоего интернет-провайдера.

---

Мы **очень настоятельно не рекомендуем** комбинировать Tor с VPN каким-либо другим способом. Не настраивай свое соединение так, чтобы оно напоминало любое из следующих:

- Ты → Tor → VPN → Интернет
- Ты → VPN → Tor → VPN → Интернет
- Любая другая конфигурация

Некоторые VPN-провайдеры и другие публикации иногда рекомендуют эти **плохие** конфигурации для обхода запретов Tor (т.е. блокировки выходных узлов веб-сайтами) в некоторых местах. [Обычно](https://support.torproject.org/#about_change-paths) Tor часто меняет путь твоего соединения через сеть. Выбирая VPN с постоянным *назначением* (подключение к VPN-серверу *после* Tor), ты лишаешь себя этого преимущества и значительно ухудшаешь свою анонимность.

Настроить подобные конфигурации случайно очень сложно, так как это обычно связано либо с настройкой пользовательских параметров прокси в Tor Browser, либо с настройкой пользовательских параметров прокси в твоём VPN-клиенте, который направляет твой VPN-трафик через Tor Browser. Пока ты избегаешь этих нестандартных конфигураций, ты, вероятно, в порядке.

---

<div class="admonition info" markdown>
<p class="admonition-title">VPN/SSH Фингерпринтинг</p>

Проект Tor [отмечает](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting), что *теоретически* использование VPN для скрытия активности Tor от твоего интернет-провайдера может быть не безупречным. VPN оказались уязвимыми для фингерпринтинга веб-трафика, когда противник все ещё может угадать, какой веб-сайт посещается, потому что все веб-сайты имеют определенные схемы трафика.

Поэтому не является необоснованным предположение, что зашифрованный трафик Tor, скрытый VPN, также может быть обнаружен с помощью аналогичных методов. По этой теме нет исследовательских работ, и мы все еще считаем, что преимущества использования VPN значительно перевешивают эти риски, но это то, о чём стоит помнить.

Если ты по-прежнему считаешь, что подключаемые транспортные протоколы (мосты) обеспечивают дополнительную защиту от отслеживания трафика веб-сайтов, которой не обладает VPN, у тебя всегда есть возможность использовать мост **и** VPN одновременно.

</div>

Определение того, следует ли тебе сначала использовать VPN для подключения к сети Tor, потребует некоторого здравого смысла и знания политики твоего собственного правительства и интернет-провайдера в отношении того, к чему ты подключаешься. Повторим, однако, что в большинстве случаев лучше быть замеченным в подключении к коммерческой сети VPN, чем напрямую к сети Tor. Если VPN-провайдеры подвергаются цензуре в твоем регионе, ты также можешь рассмотреть возможность использования подключаемых транспортов Tor (например, мостов Snowflake или meek) в качестве альтернативы, но использование этих мостов может вызвать больше подозрений, чем стандартные туннели WireGuard/OpenVPN.

## Чем Tor не является

Сеть Tor не является идеальным инструментом защиты конфиденциальности во всех случаях и имеет ряд недостатков, которые следует тщательно учитывать. Эти вещи не должны отговаривать тебя от использования Tor, если это соответствует твоим потребностям, но это всё же вещи, о которых стоит подумать при выборе наиболее подходящего решения для тебя.

### Tor — это не бесплатный VPN

Выпуск мобильного приложения *Orbot* привел к тому, что многие люди стали описывать Tor как "бесплатный VPN" для всего трафика твоего устройства. However, treating Tor like this poses some dangers compared to a typical VPN.

Unlike Tor exit nodes, VPN providers are usually not *actively* [malicious](#caveats). Because Tor exit nodes can be created by anybody, they are hotspots for network logging and modification. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs. As such, using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project doesn't provide any tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect—they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (e.g., the same bugs are present across all Tor Browser users). As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure virtual machine and protect against leaks.

## Построение пути к сервисам Clearnet

"Сервисы Clearnet" - это веб-сайты, доступ к которым можно получить с помощью любого браузера, например [privacyguides.org](https://www.privacyguides.org). Tor позволяет вам анонимно подключаться к этим сайтам, направляя ваш трафик через сеть, состоящую из тысяч, управляемых волонтёрами, серверов, которые называются узлами (или ретрансляторами).

Каждый раз, когда вы [подключаетесь к Tor](../tor.md), он выбирает три узла для построения пути в интернет - этот путь называется "цепь."

<figure markdown>
  ![Путь Tor, показывающий подключение вашего устройства к узлу входа, среднему узлу и узлу выхода до достижения целевого сайта](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Путь Tor, показывающий подключение вашего устройства к узлу входа, среднему узлу и узлу выхода до достижения целевого сайта](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Путь Tor</figcaption>
</figure>

Каждый из этих узлов имеет свою функцию:

### Входной узел

Входной узел, часто называемый сторожевым узлом, является первым узлом, к которому подключается ваш клиент Tor. Входной узел может видеть ваш IP-адрес, однако он не может видеть, к чему вы подключаетесь.

В отличие от других узлов, клиент Tor будет случайным образом выбирать входной узел и придерживаться его в течение двух-трех месяцев, чтобы защитить вас от определенных атак.[^1]

### Средний узел

Средний узел - это второй узел, к которому подключается ваш клиент Tor. Он может видеть, с какого узла пришел трафик (входного узла) и к какому узлу он идет дальше. Средний узел не может видеть ваш IP-адрес или домен, к которому вы подключаетесь.

Для каждой новой цепи средний узел выбирается случайным образом из всех доступных узлов Tor.

### Выходной узел

Выходной узел - это точка, в которой ваш веб-трафик покидает сеть Tor и перенаправляется в нужное вам место назначения. Выходной узел не может видеть ваш IP-адрес, но он знает, к какому сайту подключается.

Выходной узел  будет выбран случайным образом из всех доступных узлов Tor, запущенных с флагом ретрансляции выхода.[^2]

## Построение пути к сервисам Onion

"Сервисы Onion" (также часто называемые "скрытыми сервисами") - это веб-сайты, доступ к которым возможен только через браузер Tor. Эти сайты имеют длинное случайно сгенерированное доменное имя, заканчивающееся на `.onion`.

Подключение к сервису Onion в Tor работает аналогично подключению к сервису clearnet, но ваш трафик проходит в общей сложности через **шесть узлов**, прежде чем достигнет сервера назначения. Just like before, however, only three of these nodes are contributing to *your* anonymity, the other three nodes protect *the Onion Service's* anonymity, hiding the website's true IP and location in the same manner that Tor Browser is hiding yours.

<figure style="width:100%" markdown>
  ![Путь Tor, показывающий, что ваш трафик направляется через три ваших Tor-узла плюс три дополнительных Tor-узла, скрывающих идентичность сайта](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Путь Tor, показывающий, что ваш трафик направляется через три ваших Tor-узла плюс три дополнительных Tor-узла, скрывающих идентичность веб-сайта](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Путь цепи Tor с  сервисами Onion. Узлы в <span class="pg-blue">синем</span> квадрате принадлежат вашему браузеру, а узлы в <span class="pg-red">красном</span> квадрате принадлежат серверу, поэтому их идентичность скрыта от вас.</figcaption>
</figure>

## Шифрование

Tor encrypts each packet (a block of transmitted data) three times with the keys from the exit, middle, and entry node in that order.

После того как Tor построил цепь, передача данных осуществляется следующим образом:

1. Firstly: When the packet arrives at the entry node, the first layer of encryption is removed. В этом зашифрованном пакете входной узел найдет другой зашифрованный пакет с адресом среднего узла. Затем входной узел пересылает пакет среднему узлу.

2. Secondly: When the middle node receives the packet from the entry node, it too will remove a layer of encryption with its key, and this time finds an encrypted packet with the exit node's address. Затем средний узел пересылает пакет на выходной узел.

3. Lastly: When the exit node receives its packet, it will remove the last layer of encryption with its key. Выходной узел увидит адрес назначения и перешлет пакет на этот адрес.

Ниже приведена альтернативная диаграмма, показывающая этот процесс. Каждый узел снимает свой собственный уровень шифрования, а когда сервер назначения возвращает данные, тот же процесс происходит полностью в обратном порядке. Например, выходной узел не знает, кто вы, но он знает, с какого узла пришло сообщение, поэтому он добавляет свой собственный уровень шифрования и отправляет его обратно.

<figure markdown>
  ![Шифрование Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Шифрование Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Отправка и получение данных через сеть Tor</figcaption>
</figure>

Tor позволяет нам подключаться к серверу так, чтобы никто не знал всего пути. Входной узел знает, кто вы, но не знает, куда вы идете; средний узел не знает, кто вы и куда вы идете; а выходной узел знает, куда вы идете, но не знает, кто вы. Поскольку конечный узел устанавливает окончательное соединение, сервер назначения никогда не узнает ваш IP-адрес.

## Предостережения

Хотя Tor обеспечивает надежные гарантии конфиденциальности, следует помнить, что Tor не совершенен:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- Выходные узлы Tor также могут отслеживать проходящий через них трафик. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

Если вы хотите использовать Tor для просмотра веб-страниц, мы рекомендуем только **официальный ** Tor Browser - он разработан для предотвращения цифровых отпечатков.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges; they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges—you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Дополнительные советы

- [Руководство пользователя Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: Первый ретранслятор в вашей цепи называется "входным" или "охранным". Это быстрый и стабильный ретранслятор, который остается первым в вашей цепи в течение 2-3 месяцев для защиты от известной атаки, нарушающей анонимность. Остальная часть цепи меняется с каждым новым посещаемым сайтом, и все вместе эти реле обеспечивают полную защиту конфиденциальности Tor. Более подробную информацию о том, как работают охранные ретрансляторы, можно найти в этом [посте в блоге](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) и [документе](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) о входных узлах. ([https://support.torproject.org/tbb/tbb-2](https://support.torproject.org/tbb/tbb-2))

[^2]: Флаг ретраслятора: специальная (дис)квалификация реле для позиций цепи (например, "Guard", "Exit", "BadExit"), свойств цепи (например, "Fast", "Stable") или ролей (например, "Authority", "HSDir"), назначаемых владельцами директории и далее определенных в спецификации протокола директории. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html#relay-flag))
