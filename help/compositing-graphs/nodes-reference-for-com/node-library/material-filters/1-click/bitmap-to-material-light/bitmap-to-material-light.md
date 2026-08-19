---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Bitmap en matériau clair pour convertir rapidement des images bitmap en matériaux avec un éclairage optimisé pour des workflows rapides.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap en lumière de matériau
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Bitmap en lumière de matériau

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## Bitmap en lumière de matériau

**Entrée :** *Filtres Matériau/1-Clic*

**Intermédiaire**

</td>
<td style="border: 0;" valign="top">

## Description

Ce nœud convertit une seule entrée Diffuse/Basecolor en un matériau complet. En tant que version simple et « légère » de Bitmap2Material entièrement développé par [Allegorithmic, qui peut être acheté séparément](https://www.allegorithmic.com/products/bitmap2material), elle vous donne un aperçu de la version complète. Cela peut bien fonctionner dans les cas les plus simples.

Bien qu’elle ne garantisse pas l’obtention de matériaux parfaits et corrects pour le PBR, c’est un bon moyen rapide de commencer si vous n’avez qu’une seule image et que vous souhaitez un matériau complet.

## Paramètres

* **Canaux**
  * Active et désactive les couches de matériau dans ce groupe, par exemple lors de l’utilisation de cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Global**
  * **Balance des Profondeurs** : *-1.0 - 1.0* définit un biais/décalage pour la carte de hauteur.
* **Diffus**
  * **Renforcement** :*0.0 - 1.0* Ajoute de la netteté au résultat de diffusion.
  * **Teinte** : *0,0 - 1,0* les teintes se diffusent avec un décalage de teinte sélectionné par l’utilisateur.
  * **Saturation** : *0,0 - 1,0* modifie la saturation du résultat Diffuse.
  * **Luminosité** : *0.0 - 1.0* ajuste la luminosité du résultat diffus.
  * **Contraste** : *-1,0 - 1,0*\
    Règle le contraste du résultat.
* **Relief**\
  Le groupe Relief contrôle les sorties Normal et Height.
  * **Format normal de sortie** : *DirectX, OpenGL* bascule entre les formats normaux (bascule en vert).
  * **Inverser le Relief généré** :*Faux/Vrai* Inverse l&#39;interprétation de l&#39;height.
  * **Intensité normale** : *0.0 - 20.0* Définit l&#39;intensité du mappage normal généré.
  * **Égaliseur de Reliefs** : *0.0 - 1.0* définit les soldes de conversion pour différentes échelles de détails.
  * **Intensité du pincement** : *0,0 - 1,0* accentue la netteté des transitions normales. Ajoute un filtre de netteté avant de passer à la normale, ce qui rend les contours plus prononcés.
  * **Netteté normale** : *0.0 - 1.0* Netteté normale après la conversion, fait ressortir les détails.
  * **Adoucissement normal** : *0.0 - 1.0* adoucit le mappage normal après la conversion, masque les détails.
* **Specular**
  * **Influence diffuse du Specular** : *0,0 - 1,0* définit l&#39;influence de la diffusion sur le Specular. Affecte également les sorties Lustre et Rugosité.
  * **Saturation du Specular** : *0,0 - 1,0* modifie la saturation de la sortie Specular.
  * **Netteté au Specular** :*0.0 - 1.0* Netteté de la sortie Specular.
  * **Speculars level entrants** : *0.0 - 1.0* définit les niveaux d’entrée pour l’interprétation du Specular.
  * **Speculars level sortants** : *0,0 - 1,0* modifie les niveaux de sortie du Specular.
  * **Influence du Specular métallique** : *0.0 - 1.0* Détermine l&#39;influence de l&#39;entrée métallique facultative sur la carte du Specular.
* **Lustre**
  * **Niveaux de brillance dans** : *0.0 - 1.0* définit les niveaux d’entrée pour l’interprétation du brillant.
  * **Niveaux de brillance sortants** : *0.0 - 1.0* Modifie les niveaux de sortie de brillance.
  * **Influence du brillant métallique** : *0.0 - 1.0* Détermine l’influence de l’entrée métallique facultative sur la carte de brillance.
* **Rugosité**
  * **Niveaux de rugosité en** : *0.0 - 1.0* définit les niveaux d’entrée pour l’interprétation de la rugosité.
  * **Niveaux de rugosité sortants** : *0.0 - 1.0* Modifie les niveaux de sortie de la rugosité.
  * **Influence de la rugosité métallique** : *0.0 - 1.0* Détermine l’influence de l’entrée métallique facultative sur la carte de brillance.
* **Occlusion ambiante**
  * **Occlusion ambiante en diffusion** : *0.0 - 1.0* fusionne l&#39;AO généré en sortie diffuse.
  * **Répartition de l&#39;Occlusion ambiante** : *0.0 - 1.0* Définit la distance de propagation de l&#39;IA générée.
  * **Distance de la lumière de l&#39;Occlusion ambiante** : *0.0 - 1.0* définit l&#39;interprétation de la « profondeur » AO. A moins d’influence lorsqu’il existe une Planche importante.
  * **Angle de la lumière d&#39;Occlusion ambiante** : *0.0 - 1.0* définit un angle de dominante AO de faux éclairage. Peut être utilisé pour compenser tout AO directionnel déjà présent dans la diffusion, s’il est défini sur un angle opposé.
  * **Niveaux d&#39;Occlusion ambiante** : *0,0 - 1,0* modifie les niveaux de sortie AO.

## Exemples d’images

|  |
| --- |
| Aucune image n&#39;est jointe à cette page. |

</td>
</tr>
</table>
