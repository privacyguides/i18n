---
meta_title: "Chat IA Recomendado: Alternativas Privadas a ChatGPT - Privacy Guides"
title: Chat IA
icon: material/assistant
description: A diferencia de ChatGPT de OpenAI y sus competidores de los gigantes tecnológicos, estas herramientas de IA se ejecutan localmente, por lo que tus datos nunca salen de tu dispositivo de escritorio.
cover: ai-chatbots.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

Desde el lanzamiento de ChatGPT en 2022, las interacciones con grandes modelos lingüísticos (LLM) son cada vez más frecuentes. Los LLM pueden ayudarnos a escribir mejor, a comprender temas desconocidos o a responder a una amplia gama de preguntas. Pueden predecir estadísticamente la siguiente palabra basándose en una gran cantidad de datos extraídos de Internet.

## Preocupaciones por la Privacidad de los LLM

Sin embargo, los datos utilizados para entrenar modelos de IA incluyen una enorme cantidad de datos públicos extraídos de Internet, que pueden incluir información confidencial como nombres y direcciones. El software de IA basado en la nube a menudo [recopila tus entradas](https://openai.com/policies/row-privacy-policy), lo que significa que tus chats no son privados frente a ellos. Esta práctica también introduce un riesgo de violación de datos. Además, existe la posibilidad real de que un LLM filtre tu información privada del chat en futuras conversaciones con otros usuarios.

Si te preocupan estas prácticas, puedes negarte a usar la IA o usar [modelos verdaderamente de código abierto](https://proton.me/blog/how-to-build-privacy-first-ai) que publican y te permiten inspeccionar sus conjuntos de datos de entrenamiento. Uno de estos modelos es [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514) hecho por [Ai2](https://allenai.org/open-data).

Alternativamente, puedes ejecutar modelos de IA localmente para que tus datos nunca salgan de tu dispositivo y, por lo tanto, nunca se compartan con terceros. Como tales, los modelos locales son una alternativa más privada y segura que las soluciones basadas en la nube y permiten compartir información sensible con el modelo de IA sin preocupaciones.

## Modelos de IA

### Hardware para Modelos Locales de IA

Los modelos locales también son bastante accesibles. Es posible ejecutar modelos más pequeños a velocidades inferiores con tan solo 8 GB de RAM. Utilizar un hardware más potente, como una GPU dedicada con suficiente VRAM o un sistema moderno con memoria LPDDR5X rápida, ofrece la mejor experiencia.

Los LLM suelen diferenciarse por el número de parámetros, que pueden variar entre 1,3B y 405B para los modelos de código abierto disponibles para los usuarios finales. Por ejemplo, los modelos con parámetros inferiores a 6,7B sólo son buenos para tareas básicas como resúmenes de texto, mientras que los modelos entre 7B y 13B son un gran compromiso entre calidad y velocidad. Los modelos con capacidades de razonamiento avanzadas suelen rondar los 70B.

Para el hardware de consumo personal, generalmente se recomienda utilizar [modelos cuantizados] (https://huggingface.co/docs/optimum/en/concept_guides/quantization) para obtener el mejor equilibrio entre la calidad del modelo y el rendimiento. Echa un vistazo a la tabla de abajo para obtener información más precisa sobre los requerimientos típicos de diferentes tamaños de modelos cuantificados.

| Tamaño del Modelo (en Parámetros) | RAM Mínima | Procesador Mínimo                                    |
| ---------------------------------------------------- | ---------- | ---------------------------------------------------- |
| 7B                                                   | 8 GB       | CPU Moderna (compatible con AVX2) |
| 13B                                                  | 16 GB      | CPU Moderna (compatible con AVX2) |
| 70B                                                  | 72 GB      | GPU con VRAM                                         |

Para ejecutar IA localmente, se necesita tanto un modelo de IA como un cliente de IA.

### Elegir un Modelo

Hay muchos modelos con licencia permisiva disponibles para descargar. [Hugging Face](https://huggingface.co/models) es una plataforma que te permite navegar, investigar y descargar modelos en formatos comunes como [GGUF](https://huggingface.co/docs/hub/en/gguf). Entre las empresas que ofrecen buenos modelos open-weights figuran grandes nombres como Mistral, Meta, Microsoft y Google. Sin embargo, también hay muchos modelos comunitarios y «fine-tunes» disponibles. Como ya se ha mencionado, los modelos cuantificados ofrecen el mejor equilibrio entre calidad de modelo y rendimiento para quienes utilizan hardware de consumo personal.

Para ayudarte a elegir un modelo que se adapte a tus necesidades, puedes consultar tablas de clasificación y puntos de referencia. La tabla de clasificación más utilizada es la de la comunidad [LM Arena](https://lmarena.ai). Además, la [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) se centra en el rendimiento de los modelos de ponderación abierta en puntos de referencia comunes como [MMLU-Pro](https://arxiv.org/abs/2406.01574).  También existen puntos de referencia especializados que miden factores como [inteligencia emocional](https://eqbench.com), [«inteligencia general no censurada»](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard), y [muchos otros](https://www.nebuly.com/blog/llm-leaderboards).

## Clientes de Chat IA

| Característica            | [Kobold.cpp](#koboldcpp)                                      | [Ollama](#ollama-cli)                                                         | [Llamafile](#llamafile)                                                                                                  |
| ------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Soporte de GPU            | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                                            |
| Generación de Imágenes    | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                              |
| Reconocimiento de Voz     | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                              |
| Modelos de Autodescarga   | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Pocos modelos disponibles         |
| Parámetros Personalizados | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                                            |
| Multiplataforma           | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Limitaciones de tamaño en Windows |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Kobold.cpp Logo](assets/img/ai-chat/kobold.png){align=right}

Kobold.cpp is an AI client that runs locally on your Windows, Mac, or Linux computer. It's an excellent choice if you are looking for heavy customization and tweaking, such as for role-playing purposes.

In addition to supporting a large range of text models, Kobold.cpp also supports image generators such as [Stable Diffusion](https://stability.ai/stable-image) and automatic speech recognition tools such as [Whisper](https://github.com/ggerganov/whisper.cpp).

[:octicons-home-16: Homepage](https://github.com/LostRuins/koboldcpp){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

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
<summary>Downloads "Descargas"</summary>

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
<summary>Downloads "Descargas"</summary>

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

## Criterios

Please note we are not affiliated with any of the projects we recommend. In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project and conduct your own research to ensure it's the right choice for you.

### Requisitos Mínimos

- Must be open-source.
- Must not transmit personal data, including chat data.
- Must be multi-platform.
- Must not require a GPU.
- Must have support for GPU-powered fast inference.
- Must not require an internet connection.

### Mejor Caso

Our best-case criteria represent what we _would_ like to see from the perfect project in this category. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Should be easy to download and set up, e.g. with a one-click install process.
- Should have a built-in model downloader option.
- The user should be able to modify the LLM parameters, such as its system prompt or temperature.

[^1]: A file checksum is a type of anti-tampering fingerprint. A developer usually provides a checksum in a text file that can be downloaded separately, or on the download page itself. Verifying that the checksum of the file you downloaded matches the one provided by the developer helps ensure that the file is genuine and wasn't tampered with in transit. You can use commands like `sha256sum` on Linux and macOS, or `certutil -hashfile file SHA256` on Windows to generate the downloaded file's checksum.
