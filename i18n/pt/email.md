---
meta_title: "Recomendações de Correio Eletrónico Privado Encriptado - Privacy Guides"
title: "Serviços de Correio Eletrónico"
icon: material/email
description: Estes fornecedores de correio eletrónico são um excelente local para armazenar as suas mensagens eletrónicas em segurança e muitos oferecem encriptação OpenPGP interoperável com outros fornecedores.
cover: email.webp
---

O correio eletrónico é praticamente uma necessidade para subscrever qualquer serviço online, mas não o recomendamos para conversas pessoais. Em vez de utilizar o correio eletrónico para contactar outras pessoas, considere a possibilidade de utilizar uma aplicação de mensagens instantâneas que suporte encaminhamento sigiloso.

[Aplicações de Mensagens Instantâneas Recomendadas](real-time-communication.md ""){.md-button}

Para tudo o resto, recomendamos uma variedade de fornecedores de e-mail baseados em modelos de negócio sustentáveis e que incorporem funcionalidades de segurança e de privacidade.

- [Fornecedores de Correio Eletrónico Compatíveis com OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Outros Fornecedores com Encriptação :material-arrow-right-drop-circle:](#more-providers)
- [Serviços de Aliasing de Correio Eletrónico :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Opções Auto-Hospedadas :material-arrow-right-drop-circle:](#self-hosting-email)

## Serviços Compatíveis com OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Por exemplo, um utilizador do Proton Mail pode enviar uma mensagem E2EE a um utilizador do Mailbox.org, ou pode receber notificações encriptadas em OpenPGP de serviços Internet que o suportem.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using E2EE technology like OpenPGP your email will still have some metadata that is not encrypted in the header of the email, generally including the subject line! Read more about [email metadata](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support Forward secrecy, which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logótipo Proton Mail](assets/img/email/protonmail.svg){ align=right }

O **Proton Mail** é um serviço de e-mail que privilegia a privacidade, a encriptação, a segurança e a facilidade de utilização. Estão em funcionamento desde **2013**. A Proton AG tem sede em Genebra, na Suíça. As contas gratuitas disponibilizam 500 MB de armazenamento.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

As contas gratuitas têm algumas limitações, tais como a impossibilidade de pesquisar o corpo do texto e o facto de não terem acesso ao [Proton Mail Bridge](https://proton.me/mail/bridge), que é necessário para utilizar um [cliente recomendado de e-mail para PC](email-clients.md) (por exemplo, Thunderbird). As contas pagas incluem funcionalidades como o Proton Mail Bridge, armazenamento adicional e suporte para domínios personalizados. A [Securitum](https://research.securitum.com) [certificou](https://proton.me/blog/security-audit-all-proton-apps) as aplicações do Proton Mail, em 9 de novembro de 2021.

Se tiver o Plano Proton Unlimited, Business ou Visionary, poderá usar o [SimpleLogin](#simplelogin) Premium gratuitamente.

O Proton Mail tem relatórios internos de falhas que **não** partilham com terceiros. Verifique "Criptografia de E-mail".

#### :material-check:{ .pg-green } Domínios e aliases personalizados

Os subscritores do Proton Mail podem utilizar o seu próprio domínio com o serviço ou um endereço [catch-all](https://proton.me/support/catch-all). O Proton Mail também suporta [sub-endereçamento](https://proton.me/support/creating-aliases), o que é útil para as pessoas que não querem comprar um domínio.

#### :material-check:{ .pg-green } Métodos de pagamento privados

O Proton Mail [aceita](https://proton.me/support/payment-options) dinheiro por correio, para além dos pagamentos normais com cartão de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Segurança da conta

O Proton Mail suporta TOTP [autenticação de dois fatores](https://proton.me/support/two-factor-authentication-2fa) e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) utilizando as normas FIDO2 ou U2F. A utilização de uma chave de segurança de hardware requer a configuração prévia da autenticação de dois fatores TOTP.

#### :material-check:{ .pg-green } Segurança dos dados

O Proton Mail tem [encriptação de acesso zero](https://proton.me/blog/zero-access-encryption) no estado de repouso para os seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Só você pode aceder aos dados protegidos com encriptação de acesso zero.

Certas informações armazenadas em [Proton Contactos](https://proton.me/support/proton-contacts), tais como nomes de apresentação e endereços de e-mail, não estão protegidas por encriptação de acesso zero. Os campos dos contactos que suportam encriptação de acesso zero, como os números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Encriptação de e-mail

O Proton Mail tem [encriptação OpenPGP integrada](https://proton.me/support/how-to-use-pgp) no seu webmail. Os e-mails para outras contas do Proton Mail são encriptados automaticamente e a encriptação para endereços que não sejam do Proton Mail com uma chave OpenPGP pode ser ativada facilmente nas definições da sua conta. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD, such as Skiff Mail, will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Isto permite que as pessoas que não utilizam o Proton Mail encontrem facilmente as chaves OpenPGP das contas do Proton Mail, para E2EE entre fornecedores. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Se tiver uma conta paga e passarem 14 dias da data de pagamento [sem que seja paga](https://proton.me/support/delinquency), não poderá aceder aos seus dados. Decorridos 30 dias, a sua conta ficará em situação de incumprimento e não receberá e-mails. A faturação continuará a ser processada durante esse período.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

O Proton Mail oferece uma conta "Ilimitada" por 9,99 euros/mês, que também permite o acesso ao Proton VPN, para além de fornecer várias contas, domínios, pseudónimos e 500 GB de armazenamento.

O Proton Mail não oferece funcionalidade de legado digital.

### Skiff Mail

<div class="admonition recommendation" markdown>

![Logótipo do Skiff Mail](assets/img/email/skiff-mail.svg){ align=right }

O **Skiff Mail** é um serviço de correio eletrónico baseado na web com E2EE que começou em 2020 e está sediado em São Francisco com programadores em todo o mundo. As contas começam com 10 GB de armazenamento gratuito.

[:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
[:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
- [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
- [:octicons-browser-16: Web](https://app.skiff.com/mail)

</details>

</div>

O Skiff foi objeto de algumas [auditorias](https://skiff.com/transparency) durante o seu desenvolvimento.

#### :material-check:{ .pg-green } Domínios e aliases personalizados

Pode criar até 3 aliases de endereço eletrónico @skiff.com adicionais para além do endereço de conta principal no plano gratuito. Free accounts can add 1 [custom domain](https://skiff.com/blog/custom-domain-setup), and up to 15 custom domains on a paid plan. You can create unlimited aliases or a [catch-all](https://skiff.com/blog/catch-all-email-alias) alias on your custom domain.

#### :material-alert-outline:{ .pg-orange } Métodos de Pagamento Privados

O Skiff Mail aceita pagamentos em criptomoeda via Coinbase Commerce, incluindo Bitcoin e Ethereum, mas eles não aceitam nossa [criptomoeda](cryptocurrency.md) recomendada, Monero. Também aceitam pagamentos com cartão de crédito através do Stripe.

#### :material-check:{ .pg-green } Segurança da conta

O Skiff Mail suporta autenticação de dois fatores TOTP e chaves de segurança de hardware utilizando as normas FIDO2 ou U2F. A utilização de uma chave de segurança de hardware requer a configuração prévia da autenticação de dois fatores TOTP.

#### :material-check:{ .pg-green } Segurança dos Dados

O Skiff Mail tem encriptação de acesso zero em repouso para todos os seus dados. Isto significa que as mensagens e outros dados armazenados na sua conta só podem ser lidos por si.

#### :material-check:{ .pg-green } Encriptação de e-mail

Skiff Mail encrypts messages to other Skiff mailboxes automatically with E2EE. On December 18th, 2023, Skiff added support for PGP and automatic public key discovery via Web Key Directory (WKD). This means that emails sent to other providers which use WKD, such as Proton Mail, will be automatically encrypted with OpenPGP as well without the need to exchange public PGP keys with your contacts. New Skiff Mail accounts should have a PGP key automatically generated, while accounts from before this feature was introduced need to generate a new PGP key for their address (or upload an existing private key) in the account's address settings. Skiff Mail only has support for reading messages encrypted with PGP/MIME, not the older PGP/Inline standard. Sending messages with PGP/MIME is the [recommended approach](https://www.gnupg.org/faq/gnupg-faq.html#use_pgpmime), but may pose compatibility issues in some edge cases.

Skiff Mail also publishes the public keys of Skiff Mail accounts via HTTP from their [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This allows people who don't use Skiff Mail to find the OpenPGP keys of Skiff Mail accounts easily, for cross-provider E2EE. This only applies to email addresses ending in one of Skiff's own domains, like @skiff.com. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users without OpenPGP cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Remoção da conta

As contas do Skiff Mail não expiram, mas as contas não pagas serão solicitadas a remover quaisquer funcionalidades pagas ativadas (como pseudónimos adicionais) ou a renovar o seu plano antes de a conta poder ser utilizada.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Além disso, o Skiff oferece [funcionalidades de produtividade do espaço de trabalho](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), mas, neste momento, continuamos a preferir [opções alternativas](productivity.md) para colaborar e partilhar ficheiros.

O Skiff Mail não oferece funcionalidade de legado digital.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logótipo Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** é um serviço de e-mail cujo foco é a segurança. Não apresenta nenhum tipo de publicidade e o seu consumo de energia é garantido de forma privada por energia 100% ecológica. Estão em funcionamento desde 2014. A Mailbox.org está sediada em Berlim, na Alemanha. As contas começam com 2 GB de armazenamento, que podem ser incrementados de acordo com as necessidades.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domínios e Aliases Personalizados

O Mailbox.org permite-lhe utilizar o seu próprio domínio e suporta endereços [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). O Mailbox.org também suporta o sub-endereçamento [](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), o que é útil se não quiser comprar um domínio.

#### :material-check:{ .pg-green } Métodos de pagamento privados

O Mailbox.org não aceita quaisquer criptomoedas devido ao facto do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. No entanto, aceitam dinheiro por correio, pagamento em dinheiro para conta bancária, transferência bancária, cartão de crédito, PayPal e alguns serviços de pagamento específicos para a Alemanha: paydirekt e Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da Conta

O Mailbox.org suporta [autenticação de dois fatores](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) apenas para o seu webmail. Pode utilizar o TOTP ou uma [YubiKey](https://en.wikipedia.org/wiki/YubiKey) através da [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Normas Web como a [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportadas.

#### :material-information-outline:{ .pg-blue } Segurança dos dados

O Mailbox.org permite a encriptação do correio recebido utilizando a sua caixa de e-mail encriptada [](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). As novas mensagens recebidas serão imediatamente encriptadas com a sua chave pública.

No entanto, a [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), a plataforma de software utilizada pelo Mailbox.org, [não suporta](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) a encriptação do seu livro de endereços e calendário. Uma opção standalone [](calendar.md) pode ser mais adequada para salvaguardar a segurança dessa informação.

#### :material-check:{ .pg-green } Encriptação de e-mail

O Mailbox.org tem [encriptação integrada](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) no seu webmail, o que simplifica o envio de mensagens para pessoas com chaves OpenPGP públicas. Também possibilitam que [destinatários remotos desencriptem uma mensagem de e-mail](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) nos servidores de Mailbox.org. Esta funcionalidade é útil quando o destinatário remoto não tem o OpenPGP e não consegue desencriptar uma cópia do e-mail na sua própria caixa de correio.

O Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isto permite que pessoas que não utilizem o Mailbox.org encontrem facilmente as chaves OpenPGP das contas Mailbox.org, para E2EE entre fornecedores. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Remoção da Conta

Após o termo do contrato, a sua conta será definida como uma conta de utilizador restrita. Passados [30 dias será irrevogavelmente eliminada](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidade Adicional

Pode aceder à sua conta Mailbox.org através de IMAP/SMTP utilizando o serviço [.onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). No entanto, a sua interface de webmail não pode ser acedida através do serviço .onion e podem ocorrer erros de certificado TLS.

Todas as contas incluem um armazenamento em nuvem limitado que [pode ser encriptado](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). O Mailbox.org também oferece pseudónimo [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), que força a encriptação TLS na ligação entre servidores de e-mail. Se isso não acontecer, a mensagem não será enviada. O Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), para além dos protocolos de acesso padrão como IMAP e POP3.

O Mailbox.org tem uma funcionalidade de legado digital para todos os planos. Pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Em alternativa, pode nomear uma pessoa, fornecendo o seu nome e endereço.

## Mais Fornecedores

Estes fornecedores armazenam as suas mensagens eletrónicas com encriptação de acesso zero, o que os torna excelentes opções para manter a segurança do seu armazenamento. No entanto, não suportam normas de encriptação interoperáveis para comunicações E2EE entre fornecedores.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg){ align=right }

**Tuta** is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since **2011** and is based in Hanover, Germany. As contas gratuitas disponibilizam 1 GB de armazenamento.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com/)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/faq/#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/posts/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/howto#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Domínios e aliases personalizados

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [subaddressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Métodos de pagamento privados

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/faq/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Segurança da conta

Tuta supports [two factor authentication](https://tuta.com/faq#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Segurança dos dados

Tuta has [zero access encryption at rest](https://tuta.com/faq#what-encrypted) for your emails, [address book contacts](https://tuta.com/faq#encrypted-address-book), and [calendars](https://tuta.com/faq#calendar). Isto significa que as mensagens e outros dados armazenados na sua conta só podem ser lidos por si.

#### :material-information-outline:{ .pg-blue } Encriptação de Correio Eletrónico

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Remoção da conta

Tuta will [delete inactive free accounts](https://tuta.com/faq#inactive-accounts) after six months. Poderá reutilizar uma conta gratuita desativada, se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/posts/secure-email-for-non-profit) for free or with a heavy discount.

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect/). Isto garante que todos os contactos do cliente com a empresa utilizam o E2EE. Esta funcionalidade custa 240 euros por ano.

Tuta doesn't offer a digital legacy feature.

## Serviços de aliasing de e-mail

Um serviço de aliasing de e-mail permite-lhe gerar facilmente um novo endereço de e-mail para cada sítio Web em que efetue um registo. Os aliases de e-mail que gera são depois reencaminhados para um endereço de e-mail à sua escolha, ocultando tanto o seu endereço de e-mail "principal" como a identidade do seu fornecedor de e-mail. Um serviço de aliasing de e-mail é melhor do que o endereçamento plus habitualmente utilizado e suportado por muitos fornecedores, que permite criar aliases como yourname+[anythinghere]@example.com, porque os sites, os anunciantes e as redes de rastreio podem remover trivialmente tudo o que se segue ao sinal + para conhecer o seu verdadeiro endereço de e-mail.

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![SimpleLogin logo](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

O aliasing de e-mail pode funcionar como uma salvaguarda no caso de o seu fornecedor de e-mail cessar atividade. Nesse caso, pode facilmente reencaminhar os seus pseudónimos para um novo endereço de correio eletrónico. No entanto, está a depositar toda confiança apenas no serviço de aliasing para continuar a ter acesso ao seu e-mail.

A utilização de um serviço de aliasing de e-mail dedicado tem uma série de vantagens em relação a um alias global num domínio personalizado:

- Os pseudónimos podem ser ativados e desativados individualmente quando necessário, evitando que os sites enviem mensagens de e-mail de forma aleatória.
- As respostas são enviadas a partir do endereço alias, protegendo o seu endereço de e-mail real.

Têm também uma série de vantagens em relação aos serviços de "e-mail temporário":

- Os pseudónimos são permanentes e podem ser ativados novamente se for necessário receber alguma informação, como por exemplo uma redefinição de palavra-passe.
- Os e-mails são enviados para a sua caixa de correio de confiança, em vez de serem guardados pelo fornecedor do pseudónimo.
- Os serviços de e-mail temporário têm normalmente caixas de correio públicas que podem ser acedidas por qualquer pessoa que conheça o endereço; os pseudónimos são privados.

As nossas recomendações de aliasing de e-mail são fornecedores que lhe permitem criar aliases em domínios que eles controlam, bem como no(s) seu(s) próprio(s) domínio(s) personalizado(s), por uma módica taxa anual. Também podem ser auto-hospedados, caso pretenda um controlo máximo. No entanto, a utilização de um domínio personalizado pode ter desvantagens relacionadas com a privacidade: Se for a única pessoa a utilizar o seu domínio personalizado, as suas ações podem ser facilmente localizadas em todos os sites bastando olhar para o nome do domínio no endereço de e-mail e ignorar tudo o que vem antes do sinal arroba (@).

A utilização de um serviço de aliasing requer a sua confiança no fornecedor de e-mail e no fornecedor de aliasing, no caso das suas mensagens não serem encriptadas. Alguns fornecedores atenuam ligeiramente esta situação com a encriptação PGP automática, o que encripta os e-mails recebidos antes de serem entregues ao fornecedor final de e-mail, reduzindo o número de entidades terceiras em que é necessário confiar, de duas para uma.

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
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

The number of shared aliases (which end in a shared domain like @addy.io) that you can create is limited to 10 on addy.io's free plan, 50 on their $1/month plan and unlimited on the $4/month plan (billed $3 for a year). You can create unlimited standard aliases (which end in a domain like @[username].addy.io or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service. Securitum [audited](https://addy.io/blog/addy-io-passes-independent-security-audit/) addy.io in September 2023 and no significant vulnerabilities [were identified](https://addy.io/addy-io-security-audit.pdf).

Funcionalidades gratuitas dignas de nota:

- [x] 10 Aliases partilhados
- [x] Aliases padrão ilimitados
- [ ] Nenhuma resposta de saída
- [x] 1 Recipient Mailboxes
- [x] Encriptação PGP automática

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logótipo Simplelogin](assets/img/email/simplelogin.svg){ align=right }

O **SimpleLogin** é um serviço gratuito que fornece aliases de e-mail numa variedade de nomes de domínio partilhados e, opcionalmente, fornece funcionalidades pagas, como aliases ilimitados e domínios personalizados.

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

</details>

</div>

O SimpleLogin foi [adquirido pela Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces), em 8 de abril de 2022. Se utiliza o Proton Mail para a sua caixa de correio principal, o SimpleLogin é uma ótima escolha. Uma vez que ambos os produtos são agora propriedade da mesma empresa, só tem de confiar numa única entidade. Também esperamos que o SimpleLogin seja integrado de forma mais estreita com as ofertas da Proton no futuro. O SimpleLogin continua a suportar o reencaminhamento para qualquer fornecedor de e-mail de sua preferência. A Securitum [auditou o](https://simplelogin.io/blog/security-audit/) SimpleLogin no início de 2022 e todas os problemas identificados [foram resolvidos](https://simplelogin.io/audit2022/web.pdf).

Nas definições, pode associar a sua conta SimpleLogin à sua conta Proton. Se tiver o Plano Proton Unlimited, Business ou Visionary, terá o SimpleLogin Premium gratuitamente.

Funcionalidades gratuitas dignas de nota:

- [x] 10 Aliases partilhados
- [x] Respostas ilimitadas
- [x] 1 Caixa de correio do destinatário

## E-mail auto-hospedado

Os administradores de sistemas avançados podem considerar a possibilidade de configurar o seu próprio servidor de e-mail. Os servidores de e-mail requerem atenção e manutenção contínua para se manterem seguros e para que a entrega de e-mail seja fiável.

### Soluções de software combinadas

<div class="admonition recommendation" markdown>

![Logótipo Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** é um servidor de e-mail mais avançado, perfeito para quem tem um pouco mais de experiência em Linux. Tem tudo o que é necessário num contentor Docker: um servidor de e-mail com suporte DKIM, antivírus e monitorização de spam, webmail e ActiveSync com SOGo, e administração baseada na Web com suporte 2FA.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Código-fonte" }
[:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuir }

</div>

<div class="admonition recommendation" markdown>

![Logótipo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de e-mail no Ubuntu. O seu objetivo é facilitar a criação do seu próprio servidor de e-mail.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código-fonte" }

</div>

Para uma abordagem mais manual, selecionámos estes dois artigos:

- [Configurar um servidor de e-mail com OpenSMTPD, Dovecot e Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Como gerir o seu próprio servidor de e-mail](https://www.c0ffee.net/blog/mail-server-guide/) (agosto de 2017)

## Critérios

**Tenha em atenção que não somos afiliados de nenhum dos fornecedores que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), desenvolvemos um conjunto claro de critérios para qualquer fornecedor de e-mail que pretenda ser recomendado, incluindo a implementação das melhores práticas da indústria, tecnologia moderna e muito mais. Sugerimos que se familiarize com esta lista antes de escolher um fornecedor de e-mail e que faça a sua própria pesquisa para garantir que o fornecedor de e-mail que escolher é a escolha certa.

### Tecnologia

Consideramos que estas características são importantes para podermos prestar um serviço seguro e otimizado. Deve garantir que o fornecedor tem as características de que necessita.

**Mínimos de qualificação:**

- Encriptação de todos os dados da conta de e-mail em estado de repouso, com encriptação de acesso zero.
- Capacidade de exportação como [Mbox](https://en.wikipedia.org/wiki/Mbox) ou .eml individual com a norma [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) .
- Permitir que aos utilizadores configurar o seu próprio nome de domínio [](https://en.wikipedia.org/wiki/Domain_name). Os nomes de domínio personalizados são importantes para os utilizadores, porque lhes permitem manter a sua agência do serviço, caso este se torne mau ou seja adquirido por outra empresa que não dê prioridade à privacidade.
- Funciona com uma infraestrutura própria, isto é, não se baseia em fornecedores de serviços de e-mail de terceiros.

**Melhor caso:**

- Encriptação de todos os dados da conta (contactos, calendários, etc.) em estado de repouso, com encriptação de acesso zero.
- Encriptação E2EE/PGP integrada no webmail, fornecida como uma conveniência.
- Suporte para [WKD](https://wiki.gnupg.org/WKD) para permitir uma melhor descoberta de chaves OpenPGP públicas através de HTTP. Os utilizadores do GnuPG podem obter uma chave escrevendo: `gpg --locate-key example_user@example.com`
- Suporte para uma caixa de correio temporária para utilizadores externos. Isto é útil quando se pretende enviar uma mensagem de e-mail encriptada, sem enviar uma cópia real ao destinatário. Estas mensagens de e-mail têm normalmente um tempo de vida limitado e depois são automaticamente eliminadas. Também não requerem que o destinatário configure qualquer criptografia como o OpenPGP.
- Disponibilidade dos serviços do fornecedor de e-mail através de um serviço onion [](https://en.wikipedia.org/wiki/.onion).
- Suporte de [Sub-endereçamento](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
- Funcionalidade de Catch-all ou alias para quem possui os seus próprios domínios.
- Utilização de protocolos normais de acesso ao e-mail, como IMAP, SMTP ou [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Os protocolos de acesso normalizados garantem que os clientes podem transferir facilmente todo o seu e-mail, caso pretendam mudar para outro fornecedor.

### Privacidade

Preferimos que os nossos fornecedores recomendados recolham o mínimo de dados possível.

**Mínimos de qualificação:**

- Proteção do endereço IP do remetente. Filtrar o IP para que não apareça no campo de cabeçalho `Recebido`.
- Não exigir informações de identificação pessoal (PII) para além de um nome de utilizador e uma palavra-passe.
- Política de privacidade que cumpra os requisitos definidos pelo RGPD.

**Melhor caso:**

- Aceitação de [opções de pagamento anónimas](advanced/payments.md) ([criptomoeda](cryptocurrency.md), dinheiro, cartões de oferta, etc.)
- Alojamento numa jurisdição com leis rigorosas de proteção da privacidade do e-mail.

### Segurança

Os servidores de e-mail lidam com uma grande quantidade de dados muito sensíveis. É esperado que os fornecedores adotem as melhores práticas do setor para proteger os seus membros.

**Mínimos de qualificação:**

- Proteção do webmail com 2FA, como o TOTP.
- Encriptação de acesso zero, baseada na encriptação em estado de repouso. Vedar o acesso do fornecedor às chaves de desencriptação dos dados. Isto impede que um funcionário desonesto divulgue os dados a que tem acesso ou que um adversário remoto divulgue os dados que roubou ao obter acesso não autorizado ao servidor.
- [Suporte DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nenhum erro ou vulnerabilidade de TLS ao ser analisado por ferramentas como [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), ou [Qualys SSL Labs](https://www.ssllabs.com/ssltest); isto inclui erros relacionados com certificados e parâmetros DH fracos, como os que levaram a [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Uma opção de suite de servidor (opcional no TLSv1.3) para suites de cifras fortes que suportem encaminhamento sigiloso e encriptação autenticada.
- Uma política válida [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registos [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) válidos.
- Registos [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) válidos.
- Registo e política [DMARC](https://en.wikipedia.org/wiki/DMARC) adequados ou [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) para autenticação. Se estiver a ser utilizada a autenticação DMARC, a política deve ser definida como `reject` ou `quarantine`.
- Uma opção de suite de servidor por TLS 1.2 ou posterior e um plano para [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- Submissão [SMTPS](https://en.wikipedia.org/wiki/SMTPS), assumindo que é utilizado o SMTP.
- Normas de segurança de sites Web, tais como:
    - [Segurança de transporte estrito HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridade do sub-recurso](https://en.wikipedia.org/wiki/Subresource_Integrity) se estiver a carregar dados de domínios externos.
- Suporte para visualização dos cabeçalhos de mensagens [](https://en.wikipedia.org/wiki/Email#Message_header), uma vez que se trata de uma caraterística forense crucial para determinar se uma mensagem de e-mail é uma tentativa de phishing.

**Melhor caso:**

- Suporte para autenticação de hardware, isto é. U2F e [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). O U2F e o WebAuthn são mais seguros porque utilizam uma chave privada, armazenada num dispositivo de hardware do lado do cliente, para efeitos de autenticação, ao contrário de um segredo partilhado que é armazenado no servidor Web e no lado do cliente quando se utiliza o TOTP. Além disso, o U2F e o WebAuthn são mais resistentes ao phishing, uma vez que a sua resposta de autenticação se baseia no nome de domínio autenticado [](https://en.wikipedia.org/wiki/Domain_name).
- [Registo de Recursos de Autorização de Autoridade de Certificação (CAA) do DNS](https://tools.ietf.org/html/rfc6844), para além do suporte DANE.
- Implementação de [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), útil para pessoas que enviam mensagens para listas de e-mail [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programas de recompensa de bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Normas de segurança de sites Web, tais como:
    - [Política de segurança de conteúdo (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Confiança

Se não confiaria as suas finanças a alguém com uma identidade falsa, por que razão deveria confiar-lhe o seu e-mail? Exigimos que os nossos fornecedores recomendados sejam transparentes quanto à sua propriedade ou liderança. Gostaríamos também de ver relatórios de transparência frequentes, especialmente no que diz respeito à forma como os pedidos do governo são tratados.

**Mínimos de qualificação:**

- Liderança ou propriedade virada para o público.

**Melhor caso:**

- Liderança virada para o público.
- Relatórios de transparência frequentes.

### Marketing

Gostaríamos que os fornecedores de e-mail que recomendamos tivessem uma política de marketing responsável.

**Mínimos de qualificação:**

- As estatísticas de análise devem ser auto-hospedados (evitar Google Analytics, Adobe Analytics, etc.). O site do fornecedor deve também estar em conformidade com a política [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track), para quem opte por não participar.

Não deverão ter políticas de marketing irresponsáveis:

- Reivindicações de "encriptação inquebrável" A encriptação deve ser utilizada com a consciência de poder vir a não ser secreta no futuro, quando existir tecnologia para a decifrar.
- Garantir a proteção do anonimato a 100%. Quando alguém afirma que algo é 100%, significa que não há possibilidade de falha. Sabemos que as pessoas podem desanonimizar-se muito facilmente de várias formas, por exemplo:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Impressão digital do browser](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor caso:**

- Documentação clara e fácil de ler. Isto inclui questões como a configuração de 2FA, clientes de e-mail, OpenPGP, etc.

### Funcionalidade adicional

Embora não sejam requisitos obrigatórios, existem outros fatores de conveniência ou privacidade que analisámos ao determinar os fornecedores a recomendar.
