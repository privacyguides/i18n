---
title: "Обзор DNS"
icon: material/dns
description: Система доменных имен - это "телефонная книга интернета", помогающая вашему браузеру найти нужный сайт.
---

The [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) is the 'phone book of the Internet'. DNS переводит доменные имена в IP адреса, чтобы браузеры и другие службы могли загружать интернет-ресурсы, через децентрализованную сеть серверов.

## Что такое DNS?

Когда вы посещаете веб-сайт, вам возвращается числовой адрес. Например, при посещении сайта `privacyguides.org`возвращается адрес `192.98.54.105`.

DNS существует с [первых дней](https://en.wikipedia.org/wiki/Domain_Name_System#History) существования Интернета. DNS-запросы, направляемые на DNS-серверы и от них, обычно **не** зашифрованы. Клиент получает серверы от провайдера через [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) по месту жительства.

Незашифрованные DNS запросы могут быть легко **подсмотрены** и **изменены** во время передачи. В некоторых частях мира интернет-провайдеры обязаны осуществлять примитивную [DNS-фильтрацию](https://en.wikipedia.org/wiki/DNS_blocking). Когда вы запрашиваете IP-адрес домена, который заблокирован, сервер может не ответить или ответить другим IP-адресом. Поскольку протокол DNS не зашифрован, провайдер (или любой оператор сети) может использовать [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) для мониторинга запросов. Интернет-провайдеры также могут блокировать запросы на основе общих характеристик, независимо от того, какой DNS-сервер используется.

Ниже мы рассмотрим и предоставим учебное пособие для доказательства того, что может увидеть сторонний наблюдатель, используя обычный незашифрованный DNS и [зашифрованный DNS](#what-is-encrypted-dns).

### Незашифрованный DNS

1. Using [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (part of the [Wireshark](https://en.wikipedia.org/wiki/Wireshark) project) we can monitor and record internet packet flow. Эта команда записывает пакеты, которые соответствуют заданным правилам:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. We can then use [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS, etc.) or [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) to send the DNS lookup to both servers. Такие программы, как веб-браузеры, выполняют эти поиски автоматически, если только они не настроены на использование зашифрованного DNS.

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

3. Next, we want to [analyze](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

Если вы pfgecnbnt приведенную выше команду Wireshark, на верхней панели отобразится "[frames](https://en.wikipedia.org/wiki/Ethernet_frame)", а на нижней - все данные о выбранном кадре(frame). Корпоративные решения для фильтрации и мониторинга (например, те, которые приобретаются правительствами) могут выполнять этот процесс автоматически, без участия человека, и могут собирать эти frames для получения статистических данных, полезных для сетевого наблюдателя.

| № | Время    | Источник  | Назначение | Протокол | Длина | Инфо.                                                                  |
| - | -------- | --------- | ---------- | -------- | ----- | ---------------------------------------------------------------------- |
| 1 | 0.000000 | 192.0.2.1 | 1.1.1.1    | DNS      | 104   | Standard query 0x58ba A privacyguides.org OPT                          |
| 2 | 0.293395 | 1.1.1.1   | 192.0.2.1  | DNS      | 108   | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3 | 1.682109 | 192.0.2.1 | 8.8.8.8    | DNS      | 104   | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4 | 2.154698 | 8.8.8.8   | 192.0.2.1  | DNS      | 108   | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Наблюдатель может изменить любой из этих пакетов.

## Что такое "зашифрованный DNS"?

Encrypted DNS can refer to one of a number of protocols, the most common ones being [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot), and [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) был одним из первых методов шифрования DNS-запросов. DNSCrypt работает через порт 443 и работает с транспортными протоколами TCP или UDP. DNSCrypt has never been submitted to the [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) nor has it gone through the [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) process, so it has not been used widely outside a few [implementations](https://dnscrypt.info/implementations). В результате он был в значительной степени заменён более популярным [DNS через HTTPS](#dns-over-https-doh).

### DNS через TLS (DoT)

[**DNS через TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) - это еще один метод шифрования DNS-коммуникаций, который определен в [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Support was first implemented in Android 9, iOS 14, and on Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in version 237. Preference in the industry has been moving away from DoT to DoH in recent years, as DoT is a [complex protocol](https://dnscrypt.info/faq) and has varying compliance to the RFC across the implementations that exist. DoT также работает на выделенном порту 853, который может быть легко заблокирован брандмауэрами.

### DNS через HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. Впервые поддержка была добавлена в таких браузерах, как Firefox 60 и Chrome 83.

Нативная реализация DoH появилась в iOS 14, macOS 11, Microsoft Windows и Android 13 (однако она не будет включена [по умолчанию](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). Общая поддержка Linux'а ожидает [реализации](https://github.com/systemd/systemd/issues/8639) systemd, поэтому [всё еще требуется установка стороннего программного обеспечения](../dns.md#encrypted-dns-proxies).

### Нативная поддержка в операционных системах

#### Android

Android 9 и новее поддерживает DNS over TLS. Его можно включить в **Настройках** &rarr; **Сеть и интернет** &rarr; **Частный DNS-сервер**.

#### Устройства Apple

Последние версии iOS, iPadOS, tvOS и macOS поддерживают протоколы DoT и DoH. Оба протокола можно настроить при помощи [профилей конфигурации](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) или [API настроек DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

После установки профиля конфигурации или приложения, использующего API настроек DNS, можно выбрать конфигурацию DNS. Если включен VPN, будут использоваться настройки DNS вашего VPN-сервиса, а не системные настройки.

Apple не предоставляет нативного интерфейса для создания профилей зашифрованного DNS. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) — это неофициальный инструмент создания собственных профилей зашифрованного DNS, однако они не будут подписаны. Предпочтительнее использовать подписанные профили, так как подпись подтверждает надёжность источника профиля и помогает обеспечить его целостность. Зеленая метка «Проверено» присваивается подписанным профилям конфигурации. Чтобы получить больше информации о подписанном коде, смотрите статью [«О подписывании кода»](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, which many Linux distributions use to do their DNS lookups, doesn't yet [support DoH](https://github.com/systemd/systemd/issues/8639). If you want to use DoH, you'll need to install a proxy like [dnscrypt-proxy](../dns.md#dnscrypt-proxy) and [configure it](https://wiki.archlinux.org/title/Dnscrypt-proxy) to take all the DNS queries from your system resolver and forward them over HTTPS.

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

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. При просмотре последующих пакетов "данных приложения" ни один из них не содержит запрашиваемого нами домена или возвращаемого IP-адреса.

## Почему мне **не следует** использовать зашифрованный DNS?

В местах, где существует фильтрация интернета (или цензура), посещение запрещенных ресурсов может иметь свои последствия, которые следует учитывать в [модели угроз](../basics/threat-modeling.md). Мы **не** предлагаем использовать для этих целей зашифрованный DNS. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. Если вы используете VPN, вам следует использовать DNS-серверы вашего VPN. Используя VPN, вы уже доверяете им всю свою сетевую активность.

Когда мы выполняем поиск в DNS, это, как правило, связано с тем, что мы хотим получить доступ к ресурсу. Ниже мы покажем некоторые методы, которые могут раскрыть вашу активность в интернете, даже при использовании зашифрованного DNS:

### IP-адрес

Самым простым способом определения активности в интернете может быть просмотр IP-адресов, к которым обращаются ваши устройства. Например, если наблюдатель знает, что сайт `privacyguides.org` находится по адресу `198.98.54.105`, а ваше устройство запрашивает данные с `198.98.54.105`, то велика вероятность, что вы посещаете Privacy Guides.

Этот метод полезен только в том случае, если IP-адрес принадлежит серверу, на котором размещено всего несколько веб-сайтов. It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). Он также не очень полезен, если сервер размещен за [обратным прокси](https://en.wikipedia.org/wiki/Reverse_proxy), что очень часто встречается в современном интернете.

### Индикация имени сервера (SNI)

Server Name Indication is typically used when an IP address hosts many websites. Это может быть сервис, например Cloudflare, или какая-либо другая защита от [Denial-of-Service атак](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. Снова запустите захват с помощью `tshark`. We've added a filter with our IP address, so you don't capture many packets:

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

6. Мы можем увидеть значение SNI, которые показывают посещаемые нами сайты. Команда `tshark` может дать вам значения непосредственно для всех пакетов, содержащих значение SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Это означает, что даже если мы используем серверы "зашифрованных DNS", домен, скорее всего, будет раскрыт через SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Недавно Россия [начала блокировать иностранные сайты](https://github.com/net4people/bbs/issues/108), использующие стандарт [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). Это связано с тем, что протокол [QUIC](https://en.wikipedia.org/wiki/QUIC), который является частью HTTP/3, требует, чтобы `ClientHello` также был зашифрован.

### Протокол состояния сетевого сертификата (OCSP)

Ваш браузер может раскрыть информацию о ваших действиях в нём ещё одним путём - [протоколом состояния сетевого сертификата](https://ru.wikipedia.org/wiki/OCSP). При посещении веб-сайта HTTPS, браузер может проверить, не был ли отозван [сертификат](https://en.wikipedia.org/wiki/Public_key_certificate) веб-сайта. Обычно это делается через протокол HTTP, что означает, что это действие **не** зашифровано.

Запрос OCSP содержит "[серийный номер](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)" сертификата, который является уникальным. Он отправляется "ответчику OCSP" для проверки его статуса.

Мы можем имитировать действия браузера с помощью команды [`openssl`](https://en.wikipedia.org/wiki/OpenSSL).

1. Получите сертификат сервера и с помощью [`sed`](https://en.wikipedia.org/wiki/Sed) сохраните только важную часть и запишите ее в файл:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. Получите промежуточный сертификат. [Центры сертификации (ЦС)](https://ru.wikipedia.org/wiki/%D0%A6%D0%B5%D0%BD%D1%82%D1%80_%D1%81%D0%B5%D1%80%D1%82%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8), обычно, не подписывают сертификат напрямую, они используют так называемый "промежуточный" сертификат.

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. Первый сертификат в `pg_and_intermediate.cert` на самом деле является сертификатом сервера из шага 1. Мы можем снова использовать `sed` для удаления всего, до первого экземпляра END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. Получение ответчика OCSP для сертификата сервера:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    Наш сертификат показывает ответчика сертификата Lets Encrypt. Если мы хотим увидеть все детали сертификата, мы можем использовать:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. Запустите захват пакетов:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. Выполните запрос OCSP:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. Откройте захват:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    В протоколе "OCSP" будет два пакета: "Request"(Запрос) и "Response"(Ответ). Для "Запроса" мы можем увидеть "серийный номер", развернув треугольник &#9656; рядом с каждым полем:

    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    Для "Ответа" мы также можем увидеть "серийный номер":

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

8. Или используйте `tshark` для фильтрации пакетов по серийному номеру:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

Если у сетевого наблюдателя есть публичный сертификат, который находится в открытом доступе, он может сопоставить серийный номер с этим сертификатом и по нему определить сайт, который вы посещаете. Этот процесс можно автоматизировать и связать IP-адреса с серийными номерами. Также можно проверить серийный номер в логах [Certificate Transparency](https://en.wikipedia.org/wiki/Certificate_Transparency).

## Следует ли мне использовать зашифрованный DNS?

Мы составили эту блок-схему, чтобы описать, когда вам *следует* использовать зашифрованный DNS:

``` mermaid
graph TB
    Start[Старт] --> anonymous{Пытаетесь быть <br> анонимны?}
    anonymous --> | Да | tor(используйте Tor)
    anonymous --> | Нет | censorship{Избегаете<br> цензуру?}
    censorship --> | Да| vpnOrTor(Используйте<br> VPN или Tor)
    censorship --> | Нет| privacy{Хотите больше приватности<br> от интернет-провайдера?}
    privacy --> | Да | vpnOrTor
    privacy --> | Нет | obnoxious{Интернет-провайдер <br> перенаправляет<br> ссылки?}
    obnoxious --> | Да | encryptedDNS(Используйте<br> зашифрованный DNS<br> от других фирм)
    obnoxious --> | Нет | ispDNS{Интернет-провайдер поддерживает<br> зашифрованный DNS?}
    ispDNS --> | Да | useISP(Используйте<br> зашифрованный DNS<br> от интернет-провайдера)
    ispDNS --> | Нет | nothing(Ничего не делайте)
```

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[Список рекомендуемых DNS-серверов](../dns.md ""){.md-button}

## Что такое DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) - это функция DNS, обеспечивающая проверку подлинности ответов на запросы о поиске доменных имен. Она не обеспечивает защиту конфиденциальности этих поисков, а скорее не позволяет злоумышленникам манипулировать ответами на запросы DNS.

Другими словами, DNSSEC подписывает данные цифровой подписью, чтобы гарантировать их достоверность. Чтобы обеспечить безопасность поиска, подпись происходит на каждом уровне процесса поиска DNS. В результате всем ответам DNS можно доверять.

Процесс подписи DNSSEC похож на процесс подписи юридического документа ручкой; этот человек подписывается уникальной подписью, которую никто другой не может создать, и судебный эксперт может посмотреть на эту подпись и убедиться, что документ был подписан именно этим человеком. Эти цифровые подписи гарантируют, что данные не были подделаны.

DNSSEC реализует иерархическую политику цифровой подписи на всех уровнях DNS. Например, в случае поиска `privacyguides.org` корневой DNS-сервер подпишет ключ для сервера имен `.org`, а сервер имен `.org` затем подпишет ключ для авторитетного сервера имен от `privacyguides.org`.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## Что такое минимизация QNAME?

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

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. Дальнейшее техническое описание определено в [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## Что такое клиентская подсеть EDNS (ECS)?

[Клиентская подсеть EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) - это метод рекурсивного DNS-резольвера для определения [подсети](https://en.wikipedia.org/wiki/Subnetwork) для [хоста или клиента](https://en.wikipedia.org/wiki/Client_(computing)), который делает DNS-запрос.

Он предназначен для "ускорения" доставки данных путем предоставления клиенту ответа, принадлежащего серверу, который находится рядом, например, [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), которые часто используются при потоковой передаче видео и обслуживании веб-приложений JavaScript.

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
