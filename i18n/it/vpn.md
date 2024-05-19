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

Se stai cercando ulteriore **privacy** dal tuo ISP, su una rete Wi-Fi pubblica, o mentre fai torrenting di file, una VPN può essere la soluzione per te.

<div class="admonition danger" markdown>
<p class="admonition-title">Le VPN non forniscono l'anonimato</p>

L'utilizzo di una VPN **non** manterrà anonime le tue abitudini di navigazione, né aggiungerà ulteriore sicurezza al traffico non sicuro (HTTP).

Se cerchi l'**anonimato**, dovresti usare Tor Browser. Se stai cercando maggiore **sicurezza**, dovresti sempre assicurarti di connetterti a siti web che utilizzano HTTPS. Una VPN non sostituisce le buone pratiche di sicurezza.

[Scarica Tor](https://torproject.org){ .md-button .md-button--primary } [Miti e FAQ di Tor](advanced/tor-overview.md){ .md-button }

</div>

[Panoramica dettagliata sulle VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fornitori consigliati

I nostri provider consigliati utilizzano la crittografia, supportano WireGuard & OpenVPN e hanno una politica no-log. Leggi il nostro \[elenco completo di criteri\](#criteri) per ulteriori informazioni.

| Provider              | Paesi | WireGuard                     | Port Forwarding                                              | IPv6                                                      | Pagamenti anonimi |
| --------------------- | ----- | ----------------------------- | ------------------------------------------------------------ | --------------------------------------------------------- | ----------------- |
| [Proton](#proton-vpn) | 91+   | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Supporto parziale | :material-alert-outline:{ .pg-orange }                    | Contanti          |
| [IVPN](#ivpn)         | 37+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                       | :material-information-outline:{ .pg-blue } Solo in uscita | Monero, contanti  |
| [Mullvad](#mullvad)   | 41+   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                       | :material-check:{ .pg-green }                             | Monero, contanti  |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logo di Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** è un forte concorrente nel settore delle VPN, ed è operativo dal 2016. Proton AG ha sede in Svizzera e offre un livello gratuito limitato, così come un'opzione premium più ricca di funzioni.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 Paesi

Proton VPN ha [server in 91 Paesi](https://protonvpn.com/vpn-servers) o [5](https://protonvpn.com/support/how-to-create-free-vpn-account) se si utilizza il [piano gratuito](https://protonvpn.com/free-vpn/server).(1) Scegliere un provider VPN con un server più vicino a te ridurrà la latenza del traffico di rete inviato. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Ultimo controllo: 02-04-2024

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

A gennaio 2020, Proton VPN è stato sottoposto a un controllo indipendente da SEC Consult. SEC Consult ha trovato alcune vulnerabilità di rischio basso e medio nelle applicazioni Windows, Android e iOS di Proton VPN, tutti "corretti adeguatamente" da Proton VPN prima della pubblicazione dei rapporti. Nessuno dei problemi identificati avrebbe fornito a un malintenzionato l'accesso remoto al tuo dispositivo o traffico. Puoi visualizzare i rapporti singoli per ogni piattaforma su [protonvpn.com](https://protonvpn.com/blog/open-source). Nell'aprile 2022 Proton VPN è stata sottoposta a [un altro audit](https://protonvpn.com/blog/no-logs-audit) e il rapporto è stato [redatto da Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le app di Proton VPN, il 9 novembre 2021, da [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Client Open Source

Proton VPN fornisce il codice sorgente per i propri client desktop e mobile, nella loro [organizzazione di GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accetta contanti

Proton VPN, oltre ad accettare carte di credito/debito, PayPal e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), accetta anche **contanti/valuta locale** come forma anonima di pagamento.

#### :material-check:{ .pg-green } Supporto WireGuard

Proton VPN supporta principalmente il protocollo WireGuard®. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

Proton VPN [consiglia](https://protonvpn.com/blog/wireguard) l'uso di WireGuard con il loro servizio. Sulle app per Windows, macOS, iOS, Android, ChromeOS e Android TV di Proton VPN, WireGuard è il protocollo predefinito; tuttavia, il [supporto](https://protonvpn.com/support/how-to-change-vpn-protocols) per il protocollo non è presente nella loro app per Linux.

#### :material-alert-outline:{ .pg-orange } Nessun supporto IPv6

I server di Proton VPN sono compatibili solo con il protocollo IPv4. Le applicazioni di Proton VPN bloccheranno tutto il traffico IPv6 in uscita, quindi non dovrai preoccuparti che il tuo indirizzo IPv6 venga divulgato, ma non potrai connetterti a siti solo IPv6 e non potrai connetterti a Proton VPN da una rete solo IPv6.

#### :material-information-outline:{ .pg-info } Port Forwarding Remoto

Al momento, Proton VPN supporta soltanto il [port forwarding](https://protonvpn.com/support/port-forwarding) remoto effimero, tramite NAT-PMP, con 60 secondi di tempo di noleggio. L'app per Windows fornisce un'opzione facilmente accessibile, mentre su altri sistemi operativi dovrai eseguire il tuo [client NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Le applicazioni torrent supportano spesso NAT-PMP in modo nativo.

#### :material-information-outline:{ .pg-blue } Anti-censura

Proton VPN ha il suo [protocollo Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) che *può* aiutare in situazioni in cui protocolli VPN come OpenVPN o Wireguard sono bloccati con varie tecniche rudimentali. Stealth incapsula il tunnel VPN in una sessione TLS, in modo da sembrare traffico Internet generico.

Purtroppo non funziona molto bene nei Paesi in cui vengono impiegati filtri sofisticati che analizzano tutto il traffico in uscita nel tentativo di scoprire i tunnel criptati. Stealth non è ancora disponibile su [Windows](https://github.com/ProtonVPN/win-app/issues/64) o Linux.

#### :material-check:{ .pg-green } Client Mobile

Oltre a fornire file di configurazione OpenVPN standard, Proton VPN dispone di client mobile per [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) e [GitHub](https://github.com/ProtonVPN/android-app/releases) che consentono una facile connessione ai propri server.

#### :material-information-outline:{ .pg-blue } Note aggiuntive

I client VPN di Proton supportano l'autenticazione a due fattori su tutte le piattaforme. Proton VPN ha i propri server e datacenter in Svizzera, Islanda e Svezia. Offrono il blocco dei contenuti e il blocco di malware noti con il loro servizio DNS. Inoltre, Proton VPN offre anche server "Tor" che ti consentono di connetterti facilmente ai siti onion, ma consigliamo comunque di utilizzare [il Tor Browser ufficiale](tor.md#tor-browser) per questo scopo.

##### :material-alert-outline:{ .pg-orange } La funzione Killswitch non funziona sui Mac basati su Intel

Arresti anomali del sistema [potrebbero verificarsi](https://protonvpn.com/support/macos-t2-chip-kill-switch) sui Mac basati su Intel quando si utilizza la funzionalità killswitch VPN. Se necessiti di questa funzionalità e stai utilizzando un Mac con chipset Intel, dovresti considerare l'utilizzo di un altro servizio VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo di IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** è un altro fornitore di VPN premium, in operazione dal 2009. IVPN ha sede a Gibilterra e non offre una prova gratuita.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 Paesi

IVPN ha [server in 37 paesi](https://ivpn.net/status).(1) Scegliere un fornitore VPN con un server più vicino a te ridurrà la latenza del traffico di rete che invii. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Ultimo controllo: 02-04-2024

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN utilizzare [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

IVPN è stata sottoposta a un [controllo di non registrazione da Cure53](https://cure53.de/audit-report_ivpn.pdf), che si è concluso in accordo con la dichiarazione di non registrazione di IVPN. Inoltre, IVPN ha completato un [rapporto di cinque test completi di Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) a gennaio 2020. L'IVPN ha anche detto che prevede di avere in futuro dei [rapporti annuali](https://ivpn.net/blog/independent-security-audit-concluded). Un'ulteriore revisione è stata condotta [nell'aprile 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) ed è stata prodotta da Cure53 [sul loro sito web](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Client Open Source

A partire da febbraio 2020 le [applicazioni IVPN sono open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Il codice sorgente è ottenibile dalla loro [organizzazione di GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accetta contanti e Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Supporto WireGuard

IVPN supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

IVPN [consiglia](https://ivpn.net/wireguard) l'utilizzo di WireGuard con il loro servizio e, pertanto, il protocollo è il predefinito su tutte le app di IVPN. Inoltre, IVPN offre anche un generatore di configurazione di WireGuard da utilizzare con le [app](https://wireguard.com/install) ufficiali di WireGuard.

#### :material-information-outline:{ .pg-blue } Supporto IPv6

IVPN consente di [connettersi a servizi che utilizzano il protocollo IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), ma non permette di connettersi da un dispositivo che utilizza un indirizzo IPv6.

#### :material-alert-outline:{ .pg-orange } Port Forwarding remoto

IVPN in precedenza supportava il port forwarding, ma ha rimosso l'opzione a [giugno 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-censura

IVPN dispone di modalità di offuscamento che utilizzano il progetto [v2ray](https://v2ray.com/en/index.html), utile in situazioni in cui protocolli VPN come OpenVPN o Wireguard sono bloccati. Attualmente questa funzione è disponibile solo su Desktop e [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Dispone di due modalità in cui può utilizzare [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) su connessioni QUIC o TCP. QUIC è un protocollo moderno con un migliore controllo della congestione e quindi può essere più veloce con una latenza ridotta. La modalità TCP fa apparire i dati come normale traffico HTTP.

#### :material-check:{ .pg-green } Client Mobile

Oltre a fornire file di configurazione OpenVPN standard, IVPN dispone di client mobile per [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) e [GitHub](https://github.com/ivpn/android-app/releases) che consentono di connettersi facilmente ai propri server.

#### :material-information-outline:{ .pg-blue } Note aggiuntive

I client di IVPN supportano l'autenticazione a due fattori. Inoltre, IVPN fornisce la funzionaalità "[AntiTracker](https://ivpn.net/antitracker)", che blocca le reti e tracker pubblicitari dal livello della rete.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo di Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** è una VPN veloce ed economica con una grande attenzione alla trasparenza e alla sicurezza. Sono operativi dal **2009**. Mullvad ha sede in Svezia e non offre una prova gratuita.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Paesi

Mullvad ha [server in 41 paesi](https://mullvad.net/servers).(1) Scegliere un fornitore VPN con un server più vicino a te ridurrà la latenza del traffico di rete che invii. Questo per un percorso più breve (meno 'salti'), verso la destinazione.
{ .annotate }

1. Ultimo controllo: 02-04-2024

Riteniamo inoltre che sia meglio per la sicurezza delle chiavi private del provider VPN se utilizzano [server dedicati](https://en.wikipedia.org/wiki/Dedicated_hosting_service), invece di soluzioni condivise più economiche (con altri clienti) come [server privati virtuali](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Controllato Indipendentemente

I client VPN di Mullvad sono stati controllati da Cure53 e Assured AB in un rapporto da cinque test, [pubblicato su cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). I ricercatori della sicurezza hanno dichiarato:

> Cure53 e Assured AB sono soddisfatti dai risultati del controllo e, il software, lascia un'impressione complessiva positiva. Con la dedizione alla sicurezza del team interno al complesso Mullvad VPN, i tester non hanno dubbi riguardo alla giusta direzione del progetto da un punto di vista della sicurezza.

Nel 2020 [è stato annunciato](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) un secondo audit e il [rapporto di audit finale](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) è stato reso disponibile sul sito web di Cure53:

> I risultati di questo progetto di maggio-giugno 2020, rivolto al complesso di Mullvad, sono abbastanza positivi. [...] L'ecosistema applicativo complessivo utilizzato da Mullvad lascia un'impressione solida e strutturata. La struttura generale dell'applicazione semplifica l'introduzione di patch e correzioni, in un modo strutturato. Più di ogni altra cosa, i risultati individuati da Cure53 rivelano l'importanza di controllare e rivalutare costantemente i vettori di fuga di notizie attuali, per poter sempre assicurare la privacy degli utenti finali. Detto questo, Mullvad fa un ottimo lavoro nel proteggere l'utente finale dalle comuni perdite di informazioni d'identificazione personale e i relativi rischi legati alla privacy.

Nel 2021 [è stato annunciato](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) un audit delle infrastrutture e la [relazione finale dell'audit](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) è stata resa disponibile sul sito web di Cure53. Un altro rapporto è stato commissionato [nel giugno 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) ed è disponibile sul [sito web di Assured](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Client Open Source

Mullvad fornisce il codice sorgente per i propri client desktop e mobili nella loro [organizzazione di GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accetta contanti e Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers.

#### :material-check:{ .pg-green } Supporto WireGuard

Mullvad supporta il protocollo WireGuard®. [WireGuard](https://wireguard.com) è un protocollo più recente che utilizza una [crittografia](https://wireguard.com/protocol) all'avanguardia. Inoltre, WireGuard mira ad essere più semplice e performante.

Mullvad [consiglia](https://mullvad.net/en/help/why-wireguard) l'utilizzo di WireGuard con il proprio servizio. È il protocollo predefinito o l'unico sulle app Mullvad per Android, iOS, macOS e Linux, ma su Windows è necessario [abilitare manualmente](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Inoltre, Mullvad offre un generatore di configurazione di WireGuard da utilizzare con le [app](https://wireguard.com/install) ufficiali di WireGuard.

#### :material-check:{ .pg-green } Supporto IPv6

Mullvad consente di [accedere ai servizi ospitati su IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) e di connettersi da un dispositivo che utilizza un indirizzo IPv6.

#### :material-alert-outline:{ .pg-orange } Port Forwarding Remoto

Mullvad supportava in precedenza il port forwarding, ma ha rimosso questa opzione nel [maggio 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'assenza di questa funzionalità potrebbe influenzare negativamente alcune applicazioni, specialmente quelle tra pari come i client di torrenting.

#### :material-check:{ .pg-green } Anti-censura

Mullvad ha una modalità di offuscamento che utilizza [Shadowsocks con v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) che può essere utile in situazioni in cui protocolli VPN come OpenVPN o Wireguard sono bloccati.

#### :material-check:{ .pg-green } Client mobile

Mullvad ha pubblicato i client [App Store](https://apps.apple.com/app/id1488466513) e [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), che supportano entrambi un'interfaccia facile da usare, invece di richiedere la configurazione manuale della connessione WireGuard. Il client Android è disponibile anche su [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Note aggiuntive

Mullvad è molto trasparente su quali nodi [possiede o fitta](https://mullvad.net/en/servers). Utilizzano [ShadowSocks](https://shadowsocks.org) nella loro configurazione ShadowSocks + OpenVPN, rendendoli più resistenti ai firewall con [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) che cercano di bloccare le VPN. Presumibilmente, la [Cina deve utilizzare un metodo diverso per bloccare i server ShadowSocks](https://github.com/net4people/bbs/issues/22).

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
- Non sono accettate le informazioni personali (nome utente generato automaticamente, nessun'email necessaria, ecc.).

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
