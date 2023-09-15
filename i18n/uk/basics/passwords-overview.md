---
title: "Вступ до паролів"
icon: 'material/form-textbox-password'
description: Це кілька порад та підказок про те, як створювати найнадійніші паролі та зберігати свої акаунти в безпеці.
---

Паролі є важливою частиною нашого повсякденного цифрового життя. We use them to protect our accounts, our devices and our secrets. Despite often being the only thing between us and an adversary who's after our private information, not a lot of thought is put into them, which often leads to people using passwords that can be easily guessed or brute-forced.

## Найкращі практики

### Використовуйте унікальні паролі для кожного сервісу

Imagine this; you sign up for an account with the same e-mail and password on multiple online services. If one of those service providers is malicious, or their service has a data breach that exposes your password in an unencrypted format, all a bad actor would have to do is try that e-mail and password combination across multiple popular services until they get a hit. It doesn't matter how strong that one password is, because they already have it.

This is called [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing), and it is one of the most common ways that your accounts can be compromised by bad actors. To avoid this, make sure that you never re-use your passwords.

### Використовуйте випадково згенеровані паролі

**Ніколи** не варто покладатися на себе у виборі надійного пароля.== Ми рекомендуємо використовувати [випадково згенеровані паролі](#passwords) або [двозначні паролі](#diceware-passphrases) з достатньою ентропією для захисту ваших облікових записів і пристроїв.

Усі наші [рекомендовані менеджери паролів](../passwords.md) містять вбудований генератор паролів, яким ви можете скористатися.

### Зміна паролів

Вам слід уникати занадто частої зміни паролів, які ви повинні пам'ятати (наприклад, головний пароль вашого менеджера паролів), якщо тільки у вас немає підстав вважати, що він був скомпрометований, оскільки занадто часта зміна пароля наражає вас на ризик його забути.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multi-factor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Most password managers allow you to set an expiry date for your password to make this easier to manage.

!!! tip "Checking for data breaches"

    If your password manager lets you check for compromised passwords, make sure to do so and promptly change any password that may have been exposed in a data breach. Alternatively, you could follow [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) with the help of a [news aggregator](../news-aggregators.md).

## Створення надійних паролів

### Парольні фрази

A lot of services impose certain criteria when it comes to passwords, including a minimum or maximum length, as well as which special characters, if any, can be used. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

Якщо вам потрібен пароль, який ви зможете запам'ятати, ми рекомендуємо використовувати [парольні фрази](#diceware-passphrases).

### Менеджери паролів

Парольна фраза - це метод створення ключових фраз, які легко запам'ятати, але важко вгадати.

Фрази-паролі - чудовий варіант, коли вам потрібно запам'ятати або ввести вручну свої облікові дані, наприклад, головний пароль вашого менеджера паролів або пароль шифрування вашого пристрою.

Прикладом парольної фрази є `viewable fastness reluctant squishy seventeen shown pencil`.

Щоб згенерувати кодову фразу з використанням справжніх гральних кубиків, виконайте такі дії:

!!! note

    These instructions assume that you are using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other wordlists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

1. Киньте шестигранний кубик п'ять разів, записуючи число після кожного кидка.

2. As an example, let's say you rolled `2-5-2-6-6`. Look through the [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. You will find the word `encrypt`. Write that word down.

4. Повторюйте цей процес до тих пір, поки у вашій парольній фразі не буде стільки слів, скільки вам потрібно, які слід відокремлювати пробілами.

!!! warning "Important"

    You should **not** re-roll words until you get a combination of words that appeal to you. The process should be completely random.

Якщо у вас немає доступу до справжніх гральних кубиків або ви не хочете використовувати їх, ви можете скористатися вбудованим генератором паролів вашого менеджера паролів, оскільки більшість з них мають можливість генерувати парольні фрази на додаток до звичайних паролів.

We recommend using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [other wordlists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

??? note "Explanation of entropy and strength of diceware passphrases"

    To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.
    
    One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as $\text{log}_2(\text{WordsInList})$ and the overall entropy of the passphrase is calculated as $\text{log}_2(\text{WordsInList}^\text{WordsInPhrase})$.
    
    Therefore, each word in the aforementioned list results in ~12.9 bits of entropy ($\text{log}_2(7776)$), and a seven word passphrase derived from it has ~90.47 bits of entropy ($\text{log}_2(7776^7)$).
    
    The [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is $\text{WordsInList}^\text{WordsInPhrase}$, or in our case, $7776^7$.
    
    Let's put all of this in perspective: A seven word passphrase using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.
    
    On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

    - Ваш супротивник знає, що ви використовували парольну фразу.
    - Ваш супротивник знає конкретний список слів, який ви використовували.
    - Ваш супротивник знає, скільки слів містить ваша парольна фраза.

Підводячи підсумок, парольні фрази - це найкращий варіант, коли вам потрібно щось, що легко запам'ятовується *та* є надзвичайно надійним.

## Паролі

### Резервні копії

The best way to store your passwords is by using a password manager. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[Список рекомендованих менеджерів паролів](../passwords.md ""){.md-button}

!!! warning "Don't place your passwords and TOTP tokens inside the same password manager"

    When using TOTP codes as [multi-factor authentication](../multi-factor-authentication.md), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md#authenticator-apps).
    
    Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.
    
    Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

### Backups

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
