---
title: "Распространенные заблуждения"
icon: 'material/robot-confused'
description: Конфиденциальность - не самая простая тема, и легко попасться на удочку маркетинговых заявлений и другой дезинформации.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Всегда ли открытое ПО безопасно?
        acceptedAnswer:
          "@type": Answer
          text: |
            Открытость исходного кода и лицензирование программного обеспечения никак не влияют на его безопасность. ПО с открытым исходным кодом может быть потенциально более безопасным чем проприетарное, но нет абсолютно никакой гарантии, что это так. При оценке программного обеспечения следует обращать внимание на репутацию и безопасность каждой части в отдельности.
      - 
        "@type": Question
        name: Может ли передача доверия другому провайдеру повысить уровень конфиденциальности?
        acceptedAnswer:
          "@type": Answer
          text: |
            Мы часто говорим о "смещении доверия" при обсуждении таких решений, как VPN (смещающие доверие, которое вы возлагаете на своего интернет-провайдера, на провайдера VPN). Хотя это защищает ваши данные от вашего интернет-провайдера, выбранный вами VPN-провайдер по-прежнему имеет доступ к вашим данным: Ваши данные не защищены от всех сторон полностью.
      - 
        "@type": Question
        name: Являются ли решения, ориентированные на конфиденциальность, по своей сути надежными?
        acceptedAnswer:
          "@type": Answer
          text: |
            Сосредоточившись исключительно на политике конфиденциальности и маркетинге ПО или провайдера, вы можете не заметить его слабые стороны. Если вы ищете более частное решение, вам следует определить, в чем заключается основная проблема, и найти технические решения этой проблемы. Например, вы не хотите использовать Google Drive, который даёт Google доступ ко всем вашим данным. Основной проблемой в данном случае является отсутствие E2EE, поэтому вы должны убедиться, что провайдер, на которого вы переходите, действительно реализует E2EE, или использовать инструмент (например, Cryptomator), обеспечивающий E2EE на любом облачном провайдере. Переход на провайдера, "ориентированного на конфиденциальность" (который не реализует E2EE), не решает вашу проблему: он просто переносит доверие с Google на этого провайдера.
      - 
        "@type": Question
        name: Насколько сложной должна быть моя модель угроз?
        acceptedAnswer:
          "@type": Answer
          text: |
            Мы часто видим, как люди описывают слишком сложные модели угроз конфиденциальности. Часто эти решения включают такие проблемы, как множество различных учетных записей электронной почты или сложные настройки с большим количеством условий. Ответы, как правило, являются ответами на вопрос "Как лучшего всего сделать X?"
            Поиск "лучшего" решения для себя не обязательно означает, что вам нужно безошибочное решение с десятками условий - с такими решениями часто трудно работать в реальности. Как мы уже говорили ранее, безопасность часто достигается ценой удобства.
---

## "ПО с открытым исходным кодом всегда безопасно" или "Проприетарное ПО более безопасно"

Эти мифы проистекают из ряда предрассудков, однако доступность исходного кода и способ лицензирования программного обеспечения по своей сути никак не влияют на его безопасность. ==Программное обеспечение с открытым исходным кодом имеет *потенциал* быть более безопасным, чем проприетарное программное обеспечение, но нет абсолютно никаких гарантий, что это так.== Когда вы оцениваете программное обеспечение, вы должны смотреть на репутацию и безопасность каждого инструмента в отдельности.

Программное обеспечение с открытым исходным кодом *может* проверяться третьими сторонами, и зачастую оно более прозрачно в отношении потенциальных уязвимостей, чем проприетарные аналоги. Оно также позволяет просматривать код и отключать любые подозрительные функции, которые вы обнаружите. Однако, *если вы не сделаете этого*, нет никакой гарантии того, что код когда-либо проверялся, особенно в небольших проектах. The open development process has also sometimes been exploited to introduce new vulnerabilities known as [:material-package-variant-closed-remove: Supply Chain Attacks](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

С другой стороны, проприетарное программное обеспечение менее прозрачно, но это не означает, что оно небезопасно. Крупные проекты по разработке проприетарного программного обеспечения могут подвергаться внутреннему аудиту и аудиту сторонних организаций, а независимые исследователи безопасности все еще могут находить уязвимости с помощью таких методов, как реверс-инжиниринг.

Чтобы избежать необъективных решений, *жизненно важно* оценить стандарты конфиденциальности и безопасности программного обеспечения, которое вы используете.

## "Смещение доверия может повысить уровень конфиденциальности"

Мы часто говорим о "смещении доверия" при обсуждении таких решений, как VPN (смещающие доверие с интернет-провайдера на VPN-провайдера). Хотя это защищает ваши данные *конкретно* от вашего интернет-провайдера, выбранный вами VPN-провайдер все равно имеет доступ к вашим данным: ваши данные не защищены от всех сторон. Это означает, что:

1. Вы должны проявлять осторожность при выборе провайдера, которому вы будете доверять.
2. Для полной защиты данных все же следует использовать другие методы, например E2EE. Простое недоверие к одному провайдеру для того, чтобы довериться другому, не обеспечивает безопасность ваших данных.

## "Решения, ориентированные на конфиденциальность, по своей сути являются надёжными"

Сосредоточившись исключительно на политике конфиденциальности и маркетинге ПО или провайдера, вы можете не заметить его слабые стороны. Если вы ищете более частное решение, вам следует определить, в чем заключается основная проблема, и найти технические решения этой проблемы. Например, вы не хотите использовать Google Drive, который даёт Google доступ ко всем вашим данным. Основной проблемой в данном случае является отсутствие E2EE, поэтому вы должны убедиться, что провайдер, на которого вы переходите, действительно реализует E2EE, или использовать инструмент (например, [Cryptomator](../encryption.md#cryptomator-cloud)), обеспечивающий E2EE на любом облачном провайдере. Переход на провайдера, "ориентированного на конфиденциальность" (который не реализует E2EE), не решает вашу проблему: он просто переносит доверие с Google на этого провайдера.

Политика конфиденциальности и деловая практика выбранных вами провайдеров очень важны, но должны рассматриваться как вторичные по отношению к техническим гарантиям вашей конфиденциальности: Не стоит перекладывать доверие на другого провайдера, когда доверие к провайдеру вообще не является обязательным условием.

## "Сложнее - лучше"

Мы часто видим, как люди описывают слишком сложные модели угроз конфиденциальности. Often, these solutions include problems like multiple email accounts or complicated setups with lots of moving parts and conditions. Ответы, как правило, являются ответами на вопрос "Как лучшего всего сделать *X*?"

Поиск "лучшего" решения для себя не обязательно означает, что вам нужно безошибочное решение с десятками условий - с такими решениями часто трудно работать в реальности. Как мы уже говорили ранее, безопасность часто достигается ценой удобства. Ниже мы приводим несколько советов:

1. ==Действия должны служить определенной цели:== подумайте о том, как сделать то, что вы хотите, с помощью наименьшего количества действий.
2. ==Избегание человеческого фактора:== Мы терпим неудачи, устаем и забываем. Чтобы поддерживать безопасность, не полагайтесь на ручные условия и действия, которые вы должны помнить.
3. ==Используйте правильный уровень защиты для того, что вы задумали.== Мы часто встречаем рекомендации так называемых решений, защищенных от правоохранительных органов или судебных решений. Они часто требуют специальных знаний и, как правило, не являются тем, что нужно людям. There's no point in building an intricate threat model for anonymity if you can be easily deanonymized by a simple oversight.

Итак, как это может выглядеть?

Одна из самых четких моделей угроз - это модель, в которой люди *знают, кто вы*, и модель, в которой они этого не знают. Всегда будут ситуации, когда вы должны объявить свое юридическое имя, а есть такие, где это не нужно.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added an obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
