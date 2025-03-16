---
meta_title: "Recomendações de E-mail Privado Criptografado — Privacy Guides"
title: "Serviços de Email"
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

| Provedor                    | OpenPGP / WKD                          | IMAP / SMTP                                                    | Criptografia de Acesso Zero                            | Pagamentos anônimos           |
| --------------------------- | -------------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------ | ----------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Planos pagos apenas | :material-check:{ .pg-green }                          | Dinheiro                      |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                  | :material-information-outline:{ .pg-blue } Mail apenas | Dinheiro                      |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                         | :material-check:{ .pg-green }                          | Monero & Cash via third-party |

Além de (ou ao invés de) um provedor de e-mail recomendado aqui, você pode considerar um serviço de aliasing [e-mail dedicado](email-aliasing.md) para proteger sua privacidade. Entre outras coisas, esses serviços podem ajudar a proteger sua caixa de entrada real contra spam, impedir que marketeiros correlacionem suas contas, e criptografia de todas as mensagens recebidas com PGP.

- [Saiba mais :material-arrow-right-drop-circle:](email-aliasing.md)

## Serviços Compatíveis com OpenPGP

Esses provedores suportam nativamente criptografia/descriptografia OpenPGP e o padrão [do Diretório de Chaves Web](basics/email-security.md#what-is-the-web-key-directory-standard), permitindo e-mails independentes E2EE do provedor. Por exemplo, um usuário do Proton Mail pode mandar uma mensagem E2E para um usuário de Mailbox.org, ou você pode receber notificações criptografadas por OpenPGP de serviços de internet que suportam isso.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Aviso</p>

Ao usar a tecnologia E2EE, como o OpenPGP, seu e-mail ainda terá alguns metadados que não são criptografados no cabeçalho do e-mail, geralmente incluindo a linha de assunto! Leia mais sobre [metadados de e-mail](basics/email-security.md#email-metadata-overview).

OpenPGP também não suporta Encaminhamento Sigiloso, isso significa que se a sua chave ou a do destinatário é alguma vez roubada, todas as mensagens anteriores encriptadas com essa chave serão expostas. [Como eu protejo minhas chaves privadas?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![logo do Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** é um serviço de email com foco na privacidade, criptografia, segurança, e facilidade de uso. Eles estão operando desde 2013. A Proton AG está sedeada em Genebra, na Suíça. O plano gratuito da Proton Mail eletrônico tem 500 MB de armazenamento com a possibilidade de expansão até 1 GB

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

Contas gratuitas têm algumas limitações, como não poderem pesquisar no corpo de texto e não ter acesso à [Ponte Proton Mail](https://proton.me/mail/bridge), o que é requerido para usar um [cliente de email desktop recomendado](email-clients.md) (ex. Thunderbird). Contas pagas incluem funcionalidades como a Ponte Proton Mail, mais armazenamento, e suporte para domínios customizados. Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

Se você tem o Proton Unlimited, Bussiness, ou Visionary Plan, você também ganha o [SimpleLogin](#simplelogin) Premium de graça.

O Proton Mail tem relatórios internos de travamento que eles **não** compartilham com terceiros. Isso pode ser desativado no aplicativo Web: :gear: → **Todas as configurações** → **Conta** → **Segurança e privacidade** → **Privacidade e coleta de dados**.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Assinantes pagos do Proton Mail podem usar seu próprio domínio com o serviço ou um endereço de [pega-tudo (catch-all)](https://proton.me/support/catch-all). Proton Mail também suporta [subendereçamento](https://proton.me/support/creating-aliases), o que é útil para as pessoas que não querem comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Proton Mail [aceita](https://proton.me/support/payment-options) dinheiro por correio, para além dos pagamentos normais com cartão de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Segurança da Conta

O Proton Mail suporta [autenticação de dois fatores](https://proton.me/support/two-factor-authentication-2fa) TOTP e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) usando os padrões FIDO2 ou U2F. O uso de uma chave de segurança de hardware requer a configuração da autenticação de dois fatores TOTP primeiro.

#### :material-check:{ .pg-green } Segurança dos Dados

Proton Mail tem [criptografia de acesso zero](https://proton.me/blog/zero-access-encryption) em repouso para seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Os dados protegidos com criptografia de acesso zero só são acessíveis por você.

Certas informações armazenadas no [Proton Contacts](https://proton.me/support/proton-contacts), como nomes de exibição e endereços de e-mail, não são protegidas com criptografia de acesso zero. Campos de contatos que suportam criptografia de acesso zero, tais como números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Criptografia do Email

Proton Mail [tem criptografia OpenPGP integrada](https://proton.me/support/how-to-use-pgp) em seu webmail. E-mails para outras contas do Proton Mail são criptografados automaticamente, e criptografia para endereços não-Proton Mail com uma chave OpenPGP pode ser facilmente ativada nas configurações da sua conta. O Proton também oferece suporte à descoberta automática de chaves externas com o [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isso significa que os e-mails enviados a outros provedores que usam o WKD também serão criptografados automaticamente com o OpenPGP, sem a necessidade de trocar manualmente chaves PGP públicas com seus contatos. Eles também permitem que você [criptografe mensagens para endereços não-Proton Mail](https://proton.me/support/password-protected-emails) sem a necessidade de eles se cadastrarem com uma conta Proton Mail ou usar programas como OpenPGP.

O Proton Mail também publica as chaves públicas das contas Proton via HTTP a partir de seu WKD. Isso permite que as pessoas que não usam o Proton Mail encontrem as chaves OpenPGP de contas Proton Mail facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores. Isso só se aplica aos endereços de e-mail que terminam em um dos domínios da própria ProtonMail, como @proton.me. Se você usar um domínio personalizado, deverá [configurar o WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separadamente.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Se você tiver uma conta paga e sua conta [não for paga](https://proton.me/support/delinquency) após 14 dias, você não será capaz de acessar seus dados. Após 30 dias, a sua conta ficará inadimplente e não receberá novos e-mails. Você continuará a ser cobrado durante este período. A Proton [excluirá as contas gratuitas inativas](https://proton.me/support/inactive-accounts) após um ano. **Não é possível** reutilizar o endereço de e-mail de uma conta desativada.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

O plano [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) do Proton Mail também garante acesso a outros serviços da Proton, além de fornecer vários domínios personalizados, *aliases* (endereços de redirecionamento) ilimitados do tipo *hide-my-email* (camufle meu endereço de email) e 500 GB de armazenamento.

O Proton Mail não oferece um recurso de legado digital.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

O **Mailbox.org** é um serviço de e-mail que se concentra em ser seguro, livre de anúncios e alimentado de forma privada por energia 100% ecológica. Eles estão operando desde 2014. Mailbox.org é sediado em Berlim, Alemanha. As contas têm a o armazenamento de 2GB em seu plano inicial, que pode ser atualizado se necessário.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

O Mailbox.org permite que você use seu próprio domínio e oferece suporte a endereços [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox.org também oferece suporte para [subendereçamento](https://proton.me/support/creating-aliases), o que é útil para as pessoas que não querem comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Mailbox.org não aceita nenhuma criptomoeda como resultado do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. No entanto, eles aceitam transações pelos correios, pagamento físico para bancos, transferências bancárias, transações via Papal e serviços financeiros específicos da Alemanha como Pandeireta e Sofortuberweisung.

#### :material-check:{ .pg-green } Segurança da Conta

A Mailbox.org suporta autenticação em dois fatores  [(2FA)](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) apenas para o webmail. Você pode usar o TOTP ou uma [YubiKey](https://en.wikipedia.org/wiki/YubiKey) por meio do [YubiCloud](https://yubico.com/products/services-software/yubicloud). Padrões da Web como [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportados.

#### :material-information-outline:{ .pg-blue } Segurança dos Dados

Mailbox.org permite criptografia de e-mails recebidos usando sua [caixa de correio criptografada](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Novas mensagens que você receber serão imediatamente criptografadas com a sua chave pública.

No entanto, [o Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), a plataforma de software usada pelo Mailbox.org, [não oferece suporte à](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) criptografia do seu catálogo de endereços e calendário. Uma [opção autônoma](calendar.md) pode ser mais apropriada para essas informações.

#### :material-check:{ .pg-green } Criptografia do Email

Mailbox.org tem [criptografia integrada](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) em seu webmail, o que simplifica o envio de mensagens para pessoas com chaves OpenPGP públicas. Eles também permitem que [destinatários remotos descriptografem um e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) nos servidores do Mailbox.org. Esse recurso é útil quando o destinatário remoto não tem OpenPGP e não pode descriptografar uma cópia do e-mail em sua própria caixa de correio.

Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isso permite que pessoas fora do Mailbox.org encontrem as chaves OpenPGP de contas Mailbox.org facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores. Isso só se aplica aos endereços de e-mail que terminam em um dos domínios da própria Mailbox, como @mailbox.org. Se você usar um domínio personalizado, deverá [configurar o WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separadamente.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Sua conta será definida como uma conta de usuário restrita quando o contrato terminar. Ele será excluído de forma irrevogável após [30 dias](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Você pode acessar sua conta do Mailbox.org via IMAP/SMTP usando o [ serviço .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). A interface de webmail não pode ser acessada pelo serviço .onion e você pode encontrar alguns erros com certificados TLS.

Todas as contas vêm com armazenamento limitado na nuvem que [pode ser criptografado](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org também oferece o pseudônimo [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), que impõe a criptografia TLS na conexão entre os servidores de email, caso contrário, a mensagem não será enviada. Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), além dos protocolos de acesso padrão como IMAP e POP3.

Mailbox.org tem um recurso de legado digital para todos os planos. Você pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Como alternativa, você pode nomear uma pessoa através do seu nome e endereço.

## Mais Provedores

Estes provedores armazenam os seus e-mails com criptografia de conhecimento zero, o que os torna excelentes opções para manter seguros os seus e-mails armazenados. No entanto, eles não suportam padrões de criptografia interoperáveis para comunicações ponta-a-ponta (E2EE) entre provedores.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (anteriormente *Tutanota*) é um serviço de e-mail com foco na segurança e privacidade por meio do uso de criptografia. Tutá está em funcionamento desde 2011 e está com sede em Hanover, Alemanha. Contas gratuitas com 1GB de armazenamento.

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

A Tuta só aceita diretamente cartões de crédito e PayPal, mas [criptomoedas](cryptocurrency.md) pode ser usada como método de pagamento para adquirir cartões-presente através de uma [parceria](https://tuta.com/support/#cryptocurrency) com a Proxystore.

#### :material-check:{ .pg-green } Segurança da Conta

Também há  suporte à [autenticação de dois fatores](https://tuta.com/support#2fa) com TOTP ou U2F.

#### :material-check:{ .pg-green } Segurança dos Dados

O Tuta tem [criptografia de acesso zero em repouso](https://tuta.com/support#what-encrypted) para seus e-mails, [contatos do catálogo de endereços](https://tuta.com/support#encrypted-address-book) e [calendários](https://tuta.com/support#calendar). Isso significa que as mensagens e outros dados armazenados em sua conta só são legíveis por você.

#### :material-information-outline:{ .pg-blue } Criptografia do Email

A Tuta [não usa o OpenPGP](https://tuta.com/support/#pgp). Contas Tuta só podem receber e-mails criptografados de contas de e-mail não-Tuta quando enviados através de uma [caixa de correio temporária do Tutanota](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

A Tuta excluirá [as contas gratuitas inativas](https://tuta.com/support#inactive-accounts) após seis meses. Você poderá reutilizar uma conta gratuita desativada se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Tuta oferece a versão comercial do [Tuta para organizações sem fins lucrativos](https://tuta.com/blog/secure-email-for-non-profit) de graça ou com desconto.

O Tuta não oferece um recurso de legado digital.

## Email Auto-Hospedado

Administratores de sistema avançados podem considerar a possibilidade de configurar seu próprio servidor de e-mail. Os servidores de e-mail exigem atenção e manutenção contínua para manter a segurança e a confiabilidade da entrega de e-mails.

### Soluções combinadas de software

<div class="admonition recommendation" markdown>

![Mailcow logo](assets/img/email/mailcow.svg){ align=right }

**Mailcow** é um servidor de correio mais avançado, perfeito para aqueles com mais experiência no Linux. Ele tem tudo o que você precisa em um contêiner Docker: um servidor de e-mail com suporte a DKIM, antivírus e monitoramento de spam, webmail e ActiveSync com SOGo, e administração baseada na web com suporte a 2FA.

[:octicons-home-16: Página inicial](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Código fonte" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribuir" }

</div>

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de correio no Ubuntu. Seu objetivo é facilitar a configuração de seu próprio servidor de e-mail.

[:octicons-home-16: Página inicial](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código fonte" }

</div>

Para uma abordagem mais manual, selecionamos estes dois artigos:

- [Configuração de um servidor de correio eletrônico com OpenSMTPD, Dovecot e Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [Como rodar o seu próprio servidor de correio](https://c0ffee.net/blog/mail-server-guide) (agosto de 2017)

## Requisitos

**Por favor, note que não somos afiliados a nenhum dos provedores que recomendamos.** Além de [nosso critério básico](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de e-mail que queira ser mencionado, incluindo a implementação de melhores práticas do setor, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

### Tecnologia

Consideramos esses recursos importantes para fornecer um serviço seguro e otimizado. Você deve considerar se o provedor tem os recursos de que você precisa.

**Mínimo Para Qualificação:**

- Criptografa os dados da conta de e-mail em repouso com criptografia de acesso zero.
- Função "Exportar como" para os formatos [Mbox](https://en.wikipedia.org/wiki/Mbox) ou arquivos .eml individuais no padrão [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Permite que os usuários usem seu próprio [nome de domínio](https://en.wikipedia.org/wiki/Domain_name). Nomes de domínio personalizados são importantes para os usuários, porque lhes permite manter sua agência a partir do serviço. Deve piorar ou ser adquirido por outra empresa que não priorize a privacidade.
- Opera em uma infraestrutura própria, ou seja, não é baseada em provedores de serviços de e-mail de terceiros.

**Melhor Caso:**

- Criptografa todos os dados da conta (contatos, calendários, etc.) em repouso com criptografia de acesso zero.
- Criptografia E2EE/PGP integrada de webmail fornecido como conveniência.
- Suporte ao [WKD](https://wiki.gnupg.org/WKD) para permitir a descoberta aprimorada de chaves OpenPGP públicas via HTTP. Usuários do GnuPG podem obter uma chave digitando: `gpg --locate-key example_user@example.com`
- Suporte para uma caixa de correio temporária para usuários externos. Isso é útil quando você deseja enviar um e-mail criptografado sem enviar uma cópia real para o seu destinatário. Estes e-mails geralmente têm um tempo de vida limitado e depois são automaticamente excluídos. Eles também não exigem que o destinatário configure nenhuma criptografia, como o OpenPGP.
- Disponibilidade do site do provedor de serviços de e-mail em um [serviço onion](https://en.wikipedia.org/wiki/.onion).
- Suporte a [subendereçamento](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Funcionalidade de alias ou catch-all para aqueles que usam seus próprios domínios.
- Uso de protocolos padrão de acesso a e-mail, como IMAP, SMTP ou [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Os protocolos de acesso padrão garantem que os clientes possam baixar facilmente todos os seus e-mails, caso queiram mudar para outro provedor.

### Privacidade

Preferimos que nossos provedores recomendados coletem o mínimo possível de dados.

**Mínimo Para Qualificação:**

- Protege o endereço IP do remetente, o que pode envolver a filtragem de sua exibição no campo de cabeçalho `Received`.
- Não exige informações de identificação pessoal (PII) além de um nome de usuário e uma senha.
- Política de privacidade que atende aos requisitos definidos pelo GDPR.

**Melhor Caso:**

- Aceita [opções de pagamento anônimas](advanced/payments.md) ([criptomoedas](cryptocurrency.md), dinheiro, cartões-presente, etc.)
- Hospedado em uma jurisdição com fortes leis de proteção de privacidade de e-mail.

### Segurança

Os servidores de e-mail lidam com uma grande quantidade de dados muito confidenciais. Esperamos que os provedores adotem as melhores práticas do setor para proteger seus clientes.

**Mínimo Para Qualificação:**

- Proteção do webmail com 2FA, como TOTP.
- Criptografia de acesso zero, que se baseia na criptografia em repouso. O provedor não tem as chaves de descriptografia dos dados que possui. Isso evita que um funcionário desonesto vaze os dados aos quais tem acesso ou que um adversário remoto libere os dados que roubou ao obter acesso não autorizado ao servidor.
- Suporte a [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nenhum erro ou vulnerabilidade de TLS ao ser analisado por ferramentas como [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) ou [Qualys SSL Labs](https://ssllabs.com/ssltest); isso inclui erros relacionados a certificados e parâmetros DH fracos, como os que levaram ao [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Uma preferência de suite de servidor (opcional em TLSv1.3) para suites de cifragem fortes que suportam encaminhamento de sigilo e criptografia autenticada.
- Uma política válida de [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registros [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) válidos.
- Registros [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) válidos.
- Tenha um registro e uma política [DMARC](https://en.wikipedia.org/wiki/DMARC) adequados ou use o [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) para autenticação. Se a autenticação DMARC estiver sendo usada, a política deve ser definida como `rejeitar` ou `em quarentena`.
- Uma preferência de suíte de servidor de TLS 1.2 ou posterior e um plano para [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Envio [SMTPS](https://en.wikipedia.org/wiki/SMTPS), assumindo que o SMTP seja usado.
- Padrões de segurança do site, como:
    - [HTTP Segurança de Transporte Estrita](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridade do sub-recurso](https://en.wikipedia.org/wiki/Subresource_Integrity) se estiver carregando coisas de domínios externos.
- Deve suportar a visualização de [cabeçalhos de mensagens](https://en.wikipedia.org/wiki/Email#Message_header), pois esse é um recurso forense crucial para determinar se um e-mail é uma tentativa de phishing.

**Melhor Caso:**

- Suporte para autenticação de hardware, isto é. U2F e [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registro de recurso de autorização de autoridade de certificação (CAA) do DNS](https://tools.ietf.org/html/rfc6844), além do suporte a DANE.
- Implementação do [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), que é útil para pessoas que postam em listas de discussão [RFC8617](https://tools.ietf.org/html/rfc8617).
- Auditorias de segurança publicadas por uma empresa terceirizada de boa reputação.
- Programas de recompensa por bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Padrões de segurança do site, tais como:
    - [Política de segurança de conteúdo (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confiança

Você não confiaria suas finanças a alguém com uma identidade falsa, então por que confiar seu e-mail a essa pessoa? Exigimos que nossos provedores recomendados sejam transparentes quanto a seus proprietários ou lideranças. Também esperamos ver relatórios de transparência frequentes, especialmente com relação à forma como as solicitações do governo são tratadas.

**Mínimo Para Qualificação:**

- Liderança ou propriedade voltada para o público.

**Cenário ideal:**

- Relatórios de transparência frequentes.

### Marketing

Com os provedores de e-mail que recomendamos, gostamos de ver um marketing responsável.

**Mínimo para Qualificação:**

- Precisa precis ter um serviço de auto-hospedagem de seus dados estatísticos (sem Google Analytics, Adobe Analytics, etc. ).

Não deve haver qualquer marketing irresponsável, o que pode incluir o seguinte:

- Alegações de "criptografia inquebrável" A criptografia deve ser utilizada com a intenção de não ser secreta no futuro quando a tecnologia para quebra-lá existir.
- Garantir 100% de proteção ao anonimato. Quando alguém afirma que algo é 100%, significa que não há certeza de fracasso. Sabemos que as pessoas podem facilmente se desanonimizar de várias maneiras, por exemplo:

    - Reutilização de informações pessoais, por exemplo, (contas de e-mail, pseudônimos exclusivos etc.) que eles acessaram sem software de anonimato (Tor, I2P, VPN etc.)
    - [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor Caso:**

- Limpar e ler facilmente a documentação de tarefas como a configuração do 2FA, clientes de e-mail, OpenPGP, etc.

### Funções Adicionais

Embora não sejam requisitos estritos, há outros fatores de conveniência ou privacidade que analisamos ao determinar quais provedores recomendar.
