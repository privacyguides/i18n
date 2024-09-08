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

Wenn du deine echte E-Mail-Adresse nicht an einen Dienst weitergeben möchtest, hast du die Möglichkeit, einen Alias zu verwenden. Wir haben diese auf unserer Empfehlungsseite für E-Mail-Dienste näher beschrieben. Im Grunde erlauben dir Alias-Dienste neue E-Mail-Adressen zu generieren, die alle E-Mails an deine Hauptadresse weiterleiten. Dies kann dazu beitragen, die Nachverfolgung über verschiedene Dienste hinweg zu verhindern und die Marketing-E-Mails zu verwalten, die manchmal mit dem Anmeldeprozess einhergehen. Diese können automatisch anhand des Alias gefiltert werden, an den sie gesendet werden.

Sollte ein Dienst gehackt werden, erhältst du möglicherweise Phishing- oder Spam-E-Mails an die Adresse, die du für die Anmeldung verwendet hast. Die Verwendung eindeutiger Aliasnamen für jeden Dienst kann dabei helfen, genau festzustellen, welcher Dienst gehackt wurde.

[Empfohlene E-Mail-Aliasing-Dienste](../email-aliasing.md ""){.md-button}

### "Anmelden mit ..." (OAuth)

OAuth ist ein Authentifizierungsprotokoll, das es dir ermöglicht, dich für einen Dienst anzumelden, ohne viele Informationen an den Dienstanbieter weiterzugeben, indem du stattdessen ein bestehendes Konto bei einem anderen Dienst verwendest. Wenn du in einem Registrierungsformular etwas wie "Mit *Anbietername* anmelden" siehst, wird in der Regel OAuth verwendet.

Wenn du dich mit OAuth anmeldest, wird eine Anmeldeseite bei dem von dir gewählten Anbieter geöffnet, und dein bestehendes Konto und das neue Konto werden miteinander verbunden. Dein Passwort wird nicht weitergegeben, wohl aber einige grundlegende Informationen (die du bei der Anmeldeanfrage einsehen kannst). Dieser Vorgang ist jedes Mal erforderlich, wenn du dich bei demselben Konto anmelden möchtest.

Die wichtigsten Vorteile sind:

- **Sicherheit**: Du musst dich nicht auf die Sicherheitspraktiken des Dienstes verlassen, bei dem du dich anmeldest, wenn es um die Speicherung deiner Anmeldedaten geht, da diese bei einem externen OAuth-Anbieter gespeichert werden. Diese Dienste, wie Apple und Google, wenden in der Regel die besten Sicherheitspraktiken an, Authentifizierungssysteme werden kontinuierlich überprüft und Anmeldedaten nicht in unangemessener Weise (z. B. im Klartext) gespeichert.
- **Benutzerfreundlichkeit**: Mehrere Konten werden über ein einziges Login verwaltet.

Aber es gibt auch Nachteile:

- **Privatsphäre**: Der OAuth-Anbieter, bei dem du dich anmeldest, weiß, welche Dienste du nutzt.
- **Zentralisierung**: Wenn das Konto, das du für OAuth verwendest, kompromittiert wird oder du nicht in der Lage bist, dich bei diesem anzumelden, sind alle anderen Konten, die mit dem Account verbunden sind, betroffen.

OAuth kann besonders in Situationen nützlich sein, in denen du von einer tieferen Integration zwischen Diensten profitieren kannst. Wir empfehlen, OAuth nur dort zu verwenden, wo du es brauchst, und das Hauptkonto immer mit [MFA](multi-factor-authentication.md) zu schützen.

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Telefonnummer

Wir empfehlen, Dienste zu meiden, die eine Telefonnummer für die Anmeldung erfordern. Eine Telefonnummer kann dich bei mehreren Diensten identifizieren, und je nach den Vereinbarungen über die gemeinsame Nutzung von Daten lässt sich deine Nutzung leichter nachverfolgen, vor allem, wenn einer dieser Dienste angegriffen wird, da die Telefonnummer oft **nicht** verschlüsselt ist.

Wenn möglich, solltest du deine echte Telefonnummer nicht herausgeben. Einige Dienste gestatten die Verwendung von VOIP-Nummern, die jedoch häufig Betrugserkennungssysteme auslösen und zur Sperrung eines Kontos führen, weshalb wir dies für wichtige Konten nicht empfehlen.

In vielen Fällen musst du eine Nummer angeben, unter der du SMS oder Anrufe empfangen kannst, insbesondere bei internationalen Einkäufen, falls es bei der Grenzkontrolle Probleme mit deiner Bestellung gibt. Es ist üblich, dass Dienste deine Nummer als Verifizierungsmethode verwenden; lasse es nicht zu, dass du aus einem wichtigen Konto ausgesperrt wirst, weil du clever sein und eine falsche Nummer angeben willst!

### Benutzername und Passwort

Bei einigen Diensten kannst du dich ohne E-Mail-Adresse anmelden und musst nur einen Benutzernamen und ein Passwort festlegen. Diese Dienste können in Kombination mit einem VPN oder Tor mehr Anonymität bieten. Denke daran, dass es für diese Konten höchstwahrscheinlich **keine Möglichkeit gibt, dein Konto wiederherzustellen**, falls du deinen Benutzernamen oder dein Passwort vergisst.
