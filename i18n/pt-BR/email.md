---
meta_title: "Recomendações de E-mail Privado Criptografado — Privacy Guides"
title: "Serviços de Email"
icon: material/email
description: Esses provedores de email oferecem um ótimo lugar para armazenar seus emails de forma segura, e muitos oferecem criptografia OpenPGP compatível com outros provedores.
cover: email.png
---

O "email" é praticamente uma necessidade para usar qualquer serviço “online”, contudo não o recomendamos para conversas pessoais. Ao invés de utilizar email para falar com outras pessoas, considere utilizar um meio de mensagens instantâneas que suporte sigilo encaminhado.

[Mensageiros Instantâneos Recomendados](real-time-communication.md ""){.md-button}

Para qualquer outra coisa, recomendamos uma variedade de provedores de email baseados em modelos de negócio sustentáveis e recursos de segurança e privacidade incorporados.

- [OpenPGP-Compatible Email Providers :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Other Encrypted Providers :material-arrow-right-drop-circle:](#more-providers)
- [Email Aliasing Services :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Self-Hosted Options :material-arrow-right-drop-circle:](#self-hosting-email)

## Serviços Compatíveis com OpenPGP

Esses provedores suportam nativamente a criptografia/descriptografia OpenPGP e o padrão Web Key Directory (WKD), permitindo e-mails E2E independentes do provedor. Por exemplo, um usuário do Proton Mail pode mandar uma mensagem E2E para um usuário de Mailbox.org, ou você pode receber notificações criptografadas por OpenPGP de serviços de internet que suportam isso.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! Alerta

    Ao usar a tecnologia E2EE, como OpenPGP, o e-mail ainda terá alguns metadados que não são criptografados no cabeçalho do e-mail. Leia mais sobre [metadados de email](basics/email-security.md#email-metadata-overview).
    
    OpenPGP também não suporta Sigilo Encaminhado, isso significa que se a sua chave ou a do destinatário é alguma vez roubada, todas as mensagens anteriores encriptadas com essa chave serão expostas. [Como eu protejo minhas chaves privadas?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! recommendation

    ![logo do Proton Mail](assets/img/email/protonmail.svg){ align=right }
    
    **Proton Mail** é um serviço de email com foco na privacidade, criptografia, segurança, e facilidade de uso. Eles estão operando desde **2013**. Proton AG é localizado em Genève, Suíça. As contas começam com 500 MB de armazenamento com seu plano grátis.
    
    [:octicons-home-16: Página Inicial](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Código-Fonte" }
    
    ??? - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

Contas gratuitas têm algumas limitações, como não poderem pesquisar no corpo de texto e não ter acesso à [Ponte Proton Mail](https://proton.me/mail/bridge), o que é requerido para usar um [cliente de email desktop recomendado](email-clients.md) (ex. Thunderbird). Contas pagas incluem funcionalidades como a Ponte Proton Mail, mais armazenamento, e suporte para domínios customizados. Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

Se você tem o Proton Unlimited, Bussiness, ou Visionary Plan, você também ganha o [SimpleLogin](#simplelogin) Premium de graça.

O Proton Mail tem relatórios internos de travamento que eles **não** compartilham com terceiros. Isto pode ser desativado em: **Configurações** > **Vá para Configurações** > **Conta** > **Segurança e privacidade** > **Enviar relatórios de erro**.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Assinantes pagos do Proton Mail podem usar seu próprio domínio com o serviço ou um endereço de [pega-tudo (catch-all)](https://proton.me/support/catch-all). Proton Mail também suporta [subendereçamento](https://proton.me/support/creating-aliases), o que é útil para as pessoas que não querem comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Proton Mail [aceita](https://proton.me/support/payment-options) dinheiro por correio, para além dos pagamentos normais com cartão de crédito/débito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Segurança da Conta

Proton Mail suporta TOTP [autenticação de dois factores](https://proton.me/support/two-factor-authentication-2fa) e [chaves de segurança de hardware](https://proton.me/support/2fa-security-key) utilizando as normas FIDO2 ou U2F. O uso de uma chave de segurança de hardware requer a configuração da autenticação de dois fatores TOTP primeiro.

#### :material-check:{ .pg-green } Segurança dos Dados

Proton Mail tem [criptografia de acesso zero](https://proton.me/blog/zero-access-encryption) em repouso para seus e-mails e [calendários](https://proton.me/news/protoncalendar-security-model). Os dados protegidos com criptografia de acesso zero só são acessíveis por você.

Certas informações armazenadas no [Proton Contacts](https://proton.me/support/proton-contacts), como nomes de exibição e endereços de e-mail, não são protegidas com criptografia de acesso zero. Campos de contatos que suportam criptografia de acesso zero, tais como números de telefone, são indicados com um ícone de cadeado.

#### :material-check:{ .pg-green } Criptografia do Email

Proton Mail [tem criptografia OpenPGP integrada](https://proton.me/support/how-to-use-pgp) em seu webmail. E-mails para outras contas do Proton Mail são criptografados automaticamente, e criptografia para endereços não-Proton Mail com uma chave OpenPGP pode ser facilmente ativada nas configurações da sua conta. Eles também permitem que você [criptografe mensagens para endereços não-Proton Mail](https://proton.me/support/password-protected-emails) sem a necessidade de eles se cadastrarem para uma conta Proton Mail ou usar programas como OpenPGP.

Proton Mail também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isso permite que as pessoas que não usam o Proton Mail encontrem as chaves OpenPGP de contas Proton Mail facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Se você tiver uma conta paga e sua conta [não for paga](https://proton.me/support/delinquency) após 14 dias, você não será capaz de acessar seus dados. Após 30 dias, a sua conta ficará inadimplente e não receberá novos e-mails. Você continuará a ser cobrado durante este período.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Proton Mail oferece uma conta "Ilimitada" por 9,99 euros/mês, que também permite o acesso ao Proton VPN, além de fornecer várias contas, domínios, pseudônimos e 500 GB de armazenamento.

O Proton Mail não oferece um recurso de legado digital.

### Mailbox.org

!!! recommendation

    ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** is an email service with a focus on being secure, ad-free, and privately powered by 100% eco-friendly energy. They have been in operation since 2014. Mailbox.org is based in Berlin, Germany. Accounts start with 2 GB of storage, which can be upgraded as needed.
    
    [:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentation}
    
    ??? downloads
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Mailbox.org permite que você use seu próprio domínio, e eles suportam [endereços pega-tudo (catch-all)](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). Mailbox.org também suporta [subendereçamento](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), o que é útil se você não quer comprar um domínio.

#### :material-check:{ .pg-green } Métodos de Pagamento Privados

Mailbox.org não aceita nenhuma criptomoeda como resultado do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. No entanto, eles aceitam dinheiro por correio, pagamento em dinheiro para conta bancária, transferência bancária, cartão de crédito, PayPal e alguns processadores específicos da Alemanha: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da Conta

Mailbox.org suporta [autenticação de dois factores](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) apenas para o seu webmail. Você pode usar TOTP ou um [YubiKey](https://en.wikipedia.org/wiki/YubiKey) através do [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Padrões da Web como [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportados.

#### :material-information-outline:{ .pg-blue } Segurança dos Dados

Mailbox.org permite criptografia de e-mails recebidos usando sua [caixa de correio criptografada](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). Novas mensagens que você receber serão imediatamente criptografadas com a sua chave pública.

No entanto, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), a plataforma de software usada por Mailbox.org, [não suporta](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) a criptografia do seu catálogo de endereços e calendário. Uma [opção autônoma](calendar.md) pode ser mais apropriada para essas informações.

#### :material-check:{ .pg-green } Criptografia do Email

Mailbox.org tem [criptografia integrada](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) em seu webmail, o que simplifica o envio de mensagens para pessoas com chaves OpenPGP públicas. Eles também permitem que [destinatários remotos descriptografem um e-mail](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) nos servidores da Mailbox.org. Esse recurso é útil quando o destinatário remoto não tem OpenPGP e não pode descriptografar uma cópia do e-mail em sua própria caixa de correio.

Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isso permite que pessoas fora do Mailbox.org encontrem as chaves OpenPGP de contas Mailbox.org facilmente, para criptografia ponta-a-ponta (E2EE) entre provedores.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Sua conta será definida como uma conta de usuário restrita quando o contrato terminar, após [30 dias ela será irrevogavelmente excluída](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Você pode acessar sua conta do Mailbox.org via IMAP/SMTP usando o seu [serviço ".onion"](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). No entanto, sua interface webmail não pode ser acessada através do seu serviço ".onion" e você pode experimentar erros de certificado TLS.

Todas as contas vêm com armazenamento limitado na nuvem que [pode ser criptografado](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Mailbox.org também oferece o pseudônimo [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), que impõe a criptografia TLS na conexão entre os servidores de email, caso contrário, a mensagem não será enviada. Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), além dos protocolos de acesso padrão como IMAP e POP3.

Mailbox.org tem um recurso de legado digital para todos os planos. Você pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Como alternativa, você pode nomear uma pessoa através do seu nome e endereço.

## Mais Provedores

Estes provedores armazenam os seus e-mails com criptografia de conhecimento zero, o que os torna excelentes opções para manter seguros os seus e-mails armazenados. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Skiff Mail

!!! recommendation

    ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ align=right }
    
    **Skiff Mail** is a web based email service with E2EE that began in 2020 that is based in San Francisco with developers worldwide. Accounts start with 10GB of free storage.
    
    [:octicons-home-16: Homepage](https://skiff.com/mail){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&pli=1)
        - [:simple-appstore: iOS](https://apps.apple.com/us/app/skiff-mail/id1619168801)
        - [:octicons-browser-16: Web](https://app.skiff.com/mail)

Skiff has undergone a few [audits](https://skiff.com/transparency) during its development.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. Free accounts can add 1 [custom domain](https://skiff.com/blog/custom-domain-setup), and up to 15 custom domains on a paid plan. You can create unlimited aliases or a [catch-all](https://skiff.com/blog/catch-all-email-alias) alias on your custom domain.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } Segurança da Conta

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Segurança dos Dados

Skiff Mail has zero access encryption at rest for all of your data. Isso significa que as mensagens e outros dados armazenados em sua conta só são legíveis por você.

#### :material-information-outline:{ .pg-blue } Criptografia do Email

Skiff Mail does not use OpenPGP. Emails are only encrypted with E2EE to other Skiff Mail users. Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Tutanota

!!! recommendation

    ![Tutanota logo](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** is an email service with a focus on security and privacy through the use of encryption. Tutanota has been in operation since **2011** and is based in Hanover, Germany. Accounts start with 1GB storage with their free plan.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

Tutanota não suporta o [protocolo IMAP](https://tutanota.com/faq/#imap) ou o uso de [clientes de e-mail de terceiros](email-clients.md), e você também não será capaz de adicionar [contas de e-mail externas](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) ao aplicativo Tutanota. Nem [importação de Email](https://github.com/tutao/tutanota/issues/630) ou [subpastas](https://github.com/tutao/tutanota/issues/927) são suportados atualmente, embora isso [deva ser alterado](https://tutanota.com/blog/posts/kickoff-import). Os e-mails podem ser exportados [individualmente ou por seleção em massa](https://tutanota.com/howto#generalMail) por pasta, o que pode ser inconveniente se você tiver muitas pastas.

#### :material-check: { .pg-green } Domínios e Pseudônimos Personalizados

Contas pagas do Tutanota podem usar até 5 pseudônimos [](https://tutanota.com/faq#alias) e [domínios personalizados](https://tutanota.com/faq#custom-domain). Tutanota não permite [subendereçamento (mais endereços)](https://tutanota.com/faq#plus), mas você pode usar um [pega-tudo (catch-all)](https://tutanota.com/howto#settings-global) com um domínio personalizado.

#### :material-information-outline:{ .pg-blue } Métodos de Pagamento Privados

Tutanota só aceita diretamente cartões de crédito e PayPal, no entanto, [criptomoeda](cryptocurrency.md) pode ser usada para comprar vales-presente através de sua parceria [](https://tutanota.com/faq/#cryptocurrency) com Proxystore.

#### :material-check:{ .pg-green } Segurança da Conta

Tutanota suporta [autenticação de dois fatores](https://tutanota.com/faq#2fa) com TOTP ou U2F.

#### :material-check:{ .pg-green } Segurança dos Dados

Tutanota tem [criptografia de acesso zero em repouso](https://tutanota.com/faq#what-encrypted) para seus e-mails, [contatos de agenda](https://tutanota.com/faq#encrypted-address-book) e [calendários](https://tutanota.com/faq#calendar). Isso significa que as mensagens e outros dados armazenados em sua conta só são legíveis por você.

#### :material-information-outline:{ .pg-blue } Criptografia do Email

Tutanota [não usa o OpenPGP](https://www.tutanota.com/faq/#pgp). Contas Tutanota só podem receber e-mails criptografados de contas de e-mail não-Tutanota quando enviados através de uma [caixa de correio temporária do Tutanota](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Rescisão da Conta

Tutanota [excluirá contas gratuitas inativas](https://tutanota.com/faq#inactive-accounts) após seis meses. Você poderá reutilizar uma conta gratuita desativada se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Tutanota oferece a versão de negócios do [Tutanota para organizações sem fins lucrativos](https://tutanota.com/blog/posts/secure-email-for-non-profit) de graça ou com um grande desconto.

Tutanota também tem um recurso empresarial chamado [Secure Connect](https://tutanota.com/secure-connect/). Isso garante que o contato do cliente com a empresa use o E2EE. O recurso custa 240 euros por ano.

Tutanota não oferece um recurso de legado digital.

## Serviços de Disfarce de Email

Um serviço de disfarce de e-mail permite que você gere facilmente um novo endereço de e-mail para cada site em que se registrar. Os e-mails alternativos que você gera são encaminhados para um endereço de e-mail que você escolher, ocultando o seu endereço de e-mail "principal" e a identidade do seu provedor de email. Um verdadeiro pseudônimo de e-mail é melhor do que o endereçamento plus comumente usado e suportado por muitos provedores, que permite criar pseudônimos como seunome+[anythinghere]@exemplo.com, porque sites, anunciantes e redes de rastreamento podem remover trivialmente qualquer coisa após o sinal + para saber seu verdadeiro endereço de e-mail.

<div class="grid cards" markdown>

- ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ .twemoji }![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
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

### AnonAddy

!!! recommendation

    ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy** permite criar 20 pseudônimos de domínio gratuitamente em um domínio compartilhado, ou pseudônimos "padrão" ilimitados, que são menos anônimos.
    
    [:octicons-home-16: Homepage](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

O número de pseudônimos compartilhados (que terminam em um domínio compartilhado como @anonaddy.me) que você pode criar é limitado a 20 no plano gratuito do AnonAddy e a 50 no plano de 12 dólares por ano. Você pode criar pseudônimos padrão ilimitados (que terminam em um domínio como @[username].anonaddy.com ou um domínio personalizado em planos pagos); no entanto, conforme mencionado anteriormente, isso pode ser prejudicial à privacidade porque as pessoas podem vincular seus pseudônimos padrão de forma fácil com base apenas no nome do domínio. Pseudônimos compartilhados ilimitados estão disponíveis por um preço de 36 dólares por ano.

Recursos gratuitos de destaque:

- [x] 20 Pseudônimos Compartilhados
- [x] Pseudônimos Padrão Ilimitados
- [ ] No Outgoing Replies
- [x] 2 Caixas de Correio Destinatárias
- [x] Criptografia PGP automática

### SimpleLogin

!!! recommendation

    ![Logótipo Simplelogin](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** é um serviço gratuito que fornece pseudônimos de e-mail em uma variedade de nomes de domínio compartilhados e, opcionalmente, oferece recursos pagos, como pseudônimos ilimitados e domínios personalizados.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

SimpleLogin foi [adquirido pelo Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) a partir de 8 de abril de 2022. Se você usa o Proton Mail como sua caixa de correio principal, o SimpleLogin é uma ótima opção. Como os dois produtos agora pertencem à mesma empresa, você só precisa confiar em uma única entidade. Também esperamos que, no futuro, o SimpleLogin seja mais fortemente integrado às ofertas da Proton. SimpleLogin continua a oferecer suporte ao encaminhamento para qualquer provedor de e-mail de sua escolha. A Securitum [auditou](https://simplelogin.io/blog/security-audit/) SimpleLogin no início de 2022 e todos os problemas [foram abordados](https://simplelogin.io/audit2022/web.pdf).

Você pode vincular sua conta SimpleLogin com sua conta Proton nas configurações. Se você tiver o Proton Unlimited, Business ou Visionary Plan, terá o SimpleLogin Premium gratuitamente.

Recursos gratuitos de destaque:

- [x] 10 Pseudônimos Compartilhados
- [x] Respostas ilimitadas
- [x] 1 Caixa de Correio Destinatária

## Email Auto-Hospedado

Administratores de sistema avançados podem considerar a possibilidade de configurar seu próprio servidor de e-mail. Servidores de correio eletrônico requerem atenção e manutenção contínua para manter as coisas seguras e a entrega de correio eletrônico confiável.

### Soluções combinadas de software

!!! recommendation

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

!!! recommendation

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de correio no Ubuntu. Seu objetivo é facilitar a configuração de seu próprio servidor de e-mail.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

Para uma abordagem mais manual, selecionamos estes dois artigos:

- [Configurando um servidor de email com OpenSMTPD, Dovecot e Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Como executar seu próprio servidor de email](https://www.c0ffee.net/blog/mail-server-guide/) (agosto de 2017)

## Requisitos

**Por favor, note que não somos afiliados a nenhum dos provedores que recomendamos.** Além de [nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de e-mail que queira ser mencionado, incluindo a implementação de melhores práticas do setor, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

### Tecnologia

Consideramos esses recursos importantes para fornecer um serviço seguro e otimizado. Você deve considerar se o provedor tem os recursos de que você precisa.

**Mínimo Para Qualificação:**

- Criptografa os dados da conta de e-mail em repouso com criptografia de acesso zero.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Melhor Caso:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
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
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/), or [Qualys SSL Labs](https://www.ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLSv1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
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
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

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
