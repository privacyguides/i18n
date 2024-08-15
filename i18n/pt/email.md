---
meta_title: "Recomendações de Correio Eletrónico Privado Encriptado - Privacy Guides"
title: "Serviços de Correio Eletrónico"
icon: material/email
description: Estes fornecedores de correio eletrónico são um excelente local para armazenar as suas mensagens eletrónicas em segurança e muitos oferecem encriptação OpenPGP interoperável com outros fornecedores.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

O correio eletrónico é praticamente uma necessidade para subscrever qualquer serviço online, mas não o recomendamos para conversas pessoais. Em vez de utilizar o correio eletrónico para contactar outras pessoas, considere a possibilidade de utilizar uma aplicação de mensagens instantâneas que suporte encaminhamento sigiloso.

[Aplicações de Mensagens Instantâneas Recomendadas](real-time-communication.md ""){.md-button}

## Provedores recomendados

Para tudo o resto, recomendamos uma variedade de fornecedores de e-mail baseados em modelos de negócio sustentáveis e que incorporem funcionalidades de segurança e de privacidade. Para mais informações, consulte a lista completa de critérios [](#criteria).

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Zero Access Encryption                               | Anonymous Payments            |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Paid plans only | :material-check:{ .pg-green }                        | Dinheiro                      |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Mail only | Dinheiro                      |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Cash via third-party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## Serviços Compatíveis com OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic E2EE emails. Por exemplo, um utilizador do Proton Mail pode enviar uma mensagem E2EE a um utilizador do Mailbox.org, ou pode receber notificações encriptadas em OpenPGP de serviços Internet que o suportem.

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

![Logótipo Proton Mail](assets/img/email/protonmail.svg){ align=right }

O **Proton Mail** é um serviço de e-mail que privilegia a privacidade, a encriptação, a segurança e a facilidade de utilização. They have been in operation since 2013. A Proton AG tem sede em Genebra, na Suíça. The Proton Mail Free plan comes with 500MB of Mail storage, which you can increase up to 1GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

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

As contas gratuitas têm algumas limitações, tais como a impossibilidade de pesquisar o corpo do texto e o facto de não terem acesso ao [Proton Mail Bridge](https://proton.me/mail/bridge), que é necessário para utilizar um [cliente recomendado de e-mail para PC](email-clients.md) (por exemplo, Thunderbird). As contas pagas incluem funcionalidades como o Proton Mail Bridge, armazenamento adicional e suporte para domínios personalizados. A [Securitum](https://research.securitum.com) [certificou](https://proton.me/blog/security-audit-all-proton-apps) as aplicações do Proton Mail, em 9 de novembro de 2021.

If you have the Proton Unlimited, Business, Family, or Visionary plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail has internal crash reports that are **not** shared with third parties. This can be disabled in the web app: :gear: → **All Settings** → **Account** → **Security and privacy** → **Privacy and data collection**.

#### :material-check:{ .pg-green } Domínios e aliases personalizados

Os subscritores do Proton Mail podem utilizar o seu próprio domínio com o serviço ou um endereço [catch-all](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Métodos de pagamento privados

O Proton Mail [aceita](https://proton.me/support/payment-options) dinheiro por correio, para além dos pagamentos normais com cartão de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Segurança da conta

O Proton Mail suporta TOTP [autenticação de dois fatores](https://proton.me/support/two-factor-authentication-2fa) e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) utilizando as normas FIDO2 ou U2F. A utilização de uma chave de segurança de hardware requer a configuração prévia da autenticação de dois fatores TOTP.

#### :material-check:{ .pg-green } Segurança dos dados

O Proton Mail tem [encriptação de acesso zero](https://proton.me/blog/zero-access-encryption) no estado de repouso para os seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Só você pode aceder aos dados protegidos com encriptação de acesso zero.

Certas informações armazenadas em [Proton Contactos](https://proton.me/support/proton-contacts), tais como nomes de apresentação e endereços de e-mail, não estão protegidas por encriptação de acesso zero. Os campos dos contactos que suportam encriptação de acesso zero, como os números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Encriptação de e-mail

O Proton Mail tem [encriptação OpenPGP integrada](https://proton.me/support/how-to-use-pgp) no seu webmail. Os e-mails para outras contas do Proton Mail são encriptados automaticamente e a encriptação para endereços que não sejam do Proton Mail com uma chave OpenPGP pode ser ativada facilmente nas definições da sua conta. Proton also supports automatic external key discovery with [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). This means that emails sent to other providers which use WKD will be automatically encrypted with OpenPGP as well, without the need to manually exchange public PGP keys with your contacts. They also allow you to [encrypt messages to non-Proton Mail addresses without OpenPGP](https://proton.me/support/password-protected-emails), without the need for them to sign up for a Proton Mail account.

Proton Mail also publishes the public keys of Proton accounts via HTTP from their WKD. Isto permite que as pessoas que não utilizam o Proton Mail encontrem facilmente as chaves OpenPGP das contas do Proton Mail, para E2EE entre fornecedores. This only applies to email addresses ending in one of Proton's own domains, like @proton.me. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Se tiver uma conta paga e passarem 14 dias da data de pagamento [sem que seja paga](https://proton.me/support/delinquency), não poderá aceder aos seus dados. Decorridos 30 dias, a sua conta ficará em situação de incumprimento e não receberá e-mails. A faturação continuará a ser processada durante esse período. Proton will [delete inactive free accounts](https://proton.me/support/inactive-accounts) after one year. You **cannot** reuse the email address of a deactivated account.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500GB of storage.

O Proton Mail não oferece funcionalidade de legado digital.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logótipo Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** é um serviço de e-mail cujo foco é a segurança. Não apresenta nenhum tipo de publicidade e o seu consumo de energia é garantido de forma privada por energia 100% ecológica. Estão em funcionamento desde 2014. A Mailbox.org está sediada em Berlim, na Alemanha. Accounts start with up to 2GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domínios e aliases personalizados

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Métodos de pagamento privados

O Mailbox.org não aceita quaisquer criptomoedas devido ao facto do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da conta

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Normas Web como a [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportadas.

#### :material-information-outline:{ .pg-blue } Segurança dos dados

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). As novas mensagens recebidas serão imediatamente encriptadas com a sua chave pública.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. Uma opção standalone [](calendar.md) pode ser mais adequada para salvaguardar a segurança dessa informação.

#### :material-check:{ .pg-green } Encriptação de e-mail

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Esta funcionalidade é útil quando o destinatário remoto não tem o OpenPGP e não consegue desencriptar uma cópia do e-mail na sua própria caixa de correio.

O Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isto permite que pessoas que não utilizem o Mailbox.org encontrem facilmente as chaves OpenPGP das contas Mailbox.org, para E2EE entre fornecedores. This only applies to email addresses ending in one of Mailbox.org's own domains, like @mailbox.org. If you use a custom domain, you must [configure WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Your account will be set to a restricted user account when your contract ends. It will be irrevocably deleted after [30 days](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). No entanto, a sua interface de webmail não pode ser acedida através do serviço .onion e podem ocorrer erros de certificado TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. O Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), para além dos protocolos de acesso padrão como IMAP e POP3.

O Mailbox.org tem uma funcionalidade de legado digital para todos os planos. Pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Em alternativa, pode nomear uma pessoa, fornecendo o seu nome e endereço.

## Mais Fornecedores

Estes fornecedores armazenam as suas mensagens eletrónicas com encriptação de acesso zero, o que os torna excelentes opções para manter a segurança do seu armazenamento. No entanto, não suportam normas de encriptação interoperáveis para comunicações E2EE entre fornecedores.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

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

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Domínios e Aliases Personalizados

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Métodos de pagamento privados

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with Proxystore.

#### :material-check:{ .pg-green } Segurança da Conta

Tuta supports [two factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Segurança dos Dados

Tuta has [zero access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Isto significa que as mensagens e outros dados armazenados na sua conta só podem ser lidos por si.

#### :material-information-outline:{ .pg-blue } Encriptação de Correio Eletrónico

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Remoção da Conta

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. Poderá reutilizar uma conta gratuita desativada, se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidade Adicional

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

Tuta doesn't offer a digital legacy feature.

## E-mail auto-hospedado

Os administradores de sistemas avançados podem considerar a possibilidade de configurar o seu próprio servidor de e-mail. Os servidores de e-mail requerem atenção e manutenção contínua para se manterem seguros e para que a entrega de e-mail seja fiável.

### Soluções de software combinadas

<div class="admonition recommendation" markdown>

![Logótipo Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** é um servidor de e-mail mais avançado, perfeito para quem tem um pouco mais de experiência em Linux. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Logótipo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de e-mail no Ubuntu. O seu objetivo é facilitar a criação do seu próprio servidor de e-mail.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código-fonte" }

</div>

Para uma abordagem mais manual, selecionámos estes dois artigos:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Critérios

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Tecnologia

Consideramos que estas características são importantes para podermos prestar um serviço seguro e otimizado. Deve garantir que o fornecedor tem as características de que necessita.

**Mínimos de qualificação:**

- Encriptação de todos os dados da conta de e-mail em estado de repouso, com encriptação de acesso zero.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Permitir que aos utilizadores configurar o seu próprio nome de domínio [](https://en.wikipedia.org/wiki/Domain_name). Os nomes de domínio personalizados são importantes para os utilizadores, porque lhes permitem manter a sua agência do serviço, caso este se torne mau ou seja adquirido por outra empresa que não dê prioridade à privacidade.
- Funciona com uma infraestrutura própria, isto é, não se baseia em fornecedores de serviços de e-mail de terceiros.

**Melhor caso:**

- Encriptação de todos os dados da conta (contactos, calendários, etc.) em estado de repouso, com encriptação de acesso zero.
- Encriptação E2EE/PGP integrada no webmail, fornecida como uma conveniência.
- Suporte para [WKD](https://wiki.gnupg.org/WKD) para permitir uma melhor descoberta de chaves OpenPGP públicas através de HTTP. Os utilizadores do GnuPG podem obter uma chave escrevendo: `gpg --locate-key example_user@example.com`
- Suporte para uma caixa de correio temporária para utilizadores externos. Isto é útil quando se pretende enviar uma mensagem de e-mail encriptada, sem enviar uma cópia real ao destinatário. Estas mensagens de e-mail têm normalmente um tempo de vida limitado e depois são automaticamente eliminadas. Também não requerem que o destinatário configure qualquer criptografia como o OpenPGP.
- Disponibilidade dos serviços do fornecedor de e-mail através de um serviço onion [](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Os protocolos de acesso normalizados garantem que os clientes podem transferir facilmente todo o seu e-mail, caso pretendam mudar para outro fornecedor.

### Privacidade

Preferimos que os nossos fornecedores recomendados recolham o mínimo de dados possível.

**Mínimos de qualificação:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Não exigir informações de identificação pessoal (PII) para além de um nome de utilizador e uma palavra-passe.
- Política de privacidade que cumpra os requisitos definidos pelo RGPD.

**Melhor caso:**

- Aceitação de [opções de pagamento anónimas](advanced/payments.md) ([criptomoeda](cryptocurrency.md), dinheiro, cartões de oferta, etc.)
- Alojamento numa jurisdição com leis rigorosas de proteção da privacidade do e-mail.

### Segurança

Os servidores de e-mail lidam com uma grande quantidade de dados muito sensíveis. We expect that providers will adopt best industry practices in order to protect their customers.

**Mínimos de qualificação:**

- Proteção do webmail com 2FA, como o TOTP.
- Zero access encryption, which builds on encryption at rest. Vedar o acesso do fornecedor às chaves de desencriptação dos dados. Isto impede que um funcionário desonesto divulgue os dados a que tem acesso ou que um adversário remoto divulgue os dados que roubou ao obter acesso não autorizado ao servidor.
- [Suporte DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Uma opção de suite de servidor (opcional no TLSv1.3) para suites de cifras fortes que suportem encaminhamento sigiloso e encriptação autenticada.
- Uma política válida [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registos [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) válidos.
- Registos [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) válidos.
- Registo e política [DMARC](https://en.wikipedia.org/wiki/DMARC) adequados ou [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) para autenticação. Se estiver a ser utilizada a autenticação DMARC, a política deve ser definida como `reject` ou `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Submissão [SMTPS](https://en.wikipedia.org/wiki/SMTPS), assumindo que é utilizado o SMTP.
- Normas de segurança de sites Web, tais como:
    - [Segurança de transporte estrito HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridade do sub-recurso](https://en.wikipedia.org/wiki/Subresource_Integrity) se estiver a carregar dados de domínios externos.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Melhor caso:**

- Suporte para autenticação de hardware, isto é. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registo de Recursos de Autorização de Autoridade de Certificação (CAA) do DNS](https://tools.ietf.org/html/rfc6844), para além do suporte DANE.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Auditorias de segurança publicadas por uma empresa terceira de renome.
- Programas de recompensa de bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Normas de segurança de sites Web, tais como:
    - [Política de segurança de conteúdo (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiança

Se não confiaria as suas finanças a alguém com uma identidade falsa, por que razão deveria confiar-lhe o seu e-mail? Exigimos que os nossos fornecedores recomendados sejam transparentes quanto à sua propriedade ou liderança. Gostaríamos também de ver relatórios de transparência frequentes, especialmente no que diz respeito à forma como os pedidos do governo são tratados.

**Mínimos de qualificação:**

- Liderança ou propriedade virada para o público.

**Melhor caso:**

- Relatórios de transparência frequentes.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Mínimos de qualificação:**

- As estatísticas de análise devem ser auto-hospedados (evitar Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt out.

Must not have any irresponsible marketing, which can include the following:

- Reivindicações de "encriptação inquebrável" A encriptação deve ser utilizada com a consciência de poder vir a não ser secreta no futuro, quando existir tecnologia para a decifrar.
- Garantir a proteção do anonimato a 100%. Quando alguém afirma que algo é 100%, significa que não há possibilidade de falha. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
    - [Impressão digital do browser](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor caso:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Funcionalidade adicional

Embora não sejam requisitos obrigatórios, existem outros fatores de conveniência ou privacidade que analisámos ao determinar os fornecedores a recomendar.
