---
title: "Autenticadores Multifator"
icon: 'O uso de AMF forte pode parar mais de 99% dos acessos não autorizados à conta, e é fácil de configurar nos serviços que você já usa.'
description: Estas ferramentas ajudam-no a proteger as suas contas na Internet com a Autenticação Multifator, sem que sejam enviados os seus segredos a terceiros.
cover: multi-factor-authentication.png
---

## Chaves de Segurança de Hardware

### YubiKey

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![YubiKeys](assets/img/multi-fator-authentication/yubikey.png)
    
    As **YubiKeys** estão entre as chaves de segurança mais populares. Alguns modelos YubiKey têm uma vasta gama de características, como por exemplo: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 WebAuthn](https://en.wikipedia.org/wiki/WebAuthn), [Yubico OTP](https://developers.yubico.com/OTP/), [PIV](https://en.wikipedia.org/wiki/FIPS_201), [OpenPGP](https://developers.yubico.com/PGP/), [TOTP e HOTP](https://developers.yubico.com/OATH/) autenticação.
    
    Um dos benefícios da YubiKey é o facto de ser uma chave que pode fazer quase tudo (YubiKey 5), e que realmente tudo aquilo que se espera de uma chave de segurança de hardware. Aconselhamo-lo a consultar o sítio [quiz](https://www.yubico.com/quiz/) antes de comprar, para ter a certeza de que faz a escolha certa.
    
    [:octicons-home-16: Homepage](https://www.yubico.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://docs.yubico.com/){ .card-link title=Documentação}

A [tabela de comparação](https://www.yubico.com/store/compare/) compara as características dos diferentes tipos de YubiKeys. Recomendamos vivamente que selecione as chaves da série YubiKey 5.

As YubiKeys podem ser programadas utilizando o [YubiKey Manager](https://www.yubico.com/support/download/yubikey-manager/) ou [YubiKey Personalization Tools](https://www.yubico.com/support/download/yubikey-personalization-tools/). Para gerir os códigos TOTP, pode utilizar o [Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/). Todos os clientes da Yubico são de código aberto.

Para os modelos que suportam HOTP e TOTP, existem 2 slots na interface OTP que podem ser utilizadas para HOTP e 32 slots que permitem armazenar segredos TOTP. Estes segredos são armazenados de forma encriptada na chave e nunca são expostos aos dispositivos a que estão ligados. Uma vez que uma semente (segredo compartilhado) é dada ao Yubico Authenticator, o output só consistirá num código de seis dígitos, e nunca na semente. Este modelo de segurança ajuda a limitar o que um atacante pode fazer se comprometer um dos dispositivos que executam o Yubico Authenticator, fazendo com que a YubiKey seja resistente a um atacante físico.

!!! aviso
    O firmware da YubiKey não é de código aberto e não pode ser atualizado. Se pretender novas funcionalidades ou se existir uma vulnerabilidade na versão de firmware que está a utilizar, terá de adquirir uma nova chave.

### Nitrokey

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Nitrokey](assets/img/multi-fator-authentication/nitrokey.jpg){ align=right }
    
    A **Nitrokey** tem uma chave de segurança que suporta [FIDO2 e WebAuthn](basics/multi-fator-authentication.md#fido-fast-identity-online) chamada **Nitrokey FIDO2**. Para suporte de PGP, é necessário adquirir uma das outras chaves, como a **Nitrokey Start**, **Nitrokey Pro 2** ou **Nitrokey Storage 2**.
    
    [:octicons-home-16: Homepage](https://www.nitrokey.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.nitrokey.com/data-privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://docs.nitrokey.com/){ .card-link title=Documentação}

A [tabela de comparação](https://www.nitrokey.com/#comparison) compara as características dos diferentes modelos Nitrokey. O **Nitrokey 3** listado terá um conjunto de características combinadas.

Os modelos Nitrokey podem ser configurados através da aplicação [Nitrokey](https://www.nitrokey.com/download).

Para os modelos que suportam HOTP e TOTP, existem 3 slots para HOTP e 15 para TOTP. Alguns Nitrokeys podem funcionar como gestores de palavras-passe. Podem armazenar 16 credenciais diferentes e encriptá-las utilizando a mesma palavra-passe que a interface OpenPGP.

!!! aviso

    Embora as Nitrokeys não libertem os segredos HOTP/TOTP para o dispositivo a que estão ligados, o armazenamento HOTP e TOTP **não** é encriptado e é vulnerável a ataques físicos. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

!!! aviso

    A reposição da interface OpenPGP numa Nitrokey também fará com que a base de dados de palavras-passe fique [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

A Nitrokey Pro 2, a Nitrokey Storage 2 e a futura Nitrokey 3 suportam a verificação da integridade do sistema para computadores portáteis com o firmware [Coreboot](https://www.coreboot.org/) + [Heads](https://osresearch.net/).

O firmware da Nitrokey é de código aberto, ao contrário do YubiKey. O firmware dos modelos NitroKey modernos (exceto o **NitroKey Pro 2**) pode ser atualizado.

### Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

#### Requisitos mínimos

- Devem ser utilizados módulos de segurança de hardware de alta qualidade e invioláveis.
- Deve ser suportada a especificação FIDO2 mais recente.
- Não deverá ser permitida a extração de chaves privadas.
- Os dispositivos que custam mais de 35 dólares devem suportar o manuseamento de OpenPGP e S/MIME.

#### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Devem estar disponíveis no formato USB-C.
- Deverão disponibilizar NFC.
- Devem suportar o armazenamento de segredos TOTP.
- Devem suportar atualizações de firmware seguras.

## Aplicações de Autenticação

As Aplicações de Autenticação implementam uma norma de segurança que ºe adotada pela Internet Engineering Task Force (IETF), denominada **Time-based One-time Passwords**, ou **TOTP**. Este é um método através do qual os sites partilham um segredo, que é utilizado pela sua aplicação de autenticação para gerar um código de seis dígitos (normalmente) com base na hora atual, que deverá introduzir ao iniciar sessão, para que o site o possa verificar. Normalmente, estes códigos são regenerados de 30 em 30 segundos e, quando é gerado um novo código, o antigo deixa de poder ser utilizado. Mesmo que um pirata informático obtenha o código de seis dígitos, não há forma de reverter esse código para obter o segredo original ou de prever quais serão os códigos futuros.

Recomendamos vivamente que utilize aplicações TOTP para dispositivos móveis, em vez de alternativas para computador, uma vez que o Android e o iOS têm melhor segurança e isolamento de aplicações do que a maioria dos sistemas operativos para PC.

### Aegis Authenticator (Android)

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Aegis](assets/img/multi-fator-authentication/aegis.png){ align=right }
    
    O **Aegis Authenticator** é uma aplicação gratuita, segura e de código aberto para gerir os seus tokens de verificação em duas etapas para os seus serviços online.
    
    [:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://www.buymeacoffee.com/beemdevelopment){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
        - [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

### Raivo OTP (iOS)

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Raivo OTP](assets/img/multi-fator-authentication/raivo-otp.png){ align=right }
    
    O **Raivo OTP** é um cliente de palavras-passe nativo, leve e seguro, para iOS, que é baseado em tempo (TOTP) e em contador (HOTP). O Raivo OTP disponibiliza, opcionalmente, um sistema de cópia de segurança e de sincronização no iCloud. O Raivo OTP também está disponível para o macOS sob a forma de uma aplicação de barra de estado, mas a aplicação para Mac não funciona independentemente da aplicação para iOS.
    
    [:octicons-home-16: Homepage](https://raivo-otp.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://raivo-otp.com/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-code-16:](https://github.com/raivo-otp/ios-application){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://raivo-otp.com/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/raivo-otp/id1459042137)

### Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

- O código-fonte deve estar disponível ao público.
- Não devem exigir ligação à Internet.
- Não podem utilizar um serviço de sincronização/backup numa nuvem de terceiros.
    - O suporte de sincronização E2EE **opcional**, com ferramentas nativas do SO, é aceitável (por exemplo, sincronização encriptada via iCloud).
