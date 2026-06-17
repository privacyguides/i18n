---
meta_title: "Chat IA recommandé : alternatives privées à ChatGPT – Privacy Guides"
title: "Chat IA"
icon: material/assistant
description: "Contrairement à ChatGPT d'OpenAI et à ses concurrents du secteur des « Big Tech », ces outils d'IA fonctionnent en local : vos données ne quittent donc jamais votre ordinateur."
cover: ai-chatbots.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-server-network: Fournisseurs de Services](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalisme de Surveillance](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: Censure](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

L'utilisation des **chatbots basés sur l'IA**, également appelés « grands modèles linguistiques » (LLM), s'est généralisée depuis le lancement de ChatGPT en 2022. Les modèles de langage de grande envergure (LLM) peuvent nous aider à mieux rédiger, à comprendre des sujets qui ne nous sont pas familiers ou à répondre à un large éventail de questions. Ils fonctionnent en prédisant statistiquement le mot suivant dans leurs réponses, à partir d'une immense quantité de données extraites du Web.

## Problèmes de confidentialité liés aux modèles de langage

Les données utilisées pour entraîner les modèles d'IA comprennent toutefois une quantité considérable de données accessibles au public, extraites du Web, qui peuvent contenir des informations sensibles telles que des noms et des adresses. Les logiciels d'IA basés sur le cloud [collectent souvent vos données](https://openai.com/policies/row-privacy-policy), ce qui signifie que vos conversations ne sont pas confidentielles à leurs yeux. Cette pratique comporte également un risque de violation de données. De plus, il existe un risque réel qu’un LLM divulgue les informations de vos conversations privées lors de futures discussions avec d’autres utilisateurs.

Si ces pratiques vous préoccupent, vous pouvez soit refuser d'utiliser l'IA, soit recourir à des [modèles véritablement open source](https://proton.me/blog/how-to-build-privacy-first-ai) dont les ensembles de données d'entraînement sont rendus publics et que vous pouvez consulter. L'un de ces modèles est [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514), développé par [Ai2](https://allenai.org/open-data).

Vous pouvez également exécuter des modèles d'IA en local, de sorte que vos données ne quittent jamais votre appareil et ne soient donc jamais partagées avec des tiers. À ce titre, les modèles locaux constituent une alternative plus confidentielle et plus sécurisée que les solutions basées sur le cloud et vous permettent de partager sans crainte des informations sensibles avec le modèle d'IA.

## Modèles d'IA

### Hardware pour les modèles d'IA locaux

Les modèles locaux sont également relativement accessibles. Il est possible d'exécuter des modèles plus petits à des vitesses réduites avec seulement 8 Go de mémoire vive. L'utilisation d'un hardware plus performant, tel qu'un GPU dédié doté d'une mémoire vidéo (VRAM) suffisante ou un système moderne équipé d'une mémoire LPDDR5X rapide, garantit une expérience optimale.

Les modèles de langage à grande échelle (LLM) se distinguent généralement par le nombre de paramètres, qui peut varier entre 1,3 milliard et 405 milliards pour les modèles open source accessibles aux utilisateurs finaux. Par exemple, les modèles comportant moins de 6,7 milliards de paramètres ne conviennent qu’à des tâches élémentaires telles que la synthèse de textes, tandis que ceux comptant entre 7 et 13 milliards de paramètres constituent un excellent compromis entre qualité et rapidité. Les modèles dotés de capacités de raisonnement avancées ont généralement une taille d'environ 70 milliards.

Pour le hardware grand public, il est généralement recommandé d'utiliser des [modèles quantifiés](https://huggingface.co/docs/optimum/en/concept_guides/quantization) afin d'obtenir le meilleur compromis entre la qualité du modèle et les performances. Consultez le tableau ci-dessous pour obtenir des informations plus précises sur les exigences types relatives aux différentes tailles de modèles quantifiés.

| Taille du modèle (en nombre de paramètres) | Mémoire vive minimale | Configuration minimale du processeur                           |
| ------------------------------------------------------------- | --------------------- | -------------------------------------------------------------- |
| 7B                                                            | 8 Go                  | Processeur moderne (prise en charge d'AVX2) |
| 13B                                                           | 16 Go                 | Processeur moderne (prise en charge d'AVX2) |
| 70B                                                           | 72 Go                 | Carte graphique avec mémoire vidéo (VRAM)   |

Pour exécuter l'IA en local, vous avez besoin à la fois d'un modèle d'IA et d'un client d'IA.

### Choisir un Modèle

Il existe de nombreux modèles disponibles au téléchargement sous licence libre [Hugging Face](https://huggingface.co/models) est une plateforme qui vous permet de parcourir, de rechercher et de télécharger des modèles dans des formats courants tels que [GGUF](https://huggingface.co/docs/hub/en/gguf). Parmi les entreprises proposant de bons modèles à poids ouverts, on trouve de grands noms tels que Mistral, Meta, Microsoft et Google. Il existe toutefois également de nombreux modèles communautaires et des modèles [fine-tunés](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)). Comme indiqué plus haut, les modèles quantifiés offrent le meilleur compromis entre qualité et performances pour les utilisateurs disposant d'un hardware grand public.

Pour vous aider à choisir un modèle adapté à vos besoins, vous pouvez consulter les classements et les tests de performance. Le classement le plus utilisé est celui géré par la communauté, [LM Arena](https://lmarena.ai). Par ailleurs, le [classement OpenLLM](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) se concentre sur les performances des modèles à poids ouverts sur des benchmarks courants tels que [MMLU-Pro](https://arxiv.org/abs/2406.01574). Il existe également des tests de référence spécialisés qui évaluent des facteurs tels que [l'intelligence émotionnelle](https://eqbench.com), [« l'intelligence générale non censurée »](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard) et [bien d'autres encore](https://nebuly.com/blog/llm-leaderboards).

## Clients de chat IA

| Fonctionnalité                         |                                                                               | [Ollama](#ollama-cli)                                                         | [Llamafile](#llamafile)                                                                                                    |
| -------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Prise en charge des GPU                | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                                              |
| Génération d'images                    | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                                |
| Reconnaissance vocale                  | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                                |
| Téléchargement automatique des modèles | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Peu de modèles disponibles          |
| Paramètres personnalisés               | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                                              |
| Multi-plateforme                       | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Restrictions de taille sous Windows |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Logo Kobold.cpp](assets/img/ai-chat/kobold.png){align=right}

**Kobold.cpp** est un client de chat IA qui s'exécute localement sur votre ordinateur Windows, Mac ou Linux. C'est un excellent choix si vous recherchez des possibilités de personnalisation et de réglages poussés, notamment pour les jeux de rôle.

Outre la prise en charge d'une large gamme de modèles textuels, Kobold.cpp prend également en charge des générateurs d'images tels que [Stable Diffusion](https://stability.ai/stable-image) et des outils de reconnaissance vocale automatique tels que [Whisper](https://github.com/ggerganov/whisper.cpp).

[:octicons-repo-16: Dépôt](https://github.com/LostRuins/koboldcpp#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="Code source" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="Politique de sécurité" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: Linux](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">Problèmes de compatibilité</p>

Il se peut que « Kobold.cpp » ne fonctionne pas sur les ordinateurs ne prenant pas en charge les instructions AVX/AVX2.

</div>

Kobold.cpp vous permet de modifier certains paramètres, tels que la « température » du modèle d'IA et le message d'accueil du système de chat IA. Il permet également de créer un tunnel réseau pour accéder à des modèles d'IA depuis d'autres appareils, comme votre téléphone.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Logo Ollama](assets/img/ai-chat/ollama.png){align=right}

**Ollama** est un assistant IA en ligne de commande disponible sur macOS, Linux et Windows. Ollama est un excellent choix si vous recherchez un client IA facile à utiliser, largement compatible et rapide grâce à l'utilisation de l'inférence et d'autres techniques. Il ne nécessite pas de configuration manuelle particulière.

Outre la prise en charge d'un large éventail de modèles textuels, Ollama prend également en charge les modèles [LLaVA](https://github.com/haotian-liu/LLaVA) et offre une prise en charge expérimentale des [fonctionnalités de vision de Llama](https://huggingface.co/blog/llama32#what-is-llama-32-vision) de Meta.

[:octicons-home-16: Page d'accueil](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Code source" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Politique de sécurité" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama simplifie la mise en place d'un chat IA local en téléchargeant automatiquement le modèle d'IA que vous souhaitez utiliser. Par exemple, la commande `ollama run llama3.2` permet de télécharger et d'exécuter automatiquement le modèle Llama 3.2. Par ailleurs, Ollama gère sa propre [bibliothèque de modèles](https://ollama.com/library) dans laquelle sont hébergés les fichiers de divers modèles d'IA. Cela garantit que les modèles sont contrôlés tant au niveau de leurs performances que de leur sécurité, ce qui évite d'avoir à vérifier manuellement leur authenticité.

### Llamafile

<div class="admonition recommendation" markdown>

![Logo Llamafile](assets/img/ai-chat/llamafile.webp){align=right}

**Llamafile** est un binaire léger, constitué d'un seul fichier, qui permet aux utilisateurs d'exécuter des modèles de langage (LLM) localement sur leur propre ordinateur, sans aucune configuration préalable. Le projet est [soutenu par Mozilla](https://hacks.mozilla.org/2023/11/introducing-llamafile) et disponible sous Linux, macOS et Windows.

Llamafile prend également en charge LLaVA. Cependant, il ne prend pas en charge la reconnaissance vocale ni la génération d'images.

[:octicons-repo-16: Dépôt](https://github.com/Mozilla-Ocho/llamafile#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#quickstart){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="Code source" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="Politique de sécurité" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Mozilla-Ocho/llamafile#quickstart)
-
-

</details>

</div>





##

Toutefois, si vous souhaitez télécharger des modèles qui ne figurent pas dans leur bibliothèque, ou utiliser un client IA qui ne met pas à jour sa bibliothèque (comme [Kobold.cpp](#koboldcpp)), vous devrez prendre des précautions supplémentaires pour vous assurer que le modèle IA que vous téléchargez est sûr et légitime.

Nous vous recommandons de télécharger les fichiers de modèles depuis Hugging Face, car cette plateforme propose plusieurs fonctionnalités permettant de vérifier que votre téléchargement est authentique et peut être utilisé en toute sécurité.

Pour vérifier l'authenticité et la sécurité du modèle, vérifiez les points suivants :

- Fiches techniques accompagnées d'une documentation claire
- Un badge d'organisation vérifiée
- Avis de la communauté et statistiques d'utilisation
- Un badge « Safe » à côté du fichier du modèle (sur Hugging Face uniquement)
- Checksums concordants[^1]
  - Sur Hugging Face, vous pouvez trouver le hachage en cliquant sur un fichier de modèle et en recherchant le bouton **Copier SHA256** situé en dessous. Vous devriez comparer ce checksum avec celui du fichier du modèle que vous avez téléchargé.

Un modèle téléchargé est généralement sûr s'il répond à tous les critères de vérification mentionnés ci-dessus.

## Critères

Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons. Outre [nos critères habituels](about/criteria.md), nous avons défini un ensemble précis d'exigences afin de pouvoir formuler des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que celui-ci répond bien à vos besoins.

### Exigences minimales

- Doit être open-source.
- Il est interdit de transmettre des données à caractère personnel, y compris les données issues des discussions en ligne.
- Dois être multiplateforme.
- Ne doit pas nécessiter de carte graphique.
- Doit prendre en charge l'inférence rapide via le GPU.
- Ne doit pas nécessiter de connexion Internet.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Le projet devrait être facile à télécharger et à configurer, par exemple grâce à une procédure d'installation en un clic.
- Il devrait avoir une option intégrée permettant de télécharger des modèles.
- L'utilisateur doit pouvoir modifier les paramètres du LLM, tels que son prompt système ou sa température.

\*[LLaVA] : Assistant multimodal de langage et de vision (modèle d'IA multimodal)
\*[LLM] : Modèle de langage à grande échelle (modèle d’IA tel que ChatGPT)
\*[LLMs] : grands modèles linguistiques (modèles d’IA tels que ChatGPT)
\*[modèles à paramètres ouverts] : modèles d’IA que tout le monde peut télécharger et utiliser, mais dont les données d’entraînement et/ou les algorithmes sous-jacents sont propriétaires.
\*[prompt système] : Instructions générales données par un humain pour définir le mode de fonctionnement d'un chatbot basé sur l'IA.
\*[température] : paramètre utilisé dans les modèles d'IA pour contrôler le niveau d'aléatoire et de créativité du texte généré.

[^1]: La somme de contrôle d'un fichier est une sorte d'empreinte permettant de détecter toute altération. Un développeur fournit généralement un checksum dans un fichier texte pouvant être téléchargé séparément, ou directement sur la page de téléchargement. Vérifier que le checksum du fichier que vous avez téléchargé correspond à cellui fourni par le développeur permet de s'assurer que le fichier est authentique et qu'il n'a pas été altéré pendant le transfert. Vous pouvez utiliser des commandes telles que `sha256sum` sous Linux et macOS, ou `certutil -hashfile fichier SHA256` sous Windows pour générer le checksum du fichier téléchargé.
