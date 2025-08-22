---
title: Sur macOS
icon: material/apple-finder
description: macOS est le système d'exploitation d'Apple pour ordinateurs de bureau fonctionnant avec leur propre matériel pour assurer une sécurité renforcée.
---

**macOS** est un système d'exploitation Unix développé par Apple pour leurs ordinateurs Mac. Pour améliorer la confidentialité de macOS, il est possible de désactiver la télémétrie et renforcer les paramètres existants de confidentialité et de sécurité.

Les anciens Mac à base de processeur Intel et les Hackintosh ne prennent pas en charge toutes les fonctions de sécurité offertes par macOS. Pour améliorer la sécurité des données, nous recommandons d'utiliser un Mac plus récent avec [Apple Silicon](https://support.apple.com/HT211814).

## Remarques concernant la vie privée

macOS pose quelques problèmes importants en matière de protection de la vie privée, qu'il convient de prendre en compte. Ils concernent le système d'exploitation lui-même, et non les autres applications et services d'Apple.

### Verrouillage d'activation

Les nouveaux appareils Apple Silicon peuvent être configurés sans connexion internet. Cependant, la récupération ou la réinitialisation de votre Mac **nécessitera** une connexion internet aux serveurs d'Apple pour vérifier la base de données Verrouillage d'activation des appareils perdus ou volés.

### Contrôles de révocation des applications

macOS effectue des contrôles en ligne lorsque vous ouvrez une application afin de vérifier si elle contient des logiciels malveillants connus et si le certificat de signature du développeur a été révoqué.

Le service OCSP d'Apple utilise le chiffrement HTTPS, de sorte que seul Apple soit en mesure de voir quelles applications vous ouvrez. Ils ont [publié des informations](https://support.apple.com/HT202491) sur leur politique de journalisation pour ce service. Ils ont également [promis](http://lapcatsoftware.com/articles/2024/8/3.html) d'ajouter un mécanisme permettant aux personnes de refuser ce contrôle en ligne, mais celui-ci n'a pas été ajouté à macOS.

Bien que vous [puissiez](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) désactiver manuellement cette vérification assez facilement, nous vous déconseillons de le faire à moins que les vérifications de révocation effectuées par macOS ne vous compromettent gravement, car elles jouent un rôle important en empêchant l'exécution d'applications compromises.

## Configuration recommandée

Lorsque vous configurez votre Mac pour la première fois, vous disposez d'un compte d'administrateur, dont les privilèges sont plus élevés que ceux d'un compte d'utilisateur standard. macOS dispose d'un certain nombre de protections qui empêchent les logiciels malveillants et d'autres programmes d'abuser de vos privilèges d'administrateur, de sorte que l'utilisation de ce compte est généralement sûre.

Cependant, des exploits dans des utilitaires de protection tels que `sudo` ont été [découverts dans le passé](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass). Si vous souhaitez éviter que les programmes que vous exécutez n'abusent de vos privilèges d'administrateur, vous pouvez envisager de créer un deuxième compte d'utilisateur standard, que vous utiliserez pour les opérations quotidiennes. Cela présente l'avantage supplémentaire de rendre plus évident le fait qu'une application a besoin d'un accès administrateur, parce qu'elle vous demandera à chaque fois de fournir des informations d'identification.

Si vous utilisez un deuxième compte, il n'est pas strictement nécessaire de vous connecter à votre compte administrateur d'origine à partir de l'écran de connexion de macOS. Lorsque vous effectuez, en tant qu'utilisateur standard, une opération nécessitant des autorisations d'administrateur, le système vous invite à vous authentifier, ce qui vous permet d'entrer une seule fois vos informations d'identification d'administrateur en tant qu'utilisateur standard. Apple fournit des [conseils](https://support.apple.com/HT203998) sur la façon de masquer votre compte administrateur si vous préférez ne voir qu'un seul compte sur votre écran de connexion.

### iCloud

Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés *auxquelles Apple a accès* par défaut. C'est ce qu'Apple appelle la [Protection Standard des Données](https://support.apple.com/en-us/102651).

Par conséquent, si vous utilisez iCloud, vous devriez [activer la**Protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

Si vous souhaitez pouvoir installer des applications à partir de l'App Store mais que vous ne voulez pas activer iCloud, vous pouvez vous connecter à votre compte Apple à partir de l'App Store plutôt qu'à partir des **Réglages du Système**.

### Paramètres systèmes

Il y a un certain nombre de paramètres intégrés que vous devriez confirmer ou modifier pour renforcer votre système. Ouvrez l'application **Paramètres** :

#### Bluetooth

- [ ] Décochez **Bluetooth** (sauf si vous l'utilisez)

#### Réseau

Selon que vous utilisez **Wi-Fi** ou **Ethernet** (indiqué par un point vert et le mot "connecté"), cliquez sur l'icône correspondante.

Cliquez sur le bouton "Détails" à côté du nom de votre réseau :

- [x] Sélectionnez **Rotation** sous **Adresse Wi-Fi privée**

- [x] Cochez **Limiter le pistage des adresses IP**

##### Pare-feu

Votre pare-feu bloque les connexions réseau indésirables. Plus les réglages de votre pare-feu sont stricts, plus votre Mac est sécurisé. Toutefois, certains services seront bloqués. Vous devriez configurer votre pare-feu de manière à ce qu'il soit aussi strict que possible sans bloquer les services que vous utilisez.

- [x] Cochez **Pare-feu**

Cliquez sur le bouton **Options** :

- [x] Cochez **Bloquer toutes les connexions entrantes**

Si cette configuration est trop stricte, vous pouvez revenir et la décocher. Toutefois, macOS vous invitera généralement à autoriser les connexions entrantes pour une application si celle-ci le demande.

#### Général

Par défaut, le nom de votre appareil sera quelque chose comme "iMac de [votre nom]". Comme ce nom est diffusé publiquement sur votre réseau, vous pouvez souhaiter changer le nom de votre appareil en quelque chose de générique comme "Mac".

Cliquez sur **A propos** et tapez le nom de votre appareil dans le champ **Nom**.

##### Mises à jour du logiciel

Vous devriez installer automatiquement toutes les mises à jour disponibles pour vous assurer que votre Mac dispose des derniers correctifs de sécurité.

Cliquez sur la petite icône :material-information-outline: à côté de **Mises à jour automatiques** :

- [x] Cochez **Vérifier les mises à jour**

- [x] Cochez **Télécharger les nouvelles mises à jour lorsqu'elles sont disponibles**

- [x] Cochez **Installer les mises à jour de macOS**

- [x] Cochez **Installer les mises à jour d'applications à partir de l'App Store**

- [x] Cochez **Installer les réponses de sécurité et les fichiers système**

#### Confidentialité & sécurité

Chaque fois qu'une application demande une autorisation, celle-ci apparaît ici. Vous pouvez décider des applications pour lesquelles vous souhaitez autoriser ou refuser des autorisations spécifiques.

##### Services de localisation

Vous pouvez autoriser les services de localisation individuellement pour chaque application. Si vous n'avez pas besoin que des applications utilisent votre position, la désactivation complète des services de localisation est l'option la plus privée.

- [ ] Décochez **Services de localisation**

##### Statistiques & améliorations

Décidez si vous souhaitez partager les données analytiques avec Apple et les développeurs.

- [ ] Décochez **Partager les données analytiques du Mac**

- [ ] Décochez **Améliorer Siri & Dictée**

- [ ] Décochez **Partager avec les développeurs d'applications**

- [ ] Décochez **Partager les données analytiques iCloud** (visible si vous êtes connecté à iCloud)

##### Publicité Apple

Décidez si vous souhaitez des publicités personnalisées en fonction de votre utilisation.

- [ ] Décochez **Annonces personnalisées**

##### FileVault

Sur les appareils modernes dotés d'une Secure Enclave (puce de sécurité T2 Apple, Apple Silicon), vos données sont toujours chiffrées, mais elles sont déchiffrées automatiquement par une clé matérielle si votre appareil ne détecte pas qu'il a été altéré. L'activation de [FileVault](../encryption.md#filevault) requiert en outre votre mot de passe pour déchiffrer vos données, ce qui améliore considérablement la sécurité, en particulier lorsque l'ordinateur est éteint ou avant la première connexion après l'allumage.

Sur les anciens ordinateurs Mac à processeur Intel, FileVault est la seule forme de chiffrement de disque disponible par défaut et doit toujours être activé.

- [x] Cliquez sur **Activer**

##### Mode Isolement

Le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) désactive certaines fonctionnalités afin d'améliorer la sécurité. Certaines applications ou fonctionnalités ne fonctionneront pas de la même manière que lorsqu'il est désactivé. Par exemple, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers) et [WASM](https://developer.mozilla.org/docs/WebAssembly) sont désactivés dans Safari lorsque le mode Isolement est activé. Nous vous recommandons d'activer le mode Isolement et de voir s'il a un impact significatif sur votre utilisation, car la plupart des changements qu'il apporte sont faciles à vivre.

- [x] Cliquez sur **Activer**

### Adresse MAC aléatoire

macOS utilise une adresse MAC aléatoire lorsqu'il effectue des analyses Wi-Fi alors qu'il est déconnecté d'un réseau.

Vous pouvez configurer votre adresse MAC de manière à ce qu'elle soit aléatoire pour chaque réseau et qu'elle fasse l'objet d'une rotation occasionnelle afin d'empêcher le suivi entre les réseaux et sur le même réseau au fil du temps.

Allez dans **Paramètres Système** → **Réseaux** → **Wi-Fi** → **Détails** et réglez l'**adresse Wi-Fi privée** sur **Fixe** si vous souhaitez une adresse fixe mais unique pour le réseau auquel vous êtes connecté, ou sur **Rotation** si vous souhaitez qu'elle change au fil du temps.

Envisagez également de modifier votre nom d'hôte, qui est un autre identifiant d'appareil diffusé sur le réseau auquel vous êtes connecté. Vous pouvez définir votre nom d'hôte avec quelque chose de générique comme "MacBook Air", "Laptop", "MacBook Pro de John", ou "iPhone" dans **Réglages système** → **Général** → **Partage**. Certains [scripts de confidentialité](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) vous permettent de générer facilement des noms d'hôtes avec des noms aléatoires.

## Protections de sécurité

macOS utilise la défense en profondeur en s'appuyant sur plusieurs couches de protections logicielles et matérielles, avec des propriétés différentes. Cela garantit qu'une défaillance dans une couche ne compromet pas la sécurité globale du système.

### Sécurité du logiciel

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

macOS vous permet d'installer des mises à jour bêta. Elles sont instables et peuvent être accompagnées de données télémétriques supplémentaires puisqu'elles sont utilisées à des fins de test. Pour cette raison, nous vous recommandons d'éviter les logiciels bêta en général.

</div>

#### Volume du système signé

Les composants système de macOS sont protégés dans un volume système signé en lecture seule, ce qui signifie que ni vous ni les logiciels malveillants ne peuvent modifier les fichiers système importants.

Le volume du système est vérifié en cours d'exécution et toute donnée qui n'est pas signée par une signature cryptographique valide d'Apple sera rejetée.

#### Protection de l'intégrité du système

macOS définit certaines restrictions de sécurité qui ne peuvent pas être contournées. Il s'agit des contrôles d'accès obligatoires, qui constituent la base du sandbox, du contrôle parental et de la protection de l'intégrité du système dans macOS.

La protection de l'intégrité du système met en lecture seule les emplacements de fichiers critiques afin de les protéger contre toute modification par des codes malveillants. Cela s'ajoute à la protection de l'intégrité du noyau basée sur le matériel, qui empêche le noyau d'être modifié en mémoire.

#### Sécurité des applications

##### Sandbox des applications

Sur macOS, c'est le développeur qui détermine si une application est mise en bac à sable (sandbox) lorsqu'il la signe. L'App Sandbox protège contre les vulnérabilités dans les applications que vous exécutez en limitant ce à quoi un acteur malveillant peut accéder dans le cas où l'application est exploitée. L'App Sandbox ne peut *à lui seul* protéger contre les [:material-package-variant-closed-remove: Attaques de la Chaîne d'Approvisionnement ](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} par des développeurs malveillants. Dans ce cas de figure, le sandboxing doit être appliqué par quelqu'un d'autre que le développeur lui-même, comme c'est le cas sur l'App Store.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Les logiciels téléchargés en dehors de l'App Store officiel n'ont pas besoin d'être placés en sandbox. Si votre modèle de menace donne la priorité à la défense contre [:material-bug-outline: Attaques passives](../basics/common-threats.md#security-and-privacy){ .pg-orange }, vous pouvez alors vérifier si le logiciel que vous téléchargez en dehors de l'App Store est en bac à sable (sandbox), ce qui est laissé à l'appréciation du développeur.

</div>

Vous pouvez vérifier si une application utilise l'App Sandbox de plusieurs façons :

Vous pouvez vérifier si les applications déjà en cours d'exécution sont placées dans un bac à sable à l'aide du [Moniteur d'Activité](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Attention, ce n'est pas parce que l'un des processus d'une application est sandboxé que tous le sont.

</div>

Vous pouvez aussi vérifier les applications avant de les exécuter en lançant cette commande dans le terminal :

``` zsh
codesign -dvvv --entitlements - <path to your app>
```

Si une application est sandboxée, vous devriez obtenir le résultat suivant :

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

Si vous constatez que l'application que vous souhaitez utiliser n'est pas sandboxée, vous pouvez utiliser des méthodes de [compartimentage](../basics/common-threats.md#security-and-privacy) telles que des machines virtuelles ou des appareils séparés, utiliser une application similaire qui est sandboxée, ou choisir de ne pas utiliser l'application.

##### Hardened Runtime (exécution renforcée)

[L'exécution renforcée](https://developer.apple.com/documentation/security/hardened_runtime) est une forme de protection supplémentaire pour les applications qui empêche certains types d'exploitations. Il améliore la sécurité des applications contre de potentielles exploitations en désactivant certaines fonctions comme le JIT.

Vous pouvez vérifier si une application utilise le Hardened Runtime en utilisant cette commande :

``` zsh
codesign -dv <path to your app>
```

Si l'option Hardened Runtime est activée, vous verrez `flags=0x10000(runtime)`. La sortie `runtime` signifie que Hardened Runtime est activé. Il peut y avoir d'autres indicateurs, mais c'est l'indicateur runtime qui nous intéresse ici.

Vous pouvez activer une colonne dans Activity Monitor appelée "Restricted", qui est un drapeau empêchant les programmes d'injecter du code via l'[éditeur de liens dynamiques](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html) de macOS. Idéalement, la réponse devrait être "Oui".

##### Antivirus

macOS est doté de deux formes de défense contre les logiciels malveillants :

1. La protection contre le lancement de logiciels malveillants est assurée par le processus d'examen des applications de l'App Store, ou *Notarization* (fait partie de *Gatekeeper*), un processus au cours duquel les applications tierces sont analysées par Apple à la recherche de logiciels malveillants connus avant d'être autorisées à s'exécuter. Les applications doivent être signées par les développeurs à l'aide d'une clé fournie par Apple. Cela garantit que vous exécutez des logiciels provenant des vrais développeurs. La notarisation exige également que les développeurs activent le Hardened Runtime pour leurs applications, ce qui limite les vulnérabiltés.
2. La protection contre les autres logiciels malveillants et la remédiation des logiciels malveillants existants sur votre système sont assurées par *XProtect*, un logiciel antivirus plus traditionnel intégré à macOS.

Nous vous déconseillons d'installer des logiciels antivirus tiers, car ils n'ont généralement pas l'accès nécessaire au niveau du système pour fonctionner correctement, en raison des limitations imposées par Apple aux applications tierces, et parce que l'octroi des niveaux d'accès élevés qu'ils demandent pose souvent un risque encore plus grand pour la sécurité et la confidentialité de votre ordinateur.

##### Sauvegardes

macOS est livré avec un logiciel de sauvegarde automatique appelé [Time Machine](https://support.apple.com/HT201250), qui vous permet de créer des sauvegardes chiffrées sur un disque externe ou un lecteur réseau en cas de fichiers corrompus/supprimés.

### Sécurité matérielle

De nombreuses fonctions de sécurité modernes de macOS - telles que le Secure Boot moderne, l'atténuation des vulnérabilité au niveau matériel, les vérifications de l'intégrité du système d'exploitation et le chiffrement des fichiers - reposent sur l'Apple Silicon, et le matériel le plus récent d'Apple est toujours doté de la [meilleure sécurité](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Nous encourageons uniquement l'utilisation d'Apple Silicon, et non d'anciens ordinateurs Mac basés sur Intel, ou Hackintoshes.

Certaines de ces fonctions de sécurité modernes sont disponibles sur les anciens ordinateurs Mac à base d'Intel équipés de la puce de sécurité T2 d'Apple, mais cette puce est susceptible d'être exploitée par *checkm8*, ce qui pourrait compromettre sa sécurité.

Si vous utilisez des accessoires Bluetooth tels qu'un clavier, nous vous recommandons d'utiliser les accessoires officiels d'Apple car leur micrologiciel sera automatiquement mis à jour pour vous par macOS. L'utilisation d'accessoires tiers est possible, mais il faut penser à installer régulièrement les mises à jour du micrologiciel de ces accessoires.

Les SoC d'Apple s'attachent à minimiser la surface d'attaque en reléguant les fonctions de sécurité à un matériel dédié aux fonctionnalités limitées.

#### ROM d'amorçage

macOS empêche la persistance des logiciels malveillants en n'autorisant que les logiciels officiels d'Apple à s'exécuter au moment du démarrage ; c'est ce qu'on appelle le démarrage sécurisé. Les ordinateurs Mac le vérifient grâce à une partie de la mémoire en lecture seule du circuit intégré, appelée ROM d'amorçage, qui est mise en place lors de la fabrication de la puce.

La ROM d'amorçage constitue la racine de confiance du matériel. Cela garantit que les logiciels malveillants ne peuvent pas altérer le processus de démarrage. Lorsque votre Mac démarre, la ROM d'amorçage est la première chose qui s'exécute, formant le premier maillon de la chaîne de confiance.

Les ordinateurs Mac peuvent être configurés pour démarrer selon trois modes de sécurité : *Sécurité complète*, *Sécurité réduite*, et *Sécurité permissive*, le paramètre par défaut étant Sécurité complète. L'idéal est d'utiliser le mode de sécurité complète et d'éviter des choses comme les **extensions de noyau** qui vous obligent à réduire votre mode de sécurité. Veillez à [vérifier](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que vous utilisez le mode Sécurité complète.

#### Enclave sécurisée

Le Secure Enclave est une puce de sécurité intégrée à des appareils avec le Apple Silicon qui est responsable du stockage et de la génération de clés de chiffrement pour les données au repos, ainsi que pour les données Face ID et Touch ID. Il contient sa propre ROM d'amorçage.

Vous pouvez considérer l'Enclave sécurisée comme le centre de sécurité de votre appareil : elle dispose d'un moteur de chiffrement AES et d'un mécanisme pour stocker en toute sécurité vos clés de chiffrement, et elle est séparée du reste du système, de sorte que même si le processeur principal est compromis, elle devrait rester sûre.

#### Touch ID

La fonction Touch ID d'Apple vous permet de déverrouiller vos appareils en toute sécurité à l'aide de la biométrie.

Vos données biométriques ne quittent jamais votre appareil ; elles sont stockées uniquement dans l'Enclave sécurisée.

#### Déconnexion matérielle du microphone

Tous les ordinateurs portables équipés de l'Apple Silicon ou de la puce T2 disposent d'une déconnexion matérielle du microphone intégré lorsque le couvercle est fermé. Cela signifie qu'il n'y a aucun moyen pour un attaquant d'écouter le microphone de votre Mac, même si le système d'exploitation est compromis.

Notez que la caméra n'a pas de déconnexion matérielle, puisque sa vue est de toute façon obscurcie lorsque le couvercle est fermé.

#### Sécurité des processeurs périphériques

Les ordinateurs sont dotés de processeurs intégrés autres que le processeur principal, qui gèrent des fonctions telles que la mise en réseau, les graphiques, la gestion de l'alimentation, etc. Ces processeurs peuvent avoir une sécurité insuffisante et être compromis, c'est pourquoi Apple essaie de minimiser la nécessité de ces processeurs dans son matériel.

Lorsqu'il est nécessaire d'utiliser l'un de ces processeurs, Apple travaille avec le fournisseur pour s'assurer que le processeur

- exécute le micrologiciel vérifié du processeur principal au démarrage
- possède sa propre chaîne de démarrage sécurisé
- respecte des normes cryptographiques minimales
- garantit que les microprogrammes connus comme étant défectueux sont révoqués de manière appropriée
- a ses interfaces de débogage désactivées
- est signé avec les clés cryptographiques d'Apple

#### Protections contre l'accès direct à la mémoire

Apple Silicon sépare chaque composant qui nécessite un accès direct à la mémoire. Par exemple, un port Thunderbolt ne peut pas accéder à la mémoire réservée au noyau.

## Sources

- [Sécurité de la plate-forme Apple](https://support.apple.com/guide/security/welcome/web)
