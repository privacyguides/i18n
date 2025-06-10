---
meta_title: "Consigli e confronto sui servizi VPN privati, senza sponsor o pubblicità - Privacy Guides"
title: "Servizi VPN"
icon: material/vpn
description: The best VPN services for protecting your privacy and security online. Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">Le VPN non forniscono l'anonimato</p>

L'utilizzo di una VPN **non** manterrà anonime le tue abitudini di navigazione, né aggiungerà ulteriore sicurezza al traffico non sicuro (HTTP).

Se cerchi l'**anonimato**, dovresti usare Tor Browser. Se stai cercando maggiore **sicurezza**, dovresti sempre assicurarti di connetterti a siti web che utilizzano HTTPS. Una VPN non sostituisce le buone pratiche di sicurezza.

[Scarica Tor](https://torproject.org){ .md-button .md-button--primary } [Miti e FAQ di Tor](advanced/tor-overview.md){ .md-button }

</div>

[Panoramica dettagliata sulle VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fornitori consigliati

I nostri provider consigliati utilizzano la crittografia, supportano WireGuard & OpenVPN e hanno una politica no-log. Leggi il nostro \[elenco completo di criteri\](#criteri) per ulteriori informazioni.

| Provider              | Paesi | WireGuard                     | Port Forwarding                                        | IPv6                                                       | Pagamenti anonimi |
| --------------------- | ----- | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- | ----------------- |
| [Proton](#proton-vpn) | 112+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support | Contanti          |
| [IVPN](#ivpn)         | 37+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Solo in uscita  | Monero, contanti  |
| [Mullvad](#mullvad)   | 49+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                              | Monero, contanti  |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo di Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** è un forte concorrente nel settore delle VPN, ed è operativo dal 2016. Proton AG ha sede in Svizzera e offre un livello gratuito limitato, così come un'opzione premium più ricca di funzioni.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Countries

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2024-08-06

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

A gennaio 2020, Proton VPN è stato sottoposto a un controllo indipendente da SEC Consult. SEC Consult ha trovato alcune vulnerabilità di rischio basso e medio nelle applicazioni Windows, Android e iOS di Proton VPN, tutti "corretti adeguatamente" da Proton VPN prima della pubblicazione dei rapporti. Nessuno dei problemi identificati avrebbe fornito a un malintenzionato l'accesso remoto al tuo dispositivo o traffico. Puoi visualizzare i rapporti singoli per ogni piattaforma su [protonvpn.com](https://protonvpn.com/blog/open-source). Nell'aprile del 2022 Proton VPN è stata sottoposta ad [un altro controllo](https://protonvpn.com/blog/no-logs-audit). Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le app di Proton VPN, il 9 novembre 2021, da [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Client Open Source

Proton VPN fornisce il codice sorgente per i propri client desktop e mobile, nella loro [organizzazione di GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accetta contanti

Proton VPN, oltre ad accettare carte di credito/debito, PayPal e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), accetta anche **contanti/valuta locale** come forma anonima di pagamento.

#### :material-check:{ .pg-green } Supporto WireGuard

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

Proton VPN [consiglia](https://protonvpn.com/blog/wireguard) l'uso di WireGuard con il loro servizio. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Port Forwarding Remoto

Al momento, Proton VPN supporta soltanto il [port forwarding](https://protonvpn.com/support/port-forwarding) remoto effimero, tramite NAT-PMP, con 60 secondi di tempo di noleggio. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Le applicazioni torrent supportano spesso NAT-PMP in modo nativo.

#### :material-information-outline:{ .pg-blue } Anti-censura

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth incapsula il tunnel VPN in una sessione TLS, in modo da sembrare traffico Internet generico.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Client Mobile

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Note aggiuntive

Proton VPN clients support two-factor authentication on all platforms. Proton VPN ha i propri server e datacenter in Svizzera, Islanda e Svezia. Offrono il blocco dei contenuti e il blocco di malware noti con il loro servizio DNS. Inoltre, Proton VPN offre anche server "Tor" che ti consentono di connetterti facilmente ai siti onion, ma consigliamo comunque di utilizzare [il Tor Browser ufficiale](tor.md#tor-browser) per questo scopo.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. Se necessiti di questa funzionalità e stai utilizzando un Mac con chipset Intel, dovresti considerare l'utilizzo di un altro servizio VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo di IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** è un altro fornitore di VPN premium, in operazione dal 2009. IVPN ha sede a Gibilterra e non offre una prova gratuita.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Paesi

IVPN ha [server in 37 paesi](https://ivpn.net/status).(1) Scegliere un fornitore VPN con un server più vicino a te ridurrà la latenza del traffico di rete che invii. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2024-08-06

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Client Open Source

A partire da febbraio 2020 le [applicazioni IVPN sono open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Il codice sorgente è ottenibile dalla loro [organizzazione di GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accetta contanti e Monero

Oltre ad accettare carte di credito/debito e PayPal, IVPN accetta Bitcoin, **Monero** e **contanti/valuta locale** (sui piani annuali) come forme anonime di pagamento. Sono [disponibili anche](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) carte prepagate con codici da riscattare.

#### :material-check:{ .pg-green } Supporto WireGuard

IVPN supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

IVPN [consiglia](https://ivpn.net/wireguard) l'utilizzo di WireGuard con il loro servizio e, pertanto, il protocollo è il predefinito su tutte le app di IVPN. Inoltre, IVPN offre anche un generatore di configurazione di WireGuard da utilizzare con le [app](https://wireguard.com/install) ufficiali di WireGuard.

#### :material-information-outline:{ .pg-blue } Supporto IPv6

IVPN consente di [connettersi a servizi che utilizzano il protocollo IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), ma non permette di connettersi da un dispositivo che utilizza un indirizzo IPv6.

#### :material-alert-outline:{ .pg-orange } Port Forwarding remoto

IVPN in precedenza supportava il port forwarding, ma ha rimosso l'opzione a [giugno 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-censura

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Dispone di due modalità in cui può utilizzare [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) su connessioni QUIC o TCP. QUIC è un protocollo moderno con un migliore controllo della congestione e quindi può essere più veloce con una latenza ridotta. La modalità TCP fa apparire i dati come normale traffico HTTP.

#### :material-check:{ .pg-green } Client Mobile

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Note aggiuntive

IVPN clients support two-factor authentication. Inoltre, IVPN fornisce la funzionaalità "[AntiTracker](https://ivpn.net/antitracker)", che blocca le reti e tracker pubblicitari dal livello della rete.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo di Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** è una VPN veloce ed economica con una grande attenzione alla trasparenza e alla sicurezza. They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Last checked: 2025-03-10

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN se utilizzano [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } Client Open Source

Mullvad fornisce il codice sorgente per i propri client desktop e mobili nella loro [organizzazione di GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accetta contanti e Monero

Mullvad, oltre ad accettare carte di credito/debito e PayPal, accetta Bitcoin, Bitcoin Cash, **Monero** e **contanti/valuta locale** come forme di pagamento anonimo. Sono disponibili anche carte prepagate con codici da riscattare. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } Supporto WireGuard

Mullvad supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

Mullvad [consiglia](https://mullvad.net/en/help/why-wireguard) l'utilizzo di WireGuard con il proprio servizio. È il protocollo predefinito o l'unico sulle app Mullvad per Android, iOS, macOS e Linux, ma su Windows è necessario [abilitare manualmente](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Inoltre, Mullvad offre un generatore di configurazione di WireGuard da utilizzare con le [app](https://wireguard.com/install) ufficiali di WireGuard.

#### :material-check:{ .pg-green } Supporto IPv6

Mullvad consente di [accedere ai servizi ospitati su IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) e di connettersi da un dispositivo che utilizza un indirizzo IPv6.

#### :material-alert-outline:{ .pg-orange } Port Forwarding Remoto

Mullvad supportava in precedenza il port forwarding, ma ha rimosso questa opzione nel [maggio 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-censura

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Client mobile

Mullvad ha pubblicato i client [App Store](https://apps.apple.com/app/id1488466513) e [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), che supportano entrambi un'interfaccia facile da usare, invece di richiedere la configurazione manuale della connessione WireGuard. Il client Android è disponibile anche su [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Note aggiuntive

Mullvad è molto trasparente su quali nodi [possiede o fitta](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Criteri

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

È importante notare che l'utilizzo di una VPN non ti rende anonimo, ma può migliorare la tua privacy in alcune situazioni. Una VPN non è uno strumento per attività illegali. Non affidarti ad una politica "no log".

</div>

**Si prega di notare che non siamo affiliati a nessuno dei fornitori che raccomandiamo. Ciò ci consente di fornire consigli completamente oggettivi.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una chiara serie di requisiti per qualsiasi fornitore di VPN che desideri essere consiglito, inclusi crittografia forte, controlli di sicurezza indipendenti, tecnologia moderna e altro. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere un fornitore VPN e di condurre la tua ricerca per assicurarsi che il fornitore VPN che scegli sia il più affidabile possibile.

### Tecnologia

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Requisiti minimi:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- Se vengono forniti client VPN, devono essere [open source](https://en.wikipedia.org/wiki/Open_source), come il software VPN che generalmente hanno incorporato. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**Caso migliore:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Client VPN facili da usare
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. Ci aspettiamo che i server accettino connessioni in arrivo via IPv6 e che ti permettano di accedere a servizi su indirizzi IPv6.
- La capacità di [port forwarding remoto](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) assiste nel creare connessioni, utilizzando software di condivisione di file P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) od ospitando un server (es. Mumble).
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### Privacy

Preferiamo che i provider da noi consigliati raccolgano il minor numero di dati possibile. È necessario non raccogliere informazioni personali al momento della registrazione e accettare forme di pagamento anonime.

**Requisiti minimi:**

- [Criptovaluta anonima](cryptocurrency.md) **od** opzione di pagamento in contanti.
- Nessuna informazione personale richiesta per registrarsi: solo nome utente, password ed e-mail al massimo.

**Caso migliore:**

- Accetta più [opzioni di pagamento anonime](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Sicurezza

Una VPN è inutile se non è nemmeno in grado di fornire una sicurezza adeguata. We require all our recommended providers to abide by current security standards. L'ideale sarebbe utilizzare schemi di crittografia a prova di futuro per impostazione predefinita. Richiediamo inoltre che una terza parte indipendente verifichi la sicurezza del fornitore, idealmente in modo molto completo e su base ripetuta (annuale).

**Requisiti minimi:**

- Schemi di crittografia forti: OpenVPN con autenticazione SHA-256; handshake RSA-2048 o migliore; crittografia dei dati AES-256-GCM o AES-256-CBC.
- Segretezza in Avanti.
- Controlli di sicurezza pubblicati da uno studio di terze parti affidabile.
- VPN servers that use full-disk encryption or are RAM-only.

**Caso migliore:**

- Crittografia più forte: RSA-4096.
- Optional quantum-resistant encryption.
- Segretezza in Avanti.
- Controlli di sicurezza pubblicati e completi, da uno studio di terze parti affidabile.
- Programmi di bug-bounty e/o un processo coordinato di divulgazione delle vulnerabilità.
- RAM-only VPN servers.

### Fiducia

Non affideresti le tue finanze a qualcuno con un'identità falsa, quindi perché dovresti affidargli i tuoi dati internet? Richiediamo che i fornitori da noi consigliati rendano pubbliche la propria dirigenza o proprietà. Inoltre, vorremmo vedere rapporti di trasparenza frequenti, specialmente relativi alla gestione delle richieste del governo.

**Requisiti minimi:**

- Dirigenza o proprietà pubblica.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**Caso migliore:**

- Dirigenza pubblica.
- Rapporti di trasparenza frequenti.

### Marketing

Con i fornitori VPN che consigliamo, vorremmo vedere del marketing responsabile.

**Requisiti minimi:**

- Must self-host analytics (i.e., no Google Analytics).

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

Anche se non requisiti rigidi, ci sono alcuni fattori che abbiamo considerato nel determinare quali servizi consigliare. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
