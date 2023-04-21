---
title: "Introduzione alle password"
icon: 'material/form-textbox-password'
description: Ecco alcuni suggerimenti e trucchi su come creare le password più forti e mantenere i vostri account al sicuro.
---

Le password sono una parte essenziale della nostra vita digitale quotidiana. Le utilizziamo per proteggere i nostri account, dispositivi e segreti. Nonostante siano spesso l'unica cosa che ci separa da un nemico a caccia di informazioni private, non ci si pensa molto, il che spesso porta le persone ad utilizzare password che possono essere facilmente indovinate o forzate.

## Pratiche migliori

### Utilizza password uniche per ogni servizio

Immagina questo: registrate un account con la stessa email e la stessa password su più servizi online. Se uno di questi servizi è malevolo o il loro servizio subisce una violazione dei dati che espone la password in formato non criptato, tutto ciò che un malintenzionato dovrebbe fare è provare quella combinazione di e-mail e password su più servizi popolari finché non ottiene un risultato. Non importa quanto forte sia quella password, perchè ormai ce l'hanno già.

Questo fenomeno è chiamato [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing) ed è uno dei modi più comuni tramite cui i vostri account potrebbero venir compromessi da malintenzionati. Per evitare che ciò accada, assicurati di non riutilizzare mai le password.

### Usa password generate randomicamente

== Non dovresti **mai** affidarti a te stesso per creare un'ottima password.== Consigliamo di utilizzare [password generate randomicamente](#passwords) o [passphrase di tipo diceware](#diceware-passphrases) con un'entropia sufficiente a proteggere i tuoi account e dispositivi.

Tutti i nostri [gestori di password consigliati](../passwords.md) includono un generatore di password integrato che puoi utilizzare.

### Rotating Passwords

You should avoid changing passwords that you have to remember (such as your password manager's master password) too often unless you have reason to believe it has been compromised, as changing it too often exposes you to the risk of forgetting it.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multi-factor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Most password managers allow you to set an expiry date for your password to make this easier to manage.

!!! tip "Checking for data breaches"

    If your password manager lets you check for compromised passwords, make sure to do so and promptly change any password that may have been exposed in a data breach. Alternatively, you could follow [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) with the help of a [news aggregator](../news-aggregators.md).

## Creare password forti

### Password

Molti servizi impongono determinati criteri per quanto riguarda le password, tra cui una lunghezza minima o massima e l'eventuale utilizzo di caratteri speciali. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

If you need a password you can memorize, we recommend a [diceware passphrase](#diceware-passphrases).

### Diceware Passphrases

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

## Memorizzare le password

### Gestori di password

Il miglior modo per memorizzare le proprie password è quello di utilizzare un gestore di password. Ti consentono di memorizzare le password in un singolo file o nel cloud e di proteggerle con un'unica password principale. In questo modo, dovrete ricordare solo un'unica password forte, che vi permetterà di accedere alle altre.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[Elenco dei gestori di password consigliati](../passwords.md ""){.md-button}

!!! warning "Don't place your passwords and TOTP tokens inside the same password manager"

    When using TOTP codes as [multi-factor authentication](../multi-factor-authentication.md), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md#authenticator-apps).
    
    Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.
    
    Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

### Backup

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
