---
title: Aplicativos Gerais
description: Os aplicativos listados aqui são exclusivos do Android e melhoram ou substituem as principais funcionalidades do sistema.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Aplicativos gerais para Android
    url: ./
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilitários
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilitários
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilitários
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra a(s) seguinte(s) ameaça(s):</small>

- [:material-bug-outline: Ataques passivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Recomendamos uma ampla variedade de aplicativos Android neste site. Os aplicativos listados aqui são exclusivos do Android e melhoram ou substituem as principais funcionalidades do sistema.

### Shelter

Se o seu dispositivo estiver no Android 15 ou superior, recomendamos o uso do recurso nativo [Private Space](../os/android-overview.md#private-space), em vez disso, que fornece quase a mesma funcionalidade sem precisar confiar e conceder poderosas permissões a um app de terceiros.

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

O **shelter** é um aplicativo que ajuda a alavancar a funcionalidade do Perfil de Trabalho do Android para isolar ou duplicar aplicativos em seu dispositivo.

O Shelter suporta o bloqueio do contato entre perfis e o compartilhamento de arquivos entre perfis através do gerenciador de arquivos padrão ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).

[:octicons-repo-16: Repositório](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Código Fonte" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=Contribuir }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Aviso</p>

Ao usar o Shelter, você está colocando total confiança em seu desenvolvedor, pois o Shelter atua como um [Dispositivo Admin](https://developer.android.com/guide/topics/admin/device-admin) para criar o Perfil de Trabalho, e tem extenso acesso aos dados armazenados dentro do perfil de trabalho.

</div>

O Shelter é recomendado sobre [Insular](https://secure-system.gitlab.io/Insular) e [Island](https://github.com/oasisfeng/island), já que suporta [bloqueio de busca de contatos](https://secure-system.gitlab.io/Insular/faq.html).

### Secure Camera

<small>Protege contra a(s) seguinte(s) ameaça(s):</small>

- [:material-account-search: Exposição Pública](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

O **Secure Camera** é um aplicativo de câmera focado em privacidade e segurança que pode capturar imagens, vídeos e códigos QR. As extensões do fornecedor CameraX (Retrato, HDR, Visão noturna, Retoque facial e Automático) também são compatíveis com os dispositivos disponíveis.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
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

Os principais recursos de privacidade incluem:

- Remoção automática de metadados [Exif](https://en.wikipedia.org/wiki/Exif) (habilitada por padrão)
- Uso do novo [Media](https://developer.android.com/training/data-storage/shared/media) API, portanto [permissões de armazenamento](https://developer.android.com/training/data-storage) não são necessárias
- Permissão do microfone não é necessária a menos que você queira gravar som

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Metadata is not currently deleted from video files, but that is planned.

Os metadados da orientação da imagem não são excluídos. Se você ativar a localização (na Câmera Segura) isso **não** será excluído também. Se você deseja excluir isso mais tarde, você precisará usar um aplicativo externo, como [ExifEraser](../data-redaction.md#exiferaser-android).

</div>

### Secure PDF Viewer

<small>Protege contra a(s) seguinte(s) ameaça(s):</small>

- [:material-target-account: Ataques Localizados](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

O **Secure PDF Viewer** é um visualizador de PDF baseado em [pdf.js] (https://pt.wikipedia.org/wiki/PDF.js) que não requer nenhuma permissão. O PDF é alimentado em um [sandboxed](https://pt.wikipedia.org/wiki/Sandbox_\(desenvolvimento_de_software\)) [WebView](https://developer.android.com/guide/webapps/webview). Isso significa que não requer permissão direta para acessar conteúdo ou arquivos.

A [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) é usada para impor que o JavaScript e as propriedades de estilo dentro do WebView sejam conteúdo totalmente estático.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Critério

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.** Além de [nosso critério padrão](../about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

- As aplicações desta página não devem ser aplicáveis a nenhuma outra categoria de software do site.
- Aplicações gerais devem estender ou substituir as funcionalidades do sistema central.
- Os aplicativos devem receber atualizações e manutenção regulares.
