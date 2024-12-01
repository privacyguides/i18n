---
meta_title: 推薦的 AI 聊天：私密的 ChatGPT 替代方案 - Privacy Guides
title: AI 聊天
icon: material/assistant
description: 與 OpenAI 的 ChatGPT 和與其競爭的科技巨擘產品不同，這些 AI 工具可在本地執行，因此您的資料從未離開您的電腦。
cover: ai-chatbots.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

自 2022 年 ChatGPT 發表以來，人們與 大型語言模型(LLM) 的互動變得越來越普遍。 大型語言模型 可以幫助我們寫出更好的文章；瞭解不熟悉的主題；或是回答各式各樣的問題。 他們可以根據從網路搜刮的大量資料，以統計方式預測下一串對話。

## LLM 的隱私權疑慮

訓練 AI 模型需要用到資料；然而，用於訓練 AI 模型的資料包括從網路上獲取的大量公開資料，其中可能包括姓名和地址等敏感資訊。 基於雲端的 AI 軟體通常會 [收集您輸入的資料](https://openai.com/policies/row-privacy-policy)，這表示您的聊天內容對他們而言並非私密的。 這種做法也會帶來資料外洩的風險。 此外，LLM 真的有可能在未來與其他使用者的對話中洩露您的私人聊天資訊。

如果您擔心這些做法，您可以拒絕使用 AI，或是使用 [真正開放原始碼的模型](https://proton.me/blog/how-to-build-privacy-first-ai)，這些模型會公開釋出，並允許您檢查其訓練資料集。 由 [Ai2](https://allenai.org/open-data) 所製作的 [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514)，就是這樣的一個模型。

另外，您也可以在本地執行 AI 模型，這樣您的資料就不會離開您的裝置，因此也不會與第三方共用。 因此，相較於雲端解決方案；本機模型是更私密、更安全的替代方案，讓您可以放心地將敏感資訊分享給 AI 模型。

## AI 模型

### 本地 AI 模型的硬體

本地模型也相當容易運行。 只要 8GB 記憶體，就能以較低的速度運行較小的模型。 使用更強大的硬體，例如具有足夠 VRAM 的專用 GPU 或具有快速 LPDDR5X 記憶體的現代系統，可以提供最佳的體驗。

LLM 通常可以透過參數的數量來區分用途，對於提供給終端使用者的開放原始碼模型，參數的數量通常介於 1.3B 到 405B 之間。 例如，參數低於 6.7B 的模型只適合文字摘要等基本任務，而參數介於 7B 與 13B 之間的模型則是品質與速度的絕佳折衷。 具備進階推理能力的模型一般在 70B 左右。

對於消費級硬體，一般建議使用 [量化模型](https://huggingface.co/docs/optimum/en/concept_guides/quantization)，以達到模型品質與效能的最佳平衡。 請參閱下表，瞭解有關不同大小量化模型典型要求的更精確資訊。

| 模型大小（使用 參數 作為單位） | 最低 RAM 要求 | 最低處理器要求          |
| ---------------- | --------- | ---------------- |
| 7B               | 8GB       | 現代 CPU（需支援 AVX2） |
| 13B              | 16GB      | 現代 CPU（需支援 AVX2） |
| 70B              | 72GB      | 具備 VRAM 的 GPU    |

若要在本機執行 AI，您需要 AI 模型和 AI 客戶端。

### 選擇模型

有許多採用寬鬆式自由軟體授權條款的模型可供下載。 [Hugging Face](https://huggingface.co/models) 是一個讓您瀏覽、研究和下載常用格式模型的平台，如 [GGUF](https://huggingface.co/docs/hub/en/gguf)。 提供優質 'open-weights'模型 的公司包括 Mistral、Meta、Microsoft 和 Google 等大公司。 不過，也有許多由社群製作和「微調」的模型可用。 如上所述，量化模型為使用消費級硬體的使用者提供了模型品質與效能之間的最佳平衡。

為了幫助您選擇適合您的模型，您可以參考排行榜和基準。 使用最廣泛的排行榜是由社群驅動的 [LM Arena](https://lmarena.ai)。 此外，[OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) 著重於 'open-weights'模型 在一般基準上的表現，例如： [MMLU-Pro](https://arxiv.org/abs/2406.01574)。  There are also specialized benchmarks which measure factors like [emotional intelligence](https://eqbench.com), ["uncensored general intelligence"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard), and [many others](https://www.nebuly.com/blog/llm-leaderboards).

## AI 聊天客戶端

| 特點     | [Kobold.cpp](#koboldcpp)                                      | [Ollama](#ollama-cli)                                                         | [Llamafile](#llamafile)                                                                                 |
| ------ | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| GPU 支援 | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                           |
| 圖片生成   | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                             |
| 語音辨識   | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                             |
| 自動下載模型 | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 僅支援極少數模型         |
| 自訂參數   | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                           |
| 多平臺    | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } 在 Windows 上有大小限制 |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Kobold.cpp Logo](assets/img/ai-chat/kobold.png){align=right}

Kobold.cpp 是一個 AI 客戶端，可在您的 Windows、Mac 或 Linux 電腦上本地執行。 如果您需要大量的客製化和調整，例如為了角色扮演的目的，這是一個絕佳的選擇。

除了支援大量的文字模型之外，Kobold.cpp 也支援圖片產生器，如： [Stable Diffusion](https://stability.ai/stable-image) ；以及自動語音辨識工具，如： [Whisper](https://github.com/ggerganov/whisper.cpp)。

[:octicons-home-16: 首頁](https://github.com/LostRuins/koboldcpp){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="原始碼" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="安全性政策" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: Linux](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition note" markdown>
<p class="admonition-title">相容性問題</p>

Kobold.cpp 可能無法在不支援 AVX/AVX2 的電腦上執行。

</div>

Kobold.cpp 可讓您修改 AI 模型溫度和 AI 聊天的 system prompt 等參數。 它也支援建立網路隧道，以便從手機等其他裝置存取 AI 模型。

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Ollama Logo](assets/img/ai-chat/ollama.png){align=right}

Ollama 是一款命令列人工智能助理，可在 macOS、Linux 和 Windows 上使用。 如果您正在尋找一個易於使用、具有廣泛相容性，而且因使用 推理(inference) 和其他技術而速度極快的 AI 客戶端，Ollama 是一個不錯的選擇。 它也無須進行任何手動設定。

除了支援大量文字生成模型之外，Ollama 也支援 [LLaVA](https://github.com/haotian-liu/LLaVA) 模型，並且對 Meta 的 [Llama 視覺能力](https://huggingface.co/blog/llama32#what-is-llama-32-vision) 有實驗性的支援。

[:octicons-home-16: 首頁](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="原始碼" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="安全性政策" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama 可自動下載您要使用的 AI 模型，簡化設定本地 AI 聊天的程序。 例如：執行 `ollama run llama3.2` 會自動下載並執行 Llama 3.2 模型。 此外，Ollama 維護他們自己的 [模型庫](https://ollama.com/library)，在那裡存放著各種 AI 模型的檔案。 這可確保模型的效能和安全性都經過審核，無需手動驗證模型的真實及可靠性。

### Llamafile

<div class="admonition recommendation" markdown>

![Llamafile Logo](assets/img/ai-chat/llamafile.svg){align=right}

Llamafile 是一個輕量級的單一檔案執行檔，可讓使用者在自己的電腦上本地執行 LLM，而不需要進行任何設定。 它 [由 Mozilla 資助](https://hacks.mozilla.org/2023/11/introducing-llamafile)，可在 Linux、macOS 和 Windows 上使用。

Llamafile 也支援 LLaVA。 但是，它不支援語音辨識及圖片生成。

[:octicons-home-16: 首頁](https://github.com/Mozilla-Ocho/llamafile){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#llamafile){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="原始碼" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="安全性政策" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-solid-desktop: 電腦版](https://github.com/Mozilla-Ocho/llamafile#quickstart)

</details>

</div>

Mozilla 只為某些 Llama 和 Mistral 模型提供 llamafile，而可用的第三方 llamafile 很少。 此外，Windows 將 `.exe` 檔案大小限制為最大 4GB，而大多數模型都大於此數目。

為了迴避這些問題，您可以 [load external weights](https://github.com/Mozilla-Ocho/llamafile#using-llamafile-with-external-weights)。

## 安全地下載模型

如果您使用的 AI 客戶端 有維護他們自己的模型檔案庫（例如： [Ollama](#ollama-cli) 和 [Llamafile](#llamafile) ），您應該從那裡下載。 不過，如果您要下載的模型不在他們的檔案庫中，或是使用沒有自行維護檔案庫的 AI 客戶端（例如： [Kobold.cpp](#koboldcpp) ），您就需要進行額外的檢查，以確保您下載的 AI 模型是未經篡改且安全的。

我們建議您從 Hugging Face 下載模型檔案，因為它提供了多種功能來驗證您的下載是未經篡改且可安全使用的。

若要檢查模型的真實性和安全性，請尋找：

- 具有清晰說明的模型卡
- 經過驗證的 組織徽章(organization badge)
- 社群評論和使用情況統計
- 模型檔案旁的「Safe」徽章（僅限 Hugging Face）
- 核對 checksum（核對和）[^1]
  - 在 Hugging Face 上，您可以按一下模型檔案，並在其下方尋找 **Copy SHA256** 按鈕，以找到雜湊值。 您應該將此 checksum 與您下載的模型檔案之 checksum 進行比對。

A downloaded model is generally safe if it satisfies all of the above checks.

## 標準

請注意，我們與所推薦的任何項目毫無關聯。 除了 [我們的標準準則](about/criteria.md)，我們也制定了一套明確的要求，讓我們能提供客觀的建議。 我們建議您在選擇使用專案前先熟悉此清單，並自行研究，以確保它是適合您的選擇。

### 最低合格要求

- 必須是開源的。
- 不得傳輸個人資料，包括聊天資料。
- 必須跨平台。
- 必須不需要 GPU。
- Must have support for GPU-powered fast inference.
- 必須無需網際網路連線。

### 最佳情況

最佳情況標準代表我們 _希望_ 在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應該容易下載和設定，例如具備一鍵安裝程序。
- 應該有內建的模型下載器選項。
- 使用者應能修改 LLM 參數，例如其 system prompt 或 temperature。

[^1]: A file checksum is a type of anti-tampering fingerprint. A developer usually provides a checksum in a text file that can be downloaded separately, or on the download page itself. Verifying that the checksum of the file you downloaded matches the one provided by the developer helps ensure that the file is genuine and wasn't tampered with in transit. You can use commands like `sha256sum` on Linux and macOS, or `certutil -hashfile file SHA256` on Windows to generate the downloaded file's checksum.
