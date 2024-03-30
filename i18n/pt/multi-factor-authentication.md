---
title: "Multi-Factor Authenticators"
icon: 'material/two-factor-authentication'
description: These tools assist you with securing your internet accounts with Multi-Factor Authentication without sending your secrets to a third-party.
cover: multi-factor-authentication.webp
---

## Chaves de Segurança de Hardware

### YubiKey

<div class="admonition recommendation" markdown>

![YubiKeys](assets/img/multi-fator-authentication/yubikey.png)

As **YubiKeys** estão entre as chaves de segurança mais populares. Some YubiKey models have a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

Um dos benefícios da YubiKey é o facto de ser uma chave que pode fazer quase tudo (YubiKey 5), e que realmente tudo aquilo que se espera de uma chave de segurança de hardware. We do encourage you to take the [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

[:octicons-home-16: Homepage](https://yubico.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare. Recomendamos vivamente que selecione as chaves da série YubiKey 5.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

Para os modelos que suportam HOTP e TOTP, existem 2 slots na interface OTP que podem ser utilizadas para HOTP e 32 slots que permitem armazenar segredos TOTP. Estes segredos são armazenados de forma encriptada na chave e nunca são expostos aos dispositivos a que estão ligados. Uma vez que uma semente (segredo compartilhado) é dada ao Yubico Authenticator, o output só consistirá num código de seis dígitos, e nunca na semente. Este modelo de segurança ajuda a limitar o que um atacante pode fazer se comprometer um dos dispositivos que executam o Yubico Authenticator, fazendo com que a YubiKey seja resistente a um atacante físico.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

The firmware of YubiKey is not open source and is not updatable. Se pretender novas funcionalidades ou se existir uma vulnerabilidade na versão de firmware que está a utilizar, terá de adquirir uma nova chave.

</div>

### Nitrokey

<div class="admonition recommendation" markdown>

![Nitrokey](assets/img/multi-fator-authentication/nitrokey.jpg){ align=right }

A **Nitrokey** tem uma chave de segurança que suporta [FIDO2 e WebAuthn](basics/multi-fator-authentication.md#fido-fast-identity-online) chamada **Nitrokey FIDO2**. Para suporte de PGP, é necessário adquirir uma das outras chaves, como a **Nitrokey Start**, **Nitrokey Pro 2** ou **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. O **Nitrokey 3** listado terá um conjunto de características combinadas.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

Para os modelos que suportam HOTP e TOTP, existem 3 slots para HOTP e 15 para TOTP. Alguns Nitrokeys podem funcionar como gestores de palavras-passe. Podem armazenar 16 credenciais diferentes e encriptá-las utilizando a mesma palavra-passe que a interface OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Embora as Nitrokeys não libertem os segredos HOTP/TOTP para o dispositivo a que estão ligados, o armazenamento HOTP e TOTP **não** é encriptado e é vulnerável a ataques físicos. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

A reposição da interface OpenPGP numa Nitrokey também fará com que a base de dados de palavras-passe fique [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

The Nitrokey Pro 2, Nitrokey Storage 2, and the upcoming Nitrokey 3 supports system integrity verification for laptops with the [Coreboot](https://coreboot.org) + [Heads](https://osresearch.net) firmware.

Nitrokey's firmware is open source, unlike the YubiKey. O firmware dos modelos NitroKey modernos (exceto o **NitroKey Pro 2**) pode ser atualizado.

### Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

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

### ente Auth

<div class="admonition recommendation" markdown>

![ente Auth logo](assets/img/multi-factor-authentication/ente-auth.png){ align=right }

**ente Auth** is a free and open-source app which stores and generates TOTP tokens on your mobile device. It can be used with an online account to backup and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/ente-io/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

### Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** is a free and open-source app for Android to manage your 2-step verification tokens for your online services. Aegis Authenticator operates completely offline/locally, but includes the option to export your tokens for backup unlike many alternatives.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

### Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

- O código-fonte deve estar disponível ao público.
- Não devem exigir ligação à Internet.
- Não podem utilizar um serviço de sincronização/backup numa nuvem de terceiros.
    - O suporte de sincronização E2EE **opcional**, com ferramentas nativas do SO, é aceitável (por exemplo, sincronização encriptada via iCloud).
