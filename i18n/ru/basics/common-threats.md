---
title: "Распространённые угрозы"
icon: 'material/eye-outline'
description: Модель угрозы уникальна для каждого, но здесь описаны некоторые из тех вещей, которые волнуют многих посетителей этого сайта.
---

В широком смысле мы разделяем наши рекомендации по категориям [угроз](threat-modeling.md) или целей, которые применимы к большинству людей. ==Вас может волновать одна, несколько, все эти возможности или они могут не волновать вас вовсе==, и инструменты и услуги, которые вы используете, зависят от ваших целей. У тебя могут быть специфичные угрозы, не относящиеся к этим категориям, что определённо нормально! Важной частью является развитие понимания преимуществ и недостатков инструментов, которые ты решил использовать, потому что ни один из них не защитит тебя от всех угроз.

- <span class="pg-purple">:material-incognito: Анонимность</span> - изоляция твоей деятельности в интернете от твоей настоящей личности, защита тебя от людей, пытающихся раскрыть *именно твою* личность.
- <span class="pg-red">:material-target-account: Таргетированные атаки</span> - защита от хакеров и других злоумышленников, которые пытаются получить доступ к *именно твоим* данным и устройствам.
- <span class="pg-orange">:material-bug-outline: Пассивные атаки</span> - защита от таких вещей, как вредоносное ПО, утечка данных и других атак, которые совершаются одновременно против многих людей.
- <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> - A vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.
- <span class="pg-teal">:material-server-network: Поставщики услуг</span> - защита твоих данных от поставщиков услуг (например, с помощью E2EE, которое делает твои данные нечитаемыми для сервера).
- <span class="pg-blue">:material-eye-outline: Массовая слежка</span> - защита от правительственных агентств, организаций, веб-сайтов и служб, которые совместно отслеживают твою активность.
- <span class="pg-brown">:material-account-cash: Капитализм слежки</span> - Защита от крупных рекламных сетей, таких как Google и Facebook, а также от множества других сторонних сборщиков данных.
- <span class="pg-green">:material-account-search: Публичная экспозиция</span> - ограничение информации о вас, которая доступна онлайн поисковым системам или широкой общественности.
- <span class="pg-blue-gray">:material-close-outline: Цензура</span> - избегание цензуры как для доступа к информации, так и для её создания онлайн.

В зависимости от твоих конкретных ситуаций, некоторые угрозы могут быть более важные, чем другие. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Аналогичным образом, многие люди могут быть в первую очередь обеспокоены <span class="pg-green">:material-account-search: публичной экспозицией</span> своих личных данных, но им все равно следует опасаться проблем, связанных с безопасностью, таких как <span class="pg-orange">:material-bug-outline: пассивные атаки</span> - например, вредоносных программ, воздействующих на их устройства.

## Анонимность и Конфиденциальность

<span class="pg-purple">:material-incognito: Анонимность</span>

Анонимность часто путают с конфиденциальностью, но это разные понятия. В то время как конфиденциальность - это набор решений, которые вы принимаете относительно того, как ваши данные используются и передаются, анонимность - это полное отделение вашей деятельности в Интернете от вашей реальной личности.

Например, инсайдеры и журналисты могут иметь гораздо более экстремальную модель угрозы, которая требует полной анонимности. Это не только сокрытие того, чем они занимаются, какими данными располагают, чтобы не быть взломанными злоумышленниками или правительством, но и полное сокрытие того, кто они, на самом деле, такие. Они часто будут жертвовать любыми удобствами, если это означает защиту их анонимности, конфиденциальности или безопасности, потому что от этого может зависеть их жизнь. Большинству людей не нужно заходить так далеко.

## Безопасность и Конфиденциальность

<span class="pg-orange">:material-bug-outline: Пассивные атаки</span>

Безопасность и конфиденциальность также часто путают, поскольку для получения хоть какого-то подобия конфиденциальности необходима безопасность: использование инструментов - даже если они приватны по своей конструкции - бесполезно, если они могут быть легко использованы злоумышленниками, которые впоследствии обнародуют ваши данные. Однако обратное не всегда верно: самый защищенный в мире сервис *необязательно* приватный. Лучшим примером этого является передача данных компании Google, у которой, учитывая ее масштабы, было мало инцидентов, связанных с безопасностью, за счёт привлечения экспертов по безопасности, лидирующих в данной отрасли, для защиты своей инфраструктуры. Несмотря на то, что Google предоставляет очень безопасные услуги, очень немногие люди сочтут свои данные конфиденциальными в бесплатных продуктах Google (Gmail, YouTube и т. д.)

Когда речь идет о безопасности приложений, мы обычно не знаем (а иногда и не можем знать), является ли используемое нами программное обеспечение вредоносным или может ли оно однажды стать таковым. Даже у самых надежных разработчиков, как правило, нет гарантии, что их программное обеспечение не имеет серьезной уязвимости, которая впоследствии может быть использована.

Чтобы минимизировать возможный ущерб, которое *может* причинить вредоносное ПО, следует использовать защиту путём разделения. К примеру, это может выражаться в использовании разных компьютеров для разных задач, использовании виртуальных машин для разделения различных групп связанных приложений или использовании безопасной операционной системы с сильным акцентом на "песочницу" приложений и обязательный контроль доступа.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Мобильные операционные системы, как правило, имеют лучшую "песочницу" для приложений, чем настольные операционные системы: приложения не могут получить root-доступ и требуют разрешения на доступ к системным ресурсам.

Настольные операционные системы, как правило, отстают по части надлежащей "песочницы". ChromeOS имеет возможности "песочницы", аналогичные Android, а macOS имеет полный контроль системных разрешений (и разработчики могут отказаться от "песочницы" для приложений). Однако эти операционные системы передают идентифицирующую информацию своим соответствующим OEM-производителям. Linux, как правило, не предоставляет информацию поставщикам систем, но имеет слабую защиту от эксплойтов и вредоносных приложений. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

<span class="pg-red">:material-target-account: Целевые атаки</span>

С целенаправленными атаками на конкретного человека бороться сложнее. К распространенным атакам относятся рассылка вредоносных документов по электронной почте, использование уязвимостей (например, в браузерах и операционных системах) и физические атаки. Если это вас беспокоит, вам следует использовать более продвинутые стратегии защиты от угроз.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

По своей конструкции **веб-браузеры**, **почтовые клиенты** и **офисные приложения** обычно выполняют ненадёжный код, переданный вам третьими лицами. Запуск нескольких виртуальных машин для отделения подобных приложений от хост-системы, а также друг от друга - это одна из техник, которую можно использовать для снижения вероятности того, что эксплойт в этих приложениях скомпрометирует остальную часть вашей системы. Например, такие технологии, как Qubes OS или Microsoft Defender Application Guard в Windows, предоставляют удобные методы для этого.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Также следует убедиться, что диск зашифрован и что операционная система использует TPM или [Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) или [Secure Element](https://developers.google.com/android/security/android-ready-se) для ограничения количества попыток ввода парольной фразы шифрования. Вам следует избегать совместного использования компьютера с людьми, которым вы не доверяете, поскольку большинство настольных операционных систем не шифруют данные отдельно для каждого пользователя.

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might work their way into a position of power within a project or organization, then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what the change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enable undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Конфиденциальность от поставщиков услуг

<span class="pg-teal">:material-server-network: Поставщики услуг</span>

Мы живем в мире, где почти всё подключено к Интернету. Наши "личные" сообщения, электронные письма и социальные взаимодействия обычно хранятся где-то на каком-то сервере. Как правило, когда вы отправляете кому-либо сообщение, оно сохраняется на сервере, и когда ваш друг захочет прочитать сообщение, сервер отобразит ему его содержимое.

Очевидная проблема заключается в том, что поставщик услуг (или хакер, взломавший сервер) может получить доступ к вашим сообщениям когда угодно и как угодно, без вашего ведома. Это относится ко многим распространенным сервисам, таким как SMS, Telegram и Discord.

К счастью, сквозное шифрование (далее - E2EE) может облегчить эту проблему, шифруя сообщения между вами и желаемыми получателями еще до того, как они будут отправлены на сервер. Конфиденциальность ваших сообщений гарантирована при условии, что поставщик услуг не имеет доступа к закрытым ключам ни одной из сторон.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

На практике эффективность различных реализаций E2EE может варьироваться. Приложения, такие как [Signal](../real-time-communication.md#signal), работают на вашем устройстве, и каждая копия приложения является одинаковой при различных установках. Если поставщик услуг внедрит [backdoor](https://ru.wikipedia.org/wiki/%D0%91%D1%8D%D0%BA%D0%B4%D0%BE%D1%80) в свое приложение - в попытке украсть ваши закрытые ключи - это можно будет обнаружить с помощью [reverse engineering](https://ru.wikipedia.org/wiki/%D0%9E%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D0%B0%D1%8F_%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0).

С другой стороны, реализации E2EE, такие, как почта Proton Mail или *Web Vault* от Bitwarden, полагаются на то, что сервер динамически предоставляет браузеру код JavaScript для обработки криптографии. Вредоносный сервер может нацелиться на вас и отправить вам вредоносный код JavaScript, чтобы украсть ваш ключ шифрования (и это будет крайне сложно заметить). Поскольку сервер может выбирать для обслуживания разных веб-клиентов разных людей - даже если вы заметили атаку - доказать вину провайдера будет невероятно сложно.

Поэтому при любой возможности следует использовать нативные приложения вместо веб-клиентов.

</div>

Даже при использовании E2EE поставщики услуг все равно могут составить ваш профиль на основе **метаданных**, которые, как правило, не защищены. Хотя поставщик услуг не может читать ваши сообщения, он все же может наблюдать за такими важными вещами, как то, с кем вы общаетесь, как часто вы пишете им сообщения и когда вы обычно активны. Защита метаданных - довольно редкое явление, и, если это входит в вашу [модель угроз](threat-modeling.md), вам следует обратить пристальное внимание на техническую документацию используемого вами программного обеспечения, чтобы узнать, есть ли в нем минимизация или защита метаданных вообще.

## Программы массового наблюдения

<span class="pg-blue">:material-eye-outline: Массовое наблюдение</span>

Массовое наблюдение - это изощренные способы по отслеживанию "поведения, многих действий или информации" всего населения (или значительной его части).[^1] Часто это относится к правительственным программам, например[раскрытым Эдвардом Сноуденом в 2013 году](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Однако она может осуществляться и корпорациями, либо по поручению государственных органов, либо по собственной инициативе.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Правительства часто оправдывают программы массовой слежки как необходимые средства для борьбы с терроризмом и предотвращения преступлений. Однако, нарушая права человека, она чаще всего используется для непропорционального преследования меньшинств и политических диссидентов.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

Перед лицом [разоблачений Эдварда Сноудена о таких правительственных программах, как [PRISM](https://en.wikipedia.org/wiki/PRISM) и [Upstream](https://en.wikipedia.org/wiki/Upstream_collection)], представители разведки также признали, что АНБ в течение многих лет тайно собирало записи о телефонных звонках практически каждого американца - кто кому звонит, когда эти звонки совершаются и как долго они длятся. Подобная информация, накапливаемая АНБ день за днем, может раскрыть невероятно чувствительные детали о жизни и связях людей, например, звонили ли они пастору, специалисту по абортам, консультанту по наркомании или на горячую линию для самоубийц.

</div>

Несмотря на растущую массовую слежку в Соединенных Штатах, правительство обнаружило, что программы массовой слежки, такие как Раздел 215, имеют "мало уникальной ценности" в отношении пресечения реальных преступлений или террористических заговоров, а усилия в основном дублируют собственные целевые программы слежки ФБР.[^2]

В Интернете тебя можно отследить по различным параметрам:

- Твой IP адрес
- Файлы cookie в браузере
- Данные, которые ты предоставляешь на веб-сайтах
- Цифровой отпечаток твоего браузера или устройства
- Корреляция способов оплаты

\[Этот список не является исчерпывающим].

Если вас беспокоят программы массовой слежки, вы можете использовать такие стратегии, как разделение своей личности в Интернете, смешивание с другими пользователями или, по возможности, просто избегать предоставления идентифицирующей информации.

<span class="pg-brown">:material-account-cash: Капитализм слежки</span>

> Капитализм слежки - это экономическая система, сосредоточенная вокруг сбора и коммерциализации персональных данных с основной целью получения прибыли.[^3]

Для многих людей слежка и наблюдение со стороны частных корпораций вызывает растущее беспокойство. Всепроникающие рекламные сети, такие как Google и Facebook, распространяются в Интернете далеко за пределы контролируемых ими сайтов, отслеживая ваши действия на всём пути. Использование таких инструментов, как блокировщики контента, для ограничения сетевых запросов к их серверам, а также чтение политики конфиденциальности сервисов, которыми вы пользуетесь, может помочь вам избежать многих основных недоброжелателей (хотя это не может полностью предотвратить слежку).[^4]

Кроме того, даже компании, не относящиеся к *AdTech* или индустрии отслеживания, могут передавать вашу информацию брокерам данных [](https://en.wikipedia.org/wiki/Information_broker) (таким как Cambridge Analytica, Experian или Datalogix) или другим сторонам. Вы не можете автоматически считать, что ваши данные в безопасности только потому, что сервис, которым вы пользуетесь, не относится к типичной бизнес-модели AdTech или отслеживания. Самой надежной защитой от сбора корпоративных данных является шифрование или обфускация ваших данных всегда, когда это возможно, что затрудняет различным провайдерам соотнесение данных друг с другом и создание профиля на вас.

## Ограничение публичной информации

<span class="pg-green">:material-account-search: Публичная экспозиция</span>

Лучший способ сохранить свои данные в тайне - просто не предавать их огласке. Удаление нежелательной информации, которую вы нашли о себе в Интернете, - один из лучших первых шагов, которые вы можете предпринять для восстановления своей конфиденциальности.

- [Посмотрите наше руководство по удалению аккаунта :material-arrow-right-drop-circle:](account-deletion.md)

На сайтах, где вы делитесь информацией, очень важно проверить настройки конфиденциальности вашего аккаунта, чтобы ограничить распространение этих данных. Например, включите "приватный режим" на своих аккаунтах, если у вас есть такая возможность: Это гарантирует, что ваш аккаунт не индексируется поисковыми системами и что он не может быть просмотрен без вашего разрешения.

Если вы уже предоставили свою настоящую информацию на сайты, которые не должны ее иметь, рассмотрите возможность использования тактики дезинформации, например, представления фиктивной информации, связанной с этой онлайн-личностью. Это делает вашу настоящую информацию неотличимой от ложной.

## Избегание цензуры

<span class="pg-blue-gray">:material-close-outline: Цензура</span>

Цензура в Интернете может осуществляться (в разной степени) тоталитарными правительствами, администраторами сетей и поставщиками услуг. Эти попытки контролировать коммуникацию и ограничивать доступ к информации всегда будут несовместимы с правом человека на свободу слова и самовыражения.[^5]

Цензура на корпоративных платформах становится все более распространенным явлением, поскольку такие платформы, как Twitter и Facebook, поддаются общественному и рыночному давлению и давлению со стороны государственных органов. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

Люди, обеспокоенные угрозой цензуры, могут использовать такие технологии, как [Tor](../advanced/tor-overview.md), чтобы обойти ее, и поддерживать устойчивые к цензуре платформы для общения, такие как [Matrix](../real-time-communication.md#element), где нет централизованного органа, который может произвольно закрыть учетные записи.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Хотя уклонение от цензуры само по себе может быть легким, скрыть тот факт, что вы это делаете, может быть очень проблематично.

Вы должны учитывать, какие аспекты сети может наблюдать ваш оппонент и имеете ли вы достаточные основания для отрицания своих действий (англ. - plausible deniability). Например, использование [шифрованного DNS](../advanced/dns-overview.md#what-is-encrypted-dns) может помочь вам обойти примитивные системы цензуры, основанные на DNS, но оно не может действительно скрыть то, что вы посещаете, от вашего интернет-провайдера. VPN или Tor могут помочь скрыть от администраторов сетей то, что вы посещаете, но не могут скрыть, что вы вообще пользуетесь этими сетями. Шифрованные сетевые туннели (такие, как Obfs4proxy, Meek или Shadowsocks) могут помочь вам обойти брандмауэры, блокирующие распространенные протоколы VPN или Tor, но ваши попытки обхода блокировки могут быть обнаружены методами, такими как сканирование или [DPI](https://ru.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Вы всегда должны учитывать риски при попытке обойти цензуру, возможные последствия и то, насколько изощренным может быть ваш враг. Вы должны быть осторожны в выборе программного обеспечения и иметь запасной план на случай, если вас поймают.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: Совет по надзору за соблюдением конфиденциальности и гражданских свобод США: [*Отчет о программе записи телефонных разговоров, проводимой в соответствии с разделом 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. Вы также должны использовать другие методы смягчения последствий.
[^5]: Организация Объединенных Наций: [*Всеобщая декларация прав человека*](https://www.un.org/en/about-us/universal-declaration-of-human-rights).
