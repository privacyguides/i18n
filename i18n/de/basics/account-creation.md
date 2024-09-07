---
meta_title: "Wie man Internetkonten privat erstellt - Privacy Guides"
title: "Konto-Erstellung"
icon: 'material/account-plus'
description: Das Anlegen von Online-Konten ist praktisch eine Notwendigkeit für das Internet. Mit diesen Schritten kannst du sicherstellen, dass du privat bleibst.
---

Oft melden sich Menschen für Dienste an, ohne nachzudenken. Vielleicht ist es ein Streaming-Dienst, mit dem du die neue Serie, über die alle reden, sehen kannst, oder ein Konto, mit dem du einen Rabatt für dein Lieblingsrestaurant bekommst. In jedem Fall solltest du die Auswirkungen auf Ihre Daten jetzt und in Zukunft beachten.

Mit jedem neuen Dienst, den du nutzt, sind Risiken verbunden. Datenlecks, die Weitergabe von Kundeninformationen an Dritte, der Zugriff auf Daten durch unberechtigte Mitarbeiter - all dies sind Möglichkeiten, die bei der Weitergabe deiner Informationen berücksichtigt werden müssen. Du musst sicher sein, dass du dem Dienst vertrauen kannst. Deshalb empfehlen wir, wertvolle Daten nur auf den ausgereiftesten und erprobten Produkten zu speichern. Das bedeutet in der Regel Dienste, die E2EE anbieten und eine kryptographisches Audit durchlaufen haben. Ein Audit erhöht die Sicherheit, dass das Produkt ohne eklatante Sicherheitsprobleme entwickelt wurde, die von einem unerfahrenen Entwickler verursacht wurden.

Bei einigen Diensten kann es auch schwierig sein, die Konten zu löschen. Manchmal ist es möglich, die mit einem Konto verbundenen Daten [zu überschreiben](account-deletion.md#overwriting-account-information), aber in anderen Fällen speichert der Dienst die gesamte Historie der Änderungen an dem Konto.

## Nutzungsbedingungen & Datenschutzbestimmungen

Die Nutzungsbedingungen sind die Regeln, denen du zustimmst, wenn du einen Dienst in Anspruch nimmst. Bei größeren Dienstleistern werden diese Regeln oft durch automatisierte Systeme durchgesetzt. Manchmal können diese automatischen Systeme Fehler machen. So kann es beispielsweise vorkommen, dass dein Konto bei einigen Diensten gesperrt wird, weil du eine VPN- oder VOIP-Nummer verwendest. Gegen solche Verbote Einspruch zu erheben, ist oft schwierig und erfordert auch ein automatisiertes Verfahren, das nicht immer erfolgreich ist. Dies wäre einer der Gründe, warum wir beispielsweise nicht empfehlen würden, Gmail für E-Mail zu verwenden. E-Mail ist entscheidend für den Zugriff auf andere Dienste, für die du dich möglicherweise angemeldet hast.

In den Datenschutzrichtlinien steht, wie der Dienst deine Daten verwenden wird, und es lohnt sich, sie zu lesen, damit du verstehst, wie deine Daten verwendet werden. Ein Unternehmen oder eine Organisation ist möglicherweise rechtlich nicht verpflichtet, alles zu befolgen, was in der Richtlinie enthalten ist (dies hängt von der jeweiligen Rechtsprechung ab). Wir empfehlen dir, einen Überblick über die örtlichen Gesetze zu verschaffen und darüber, was ein Anbieter erheben darf.

Wir empfehlen die Suche nach bestimmten Begriffen wie "Datenerfassung", "Datenanalyse", "Cookies", "Anzeigen" oder "Drittanbieter". Manchmal hast du die Möglichkeit, die Datenerfassung oder die Weitergabe deiner Daten abzulehnen, aber es ist am besten, einen Dienst zu wählen, der deine Privatsphäre von Anfang an respektiert.

Denke auch daran, dass du dem Unternehmen oder der Organisation dein Vertrauen schenkst und dass sie ihre eigenen Datenschutzrichtlinien einhalten.

## Authentifizierungsmethoden

In der Regel gibt es mehrere Möglichkeiten, sich für ein Konto anzumelden, jede mit ihren eigenen Vor- und Nachteilen.

### E-Mail und Passwort

Die häufigste Art, ein neues Konto zu erstellen, ist die Eingabe einer E-Mail-Adresse und eines Passworts. Wenn du diese Methode anwendest, solltest du einen Passwort-Manager verwenden und die [besten Praktiken](passwords-overview.md) für Passwörter befolgen.

<div class="admonition tip" markdown>
<p class="admonition-title">Tipp</p>

Du kannst deinen Passwort-Manager auch zur Organisation anderer Authentifizierungsmethoden verwenden! Füge einfach den neuen Eintrag hinzu und fülle die entsprechenden Felder aus. Du kannst Notizen für Dinge wie Sicherheitsfragen oder einen Backup-Schlüssel hinzufügen.

</div>

Du bist für die Verwaltung deiner Anmeldedaten verantwortlich. Für zusätzliche Sicherheit kannst du [MFA](multi-factor-authentication.md) für deine Konten einrichten.

[Empfohlene Passwort-Manager](../passwords.md ""){.md-button}

#### E-Mail-Aliasse

Wenn du deine echte E-Mail-Adresse nicht an einen Dienst weitergeben möchtest, hast du die Möglichkeit, einen Alias zu verwenden. Wir haben diese auf unserer Empfehlungsseite für E-Mail-Dienste näher beschrieben. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Empfohlene E-Mail-Aliasing-Dienste](../email-aliasing.md ""){.md-button}

### "Anmelden mit ..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

Die wichtigsten Vorteile sind:

- **Security**: you don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials, because they are stored with the external OAuth provider, which when it comes to services like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease of use**: multiple accounts are managed by a single login.

Aber es gibt auch Nachteile:

- **Privacy**: the OAuth provider you log in with will know the services you use.
- **Centralization**: if the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Telefonnummer

We recommend avoiding services that require a phone number for sign up. A phone number can identity you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VOIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Benutzername und Passwort

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
