---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

'비밀번호'는 우리의 일상 디지털 생활에 있어서 필수적인 요소입니다. 우리는 비밀번호를 통해 계정, 기기, 개인 정보를 보호합니다. 간혹 비밀번호는 우리의 개인 정보를 노리는 공격자와 우리 사이의 유일한 방어 수단임에도 불구하고, 사람들은 비밀번호의 중요성을 심각하게 생각하지 않아 쉽게 추측되거나 무차별 대입 공격에 취약한 비밀번호를 사용하는 경우가 흔합니다.

## 모범 사례

### 모든 서비스마다 서로 다른 비밀번호 사용하기

여러분이 여러 온라인 서비스에 똑같은 이메일, 비밀번호로 가입했다고 가정해봅시다. 서비스 제공 업체 중 하나가 악의적이거나, 해당 서비스에서 데이터 유출 사고가 발생해 비밀번호가 암호화되지 않은 형식으로 노출될 경우, 악의적인 공격자는 여러 유명 서비스에서 해당 이메일과 비밀번호 조합을 시도해 성공할 때까지 기다리기만 하면 됩니다. 비밀번호를 이미 알아낸 상태이기 때문에, 비밀번호가 얼마나 강력한지는 중요하지 않습니다.

이를 [크리덴셜 스터핑(Credential stuffing)](https://en.wikipedia.org/wiki/Credential_stuffing)이라 하며, 악의적인 공격자가 계정을 탈취하는 굉장히 흔한 방법 중 하나입니다. 이를 방지하려면 비밀번호를 재사용하지 말아야 합니다.

### 무작위로 생성된 비밀번호 사용하기

==You should **never** rely on yourself to come up with a good password.== We recommend using [randomly generated passwords](#passwords) or [diceware passphrases](#diceware-passphrases) with sufficient entropy to protect your accounts and devices.

All of our [recommended password managers](../passwords.md) include a built-in password generator that you can use.

### Rotating Passwords

You should avoid changing passwords that you have to remember (such as your password manager's master password) too often unless you have reason to believe it has been compromised, as changing it too often exposes you to the risk of forgetting it.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multi-factor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Most password managers allow you to set an expiry date for your password to make this easier to manage.

!!! tip "Checking for data breaches"

    If your password manager lets you check for compromised passwords, make sure to do so and promptly change any password that may have been exposed in a data breach. Alternatively, you could follow [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) with the help of a [news aggregator](../news-aggregators.md).

## 강력한 비밀번호 만들기

### 패스워드

A lot of services impose certain criteria when it comes to passwords, including a minimum or maximum length, as well as which special characters, if any, can be used. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

If you need a password you can memorize, we recommend a [diceware passphrase](#diceware-passphrases).

### Diceware 패스프레이즈

Diceware is a method for creating passphrases which are easy to remember, but hard to guess.

Diceware passphrases are a great option when you need to memorize or manually input your credentials, such as for your password manager's master password or your device's encryption password.

An example of a diceware passphrase is `viewable fastness reluctant squishy seventeen shown pencil`.

To generate a diceware passphrase using real dice, follow these steps:

!!! note

    These instructions assume that you are using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other wordlists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

1. Roll a six-sided die five times, noting down the number after each roll.

2. As an example, let's say you rolled `2-5-2-6-6`. Look through the [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. You will find the word `encrypt`. Write that word down.

4. Repeat this process until your passphrase has as many words as you need, which you should separate with a space.

!!! warning "Important"

    You should **not** re-roll words until you get a combination of words that appeal to you. The process should be completely random.

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords.

We recommend using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [other wordlists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

??? note "Explanation of entropy and strength of diceware passphrases"

    To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.
    
    One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as $\text{log}_2(\text{WordsInList})$ and the overall entropy of the passphrase is calculated as $\text{log}_2(\text{WordsInList}^\text{WordsInPhrase})$.
    
    Therefore, each word in the aforementioned list results in ~12.9 bits of entropy ($\text{log}_2(7776)$), and a seven word passphrase derived from it has ~90.47 bits of entropy ($\text{log}_2(7776^7)$).
    
    The [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is $\text{WordsInList}^\text{WordsInPhrase}$, or in our case, $7776^7$.
    
    Let's put all of this in perspective: A seven word passphrase using [EFF's large wordlist](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.
    
    On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

    - Your adversary knows that you used the diceware method.
    - Your adversary knows the specific wordlist that you used.
    - Your adversary knows how many words your passphrase contains.

To sum it up, diceware passphrases are your best option when you need something that is both easy to remember *and* exceptionally strong.

## 비밀번호 저장

### 비밀번호 관리자

비밀번호를 저장하는 가장 좋은 방법은 비밀번호 관리자를 사용하는 것입니다. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[권장 비밀번호 관리자 목록](../passwords.md ""){.md-button}

!!! warning "비밀번호와 TOTP 토큰을 하나의 비밀번호 관리자에 저장하지 마세요"

    When using TOTP codes as [multi-factor authentication](../multi-factor-authentication.md), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md#authenticator-apps).
    
    Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.
    
    Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

### 백업

비밀번호를 [암호화하여](../encryption.md) 백업하고 여러 저장 장치 혹은 클라우드 서비스에 저장해야 합니다. 이렇게 함으로써 주로 사용하는 기기나 이용하는 서비스에 문제가 생기더라도 자신의 비밀번호에 접근할 수 있습니다.
