---
title: "DNS 簡介"
icon: material/dns
description: 網域名稱系統是“網際網路電話簿” ，可幫助瀏覽器找到它正在尋找的網站。
---

[網域名稱系統](https://en.wikipedia.org/wiki/Domain_Name_System) 是「網際網路的電話簿」。 DNS 將網域名稱轉換為 IP 位址，以便瀏覽器和其他服務可以通過分散的伺服器網路載入網路資源。

## 什麼是 DNS？

當您訪問一個網站時，會傳回一個數字地址。 以訪問 `privacyguides.org`網站為例，它傳回的地址為 `192.98.54.105` 。

DNS 從網際網路的 [早期](https://en.wikipedia.org/wiki/Domain_Name_System#History) 就存在了。 來往 DNS 伺服器的 DNS 請求通常 **不是** 加密的。 一般家用的網路中，客戶的伺服器通常是由 ISP 透過 [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)給予的。

未經加密的 DNS 請求很容易**被監視** 或在傳輸過程中**遭到修改modified**。 在某些地區， ISP 被要求做初級的 [DNS 過濾](https://en.wikipedia.org/wiki/DNS_blocking)。 當您要求被封鎖網域的IP位址時，伺服器可能不會回應，或可能會使用其他IP位址回應。 由於DNS通訊協定沒有加密， ISP （或任何網路營運商）可以使用 [DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) 來監控請求。 網路服務供應商也可以根據共同特徵封鎖請求，無論你使用哪種 DNS 伺服器。 未加密的 DNS 總是使用 53 號[端口](https://en.wikipedia.org/wiki/Port_(computer_networking)) ，並且總是使用UDP。

接下來，我們將討論並提供一個教程來證明外部觀察者可以使用普通的未加密 DNS 和 [加密 DNS ](#what-is-encrypted-dns)看到什麼。

### 未加密的 DNS

1. 使用 [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) ([Wireshark](https:// en.wikipedia.org/wiki/Wireshark)專案）可以監控和記錄網路封包。 此命令記錄符合指定規則的封包：

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. 然後我們可以使用 [`dig`](https://en.wikipedia.org/wiki/Dig_(command)) （ Linux ， MacOS 等）或 [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) （ Windows ）將 DNS查詢發送到兩個伺服器。 Web 瀏覽器等軟體會自動執行這些查詢，除非它們被配置為使用加密的DNS。

    === "Linux ， macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "Windows"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. 接下來，[分析](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs)結果：

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

如果執行上面的 Wireshark 命令，頂部窗格會顯示「[frame](https://en.wikipedia.org/wiki/Ethernet_frame)」，底部窗格會顯示所選框架的所有資料。 企業過濾和監控解決方案（例如政府購買的解決方案）可以自動執行此過程，而無需人工交互，並且可以聚合這些框架以產生對網路觀察者有用的統計數據。

| 不。 | 時間       | 來源        | 目的地       | 協議  | 長度  | 資訊                                                                     |
| -- | -------- | --------- | --------- | --- | --- | ---------------------------------------------------------------------- |
| 1  | 0.000000 | 192.0.2.1 | 1.1.1.1   | DNS | 104 | Standard query 0x58ba A privacyguides.org OPT                          |
| 2  | 0.293395 | 1.1.1.1   | 192.0.2.1 | DNS | 108 | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3  | 1.682109 | 192.0.2.1 | 8.8.8.8   | DNS | 104 | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4  | 2.154698 | 8.8.8.8   | 192.0.2.1 | DNS | 108 | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

觀察者可以修改這些封包。

## 什麼是「加密後的 DNS」 ？

加密 DNS 可以指多種協定之一，最常見的協定是 [DNSCrypt](#dnscrypt)、[DNS over TLS ](#dns-over-tls-dot) 和[DNS over HTTPS](#dns-over-https-doh)。

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) 是第一種查詢加密 DNS 的方法之一。 DNSCrypt 在 443 端口上運作，與 TCP 或 UDP 傳輸協議一起使用。 DNSCrypt 從未向 [Internet Engineering Task Force (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force)提交文件 ，也未通過 [Request for Comments (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments) 流程，因此 [實用少](https://dnscrypt.info/implementations)並未被廣泛使用。 因此，它大量被更受歡迎的 [DNS over HTTPS](#dns-over-https-doh) 取代。

### 通過 TLS 的 DNS)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) 是另一種加密 DNS 通訊方式，其定義於 [RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858)。 首次於 Android 9、iOS 14 和 Linux 上的 [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) 在版本237 提供支援。 近年來，業界偏好已經從 DoT 轉移到 DoH ，因為 DoT 協議[複雜](https://dnscrypt.info/faq) ，並且在實現中對RFC 的遵照狀況各不相同。 DoT 還在專用端口 853 上運行，但很容易被限制性防火牆阻止。

### 通過 HTTPS 的 DNS)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS)，如 [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484)所定義，將查詢打包在[ HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) 協定並透過 HTTPS 提供安全。 最初使用於 Firefox 60 和 Chrome 83 等網頁瀏覽器。

DoH 原生執行出現在 iOS 14, macOS 11, Microsoft Windows, 與 Android 13 (不過其並未[預設啟動 ](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144))。 一般 Linux 桌面支援仍待 systemd [實現](https://github.com/systemd/systemd/issues/8639)， 所以 [還是得安裝第三方軟體](../dns.md#encrypted-dns-proxies)。

### 原生作業系統支援

#### Android

Android 9 以上版本支持 DoT (DNS over TLS)。 設定方式可以在以下位置找到： **設定** &rarr; **網路 & 網際網路** &rarr; **私人 DNS**。

#### Apple裝置

最新版本的 iOS、iPadOS、tvOS 和 macOS 都支持 DoT 和 DoH。 這兩個通訊協議都透過 [組態檔](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) 或透過 [DNS 設定 API ](https://developer.apple.com/documentation/networkextension/dns_settings)獲得原生支援。

安裝設定設定檔或使用 DNS 設定API 的應用程式後，即可選擇 DNS 設定。 如果啟用 VPN， 隧道內的解析將使用 VPN 的 DNS 設置，而不是設備系統的設置。

Apple不提供用於建立加密DNS設定檔的原生介面。 [Secure DNS profile creator](https://dns.notjakob.com/tool.html) 是一款非正式工具用以建立您自己的加密 DNS 設定檔。不過這個軟體並未得到簽署。 最好是簽署過個人資設定檔；簽署會驗證個人資料的來源，並有助於確保個人資料的完整性。 綠色的「已驗證」標籤會提供給已簽署的配置文件。 代碼簽名的詳細資訊，請參閱 [關於代碼簽名](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html)。

#### Linux

許多 Linux 版本所使用的distributions DNS lookups `systemd-resolved`尚未[支援 DoH](https://github.com/systemd/systemd/issues/8639)。 如果要使用 DoH ，您需要安裝一個類似[dnscrypt-proxy](../dns.md#dnscrypt-proxy)的代理，並[設定](https://wiki.archlinux.org/title/Dnscrypt-proxy) 系統解析器獲取所有 DNS 查詢，透過 HTTPS 轉發。

## 外部人士可以看到什麼？

在此範例中，我們將記錄當我們提出 DoH 請求時發生的事情：

1. 首先，打開 `tshark`：

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. 其次，使用 `curl`提出請求：

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. 提出請求後，快速鍵 <kbd>CTRL</kbd> + <kbd>C</kbd>可停止封包捉取。

4. 在 Wireshark 中分析結果：

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

可看到[連接建立](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_builtment)和[TLS 握手](https://cloudflare.com/learning/ssl/ What-happens-in-a-tls-handshake)發生在加密連線時。 當查看隨後的“應用程序數據”封包時，都不包含所請求的域名或它的 IP 地址。

## 什麼時候 **不該** 使用加密的 DNS ？

在有網路過濾（或審查）的地方，訪問被禁止的資源可能會產生某些後果，您應該在 [威脅模型](../basics/threat-modeling.md)中考慮這些後果。 非常 **不建議**把加密 DNS 用在此目的上。 請改用 [Tor](../advanced/tor-overview.md) 或 [VPN](../vpn.md)。 如果您使用的是VPN ，則應使用 VPN 的 DNS 伺服器。 使用 VPN 時，您已經信任它們與您的所有網路活動。

當我們進行 DNS 查詢時，通常是因為我們想要存取資源。 接下來，我們將討論一些即使在使用加密 DNS 時也可能會披露您的瀏覽活動的情況：

### IP 位址

確定瀏覽活動的最簡單方法可能是查看您的設備正在訪問的 IP 位址。 例如，如果觀察者知道 `privacyguides.org` 位於 `198.98.54.105`，而您的裝置正在請求 `198.98.54.105`的數據，則很有可能您正在訪問隱私指南。

此方法僅在 IP 位址屬於僅託管少數網站的伺服器時才有用。 如果網站託管在共享平臺(例如 Github Pages ， Cloudflare Pages ， Netlify ， WordPress ， Blogger等)，它就不太有用。 如果服務器託管在 [反向代理](https://en.wikipedia.org/wiki/Reverse_proxy)之後，這也不是很有用，這在現代互聯網上非常常見。

### 伺服器名指示(SNI)

伺服器名稱指示通常用於IP位址託管多個網站時。 這可能是像 Cloudflare 的服務，或者其他 [阻斷服務攻擊](https://en.wikipedia.org/wiki/Denial-of-service_attack) 保護。

1. 再次開始捕捉 `tshark`。 我們添加了一個自身IP 地址的過濾器，因此您不會捕獲過多封包：

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. 然後訪問 [https://privacyguides.org](https://privacyguides.org)。

3. 在訪問網站後，以 <kbd>CTRL</kbd> + <kbd>C</kbd>停止封包捕捉。

4. 接下來分析結果：

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    連接建立後與 privacyguides 網站的TLS 握手。 大約在第5 幀附近。 你會看到一個“客戶你好”。

5. 展開每個字段旁邊的三角形 &#9656; ：

    ```text
    ▸ Transport Layer Security
      ▸ TLSv1.3 Record Layer: Handshake Protocol: Client Hello
        ▸ Handshake Protocol: Client Hello
          ▸ Extension: server_name (len=22)
            ▸ Server Name Indication extension
    ```

6. 我們可以看到我們正在訪問的網站的SNI值。 `tshark` 命令可以直接爲所有包含 SNI 封包提供值：

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

即便使用「加密 DNS」伺服器，網域也可能會透過 SNI 披露。 [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) 協議帶來 [加密的 Client Hello](https://blog.cloudflare。com /encrypted-client-hello)，可防止這種洩漏。

各國政府，特別是中國< /a> 和[俄羅斯](https://zdnet.com/article/ Russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh- dot -esni)，已經[開始阻止](https://en.wikipedia.org/wiki/Server_Name_Inspiration#Encrypted_Client_Hello)它，或表達出企圖這樣做的想法。 近來俄羅斯 開始屏蔽使用 [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3)的外國網站。 這是因為作為HTTP/3的一部分的 [QUIC](https://en.wikipedia.org/wiki/QUIC) 協議要求 `ClientHello` 也被加密。</p> 



### 線上憑邆狀態協議 (OCSP)

瀏覽器會披露瀏覽活動的另一種方式是使用 [線上憑證狀態協議 (Online Certificate Status Protocol)](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol)。 訪問有 HTTPS 網站時，瀏覽器會檢查網站的 [憑證](https://en.wikipedia.org/wiki/Public_key_certificate) 是否已被撤銷。 這是透過 HTTP 協議完成的，這意味著它**不是** 加密的。

OCSP 請求包含憑證，其帶有獨特的"[序列號](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)"。 它被發送到 “OCSP 回應器”去檢查其狀態。

利用 [`openssl`](https://en.wikipedia.org/wiki/OpenSSL) 命令模擬瀏覽器會做什麼。

1. 取得伺服器憑證並使用 [`sed`](https://en.wikipedia.org/wiki/Sed) 來保留重要部分並將其寫入檔案： 
   
   

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```


2. 取得中間憑證。 [憑證授權機構(CA)](https://en.wikipedia.org/wiki/Certificate_authority) 通常不會直接簽署憑證；他們使用所謂的「中間」憑證。 
   
   

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```


3. `pg_and_intermediate.cert` 中的第一個憑證實際上是步驟1 的伺服器憑證。 我們可以再次使用 `sed` 來刪除直到 END 第一個實例： 
   
   

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```


4. 取得伺服器憑證的OCSP 回應器： 
   
   

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```


我們的憑證顯示 Lets Encrypt 憑證回應器。 如果我們想查看憑證的所有細節，我們可以使用： 



    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```


5. 開始捕取封包: 
   
   

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```


6. 提出 OCSP 要求： 
   
   

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```


7. 打開捕捉資料： 
   
   

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```


將會有兩個帶有「OCSP」通訊協定的封包：「Request」和「Response」。 對於“Request” ，可以通過擴展每個字段旁邊的三角形 &#9656; 來看到“序列號” ： 



    ```bash
    ▸ Online Certificate Status Protocol
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```


對於“回應” ，我們也可以看到“序列號” ： 



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


8. 或者使用 `tshark` 來過濾序列號的封包： 
   
   

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```


如果網路觀察者拿到可公開取得的公共憑證，就可將序列號與該憑證作匹配，從而確定您正在訪問的網站。 這個過程可以自動化，並且可以將IP地址與序列號相關聯。 也可檢查 [憑證透明度](https://en.wikipedia.org/wiki/Certificate_Transparency) 日誌的序列號。



## 我應該用加密 DNS 嗎？

這個流程圖描述了何時 *應該使用* 加密 DNS:



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


與第三方合作的加密 DNS 應限於避開重定向和基本的 [DNS 封鎖](https://en.wikipedia.org/wiki/DNS_blocking) ，也就是確定無後顧或對供應商的基本過濾感興趣時才用第三方。

[推薦的 DNS 伺服器列表](../dns.md ""){.md-button}



## 什麼是 DNSSEC ？

[Domain Name System Security Extensions](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC)是 DNS 的一項功能，域名查找的回應予以驗證。 它無法為查詢者提供隱私保護，而是防止攻擊者操縱或毒害對DNS 請求的回應。

換句話說， DNSSEC 對資料進行數位簽名，幫助確保其有效性。 為了確保安全查找，過程中的每個層級都會簽名。 因此，DNS 全部的回答都可以被信任。

DNSSEC 簽署過程類似於無法仿製的個人獨特簽名於法律文件，法院專家透過簽名驗證該文件效力須依據簽名的真假判定。 這些數位簽名確保資料不會被篡改。

DNSSEC 在所有 DNS 層中實施分級數位簽名政策。 例如，查詢 `privacyguides.org` ，根 DNS 伺服器將簽署尾綴 `.org` 伺服器密鑰，然後 `.org` 伺服器再簽署 `privacyguides.org`的授權名稱伺服器的密鑰。

<small>改編自 Google 的 [DNS 安全擴充 (DNSSEC) 概述](https://cloud.google.com/dns/docs/dnssec) 和 Cloudflare 提供的[DNSSEC：簡介](https://blog.cloudflare.com/dnssec- an -introduction），兩者皆以 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0) 授權。</small> 



## 什麼是QNAME最小化？

QNAME 指 "合格域名"，例如 `discuss.privacyguides.net`. 過去，在解析網域名稱時， DNS 解析器會要求鏈中各伺服器提供關於此查詢的全部資訊。 在下面範例中，每個 DNS 伺服器提供者都會被詢問尋找 `discuss.privacyguides.net` IP 位址的請求：

| 伺服器                | 問題請求                                | 回應                           |
| ------------------ | ----------------------------------- | ---------------------------- |
| 根伺服器               | Discuss.privacyguides.net 的 IP 是多少? | 不知道，請求 .net 伺服器              |
| .net 伺服器           | Discuss.privacyguides.net 的 IP 是多少? | 不知道，請求 Privacy Guides 伺服器... |
| Privacy Guides 伺服器 | Discuss.privacyguides.net 的 IP 是多少? | 5.161.195.190!               |


透過“QNAME 最小化”，DNS 解析器現在只需要足夠的資訊來尋找鏈中的下一個伺服器。 在範例中，僅要求根伺服器提供足夠的資訊來尋找 .net TLD 的適當名稱伺服器等，而無需知道您嘗試造訪的完整網域：

| 伺服器                | 問題請求                                 | 回應                      |
| ------------------ | ------------------------------------ | ----------------------- |
| 根伺服器               | 什麼是 .net 域名伺服器?                      | *提供 .net 伺服器*           |
| .net 伺服器           | Privacyguides.net 的域名伺服器是什麼?         | *提供 Privacy Guides 伺服器* |
| Privacy Guides 伺服器 | discuss.privacyguides.net 的域名伺服器是什麼? | 此伺服器                    |
| Privacy Guides 伺服器 | Discuss.privacyguides.net 的 IP 是多少?  | 5.161.195.190           |


雖然此過程可能稍減低效率低，但中央根網域伺服器和 TLD 網域伺服器都不會收到有關您的*完整*查詢的資訊，從而減少了資訊量傳輸您瀏覽習慣。 進一步的技術描述在 [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816)。



## 什麼是 EDNS 客戶端子網(ECS ) ？

[EDNS Client Subnet](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) 是遞歸DNS 解析器為DNS 查詢的 [主機或客戶端](https://en.wikipedia.org/wiki/Client_(computing))，指定 [子網絡](https://en.wikipedia.org/wiki/Subnetwork) 的方法。

它的目的是回答客戶端距離最靠近的伺服器以“加快”資料的傳遞，類似[內容傳遞網絡](https://en.wikipedia.org/wiki/Content_delivery_network)，後者通常用於視頻串流和 JavaScript Web 應用程序。

此功能確實以隱私為代價，因為它會告訴 DNS伺服器一些有關客戶端位置的資訊。 例如，如果 IP 位址是 `198.51.100.32`，DNS 提供者可能會與權威伺服器共用 `198.51.100.0/24`。 一些 DNS 提供者透過大約鄰近位置的另一個 IP 位址來匿名化此資料。

如果有安裝 `dig`，可以用以下命令測試 DNS 提供者是否向 DNS 名稱伺服器提供 EDNS 資訊：



```bash
dig +nocmd -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


請注意，此命令將聯絡 Google 進行測試，並返回您的 IP 以及 EDNS 客戶端子網資訊。 如要測試另一個 DNS 解析器，可指定其 IP，例如測試 `9.9.9.11`：



```bash
dig +nocmd @9.9.9.11 -t txt o-o.myaddr.l.google.com +nocomments +noall +answer +stats
```


如果結果包含第二筆 edns0-client-subnet TXT 記錄（如下所示），則您的 DNS 伺服器正在傳遞 EDNS 資訊。 後面顯示的 IP 或網路是您的 DNS 提供者與 Google 共享的準確資訊。



```text
o-o.myaddr.l.google.com. 60 IN TXT "198.51.100.32"
o-o.myaddr.l.google.com. 60 IN TXT "edns0-client-subnet 198.51.100.0/24"
;; Query time: 64 msec
;; SERVER: 9.9.9.11#53(9.9.9.11)
;; WHEN: Wed Mar 13 10:23:08 CDT 2024
;; MSG SIZE  rcvd: 130
```
