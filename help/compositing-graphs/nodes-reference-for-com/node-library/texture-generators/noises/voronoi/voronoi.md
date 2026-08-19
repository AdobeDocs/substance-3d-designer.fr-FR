---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Utilisez le nœud Voronoi pour générer des motifs Voronoi afin de créer des textures cellulaires et des effets de matériau organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**Entrée :** *Générateurs De Textures* */Bruits*

**Intermédiaire**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Voronoi** génère un bruit de Voronoi 3D mappé à une image 2D à l&#39;aide d&#39;une *projection orthographique Z-down*.

Ce nœud peut être testé avec [Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) en entrée au lieu d&#39;une map bakée réelle (comme illustré dans l&#39;exemple ci-dessous).

>[!WARNING]
>
> Ce bruit est destiné à être utilisé avec le *moteur GPU uniquement* (c&#39;est-à-dire **Direct** ou **OpenGL**). Accédez à **Outils > Changer de moteur...** ou appuyez sur la touche **F9** pour sélectionner le moteur souhaité.

</td>
</tr>
</table>

## Paramètres

* **Inverser** *Booléen*\
  Inverse l’image de sortie.
* **Échelle** *Flottant*\
  Contrôle l’échelle du bruit de Voronoï.\
  *Remarque* : lorsque la fonctionnalité **Mosaïque** est activée sur *n&#39;importe quel axe*, l&#39;ajustement de l&#39;échelle est *gradué*. C&#39;est ce qui est attendu.
* **Taille** *Float3*\
  Contrôle la taille du bruit de Voronoï sur les axes **X**, **Y** et **Z**. Les valeurs non uniformes entraînent un effet d&#39;*étirement ou de compression*.\
  *Remarque* : lorsque la **mosaïque** est activée sur *n&#39;importe quel axe*, le réglage de la taille est *par paliers*. C&#39;est ce qui est attendu.
* **Décalage** *Float3*\
  Applique un décalage à la *position* du bruit de Voronoï sur les axes **X**, **Y** et **Z**.
* **Désordre** *Float3*\
  Intensité du *décalage aléatoire* appliqué à chaque point du bruit sur les axes **X**, **Y** et **Z**.
* **Intensité de la Distorsion** *Flottant*\
  Contrôle l&#39;intensité d&#39;un *effet de déformation* appliqué sur le bruit de Voronoï.
* **Multiplicateur D&#39;Échelle De Distorsion** *Flottant*\
  Contrôle l&#39;échelle du *motif de déformation* utilisé dans l&#39;effet de déformation contrôlé par l&#39;**intensité de la Distorsion**.
* **Courbe Arrondie** *Flottant*\
  Arrondit la *pente* autour de chaque point du bruit pour le rendre *convexe*.\
  *Remarque* : ce paramètre n&#39;est pas disponible lorsque le paramètre **Style** est défini sur *Edge*.
* **Échelle de distance** *Flottant*\
  Ajuste la *distance du dégradé* autour de chaque point du bruit.
* **Mode Distance** *Nombre entier*\
  Définit la méthode pour *calculer le gradient de distance* autour de chaque point du bruit :
  * *Euclidéen*
  * *Manhattan*
  * *Tchebychev*
  * *Minkowski*
* **Nombre de Minkowski** *Flottant*\
  Ordre *p* de la distance de Minkowski. Si nous divisons le dégradé de distance en quadrants, ce nombre a l&#39;impact suivant sur ces quadrants :
  * p est *exactement* 1 : droit
  * p est *inférieur* à 1 : concave
  * p est *supérieur* à 1 : convexe\
    Valeurs intéressantes :\
    *-1.0* : distance de Manhattan\
    *-2.0* : distance euclidienne\
    *- Infini* : distance de Tchebychev\
    *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Mode distance** est défini sur *Minkowski*.
* **Style** *Entier* Définit la méthode *de rendu des données* du bruit de Voronoï, en tenant compte du fait que le bruit est basé sur un ensemble de points dans l&#39;espace :
  * *F1* : distance jusqu&#39;au *point le plus proche* dans l&#39;espace
  * *F2* : distance jusqu&#39;au *deuxième point le plus proche* dans l&#39;espace
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Bord *: le* bord entre chaque cellule* du bruit dans l&#39;espace
  * *Couleur aléatoire* : attribuez une *couleur plate aléatoire* à chaque cellule du bruit dans l&#39;espace
* **Thickness des contours** *Flotter* Ajuste le thickness des contours détectés entre les cellules du bruit de Voronoï. Les arêtes sont détectées dans les axes X, Y et Z, de sorte que certaines épaisseurs peuvent augmenter plus rapidement que d&#39;autres en fonction de la *profondeur* des cellules.\
  *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Style** est défini sur *Edge*.
* **Mode générateur de couleurs aléatoire** *Entier*\
  Définit la méthode d&#39;*acquisition* de la valeur de départ aléatoire pour la sélection de couleur par cellule :
  * *Valeur de départ aléatoire globale* : utilisez la valeur de départ *héritée* par le nœud
  * *Valeur initiale manuelle* : utilisez une valeur initiale *discrète*\
    *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Style** est défini sur *Couleur aléatoire*.
* **Générateur De Couleurs Aléatoire** *Nombre Entier*\
  Valeur de départ aléatoire discrète qui doit être utilisée pour la sélection de couleur par cellule.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Style** est défini sur *Couleur aléatoire* et que le paramètre **Mode générateur de couleur aléatoire** est défini sur ***Générateur manuel***.
* **Extension non carrée** *Booléenne*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
