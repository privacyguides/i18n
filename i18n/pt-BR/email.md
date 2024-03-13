---
meta_title: "Recomendações de E-mail Privado Criptografado — Privacy Guides"
title: "Serviços de Email"
icon: material/email
description: Esses provedores de email oferecem um ótimo lugar para armazenar seus emails de forma segura, e muitos oferecem criptografia OpenPGP compatível com outros provedores.
cover: email.webp
---

O "email" é praticamente uma necessidade para usar qualquer serviço “online”, contudo não o recomendamos para conversas pessoais. Ao invés de utilizar email para falar com outras pessoas, considere utilizar um meio de mensagens instantâneas que suporte sigilo encaminhado.

[Mensageiros Instantâneos Recomendados](real-time-communication.md ""){.md-button}

Para qualquer outra coisa, recomendamos uma variedade de provedores de email baseados em modelos de negócio sustentáveis e recursos de segurança e privacidade incorporados.

- [OpenPGP-Compatible Email Providers :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Other Encrypted Providers :material-arrow-right-drop-circle:](#more-providers)
- [Email Aliasing Services :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Self-Hosted Options :material-arrow-right-drop-circle:](#self-hosting-email)

## Serviços Compatíveis com OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Por exemplo, um usuário do Proton Mail pode mandar uma mensagem E2E para um usuário de Mailbox.org, ou você pode receber notificações criptografadas por OpenPGP de serviços de internet que suportam isso.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![logo do Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** é um serviço de email com foco na privacidade, criptografia, segurança, e facilidade de uso. Eles estão operando desde **2013**. Proton AG é localizado em Genève, Suíça. As contas começam com 500 MB de armazenamento com seu plano grátis.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Contas gratuitas têm algumas limitações, como não poderem pesquisar no corpo de texto e não ter acesso à [Ponte Proton Mail](https://proton.me/mail/bridge), o que é requerido para usar um [cliente de email desktop recomendado](email-clients.md) (ex. Thunderbird). Contas pagas incluem funcionalidades como a Ponte Proton Mail, mais armazenamento, e suporte para domínios customizados. Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

Se você tem o Proton Unlimited, Bussiness, ou Visionary Plan, você também ganha o [SimpleLogin](#simplelogin) Premium de graça.

O Proton Mail tem relatórios internos de travamento que eles **não** compartilham com terceiros. Isto pode ser desativado em: **Configurações** > **Vá para Configurações** > **Conta** > **Segurança e privacidade** > **Enviar relatórios de erro**.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Assinantes pagos do Proton Mail podem usar seu próprio domínio com o serviço ou um endereço de [pega-tudo (catch-all)](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Proton Mail [aceita](https://proton.me/support/payment-options) dinheiro por correio, para além dos pagamentos normais com cartão de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Segurança da Conta

Proton Mail suporta TOTP [autenticação de dois factores](https://proton.me/support/two-factor-authentication-2fa) e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) utilizando as normas FIDO2 ou U2F. O uso de uma chave de segurança de hardware requer a configuração da autenticação de dois fatores TOTP primeiro.

#### :material-check:{ .pg-green } Segurança dos Dados

Proton Mail tem [criptografia de acesso zero](https://proton.me/blog/zero-access-encryption) em repouso para seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Os dados protegidos com criptografia de acesso zero só são acessíveis por você.

Certas informações armazenadas no [Proton Contacts](https://proton.me/support/proton-contacts), como nomes de exibição e endereços de e-mail, não são protegidas com criptografia de acesso zero. Campos de contatos que suportam criptografia de acesso zero, tais como números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Criptografia do Email

Proton Mail [tem criptografia OpenPGP integrada](https://proton.me/support/how-to-use-pgp) em seu webmail. E-mails para outras contas do Proton Mail são criptografados automaticamente, e criptografia para endereços não-Proton Mail com uma chave OpenPGP pode ser facilmente ativada nas configurações da sua conta. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Isso permite que as pessoas que não usam o Proton Mail encontrem as chaves OpenPGP de contas Proton Mail facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Se você tiver uma conta paga e sua conta [não for paga](https://proton.me/support/delinquency) após 14 dias, você não será capaz de acessar seus dados. Após 30 dias, a sua conta ficará inadimplente e não receberá novos e-mails. Você continuará a ser cobrado durante este período.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Proton Mail oferece uma conta "Ilimitada" por 9,99 euros/mês, que também permite o acesso ao Proton VPN, além de fornecer várias contas, domínios, pseudônimos e 500 GB de armazenamento.

O Proton Mail não oferece um recurso de legado digital.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and privately powered by 100% eco-friendly energy. They have been in operation since 2014. Mailbox.org is based in Berlin, Germany. Accounts start with 2 GB of storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Mailbox.org não aceita nenhuma criptomoeda como resultado do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. No entanto, eles aceitam dinheiro por correio, pagamento em dinheiro para conta bancária, transferência bancária, cartão de crédito, PayPal e alguns processadores específicos da Alemanha: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da Conta

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Padrões da Web como [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportados.

#### :material-information-outline:{ .pg-blue } Segurança dos Dados

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Novas mensagens que você receber serão imediatamente criptografadas com a sua chave pública.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. Uma [opção autônoma](calendar.md) pode ser mais apropriada para essas informações.

#### :material-check:{ .pg-green } Criptografia do Email

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Esse recurso é útil quando o destinatário remoto não tem OpenPGP e não pode descriptografar uma cópia do e-mail em sua própria caixa de correio.

Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isso permite que pessoas fora do Mailbox.org encontrem as chaves OpenPGP de contas Mailbox.org facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Sua conta será definida como uma conta de usuário restrita quando o contrato terminar, após [30 dias ela será irrevogavelmente excluída](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). No entanto, sua interface webmail não pode ser acessada através do seu serviço ".onion" e você pode experimentar erros de certificado TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), além dos protocolos de acesso padrão como IMAP e POP3.

Mailbox.org tem um recurso de legado digital para todos os planos. Você pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Como alternativa, você pode nomear uma pessoa através do seu nome e endereço.

## Mais Provedores

Estes provedores armazenam os seus e-mails com criptografia de conhecimento zero, o que os torna excelentes opções para manter seguros os seus e-mails armazenados. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Métodos de Pagamento Privados

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Segurança da Conta

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Segurança dos Dados

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). Isso significa que as mensagens e outros dados armazenados em sua conta só são legíveis por você.

#### :material-information-outline:{ .pg-blue } Criptografia do Email

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. Você poderá reutilizar uma conta gratuita desativada se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect). Isso garante que o contato do cliente com a empresa use o E2EE. O recurso custa 240 euros por ano.

Tuta doesn't offer a digital legacy feature.

## Serviços de Disfarce de Email

Um serviço de disfarce de e-mail permite que você gere facilmente um novo endereço de e-mail para cada site em que se registrar. Os e-mails alternativos que você gera são encaminhados para um endereço de e-mail que você escolher, ocultando o seu endereço de e-mail "principal" e a identidade do seu provedor de email. Um verdadeiro pseudônimo de e-mail é melhor do que o endereçamento plus comumente usado e suportado por muitos provedores, que permite criar pseudônimos como seunome+[anythinghere]@exemplo.com, porque sites, anunciantes e redes de rastreamento podem remover trivialmente qualquer coisa após o sinal + para saber seu verdadeiro endereço de e-mail.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

Os pseudônimos de e-mail podem funcionar como uma proteção caso seu provedor de e-mail encerre suas atividades. Nesse cenário, você pode facilmente redirecionar seus pseudônimos para um novo endereço de e-mail. Por outro lado, no entanto, você está depositando confiança na continuidade do funcionamento do serviço de pseudônimo.

O uso de um serviço especializado em pseudônimos de e-mail também tem várias vantagens em relação a um pseudônimo "catch-all" genérico de um domínio personalizado:

- Pseudônimos podem ser ativados e desativados individualmente quando você precisar deles, evitando que os sites enviem e-mails aleatórios para você.
- Suas respostas são enviadas pelo endereço de pseudônimo, protegendo seu endereço de e-mail real.

Eles também têm vários benefícios em relação aos serviços de "e-mail temporário":

- Os pseudônimos são permanentes e podem ser ativadas novamente se você precisar receber algo como uma redefinição de senha.
- E-mails são enviados para sua caixa de correio confiável em vez de serem armazenados pelo provedor de pseudônimos.
- Serviços de e-mail temporários normalmente têm caixas de correio públicas que podem ser acessadas por qualquer pessoa que conheça o endereço; os pseudônimos são privados para você.

Nossas recomendações de pseudônimos de e-mail são provedores que permitem que você crie pseudônimos nos domínios que eles controlam, bem como em seu(s) próprio(s) domínio(s) personalizado(s), por uma modesta taxa anual. Eles também podem ser auto-hospedados se você quiser ter o máximo de controle. Contudo, o uso de um domínio personalizado pode ter desvantagens relacionadas à privacidade: Se você for a única pessoa a usar seu domínio personalizado, suas ações poderão ser facilmente rastreadas em todos os sites simplesmente observando o nome do domínio no endereço de e-mail e ignorando tudo antes do sinal de arroba (@).

O uso de um serviço de pseudônimo exige que as mensagens não criptografadas sejam confiadas ao seu provedor de e-mail e ao provedor de pseudônimo. Alguns provedores diminuem um pouco esse problema com a criptografia PGP automática, que reduz o número de partes em que você precisa confiar de duas para uma, criptografando os e-mails recebidos antes de serem entregues ao seu provedor de caixa de correio final.

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email/addy.svg#only-light){ align=right }
![addy.io logo](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentation}
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

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Recursos gratuitos de destaque:

- [x] 10 Pseudônimos Compartilhados
- [x] Pseudônimos Padrão Ilimitados
- [ ] No Outgoing Replies
- [x] 1 Recipient Mailboxes
- [x] Criptografia PGP automática

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logótipo Simplelogin](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** é um serviço gratuito que fornece pseudônimos de e-mail em uma variedade de nomes de domínio compartilhados e, opcionalmente, oferece recursos pagos, como pseudônimos ilimitados e domínios personalizados.

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
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin foi [adquirido pelo Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) a partir de 8 de abril de 2022. Se você usa o Proton Mail como sua caixa de correio principal, o SimpleLogin é uma ótima opção. Como os dois produtos agora pertencem à mesma empresa, você só precisa confiar em uma única entidade. Também esperamos que, no futuro, o SimpleLogin seja mais fortemente integrado às ofertas da Proton. SimpleLogin continua a oferecer suporte ao encaminhamento para qualquer provedor de e-mail de sua escolha. Securitum [audited](https://simplelogin.io/blog/security-audit) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

Você pode vincular sua conta SimpleLogin com sua conta Proton nas configurações. Se você tiver o Proton Unlimited, Business ou Visionary Plan, terá o SimpleLogin Premium gratuitamente.

Recursos gratuitos de destaque:

- [x] 10 Pseudônimos Compartilhados
- [x] Respostas ilimitadas
- [x] 1 Caixa de Correio Destinatária

## Email Auto-Hospedado

Administratores de sistema avançados podem considerar a possibilidade de configurar seu próprio servidor de e-mail. Servidores de correio eletrônico requerem atenção e manutenção contínua para manter as coisas seguras e a entrega de correio eletrônico confiável.

### Soluções combinadas de software

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de correio no Ubuntu. Seu objetivo é facilitar a configuração de seu próprio servidor de e-mail.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

Para uma abordagem mais manual, selecionamos estes dois artigos:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Requisitos

**Por favor, note que não somos afiliados a nenhum dos provedores que recomendamos.** Além de [nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de e-mail que queira ser mencionado, incluindo a implementação de melhores práticas do setor, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

### Tecnologia

Consideramos esses recursos importantes para fornecer um serviço seguro e otimizado. Você deve considerar se o provedor tem os recursos de que você precisa.

**Mínimo Para Qualificação:**

- Criptografa os dados da conta de e-mail em repouso com criptografia de acesso zero.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Melhor Caso:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Privacidade

Preferimos que nossos provedores recomendados coletem o mínimo possível de dados.

**Mínimo Para Qualificação:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Melhor Caso:**

- Aceita [opções de pagamento anônimas](advanced/payments.md) ([criptomoedas](cryptocurrency.md), dinheiro, cartões-presente, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Segurança

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**Mínimo Para Qualificação:**

- Protection of webmail with 2FA, such as TOTP.
- Zero access encryption, builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [Message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Melhor Caso:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programas de recompensa por bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiança

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Exigimos que nossos provedores recomendados sejam transparentes quanto a seus proprietários ou lideranças. Também esperamos ver relatórios de transparência frequentes, especialmente com relação à forma como as solicitações do governo são tratadas.

**Mínimo Para Qualificação:**

- Liderança ou propriedade voltada para o público.

**Melhor Caso:**

- Liderança orientada para o público (usuário).
- Relatórios de transparência frequentes.

### Marketing

With the email providers we recommend we like to see responsible marketing.

**Mínimo Para Qualificação:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Não deve ter nenhum marketing irresponsável:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Garantir 100% de proteção ao anonimato. When someone makes a claim that something is 100% it means there is no certainty for failure. Sabemos que as pessoas podem se desanonimizar facilmente de várias maneiras, por exemplo:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor Caso:**

- Clear and easy to read documentation. This includes things like, setting up 2FA, email clients, OpenPGP, etc.

### Funções Adicionais

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
