---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: Utilisez le nœud fractal de Voronoï pour générer des motifs fractaux de Voronoï pour créer des textures cellulaires organiques.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal.png){width="200px"}

**Entrée :** *Générateurs De Textures* */Bruits*

**Intermédiaire**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **fractal Voronoi** génère un bruit de Voronoi 3D *fractal* mappé à une image 2D à l&#39;aide d&#39;une *projection orthographique Z-down*.

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
  Contrôle l&#39;échelle du bruit fractal de Voronoï.\
  *Remarque* : lorsque la fonctionnalité **Mosaïque** est activée sur *n&#39;importe quel axe*, l&#39;ajustement de l&#39;échelle est *gradué*. C&#39;est ce qui est attendu.
* **Taille** *Float3*\
  Contrôle la taille du bruit fractal de Voronoï sur les axes **X**, **Y** et **Z**. Les valeurs non uniformes entraînent un effet d&#39;*étirement ou de compression*.\
  *Remarque* : lorsque la **mosaïque** est activée sur *n&#39;importe quel axe*, le réglage de la taille est *par paliers*. C&#39;est ce qui est attendu.
* **Décalage** *Float3*\
  Applique un décalage à la *position* du bruit fractal de Voronoï sur les axes **X**, **Y** et **Z**.
* **Désordre** *Float3*\
  Intensité du *décalage aléatoire* appliqué à chaque point du bruit sur les axes **X**, **Y** et **Z**.
* **Intensité de la Distorsion** *Flottant*\
  Contrôle l&#39;intensité d&#39;un *effet de déformation* appliqué sur le bruit fractal de Voronoi.
* **Multiplicateur D&#39;Échelle De Distorsion** *Flottant*\
  Contrôle l&#39;échelle du *motif de déformation* utilisé dans l&#39;effet de déformation contrôlé par l&#39;**intensité de la Distorsion**.
* **Niveau Min** *Nombre Entier*\
  *niveau minimum de répétition* utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif *plus riche* avec une variation sur davantage de plages de fréquences.
* **Niveau Max** *Nombre Entier*\
  *niveau de répétition* maximum utilisé dans le motif fractal. Une plage minimale/maximale plus large donne un motif *plus riche* avec une variation sur davantage de plages de fréquences.
* **Rugosité** *Flotter*\
  Contrôle l&#39;*équilibre* entre les *niveaux de répétition* bas et élevés dans le motif fractal.\
  *Remarque* : une valeur de **0** entraîne une sortie *non conforme* à d&#39;autres valeurs faibles qui la suivent. C&#39;est ce qui est attendu.\
  *Remarque 2* : ce paramètre est disponible uniquement lorsque le paramètre **Mode de fusion** est défini sur *Ajouter*.
* **Lacunarité** *Flottant*\
  Contrôle la façon dont le motif fractal appliqué *remplit l&#39;espace*. Une valeur *plus élevée* entraîne *moins d&#39;espaces* dans le motif et un bruit *plus dense*.
* **Opacité globale** *Flottant*\
  Contrôle la *plage* des valeurs fractales de bruit de Perlin à partir de 0.
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
* **Mode de fusion** *Entier*\
  Définit la méthode de fusion des valeurs des *cellules se chevauchant* dans l&#39;espace :
  * *Ajouter* : ajoutez les valeurs
  * *Max* : conserver la valeur *la plus élevée*
  * *Min* : conserver la valeur *la plus basse*
* **Style** *Entier* Définit la méthode *de rendu des données* du bruit fractal de Voronoi, en tenant compte du fait que le bruit est basé sur un ensemble de points dans l&#39;espace :
  * *F1* : distance jusqu&#39;au *point le plus proche* dans l&#39;espace
  * *F2* : distance jusqu&#39;au *deuxième point le plus proche* dans l&#39;espace
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Bord *: le* bord entre chaque cellule* du bruit dans l&#39;espace
  * *Couleur aléatoire* : attribuez une *couleur plate aléatoire* à chaque cellule du bruit dans l&#39;espace
* **Thickness des contours** *Flotter* Ajuste le thickness des contours détectés entre les cellules du bruit fractal de Voronoï. Les arêtes sont détectées dans les axes X, Y et Z, de sorte que certaines épaisseurs peuvent augmenter plus rapidement que d&#39;autres en fonction de la *profondeur* des cellules.\
  *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Style** est défini sur *Edge*.
* **Mode générateur de couleurs aléatoire** *Entier*\
  Définit la méthode d&#39;*acquisition* de la valeur de départ aléatoire pour la sélection de couleur par cellule :
  * *Valeur de départ aléatoire globale* : utilisez la valeur de départ *héritée* par le nœud
  * *Valeur initiale manuelle* : utilisez une valeur initiale *discrète*\
    *Remarque* : ce paramètre est uniquement disponible lorsque le paramètre **Style** est défini sur *Couleur aléatoire*.
* **Générateur De Couleurs Aléatoire** *Nombre Entier*\
  Valeur de départ aléatoire discrète qui doit être utilisée pour la sélection de couleur par cellule.\
  *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Style** est défini sur *Couleur aléatoire* et que le paramètre **Mode générateur de couleur aléatoire** est défini sur *Générateur manuel*.
* **Activer les limites** *booléennes*\
  Ajuste le bruit fractal de Voronoi de sorte que son motif résultant *se répète* sur les axes X, Y et Z.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-sea.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-scifi-panel.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant4.jpg){width="256px"}

</td>
</tr>
</table>
