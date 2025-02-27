---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

Пароли являются неотъемлемой частью нашей повседневной цифровой жизни. Мы используем их для защиты наших аккаунтов, девайсов и секретов. Очень часто пароли, это единственное, что защищает нас от злоумышленников, которые хотят получить нашу личную информацию или деньги. Несмотря на это, паролям не уделяют должного внимания, что часто приводит к использованию простых паролей, которые легко угадать или подобрать.

## Лучшие практики

### Используйте уникальные пароли для каждого сервиса

Представьте: вы регистрируете учетную запись с одним и тем же электронным адресом и паролем на нескольких веб-сайтах. Если один из владельцев этих сайтов злоумышленник, или в его сервисе произошла утечка данных, в результате которой ваш пароль оказался в незашифрованном виде, все, что нужно сделать злоумышленнику, это попробовать комбинацию электронной почты и пароля в нескольких популярных сервисах, пока он не добьется успеха. Не имеет значения, насколько сложным является этот пароль, потому что он уже у них есть.

Это называется [подстановка учетных данных](https://en.wikipedia.org/wiki/Credential_stuffing), и это один из самых распространенных способов взлома ваших учетных записей. Чтобы избежать этого, убедитесь, что вы никогда не используете свои пароли повторно.

### Используйте случайно сгенерированные пароли

==Вы **никогда** не должны полагаться на себя, чтобы придумать хороший пароль.== Мы рекомендуем использовать [случайно сгенерированные пароли](#passwords) или [парольные фразы с помощью кубика](#diceware-passphrases) с достаточной энтропией для защиты ваших учетных записей и устройств.

Все рекомендуемые нами [менеджеры паролей](../passwords.md) включают встроенный генератор паролей, который вы можете использовать.

### Изменение паролей

Вам не следует слишком часто менять пароли, которые вы должны помнить (например, мастер-пароль от вашего менеджера паролей), если у вас нет оснований полагать, что он был взломан, поскольку слишком частая смена пароля подвергает вас риску его забыть.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Большинство менеджеров паролей позволяют установить срок действия пароля, чтобы облегчить отслеживание их давности.

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

Если ваш менеджер паролей позволяет проверять скомпрометированные пароли, обязательно сделайте это и незамедлительно измените любой пароль, который мог быть раскрыт в результате утечки данных. В качестве альтернативы вы можете подписаться на [ленту последних взломов от Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) с помощью [агрегатора новостей](../news-aggregators.md).

</div>

## Создание надежных паролей

### Пароли

Многие сервисы устанавливают определенные критерии для паролей, включая минимальную или максимальную длину, а также то, какие специальные символы могут быть использованы. Вы должны использовать встроенный в менеджере паролей генератор паролей, чтобы создавать пароли настолько длинные и сложные, насколько это позволяет сервис, включая заглавные и строчные буквы, цифры и специальные символы.

Если вам нужен пароль, который можно запомнить, мы рекомендуем вам [парольные фразы с помощью кубика](#diceware-passphrases).

### Парольные фразы с помощью игрального кубика

С помощью игрального кубика можно создавать парольные фразы, которые легко запомнить, но трудно угадать.

Парольные фразы с помощью кубика - это отличный вариант, когда вам нужно запомнить или ввести вручную свои учетные данные, например, главный пароль менеджера паролей или пароль шифрования вашего устройства.

Примером такой парольной фразы является `viewable fastness reluctant squishy seventeen shown pencil`.

Чтобы сгенерировать парольную фразу с использованием настоящих игральных кубиков, выполните следующие действия:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Бросьте шестигранный кубик пять раз, записывая число после каждого броска.

2. В качестве примера, допустим, вы бросили `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. Вы найдете слово `encrypt`. Запишите это слово.

4. Повторяйте этот процесс до тех пор, пока ваша парольная фраза не будет содержать столько слов, сколько вам нужно, которые следует разделять пробелом.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

Вы **не** должны перебрасывать кубик, в надежде получить комбинацию слов, которая вам нравится. Процесс должен быть полностью случайным.

</div>

Если у вас нет доступа к настоящим игральным костям или вы предпочитаете не использовать их, вы можете воспользоваться встроенным в менеджере паролей генератором паролей, поскольку большинство из них имеют возможность генерировать парольные фразы в дополнение к обычным паролям.

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

В среднем, чтобы угадать вашу фразу, нужно попробовать 50% всех возможных комбинаций. Учитывая это, даже если ваш противник способен на ~1 000 000 000 000 000 000 угадываний в секунду, ему все равно потребуется ~27 255 689 лет, чтобы угадать вашу кодовую фразу. Это так, даже если верны следующие вещи:

- Ваш противник знает, что вы использовали метод с кубиком.
- Your adversary knows the specific word list that you used.
- Ваш противник знает, сколько слов содержит ваша парольная фраза.

</details>

Подводя итог, можно сказать, что парольные фразы с помощью кубика - это лучший вариант, если вам нужно что-то такое, что легко запомнить *и* исключительно сильное.

## Хранение паролей

### Менеджеры паролей

Лучший способ хранения паролей - это использование менеджера паролей. Они позволяют хранить пароли в файле или в облаке и защищать их одним мастер-паролем. Таким образом, вам придется запомнить только один надежный пароль, который позволит вам получить доступ к остальным.

Существует множество хороших вариантов, как облачных, так и локальных. Выберите один из рекомендуемых нами менеджеров паролей и используйте его для создания надежных паролей для всех ваших учетных записей. Мы рекомендуем защитить ваш менеджер паролей [парольной фразой](#diceware-passphrases), состоящей как минимум из семи слов.

[Список рекомендуемых менеджеров паролей](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Хранение TOTP-токенов в том же месте, что и паролей, хотя и удобно, но сводит защиту учетных записей к одному фактору в случае, если злоумышленник получит доступ к вашему менеджеру паролей.

Кроме того, мы не рекомендуем хранить одноразовые коды восстановления в менеджере паролей. Их следует хранить отдельно, например, в зашифрованном контейнере на автономном устройстве хранения.

</div>

### Резервное копирование

Вы должны хранить [зашифрованную](../encryption.md) резервную копию ваших паролей на нескольких устройствах или в облачном хранилище. Это может быть полезно, если что-то случится с вашим устройством или с сервисом, которым вы пользуетесь.
