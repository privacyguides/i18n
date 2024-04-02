---
title: "Partilha e sincronização de ficheiros"
icon: material/share-variant
description: Descubra como partilhar os seus ficheiros em privado entre os seus dispositivos, com os seus amigos e família, ou anonimamente online.
cover: file-sharing.webp
---

Descubra como partilhar os seus ficheiros em privado entre os seus dispositivos, com os seus amigos e família, ou anonimamente online.

## Gestores de senhas

### OnionShare

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** is a fork of Mozilla's discontinued Firefox Send service which allows you to send files to others with a link. Os ficheiros são encriptados no seu dispositivo para não poderem ser lidos pelo servidor e, opcionalmente, também podem ser protegidos por palavra-passe. The maintainer of Send hosts a [public instance](https://send.vis.ee). Pode utilizar outras instâncias públicas ou pode alojar o Send por si.

[:octicons-home-16: Página Inicial](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Instâncias Públicas"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Código fonte" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribuir }

</details>

</div>

O Send pode ser utilizado através da sua interface web ou através do [ffsend](https://github.com/timvisee/ffsend) CLI. Se estiver familiarizado com a linha de comandos e enviar ficheiros frequentemente, recomendamos a utilização do cliente CLI para evitar a encriptação baseada em JavaScript. Pode especificar o sinalizador `--host` para utilizar um servidor específico:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![Logótipo OnionShare](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** é uma ferramenta de código aberto que lhe permite partilhar segura e anonimamente um ficheiro de qualquer tamanho. Funciona iniciando um servidor web acessível como um serviço Tor onion, com um URL indetetável que pode ser partilhado com os destinatários para descarregar ou enviar ficheiros.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

### Critérios

**Por favor note que não somos afiliados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrões](about/criteria.md), nós desenvolvemos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por utilizar um projeto e que faça a sua própria investigação para garantir que é a escolha certa para si.

- Must not store decrypted data on a remote server.
- O software deve ser de código aberto.
- Must either have clients for Linux, macOS, and Windows; or have a web interface.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** is an operating system designed to be run on a [single-board computer (SBC)](https://en.wikipedia.org/wiki/Single-board_computer). The purpose is to make it easy to set up server applications that you might want to self-host.

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribute }

</details>

</div>

## Sincronização de arquivos

### Nextcloud (Client-Server)

<div class="admonition recommendation" markdown>

![logotipo do LibreOffice](/assets/img/productivity/libreoffice.svg){ align=right }

**LibreOffice** é uma suite de escritório gratuita e de código aberto com amplas funcionalidades.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

![OnlyOffice logo](/assets/img/productivity/onlyoffice.svg){ align=right }

**OnlyOffice** é uma alternativa, é uma suite de escritório gratuita e de código aberto com uma extensa funcionalidade.

</div>

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** is an open-source peer-to-peer continuous file synchronization utility. It is used to synchronize files between two or more devices over the local network or the internet. Syncthing does not use a centralized server; it uses the [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) to transfer data between devices. All data is encrypted using TLS.

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
- [:simple-windows11: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

#### Requisitos mínimos

- Must not require a third-party remote/cloud server.
- O software deve ser de código aberto.
- Must either have clients for Linux, macOS, and Windows; or have a web interface.

#### Melhor caso

Os nossos melhores critérios representam o que gostaríamos de ver num projeto perfeito desta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Has mobile clients for iOS and Android, which at least support document previews.
- Supports photo backup from iOS and Android, and optionally supports file/folder sync on Android.
