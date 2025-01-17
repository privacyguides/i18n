---
meta_title: Os melhores sistemas operacionais Android - Privacy Guides
title: Distribuições alternativas
description: Você pode substituir o sistema operacional do seu telefone Android por essas alternativas seguras e que respeitam a privacidade.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Sistemas Operacionais Privados para Android
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en-m-wikipedia-org.translate.goog/wiki/GrapheneOS?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=en&_x_tr_pto=wapp
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra a(s) seguinte(s) ameaça(s):</small>

- [:material-target-account: Ataques Localizados](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques Passivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Um **sistema operacional personalizado baseado no Android** (às vezes chamado de \*_custom ROM_) pode ser uma maneira de obter um nível mais alto de privacidade e segurança no seu dispositivo. Isso contrasta com a versão "padrão" do Android, que vem de fábrica com o telefone e geralmente é profundamente integrada ao Google Play Services e a softwares de outros fornecedores.

Recomendamos que você instale o GrapheneOS se tiver um Google Pixel, pois ele oferece reforço de segurança aprimorado e recursos adicionais de privacidade. Os motivos pelos quais não listamos outros sistemas operacionais ou dispositivos são os seguintes:

- Muitas vezes, eles têm [segurança fraca](index.md#install-a-custom-distribution).
- O suporte é frequentemente descartado quando o mantenedor perde interesse ou atualiza seu dispositivo, que contrasta com o previsível [ciclo de suporte](https://grapheneos.org/faq#device-lifetime) que o GrapheneOS segue.
- Geralmente, eles têm poucas ou nenhumas melhorias notáveis em termos de privacidade ou segurança que as tornam válidas.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** é a melhor escolha quando se trata de privacidade e segurança.

O GrapheneOS oferece melhorias adicionais de [reforço de segurança](https://en.wikipedia.org/wiki/Hardening_\(computing\)) e privacidade. Tem um [alocador de memória endurecido](https://github.com/GrapheneOS/hardened_malloc), rede e permissões de sensor e vários outros [recursos de segurança](https://grapheneos.org/features). O GrapheneOS também vem com atualizações completas de firmware e compilações assinadas, então a inicialização verificada é totalmente suportada.

[:octicons-home-16: Página Inicial](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de Privacidade" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentação}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código Fonte" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

</div>

GrapheneOS suporta [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), que executa o Google Play Services com sandbox total como qualquer outro aplicativo regular. Isso significa que você pode aproveitar a maioria dos serviços do Google Play, como as notificações por push, ao mesmo tempo em que lhe dá controle total sobre as permissões e o acesso a eles e os restringe a um [perfil de trabalho](../os/android-overview.md#work-profile) ou [perfil de usuário](../os/android-overview.md#user-profiles) específico de sua escolha.

Os [telefones Google Pixel](../mobile-phones.md#google-pixel) são os únicos dispositivos que atualmente atendem aos [requisitos de segurança de hardware] do GrapheneOS(https://grapheneos.org/faq#future-devices).

Por padrão, o Android faz muitas conexões de rede com o Google para realizar verificações de conectividade DNS, para sincronizar com a hora atual da rede, para verificar sua conectividade de rede e para muitas outras tarefas em segundo plano. A GrapheneOS os substitui por conexões com servidores operados pela GrapheneOS e sujeitos à sua política de privacidade. Isso oculta informações como seu endereço IP [do Google](../basics/common-threats.md#privacy-from-service-providers), mas significa que é trivial para um administrador da sua rede ou ISP ver que você está fazendo conexões com `grapheneos.network`, `grapheneos.org`, etc. e deduzir qual sistema operacional você está usando.

Se quiser ocultar informações como essa de um adversário em sua rede ou ISP, você **deve** usar uma [VPN confiável](../vpn.md) além de alterar a configuração de verificação de conectividade para **Standard (Google)**. Pode ser encontrado em :gear: **Configurações** → **Rede e internet** → **Verificações de conectividade de Internet**. Esta opção permite que você se conecte aos servidores do Google para verificar a conectividade, que, juntamente com o uso de uma VPN, ajuda a misturar com um conjunto maior de dispositivos Android.

## Critério

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.** Além de [nosso critério padrão](../about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de e-mail e faça sua própria pesquisa para garantir que o provedor de e-mail escolhido seja a opção certa para você.

- Deve ser um software de código aberto.
- Deve suportar o bloqueio de bootloader com suporte personalizado à chave AVB.
- Precisa receber as principais atualizações do Android dentro de 0-1 meses após o lançamento.
- Deve receber atualizações de recursos do Android (versão menor) dentro de 0-14 dias após o lançamento.
- Precisa receber correções de segurança regulares dentro de 0-5 dias após o lançamento.
- **Não** deve estar "rooted" fora da caixa.
- É necessário que o Google Play Services **não** esteja habilitado por padrão.
- Não deve **exigir** modificações no sistema para oferecer suporte ao Google Play Services.
