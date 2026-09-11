---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière sphérique pour ajouter des sources de lumière sphériques aux environnements HDRI afin d’améliorer le contrôle de l’éclairage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lumière sphérique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# Lumière sphérique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sphere-light.resources/panorama-sphere-light.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une forme sphérique projetée. La transformation de sphère est pilotée par un gadget de transformation.

La Sphère lumineuse est très polyvalente et dispose d&#39;options qui lui permettent non seulement de générer de simples lumières rondes, mais aussi des planètes ou d&#39;autres corps célestes. Si vous n&#39;avez pas besoin des options d&#39;éclairage et de rotation plus avancées, consultez [Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) à la place.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée d&#39;image d&#39;arrière-plan</b> <i>Entrée couleur</i> | Arrière-plan facultatif sur lequel composer la lumière générée. |
| <b>Entrée d&#39;image de forme</b> <i>Entrée couleur</i> | Image facultative à mapper sur la lumière Sphère. Utilisé uniquement lorsque le mode colorimétrique de la forme est défini sur Entrée image. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de position</b> <i>Distance avec l&#39;origine, position mondiale</i> | Choisissez entre deux modes de placement. La distance avec l&#39;origine est similaire aux coordonnées polaires, la sphère est définie par rapport au centre du panorama, la position universelle fonctionne comme les coordonnées 3D standard. |
| <b>Coordonnées De Position</b> |  |
| <b>Up Vector</b> <i>Z vers le haut, Y vers le haut</i> | En mode Position universelle uniquement, déterminez l&#39;orientation du repère. |
| <b>Position mondiale Sphère</b> <i>-2.0 - 2.0</i> | Uniquement avec le mode Position universelle, définit la position de la sphère dans l’espace monde. |
| <b>Position</b> | Uniquement en mode Distance avec l&#39;origine. Définit la position par rapport au centre. Peut être manipulé en vue 2D. |
| <b>Distance avec l&#39;origine</b> <i>0.0 - 20.0</i> | Uniquement en mode Distance avec l&#39;origine. Définit la distance par rapport à l’origine et affecte la taille visible de la sphère. |
| <b>Mode colorimétrique de la forme</b> <i>RGB, Température (Kelvin), Entrée d&#39;image</i> | Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée. |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme. |
| <b>Température de forme</b> <i>800.0 - 20000.0</i> | Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme. |
| <b>Gamma d&#39;entrée d&#39;image sphère</b> <i>sRVB, linéaire</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme. |
| <b>Rotation de la sphère</b> <i>0.0 - 1.0</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Fait tourner la sphère autour de son centre pour orienter l’image mappée. |
| <b>Exposition (EV)</b> <i>0.0 - 10.0</i> | Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan. |
| <b>Rayon sphère</b> <i>0.0 - 1.0</i> | Définit le rayon/la taille de la sphère. |
| <b>Dureté Sphère</b> <i>0.0 - 1.0</i> | Définit la dureté/atténuation de la sphère. |
| <b>Ombrage</b> <i>Sans, Obscurcissement des membres, Lumière d&#39;Ombrage</i> | Définissez si un ombrage doit être appliqué à la sphère. Permet à la sphère de ne pas apparaître comme un objet solide non éclairé. L’obscurcissement des membres signifie qu’un léger obscurcissement apparaît sur les bords, l’éclairage Ombrage signifie que la sphère est éclairée par une lumière Ombrage facultative. |
| <b>Position mondiale Ombrage clair</b> <i>-1.0 - 1.0</i> | Si l’option Ombrage est définie sur Lumière d’Ombrage, la position de la lumière sur la sphère est ici contrôlée. |
| <b>Transparence Penombra</b> <i>0.0 - 1.0</i> | Si l’option Ombrage est définie sur Lumière d’Ombrage, contrôle le retrait de l’ombrage. |
| <b>Activer l&#39;entrée en arrière-plan</b> <i>Faux/Vrai</i> | Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie. |
| <b>Gamma d&#39;arrière-plan</b> <i>sRVB, linéaire</i> | Si l’entrée Arrière-plan est utilisée, définissez comment interpréter l’entrée Arrière-plan. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/spherelight-ex1.png" />
        </td>
    </tr>
</table>
