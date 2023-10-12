---
title: Introduction à macOS
icon: material/apple-finder
description: macOS est le système d'exploitation d'Apple pour ordinateurs de bureau fonctionnant avec leur propre matériel pour assurer une sécurité renforcée.
---

**macOS** est un système d'exploitation Unix développé par Apple pour leurs ordinateurs Mac. Pour améliorer la confidentialité de macOS, il est possible de désactiver la télémétrie et renforcer les paramètres existants de confidentialité et de sécurité.

Les anciens Mac à base de processeur Intel et les Hackintosh ne prennent pas en charge toutes les fonctions de sécurité offertes par macOS. Pour améliorer la sécurité des données, nous recommandons d'utiliser un Mac plus récent avec un processeur [Apple silicium](https://support.apple.com/fr-fr/HT211814).

## Remarques concernant la vie privée

macOS pose quelques problèmes importants en matière de protection de la vie privée, qu'il convient de prendre en compte. Ils concernent le système d'exploitation lui-même, et non les autres applications et services d'Apple.

### Verrouillage d'activation

Les nouveaux appareils Apple silicium peuvent être configurés sans connexion internet. Cependant, la récupération ou la réinitialisation de votre Mac **nécessitera** une connexion internet aux serveurs d'Apple pour vérifier la base de données Verrouillage d'activation des appareils perdus ou volés.

### Contrôles de révocation des applications

macOS effectue des contrôles en ligne lorsque vous ouvrez une application afin de vérifier si elle contient des logiciels malveillants connus et si le certificat de signature du développeur a été révoqué.

Auparavant, ces vérifications étaient effectuées via un protocole OCSP non chiffré, ce qui pouvait entraîner une fuite d'informations sur les applications que vous exécutez sur votre réseau. Apple a mis à jour son service OCSP pour utiliser le chiffrement HTTPS en 2021, et [a publié des informations](https://support.apple.com/HT202491) sur sa politique de journalisation pour ce service. Ils ont également promis d'ajouter un mécanisme permettant aux personnes de se retirer de cette vérification en ligne, mais cela n'a pas été ajouté à macOS en date de juillet 2023.

Bien que vous [puissiez](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private/) désactiver manuellement cette vérification assez facilement, nous vous déconseillons de le faire à moins que les vérifications de révocation effectuées par macOS ne vous compromettent gravement, car elles jouent un rôle important en empêchant l'exécution d'applications compromises.

## Configuration recommandée

Lorsque vous configurez votre Mac pour la première fois, vous disposez d'un compte d'administrateur, dont les privilèges sont plus élevés que ceux d'un compte d'utilisateur standard. macOS dispose d'un certain nombre de protections qui empêchent les logiciels malveillants et d'autres programmes d'abuser de vos privilèges d'administrateur, de sorte que l'utilisation de ce compte est généralement sûre.

Cependant, des exploits dans des utilitaires de protection tels que `sudo` ont été [découverts dans le passé](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/). Si vous souhaitez éviter que les programmes que vous exécutez n'abusent de vos privilèges d'administrateur, vous pouvez envisager de créer un deuxième compte d'utilisateur standard, que vous utiliserez pour les opérations quotidiennes. Cela présente l'avantage supplémentaire de rendre plus évident le fait qu'une application a besoin d'un accès administrateur, parce qu'elle vous demandera à chaque fois de fournir des informations d'identification.

Si vous utilisez un deuxième compte, il n'est pas strictement nécessaire de vous connecter à votre compte administrateur d'origine à partir de l'écran de connexion de macOS. Lorsque vous effectuez, en tant qu'utilisateur standard, une opération nécessitant des autorisations d'administrateur, le système vous invite à vous authentifier, ce qui vous permet d'entrer une seule fois vos informations d'identification d'administrateur en tant qu'utilisateur standard. Apple fournit des [conseils](https://support.apple.com/HT203998) sur la façon de masquer votre compte administrateur si vous préférez ne voir qu'un seul compte sur votre écran de connexion.

Vous pouvez également utiliser un utilitaire tel que [macOS Enterprise Privileges](https://github.com/SAP/macOS-enterprise-privileges) pour obtenir les droits d'administrateur à la demande, mais cette solution peut être vulnérable à un exploit non découvert, comme toutes les protections basées sur des logiciels.

### iCloud

La majorité des préoccupations relatives à la protection de la vie privée et à la sécurité des produits Apple sont liées à leurs *services cloud*, et non à leurs matériels ou à leurs logiciels. Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés *auxquelles Apple a accès* par défaut. Ce niveau d'accès a parfois été utilisé de manière abusive par les forces de l'ordre pour contourner le fait que vos données sont par ailleurs chiffrées de manière sécurisée sur votre appareil, et bien sûr Apple est vulnérable aux fuites de données comme toute autre entreprise.

Par conséquent, si vous utilisez iCloud, vous devriez [activer la**Protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

### Paramètres systèmes

Il y a un certain nombre de paramètres intégrés que vous devriez confirmer ou modifier pour renforcer votre système. Ouvrez l'application **Paramètres** :

#### Bluetooth

- [ ] Décochez **Bluetooth** (sauf si vous l'utilisez)

#### Réseau

Selon que vous utilisez **Wi-Fi** ou **Ethernet** (indiqué par un point vert et le mot "connecté"), cliquez sur l'icône correspondante.

Cliquez sur le bouton "Détails" à côté du nom de votre réseau :

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

Sur les appareils modernes dotés d'une Secure Enclave (puce de sécurité T2 d'Apple, Apple silicium), vos données sont toujours chiffrées, mais elles sont déchiffrées automatiquement par une clé matérielle si votre appareil ne détecte pas qu'il a été altéré. L'activation de FileVault requiert en outre votre mot de passe pour déchiffrer vos données, ce qui améliore considérablement la sécurité, en particulier lorsque l'ordinateur est éteint ou avant la première connexion après la mise sous tension.

Sur les anciens ordinateurs Mac à processeur Intel, FileVault est la seule forme de chiffrement de disque disponible par défaut et doit toujours être activé.

- [x] Cliquez sur **Activer**

##### Mode Isolement

Le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) désactive certaines fonctionnalités afin d'améliorer la sécurité. Certaines applications ou fonctionnalités ne fonctionneront pas de la même manière que lorsqu'il est désactivé. Par exemple, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) et [WASM](https://developer.mozilla.org/fr/docs/WebAssembly) sont désactivés dans Safari lorsque le mode Isolement est activé. Nous vous recommandons d'activer le mode Isolement et de voir s'il a un impact significatif sur votre utilisation, car la plupart des changements qu'il apporte sont faciles à vivre.

- [x] Cliquez sur **Activer**

### Adresse MAC aléatoire

macOS utilise une adresse MAC aléatoire lorsqu'il effectue des analyses Wi-Fi alors qu'il est déconnecté d'un réseau. Toutefois, lorsque vous vous connectez à un réseau Wi-Fi préféré, l'adresse MAC utilisée n'est jamais aléatoire. La randomisation complète des adresses MAC est un sujet avancé, et la plupart des gens n'ont pas besoin de se préoccuper des étapes suivantes.

Contrairement à iOS, macOS ne propose pas d'option de randomisation de l'adresse MAC dans les paramètres, de sorte que si vous souhaitez modifier cet identifiant, vous devrez le faire à l'aide d'une commande ou d'un script. Pour définir une adresse MAC aléatoire, déconnectez-vous d'abord du réseau si vous êtes déjà connecté, puis ouvrez **Terminal** et entrez cette commande pour randomiser votre adresse MAC :

``` zsh
openssl rand -hex 6 | sed 's/^\(.\{1\}\)./\12/; s/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en0 ether
```

`en0` est le nom de l'interface dont vous modifiez l'adresse MAC. Il se peut que ce ne soit pas la bonne sur tous les Mac, donc pour vérifier, vous pouvez maintenir la touche option et cliquer sur le symbole Wi-Fi en haut à droite de votre écran. Le "nom de l'interface" doit être affiché en haut du menu déroulant.

Cette commande définit votre adresse MAC comme une adresse aléatoire "administrée localement", ce qui correspond au comportement des fonctions de randomisation des adresses MAC d'iOS, de Windows et d'Android. Cela signifie que chaque caractère de l'adresse MAC est entièrement aléatoire, à l'exception du deuxième caractère, qui indique que l'adresse MAC est *administrée localement*, et qu'elle n'est en conflit avec aucun matériel réel. Cette méthode est la plus compatible avec les réseaux modernes. Une autre méthode consiste à attribuer aux six premiers caractères de l'adresse MAC l'un des *identificateurs organisationnels uniques* d'Apple, que nous laisserons à l'appréciation du lecteur. Cette méthode est plus susceptible d'entrer en conflit avec certains réseaux, mais peut être moins visible. Étant donné la prévalence des adresses MAC randomisées et administrées localement dans d'autres systèmes d'exploitation modernes, nous ne pensons pas qu'une méthode présente des avantages significatifs en matière de protection de la vie privée par rapport à l'autre.

Lorsque vous vous connecterez à nouveau au réseau, vous le ferez avec une adresse MAC aléatoire. Cela sera réinitialisé lors du redémarrage.

Votre adresse MAC n'est pas la seule information unique concernant votre appareil qui est diffusée sur le réseau, votre nom d'hôte est un autre élément d'information qui pourrait vous identifier de manière unique. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** > **General** > **Sharing**. Some [privacy scripts](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) allow you to easily generate hostnames with random names.

## Protections de sécurité

macOS utilise la défense en profondeur en s'appuyant sur plusieurs couches de protections logicielles et matérielles, avec des propriétés différentes. Cela garantit qu'une défaillance dans une couche ne compromet pas la sécurité globale du système.

### Sécurité du logiciel

!!! warning "Avertissement"

    macOS vous permet d'installer des mises à jour bêta. Elles sont instables et peuvent être accompagnées de données télémétriques supplémentaires puisqu'elles sont utilisées à des fins de test. Pour cette raison, nous vous recommandons d'éviter les logiciels bêta en général.

#### Volume du système signé

Les composants système de macOS sont protégés dans un volume système signé en lecture seule, ce qui signifie que ni vous ni les logiciels malveillants ne peuvent modifier les fichiers système importants.

Le volume du système est vérifié en cours d'exécution et toute donnée qui n'est pas signée par une signature cryptographique valide d'Apple sera rejetée.

#### Protection de l'intégrité du système

macOS définit certaines restrictions de sécurité qui ne peuvent pas être contournées. Il s'agit des contrôles d'accès obligatoires, qui constituent la base du sandbox, du contrôle parental et de la protection de l'intégrité du système dans macOS.

La protection de l'intégrité du système met en lecture seule les emplacements de fichiers critiques afin de les protéger contre toute modification par des codes malveillants. Cela s'ajoute à la protection de l'intégrité du noyau basée sur le matériel, qui empêche le noyau d'être modifié en mémoire.

#### Sécurité des applications

##### Sandbox des applications

Les applications macOS téléchargées à partir de l'App Store doivent être mises en sandbox à l'aide de [App Sandbox](https://developer.apple.com/documentation/security/app_sandbox).

!!! warning "Avertissement"

    Les logiciels téléchargés en dehors de l'App Store officiel n'ont pas besoin d'être placés en sandbox. Vous devriez éviter autant que possible les logiciels qui ne font pas partie de l'App Store.

##### Antivirus

macOS est doté de deux formes de défense contre les logiciels malveillants :

1. La protection contre le lancement de logiciels malveillants est assurée par le processus d'examen des applications de l'App Store, ou *Notarization* (fait partie de *Gatekeeper*), un processus au cours duquel les applications tierces sont analysées par Apple à la recherche de logiciels malveillants connus avant d'être autorisées à s'exécuter.
2. La protection contre les autres logiciels malveillants et la remédiation des logiciels malveillants existants sur votre système sont assurées par *XProtect*, un logiciel antivirus plus traditionnel intégré à macOS.

Nous vous déconseillons d'installer des logiciels antivirus tiers, car ils n'ont généralement pas l'accès au niveau du système nécessaire pour fonctionner correctement, en raison des limitations imposées par Apple aux applications tierces, et parce que l'octroi des niveaux d'accès élevés qu'ils demandent pose souvent un risque encore plus grand pour la sécurité et la vie privée de votre ordinateur.

##### Sauvegardes

macOS est livré avec un logiciel de sauvegarde automatique appelé [Time Machine](https://support.apple.com/HT201250), qui vous permet de créer des sauvegardes chiffrées sur un disque externe ou réseau en cas de fichiers corrompus/supprimés.

### Sécurité matérielle

De nombreuses fonctions de sécurité modernes de macOS - telles que le démarrage sécurisé moderne, l'atténuation des exploits au niveau matériel, les vérifications de l'intégrité du système d'exploitation et le chiffrement des fichiers - reposent sur le silicium d'Apple, et le matériel le plus récent d'Apple est toujours doté de la [meilleure sécurité](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Nous n'encourageons que l'utilisation du silicium d'Apple, et non des anciens ordinateurs Mac à base d'Intel ou des Hackintosh.

Certaines de ces fonctions de sécurité modernes sont disponibles sur les anciens ordinateurs Mac à base d'Intel équipés de la puce de sécurité T2 d'Apple, mais cette puce est susceptible d'être exploitée par *checkm8*, ce qui pourrait compromettre sa sécurité.

Si vous utilisez des accessoires Bluetooth tels qu'un clavier, nous vous recommandons d'utiliser les accessoires officiels d'Apple car leur micrologiciel sera automatiquement mis à jour pour vous par macOS. L'utilisation d'accessoires tiers est possible, mais il faut penser à installer régulièrement les mises à jour du micrologiciel de ces accessoires.

Les SoC d'Apple s'attachent à minimiser la surface d'attaque en reléguant les fonctions de sécurité à un matériel dédié aux fonctionnalités limitées.

#### ROM d'amorçage

macOS empêche la persistance des logiciels malveillants en n'autorisant que les logiciels officiels d'Apple à s'exécuter au moment du démarrage ; c'est ce qu'on appelle le démarrage sécurisé. Les ordinateurs Mac le vérifient grâce à une partie de la mémoire en lecture seule du circuit intégré, appelée ROM d'amorçage, qui est mise en place lors de la fabrication de la puce.

La ROM d'amorçage constitue la racine de confiance du matériel. Cela garantit que les logiciels malveillants ne peuvent pas altérer le processus de démarrage. Lorsque votre Mac démarre, la ROM d'amorçage est la première chose qui s'exécute, formant le premier maillon de la chaîne de confiance.

Les ordinateurs Mac peuvent être configurés pour démarrer selon trois modes de sécurité : *Sécurité complète*, *Sécurité réduite*, et *Sécurité permissive*, le paramètre par défaut étant Sécurité complète. L'idéal est d'utiliser le mode de sécurité complète et d'éviter des choses comme les **extensions de noyau** qui vous obligent à réduire votre mode de sécurité. Veillez à [vérifier](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que vous utilisez le mode Sécurité complète.

#### Enclave sécurisée

L'Enclave sécurisée est une puce de sécurité intégrée dans les appareils dotés du silicium d'Apple, qui est chargée de stocker et de générer des clés de chiffrement pour les données au repos ainsi que pour les données Face ID et Touch ID. Il contient sa propre ROM d'amorçage.

Vous pouvez considérer l'Enclave sécurisée comme le centre de sécurité de votre appareil : elle dispose d'un moteur de chiffrement AES et d'un mécanisme pour stocker en toute sécurité vos clés de chiffrement, et elle est séparée du reste du système, de sorte que même si le processeur principal est compromis, elle devrait rester sûre.

#### Touch ID

La fonction Touch ID d'Apple vous permet de déverrouiller vos appareils en toute sécurité à l'aide de la biométrie.

Vos données biométriques ne quittent jamais votre appareil ; elles sont stockées uniquement dans l'Enclave sécurisée.

#### Déconnexion matérielle du microphone

Tous les ordinateurs portables équipés de silicium Apple ou de la puce T2 disposent d'une déconnexion matérielle du microphone intégrée lorsque le couvercle est fermé. Cela signifie qu'il n'y a aucun moyen pour un attaquant d'écouter le microphone de votre Mac, même si le système d'exploitation est compromis.

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

Le silicium d'Apple sépare chaque composant qui nécessite un accès direct à la mémoire. Par exemple, un port Thunderbolt ne peut pas accéder à la mémoire réservée au noyau.

## Sources

- [Sécurité de la plate-forme Apple](https://support.apple.com/guide/security/welcome/web)
