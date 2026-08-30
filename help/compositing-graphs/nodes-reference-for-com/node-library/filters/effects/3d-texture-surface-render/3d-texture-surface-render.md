---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Utilisez le nœud Rendu de surface de texture 3D pour effectuer le rendu des textures de surface à partir de données 3D afin de créer des effets de surface procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendu de surface de texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Rendu de surface de texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>Entrée :</b> Filtre > Effet

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Le nœud **Rendu de surface de texture 3D** effectue le rendu de la surface d&#39;une forme décrite par une *texture 3D*, en utilisant son *champ de distance* correspondant à partir de l&#39;entrée d&#39;image **Champ de distance 3D**.

La surface est représentée dans les limites d&#39;un *cube unitaire*. L&#39;éclairage est calculé à l&#39;aide de l&#39;image d&#39;entrée **Environnement** mappée à une sphère infinie.

>[!NOTE]
>
> Le champ de distance est censé être une texture **4096x4096** décrivant la forme avec une grille **16x16** de 256 tranches.\
> Vous pouvez utiliser le nœud [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) pour calculer le champ de distance pour une texture 3D de 256 tranches.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Champ de distance 3D</b> <i>Niveaux de gris</i> | Image 4 096 x 4 096 représentant les 256 <i>tranches</i> du <i>champ de distance</i> d&#39;une forme, organisées dans une grille 16 x 16.<br>Vous pouvez utiliser le nœud [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) pour calculer le champ de distance pour une texture 3D de 256 tranches. |
| <b>Environnement</b> <i>Couleur</i> | Image représentant l&#39;<i>environnement</i> qui doit être mappée à une sphère infinie dans le rendu et utilisée pour calculer l&#39;<i>éclairage</i>.<br>L&#39;image est également utilisée pour effectuer le rendu de l&#39;arrière-plan de la scène lorsque le paramètre <b>Mode de l&#39;arrière-plan</b> est défini sur <i>Ambiant</i> ou <i>Environnement</i>. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Résolution de sortie</b> <i>Entier2</i> | Résolution de l&#39;image de sortie en <b>X</b> et <b>Y</b>, exprimée comme une <i>puissance de deux</i>. |
| <b>Position de la Caméra</b> <i>Float2</i> | Position de la caméra autour de la forme.<br>Lorsque le nœud est sélectionné, vous pouvez utiliser le widget de position dans la <b>vue 2D</b> pour <i>orbite</i> de la caméra. |
| <b>Distance De Caméra</b> <i>Flotter</i> | Distance entre la caméra et la forme. |
| <b>Caméra FOV</b> <i>Flotter</i> | Champ de vision de l&#39;appareil photo en <i>degrés</i>. |
| <b>Albédo</b> <i>Float3</i> | Couleur albédo de la surface de la forme. |
| <b>Mode Arrière-plan</b> <i>Nombre entier</i> | Méthode de représentation de l&#39;arrière-plan de la scène rendue : <br>- <i>Éclairement du Sol</i> : éclairement calculé du plan du sol<br>- <i>Ambiant</i> : couleur ambiante de l&#39;entrée d&#39;image <b>Environnement</b> mappée à une sphère infinie, qui est semblable à une version fortement floue de l&#39;image<br>- <i>Couleur uniforme</i> : remplir uniformément l&#39;arrière-plan avec une couleur spécifiée<br>- <i>Environnement</i> : l&#39;entrée d&#39;image <b>Environnement</b> mappée à un sphère infinie |
| <b>Couleur d&#39;arrière-plan</b> <i>Float4</i> | Couleur utilisée pour remplir uniformément l&#39;arrière-plan de la scène rendue.<br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Mode arrière-plan</b> est défini sur <i>Couleur uniforme</i>. |
| <b>Activer le plan de Sol</b> <i>Booléen</i> | Lorsque <i>Vrai</i>, rend un plan au sol. Le <i>cube unitaire</i> entourant la forme repose sur ce plan. |
| <b>Plan Infini</b> <i>Booléen</i> | Définit le plan du sol sur <i>s&#39;étendre à l&#39;infini</i> jusqu&#39;à l&#39;horizon.<br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Activer le plan du Sol</b> est défini sur <i>Vrai</i>. |
| <b>Taille du plan du Sol</b> <i>Float2</i> | Ajuste la taille du plan du sol.<br><i>Remarque</i> : ce paramètre n&#39;est disponible que lorsque le paramètre <b>Activer le plan du Sol</b> est défini sur <i>Vrai</i> et le paramètre <b>Plan infini</b> sur <i>Faux</i>. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
