---
meta_title: "Recomendações de E-mail Privado Criptografado — Privacy Guides"
title: Serviços de Email
icon: material/email
description: Esses provedores de email oferecem um ótimo lugar para armazenar seus emails de forma segura, e muitos oferecem criptografia OpenPGP compatível com outros provedores.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protege contra as seguintes ameaça(s):</small>

- [:material-server-network: Provedores de serviços](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

O "email" é praticamente uma necessidade para usar qualquer serviço “online”, contudo não o recomendamos para conversas pessoais. Ao invés de utilizar email para falar com outras pessoas, considere utilizar um meio de mensagens instantâneas que suporte sigilo encaminhado.

[Mensageiros Instantâneos Recomendados](real-time-communication.md ""){.md-button}

## Provedores Recomendados

Para qualquer outra coisa, recomendamos uma variedade de provedores de email baseados em modelos de negócio sustentáveis e recursos de segurança e privacidade incorporados. Leia nossa [lista completa de requisitos](#criteria) para mais informações.

| Provedor                      | OpenPGP / WKD                          | IMAP / SMTP                                                    | Zero-Access Encryption                                 | Métodos de Pagamento Anônimos         |
| ----------------------------- | -------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------ | ------------------------------------- |
| [Proton Mail](#proton-mail)   | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Planos pagos apenas | :material-check:{ .pg-green }                          | Dinheiro                              |
| [Mailbox Mail](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                  | :material-information-outline:{ .pg-blue } Mail apenas | Dinheiro                              |
| [Tuta](#tuta)                 | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                         | :material-check:{ .pg-green }                          | Monero <br>Cash via third party |

Além de (ou ao invés de) um provedor de e-mail recomendado aqui, você pode considerar um [serviço de aliasing de e-mail](email-aliasing.md#recommended-providers), para proteger sua privacidade. Entre outras coisas, esses serviços podem ajudar a proteger sua caixa de entrada real contra spam, impedir que marketeiros correlacionem suas contas, e criptografia de todas as mensagens recebidas com PGP.

- [Saiba mais :material-arrow-right-drop-circle:](email-aliasing.md)

## Serviços Compatíveis com OpenPGP

Esses provedores suportam nativamente a criptação/decriptação do OpenPGP e o padrão do[Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), possibilitando *e-mails* criptografados independente do provedor. Por exemplo, um usuário do Proton Mail pode enviar uma mensagem criptografada para um usuário do Mailbox Mail, ou você poderia receber notificações criptografadas em OpenPGP de serviços de *internet* que as suportam.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ .twemoji } [Mailbox Mail](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Aviso</p>

Ao usar a tecnologia E2EE, como o OpenPGP, seu e-mail ainda terá alguns metadados que não são criptografados no cabeçalho do e-mail, geralmente incluindo a linha de assunto! Leia mais sobre [metadados de e-mail](basics/email-security.md#email-metadata-overview).

OpenPGP também não suporta segredos futuros. Ou seja, se a sua chave privada ou a do recipiente forem vazadas, todas as mensagens criptografadas com elas serão expostas.

- [Como que eu protejo minhas chaves privadas? (em inglês)](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![logo do Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** é um serviço de email com foco na privacidade, criptografia, segurança, e facilidade de uso. Eles estão operando desde 2013. A Proton AG está sedeada em Genebra, na Suíça.

O plano Proton Free vem com 500 MB de armazenamento para <em>e-mails</em>. Onde é possível aumentar para até 1 GB de graça.

[:octicons-home-16: Página inicial](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Serviço Onion" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Política de Privacidade" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Código Fonte" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Contas gratuitas têm algumas limitações, como não poder pesquisar o corpo do texto e não terem acesso ao [Proton Mail Bridge](https://proton.me/mail/bridge), necessário para usar um dos [clientes de *e-mail* recomendados](email-clients.md) (por exemplo, o Thunderbird). Contas pagas incluem funcionalidades como a Ponte Proton Mail, mais armazenamento, e suporte para domínios customizados. Se você tem o Proton Unlimited, Bussiness, ou Visionary Plan, você também ganha o [SimpleLogin](#simplelogin) Premium de graça.

Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

O Proton Mail tem relatórios internos de travamento que eles **não** compartilham com terceiros. Isso pode ser desativado no aplicativo Web: :gear: → **Todas as configurações** → **Conta** → **Segurança e privacidade** → **Privacidade e coleta de dados**.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Assinantes pagos do Proton Mail podem usar seu próprio domínio com o serviço ou um endereço de [pega-tudo (catch-all)](https://proton.me/support/catch-all). Proton Mail também suporta [subendereçamento](https://proton.me/support/creating-aliases), o que é útil para as pessoas que não querem comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Proton Mail [aceita](https://proton.me/support/payment-options) **dinheiro** por correio além de cartões de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e pagamentos pelo PayPal.

#### :material-check:{ .pg-green } Segurança da Conta

O Proton Mail suporta [autenticação de dois fatores](https://proton.me/support/two-factor-authentication-2fa) TOTP e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) usando os padrões FIDO2 ou U2F. O uso de uma chave de segurança de hardware requer a configuração da autenticação de dois fatores TOTP primeiro.

#### :material-check:{ .pg-green } Segurança dos Dados

Proton Mail tem [criptografia de acesso zero](https://proton.me/blog/zero-access-encryption) em repouso para seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Os dados protegidos com criptografia de acesso zero só são acessíveis por você.

Certas informações armazenadas no [Proton Contacts](https://proton.me/support/proton-contacts), como nomes de exibição e endereços de e-mail, não são protegidas com criptografia de acesso zero. Campos de contatos que suportam criptografia de acesso zero, tais como números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Criptografia do Email

Proton Mail [tem criptografia OpenPGP integrada](https://proton.me/support/how-to-use-pgp) em seu webmail. E-mails para outras contas do Proton Mail são criptografados automaticamente, e criptografia para endereços não-Proton Mail com uma chave OpenPGP pode ser facilmente ativada nas configurações da sua conta. Proton também suporta descoberta automática de chave externa com WKD. Isso significa que os e-mails enviados a outros provedores que usam o WKD também serão criptografados automaticamente com o OpenPGP, sem a necessidade de trocar manualmente chaves PGP públicas com seus contatos. Eles também permitem que você [criptografe mensagens para endereços não-Proton Mail](https://proton.me/support/password-protected-emails) sem a necessidade de eles se cadastrarem com uma conta Proton Mail ou usar programas como OpenPGP.

O Proton Mail também publica as chaves públicas das contas Proton via HTTP a partir de seu WKD. Isso permite as pessoas que não usam Proton Mail a acharem as chaves OpenPGP de contas do Proton Mail para E2F entre provedores. Isso só se aplica a endereços de *e-mail* que terminam em um dos domínios da Proton, como `@proton.me`. Se você usa um domínio customizado, você deve [configurar o WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separadamente.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Se você tiver uma conta paga e sua conta [não for paga](https://proton.me/support/delinquency) após 14 dias, você não será capaz de acessar seus dados. Após 30 dias, a sua conta ficará inadimplente e não receberá novos e-mails. Você continuará a ser cobrado durante este período. A Proton [excluirá as contas gratuitas inativas](https://proton.me/support/inactive-accounts) após um ano. **Não é possível** reutilizar o endereço de e-mail de uma conta desativada.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

O plano [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) do Proton Mail também permite acesso a outros serviços da Proton, além de prover domínios customizados, aliases hide-my-email infinitos e 500 GB de armazenamento.

### Mailbox Mail

<div class="admonition recommendation" markdown>

![Mailbox Mail logo](assets/img/email/mailbox-mail.svg){ align=right }

**Mailbox Mail** é um serviço de *e-mail* com um foco em ser seguro, livre de anúncios e energizado 100% por energia verde. Eles estão operando desde 2014. Mailbox Mail é localizado em Berlim, Alemanha.

Contas começam com até 2 GB de armazenamento, que pode ser melhorado quando preciso.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Mailbox Mail deixa você utilizar seu próprio domínio e eles suportam endereços [*catch-all*](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox Mail também suporta [sub-endereços](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), o que é útil se você não quiser comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Mailbox Mail não aceita nenhuma criptomoeda, pois seu processador de pagamentos, BitPay, encerrou suas operações na Alemanha. Porém, eles aceitam **dinheiro** por correio, pagamentos diretos para a conta bancária, transferência de banco, cartões de crédito, PayPal e dois processadores específicos da Alemanha: Paydirekt e Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da Conta

Mailbox Mail suporta [autenticação por dois fatores](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) apenas para o *webmail*. You can use either TOTP or a [YubiKey](security-keys.md#yubikey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Segurança dos Dados

Mailbox Mail allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Novas mensagens que você receber serão imediatamente criptografadas com a sua chave pública.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox Mail, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Criptografia do Email

Mailbox Mail has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox Mail's servers. Esse recurso é útil quando o destinatário remoto não tem OpenPGP e não pode descriptografar uma cópia do e-mail em sua própria caixa de correio.

Mailbox Mail also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox Mail to find the OpenPGP keys of Mailbox Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox Mail's own domains, like `@mailbox.org`. Se você usa um domínio customizado, você deve [configurar o WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separadamente.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Sua conta será definida como uma conta de usuário restrita quando o contrato terminar. Ele será excluído de forma irrevogável após [30 dias](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

You can access your Mailbox Mail account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). A interface de webmail não pode ser acessada pelo serviço .onion e você pode encontrar alguns erros com certificados TLS.

Todas as contas vêm com armazenamento limitado na nuvem que [pode ser criptografado](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox Mail also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox Mail also supports [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) in addition to standard access protocols like IMAP and POP3.

Mailbox Mail has a digital legacy feature for all plans. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Como alternativa, você pode nomear uma pessoa através do seu nome e endereço.

## Mais Provedores

Estes provedores armazenam os seus e-mails com criptografia de conhecimento zero, o que os torna excelentes opções para manter seguros os seus e-mails armazenados. No entanto, eles não suportam padrões de criptografia interoperáveis para comunicações ponta-a-ponta (E2EE) entre provedores.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (anteriormente *Tutanota*) é um serviço de e-mail com foco na segurança e privacidade por meio do uso de criptografia. Tutá está em funcionamento desde 2011 e está com sede em Hanover, Alemanha.

Free accounts start with 1 GB of storage.

[:octicons-home-16: Página inicial](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Código fonte" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta não é compatível com o [protocolo IMAP](https://tuta.com/support#imap) nem com o uso de [clientes de e-mail](email-clients.md) de terceiros, e você também não poderá adicionar [contas de e-mail externas](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) ao aplicativo Tuta. [A importação de e-mails](https://github.com/tutao/tutanota/issues/630) também não é suportada no momento, embora isso deva [ser alterado](https://tuta.com/blog/kickoff-import). E-mails podem ser exportados [individualmente ou por seleção em massa](https://tuta.com/support#generalMail) por pasta, o que pode ser inconveniente se você tiver muitas pastas.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Contas pagas da Tuta podem usar 15 ou 30 pseudônimos, dependendo do plano, e pseudônimos ilimitados em [domínios personalizados](https://tuta.com/support#custom-domain). Tutá não permite [subendereçamento (mais endereços)](https://tuta.com/support#plus), mas você pode usar um [catch-all](https://tuta.com/support#settings-global) com um domínio personalizado.

#### :material-information-outline:{ .pg-blue } Métodos de Pagamento Privados

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Segurança da Conta

Também há  suporte à [autenticação de dois fatores](https://tuta.com/support#2fa) com TOTP ou U2F.

#### :material-check:{ .pg-green } Segurança dos Dados

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Isso significa que as mensagens e outros dados armazenados em sua conta só são legíveis por você.

#### :material-information-outline:{ .pg-blue } Criptografia do Email

A Tuta [não usa o OpenPGP](https://tuta.com/support/#pgp). Contas Tuta só podem receber e-mails criptografados de contas de e-mail não-Tuta quando enviados através de uma [caixa de correio temporária do Tutanota](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

A Tuta excluirá [as contas gratuitas inativas](https://tuta.com/support#inactive-accounts) após seis meses. Você poderá reutilizar uma conta gratuita desativada se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Tuta oferece a versão comercial do [Tuta para organizações sem fins lucrativos](https://tuta.com/blog/secure-email-for-non-profit) de graça ou com desconto.

## Requisitos

**Por favor, note que não somos afiliados a nenhum dos provedores que recomendamos.** Além de [nosso critério básico](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de e-mail que queira ser mencionado, incluindo a implementação de melhores práticas do setor, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

### Tecnologia

Consideramos esses recursos importantes para fornecer um serviço seguro e otimizado. You should consider whether the provider has the features you require.

**Mínimo Para Qualificação:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Nomes de domínio personalizados são importantes para os usuários, porque lhes permite manter sua agência a partir do serviço. Deve piorar ou ser adquirido por outra empresa que não priorize a privacidade.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Melhor Caso:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Suporte para uma caixa de correio temporária para usuários externos. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Estes e-mails geralmente têm um tempo de vida limitado e depois são automaticamente excluídos. Eles também não exigem que o destinatário configure nenhuma criptografia, como o OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Nomes de domínio personalizados são importantes para os usuários, porque lhes permite manter sua agência a partir do serviço. Deve piorar ou ser adquirido por outra empresa que não priorize a privacidade.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Privacidade

Preferimos que nossos provedores recomendados coletem o mínimo possível de dados.

**Mínimo Para Qualificação:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Melhor Caso:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Segurança

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Mínimo Para Qualificação:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. O provedor não tem as chaves de descriptografia dos dados que possui. Isso evita que um funcionário desonesto vaze os dados aos quais tem acesso ou que um adversário remoto libere os dados que roubou ao obter acesso não autorizado ao servidor.
- Suporte a [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nenhum erro ou vulnerabilidade de TLS ao ser analisado por ferramentas como [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) ou [Qualys SSL Labs](https://ssllabs.com/ssltest); isso inclui erros relacionados a certificados e parâmetros DH fracos, como os que levaram ao [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Uma política válida de [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registros [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) válidos.
- Registros [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) válidos.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Se a autenticação DMARC estiver sendo usada, a política deve ser definida como `rejeitar` ou `em quarentena`.
- Uma preferência de suíte de servidor de TLS 1.2 ou posterior e um plano para [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Envio [SMTPS](https://en.wikipedia.org/wiki/SMTPS), assumindo que o SMTP seja usado.
- Padrões de segurança do site, como:
    - [HTTP Segurança de Transporte Estrita](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridade do sub-recurso](https://en.wikipedia.org/wiki/Subresource_Integrity) se estiver carregando coisas de domínios externos.
- Deve suportar a visualização de [cabeçalhos de mensagens](https://en.wikipedia.org/wiki/Email#Message_header), pois esse é um recurso forense crucial para determinar se um e-mail é uma tentativa de phishing.

**Melhor Caso:**

- Should support hardware authentication, i.e. U2F e [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registro de recurso de autorização de autoridade de certificação (CAA) do DNS](https://tools.ietf.org/html/rfc6844), além do suporte a DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Programas de recompensa por bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Padrões de segurança do site, tais como:
    - [Política de segurança de conteúdo (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiança

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Exigimos que nossos provedores recomendados sejam transparentes quanto a seus proprietários ou lideranças. Também esperamos ver relatórios de transparência frequentes, especialmente com relação à forma como as solicitações do governo são tratadas.

**Mínimo Para Qualificação:**

- Liderança ou propriedade voltada para o público.

**Melhor Caso:**

- Relatórios de transparência frequentes.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Mínimo Para Qualificação:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor Caso:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Funções Adicionais

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
