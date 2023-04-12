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
        name: Является ли ПО с открытым исходным кодом безопасным по своей сути?
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

These myths stem from a number of prejudices, but whether the source code is available and how software is licensed does not inherently affect its security in any way. ==Open-source software has the *potential* to be more secure than proprietary software, but there is absolutely no guarantee this is the case.== When you evaluate software, you should look at the reputation and security of each tool on an individual basis.

Open-source software *can* be audited by third-parties, and is often more transparent about potential vulnerabilities than proprietary counterparts. It also allows you to review the code and disable any suspicious functionality you find yourself. However, *unless you do so*, there is no guarantee that code has ever been evaluated, especially with smaller software projects. The open development process has also sometimes been exploited to introduce new vulnerabilities into even large projects.[^1]

On the flip side, proprietary software is less transparent, but that doesn't imply that it's not secure. Major proprietary software projects can be audited internally and by third-party agencies, and independent security researchers can still find vulnerabilities with techniques like reverse engineering.

To avoid biased decisions, it's *vital* that you evaluate the privacy and security standards of the software you use.

## "Смещение доверия может повысить уровень конфиденциальности"

We talk about "shifting trust" a lot when discussing solutions like VPNs (which shift the trust you place in your ISP to the VPN provider). While this protects your browsing data from your ISP *specifically*, the VPN provider you choose still has access to your browsing data: Your data isn't completely secured from all parties. This means that:

1. You must exercise caution when choosing a provider to shift trust to.
2. You should still use other techniques, like E2EE, to protect your data completely. Merely distrusting one provider to trust another is not securing your data.

## "Решения, ориентированные на конфиденциальность, по своей сути являются надёжными"

Сосредоточившись исключительно на политике конфиденциальности и маркетинге ПО или провайдера, вы можете не заметить его слабые стороны. Если вы ищете более частное решение, вам следует определить, в чем заключается основная проблема, и найти технические решения этой проблемы. Например, вы не хотите использовать Google Drive, который даёт Google доступ ко всем вашим данным. Основной проблемой в данном случае является отсутствие E2EE, поэтому вы должны убедиться, что провайдер, на которого вы переходите, действительно реализует E2EE, или использовать инструмент (например, [Cryptomator](../encryption.md#cryptomator-cloud)), обеспечивающий E2EE на любом облачном провайдере. Переход на провайдера, "ориентированного на конфиденциальность" (который не реализует E2EE), не решает вашу проблему: он просто переносит доверие с Google на этого провайдера.

Политика конфиденциальности и деловая практика выбранных вами провайдеров очень важны, но должны рассматриваться как вторичные по отношению к техническим гарантиям вашей конфиденциальности: Не стоит перекладывать доверие на другого провайдера, когда доверие к провайдеру вообще не является обязательным условием.

## "Сложнее - лучше"

Мы часто видим, как люди описывают слишком сложные модели угроз конфиденциальности. Часто эти решения включают такие проблемы, как множество различных учетных записей электронной почты или сложные настройки с большим количеством условий. Ответы, как правило, являются ответами на вопрос "Как лучшего всего сделать *X*?"

Поиск "лучшего" решения для себя не обязательно означает, что вам нужно безошибочное решение с десятками условий - с такими решениями часто трудно работать в реальности. Как мы уже говорили ранее, безопасность часто достигается ценой удобства. Ниже мы приводим несколько советов:

1. ==Actions need to serve a particular purpose:== think about how to do what you want with the fewest actions.
2. ==Remove human failure points:== We fail, get tired, and forget things. To maintain security, avoid relying on manual conditions and processes that you have to remember.
3. ==Use the right level of protection for what you intend.== We often see recommendations of so-called law-enforcement or subpoena-proof solutions. These often require specialist knowledge and generally aren't what people want. There's no point in building an intricate threat model for anonymity if you can be easily de-anonymized by a simple oversight.

So, how might this look?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    !!! tip
   
        When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://www.getmonero.org/). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: One notable example of this is the [2021 incident in which University of Minnesota researchers introduced three vulnerabilities into the Linux kernel development project](https://cse.umn.edu/cs/linux-incident).
