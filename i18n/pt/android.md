---
meta_title: "Recomendações para Android: GrapheneOS e DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: Pode substituir o sistema operativo do seu telemóvel Android por estas alternativas seguras e respeitadoras de privacidade.
cover: android.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Sistemas Operativos Android Privados
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://pt.wikipedia.org/wiki/Android_(sistema_operativo)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://pt.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Perfis de usuário
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Perfil de trabalho
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Câmara Segura
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Visualizador de PDF Seguro
    applicationCategory: Utilities
    operatingSystem: Android
---

![Logótipo do Android](assets/img/android/android.svg){ align=right }

O **Projeto de Código Aberto do Android** é um sistema operativo móvel de código aberto liderado pela Google que alimenta a maioria dos dispositivos móveis do mundo. A maioria dos telemóveis vendidos com Android são modificados para incluir integrações e aplicações invasivas, como o Google Play Services, pelo que pode melhorar significativamente a sua privacidade no seu dispositivo móvel substituindo a instalação predefinida do seu telemóvel por uma versão do Android sem estas funcionalidades invasivas.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Página Inicial }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Código fonte" }

Estes são os sistemas operativos, dispositivos e aplicações Android que recomendamos para maximizar a segurança e a privacidade do seu dispositivo móvel. Para saber mais sobre o Android:

[Visão Geral do Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Derivados AOSP

Recomendamos instalar um destes sistemas operativos Android personalizados no seu dispositivo, listados por ordem de preferência, dependendo da compatibilidade do seu dispositivo com estes sistemas operativos.

!!! nota

    Os dispositivos em fim de vida (como os dispositivos GrapheneOS ou CalyxOS com "suporte alargado") não têm patches de segurança completos (atualizações de firmware) devido ao fato de o OEM ter interrompido o suporte. Estes dispositivos não podem ser considerados completamente seguros, independentemente do software instalado.

### GrapheneOS

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![Logótipo GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    O **GrapheneOS** é a melhor escolha quando se trata de privacidade e segurança.
    
    O GrapheneOS proporciona melhorias adicionais [reforço da segurança](https://en.wikipedia.org/wiki/Hardening_(computing)) e da privacidade. Tem um [alocador de memória reforçado](https://github.com/GrapheneOS/hardened_malloc), permissões de rede e de sensor e várias outras [características de segurança](https://grapheneos.org/features). O GrapheneOS também vem com atualizações de firmware completas e compilações assinadas, pelo que o arranque verificado é totalmente suportado.
    
    [:octicons-home-16: Página Inicial](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

GrapheneOS suporta o [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), que executa [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) totalmente sandboxed como qualquer outro aplicativo regular. Isto significa que pode tirar partido da maioria dos serviços do Google Play, como as notificações push [](https://firebase.google.com/docs/cloud-messaging/), ao mesmo tempo que lhe dá controlo total sobre as suas permissões e acesso, e, ao mesmo tempo, que os restringe a um perfil de trabalho específico [](os/android-overview.md#work-profile) ou a um perfil de utilizador [](os/android-overview.md#user-profiles) à sua escolha.

Os telemóveis Google Pixel são os únicos dispositivos que cumprem atualmente os requisitos de segurança de hardware do GrapheneOS [](https://grapheneos.org/faq#device-support).

[Por que recomendamos GrapheneOS em vez de CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do DivestOS](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** é um soft-fork do [LineageOS](https://lineageos.org/).
    O DivestOS herda muitos [dispositivos suportados] (https://divestos.org/index.php?page=devices&base=LineageOS) do LineageOS. Tem compilações assinadas, possibilitando ter [arranque verificado](https://source.android.com/security/verifiedboot) em alguns dispositivos não Pixel.
    
    [:octicons-home-16: Página Inicial](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuir }

O DivestOS tem vulnerabilidades automatizadas do kernel ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), menos blobs proprietários, e um ficheiro [hosts](https://divested.dev/index.php?page=dnsbl) personalizado. O seu WebView reforçado, [Mulch](https://gitlab.com/divested-mobile/mulch), permite [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) para todas as arquiteturas e [particionamento do estado da rede](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), e recebe atualizações fora de banda. O DivestOS também inclui patches de kernel do GrapheneOS e habilita todos os recursos de segurança do kernel disponíveis via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). Todos os kernels mais recentes que a versão 3.4 incluem [sanitização de página inteira](https://lwn.net/Articles/334747/) e todos os ~22 kernels compilados pela Clang têm [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) ativado.

O DivestOS implementa alguns patches de proteção de sistema originalmente desenvolvidos para o GrapheneOS. O DivestOS 16.0 e superior implementa as permissões [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) e SENSORS do GrapheneOS, [alocador de memória endurecido](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constificação](https://en.wikipedia.org/wiki/Const_(computer_programming)), e patchsets parciais de endurecimento [bionic](https://en.wikipedia.org/wiki/Bionic_(software)). 17.1 e superior apresenta a opção de randomização completa do GrapheneOS por rede [MAC](https://en.wikipedia.org/wiki/MAC_address#Randomization), [`controle ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html), e opções de tempo limite de reinicialização automática/Wi-Fi/Bluetooth [](https://grapheneos.org/features).

O DivestOS utiliza o F-Droid como loja de aplicações por padrão. Normalmente, recomendamos que evite o F-Droid devido aos seus inúmeros problemas de segurança [](#f-droid). No entanto, fazê-lo no DivestOS não é viável; os programadores atualizam as suas aplicações através dos seus próprios repositórios F-Droid ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) e [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). Recomendamos desativar a aplicação oficial F-Droid e utilizar [Neo Store](https://github.com/NeoApplications/Neo-Store/) com os repositórios DivestOS ativados para manter esses componentes atualizados. Para outras aplicações, os nossos métodos recomendados para as obter continuam a aplicar-se.

!!! aviso

    Atualizações do firmware do DivestOS [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) e o controlo de qualidade variam consoante os dispositivos que suporta. Continuamos a recomendar o GrapheneOS, dependendo da compatibilidade do seu dispositivo. Para outros dispositivos, o DivestOS é uma boa alternativa.
    
    Nem todos os dispositivos suportados têm arranque verificado, e alguns têm-no melhor do que outros.

## Dispositivos Android

Ao comprar um dispositivo, recomendamos que o adquira o mais novo possível. O software e o firmware dos dispositivos móveis só são suportados durante um período limitado, pelo que comprar um novo prolonga o mais possível essa vida útil.

Evite comprar telemóveis a operadores de redes móveis. Estes têm frequentemente um **bootloader bloqueado** e não suportam [desbloqueio OEM](https://source.android.com/devices/bootloader/locking_unlocking). Estas variantes de telemóvel impedem-no de instalar qualquer tipo de distribuição alternativa do Android.

Tenha muito **cuidado** ao comprar telemóveis em segunda mão em mercados online. Verifique sempre a reputação do vendedor. Se o dispositivo for roubado, existe a possibilidade de o [IMEI ser colocado na lista negra](https://www.gsma.com/security/resources/imei-blacklisting/). Existe também o risco de estar associado à atividade do proprietário anterior.

Mais algumas dicas sobre dispositivos Android e compatibilidade com o sistema operativo:

- Não compre dispositivos que tenham atingido ou estejam perto do fim da sua vida útil; as atualizações de firmware adicionais devem ser fornecidas pelo fabricante.
- Não compre telemóveis LineageOS ou /e/ OS pré-carregados ou quaisquer telemóveis Android sem o devido suporte [Verified Boot](https://source.android.com/security/verifiedboot) e atualizações de firmware. Estes dispositivos também não permitem verificar se foram adulterados.
- Em suma, se um dispositivo ou uma distribuição Android não constar da lista, existe provavelmente um bom motivo. Consulte o nosso [fórum](https://discuss.privacyguides.net/) para obter mais informações!

### Google Pixel

Os telemóveis Google Pixel são os **únicos dispositivos** que recomendamos para compra. Os telemóveis Pixel têm uma segurança de hardware mais forte do que qualquer outro dispositivo Android atualmente no mercado, devido ao suporte AVB adequado para sistemas operativos de terceiros e aos chips de segurança personalizados [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) da Google, que atuam como elemento seguro.

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    Os dispositivos **Google Pixel** são conhecidos por terem uma boa segurança e suportarem corretamente o [Verified Boot] (https://source.android.com/security/verifiedboot), mesmo quando instalam sistemas operativos personalizados.
    
    A partir do **Pixel 6** e do **6 Pro**, os dispositivos Pixel recebem um mínimo de 5 anos de atualizações de segurança garantidas, assegurando uma vida útil muito mais longa em comparação com os 2-4 anos que os OEM concorrentes normalmente oferecem.
    
    [:material-shopping: Loja](https://store.google.com/category/phones){ .md-button .md-button--primary }

Os Secure Elements, como o Titan M2, são mais limitados do que o Trusted Execution Environment do processador utilizado pela maioria dos outros telemóveis, uma vez que são utilizados apenas para armazenamento de segredos, atestação de hardware e limitação de taxas, e não para executar programas "de confiança". Os telemóveis sem um elemento seguro têm de utilizar o TEE para *todas* essas funções, o que resulta numa maior superfície de ataque.

Os telemóveis Google Pixel utilizam um TEE OS chamado Trusty, que é [de código aberto](https://source.android.com/security/trusty#whyTrusty), ao contrário de muitos outros telemóveis.

A instalação do GrapheneOS num telemóvel Pixel é fácil com o seu [instalador por web](https://grapheneos.org/install/web). Se não se sentir à vontade para o fazer por si mesmo e estiver disposto a gastar um pouco mais de dinheiro, consulte o [NitroPhone](https://shop.nitrokey.com/shop), uma vez que vem pré-carregado com GrapheneOS da reputada empresa [Nitrokey](https://www.nitrokey.com/about).

Mais algumas dicas para comprar um Google Pixel:

- Se procura uma pechincha num dispositivo Pixel, sugerimos que compre um modelo "**a**", logo após o lançamento do próximo topo de gama. Normalmente, os descontos estão disponíveis porque a Google está a tentar liquidar o seu stock.
- Considere as opções de redução de preços e as promoções oferecidas nas lojas físicas.
- Consulte os sítios de pechinchas da comunidade em linha no seu país. Estes podem alertá-lo para boas vendas.
- A Google fornece uma lista com o [ciclo de suporte](https://support.google.com/nexus/answer/4457705) para cada um dos seus dispositivos. O preço por dia de um dispositivo pode ser calculado da seguinte forma: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$, o que significa que quanto maior for o tempo de utilização do dispositivo, menor será o custo por dia.

## Aplicações Gerais

Nós recomendamos uma grande variedade de aplicações Android neste sítio web. As aplicações aqui listadas são exclusivas do Android e melhoram ou substituem especificamente as principais funcionalidades do sistema.

### Shelter

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do Shelter](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** é uma aplicação que o ajuda a tirar partido da funcionalidade Perfil de trabalho do Android para isolar ou duplicar aplicações no seu dispositivo.
    
    O Shelter suporta o bloqueio da pesquisa de contactos entre perfis e a partilha de ficheiros entre perfis através do gestor de ficheiros predefinido ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Repositório](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribuir }

!!! aviso

    O Shelter é recomendado em relação a [Insular](https://secure-system.gitlab.io/Insular/) e [Island](https://github.com/oasisfeng/island), uma vez que suporta [bloqueio de pesquisa de contactos] (https://secure-system.gitlab.io/Insular/faq.html).
    
    Ao utilizar o Shelter, deposita a total confiança no seu programador, uma vez que o Shelter atua como [Device Admin] (https://developer.android.com/guide/topics/admin/device-admin) para criar o Perfil de Trabalho com um acesso alargado aos dados armazenados no Perfil de Trabalho.

### Auditor

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do Auditor](assets/img/android/auditor.svg#only-light){ align=right }
    ![Logótipo do auditor](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** é uma aplicação que tira partido das funcionalidades de segurança do hardware para fornecer monitorização da integridade do dispositivo, validando ativamente a identidade de um dispositivo e a integridade do seu sistema operativo. Atualmente, só funciona com o GrapheneOS ou com o sistema operativo de stock para [dispositivos suportados] (https://attestation.app/about#device-support).
    
    [:octicons-home-16: Página Inicial](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentação}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

O Auditor efetua a certificação e a deteção de intrusões por:

- Usar um modelo [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) entre um auditor ** e um auditado **, o par estabelece uma chave privada no [keystore suportado por hardware](https://source.android.com/security/keystore/) do *Auditor*.
- O *auditor* pode ser outra instância da aplicação Auditor ou o [Serviço de Certificação Remota](https://attestation.app).
- O *auditor* regista o estado e a configuração atuais do *auditado*.
- Caso ocorra uma adulteração do sistema operativo da entidade *auditada* após a conclusão do emparelhamento, o auditor terá conhecimento da alteração do estado e das configurações do dispositivo.
- Será alertado para a alteração.

Não são transmitidas ao serviço de atestação quaisquer informações pessoais identificáveis. Recomendamos que se registe com uma conta anónima e que ative o atestado remoto para uma monitorização contínua.

Se o seu [modelo de ameaça](basics/threat-modeling.md) requer privacidade, pode considerar a utilização do [Orbot](tor.md#orbot) ou de uma VPN para ocultar o seu endereço IP do serviço de atestação. Para se certificar de que o seu hardware e sistema operativo são genuínos, realize [uma certificação local](https://grapheneos.org/install/web#verifying-installation) imediatamente após a instalação do dispositivo e antes de qualquer ligação à Internet.

### Câmara Segura

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo da Câmara Segura](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Logótipo da Câmara Segura](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** é uma aplicação de câmara centrada na privacidade e segurança que pode captar imagens, vídeos e códigos QR. As extensões do fornecedor CameraX (Retrato, HDR, Visão noturna, retoque facial e Automático) também são suportadas nos dispositivos disponíveis.
    
    [:octicons-repo-16: Repositório](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

As principais características de privacidade incluem:

- Remoção automática dos metadados [Exif](https://en.wikipedia.org/wiki/Exif) (ativada por predefinição)
- Utilização da nova API [Media](https://developer.android.com/training/data-storage/shared/media), pelo que não são necessárias as [permissões de armazenamento](https://developer.android.com/training/data-storage)
- Não é necessária autorização para microfone, exceto se pretender gravar som

!!! nota

    Atualmente, os metadados não são eliminados dos ficheiros de vídeo, mas isso está planeado.
    
    Os metadados de orientação da imagem não são eliminados. Se ativar a localização (na Câmara segura), esta **não será** apagada. Se pretender eliminar essa informação mais tarde, terá de utilizar uma aplicação externa, como [ExifEraser](data-redaction.md#exiferaser).

### Visualizador de PDF Seguro

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do Visualizador Seguro de PDF](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Logótipo do Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    O **Secure PDF Viewer** é um visualizador de PDF baseado em [pdf.js](https://en.wikipedia.org/wiki/PDF.js) que não requer quaisquer permissões. O PDF é introduzido num ficheiro [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). Isto significa que não necessita de permissão direta para aceder a conteúdos ou ficheiros.
    
    [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) é utilizado para garantir que o JavaScript e as propriedades de estilo no WebView são inteiramente conteúdos estáticos.
    
    [:octicons-repo-16: Repositório](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Código fonte" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Obter Aplicações

### Loja de Aplicações GrapheneOS

A loja de aplicações GrapheneOS está disponível no [GitHub](https://github.com/GrapheneOS/Apps/releases). Suporta o Android 12 e superior, e é capaz de se atualizar. A loja de aplicações tem aplicações autónomas criadas pelo projeto GrapheneOS, tais como [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), e [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Se estiver à procura destas aplicações, recomendamos vivamente que as obtenha na loja de aplicações GrapheneOS em vez de na Play Store, uma vez que as aplicações na sua loja são assinadas pela própria assinatura do projeto GrapheneOS, à qual a Google não tem acesso.

### Loja Aurora

A Google Play Store requer uma conta do Google para entrar, o que não é ótimo para privacidade. Pode contornar isto utilizando um cliente alternativo, como a Aurora Store.

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo da Aurora Store](assets/img/android/aurora-store.webp){ align=right }
    
    A **Aurora Store** é um cliente da Google Play Store que não requer uma Conta Google, Google Play Services ou microG para transferir aplicações.
    
    [:octicons-home-16: Página Inicial](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Código fonte" }
    
    ??? downloads
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

A Aurora Store não permite descarregar aplicações pagas com a sua funcionalidade de conta anónima. Opcionalmente, pode iniciar sessão com a sua conta Google na Aurora Store para descarregar aplicações que tenha comprado, o que dá acesso à lista de aplicações que instalou para a Google, mas continua a beneficiar do facto de não necessitar do cliente Google Play completo e do Google Play Services ou do microG no seu dispositivo.

### Manualmente com notificações RSS

Para aplicações que são lançadas em plataformas como o GitHub e o GitLab, poderá ser possível adicionar um feed RSS ao seu [agregador de notícias](/news-aggregators) que o ajudará a acompanhar os novos lançamentos.

![APK do RSS](./assets/img/android/rss-apk-light.png#only-light) ![APK do RSS](./assets/img/android/rss-apk-dark.png#only-dark) ![Alterações de APK](./assets/img/android/rss-changes-light.png#only-light) ![Alterações de APK](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

No GitHub, utilizando [Secure Camera](#secure-camera) como exemplo, deve navegar para a sua [página de lançamentos](https://github.com/GrapheneOS/Camera/releases) e anexar `atom` ao URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

No GitLab, utilizando [Aurora Store](#aurora-store) como exemplo, navegará para o seu [repositório de projeto](https://gitlab.com/AuroraOSS/AuroraStore) e acrescentará `/-/tags?format=atom` ao URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verificar impressões digitais APK

Se descarregar ficheiros APK para instalar manualmente, pode verificar a sua assinatura com a ferramenta [`apksigner`](https://developer.android.com/studio/command-line/apksigner), que faz parte do Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Instale [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Descarregue as ferramentas de linha de comandos do [Android Studio](https://developer.android.com/studio#command-tools).

3. Extraia o arquivo descarregado:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Execute o comando de verificação da assinatura:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. Os hashes resultantes podem então ser comparados com outra fonte. Alguns programadores, como o Signal, [mostram as impressões digitais](https://signal.org/android/apk/) no seus sítio web.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Logótipo do F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==Nós **não** recomendamos atualmente o F-Droid como forma de obter aplicações.== O F-Droid é frequentemente recomendado como alternativa ao Google Play, especialmente na comunidade de privacidade. A opção de adicionar repositórios de terceiros e não ficar confinado ao jardim murado do Google levou à sua popularidade. Além disso, o F-Droid tem [builds reproduzíveis](https://f-droid.org/en/docs/Reproducible_Builds/) para algumas aplicações e dedica-se ao software livre e de código aberto. No entanto, existem [problemas notáveis](https://privsec.dev/posts/android/f-droid-security-issues/) com o cliente oficial F-Droid, o seu controlo de qualidade e a forma como constroem, assinam e entregam os pacotes.

Devido ao seu processo de criação de aplicações, as aplicações no repositório oficial do F-Droid atrasam-se frequentemente nas atualizações. Os manejadores do F-Droid também reutilizam IDs de pacotes enquanto assinam aplicativos com as suas próprias chaves, o que não é ideal, por dar à equipe do F-Droid a confiança final.

Outros repositórios populares de terceiros, como [IzzyOnDroid](https://apt.izzysoft.de/fdroid/), aliviam algumas dessas preocupações. O repositório IzzyOnDroid puxa as compilações diretamente do GitHub e é a melhor coisa a seguir aos repositórios dos próprios programadores. No entanto, não é algo que possamos recomendar, uma vez que as aplicações são normalmente [removidas](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) desse repositório quando chegam ao repositório principal do F-Droid. Embora isso faça sentido (uma vez que o objetivo desse repositório em particular é alojar aplicações antes de serem aceites no repositório principal do F-Droid), pode deixá-lo com aplicações instaladas que já não recebem atualizações.

Dito isto, os repositórios [F-Droid](https://f-droid.org/en/packages/) e [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) são o lar de inúmeras aplicações, pelo que podem ser uma ferramenta útil para procurar e descobrir aplicações de código aberto que podem ser transferidas através da Play Store, da Aurora Store ou obtendo o APK diretamente do programador. É importante ter em conta que algumas aplicações nestes repositórios não são atualizadas há anos e podem depender de bibliotecas não suportadas, entre outras coisas, representando um potencial risco de segurança. Deve usar o seu bom senso ao procurar novas aplicações através deste método.

!!! nota

    Em alguns casos raros, o programador de uma aplicação só a distribui através do F-Droid ([Gadgetbridge](https://gadgetbridge.org/) é um exemplo disso). Se precisar mesmo de uma aplicação como esta, recomendamos que utilize a [Neo Store](https://github.com/NeoApplications/Neo-Store/) em vez da aplicação oficial F-Droid para a obter.

## Critérios

**Por favor note que não somos afiliados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrões](about/criteria.md), nós desenvolvemos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por utilizar um projeto e que faça a sua própria investigação para garantir que é a escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios definidos para cada secção do nosso sítio, o que pode estar sujeito a alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum](https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

### Sistemas Operativos

- O software deve ser de código aberto.
- Deve suportar o bloqueio do carregador de arranque com suporte de chave AVB personalizada.
- Deve receber as principais atualizações do Android no prazo de 0 a 1 mês após o lançamento.
- Deve receber atualizações de funcionalidades Android (versão secundária) no prazo de 0-14 dias após o lançamento.
- Deve receber regularmente correções de segurança no prazo de 0 a 5 dias após o lançamento.
- Deve **não** estar "enraizado" fora da caixa.
- Deve **não** ativar o Google Play Services por predefinição.
- Deve **não** exigir a modificação do sistema para suportar o Google Play Services.

### Dispositivos

- Deve suportar pelo menos um dos nossos sistemas operativos personalizados recomendados.
- Deve ser atualmente vendido novo nas lojas.
- Deve receber um mínimo de 5 anos de atualizações de segurança.
- Deve ter hardware dedicado a elementos seguros.

### Aplicações

- As aplicações desta página não devem ser aplicáveis a nenhuma outra categoria de software do sítio.
- As aplicações gerais devem alargar ou substituir a funcionalidade central do sistema.
- As aplicações devem receber actualizações e manutenção regulares.
