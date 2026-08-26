---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Vérifiez la configuration requise pour Substance 3D Designer pour vous assurer que votre ordinateur répond aux spécifications requises.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuration requise
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Systèmes pris en charge

Vous trouverez ci-dessous une liste du matériel et des systèmes pris en charge par l’application :

## Windows

|  | Minimum | Recommandé | Optimale |
| --- | --- | --- | --- |
| <b>SE</b> | Windows 11 64 bits version 23H2 | Windows 11 64 bits version 24H1 | Windows 11 64 bits version 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 Go | 16 Go | 24 Go |
| <b>RAM</b> | 16 Go | 32 Go | 64 Go |
| <b>Stockage</b> | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

### macos

|  | Minimum | Recommandé | Optimale |
| --- | --- | --- | --- |
| <b>SE</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 Go | 32 Go | 64 Go |
| <b>Stockage</b> | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

### Linux

| Grands comptes | Vapeur |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## Recommandations générales

* Pour travailler dans des conditions confortables, nous vous recommandons un moniteur avec une résolution supérieure à 1 méga pixel et plus large que 1 280 pixels.
* De nombreuses applications de Substance dépendent d’OpenSSL 1.1.1 pour la compatibilité RHEL8/9. Pour les systèmes dotés de nouvelles versions d’OpenSSL, vous devez les fournir manuellement.
* *Seules* les versions <b>2019.x</b> et ultérieures ont été authentifiées par acte notarié afin de s&#39;exécuter sur <b>MacOS 10.15</b> (Catalina).
* La connexion <b>Bureau à distance</b> est possible si un contexte OpenGL 3.3 est disponible. Il fonctionnera sur <b>Nvidia Quadro</b> mais *pas* sur Nvidia GeForce, car il fournit uniquement un contexte OpenGL 1.4. Si cela pose problème, nous vous recommandons d&#39;utiliser d&#39;autres solutions telles que <b>VNC</b>/<b>Teamviewer</b>.
* Les utilisateurs de la version <b>Steam</b> doivent *désactiver* l&#39;<b>incrustation Steam</b> pour Designer, car cela peut entraîner des problèmes de performances lorsqu&#39;elle est active.

## GPU pris en charge

Vous trouverez ci-dessous une liste des GPU compatibles avec l’application :

* NVIDIA GeForce GTX 1060 et versions ultérieures
* NVIDIA Quadro P2200 et versions ultérieures
* AMD Radeon RX 580 et versions ultérieures
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR (Windows uniquement)**
> 
> Pour une meilleure stabilité globale lors de l&#39;exécution de calculs lourds sur le GPU (par exemple, le rendu de graphiques complexes, le rendu dans la vue 3D, l&#39;exportation d&#39;une scène à partir de la vue 3D, etc.), il est fortement recommandé de s&#39;assurer que les valeurs <b>Détection et récupération du délai d&#39;expiration (TDR)</b> correspondent aux recommandations figurant dans [cette page](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) de notre documentation.

## Configurations non prises en charge

<b>Windows</b>

* Les ordinateurs virtuels ne sont pas pris en charge.
* Windows Server n&#39;est pas pris en charge.

<b>macOS</b>

* Les systèmes macOS Intel ne sont pas pris en charge.
* Seules les configurations Apple officielles sont prises en charge.
* Les eGPU ne sont actuellement pas pris en charge et peuvent présenter des problèmes de stabilité.

<b>Linux</b>

* Les pilotes Mesa sous Linux ne sont pas pris en charge.

<b>Toute plateforme</b>

* Les GPU intégrés ne sont pas pris en charge sur les processeurs x86-64 (Intel, AMD).
* L’utilisation de Designer en association avec un logiciel tiers qui intercepte les appels Designer aux pilotes graphiques n’est pas prise en charge. Ces logiciels comprennent :
  * Injecteurs de post-traitement tels que les nuanciers qui appliquent un étalonnage des couleurs, des effets de caméra, ...
  * Incrustations à l’écran telles que les réticules personnalisés, les métriques de performance GPU, les habillages pour la diffusion vidéo...

## Versions minimales du pilote GPU

Vous trouverez ci-dessous une liste des versions minimales du pilote GPU requises pour que l’application s’exécute sans problème. Cette liste peut être modifiée à mesure que de nouvelles versions sont publiées.

Pour télécharger de nouveaux pilotes, voir : [Le GPU a des pilotes obsolètes](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SE | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Non pris en charge |

>[!NOTE]
>
> Sur **Mac OS**, le pilote GPU est fourni par le système d&#39;exploitation lui-même. Effectuez une mise à jour vers la dernière version de votre système d’exploitation pour accéder au pilote le plus récent.

## GPU raytracing à cuire

Pour activer GPU raytracing via Optix ou DXR, les pilotes recommandés ci-dessus doivent être installés.

<b>DXR</b> nécessite la configuration minimale suivante :

* <b>Windows 10</b> version 1809, consultez [cette page](https://experienceleague.adobe.com/fr/docs/substance-3d/bakers/features/gpu-raytracing) pour plus d&#39;informations
* <b>GPU avec architecture Pascal</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU raytracing s’exécute de manière optimale sur du matériel de lancer de rayons dédié tel que les GPU NVIDIA GeForce RTX ou NVIDIA Quadro RTX.

## Utilisation des comprimés

Les utilisateurs de tablettes sous <b>Windows</b> doivent appliquer les paramètres décrits dans la page suivante pour bénéficier de l&#39;expérience la plus fiable : [Configuration des stylos et des tablettes](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## Langues

L’interface du logiciel est disponible dans les langues suivantes :

* Deutsch (Deutschland)
* Anglais (États-Unis)
* Español (Espagne)
* Français (France)
* Italiano (Italia)
* Português (Brasil)
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)
