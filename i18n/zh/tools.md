---
meta_title: "Ad-Free Privacy Tool/Service Recommendations - Privacy Guides"
title: "隐私工具"
icon: 资料/工具
hide:
  - toc
description: A complete list of the privacy tools, services, software, and hardware recommended by the Privacy Guides community.
---

如果你正在寻找某项具体解决方案，这里是一些我们推荐的各种类别的软硬件工具。 我们推荐的隐私工具主要依据它们的安全功能来选择，另外还强调了去中心化和开源。 They are applicable to a variety of threat models ranging from protection against global mass surveillance programs and avoiding big tech companies to mitigating attacks, but only you can determine what will work best for your needs.

<div class="grid" markdown>

<div markdown>
[VPN Providers](vpn.md){ .md-button }
[Password Managers](passwords.md){ .md-button }
[Email Providers](email.md){ .md-button }
[Browser Extensions](browser-extensions.md){ .md-button }
[DNS Servers](dns.md){ .md-button }
[Email Aliasing Services](email-aliasing.md){ .md-button }
[Photo Organization Tools](photo-management.md){ .md-button }
</div>

</div>

<div markdown>

<div class="admonition info" markdown>

[Self-hosting recommendations](self-hosting/index.md) have been moved to their own category.

</div>

</div>

If you want assistance figuring out the best privacy tools and alternative programs for your needs, start a discussion on our [forum](https://discuss.privacyguides.net) or our [Matrix](https://matrix.to/#/#privacyguides:matrix.org) community!

关于每个项目的更多相关细节, 为什么选择它们以及我们提议的一些额外的使用提示或技巧，请点击每个部分的 "了解详情" 链接, 或者也可以点击推荐项本身来转到具体的页面部分。

<div class="grid" markdown>

<div markdown>
- [x] **Ad-Free Recommendations**
- [x] **Frequent Updates**
- [x] **Trusted by Readers**
</div>

<div markdown>
- [x] **Complete Editorial Independence**
- [x] **Open-Source Contributions**
- [x] **Trusted by Journalists**
</div>

</div>

## Private Web Browsers

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=left }

**Tor Browser** (Desktop & Android) is the top choice if you need anonymity, as it provides you with access to the **Tor** network, a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. 个人和组织也可以通过Tor网络与".onion隐藏服务"分享信息，而不损害其隐私。 由于Tor流量难以阻止和跟踪，因此Tor是一种有效的审查规避工具。

[Read Our Full Review :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary }

</div>

<div class="grid cards" markdown>

- ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ .lg .middle .twemoji } **Mullvad Browser**

    ---

    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users.

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#mullvad-browser)

- ![Firefox logo](assets/img/browsers/firefox.svg){ .lg .middle .twemoji } **Firefox**

    ---

    **Firefox** is a great Chromium alternative which provides strong privacy settings such as [Enhanced Tracking Protection](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), which can help block various [types of tracking](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

    - [Read Full Review :material-arrow-right-drop-circle:](desktop-browsers.md#firefox)

- ![Brave logo](assets/img/browsers/brave.svg){ .lg .middle .twemoji } **Brave Browser**

    ---

    **Brave** is a private-by-default browser based on Chromium, so it should feel familiar and have minimal website compatibility issues.

    - [Brave Desktop Review :material-arrow-right-drop-circle:](desktop-browsers.md#brave)
    - [Brave Mobile Review :material-arrow-right-drop-circle:](mobile-browsers.md#brave)

- ![Cromite logo](assets/img/browsers/cromite.svg){ .lg .middle .twemoji } **Cromite (Android)**

    ---

    **Cromite** is a Chromium-based Android browser with built-in ad-blocking and [privacy enhancements](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the popular, now-discontinued Bromite browser.

    - [Read Full Review :material-arrow-right-drop-circle:](mobile-browsers.md#cromite-android)

- ![Safari logo](assets/img/browsers/safari.svg){ .lg .middle .twemoji } **Safari (iOS)**

    ---

    We recommend **Safari** due to its [anti-fingerprinting](https://webkit.org/blog/15697/private-browsing-2-0) features and default tracker blocking. It also separates your cookies in private browsing mode to prevent tracking between tabs.

    - [Read Full Review :material-arrow-right-drop-circle:](mobile-browsers.md#safari-ios)

</div>

<div class="grid" markdown>

<div markdown>
### Browser Extensions

<div class="grid cards" markdown>

- ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ .twemoji loading=lazy } [uBlock Origin](browser-extensions.md#ublock-origin)
- ![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ .twemoji loading=lazy } [uBlock Origin Lite](browser-extensions.md#ublock-origin-lite)
- ![AdGuard logo](assets/img/browsers/adguard.svg){ .twemoji loading=lazy } [AdGuard for iOS](browser-extensions.md#adguard)

</div>

</div>

<div markdown>
### More Tor Network Tools

<div class="grid cards" markdown>

- ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ .twemoji loading=lazy } [Onion Browser (Tor for iOS)](tor.md#onion-browser-ios)

</div>

</div>

</div>

## Top 3 Private VPN Providers

<details class="danger" markdown>
<summary>VPNs do not provide anonymity</summary>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser.

If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. VPN不是良好安全实践的替代品。

[了解更多 :hero-arrow-circle-right-fill:](vpn.md)

</details>

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .lg .middle .twemoji } **Proton VPN**

    ---

    - [x] **112+ Countries**
    - [x] WireGuard Support
    - [x] Cash Payments
    - [x] Partial Port Forwarding Support
    - [ ] No IPv6

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#proton-vpn)

- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .lg .middle .twemoji } **IVPN**

    ---

    - [x] **37+ Countries**
    - [x] WireGuard Support
    - [x] Monero & Cash Payments
    - [ ] No Port Forwarding
    - [ ] No IPv6

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#ivpn)

- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .lg .middle .twemoji } **Mullvad**

    ---

    - [x] **49+ Countries**
    - [x] WireGuard Support
    - [x] Monero & Cash Payments
    - [ ] No Port Forwarding
    - [x] IPv6 Support

    [Read Full Review :material-arrow-right-drop-circle:](vpn.md#mullvad)

</div>

## Top 3 Private Email Providers

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .lg .middle .twemoji } **Proton Mail**

    ---

    Proton Mail is an email service with a focus on privacy, encryption, security, and ease of use. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland. The Proton Mail Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

    [Read Full Review :material-arrow-right-drop-circle:](email.md#proton-mail)

- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .lg .middle .twemoji } **Mailbox.org**

    ---

    Mailbox.org is an email service with a focus on being secure, ad-free, and privately powered by 100% eco-friendly energy. 他们自2014年以来一直在运作。 Mailbox.org总部位于德国柏林。 Accounts start with up to 2 GB storage, which can be upgraded as needed.

    [Read Full Review :material-arrow-right-drop-circle:](email.md#mailboxorg)

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .lg .middle .twemoji }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .lg .middle .twemoji } **Tuta**

    ---

    Tuta (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1 GB of storage.

    [Read Full Review :material-arrow-right-drop-circle:](email.md#tuta)

</div>

<div class="grid" markdown>

<div markdown>
### Email Aliasing Services

<div class="grid cards" markdown>

- ![Addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji loading=lazy } [Addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji loading=lazy } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

</div>

</div>

### Secure Email Clients

<div class="grid cards" markdown>

- ![Thunderbird logo](assets/img/email-clients/thunderbird.svg){ .twemoji loading=lazy } [Thunderbird](email-clients.md#thunderbird)
- ![Apple Mail logo](assets/img/email-clients/applemail.png){ .twemoji loading=lazy } [Apple Mail (macOS)](email-clients.md#apple-mail-macos)
- ![FairEmail logo](assets/img/email-clients/fairemail.svg){ .twemoji loading=lazy } [FairEmail (Android)](email-clients.md#fairemail-android)
- ![GNOME Evolution logo](assets/img/email-clients/evolution.svg){ .twemoji loading=lazy } [GNOME Evolution (Linux)](email-clients.md#gnome-evolution-gnome)
- ![Kontact logo](assets/img/email-clients/kontact.svg){ .twemoji loading=lazy } [Kontact (Linux)](email-clients.md#kontact-kde)
- ![Mailvelope logo](assets/img/email-clients/mailvelope.svg){ .twemoji loading=lazy } [Mailvelope (PGP in standard webmail)](email-clients.md#mailvelope-browser)
- ![NeoMutt logo](assets/img/email-clients/mutt.svg){ .twemoji loading=lazy } [NeoMutt (CLI)](email-clients.md#neomutt-cli)

</div>

[了解更多 :hero-arrow-circle-right-fill:](email-clients.md)

## More Private Service Providers

### 路由器固件

<div class="grid cards" markdown>

- ![Proton Drive logo](assets/img/cloud/protondrive.svg){ .twemoji loading=lazy } [Proton Drive](cloud.md#proton-drive)
- ![Tresorit logo](assets/img/cloud/tresorit.svg){ .twemoji loading=lazy } [Tresorit](cloud.md#tresorit)
- ![Peergos logo](assets/img/cloud/peergos.svg){ .twemoji loading=lazy } [Peergos](cloud.md#peergos)

</div>

[了解更多 :hero-arrow-circle-right-fill:](cloud.md)

### Data Removal Services

<div class="grid cards" markdown>

- ![EasyOptOuts logo](assets/img/data-broker-removals/easyoptouts.svg){ .twemoji loading=lazy } [EasyOptOuts](data-broker-removals.md#easyoptouts-paid)
- ![Google logo](assets/img/data-broker-removals/google.svg){ .twemoji loading=lazy } [Google *Results about you*](data-broker-removals.md#google-results-about-you-free)

</div>

[了解更多 :hero-arrow-circle-right-fill:](data-broker-removals.md)

### 云存储

#### 加密DNS代理

We [recommend](dns.md#recommended-providers) a number of encrypted DNS servers based on a variety of criteria, such as [Mullvad](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) and [Quad9](https://quad9.net) amongst others. We recommend for you to read our pages on DNS before choosing a provider. In many cases, using an alternative DNS provider is not recommended.

[了解更多 :hero-arrow-circle-right-fill:](dns.md)

#### Encrypted DNS Proxies

<div class="grid cards" markdown>

- ![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ .twemoji loading=lazy }![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ .twemoji loading=lazy } [RethinkDNS](dns.md#rethinkdns)
- ![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ .twemoji loading=lazy } [DNSCrypt-Proxy](dns.md#dnscrypt-proxy)

</div>

[了解更多 :hero-arrow-circle-right-fill:](dns.md#encrypted-dns-proxies)

#### Self-hosted Solutions

<div class="grid cards" markdown>

- ![AdGuard Home logo](assets/img/dns/adguard-home.svg){ .twemoji loading=lazy } [AdGuard Home](dns.md#adguard-home)
- ![Pi-hole logo](assets/img/dns/pi-hole.svg){ .twemoji loading=lazy } [Pi-hole](dns.md#pi-hole)

</div>

[了解更多 :hero-arrow-circle-right-fill:](dns.md#self-hosted-dns-filtering)

### Financial Services

#### Payment Masking Services

<div class="grid cards" markdown>

- ![Privacy.com logo](assets/img/financial-services/privacy_com.svg#only-light){ .twemoji loading=lazy }![Privacy.com logo](assets/img/financial-services/privacy_com-dark.svg#only-dark){ .twemoji loading=lazy } [Privacy.com](financial-services.md#privacycom-us)
- ![MySudo logo](assets/img/financial-services/mysudo.svg#only-light){ .twemoji loading=lazy }![MySudo logo](assets/img/financial-services/mysudo-dark.svg#only-dark){ .twemoji loading=lazy } [MySudo](financial-services.md#mysudo-us-paid)

</div>

[了解更多 :hero-arrow-circle-right-fill:](financial-services.md#payment-masking-services)

#### Online Gift Card Marketplaces

<div class="grid cards" markdown>

- ![Coincards logo](assets/img/financial-services/coincards.svg){ .twemoji loading=lazy } [Coincards](financial-services.md#coincards)

</div>

[了解更多 :hero-arrow-circle-right-fill:](financial-services.md#gift-card-marketplaces)

### Photo Management

<div class="grid cards" markdown>

- ![Ente logo](assets/img/photo-management/ente.svg){ .twemoji loading=lazy } [Ente Photos](photo-management.md#ente-photos)
- ![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ .twemoji loading=lazy } [PhotoPrism](photo-management.md#photoprism)

</div>

[了解更多 :hero-arrow-circle-right-fill:](photo-management.md)

### Search Engines

<div class="grid cards" markdown>

- ![Brave Search logo](assets/img/search-engines/brave-search.svg){ .twemoji loading=lazy } [Brave Search](search-engines.md#brave-search)
- ![DuckDuckGo logo](assets/img/search-engines/duckduckgo.svg){ .twemoji loading=lazy } [DuckDuckGo](search-engines.md#duckduckgo)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji loading=lazy } [Mullvad Leta](search-engines.md#mullvad-leta)
- ![SearXNG logo](assets/img/search-engines/searxng.svg){ .twemoji loading=lazy } [SearXNG](search-engines.md#searxng)
- ![Startpage logo](assets/img/search-engines/startpage.svg#only-light){ .twemoji loading=lazy }![Startpage logo](assets/img/search-engines/startpage-dark.svg#only-dark){ .twemoji loading=lazy } [Startpage](search-engines.md#startpage)

</div>

[了解更多 :hero-arrow-circle-right-fill:](search-engines.md)

## Software

### AI Chat

<div class="grid cards" markdown>

- ![Kobold logo](assets/img/ai-chat/kobold.png){ .twemoji loading=lazy } [Kobold.cpp](ai-chat.md#koboldcpp)
- ![Llamafile logo](assets/img/ai-chat/llamafile.webp){ .twemoji loading=lazy } [Llamafile](ai-chat.md#llamafile)
- ![Ollama logo](assets/img/ai-chat/ollama.png){ .twemoji loading=lazy } [Ollama (CLI)](ai-chat.md#ollama-cli)

</div>

[了解更多 :hero-arrow-circle-right-fill:](ai-chat.md)

### VPN供应商

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](calendar.md#tuta)
- ![Proton Calendar logo](assets/img/calendar/proton-calendar.svg){ .twemoji loading=lazy } [Proton Calendar](calendar.md#proton-calendar)

</div>

[了解更多 :hero-arrow-circle-right-fill:](calendar.md)

### Cryptocurrency

<div class="grid cards" markdown>

- ![Monero logo](assets/img/cryptocurrency/monero.svg){ .twemoji loading=lazy } [Monero](cryptocurrency.md#monero)

</div>

[了解更多 :hero-arrow-circle-right-fill:](cryptocurrency.md)

### Data and Metadata Redaction

<div class="grid cards" markdown>

- ![MAT2 logo](assets/img/data-redaction/mat2.svg){ .twemoji loading=lazy } [MAT2](data-redaction.md#mat2)
- ![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ .twemoji loading=lazy } [ExifEraser (Android)](data-redaction.md#exiferaser-android)
- ![ExifTool logo](assets/img/data-redaction/exiftool.png){ .twemoji loading=lazy } [ExifTool (CLI)](data-redaction.md#exiftool-cli)

</div>

[了解更多 :hero-arrow-circle-right-fill:](data-redaction.md)

### Document Collaboration

<div class="grid cards" markdown>

- ![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud (Self-Hostable)](document-collaboration.md#nextcloud)
- ![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ .twemoji loading=lazy } [CryptPad](document-collaboration.md#cryptpad)

</div>

[了解更多 :hero-arrow-circle-right-fill:](document-collaboration.md)

### 加密软件

<details class="info" markdown>
<summary>Operating System Encryption</summary>

For encrypting your OS drive, we typically recommend using the encryption tool your operating system provides, whether that is **BitLocker** on Windows, **FileVault** on macOS, or **LUKS** on Linux. These tools are included with the operating system and take advantage of hardware encryption elements such as a [secure cryptoprocessor](basics/hardware.md/#tpmsecure-cryptoprocessor).

[了解更多 :hero-arrow-circle-right-fill:](encryption.md#operating-system-encryption)

</details>

#### Cross-Platform Tools

<div class="grid cards" markdown>

- ![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ .twemoji loading=lazy } [Cryptomator](encryption.md#cryptomator-cloud)
- ![Picocrypt logo](assets/img/encryption-software/picocrypt.svg){ .twemoji loading=lazy } [Picocrypt](encryption.md#picocrypt-file)
- ![VeraCrypt logo](assets/img/encryption-software/veracrypt.svg#only-light){ .twemoji loading=lazy }![VeraCrypt logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ .twemoji loading=lazy } [VeraCrypt (FDE)](encryption.md#veracrypt-disk)
- ![Kryptor logo](assets/img/encryption-software/kryptor.png){ .twemoji loading=lazy } [Kryptor](encryption.md#kryptor)
- ![Tomb logo](assets/img/encryption-software/tomb.png){ .twemoji loading=lazy } [Tomb](encryption.md#tomb)

</div>

[了解更多 :hero-arrow-circle-right-fill:](encryption.md)

#### OpenPGP Clients

<div class="grid cards" markdown>

- ![GnuPG logo](assets/img/encryption-software/gnupg.svg){ .twemoji loading=lazy } [GnuPG](encryption.md#gnu-privacy-guard)
- ![GPG4Win logo](assets/img/encryption-software/gpg4win.svg){ .twemoji loading=lazy } [GPG4Win (Windows)](encryption.md#gpg4win)
- ![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ .twemoji loading=lazy } [GPG Suite (macOS)](encryption.md#gpg-suite)
- ![OpenKeychain logo](assets/img/encryption-software/openkeychain.svg){ .twemoji loading=lazy } [OpenKeychain](encryption.md#openkeychain)

</div>

[了解更多 :hero-arrow-circle-right-fill:](encryption.md#openpgp)

### 加密软件

<div class="grid cards" markdown>

- ![Send logo](assets/img/file-sharing-sync/send.svg){ .twemoji loading=lazy } [Send](file-sharing.md#send)
- ![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ .twemoji loading=lazy } [OnionShare](file-sharing.md#onionshare)
- ![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ .twemoji loading=lazy } [FreedomBox](file-sharing.md#freedombox)
- ![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ .twemoji loading=lazy } [Nextcloud (Self-Hostable)](file-sharing.md#nextcloud-client-server)
- ![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ .twemoji loading=lazy } [Syncthing](file-sharing.md#syncthing-p2p)

</div>

[了解更多 :hero-arrow-circle-right-fill:](file-sharing.md)

### 文件共享

<div class="grid cards" markdown>

- ![Redlib logo](assets/img/frontends/redlib.svg){ .twemoji loading=lazy } [Redlib (Reddit, Web)](frontends.md#redlib)
- ![ProxiTok logo](assets/img/frontends/proxitok.svg){ .twemoji loading=lazy } [ProxiTok (TikTok, Web)](frontends.md#proxitok)
- ![FreeTube logo](assets/img/frontends/freetube.svg){ .twemoji loading=lazy } [FreeTube (YouTube, Desktop)](frontends.md#freetube)
- ![Yattee logo](assets/img/frontends/yattee.svg){ .twemoji loading=lazy } [Yattee (YouTube; iOS, tvOS, macOS)](frontends.md#yattee)
- ![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ .twemoji loading=lazy }![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ .twemoji loading=lazy } [LibreTube (YouTube, Android)](frontends.md#libretube-android)
- ![NewPipe logo](assets/img/frontends/newpipe.svg){ .twemoji loading=lazy } [NewPipe (YouTube, Android)](frontends.md#newpipe-android)
- ![Invidious logo](assets/img/frontends/invidious.svg#only-light){ .twemoji loading=lazy }![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ .twemoji loading=lazy } [Invidious (YouTube, Web)](frontends.md#invidious)
- ![Piped logo](assets/img/frontends/piped.svg){ .twemoji loading=lazy } [Piped (YouTube, Web)](frontends.md#piped)

</div>

[了解更多 :hero-arrow-circle-right-fill:](frontends.md)

### Health and Wellness Apps

<div class="grid cards" markdown>

- ![Drip logo](assets/img/health-and-wellness/drip.png){ .twemoji loading=lazy } [Drip](health-and-wellness.md#drip)
- ![Euki logo](assets/img/health-and-wellness/euki.svg){ .twemoji loading=lazy } [Euki](health-and-wellness.md#euki)
- ![Apple Health logo](assets/img/health-and-wellness/apple-health.svg#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/img/health-and-wellness/apple-health-dark.svg#only-dark){ .twemoji loading=lazy } [Apple Health](health-and-wellness.md#apple-health)
- ![Gadgetbridge logo](assets/img/health-and-wellness/gadgetbridge.svg#only-light){ .twemoji loading=lazy }![Gadgetbridge logo](assets/img/health-and-wellness/gadgetbridge-dark.svg#only-dark){ .twemoji loading=lazy } [Gadgetbridge](health-and-wellness.md#gadgetbridge)
- ![Apple Health logo](assets/img/health-and-wellness/apple-health.svg#only-light){ .twemoji loading=lazy } ![Apple Health logo](assets/img/health-and-wellness/apple-health-dark.svg#only-dark){ .twemoji loading=lazy } [Apple Health Records](health-and-wellness.md#apple-health-records)
- ![CommonHealth logo](assets/img/health-and-wellness/commonhealth.png){ .twemoji loading=lazy } [CommonHealth](health-and-wellness.md#commonhealth)

</div>

[了解更多 :hero-arrow-circle-right-fill:](health-and-wellness.md)

### Language Tools

<div class="grid cards" markdown>

- ![LanguageTool logo](assets/img/language-tools/languagetool.svg#only-light){ .twemoji loading=lazy }![LanguageTool logo](assets/img/language-tools/languagetool-dark.svg#only-dark){ .twemoji loading=lazy } [LanguageTool](language-tools.md#languagetool)

</div>

[了解更多 :hero-arrow-circle-right-fill:](language-tools.md)

### Maps and Navigation Apps

<div class="grid cards" markdown>

- ![Organic Maps logo](assets/img/maps/organic-maps.svg){ .twemoji loading=lazy } [Organic Maps](maps.md#organic-maps)
- ![OsmAnd logo](assets/img/maps/osmand.svg){ .twemoji loading=lazy } [OsmAnd](maps.md#osmand)

</div>

[了解更多 :hero-arrow-circle-right-fill:](maps.md)

### 数据和元数据处理

**Note:** [Hardware security keys](#security-keys) have been moved to their own category.

<div class="grid cards" markdown>

- ![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ .twemoji loading=lazy } [Ente Auth](multi-factor-authentication.md#ente-auth)
- ![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ .twemoji loading=lazy } [Aegis Authenticator (Android)](multi-factor-authentication.md#aegis-authenticator-android)

</div>

[了解更多 :hero-arrow-circle-right-fill:](multi-factor-authentication.md)

### 多因素认证工具

<div class="grid cards" markdown>

- ![Akregator logo](assets/img/news-aggregators/akregator.svg){ .twemoji loading=lazy } [Akregator](news-aggregators.md#akregator)
- ![NewsFlash logo](assets/img/news-aggregators/newsflash.png){ .twemoji loading=lazy } [NewsFlash](news-aggregators.md#newsflash)
- ![Feeder logo](assets/img/news-aggregators/feeder.png){ .twemoji} [Feeder (Android)](news-aggregators.md#feeder)
- ![Miniflux logo](assets/img/news-aggregators/miniflux.svg#only-light){ .twemoji loading=lazy }![Miniflux logo](assets/img/news-aggregators/miniflux-dark.svg#only-dark){ .twemoji loading=lazy } [Miniflux](news-aggregators.md#miniflux)
- ![NetNewsWire logo](assets/img/news-aggregators/netnewswire.png){ .twemoji loading=lazy } [NetNewsWire](news-aggregators.md#netnewswire)
- ![Newsboat logo](assets/img/news-aggregators/newsboat.svg){ .twemoji loading=lazy } [Newsboat](news-aggregators.md#newsboat)

</div>

[了解更多 :hero-arrow-circle-right-fill:](news-aggregators.md)

### Notebooks

<div class="grid cards" markdown>

- ![Standard Notes logo](assets/img/notebooks/standard-notes.svg){ .twemoji loading=lazy } [Standard Notes](notebooks.md#standard-notes)
- ![Notesnook logo](assets/img/notebooks/notesnook.svg){ .twemoji loading=lazy } [Notesnook](notebooks.md#notesnook)
- ![Joplin logo](assets/img/notebooks/joplin.svg){ .twemoji loading=lazy } [Joplin](notebooks.md#joplin)
- ![Cryptee logo](assets/img/notebooks/cryptee.svg#only-light){ .twemoji loading=lazy }![Cryptee logo](assets/img/notebooks/cryptee-dark.svg#only-dark){ .twemoji loading=lazy } [Cryptee](notebooks.md#cryptee)
- ![Org-mode logo](assets/img/notebooks/org-mode.svg){ .twemoji loading=lazy } [Org-mode](notebooks.md#org-mode)

</div>

[了解更多 :hero-arrow-circle-right-fill:](notebooks.md)

### Office Suites

<div class="grid cards" markdown>

- ![LibreOffice logo](assets/img/office-suites/libreoffice.svg){ .twemoji loading=lazy } [LibreOffice](office-suites.md#libreoffice)
- ![OnlyOffice logo](assets/img/office-suites/onlyoffice.svg){ .twemoji loading=lazy } [OnlyOffice](office-suites.md#onlyoffice)

</div>

[了解更多 :hero-arrow-circle-right-fill:](office-suites.md)

### 生产力工具

<div class="grid cards" markdown>

- ![Bitwarden logo](assets/img/password-management/bitwarden.svg){ .twemoji loading=lazy } [Bitwarden](passwords.md#bitwarden)
- ![Proton Pass logo](assets/img/password-management/protonpass.svg){ .twemoji loading=lazy } [Proton Pass](passwords.md#proton-pass)
- ![1Password logo](assets/img/password-management/1password.svg){ .twemoji loading=lazy } [1Password](passwords.md#1password)
- ![Psono logo](assets/img/password-management/psono.svg){ .twemoji loading=lazy } [Psono](passwords.md#psono)
- ![KeePassXC logo](assets/img/password-management/keepassxc.svg){ .twemoji loading=lazy } [KeePassXC](passwords.md#keepassxc)
- ![KeePassDX logo](assets/img/password-management/keepassdx.svg){ .twemoji loading=lazy } [KeePassDX (Android)](passwords.md#keepassdx-android)
- ![Gopass logo](assets/img/password-management/gopass.svg){ .twemoji loading=lazy } [Gopass (CLI)](passwords.md#gopass-cli)

</div>

[了解更多 :hero-arrow-circle-right-fill:](passwords.md)

### Pastebins

<div class="grid cards" markdown>

- ![PrivateBin logo](assets/img/pastebins/privatebin.svg){ .twemoji loading=lazy } [PrivateBin](pastebins.md#privatebin)
- ![Paaster logo](assets/img/pastebins/paaster.svg){ .twemoji loading=lazy } [Paaster](pastebins.md#paaster)

</div>

[了解更多 :hero-arrow-circle-right-fill:](pastebins.md)

### 实时通讯

<div class="grid cards" markdown>

- ![Signal logo](assets/img/messengers/signal.svg){ .twemoji loading=lazy } [Signal](real-time-communication.md#signal)
- ![Briar logo](assets/img/messengers/briar.svg){ .twemoji loading=lazy } [Briar](real-time-communication.md#briar)
- ![SimpleX Chat logo](assets/img/messengers/simplex.svg){ .twemoji loading=lazy } [SimpleX Chat](real-time-communication.md#simplex-chat)

</div>

[了解更多 :hero-arrow-circle-right-fill:](real-time-communication.md)

### Social Networks

<div class="grid cards" markdown>

- ![Mastodon logo](assets/img/social-networks/mastodon.svg){ .twemoji loading=lazy } [Mastodon](social-networks.md#mastodon)
- ![Element logo](assets/img/social-networks/element.svg){ .twemoji loading=lazy } [Element](social-networks.md#element)

</div>

[了解更多 :hero-arrow-circle-right-fill:](social-networks.md)

## Hardware

### Security Keys

<div class="grid cards" markdown>

- ![Yubico logo](assets/img/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [Yubico Security Key](security-keys.md#yubico-security-key)
- ![Yubico logo](assets/img/security-keys/mini/yubico.svg){ .twemoji loading=lazy } [YubiKey](security-keys.md#yubikey)
- ![Nitrokey](assets/img/security-keys/mini/nitrokey.svg){ .twemoji loading=lazy } [Nitrokey](security-keys.md#nitrokey)

</div>

[了解更多 :hero-arrow-circle-right-fill:](security-keys.md)

### Mobile Phones

<div class="grid cards" markdown>

- ![Google Pixel 6](assets/img/android/google-pixel.png){ .twemoji loading=lazy } [Google Pixel](mobile-phones.md#google-pixel)

</div>

[了解更多 :hero-arrow-circle-right-fill:](mobile-phones.md)

## 服务供应商

### Android

#### Custom Android Operating Systems

<div class="grid cards" markdown>

- ![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ .twemoji loading=lazy }![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ .twemoji loading=lazy } [GrapheneOS](android/distributions.md#grapheneos)

</div>

[了解更多 :hero-arrow-circle-right-fill:](android/distributions.md)

#### Android Apps

<div class="grid cards" markdown>

- ![Shelter logo](assets/img/android/mini/shelter.svg){ .twemoji loading=lazy } [Shelter (Work Profiles)](android/general-apps.md#shelter)
- ![Secure Camera logo](assets/img/android/secure_camera.svg#only-light){ .twemoji loading=lazy }![Secure Camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ .twemoji loading=lazy } [Secure Camera](android/general-apps.md#secure-camera)
- ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ .twemoji loading=lazy }![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ .twemoji loading=lazy } [Secure PDF Viewer](android/general-apps.md#secure-pdf-viewer)

</div>

[了解更多 :hero-arrow-circle-right-fill:](android/general-apps.md)

#### Ways to Obtain Android Apps

<div class="grid cards" markdown>

- ![Obtainium logo](assets/img/android/obtainium.svg){ .twemoji loading=lazy } [Obtainium (App Manager)](android/obtaining-apps.md#obtainium)
- ![Aurora Store logo](assets/img/android/aurora-store.webp){ .twemoji loading=lazy } [Aurora Store (Google Play Client)](android/obtaining-apps.md#aurora-store)

</div>

[了解更多 :hero-arrow-circle-right-fill:](android/obtaining-apps.md)

### Android 应用

<div class="grid cards" markdown>

- ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ .twemoji loading=lazy } [Qubes OS (Xen VM Distribution)](desktop.md#qubes-os)
- ![Fedora logo](assets/img/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Linux](desktop.md#fedora-linux)
- ![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ .twemoji loading=lazy } [openSUSE Tumbleweed](desktop.md#opensuse-tumbleweed)
- ![Arch logo](assets/img/linux-desktop/archlinux.svg){ .twemoji loading=lazy } [Arch Linux](desktop.md#arch-linux)
- ![Fedora logo](assets/img/linux-desktop/fedora.svg){ .twemoji loading=lazy } [Fedora Atomic Desktops](desktop.md#fedora-atomic-desktops)
- ![NixOS logo](assets/img/linux-desktop/nixos.svg){ .twemoji loading=lazy } [NixOS](desktop.md#nixos)
- ![Whonix logo](assets/img/linux-desktop/whonix.svg){ .twemoji loading=lazy } [Whonix (Tor)](desktop.md#whonix)
- ![Tails logo](assets/img/linux-desktop/tails.svg){ .twemoji loading=lazy } [Tails (Live Boot)](desktop.md#tails)
- ![Secureblue logo](assets/img/linux-desktop/secureblue.svg){ .twemoji loading=lazy } [Secureblue](desktop.md#secureblue)
- ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ .twemoji loading=lazy } [Kicksecure](desktop.md#kicksecure)

</div>

[了解更多 :hero-arrow-circle-right-fill:](desktop.md)

### Router Firmware

<div class="grid cards" markdown>

- ![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ .twemoji loading=lazy }![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ .twemoji loading=lazy } [OpenWrt](router.md#openwrt)
- ![OPNsense logo](assets/img/router/opnsense.svg){ .twemoji loading=lazy } [OPNsense](router.md#opnsense)

</div>

[了解更多 :hero-arrow-circle-right-fill:](router.md)

## Advanced Tools

These tools may provide utility for certain individuals. They provide functionality which most people do not need to worry about, and often require more in-depth technical knowledge to utilize effectively.

### Alternative Networks

<div class="grid cards" markdown>

- ![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ .twemoji loading=lazy } ![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ .twemoji loading=lazy } [I2P](alternative-networks.md#i2p-the-invisible-internet-project)
- ![Tor logo](assets/img/self-contained-networks/tor.svg){ .twemoji loading=lazy } [Tor](alternative-networks.md#tor)
- ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ .twemoji loading=lazy } [Orbot (Mobile Tor Proxy)](alternative-networks.md#orbot)
- ![Snowflake logo](assets/img/self-contained-networks/snowflake.svg#only-light){ .twemoji loading=lazy }![Snowflake logo](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ .twemoji loading=lazy } [Snowflake](alternative-networks.md#snowflake)

</div>

[了解更多 :hero-arrow-circle-right-fill:](alternative-networks.md)

### Device Integrity Verification

<div class="grid cards" markdown>

- ![MVT logo](assets/img/device-integrity/mvt.webp#only-light){ .twemoji loading=lazy }![MVT logo](assets/img/device-integrity/mvt-dark.png#only-dark){ .twemoji loading=lazy } [Mobile Verification Toolkit](device-integrity.md#mobile-verification-toolkit)
- ![iMazing logo](assets/img/device-integrity/imazing.png){ .twemoji loading=lazy } [iMazing (iOS)](device-integrity.md#imazing-ios)
- ![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ .twemoji loading=lazy }![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ .twemoji loading=lazy } [Auditor (Android)](device-integrity.md#auditor-android)

</div>

[了解更多 :hero-arrow-circle-right-fill:](device-integrity.md)
