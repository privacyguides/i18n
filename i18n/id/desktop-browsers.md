---
meta_title: "Browser Web yang Menghargai Privasi untuk PC dan Mac - Privacy Guides"
title: "Browser Dekstop"
icon: material/laptop
description: Browser web ini memberikan perlindungan privasi yang lebih kuat daripada Google Chrome.
cover: desktop-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Rekomendasi Browser Desktop Pribadi
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

Berikut ini adalah browser web desktop yang kami rekomendasikan saat ini beserta dengan konfigurasi untuk penjelajahan standar/non-anonim. Kami merekomendasikan [Mullvad Browser](#mullvad-browser) jika Anda berfokus pada perlindungan privasi yang kuat dan anti-fingerprinting otomatis, [Firefox](#firefox) bagi para penjelajah internet biasa yang mencari alternatif baik untuk Google Chrome, dan [Brave](#brave) jika Anda membutuhkan kompabilitas browser Chromium.

Jika Anda perlu menjelajah internet secara anonim, Anda sebaiknya menggunakan [Tor](tor.md) sebagai gantinya. Kami memberikan beberapa rekomendasi konfigurasi pada halaman ini, tetapi semua browser selain Peramban Tor akan dapat dilacak oleh * seseorang* dengan satu cara atau cara lain.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** adalah versi dari [Tor Browser](tor.md#tor-browser) dengan integrasi jaringan Tor yang telah dihilangkan. Mullvad Browser bertujuan untuk menyediakan teknologi peramban anti-fingerprinting yang ada di Peramban Tor kepada pengguna VPN. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Kode Sumber" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Seperti [Tor Browser](tor.md), Mullvad Browser dirancang untuk mencegah fingerprinting dengan membuat fingerprint di browser Anda identik dengan semua pengguna Mullvad Browser lainnya, serta mencakup pengaturan default dan ekstensi yang secara otomatis dikonfigurasi oleh tingkat keamanan default seperti: *Standar*, *Lebih Aman* dan *Paling Aman*. Oleh karena itu, sangat penting bagi Anda untuk tidak memodifikasi pengaturan browser sama sekali kecuali penyesuaian [tingkat keamanan](https://tb-manual.torproject.org/security-settings/). Melakukan modifikasi akan membuat fingerprint pada browser ini menjadi unik, sehingga mengubah tujuan penggunaan dari browser ini. Jika Anda ingin merubah pengaturan browser Anda dengan sesuai dengan keinginan Anda dan fingerprint bukan menjadi masalah bagi Anda, kami sarankan untuk menggunakan [Firefox](#firefox) sebagai gantinya.

### Anti-Fingerprinting

**Tanpa** menggunakan [VPN](vpn.md), Mullvad Browser memberikan perlindungan yang sama terhadap [skrip pencocokan fingerprint](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) seperti browser pribadi lainnya seperti Firefox+[Arkenfox](#arkenfox-advanced) atau [Brave](#brave). Mullvad Browser menyediakan perlindungan tersebut secara bawaan, dengan mengorbankan sedikit fleksibilitas dan kenyamanan yang dapat diberikan oleh browser pribadi lainnya.

==Untuk perlindungan anti-fingerprinting yang paling kuat, kami sarankan untuk menggunakan Mullvad Browser bersama **dengan** VPN==, baik itu Mullvad atau penyedia VPN lain yang direkomendasikan. Saat menggunakan VPN dengan Mullvad Browser, Anda akan berbagi fingerprint dan alamat IP dengan pengguna lain, memberikan Anda "kerumunan" untuk berbaur. Strategi ini merupakan satu-satunya cara untuk menggagalkan skrip pelacakan tingkat lanjut, dan merupakan teknik anti-fingerprinting yang sama dengan yang digunakan oleh Tor Browser.

Perlu dicatat bahwa meskipun Anda dapat menggunakan Mullvad Browser dengan penyedia VPN mana pun, orang lain dalam VPN tersebut juga harus menggunakan Mullvad Browser agar "kerumunan" ini terbentuk, hal ini lebih mungkin terjadi pada Mullvad VPN dibandingkan dengan penyedia lainnya, terutama menjelang peluncuran Mullvad Browser. Mullvad Browser tidak memiliki konektivitas VPN bawaan, dan juga tidak memeriksa apakah Anda menggunakan VPN sebelum menjelajah; koneksi VPN Anda harus dikonfigurasikan dan dikelola secara terpisah.

Mullvad Browser hadir dengan *uBlock Origin* dan *NoScript* ekstensi browser yang sudah terpasang. Meskipun biasanya kami [tidak merekomendasikan](#extensions) menambahkan ekstensi browser *tambahan*, ekstensi-ekstensi yang telah terpasang dengan browser ini sebaiknya **tidak** dihapus atau dikonfigurasi di luar nilai-nilai defaultnya. Karena jika dilakukan, hal tersebut akan membuat fingerprint browser Anda berbeda secara mencolok dari pengguna Mullvad Browser lainnya. Browser ini juga telah terpasang dengan Ekstensi Mullvad Browser, yang *dapat* dihapus dengan aman tanpa mempengaruhi sidik jari peramban Anda jika Anda menginginkannya, tetapi juga aman untuk tetap dipertahankan bahkan jika Anda tidak menggunakan Mullvad VPN.

### Mode Penjelajahan Pribadi

Mullvad Browser beroperasi dalam mode penjelajahan pribadi permanen, yang mana riwayat, cookies, dan data situs lainnya akan selalu dihapus setiap kali browser ditutup. Bookmark, pengaturan browser, dan pengaturan ekstensi Anda akan tetap dipertahankan.

Hal ini diperlukan untuk mencegah bentuk pelacakan tingkat lanjut, tetapi harus mengorbankan kenyamanan dan beberapa fitur Firefox seperti Multi-Account Containers. Ingatlah bahwa Anda selalu dapat menggunakan beberapa browser lain. Misalnya Anda dapat mempertimbangkan untuk menggunakan Firefox+Arkenfox untuk beberapa situs yang ingin Anda tetap masuk atau yang tidak berfungsi dengan baik di Mullvad Browser. Lalu menggunakan Mullvad Browser untuk penjelajahan umum.

### Mullvad Leta

Mullvad Browser hadir dengan DuckDuckGo yang ditetapkan sebagai mesin pencari default [](search-engines.md), tetapi juga sudah terinstal dengan **Mullvad Leta**, mesin pencari yang membutuhkan langganan Mullvad VPN yang aktif untuk mengaksesnya. Mullvad Leta menggunakan API pencarian berbayar Google secara langsung (itulah sebabnya mengapa terbatas pada pelanggan berbayar), namun karena keterbatasan ini, Mullvad dapat menghubungkan pencarian dan akun VPN Mullvad. Karena alasan ini kami tidak menyarankan penggunaan Mullvad Leta, meskipun Mullvad mengumpulkan sangat sedikit informasi tentang pelanggan VPN mereka.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox** provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
    [:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentation}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Konfigurasi yang Disarankan

These options can be found in :material-menu: → **Settings**

#### Search

- [ ] Uncheck **Provide search suggestions**

Search suggestion features may not be available in your region.

Search suggestions send everything you type in the address bar to the default search engine, regardless of whether you submit an actual search. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

#### Privacy & Security

##### Enhanced Tracking Protection

- [x] Select **Strict** Enhanced Tracking Protection

This protects you by blocking social media trackers, fingerprinting scripts (note that this does not protect you from *all* fingerprinting), cryptominers, cross-site tracking cookies, and some other tracking content. ETP protects against many common threats, but it does not block all tracking avenues because it is designed to have minimal to no impact on site usability.

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

##### Sanitize on Close

If you want to stay logged in to particular sites, you can allow exceptions in **Cookies and Site Data** → **Manage Exceptions...**

- [x] Check **Delete cookies and site data when Firefox is closed**

This protects you from persistent cookies, but does not protect you against cookies acquired during any one browsing session. When this is enabled, it becomes possible to easily cleanse your browser cookies by simply restarting Firefox. You can set exceptions on a per-site basis, if you wish to stay logged in to a particular site you visit often.

##### Telemetry

- [ ] Uncheck **Allow Firefox to send technical and interaction data to Mozilla**
- [ ] Uncheck **Allow Firefox to install and run studies**
- [ ] Uncheck **Allow Firefox to send backlogged crash reports on your behalf**

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

Additionally, the Firefox Accounts service collects [some technical data](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). If you use a Firefox Account you can opt-out:

1. Open your [profile settings on accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### HTTPS-Only Mode

- [x] Select **Enable HTTPS-Only Mode in all windows**

This prevents you from unintentionally connecting to a website in plain-text HTTP. Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day to day browsing.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (advanced)

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly - [which you can easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features/), many of which are enabled by default.
    
    Brave dibuat berdasarkan proyek peramban web Chromium, sehingga seharusnya terasa familier dan memiliki masalah kompatibilitas situs web yang minimal.
    
    [:octicons-home-16: Laman Beranda](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Layanan Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Kebijakan Privasi" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Dokumentasi}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Kode Sumber" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. We advise against using the Flatpak version of Brave, as it replaces Chromium's sandbox with Flatpak's, which is less effective. Additionally, the package is not maintained by Brave Software, Inc.

### Konfigurasi yang Disarankan

These options can be found in :material-menu: → **Settings**.

#### Settings

##### Perisai

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) feature. We suggest configuring these options [globally](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) across all pages that you visit.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

    ??? warning "Use default filter lists"
        Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

- [x] Select **Strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

##### Social media blocking

- [ ] Uncheck all social media components

##### Privacy and security

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

    !!! tip "Sanitizing on Close"

        - [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

        If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

1. Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. Where [strong anonymity is required](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) use the [Tor Browser](tor.md#tor-browser).

##### Extensions

Disable built-in extensions you do not use in **Extensions**

- [ ] Uncheck **Hangouts**
- [ ] Uncheck **WebTorrent**

##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Set **Method to resolve IPFS resources** to **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Sumber Daya Tambahan

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin** is a popular content blocker that could help you block ads, trackers, and fingerprinting scripts.
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Other lists

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Kriteria

**Harap diperhatikan bahwa kami tidak berafiliasi dengan proyek-proyek yang kami rekomendasikan.** Selain [kriteria standar kami](about/criteria.md), kami telah mengembangkan serangkaian persyaratan yang jelas untuk memungkinkan kami memberikan rekomendasi yang objektif. Kami sarankan Anda membiasakan diri dengan daftar ini sebelum memilih untuk menggunakan sebuah proyek, dan melakukan penelitian sendiri untuk memastikan bahwa itu adalah pilihan yang tepat untuk Anda.

!!! contoh "Bagian ini baru"

    Kami sedang berupaya menetapkan kriteria yang jelas untuk setiap bagian dari situs kami, dan hal ini dapat berubah sewaktu-waktu. Jika Anda memiliki pertanyaan mengenai kriteria kami, silakan [tanyakan di forum](https://discuss.privacyguides.net/latest) dan jangan berasumsi bahwa kami tidak mempertimbangkan sesuatu saat membuat rekomendasi jika tidak tercantum di sini. Ada banyak faktor yang dipertimbangkan dan didiskusikan saat kami merekomendasikan sebuah proyek, dan mendokumentasikan setiap faktor tersebut merupakan sebuah pekerjaan yang sedang berjalan.

### Persyaratan Minimum

- Harus berupa perangkat lunak sumber terbuka.
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Kasus Terbaik

Kriteria kasus terbaik kami mewakili apa yang ingin kami lihat dari proyek yang sempurna dalam kategori ini. Rekomendasi kami mungkin tidak menyertakan salah satu atau semua fungsi ini, tetapi rekomendasi yang menyertakan fungsi ini mungkin memiliki peringkat yang lebih tinggi daripada yang lain di halaman ini.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).

### Extension Criteria

- Must not replicate built-in browser or OS functionality.
- Must directly impact user privacy, i.e. must not simply provide information.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
