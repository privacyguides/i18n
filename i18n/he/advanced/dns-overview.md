---
title: "סקירה כללית של DNS"
icon: material/dns
description: מערכת שמות הדומיין היא "ספר הטלפונים של האינטרנט", שעוזרת לדפדפן שלך למצוא את האתר שהוא מחפש.
---

[מערכת שמות הדומיין](https://en.wikipedia.org/wiki/Domain_Name_System) היא 'ספר הטלפונים של האינטרנט'. DNS מתרגם שמות דומיין לכתובות IP כך שדפדפנים ושירותים אחרים יכולים לטעון משאבי אינטרנט, דרך רשת מבוזרת של שרתים.

## מה זה DNS?

כאשר אתה מבקר באתר אינטרנט, מוחזרת כתובת מספרית. לדוגמה, כאשר אתה מבקר ב-`privacyguides.org`, הכתובת `192.98.54.105` מוחזרת.

DNS קיים מאז [הימים הראשונים](https://en.wikipedia.org/wiki/Domain_Name_System#History) של האינטרנט. בקשות DNS המבוצעות אל ומשרתי DNS **אינן** מוצפנות בדרך כלל. בסביבה מגורים, לקוח מקבל שרתים על ידי ספק שירותי האינטרנט באמצעות [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol).

בקשות DNS לא מוצפנות יכולות להיות **למעקב** בקלות ו**לשנות** בזמן העברה. בחלקים מסוימים של העולם, ספקי האינטרנט מצווים לבצע [סינון DNS](https://en.wikipedia.org/wiki/DNS_blocking) פרימיטיבי. כאשר אתה מבקש כתובת IP של דומיין חסום, ייתכן שהשרת לא יגיב או שיגיב עם כתובת IP אחרת. מכיוון שפרוטוקול ה-DNS אינו מוצפן, ספק שירותי האינטרנט (או כל מפעיל רשת) יכול להשתמש ב-[DPI](https://en.wikipedia.org/wiki/Deep_packet_inspection) כדי לנטר בקשות. ספקי שירותי אינטרנט יכולים גם לחסום בקשות על סמך מאפיינים משותפים, ללא קשר לשרת ה-DNS שבו נעשה שימוש. DNS לא מוצפן משתמש תמיד ב[פורט](https://en.wikipedia.org/wiki/Port_(computer_networking)) 53 ותמיד משתמש ב-UDP.

להלן, אנו דנים ומספקים מדריך כדי להוכיח את מה שצופה מבחוץ עשוי לראות באמצעות DNS רגיל לא מוצפן ו[DNS מוצפן](#what-is-encrypted-dns).

### DNS לא מוצפן

1. Using [`tshark`](https://wireshark.org/docs/man-pages/tshark.html) (part of the [Wireshark](https://en.wikipedia.org/wiki/Wireshark) project) we can monitor and record internet packet flow. פקודה זו מתעדת מנות העומדות בכללים שצוינו:

    ```bash
    tshark -w /tmp/dns.pcap udp port 53 and host 1.1.1.1 or host 8.8.8.8
    ```

2. לאחר מכן נוכל להשתמש ב[`dig`](https://en.wikipedia.org/wiki/Dig_(command)) (Linux, MacOS וכו') או [`nslookup`](https://en.wikipedia.org/wiki/Nslookup) (Windows) כדי לשלוח את בדיקת ה-DNS לשני השרתים. תוכנות כגון דפדפני אינטרנט מבצעות חיפושים אלו באופן אוטומטי, אלא אם כן הם מוגדרים לשימוש ב-DNS מוצפן.

    === "לינוקס, macOS"

        ```
        dig +noall +answer privacyguides.org @1.1.1.1
        dig +noall +answer privacyguides.org @8.8.8.8
        ```
    === "ווינדוס"

        ```
        nslookup privacyguides.org 1.1.1.1
        nslookup privacyguides.org 8.8.8.8
        ```

3. Next, we want to [analyse](https://wireshark.org/docs/wsug_html_chunked/ChapterIntroduction.html#ChIntroWhatIs) the results:

    === "Wireshark"

        ```
        wireshark -r /tmp/dns.pcap
        ```

    === "tshark"

        ```
        tshark -r /tmp/dns.pcap
        ```

אם אתה מפעיל את פקודת Wireshark למעלה, החלונית העליונה מציגה את "[מסגרות](https://en.wikipedia.org/wiki/Ethernet_frame)", והחלונית התחתונה מציגה את כל הנתונים אודות המסגרת שנבחרה. פתרונות סינון וניטור ארגוניים (כגון אלה שנרכשו על ידי ממשלות) יכולים לבצע את התהליך באופן אוטומטי, ללא אינטראקציה אנושית, ויכולים לצבור מסגרות אלה כדי לייצר נתונים סטטיסטיים שימושיים לצופה ברשת.

| No. | Time     | Source    | Destination | Protocol | Length | Info                                                                   |
| --- | -------- | --------- | ----------- | -------- | ------ | ---------------------------------------------------------------------- |
| 1   | 0.000000 | 192.0.2.1 | 1.1.1.1     | DNS      | 104    | Standard query 0x58ba A privacyguides.org OPT                          |
| 2   | 0.293395 | 1.1.1.1   | 192.0.2.1   | DNS      | 108    | Standard query response 0x58ba A privacyguides.org A 198.98.54.105 OPT |
| 3   | 1.682109 | 192.0.2.1 | 8.8.8.8     | DNS      | 104    | Standard query 0xf1a9 A privacyguides.org OPT                          |
| 4   | 2.154698 | 8.8.8.8   | 192.0.2.1   | DNS      | 108    | Standard query response 0xf1a9 A privacyguides.org A 198.98.54.105 OPT |

צופה יכול לשנות כל אחת מהחבילות הללו.

## מה זה "DNS מוצפן"?

Encrypted DNS can refer to one of a number of protocols, the most common ones being [DNSCrypt](#dnscrypt), [DNS over TLS](#dns-over-tls-dot), and [DNS over HTTPS](#dns-over-https-doh).

### DNSCrypt

[**DNSCrypt**](https://en.wikipedia.org/wiki/DNSCrypt) הייתה אחת השיטות הראשונות להצפנת שאילתות DNS. DNSCrypt פועל על יציאה 443 ועובד עם פרוטוקולי התחבורה TCP או UDP. DNSCrypt מעולם לא הוגש ל[כוח המשימה להנדסת אינטרנט (IETF)](https://en.wikipedia.org/wiki/Internet_Engineering_Task_Force) וגם לא עבר דרך [בקשה להערות (RFC)](https://en.wikipedia.org/wiki/Request_for_Comments), כך שלא נעשה בו שימוש נרחב מחוץ לכמה [יישומים](https://dnscrypt.info/implementations). כתוצאה מכך, הוא הוחלף במידה רבה על ידי [DNS על HTTPS](#dns-over-https-doh) הפופולרי יותר.

### DNS על TLS (DoT)

[**DNS over TLS**](https://en.wikipedia.org/wiki/DNS_over_TLS) היא שיטה נוספת להצפנת תקשורת DNS שהיא מוגדרת ב-[RFC 7858](https://datatracker.ietf.org/doc/html/rfc7858). Support was first implemented in Android 9, iOS 14, and on Linux in [systemd-resolved](https://freedesktop.org/software/systemd/man/resolved.conf.html#DNSOverTLS=) in version 237. Preference in the industry has been moving away from DoT to DoH in recent years, as DoT is a [complex protocol](https://dnscrypt.info/faq) and has varying compliance to the RFC across the implementations that exist. Dot פועלת גם על פורט ייעודי 853 שניתן לחסום בקלות על ידי חומות אש מגבילות.

### DNS דרך HTTPS (DoH)

[**DNS over HTTPS**](https://en.wikipedia.org/wiki/DNS_over_HTTPS), as defined in [RFC 8484](https://datatracker.ietf.org/doc/html/rfc8484), packages queries in the [HTTP/2](https://en.wikipedia.org/wiki/HTTP/2) protocol and provides security with HTTPS. תמיכה נוספה לראשונה בדפדפני אינטרנט כגון Firefox 60 ו-Chrome 83.

יישום מקורי של DoH הופיע ב-iOS 14, macOS 11, Microsoft Windows ו-אנדרואיד 13 (עם זאת, הוא לא יופעל [>כברירת מחדל](https://android-review.googlesource.com/c/platform/packages/modules/DnsResolver/+/1833144)). תמיכת שולחן העבודה הכללית של לינוקס ממתינה ל[יישום](https://github.com/systemd/systemd/issues/8639) של systemd כך ש[עדיין נדרשת התקנת תוכנת צד שלישי](../dns.md#encrypted-dns-proxies).

### תמיכה במערכת הפעלה מקומית

#### אנדרואיד

אנדרואיד 9 ומעלה תומכת ב-DNS דרך TLS. ניתן למצוא את ההגדרות ב: **הגדרות** &rarr; **רשת & אינטרנט** &rarr; **פרטי DNS**.

#### מוצרי Apple

הגרסאות האחרונות של iOS, iPadOS, tvOS ו-macOS, תומכות הן ב-DoT והן ב-DoH. שני הפרוטוקולים נתמכים באופן מקורי באמצעות [פרופילי תצורה](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) או דרך [ממשק API להגדרות DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

לאחר התקנה של פרופיל תצורה או אפליקציה המשתמשת ב-API של הגדרות DNS, ניתן לבחור את תצורת ה-DNS. אם VPN פעיל, הרזולוציה בתוך מנהרת ה-VPN תשתמש בהגדרות ה-DNS של ה-VPN ולא בהגדרות כלל המערכת שלך.

Apple אינה מספקת ממשק מקורי ליצירת פרופילי DNS מוצפנים. [יוצר פרופיל DNS מאובטח](https://dns.notjakob.com/tool.html) הוא כלי לא רשמי ליצירת פרופילי DNS מוצפנים משלך, אולם הם לא ייחתמו. פרופילים חתומים מועדפים; החתימה מאמתת את מקור הפרופיל ומסייעת להבטיח את שלמות הפרופילים. תווית "מאומת" ירוקה ניתנת לפרופילי תצורה חתומים. לקבלת מידע נוסף על חתימת קוד, ראה [אודות חתימת קוד](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).

#### לינוקס

`systemd-resolved`, which many Linux distributions use to do their DNS lookups, doesn't yet [support DoH](https://github.com/systemd/systemd/issues/8639). If you want to use DoH, you'll need to install a proxy like [dnscrypt-proxy](../dns.md#dnscrypt-proxy) and [configure it](https://wiki.archlinux.org/title/Dnscrypt-proxy) to take all the DNS queries from your system resolver and forward them over HTTPS.

## מה יכול גורם חיצוני לראות?

בדוגמה זו נתעד מה קורה כאשר אנו מבקשים בקשת DoH:

1. ראשית, התחל `tshark`:

    ```bash
    tshark -w /tmp/dns_doh.pcap -f "tcp port https and host 1.1.1.1"
    ```

2. שנית, הגש בקשה עם `curl`:

    ```bash
    curl -vI --doh-url https://1.1.1.1/dns-query https://privacyguides.org
    ```

3. לאחר הגשת הבקשה, נוכל לעצור את לכידת החבילות עם <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. נתח את התוצאות ב-Wireshark:

    ```bash
    wireshark -r /tmp/dns_doh.pcap
    ```

We can see the [connection establishment](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#Connection_establishment) and [TLS handshake](https://cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake) that occurs with any encrypted connection. כאשר מסתכלים על חבילות "האפליקציה" שלאחר מכן, אף אחת מהן לא מכילה את הדומיין שביקשנו או את כתובת ה-IP שהוחזרה.

## מדוע **אסור** לי להשתמש ב-DNS מוצפן?

במקומות שבהם קיים סינון (או צנזורה) באינטרנט, לביקור במשאבים אסורים עשויות להיות השלכות משלו, שכדאי לשקול ב[מודל האיומים](../basics/threat-modeling.md) שלך. אנו **לא** מציעים להשתמש ב-DNS מוצפן למטרה זו. Use [Tor](../advanced/tor-overview.md) or a [VPN](../vpn.md) instead. אם אתה משתמש ב-VPN, עליך להשתמש בשרתי ה-DNS של ה-VPN שלך. כשאתה משתמש ב-VPN, אתה כבר סומך עליהם בכל פעילות הרשת שלך.

כאשר אנו מבצעים חיפוש DNS, זה בדרך כלל בגלל שאנו רוצים לגשת למשאב. להלן, נדון בכמה מהשיטות שעלולות לחשוף את פעילויות הגלישה שלך גם בעת שימוש ב-DNS מוצפן:

### כתובת IP

הדרך הפשוטה ביותר לקבוע את פעילות הגלישה עשויה להיות להסתכל על כתובות ה-IP שהמכשירים שלך ניגשים אליהם. לדוגמה, אם הצופה יודע ש-`privacyguides.org` נמצא בכתובת `198.98.54.105`, והמכשיר שלך מבקש נתונים מ-`198.98.54.105`, יש יש סיכוי טוב שאתה מבקר בPrivacy Guides.

שיטה זו שימושית רק כאשר כתובת ה-IP שייכת לשרת המארח רק מעט אתרים. זה גם לא מאוד שימושי אם האתר מתארח בפלטפורמה משותפת (למשל Github Pages, Cloudflare Pages, Netlify, WordPress, Blogger וכו'). זה גם לא מאוד שימושי אם השרת מתארח מאחורי [פרוקסי הפוך](https://en.wikipedia.org/wiki/Reverse_proxy), הנפוץ מאוד באינטרנט המודרני.

### ציון שם השרת (SNI)

ציון שם שרת משמש בדרך כלל כאשר כתובת IP מארחת אתרים רבים. זה יכול להיות שירות כמו Cloudflare, או הגנה אחרת של [מניעת מניעת שירות](https://en.wikipedia.org/wiki/Denial-of-service_attack).

1. התחל לתעד שוב עם `tshark`. הוספנו מסנן עם כתובת ה-IP שלנו כדי שלא תלכוד הרבה מנות:

    ```bash
    tshark -w /tmp/pg.pcap port 443 and host 198.98.54.105
    ```

2. לאחר מכן נבקר בכתובת [https://privacyguides.org](https://privacyguides.org).

3. לאחר ביקור באתר, אנו רוצים לעצור את לכידת החבילה עם <kbd>CTRL</kbd> + <kbd>C</kbd>.

4. בשלב הבא אנו רוצים לנתח את התוצאות:

    ```bash
    wireshark -r /tmp/pg.pcap
    ```

    אנו נראה את יצירת החיבור, ולאחר מכן את לחיצת היד TLS עבור אתר מדריכי הפרטיות Privacy Guides. סביב מסגרת 5. אתה תראה "שלום לקוח ".

5. מרחיבים את המשולש &#9656; ליד כל שדה:

    ```text
    אבטחת שכבת▸ תחבורה
      ▸ TLSv1.3 שכבת שיא: פרוטוקול לחיצת יד: לקוח שלום
        פרוטוקול         ▸ לחיצת יד: לקוח שלום
          ▸ סיומת: server_name (len=22)
            סיומת סימון שם             ▸ שרת
    ```

6. אנו יכולים לראות את ערך SNI אשר חושף את האתר בו אנו מבקרים. הפקודה `tshark` יכולה לתת לך את הערך ישירות עבור כל החבילות המכילות ערך SNI:

    ```bash
    tshark -r /tmp/pg.pcap -Tfields -Y tls.handshake.extensions_server_name -e tls.handshake.extensions_server_name
    ```

משמעות הדבר היא שגם אם אנו משתמשים בשרתי "DNS מוצפן", הדומיין ככל הנראה ייחשף דרך SNI. The [TLS v1.3](https://en.wikipedia.org/wiki/Transport_Layer_Security#TLS_1.3) protocol brings with it [Encrypted Client Hello](https://blog.cloudflare.com/encrypted-client-hello), which prevents this kind of leak.

Governments, in particular [China](https://zdnet.com/article/china-is-now-blocking-all-encrypted-https-traffic-using-tls-1-3-and-esni) and [Russia](https://zdnet.com/article/russia-wants-to-ban-the-use-of-secure-protocols-such-as-tls-1-3-doh-dot-esni), have either already [started blocking](https://en.wikipedia.org/wiki/Server_Name_Indication#Encrypted_Client_Hello) it or expressed a desire to do so. לאחרונה רוסיה [החלה לחסום אתרים](https://github.com/net4people/bbs/issues/108) המשתמשים בתקן זה [HTTP/3](https://en.wikipedia.org/wiki/HTTP/3) סטנדרטי. הסיבה לכך היא ש [QUIC](https://en.wikipedia.org/wiki/QUIC) פרוטוקול המהווה חלק מ HTTP/3 דורש שגם `ClientHello` יהיה מוצפן.

### פרוטוקול סטטוס תעודה מקוון (OCSP)

דרך נוספת שהדפדפן שלך יכול לחשוף את פעילויות הגלישה שלך היא באמצעות [פרוטוקול מצב אישור מקוון](https://en.wikipedia.org/wiki/Online_Certificate_Status_Protocol). בעת ביקור באתר HTTPS, הדפדפן עשוי לבדוק אם [אישור](https://en.wikipedia.org/wiki/Public_key_certificate) של האתר בוטלה. זה נעשה בדרך כלל באמצעות פרוטוקול HTTP, כלומר הוא **לא** מוצפן.

בקשת ה-OCSP מכילה את האישור "[מספר סידורי](https://en.wikipedia.org/wiki/Public_key_certificate#Common_fields)", שהוא ייחודי. הוא נשלח ל"מגיב OCSP" על מנת לבדוק את מצבו.

אנו יכולים לדמות מה דפדפן יעשה באמצעות הפקודה [`openssl`](https://en.wikipedia.org/wiki/OpenSSL).

1. קבל את אישור השרת והשתמש ב-[`sed`](https://en.wikipedia.org/wiki/Sed) כדי לשמור רק על החלק החשוב ולכתוב אותו לקובץ:

    ```bash
    openssl s_client -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_server.cert
    ```

2. קבלו את תעודת הביניים. [רשויות אישורים (CA)](https://en.wikipedia.org/wiki/Certificate_authority) בדרך כלל אינן חותמות ישירות על אישור; הם משתמשים במה שמכונה תעודת "ביניים".

    ```bash
    openssl s_client -showcerts -connect privacyguides.org:443 < /dev/null 2>&1 |
        sed -n '/^-*BEGIN/,/^-*END/p' > /tmp/pg_and_intermediate.cert
    ```

3. האישור הראשון ב-`pg_and_intermediate.cert` הוא למעשה אישור השרת משלב 1. נוכל להשתמש שוב ב-`sed` כדי למחוק עד למופע הראשון של END:

    ```bash
    sed -n '/^-*END CERTIFICATE-*$/!d;:a n;p;ba' \
        /tmp/pg_and_intermediate.cert > /tmp/intermediate_chain.cert
    ```

4. קבל את מגיב OCSP עבור אישור השרת:

    ```bash
    openssl x509 -noout -ocsp_uri -in /tmp/pg_server.cert
    ```

    התעודה שלנו מציגה את מגיב האישורים של Let's Encrypt. אם אנחנו רוצים לראות את כל הפרטים של התעודה נוכל להשתמש ב:

    ```bash
    openssl x509 -text -noout -in /tmp/pg_server.cert
    ```

5. התחל את לכידת החבילה:

    ```bash
    tshark -w /tmp/pg_ocsp.pcap -f "tcp port http"
    ```

6. הגש את בקשת ה - OCSP:

    ```bash
    openssl ocsp -issuer /tmp/intermediate_chain.cert \
                 -cert /tmp/pg_server.cert \
                 -text \
                 -url http://r3.o.lencr.org
    ```

7. פתח את הלכידה:

    ```bash
    wireshark -r /tmp/pg_ocsp.pcap
    ```

    יהיו שתי חבילות עם פרוטוקול "OCSP": "בקשה" ו"תגובה". עבור ה"בקשה" נוכל לראות את ה"מספר הסידורי" על ידי הרחבת המשולש &#9656; ליד כל שדה:

    ```bash
    ▸ פרוטוקול מצב אישור מקוון
      ▸ tbsRequest
        ▸ requestList: 1 item
          ▸ Request
            ▸ reqCert
              serialNumber
    ```

    עבור ה"תגובה" נוכל לראות גם את ה"מספר הסידורי":

    ```bash
    פרוטוקול מצב אישור▸ מקוון
      ▸ responseBytes
        ▸ BasicOCSPResponse
          ▸ tbsResponseData
            ▸ תגובות: פריט 1
              ▸ SingleResponse
                ▸ certID
                  serialNumber
    ```

8. או השתמש ב-`tshark` כדי לסנן את החבילות עבור המספר הסידורי:

    ```bash
    tshark -r /tmp/pg_ocsp.pcap -Tfields -Y ocsp.serialNumber -e ocsp.serialNumber
    ```

אם למשקיף הרשת יש את האישור הציבורי, הזמין לציבור, הוא יכול להתאים את המספר הסידורי לאישור הזה ולכן לקבוע את האתר שבו אתה מבקר. התהליך יכול להיות אוטומטי ויכול לשייך כתובות IP למספרים סידוריים. אפשר גם לבדוק ביומני [שקיפות אישורים](https://en.wikipedia.org/wiki/Certificate_Transparency) עבור המספר הסידורי.

## האם להשתמש ב - DNS מוצפן?

הכנו את תרשים הזרימה הזה כדי לתאר מתי *כדאי* להשתמש ב-DNS מוצפן:

``` mermaid
graph TB
    התחל[התחל] --> אנונימי{מנסה להיות<br> אנונימי?}
    אנונימי--> | כן | tor(השתמש בTor)
     אנונימי --> | לא | צנזורה{הימנעות<br> מצנזורה?}
    צנזורה --> | כן | vpnאוTor(השתמש ב- <br> VPN או Tor)
     צנזורה --> | לא | פרטיות{רוצה פרטיות<br> מ-ISP?}
    פרטיות --> | כן | vpnאוTor
    פרטיות --> | לא | מעצבן{ISP מייצרת<br> הפניות<br> מעצבנות?}
    מעצבן --> | כן | מוצפןDNS(השתמש ב<br> מוצפן DNS<br> עם צד שלישי)
    מעצבן --> | לא | ispDNS{האם ISP תומך ב<br> מוצפן DNS?}
    ispDNS --> | כן | השתמשISP(השתמש<br> מוצפן DNS<br> עם ISP)
    ispDNS --> | לא | כלום(לא לעשות כלום)
```

יש להשתמש ב-DNS מוצפן עם צד שלישי רק כדי לעקוף הפניות מחדש ו[חסימת DNS](https://en.wikipedia.org/wiki/DNS_blocking) בסיסית כאשר אתה יכול להיות בטוח שלא יהיו השלכות או שאתה מעוניין בספק שיבצע סינון ראשוני.

[רשימת שרתי DNS מומלצים](../dns.md ""){.md-button}

## מהו DNSSEC?

[תוספי אבטחת מערכת שמות דומיין](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) (DNSSEC) היא תכונה של DNS המאמתת תגובות לחיפושי שמות דומיין. הוא אינו מספק הגנת פרטיות לאותם חיפושים, אלא מונע מתוקפים לתמרן או להרעיל את התגובות לבקשות DNS.

במילים אחרות, DNSSEC חותם נתונים דיגיטליים כדי להבטיח את תקפותם. על מנת להבטיח חיפוש מאובטח, החתימה מתרחשת בכל רמה בתהליך חיפוש ה-DNS. כתוצאה מכך, ניתן לסמוך על כל התשובות מה-DNS.

תהליך החתימה של DNSSEC דומה למישהו שחתום על מסמך משפטי בעט; אותו אדם חותם בחתימה ייחודית שאף אחד אחר לא יכול ליצור, ומומחה בית המשפט יכול להסתכל על החתימה הזו ולוודא שהמסמך נחתם על ידי אותו אדם. חתימות דיגיטליות אלו מבטיחות שלא בוצע שיבוש בנתונים.

DNSSEC מיישמת מדיניות חתימה דיגיטלית היררכית בכל שכבות ה-DNS. לדוגמה, במקרה של חיפוש `privacyguides.org`, שרת DNS שורש יחתום על מפתח עבור שרת השמות `.org` ו-`.org` nameserver יחתום על מפתח עבור שרת השמות הסמכותי של `privacyguides.org`.

<small>Adapted from [DNS Security Extensions (DNSSEC) overview](https://cloud.google.com/dns/docs/dnssec) by Google and [DNSSEC: An Introduction](https://blog.cloudflare.com/dnssec-an-introduction) by Cloudflare, both licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).</small>

## מהו מזעור QName?

A QNAME is a "qualified name", for example `discuss.privacyguides.net`. בעבר, בעת פתרון שם דומיין, פותר ה-DNS שלך היה מבקש מכל שרת בשרשרת לספק כל מידע שיש לו על השאילתה המלאה שלך. In this example below, your request to find the IP address for `discuss.privacyguides.net` gets asked of every DNS server provider:

| Server                 | שאלה שנשאלה                                 | Response                                    |
| ---------------------- | ------------------------------------------- | ------------------------------------------- |
| Root server            | What's the IP of discuss.privacyguides.net? | I don't know, ask .net's server...          |
| .net's server          | What's the IP of discuss.privacyguides.net? | I don't know, ask Privacy Guides' server... |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net? | 5.161.195.190!                              |

With "QNAME minimization," your DNS resolver now only asks for just enough information to find the next server in the chain. In this example, the root server is only asked for enough information to find the appropriate nameserver for the .net TLD, and so on, without ever knowing the full domain you're trying to visit:

| Server                 | שאלה שנשאלה                                          | Response                          |
| ---------------------- | ---------------------------------------------------- | --------------------------------- |
| Root server            | What's the nameserver for .net?                      | *Provides .net's server*          |
| .net's server          | What's the nameserver for privacyguides.net?         | *Provides Privacy Guides' server* |
| Privacy Guides' server | What's the nameserver for discuss.privacyguides.net? | השרת הזה!                         |
| Privacy Guides' server | What's the IP of discuss.privacyguides.net?          | 5.161.195.190                     |

While this process can be slightly more inefficient, in this example neither the central root nameservers nor the TLD's nameservers ever receive information about your *full* query, thus reducing the amount of information being transmitted about your browsing habits. תיאור טכני נוסף מוגדר ב [RFC 7816](https://datatracker.ietf.org/doc/html/rfc7816).

## מהי רשת משנה של לקוח EDNS (ECS)?

[רשת המשנה של לקוח EDNS](https://en.wikipedia.org/wiki/EDNS_Client_Subnet) היא שיטה לפותר DNS רקורסיבי לציון [רשת משנה](https://en.wikipedia.org/wiki/Subnetwork) עבור [המארח או הלקוח](https://en.wikipedia.org/wiki/Client_(computing)) שמבצע את שאילתת ה-DNS.

זה נועד "לזרז" את מסירת הנתונים על ידי מתן תשובה ללקוח השייך לשרת הקרוב אליו כגון [תוכן רשת מסירה](https://en.wikipedia.org/wiki/Content_delivery_network), המשמשות לעתים קרובות בהזרמת וידאו והגשת יישומי אינטרנט של JavaScript.

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
