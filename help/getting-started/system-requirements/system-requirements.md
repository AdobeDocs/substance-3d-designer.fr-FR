---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ""
description: Vérifiez la configuration requise pour Substance 3D Designer pour vous assurer que votre ordinateur répond aux spécifications requises.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configuration requise
user-guide-description: ""
user-guide-title: ""
source-git-commit: aeb517a0def4b5bc2de723633f8932dfc03f052c
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%
---

# Configuration requise

Vous trouverez ci-dessous une liste du matériel et des systèmes pris en charge par l’application :

## Configuration du système par plate-forme

### Windows

|             | Minimum | Recommandé | Optimale |
|:------------|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| **SE** | Windows 11 64 bits version 23H2 | Windows 11 64 bits version 24H1 | Windows 11 64 bits version 24H2 |
| **CPU** | Intel Core i5<br>AMD Ryzen 5 | Intel Core i7<br>AMD Ryzen 7 | Intel Core i9<br>AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super<br>NVIDIA Quadro RTX 4000<br>AMD Radeon RX 5700 XT<br>AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080<br>NVIDIA Quadro RTX A4000<br>AMD Radeon RX 6800 XT<br>AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090<br>NVIDIA Quadro RTX 5000 Ada Generation<br>AMD Radeon RX 7900 XTX<br>AMD Radeon Pro W7800 |
| **VRAM** | 8 Go | 16 Go | 24 Go |
| **RAM** | 16 Go | 32 Go | 64 Go |
| **Stockage** | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

### macOS

|             | Minimum | Recommandé | Optimale |
|:------------|:----------------------------------|:----------------------------------|:----------------------------------|
| **SE** | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 Go | 32 Go | 64 Go |
| **Stockage** | Disque SSD avec 30 Go d’espace disponible | Disque SSD avec 50 Go d’espace disponible | Disque SSD avec 70 Go d’espace disponible |

### Linux

| Grands comptes | Vapeur |
|:------------------|:-------------|
| RHEL 8</br>RHEL 9 | Ubuntu 22.04 |

## Recommandations générales

* Pour travailler dans des conditions confortables, nous vous recommandons un moniteur avec une résolution supérieure à 1 méga pixel et plus large que 1 280 pixels.
* De nombreuses applications de Substance dépendent d’OpenSSL 1.1.1 pour la compatibilité RHEL8/9. Pour les systèmes dotés de nouvelles versions d’OpenSSL, vous devez les fournir manuellement.
* *Seules* les versions **2019.x** et ultérieures ont été authentifiées par acte notarié afin de s&#39;exécuter sur **macOS 10.15 Catalina**.
* La connexion **Bureau à distance** est possible si un contexte OpenGL 3.3 est disponible. Il fonctionnera sur **Nvidia Quadro** mais *pas* sur Nvidia GeForce, car il fournit uniquement un contexte OpenGL 1.4. Si cela pose problème, nous vous recommandons d&#39;utiliser d&#39;autres solutions telles que **VNC/Teamviewer**.
* Les utilisateurs de la version **Steam** doivent *désactiver* l&#39;**incrustation Steam** pour Designer, car cela peut entraîner des problèmes de performances lorsqu&#39;elle est active.

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
> Pour une meilleure stabilité globale lors de l&#39;exécution de calculs lourds sur le GPU (par exemple, le rendu de graphes complexes, le rendu dans la vue 3D, l&#39;exportation d&#39;une scène à partir de la vue 3D, etc.), il est fortement recommandé de s&#39;assurer que les valeurs **Détection et récupération du délai d&#39;expiration (TDR)** correspondent aux recommandations figurant dans [cette page](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) de notre documentation.

## Configurations non prises en charge

**Windows**

* Les ordinateurs virtuels ne sont pas pris en charge.
* Windows Server n&#39;est pas pris en charge.

**macOS**

* Les systèmes macOS Intel ne sont pas pris en charge.
* Seules les configurations Apple officielles sont prises en charge.
* Les eGPU ne sont actuellement pas pris en charge et peuvent présenter des problèmes de stabilité.

**Linux**

* Les pilotes Mesa sous Linux ne sont pas pris en charge.

**Toute plateforme**

* Les GPU intégrés ne sont pas pris en charge sur les processeurs x86-64 (Intel, AMD).
* L’utilisation de Designer en association avec un logiciel tiers qui intercepte les appels Designer aux pilotes graphiques n’est pas prise en charge. Ces logiciels comprennent :
  * Injecteurs de post-traitement tels que les ré-ombrages qui appliquent un étalonnage des couleurs, des effets de caméra, ...
  * Incrustations à l’écran telles que les réticules personnalisés, les métriques de performance GPU, les habillages pour la diffusion vidéo...

## Versions minimales du pilote GPU

Vous trouverez ci-dessous une liste des versions minimales du pilote GPU requises pour que l’application s’exécute sans problème. Cette liste peut être modifiée à mesure que de nouvelles versions sont publiées.

Pour télécharger de nouveaux pilotes, voir : [Le GPU a des pilotes obsolètes](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SE | NVIDIA | AMD | Intel |
|:------------|:-----------------------------|:-----------------------------------------|:------------|
| **Windows** | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| **Linux** | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Non pris en charge |

>[!NOTE]
>
> Sur **macOS**, le pilote GPU est fourni par le système d&#39;exploitation lui-même. Effectuez une mise à jour vers la dernière version de votre système d’exploitation pour accéder au pilote le plus récent.

## GPU raytracing de baking

Pour activer GPU raytracing via Optix ou DXR, les pilotes recommandés ci-dessus doivent être installés.

**DXR** nécessite la configuration minimale suivante :

* **Windows 10** version 1809, consultez [cette page](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) pour plus d&#39;informations
* **GPU avec architecture Pascal** (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU raytracing s’exécute de manière optimale sur le matériel de raytracing dédié tel que les GPU NVIDIA GeForce RTX ou NVIDIA Quadro RTX.

## Utilisation des comprimés

Les utilisateurs de tablettes sous **Windows** doivent appliquer les paramètres décrits dans la page suivante pour bénéficier d&#39;une expérience optimale : [Configuration des stylets et des tablettes](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

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
