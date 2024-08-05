---
title: "Поширені Загрози"
icon: 'material/eye-outline'
description: Ваша модель загроз є особистою, але це деякі з речей, які хвилюють багатьох відвідувачів цього сайту.
---

Загалом, ми класифікуємо наші рекомендації на [загрози](threat-modeling.md) або цілі, які стосуються більшості людей. ==Ви можете бути зацікавлені в жодній, одній, кількох або всіх цих можливостях==, і інструменти та сервіси, які ви використовуєте, залежать від того, які цілі ви ставите перед собою. Ви також можете мати специфічні загрози поза цими категоріями, і це цілком нормально! Важливою частиною є розуміння переваг і недоліків інструментів, які ви обираєте, оскільки практично жоден з них не захистить вас від усіх можливих загроз.

<span class="pg-purple">:material-incognito: **Anonymity**</span>
:

Shielding your online activity from your real identity, protecting you from people who are trying to uncover *your* identity specifically.

<span class="pg-red">:material-target-account: **Targeted Attacks**</span>
:

Being protected from hackers or other malicious actors who are trying to gain access to *your* data or devices specifically.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain Attacks**</span>
:

Typically a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Attacks**</span>
:

Being protected from things like malware, data breaches, and other attacks that are made against many people at once.

<span class="pg-teal">:material-server-network: **Service Providers**</span>
:

Protecting your data from service providers (e.g. with E2EE, which renders your data unreadable to the server).

<span class="pg-blue">:material-eye-outline: **Mass Surveillance**</span>
:

Protection from government agencies, organizations, websites, and services which work together to track your activities.

<span class="pg-brown">:material-account-cash: **Surveillance Capitalism**</span>
:

Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Limiting the information about you that is accessible online—to search engines or the general public.

<span class="pg-blue-gray">:material-close-outline: **Censorship**</span>
:

Avoiding censored access to information or being censored yourself when speaking online.

Деякі з цих загроз можуть бути важливішими для вас, ніж інші, залежно від ваших конкретних проблем. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Аналогічно, багато людей можуть бути в першу чергу стурбовані <span class="pg-green">:material-account-search: публічним розголошенням</span> їхніх персональних даних, але їм все одно слід остерігатися проблем, пов'язаних з безпекою, таких як <span class="pg-orange">:material-bug-outline: пасивні атаки</span> — як-от шкідливе програмне забезпечення, що вражає їхні пристрої.

## Анонімність проти Конфіденційності

<span class="pg-purple">:material-incognito: Анонімність</span>

Анонімність часто плутають з конфіденційністю, але це різні поняття. У той час як конфіденційність це набір рішень, які ви приймаєте щодо того, як використовуються і поширюються ваші дані, анонімність — це повне відокремлення вашої діяльності в Інтернеті від вашої реальної особистості.

Наприклад, інформатори та журналісти можуть мати набагато більш екстремальну модель загроз, яка вимагає повної анонімності. Це не лише приховування того, чим вони займаються, які дані мають, і щоб їх не зламали зловмисники чи уряд, а й повне приховування того, ким вони є насправді. Вони часто жертвують будь-якими зручностями, якщо це важливо для захисту їхньої анонімності, конфіденційності або безпеки, тому що від цього може залежати їхнє життя. Більшості людей не потрібно заходити так далеко.

## Безпека та Конфіденційність

<span class="pg-orange">:material-bug-outline: Пасивні атаки</span>

Безпеку і конфіденційність також часто плутають, адже для досягнення будь-якої суттєвої конфіденційності вам потрібна безпека: використання інструментів, навіть якщо вони є конфіденційними за своєю суттю, є марним, якщо вони можуть бути легко експлуатовані зловмисниками, які згодом оприлюднять ваші дані. Однак зворотне не обов'язково вірно: найбезпечніший сервіс у світі *не обов'язково є* конфіденційним. Найкращим прикладом цього є довіра даних компанії Google, яка, зважаючи на свої масштаби, мала мало інцидентів безпеки завдяки залученню провідних експертів у галузі безпеки для захисту своєї інфраструктури. Попри те, що Google надає дуже безпечні послуги, дуже мало людей вважають свої дані конфіденційними в безкоштовних споживчих продуктах Google (Gmail, YouTube і т.д.).

Коли мова йде про безпеку додатків, ми зазвичай не знаємо (а іноді й не можемо знати), чи є програмне забезпечення, яке ми використовуємо, шкідливим, або чи може воно колись таким стати. Навіть найнадійніші розробники не можуть гарантувати, що їхнє програмне забезпечення не має серйозних вразливостей, які згодом можуть бути використані.

Щоб мінімізувати шкоду, яку може завдати шкідливе програмне забезпечення **, вам слід застосовувати захист за допомогою розмежування. Наприклад, це може бути використання різних комп'ютерів для різних завдань, використання віртуальних машин для розділення різних груп пов'язаних додатків або використання безпечної операційної системи з сильним акцентом на ізоляцію додатків і обов'язковим контролем доступу.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Мобільні операційні системи зазвичай мають кращу ізоляцію додатків, ніж операційні системи для ПК: програми не можуть отримати root-доступ і потребують дозволу для доступу до системних ресурсів.

Десктопні операційні системи зазвичай відстають у створенні належної ізоляції. ChromeOS має схожі можливості ізоляції з Android, а macOS має повний контроль прав у системі (і розробники можуть ввімкнути ізоляцію додатків). Однак ці операційні системи передають ідентифікаційну інформацію відповідним виробникам обладнання. Linux, як правило, не надає інформацію постачальникам систем, але має слабкий захист від експлойтів та шкідливих програм. This can be mitigated somewhat with specialized distributions which make significant use of virtual machines or containers, such as [Qubes OS](../desktop.md#qubes-os).

</div>

## Attacks against Specific Individuals

<span class="pg-red">:material-target-account: Цілеспрямовані атаки</span>

З цілеспрямованими атаками на конкретну особу боротися складніше. Поширені атаки включають надсилання шкідливих документів електронною поштою, експлуатацію вразливостей (наприклад, у браузерах та операційних системах) і фізичні атаки. Якщо це викликає у вас занепокоєння, вам слід використовувати більш просунуті стратегії пом'якшення загроз.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

За своєю суттю **веб-браузери**, **поштові клієнти** та **офісні програми** зазвичай виконують ненадійний код, надісланий вам третіми сторонами. Запуск декількох віртуальних машин для відокремлення таких додатків від основної системи, а також один від одного - це один зі способів зменшити ймовірність того, що експлойт в цих додатках може скомпрометувати решту системи. Наприклад, такі технології, як Qubes OS або Microsoft Defender Application Guard на Windows, надають зручні методи для цього.

</div>

If you are concerned about **physical attacks** you should use an operating system with a secure verified boot implementation, such as Android, iOS, macOS, or [Windows (with TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Також слід переконатися, що ваш диск зашифровано, а операційна система використовує TPM або Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) чи [Element](https://developers.google.com/android/security/android-ready-se) для обмеження кількості спроб введення ключової фрази шифрування. Вам слід уникати спільного використання комп'ютера з людьми, яким ви не довіряєте, оскільки більшість настільних операційних систем не шифрують дані окремо для кожного користувача.

## Attacks against Certain Organizations

<span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>

Supply chain attacks are frequently a form of <span class="pg-red">:material-target-account: Targeted Attack</span> towards businesses, governments, and activists, although they can end up compromising the public at large as well.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

A notable example of this occurred in 2017 when M.E.Doc, a popular accounting software in Ukraine, was infected with the *NotPetya* virus, subsequently infecting people who downloaded that software with ransomware. NotPetya itself was a ransomware attack which impacted 2000+ companies in various countries, and was based on the *EternalBlue* exploit developed by the NSA to attack Windows computers over the network.

</div>

There are few ways in which this type of attack might be carried out:

1. A contributor or employee might first work their way into a position of power within a project or organization, and then abuse that position by adding malicious code.
2. A developer may be coerced by an outside party to add malicious code.
3. An individual or group might identify a third party software dependency (also known as a library) and work to infiltrate it with the above two methods, knowing that it will be used by "downstream" software developers.

These sorts of attacks can require a lot of time and preparation to perform and are risky because they can be detected, particularly in open source projects if they are popular and have outside interest. Unfortunately they're also one of the most dangerous as they are very hard to mitigate entirely. We would encourage readers to only use software which has a good reputation and makes an effort to reduce risk by:

1. Only adopting popular software that has been around for a while. The more interest in a project, the greater likelihood that external parties will notice malicious changes. A malicious actor will also need to spend more time gaining community trust with meaningful contributions.
2. Finding software which releases binaries with widely-used, trusted build infrastructure platforms, as opposed to developer workstations or self-hosted servers. Some systems like GitHub Actions let you inspect the build script that runs publicly for extra confidence. This lessens the likelihood that malware on a developer's machine could infect their packages, and gives confidence that the binaries produced are in fact produced correctly.
3. Looking for code signing on individual source code commits and releases, which creates an auditable trail of who did what. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: Постачальники послуг</span>

Ми живемо у світі, де майже все підключено до інтернету. Наші "приватні" повідомлення, електронні листи та соціальні взаємодії зазвичай зберігаються десь на сервері. Зазвичай, коли ви надсилаєте комусь повідомлення, воно зберігається на сервері, і коли ваш друг захоче прочитати повідомлення, сервер покаже йому повідомлення.

Очевидна проблема полягає в тому, що постачальник послуг (або хакер, який зламав сервер) може отримати доступ до ваших розмов, коли завгодно і як завгодно, без вашого відома. Це стосується багатьох поширених сервісів, таких як SMS-повідомлення, Telegram і Discord.

На щастя, E2EE може вирішити цю проблему, шифруючи повідомлення між вами й вашими бажаними одержувачами ще до того, як вони будуть відправлені на сервер. Конфіденційність ваших повідомлень гарантується, якщо постачальник послуг не має доступу до приватних ключів жодної зі сторін.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

На практиці ефективність різних реалізацій E2EE відрізняється. Такі додатки як [Signal](../real-time-communication.md#signal) працюють на вашому пристрої за замовчуванням, і кожна копія програми однакова для різних інсталяцій. Якщо постачальник послуг впровадить [бекдор](https://uk.wikipedia.org/wiki/Бекдор) у свій додаток — у спробі викрасти ваші приватні ключі — це можна буде пізніше виявити за допомогою [зворотної розробки](https://uk.wikipedia.org/wiki/Зворотня_розробка).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. Шкідливий сервер може вибрати вас і надіслати вам шкідливий JavaScript-код, щоб викрасти ваш ключ шифрування (і це буде надзвичайно важко помітити). Оскільки сервер може обслуговувати різних веб-клієнтів для різних людей — навіть якщо ви помітили атаку — довести провину провайдера буде неймовірно складно.

Тому вам слід використовувати нативні додатки замість веб-клієнтів, коли це можливо.

</div>

Навіть з E2EE постачальники послуг все ще можуть профілювати вас на основі **метаданих**, які, як правило, не захищені. Хоча провайдер не може читати ваші повідомлення, він може спостерігати за важливими речами, наприклад, за тим, з ким ви розмовляєте, як часто ви надсилаєте їм повідомлення і коли ви зазвичай активні. Захист метаданих є досить рідкісним явищем, і — якщо це входить до вашої [моделі загроз](threat-modeling.md) — вам слід звернути пильну увагу на технічну документацію програмного забезпечення, яке ви використовуєте, щоб дізнатися, чи передбачено мінімізацію або захист метаданих взагалі.

## Програми масового спостереження

<span class="pg-blue">:material-eye-outline: Масове спостереження</span>

Масове спостереження — це складні зусилля з моніторингу "поведінки, багатьох видів діяльності або інформації" всього (або значної частини) населення.[^1] Часто йдеться про урядові програми, такі як ті, що [розкрив Едвард Сноуден у 2013 році](https://uk.wikipedia.org/wiki/Викриття_масового_стеження_у_2013_році). Однак це також може здійснюватися корпораціями, як від імені державних органів, так і за власною ініціативою.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Уряди часто виправдовують програми масового спостереження як необхідні засоби для боротьби з тероризмом і запобігання злочинності. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. Така інформація, яку АНБ збирає день за днем, може розкрити неймовірно делікатні подробиці про життя людей і їхні зв'язки, наприклад, чи телефонували вони до пастора, лікаря, який робить аборти, консультанта з питань залежності або на гарячу лінію для самогубців.

</div>

Незважаючи на зростання масового стеження в США, уряд виявив, що програми масового стеження, такі як Розділ 215, мають "невелику унікальну цінність" щодо припинення реальних злочинів або терористичних змов, а їхні зусилля значною мірою дублюють власні програми цільового стеження, що проводяться ФБР.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- Ваша IP-адреса
- Файли cookie браузера
- Дані, які ви передаєте на веб-сайти
- Відбиток вашого браузера або пристрою
- Кореляція способів оплати

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Капіталізм нагляду</span>

> Капіталізм нагляду - це економічна система, в основі якої лежить збір і комерціалізація персональних даних з метою отримання прибутку.[^3]

Для багатьох людей відстеження та нагляд з боку приватних корпорацій викликає дедалі більше занепокоєння. Повсюдні рекламні мережі, такі як Google і Facebook, охоплюють Інтернет далеко за межами сайтів, які вони контролюють, відстежуючи ваші дії по дорозі. Використання таких інструментів, як блокувальники контенту для обмеження мережевих запитів до їх серверів, а також ознайомлення з політикою конфіденційності сервісів, якими ви користуєтеся, може допомогти вам уникнути багатьох основних загроз (хоча повністю запобігти відстеженню не вдасться).[^4]

Крім того, навіть компанії, що не належать до *AdTech* або трекінгової індустрії, можуть ділитися вашою інформацією з [брокерами даних](https://en.wikipedia.org/wiki/Data_broker) (такими як Cambridge Analytica, Experian або Datalogix) або іншими сторонами. Ви не можете автоматично вважати, що ваші дані в безпеці лише тому, що сервіс, яким ви користуєтеся, не підпадає під типову бізнес-модель рекламних технологій або трекінгу. Найсильнішим захистом від корпоративного збору даних є шифрування або обфускація ваших даних, коли це можливо, що ускладнює різним провайдерам співвіднесення даних один з одним і створення профілю вашої особистості.

## Обмеження публічно доступної інформації

<span class="pg-green">:material-account-search: Публічний розголос</span>

Найкращий спосіб зберегти ваші дані конфіденційними — це просто не оприлюднювати їх взагалі. Видалення небажаної інформації, яку ви знаходите про себе в Інтернеті, є одним з найкращих перших кроків, які ви можете зробити, щоб відновити свою конфіденційність.

- [Перегляньте нашу інструкцію з видалення облікового запису :material-arrow-right-drop-circle:](account-deletion.md)

На сайтах, де ви ділитеся інформацією, дуже важливо перевірити налаштування конфіденційності вашого облікового запису, щоб обмежити поширення цих даних. Наприклад, увімкніть "приватний режим" у своїх акаунтах, якщо є така можливість: це гарантує, що ваш акаунт не буде індексовано пошуковими системами, і його не можна буде переглянути без вашого дозволу.

Якщо ви вже надали свою справжню інформацію сайтам, які не повинні її мати, розгляньте можливість використання тактики дезінформації, наприклад, надання вигаданої інформації, пов'язаної з цією онлайн-особистістю. Це зробить вашу справжню інформацію нерозрізненою з неправдивою.

## Уникнення цензури

<span class="pg-blue-gray">:material-close-outline: Цензура</span>

Цензуру в Інтернеті можуть здійснювати (різною мірою) такі суб'єкти, як тоталітарні уряди, мережеві адміністратори та провайдери послуг. Ці спроби контролювати комунікацію та обмежувати доступ до інформації завжди будуть несумісні з правом людини на свободу вираження поглядів.[^5]

Цензура на корпоративних платформах стає все більш поширеним явищем, оскільки такі платформи, як Twitter і Facebook, піддаються суспільному попиту, тиску ринку і тиску з боку державних органів. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

Люди, стурбовані загрозою цензури, можуть використовувати такі технології, як [Tor](../advanced/tor-overview.md), щоб обійти її, і підтримувати стійкі до цензури комунікаційні платформи, такі як [Matrix](../real-time-communication.md#element), які не мають централізованого облікового органу, що може довільно закривати акаунти.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

У той час як уникнути цензури може бути легко, приховати той факт, що ви це робите, може бути дуже проблематично.

Ви повинні враховувати, які аспекти мережі може спостерігати ваш супротивник, і чи є у вас правдоподібне заперечення ваших дій. Наприклад, використання [зашифрованого DNS](../advanced/dns-overview.md#what-is-encrypted-dns) може допомогти вам обійти рудиментарні системи цензури, засновані на DNS, але це не може по-справжньому приховати те, що ви відвідуєте, від вашого Інтернет-провайдера. VPN або Tor можуть допомогти приховати від мережевих адміністраторів що саме ви відвідуєте, але не можуть приховати сам факт використання цих мереж. Підключувані засоби передачі (такі як Obfs4proxy, Meek або Shadowsocks) можуть допомогти вам обійти брандмауери, які блокують поширені VPN-протоколи або Tor, але ваші спроби обходу все одно можуть бути виявлені такими методами, як зондування або [Deep Packet Inspection] (https://uk.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Ви завжди повинні враховувати ризики, пов'язані зі спробами обійти цензуру, потенційні наслідки і те, наскільки витонченим може бути ваш супротивник. Ви повинні бути обережними у виборі програмного забезпечення та мати запасний план на випадок, якщо вас спіймають.

[^1]: Вікіпедія: [*Масове спостереження*](https://en.wikipedia.org/wiki/Mass_surveillance) та [*Спостереження*](https://uk.wikipedia.org/wiki/Спостереження_(негласне)).
[^2]: Рада з нагляду за дотриманням приватності та громадянських свобод США: [*Звіт про програму прослуховування телефонних розмов, здійснену відповідно до Розділу 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Вікіпедія: [*Капіталізм нагляду*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. Ви також повинні використовувати інші методи пом'якшення.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
