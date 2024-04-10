---
title: "Обзор Tor"
icon: 'simple/torproject'
description: Tor - это бесплатная в использовании децентрализованная сеть, разработанная для использования интернета с максимально возможной степенью конфиденциальности.
---

![Логотип Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) is a free to use, decentralized network designed for using the internet with as much privacy as possible. При правильном использовании сеть позволяет осуществлять частный и анонимный браузинг и общение. Поскольку трафик Tor сложно заблокировать и отследить, Tor является эффективным инструментом обхода цензуры.

Tor works by routing your internet traffic through volunteer-operated servers, instead of making a direct connection to the site you're trying to visit. Это скрывает, откуда идет трафик, и ни один сервер на пути соединения не может увидеть полный путь того, откуда и куда идет трафик, то есть даже серверы, которые ты используешь для подключения, не могут нарушить твою анонимность.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

## Safely Connecting to Tor

Before connecting to Tor, you should carefully consider what you're looking to accomplish by using Tor in the first place, and who you're trying to hide your network activity from.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [de-stigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

If you have the ability to access a trusted VPN provider and **any** of the following are true, you almost certainly should connect to Tor through a VPN:

- You already use a [trusted VPN provider](../vpn.md)
- Your threat model includes an adversary which is capable of extracting information from your ISP
- Your threat model includes your ISP itself as an adversary
- Your threat model includes local network administrators before your ISP as an adversary

Because we already [generally recommend](../basics/vpn-overview.md) that the vast majority of people use a trusted VPN provider for a variety of reasons, the following recommendation about connecting to Tor via a VPN likely applies to you. <mark>There is no need to disable your VPN before connecting to Tor</mark>, as some online resources would lead you to believe.

Connecting directly to Tor will make your connection stand out to any local network administrators or your ISP. Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) in the past by network administrators to identify and deanonymize specific Tor users on their network. On the other hand, connecting to a VPN is almost always less suspicious, because commercial VPN providers are used by everyday consumers for a variety of mundane tasks like bypassing geo-restrictions, even in countries with heavy internet restrictions.

Therefore, you should make an effort to hide your IP address **before** connecting to the Tor network. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal, through Tor Browser for example. This creates a connection chain like:

- [x] You → VPN → Tor → Internet

From your ISP's perspective, it looks like you're accessing a VPN normally (with the associated cover that provides you). From your VPN's perspective, they can see that you are connecting to the Tor network, but nothing about what websites you're accessing. From Tor's perspective, you're connecting normally, but in the unlikely event of some sort of Tor network compromise, only your VPN's IP would be exposed, and your VPN would *additionally* have to be compromised to deanonymize you.

This is **not** censorship circumvention advice, because if Tor is blocked entirely by your ISP, your VPN likely is as well. Rather, this recommendation aims to make your traffic blend in better with commonplace VPN user traffic, and provide you with some level of plausible deniability by obscuring the fact that you're connecting to Tor from your ISP.

---

We **very strongly discourage** combining Tor with a VPN in any other manner. Do not configure your connection in a way which resembles any of the following:

- You → Tor → VPN → Internet
- You → VPN → Tor → VPN → Internet
- Any other configuration

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (exit nodes being blocked by websites) in some places. [Normally](https://support.torproject.org/#about_change-paths), Tor frequently changes your circuit path through the network. When you choose a permanent *destination* VPN (connecting to a VPN server *after* Tor), you're eliminating this advantage and drastically harming your anonymity.

Setting up bad configurations like these is difficult to do accidentally, because it usually involves either setting up custom proxy settings inside Tor Browser, or setting up custom proxy settings inside your VPN client which routes your VPN traffic through the Tor Browser. As long as you avoid these non-default configurations, you're probably fine.

---

<div class="admonition info" markdown>
<p class="admonition-title">VPN/SSH Fingerprinting</p>

The Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) that *theoretically* using a VPN to hide Tor activities from your ISP may not be foolproof. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited, because all websites have specific traffic patterns.

Therefore, it's not unreasonable to believe that encrypted Tor traffic hidden by a VPN could also be detected via similar methods. There are no research papers on this subject, and we still consider the benefits of using a VPN to far outweigh these risks, but it is something to keep in mind.

If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

</div>

Determining whether you should first use a VPN to connect to the Tor network will require some common sense and knowledge of your own government's and ISP's policies relating to what you're connecting to. However, again in most cases you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g. Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## What Tor is Not

The Tor network is not the perfect privacy protection tool in all cases, and has a number of drawbacks which should be carefully considered. These things should not discourage you from using Tor if it is appropriate for your needs, but they are still things to think about when deciding which solution is most appropriate for you.

### Tor is not a free VPN

The release of the *Orbot* mobile app has lead many people to describe Tor as a "free VPN" for all of your device traffic. However, treating Tor like this poses some dangers compared to a typical VPN.

Unlike Tor exit nodes, VPN providers are usually not *actively* [malicious](#caveats). Because Tor exit nodes can be created by anybody, they are hotspots for network logging and modification. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

**Even if you use bridges and pluggable transports,** the Tor Project provides no tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect, they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (the same bugs are present across all Tor Browser users). As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure VM and protect against leaks.

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

Подключение к сервису Onion в Tor работает аналогично подключению к сервису clearnet, но ваш трафик проходит в общей сложности через **шесть узлов**, прежде чем достигнет сервера назначения. Однако, как и раньше, только три из этих узлов способствуют *вашей* анонимности, остальные три узла защищают анонимность *сервисов Onion*, скрывая истинный IP и местоположение сайта так же, как Tor Browser скрывает ваш.

<figure style="width:100%" markdown>
  ![Путь Tor, показывающий, что ваш трафик направляется через три ваших Tor-узла плюс три дополнительных Tor-узла, скрывающих идентичность сайта](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Путь Tor, показывающий, что ваш трафик направляется через три ваших Tor-узла плюс три дополнительных Tor-узла, скрывающих идентичность веб-сайта](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Путь цепи Tor с  сервисами Onion. Узлы в <span class="pg-blue">синем</span> квадрате принадлежат вашему браузеру, а узлы в <span class="pg-red">красном</span> квадрате принадлежат серверу, поэтому их идентичность скрыта от вас.</figcaption>
</figure>

## Шифрование

Tor шифрует каждый пакет (блок передаваемых данных) три раза с помощью ключей от выходного, среднего и входного узла - именно в таком порядке.

После того как Tor построил цепь, передача данных осуществляется следующим образом:

1. Во-первых: когда пакет поступает на входной узел, первый уровень шифрования снимается. В этом зашифрованном пакете входной узел найдет другой зашифрованный пакет с адресом среднего узла. Затем входной узел пересылает пакет среднему узлу.

2. Во-вторых: когда средний узел получает пакет от входного узла, он тоже снимает слой шифрования своим ключом, и на этот раз находит зашифрованный пакет с адресом выходного узла. Затем средний узел пересылает пакет на выходной узел.

3. И последнее: когда выходной узел получает свой пакет, он удаляет последний уровень шифрования своим ключом. Выходной узел увидит адрес назначения и перешлет пакет на этот адрес.

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

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Дополнительные советы

- [Руководство пользователя Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Первый ретранслятор в вашей цепи называется "входным" или "охранным". Это быстрый и стабильный ретранслятор, который остается первым в вашей цепи в течение 2-3 месяцев для защиты от известной атаки, нарушающей анонимность. Остальная часть цепи меняется с каждым новым посещаемым сайтом, и все вместе эти реле обеспечивают полную защиту конфиденциальности Tor. Более подробную информацию о том, как работают охранные ретрансляторы, можно найти в этом [посте в блоге](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) и [документе](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) о входных узлах. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2))

[^2]: Флаг ретраслятора: специальная (дис)квалификация реле для позиций цепи (например, "Guard", "Exit", "BadExit"), свойств цепи (например, "Fast", "Stable") или ролей (например, "Authority", "HSDir"), назначаемых владельцами директории и далее определенных в спецификации протокола директории. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
