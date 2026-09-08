---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Utilisez le nœud Concepteur de masque pour combiner plusieurs entrées de masque et créer des motifs de masque complexes pour des effets de matériau.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Générateur de masques
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 10%

---


# Générateur de masques

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Générateurs de masque

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère un masque noir et blanc en fonction des maps bakées et des paramètres utilisateur. Il s’agit de la version Designer de Painter Mask Builder.

Il s&#39;agit d&#39;un outil complexe conçu comme un constructeur de masques global, basé sur des maps bakées, des paramètres utilisateur et des modèles et cartes d&#39;usure/salissures. Il est principalement conçu comme un nœud très avancé et à contrôle total pour se fondre dans le dirt de pli et l&#39;usure des bords. Ce nœud est assez puissant pour imiter tous les autres Générateurs de masque.

Aucun bake n&#39;est explicitement requis, mais plus vous fournissez de ressources, plus ce nœud est capable d&#39;effectuer de tâches.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Courbure</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Espace universel normal</b> <i>Entrée couleur</i> |  |
| <b>Entrée Usure/salissures</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Entrée Usure/salissures 2</b> <i>Entrée en niveaux de gris</i> |  |
| <b>Entrée Dispersion</b> <i>Entrée en niveaux de gris</i> | Tampon de dispersion personnalisé, requis pour utiliser les paramètres de Dispersion. |
| <b>Masquer (facultatif)</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Position</b> <i>Entrée couleur</i> | Ce paramètre est utilisé pour les effets triplanaires et de haut en bas. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Niveau</b> <i>0.0 - 1.0</i> | Définit le niveau total de l’effet, qui s’affiche progressivement. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du résultat. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse le résultat. Utile pour obtenir l’opposé du masque que vous créez. |
| <b>Utiliser le mode triplanaire</b> <i>Faux/Vrai</i> | Permet la Projection triplanaire, en évitant tout seam avec des mappages usure/salissures. |
| <b>Contraste de fusion triplanaire</b> <i>0.0 - 1.0</i> | Définit le contraste de la fusion triplanaire. |
| <b>Usure/salissures</b> <i>0.0 - 1.0</i> | Définit la quantité d’Usure/salissures à intégrer globalement. |
| <b>Usure/salissures</b> |  |
| <b>Échelle</b> <i>0 - 10</i> | Définit l’échelle de l’Usure/salissures globale. |
| <b>Utiliser l&#39;Usure/salissures personnalisée</b> <i>Faux/Vrai</i> | Active l&#39;entrée Usure/salissures personnalisée. |
| <b>Usure/salissures personnalisée secondaire</b> <i>0.0 - 1.0</i> | Active une deuxième entrée Usure/salissures personnalisée. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse la courbe d’Usure/salissures. |
| <b>AO</b> <i>-1.0 - 1.0</i> | Définit la mesure dans laquelle l’effet doit apparaître dans les zones de zone de zoom occultées. Peut être modifié avec le groupe ci-dessous. |
| <b>AO</b> |  |
| <b>Plage</b> <i>0.0 - 1.0</i> | Définit le seuil ou la plage d’apparence du dirt. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste de l’effet AOP. |
| <b>Bruit</b> <i>0.0 - 1.0</i> | Définit la quantité de bruit/usure/salissures à fusionner avec l’effet AO. |
| <b>Échelle de Bruit</b> <i>0 - 10</i> | Définit l’échelle du bruit/de l’usure/salissures AO. |
| <b>Type de Bruit</b> <i>Taches, Nuages, Humidité, Bruit Blanc</i> | Permet de basculer entre 4 types de bruits AO différents. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse l’interprétation de la carte AO : le bruit apparaîtra dans les zones AO claires, et non dans les zones AO sombres. |
| <b>Courbure</b> <i>0.0 - 1.0</i> | Définit la quantité d’effet qui doit apparaître sur les contours de la Courbure. Il peut s’agir de formes convexes et concaves. Modifiez ceci avec le groupe ci-dessous. |
| <b>Courbure</b> |  |
| <b>Plage convexe</b> <i>-1.0 - 1.0</i> | Définit la quantité d’effet à appliquer aux contours de courbure convexes (clairs). |
| <b>Contraste convexe</b> <i>0.0 - 1.0</i> | Définit le contraste de l’effet Convexe. |
| <b>Inversion convexe</b> <i>Faux/Vrai</i> | Inverse l’interprétation des contours convexes. |
| <b>Plage concave</b> <i>-1.0 - 1.0</i> | Définit la quantité d’effet à appliquer sur les bords de courbure concaves (sombres). |
| <b>Contraste concave</b> <i>0.0 - 1.0</i> | Définit le contraste de la plage concave. |
| <b>Conserver l&#39;inversion</b> <i>Faux/Vrai</i> | Inverse l&#39;interprétation des arêtes concaves. |
| <b>Smoothness</b> <i>0.0 - 16.0</i> | Niveau de flou et de lissage à appliquer aux contours de la Courbure. |
| <b>Amplification de niveau</b> <i>0.0 - 1.0</i> | Amplificateur supplémentaire si l&#39;effet n&#39;est pas assez visible. |
| <b>Bruit</b> <i>0.0 - 1.0</i> | Définit l’influence du bruit/de l’usure/salissures sur l’effet Courbure. |
| <b>Échelle de Bruit</b> <i>0 - 10</i> | Définit l’échelle du bruit. |
| <b>Type de Bruit</b> <i>Taches, Nuages, Humidité, Bruit Blanc</i> | Choisissez entre 4 types de Bruits différents. |
| <b>Dégradé Haut/Bas</b> <i>-1.0 - 1.0</i> | Fusion ou masque avec un dégradé de haut en bas en fonction du mappage de position. Les valeurs positives éclaircissent les choses, tandis que les valeurs négatives masquent les effets existants. |
| <b>Dégradé</b> |  |
| <b>Plage</b> <i>0.0 - 1.0</i> | Définit la position du dégradé. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Règle le contraste du dégradé. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse le dégradé. Permute efficacement le bas et le haut. |
| <b>Normale de l&#39;espace monde</b> <i>0.0 - 1.0</i> | Similaire au dégradé Haut/Bas, mais avec la carte de position et dans six directions, semblable à un faux éclairage. Les valeurs positives s’éclaircissent, les valeurs négatives s’assombrissent. |
| <b>Normale de l&#39;espace monde</b> |  |
| <b>Intensité supérieure</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensité inférieure</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensité avant</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensité du dos</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensité correcte</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensité gauche</b> <i>-1.0 - 1.0</i> |  |
| <b>Scratches</b> <i>-1.0 - 1.0</i> | Les fusions rayent sur les zones blanches. |
| <b>Scratches</b> |  |
| <b>Quantité</b> <i>0 - 4096</i> | Définit la quantité totale de rayures. |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Définit l’échelle des rayures individuelles. |
| <b>Dispersion</b> <i>-1.0 - 1.0</i> | Dispersion un tampon personnalisé dans des zones blanches. |
| <b>Dispersion</b> |  |
| <b>Échelle</b> <i>0 - 50</i> | Échelle totale de l’effet. |
| <b>Densité</b> <i>0.0 - 1.0</i> | Contrôle de la densité de diffusion, nombre qui doit apparaître. |
| <b>Taille</b> <i>0.0 - 4.0</i> | Taille du tampon dispersé. |
| <b>Variation de taille</b> <i>0.0 - 1.0</i> | Variation dans la taille du tampon. |
| <b>Variation d&#39;opacité</b> <i>0.0 - 1.0</i> | Variation de l’opacité du tampon. |
