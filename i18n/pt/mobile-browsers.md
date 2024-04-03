---
meta_title: "Navegadores para Android e iOS que respeitam a privacidade - Privacy Guides"
title: "Navegadores para dispositivos móveis"
icon: material/cellphone-information
description: Estes navegadores são os que recomendamos atualmente para a navegação normal/não anónima na Internet no seu telemóvel.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de navegadores privados para dispositivos móveis
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Bromite
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Origem do uBlock
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Estes são os navegadores para dispositivos móveis e as configurações atualmente recomendados para a navegação normal/não anónima na Internet. Se precisar de navegar anonimamente na Internet, deve utilizar o [Tor](tor.md). Em geral, recomendamos que a utilização de extensões seja reduzida ao mínimo; têm acesso privilegiado no seu browser, exigem que confie no programador, podem fazer com que se destaque [](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)e [enfraquecem o isolamento do site](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Inclui [características de privacidade](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0), tais como Proteção de Rastreamento Inteligente, Relatório de Privacidade, abas isoladas de Navegação Privada, iCloud Private Relay, e atualizações automáticas de HTTPS.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Recommended Brave Configuration

O Tor é a única forma de navegar verdadeiramente de forma anónima na Internet. Quando utilizar o Brave, recomendamos que altere as seguintes definições para proteger a sua privacidade de determinadas entidades terceiras. Contudo, todos os browsers, com a exceção do [Tor](tor.md#tor-browser) serão rastreáveis por *alguém* de uma forma ou de outra.

Estas opções podem ser encontradas em :material-menu: → **Definições** → **Proteção do Brave & privacidade**

##### Proteções

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Predefinições globais das proteções do Brave

As opções de proteção podem ser revogadas por cada site, de acordo com as necessidades, mas por predefinição recomendamos as seguintes definições:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Aconselhamos a não utilizar esta funcionalidade; em vez disso, mantenha as listas de filtros predefinidas. A utilização de listas extra fará com que se destaque dos outros utilizadores do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

</details>

- [x] Selecione **Atualizar as ligações para HTTPS**
- [x] Selecione **Utilizar sempre ligações seguras**
- [x] (Opcional) Selecionar **Bloquear scripts** (1)
- [x] na opção Bloquear impressão digital, selecionar **Estrito, pode causar problemas nos sites**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### Limpar dados de navegação

- [x] Selecionar **Limpar dados ao sair**

##### Bloqueio de redes sociais

- [ ] Desmarcar todos os componentes das redes sociais

##### Outras definições de privacidade

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. O InterPlanetary File System (IPFS) é uma rede descentralizada, peer-to-peer, para armazenar e partilhar dados num sistema de ficheiros distribuído. A menos que utilize a funcionalidade, desative-a.

#### Sincronização do Brave

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

No iOS, qualquer aplicação que possa navegar na Web está [limitada](https://developer.apple.com/app-store/review/guidelines) à utilização de uma estrutura WebKit fornecida pela Apple [](https://developer.apple.com/documentation/webkit), pelo que não há nenhuma vantagem em utilizar um navegador diferente de outro fornecedor.

### Safari

<div class="admonition recommendation" markdown>

![Logótipo Safari](assets/img/browsers/safari.svg){ align=right }

O **Safari** é o navegador predefinido no iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Recommended Firefox Configuration

These options can be found in :gear: **Settings** → **Safari**

##### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### Privacidade & Segurança

- [x] Ativar **Prevenir o rastreio entre sites**

    Isto liga a [Proteção Inteligente de Rastreio da WebKit](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). A funcionalidade ajuda a proteger contra o rastreio indesejado, utilizando a aprendizagem automática no dispositivo para impedir os rastreadores. A ITP contra a monitorização protege-o contra muitas ameaças comuns, mas não bloqueia todos os modos de rastreio, uma vez que foi concebida para ter um impacto mínimo ou nulo na usabilidade do site.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Relatório de Privacidade

O Relatório de Privacidade fornece uma foto de rastreadores entre sites atualmente impedidos de criar perfis no site que está a visitar. Também pode exibir um relatório semanal para mostrar quais rastreadores foram bloqueados ao longo do tempo.

O Relatório de Privacidade é acessível através do menu de Configurações.

##### Medidor de Anúncios Respeitador de Privacidade

- [ ] Desativar **Medidor de Anúncios Respeitador de Privacidade**

A medição de clique em anúncios tem usado tradicionalmente a tecnologia de rastreamento que viola a privacidade do utilizador. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

A funcionalidade tem poucas preocupações de privacidade por si só, então enquanto pode optar por deixá-lo ligado, nós consideramos que ele é automaticamente desativado na navegação privativa como um indicador para desativar o recurso.

##### Navegação Privada sempre-ativa

Abra o Safari e clique no botão Abas, localizado na parte inferior direita. Depois, expanda a lista de Grupos de Abas.

- [x] Selecione **Privado**

O modo de Navegação Privada do Safari oferece adicionais proteções de privacidade. A Navegação Privada usa uma nova sessão [efémera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada aba, o que significa que as abas estão isoladas uma da outra. Também há outras vantagens pequenas em privacidade com a Navegação Privada, como não enviar o endereço de página de web à Apple quando usar a funcionalidade de tradução do Safari.

Tenha em atenção que a Navegação Privada não guarda cookies e dados de sítios Web, pelo que não será possível permanecer ligado a sítios. Isto pode ser uma inconveniência.

##### Sincronização iCloud

A sincronização do histórico do Safari, grupos de separadores, separadores do iCloud e palavras-passe guardadas são E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Aceda ao seu **Nome de ID Apple → iCloud → Proteção de Dados Avançada**.

- [x] Ligue a **Proteção de Dados Avançada**

Se utilizar o iCloud com a Proteção Avançada de Dados desativada, também recomendamos que verifique se a localização de transferência predefinida do Safari está definida para localmente no seu dispositivo. Esta opção pode ser encontrada em :gear: **Definições** → **Safari** → **General** → **Transferências**.

## Framadate

**Por favor, note que não somos afiliados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrões](about/criteria.md), desenvolvemos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por utilizar um projeto e que faça a sua própria investigação para garantir que é a escolha certa para si.

### Requisitos Mínimos

- Deve suportar atualizações automáticas.
- Deve receber atualizações do motor em 0-1 dias a partir do lançamento do upstream.
- Quaisquer alterações necessárias para tornar o browser mais respeitador da privacidade não devem afetar negativamente a experiência do utilizador.
- Os navegadores Android têm de utilizar o motor Chromium.
    - Infelizmente, o Mozilla GeckoView continua menos seguro do que o Chromium no Android.
    - Os navegadores iOS estão limitados ao WebKit.
