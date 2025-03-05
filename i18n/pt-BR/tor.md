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

[Detalhes do Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Dica</p>

Antes de se conectar ao Tor, certifique-se de ler nosso [overview](advanced/tor-overview.md) sobre o que é Tor e como se conectar com segurança. Geralmente, recomendamos que você se conecte ao Tor por meio de um [provedor de VPN] confiável (vpn.md), mas é preciso fazer isso **de forma adequada** para evitar a diminuição do seu anonimato.

</div>

Há uma variedade de maneiras de se conectar à rede Tor a partir do seu dispositivo, o mais utilizado é o **Navegador Tor**, um fork do Firefox projetado para [:material-incognito: anônimo](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} navegação para computadores de computador e Android.

Alguns desses aplicativos são melhores do que outros, e novamente fazer uma determinação equivale ao seu modelo de ameaça. Se você é um usuário casual do Tor que não está preocupado com o ISP que coleta provas contra você, usar aplicativos como o [Orbot](#orbot) ou aplicativos do navegador móvel para acessar a rede Tor provavelmente não é problema. Aumentar o número de pessoas que usam Tor todos os dias ajuda a reduzir o mau estigma do Tor, e diminui a qualidade das "listas de usuários de Tor" que os ISPs e os governos podem compilar.

Se o anonimato mais completo for fundamental para a sua situação, você deve somente **** utilizar o cliente do navegador Tor para área de trabalho, idealmente em uma configuração de [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os). Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

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

Você nunca deve instalar outras extensões no Navegador Tor ou editar as configurações em `about:config`, incluindo as que sugerimos para o Firefox. downloads

    - [:fontawesome-brands-windows: Windows](https://www.mozilla.org/firefox/windows)
    - [:fontawesome-brands-apple: macOS](https://www.mozilla.org/firefox/mac)
    - [:fontawesome-brands-linux: Linux](https://www.mozilla.org/firefox/linux)
    - [:pg-flathub: Flatpak](https://flathub.org/apps/details/org.mozilla.firefox)
    - [:fontawesome-brands-git: Fonte](https://hg.mozilla.org/mozilla-central)

</div>

Este navegador dá acesso às Pontes Tor (Tor Bridges) e a \[Rede Tor\](https://en.wikipedia.org/wiki/Tor_(rede)), juntamente com extensões que podem ser configuradas automaticamente para se adaptarem aos três níveis de segurança propostos - *Standard*, *Safer* e *Safest*. Portanto, é imperativo que você **não** modifique o navegador além do padrão de níveis de segurança [](https://tb-manual.torproject.org/security-settings).

Além de instalar o Navegador Tor diretamente no seu computador, existem também sistemas operacionais projetados especificamente para se conectar à rede Tor, como [Whonix](desktop.md#whonix) na [Qubes OS](desktop.md#qubes-os), que oferecem segurança e proteção ainda maiores do que o Navegador Tor padrão sozinho.

## Orbot

<div class="admonition recommendation" markdown>

![logótipo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** é uma VPN Tor gratuita para celulares que encaminha o tráfego de qualquer aplicativo no seu dispositivo através da Rede Tor.

[:octicons-home-16: Página inicial](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Política de Privacidade" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentação}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Código Fonte" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Antes, recomendávamos habilitar a opção *"Isolar os endereços de destino"* (Isolate Destination Address) nas configurações do Orbot. Embora essa configuração possa, teoricamente, melhorar a privacidade, impondo o uso de um circuito diferente para cada endereço IP ao qual você se conecta, ela não fornece uma vantagem prática para a maioria dos aplicativos (especialmente a navegação na Internet), podendo vir com uma significativa perda de desempenho, e aumento da sobrecarga na rede Tor. Não recomendamos mais ajustar esta definição a partir do seu valor padrão, a menos que você saiba o que precisa.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Dicas para o Android</p>

Orbot pode fazer proxy em aplicativos individuais se eles suportarem proxy SOCKS ou HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN kill switch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot costuma estar desatualizado no [repositório F-Droid, do Projeto Guardian](https://guardianproject.info/fdroid) e na [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), então, considere baixar diretamente do [repositório GitHub](https://github.com/guardianproject/orbot/releases) em vez disso.

All versions are signed using the same signature, so they should be compatible with each other.

</div>

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Logotipo do navegador Onion](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** é um navegador de código aberto que permite que você navegue na web anonimamente sobre a rede Tor em dispositivos iOS e é endossado pelo [Projeto Tor](https://support.torproject.org/glossary/onion-browser). [:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review/)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

O Onion Browser não oferece os mesmos níveis de proteções de privacidade que o Navegador Tor disponibiliza em plataformas desktop. Para uso casual é uma maneira perfeitamente excelente de acessar serviços ocultos, mas se você está preocupado em ser rastreado ou monitorado por adversários avançados você não deve confiar nisso como uma ferramenta de anonimato.

[^1]: A configuração `IsolateDestAddr` é discutida na [lista de envio Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) e [Documentação de isolamento de transmissão da Whonix's](https://whonix.org/wiki/Stream_Isolation), onde ambos os projetos sugerem que normalmente não é uma boa abordagem para a maioria das pessoas.
