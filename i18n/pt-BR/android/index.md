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

### Evite ROOT

[Rooting](https://pt.wikipedia.org/wiki/Root_no_Android#:~:text=O%20root%20ou%20rooting%20%C3%A9,indispon%C3%ADveis%20em%20sua%20configura%C3%A7%C3%A3o%20padr%C3%A3o.)) telefones Android pode diminuir significativamente a segurança pois enfraquece o [modelo de segurança do Android](https://pt.wikipedia.org/wiki/Android#:~:text=Android%20%C3%A9%20um%20sistema%20operacional,desenvolvedores%20conhecido%20como%20Open%20Handset)#Security_and_privacy). Isto pode diminuir a privacidade se houver um exploit que seja assistenciado pela diminuição da segurança. Métodos comuns de root envolvem diretamente adulteração com a partição de boot, tornando impossível executar uma boot verificada com sucesso. Apps que requerem root também modificarão a partição do sistema, o que significa que o Boot Verificado terá de permanecer desativado. Ter o root exposto diretamente na interface do usuário também aumenta a superfície de ataque do seu dispositivo e pode ajudar na [escalada de privilégios](https://pt.wikipedia.org/wiki/Escalonamento_de_privil%C3%A9gios#:~:text=A%20escala%C3%A7%C3%A3o%20de%20privil%C3%A9gios%20%C3%A9,de%20um%20aplicativo%20ou%20usu%C3%A1rio.) vulnerabilidades e desvios da política do SELinux.

Bloqueadores de conteúdo que modificam os [arquivos hosts](https://pt.wikipedia.org/wiki/Hosts_\(arquivo\)#:~:text=O%20arquivo%20hosts%2C%20%C3%A9%20um,plano%2C%20tradicionalmente%20nomeado%20como%20hosts.)) (AdAway) e firewalls (AFWall+) que exigem acesso à raiz de forma persistente são perigosos e não devem ser usados. Eles também não são a maneira correta de resolver seus objetivos pretendidos. Para bloqueio de conteúdo, sugerimos criptografia [DNS](../dns.md) ou funcionalidade de bloqueio de conteúdo fornecida por uma VPN. TrackerControl e AdAway em modo sem root ocuparão o slot de VPN (usando uma VPN com loopback local), impedindo que você utilize serviços de aprimoramento de privacidade como [Orbot](../tor.md#orbot) ou um [verdadeiro provedor VPN](../vpn.md).

O AFWall+ funciona com base na abordagem [filtro de pacotes](https://en-m-wikipedia-org.translate.goog/?_x_tr_sl=auto&_x_tr_tl=pt&_x_tr_hl=pt-BR&_x_tr_pto=wapp&_x_tr_hist=true#Packet_filter):~:text=de%20uma%20rede-,Filtro%20de%20pacotes,-O%20primeiro%20tipo) e pode ser contornável em algumas situações.

Não acreditamos que os sacrifícios de segurança feitos ao fazer o root em um telefone valham os benefícios questionáveis de privacidade desses aplicativos.

### Instale atualizações regularmente

É importante não usar uma versão [end-of-life](https://endoflife.date/android) do Android. As versões mais recentes do Android recebem não apenas atualizações de segurança para o sistema operacional, mas também importantes atualizações de aprimoramento da privacidade.

Por exemplo, [antes do Android 10](https://developer.android.com/about/versions/10/privacy/changes), qualquer aplicativo com a permissão [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) poderia acessar números de série confidenciais e exclusivos do seu telefone, como [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) ou o [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) do seu cartão SIM; agora, eles precisam ser aplicativos do sistema para fazer isso. Os aplicativos do sistema são fornecidos apenas pelo OEM ou pela distribuição do Android.

### Use os recursos de compartilhamento incorporados

Você pode evitar dar permissão a muitos aplicativos para acessar sua mídia com os recursos de compartilhamento integrados do Android. Muitos aplicativos permitem que você "compartilhe" um arquivo com eles para fazer upload de mídia.

Por exemplo, se você quiser publicar uma foto no Discord, poderá abrir o gerenciador de arquivos ou a galeria e compartilhar essa foto com o aplicativo Discord, em vez de conceder ao Discord acesso total à sua mídia e às suas fotos.
