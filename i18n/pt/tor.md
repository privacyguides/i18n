---
meta_title: "Navegador e rede Tor: navegação anónima na Web - Privacy Guides"
title: "Rede Tor"
icon: simple/torproject
description: Proteja a sua navegação na Internet de olhares curiosos utilizando a rede Tor, uma rede segura que contorna a censura.
cover: tor.webp
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

![Logótipo do Tor](assets/img/self-contained-networks/tor.svg){ align=right }

A rede **Tor** é um grupo de servidores operados por voluntários que pode utilizar gratuitamente para melhorar a sua privacidade e segurança na Internet. Os indivíduos e as organizações também podem partilhar informações através da rede Tor com os serviços ocultos ".onion", sem comprometer a sua privacidade. O facto do tráfego do Tor ser difícil de bloquear e rastrear, faz dele uma ferramenta eficaz para contornar a censura.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

O Tor encaminha o seu tráfego de Internet através destes servidores operados por voluntários, em vez de estabelecer uma ligação direta ao site que está a tentar visitar. A origem do tráfego fica assim ofuscada e nenhum servidor ao longo do caminho da ligação pode saber o caminho completo, o que significa que mesmo os servidores que utiliza para se ligar não conseguem quebrar o seu anonimato.

[Visão detalhada do Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Ligar ao Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

Existem várias formas de se ligar à rede Tor a partir do seu dispositivo, sendo a mais utilizada o **Navegador Tor**, um fork do Firefox concebido para navegação anónima em computadores desktop e em dispositivos Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Browser Tor

<div class="admonition recommendation" markdown>

![Logótipo Tor](assets/img/browsers/tor.svg){ align=right }

O **Browser Tor** é a escolha certa se precisar de anonimato, uma vez que lhe dá acesso à rede Tor e às sua bridges, e inclui definições por defeito e extensões que são automaticamente configuradas com níveis de segurança predefinidos: *Standard*, *Seguro* e *Máxima Segurança*.

[:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://www.torproject.org/download/#android)
- [:simple-windows11: Windows](https://www.torproject.org/download/)
- [:simple-apple: macOS](https://www.torproject.org/download/)
- [:simple-linux: Linux](https://www.torproject.org/download/)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

**Nunca** devem ser instaladas quaisquer extensões adicionais no Tor ou editadas as configurações `about:config`, incluindo as que sugerimos para o Firefox. Extensões e configurações não-padrão fazem com que se destaque dos outros utilizadores da rede Tor, tornando o seu browser mais suscetível a identificação de [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

O Tor foi concebido para evitar a recolha de impressões digitais, ou a sua identificação com base na configuração. Por esse motivo, é imperativo que **não** modifique o browser para além dos níveis de segurança predefinidos [](https://tb-manual.torproject.org/security-settings/).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Logótipo Orbot](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** é uma VPN Tor gratuita para dispositivos móveis que encaminha o tráfego de qualquer aplicação no seu dispositivo através da rede Tor.

[:octicons-home-16: Homepage](https://orbot.app/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/orbot/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Anteriormente, recomendamos ativar a preferência *Isolar endereço de destino* nas configurações do Orbot. Enquanto esta configuração pode teoricamente melhorar a privacidade ao forçar o uso de um circuito diferente para cada endereço IP ao qual você se conecta, ela não fornece uma vantagem prática para a maioria das aplicações (especialmente navegação na web), pode vir com uma penalidade significativa de desempenho, e aumenta a carga na rede Tor. Não recomendamos mais o ajuste dessa configuração do valor padrão, a menos que saiba que é necessário.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Os dados de cada usuário são criptografados usando sua própria chave de criptografia exclusiva, e os arquivos do sistema operacional são deixados não criptografados. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

O Orbot está frequentemente desatualizado no [repositório F-Droid](https://guardianproject.info/fdroid) e no [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) do Projeto Guardian, então considere fazer o download diretamente do [repositório GitHub](https://github.com/guardianproject/orbot/releases).

[Visite orbot.app](https://orbot.app/){ .md-button .md-button--primary }

**Downloads***
- [:fontawesome-brands-google-play: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:pg-f-droid: F-Droid](https://guardianproject.info/fdroid)
- [:fontawesome-brands-github: GitHub](https://github.com/guardianproject/orbot)
- [:fontawesome-brands-gitlab: GitLab](https://gitlab.com/guardianproject/orbot)

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser/).

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

## Relays e Pontes

### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** permite-lhe doar largura de banda ao Projeto Tor através da utilização de um "proxy Snowflake" no seu navegador.

As pessoas censuradas podem utilizar proxies Snowflake para se ligarem à rede Tor. Snowflake é uma ótima maneira de contribuir para a rede, mesmo que não tenha o conhecimento técnico para executar um retransmissor ou ponte Tor.

[:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

</details>

</div>

Pode ativar o Snowflake no seu navegador abrindo-o noutro separador e ligando o interrutor. Pode deixá-lo a funcionar em segundo plano enquanto navega para contribuir para a sua ligação. Não recomendamos instalar o Snowflake como uma extensão do navegador; adicionar extensões de terceiros pode aumentar a sua superfície de ataque.

[Execute o Snowflake no seu navegador :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

O Snowflake não aumenta a sua privacidade de forma alguma, nem é utilizado para ligar à rede Tor no seu navegador pessoal. No entanto, se a sua ligação à Internet não for censurada, deve considerar a possibilidade de o executar para ajudar as pessoas em redes censuradas a obterem uma maior privacidade. Não há necessidade de se preocupar com os sites a que as pessoas acedem através do seu proxy—o endereço IP de navegação visível corresponderá ao nó de saída Tor, não ao seu.

Executar um proxy Snowflake é de baixo risco, ainda mais do que executar um Relay Tor ou uma ponte, que já não são empreendimentos particularmente arriscados. No entanto, continua a fazer proxy do tráfego através da sua rede, o que pode ter algum impacto, especialmente se a sua rede tiver uma largura de banda limitada. Certifique-se de que compreende [como funciona o Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) antes de decidir se pretende executar um proxy.

[^1]: A definição `IsolateDestAddr` é discutida na [lista de e-mails do Tor](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) e [Documentação do Stream Isolation de Whonix](https://www.whonix.org/wiki/Stream_Isolation), onde ambos os projetos sugerem que normalmente não é uma boa abordagem para a maioria das pessoas.
