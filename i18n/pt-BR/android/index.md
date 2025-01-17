---
title: Android
description: Nosso conselho para substituir os recursos padrão do Android que invadem a privacidade por alternativas privadas e seguras.
icon: simples/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recomendações para Android
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://pt.wikipedia.org/wiki/Android#:~:text=Android%20%C3%A9%20um%20sistema%20operacional,desenvolvedores%20conhecido%20como%20Open%20Handset
---

![Shelter logo](../assets/img/android/android.svg){ align=right }

O **Android Open Source Project** (AOSP) é um sistema operacional móvel de código aberto liderado pelo Google que alimenta a maioria dos dispositivos móveis do mundo. A maioria dos celulares vendidos com Android são modificados para incluir integrações invasivas e aplicativos como o Google Play Services. Você pode melhorar a privacidade de seu dispositivo significativamente ao usar uma versão do Android sem esses recursos invasivos.

[Visão geral do Android :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Nosso conselho

### Substituir Google Services

Há muitos métodos para obter aplicativos no Android, evitando o Google Play. Sempre que possível, tente usar um desses métodos antes de obter seus aplicativos de fontes não privadas:

[Obtenção de aplicativos :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

Há também muitas alternativas privadas para os aplicativos que vêm pré-instalados no seu telefone, como o aplicativo da câmera. Além dos aplicativos para Android que recomendamos neste site em geral, criamos uma lista de utilitários de sistema específicos para Android que podem ser úteis.

[Recomendações Gerais do Aplicativo :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Instalar uma Distribuição Personalizada

Quando você compra um telefone Android, o sistema operacional padrão vem empacotado com aplicativos e funcionalidades que não fazem parte do Projeto de Código Aberto Android. Muitos destes aplicativos - até mesmo aplicativos como o discador que fornecem a funcionalidade básica do sistema - exigem integrações invasivas com os Serviços do Google Play, que, por sua vez, pede privilégios para acessar seus arquivos, armazenamento de contatos, registros de chamadas, mensagens SMS, localização, câmera, microfone, e várias outras coisas no seu dispositivo para que esses aplicativos básicos de sistema e muitos outros apps funcionem em primeiro lugar. Frameworks como o Google Play Services aumentam a superfície de ataque do seu dispositivo e são a fonte de várias preocupações de privacidade com o Android.

Este problema poderia ser resolvido usando uma distribuição alternativa para Android, comumente conhecida como _custom ROM_, que não vem com tal integração invasiva. Infelizmente, muitas distribuições personalizadas do Android muitas vezes violam o modelo de segurança do Android não suportando recursos de segurança críticos como AVB, proteção reversa, atualizações de firmware e assim por diante. Algumas distribuições também fornecem compilações [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) que expõem a raiz via [ADB](https://developer.android.com/studio/command-line/adb) e exigem políticas SELinux [mais permissivas](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug\&type=code) para acomodar os recursos de depuração, resultando em uma superfície de ataque ainda maior e em um modelo de segurança enfraquecido.

O ideal é que, ao escolher uma distribuição personalizada do Android, você se certifique de que ela mantenha o modelo de segurança do Android. No mínimo, a distribuição deve ter construções de produção, apoio à proteção rollback de AVB, atualizações oportunas do firmware e do sistema operacional e do SELinux no [modo de implementação](https://source.android.com/security/selinux/concepts#enforcement_levels). Todas as nossas distribuições recomendadas do Android satisfazem esses critérios:

[Distribuições recomendadas :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). This can decrease privacy should there be an exploit that is assisted by the decreased security. Common rooting methods involve directly tampering with the boot partition, making it impossible to perform successful Verified Boot. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. They are also not the correct way to solve their intended purposes. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

We do not believe that the security sacrifices made by rooting a phone are worth the questionable privacy benefits of those apps.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Use Built-in Sharing Features

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.
