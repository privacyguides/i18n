---
meta_title: "Browser e rede Tor: navegação anónima na Web - Privacy Guides"
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
    sameAs: https://pt.wikipedia.org/wiki/Tor_(rede_de_anonimato)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": Página Web
      url: "./"
---

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

A rede **Tor** é um grupo de servidores operados por voluntários que pode utilizar gratuitamente para melhorar a sua privacidade e segurança na Internet. Os indivíduos e as organizações também podem partilhar informações através da rede Tor com os serviços ocultos ".onion", sem comprometer a sua privacidade. O facto do tráfego do Tor ser difícil de bloquear e rastrear, faz dele uma ferramenta eficaz para contornar a censura.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Serviço Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org/) [:octicons-code-16:](https://gitweb.torproject.org/tor.git){ .card-link title=Documentação} { .card-link title="Código-fonte" } [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuir }

O Tor encaminha o seu tráfego de Internet através destes servidores operados por voluntários, em vez de estabelecer uma ligação direta ao site que está a tentar visitar. A origem do tráfego fica assim ofuscada e nenhum servidor ao longo do caminho da ligação é capaz de saber o caminho completo, o que significa que mesmo os servidores que está a utilizar para se ligar não conseguem quebrar o seu anonimato.

[Visão detalhada do Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Ligar ao Tor

Existem várias formas de se ligar à rede Tor a partir do seu dispositivo, sendo a mais utilizada o **Browser Tor**, um fork do Firefox concebido para navegação anónima em computadores desktop e em dispositivos Android. Para além das aplicações abaixo listadas, existem também sistemas operativos concebidos especificamente para se ligarem à rede Tor, como o [Whonix](desktop.md#whonix) em [Qubes OS](desktop.md#qubes-os), que fornecem ainda mais segurança e proteções do que o browser Tor padrão.

### Browser Tor

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Tor](assets/img/browsers/tor.svg){ align=right }
    
    O **Browser Tor** é a escolha certa se precisar de anonimato, uma vez que lhe dá acesso à rede Tor e às sua bridges, e inclui definições por defeito e extensões que são automaticamente configuradas com níveis de segurança predefinidos: *Standard*, *Seguro* e *Máxima Segurança*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Serviço Onion" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentação }
    [:octicons-code-16:](https://gitweb.torproject.org/tor-browser.git/){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! perigo

    **Nunca** devem ser instaladas quaisquer extensões adicionais no Tor ou editadas as configurações `about:config`, incluindo as que sugerimos para o Firefox. Extensões e configurações não-padrão fazem com que se destaque dos outros utilizadores da rede Tor, tornando o seu browser mais suscetível a identificação de [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

O Tor foi concebido para evitar a recolha de impressões digitais, ou a sua identificação com base na configuração. Por esse motivo, é imperativo que **não** modifique o browser para além dos níveis de segurança predefinidos [](https://tb-manual.torproject.org/security-settings/).

### Orbot

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }
    
    **Orbot** é uma VPN Tor gratuita para dispositivos móveis que encaminha o tráfego de qualquer aplicação no seu dispositivo através da rede Tor.
    
    [:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentação}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! tip "Tips for Android"

    Os dados de cada usuário são criptografados usando sua própria chave de criptografia exclusiva, e os arquivos do sistema operacional são deixados não criptografados. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.
    
    Orbot is often outdated on the Guardian Project's [F-Droid repository](https://guardianproject.info/fdroid) and [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android), so consider downloading directly from the [GitHub repository](https://github.com/guardianproject/orbot/releases) instead.
    
    [Visite orbot.app](https://orbot.app/){ .md-button .md-button--primary }
    
    **Downloads***
    - [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
    - [:pg-f-droid: F-Droid](https://guardianproject.info/fdroid)
    - [:fontawesome-brands-github: GitHub](https://github.com/guardianproject/orbot)
    - [:fontawesome-brands-gitlab: GitLab](https://gitlab.com/guardianproject/orbot)

## Relays and Bridges

### Snowflake

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

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

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
