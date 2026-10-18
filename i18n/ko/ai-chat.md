---
meta_title: "추천 AI 채팅: 프라이버시를 지키는 ChatGPT 대안 - 프라이버시 가이드"
title: "AI 채팅"
icon: material/assistant
description: 오픈AI의 ChatGPT나 빅테크 경쟁 제품과 달리, 이 AI 도구는 로컬에서 실행되므로 데이터가 데스크톱 기기 밖으로 나가지 않습니다.
cover: ai-chatbots.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

대규모 언어 모델(LLM)이라고도 하는 **AI 채팅**은 2022년 ChatGPT가 출시된 이후 점점 더 흔하게 사용되고 있습니다. LLM은 글을 더 잘 쓰거나, 낯선 주제를 이해하거나, 다양한 질문에 답하는 데 도움을 줄 수 있습니다. LLM은 웹에서 수집한 방대한 양의 데이터를 바탕으로 응답의 다음 단어를 통계적으로 예측하는 방식으로 작동합니다.

## LLM의 프라이버시 문제 { #privacy-concerns-about-llms }

하지만 AI 모델 학습에 사용되는 데이터에는 웹에서 수집한 방대한 양의 공개 데이터가 포함되며, 여기에는 이름과 주소 같은 민감한 정보가 포함될 수 있습니다. 클라우드 기반 AI 소프트웨어는 [사용자의 입력을 수집](https://openai.com/policies/row-privacy-policy)하는 경우가 많으므로, 여러분의 채팅은 해당 업체에 대해 비공개가 아닙니다. 이러한 관행은 데이터 유출 위험도 초래합니다. 게다가 LLM이 향후 다른 사용자와의 대화에서 여러분의 비공개 채팅 정보를 유출할 가능성도 실제로 존재합니다.

이러한 관행이 우려된다면 AI 사용을 거부하거나, 학습 데이터 세트를 공개하여 검토할 수 있게 하는 [진정한 오픈 소스 모델](https://proton.me/blog/how-to-build-privacy-first-ai)을 사용할 수 있습니다. 그러한 모델 중 하나로 [Ai2](https://allenai.org/open-data)가 만든 [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514)가 있습니다.

또는 AI 모델을 로컬에서 실행하면 데이터가 기기 밖으로 나가지 않으므로 제3자와 공유되는 일이 없습니다. 따라서 로컬 모델은 클라우드 기반 솔루션보다 프라이버시를 더 잘 보호하고 안전한 대안이며, 걱정 없이 민감한 정보를 AI 모델과 공유할 수 있습니다.

## AI 모델 { #ai-models }

### 로컬 AI 모델을 위한 하드웨어 { #hardware-for-local-ai-models }

로컬 모델은 비교적 쉽게 사용할 수 있습니다. RAM이 8GB밖에 안 되더라도 작은 모델을 느린 속도로 실행할 수 있습니다. VRAM이 충분한 전용 GPU나 빠른 LPDDR5X 메모리를 갖춘 최신 시스템처럼 더 강력한 하드웨어를 사용하면 최상의 경험을 할 수 있습니다.

LLM은 일반적으로 매개변수 수로 구분하며, 최종 사용자가 사용할 수 있는 오픈 소스 모델의 경우 1.3B에서 405B까지 다양합니다. 예를 들어 매개변수가 6.7B 미만인 모델은 텍스트 요약 같은 기본 작업에만 적합하며, 7B에서 13B 사이의 모델은 품질과 속도 사이의 훌륭한 절충안입니다. 고급 추론 능력을 갖춘 모델은 일반적으로 70B 정도입니다.

일반 소비자용 하드웨어에서는 모델 품질과 성능 사이의 균형을 가장 잘 맞추기 위해 [양자화된 모델](https://huggingface.co/docs/optimum/en/concept_guides/quantization)을 사용하는 것이 일반적으로 권장됩니다. 다양한 크기의 양자화된 모델에 대한 일반적인 요구 사항은 아래 표에서 더 자세히 확인할 수 있습니다.

| 모델 크기(매개변수 수) | 최소 RAM | 최소 프로세서                            |
| -------------------------------- | ------ | ---------------------------------- |
| 7B                               | 8 GB   | 최신 CPU(AVX2 지원) |
| 13B                              | 16 GB  | 최신 CPU(AVX2 지원) |
| 70B                              | 72 GB  | VRAM이 있는 GPU                       |

AI를 로컬에서 실행하려면 AI 모델과 AI 클라이언트가 모두 필요합니다.

### 모델 선택하기 { #choosing-a-model }

허용적인 라이선스로 제공되어 다운로드할 수 있는 모델이 많이 있습니다. [허깅 페이스](https://huggingface.co/models)는 [GGUF](https://huggingface.co/docs/hub/en/gguf) 같은 일반적인 형식의 모델을 둘러보고, 조사하고, 다운로드할 수 있는 플랫폼입니다. 좋은 오픈 웨이트 모델 제공 기업으로는 미스트랄, 메타, 마이크로소프트, 구글 같은 대기업이 있습니다. 하지만 커뮤니티 모델과 [파인 튜닝된](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)) 모델도 많이 있습니다. 앞서 언급했듯이 일반 소비자용 하드웨어를 사용하는 경우 양자화된 모델이 모델 품질과 성능 사이의 균형을 가장 잘 맞춰 줍니다.

필요에 맞는 모델을 고르는 데 도움이 되도록 리더보드와 벤치마크를 참고할 수 있습니다. 가장 널리 사용되는 리더보드는 커뮤니티 주도의 [LM 아레나](https://lmarena.ai)입니다. 또한 [Open LLM 리더보드](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard)는 [MMLU-Pro](https://arxiv.org/abs/2406.01574) 같은 일반적인 벤치마크에서 오픈 웨이트 모델 성능에 초점을 맞춥니다. [감성 지능](https://eqbench.com), ["검열되지 않은 일반 지능"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard) 등 [다양한 요소](https://nebuly.com/blog/llm-leaderboards)를 측정하는 특화된 벤치마크도 있습니다.

## AI 채팅 클라이언트 { #ai-chat-clients }

| 기능          | [Kobold.cpp](#koboldcpp)                                      | [올라마](#ollama-cli)                                                            | [라마파일](#llamafile)                                                                                    |
| ----------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| GPU 지원      | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                         |
| 이미지 생성      | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                           |
| 음성 인식       | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                           |
| 모델 자동 다운로드  | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 사용 가능한 모델이 적음  |
| 사용자 지정 매개변수 | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                         |
| 멀티 플랫폼      | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 윈도우에서 크기 제한 있음 |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Kobold.cpp 로고](assets/img/ai-chat/kobold.png){align=right}

**Kobold.cpp**는 윈도우, 맥, 리눅스 컴퓨터에서 로컬로 실행되는 AI 클라이언트입니다. 롤플레이 용도처럼 세밀한 사용자 지정과 조정이 필요하다면 훌륭한 선택입니다.

Kobold.cpp는 다양한 텍스트 모델을 지원할 뿐만 아니라, [스테이블 디퓨전](https://stability.ai/stable-image) 같은 이미지 생성기와 [위스퍼](https://github.com/ggerganov/whisper.cpp) 같은 자동 음성 인식 도구도 지원합니다.

[:octicons-repo-16: 저장소](https://github.com/LostRuins/koboldcpp#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="소스 코드" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="보안 정책" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: 리눅스](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">호환성 문제</p>

Kobold.cpp는 AVX/AVX2를 지원하지 않는 컴퓨터에서는 실행되지 않을 수 있습니다.

</div>

Kobold.cpp에서는 AI 모델 온도, AI 채팅의 시스템 프롬프트 같은 매개변수를 수정할 수 있습니다. 또한 네트워크 터널을 만들어 휴대폰 같은 다른 기기에서 AI 모델에 접근하는 기능도 지원합니다.

### 올라마(CLI) { #ollama-cli }

<div class="admonition recommendation" markdown>

![올라마 로고](assets/img/ai-chat/ollama.png){align=right}

**올라마**는 macOS, 리눅스, 윈도우에서 사용할 수 있는 명령줄 AI 어시스턴트입니다. 올라마는 사용하기 쉽고 호환성이 넓으며, 추론 및 기타 기법을 사용해 속도가 빠른 AI 클라이언트를 찾는다면 훌륭한 선택입니다. 또한 수동 설정이 전혀 필요하지 않습니다.

올라마는 다양한 텍스트 모델을 지원할 뿐만 아니라 [LLaVA](https://github.com/haotian-liu/LLaVA) 모델도 지원하며, 메타의 [라마 비전 기능](https://huggingface.co/blog/llama32#what-is-llama-32-vision)도 실험적으로 지원합니다.

[:octicons-home-16: 홈페이지](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="소스 코드" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="보안 정책" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: 리눅스](https://ollama.com/download/linux)

</details>

</div>

올라마는 사용하려는 AI 모델을 자동으로 다운로드하여 로컬 AI 채팅을 설정하는 과정을 단순화합니다. 예를 들어 `ollama run llama3.2`를 실행하면 라마 3.2 모델이 자동으로 다운로드되어 실행됩니다. 또한 올라마는 다양한 AI 모델의 파일을 호스팅하는 자체 [모델 라이브러리](https://ollama.com/library)를 관리합니다. 이를 통해 모델의 성능과 보안이 모두 검증되므로, 모델의 진위를 직접 확인할 필요가 없습니다.

### 라마파일 { #llamafile }

<div class="admonition recommendation" markdown>

![라마파일 로고](assets/img/ai-chat/llamafile.webp){align=right}

**라마파일**은 별도의 설정 없이 사용자의 컴퓨터에서 LLM을 로컬로 실행할 수 있게 해 주는 가벼운 단일 파일 실행 파일입니다. [모질라의 지원](https://hacks.mozilla.org/2023/11/introducing-llamafile)을 받고 있으며 리눅스, macOS, 윈도우에서 사용할 수 있습니다.

라마파일도 LLaVA를 지원합니다. 하지만 음성 인식이나 이미지 생성은 지원하지 않습니다.

[:octicons-repo-16: 저장소](https://github.com/Mozilla-Ocho/llamafile#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#quickstart){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="소스 코드" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="보안 정책" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:fontawesome-brands-windows: 윈도우](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-apple: macOS](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-linux: 리눅스](https://github.com/Mozilla-Ocho/llamafile#quickstart)

</details>

</div>

모질라는 일부 라마 및 미스트랄 모델에 대해서만 라마파일을 제공하며, 서드파티 라마파일도 거의 없습니다. 게다가 윈도우는 `.exe` 파일을 4GB로 제한하는데, 대부분의 모델은 그보다 큽니다.

이러한 문제를 피하려면 [외부 가중치를 불러올](https://github.com/Mozilla-Ocho/llamafile#using-llamafile-with-external-weights) 수 있습니다.

## 안전하게 모델 다운로드하기 { #securely-downloading-models }

([올라마](#ollama-cli)나 [라마파일](#llamafile)처럼) 자체 모델 파일 라이브러리를 관리하는 AI 클라이언트를 사용한다면, 해당 라이브러리에서 다운로드해야 합니다. 하지만 라이브러리에 없는 모델을 다운로드하거나, ([Kobold.cpp](#koboldcpp)처럼) 라이브러리를 관리하지 않는 AI 클라이언트를 사용한다면, 다운로드하는 AI 모델이 안전하고 정상적인 것인지 확인하기 위한 추가 단계를 거쳐야 합니다.

허깅 페이스는 다운로드한 파일이 진짜이고 안전하게 사용할 수 있는지 확인하는 여러 기능을 제공하므로, 모델 파일은 허깅 페이스에서 다운로드할 것을 권장합니다.

모델의 진위와 안전성을 확인하려면 다음 사항을 살펴보세요:

- 명확한 문서를 갖춘 모델 카드
- 인증된 조직 배지
- 커뮤니티 리뷰 및 사용 통계
- 모델 파일 옆의 "Safe" 배지(허깅 페이스에만 해당)
- 일치하는 체크섬[^1]
  - 허깅 페이스에서는 모델 파일을 클릭하고 그 아래에 있는 **Copy SHA256** 버튼을 찾으면 해시를 확인할 수 있습니다. 이 체크섬을 다운로드한 모델 파일의 체크섬과 비교해야 합니다.

다운로드한 모델이 위의 모든 확인 사항을 충족한다면 일반적으로 안전합니다.

## 평가 기준 { #criteria }

프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다. [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 오픈 소스여야 합니다.
- 채팅 데이터를 포함한 개인 데이터를 전송해서는 안 됩니다.
- 멀티 플랫폼을 지원해야 합니다.
- GPU가 필수여서는 안 됩니다.
- GPU를 활용한 빠른 추론을 지원해야 합니다.
- 인터넷 연결이 필수여서는 안 됩니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 _하는_ 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 클릭 한 번으로 설치하는 등 다운로드와 설정이 쉬운 것이 좋습니다.
- 모델 다운로더가 내장되어 있는 것이 좋습니다.
- 사용자가 시스템 프롬프트, 온도 같은 LLM 매개변수를 수정할 수 있는 것이 좋습니다.

\*[LLaVA]: Large Language and Vision Assistant(멀티모달 AI 모델)
\*[LLM]: 대규모 언어 모델(ChatGPT 같은 AI 모델)
\*[LLMs]: 대규모 언어 모델(ChatGPT 같은 AI 모델)
\*[오픈 웨이트 모델]: 누구나 다운로드하여 사용할 수 있지만, 기반이 되는 학습 데이터 및/또는 알고리즘은 독점인 AI 모델.
\*[시스템 프롬프트]: AI 채팅이 어떻게 작동해야 하는지 안내하기 위해 사람이 제공하는 일반적인 지침.
\*[온도]: AI 모델에서 생성되는 텍스트의 무작위성과 창의성 수준을 조절하는 데 사용되는 매개변수.

[^1]: 파일 체크섬은 일종의 변조 방지 지문입니다. 개발자는 보통 별도로 다운로드할 수 있는 텍스트 파일이나 다운로드 페이지 자체에 체크섬을 제공합니다. 다운로드한 파일의 체크섬이 개발자가 제공한 체크섬과 일치하는지 확인하면 파일이 진짜이며 전송 중에 변조되지 않았음을 확인하는 데 도움이 됩니다. 리눅스와 macOS에서는 `sha256sum`, 윈도우에서는 `certutil -hashfile file SHA256` 같은 명령을 사용하여 다운로드한 파일의 체크섬을 생성할 수 있습니다.
