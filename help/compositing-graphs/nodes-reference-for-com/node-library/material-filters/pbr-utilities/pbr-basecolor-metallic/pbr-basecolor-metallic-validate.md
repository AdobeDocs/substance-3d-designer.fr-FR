---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Utilisez le nœud Validation métallique de la couleur de base PBR pour valider et corriger les valeurs métalliques et de couleur de base des matériaux PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Validation métallique de couleur de base PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR BaseColor / Metallic Validate

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR BaseColor / Metallic Validate

**Entrée :** *Filtres de matériaux/Utilitaires PBR*

**Simple**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud d&#39;utilitaire qui génère une « carte thermique » de bonne à mauvaise dont les valeurs sont correctes ou incorrectes selon les normes PBR.

Il est très utile comme outil d&#39;apprentissage pour la PBR, car il fournit un retour visuel très clair sur les erreurs et où elles peuvent être trouvées.

N’utilisez pas cet outil comme outil final, mais assurez-vous de toujours comprendre clairement pourquoi vous enfreignez les règles mises en évidence par cet outil.

## Paramètres

* **Mode de validation** : *Albédo, Metal, Combiné* Définit s&#39;il faut cocher uniquement Albédo, Metal, ou les deux en tant que mode de présentation.
* **Seuil de la plage d&#39;obscurité de l&#39;Albédo** : *50 sRVB, 30 sRVB* définit la limite inférieure de l&#39;Albédo sur 50 ou 30 sRVB. Peut diminuer ou augmenter la tolérance pour les zones rouges.
* **Plage de réflectance du métal** : *Réfléchissant de 70 à 100 %, Réfléchissant de 60 à 100 %* modifie la plage métallique pour qu’elle soit considérée comme correcte. Peut diminuer ou augmenter la tolérance pour les zones rouges.
* **Superposer la carte** : le mode de débogage rapide *Faux/Vrai* pour superposer les cartes d&#39;entrée, permet un suivi plus rapide des zones problématiques.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
