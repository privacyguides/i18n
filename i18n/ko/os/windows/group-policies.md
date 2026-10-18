---
title: 그룹 정책 설정
description: 윈도우를 조금 더 프라이버시 친화적으로 만들기 위한 그룹 정책 구성 빠른 가이드입니다.
---

레지스트리를 직접 수정하는 것을 제외하면, **로컬 그룹 정책 편집기**는 서드파티 도구를 설치하지 않고 시스템의 여러 측면을 변경할 수 있는 가장 강력한 방법입니다. 이 설정을 변경하려면 [프로 에디션](index.md#windows-editions) 이상이 필요합니다.

이 설정은 윈도우를 새로 설치한 상태에서 적용해야 합니다. 기존 설치에 적용해도 작동은 하겠지만, 예측할 수 없는 동작이 발생할 수 있으므로 본인 책임하에 진행해야 합니다.

이 모든 설정에는 그룹 정책 편집기에 각 설정이 정확히 무엇을 하는지 대개 매우 자세히 알려 주는 설명이 첨부되어 있습니다. 변경할 때 이 설명을 잘 읽어 보고, 여기서 무엇을 권장하는지 정확히 이해하도록 하세요. 또한 윈도우에 포함된 설명이 불충분한 경우에는 아래에서 일부 선택에 대해 설명을 덧붙였습니다.

## 관리 템플릿 { #administrative-templates }

`gpedit.msc`를 열고 왼쪽 사이드바에서 **로컬 컴퓨터 정책** > **컴퓨터 구성** > **관리 템플릿**으로 이동하면 이러한 설정을 찾을 수 있습니다. 이 페이지의 제목은 관리 템플릿 안의 폴더/하위 폴더에 해당하며, 글머리 기호 항목은 개별 정책에 해당합니다.

그룹 정책을 변경하려면 해당 정책을 두 번 클릭하고, 아래 권장 사항에 따라 나타나는 창의 상단에서 사용 또는 사용 안 함을 선택하세요. 일부 그룹 정책에는 구성할 수 있는 추가 설정이 있으며, 이 경우 해당 설정도 아래에 함께 기재했습니다.

### 시스템 { #system }

#### Device Guard

- 가상화 기반 보안 켜기(Turn On Virtualization Based Security): **사용**
  - 플랫폼 보안 수준(Platform Security Level): **보안 부팅 및 DMA 보호**
  - 보안 시작 구성(Secure Launch Configuration): **사용**

#### 인터넷 통신 관리 { #internet-communication-management }

- Windows 사용자 환경 개선 프로그램 끄기(Turn off Windows Customer Experience Improvement Program): **사용**
- Windows 오류 보고 끄기(Turn off Windows Error Reporting): **사용**
- Windows Messenger 사용자 환경 개선 프로그램 끄기(Turn off the Windows Messenger Customer Experience Improvement Program): **사용**

Windows 사용자 환경 개선 프로그램을 비활성화하면 그룹 정책으로 개별 제어할 수 있는 다른 추적 기능 일부도 함께 비활성화된다는 점에 유의하세요. 이 설정이 해당 기능들을 포괄하므로 여기에 모두 나열하거나 개별적으로 비활성화하지는 않았습니다.

#### OS 정책 { #os-policies }

- 클립보드 기록 허용(Allow Clipboard History): **사용 안 함**
- 장치 간 클립보드 동기화 허용(Allow Clipboard synchronization across devices): **사용 안 함**
- 활동 피드 사용(Enables Activity Feed): **사용 안 함**
- 사용자 활동 게시 허용(Allow publishing of User Activities): **사용 안 함**
- 사용자 활동 업로드 허용(Allow upload of User Activities): **사용 안 함**

#### 사용자 프로필 { #user-profiles }

- 광고 ID 끄기(Turn off the advertising ID): **사용**

### Windows 구성 요소 { #windows-components }

#### 자동 실행 정책 { #autoplay-policies }

자동 실행(AutoRun)과 자동 재생(AutoPlay)은 장치가 연결되었을 때 윈도우가 스크립트를 실행하거나 기타 작업을 수행하도록 하는 기능으로, 사용자 동의를 요구하는 보안 조치를 우회하기도 합니다. 이로 인해 신뢰할 수 없는 장치가 여러분 모르게 악성 코드를 실행할 수 있습니다. 이러한 기능을 비활성화하고 외장 디스크의 파일은 직접 여는 것이 보안 모범 사례입니다.

- 자동 실행 끄기(Turn off AutoPlay): **사용**
- 볼륨이 아닌 장치에 대해 자동 실행 허용 안 함(Disallow Autoplay for nonvolume devices): **사용**
- 자동 실행의 기본 동작 설정(Set the default behavior for AutoRun): **사용**
  - 기본 자동 실행 동작(Default AutoRun Behavior): **자동 실행 명령 실행 안 함**(Do not execute any AutoRun commands)

#### BitLocker 드라이브 암호화 { #bitlocker-drive-encryption }

이 설정을 변경한 후에는 운영 체제 드라이브를 다시 암호화하는 것이 좋을 수 있습니다.

- 드라이브 암호화 방법 및 암호화 강도 선택(Choose drive encryption method and cipher strength) (Windows Vista, Windows Server 2008, Windows 7): **사용**
  - 암호화 방법 선택(Select the encryption method): **AES-256**

Windows 7 정책에 암호화 강도를 설정하면 최신 버전의 윈도우에도 해당 강도가 그대로 적용됩니다.

##### 운영 체제 드라이브 { #operating-system-drives }

- 시작 시 추가 인증 요구(Require additional authentication at startup): **사용**
- 시작 시 고급 PIN 허용(Allow enhanced PINs for startup): **사용**

정책 이름과 달리 이 설정은 기본적으로 아무것도 _요&#xAD6C;_&#xD558;지 않지만, BitLocker 설정 마법사에서 (시작 시 TPM과 함께 PIN 요구 같은) 더 복잡한 설정을 할 수 있는 _옵&#xC158;_&#xC744; 활성화합니다.

#### 클라우드 콘텐츠 { #cloud-content }

- 클라우드 최적화 콘텐츠 끄기(Turn off cloud optimized content): **사용**
- 클라우드 소비자 계정 상태 콘텐츠 끄기(Turn off cloud consumer account state content): **사용**
- Windows 팁 표시 안 함(Do not show Windows tips): **사용**
- Microsoft 소비자 환경 끄기(Turn off Microsoft consumer experiences): **사용**

#### 자격 증명 사용자 인터페이스 { #credential-user-interface }

- 자격 증명 입력에 신뢰할 수 있는 경로 필요(Require trusted path for credential entry): **사용**
- 로컬 계정에 보안 질문 사용 금지(Prevent the use of security questions for local accounts): **사용**

#### 데이터 수집 및 미리 보기 빌드 { #data-collection-and-preview-builds }

- 진단 데이터 허용(Allow Diagnostic Data): **사용**
  - 옵션: **필수 진단 데이터 보내기**(Send required diagnostic data) (프로 에디션) 또는
  - 옵션: **진단 데이터 끄기**(Diagnostic data off) (엔터프라이즈 또는 에듀케이션 에디션)
- 진단 로그 수집 제한(Limit Diagnostic Log Collection): **사용**
- 덤프 수집 제한(Limit Dump Collection): **사용**
- 데스크톱 분석에 대한 선택적 진단 데이터 제한(Limit optional diagnostic data for Desktop Analytics): **사용**
  - 옵션: **데스크톱 분석 수집 사용 안 함**(Disable Desktop Analytics collection)
- 피드백 알림 표시 안 함(Do not show feedback notifications): **사용**

#### 파일 탐색기 { #file-explorer }

- 파일 탐색기에서 계정 기반 인사이트, 최근 파일, 즐겨찾기 파일, 추천 파일 끄기(Turn off account-based insights, recent, favorite, and recommended files in File Explorer): **사용**

#### MDM

- MDM 등록 사용 안 함(Disable MDM Enrollment): **사용**

#### OneDrive

- 기본적으로 OneDrive에 문서 저장(Save documents to OneDrive by default): **사용 안 함**
- 사용자가 OneDrive에 로그인할 때까지 OneDrive에서 네트워크 트래픽을 생성하지 않도록 방지(Prevent OneDrive from generating network traffic until the user signs in to OneDrive): **사용**
- 파일 저장소로 OneDrive 사용 방지(Prevent the usage of OneDrive for file storage): **사용**

마지막 설정은 시스템에서 원드라이브를 비활성화하므로, 원드라이브를 사용한다면 **사용 안 함**으로 변경하세요.

#### 푸시하여 설치 { #push-to-install }

- 푸시하여 설치 서비스 끄기(Turn off Push To Install service): **사용**

#### 검색 { #search }

- Cortana 허용(Allow Cortana): **사용 안 함**
- 웹을 검색하거나 검색에 웹 결과 표시 안 함(Don't search the web or display web results in Search): **사용**
- 검색에서 공유되는 정보 설정(Set what information is shared in Search): **사용**
  - 정보 유형(Type of information): **익명 정보**(Anonymous info)

#### 설정 동기화 { #sync-your-settings }

- 동기화 안 함(Do not sync): **사용**

#### 텍스트 입력 { #text-input }

- 수동 입력 및 입력 인식 향상(Improve inking and typing recognition): **사용 안 함**

#### Windows AI

<div class="admonition info" markdown>
<p class="admonition-title">Windows Recall</p>

윈도우 11에는 최근 **리콜**이라는 기능이 도입되었는데, 이 기능은 모든 활동을 기록하고 그 활동 기록을 검색할 수 있는 보관 파일을 생성합니다. 이러한 보관 파일에는 매우 민감한 정보(사실상 화면에 표시되는 모든 것)가 저장될 수 있고, 특별한 권한이나 관리자 권한이 없는 멀웨어도 잠금이 해제된 이후에는 언제든지 전체 리콜 데이터베이스에 손쉽게 [접근](https://github.com/xaitax/TotalRecall)할 수 있으므로, 이는 엄청난 프라이버시 취약점입니다.

</div>

- 리콜에 사용할 스냅숏 저장 끄기(Turn off saving snapshots for use with Recall): **사용**

#### Windows 오류 보고 { #windows-error-reporting }

- 추가 데이터 보내지 않기(Do not send additional data): **사용**
- 동의(Consent) > 기본 동의 구성(Configure Default consent): **사용**
  - 동의 수준(Consent level): **데이터를 보내기 전에 항상 확인**(Always ask before sending data)
