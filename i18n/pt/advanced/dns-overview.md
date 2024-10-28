---
title: "Visão geral do DNS"
icon: material/dns
description: O sistema de nomes de domínio, DNS, é a "lista telefónica da Internet", e ajuda o seu browser a encontrar o site que procura.
---

O sistema de nomes de domínio [](https://en.wikipedia.org/wiki/Domain_Name_System) é a "lista telefónica da Internet". O DNS traduz os nomes de domínio em endereços IP, para que os navegadores e outros serviços possam carregar os recursos da Internet, através de uma rede descentralizada de servidores.

## O que é o DNS?

Quando se visita um site, é devolvido um endereço numérico. Por exemplo, quando se visita o `privacyguides.org`, é devolvido o endereço `192.98.54.105`.

O DNS existe desde os [primeiros dias](https://en.wikipedia.org/wiki/Domain_Name_System#History) da Internet. Os pedidos de DNS realizado, de e para servidores DNS, **não são** geralmente encriptados. Numa configuração caseira, o utilizador usa os servidores de DNS do ISP, através de [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Os pedidos de DNS não encriptados podem ser facilmente **vigiados** e **modificados** em trânsito. Em algumas partes do mundo, os ISP são obrigados a efetuar uma [filtragem de DNS](https://en.wikipedia.org/wiki/DNS_blocking). Quando solicita o endereço IP de um domínio que está bloqueado, o servidor pode não responder ou pode responder com um endereço IP diferente. Como o protocolo DNS não é encriptado, o ISP (ou qualquer operador de rede) pode utilizar o [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) para monitorizar os pedidos. Os ISPs também podem bloquear pedidos com base em características comuns, independentemente do servidor DNS utilizado.

Abaixo, discutimos e fornecemos um tutorial que prova o que um observador externo pode ver, quando se utiliza DNS normal não encriptado e [DNS encriptado](#what-is-encrypted-dns).

### DNS não encriptado

1. Using [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (part of the [Wireshark](https://en.wikipedia.org/wiki/Wireshark) project) we can monitor and record internet packet flow. Este é um comando que regista os pacotes que cumprem determinadas regras:

    ```bash
    tshark -w /tmp/dns.pcap udp porto 53 e host 1.1.1.1 ou host 8.8.8.8
    ```

2. Podemos depois utilizar o [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, MacOS, etc.) ou o [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) para enviar a pesquisa de DNS para ambos os servidores. Software como, por exemplo, os browsers fazem estas pesquisas automaticamente, a menos que estejam configurados para utilizar DNS encriptado.

    === "Linux, macOS"

        ```
        dig noall answer privacyguides.org @1.1.1.1.1
        dig noall answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. Next, we want to [analyse](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    ==== "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Se executar o comando Wireshark indicado acima, o painel superior mostra os "[frames](https://en.wikipedia.org/wiki/Ethernet_frame)", e o painel inferior mostra todos os dados sobre o frame selecionado. As soluções empresariais de filtragem e monitorização (como as adquiridas pelos governos) podem fazer o processo automaticamente, sem interação humana, e podem agregar essas imagens para produzir dados estatísticos úteis para o observador da rede.

| No. | Time     | Source    | Destination | Protocol | Length | Info                                                                   |
| --- | -------- | --------- | ----------- | -------- | ------ | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1     | DNS      | 104    | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1   | DNS      | 108    | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8     | DNS      | 104    | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1   | DNS      | 108    | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Um observador pode modificar qualquer um destes pacotes.

## O que é o "DNS encriptado"?

Encrypted DNS can refer to one of a number of protocols, the most common ones being [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot), and [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

O [**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) foi um dos primeiros métodos de encriptação de pedidos DNS. O DNSCrypt funciona na porta 443 e utiliza os protocolos de transporte TCP ou UDP. O DNSCrypt nunca foi submetido à [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force), nem passou pelo processo [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments), pelo que não foi amplamente utilizado, exceto em algumas implementações [](https://dnscrypt.info/implementations). Por esse motivo, foi amplamente substituído pelo mais popular [DNS sobre HTTPS](#dns-over-https-doh).

### DNS sobre TLS (DoT)

O [**DNS sobre TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) é outro método para encriptar a comunicação DNS, definido em [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Support was first implemented in Android 9, iOS 14, and on Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in version 237. Preference in the industry has been moving away from DoT to DoH in recent years, as DoT is a [complex protocol](https://dnscrypt.info/faq) and has varying compliance to the RFC across the implementations that exist. O DoT também funciona numa porta dedicada, a 853, que pode ser facilmente bloqueada por firewalls restritivas.

### DNS sobre HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. O suporte foi adicionado pela primeira vez em browsers como o Firefox 60 e o Chrome 83.

A implementação nativa do DoH apareceu no iOS 14, macOS 11, Microsoft Windows e Android 13 (no entanto, não será ativado [por predefinição](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). O suporte geral do ambiente de trabalho Linux está à espera da [implementação](https://github.com/systemd/systemd/issues/8639) do systemd, pelo que [ainda é necessário instalar software de terceiros](../dns.md#encrypted-dns-proxies).

### Native Operating System Support

#### Android

As últimas versões do iOS, iPadOS, tvOS e macOS, suportam tanto DoT como DoH. Ambos os protocolos são suportados nativamente através de [perfis de configuração](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) ou através de [DNS Settings API](https://developer.apple.com/documentation/networkextension/dns_settings).

#### Apple Devices

Após a instalação de um perfil de configuração ou de um aplicativo que utiliza a API de configurações DNS, a configuração DNS pode ser selecionada. Se uma VPN estiver activa, a resolução dentro do túnel VPN utilizará as definições DNS da VPN e não as definições de todo o seu sistema.

A Apple não fornece uma interface nativa para a criação de perfis DNS criptografados. [Criador de perfil DNS seguro](https://dns.notjakob.com/tool.html) é uma ferramenta não oficial para criar os seus próprios perfis DNS encriptados, no entanto eles não serão assinados.

Apple does not provide a native interface for creating encrypted DNS profiles. Informações Signed profiles are preferred; signing validates a profile's origin and helps to ensure the integrity of the profiles. A green "Verified" label is given to signed configuration profiles. For more information on code signing, see [About Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, which many Linux distributions use to do their DNS lookups, doesn't yet [support DoH](https://github.com/systemd/systemd/issues/8639). If you want to use DoH, you'll need to install a proxy like [dnscrypt-proxy](../dns.md#dnscrypt-proxy) and [configure it](https://wiki.archlinux.org/title/Dnscrypt-proxy) to take all the DNS queries from your system resolver and forward them over HTTPS.

## O que é que uma pessoa de fora pode ver?

Neste exemplo, vamos registar o que acontece quando fazemos um pedido ao DoH:

1. Primeiro, inicie o `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https e host 1.1.1.1"
    ```

2. Em segundo lugar, faça um pedido com `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. Depois de fazer o pedido, podemos parar a captura de pacotes com <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Analise os resultados no Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. Ao olhar para os pacotes de "dados da aplicação" que se seguem, verificamos que nenhum deles contém o domínio que pedimos ou o endereço IP devolvido.

## Por que razão **não devo** utilizar DNS encriptado?

Em locais onde existe filtragem (ou censura) da Internet, visitar recursos proibidos pode ter as suas próprias consequências, que devem ser consideradas no [modelo de ameaças](../basics/threat-modeling.md). **Não** sugerimos a utilização de DNS encriptado para este fim. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. Se estiver a utilizar uma VPN, deve utilizar os servidores DNS da sua VPN. Ao utilizar uma VPN, está a confiar-lhes toda a sua atividade de rede.

Quando fazemos uma pesquisa DNS, geralmente é porque queremos aceder a um recurso. Abaixo, falaremos de alguns dos métodos que podem revelar as suas atividades de navegação, mesmo quando utiliza DNS encriptado:

### Endereço IP

A forma mais simples de determinar a sua atividade de navegação é verificar os endereços IP a que os seus dispositivos acedem. Por exemplo, se o observador sabe que `privacyguides.org` está em `198.98.54.105`, e o seu dispositivo está a pedir dados a `198.98.54.105`, há uma boa hipótese de estar a visitar o Privacy Guides.

Este método só é útil quando o endereço IP pertence a um servidor que aloja um número reduzido de sites. Também não é muito útil se o site estiver alojado numa plataforma partilhada (por exemplo, Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). Também não é muito útil se o servidor estiver hospedado atrás de um [proxy reverso](https://en.wikipedia.org/wiki/Reverse_proxy), o que é muito comum na Internet moderna.

### Indicação do nome do servidor (SNI)

A indicação do nome do servidor é normalmente utilizada quando um endereço IP aloja uma grande quantidade de sites. Pode ser um serviço como o Cloudflare ou alguma outra proteção contra [ataques de negação de serviço (DoS)](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. Comece a capturar novamente com o `tshark`. Adicionámos um filtro com o nosso endereço IP para que não capture muitos pacotes:

    ```bash
    tshark -w /tmp/pg.pcap porto 443 e host 198.98.54.105
    ```

2. Em seguida, visitamos [https://privacyguides.org](https://privacyguides.org).

3. Depois de visitar o site, paramos a captura de pacotes com <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Em seguida, analisamos os resultados:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    Veremos o estabelecimento da ligação, seguida do TLS handshake para o site Privacy Guides. Algures na proximidade da frame 5. verá um "Client Hello".

5. Expanda o triângulo &#9656; junto a cada campo:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Protocolo de Aperto de Mãos: Cliente Olá
        ▸ Protocolo de Aperto de Mãos: Cliente Olá
          ▸ Extensão: Server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. Podemos ver o valor SNI que revela o site que estamos a visitar. O comando `tshark` pode fornecer-lhe o valor diretamente para todos os pacotes que contêm um valor SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Isto significa que mesmo que estejamos a utilizar servidores "DNS Encriptados", o domínio será provavelmente divulgado através do SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Recentemente, a Rússia [começou a bloquear sites estrangeiros](https://github.com/net4people/bbs/issues/108) que utilizam a norma [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). Isto deve-se ao facto do protocolo [QUIC](https://en.wikipedia.org/wiki/QUIC), que faz parte do HTTP/3, exigir que o `ClientHello` também seja encriptado.

### Protocolo de estado dos certificados em linha (OCSP)

Outra forma de o seu browser revelar as suas atividades de navegação é através do [protocolo de estado dos certificados online](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). Ao visitar um site HTTPS, o browser pode verificar se o certificado [do site](https://en.wikipedia.org/wiki/Public_key_certificate) foi revogado. Isto é geralmente feito através do protocolo HTTP, o que significa que **não** é encriptado.

O pedido OCSP contém o "[número de série](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)" do certificado, que é único. É enviado para o "OCSP responder" para verificar o seu estado.

Podemos simular o que um browser faz ao usar o comando [`openssl`](https://en.wikipedia.org/wiki/OpenSSL).

1. Obtenha o certificado do servidor e utilize [`sed`](https://en.wikipedia.org/wiki/Sed) para ficar apenas com a parte importante e escrevê-la num ficheiro:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Obtenha o certificado intermédio. As [Autoridades de Certificação (CA)](https://en.wikipedia.org/wiki/Certificate_authority) normalmente não assinam um certificado diretamente; utilizam o que se conhece por certificado "intermédio".

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. O primeiro certificado em `pg_and_intermediate.cert` é, de facto, o certificado do servidor do passo 1. Podemos usar`sed` novamente para eliminar até à primeira instância de END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Obtenha o OCSP responder para o certificado do servidor:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    O nosso certificado mostra o Lets Encrypt certificate responder. Se quisermos ver todos os pormenores do certificado, podemos usar:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Inicie a captura de pacotes:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http
    ```

6. Faça o pedido OCSP:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Abra a captura:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    Haverá dois pacotes com o protocolo "OCSP": um "Pedido" e uma "Resposta". Para o "Pedido", podemos ver o "número de série" expandindo o triângulo &#9656; ao lado de cada campo:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ request
            ▸ reqCert
              serialNumber
    ```

    Para a "Resposta", também podemos ver o "número de série":

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ Respostas Simples
                ▸ certID
                  serialNumber
    ```

8. Ou utilizar o `tshark` para filtrar os pacotes pelo número de série:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

Se o observador da rede tiver o certificado público, que está disponível publicamente, pode fazer corresponder o número de série a esse certificado e, assim, determinar o site que está a visitar. O processo pode ser automatizado e pode associar endereços IP a números de série. Também é possível consultar os logs de [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) para obter o número de série.

## Devo utilizar DNS encriptado?

Criámos este fluxograma para descrever quando é que *deve* utilizar DNS encriptado:

``` mermaid
graph TB
    Iniciar[Start] --> anonimato{Pretende <br> anonimato?}
    anonimato--> | Sim | tor(Use o Tor)
    anonimato --> | Não | censura{Evitar<br> censura?}
    censura --> | Sim | vpnOrTor(Use<br> uma VPN ou o Tor)
    censura --> | Não | privacidade{Quer privacidade em relação<br> ao ISP?}
    privacidade --> | Sim | vpnOrTor
    privacidade --> | Não | obnoxious{O ISP faz<br>redirecionamentos<br> desagradáveis?}
    obnoxious --> | Sim | encryptedDNS(Use<br> DNS encriptado<br> com fornecedor terceiro)
    obnoxious --> | Não | ispDNS{O ISP suporta<br> DNS encriptado?}
    ispDNS --> | Sim | useISP(Use<br> DNS encriptado<br> com ISP)
    ispDNS --> | Não | nothing(Não faça nada)
```

O DNS encriptado com terceiros só deve ser utilizado para contornar redirecionamentos e o bloqueio básico do DNS [](https://en.wikipedia.org/wiki/DNS_blocking) quando tiver a certeza de que não haverá quaisquer consequências ou quando estiver interessado num fornecedor que efetue uma filtragem rudimentar.

[Lista de servidores DNS recomendados](../dns.md ""){.md-button}

## O que é o DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) é uma funcionalidade do DNS que autentica as respostas às pesquisas de nomes de domínio. Não fornece proteções de privacidade para essas pesquisas, mas impede que os atacantes manipulem ou envenenem as respostas aos pedidos de DNS.

Por outras palavras, o DNSSEC assina digitalmente os dados para ajudar a garantir a sua validade. Para garantir uma pesquisa segura, a assinatura ocorre em todos os níveis do processo de pesquisa do DNS. Como resultado, todas as respostas do DNS são fiáveis.

O processo de assinatura DNSSEC é semelhante ao de alguém que assina um documento legal com uma caneta; essa pessoa assina com uma assinatura única que mais ninguém pode criar, e um perito judicial pode olhar para essa assinatura e verificar que o documento foi assinado por essa pessoa. Estas assinaturas digitais garantem que os dados não foram adulterados.

O DNSSEC implementa uma política de assinatura digital hierárquica em todos os níveis do DNS. Por exemplo, no caso de uma pesquisa em `privacyguides.org`, um servidor DNS de raiz assinaria uma chave para o DNS de `.org`, e o DNS de `.org` assinaria então uma chave para o DNS autoritário `privacyguides.org`.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## O que é a minimização de QNAME?

A QNAME is a "qualified name", for example `discuss.privacyguides.net`. In the past, when resolving a domain name your DNS resolver would ask every server in the chain to provide any information it has about your full query. In this example below, your request to find the IP address for `discuss.privacyguides.net` gets asked of every DNS server provider:

| Server                 | Question Asked                              | Response                                    |
| ---------------------- | ------------------------------------------- | ------------------------------------------- |
| Root server            | What's the IP of discuss.privacyguides.net? | I don't know, ask .net's server...          |
| .net's server          | What's the IP of discuss.privacyguides.net? | I don't know, ask Privacy Guides' server... |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net? | 5.161.195.190!                              |

With "QNAME minimization," your DNS resolver now only asks for just enough information to find the next server in the chain. In this example, the root server is only asked for enough information to find the appropriate nameserver for the .net TLD, and so on, without ever knowing the full domain you're trying to visit:

| Server                 | Question Asked                                       | Response                          |
| ---------------------- | ---------------------------------------------------- | --------------------------------- |
| Root server            | What's the nameserver for .net?                      | *Provides .net's server*          |
| .net's server          | What's the nameserver for privacyguides.net?         | *Provides Privacy Guides' server* |
| Privacy Guides' server | What's the nameserver for discuss.privacyguides.net? | This server!                      |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net?          | 5.161.195.190                     |

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. Uma descrição técnica mais pormenorizada é definida em [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## O que é a Sub-rede de Cliente EDNS (ECS)?

A sub-rede de cliente [EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) é um método para um resolver DNS recursivo especificar uma [sub-rede](https://en.wikipedia.org/wiki/Subnetwork) para o [anfitrião ou cliente](https://en.wikipedia.org/wiki/Client_(computing)) que está a efetuar a consulta DNS.

Destina-se a "acelerar" a entrega de dados, dando ao cliente uma resposta que pertence a um servidor que está perto dele, como uma rede de entrega de conteúdos [](https://en.wikipedia.org/wiki/Content_delivery_network), que são frequentemente utilizados em streaming de vídeo e no fornecimento de aplicações Web JavaScript.

This feature does come at a privacy cost, as it tells the DNS server some information about the client's location, generally your IP network. For example, if your IP address is `198.51.100.32` the DNS provider might share `198.51.100.0/24` with the authoritative server. Some DNS providers anonymize this data by providing another IP address which is approximately near your location.

If you have `dig` installed you can test whether your DNS provider gives EDNS information out to DNS nameservers with the following command:

```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

Note that this command will contact Google for the test, and return your IP as well as EDNS client subnet information. If you want to test another DNS resolver you can specify their IP, to test `9.9.9.11` for example:

```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```

If the results include a second edns0-client-subnet TXT record (like shown below), then your DNS server is passing along EDNS information. The IP or network shown after is the precise information which was shared with Google by your DNS provider.

```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
