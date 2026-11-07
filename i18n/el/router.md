---
title: "Υλικολογισμικό Δρομολογητή"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/images/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/images/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** is a Linux-based operating system; it's primarily used on embedded devices to route network traffic. Περιλαμβάνει τα util-linux, uClibc, και BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Αρχική](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Τεκμηρίωση}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Πηγαίος Κώδικας" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Συνεισφέρετε }

</details>

</div>

Μπορείτε να συμβουλευτείτε τον [πίνακα υλικού](https://openwrt.org/toh/start) του OpenWrt για να ελέγξετε αν η συσκευή σας υποστηρίζεται.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/images/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. Το OPNsense αναπτύσσεται συνήθως ως περιμετρικό τείχος προστασίας, δρομολογητής, ασύρματο σημείο πρόσβασης, διακομιστής DHCP, διακομιστής DNS και τελικό σημείο VPN.

[:octicons-home-16: Αρχική](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Τεκμηρίωση}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Πηγαίος Κώδικας" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Συνεισφέρετε }

</details>

</div>

Το OPNsense αναπτύχθηκε αρχικά από το [pfSense](https://en.wikipedia.org/wiki/PfSense), και τα δύο έργα έχουν χαρακτηριστεί ως δωρεάν και αξιόπιστες διανομές τείχους προστασίας που προσφέρουν χαρακτηριστικά που συχνά συναντώνται μόνο σε ακριβά εμπορικά τείχη προστασίας. Ξεκίνησε το 2015, οι προγραμματιστές του OPNsense [ανέφεραν](https://docs.opnsense.org/history/thefork.html) σε μια σειρά από ζητήματα ασφάλειας και ποιότητας κώδικα με το pfSense, τα οποία θεωρούσαν ότι καθιστούσαν αναγκαία μια διακλάδωση του έργου, καθώς και σε ανησυχίες σχετικά με την εξαγορά της πλειοψηφίας του pfSense από την Netgate και τη μελλοντική κατεύθυνση του έργου pfSense.

## Κριτήρια

**Σημειώστε ότι δε συσχετιζόμαστε με κανένα από τα project που προτείνουμε.** Εκτός από τα [συνήθη κριτήριά μας](about/criteria.md), έχουμε αναπτύξει ένα σαφές σύνολο απαιτήσεων που μας επιτρέπουν να παρέχουμε αντικειμενικές συστάσεις. Σας προτείνουμε να εξοικειωθείτε με αυτόν τον κατάλογο προτού επιλέξετε να χρησιμοποιήσετε ένα project και να διεξάγετε τη δική σας έρευνα για να βεβαιωθείτε ότι είναι η σωστή επιλογή για εσάς.

- Πρέπει να είναι ανοικτού κώδικα.
- Πρέπει να λαμβάνει τακτικές ενημερώσεις.
- Πρέπει να υποστηρίζει μεγάλη ποικιλία υλικού.
