---
meta_title: "Ιδιωτικοί Περιηγητές Ιστού για PC και Mac - Privacy Guides"
title: "Περιηγητές Desktop"
icon: material/laptop
description: Οι εξής περιηγητές ιστού παρέχουν ισχυρότερες προστασίες απορρήτου από το Google Chrome.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Συστάσεις Ιδιωτικών Περιηγητών για Επιφάνειες Εργασίας
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://en.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

Αυτοί είναι οι περιηγητές ιστού επιφάνειας εργασίας, τους οποίους προτείνουμε επί του παρόντος, καθώς και οι ρυθμίσεις για τυπική/μη-ανώνυμη περιήγηση. Προτείνουμε τον [Mullvad Browser](#mullvad-browser) εαν σε απασχολεί ιδιαίτερα η ιδιωτικότητα και η προστασία του ψηφιακού σου αποτυπώματος και θέλεις αυτά να υφίστανται από προεπιλογή, [το Firefox](#firefox) για καθημερινή περιήγηση αν κυρίως αναζητάς μια καλή εναλλακτική στο Google Chrome, και τέλος [το Brave](#brave) αν χρειάζεσαι συμβατότητα με περιηγητές τύπου Chromium.

Εάν χρειάζεται να περιηγηθείτε στο διαδίκτυο ανώνυμα, θα πρέπει σε αυτή την περίπτωση να χρησιμοποιήσετε το [Tor](tor.md). Προτείνουμε ορισμένες ρυθμίσεις στην παρούσα σελίδα, μα όλοι οι περιηγητές εκτός του Tor Browser θα είναι ανιχνεύσιμοι από *κάποιο* με τον έναν ή τον άλλο τρόπο, ανεξαρτήτως ρυθμίσεων.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

Ο **Mullvad Browser** είναι μία έκδοση του [Tor Browser](tor.md#tor-browser) δίχως ενσωματώσεις δικτύου Tor και αποσκοπεί να προσφέρει τις τεχνολογίες "αντι-αποτύπωσης" (anti-fingerprinting) του Tor Browser σε χρήστ(ρι)ες VPN. Αναπτύσσεται από το Tor Project και διανέμεται από τη [Mullvad](vpn.md#mullvad), και **δεν** απαιτεί χρήση του Mullvad VPN.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Λήψεις</summary>

- [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Παρόμοια του [Tor Browser](tor.md), ο Mullvad Browser σχεδιάστηκε να αποτρέπει την αποτύπωση καθιστώντας το ψηφιακό αποτύπωμα του περιηγητή σου πανομοιότυπο με όλων των υπόλοιπων χρηστ(ρι)ών του Mullvad Browser, και περιλαμβάνει προεπιλεγμένες ρυθμίσεις και επεκτάσεις, οι οποίες διαμορφώνονται αυτόματα από τα προεπιλεγμένα επίπεδα ασφαλείας: *Τυπικό*, *Ασφαλέστερο* και *Ασφαλέστατο*. Συνεπώς, είναι ζωτικής σημασίας να μην τροποποιήσεις τον περιηγητή πέραν της επιλογής [επιπέδου ασφαλείας](https://tb-manual.torproject.org/security-settings). Άλλες τροποποιήσεις θα κάνουν το ψηφιακό σου αποτύπωμα μοναδικό, αναιρώντας έτσι τον σκοπό χρήσης του συγκεκριμένου περιηγητή. Εάν θέλεις να ρυθμίσεις τον περιηγητή σου σε μεγαλύτερο βαθμό και η αποτύπωση δεν σε απασχολεί, τότε σου προτείνουμε το [Firefox](#firefox).

### Αντι-Αποτύπωση (Anti-Fingerprinting)

**Δίχως** χρήση [VPN](vpn.md), ο Mullvad Browser προστατεύει από [απλοϊκά σκριπτάκια αποτύπωσης](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) όσο και οι άλλοι ιδιωτικοί περιηγητές όπως ο Firefox+[Arkenfox](#arkenfox-advanced) ή [ ο Brave](#brave). Ο περιηγητής Mullvad παρέχει εξαρχής αυτές τις προστασίες εις βάρος ορισμένης ευελιξίας και ευκολίας, που δύναται να προσφέρουν άλλα προγράμματα περιήγησης, τα οποία δίνουν έμφαση στην ιδιωτικότητα.

==Για την ισχυρότερη προστασία έναντι του fingerprinting, συνιστούμε τη χρήση του περιηγητή Mullvad σε συνδυασμό **με** ένα VPN==, είτε αυτό είναι της Mullvad είτε ενός άλλου συνιστώμενου παρόχου VPN. Όταν χρησιμοποιείτε ένα VPN με το περιηγητή Mullvad, θα μοιράζεστε ένα ψηφιακό δακτυλικό αποτύπωμα και μια ομάδα διευθύνσεων IP με πολλούς άλλους χρήστες, δίνοντάς σας έτσι ένα "πλήθος" για να κρυφτείται ανάμεσα. Αυτή η στρατηγική είναι ο μόνος τρόπος για να αποτρέψετε προηγμένα tracking scripts και είναι η ίδια τεχνική κατά του fingerprinting, που χρησιμοποιείται από το περιηγητή Tor.

Σημειώστε, ότι ενώ μπορείτε να χρησιμοποιήσετε το περιηγητή Mullvad σε συνδυασμό με οποιονδήποτε πάροχο VPN, οι άλλοι άνθρωποι σε αυτό το VPN πρέπει επίσης να χρησιμοποιούν το περιηγητή Mullvad, ετσί ώστε να μπορέσει να υπάρξει αυτό το "πλήθος", κάτι που είναι πιο πιθανό στο Mullvad VPN σε σύγκριση με άλλους παρόχους, ιδιαίτερα τόσο κοντά στην κυκλοφορία του Mullvad Browser. Ο περιηγητής Mullvad δε διαθέτει ενσωματωμένη συνδεσιμότητα VPN, ούτε ελέγχει εάν χρησιμοποιείτε ένα VPN πριν από την περιήγηση- η σύνδεση VPN πρέπει να ρυθμιστεί και να υπόκειται σε διαχείρισή ξεχωριστά.

Ο περιηγητής Mullvad διαθέτει προεγκατεστημένες τις επεκτάσεις *uBlock Origin* και *NoScript*. Ενώ συνήθως δεν συνιστούμε την πρόσθεση *επιπλέων* [πρόσθετων επεκτάσεων](browser-extensions.md), αυτές οι επεκτάσεις, οι οποίες είναι προ-εγκατεστημένες στο πρόγραμμα περιήγησης θα πρέπει να **μην** αφαιρεθούν ή να ρυθμιστούν πέρα από τις προεπιλεγμένες ρυθμίσεις τους, διότι κάτι τέτοιο θα κάνει αισθητά το ψηφιακό δακτυλικό αποτύπωμα του περιηγητή σας διακριτό από τους άλλους χρήστες του προγράμματος περιήγησης Mullvad. Έρχεται επίσης προεγκατεστημένο με την επέκταση περιήγησης Mullvad, η οποία *μπορεί* να αφαιρεθεί με ασφάλεια χωρίς να επηρεάσει το ψηφιακό δακτυλικό αποτύπωμα του προγράμματος περιήγησής σας, αν θέλετε, αλλά είναι επίσης ασφαλές να το διατηρήσετε ακόμα και αν δεν χρησιμοποιείτε το Mullvad VPN.

### Λειτουργία Ιδιωτικής Περιήγησης

Ο περιηγητής Mullvad βρίσκεται μόνιμα σε λειτουργία ιδιωτικής περιήγησης, με αποτέλεσμά το ιστορικό, τα cookies και άλλα δεδομένα του ιστότοπου να διαγράφονται πάντα κάθε φορά που κλείνετε το πρόγραμμα περιήγησης. Οι σελιδοδείκτες, οι ρυθμίσεις του προγράμματος περιήγησης και οι ρυθμίσεις των επεκτάσεων θα διατηρηθούν.

Αυτό είναι απαραίτητο για την αποτροπή προηγμένων μορφών εντοπισμού, αλλά έχει ως κόστος την ευκολία και ορισμένες λειτουργίες του Firefox, όπως τα Multi-Account Containers. Θυμηθείτε ότι μπορείτε πάντα να χρησιμοποιείτε πολλαπλά προγράμματα περιήγησης, για παράδειγμα, μπορείτε να χρησιμοποιήσετε το Firefox+Arkenfox για μερικούς ιστότοπους, στους οποίους επιθυμείται να παραμείνετε συνδεδεμένοι ή οι οποίοι δεν λειτουργούν σωστά στο περιηγήτη Mullvad, και το περιηγητή Mullvad για γενική περιήγηση.

### Mullvad Leta

Ο περιηγητής Mullvad διαθέτει το DuckDuckGo ως προεπιλεγμένη μηχανή αναζήτησης [](search-engines.md), αλλά έχει επίσης προεγκατεστημένο και το **Mullvad Leta**, μια μηχανή αναζήτησης που απαιτεί μια ενεργή συνδρομή Mullvad VPN για πρόσβαση. Το Mullvad Leta αναζητά απευθείας το API πληρωμένης αναζήτησης της Google, γι' αυτό και περιορίζεται σε συνδρομητές επί πληρωμής. Ωστόσο, η Mullvad μπορεί να συσχετίσει τα ερωτήματα αναζήτησης και τους λογαριασμούς VPN της Mullvad λόγω αυτού του περιορισμού. Για το λόγο αυτό, αποθαρρύνουμε τη χρήση του Mullvad Leta, παρόλο που η Mullvad συλλέγει πολύ λίγες πληροφορίες για τους συνδρομητές VPN της.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

**Firefox** provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Προσοχή</p>

Ο Firefox περιλαμβάνει ένα μοναδικό [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) στις λήψεις από τον ιστότοπο της Mozilla και χρησιμοποιεί την τηλεμετρία του Firefox για την αποστολή του token. Το token **δεν** περιλαμβάνεται στις εκδόσεις από το [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Συνιστώμενη διαμόρφωση του Firefox

Αυτές οι επιλογές βρίσκονται στο :material-menu: → **Ρυθμίσεις**

#### Αναζήτηση

- [ ] Απενεργοποιήστε την επιλογή **Εμφάνιση προτάσεων αναζήτησης**

Οι λειτουργίες προτάσεων αναζήτησης ενδέχεται να μην είναι διαθέσιμες στην περιοχή σας.

Οι προτάσεις αναζήτησης στέλνουν ό,τι πληκτρολογείτε στη γραμμή διευθύνσεων στην προεπιλεγμένη μηχανή αναζήτησης, ανεξάρτητα από το αν κάνετε πραγματική αναζήτηση. Η απενεργοποίηση των προτάσεων αναζήτησης σας επιτρέπει να ελέγχετε με μεγαλύτερη ακρίβεια τα δεδομένα που στέλνετε στον πάροχο της μηχανής αναζήτησης.

##### Firefox Suggest (μόνο στις ΗΠΑ)

Το [Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) είναι μια λειτουργία παρόμοια με τις προτάσεις αναζήτησης, η οποία είναι διαθέσιμη μόνο στις ΗΠΑ. Συνιστούμε την απενεργοποίησή της για τον ίδιο λόγο που συνιστούμε την απενεργοποίηση των προτάσεων αναζήτησης. Εάν δεν βλέπετε αυτές τις επιλογές κάτω από την επικεφαλίδα της **Γραμμής Διευθύνσεων**, δεν έχετε τη νέα λειτουργία και μπορείτε να αγνοήσετε αυτές τις αλλαγές.

- [ ] Αποεπιλέξτε **Προτάσεις από τον Firefox**
- [ ] Αποεπιλέξτε **Προτάσεις από χορηγούς**

#### Απόρρητο και ασφάλεια

##### Ενισχυμένη προστασία από καταγραφή

- [x] Επιλέξτε **Αυστηρή** ενισχυμένη προστασία εντοπισμού

Αυτό σας προστατεύει αποκλείοντας τους ιχνηλάτες κοινωνικών δικτύων, το περιεχόμενο καταγραφής σε όλα τα παράθυρα (σημειώστε ότι αυτό δεν σας προστατεύει από *όλα τα* fingerprinting), τα cryptominers, τα cookie μεταξύ ισοτόπων σε όλα τα παράθυρα και κάποιο άλλο περιεχόμενο παρακολούθησης. Η ενισχυμένη προστασία από καταγραφή προστατεύει από πολλές κοινές απειλές, αλλά δεν μπλοκάρει όλες τις οδούς εντοπισμού, επειδή έχει σχεδιαστεί για να έχει ελάχιστες έως καθόλου επιπτώσεις στη χρηστικότητα του ιστότοπου.

##### Sanitize on Close

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Check **Delete cookies and site data when Firefox is closed**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Uncheck **Allow Firefox to send technical and interaction data to Mozilla**
- [ ] Uncheck **Allow Firefox to install and run studies**
- [ ] Uncheck **Allow Firefox to send backlogged crash reports on your behalf**

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. Open your [profile settings on accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### HTTPS-Only Mode

- [x] Select **Enable HTTPS-Only Mode in all windows**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day to day browsing.

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (advanced)

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

</div>

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly - [which you can easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-windows11: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

These options can be found in :material-menu: → **Settings**.

#### Settings

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### Privacy and security

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Extensions

Disable built-in extensions you do not use in **Extensions**

- [ ] Uncheck **Hangouts**
- [ ] Uncheck **WebTorrent**

##### Web3

Τα χαρακτηριστικά Web3 του Brave μπορούν δυνητικά να αυξήσουν το δακτυλικό αποτύπωμα του προγράμματος περιήγησης και την επιφάνεια επιθέσεων. Αν δεν χρησιμοποιείτε καμία από τις λειτουργίες, θα πρέπει να τις απενεργοποιήσετε.

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Ορίστε τη **Μέθοδο αποκρυπτογράφησης πόρων IPFS** σε **Απενεργοποιημένη**

##### Σύστημα

<div class="annotate" markdown>

- [ ] Αποεπιλέξτε την επιλογή **Να συνεχίζεται η εκτέλεση εφαρμογών παρασκηνίου όταν το Brave είναι κλειστό** για να απενεργοποιήσετε τις εφαρμογές παρασκηνίου (1)

</div>

1. Αυτή η επιλογή δεν υπάρχει σε όλες τις πλατφόρμες.

#### Brave Sync

Το [Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) επιτρέπει στα δεδομένα περιήγησής σας (ιστορικό, σελιδοδείκτες κ. λπ.) να είναι προσβάσιμα σε όλες τις συσκευές σας χωρίς να απαιτείται λογαριασμός και τα προστατεύει με κρυπτογράφηση από άκρο σε άκρο.

#### Brave Rewards and Wallet

Το **Brave Rewards** σας επιτρέπει να λαμβάνετε το κρυπτονόμισμα Basic Attention Token (BAT) για την εκτέλεση ορισμένων ενεργειών στο Brave. Βασίζεται σε custodial λογαριασμό και KYC από έναν επιλεγμένο αριθμό παρόχων. Δεν συνιστούμε το BAT ως [ιδιωτικό κρυπτονόμισμα](cryptocurrency.md), ούτε συνιστούμε τη χρήση ενός [ custodial πορτοφολιού](advanced/payments.md#other-coins-bitcoin-ethereum-etc), οπότε αποθαρρύνουμε τη χρήση αυτής της λειτουργίας.

Το **Brave Wallet** λειτουργεί τοπικά στον υπολογιστή σας, αλλά δεν υποστηρίζει ιδιωτικά κρυπτονομίσματα, οπότε θα αποθαρρύναμε τη χρήση και αυτής της δυνατότητας.

## Επιπλέον πόροι

## Κριτήρια

**Σημειώστε ότι δε συσχετιζόμαστε με κανένα από τα project που προτείνουμε.** Εκτός από τα [συνήθη κριτήριά μας](about/criteria.md), έχουμε αναπτύξει ένα σαφές σύνολο απαιτήσεων που μας επιτρέπουν να παρέχουμε αντικειμενικές συστάσεις. Σας προτείνουμε να εξοικειωθείτε με αυτόν τον κατάλογο προτού επιλέξετε να χρησιμοποιήσετε ένα project και να διεξάγετε τη δική σας έρευνα για να βεβαιωθείτε ότι είναι η σωστή επιλογή για εσάς.

### Ελάχιστες Απαιτήσεις

- Πρέπει να είναι λογισμικό ανοικτού κώδικα.
- Υποστηρίζει αυτόματες ενημερώσεις.
- Λαμβάνει ενημερώσεις engine σε 0-1 ημέρες από την έκδοση του upstream.
- Είναι διαθέσιμο σε Linux, macOS και Windows.
- Οποιεσδήποτε αλλαγές απαιτούνται για να γίνει το πρόγραμμα περιήγησης πιο φιλικό προς το απόρρητο δεν θα πρέπει να επηρεάζουν αρνητικά την εμπειρία του χρήστη.
- Μπλοκάρει τα cookies τρίτων από προεπιλογή.
- Υποστηρίζει [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) για τον μετριασμό της παρακολούθησης μεταξύ των τοποθεσιών.[^1]

### Βέλτιστη Περίπτωση

Τα κριτήρια της καλύτερης περίπτωσης αντιπροσωπεύουν αυτό που θα θέλαμε να δούμε από το τέλειο project σε αυτή την κατηγορία. Οι συστάσεις μας ενδέχεται να μην περιλαμβάνουν κάποια ή όλες αυτές τις λειτουργίες, αλλά εκείνες που τις περιλαμβάνουν ενδέχεται να κατατάσσονται υψηλότερα από άλλες σε αυτή τη σελίδα.

- Περιλαμβάνει ενσωματωμένη λειτουργία αποκλεισμού περιεχομένου.
- Υποστηρίζει διαμερισμό cookie ([Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Υποστηρίζει Progressive Web Apps. Τα PWA σάς επιτρέπουν να εγκαθιστάτε ορισμένους ιστότοπους σαν να ήταν εγγενείς εφαρμογές στον υπολογιστή σας. Αυτό μπορεί να έχει πλεονεκτήματα σε σχέση με την εγκατάσταση εφαρμογών που βασίζονται στο Electron, επειδή επωφελείστε από τις τακτικές ενημερώσεις ασφαλείας του προγράμματος περιήγησής σας.
- Δεν περιλαμβάνει πρόσθετες λειτουργίες (bloatware) που δεν επηρεάζουν το απόρρητο του χρήστη.
- Δεν συλλέγει τηλεμετρία από προεπιλογή.
- Παρέχει υλοποίηση διακομιστή συγχρονισμού ανοικτού κώδικα.
- Προεπιλογή σε μια [ιδιωτική μηχανή αναζήτησης](search-engines.md).

[^1]: Η εφαρμογή της Brave περιγράφεται λεπτομερώς στο [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
