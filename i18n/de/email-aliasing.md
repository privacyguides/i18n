---
title: E-Mail-Aliasing
icon: material/email-lock
description: Mit einem E-Mail-Aliasing-Dienst kannst du für jede Website, für die du dich anmeldest, ganz einfach eine neue E-Mail-Adresse generieren.
cover: email-aliasing.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Public Exposure](basics/common-threats.md#limiting-public-information){ .pg-green }

Mit einem **E-Mail-Aliasing-Dienst** kannst du für jede Website, für die du dich anmeldest, ganz einfach eine neue E-Mail-Adresse generieren. Die von dir erstellten E-Mail-Aliase werden dann an eine E-Mail-Adresse deiner Wahl weitergeleitet, wobei sowohl deine "Haupt"-E-Mail-Adresse als auch die Identität deines [E-Mail-Anbieters](email.md) verborgen bleiben. Echtes E-Mail-Aliasing ist besser als die von vielen Providern verwendete und unterstützte Plus-Adressierung, mit der du Aliase wie "meinname+[irgendwashier]@beispiel.com" erstellen kannst, da Websites, Werbetreibende und Tracking-Netzwerke alles nach dem "+"-Zeichen ganz einfach entfernen können. Organisationen wie das [IAB](https://de.wikipedia.org/wiki/Interactive_Advertising_Bureau) verlangen, dass Werbetreibende [E-Mail-Adressen normalisieren](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them), damit sie korreliert und nachverfolgt werden können, ohne Rücksicht auf die Datenschutzwünsche der Nutzer.

<div class="grid cards" markdown>

- ![addy.io Logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email-aliasing.md#addyio)
- ![SimpleLogin Logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

Das E-Mail-Aliasing kann auch als Schutz dienen, falls dein E-Mail-Anbieter einmal seinen Betrieb einstellt. In diesem Fall kannst du deine Aliase einfach an eine neue E-Mail-Adresse weiterleiten. Im Gegenzug vertraust du jedoch darauf, dass der Aliasing-Dienst weiterhin funktioniert.

Die Verwendung eines speziellen E-Mail-Aliasdienstes hat auch eine Reihe von Vorteilen gegenüber einem Catch-All-Alias auf einer benutzerdefinierten Domäne:

- Aliasnamen können bei Bedarf individuell ein- und ausgeschaltet werden, um zu verhindern, dass Websites wahllos E-Mails an dich senden.
- Die Antworten werden von der Alias-Adresse gesendet, sodass deine echte E-Mail-Adresse verborgen bleibt.

Sie haben auch eine Reihe von Vorteilen gegenüber "temporären E-Mail-Diensten":

- Aliase sind dauerhaft und können wieder aktiviert werden, wenn du z. B. ein neues Kennwort erhalten musst.
- E-Mails werden an dein vertrauenswürdiges Postfach gesendet und nicht beim Alias-Anbieter gespeichert.
- Temporäre E-Mail-Dienste haben in der Regel öffentliche Postfächer, auf die jeder zugreifen kann, der die Adresse kennt, während Aliase privat sind.

Unsere E-Mail-Aliasing-Empfehlungen beziehen sich auf Provider, die es dir ermöglichen, gegen eine geringe Jahresgebühr Aliase für die von ihnen kontrollierten Domains sowie für deine eigene(n) benutzerdefinierte(n) Domain(s) zu erstellen. Sie können auch selbst gehostet werden, für maximale Kontrolle. Die Verwendung einer benutzerdefinierten Domain kann jedoch datenschutzbezogene Nachteile haben: Wenn du die einzige Person bist, die deine benutzerdefinierte Domain verwendet, können deine Aktionen auf verschiedenen Websites leicht nachverfolgt werden, indem einfach der Domainname in der E-Mail-Adresse betrachtet und alles vor dem @-Zeichen ignoriert wird.

Die Verwendung eines Alias-Dienstes setzt voraus, dass du sowohl deinem E-Mail-Anbieter als auch deinem Alias-Anbieter deine unverschlüsselten Nachrichten anvertraust. Einige Anbieter entschärfen dieses Problem teils durch automatische PGP-Verschlüsselung[^1], bei der die Anzahl der Parteien, denen du vertrauen musst, von zwei auf eine reduziert wird, indem eingehende E-Mails verschlüsselt werden, bevor sie an deinen endgültigen Mailbox-Anbieter übermittelt werden.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io Logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** lässt dich 10 Domain-Aliase auf einer gemeinsam genutzten Domain kostenlos oder unbegrenzt „Standard“-Aliase erstellen.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/de/firefox/addon/addy_io/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Die Anzahl der geteilten Aliase (die auf eine gemeinsam genutzte Domain wie @addy.io enden), die du erstellen kannst, ist beim kostenlosen Tarif von addy.io auf 10 begrenzt, beim Tarif für 1 €/Monat auf 50 und beim Tarif für 4 €/Monat (der für ein Jahr mit 3 € berechnet wird) unbegrenzt. Du kannst für diese Tarife mit [Kryptowährung](https://addy.io/help/subscribing-with-cryptocurrency) bezahlen oder einen Gutscheincode von [ProxyStore](https://addy.io/help/voucher-codes), addy.io's offiziellem Reseller, erwerben.

Du kannst unbegrenzt viele Standard-Aliase erstellen, die auf eine Domain wie @[Benutzername].addy.io oder eine benutzerdefinierte Domain bei kostenpflichtigen Tarifen enden. Wie bereits erwähnt, kann sich dies jedoch nachteilig auf deine Privatsphäre auswirken, da andere Personen deine Standard-Aliasnamen allein aufgrund des Domainnamens trivialerweise miteinander verknüpfen können. Standard Aliase sind sinnvoll, wenn geteilte Domains von einer Website geblockt werden. Securitum [auditierte](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io im September 2023, wobei keine signifikanten Schwachstellen [identifiziert wurden](https://addy.io/addy-io-security-audit.pdf).

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Standard-Aliasnamen
- [ ] Keine ausgehenden Antworten
- [x] 1 Empfänger-Mailbox
- [x] Automatische PGP-Verschlüsselung[^1]

If you cancel your subscription, you will still enjoy the features of your paid plan until the billing cycle ends. After the end of your current billing cycle, most paid features (including any custom domains) will be [deactivated](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), paid account settings will be reverted to their defaults, and catch-all will be enabled if it was previously disabled.

### SimpleLogin

<div class="admonition recommendation" markdown>

![SimpleLogin Logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.

[:octicons-home-16: Homepage](https://simplelogin.io/de/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<0>Downloads</0>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/de/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff?hl=de-DE)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. Wenn du Proton Pass Plus, Proton Unlimited oder einen anderen Proton Multi-User-Tarif hast, erhältst du SimpleLogin Premium kostenlos.

You can also purchase a voucher code for SimpleLogin Premium anonymously via their official reseller, [ProxyStore](https://simplelogin.io/faq).

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Antworten
- [x] 1 Empfänger-Mailbox
- [ ] Automatische PGP-Verschlüsselung[^1] ist nur bei kostenpflichtigen Tarifen verfügbar

When your subscription ends, all aliases you created will still be able to receive and send emails. However, you cannot create any new aliases that would exceed the free plan limit, nor can you add a new domain, directory, or mailbox.

## Kriterien

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we evaluate email aliasing providers to the same standard as our regular [email provider criteria](email.md#criteria) where applicable. We suggest you familiarize yourself with this list before choosing an email service, and conduct your own research to ensure the provider you choose is the right choice for you.

[^1]: Mit der automatischen PGP-Verschlüsselung kannst du unverschlüsselte eingehende E-Mails verschlüsseln, bevor sie an dein Postfach weitergeleitet werden, sodass dein primärer Mail-Anbieter niemals unverschlüsselte E-Mail-Inhalte sieht.
