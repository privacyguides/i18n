---
title: "DNS Übersicht"
icon: material/dns
description: Das Domain Name System ist das "Telefonbuch des Internets" und hilft dem Browser, die gesuchte Webseite zu finden.
---

The [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System) is the 'phone book of the Internet'. DNS übersetzt Domainnamen in IP-Adressen, damit Browser und andere Dienste Internet-Ressourcen über ein dezentrales Netz von Servern laden können.

## Was ist DNS?

Wenn du eine Website besuchst, wird eine numerische Adresse zurückgegeben. Wenn du zum Beispiel `privacyguides.org` besuchst, wird die Adresse `192.98.54.105` zurückgegeben.

DNS gibt es schon seit den [Anfängen des Internets](https://de.wikipedia.org/wiki/Domain_Name_System#%C3%9Cberblick). DNS-Anfragen an und von DNS-Servern werden im Allgemeinen **nicht** verschlüsselt. In einer privaten Umgebung erhält der Kunde die Server vom Internetanbieter über [DHCP](https://de.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

Unverschlüsselte DNS-Anfragen können während der Übertragung leicht **überwacht** und **verändert** werden. In einigen Teilen der Welt werden Internetanbieter angewiesen, primitive [DNS-Filterung](https://en.wikipedia.org/wiki/DNS_blocking)durchzuführen. Wenn du die IP-Adresse einer gesperrten Domain anforderst, kann es sein, dass der Server nicht oder mit einer anderen IP-Adresse antwortet. Da das DNS-Protokoll nicht verschlüsselt ist, kann der Internetanbieter (oder jeder andere Netzbetreiber) [DPI](https://de.wikipedia.org/wiki/Deep_Packet_Inspection) einsetzen, um Anfragen zu überwachen. Internetanbieter können Anfragen auch auf der Grundlage gemeinsamer Merkmale blockieren, unabhängig davon, welcher DNS-Server verwendet wird.

Im Folgenden erörtern wir, was ein außenstehender Beobachter mit Hilfe von normalem unverschlüsseltem DNS und [verschlüsseltem DNS](#what-is-encrypted-dns)sehen kann, und stellen eine Anleitung dazu zur Verfügung.

### Unverschlüsselter DNS

1. Mit [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (Teil des [Wireshark](https://en.wikipedia.org/wiki/Wireshark) Projekts) können wir den Internet-Paketfluss überwachen und aufzeichnen. Dieser Befehl zeichnet Pakete auf, die den angegebenen Regeln entsprechen:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. We can then use [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, macOS, etc.) or [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) to send the DNS lookup to both servers. Software wie Webbrowser führen diese Nachschläge automatisch durch, sofern sie nicht für die Verwendung von verschlüsseltem DNS konfiguriert sind.

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

Wenn Sie den obigen Wireshark-Befehl ausführen, zeigt das obere Fenster die "[frames](https://en.wikipedia.org/wiki/Ethernet_frame)", und das untere Fenster zeigt alle Daten über den ausgewählten Frame. Filter- und Überwachungslösungen für Unternehmen (z. B. solche, die von Regierungen gekauft werden) können den Prozess automatisch und ohne menschliche Interaktion durchführen und diese Frames zusammenfassen, um statistische Daten zu erzeugen, die für den Netzwerkbeobachter nützlich sind.

| Nr. | Zeit     | Ursprung  | Ziel      | Protokoll | Länge | Info                                                                   |
| --- | -------- | --------- | --------- | --------- | ----- | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1   | DNS       | 104   | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1 | DNS       | 108   | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8   | DNS       | 104   | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1 | DNS       | 108   | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

Ein Beobachter könnte jedes dieser Pakete verändern.

## Was ist ein "verschlüsseltes DNS"?

Verschlüsseltes DNS kann sich auf eine Reihe von Protokollen beziehen, die gängigsten sind [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot) und [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) war eine der ersten Methoden zur Verschlüsselung von DNS-Anfragen. DNSCrypt arbeitet auf Port 443 und funktioniert mit den Transportprotokollen TCP und UDP. DNSCrypt has never been submitted to the [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) nor has it gone through the [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) process, so it has not been used widely outside a few [implementations](https://dnscrypt.info/implementations). Infolgedessen wurde es weitgehend durch das populärere [DNS über HTTPS](#dns-over-https-doh) ersetzt.

### DNS über TLS (DoT)

[**DNS über TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) ist eine weitere Methode zur Verschlüsselung der DNS-Kommunikation, die in [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858) definiert ist. Die Unterstützung wurde erstmals in Android 9, iOS 14 und unter Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in Version 237 implementiert. In den letzten Jahren hat sich die Präferenz in der Branche von DoT auf DoH verlagert, da DoT ein [komplexes Protokoll](https://dnscrypt.info/faq) ist und die Einhaltung des RFC bei den vorhandenen Implementierungen unterschiedlich ist. DoT arbeitet auch über einen speziellen Port 853, der von restriktiven Firewalls leicht blockiert werden kann.

### DNS über HTTPS (DoH)

[**DNS über HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)wie in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484) definiert, verpackt Abfragen im [HTTP/2-Protokoll](https://en.wikipedia.org/wiki/HTTP/2) und bietet Sicherheit mit HTTPS. Die Unterstützung wurde erstmals in Webbrowsern wie Firefox 60 und Chrome 83 hinzugefügt.

Die native Implementierung von DoH tauchte in iOS 14, macOS 11, Microsoft Windows und Android 13 auf (sie wird jedoch nicht [standardmäßig](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144) aktiviert). Der allgemeine Linux-Desktop-Support wartet auf die [systemd-Implementierung](https://github.com/systemd/systemd/issues/8639), so dass [die Installation von Drittanbieter-Software weiterhin erforderlich ist](../dns.md#encrypted-dns-proxies).

### Native Betriebssystemunterstützung

#### Android

Android 9 und höher unterstützen DNS über TLS. Die Einstellungen sind zu finden unter: **Einstellungen** &rarr; **Netzwerk & Internet** &rarr; **Privates DNS**.

#### Apple-Geräte

Die neuesten Versionen von iOS, iPadOS, tvOS und macOS unterstützen sowohl DoT als auch DoH. Beide Protokolle werden nativ über [Konfigurationsprofile](https://support.apple.com/de-de/guide/security/secf6fb9f053/web) oder über die [DNS Settings API](https://developer.apple.com/documentation/networkextension/dns_settings)unterstützt.

Nach der Installation eines Konfigurationsprofils oder einer Anwendung, die die DNS-Einstellungs-API verwendet, kann die DNS-Konfiguration ausgewählt werden. Wenn ein VPN aktiv ist, verwendet die DNS Auflösung innerhalb des VPN-Tunnels die DNS-Einstellungen des VPN und nicht deine systemweiten Einstellungen.

Apple bietet keine native Schnittstelle zur Erstellung von Profilen mit verschlüsseltem DNS. [Secure DNS profile creator](https://dns.notjakob.com/tool.html) ist ein inoffizielles Tool zur Erstellung eigener Profile mit verschlüsseltem DNS, diese sind jedoch nicht signiert. Signierte Profile sind zu bevorzugen; das Signieren bestätigt die Herkunft eines Profils und trägt dazu bei, die Integrität der Profile zu gewährleisten. Signierte Konfigurationsprofile erhalten ein grünes "Verifiziert"-Label. Weitere Informationen zum Code Signing findest du unter [Über Code Signing](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### Linux

`systemd-resolved`, das viele Linux-Distributionen für die DNS-Suche verwenden, [unterstützt DoH](https://github.com/systemd/systemd/issues/8639) noch nicht. Wenn Sie DoH verwenden möchten, müssen Sie einen Proxy wie [dnscrypt-proxy](../dns.md#dnscrypt-proxy) installieren und [ihn](https://wiki.archlinux.org/title/Dnscrypt-proxy) so [konfigurieren](https://wiki. archlinux. org/title/Dnscrypt-proxy), dass er alle DNS-Anfragen von Ihrem Systemresolver entgegennimmt und über HTTPS weiterleitet.

## Was kann ein Außenstehender sehen?

In diesem Beispiel werden wir aufzeichnen, was passiert, wenn wir eine DoH-Anfrage stellen:

1. Starten Sie zunächst `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. Zweitens: Stellen Sie eine Anfrage mit `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. Nach der Anfrage können wir die Paketaufnahme mit <kbd>STRG</kbd> + <kbd>C</kbd> beenden.

4. Analyze the results in Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

Wir können den [Verbindungsaufbau](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) und den [TLS-Handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) sehen, der bei jeder verschlüsselten Verbindung stattfindet. Die folgenden "Anwendungsdaten"-Pakete enthalten weder die von uns angeforderte Domäne noch die zurückgegebene IP-Adresse.

## Why **shouldn't** I use encrypted DNS?

In locations where there is internet filtering (or censorship), visiting forbidden resources may have its own consequences which you should consider in your [threat model](../basics/threat-modeling.md). We do **not** suggest the use of encrypted DNS for this purpose. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. If you're using a VPN, you should use your VPN's DNS servers. When using a VPN, you are already trusting them with all your network activity.

When we do a DNS lookup, it's generally because we want to access a resource. Below, we will discuss some of the methods that may disclose your browsing activities even when using encrypted DNS:

### IP Address

The simplest way to determine browsing activity might be to look at the IP addresses your devices are accessing. For example, if the observer knows that `privacyguides.org` is at `198.98.54.105`, and your device is requesting data from `198.98.54.105`, there is a good chance you're visiting Privacy Guides.

This method is only useful when the IP address belongs to a server that only hosts few websites. It's also not very useful if the site is hosted on a shared platform (e.g. GitHub Pages, Cloudflare Pages, Netlify, WordPress, Blogger, etc.). It also isn't very useful if the server is hosted behind a [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy), which is very common on the modern Internet.

### Server Name Indication (SNI)

Server Name Indication is typically used when an IP address hosts many websites. This could be a service like Cloudflare, or some other [Denial-of-service attack](https://en.wikipedia.org/wiki/Denial-of-service_attack) protection.

1. Start capturing again with `tshark`. We've added a filter with our IP address, so you don't capture many packets:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. Then we visit [https://privacyguides.org](https://privacyguides.org).

3. After visiting the website, we want to stop the packet capture with <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. Next we want to analyze the results:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    We will see the connection establishment, followed by the TLS handshake for the Privacy Guides website. Around frame 5. you'll see a "Client Hello".

5. Expand the triangle &#9656; next to each field:

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

This means even if we are using "Encrypted DNS" servers, the domain will likely be disclosed through SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. Recently, Russia has [started blocking foreign websites](https://github.com/net4people/bbs/issues/108) that use the [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) standard. This is because the [QUIC](https://en.wikipedia.org/wiki/QUIC) protocol that is a part of HTTP/3 requires that `ClientHello` also be encrypted.

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

## Should I use encrypted DNS?

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

Encrypted DNS with a third party should only be used to get around redirects and basic [DNS blocking](https://en.wikipedia.org/wiki/DNS_blocking) when you can be sure there won't be any consequences, or you're interested in a provider that does some rudimentary filtering.

[List of recommended DNS servers](../dns.md ""){.md-button}

## What is DNSSEC?

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) is a feature of DNS that authenticates responses to domain name lookups. It does not provide privacy protections for those lookups, but rather prevents attackers from manipulating or poisoning the responses to DNS requests.

In other words, DNSSEC digitally signs data to help ensure its validity. In order to ensure a secure lookup, the signing occurs at every level in the DNS lookup process. As a result, all answers from DNS can be trusted.

The DNSSEC signing process is similar to someone signing a legal document with a pen; that person signs with a unique signature that no one else can create, and a court expert can look at that signature and verify that the document was signed by that person. These digital signatures ensure that data has not been tampered with.

DNSSEC implements a hierarchical digital signing policy across all layers of DNS. For example, in the case of a `privacyguides.org` lookup, a root DNS server would sign a key for the `.org` nameserver, and the `.org` nameserver would then sign a key for `privacyguides.org`’s authoritative nameserver.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## What is QNAME minimization?

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

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. Further technical description is defined in [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## What is EDNS Client Subnet (ECS)?

The [EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) is a method for a recursive DNS resolver to specify a [subnetwork](https://en.wikipedia.org/wiki/Subnetwork) for the [host or client](https://en.wikipedia.org/wiki/Client_(computing)) which is making the DNS query.

It's intended to "speed up" delivery of data by giving the client an answer that belongs to a server that is close to them such as a [content delivery network](https://en.wikipedia.org/wiki/Content_delivery_network), which are often used in video streaming and serving JavaScript web apps.

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
