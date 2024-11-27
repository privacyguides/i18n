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

自 2022 年 ChatGPT 發表以來，人們與 大型語言模型(LLM) 的互動變得越來越普遍。 大型語言模型 可以幫助我們寫出更好的文章；瞭解不熟悉的主題；或是回答各式各樣的問題。 They can statistically predict the next word based on a vast amount of data scraped from the web.

## 大型語言模型的隱私權疑慮

訓練 AI 模型需要用到資料；然而，用於訓練 AI 模型的資料包括從網路上獲取的大量公開資料，其中可能包括姓名和地址等敏感資訊。 基於雲端的 AI 軟體通常會 [收集您輸入的資料](https://openai.com/policies/row-privacy-policy)，這表示您的聊天內容對他們而言並非私密的。 這種做法也會帶來資料外洩的風險。 此外，大型語言模型 真的有可能在未來與其他使用者的對話中洩露您的私人聊天資訊。

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

There are many permissively licensed models available to download. [Hugging Face](https://huggingface.co/models) 是一個讓您瀏覽、研究和下載常用格式模型的平台，如 [GGUF](https://huggingface.co/docs/hub/en/gguf)。 Companies that provide good open-weights models include big names like Mistral, Meta, Microsoft, and Google. However, there are also many community models and 'fine-tunes' available. 如上所述，量化模型為使用消費級硬體的使用者提供了模型品質與效能之間的最佳平衡。

為了幫助您選擇適合您的模型，您可以參考排行榜和基準。 使用最廣泛的排行榜是由社群驅動的 [LM Arena](https://lmarena.ai)。 Additionally, the [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) focuses on the performance of open-weights models on common benchmarks like [MMLU-Pro](https://arxiv.org/abs/2406.01574).  There are also specialized benchmarks which measure factors like [emotional intelligence](https://eqbench.com), ["uncensored general intelligence"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard), and [many others](https://www.nebuly.com/blog/llm-leaderboards).

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

Kobold.cpp 是一個 AI 用戶端，可在您的 Windows、Mac 或 Linux 電腦上本地執行。 如果您需要大量的客製化和調整，例如為了角色扮演的目的，這是一個絕佳的選擇。

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
<p class="admonition-title">Compatibility Issues</p>

Kobold.cpp might not run on computers without AVX/AVX2 support.

</div>

Kobold.cpp allows you to modify parameters such as the AI model temperature and the AI chat's system prompt. It also supports creating a network tunnel to access AI models from other devices such as your phone.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Ollama Logo](assets/img/ai-chat/ollama.png){align=right}

Ollama is a command-line AI assistant that is available on macOS, Linux, and Windows. Ollama is a great choice if you're looking for an AI client that's easy-to-use, widely compatible, and fast due to its use of inference and other techniques. It also doesn't involve any manual setup.

In addition to supporting a wide range of text models, Ollama also supports [LLaVA](https://github.com/haotian-liu/LLaVA) models and has experimental support for Meta's [Llama vision capabilities](https://huggingface.co/blog/llama32#what-is-llama-32-vision).

[:octicons-home-16: Homepage](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama simplifies the process of setting up a local AI chat by downloading the AI model you want to use automatically. For example, running `ollama run llama3.2` will automatically download and run the Llama 3.2 model. Furthermore, Ollama maintains their own [model library](https://ollama.com/library) where they host the files of various AI models. This ensures that models are vetted for both performance and security, eliminating the need to manually verify model authenticity.

### Llamafile

<div class="admonition recommendation" markdown>

![Llamafile Logo](assets/img/ai-chat/llamafile.svg){align=right}

Llamafile is a lightweight single-file executable that allows users to run LLMs locally on their own computers without any setup involved. It is [backed by Mozilla](https://hacks.mozilla.org/2023/11/introducing-llamafile) and available on Linux, macOS, and Windows.

Llamafile also supports LLaVA. However, it doesn't support speech recognition or image generation.

[:octicons-home-16: Homepage](https://github.com/Mozilla-Ocho/llamafile){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#llamafile){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-solid-desktop: Desktop](https://github.com/Mozilla-Ocho/llamafile#quickstart)

</details>

</div>

Mozilla has made llamafiles available for only some Llama and Mistral models, while there are few third-party llamafiles available. Moreover, Windows limits `.exe` files to 4GB, and most models are larger than that.

To circumvent these issues, you can [load external weights](https://github.com/Mozilla-Ocho/llamafile#using-llamafile-with-external-weights).

## Securely Downloading Models

If you use an AI client that maintains their own library of model files (such as [Ollama](#ollama-cli) and [Llamafile](#llamafile)), you should download it from there. However, if you want to download models not present in their library, or use an AI client that doesn't maintain its library (such as [Kobold.cpp](#koboldcpp)), you will need to take extra steps to ensure that the AI model you download is safe and legitimate.

We recommend downloading model files from Hugging Face since it provides several features to verify that your download is genuine and safe to use.

To check the authenticity and safety of the model, look for:

- Model cards with clear documentation
- A verified organization badge
- Community reviews and usage statistics
- A "Safe" badge next to the model file (Hugging Face only)
- Matching checksums[^1]
  - On Hugging Face, you can find the hash by clicking on a model file and looking for the **Copy SHA256** button below it. You should compare this checksum with the one from the model file you downloaded.

A downloaded model is generally safe if it satisfies all of the above checks.

## 標準

Please note we are not affiliated with any of the projects we recommend. In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project and conduct your own research to ensure it's the right choice for you.

### 最低合格要求

- Must be open-source.
- Must not transmit personal data, including chat data.
- Must be multi-platform.
- Must not require a GPU.
- Must have support for GPU-powered fast inference.
- Must not require an internet connection.

### 最佳情況

Our best-case criteria represent what we _would_ like to see from the perfect project in this category. 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Should be easy to download and set up, e.g. with a one-click install process.
- Should have a built-in model downloader option.
- The user should be able to modify the LLM parameters, such as its system prompt or temperature.

[^1]: A file checksum is a type of anti-tampering fingerprint. A developer usually provides a checksum in a text file that can be downloaded separately, or on the download page itself. Verifying that the checksum of the file you downloaded matches the one provided by the developer helps ensure that the file is genuine and wasn't tampered with in transit. You can use commands like `sha256sum` on Linux and macOS, or `certutil -hashfile file SHA256` on Windows to generate the downloaded file's checksum.