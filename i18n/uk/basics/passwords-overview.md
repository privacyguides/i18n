---
title: Introduction to Passwords
icon: material/form-textbox-password
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

Паролі є важливою частиною нашого повсякденного цифрового життя. We use them to protect our accounts, our devices, and our secrets. Попри те, що часто вони є єдиною перешкодою між нами та зловмисником, який хоче отримати нашу особисту інформацію, ми не замислюємося над ними, що часто призводить до того, що люди використовують паролі, які можна легко вгадати або підібрати грубим перебором.

## Передовий досвід

### Використовуйте унікальні паролі для кожного сервісу

Imagine this: You sign up for an account with the same e-mail and password on multiple online services. Якщо один з цих постачальників послуг є зловмисником, або в його сервісі стався витік даних, який розкрив ваш пароль у незашифрованому вигляді, все, що потрібно зробити зловмиснику, - це спробувати цю комбінацію електронної пошти та пароля на інших популярних сервісах, поки він не отримає доступ. Не має значення, наскільки надійним є цей пароль, адже він вже у них є.

Це називається [підміна облікових даних](https://en.wikipedia.org/wiki/Credential_stuffing), і це один з найпоширеніших способів, за допомогою якого зловмисники можуть скомпрометувати ваші облікові записи. Щоб уникнути цього, переконайтеся, що ви ніколи не використовуєте свої паролі повторно.

### Використовуйте випадково згенеровані паролі

**Ніколи** не варто покладатися на себе у виборі надійного пароля.== Ми рекомендуємо використовувати [випадково згенеровані паролі](#passwords) або [парольні фрази](#diceware-passphrases) з достатньою ентропією для захисту ваших облікових записів і пристроїв.

Усі наші [рекомендовані менеджери паролів](../passwords.md) містять вбудований генератор паролів, яким ви можете скористатися.

### Зміна паролів

Вам слід уникати занадто частої зміни паролів, які ви повинні пам'ятати (наприклад, головний пароль вашого менеджера паролів), якщо тільки у вас немає підстав вважати, що він був скомпрометований, оскільки занадто часта зміна пароля наражає вас на ризик його забути.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Більшість менеджерів паролів дозволяють встановити дату закінчення терміну дії пароля, щоб полегшити керування ним.

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

Якщо ваш менеджер паролів дозволяє перевіряти скомпрометовані паролі, переконайтеся, що ви це робите, і негайно змінюйте будь-який пароль, який, можливо, був розкритий під час витоку даних. Крім того, ви можете стежити за [стрічкою останніх порушень Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) за допомогою [новинного агрегатора](../news-aggregators.md).

</div>

## Створення надійних паролів

### Паролі

Багато сервісів встановлюють певні критерії до паролів, включаючи мінімальну або максимальну довжину, а також те, які спеціальні символи можна використовувати, якщо такі є. Використовуйте вбудований у ваш менеджер паролів генератор паролів, щоб створювати паролі настільки довгі та складні, наскільки це дозволяє сервіс, включаючи великі та малі літери, цифри та спеціальні символи.

Якщо вам потрібен пароль, який ви зможете запам'ятати, ми рекомендуємо використовувати [парольні фрази](#diceware-passphrases).

### Менеджери паролів

Парольна фраза - це метод створення ключових фраз, які легко запам'ятати, але важко вгадати.

Фрази-паролі - чудовий варіант, коли вам потрібно запам'ятати або ввести вручну свої облікові дані, наприклад, головний пароль вашого менеджера паролів або пароль шифрування вашого пристрою.

Прикладом парольної фрази є `viewable fastness reluctant squishy seventeen shown pencil`.

Щоб згенерувати кодову фразу з використанням справжніх гральних кубиків, виконайте такі дії:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Киньте шестигранний кубик п'ять разів, записуючи число після кожного кидка.

2. Для прикладу, припустимо, що ви викинули `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. Ви знайдете слово `encrypt`. Запишіть це слово.

4. Повторюйте цей процес до тих пір, поки у вашій парольній фразі не буде стільки слів, скільки вам потрібно, слова слід відокремлювати пробілами.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

Ви **не** повинні повторювати слова до тих пір, поки не отримаєте комбінацію слів, яка вам подобається. Процес має бути абсолютно випадковим.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords. We recommend setting the generated passphrase length to at least 6 words.

We also recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

В середньому, щоб вгадати вашу фразу, потрібно спробувати 50% всіх можливих комбінацій. Враховуючи це, навіть якщо ваш супротивник здатний робити ~1 000 000 000 000 000 спроб за секунду, йому все одно знадобиться ~27 255 689 років, щоб вгадати вашу парольну фразу. Це так, навіть якщо чинні наступні умови:

- Ваш супротивник знає, що ви використовували парольну фразу.
- Your adversary knows the specific word list that you used.
- Ваш супротивник знає, скільки слів містить ваша парольна фраза.

</details>

Підсумовуючи, парольні фрази - це найкращий варіант, коли вам потрібно щось, що легко запам'ятовується *та* є надзвичайно надійним.

## Зберігання паролів

### Менеджери паролів

Найкращий спосіб зберігати паролі - це використовувати менеджер паролів. Вони дозволяють зберігати паролі у файлі або в хмарі та захищати їх за допомогою єдиного головного пароля. Таким чином, вам потрібно буде запам'ятати лише один надійний пароль, який дозволить вам отримати доступ до решти.

Є багато хороших варіантів на вибір, як хмарних, так і локальних. Виберіть один із рекомендованих нами менеджерів паролів і використовуйте його для створення надійних паролів для всіх ваших акаунтів. Ми рекомендуємо захистити ваш менеджер паролів за допомогою [парольної фрази](#diceware-passphrases), що складається щонайменше з семи слів.

[Список рекомендованих менеджерів паролів](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Зберігання токенів TOTP в одному місці з паролями хоч і зручно, але зводить облікові записи до одного фактору в разі, якщо зловмисник отримає доступ до вашого менеджера паролів.

Крім того, ми не рекомендуємо зберігати в менеджері паролів одноразові коди відновлення. Їх слід зберігати окремо, наприклад, у зашифрованому контейнері на автономному накопичувачі.

</div>

### Резервні копії

Ви маєте зберігати резервну копію своїх паролів у [шифрованому](../encryption.md) вигляді на декількох накопичувачах або у хмарному сховищі. Це може допомогти вам отримати доступ до ваших паролів, якщо щось станеться з вашим основним пристроєм або сервісом, яким ви користуєтеся.
