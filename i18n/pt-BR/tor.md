---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "Rede Tor"
icon: simple/torproject
description: Proteja a sua navegação na Internet de olhares curiosos utilizando a rede Tor, uma rede segura que contorna a censura.
cover: tor.png
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Navegador Tor
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
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

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

A rede **Tor** é um grupo de servidores operados por voluntários que permite que você se conecte gratuitamente para melhorar a sua privacidade e segurança na Internet. Os indivíduos e organizações também podem compartilhar informações através da rede Tor com "serviços ocultos .onion", sem comprometer sua privacidade. Como o tráfego do Tor é difícil de bloquear e rastrear, o Tor é uma ferramenta eficaz para contornar a censura.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

O Tor funciona roteando seu tráfego de internet através desses servidores operados por voluntários, em vez de fazer uma conexão direta com o site que você está tentando visitar. Isto esconde de onde vem o tráfego, e nenhum servidor no caminho de conexão consegue ver toda a trajetória de onde o tráfego vem e para onde vai, isto significa que mesmo os servidores que você está usando para conectar não podem quebrar seu anonimato.

[Detalhes do Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Conectando-se ao Tor

Existem várias maneiras de se conectar à rede Tor a partir do seu dispositivo, a mais usada é o **Navegador Tor**, um garfo do Firefox projetado para navegação anônima em computadores e em celulares Android. Além dos aplicativos listados abaixo, também existem sistemas operacionais projetados especificamente para se conectar à rede Tor, como [Whonix](desktop.md#whonix) no [Qubes OS](desktop.md#qubes-os), que proporcionam ainda mais segurança e proteção do que o tradicional Navegador Tor.

### Navegador Tor

!!! recommendation

    ![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }
    
    O **Navegador Tor** é a melhor opção se você quer anonimato, pois ele fornece acesso à rede Tor e pontes, e inclui configurações padrão e extensões que são configuradas automaticamente pelos níveis de segurança: *Padrão*, *Mais seguro* e *O Mais Seguro*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! danger

    Você nunca deve instalar outras extensões no Navegador Tor ou editar as configurações em `about:config`, incluindo as que sugerimos para o Firefox. downloads
    
        - [:fontawesome-brands-windows: Windows](https://www.mozilla.org/firefox/windows)
        - [:fontawesome-brands-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:fontawesome-brands-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:pg-flathub: Flatpak](https://flathub.org/apps/details/org.mozilla.firefox)
        - [:fontawesome-brands-git: Fonte](https://hg.mozilla.org/mozilla-central)

Este navegador dá acesso às Pontes Tor (Tor Bridges) e a \[Rede Tor\](https://en.wikipedia.org/wiki/Tor_(rede)), juntamente com extensões que podem ser configuradas automaticamente para se adaptarem aos três níveis de segurança propostos - *Standard*, *Safer* e *Safest*. Portanto, é importante que você **não** modifique o navegador fora dos [níveis de segurança disponíveis](https://tb-manual.torproject.org/security-settings/).

### Orbot

!!! recommendation

    ![logótipo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** é uma VPN Tor gratuita para celulares que encaminha o tráfego de qualquer aplicativo no seu dispositivo através da Rede Tor.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

Antes, recomendávamos habilitar a opção *"Isolar os endereços de destino"* (Isolate Destination Address) nas configurações do Orbot. Embora essa configuração possa, teoricamente, melhorar a privacidade, impondo o uso de um circuito diferente para cada endereço IP ao qual você se conecta, ela não fornece uma vantagem prática para a maioria dos aplicativos (especialmente a navegação na Internet), podendo vir com uma significativa perda de desempenho, e aumento da sobrecarga na rede Tor. Nós não mais recomendamos que você mude esta configuração do seu valor padrão, a menos que você saiba que precisa disso.[^1]

!!! tip "Tips for Android"

    Orbot pode fazer proxy em aplicativos individuais se eles suportarem proxy SOCKS ou HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot costuma estar desatualizado no [repositório F-Droid, do Projeto Guardian](https://guardianproject.info/fdroid) e na [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), então, considere baixar diretamente do [repositório GitHub](https://github.com/guardianproject/orbot/releases) em vez disso.
    
    All versions are signed using the same signature so they should be compatible with each other.

### Onion Browser

!!! recommendation

    ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }
    
    **Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser/).
    
    [:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

## Relays and Bridges

### Snowflake

!!! recommendation

    ![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** allows you to donate bandwidth to the Tor Project by operating a "Snowflake proxy" within your browser.
    
    People who are censored can use Snowflake proxies to connect to the Tor network. Snowflake is a great way to contribute to the network even if you don't have the technical know-how to run a Tor relay or bridge.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitweb.torproject.org/pluggable-transports/snowflake.git/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

You can enable Snowflake in your browser by opening it in another tab and turning the switch on. You can leave it running in the background while you browse to contribute your connection. We don't recommend installing Snowflake as a browser extension; adding third-party extensions can increase your attack surface.

[Run Snowflake in your Browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake does not increase your privacy in any way, nor is it used to connect to the Tor network within your personal browser. However, if your internet connection is uncensored, you should consider running it to help people in censored networks achieve better privacy themselves. There is no need to worry about which websites people are accessing through your proxy—their visible browsing IP address will match their Tor exit node, not yours.

Running a Snowflake proxy is low-risk, even moreso than running a Tor relay or bridge which are already not particularly risky endeavours. However, it does still proxy traffic through your network which can be impactful in some ways, especially if your network is bandwidth-limited. Make sure you understand [how Snowflake works](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) before deciding whether to run a proxy.

[^1]: A configuração `"Isolar os endereços de destino"` (IsolateDestAddr) é discutida na [lista de e-mails do Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) e na documentação ["Whonix's Stream Isolation"](https://www.whonix.org/wiki/Stream_Isolation), onde ambos os projetos sugerem que, normalmente, essa não é uma boa opção para a maioria das pessoas.
