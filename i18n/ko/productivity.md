---
title: "생산성 툴"
icon: material/file-sign
description: 온라인 오피스 프로그램은 대부분 E2EE를 제공하지 않으며, 여러분의 작업 파일을 클라우드 제공 업체가 볼 수 있습니다.
cover: productivity.webp
---

온라인 오피스 프로그램은 대부분 E2EE를 제공하지 않으며, 여러분의 작업 파일을 클라우드 제공 업체가 볼 수 있습니다. 여러분의 권리는 프라이버시 정책에 의해 법적으로 보호되지만, 기술적으로 클라우드 제공 업체의 접근을 방지하지는 않습니다.

## 협업 플랫폼

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud 로고](assets/img/productivity/nextcloud.svg){ align=right }

**Nextcloud**는 사용자가 관리하는 개인 서버에서 자기만의 파일 호스팅 서비스를 구축할 수 있는 무료 오픈 소스 클라이언트-서버 소프트웨어 제품군입니다.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
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

[:octicons-home-16: 홈페이지](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE/){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://docs.cryptpad.fr/){ .card-link title=문서}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=기부 }

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

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
- TOTP/FIDO2 다중 인증 혹은 Passkey 로그인을 지원해야 합니다.

## 오피스 제품군

### LibreOffice

<div class="admonition recommendation" markdown>

![LibreOffice 로고](assets/img/productivity/libreoffice.svg){ align=right }

**LibreOffice**는 다양한 기능을 갖춘 무료 오픈 소스 오피스 프로그램 제품군입니다.

[:octicons-home-16: Homepage](https://www.libreoffice.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.libreoffice.org/about-us/privacy/privacy-policy-en/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://documentation.libreoffice.org/en/english-documentation/){ .card-link title=Documentation}
[:octicons-code-16:](https://www.libreoffice.org/about-us/source-code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://www.libreoffice.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://www.libreoffice.org/download/android-and-ios/)
- [:simple-appstore: App Store](https://www.libreoffice.org/download/android-and-ios/)
- [:simple-windows11: Windows](https://www.libreoffice.org/download/download/)
- [:simple-apple: macOS](https://www.libreoffice.org/download/download/)
- [:simple-linux: Linux](https://www.libreoffice.org/download/download/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.libreoffice.LibreOffice)

</details>

</div>

### OnlyOffice

<div class="admonition recommendation" markdown>

![OnlyOffice 로고](assets/img/productivity/onlyoffice.svg){ align=right }

**OnlyOffice**는 클라우드 기반 무료 오픈 소스 오피스 프로그램 제품군입니다. Nextcloud 연동 등 다양한 기능을 제공합니다.

[:octicons-home-16: Homepage](https://www.onlyoffice.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://help.onlyoffice.com/products/files/doceditor.aspx?fileid=5048502&doc=SXhWMEVzSEYxNlVVaXJJeUVtS0kyYk14YWdXTEFUQmRWL250NllHNUFGbz0_IjUwNDg1MDIi0){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://helpcenter.onlyoffice.com/userguides.aspx){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ONLYOFFICE){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onlyoffice.documents)
- [:simple-appstore: App Store](https://apps.apple.com/app/id944896972)
- [:simple-windows11: Windows](https://www.onlyoffice.com/download-desktop.aspx)
- [:simple-apple: macOS](https://www.onlyoffice.com/download-desktop.aspx)
- [:simple-linux: Linux](https://www.onlyoffice.com/download-desktop.aspx)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.onlyoffice.desktopeditors)

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

일반적으로, Privacy Guides에서 선정하는 '오피스 제품군'의 기준은 'Microsoft Word 대신 사용할 만한 애플리케이션'입니다.

- 크로스 플랫폼을 지원해야 합니다.
- 오픈 소스 소프트웨어여야 합니다.
- 오프라인에서 작동해야 합니다.
- 문서, 스프레드시트, 슬라이드쇼 편집을 지원해야 합니다.
- 파일을 표준 문서 형식으로 내보내야 합니다.

## 텍스트 공유 서비스

### PrivateBin

<div class="admonition recommendation" markdown>

![PrivateBin 로고](assets/img/productivity/privatebin.svg){ align=right }

**PrivateBin**은 서버에 어떠한 정보도 공유되지 않는 미니멀한 오픈 소스 온라인 텍스트 공유 서비스입니다. 데이터는 브라우저에서 AES-256으로 암호화/복호화됩니다. ZeroBin을 개선한 버전의 서비스이기도 합니다.

[:octicons-home-16: 홈페이지](https://privatebin.info){ .md-button .md-button--primary }
[:octicons-server-16:](https://privatebin.info/directory/){ .card-link title="공개 인스턴스"}
[:octicons-info-16:](https://github.com/PrivateBin/PrivateBin/wiki/FAQ){ .card-link title=문서}
[:octicons-code-16:](https://github.com/PrivateBin/PrivateBin){ .card-link title="소스 코드" }

</details>

</div>

### 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

#### 최소 요구 사항

- 오픈 소스여야 합니다.
- 'Zero Trust' 종단 간 암호화를 구현해야 합니다.
- 파일을 비밀번호로 보호하는 기능을 지원해야 합니다

#### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 평판이 좋은 독립적인 제3자로부터 공개 감사를 받아야 합니다.
