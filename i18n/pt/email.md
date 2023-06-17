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
    [:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Código Fonte" }
    
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

Estes fornecedores armazenam os seus e-mails com encriptação de acesso zero, o que os torna excelentes opções para manter a segurança do seu armazenamento. No entanto, não suportam normas de encriptação interoperáveis para comunicações E2EE entre fornecedores.

<div class="grid cards" markdown>

- ![Logótipo Tutanota](assets/img/email/tutanota.svg){ .twemoji } [Tutanota](email.md#tutanota)

</div>

### Tutanota

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Tutanota](assets/img/email/tutanota.svg){ align=right }
    
    **Tutanota** é um serviço de e-mail que privilegia a segurança e a privacidade, através da utilização de encriptação. Tutanota está em atividade desde **2011** e tem sede em Hanover, Alemanha. As contas gratuitas disponibilizam 1 GB de armazenamento.
    
    [:octicons-home-16: Homepage](https://tutanota.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://tutanota.com/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://tutanota.com/faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Código Fonte" }
    [:octicons-heart-16:](https://tutanota.com/community/){ .card-link title=Contributo }
    
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

Um serviço de aliasing de e-mail permite-lhe gerar facilmente um novo endereço de e-mail para cada sítio Web em que efetue um registo. Os aliases de e-mail que gera são depois reencaminhados para um endereço de e-mail à sua escolha, ocultando tanto o seu endereço de e-mail "principal" como a identidade do seu fornecedor de e-mail. True email aliasing is better than plus addressing commonly used and supported by many providers, which allows you to create aliases like yourname+[anythinghere]@example.com, because websites, advertisers, and tracking networks can trivially remove anything after the + sign to know your true email address.

<div class="grid cards" markdown>

- ![Joplin logo](/assets/img/notebooks/joplin.svg){ .twemoji } [Joplin](https://joplinapp.org/)
- ![Standard Notes logo](/assets/img/notebooks/standard-notes.svg){ .twemoji } [Standard Notes](https://standardnotes.org/)

</div>

Email aliasing can act as a safeguard in case your email provider ever ceases operation. In that scenario, you can easily re-route your aliases to a new email address. In turn, however, you are placing trust in the aliasing service to continue functioning.

Using a dedicated email aliasing service also has a number of benefits over a catch-all alias on a custom domain:

- Aliases can be turned on and off individually when you need them, preventing websites from emailing you randomly.
- Replies are sent from the alias address, shielding your real email address.

They also have a number of benefits over "temporary email" services:

- Aliases are permanent and can be turned on again if you need to receive something like a password reset.
- Emails are sent to your trusted mailbox rather than stored by the alias provider.
- Temporary email services typically have public mailboxes which can be accessed by anyone who knows the address, aliases are private to you.

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as your own custom domain(s) for a modest yearly fee. They can also be self-hosted if you want maximum control. However, using a custom domain can have privacy-related drawbacks: If you are the only person using your custom domain, your actions can be easily tracked across websites simply by looking at the domain name in the email address and ignoring everything before the at (@) sign.

Using an aliasing service requires trusting both your email provider and your aliasing provider with your unencrypted messages. Some providers mitigate this slightly with automatic PGP encryption, which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### StartMail

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![AnonAddy logo](assets/img/email/anonaddy.svg#only-light){ align=right }
    ![AnonAddy logo](assets/img/email/anonaddy-dark.svg#only-dark){ align=right }
    
    **AnonAddy** lets you create 20 domain aliases on a shared domain for free, or unlimited "standard" aliases which are less anonymous.
    
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

The number of shared aliases (which end in a shared domain like @anonaddy.me) that you can create is limited to 20 on AnonAddy's free plan and 50 on their $12/year plan. You can create unlimited standard aliases (which end in a domain like @[username].anonaddy.com or a custom domain on paid plans), however, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. Unlimited shared aliases are available for $36/year.

Notable free features:

- Criptografa os dados da conta em repouso.
- A criptografia integrada do webmail proporciona conveniência aos usuários que desejam melhorar ao não ter [E2EE](https://en.wikipedia.org/wiki/End-to-end_encryption) criptografia.
- [ ] No Outgoing Replies
- [x] 2 Recipient Mailboxes
- [x] Automatic PGP Encryption

### CTemplar

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Simplelogin logo](assets/img/email/simplelogin.svg){ align=right }
    
    **SimpleLogin** is a free service which provides email aliases on a variety of shared domain names, and optionally provides paid features like unlimited aliases and custom domains.
    
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

SimpleLogin was [acquired by Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) as of April 8, 2022. If you use Proton Mail for your primary mailbox, SimpleLogin is a great choice. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin continues to support forwarding to any email provider of your choosing. Securitum [audited](https://simplelogin.io/blog/security-audit/) SimpleLogin in early 2022 and all issues [were addressed](https://simplelogin.io/audit2022/web.pdf).

You can link your SimpleLogin account in the settings with your Proton account. If you have the Proton Unlimited, Business, or Visionary Plan, you will have SimpleLogin Premium for free.

Notable free features:

- Criptografa os dados da conta em repouso com criptografia de acesso zero.
- [x] Unlimited Replies
- [x] 1 Recipient Mailbox

## Visão Geral dos Metadados de Email

Advanced system administrators may consider setting up their own email server. Mail servers require attention and continuous maintenance in order to keep things secure and mail delivery reliable.

### Combined software solutions

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Mailcow logo](assets/img/email/mailcow.svg){ align=right }
    
    **Mailcow** is a more advanced mail server perfect for those with a bit more Linux experience. It has everything you need in a Docker container: A mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.
    
    [:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Mail-in-a-Box logo](assets/img/email/mail-in-a-box.svg){ align=right }
    
    **Mail-in-a-Box** is an automated setup script for deploying a mail server on Ubuntu. Its goal is to make it easier for people to set up their own mail server.
    
    [:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
    [:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

For a more manual approach we've picked out these two articles:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide/) (August 2017)

## Framadate

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any Email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an Email provider, and conduct your own research to ensure the Email provider you choose is the right choice for you.

### Jurisdição

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider which has the features you require.

**O melhor caso:**

- Operando fora dos EUA ou de outros países da Five Eyes.
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Operates on owned infrastructure, i.e. not built upon third-party email service providers.

**Best Case:**

- Encrypts all account data (Contacts, Calendars, etc.) at rest with zero-access encryption.
- Integrated webmail E2EE/PGP encryption provided as a convenience.
- Support for [WKD](https://wiki.gnupg.org/WKD) to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key by typing: `gpg --locate-key example_user@example.com`
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email, without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Availability of the email provider's services via an [onion service](https://en.wikipedia.org/wiki/.onion).
- [Subaddressing](https://en.wikipedia.org/wiki/Email_address#Subaddressing) support.
- Catch-all or alias functionality for those who own their own domains.
- Use of standard email access protocols such as IMAP, SMTP or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Tecnologia

We prefer our recommended providers to collect as little data as possible.

**O melhor caso:**

- Protect sender's IP address. Filter it from showing in the `Received` header field.
- Don't require personally identifiable information (PII) besides a username and a password.
- Privacy policy that meets the requirements defined by the GDPR.

**Best Case:**

- Accepts [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Hosted in a jurisdiction with strong email privacy protection laws.

### Privacidade

Email servers deal with a lot of very sensitive data. We expect that providers will adopt best industry practices in order to protect their members.

**O melhor caso:**

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

**Best Case:**

- Support for hardware authentication, i.e. U2F and [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F and WebAuthn are more secure as they use a private key stored on a client-side hardware device to authenticate people, as opposed to a shared secret that is stored on the web server and on the client side when using TOTP. Furthermore, U2F and WebAuthn are more resistant to phishing as their authentication response is based on the authenticated [domain name](https://en.wikipedia.org/wiki/Domain_name).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), this is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programas de recompensa de bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Segurança

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? We require our recommended providers to be public about their ownership or leadership. We also would like to see frequent transparency reports, especially in regard to how government requests are handled.

**O melhor caso:**

- Esquemas de Criptografia Fortes: OpenVPN com autenticação SHA-256; RSA-2048 ou melhor aperto de mão; AES-256-GCM ou AES-256-CBC encriptação de dados.

**Best Case:**

- A Encriptação mais forte: RSA-4096.
- Perfect Forward Secrecy (PFS).

### Confiança

With the email providers we recommend we like to see responsible marketing.

**O melhor caso:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.). The provider's site must also comply with [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) for those who wish to opt-out.

Must not have any marketing which is irresponsible:

- Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
- Fazer garantias de protecção do anonimato a 100%. Quando alguém afirma que algo é 100%, significa que não há certeza de fracasso. We know people can quite easily deanonymize themselves in a number of ways, e.g.:

- Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software (Tor, VPN, etc.)
- [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Best Case:**

- Deve auto-instalar análises (sem Google Analytics, etc.). This includes things like, setting up 2FA, email clients, OpenPGP, etc.

### Marketing

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
