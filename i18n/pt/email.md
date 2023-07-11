---
meta_title: "Recomendações de e-mail privado encriptado - Privacy Guides"
title: "Serviços de e-mail"
icon: material/email
description: Estes fornecedores de e-mail são um excelente local para armazenar os seus e-mails em segurança e muitos oferecem encriptação OpenPGP interoperável com outros fornecedores.
cover: email.png
---

O e-mail é praticamente uma necessidade para subscrever qualquer serviço online, mas não o recomendamos para conversas pessoais. Em vez de utilizar o e-mail para contactar outras pessoas, considere a possibilidade de utilizar uma aplicação de mensagens instantâneas que suporte encaminhamento sigiloso.

[Aplicações de mensagens instantâneas recomendadas](real-time-communication.md ""){.md-button}

Para tudo o resto, recomendamos uma variedade de fornecedores de e-mail baseados em modelos de negócio sustentáveis e que incorporem funcionalidades de segurança e de privacidade.

- [Fornecedores de e-mail compatíveis com OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Outros fornecedores com encriptação :material-arrow-right-drop-circle:](#more-providers)
- [Serviços de aliasing de e-mail :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Opções auto-hospedadas :material-arrow-right-drop-circle:](#self-hosting-email)

## Serviços compatíveis com OpenPGP

Estes fornecedores suportam nativamente a encriptação/desencriptação OpenPGP e a norma Web Key Directory (WKD), permitindo e-mails E2EE independentes do fornecedor. Por exemplo, um utilizador do Proton Mail pode enviar uma mensagem E2EE a um utilizador do Mailbox.org, ou pode receber notificações encriptadas em OpenPGP de serviços Internet que o suportem.

<div class="grid cards" markdown>

- ![Logótipo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Logótipo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

!!! aviso

    Ao utilizar a tecnologia E2EE como o OpenPGP, o e-mail continuará a ter alguns metadados no cabeçalho que não são encriptados. Leia mais sobre [metadados de e-mail](basics/email-security.md#email-metadata-overview).
    
    O OpenPGP também não suporta o encaminhamento sigiloso, o que significa que se a sua chave privada ou a do destinatário for roubada, todas as mensagens encriptadas anteriormente com essa chave serão expostas. [Como protejo as minhas chaves privadas?](basics/email-security.md#how-do-i-protect-my-private-keys)

### Proton Mail

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Proton Mail](assets/img/email/protonmail.svg){ align=right }
    
    O **Proton Mail** é um serviço de e-mail que privilegia a privacidade, a encriptação, a segurança e a facilidade de utilização. Estão em funcionamento desde **2013**. A Proton AG tem sede em Genebra, na Suíça. As contas gratuitas disponibilizam 500 MB de armazenamento.
    
    [:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
        - [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
        - [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
        - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
        - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
        - [:octicons-browser-16: Web](https://mail.proton.me)

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

O Proton Mail tem [encriptação OpenPGP integrada](https://proton.me/support/how-to-use-pgp) no seu webmail. Os e-mails para outras contas do Proton Mail são encriptados automaticamente e a encriptação para endereços que não sejam do Proton Mail com uma chave OpenPGP pode ser ativada facilmente nas definições da sua conta. ´E possível também [encriptar mensagens para endereços que não sejam do Proton Mail](https://proton.me/support/password-protected-emails) sem que seja necessário que se inscrevam numa conta Proton Mail ou utilizem software como o OpenPGP.

O Proton Mail também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isto permite que as pessoas que não utilizam o Proton Mail encontrem facilmente as chaves OpenPGP das contas do Proton Mail, para E2EE entre fornecedores.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Se tiver uma conta paga e passarem 14 dias da data de pagamento [sem que seja paga](https://proton.me/support/delinquency), não poderá aceder aos seus dados. Decorridos 30 dias, a sua conta ficará em situação de incumprimento e não receberá e-mails. A faturação continuará a ser processada durante esse período.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

O Proton Mail oferece uma conta "Ilimitada" por 9,99 euros/mês, que também permite o acesso ao Proton VPN, para além de fornecer várias contas, domínios, pseudónimos e 500 GB de armazenamento.

O Proton Mail não oferece funcionalidade de legado digital.

### Mailbox.org

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }
    
    **Mailbox.org** é um serviço de e-mail cujo foco é a segurança. Não apresenta nenhum tipo de publicidade e o seu consumo de energia é garantido de forma privada por energia 100% ecológica. Estão em funcionamento desde 2014. A Mailbox.org está sediada em Berlim, na Alemanha. As contas começam com 2 GB de armazenamento, que podem ser incrementados de acordo com as necessidades.
    
    [:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentação}
    
    ??? downloads
    
        - [:octicons-browser-16: Web](https://login.mailbox.org)

#### :material-check:{ .pg-green } Domínios e aliases personalizados

O Mailbox.org permite-lhe utilizar o seu próprio domínio e suporta endereços [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). O Mailbox.org também suporta o sub-endereçamento [](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), o que é útil se não quiser comprar um domínio.

#### :material-check:{ .pg-green } Métodos de pagamento privados

O Mailbox.org não aceita quaisquer criptomoedas devido ao facto do seu processador de pagamentos BitPay ter suspendido as operações na Alemanha. No entanto, aceitam dinheiro por correio, pagamento em dinheiro para conta bancária, transferência bancária, cartão de crédito, PayPal e alguns serviços de pagamento específicos para a Alemanha: paydirekt e Sofortüberweisung.

#### :material-check:{ .pg-green } Segurança da conta

O Mailbox.org suporta [autenticação de dois fatores](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) apenas para o seu webmail. Pode utilizar o TOTP ou uma [YubiKey](https://en.wikipedia.org/wiki/YubiKey) através da [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Normas Web como a [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) ainda não são suportadas.

#### :material-information-outline:{ .pg-blue } Segurança dos dados

O Mailbox.org permite a encriptação do correio recebido utilizando a sua caixa de e-mail encriptada [](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). As novas mensagens recebidas serão imediatamente encriptadas com a sua chave pública.

No entanto, a [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), a plataforma de software utilizada pelo Mailbox.org, [não suporta](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) a encriptação do seu livro de endereços e calendário. Uma opção standalone [](calendar.md) pode ser mais adequada para salvaguardar a segurança dessa informação.

#### :material-check:{ .pg-green } Encriptação de e-mail

O Mailbox.org tem [encriptação integrada](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) no seu webmail, o que simplifica o envio de mensagens para pessoas com chaves OpenPGP públicas. Também possibilitam que [destinatários remotos desencriptem uma mensagem de e-mail](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) nos servidores de Mailbox.org. Esta funcionalidade é útil quando o destinatário remoto não tem o OpenPGP e não consegue desencriptar uma cópia do e-mail na sua própria caixa de correio.

O Mailbox.org também suporta a descoberta de chaves públicas via HTTP a partir do seu [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Isto permite que pessoas que não utilizem o Mailbox.org encontrem facilmente as chaves OpenPGP das contas Mailbox.org, para E2EE entre fornecedores.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Após o termo do contrato, a sua conta será definida como uma conta de utilizador restrita. Passados [30 dias será irrevogavelmente eliminada](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Pode aceder à sua conta Mailbox.org através de IMAP/SMTP utilizando o serviço [.onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). No entanto, a sua interface de webmail não pode ser acedida através do serviço .onion e podem ocorrer erros de certificado TLS.

Todas as contas incluem um armazenamento em nuvem limitado que [pode ser encriptado](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). O Mailbox.org também oferece pseudónimo [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), que força a encriptação TLS na ligação entre servidores de e-mail. Se isso não acontecer, a mensagem não será enviada. O Mailbox.org também suporta [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), para além dos protocolos de acesso padrão como IMAP e POP3.

O Mailbox.org tem uma funcionalidade de legado digital para todos os planos. Pode escolher se quer que os seus dados sejam transmitidos aos seus herdeiros, desde que estes o solicitem e apresentem o seu testamento. Em alternativa, pode nomear uma pessoa, fornecendo o seu nome e endereço.

## Mais fornecedores

Estes fornecedores armazenam os seus e-mails com encriptação de acesso zero, o que os torna excelentes opções para manter a segurança do seu armazenamento. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Tutanota logo](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Skiff Mail

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

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

#### :material-check:{ .pg-green } Domínios e aliases personalizados

You can create up to 3 additional @skiff.com email aliases in addition to your primary account address on their free plan. [Custom domains](https://skiff.com/blog/custom-domain-setup) are available on their Pro or Business plan, and allow you to create unlimited aliases.

#### :material-alert-outline:{ .pg-orange } Private Payment Methods

Skiff Mail accepts cryptocurrency payments via Coinbase Commerce, including Bitcoin and Ethereum, but they do not accept our recommended [cryptocurrency](cryptocurrency.md), Monero. They also accept credit card payments via Stripe.

#### :material-check:{ .pg-green } Segurança da conta

Skiff Mail supports TOTP two-factor authentication and hardware security keys using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Segurança dos dados

Skiff Mail has zero access encryption at rest for all of your data. Isto significa que as mensagens e outros dados armazenados na sua conta só podem ser lidos por si.

#### :material-information-outline:{ .pg-blue } Encriptação de e-mail

Skiff Mail does not use OpenPGP. Emails are only encrypted with E2EE to other Skiff Mail users. Skiff does not have a "temporary inbox" or "passworded email" feature like some other providers have, so that external users cannot receive or reply to messages with E2EE.

#### :material-information-outline:{ .pg-blue } Remoção da conta

Skiff Mail accounts do not expire, but unpaid accounts will be prompted to remove any enabled paid features (such as additional aliases) or renew their plan before the account can be used.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Skiff additionally offers [workspace productivity features](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), but we still prefer [alternative](productivity.md) options for collaborating and file sharing at this time.

Skiff Mail does not offer a digital legacy feature.

### Tutanota

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Tutanota](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** é um serviço de e-mail que privilegia a segurança e a privacidade, através da utilização de encriptação. Tutanota está em atividade desde **2011** e tem sede em Hanover, Alemanha. As contas gratuitas disponibilizam 1 GB de armazenamento.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
        - [:simple-appstore: App Store](https://apps.apple.com/app/tutanota/id922429609)
        - [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
        - [:simple-windows11: Windows](https://tutanota.com/#download)
        - [:simple-apple: macOS](https://tutanota.com/#download)
        - [:simple-linux: Linux](https://tutanota.com/#download)
        - [:octicons-browser-16: Web](https://mail.tutanota.com/)

O Tutanota não suporta o protocolo [IMAP](https://tutanota.com/faq/#imap) ou o uso de clientes de e-mail de terceiros [](email-clients.md), assim como [contas de e-mail externas](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647). A [importação de e-mail](https://github.com/tutao/tutanota/issues/630) e as [subpastas](https://github.com/tutao/tutanota/issues/927) não são atualmente suportadas, embora [esta situação deva ser alterada em breve](https://tutanota.com/blog/posts/kickoff-import). Os e-mails podem ser exportados [individualmente ou por seleção em massa](https://tutanota.com/howto#generalMail) por pasta, o que pode ser um inconveniente se tiver uma grande quantidade de pastas.

#### :material-check:{ .pg-green } Domínios e aliases personalizados

As contas pagas do Tutanota podem utilizar até 5 pseudónimos [](https://tutanota.com/faq#alias) e [domínios personalizados](https://tutanota.com/faq#custom-domain). O Tutanota não permite [sub-endereçamento](https://tutanota.com/faq#plus), mas permite utilizar um [catch-all](https://tutanota.com/howto#settings-global) com um domínio personalizado.

#### :material-information-outline:{ .pg-blue } Métodos de pagamento privados

O Tutanota só aceita diretamente cartões de crédito e PayPal, no entanto, podem ser usadas [criptomoedas](cryptocurrency.md) para comprar cartões de oferta, através da sua parceria [](https://tutanota.com/faq/#cryptocurrency) com a Proxystore.

#### :material-check:{ .pg-green } Segurança da conta

O Tutanota suporta [autenticação de dois fatores](https://tutanota.com/faq#2fa) com TOTP ou U2F.

#### :material-check:{ .pg-green } Segurança dos dados

O Tutanota tem [encriptação de acesso zero em estado de repouso](https://tutanota.com/faq#what-encrypted) para os seus e-mails, [livro de endereços](https://tutanota.com/faq#encrypted-address-book), e [calendários](https://tutanota.com/faq#calendar). Isto significa que as mensagens e outros dados armazenados na sua conta só podem ser lidos por si.

#### :material-information-outline:{ .pg-blue } Encriptação de e-mail

O Tutanota [não utiliza o OpenPGP](https://www.tutanota.com/faq/#pgp). As contas Tutanota só podem receber mensagens de e-mail encriptadas de contas de e-mail não-Tutanota, quando enviadas através de uma caixa de e-mail Tutanota temporária [](https://www.tutanota.com/howto/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Remoção da conta

O Tutanota [eliminará as contas gratuitas que estejam inativas](https://tutanota.com/faq#inactive-accounts) durante seis meses. Poderá reutilizar uma conta gratuita desativada, se pagar.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

O Tutanota oferece a versão empresarial do [Tutanota para organizações sem fins lucrativos](https://tutanota.com/blog/posts/secure-email-for-non-profit) gratuitamente ou com um grande desconto.

O Tutanota também tem uma funcionalidade para empresas chamada [Secure Connect](https://tutanota.com/secure-connect/). Isto garante que todos os contactos do cliente com a empresa utilizam o E2EE. Esta funcionalidade custa 240 euros por ano.

O Tutanota não oferece funcionalidade de legado digital.

## Serviços de aliasing de e-mail

Um serviço de aliasing de e-mail permite-lhe gerar facilmente um novo endereço de e-mail para cada sítio Web em que efetue um registo. Os aliases de e-mail que gera são depois reencaminhados para um endereço de e-mail à sua escolha, ocultando tanto o seu endereço de e-mail "principal" como a identidade do seu fornecedor de e-mail. Um serviço de aliasing de e-mail é melhor do que o endereçamento plus habitualmente utilizado e suportado por muitos fornecedores, que permite criar aliases como yourname+[anythinghere]@example.com, porque os sites, os anunciantes e as redes de rastreio podem remover trivialmente tudo o que se segue ao sinal + para conhecer o seu verdadeiro endereço de e-mail.

<div class="grid cards" markdown>

- ![Logótipo AnonAddy](assets/img/email/anonaddy.svg#only-light){ .twemoji }![Logótipo AnonAddy](assets/img/email/anonaddy-dark.svg#only-dark){ .twemoji } [AnonAddy](email.md#anonaddy)
- ![Logótipo SimpleLogin](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

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

### AnonAddy

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo AnonAddy](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![Logótipo AnonAddy](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy** permite-lhe criar 20 aliases de domínio num domínio partilhado, gratuitamente, ou aliases "standard" ilimitados que são menos anónimos.
    
    [:octicons-home-16: Homepage](https://anonaddy.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://anonaddy.com/privacy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://app.anonaddy.com/docs/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://anonaddy.com/donate/){ .card-link title=Contribuir }
    
    ??? transferências
    
        - [:simple-android: Android](https://anonaddy.com/faq/#is-there-an-android-app)
        - [:material-apple-ios: iOS](https://anonaddy.com/faq/#is-there-an-ios-app)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-GB/firefox/addon/anonaddy/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/anonaddy-anonymous-email/iadbdpnoknmbdeolbapdackdcogdmjpe)

O número de aliases partilhados (que terminam num domínio partilhado como @anonaddy.me) que pode criar está limitado a 20, no plano gratuito do AnonAddy, e a 50, no plano que custa 12 dólares por ano. Pode criar pseudónimos padrão ilimitados (que terminam num domínio como @[username].anonaddy.com ou um domínio personalizado em planos pagos), no entanto, tal como mencionado anteriormente, isto pode ser prejudicial para a privacidade, uma vez que as pessoas podem associar trivialmente os seus pseudónimos padrão com base apenas no nome do domínio. Estão disponíveis aliases partilhados ilimitados por $36/ano.

Funcionalidades gratuitas dignas de nota:

- [x] 20 Aliases partilhados
- [x] Aliases padrão ilimitados
- [ ] Nenhuma resposta de saída
- [x] 2 Caixas de correio de destinatários
- [x] Encriptação PGP automática

### SimpleLogin

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Simplelogin](assets/img/email/simplelogin.svg){ align=right }
    
    O **SimpleLogin** é um serviço gratuito que fornece aliases de e-mail numa variedade de nomes de domínio partilhados e, opcionalmente, fornece funcionalidades pagas, como aliases ilimitados e domínios personalizados.
    
    [:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/simple-login){ .card-link title="Código-fonte" }
    
    ??? transferências
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
        - [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/en-US/firefox/addon/simplelogin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
        - [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

O SimpleLogin foi [adquirido pela Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces), em 8 de abril de 2022. Se utiliza o Proton Mail para a sua caixa de correio principal, o SimpleLogin é uma ótima escolha. Uma vez que ambos os produtos são agora propriedade da mesma empresa, só tem de confiar numa única entidade. Também esperamos que o SimpleLogin seja integrado de forma mais estreita com as ofertas da Proton no futuro. O SimpleLogin continua a suportar o reencaminhamento para qualquer fornecedor de e-mail de sua preferência. A Securitum [auditou o](https://simplelogin.io/blog/security-audit/) SimpleLogin no início de 2022 e todas os problemas identificados [foram resolvidos](https://simplelogin.io/audit2022/web.pdf).

Nas definições, pode associar a sua conta SimpleLogin à sua conta Proton. Se tiver o Plano Proton Unlimited, Business ou Visionary, terá o SimpleLogin Premium gratuitamente.

Funcionalidades gratuitas dignas de nota:

- [x] 10 Aliases partilhados
- [x] Respostas ilimitadas
- [x] 1 Caixa de correio do destinatário

## E-mail auto-hospedado

Os administradores de sistemas avançados podem considerar a possibilidade de configurar o seu próprio servidor de e-mail. Os servidores de e-mail requerem atenção e manutenção contínua para se manterem seguros e para que a entrega de e-mail seja fiável.

### Soluções de software combinadas

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Mailcow](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** é um servidor de e-mail mais avançado, perfeito para quem tem um pouco mais de experiência em Linux. Tem tudo o que é necessário num contentor Docker: um servidor de e-mail com suporte DKIM, antivírus e monitorização de spam, webmail e ActiveSync com SOGo, e administração baseada na Web com suporte 2FA.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuir }

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** é um script de configuração automatizado para implementar um servidor de e-mail no Ubuntu. O seu objetivo é facilitar a criação do seu próprio servidor de e-mail.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código-fonte" }

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

- Reutilizar informações pessoais, por exemplo (contas de e-mail, pseudónimos únicos, etc.) a que acederam sem software de anonimato (Tor, VPN, etc.)
- [Impressão digital do browser](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Melhor caso:**

- Documentação clara e fácil de ler. Isto inclui questões como a configuração de 2FA, clientes de e-mail, OpenPGP, etc.

### Funcionalidade adicional

Embora não sejam requisitos obrigatórios, existem outros fatores de conveniência ou privacidade que analisámos ao determinar os fornecedores a recomendar.
