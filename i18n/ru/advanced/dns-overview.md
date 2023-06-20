---
title: "Обзор DNS"
icon: material/dns
description: Система доменных имен - это "телефонная книга интернета", помогающая вашему браузеру найти нужный сайт.
---

[Система доменных имен](https://en.wikipedia.org/wiki/Domain_Name_System) - это "телефонная книга Интернета". DNS переводит доменные имена в IP адреса, чтобы браузеры и другие службы могли загружать интернет-ресурсы, через децентрализованную сеть серверов.

## Что такое DNS?

Когда вы посещаете веб-сайт, вам возвращается числовой адрес. Например, при посещении сайта `privacyguides.org`возвращается адрес `192.98.54.105`.

DNS существует с [первых дней](https://en.wikipedia.org/wiki/Domain_Name_System#History) существования Интернета. DNS-запросы, направляемые на DNS-серверы и от них, обычно **не** зашифрованы. Клиент получает серверы от провайдера через [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) по месту жительства.

Незашифрованные DNS запросы могут быть легко **подсмотрены** и **изменены** во время передачи. В некоторых частях мира интернет-провайдеры обязаны осуществлять примитивную [DNS-фильтрацию](https://en.wikipedia.org/wiki/DNS_blocking). Когда вы запрашиваете IP-адрес домена, который заблокирован, сервер может не ответить или ответить другим IP-адресом. Поскольку протокол DNS не зашифрован, провайдер (или любой оператор сети) может использовать [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) для мониторинга запросов. Интернет-провайдеры также могут блокировать запросы на основе общих характеристик, независимо от того, какой DNS-сервер используется. Незашифрованный DNS всегда использует [порт](https://en.wikipedia.org/wiki/Port_(computer_networking)) 53 и UDP.

Ниже мы рассмотрим и предоставим учебное пособие для доказательства того, что может увидеть сторонний наблюдатель, используя обычный незашифрованный DNS и [зашифрованный DNS](#what-is-encrypted-dns).

### Незашифрованный DNS

1. Используя [`tshark`](https://www.wireshark.org/docs/man-pages/tshark.html) (часть проекта [Wireshark](https://en.wikipedia.org/wiki/Wireshark)), мы можем отслеживать и записывать поток интернет-пакетов. Эта команда записывает пакеты, которые соответствуют заданным правилам:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. Затем мы можем использовать [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, MacOS и т.д.) или [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) для поиска DNS на обоих серверах. Такие программы, как веб-браузеры, выполняют эти поиски автоматически, если только они не настроены на использование зашифрованного DNS.

    === "Linux, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. Далее мы хотим [проанализировать](https://www.wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) результаты:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Если вы pfgecnbnt приведенную выше команду Wireshark, на верхней панели отобразится "[frames](https://en.wikipedia.org/wiki/Ethernet_frame)", а на нижней - все данные о выбранном кадре(frame). Корпоративные решения для фильтрации и мониторинга (например, те, которые приобретаются правительствами) могут выполнять этот процесс автоматически, без участия человека, и могут собирать эти frames для получения статистических данных, полезных для сетевого наблюдателя.

| No. (Номер) | Time (Время) | Source (Источник) | Destination (Назначение) | Protocol (Протокол) | Length (Длина) | Info (Инфо)                                                            |
| ----------- | ------------ | ----------------- | ------------------------ | ------------------- | -------------- | ---------------------------------------------------------------------- |
| 1           | 0.000000     | 192.0.2.1         | 1.1.1.1                  | DNS                 | 104            | Standard query 0x58ba A privacyguides.org OPT                          |
| 2           | 0.293395     | 1.1.1.1           | 192.0.2.1                | DNS                 | 108            | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3           | 1.682109     | 192.0.2.1         | 8.8.8.8                  | DNS                 | 104            | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4           | 2.154698     | 8.8.8.8           | 192.0.2.1                | DNS                 | 108            | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Наблюдатель может изменить любой из этих пакетов.

## Что такое "зашифрованный DNS"?

Зашифрованный DNS может относиться к одному из нескольких протоколов, наиболее распространенными из которых являются:

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) был одним из первых методов шифрования DNS-запросов. DNSCrypt работает через порт 443 и работает с транспортными протоколами TCP или UDP. DNSCrypt никогда не был представлен в [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) и не проходил через [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) процесс, поэтому он не использовался широко за пределами нескольких [реализаций](https://dnscrypt.info/implementations). В результате он был в значительной степени заменён более популярным [DNS через HTTPS](#dns-over-https-doh).

### DNS через TLS (DoT)

[**DNS через TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) - это еще один метод шифрования DNS-коммуникаций, который определен в [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Впервые поддержка была реализована в Android 9, iOS 14 и в Linux в [systemd-resolved](https://www.freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) в версии 237. В последние годы предпочтение в этой отрасли отошло от DoT к DoH, поскольку DoT является [комплексным протоколом](https://dnscrypt.info/faq/) и имеет различное соответствие RFC между существующими реализациями. DoT также работает на выделенном порту 853, который может быть легко заблокирован брандмауэрами.

### DNS через HTTPS (DoH)

[**DNS через HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS) как определено в [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484) упаковывает запросы в [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) протокол и обеспечивает безопасность с помощью HTTPS. Впервые поддержка была добавлена в таких браузерах, как Firefox 60 и Chrome 83.

Нативная реализация DoH появилась в iOS 14, macOS 11, Microsoft Windows и Android 13 (однако она не будет включена [по умолчанию](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). Общая поддержка Linux'а ожидает [реализации](https://github.com/systemd/systemd/issues/8639) systemd, поэтому [всё еще требуется установка стороннего программного обеспечения](../dns.md#encrypted-dns-proxies).

## Что может увидеть посторонний человек?

В этом примере мы запишем, что происходит, когда мы делаем запрос DoH:

1. Сначала запустите `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. Во-вторых, сделайте запрос с помощью `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. После выполнения запроса мы можем остановить захват пакетов с помощью <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Проанализируйте результаты в программе Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

Мы видим [установление соединения](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) и [TLS-рукопожатие](https://www.cloudflare.com/ru-ru/learning/ssl/what-happens-in-a-tls-handshake/), которое происходит при любом зашифрованном соединении. При просмотре последующих пакетов "данных приложения" ни один из них не содержит запрашиваемого нами домена или возвращаемого IP-адреса.

## Почему мне **не следует** использовать зашифрованный DNS?

В местах, где существует фильтрация интернета (или цензура), посещение запрещенных ресурсов может иметь свои последствия, которые следует учитывать в [модели угроз](../basics/threat-modeling.md). Мы **не** предлагаем использовать для этих целей зашифрованный DNS. Вместо этого используйте [Tor](https://torproject.org) или [VPN](../vpn.md). Если вы используете VPN, вам следует использовать DNS-серверы вашего VPN. Используя VPN, вы уже доверяете им всю свою сетевую активность.

Когда мы выполняем поиск в DNS, это, как правило, связано с тем, что мы хотим получить доступ к ресурсу. Ниже мы покажем некоторые методы, которые могут раскрыть вашу активность в интернете, даже при использовании зашифрованного DNS:

### IP-адрес

Самым простым способом определения активности в интернете может быть просмотр IP-адресов, к которым обращаются ваши устройства. Например, если наблюдатель знает, что сайт `privacyguides.org` находится по адресу `198.98.54.105`, а ваше устройство запрашивает данные с `198.98.54.105`, то велика вероятность, что вы посещаете Privacy Guides.

Этот метод полезен только в том случае, если IP-адрес принадлежит серверу, на котором размещено всего несколько веб-сайтов. Он также не очень полезен, если сайт размещен на общей платформе (например, Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger и т.д.). Он также не очень полезен, если сервер размещен за [обратным прокси](https://en.wikipedia.org/wiki/Reverse_proxy), что очень часто встречается в современном интернете.

### Индикация имени сервера (SNI)

Индикация имени сервера обычно используется, когда на одном IP-адресе размещается множество веб-сайтов. Это может быть сервис, например Cloudflare, или какая-либо другая защита от [Denial-of-Service атак](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. Снова запустите захват с помощью `tshark`. Мы добавили фильтр с нашим IP-адресом, чтобы не перехватывать много пакетов:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. Затем мы посетим сайт [https://privacyguides.org](https://privacyguides.org).

3. После посещения сайта мы хотим остановить захват пакетов с помощью <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Далее мы хотим проанализировать полученные результаты:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    Мы увидим установление соединения, а затем TLS-рукопожатие для сайта Privacy Guides. Около frame 5. вы увидите "Client Hello".

5. Раскройте треугольник &#9656; рядом с каждым полем:

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. We can see the SNI value which discloses the website we are visiting. The `tshark` command can give you the value directly for all packets containing a SNI value:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

This means even if we are using "Encrypted DNS" servers, the domain will likely be disclosed through SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello/), which prevents this kind of leak.

Governments, in particular [China](https://www.zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni/) and [Russia](https://www.zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni/), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Recently, Russia has [started blocking foreign websites](https://github.com/net4people/bbs/issues/108) that use the [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) standard. This is because the [QUIC](https://en.wikipedia.org/wiki/QUIC) protocol that is a part of HTTP/3 requires that `ClientHello` also be encrypted.

### Online Certificate Status Protocol (OCSP)

Another way your browser can disclose your browsing activities is with the [Online Certificate Status Protocol](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). When visiting an HTTPS website, the browser might check to see if the website's [certificate](https://en.wikipedia.org/wiki/Public_key_certificate) has been revoked. This is generally done through the HTTP protocol, meaning it is **not** encrypted.

The OCSP request contains the certificate "[serial number](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", which is unique. It is sent to the "OCSP responder" in order to check its status.

We can simulate what a browser would do using the [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) command.

1. Get the server certificate and use [`sed`](https://en.wikipedia.org/wiki/Sed) to keep just the important part and write it out to a file:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Get the intermediate certificate. [Certificate Authorities (CA)](https://en.wikipedia.org/wiki/Certificate_authority) normally don't sign a certificate directly; they use what is known as an "intermediate" certificate.

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. The first certificate in `pg_and_intermediate.cert` is actually the server certificate from step 1. We can use `sed` again to delete until the first instance of END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Get the OCSP responder for the server certificate:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Our certificate shows the Lets Encrypt certificate responder. If we want to see all the details of the certificate we can use:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Start the packet capture:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. Make the OCSP request:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Open the capture:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    There will be two packets with the "OCSP" protocol: a "Request" and a "Response". For the "Request" we can see the "serial number" by expanding the triangle &#9656; next to each field:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    For the "Response" we can also see the "serial number":

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ responses: 1 item
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```

8. Or use `tshark` to filter the packets for the Serial Number:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

If the network observer has the public certificate, which is publicly available, they can match the serial number with that certificate and therefore determine the site you're visiting from that. The process can be automated and can associate IP addresses with serial numbers. It is also possible to check [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency) logs for the serial number.

## Следует ли мне использовать зашифрованный DNS?

We made this flow chart to describe when you *should* use encrypted DNS:

``` mermaid
graph TB
    Start[Start] --> anonymous{Trying to be<br> anonymous?}
    anonymous--> | Yes | tor(Use Tor)
    anonymous --> | No | censorship{Avoiding<br> censorship?}
    censorship --> | Yes | vpnOrTor(Use<br> VPN or Tor)
    censorship --> | No | privacy{Want privacy<br> from ISP?}
    privacy --> | Yes | vpnOrTor
    privacy --> | No | obnoxious{ISP makes<br> obnoxious<br> redirects?}
    obnoxious --> | Yes | encryptedDNS(Use<br> encrypted DNS<br> with 3rd party)
    obnoxious --> | No | ispDNS{Does ISP support<br> encrypted DNS?}
    ispDNS --> | Yes | useISP(Use<br> encrypted DNS<br> with ISP)
    ispDNS --> | No | nothing(Do nothing)
```

Encrypted DNS with a third-party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences or you're interested in a provider that does some rudimentary filtering.

[List of recommended DNS servers](../dns.md ""){.md-button}

## Что такое DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) is a feature of DNS that authenticates responses to domain name lookups. It does not provide privacy protections for those lookups, but rather prevents attackers from manipulating or poisoning the responses to DNS requests.

In other words, DNSSEC digitally signs data to help ensure its validity. In order to ensure a secure lookup, the signing occurs at every level in the DNS lookup process. As a result, all answers from DNS can be trusted.

The DNSSEC signing process is similar to someone signing a legal document with a pen; that person signs with a unique signature that no one else can create, and a court expert can look at that signature and verify that the document was signed by that person. These digital signatures ensure that data has not been tampered with.

DNSSEC implements a hierarchical digital signing policy across all layers of DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction/) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).</small>

## What is QNAME minimization?

A QNAME is a "qualified name", for example `privacyguides.org`. QNAME minimisation reduces the amount of information sent from the DNS server to the [authoritative name server](https://en.wikipedia.org/wiki/Name_server#Authoritative_name_server).

Instead of sending the whole domain `privacyguides.org`, QNAME minimization means the DNS server will ask for all the records that end in `.org`. Further technical description is defined in [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## What is EDNS Client Subnet (ECS)?

The [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) is a method for a recursive DNS resolver to specify a [subnetwork](https://en.wikipedia.org/wiki/Subnetwork) for the [host or client](https://en.wikipedia.org/wiki/Client_(computing)) which is making the DNS query.

It's intended to "speed up" delivery of data by giving the client an answer that belongs to a server that is close to them such as a [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), which are often used in video streaming and serving JavaScript web apps.

This feature does come at a privacy cost, as it tells the DNS server some information about the client's location.
