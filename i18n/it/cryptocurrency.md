---
meta_title: "Blockchain private di criptovalute"
description: Unlike most cryptocurrencies, these ones provide transaction privacy by default. Monero is our top choice for obfuscating transaction information.
title: Criptovalute
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Protects against the following threat(s):</small>

- [:material-eye-outline: Sorveglianza di massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Effettuare pagamenti online è una delle maggiori sfide per la privacy. Queste criptovalute offrono la privacy delle transazioni di default (cosa che **non** è garantita dalla maggior parte delle criptovalute), a condizione che si abbia una buona conoscenza di come effettuare pagamenti privati in modo efficace. Ti consigliamo vivamente di leggere prima il nostro articolo panoramico sui pagamenti prima di effettuare qualsiasi acquisto:

[Effettuare pagamenti privati :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Molte, se non la gran parte delle criptovalute sono delle truffe. Effettua attentamente le transazioni, soltanto con i progetti di cui ti fidi.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** uses a blockchain with privacy-enhancing technologies that obfuscate transactions to achieve [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }. Ogni transazione di Monero nasconde l'importo della transazione, gli indirizzi di invio e ricezione e la fonte dei fondi senza dover fare i salti mortali, il che la rende una scelta ideale per i neofiti delle criptovalute.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Source Code" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Contribute }

</details>

</div>

Con Monero, gli osservatori esterni non possono decifrare gli indirizzi che scambiano Monero, gli importi delle transazioni, i saldi degli indirizzi o gli storici delle transazioni.

Per una privacy ottimale, assicurati di utilizzare un portafoglio non custodiale in cui la chiave di visualizzazione del portafoglio resta sul dispositivo. Ciò significa che soltanto tu potrai spendere i tuoi fondi e visualizzare le transazioni in entrata e in uscita. Se utilizzi un portafoglio custodiale, il fornitore può vedere **tutto** ciò che fai; se utilizzi un portafoglio "leggero" in cui il fornitore conserva la chiave di visualizzazione privata, questi può vedere quasi tutto ciò che fai. Alcuni portafogli non custodiali sono:

- [Client ufficiale Monero ](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet supporta più criptovalute. A Monero-only version of Cake Wallet for iOS and Android is available at [Monero.com](https://monero.com).
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Per ottenere la massima privacy (anche con un portafoglio non custodiale), dovresti operare il tuo nodo di Monero. Utilizzare il nodo di un'altra persona espone loro alcune informazioni, come l'indirizzo IP da cui ti connetti, le marche orarie di sincronizzazione del tuo portafoglio e le transazioni inviate da esso (ma nessun altro dettaglio su tali transazioni). Alternatively, you can connect to someone else’s Monero node over Tor or [I2P](alternative-networks.md#i2p-the-invisible-internet-project).

In August 2021, CipherTrace [announced](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) enhanced Monero tracing capabilities for government agencies. I post pubblici mostrano che la Rete di Controllo dei Crimini Finanziari del Dipartimento del Tesoro degli USA [ha concesso una licenza ](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view) per il "Modulo Monero" di CipherTrace, alla fine del 2022.

La privacy del grafico delle transazioni di Monero è limitata da firme ad anello relativamente piccole, soprattutto contro gli attacchi mirati. Monero's privacy features have also been [called into question](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy) by some security researchers, and a number of severe vulnerabilities have been found and patched in the past, so the claims made by organizations like CipherTrace are not out of the question. Sebbene sia improbabile che esistano strumenti di sorveglianza di massa di Monero, come quelli per Bitcoin e altri, è certo che gli strumenti di tracciamento assistano con le indagini mirate.

Infine, Monero è il contenendente più forte per una criptovaluta rispettosa della privacy, ma le sue affermazioni sulla privacy **non** sono state dimostrate definitivamente, in un modo o nell'altro. Più tempo e ricerca sono necessari per valutare se Monero sia abbastanza resiliente agli attacchi, da fornire sempre una privacy adeguata.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

- Le criptovalute devono fornire transazioni private e non tracciabili di default.
