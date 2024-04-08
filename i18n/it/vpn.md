---
meta_title: "Consigli e confronto sui servizi VPN privati, senza sponsor o pubblicità - Privacy Guides"
title: "Servizi VPN"
icon: material/vpn
description: Questi sono i migliori servizi VPN per proteggere la tua privacy e sicurezza online. Trova qui un fornitore che non ti spii.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->

If you're looking for additional **privacy** from your ISP, on a public Wi-Fi network, or while torrenting files, a VPN may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. Una VPN non è un sostituto per buone pratiche di sicurezza.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Panoramica dettagliata sulle VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fornitori consigliati

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Leggi il nostro \[elenco completo di criteri\](#criteri) per ulteriori informazioni.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 91+       | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Contanti           |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo di Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** è un forte concorrente nel settore delle VPN, ed è operativo dal 2016. Proton AG ha sede in Svizzera e offre un livello gratuito limitato, così come un'opzione premium più ricca di funzioni.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Countries

Proton VPN has [servers in 91 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2024-04-02

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

A gennaio 2020, Proton VPN è stato sottoposto a un controllo indipendente da SEC Consult. SEC Consult ha trovato alcune vulnerabilità di rischio basso e medio nelle applicazioni Windows, Android e iOS di Proton VPN, tutti "corretti adeguatamente" da Proton VPN prima della pubblicazione dei rapporti. Nessuno dei problemi identificati avrebbe fornito a un malintenzionato l'accesso remoto al tuo dispositivo o traffico. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit) and the report was [produced by Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le app di Proton VPN, il 9 novembre 2021, da [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Client Open Source

Proton VPN fornisce il codice sorgente per i propri client desktop e mobile, nella loro [organizzazione di GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accetta contanti

Proton VPN, oltre ad accettare carte di credito/debito, PayPal e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), accetta anche **contanti/valuta locale** come forma anonima di pagamento.

#### :material-check:{ .pg-green } Supporto WireGuard

Proton VPN supporta principalmente il protocollo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Inoltre, WireGuard mira ad essere più semplice e performante.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Le applicazioni torrent supportano spesso NAT-PMP in modo nativo.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth incapsula il tunnel VPN in una sessione TLS, in modo da sembrare traffico Internet generico.

Purtroppo non funziona molto bene nei Paesi in cui vengono impiegati filtri sofisticati che analizzano tutto il traffico in uscita nel tentativo di scoprire i tunnel criptati. Stealth non è ancora disponibile su [Windows](https://github.com/ProtonVPN/win-app/issues/64) o Linux.

#### :material-check:{ .pg-green } Client Mobile

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-alert-outline:{ .pg-orange } Additional Notes

I client di ProtonVPN supportano l'autenticazione a due fattori su tutte le piattaforme, tranne Linux, al momento. Proton VPN ha i propri server e datacenter in Svizzera, Islanda e Svezia. Offrono il blocco dei contenuti e il blocco di malware noti con il loro servizio DNS. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](https://torproject.org) for this purpose.

##### :material-alert-outline:{ .pg-orange } La funzione Killswitch non funziona sui Mac basati su Intel

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Se necessiti di questa funzionalità e stai utilizzando un Mac con chipset Intel, dovresti considerare l'utilizzo di un altro servizio VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo di IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** è un altro fornitore di VPN premium, in operazione dal 2009. IVPN ha sede in Gibilterra.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Paesi

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2024-04-02

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

IVPN è stata sottoposta a un [controllo di non registrazione da Cure53](https://cure53.de/audit-report_ivpn.pdf), che si è concluso in accordo con la dichiarazione di non registrazione di IVPN. Inoltre, IVPN ha completato un [rapporto di cinque test completi di Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) a gennaio 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Client Open Source

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Il codice sorgente è ottenibile dalla loro [organizzazione di GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accetta contanti e Monero

Oltre ad accettare carte di credito/debito e PayPal, IVPN accetta Bitcoin, **Monero** e **contanti/valuta locale** (sui piani annuali) come forme anonime di pagamento.

#### :material-check:{ .pg-green } Supporto WireGuard

IVPN supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Inoltre, WireGuard mira ad essere più semplice e performante.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://www.ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Port Forwarding remoto

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Dispone di due modalità in cui può utilizzare [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) su connessioni QUIC o TCP. QUIC è un protocollo moderno con un migliore controllo della congestione e quindi può essere più veloce con una latenza ridotta. La modalità TCP fa apparire i dati come normale traffico HTTP.

#### :material-check:{ .pg-green } Client Mobile

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

I client IVPN supportano l'autenticazione a due fattori (i client Mullvad no). IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo di Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** è una VPN veloce ed economica con una grande attenzione alla trasparenza e alla sicurezza. Sono operativi dal **2009**. Mullvad ha sede in Svezia e non dispone di una prova gratuita.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

Mullvad has [servers in 41 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2024-04-02

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN se utilizzano [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

I client VPN di Mullvad sono stati controllati da Cure53 e Assured AB in un rapporto da cinque test, [pubblicato su cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). I ricercatori della sicurezza hanno dichiarato:

> Cure53 e Assured AB sono soddisfatti dai risultati del controllo e, il software, lascia un'impressione complessiva positiva. Con la dedizione alla sicurezza del team interno al complesso Mullvad VPN, i tester non hanno dubbi riguardo alla giusta direzione del progetto da un punto di vista della sicurezza.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> I risultati di questo progetto di maggio-giugno 2020, rivolto al complesso di Mullvad, sono abbastanza positivi. [...] L'ecosistema applicativo complessivo utilizzato da Mullvad lascia un'impressione solida e strutturata. La struttura generale dell'applicazione semplifica l'introduzione di patch e correzioni, in un modo strutturato. Più di ogni altra cosa, i risultati individuati da Cure53 rivelano l'importanza di controllare e rivalutare costantemente i vettori di fuga di notizie attuali, per poter sempre assicurare la privacy degli utenti finali. Detto questo, Mullvad fa un ottimo lavoro nel proteggere l'utente finale dalle comuni perdite di informazioni d'identificazione personale e i relativi rischi legati alla privacy.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Client Open Source

Mullvad fornisce il codice sorgente per i propri client desktop e mobili nella loro [organizzazione di GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accetta contanti e Monero

Mullvad, oltre ad accettare carte di credito/debito e PayPal, accetta Bitcoin, Bitcoin Cash, **Monero** e **contanti/valuta locale** come forme anonime di pagamento. Accettano inoltre Swish e bonifici bancari.

#### :material-check:{ .pg-green } Supporto WireGuard

Mullvad supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Inoltre, WireGuard mira ad essere più semplice e performante.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Supporto IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Port Forwarding Remoto

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad ha una modalità di offuscamento che utilizza [Shadowsocks con v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) che può essere utile in situazioni in cui protocolli VPN come OpenVPN o Wireguard sono bloccati.

#### :material-check:{ .pg-green } Client mobile

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. Il client Android è disponibile anche su [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Presumibilmente, la [Cina deve utilizzare un metodo diverso per bloccare i server ShadowSocks](https://github.com/net4people/bbs/issues/22). Il sito web di Mullvad è accessibile anche tramite Tor presso [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Criteri

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

È importante notare che l'utilizzo di una VPN non ti rende anonimo, ma può migliorare la tua privacy in alcune situazioni. Una VPN non è uno strumento per attività illegali. Non affidarti ad una politica "no log".

</div>

**Si prega di notare che non siamo affiliati a nessuno dei fornitori che raccomandiamo. Ciò ci consente di fornire consigli completamente oggettivi.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una chiara serie di requisiti per qualsiasi fornitore di VPN che desideri essere consiglito, inclusi crittografia forte, controlli di sicurezza indipendenti, tecnologia moderna e altro. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere un fornitore VPN e di condurre la tua ricerca per assicurarsi che il fornitore VPN che scegli sia il più affidabile possibile.

### Tecnologia

Richiediamo a tutti i nostri fornitori di VPN consigliati di fornire i file di configurazione di OpenVPN, da utilizzare su qualsiasi client. **Se** una VPN fornisce il proprio client personalizzato, richiediamo un'Interruttore d'Emergenza per bloccare le fughe di dati della rete, quando disconnessa.

**Requisiti minimi:**

- Supporto per protocolli forti come WireGuard & OpenVPN.
- Killswitch integrato nei client.
- Supporto multihop. Il multihopping è importante per mantenere i dati privati nel caso in cui un nodo venisse compromesso.
- Se vengono forniti client VPN, devono essere [open source](https://en.wikipedia.org/wiki/Open_source), come il software VPN che generalmente hanno incorporato. Crediamo che la disponibilità del [codice sorgente](https://en.wikipedia.org/wiki/Source_code) fornisca maggiore trasparenza su ciò che il dispositivo sta effettivamente facendo.

**Caso migliore:**

- Supporto per WireGuard e OpenVPN.
- Interruttore d'Emergenza con opzioni altamente configurabili (abilitare/disabilitare su certe reti, all'avvio, etc.)
- Client VPN facili da usare
- Supporto per [IPv6](https://en.wikipedia.org/wiki/IPv6). Ci aspettiamo che i server accettino connessioni in arrivo via IPv6 e che ti permettano di accedere a servizi su indirizzi IPv6.
- La capacità di [port forwarding remoto](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) assiste nel creare connessioni, utilizzando software di condivisione di file P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) od ospitando un server (es. Mumble).
- Tecnologia di offuscamento che riempe i pacchetti di dati con dati casuali per aggirare la censura di Internet.

### Privacy

Preferiamo che i provider da noi consigliati raccolgano il minor numero di dati possibile. È necessario non raccogliere informazioni personali al momento della registrazione e accettare forme di pagamento anonime.

**Requisiti minimi:**

- [Criptovaluta anonima](cryptocurrency.md) **od** opzione di pagamento in contanti.
- Nessuna informazione personale richiesta per registrarsi: solo nome utente, password ed e-mail al massimo.

**Caso migliore:**

- Accetta più [opzioni di pagamento anonime](advanced/payments.md).
- Non sono accettate le informazioni personali (nome utente generato automaticamente, nessun'email necessaria, etc.).

### Sicurezza

Una VPN è inutile se non è nemmeno in grado di fornire una sicurezza adeguata. Richiediamo a tutti i nostri provider consigliati di rispettare gli standard di sicurezza attuali per le loro connessioni di OpenVPN. L'ideale sarebbe utilizzare schemi di crittografia a prova di futuro per impostazione predefinita. Richiediamo inoltre che una terza parte indipendente verifichi la sicurezza del fornitore, idealmente in modo molto completo e su base ripetuta (annuale).

**Requisiti minimi:**

- Schemi di crittografia forti: OpenVPN con autenticazione SHA-256; handshake RSA-2048 o migliore; crittografia dei dati AES-256-GCM o AES-256-CBC.
- Segretezza in Avanti.
- Controlli di sicurezza pubblicati da uno studio di terze parti affidabile.

**Caso migliore:**

- Crittografia più forte: RSA-4096.
- Segretezza in Avanti.
- Controlli di sicurezza pubblicati e completi, da uno studio di terze parti affidabile.
- Programmi di bug-bounty e/o un processo coordinato di divulgazione delle vulnerabilità.

### Fiducia

Non affideresti le tue finanze a qualcuno con un'identità falsa, quindi perché dovresti affidargli i tuoi dati internet? Richiediamo che i fornitori da noi consigliati rendano pubbliche la propria dirigenza o proprietà. Inoltre, vorremmo vedere rapporti di trasparenza frequenti, specialmente relativi alla gestione delle richieste del governo.

**Requisiti minimi:**

- Dirigenza o proprietà pubblica.

**Caso migliore:**

- Dirigenza pubblica.
- Rapporti di trasparenza frequenti.

### Marketing

Con i fornitori VPN che consigliamo, vorremmo vedere del marketing responsabile.

**Requisiti minimi:**

- Deve ospitare autonomamente i dati analitici (cioè, senza Google Analytics). Il sito del fornitore deve inoltre conformarsi con [DNT (Non Tracciare](https://en.wikipedia.org/wiki/Do_Not_Track), per le persone che desiderano rinunciare.

Non deve avere alcun marketing irresponsabile:

- Garantire al 100% la protezione dell'anonimato. Quando qualcuno afferma che qualcosa è al 100%, significa che non vi è certezza di fallimento. Sappiamo che le persone possono deanonimizzarsi facilmente in vari modi, ad es.:
    - Riutilizzo di informazioni personali, es. (profili email, pseudonimi univoci, etc.), accessibili senza software di anonimato (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Sostenere che una VPN a circuito singolo sia "più anonima" di Tor, che è un circuito di tre o più salti, che cambiano regolarmente.
- Utilizzare linguaggio responsabile: per esempio, è accettabile dire che la VPN è "disconnessa" o "non connessa", tuttavia affermare che un utente è "esposto", "vulnerabile" o "compromesso" può creare allarmismi incorretti e inutili. Ad esempio, quella persona potrebbe semplicemente scegliere un altro servizio VPN o utilizzare Tor.

**Caso migliore:**

Il marketing responsabile, che è sia educativo che utile per il consumatore, potrebbe includere:

- Un confronto accurato con quando si dovrebbe usare [Tor](tor.md).
- Disponibilità del sito web del provider VPN su un [servizio .onion](https://en.wikipedia.org/wiki/.onion)

### Funzionalità aggiuntive

Anche se non requisiti rigidi, ci sono alcuni fattori che abbiamo considerato nel determinare quali servizi consigliare. Questi includono funzionalità di blocco dei contenuti, warrant canaries, connessioni multihop, eccellente supporto clienti, il numero di connessioni simultanee consentite, ecc.
