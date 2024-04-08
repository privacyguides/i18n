---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
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
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Logótipo do Android](assets/img/android/android.svg){ align=right }

O **Projeto de Código Aberto do Android** é um sistema operativo móvel de código aberto liderado pela Google que alimenta a maioria dos dispositivos móveis do mundo. A maioria dos telemóveis vendidos com Android são modificados para incluir integrações e aplicações invasivas, como o Google Play Services, pelo que pode melhorar significativamente a sua privacidade no seu dispositivo móvel substituindo a instalação predefinida do seu telemóvel por uma versão do Android sem estas funcionalidades invasivas.

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject){ .card-link title="Source Code" }

Estes são os sistemas operativos, dispositivos e aplicações Android que recomendamos para maximizar a segurança e a privacidade do seu dispositivo móvel. Para saber mais sobre o Android:

[Visão Geral do Android :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## Derivados AOSP

Recomendamos instalar um destes sistemas operativos Android personalizados no seu dispositivo, listados por ordem de preferência, dependendo da compatibilidade do seu dispositivo com estes sistemas operativos.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Os dispositivos em fim de vida (como os dispositivos GrapheneOS ou CalyxOS com "suporte alargado") não têm patches de segurança completos (atualizações de firmware) devido ao fato de o OEM ter interrompido o suporte. Estes dispositivos não podem ser considerados completamente seguros, independentemente do software instalado.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![Logótipo GrapheneOS](assets/img/android/grapheneos.svg#only-light){ align=right }
![Logótipo GrapheneOS](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

O **GrapheneOS** é a melhor escolha quando se trata de privacidade e segurança.

O GrapheneOS proporciona melhorias adicionais [reforço da segurança](https://en.wikipedia.org/wiki/Hardening_(computing)) e da privacidade. Tem um [alocador de memória reforçado](https://github.com/GrapheneOS/hardened_malloc), permissões de rede e de sensor e várias outras [características de segurança](https://grapheneos.org/features). O GrapheneOS também vem com atualizações de firmware completas e compilações assinadas, pelo que o arranque verificado é totalmente suportado.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS suporta o [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), que executa [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) totalmente sandboxed como qualquer outro aplicativo regular. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel phones are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices).

[Por que recomendamos GrapheneOS em vez de CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS logo](assets/img/android/divestos.svg){ align=right }

**DivestOS** is a soft-fork of [LineageOS](https://lineageos.org).
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. Tem compilações assinadas, possibilitando ter [arranque verificado](https://source.android.com/security/verifiedboot) em alguns dispositivos não Pixel.

[:octicons-home-16: Página Inicial](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Serviço Onion" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Política de Privacidade" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Código fonte" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribuir }

</div>

O DivestOS tem vulnerabilidades automatizadas do kernel ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), menos blobs proprietários, e um ficheiro [hosts](https://divested.dev/index.php?page=dnsbl) personalizado. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. O DivestOS também inclui patches de kernel do GrapheneOS e habilita todos os recursos de segurança do kernel disponíveis via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

O DivestOS implementa alguns patches de proteção de sistema originalmente desenvolvidos para o GrapheneOS. O DivestOS 16.0 e superior implementa as permissões [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) e SENSORS do GrapheneOS, [alocador de memória endurecido](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constificação](https://en.wikipedia.org/wiki/Const_(computer_programming)), e patchsets parciais de endurecimento [bionic](https://en.wikipedia.org/wiki/Bionic_(software)). 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

O DivestOS utiliza o F-Droid como loja de aplicações por padrão. We normally [recommend avoiding F-Droid](#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) **with the DivestOS repositories enabled** to keep those components up to date. Para outras aplicações, os nossos métodos recomendados para as obter continuam a aplicar-se.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Atualizações do firmware do DivestOS [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) e o controlo de qualidade variam consoante os dispositivos que suporta. Continuamos a recomendar o GrapheneOS, dependendo da compatibilidade do seu dispositivo. Para outros dispositivos, o DivestOS é uma boa alternativa.

Nem todos os dispositivos suportados têm arranque verificado, e alguns têm-no melhor do que outros.

</div>

## Dispositivos Android

Ao comprar um dispositivo, recomendamos que o adquira o mais novo possível. O software e o firmware dos dispositivos móveis só são suportados durante um período limitado, pelo que comprar um novo prolonga o mais possível essa vida útil.

Evite comprar telemóveis a operadores de redes móveis. Estes têm frequentemente um **bootloader bloqueado** e não suportam [desbloqueio OEM](https://source.android.com/devices/bootloader/locking_unlocking). Estas variantes de telemóvel impedem-no de instalar qualquer tipo de distribuição alternativa do Android.

Tenha muito **cuidado** ao comprar telemóveis em segunda mão em mercados online. Verifique sempre a reputação do vendedor. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Existe também o risco de estar associado à atividade do proprietário anterior.

Mais algumas dicas sobre dispositivos Android e compatibilidade com o sistema operativo:

- Não compre dispositivos que tenham atingido ou estejam perto do fim da sua vida útil; as atualizações de firmware adicionais devem ser fornecidas pelo fabricante.
- Não compre telemóveis LineageOS ou /e/ OS pré-carregados ou quaisquer telemóveis Android sem o devido suporte [Verified Boot](https://source.android.com/security/verifiedboot) e atualizações de firmware. Estes dispositivos também não permitem verificar se foram adulterados.
- Em suma, se um dispositivo ou uma distribuição Android não constar da lista, existe provavelmente um bom motivo. Check out our [forum](https://discuss.privacyguides.net) to find details!

### Google Pixel

Os telemóveis Google Pixel são os **únicos dispositivos** que recomendamos para compra. Os telemóveis Pixel têm uma segurança de hardware mais forte do que qualquer outro dispositivo Android atualmente no mercado, devido ao suporte AVB adequado para sistemas operativos de terceiros e aos chips de segurança personalizados [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) da Google, que atuam como elemento seguro.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Os dispositivos **Google Pixel** são conhecidos por terem uma boa segurança e suportarem corretamente o [Verified Boot] (https://source.android.com/security/verifiedboot), mesmo quando instalam sistemas operativos personalizados.

Beginning with the **Pixel 8** and **8 Pro**, Pixel devices receive a minimum of 7 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-5 years competing OEMs typically offer.

[:material-shopping: Loja](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Os Secure Elements, como o Titan M2, são mais limitados do que o Trusted Execution Environment do processador utilizado pela maioria dos outros telemóveis, uma vez que são utilizados apenas para armazenamento de segredos, atestação de hardware e limitação de taxas, e não para executar programas "de confiança". Os telemóveis sem um elemento seguro têm de utilizar o TEE para *todas* essas funções, o que resulta numa maior superfície de ataque.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

A instalação do GrapheneOS num telemóvel Pixel é fácil com o seu [instalador por web](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

Mais algumas dicas para comprar um Google Pixel:

- Se procura uma pechincha num dispositivo Pixel, sugerimos que compre um modelo "**a**", logo após o lançamento do próximo topo de gama. Normalmente, os descontos estão disponíveis porque a Google está a tentar liquidar o seu stock.
- Considere as opções de redução de preços e as promoções oferecidas nas lojas físicas.
- Consulte os sítios de pechinchas da comunidade em linha no seu país. Estes podem alertá-lo para boas vendas.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math> , meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## Aplicações Gerais

Nós recomendamos uma grande variedade de aplicações Android neste sítio web. As aplicações aqui listadas são exclusivas do Android e melhoram ou substituem especificamente as principais funcionalidades do sistema.

### Shelter

<div class="admonition recommendation" markdown>

![Logótipo do Shelter](assets/img/android/shelter.svg){ align=right }

**Shelter** é uma aplicação que o ajuda a tirar partido da funcionalidade Perfil de trabalho do Android para isolar ou duplicar aplicações no seu dispositivo.

O Shelter suporta o bloqueio da pesquisa de contactos entre perfis e a partilha de ficheiros entre perfis através do gestor de ficheiros predefinido ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribute }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

Ao utilizar o Shelter, deposita a total confiança no seu programador, uma vez que o Shelter atua como [Device Admin] (https://developer.android.com/guide/topics/admin/device-admin) para criar o Perfil de Trabalho com um acesso alargado aos dados armazenados no Perfil de Trabalho.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Logótipo da Câmara Segura](assets/img/android/secure_camera.svg#only-light){ align=right }
![Logótipo da Câmara Segura](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** é uma aplicação de câmara centrada na privacidade e segurança que pode captar imagens, vídeos e códigos QR. As extensões do fornecedor CameraX (Retrato, HDR, Visão noturna, retoque facial e Automático) também são suportadas nos dispositivos disponíveis.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

As principais características de privacidade incluem:

- Remoção automática dos metadados [Exif](https://en.wikipedia.org/wiki/Exif) (ativada por predefinição)
- Utilização da nova API [Media](https://developer.android.com/training/data-storage/shared/media), pelo que não são necessárias as [permissões de armazenamento](https://developer.android.com/training/data-storage)
- Não é necessária autorização para microfone, exceto se pretender gravar som

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Atualmente, os metadados não são eliminados dos ficheiros de vídeo, mas isso está planeado.

Os metadados de orientação da imagem não são eliminados. Se ativar a localização (na Câmara segura), esta **não será** apagada. If you want to delete that later you will need to use an external app such as [ExifEraser](data-redaction.md#exiferaser-android).

</div>

### Visualizador de PDF Seguro

<div class="admonition recommendation" markdown>

![Logótipo do Visualizador Seguro de PDF](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Logótipo do Secure PDF Viewer](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

O **Secure PDF Viewer** é um visualizador de PDF baseado em [pdf.js](https://en.wikipedia.org/wiki/PDF.js) que não requer quaisquer permissões. O PDF é introduzido num ficheiro [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). Isto significa que não necessita de permissão direta para aceder a conteúdos ou ficheiros.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) é utilizado para garantir que o JavaScript e as propriedades de estilo no WebView são inteiramente conteúdos estáticos.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Obter Aplicações

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](assets/img/android/obtainium.svg){ align=right }

**Obtainium** is an app manager which allows you to install and update apps directly from the developer's own releases page (i.e. GitHub, GitLab, the developer's website, etc.), rather than a centralized app store/repository. It supports automatic background updates on Android 12 and higher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium allows you to download APK installer files from a wide variety of sources, and it is up to you to ensure those sources and apps are legitimate. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. The risk of installing a malicious *update* is lower, because Android itself verifies that all app updates are signed by the same developer as the existing app on your phone before installing them.

### Loja de Aplicações GrapheneOS

A loja de aplicações GrapheneOS está disponível no [GitHub](https://github.com/GrapheneOS/Apps/releases). Suporta o Android 12 e superior, e é capaz de se atualizar. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). Se estiver à procura destas aplicações, recomendamos vivamente que as obtenha na loja de aplicações GrapheneOS em vez de na Play Store, uma vez que as aplicações na sua loja são assinadas pela própria assinatura do projeto GrapheneOS, à qual a Google não tem acesso.

### Loja Aurora

A Google Play Store requer uma conta do Google para entrar, o que não é ótimo para privacidade. Pode contornar isto utilizando um cliente alternativo, como a Aurora Store.

<div class="admonition recommendation" markdown>

![Logótipo da Aurora Store](assets/img/android/aurora-store.webp){ align=right }

A **Aurora Store** é um cliente da Google Play Store que não requer uma Conta Google, Google Play Services ou microG para transferir aplicações.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

A Aurora Store não permite descarregar aplicações pagas com a sua funcionalidade de conta anónima. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google. However, you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### Manualmente com notificações RSS

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](news-aggregators.md) that will help you keep track of new releases.

![APK do RSS](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![Alterações de APK](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

No GitHub, utilizando [Secure Camera](#secure-camera) como exemplo, deve navegar para a sua [página de lançamentos](https://github.com/GrapheneOS/Camera/releases) e anexar `atom` ao URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

No GitLab, utilizando [Aurora Store](#aurora-store) como exemplo, navegará para o seu [repositório de projeto](https://gitlab.com/AuroraOSS/AuroraStore) e acrescentará `/-/tags?format=atom` ao URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verificar impressões digitais APK

Se descarregar ficheiros APK para instalar manualmente, pode verificar a sua assinatura com a ferramenta [`apksigner`](https://developer.android.com/studio/command-line/apksigner), que faz parte do Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

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

5. Os hashes resultantes podem então ser comparados com outra fonte. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![Logótipo do F-Droid](assets/img/android/f-droid.svg){ align=right width=120px }

==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. A opção de adicionar repositórios de terceiros e não ficar confinado ao jardim murado do Google levou à sua popularidade. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Devido ao seu processo de criação de aplicações, as aplicações no repositório oficial do F-Droid atrasam-se frequentemente nas atualizações. Os manejadores do F-Droid também reutilizam IDs de pacotes enquanto assinam aplicativos com as suas próprias chaves, o que não é ideal, por dar à equipe do F-Droid a confiança final. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. O repositório IzzyOnDroid puxa as compilações diretamente do GitHub e é a melhor coisa a seguir aos repositórios dos próprios programadores. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. Embora isso faça sentido (uma vez que o objetivo desse repositório em particular é alojar aplicações antes de serem aceites no repositório principal do F-Droid), pode deixá-lo com aplicações instaladas que já não recebem atualizações.

That said, the [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>

## Critérios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

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
