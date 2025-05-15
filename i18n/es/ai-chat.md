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

The use of **AI chat**, also known as Large Language Models (LLMs), has become increasingly common since the release of ChatGPT in 2022. Los LLM pueden ayudarnos a escribir mejor, a comprender temas desconocidos o a responder a una amplia gama de preguntas. They work by statistically predicting the next word in their responses based on a vast amount of data scraped from the web.

## Preocupaciones por la Privacidad de los LLM

Sin embargo, los datos utilizados para entrenar modelos de IA incluyen una enorme cantidad de datos públicos extraídos de Internet, que pueden incluir información confidencial como nombres y direcciones. El software de IA basado en la nube a menudo [recopila tus entradas](https://openai.com/policies/row-privacy-policy), lo que significa que tus chats no son privados frente a ellos. Esta práctica también introduce un riesgo de violación de datos. Además, existe la posibilidad real de que un LLM filtre tu información privada del chat en futuras conversaciones con otros usuarios.

Si te preocupan estas prácticas, puedes negarte a usar la IA o usar [modelos verdaderamente de código abierto](https://proton.me/blog/how-to-build-privacy-first-ai) que publican y te permiten inspeccionar sus conjuntos de datos de entrenamiento. Uno de estos modelos es [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514) hecho por [Ai2](https://allenai.org/open-data).

Alternativamente, puedes ejecutar modelos de IA localmente para que tus datos nunca salgan de tu dispositivo y, por lo tanto, nunca se compartan con terceros. Como tales, los modelos locales son una alternativa más privada y segura que las soluciones basadas en la nube y permiten compartir información sensible con el modelo de IA sin preocupaciones.

## Modelos de IA

### Hardware para Modelos Locales de IA

Los modelos locales también son bastante accesibles. It's possible to run smaller models at lower speeds on as little as 8 GB of RAM. Utilizar un hardware más potente, como una GPU dedicada con suficiente VRAM o un sistema moderno con memoria LPDDR5X rápida, ofrece la mejor experiencia.

Los LLM suelen diferenciarse por el número de parámetros, que pueden variar entre 1,3B y 405B para los modelos de código abierto disponibles para los usuarios finales. Por ejemplo, los modelos con parámetros inferiores a 6,7B sólo son buenos para tareas básicas como resúmenes de texto, mientras que los modelos entre 7B y 13B son un gran compromiso entre calidad y velocidad. Los modelos con capacidades de razonamiento avanzadas suelen rondar los 70B.

Para el hardware de consumo personal, generalmente se recomienda utilizar [modelos cuantizados] (https://huggingface.co/docs/optimum/en/concept_guides/quantization) para obtener el mejor equilibrio entre la calidad del modelo y el rendimiento. Echa un vistazo a la tabla de abajo para obtener información más precisa sobre los requerimientos típicos de diferentes tamaños de modelos cuantificados.

| Tamaño del Modelo (en Parámetros) | RAM Mínima | Procesador Mínimo                                    |
| ---------------------------------------------------- | ---------- | ---------------------------------------------------- |
| 7B                                                   | 8 GB       | CPU Moderna (compatible con AVX2) |
| 13B                                                  | 16 GB      | CPU Moderna (compatible con AVX2) |
| 70B                                                  | 72 GB      | GPU con VRAM                                         |

Para ejecutar IA localmente, se necesita tanto un modelo de IA como un cliente de IA.

### Elegir un Modelo

Hay muchos modelos con licencia permisiva disponibles para descargar. [Hugging Face](https://huggingface.co/models) es una plataforma que te permite navegar, investigar y descargar modelos en formatos comunes como [GGUF](https://huggingface.co/docs/hub/en/gguf). Entre las empresas que ofrecen buenos modelos open-weights figuran grandes nombres como Mistral, Meta, Microsoft y Google. However, there are also many community models and [fine-tuned](https://en.wikipedia.org/wiki/Fine-tuning_\(deep_learning\)) models available. Como ya se ha mencionado, los modelos cuantificados ofrecen el mejor equilibrio entre calidad de modelo y rendimiento para quienes utilizan hardware de consumo personal.

Para ayudarte a elegir un modelo que se adapte a tus necesidades, puedes consultar tablas de clasificación y puntos de referencia. La tabla de clasificación más utilizada es la de la comunidad [LM Arena](https://lmarena.ai). Además, la [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) se centra en el rendimiento de los modelos open-weights en puntos de referencia comunes como [MMLU-Pro](https://arxiv.org/abs/2406.01574).  There are also specialized benchmarks which measure factors like [emotional intelligence](https://eqbench.com), ["uncensored general intelligence"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard), and [many others](https://nebuly.com/blog/llm-leaderboards).

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

**Kobold.cpp** is an AI client that runs locally on your Windows, Mac, or Linux computer. Es una opción excelente si lo que buscas es una gran personalización y ajuste, por ejemplo para juegos de rol.

Además de soportar una amplia gama de modelos de texto, Kobold.cpp también soporta generadores de imágenes como [Stable Diffusion](https://stability.ai/stable-image) y herramientas de reconocimiento automático de voz como [Whisper](https://github.com/ggerganov/whisper.cpp).

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
<p class="admonition-title">Problemas de Compatibilidad</p>

Kobold.cpp podría no funcionar en ordenadores sin soporte AVX/AVX2.

</div>

Kobold.cpp te permite modificar parámetros como la temperatura del modelo de IA y el prompt de sistema del chat de IA. También permite crear un túnel de red para acceder a los modelos de IA desde otros dispositivos, como el teléfono.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Ollama Logo](assets/img/ai-chat/ollama.png){align=right}

**Ollama** is a command-line AI assistant that is available on macOS, Linux, and Windows. Ollama es una gran elección si buscas un cliente de IA fácil de usar, ampliamente compatible y rápido gracias a su uso de la inferencia y otras técnicas. Tampoco requiere ninguna configuración manual.

Además de soportar una amplia gama de modelos de texto, Ollama también soporta modelos [LLaVA](https://github.com/haotian-liu/LLaVA) y tiene soporte experimental para las [capacidades vision de Llama] (https://huggingface.co/blog/llama32#what-is-llama-32-vision) de Meta.

[:octicons-home-16: Página Principal](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Código Fuente" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Política de Seguridad" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama simplifica el proceso de creación de un chat de IA local descargando automáticamente el modelo de IA que deseas utilizar. Por ejemplo, ejecutar `ollama run llama3.2` descargará y ejecutará automáticamente el modelo Llama 3.2. Además, Ollama mantiene su propia [biblioteca de modelos](https://ollama.com/library) donde aloja los archivos de varios modelos de IA. De este modo se garantiza que los modelos se examinan tanto en lo que respecta al rendimiento como a la seguridad, eliminando la necesidad de verificar manualmente la autenticidad de los modelos.

### Llamafile

<div class="admonition recommendation" markdown>

![Llamafile Logo](assets/img/ai-chat/llamafile.webp){align=right}

**Llamafile** is a lightweight, single-file executable that allows users to run LLMs locally on their own computers without any setup involved. Está [respaldado por Mozilla](https://hacks.mozilla.org/2023/11/introducing-llamafile) y disponible en Linux, macOS y Windows.

Llamafile también es compatible con LLaVA. Sin embargo, no admite el reconocimiento de voz ni la generación de imágenes.

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

Mozilla ha puesto a disposición llamafiles solo para algunos modelos de Llama y Mistral, mientras que hay pocos llamafiles de terceros disponibles. Moreover, Windows limits `.exe` files to 4 GB, and most models are larger than that.

Para evitar estos problemas, puedes [cargar weights externos](https://github.com/Mozilla-Ocho/llamafile#using-llamafile-with-external-weights).

## Descarga Segura de Modelos

Si utilizas un cliente de IA que mantiene su propia biblioteca de archivos modelo (como [Ollama](#ollama-cli) y [Llamafile](#llamafile)), deberías descargarlo desde allí. Sin embargo, si quieres descargar modelos que no están presentes en su biblioteca, o utilizar un cliente de IA que no mantiene su biblioteca (como [Kobold.cpp](#koboldcpp)), tendrás que tomar medidas adicionales para asegurarte de que el modelo de IA que descargas es seguro y legítimo.

Recomendamos descargar archivos modelo de Hugging Face, ya que ofrece varias funciones para comprobar que su descarga es auténtica y segura.

Para comprobar la autenticidad y seguridad del modelo, busca:

- Tarjetas modelo con documentación clara
- Un distintivo de organización verificada
- Comentarios de la comunidad y estadísticas de uso
- Un distintivo "Seguro" junto a la ficha del modelo (solo Hugging Face)
- Checksums coincidentes[^1]
    - En Hugging Face, puedes encontrar el hash haciendo clic en un archivo de modelo y buscando el botón **Copy SHA256** debajo de él. Debes comparar esta checksum con la del fichero modelo que has descargado.

A downloaded model is generally safe if it satisfies all the above checks.

## Criterios

Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos. Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista antes de decidir utilizar un proyecto y realices tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe ser de código abierto.
- No debe transmitir datos personales, incluidos los del chat.
- Debe ser multiplataforma.
- No debe requerir GPU.
- Must support GPU-powered, fast inference.
- No debe requerir conexión a Internet.

### Mejor Caso

Nuestros criterios para el mejor de los casos representan lo que nos _gustaría_ ver en el proyecto perfecto de esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Should be easy to download and set up, e.g. with a one-click installation process.
- Debería tener una opción de descarga de modelos integrada.
- El usuario debería poder modificar los parámetros de la LLM, como su prompt de sistema o su temperatura.

\*[LLaVA]: Large Language and Vision Assistant (multimodal AI model)
\*[LLM]: Large Language Model (AI model such as ChatGPT)
\*[LLMs]: Large Language Models (AI models such as ChatGPT)
\*[open-weights models]: AI models that anyone can download and use, but the underlying training data and/or algorithms for them are proprietary.
\*[system prompt]: The general instructions given by a human to guide how an AI chat should operate.
\*[temperature]: A parameter used in AI models to control the level of randomness and creativity in the generated text.

[^1]: La checksum de un archivo es un tipo de huella digital antimanipulación. Un desarrollador suele proporcionar una checksum en un archivo de texto que puede descargarse por separado, o en la propia página de descarga. Verificar que la checksum del archivo descargado coincide con la proporcionada por el desarrollador ayuda a garantizar que el archivo es auténtico y no ha sido manipulado durante el transporte. Puedes utilizar comandos como `sha256sum` en Linux y macOS, o `certutil -hashfile file SHA256` en Windows para generar la checksum del archivo descargado.
