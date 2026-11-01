---
meta_title: "أفضل تطبيقات الدردشة بالذكاء الاصطناعي: بدائل خاصة لـ ChatGPT - Privacy Guides"
title: "الدردشة بالذكاء الاصطناعي"
icon: material/assistant
description: على عكس ChatGPT من OpenAI ومنافسيه من شركات التقنية الكبرى، تعمل أدوات الذكاء الاصطناعي هذه محليا على جهاز الكمبيوتر، بحيث لا تغادر بياناتك جهازك.
cover: ai-chatbots.webp
---

<small>يحمي من التهديدات التالية:</small>

- [:material-server-network: مقدّمو الخدمات](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash:رأسمالية المراقبة](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: الرقابة](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

أصبح استخدام الدردشة **بالذكاء الاصطناعي**، المعتمدة على الـ (LLMs)، أكثر شيوعا منذ إطلاق ChatGPT عام 2022. يمكن أن تساعدنا نماذج اللغة الكبيرة (LLMs) على تحسين كتابتنا، وفهم المواضيع غير المألوفة، والإجابة عن مجموعة واسعة من الأسئلة. تعمل هذه النماذج من خلال التنبؤ إحصائيا بالكلمة التالية في ردودها، اعتمادا على كميات هائلة من البيانات التي جُمعت من الإنترنت.

## مخاوف الخصوصية المتعلقة بالـ (LLMs)

لكن البيانات المستخدمة لتدريب نماذج الذكاء الاصطناعي تتضمن كميات هائلة من البيانات المتاحة للعامة، والتي جُمعت من الإنترنت، وقد تحتوي على معلومات حساسة مثل الأسماء والعناوين. غالبا ما تجمع برامج الذكاء الاصطناعي السحابية (Cloud-based AI) [البيانات التي تُدخلها إليها](https://openai.com/policies/row-privacy-policy)، ما يعني أن محادثاتك ليست خاصة عن الشركات التي تدير هذه البرامج. وتزيد هذه الممارسة أيضا من خطر حدوث تسريبات للبيانات. بالإضافة إلى ذلك، هناك احتمال حقيقي أن يسرّب أحد نماذج الـ (LLMs) معلومات من محادثاتك الخاصة خلال محادثات لاحقة مع مستخدمين آخرين.

إذا كانت هذه الممارسات تثير قلقك، فيمكنك إما الامتناع عن استخدام الذكاء الاصطناعي، أو استخدام [نماذج مفتوحة المصدر بالكامل](https://proton.me/blog/how-to-build-privacy-first-ai) تنشر بيانات تدريبها علنا وتتيح لك الاطلاع عليها. ومن هذه النماذج [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514) الذي طوّرته [Ai2](https://allenai.org/open-data).

وبدلا من ذلك، يمكنك تشغيل نماذج الذكاء الاصطناعي محليا على جهازك، بحيث لا تغادر بياناتك الجهاز ولا تُشارك مع أي جهات خارجية. لذلك، تُعد النماذج التي تعمل محليًا بديلًا أكثر خصوصية وأمانًا من الحلول السحابية، وتتيح لك مشاركة معلومات حساسة مع نموذج الذكاء الاصطناعي دون قلق.

## نماذج الذكاء الاصطناعي

### متطلبات الأجهزة لتشغيل نماذج الذكاء الاصطناعي محليًا

كما أن تشغيل النماذج محليًا سهل نسبيا ومتاح للكثيرين. يمكن تشغيل النماذج الأصغر حجما، وإن كان ذلك بسرعة أقل، على أجهزة تحتوي على ذاكرة RAM بسعة 8 GB فقط. للحصول على أفضل تجربة، يُفضل استخدام جهاز بمواصفات قوية، مثل بطاقة رسوميات منفصلة (GPU) تحتوي على ذاكرة VRAM كافية، أو جهاز حديث مزود بذاكرة LPDDR5X سريعة.

يمكن عادةً التمييز بين نماذج الـ (LLMs) من خلال عدد المعاملات (Parameters) التي تحتوي عليها، والذي قد يتراوح بين 1.3 مليار و405 مليارات في النماذج مفتوحة المصدر المتاحة للمستخدمين. على سبيل المثال، النماذج التي تحتوي على أقل من 6.7 مليار معامل مناسبة فقط للمهام البسيطة، مثل تلخيص النصوص، بينما توفر النماذج التي تحتوي على ما بين 7 و13 مليار معامل توازنا ممتازا بين الجودة والسرعة. عادةً ما تحتوي النماذج ذات قدرات الاستدلال المتقدمة على نحو 70 مليار معامل.

عند استخدام أجهزة مخصصة للمستهلكين، يُنصح عموما باستخدام [النماذج المكمّمة (Quantized Models)](https://huggingface.co/docs/optimum/en/concept_guides/quantization) لتحقيق أفضل توازن بين جودة النموذج وأدائه. اطّلع على الجدول أدناه لمعرفة المتطلبات المعتادة لتشغيل النماذج المكممة (Quantized Models) بمختلف أحجامها بشكل أكثر دقة.

| حجم النموذج (بعدد المعاملات) | الحد الأدنى لذاكرة الـ RAM | الحد الأدنى لمواصفات المعالج                             |
| ----------------------------------------------- | -------------------------- | -------------------------------------------------------- |
| 7B                                              | 8 GB                       | معالج CPU حديث (يدعم AVX2)            |
| 13B                                             | 16 GB                      | معالج CPU حديث (يدعم AVX2)            |
| 70B                                             | 72 GB                      | بطاقة رسوميات (GPU) مزودة بذاكرة VRAM |

لتشغيل الذكاء الاصطناعي محليا على جهازك، تحتاج إلى نموذج ذكاء اصطناعي وبرنامج لتشغيله.

### اختيار النموذج

تتوفر نماذج كثيرة يمكنك تنزيلها واستخدامها بموجب تراخيص تسمح باستخدامها بحرية. منصة [Hugging Face](https://huggingface.co/models) هي منصة تتيح لك استعراض نماذج الذكاء الاصطناعي والبحث عنها وتنزيلها بصيغ شائعة مثل [GGUF](https://huggingface.co/docs/hub/en/gguf). من الشركات الكبرى التي تقدم نماذج جيدة بأوزان مفتوحة (Open Weights): Mistral وMeta وMicrosoft وGoogle. لكن تتوفر أيضا نماذج كثيرة طورها المجتمع، بالإضافة إلى نماذج [خضعت لضبط دقيق (Fine-tuning)](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning). كما ذكرنا سابقا، توفر النماذج المكممة (Quantized Models) أفضل توازن بين جودة النموذج وأدائه عند استخدام أجهزة مخصصة للمستهلكين.

لمساعدتك في اختيار نموذج يناسب احتياجاتك، يمكنك الاطلاع على تصنيفات النماذج واختبارات الأداء (Benchmarks). أكثر تصنيفات نماذج الذكاء الاصطناعي استخدامًا هو [LM Arena](https://lmarena.ai)، الذي يعتمد على تقييمات المستخدمين. بالإضافة إلى ذلك، يركز [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) على تقييم أداء النماذج ذات الأوزان المفتوحة (Open Weights) باستخدام اختبارات أداء معيارية شائعة مثل [MMLU-Pro](https://arxiv.org/abs/2406.01574). توجد أيضا اختبارات أداء متخصصة تقيس جوانب مثل [الذكاء العاطفي](https://eqbench.com) و["الذكاء العام دون رقابة على المحتوى"](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard) و[العديد من الجوانب الأخرى](https://nebuly.com/blog/llm-leaderboards).

## برامج الدردشة بالذكاء الاصطناعي

| الميزة                                                           | [Kobold.cpp](#koboldcpp)                                      | [Ollama](#ollama-cli)                                                         | [Llamafile](#llamafile)                                                                                          |
| ---------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| دعم الـ (GPU)                                 | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                                    |
| توليد الصور                                                      | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                      |
| التعرّف على الكلام                                               | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                      |
| تنزيل النماذج تلقائيًا                                           | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } عدد النماذج المتاحة محدود |
| إعدادات المعاملات المخصصة (Custom Parameters) | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                                    |
| متعدد المنصات                                                    | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } قيود على الحجم في Windows |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Kobold.cpp Logo](assets/img/ai-chat/kobold.png){align=right}

برنامج Kobold.cpp هو برنامج لتشغيل الذكاء الاصطناعي محليا على جهازك، سواء كنت تستخدم Windows أو Mac أو Linux. يُعد خيارا ممتازا إذا كنت تبحث عن إمكانيات واسعة لتخصيص الإعدادات وضبطها، مثل استخدامه في تقمص الأدوار.

بالإضافة إلى دعمه لمجموعة واسعة من النماذج النصية، يدعم Kobold.cpp أيضًا أدوات توليد الصور مثل [Stable Diffusion](https://stability.ai/stable-image)، وأدوات التعرّف التلقائي على الكلام مثل [Whisper](https://github.com/ggerganov/whisper.cpp).

[:octicons-repo-16: Repository](https://github.com/LostRuins/koboldcpp#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:fontawesome-brands-windows: وندوز](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: لينكس](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">مشكلات التوافق</p>

قد لا يعمل Kobold.cpp على أجهزة الكمبيوتر التي لا تدعم AVX أو AVX2.

</div>

يتيح لك Kobold.cpp تغيير إعدادات مثل مستوى العشوائية في ردود نموذج الذكاء الاصطناعي (Temperature)، والتعليمات الأساسية التي تحدد طريقة استجابته (System Prompt). ويدعم أيضا إنشاء نفق اتصال شبكي (Network Tunnel) يتيح لك الوصول إلى نماذج الذكاء الاصطناعي من أجهزة أخرى، مثل هاتفك.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Ollama Logo](assets/img/ai-chat/ollama.png){align=right}

برنامج Ollama هو مساعد ذكاء اصطناعي يعمل من خلال سطر الأوامر (Command Line)، ومتوفر على أنظمة macOS وLinux وWindows. يُعد Ollama خيارا ممتازا إذا كنت تبحث عن برنامج ذكاء اصطناعي سهل الاستخدام، ومتوافق مع أجهزة وأنظمة تشغيل كثيرة، ويوفر أداء سريعا بفضل التقنيات التي يستخدمها. كما أنه لا يتطلب أي إعداد يدوي.

بالإضافة إلى دعمه لمجموعة واسعة من النماذج النصية، يدعم Ollama أيضًا نماذج [LLaVA](https://github.com/haotian-liu/LLaVA)، ويوفر دعما تجريبيا [لقدرات Llama على فهم الصور](https://huggingface.co/blog/llama32#what-is-llama-32-vision) من Meta.

[:octicons-home-16: Homepage](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:fontawesome-brands-windows: وندوز](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: لينكس](https://ollama.com/download/linux)

</details>

</div>

يسهّل Ollama تشغيل الدردشة بالذكاء الاصطناعي محليا على جهازك، إذ ينزّل النموذج الذي تريد استخدامه تلقائيًا. على سبيل المثال، عند تنفيذ الأمر `ollama run llama3.2`، سيُنزل Ollama نموذج Llama 3.2 ويشغله تلقائيا. بالإضافة إلى ذلك، يوفر Ollama [مكتبة خاصة بالنماذج](https://ollama.com/library) تضم ملفات نماذج ذكاء اصطناعي متنوعة. وهذا يضمن مراجعة النماذج للتأكد من أدائها وأمانها، مما يغنيك عن التحقق يدويا من أصالتها ومصدرها.

### Llamafile

<div class="admonition recommendation" markdown>

![Llamafile Logo](assets/img/ai-chat/llamafile.webp){align=right}

برنامج **Llamafile** هو برنامج خفيف يأتي في ملف تنفيذي واحد، ويتيح لك تشغيل نماذج اللغة الكبيرة (LLMs) محليا على جهازك دون الحاجة إلى أي إعدادات. يحظى بدعم [Mozilla](https://hacks.mozilla.org/2023/11/introducing-llamafile)، ويتوفر على أنظمة Linux وmacOS وWindows.

يدعم Llamafile أيضا نماذج LLaVA. لكنه لا يدعم التعرف على الكلام أو توليد الصور.

[:octicons-repo-16: Repository](https://github.com/Mozilla-Ocho/llamafile#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#quickstart){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="Source Code" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="Security Policy" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:fontawesome-brands-windows: وندوز](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-apple: macOS](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-linux: لينكس](https://github.com/Mozilla-Ocho/llamafile#quickstart)

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

- Must be open source.
- Must not transmit personal data, including chat data.
- Must be multi-platform.
- Must not require a GPU.
- Must support GPU-powered, fast inference.
- Must not require an internet connection.

### Best-Case

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

[^1]: A file checksum is a type of anti-tampering fingerprint. A developer usually provides a checksum in a text file that can be downloaded separately, or on the download page itself. Verifying that the checksum of the file you downloaded matches the one provided by the developer helps ensure that the file is genuine and wasn't tampered with in transit. يمكنك استخدام أوامر مثل `sha256sum` على Linux وmacOS، أو `certutil -hashfile file SHA256` على Windows، لحساب قيمة التحقق (Checksum) للملف الذي نزلته.
