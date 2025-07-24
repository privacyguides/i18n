---
meta_title: "Agentes de IA recomendados: Alternativas ao ChatGPT que protegem sua privacidade - Guia de Privacidade"
title: "Agente de IA"
icon: material/assistant
description: Diferente do ChatGPT da empresa OpenAI e seus concorrentes, as ferramentas aqui sugeridas são executadas localmente com a finalidade de não fornecer ou dificultar a coleta de dados em seu Desktop
cover: ai-chatbots.webp
---

Protege contra as seguintes ameaças:

- [:material-server-network: Provedores](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Vigilância Capitalista](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

The use of **AI chat**, also known as Large Language Models (LLMs), has become increasingly common since the release of ChatGPT in 2022. Os LLMs podem nos ajudar a escrever melhor, entender sobre assuntos desconhecidos ou responder a uma ampla gama de perguntas,  They work by statistically predicting the next word in their responses based on a vast amount of data scraped from the web.

## Preocupações em relação aos LLMs

Os dados usados para treinar modelos de IA, no entanto, incluem uma enorme quantidade de dados disponíveis publicamente extraídos da Web, que eventualmente podem incluir informações confidenciais, como nomes e endereços. O software de IA baseado em nuvem geralmente [coleta suas entradas] (https://openai.com/policies/row-privacy-policy), o que significa que suas mensagens não são privados. Essa prática leva à um risco maior de vazamentos de dados. Além disso, existe a possibilidade real de um LLM vazar informações privadas de mensagens e informações coletadas em conversas futuras com outros usuários.

Se estiver preocupado com essas práticas, você pode se recusar a usar IA ou usar [modelos verdadeiramente de código aberto] (https://proton.me/blog/how-to-build-privacy-first-ai)Estes são lançados publicamente e permitem que você cheque e inspecione os conjuntos de dados de treinamento. Uma dessas alternativas de modelos é o [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514) criado pela [Ai2](https://allenai.org/open-data).

Como alternativa, você pode executar modelos de IA localmente e seus dados nunca sairão do seu dispositivo, evitando assim que os mesmos sejam compartilhados com terceiros. Dessa forma, os modelos locais são uma alternativa privada e segura às soluções baseadas em nuvem. Além de permitir que você compartilhe informações pessoais com o modelo de IA sem preocupações.

## Modelos de IA

### Especificações de Hardware para Modelos de IA de funcionamento local

Os modelos locais também são bastante acessíveis. É possível executar modelos menores em velocidades mais baixas com apenas 8 GB de RAM. O uso de hardware mais avançado como uma placa de vídeo dedicada com VRAM suficiente ou um sistema moderno com memória LPDDR5X rápida oferecerá uma melhor experiência.

LLMs can usually be differentiated by the number of parameters, which can vary between 1.3B to 405B for open-source models available for end users. Por exemplo, modelos com parâmetros abaixo de 6,7B são bons apenas para tarefas básicas, como resumos de texto. Já modelos entre 7B e 13B são um ótimo compromisso entre qualidade e velocidade. Os modelos com recursos avançados de raciocínio geralmente ficam em torno de 70B.

Para computadores pessoais pessoais, geralmente recomenda-se usar [modelos quantizados] (https://huggingface.co/docs/optimum/en/concept_guides/quantization) para obter o melhor equilíbrio entre a qualidade e o desempenho do modelo. Consulte a tabela abaixo para obter mais informações sobre os requisitos ideais para diferentes tamanhos de modelos.

| Tamanho do modelo (em parâmetros) | RAM mínima | Processador Mínimo                              |
| ---------------------------------------------------- | ---------- | ----------------------------------------------- |
| 7B                                                   | 8 GB       | CPU moderna (suporte a AVX2) |
| 13B                                                  | 16 GB      | CPU moderna (suporte a AVX2) |
| 70B                                                  | 72 GB      | GPU com VRAM                                    |

Para executar a IA localmente é necessário um modelo de IA e um cliente de IA.

### Escolhendo um Modelo

Há muitos modelos de código aberto ou de licença livre disponíveis para download. A [Hugging Face](https://huggingface.co/models) é uma plataforma que permite que você navegue, pesquise e faça download de modelos em formatos comuns, como [GGUF](https://huggingface.co/docs/hub/en/gguf). Empresas que fornecem bons modelos de direitos facilitados incluem grandes nomes como Mistral, Meta, Microsoft e Google. However, there are also many community models and [fine-tuned](https://en.wikipedia.org/wiki/Fine-tuning_\(deep_learning\)) models available. Conforme mencionado acima: modelos quantizados oferecem o melhor equilíbrio entre a qualidade e o desempenho do modelo para aqueles que usam um computador pessoal (equipamento de nível de consumidor).

To help you choose a model that fits your needs, you can look at leaderboards and benchmarks. The most widely-used leaderboard is the community-driven [LM Arena](https://lmarena.ai). Additionally, the [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) focuses on the performance of open-weights models on common benchmarks like [MMLU-Pro](https://arxiv.org/abs/2406.01574).  There are also specialized benchmarks which measure factors like [emotional intelligence](https://eqbench.com), ["uncensored general intelligence"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard), and [many others](https://nebuly.com/blog/llm-leaderboards).

## AI Chat Clients

| Feature                     | [Kobold.cpp](#koboldcpp)                                    | [Ollama](#ollama-cli)                                                       | [Llamafile](#llamafile)                                                                                            |
| --------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| GPU Support                 | :material-check:                            | :material-check:                            | :material-check:                                                                   |
| Image Generation            | :material-check:                            | :material-close:{ .pg-red } | :material-close:{ .pg-red }                                        |
| Speech Recognition          | :material-check:                            | :material-close:{ .pg-red } | :material-close:{ .pg-red }                                        |
| Auto-download Models        | :material-close:{ .pg-red } | :material-check:                            | :material-alert-outline:{ .pg-orange } Few models available        |
| Custom Parameters           | :material-check:                            | :material-close:{ .pg-red } | :material-check:                                                                   |
| Aplicativos multiplataforma | :material-check:                            | :material-check:                            | :material-alert-outline:{ .pg-orange } Size limitations on Windows |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Kobold.cpp Logo](assets/img/ai-chat/kobold.png){align=right}

**Kobold.cpp** is an AI client that runs locally on your Windows, Mac, or Linux computer. It's an excellent choice if you are looking for heavy customization and tweaking, such as for role-playing purposes.

In addition to supporting a large range of text models, Kobold.cpp also supports image generators such as [Stable Diffusion](https://stability.ai/stable-image) and automatic speech recognition tools such as [Whisper](https://github.com/ggerganov/whisper.cpp).

[:octicons-repo-16: Repository](https://github.com/LostRuins/koboldcpp#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: Linux](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">Compatibility Issues</p>

Kobold.cpp might not run on computers without AVX/AVX2 support.

</div>

Kobold.cpp allows you to modify parameters such as the AI model temperature and the AI chat's system prompt. It also supports creating a network tunnel to access AI models from other devices such as your phone.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Ollama Logo](assets/img/ai-chat/ollama.png){align=right}

**Ollama** is a command-line AI assistant that is available on macOS, Linux, and Windows. Ollama is a great choice if you're looking for an AI client that's easy-to-use, widely compatible, and fast due to its use of inference and other techniques. It also doesn't involve any manual setup.

In addition to supporting a wide range of text models, Ollama also supports [LLaVA](https://github.com/haotian-liu/LLaVA) models and has experimental support for Meta's [Llama vision capabilities](https://huggingface.co/blog/llama32#what-is-llama-32-vision).

[:octicons-home-16: Homepage](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama simplifies the process of setting up a local AI chat by downloading the AI model you want to use automatically. For example, running `ollama run llama3.2` will automatically download and run the Llama 3.2 model. Furthermore, Ollama maintains their own [model library](https://ollama.com/library) where they host the files of various AI models. This ensures that models are vetted for both performance and security, eliminating the need to manually verify model authenticity.

### Llamafile

<div class="admonition recommendation" markdown>

![Llamafile Logo](assets/img/ai-chat/llamafile.webp){align=right}

**Llamafile** is a lightweight, single-file executable that allows users to run LLMs locally on their own computers without any setup involved. It is [backed by Mozilla](https://hacks.mozilla.org/2023/11/introducing-llamafile) and available on Linux, macOS, and Windows.

Llamafile also supports LLaVA. However, it doesn't support speech recognition or image generation.

[:octicons-repo-16: Repository](https://github.com/Mozilla-Ocho/llamafile#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#quickstart){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-apple: macOS](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-linux: Linux](https://github.com/Mozilla-Ocho/llamafile#quickstart)

</details>

</div>

Mozilla has made llamafiles available for only some Llama and Mistral models, while there are few third-party llamafiles available. Moreover, Windows limits `.exe` files to 4 GB, and most models are larger than that.

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

A downloaded model is generally safe if it satisfies all the above checks.

## Criteria

Please note we are not affiliated with any of the projects we recommend. In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Deve ser de código aberto.
- Must not transmit personal data, including chat data.
- Must be multi-platform.
- Must not require a GPU.
- Must support GPU-powered, fast inference.
- Must not require an internet connection.

### Melhor Caso

Our best-case criteria represent what we _would_ like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Should be easy to download and set up, e.g. with a one-click installation process.
- Should have a built-in model downloader option.
- The user should be able to modify the LLM parameters, such as its system prompt or temperature.

\*[LLaVA]: Large Language and Vision Assistant (multimodal AI model)
\*[LLM]: Large Language Model (AI model such as ChatGPT)
\*[LLMs]: Large Language Models (AI models such as ChatGPT)
\*[open-weights models]: AI models that anyone can download and use, but the underlying training data and/or algorithms for them are proprietary.
\*[system prompt]: The general instructions given by a human to guide how an AI chat should operate.
\*[temperature]: A parameter used in AI models to control the level of randomness and creativity in the generated text.

[^1]: A file checksum is a type of anti-tampering fingerprint. A developer usually provides a checksum in a text file that can be downloaded separately, or on the download page itself. Verifying that the checksum of the file you downloaded matches the one provided by the developer helps ensure that the file is genuine and wasn't tampered with in transit. You can use commands like `sha256sum` on Linux and macOS, or `certutil -hashfile file SHA256` on Windows to generate the downloaded file's checksum.
