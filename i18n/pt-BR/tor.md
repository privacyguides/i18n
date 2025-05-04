---
meta_title: "Navegador e Rede Tor: Navegação anônima na Web - Guias de privacidade"
title: "Navegador Tor"
icon: simple/torbrowser
description: Proteja a sua navegação na Internet de olhares curiosos utilizando a rede Tor, uma rede segura que contorna a censura.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Navegador Tor
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Navegador de Internet
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protege contra a(s) seguinte(s) ameaça(s):</small>

- [:material-account-cash: Capitalismo de Vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Vigilância em massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

A rede **Tor** é um grupo de servidores operados por voluntários que permite que você se conecte gratuitamente para melhorar a sua privacidade e segurança na Internet. Os indivíduos e organizações também podem compartilhar informações através da rede Tor com "serviços ocultos .onion", sem comprometer sua privacidade. Como o tráfego do Tor é difícil de bloquear e rastrear, o Tor é uma ferramenta eficaz para contornar a censura.

[Uma visão geral do navegador Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Por que você precisa do Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Dica</p>

Antes de se conectar ao Tor, certifique-se de ler nosso [overview](advanced/tor-overview.md) sobre o que é Tor e como se conectar com segurança. Geralmente, recomendamos que você se conecte ao Tor por meio de um [provedor de VPN] confiável (vpn.md), mas é preciso fazer isso **de forma adequada** para evitar a diminuição do seu anonimato.

</div>

Há uma variedade de maneiras de se conectar à rede Tor a partir do seu dispositivo, o mais utilizado é o **Navegador Tor**, um fork do Firefox projetado para [:material-incognito: anônimo](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} navegação para computadores de computador e Android.

Alguns desses aplicativos são melhores do que outros, e novamente fazer uma determinação equivale ao seu modelo de ameaça. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. Aumentar o número de pessoas que usam Tor todos os dias ajuda a reduzir o mau estigma do Tor, e diminui a qualidade das "listas de usuários de Tor" que os ISPs e os governos podem compilar.

Se o anonimato mais completo for fundamental para a sua situação, você deve somente **** utilizar o cliente do navegador Tor para área de trabalho, idealmente em uma configuração de [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Navegadores móveis com acesso à rede Tor são escolhas menos comuns (e mais rastreáveis) para o usuário final, algumas de suas configurações não passaram por testes de segurança e desanimalização.

## Navegador Tor

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

O **Navegador Tor** é a melhor opção se você quer anonimato, pois ele fornece acesso à rede Tor e pontes, e inclui configurações padrão e extensões que são configuradas automaticamente pelos níveis de segurança: *Padrão*, *Mais seguro* e *O Mais Seguro*.

[:octicons-home-16: Página inicial](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Serviço Onion }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentação }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Código Fonte" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Perigo</p>

Você nunca deve instalar outras extensões no Navegador Tor ou editar as configurações em `about:config`, incluindo as que sugerimos para o Firefox. Extensões de navegador e configurações personalizadas fazem com que você se destaque dos outros na rede Tor, tornando seu navegador mais fácil de [ser detectado](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

O Navegador Tor foi projetado para evitar a coleta de suas "impressões digitais" ou a identificação do usuário com base na configuração do navegador. Portanto, é imperativo que você **não** modifique o navegador além do padrão de níveis de segurança [](https://tb-manual.torproject.org/security-settings). When modifying the security level setting, you **must** always restart the browser before continuing to use it. Otherwise, [the security settings may not be fully applied](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw/), putting you at a higher risk of fingerprinting and exploits than you may expect based on the setting chosen.

Além de instalar o Navegador Tor diretamente no seu computador, existem também sistemas operacionais projetados especificamente para se conectar à rede Tor, como [Whonix](desktop.md#whonix) na [Qubes OS](desktop.md#qubes-os), que oferecem segurança e proteção ainda maiores do que o Navegador Tor padrão sozinho.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Logotipo do navegador Onion](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** é um navegador de código aberto que permite que você navegue na web anonimamente sobre a rede Tor em dispositivos iOS e é endossado pelo [Projeto Tor](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Leia a nossa última análise do Onion Browser.](/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Página Inicial](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Política de Privacidade }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Código Fonte" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribua com o projeto }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

O Onion Browser não oferece os mesmos níveis de proteções de privacidade que o Navegador Tor disponibiliza em plataformas ‘desktop’. Para uso casual é uma maneira perfeitamente excelente de acessar serviços ocultos, mas se você está preocupado em ser rastreado ou monitorado por adversários avançados você não deve confiar nisso como uma ferramenta de anonimato.

[É importante observar que](https://github.com/privacyguides/privacyguides.org/issues/2929) O Onion Browser não *garante que* todas as solicitações passem pelo Tor. Ao usar a versão integrada do Tor, [seu IP real **será** vazado via WebRTC e fluxos de áudio/vídeo](https://onionbrowser.com/faqs) devido às limitações do WebKit. It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
