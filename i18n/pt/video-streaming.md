---
title: "Streaming de vídeo"
icon: material/video-wireless
description: Estas redes permitem-lhe fazer streaming de conteúdos na Internet sem que seja necessário criar um perfil baseado nos seus interesses.
cover: video-streaming.png
---

A principal ameaça quando se utiliza uma plataforma de streaming de vídeo é que os seus hábitos de streaming e listas de subscrição podem ser utilizados para traçar o seu perfil. Deve combinar estas ferramentas com uma [VPN](vpn.md) ou [com o Tor](https://www.torproject.org/), de forma a dificultar a definição do seu perfil de utilização.

## LBRY

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo LBRY](assets/img/video-streaming/lbry.svg){ align=right }
    
    **A rede LBRY** é uma rede descentralizada de partilha de vídeos. Utiliza uma rede do tipo [BitTorrent](https://wikipedia.org/wiki/BitTorrent) para armazenar o conteúdo de vídeo e uma rede do tipo [blockchain](https://wikipedia.org/wiki/Blockchain) para armazenar os índices desses vídeos. A principal vantagem deste modelo conceptual é a resistência à censura.
    
    **O cliente de desktop LBRY** ajuda-o a fazer stream vídeos da rede LBRY e armazena a sua lista de subscrições na sua própria carteira LBRY.
    
    [:octicons-home-16: Homepage](https://lbry.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://lbry.com/privacypolicy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://lbry.com/faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/lbryio/lbry-desktop){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://lbry.com/windows)
        - [:simple-apple: macOS](https://lbry.com/osx)
        - [:simple-linux: Linux](https://lbry.com/linux)

!!! nota

    Apenas recomendamos a utilização do **cliente LBRY para desktop**, uma vez que o site [Odysee](https://odysee.com) e os clientes LBRY no F-Droid, Play Store e App Store têm sincronização e telemetria obrigatórias.

!!! aviso

    Durante a visualização e hospedagem de vídeos, o seu endereço IP fica visível para a rede LBRY. Considere a utilização de uma [VPN](vpn.md) ou [Tor](https://www.torproject.org) se o seu [modelo de ameaça](basics/threat-modeling.md) exigir a ocultação do seu endereço IP.

Recomendamos ** que não sincronize** a sua carteira com a LBRY Inc., uma vez que a sincronização de carteiras encriptadas ainda não é suportada. Se sincronizar a sua carteira com a LBRY Inc., terá de confiar que a lista de subscrições não será acedida, ou divulgada a fundos [LBC](https://lbry.com/faq/earn-credits), ou mesmo que o controle do canal possa ser assumido indevidamente.

Pode desativar a opção *Guardar dados de alojamento para ajudar a rede LBRY* em :gear: **Definições** → **Definições avançadas**, para evitar a exposição do seu endereço IP e dos vídeos vistos quando utilizar LBRY durante um período de tempo prolongado.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), desenvolvemos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar pela utilização de um projeto, e que faça a sua própria investigação para garantir que a escolha que faz é a certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de definir critérios para cada secção do nosso site, o que pode dar origem a alterações. Se tiver alguma dúvida sobre os nossos critérios, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que omitimos algum projeto nas nossas recomendações, caso ele não se encontre nas nossas recomendações. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e a documentação de cada um deles é um trabalho em curso.

- Não deve ser exigida uma conta centralizada para visualizar vídeos.
    - A autenticação descentralizada através da chave privada de uma carteira móvel é aceitável.
