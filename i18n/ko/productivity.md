---
title: "생산성 툴"
icon: material/file-sign
description: 온라인 오피스 프로그램은 대부분 E2EE를 제공하지 않으며, 여러분의 작업 파일을 클라우드 제공 업체가 볼 수 있습니다.
cover: productivity.webp
---

<!-- markdownlint-disable MD024 -->
온라인 오피스 프로그램은 대부분 E2EE를 제공하지 않으며, 여러분의 작업 파일을 클라우드 제공 업체가 볼 수 있습니다. 여러분의 권리는 프라이버시 정책에 의해 법적으로 보호되지만, 기술적으로 클라우드 제공 업체의 접근을 방지하지는 않습니다.

## 협업 플랫폼

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud 로고](assets/img/productivity/nextcloud.svg){ align=right }

**Nextcloud**는 사용자가 관리하는 개인 서버에서 자기만의 파일 호스팅 서비스를 구축할 수 있는 무료 오픈 소스 클라이언트-서버 소프트웨어 제품군입니다.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Privacy Guides는 Nextcloud용 [E2EE 앱](https://apps.nextcloud.com/apps/end_to_end_encryption)을 사용하는 것을 권장드리지 않습니다. 데이터 손실이 발생할 수 있고, 실험적인 성향이 강하며, 실사용할 만한 품질이 아니기 때문입니다. Nextcloud에는 적절한 E2EE 수단이 존재하지 않기 때문에, Privacy Guides는 타인이 운영하는 Nextcloud 서비스를 사용하는 것을 권장드리지 않습니다.

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad 로고](assets/img/productivity/cryptpad.svg){ align=right }

**CryptPad**는 보편적으로 쓰이는 오피스 툴의 프라이버시 중심 대체제입니다. CryptPad 웹 서비스의 모든 콘텐츠는 종단 간 암호화되며, 다른 사용자와의 공유도 간편합니다.

[:octicons-home-16: Homepage](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=Contribute }

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

#### 최소 요구 사항

일반적으로, Privacy Guides에서 선정하는 '협업 플랫폼'의 기준은 'Google 드라이브 같은 협업 플랫폼을 대체할 수 있을 만한 완전한 제품군'입니다.

- Open source.
- WebDAV를 통한 파일 접근을 지원해야 합니다(종단 간 암호화로 인해 불가능한 경우 제외).
- Linux, macOS, Windows 동기화 클라이언트를 제공해야 합니다.
- 문서 및 스프레드시트 편집을 지원해야 합니다.
- 실시간 문서 협업을 지원해야 합니다.
- 표준 문서 형식(ODF 등)으로 문서 내보내기를 지원해야 합니다.

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 파일 관리는 일반적인 파일 시스템 상에서 이루어져야 합니다.
- Should support TOTP or FIDO2 multi-factor authentication support, or passkey logins.

## 오피스 제품군

### LibreOffice

<div class="admonition recommendation" markdown>

![LibreOffice 로고](assets/img/productivity/libreoffice.svg){ align=right }

**LibreOffice**는 다양한 기능을 갖춘 무료 오픈 소스 오피스 프로그램 제품군입니다.

[:octicons-home-16: Homepage](https://libreoffice.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://libreoffice.org/about-us/privacy/privacy-policy-en){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation){ .card-link title=Documentation}
[:octicons-code-16:](https://libreoffice.org/about-us/source-code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://libreoffice.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://libreoffice.org/download/android-and-ios)
- [:simple-appstore: App Store](https://libreoffice.org/download/android-and-ios)
- [:fontawesome-brands-windows: Windows](https://libreoffice.org/download/download)
- [:simple-apple: macOS](https://libreoffice.org/download/download)
- [:simple-linux: Linux](https://libreoffice.org/download/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)

</details>

</div>

### OnlyOffice

<div class="admonition recommendation" markdown>

![OnlyOffice 로고](assets/img/productivity/onlyoffice.svg){ align=right }

**OnlyOffice**는 클라우드 기반 무료 오픈 소스 오피스 프로그램 제품군입니다. Nextcloud 연동 등 다양한 기능을 제공합니다.

[:octicons-home-16: Homepage](https://onlyoffice.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
- [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
- [:fontawesome-brands-windows: Windows](https://onlyoffice.com/download-desktop.aspx)
- [:simple-apple: macOS](https://onlyoffice.com/download-desktop.aspx)
- [:simple-linux: Linux](https://onlyoffice.com/download-desktop.aspx)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

일반적으로, Privacy Guides에서 선정하는 '오피스 제품군'의 기준은 'Microsoft Word 대신 사용할 만한 애플리케이션'입니다.

- 크로스 플랫폼을 지원해야 합니다.
- 오픈 소스 소프트웨어여야 합니다.
- 오프라인에서 작동해야 합니다.
- 문서, 스프레드시트, 슬라이드쇼 편집을 지원해야 합니다.
- 파일을 표준 문서 형식으로 내보내야 합니다.

## Language services

### LanguageTool

<div class="admonition recommendation" markdown>

![LanguageTool logo](assets/img/productivity/languagetool.svg#only-light){ align=right }
![LanguageTool logo](assets/img/productivity/languagetool-dark.svg#only-dark){ align=right }

**LanguageTool** is a multilingual grammar, style and spell checker that supports more than 20 languages. The software is [self-hostable](https://dev.languagetool.org/http-server), and the extensions do not send your input text to their server.

  LanguageTool offers integration with a variety of [office suites](https://languagetool.org/services#text_editors) and [email clients](https://languagetool.org/services#mail_clients).

[:octicons-home-16: Homepage](https://languagetool.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://languagetool.org/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://languagetooler.freshdesk.com/en/support/solutions){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/languagetool-org){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1534275760)
- [:fontawesome-brands-windows: Windows](https://languagetool.org/windows-desktop)
- [:simple-apple: macOS](https://languagetool.org/mac-desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/languagetool)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/grammar-and-spell-checker/oldceeleldhonbafppcapldpdifcinji)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/hfjadhjooeceemgojogkhlppanjkbobc)
- [:simple-safari: Safari](https://apps.apple.com/app/id1534275760)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- 오픈 소스여야 합니다.
- Must be possible to self-host.
