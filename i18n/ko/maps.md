---
meta_title: "추천 지도 및 내비게이션 앱 - 프라이버시 가이드"
title: 지도 및 내비게이션
icon: material/map
description: 검색 기록과 위치를 바탕으로 광고 프로필을 만들지 않는, 프라이버시를 존중하는 지도 제공업체와 내비게이션 앱입니다.
cover: maps.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

검색 기록과 위치 기록을 바탕으로 광고 프로필을 만들지 않는 **지도 및 내비게이션 앱**을 사용하세요. 구글 지도, 애플 지도, 웨이즈 대신 프라이버시를 존중하는 다음 대안을 추천합니다.

각 애플리케이션의 개인정보 처리방침에 따르면 여기서 추천하는 앱은 개인 식별 정보(PII)를 수집하지 않습니다. 이러한 개인정보 처리방침이 지켜진다는 **보장은 없습니다**.

## 오가닉 맵스 { #organic-maps }

<div class="admonition recommendation" markdown>

![오가닉 맵스 로고](assets/img/maps/organic-maps.svg){ align=right }

**오가닉 맵스**는 도보 이용자, 운전자, 자전거 이용자를 위한 커뮤니티 개발 오픈 소스 지도 표시 및 위성 내비게이션 방식의 길 안내 앱입니다. 오픈스트리트맵 데이터를 기반으로 전 세계 오프라인 지도를 제공하며, 위치 추적, 데이터 수집, 광고 없이 프라이버시를 지키는 길 안내를 제공합니다. 앱을 완전히 오프라인으로 사용할 수 있습니다.

주요 기능으로는 자전거 경로, 등산로 및 산책로, 음성 안내가 포함된 턴바이턴 길 안내, 대중교통 경로 계획(지원되는 지역과 도시에서만 사용 가능) 등이 있습니다.

[:octicons-home-16: 홈페이지](https://organicmaps.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://organicmaps.app/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-code-16:](https://github.com/organicmaps/organicmaps){ .card-link title="소스 코드" }

<details class="downloads" markdown><summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=app.organicmaps)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/organic-maps/id1567437057)
- [:simple-github: 깃허브](https://github.com/organicmaps/organicmaps/releases)
- [:simple-linux: 리눅스](https://flathub.org/apps/app.organicmaps.desktop)

</details>

</div>

오가닉 맵스는 위성 이미지, 거리뷰 이미지, 실시간 교통 정보처럼 많은 사용자가 기대할 만한 일부 기능이 없는 단순하고 기본적인 앱이라는 점에 유의하세요.

## OsmAnd

<div class="admonition recommendation" markdown>

![OsmAnd 로고](assets/img/maps/osmand.svg){ align=right }

**OsmAnd**는 오픈스트리트맵을 기반으로 하는 오픈 소스 오프라인 지도 및 내비게이션 애플리케이션으로, 도보, 자전거, 운전은 물론 대중교통에 대한 턴바이턴 길 안내를 제공합니다. OsmAnd가 지원하는 [기능](https://wiki.openstreetmap.org/wiki/OsmAnd#Features)에 대한 자세한 개요는 오픈스트리트맵 위키에서 확인할 수 있습니다.

[:octicons-home-16: 홈페이지](https://osmand.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://osmand.net/docs/legal/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://osmand.net/docs/intro){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/osmandapp){ .card-link title="소스 코드" }

<details class="downloads" markdown><summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=net.osmand)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/us/app/id934850257)
- [:simple-android: 안드로이드](https://osmand.net/docs/versions/free-versions)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">고유 사용자 식별자</p>

OsmAnd는 앱 설치마다 [고유 사용자 식별자(UUID)](https://osmand.net/docs/legal/terms-of-use/#6-unique-user-indentifier)를 생성하는데, 이 식별자는 3개월마다 바뀌며 내부 보고서와 통계에 사용됩니다. UUID는 지도를 다운로드할 때도 OsmAnd 서버로 전송됩니다. 안드로이드에는 다운로드 요청마다 UUID를 함께 보낼지 제어하는 설정이 있습니다. 홈 화면에서 :material-menu: → :gear: **설정** → :gear: **OsmAnd 설정** → :material-web: **식별자**로 이동하세요.

- [ ] **고유 사용자 식별자(UUID) 보내기**(Send Unique User Identifier) 선택 해제

iOS 앱에는 이 설정이 없습니다.

</div>

앱에는 다운로드한 지도와 사용하는 기능에 관한 익명 데이터를 공유하는 설정도 있습니다. 이 설정은 안드로이드에서는 기본적으로 비활성화되어 있지만, iOS에서는 기본적으로 활성화되어 있습니다. iOS 앱에서 이를 비활성화하려면 홈 화면에서 :material-menu:을 탭해 :gear: **설정** 메뉴를 찾으세요. 이를 선택한 다음 :gear: **OsmAnd 설정**을 선택하세요.

- [ ] **익명 데이터 보내기**(Send anonymous data) 선택 해제

OsmAnd에서는 마이크로소프트의 위성 이미지나 구글의 [교통 데이터](https://themm.net/public/osmand_traffic) 같은 외부 지도 데이터를 겹치거나 아래에 깔아 표시할 수 있지만, 후자는 자동 경로 계획에 반영되지 않습니다. OsmAnd는 [매필러리](https://mapillary.com)가 제공하는 거리뷰 이미지를 선택적으로 연동하는 기능도 제공합니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 개인정보 처리방침에 따라 PII를 수집하지 않아야 합니다.
- 사용자에게 계정 생성을 요구해서는 안 됩니다.
- 사용자에게 위치 데이터 공유를 요구해서는 안 됩니다. 사용자가 위치 공유를 선택한 경우, 해당 데이터는 익명화되어야 합니다.
- 오프라인에서도 핵심 기능을 유지해야 하며, 사용자가 오프라인 사용을 위해 지도를 다운로드할 수 있어야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 앱은 오픈 소스인 것이 좋습니다.
- 대중교통 경로 계획을 지원하는 것이 좋습니다.
- 경로 계획을 위한 실시간 교통 정보를 제공하는 것이 좋습니다.
- 상세한 상점/관심 지점(POI) 정보 및 리뷰, 지형도, 위성 및 거리뷰 이미지 같은 고급 기능을 지원하는 것이 좋습니다.
