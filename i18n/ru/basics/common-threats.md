---
title: "Распространённые угрозы"
icon: 'material/eye-outline'
description: Модель угрозы уникальна для каждого, но здесь описаны некоторые из тех вещей, которые волнуют многих посетителей этого сайта.
---

В широком смысле мы разделяем наши рекомендации по категориям [угроз](threat-modeling.md) или целей, которые применимы к большинству людей. ==You may be concerned with none, one, a few, or all of these possibilities==, and the tools and services you use depend on what your goals are. У тебя могут быть специфичные угрозы, не относящиеся к этим категориям, что определённо нормально! Важной частью является развитие понимания преимуществ и недостатков инструментов, которые ты решил использовать, потому что ни один из них не защитит тебя от всех угроз.

- <span class="pg-purple">:material-incognito: Анонимность</span> - изоляция твоей деятельности в интернете от твоей настоящей личности, защита тебя от людей, пытающихся раскрыть *именно твою* личность.
- <span class="pg-red">:material-target-account: Таргетированные атаки</span> - защита от хакеров и других злоумышленников, которые пытаются получить доступ к *именно твоим* данным и устройствам.
- <span class="pg-orange">:material-bug-outline: Пассивные атаки</span> - защита от таких вещей, как вредоносное ПО, утечка данных и других атак, которые совершаются одновременно против многих людей.
- <span class="pg-teal">:material-server-network: Поставщики услуг</span> - защита твоих данных от поставщиков услуг (например, с помощью E2EE, которое делает твои данные нечитаемыми для сервера).
- <span class="pg-blue">:material-eye-outline: Массовая слежка</span> - защита от правительственных агентств, организаций, веб-сайтов и служб, которые совместно отслеживают твою активность.
- <span class="pg-brown">:material-account-cash: Surveillance Capitalism</span> - Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.
- <span class="pg-green">:material-account-search: Public Exposure</span> - Limiting the information about you that is accessible online—to search engines or the general public.
- <span class="pg-blue-gray">:material-close-outline: Censorship</span> - Avoiding censored access to information or being censored yourself when speaking online.

Some of these threats may be more important to you than others, depending on your specific concerns. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-red">:material-target-account: Targeted Attacks</span>, but they probably still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Similarly, many people may be primarily concerned with <span class="pg-green">:material-account-search: Public Exposure</span> of their personal data, but they should still be wary of security-focused issues, such as <span class="pg-orange">:material-bug-outline: Passive Attacks</span>—like malware affecting their devices.

## Анонимность и Конфиденциальность

<span class="pg-purple">:material-incognito: Анонимность</span>

Анонимность часто путают с конфиденциальностью, но это разные понятия. В то время как конфиденциальность - это набор решений, которые вы принимаете относительно того, как ваши данные используются и передаются, анонимность - это полное отделение вашей деятельности в Интернете от вашей реальной личности.

Например, инсайдеры и журналисты могут иметь гораздо более экстремальную модель угрозы, которая требует полной анонимности. Это не только сокрытие того, чем они занимаются, какими данными располагают, чтобы не быть взломанными злоумышленниками или правительством, но и полное сокрытие того, кто они, на самом деле, такие. Они часто будут жертвовать любыми удобствами, если это означает защиту их анонимности, конфиденциальности или безопасности, потому что от этого может зависеть их жизнь. Большинству людей не нужно заходить так далеко.

## Безопасность и Конфиденциальность

<span class="pg-orange">:material-bug-outline: Пассивные атаки</span>

Безопасность и конфиденциальность также часто путают, поскольку для получения хоть какого-то подобия конфиденциальности необходима безопасность: использование инструментов - даже если они приватны по своей конструкции - бесполезно, если они могут быть легко использованы злоумышленниками, которые впоследствии обнародуют ваши данные. Однако обратное не всегда верно: самый защищенный в мире сервис *необязательно* приватный. Лучшим примером этого является передача данных компании Google, у которой, учитывая ее масштабы, было мало инцидентов, связанных с безопасностью, за счёт привлечения экспертов по безопасности, лидирующих в данной отрасли, для защиты своей инфраструктуры. Несмотря на то, что Google предоставляет очень безопасные услуги, очень немногие люди сочтут свои данные конфиденциальными в бесплатных продуктах Google (Gmail, YouTube и т. д.)

Когда речь идет о безопасности приложений, мы обычно не знаем (а иногда и не можем знать), является ли используемое нами программное обеспечение вредоносным или может ли оно однажды стать таковым. Даже у самых надежных разработчиков, как правило, нет гарантии, что их программное обеспечение не имеет серьезной уязвимости, которая впоследствии может быть использована.

Чтобы минимизировать возможный ущерб, которое *может* причинить вредоносное ПО, следует использовать защиту путём разделения. К примеру, это может выражаться в использовании разных компьютеров для разных задач, использовании виртуальных машин для разделения различных групп связанных приложений или использовании безопасной операционной системы с сильным акцентом на "песочницу" приложений и обязательный контроль доступа.

!!! tip

    Мобильные операционные системы, как правило, имеют лучшую "песочницу" для приложений, чем настольные операционные системы: приложения не могут получить root-доступ и требуют разрешения на доступ к системным ресурсам.
    
    Настольные операционные системы, как правило, отстают по части надлежащей "песочницы". ChromeOS имеет возможности "песочницы", аналогичные Android, а macOS имеет полный контроль системных разрешений (и разработчики могут отказаться от "песочницы" для приложений). Однако эти операционные системы передают идентифицирующую информацию своим соответствующим OEM-производителям. Linux, как правило, не предоставляет информацию поставщикам систем, но имеет слабую защиту от эксплойтов и вредоносных приложений. Это можно несколько смягчить с помощью специализированных дистрибутивов, которые в значительной степени используют виртуальные машины или контейнеры, например [Qubes OS](../../desktop/#qubes-os).

<span class="pg-red">:material-target-account: Целевые атаки</span>

С целенаправленными атаками на конкретного человека бороться сложнее. К распространенным атакам относятся рассылка вредоносных документов по электронной почте, использование уязвимостей (например, в браузерах и операционных системах) и физические атаки. Если это вас беспокоит, вам следует использовать более продвинутые стратегии защиты от угроз.

!!! tip

    По своей конструкции **веб-браузеры**, **почтовые клиенты** и **офисные приложения** обычно выполняют ненадёжный код, переданный вам третьими лицами. Запуск нескольких виртуальных машин для отделения подобных приложений от хост-системы, а также друг от друга - это одна из техник, которую можно использовать для снижения вероятности того, что эксплойт в этих приложениях скомпрометирует остальную часть вашей системы. Например, такие технологии, как Qubes OS или Microsoft Defender Application Guard в Windows, предоставляют удобные методы для этого.

Если вы опасаетесь **физических атак**, вам следует использовать операционную систему с реализацией безопасной проверенной загрузки, например Android, iOS, macOS или [Windows (с TPM)](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process). Также следует убедиться, что диск зашифрован и что операционная система использует TPM или [Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) или [Secure Element](https://developers.google.com/android/security/android-ready-se) для ограничения количества попыток ввода парольной фразы шифрования. Вам следует избегать совместного использования компьютера с людьми, которым вы не доверяете, поскольку большинство настольных операционных систем не шифруют данные отдельно для каждого пользователя.

## Конфиденциальность от поставщиков услуг

<span class="pg-teal">:material-server-network: Поставщики услуг</span>

Мы живем в мире, где почти всё подключено к Интернету. Наши "личные" сообщения, электронные письма и социальные взаимодействия обычно хранятся где-то на каком-то сервере. Как правило, когда вы отправляете кому-либо сообщение, оно сохраняется на сервере, и когда ваш друг захочет прочитать сообщение, сервер отобразит ему его содержимое.

Очевидная проблема заключается в том, что поставщик услуг (или хакер, взломавший сервер) может получить доступ к вашим сообщениям когда угодно и как угодно, без вашего ведома. Это относится ко многим распространенным сервисам, таким как SMS, Telegram и Discord.

К счастью, сквозное шифрование (далее - E2EE) может облегчить эту проблему, шифруя сообщения между вами и желаемыми получателями еще до того, как они будут отправлены на сервер. Конфиденциальность ваших сообщений гарантирована при условии, что поставщик услуг не имеет доступа к закрытым ключам ни одной из сторон.

!!! note "Примечание о шифровании на основе веб-технологий"

    На практике эффективность различных реализаций E2EE может варьироваться. Приложения, такие как [Signal](../real-time-communication.md#signal), работают на вашем устройстве, и каждая копия приложения является одинаковой при различных установках. Если поставщик услуг внедрит [backdoor](https://ru.wikipedia.org/wiki/%D0%91%D1%8D%D0%BA%D0%B4%D0%BE%D1%80) в свое приложение - в попытке украсть ваши закрытые ключи - это можно будет обнаружить с помощью [reverse engineering] (https://ru.wikipedia.org/wiki/%D0%9E%D0%B1%D1%80%D0%B0%D1%82%D0%BD%D0%B0%D1%8F_%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0).
    
    С другой стороны, реализации E2EE, такие, как почта Proton Mail или *Web Vault* от Bitwarden, полагаются на то, что сервер динамически предоставляет браузеру код JavaScript для обработки криптографии. Вредоносный сервер может нацелиться на вас и отправить вам вредоносный код JavaScript, чтобы украсть ваш ключ шифрования (и это будет крайне сложно заметить). Поскольку сервер может выбирать для обслуживания разных веб-клиентов разных людей - даже если вы заметили атаку - доказать вину провайдера будет невероятно сложно.
    
    Поэтому при любой возможности следует использовать нативные приложения вместо веб-клиентов.

Даже при использовании E2EE поставщики услуг все равно могут составить ваш профиль на основе **метаданных**, которые, как правило, не защищены. Хотя поставщик услуг не может читать ваши сообщения, он все же может наблюдать за такими важными вещами, как то, с кем вы общаетесь, как часто вы пишете им сообщения и когда вы обычно активны. Защита метаданных - довольно редкое явление, и, если это входит в вашу [модель угроз](threat-modeling.md), вам следует обратить пристальное внимание на техническую документацию используемого вами программного обеспечения, чтобы узнать, есть ли в нем минимизация или защита метаданных вообще.

## Программы массового наблюдения

<span class="pg-blue">:material-eye-outline: Массовое наблюдение</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

!!! abstract "Atlas of Surveillance"

    If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org/) by the [Electronic Frontier Foundation](https://www.eff.org/).
    
    In France you can take a look at the [Technolopolice website](https://technopolice.fr/villes/) maintained by the non-profit association La Quadrature du Net.

Governments often justify mass surveillance programs as necessary means to combat terrorism and prevent crime. However, breaching human rights, it's most often used to disproportionately target minority groups and political dissidents, among others.

!!! quote "ACLU: [*The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward*](https://www.aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward)"

    In the face of [Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection)], intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. This kind of information, when amassed by the NSA day after day, can reveal incredibly sensitive details about people’s lives and associations, such as whether they have called a pastor, an abortion provider, an addiction counselor, or a suicide hotline.

Despite growing mass surveillance in the United States, the government has found that mass surveillance programs like Section 215 have had "little unique value" with respect to stopping actual crimes or terrorist plots, with efforts largely duplicating the FBI's own targeted surveillance programs.[^2]

В Интернете тебя можно отследить по различным параметрам:

- Твой IP адрес
- Файлы cookie в браузере
- Данные, которые ты предоставляешь на веб-сайтах
- Цифровой отпечаток твоего браузера или устройства
- Корреляция способов оплаты

\[This list isn't exhaustive].

If you're concerned about mass surveillance programs, you can use strategues like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

<span class="pg-brown">:material-account-cash: Surveillance Capitalism</span>

> Surveillance capitalism is an economic system centered around the capture and commodification of personal data for the core purpose of profit-making.[^3]

For many people, tracking and surveillance by private corporations is a growing concern. Pervasive ad networks, such as those operated by Google and Facebook, span the internet far beyond just the sites they control, tracking your actions along the way. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside of the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. The strongest protection against corporate data collection is to encrypt or obfuscate your data whenever possible, making it difficult for different providers to correlate data with each other and build a profile on you.

## Ограничение публичной информации

<span class="pg-green">:material-account-search: Общественное воздействие</span>

Лучший способ сохранить свои данные в тайне - просто не предавать их огласке. Удаление нежелательной информации, которую вы нашли о себе в Интернете, - один из лучших первых шагов, которые вы можете предпринять для восстановления своей конфиденциальности.

- [Посмотрите наше руководство по удалению аккаунта :material-arrow-right-drop-circle:](account-deletion.md)

На сайтах, где вы делитесь информацией, очень важно проверить настройки конфиденциальности вашего аккаунта, чтобы ограничить распространение этих данных. Например, включите "приватный режим" на своих аккаунтах, если у вас есть такая возможность: Это гарантирует, что ваш аккаунт не индексируется поисковыми системами и что он не может быть просмотрен без вашего разрешения.

Если вы уже предоставили свою настоящую информацию на сайты, которые не должны ее иметь, рассмотрите возможность использования тактики дезинформации, например, представления фиктивной информации, связанной с этой онлайн-личностью. Это делает вашу настоящую информацию неотличимой от ложной.

## Избегание цензуры

<span class="pg-blue-gray">:material-close-outline: Цензура</span>

Цензура в Интернете может осуществляться (в разной степени) тоталитарными правительствами, администраторами сетей и поставщиками услуг. Эти попытки контролировать коммуникацию и ограничивать доступ к информации всегда будут несовместимы с правом человека на свободу слова и самовыражения.[^5]

Цензура на корпоративных платформах становится все более распространенным явлением, поскольку такие платформы, как Twitter и Facebook, поддаются общественному и рыночному давлению и давлению со стороны государственных органов. Давление со стороны правительства может быть скрытым, например, Белый дом [требует удалить](https://www.nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) провокационное видео на YouTube, или открытым, например, правительство Китая требует от компаний придерживаться строгого режима цензуры.

Люди, обеспокоенные угрозой цензуры, могут использовать такие технологии, как [Tor](../advanced/tor-overview.md), чтобы обойти ее, и поддерживать устойчивые к цензуре платформы для общения, такие как [Matrix](../real-time-communication.md#element), где нет централизованного органа, который может произвольно закрыть учетные записи.

!!! совет

    Хотя уклонение от цензуры само по себе может быть легким, скрыть тот факт, что вы это делаете, может быть очень проблематично.
    
    Вы должны учитывать, какие аспекты сети может наблюдать ваш оппонент и имеете ли вы достаточные основания для отрицания своих действий (англ. - plausible deniability). Например, использование [шифрованного DNS](../advanced/dns-overview.md#what-is-encrypted-dns) может помочь вам обойти примитивные системы цензуры, основанные на DNS, но оно не может действительно скрыть то, что вы посещаете, от вашего интернет-провайдера. VPN или Tor могут помочь скрыть от администраторов сетей то, что вы посещаете, но не могут скрыть, что вы вообще пользуетесь этими сетями. Шифрованные сетевые туннели (такие, как Obfs4proxy, Meek или Shadowsocks) могут помочь вам обойти брандмауэры, блокирующие распространенные протоколы VPN или Tor, но ваши попытки обхода блокировки могут быть обнаружены методами, такими как сканирование или [DPI](https://ru.wikipedia.org/wiki/Deep_packet_inspection).

Вы всегда должны учитывать риски при попытке обойти цензуру, возможные последствия и то, насколько изощренным может быть ваш враг. Вы должны быть осторожны в выборе программного обеспечения и иметь запасной план на случай, если вас поймают.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://www.ranum.com/security/computer_security/editorials/dumb/)" (or, "listing all the bad things that we know about"), as many adblockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://www.un.org/en/about-us/universal-declaration-of-human-rights).
