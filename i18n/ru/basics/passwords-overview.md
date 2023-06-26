---
title: "Введение в пароли"
icon: 'material/form-textbox-password'
description: Вот несколько советов и рекомендаций о том, как создавать самые надежные пароли и обеспечивать безопасность своих учетных записей.
---

Passwords are an essential part of our everyday digital lives. We use them to protect our accounts, our devices and our secrets. Despite often being the only thing between us and an adversary who's after our private information, not a lot of thought is put into them, which often leads to people using passwords that can be easily guessed or brute-forced.

## Лучшие практики

### Используйте уникальные пароли для каждого сервиса

Imagine this; you sign up for an account with the same e-mail and password on multiple online services. If one of those service providers is malicious, or their service has a data breach that exposes your password in an unencrypted format, all a bad actor would have to do is try that e-mail and password combination across multiple popular services until they get a hit. It doesn't matter how strong that one password is, because they already have it.

This is called [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing), and it is one of the most common ways that your accounts can be compromised by bad actors. To avoid this, make sure that you never re-use your passwords.

### Используйте случайно сгенерированные пароли

==You should **never** rely on yourself to come up with a good password.== We recommend using [randomly generated passwords](#passwords) or [diceware passphrases](#diceware-passphrases) with sufficient entropy to protect your accounts and devices.

All of our [recommended password managers](../passwords.md) include a built-in password generator that you can use.

### Изменение паролей

You should avoid changing passwords that you have to remember (such as your password manager's master password) too often unless you have reason to believe it has been compromised, as changing it too often exposes you to the risk of forgetting it.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multi-factor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Most password managers allow you to set an expiry date for your password to make this easier to manage.

!!! tip "Checking for data breaches"

    If your password manager lets you check for compromised passwords, make sure to do so and promptly change any password that may have been exposed in a data breach. Alternatively, you could follow [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) with the help of a [news aggregator](../news-aggregators.md).

## Создание надежных паролей

### Пароли

A lot of services impose certain criteria when it comes to passwords, including a minimum or maximum length, as well as which special characters, if any, can be used. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

If you need a password you can memorize, we recommend a [diceware passphrase](#diceware-passphrases).

### Парольные фразы с помощью игрального кубика

С помощью игрального кубика можно создавать парольные фразы, которые легко запомнить, но трудно угадать.

Diceware passphrases are a great option when you need to memorize or manually input your credentials, such as for your password manager's master password or your device's encryption password.

An example of a diceware passphrase is `viewable fastness reluctant squishy seventeen shown pencil`.

To generate a diceware passphrase using real dice, follow these steps:

!!! note "Примечание"

    These instructions assume that you are using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other wordlists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

1. Roll a six-sided die five times, noting down the number after each roll.

2. As an example, let's say you rolled `2-5-2-6-6`. Look through the [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. You will find the word `encrypt`. Write that word down.

4. Repeat this process until your passphrase has as many words as you need, which you should separate with a space.

!!! warning "Important"

    You should **not** re-roll words until you get a combination of words that appeal to you. The process should be completely random.

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords.

We recommend using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [other wordlists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

??? note "Объяснение энтропии и прочности парольных фраз, созданных с помощью кубика"

    Чтобы продемонстрировать, насколько сильны такие парольные фразы, мы воспользуемся вышеупомянутой парольной фразой из семи слов (`viewable fastness reluctant squishy seventeen shown pencil`) и [большим списком слов EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) в качестве примера.
    
    Одним из показателей для определения силы парольной фразы является ее энтропия. Энтропия каждого слова в парольной фразе вычисляется как $\text{log}_2(\text{Слов-в-списке})$, а общая энтропия парольной фразы вычисляется как $\text{log}_2(\text{Слов-в-списке}^\text{Слов-в-фразе})$.
    
    Таким образом, каждое слово в вышеупомянутом списке дает ~12,9 бит энтропии ($\text{log}_2(7776)$), а парольная фраза из семи слов имеет ~90,47 бит энтропии ($\text{log}_2(7776^7)$).
    
    [Большой список слов EFF](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) содержит 7776 уникальных слов. Чтобы вычислить количество возможных парольных фраз, достаточно $\text{Слов-в-списке}^\text{Слов-в-фразе}$, или, в нашем случае, $7776^7$.
    
    Давайте представим все это в перспективе: парольная фраза из семи слов, использующая [большой список слов EFF] (https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt), является одной из ~1 719 070 799 748 422 500 000 000 000 000 возможных парольных фраз.
    
    В среднем, чтобы угадать вашу фразу, нужно попробовать 50% всех возможных комбинаций. Учитывая это, даже если ваш противник способен на ~1 000 000 000 000 000 000 угадываний в секунду, ему все равно потребуется ~27 255 689 лет, чтобы угадать вашу кодовую фразу. Это так, даже если верны следующие вещи:

    - Ваш противник знает, что вы использовали метод с кубиком.
    - Ваш противник знает конкретный список слов, который вы использовали.
    - Ваш противник знает, сколько слов содержит ваша парольная фраза.

Подводя итог, можно сказать, что парольные фразы с помощью кубика - это лучший вариант, если вам нужно что-то такое, что легко запомнить *и* исключительно сильное.

## Хранение паролей

### Менеджеры паролей

The best way to store your passwords is by using a password manager. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[List of recommended password managers](../passwords.md ""){.md-button}

!!! warning "Don't place your passwords and TOTP tokens inside the same password manager"

    When using TOTP codes as [multi-factor authentication](../multi-factor-authentication.md), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md#authenticator-apps).
    
    Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.
    
    Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

### Резервное копирование

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
