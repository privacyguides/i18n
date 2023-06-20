---
meta_title: "Motores de pesquisa recomendados: alternativas anónimas ao Google - Privacy Guides"
title: "Motores de Busca"
icon: material/search-web
description: Estes motores de busca, que respeitam a privacidade, não criam um perfil de marketing com base nas suas pesquisas.
cover: search-engines.png
---

Utilize um motor de busca que não crie um perfil de marketing com base nas suas pesquisas.

As recomendações aqui apresentadas baseiam-se nos méritos da política de privacidade de cada serviço. Não existe **qualquer garantia** de que estas políticas de privacidade sejam respeitadas.

Considere a utilização de uma [VPN](vpn.md) ou o [Tor](https://www.torproject.org/), se o seu modelo de ameaça exigir a ocultação do seu endereço IP do motor de busca.

## Brave Search

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Brave Search](assets/img/search-engines/brave-search.svg){ align=right }
    
    O **Brave Search** é desenvolvido pela Brave e apresenta resultados que resultam do seu próprio índice independente. O índice está otimizado para emular a pesquisa Google e, por esse motivo, está em condições de fornecer resultados mais precisos em termos contextuais do que outras alternativas.
    
    O Brave Search inclui funcionalidades exclusivas, como as Discussões, que destacam resultados centrados em conversações, como publicações em fóruns.
    
    Recomendamos que desative a opção [Métricas de utilização anónimas] (https://search.brave.com/help/usage-metrics), nas definições, uma vez que está ativada por defeito.
    
    [:octicons-home-16: Homepage](https://search.brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://search.brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://search.brave.com/help/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://search.brave.com/help){ .card-link title=Documentação}

O Brave Search está sediado nos Estados Unidos. A sua [ política de privacidade ](https://search.brave.com/help/privacy-policy) faz saber que recolhem métricas de utilização agregadas, que incluem o sistema operativo e o browser utilizado, mas não são recolhidas informações pessoais. Os endereços IP são processados temporariamente, mas não são armazenados.

## DuckDuckGo

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo DuckDuckGo](assets/img/search-engines/duckduckgo.svg){ align=right }
    
    O **DuckDuckGo** é um dos motores de pesquisa mais comuns, no que toca à privacidade. De entre as suas notáveis funcionalidades de pesquisa, destque para os [bangs](https://duckduckgo.com/bang) e muitas [respostas instantâneas] (https://help.duckduckgo.com/duckduckgo-help-pages/features/instant-answers-and-other-features/). Para fornecer os resultado, o motor de busca baseia-se numa API comercial do Bing, embora utilize diversas [outras fontes] (https://help.duckduckgo.com/results/sources/) para respostas instantâneas e outros resultados não primários.
    
    O DuckDuckGo é o motor de busca predefinido do browser Tor e é uma das poucas opções disponíveis no browser Safari da Apple.
    
    [:octicons-home-16: Homepage](https://duckduckgo.com){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://duckduckgo.com/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://help.duckduckgo.com/){ .card-link title=Documentação}

O DuckDuckGo está sediado nos Estados Unidos. A sua [política de privacidade](https://duckduckgo.com/privacy) faz saber que **são feitos** registos das suas pesquisas para fins de melhoria do produto, mas não o seu endereço IP ou qualquer outra informação de identificação pessoal.

O DuckDuckGo oferece duas [outras versões](https://help.duckduckgo.com/features/non-javascript/) do seu motor de pesquisa, e ambas não requerem JavaScript. No entanto, estas versões carecem de funcionalidades. Estas versões também podem ser utilizadas em conjunto com o seu endereço [onion no Tor](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/), acrescentando [/lite](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/lite) ou [/html](https://duckduckgogg42xjoc72x3sjasowoarfbgcmvfimaftt6twagswzczad.onion/html) para a respectiva versão.

## SearXNG

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo SearXNG](assets/img/search-engines/searxng.svg){ align=right }
    
    **SearXNG** é um motor de meta-pesquisa de código aberto, auto-hospedado, que agrega os resultados de outros motores de busca, sem armazenar qualquer informação. É um fork de [SearX](https://github.com/searx/searx) com atualizações regulares.
    
    [:octicons-home-16: Homepage](https://searxng.org){ .md-button .md-button--primary }
    [:octicons-server-16:](https://searx.space/){ .card-link title="Instâncias públicas"}
    [:octicons-code-16:](https://github.com/searxng/searxng){ .card-link title="Código-fonte" }

O SearXNG funciona como um proxy entre si e os motores de busca que agrega. As suas consultas de pesquisa continuarão a ser enviadas para os motores de busca, sendo os resultados obtidos pelo SearXNG.

Ao usar a auto-hospedagem, é importante as outras pessoas utilizem a sua instância, de forma a que as consultas sejam integradas. Deve ter cuidado com o local e a forma como aloja o SearXNG, uma vez que as pessoas que procuram conteúdos ilegais na sua instância podem chamar a atenção indesejada das autoridades.

Quando estiver a utilizar uma instância do SearXNG, certifique-se de que lê a política de privacidade. Uma vez que as instâncias do SearXNG podem ser modificadas pelos seus proprietários, não é garantido que sigam a sua política de privacidade. Algumas instâncias são executadas como um serviço oculto Tor, o que pode garantir alguma privacidade, desde que as suas consultas de pesquisa não contenham informações pessoais.

## StartPage

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Startpage](assets/img/search-engines/startpage.svg#only-light){ align=right }
    ![Logótipo Startpage](assets/img/search-engines/startpage-dark.svg#only-dark){ align=right }
    
    O **Startpage** é um motor de pesquisa com a privacidade em mente, conhecido por apresentar resultados de pesquisa do Google.  Uma das características únicas do Startpage é a [Visualização anónima] (https://www.startpage.com/en/anonymous-view/), tentando normalizar a atividade do utilizador para que a sua identificação exclusiva seja dificultada. A funcionalidade pode ser útil para ocultar [some](https://support.startpage.com/hc/en-us/articles/4455540212116-The-Anonymous-View-Proxy-technical-details) propriedades da rede e do browser. Ao contrário do que o nome sugere, esta funcionalidade não deve ser utilizada para garantir o anonimato. Se procura anonimato, utilize o [Browser Tor] (tor.md#tor-browser).
    
    [:octicons-home-16: Homepage](https://www.startpage.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.startpage.com/en/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.startpage.com/hc/en-us/categories/4481917470356-Startpage-Search-Engine){ .card-link title=Documentação}

!!! aviso

    O Startpage limita regularmente o acesso a determinados endereços IP, tais como IPs reservados para VPNs ou Tor. O [DuckDuckGo](#duckduckgo) e o [Brave Search](#brave-search) são opções mais amigáveis, se o seu modelo de ameaça exigir que oculte o seu endereço IP do motor de busca.

O Startpage está sediado nos Países Baixos. De acordo com a sua [política de privacidade](https://www.startpage.com/en/privacy-policy/), são registados detalhes como: sistema operativo, tipo de browser e idioma. Não registam o seu endereço IP, pesquisas ou outras informações de identificação pessoal.

O acionista maioritário do Startpage é a System1, uma empresa marketing tecnológico. Não acreditamos que isso constitua um problema, uma vez que têm uma [ política de privacidade](https://system1.com/terms/privacy-policy) separada. A equipa do Privacy Guides contactou o Startpage [em 2020](https://web.archive.org/web/20210118031008/https://blog.privacytools.io/relisting-startpage/) para esclarecer preocupações suscitadas pelo investimento considerável da System1 no serviço. Ficámos satisfeitos com as respostas que recebemos.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

### Requisitos mínimos

- A sua política de privacidade deve garantir que não são recolhidas informações pessoais identificáveis.
- Não deve ser obrigatório criar uma conta.

### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Deve basear-se em software de fonte aberta.
- Não deve bloquear os endereços IP dos nós de saída do Tor.
