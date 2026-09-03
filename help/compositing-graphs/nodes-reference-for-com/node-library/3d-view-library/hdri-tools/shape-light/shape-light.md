---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilisez le nœud Shape Light pour ajouter des sources lumineuses de forme personnalisée aux environnements HDRI afin d’obtenir des effets d’éclairage créatifs.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Light
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# Shape Light

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/shape-light-01.png){width="200px"}

<b>Entrée :</b> vue 3D > Outils HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère une forme rectangulaire projetée sphériquement. La transformation de forme est pilotée par un gadget de transformation.

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
| <b>Matrice de forme</b> |  |
| <b>Matrice</b> <i>(Matrice de transformation)</i> | Contrôle de la transformation du résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Décalage</b> <i>-2.0 - 2.0</i> | Déplace ou traduit le résultat. Le résultat peut être modifié en interagissant directement avec la zone de travail. |
| <b>Forme</b> <i>Rectangle, Disque</i> | Choisissez la forme à placer. |
| <b>Mode colorimétrique de la forme</b> <i>RGB, Température (Kelvin), Entrée d&#39;image</i> | Choisissez la méthode à utiliser pour définir la couleur de la forme. Image Input permet d&#39;utiliser le deuxième emplacement d&#39;entrée. |
| <b>Couleur</b> <i>(valeur de couleur)</i> | Uniquement avec le mode colorimétrique de la forme défini sur RGB. Choisit la couleur de la forme. |
| <b>Température de forme</b> <i>800.0 - 20000.0</i> | Uniquement avec le mode Couleur de la forme réglé sur Température. Définit la valeur Kelvin pour la couleur de la forme. |
| <b>Gamma d&#39;entrée d&#39;image de forme</b> <i>sRVB, linéaire</i> | Uniquement avec le mode colorimétrique de la forme défini sur Entrée image. Déterminez comment interpréter l’entrée d’image de forme. |
| <b>Exposition de forme (EV)</b> <i>0.0 - 10.0</i> | Définissez la valeur d’exposition de la forme générée, idéalement adaptée à la valeur d’exposition de l’image d’arrière-plan. |
| <b>Dureté de forme</b> <i>0.0 - 1.0</i> | Définissez la dureté des contours de la forme. |
| <b>Exposition aux zones réactives (EV)</b> <i>0.0 - 10.0</i> | Définissez l’exposition de la zone réactive centrale. Notez que ce n’est pas très visible en mode RGB. |
| <b>Taille de la zone réactive</b> <i>0.0 - 1.0</i> | Taille de la zone réactive centrale. |
| <b>Suppression de la zone réactive</b> <i>0.0 - 1.0</i> | Atténuation de la zone réactive centrale. |
| <b>Position de la zone réactive</b> <i>0.0 - 1.0</i> | Position X et Y de la zone réactive centrale. |
| <b>Activer l&#39;entrée en arrière-plan</b> <i>Faux/Vrai</i> | Active/désactive l’utilisation d’une image d’arrière-plan facultative. Les composites ont généré de la lumière au-dessus de l’arrière-plan. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur)</i> | Si l’entrée Arrière-plan n’est pas utilisée, définissez ici une valeur d’arrière-plan de couleur unie. |
| <b>Gamma d&#39;arrière-plan</b> <i>sRVB, linéaire</i> | Si l’entrée Arrière-plan est utilisée, définissez comment interpréter l’entrée Arrière-plan. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-02.gif" />
        </td>
    </tr>
</table>
