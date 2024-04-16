---
title: "Поширені міфи"
icon: 'material/robot-confused'
description: Конфіденційність — непроста тема, і легко піддатися маркетинговим заявам та іншій дезінформації.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            Доступність вихідного коду та спосіб ліцензування програмного забезпечення жодним чином не впливають на його безпеку. Програмне забезпечення з відкритим вихідним кодом може бути більш безпечним, ніж пропрієтарне програмне забезпечення, але немає жодних гарантій, що це так. Оцінюючи програмне забезпечення, ви повинні звертати увагу на репутацію та безпеку кожного інструменту на індивідуальній основі.
      - 
        "@type": Question
        name: Чи може передача довіри іншому провайдеру підвищити рівень конфіденційності?
        acceptedAnswer:
          "@type": Answer
          text: |
            Ми багато говоримо про "передачу довіри", коли обговорюємо такі рішення, як VPN (які передають довіру, яку ви покладаєте на свого інтернет-провайдера, до VPN-провайдера). Хоча це захищає ваші дані від вашого інтернет-провайдера, обраний вами VPN-провайдер все одно має доступ до ваших даних: ваші дані не повністю захищені від усіх сторін.
      - 
        "@type": Question
        name: Чи є рішення, орієнтовані на конфіденційність, за своєю суттю надійними?
        acceptedAnswer:
          "@type": Answer
          text: |
            Зосередження виключно на політиці конфіденційності та маркетингу інструменту або провайдера може відвернути вашу увагу від його слабких сторін. Коли ви шукаєте більш конфіденційне рішення, вам слід визначити, в чому полягає основна проблема, і знайти технічні розв'язання цієї проблеми. Наприклад, ви можете не використовувати Google Диск, який надає Google доступ до всіх ваших даних. Основною проблемою в цьому випадку є відсутність E2EE, тому вам слід переконатися, що провайдер, до якого ви переходите, дійсно реалізує E2EE, або скористатися інструментом (наприклад, Cryptomator), який забезпечує E2EE на будь-якому хмарному провайдері. Перехід до "орієнтованого на конфіденційність" провайдера (який не впроваджує E2EE) не вирішить вашу проблему: він просто змістить довіру від Google до цього провайдера.
      - 
        "@type": Question
        name: Наскільки складною має бути моя модель загроз?
        acceptedAnswer:
          "@type": Answer
          text: |
            Ми часто бачимо, як люди описують надто складні моделі загроз конфіденційності. Часто ці рішення включають в себе такі проблеми, як багато різних облікових записів електронної пошти або складні налаштування з великою кількістю рухомих частин і умов. Відповіді зазвичай відповідають на питання: «Який найкращий спосіб зробити X?»
            Пошук "найкращого" рішення для себе не обов'язково означає, що ви шукаєте безпомилкове рішення з десятками умов — з такими рішеннями часто важко працювати на практиці. Як ми обговорювали раніше, безпека часто приходить за рахунок зручності.
---

## "Програмне забезпечення з відкритим кодом завжди безпечне" або "Пропрієтарне програмне забезпечення більш безпечне"

Ці міфи випливають з низки упереджень, але доступність вихідного коду та спосіб ліцензування програмного забезпечення жодним чином не впливають на його безпеку. == Програмне забезпечення з відкритим вихідним кодом має *потенціал* бути безпечнішим, ніж пропрієтарне програмне забезпечення, але немає жодних гарантій, що це так.== Коли ви оцінюєте програмне забезпечення, ви повинні дивитися на репутацію та безпеку кожного інструменту на індивідуальній основі.

Програмне забезпечення з відкритим кодом *може* перевірятися третіми сторонами і часто є більш прозорим щодо потенційних вразливостей, ніж пропрієтарні аналоги. Це також дає змогу ознайомитися з кодом та вимкнути всі підозрілі функції, які ви знайдете самі. Однак, *якщо ви не зробите цього*, немає ніякої гарантії, що код коли-небудь оцінювався, особливо для невеликих проєктів. The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

З іншого боку, пропрієтарне програмне забезпечення менш прозоре, але це не означає, що воно не є безпечним. Великі проєкти пропрієтарного програмного забезпечення можуть бути перевірені як внутрішніми, так і сторонніми організаціями, а незалежні дослідники безпеки все ще можуть знайти вразливості за допомогою таких методів, як зворотна інженерія.

Щоб уникнути упереджених рішень, *дуже важливо* оцінювати стандарти конфіденційності та безпеки програмного забезпечення, яке ви використовуєте.

## "Передача довіри може підвищити конфіденційність"

Ми багато говоримо про "передачу довіри", коли обговорюємо такі рішення, як VPN (які передають довіру, яку ви покладаєте на свого інтернет-провайдера, до VPN-провайдера). Хоча це захищає ваші дані *конкретно* від вашого інтернет-провайдера, обраний вами VPN-провайдер все одно має доступ до ваших даних: Ваші дані не повністю захищені від усіх сторін. Це означає, що:

1. Ви повинні бути обережними при виборі постачальника, якому ви передаєте довіру.
2. Ви все одно повинні використовувати інші методи, такі як E2EE, щоб повністю захистити свої дані. Просто недовіряти одному провайдеру, щоб довіряти іншому, не захищає ваші дані.

## "Рішення, орієнтовані на конфіденційність, за своєю суттю є надійними"

Зосередження виключно на політиці конфіденційності та маркетингу інструменту або провайдера може відвернути вашу увагу від його слабких сторін. Коли ви шукаєте більш конфіденційне рішення, вам слід визначити, в чому полягає основна проблема, і знайти технічні розв'язання цієї проблеми. Наприклад, ви можете не використовувати Google Диск, який надає Google доступ до всіх ваших даних. Основною проблемою в цьому випадку є відсутність E2EE, тому вам слід переконатися, що провайдер, до якого ви переходите, дійсно реалізує E2EE, або скористатися інструментом (наприклад, [Cryptomator](../encryption.md#cryptomator-cloud)), який забезпечує E2EE на будь-якому хмарному провайдері. Перехід до "орієнтованого на конфіденційність" провайдера (який не впроваджує E2EE) не вирішить вашу проблему: він просто змістить довіру від Google до цього провайдера.

Політика конфіденційності та бізнес-практики постачальників, яких ви обираєте, дуже важливі, але їх слід вважати другорядними у порівнянні з технічними гарантіями вашої конфіденційності: ви не повинні перекладати довіру на іншого постачальника, коли довіра до постачальника взагалі не є вимогою.

## "Складніше — краще"

Ми часто бачимо, як люди описують надто складні моделі загроз конфіденційності. Часто ці рішення включають в себе такі проблеми, як багато різних облікових записів електронної пошти або складні налаштування з великою кількістю рухомих частин і умов. Відповіді зазвичай відповідають на питання: «Який найкращий спосіб зробити *X*?»

Пошук "найкращого" рішення для себе не обов'язково означає, що ви шукаєте безпомилкове рішення з десятками умов — з такими рішеннями часто важко працювати на практиці. Як ми обговорювали раніше, безпека часто приходить за рахунок зручності. Нижче ми надаємо кілька порад:

1. ==Дії повинні служити певній меті:== подумайте, як зробити те, що ви хочете, з найменшою кількістю дій.
2. ==Усунення точок людських помилок:== ми зазнаємо невдач, втомлюємося і забуваємо про щось. Щоб підтримувати безпеку, уникайте покладатися на ручні умови та процеси, які вам потрібно запам'ятати.
3. ==Використовуйте правильний рівень захисту для того, що ви плануєте.== ми часто зустрічаємо рекомендації щодо так званих рішень, захищених від правоохоронних органів або повісток до суду. Вони часто вимагають спеціальних знань і, як правило, не є тим, чого хочуть люди. Немає сенсу будувати складну модель загроз для анонімності, якщо вас можна легко деанонімізувати за допомогою простого нагляду.

Отже, як це може виглядати?

Однією з найяскравіших моделей загроз є та, коли люди *знають, хто ви*, і та, коли вони цього не знають. Завжди будуть ситуації, коли ви повинні заявити своє юридичне ім 'я, і є інші, де в цьому нема потреби.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
