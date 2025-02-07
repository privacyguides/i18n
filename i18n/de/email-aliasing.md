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

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as on your own custom domain(s) for a modest yearly fee. They can also be self-hosted if you want maximum control. However, using a custom domain can have privacy-related drawbacks: If you are the only person using your custom domain, your actions can be easily tracked across websites simply by looking at the domain name in the email address and ignoring everything before the at (@) sign.

Using an aliasing service requires trusting both your email provider and your aliasing provider with your unencrypted messages. Some providers mitigate this slightly with automatic PGP encryption[^1], which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases which end in a domain like @[username].addy.io or a custom domain on paid plans. However, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Standard-Aliasnamen
- [ ] Keine ausgehenden Antworten
- [x] 1 Empfänger-Mailbox
- [x] Automatische PGP-Verschlüsselung[^1]

If you cancel your subscription, you will still enjoy the features of your paid plan until the billing cycle ends. After the end of your current billing cycle, most paid features (including any custom domains) will be [deactivated](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), paid account settings will be reverted to their defaults, and catch-all will be enabled if it was previously disabled.

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have Proton Pass Plus, Proton Unlimited, or any multi-user Proton plan, you will have SimpleLogin Premium for free.

Bemerkenswerte kostenlose Funktionen:

- [x] 10 Gemeinsame Aliasnamen
- [x] Unbegrenzte Antworten
- [x] 1 Empfänger-Mailbox
- [ ] Automatische PGP-Verschlüsselung[^1] ist nur bei kostenpflichtigen Tarifen verfügbar

When your subscription ends, all aliases you created will still be able to receive and send emails. However, you cannot create any new aliases that would exceed the free plan limit, nor can you add a new domain, directory, or mailbox.

## Kriterien

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we evaluate email aliasing providers to the same standard as our regular [email provider criteria](email.md#criteria) where applicable. We suggest you familiarize yourself with this list before choosing an email service, and conduct your own research to ensure the provider you choose is the right choice for you.

[^1]: Mit der automatischen PGP-Verschlüsselung kannst du unverschlüsselte eingehende E-Mails verschlüsseln, bevor sie an dein Postfach weitergeleitet werden, sodass dein primärer Mail-Anbieter niemals unverschlüsselte E-Mail-Inhalte sieht.
