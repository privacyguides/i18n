---
title: "Visão geral do DNS"
icon: material/dns
description: O sistema de nomes de domínio, DNS, é a "lista telefónica da Internet", e ajuda o seu browser a encontrar o site que procura.
---

O sistema de nomes de domínio [](https://en.wikipedia.org/wiki/Domain_Name_System) é a "lista telefónica da Internet". O DNS traduz os nomes de domínio em endereços IP, para que os navegadores e outros serviços possam carregar os recursos da Internet, através de uma rede descentralizada de servidores.

## O que é o DNS?

Quando se visita um site, é devolvido um endereço numérico. Por exemplo, quando se visita o `privacyguides.org`, é devolvido o endereço `192.98.54.105`.

O DNS existe desde os [primeiros dias](https://en.wikipedia.org/wiki/Domain_Name_System#History) da Internet. Os pedidos de DNS realizado, de e para servidores DNS, **não são** geralmente encriptados. Numa configuração caseira, o utilizador usa os servidores de DNS do ISP, através de [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Os pedidos de DNS não encriptados podem ser facilmente **vigiados** e **modificados** em trânsito. Em algumas partes do mundo, os ISP são obrigados a efetuar uma [filtragem de DNS](https://en.wikipedia.org/wiki/DNS_blocking). Quando solicita o endereço IP de um domínio que está bloqueado, o servidor pode não responder ou pode responder com um endereço IP diferente. Como o protocolo DNS não é encriptado, o ISP (ou qualquer operador de rede) pode utilizar o [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) para monitorizar os pedidos. Os ISPs também podem bloquear pedidos com base em características comuns, independentemente do servidor DNS utilizado. O DNS não encriptado utiliza sempre a porta [](https://en.wikipedia.org/wiki/Port_(computer_networking)) 53 e o protocolo UDP.

Abaixo, discutimos e fornecemos um tutorial que prova o que um observador externo pode ver, quando se utiliza DNS normal não encriptado e [DNS encriptado](#what-is-encrypted-dns).

### DNS não encriptado

1. Utilizando o [`tshark`](https://www.wireshark.org/docs/man-pages/tshark.html) (que faz parte do projeto [Wireshark](https://en.wikipedia.org/wiki/Wireshark)), podemos monitorizar e gravar o fluxo de pacotes da Internet. Este é um comando que regista os pacotes que cumprem determinadas regras:

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

3. Em seguida, vamos [analisar](https://www.wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) os resultados:

    ==== "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Se executar o comando Wireshark indicado acima, o painel superior mostra os "[frames](https://en.wikipedia.org/wiki/Ethernet_frame)", e o painel inferior mostra todos os dados sobre o frame selecionado. As soluções empresariais de filtragem e monitorização (como as adquiridas pelos governos) podem fazer o processo automaticamente, sem interação humana, e podem agregar essas imagens para produzir dados estatísticos úteis para o observador da rede.

| Não. | Hora     | Origem    | Destino   | Protocolo | Comprimento | Informações                                                                |
| ---- | -------- | --------- | --------- | --------- | ----------- | -------------------------------------------------------------------------- |
| 1    | 0.000000 | 192.0.2.1 | 1.1.1.1   | DNS       | 104         | Consulta padrão 0x58ba A privacyguides.org OPT                             |
| 2    | 0.293395 | 1.1.1.1   | 192.0.2.1 | DNS       | 108         | Resposta de consulta padrão 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3    | 1.682109 | 192.0.2.1 | 8.8.8.8   | DNS       | 104         | Consulta padrão 0xf1a9 A privacyguides.org OPT                             |
| 4    | 2.154698 | 8.8.8.8   | 192.0.2.1 | DNS       | 108         | Resposta de consulta padrão 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Um observador pode modificar qualquer um destes pacotes.

## O que é o "DNS encriptado"?

O DNS encriptado pode referir-se a um de vários protocolos, sendo os mais comuns:

### DNSCrypt

O [**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) foi um dos primeiros métodos de encriptação de pedidos DNS. O DNSCrypt funciona na porta 443 e utiliza os protocolos de transporte TCP ou UDP. O DNSCrypt nunca foi submetido à [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force), nem passou pelo processo [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments), pelo que não foi amplamente utilizado, exceto em algumas implementações [](https://dnscrypt.info/implementations). Por esse motivo, foi amplamente substituído pelo mais popular [DNS sobre HTTPS](#dns-over-https-doh).

### DNS sobre TLS (DoT)

O [**DNS sobre TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) é outro método para encriptar a comunicação DNS, definido em [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). O suporte foi implementado pela primeira vez no Android 9, iOS 14 e no Linux, no [systemd-resolved](https://www.freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=), na versão 237. Nos últimos anos, o setor tem vindo a afastar-se do DoT em favor do DoH, uma vez que o DoT é um [protocolo complexo](https://dnscrypt.info/faq/) e tem uma conformidade variável com o RFC nas implementações existentes. O DoT também funciona numa porta dedicada, a 853, que pode ser facilmente bloqueada por firewalls restritivas.

### DNS sobre HTTPS (DoH)

O [**DNS sobre HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), tal como definido em [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), agrupa as consultas através do protocolo [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) e proporciona segurança com HTTPS. O suporte foi adicionado pela primeira vez em browsers como o Firefox 60 e o Chrome 83.

Native implementation of DoH showed up in iOS 14, macOS 11, Microsoft Windows, and Android 13 (however, it won't be enabled [by default](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). General Linux desktop support is waiting on the systemd [implementation](https://github.com/systemd/systemd/issues/8639) so [installing third-party software is still required](../dns.md#encrypted-dns-proxies).

## O que é que uma festa exterior pode ver?

Neste exemplo vamos registar o que acontece quando fazemos um pedido DoH:

1. Primeiro, iniciar `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https e host 1.1.1.1"
    ```

2. Segundo, faça um pedido com `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. Após fazer o pedido, podemos parar a captura de pacotes com <kbd>CTRL</kbd> <kbd>C</kbd>.

4. Analisar os resultados em Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

Podemos ver o estabelecimento de conexão [e](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) e [aperto de mão TLS](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/) que ocorre com qualquer conexão criptografada. Ao olhar para os pacotes de "dados de aplicação" que se seguem, nenhum deles contém o domínio que solicitamos ou o endereço IP devolvido.

## Porque **não deveria** Eu uso DNS encriptado?

In locations where there is internet filtering (or censorship), visiting forbidden resources may have its own consequences which you should consider in your [threat model](../basics/threat-modeling.md). Fazemos **não** sugerimos o uso de DNS criptografado para este fim. Use [Tor](https://torproject.org) or a [VPN](../vpn.md) instead. Se você estiver usando uma VPN, você deve usar os servidores DNS da sua VPN. Ao utilizar uma VPN, já está a confiar-lhes toda a sua actividade na rede.

Quando fazemos uma pesquisa DNS, geralmente é porque queremos aceder a um recurso. Abaixo, discutiremos alguns dos métodos que podem revelar as suas actividades de navegação mesmo quando utiliza DNS encriptado:

### Endereço IP

A maneira mais simples de determinar a atividade de navegação pode ser olhar para os endereços IP que seus dispositivos estão acessando. Por exemplo, se o observador sabe que `privacyguides.org` está em `198.98.54.105`, e o seu dispositivo está solicitando dados de `198.98.54.105`, há uma boa chance de você estar visitando os Guias de Privacidade.

Este método só é útil quando o endereço IP pertence a um servidor que só hospeda poucos sites. It's also not very useful if the site is hosted on a shared platform (e.g. Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). Também não é muito útil se o servidor estiver hospedado atrás de um [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy), o que é muito comum na Internet moderna.

### Indicação do nome do servidor (SNI)

A indicação do nome do servidor é normalmente usada quando um endereço IP hospeda muitos sites. Este pode ser um serviço como o Cloudflare, ou algum outro [ataque de negação de serviço](https://en.wikipedia.org/wiki/Denial-of-service_attack) protecção.

1. Comece a capturar novamente com `tshark`. Adicionamos um filtro com nosso endereço IP para que você não capture muitos pacotes:

    ```bash
    tshark -w /tmp/pg.pcap porto 443 e host 198.98.54.105
    ```

2. Depois visitamos [https://privacyguides.org](https://privacyguides.org).

3. Depois de visitar o site, nós o que parar a captura de pacotes com <kbd>CTRL</kbd> <kbd>C</kbd>.

4. A seguir queremos analisar os resultados:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    Veremos o [estabelecimento de conexão](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment), seguido pelo [aperto de mão TLS](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/) para o site Guias de Privacidade. Em redor da moldura 5. verás um "Olá Cliente".

5. Expandir o triângulo &#9656; ao lado de cada campo:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Protocolo de Aperto de Mãos: Cliente Olá
        ▸ Protocolo de Aperto de Mãos: Cliente Olá
          ▸ Extensão: Server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. Podemos ver o [Server Name Indication (SNI)](https://en.wikipedia.org/wiki/Server_Name_Indication) valor que revela o site que estamos visitando. O comando `tshark` pode dar-lhe o valor directamente para todos os pacotes que contenham um valor SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Isto significa que mesmo que estejamos usando servidores DNS "Encriptados", o domínio provavelmente será divulgado através do SNI. O protocolo [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) traz consigo [Cliente Encriptado Olá](https://blog.cloudflare.com/encrypted-client-hello/), o que evita este tipo de fuga.

Governos, em particular [China](https://www.zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni/) e [Rússia](https://www.zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni/), ou já [começaram a bloquear](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) ou manifestaram o desejo de o fazer. Recently, Russia has [started blocking foreign websites](https://github.com/net4people/bbs/issues/108) that use the [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) standard. Isto porque o [QUIC](https://en.wikipedia.org/wiki/QUIC) protocolo que faz parte do HTTP/3 requer que `ClientHello` também seja criptografado.

### Protocolo de Status de Certificado Online (OCSP)

Outra forma do seu navegador poder divulgar suas atividades de navegação é com o [Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). When visiting an HTTPS website, the browser might check to see if the website's [certificate](https://en.wikipedia.org/wiki/Public_key_certificate) has been revoked. Isto geralmente é feito através do protocolo [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) , significando que é **não** encriptado.

O pedido OCSP contém o certificado "[número de série](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", que é único. Ele é enviado ao "OCSP respondedor" para verificar o seu estado.

Podemos simular o que um navegador faria usando o comando [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) .

1. Obtenha o certificado do servidor e use [`sed`](https://en.wikipedia.org/wiki/Sed) para manter apenas a parte importante e escrevê-la em um arquivo:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Obter o certificado intermediário. [Autoridades Certificadoras (AC)](https://en.wikipedia.org/wiki/Certificate_authority) normalmente não assinam um certificado diretamente; eles usam o que é conhecido como certificado "intermediário".

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. O primeiro certificado em `pg_and_intermediate.cert` é na verdade o certificado do servidor do passo 1. Podemos usar `sed` novamente para apagar até a primeira instância de TERMINAR:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Obtenha o OCSP respondedor para o certificado do servidor:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    O nosso certificado mostra o Lets Encrypt Responder ao certificado. Se quisermos ver todos os detalhes do certificado, podemos usar:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Comece a captura do pacote:

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

    There will be two packets with the "OCSP" protocol: a "Request" and a "Response". Para o "Request" podemos ver o "serial number", expandindo o triângulo &#9656; ao lado de cada campo:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ request
            ▸ reqCert
              serialNumber
    ```

    Para a "Resposta" também podemos ver o "número de série":

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

8. Ou use `tshark` para filtrar os pacotes para o Número de Série:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

Se o observador da rede tiver o certificado público, que está disponível publicamente, ele pode fazer corresponder o número de série com esse certificado e, portanto, determinar o site que você está visitando a partir daí. O processo pode ser automatizado e pode associar endereços IP com números de série. Também é possível verificar [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) logs para o número de série.

## Devo utilizar DNS encriptado?

Nós fizemos este fluxograma para descrever quando você *deve* usar DNS criptografado:

``` mermaid
graph TB
    Start[Start] --> anonymous{Trying to be<br> anonymous?}
    anonymous--> | Yes | tor(Use Tor)
    anonymous --> | No | censorship{Avoiding<br> censorship?}
    censorship --> | Yes | vpnOrTor(Use<br> VPN ou Tor)
    censorship --> | No | privacy{Want privacy<br> from ISP?}
    privacidade --> | Yes | vpnOrTor
    privacidade --> | No | obnoxious{ISP makes<br> obnoxious<br> redirecciona?}
    obnóxio --> | Yes | encryptedDNS(Use<br> encrypted DNS<br> with 3rd party)
    obnóxio --> | No | ispDNS{Does ISP support<br> encrypted DNS?}
    ispDNS --> | Yes | useISP(Use<br> DNS encriptado<br> com ISP)
    ispDNS --> | No | nothing(Do nothing)
```

Encrypted DNS with a third-party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences or you're interested in a provider that does some rudimentary filtering.

[Lista de servidores DNS recomendados](../dns.md ""){.md-button}

## What is DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) is a feature of DNS that authenticates responses to domain name lookups. It does not provide privacy protections for those lookups, but rather prevents attackers from manipulating or poisoning the responses to DNS requests.

In other words, DNSSEC digitally signs data to help ensure its validity. In order to ensure a secure lookup, the signing occurs at every level in the DNS lookup process. As a result, all answers from DNS can be trusted.

The DNSSEC signing process is similar to someone signing a legal document with a pen; that person signs with a unique signature that no one else can create, and a court expert can look at that signature and verify that the document was signed by that person. These digital signatures ensure that data has not been tampered with.

DNSSEC implements a hierarchical digital signing policy across all layers of DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction/) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).</small>

## O que é a minimização do QNAME?

Um QNAME é um "nome qualificado", por exemplo `privacyguides.org`. A minimização do QNAME reduz a quantidade de informação enviada do servidor DNS para o [servidor de nomes autorizado](https://en.wikipedia.org/wiki/Name_server#Authoritative_name_server).

Em vez de enviar o domínio inteiro `privacyguides.org`, a minimização do QNAME significa que o servidor DNS irá pedir todos os registos que terminem em `.org`. Descrição técnica adicional é definida em [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## O que é a Sub-Rede do Cliente EDNS (ECS)?

O [subrede do cliente EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) é um método para um resolvedor DNS recursivo para especificar um [sub-rede](https://en.wikipedia.org/wiki/Subnetwork) para o [host ou cliente](https://en.wikipedia.org/wiki/Client_(computing)) que está fazendo a consulta DNS.

O objectivo é "acelerar" a entrega de dados, dando ao cliente uma resposta que pertence a um servidor que lhes está próximo, tal como um [content delivery network (CDN)](https://en.wikipedia.org/wiki/Content_delivery_network), que são frequentemente utilizados em streaming de vídeo e em aplicações web JavaScript.

Este recurso tem um custo de privacidade, pois informa ao servidor DNS algumas informações sobre a localização do cliente.
