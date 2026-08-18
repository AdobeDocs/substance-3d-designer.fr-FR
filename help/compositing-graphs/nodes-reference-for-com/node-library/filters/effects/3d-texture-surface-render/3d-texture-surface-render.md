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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# Rendu de surface de texture 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**Entrée :** *Filtre/Effet*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

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

## Paramètres

### Entrées

* **Champ De Distance 3D** *Niveaux De Gris*\
  Image 4 096 x 4 096 représentant les 256 *tranches* du *champ de distance* d&#39;une forme, organisées dans une grille 16 x 16.\
  Vous pouvez utiliser le nœud [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) pour calculer le champ de distance pour une texture 3D de 256 tranches.
* **Environnement** *Couleur*\
  Image représentant l&#39;*environnement* qui doit être mappée à une sphère infinie dans le rendu et utilisée pour calculer l&#39;*éclairage*.\
  L&#39;image est également utilisée pour effectuer le rendu de l&#39;arrière-plan de la scène lorsque le paramètre **Mode de l&#39;arrière-plan** est défini sur *Ambiant* ou *Environnement*.

### Paramètres

* **Résolution de sortie** *Entier2*\
  Résolution de l&#39;image de sortie en **X** et **Y**, exprimée comme une *puissance de deux*.
* **Position de l&#39;appareil photo** *Float2*\
  Position de la caméra autour de la forme.\
  Lorsque le nœud est sélectionné, vous pouvez utiliser l&#39;objet de positionnement dans la **Vue 2D** pour *orbiter* la caméra.
* **Distance appareil photo** *Flottant*\
  Distance entre la caméra et la forme.
* **Camera FOV** *Float*\
  Champ de vision de l&#39;appareil photo en *degrés*.
* **Albédo** *Float3*\
  Couleur albédo de la surface de la forme.
* **Mode Arrière-Plan** *Entier*\
  Méthode de représentation de l’arrière-plan de la scène rendue :
  * *Irradiance du sol* : l&#39;irradiance calculée du plan au sol
  * *Ambiant* : la couleur ambiante de l&#39;entrée d&#39;image de l&#39;**environnement** mappée à une sphère infinie, qui s&#39;apparente à une version fortement floue de l&#39;image
  * *Couleur uniforme* : remplir uniformément l&#39;arrière-plan avec une couleur spécifiée
  * *Environnement* : entrée d&#39;image **Environnement** mappée à une sphère infinie
* **Couleur D&#39;Arrière-Plan** *Float4*\
  Couleur utilisée pour remplir uniformément l’arrière-plan de la scène rendue.\
  *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Mode d&#39;arrière-plan** est défini sur *Couleur uniforme*.
* **Activer le plan au sol** *booléen*\
  Lorsque *Vrai*, rend un plan au sol. Le *cube unitaire* entourant la forme repose sur ce plan.
* **Plan Infini** *Booléen*\
  Définit le plan au sol sur *s&#39;étendre infiniment* jusqu&#39;à l&#39;horizon.\
  *Remarque* : ce paramètre est disponible uniquement lorsque le paramètre **Activer le plan au sol** est défini sur *Vrai*.
* **Taille du plan au sol** *Float2* Ajuste la taille du plan au sol.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Activer le plan au sol** est défini sur *Vrai* et le paramètre **Plan infini** sur *Faux*.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
