---
title: "Ferramentas de produtividade"
icon: material/file-sign
description: A maioria das suites de escritório online não suporta E2EE, o que significa que o fornecedor da nuvem tem acesso a tudo o que faz.
cover: productivity.png
---

A maioria das suites de escritório online não suporta E2EE, o que significa que o fornecedor da nuvem tem acesso a tudo o que faz. A política de privacidade pode proteger legalmente os seus direitos, mas não prevê restrições técnicas de acesso.

## Plataformas de colaboração

### LibreOffice

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Nextcloud](assets/img/productivity/nextcloud.svg){ align=right }
    
    O **Nextcloud** é um conjunto de software cliente-servidor gratuito e de código aberto que lhe permite criar os seus próprios serviços de alojamento de ficheiros num servidor que controla.
    
    [:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/nextcloud)

!!! perigo

    Não recomendamos a utilização da [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) para o Nextcloud, uma vez que pode levar à perda de dados; é altamente experimental e não tem qualidade de produção. Por esse motivo, não recomendamos fornecedores Nextcloud de terceiros.

### CryptPad

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo CryptPad](assets/img/productivity/cryptpad.svg){ align=right }
    
    O **CryptPad** é uma alternativa privada por design às ferramentas de escritório populares. Todos os conteúdos deste serviço Web são encriptados de ponta a ponta e podem ser facilmente partilhados com outros utilizadores.
    
    [:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE/){ .card-link title="Olítica de Privacidade" }
    [:octicons-info-16:](https://docs.cryptpad.fr/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribuir }

### Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

Em geral, definimos as plataformas de colaboração como suites completas que podem razoavelmente atuar como substitutos de plataformas de colaboração, como o Google Drive.

- Código aberto.
- Torna os ficheiros acessíveis através de WebDAV, a menos que tal seja impossível devido ao E2EE.
- Tem clientes de sincronização para Linux, macOS e Windows.
- Suporta a edição de documentos e folhas de cálculo.
- Suporta a colaboração de documentos em tempo real.
- Suporta a exportação de documentos para formatos de documento padrão (por exemplo, ODF).

#### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Deve armazenar ficheiros num sistema de ficheiros convencional.
- Deve suportar a autenticação multifator TOTP ou FIDO2, ou logins Passkey.

## Suites de escritório

### LibreOffice

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![LibreOffice logo](assets/img/productivity/libreoffice.svg){ align=right }
    
    **LibreOffice** is a free and open-source office suite with extensive functionality.
    
    [:octicons-home-16: Homepage](https://www.libreoffice.org){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation/){ .card-link title=Documentation}
    [:octicons-code-16:](https://www.libreoffice.org/about-us/source-code){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.libreoffice.org/donate/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-appstore: App Store](https://www.libreoffice.org/download/android-and-ios/)
        - [:simple-windows11: Windows](https://www.libreoffice.org/download/download/)
        - [:simple-apple: macOS](https://www.libreoffice.org/download/download/)
        - [:simple-linux: Linux](https://www.libreoffice.org/download/download/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/editors/libreoffice/)

### OnlyOffice

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![OnlyOffice logo](assets/img/productivity/onlyoffice.svg){ align=right }
    
    **OnlyOffice** is a cloud-based free and open-source office suite with extensive functionality, including integration with Nextcloud.
    
    [:octicons-home-16: Homepage](https://www.onlyoffice.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
        - [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)
        - [:simple-freebsd: FreeBSD](https://www.freshports.org/www/onlyoffice-documentserver/)

### Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

In general, we define office suites as applications which could reasonably act as a replacement for Microsoft Word for most needs.

- Must be cross-platform.
- Must be open-source software.
- Must function offline.
- Must support editing documents, spreadsheets, and slideshows.
- Must export files to standard document formats.

## Paste services

### PrivateBin

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![PrivateBin logo](assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** is a minimalist, open-source online pastebin where the server has zero knowledge of pasted data. Data is encrypted/decrypted in the browser using 256-bit AES. It is the improved version of ZeroBin. There is a [list of instances](https://privatebin.info/directory/).
    
    [:octicons-home-16: Homepage](https://privatebin.info){ .md-button .md-button--primary }
    [:octicons-server-16:](https://privatebin.info/directory/){ .card-link title="Public Instances"}
    [:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="Source Code" }

### Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

#### Minimum Requirements

- Must be open-source.
- Must implement "zero-trust" end-to-end encryption.
- Must support password-protected files.


#### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should have a published audit from a reputable, independent third-party.
