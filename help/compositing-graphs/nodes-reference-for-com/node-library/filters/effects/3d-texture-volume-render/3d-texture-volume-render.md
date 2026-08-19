---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Utilisez le nœud de rendu de volume de texture 3D pour effectuer le rendu des textures volumétriques à partir de données 3D afin de créer des effets de nuage et de brouillard.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendu du volume de texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# Rendu du volume de texture 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**Entrée :** *Filtre/Effet*

**Simple**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Rendu du volume de texture 3D** effectue le rendu du volume d&#39;une forme décrite par une *texture 3D*, en utilisant son *champ de distance signé* correspondant à partir de l&#39;entrée d&#39;image **3D Champ de distance signée**.

Le volume est représenté dans les limites d&#39;un *cube unitaire*. L&#39;éclairage est calculé à l&#39;aide d&#39;une *lumière directionnelle* et d&#39;une *lucarne hémisphérique*.

>[!NOTE]
>
> Le champ de distance signé devrait être une texture **4096x4096** décrivant la forme avec une grille **16x16** de 256 tranches.\
> Vous pouvez utiliser le nœud [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) pour calculer le champ de distance signé pour une texture 3D de 256 tranches.

</td>
</tr>
</table>

## Paramètres

### Entrées

* **Champ de distance signée 3D** *Niveaux de gris*\
  Image 4 096 x 4 096 représentant les 256 *tranches* du champ de distance signé&#x200B;*d&#39;une forme, organisées dans une grille 16 x 16.*\
  Vous pouvez utiliser le nœud [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) pour calculer le champ de distance signé pour une texture 3D de 256 tranches.
* **Densité** *Niveaux de gris*\
  Image 4 096 x 4 096 représentant les 256 *tranches* de la *densité* d&#39;une forme, disposées dans une grille 16 x 16. La densité est mappée en utilisant des valeurs de niveaux de gris comprises entre 0 (entièrement transparent) et 1 (entièrement opaque).\
  Vous pouvez utiliser un [masque de volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) ou des nœuds de bruit 3D ([Bruit de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [Voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [Fractal de bruit strié 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md), etc.), combinés à un nœud [Position de texture 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) comme entrée de position, pour générer un masque de volume sous la forme d&#39;une texture 3D de 256 tranches.

### Paramètres

* **Résolution de sortie** *Entier2*\
  Résolution de l&#39;image de sortie en **X** et **Y**, exprimée comme une *puissance de deux*.
* **Position de l&#39;appareil photo** *Float2*\
  Position de la caméra autour de la forme.\
  Lorsque le nœud est sélectionné, vous pouvez utiliser l&#39;objet de positionnement dans la **Vue 2D** pour *orbiter* la caméra.
* **Position Claire** *Float2*\
  Position de la *lumière directionnelle* autour de la forme.\
  Lorsque le nœud est sélectionné, vous pouvez utiliser l&#39;objet de positionnement dans la **Vue 2D** pour *orbiter* la source lumineuse.
* **Distance appareil photo** *Flottant*\
  Distance entre la caméra et la forme.
* **Camera FOV** *Float*\
  Champ de vision de l&#39;appareil photo en *degrés*.
* **Absorption** *Flottant*\
  Règle la quantité de lumière absorbée lorsqu&#39;elle passe *à* dans le volume.
* **Contour progressif** *Flottant*\
  Multiplie la valeur fournie par l&#39;entrée **Densité** avec la valeur de champ de distance *interne*.\
  Cela ajuste efficacement la largeur du *dégradé de fondu* à partir de la limite extérieure du volume vers l&#39;intérieur.
* **Mode Couleur Claire** *Entier*\
  Définit la méthode d’acquisition de la couleur de la lumière directionnelle :
  * *Température (Kelvin)* : la couleur résulte de la température de la lumière, où une valeur *inférieure* entraîne une couleur *plus chaude*
  * *Couleur RGB* : définissez la couleur à l&#39;aide des valeurs RGB
* **Température De La Lumière (Kelvin)** *Flotter*\
  Température de la lumière directionnelle, qui affecte sa *couleur*. Une valeur *inférieure* entraîne une couleur *plus chaude*.\
  Valeurs utiles :\
  1800 K - Lumière de bougie\
  2800 K - Ampoule à incandescence\
  5500 K - Lumière du jour\
  6200 K - Blanc naturel\
  7000 K - Ciel couvert\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Mode couleur clair** est défini sur *Température (Kelvin)*.
* **Couleur claire** *Float3*\
  Couleur de la lumière directionnelle.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Mode de couleur de la lumière** est défini sur *Couleur RGB*.
* **Intensité de la lumière** *Flottant*\
  Intensité de la lumière directionnelle.
* **Couleur ambiante** *Float3*\
  Couleur de la lucarne ambiante.
* **Intensité ambiante** *Flottant*\
  Intensité de la lucarne ambiante.
* **Albédo** *Float3*\
  Couleur albédo du volume.
* **Mode Arrière-Plan** *Entier*\
  Méthode d&#39;ombrage de l&#39;arrière-plan de la scène rendue, en fonction de la **couleur d&#39;arrière-plan** :
  * *Ombré* : la couleur est affectée par la *couleur* et l&#39;*intensité*-*couleur constante* de la lumière directionnelle : la couleur est appliquée uniformément *quelle que soit* la couleur de la lumière directionnelle
* **Couleur D&#39;Arrière-Plan** *Float4*\
  Couleur utilisée pour remplir l’arrière-plan de la scène rendue.
* **Tramage** *Flottant*\
  Règle l&#39;intensité du *tramage du bruit bleu* utilisé pour lisser l&#39;ombrage.
* **Activer le plan au sol** *booléen*\
  Lorsque la valeur *True* est appliquée, elle rend un plan au sol *infini*. Le *cube unitaire* entourant la forme repose sur ce plan.
* **Plan Infini** *Booléen*\
  Définit le plan au sol sur *s&#39;étendre infiniment* jusqu&#39;à l&#39;horizon.\
  *Remarque* : ce paramètre est disponible uniquement lorsque le paramètre **Activer le plan au sol** est défini sur *Vrai*.
* **Taille du plan au sol** *Float2* Ajuste la taille du plan au sol.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Activer le plan au sol** est défini sur *Vrai* et le paramètre **Plan infini** sur *Faux*.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
