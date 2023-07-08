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

6. Мы можем увидеть значение SNI, которые показывают посещаемые нами сайты. Команда `tshark` может дать вам значения непосредственно для всех пакетов, содержащих значение SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

Это означает, что даже если мы используем серверы "зашифрованных DNS", домен, скорее всего, будет раскрыт через SNI. Протокол [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) предлагает функцию [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello/), которая предотвращает подобную утечку.

Правительства, в частности [Китая](https://www.zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni/) и [России](https://www.zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni/), либо уже [начали блокировать](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) его, либо выразили желание сделать это. Недавно Россия [начала блокировать иностранные сайты](https://github.com/net4people/bbs/issues/108), использующие стандарт [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3). Это связано с тем, что протокол [QUIC](https://en.wikipedia.org/wiki/QUIC), который является частью HTTP/3, требует, чтобы `ClientHello` также был зашифрован.

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

Зашифрованный DNS, предоставляемые не вашим интернет-провайдером, следует использовать только для обхода перенаправлений и обхода базовой [блокировки DNS](https://en.wikipedia.org/wiki/DNS_blocking) тогда, когда вы можете быть уверены, что это не повлечет за собой никаких последствий или вы заинтересованы в провайдере, который осуществляет элементарную фильтрацию.

[Список рекомендуемых DNS-серверов](../dns.md ""){.md-button}

## Что такое DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) - это функция DNS, обеспечивающая проверку подлинности ответов на запросы о поиске доменных имен. Она не обеспечивает защиту конфиденциальности этих поисков, а скорее не позволяет злоумышленникам манипулировать ответами на запросы DNS.

Другими словами, DNSSEC подписывает данные цифровой подписью, чтобы гарантировать их достоверность. Чтобы обеспечить безопасность поиска, подпись происходит на каждом уровне процесса поиска DNS. В результате всем ответам DNS можно доверять.

Процесс подписи DNSSEC похож на процесс подписи юридического документа ручкой; этот человек подписывается уникальной подписью, которую никто другой не может создать, и судебный эксперт может посмотреть на эту подпись и убедиться, что документ был подписан именно этим человеком. Эти цифровые подписи гарантируют, что данные не были подделаны.

DNSSEC реализует иерархическую политику цифровой подписи на всех уровнях DNS. Например, в случае поиска `privacyguides.org` корневой DNS-сервер подпишет ключ для сервера имен `.org`, а сервер имен `.org` затем подпишет ключ для авторитетного сервера имен от `privacyguides.org`.

<small>Адаптировано из [Обзор расширений безопасности DNS (DNSSEC)](https://cloud.google.com/dns/docs/dnssec) от Google и [DNSSEC: введение](https://blog.cloudflare.com/dnssec-an-introduction/) от Cloudflare, оба лицензированы под [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).</small>

## Что такое минимизация QNAME?

QNAME - это "квалифицированное имя", например `privacyguides.org`. Минимизация QNAME уменьшает объем информации, отправляемой с сервера DNS на [авторитетный сервер имен](https://en.wikipedia.org/wiki/Name_server#Authoritative_name_server).

Вместо того чтобы отправлять весь домен `privacyguides.org`, минимизация QNAME означает, что DNS-сервер будет запрашивать все записи, которые заканчиваются на `.org`. Дальнейшее техническое описание определено в [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## Что такое клиентская подсеть EDNS (ECS)?

[Клиентская подсеть EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) - это метод рекурсивного DNS-резольвера для определения [подсети](https://en.wikipedia.org/wiki/Subnetwork) для [хоста или клиента](https://en.wikipedia.org/wiki/Client_(computing)), который делает DNS-запрос.

Он предназначен для "ускорения" доставки данных путем предоставления клиенту ответа, принадлежащего серверу, который находится рядом, например, [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), которые часто используются при потоковой передаче видео и обслуживании веб-приложений JavaScript.

Эта функция работает в ущерб конфиденциальности, поскольку она сообщает DNS-серверу некоторую информацию о местонахождении клиента.
