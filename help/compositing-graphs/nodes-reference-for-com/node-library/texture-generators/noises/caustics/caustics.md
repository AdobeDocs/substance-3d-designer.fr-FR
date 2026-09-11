---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilisez le nœud Caustique pour générer des motifs de lumière caustique afin de créer des effets d'éclairage sous-marin et réfractif.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Caustique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# Caustique

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/rt-caustics-grayscale.png){width="128px"}

<b>Entrées :</b> Générateurs de Textures > Bruits

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère des réverbérations projetées en fonction d’une map height et d’une direction de la lumière.Disponible en niveaux de gris et en couleurs, les différences sont subtiles, mais la version couleur ajoute des effets de dispersion des couleurs. La lumière est convertie à partir d’un seul point, aucune Map d&#39;environnement n’est utilisée.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Espace colorimétrique de sortie</b> <i>Raw, sRGB</i> | Définissez l’espace colorimétrique de sortie. |
| <b>Taille de la Grille de photons</b> <i>Auto, 512, 1024, 2048, 4096</i> | Définit la qualité en ajustant la taille de la grille, mais utilise par défaut l’entrée correspondante. Peut être utilisé pour accélérer le calcul. |
| <b>Échelle d&#39;Height de surface</b> <i>0.0 - 1.0</i> | Multiplicateur pour déterminer comment l’height est interprété. |
| <b>Position de l&#39;Height de surface</b> <i>0.0 - 1.0</i> | Définissez la distance entre la surface de réfraction et la projection. |
| <b>IOR de surface</b> <i>1.0 - 2.0</i> | Définissez l’index de réfraction. Dans la version couleur, cette option ajoute une dispersion de couleur supplémentaire. |
| <b>Taille du photon</b> <i>1.0 - 50.0</i> | La taille du photon affecte la netteté de l’effet. |
| <b>Dispersion</b> <i>0.0 - 0.01 (version couleur uniquement)</i> | Affectez uniquement la dispersion des couleurs. Non visible lorsque l&#39;IOR est faible. |
| <b>Variation</b> <i>0.0 - 1.0</i> | Ajoutez une variation irrégulière aux particules de photons de convertit. |
| <b>Position claire</b> | Déplace la position de la lumière. Également fait à travers un gadget dans la Vue 2D. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur de couleur) (version de couleur uniquement)</i> | Modifiez la couleur d’arrière-plan. Limité au noir dans la version en niveaux de gris. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Activer la compensation de la courbure et du étire avec des rapports non carrés. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/rt-caustics-grayscale-1.png" />
        </td>
    </tr>
</table>
