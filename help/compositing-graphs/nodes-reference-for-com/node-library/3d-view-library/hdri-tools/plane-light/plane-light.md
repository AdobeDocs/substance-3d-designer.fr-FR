---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Lumière plane pour ajouter des sources lumineuses planes aux environnements HDRI afin de contrôler l’éclairage directionnel.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclairage plan
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Éclairage plan

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plane-light.resources/panorama-plane-light.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une forme plane projetée sphériquement. Le plan peut être placé et orienté en 3D à l’aide des paramètres d’entrée.

Elle diffère de la [lumière de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) plus simple en ce sens qu&#39;elle offre des options de placement plus avancées en dehors de la projection de Distance avec l&#39;origine plus simple, et que davantage de motifs et de masques peuvent être appliqués, tout comme la [lumière de ligne](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée d&#39;image d&#39;arrière-plan</b> <i>Entrée couleur</i> | Arrière-plan facultatif sur lequel composer la lumière générée. |
| <b>Entrée d&#39;image de forme</b> <i>Entrée couleur</i> | Image facultative à plaquer sur l’éclairage linéaire. Utilisé uniquement lorsque le mode colorimétrique de la forme est défini sur Entrée image. |
| <b>Entrée d&#39;image de motif</b> <i>Entrée en niveaux de gris</i> | Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Mode de position</b> <i>Sol/Plafond, Distance avec l&#39;origine, Positions Mondiales</i> | Choisissez parmi trois modes de placement différents. Manipulation de la prise en charge du sol/plafond et de la Distance avec l&#39;origine dans la vue 2D, les positions universelles ne peuvent être modifiées que par le biais des propriétés, mais prennent en charge un placement plus exact. |
| <b>Afficher la Grille du Sol</b> <i>Faux/Vrai</i> | Fonction d&#39;aide permettant de dessiner une grille de mise à la terre de débogage. Permet d’estimer la position des lignes dans l’espace. |
| <b>Coordonnées De Position</b> |  |
| <b>Up Vector</b> <i>Z vers le haut, Y vers le haut</i> | En mode Position universelle uniquement, déterminez l&#39;orientation du repère. |
| <b>Position de l&#39;UV du plan</b> | Seulement avec sol / plafond et Distance avec l&#39;origine. Définit la position du plan dans l’espace UV. |
| <b>Position Planétaire En Plan</b> <i>-2.0 - 2.0</i> | Uniquement avec le mode Positions universelles. Définit la position du plan dans l’espace universel. Aucune interaction de vue 2D prise en charge. |
| <b>Height absolu du plan</b> <i>0.0 - 1.0</i> | Uniquement avec le mode Position sol/plafond, définit l&#39;height absolu à partir du plafond. Utilisez Afficher la grille au sol pour mieux estimer la position. |
| <b>Distance avec l&#39;origine</b> <i>0.0 - 1.0</i> | Uniquement avec le mode Position de la Distance avec l&#39;origine. Définit la distance entre les deux points du panorama. |
| <b>Mode colorimétrique de la forme</b> <i>RGB, Température (Kelvin), Entrée d&#39;image</i> | Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée. |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme. |
| <b>Température</b> <i>800.0 - 20000.0</i> | Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme. |
| <b>Mode D&#39;UV D&#39;Image De Forme</b> <i>Étirer, Étirer au milieu uniquement, Répéter + Espacement</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Définit la façon dont l’image est appliquée à la forme de trait et détermine le comportement de répétition UV. |
| <b>Espacement de répétition de l&#39;image de forme</b> <i>0.0 - 1.0</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image et avec le mode UV défini sur Répétition + Espacement. Définit l’espacement lorsque l’image se répète le long de la ligne. |
| <b>Gamma d&#39;image de forme</b> <i>sRVB, linéaire</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme. |
| <b>Exposition (EV)</b> <i>0.0 - 10.0</i> | Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan. |
| <b>Échelle de plan</b> <i>0.0 - 1.0</i> | Définissez une échelle uniforme pour la forme Plan. |
| <b>Taille du plan</b> <i>0.0 - 1.0</i> | Définissez une taille non uniforme de la forme Plan. |
| <b>Rotation du plan</b> <i>0.0 - 1.0</i> | Faire pivoter le plan le long de son axe central. |
| <b>Motif</b> <i>Carré Lisse, Carré Net, Cône, Hémisphère, Entrée D&#39;Image</i> | Sélectionnez la forme de motif à utiliser. |
| <b>Dureté de motif</b> <i>0.0 - 1.0</i> | Définissez la dureté/le contraste du motif. |
| <b>Mode d&#39;UV de motif</b> <i>Étirer, Étirer au milieu uniquement</i> | Définissez comment utiliser le masque de motif secondaire, appliqué au-dessus de l’image de forme. |
| <b>Activer l&#39;écrêtage du Sol</b> <i>Faux/Vrai</i> | Activez cette option si le plan peut être écrêté par un plan au sol ou s’il est toujours affiché en dessous. Utilisez l’option Afficher la grille au sol pour mieux l’estimer. |
| <b>Height du Sol</b> <i>-2.0 - 0.0</i> | Réglez l’height au sol pour l’écrêtage. |
| <b>Activer l&#39;entrée en arrière-plan</b> <i>Faux/Vrai</i> | Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie. |
| <b>Gamma d&#39;arrière-plan</b> <i>sRVB, linéaire</i> | Si l’entrée Arrière-plan est utilisée, définissez comment interpréter l’entrée Arrière-plan. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plane-light.resources/plane-light-ex.gif" />
        </td>
    </tr>
</table>
