---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: Utilisez le nœud Mosaïque aléatoire 2 pour créer des motifs de mosaïque aléatoires avec des commandes de variation avancées dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque aléatoire 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---


# Mosaïque aléatoire 2

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2.jpg){width="200px"}

**Entrée :** *Générateurs de textures* */Motifs*

**Complexe**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Le nœud **Tile Random 2** génère des carreaux adjacents de tailles aléatoires et de rapports height/largeur.

La grille peut être modifiée en *inclinant* de manière aléatoire les côtés des formes pour séparer les angles.

Les formes peuvent être ajustées avec des options de *mise à l&#39;échelle*, de *biseautage*, d&#39;*arrondi des angles*, ainsi que de *rotation déformée*.

Ces réglages peuvent être contrôlés par des *cartes d&#39;entrée*.

Une sortie dédiée vous permet d&#39;entrer les **UV** de la forme en **Flood Fill à (...)** pour appliquer une variation supplémentaire.

</td>
</tr>
</table>

## Paramètres

### Entrées

* **Mappage De Taille Aléatoire** *Niveaux De Gris*\
  Image d’entrée en niveaux de gris qui contrôle l’échelle aléatoire des formes.\
  Son impact est contrôlé par le paramètre **Multiplicateur de mappage d&#39;entrée de taille aléatoire**.
* **Random Slant Map** *Grayscale* Image d&#39;entrée en niveaux de gris qui contrôle l&#39;inclinaison aléatoire des formes.\
  Son impact est contrôlé par le paramètre **Multiplicateur de mappage d&#39;entrée d&#39;inclinaison aléatoire**.
* **Courbe De Rayon D&#39;Arrondi** *En Niveaux De Gris*\
  Image d’entrée en niveaux de gris qui contrôle le rayon des angles arrondis des formes.\
  Son impact est contrôlé par la **texture d&#39;entrée de rayon d&#39;arrondi**. paramètre.
* **Map distance Biseautée** *Niveaux De Gris*\
  Image d’entrée en niveaux de gris qui contrôle le biseau des formes.\
  Son impact est contrôlé par la **courbe de transfert de distance en biseau Mult.** paramètre.
* **Mappage De Masque** *En Niveaux De Gris*\
  Image en niveaux de gris qui contrôle le masquage des formes.\
  Son impact est contrôlé par les paramètres **Début de l&#39;entrée de mappage de masque** et **Fin de l&#39;entrée de mappage de masque**.

### Paramètres

* **Quantité X** *Nombre entier*\
  Nombre de cellules sur l&#39;axe **X**.
* **Quantité Y** *Entier*\
  Nombre de cellules sur l&#39;axe **Y**.
* Taille
  * **Multiplicateur De Taille Aléatoire** *Flottant*\
    Applique un réglage *global* à l&#39;intensité de la mise à l&#39;échelle aléatoire.
  * **Multiplicateur De Mappage D&#39;Entrée De Taille Aléatoire** *Flottant*\
    Règle l&#39;intensité de la mise à l&#39;échelle aléatoire à l&#39;aide des valeurs *échantillonnées* à partir de l&#39;entrée **Mappage de taille aléatoire**.
  * **Taille Aléatoire X** *Flottant*\
    Règle l&#39;intensité de la mise à l&#39;échelle aléatoire sur l&#39;axe **X** *uniquement*.
  * **Taille Aléatoire Y** *Flottant*\
    Règle l&#39;intensité de la mise à l&#39;échelle aléatoire sur l&#39;axe **Y** *uniquement*.
  * **Répartition Aléatoire De La Taille** *Nombre Entier*\
    Contrôle la méthode de distribution des valeurs de mise à l’échelle aléatoire :
    * *Uniforme* : l&#39;échelle aléatoire est appliquée *de la même manière* sur toutes les cellules
    * *Bruit bleu* : l&#39;échelle aléatoire est *ajustée* à l&#39;aide d&#39;un motif de bruit bleu
* Aspect de la forme - Transformation
  * **Thickness d&#39;interstice** *Flottant* Ajuste le thickness de l&#39;espace entre les formes. Il est *égal pour toutes* formes.
  * **Multiplicateur De Position Aléatoire** *Flottant*\
    Applique un décalage de position aléatoire à la forme jusqu&#39;à ce qu&#39;elle *rencontre la bordure de sa cellule*.
  * **Rayon des angles arrondis** *Flottant* Ajuste le *rayon* des angles arrondis des formes. Une valeur de **0** signifie qu&#39;aucun arrondi n&#39;est appliqué.\
    *Remarque* : cet effet ne peut pas être appliqué lorsque le paramètre **Activer le contrôle de biseau par axe** est défini sur *Vrai*.
  * **Cartographie d&#39;entrée de rayon d&#39;arrondi multiple.** *Flottant* Ajuste l&#39;intensité de l&#39;impact de la courbe d&#39;entrée **Courbe de transfert de rayon d&#39;arrondi** sur le rayon des angles arrondis.\
    La carte agit comme un multiplicateur *par pixel* pour le paramètre **Rayon d&#39;arrondi**.\
    *Remarque* : cet effet ne peut pas être appliqué lorsque le paramètre **Activer le contrôle de biseau par axe** est défini sur *Vrai*.
  * **Multiplicateur D&#39;Échelle** *Flottant*\
    Ajuste la taille de chaque forme, en tant que proportion de la *zone de sa cellule*.
  * **Échelle aléatoire** *Flottant* Ajuste l&#39;intensité selon laquelle une échelle aléatoire est appliquée à *chaque* forme.
  * **Rotation** *Flotter* Fait pivoter les formes dans leurs cellules en déplaçant chaque *coin* vers son *voisin* le long de la bordure de la cellule.\
    Cette méthode entraîne l&#39;application d&#39;une certaine quantité de *distorsion* et de *mise à l&#39;échelle* à la forme lors de sa rotation.
  * **Aléatoire de rotation** *Flottant* Ajuste l&#39;intensité selon laquelle une quantité aléatoire de rotation est appliquée à chaque forme.\
    La méthode de rotation est décrite dans le paramètre **Rotation**.
  * **Les coins se positionnent aléatoirement** *flottent* déforment les formes en appliquant une quantité aléatoire de *décalage* à chacun de leurs *coins* le long de la bordure de leur cellule.
* Inclinaison
  * **Multiplicateur aléatoire d&#39;inclinaison** *Flottant*\
    Applique un réglage *global* à l&#39;intensité de l&#39;inclinaison aléatoire.
  * **Multiplicateur de mappage d&#39;entrée d&#39;inclinaison aléatoire** *Flottant*\
    Règle l&#39;intensité de l&#39;inclinaison aléatoire à l&#39;aide des valeurs *échantillonnées* à partir de l&#39;entrée **Courbe de l&#39;inclinaison aléatoire**.
  * **Inclinaison Aléatoire X** *Flottant*\
    Règle l’intensité de l’inclinaison aléatoire\
    sur l&#39;axe **X** *uniquement*.
  * **Inclinaison aléatoire Y** *Flotter*\
    Règle l’intensité de l’inclinaison aléatoire\
    sur l&#39;axe **Y** *uniquement*.
  * **Distribution Aléatoire De L&#39;Inclinaison** *Nombre Entier*\
    Contrôle la méthode de distribution des valeurs d’inclinaison aléatoires :
    * *Uniforme* : l&#39;inclinaison aléatoire est appliquée *de la même manière* sur toutes les cellules
    * *Bruit bleu* : l&#39;inclinaison aléatoire est *ajustée* à l&#39;aide d&#39;un motif de bruit bleu
* Biseau
  * **Mode De Distance Biseautée** *Nombre Entier*\
    Définit la méthode d&#39;*acquisition de la distance* selon laquelle les formes doivent être biseautées :
    * *Selon la taille de la grille* : les formes sont biseautées selon la *proportion de leur taille de grille* spécifiée-*Selon la taille de forme* spécifiée : les formes sont biseautées selon la *proportion de leur taille* spécifiée
    * *Par rapport à la taille de l&#39;image* : les formes sont biseautées selon la *proportion de l&#39;image* spécifiée
  * **Multiplicateur de distance en biseau** *Flottant*\
    Applique un réglage *global* à la distance du biseau.
  * **Courbe de transfert de distance en biseau multiple.** *Flotter*\
    Ajuste la distance du biseau à l&#39;aide de la courbe d&#39;entrée de la **Map distance du biseau** sous la forme d&#39;un multiplicateur *par pixel*.
  * **Courbe Arrondie En Biseau** *Flottant*\
    Ajuste l&#39;intensité de l&#39;arrondi appliqué à l&#39;angle de biseau pour le rendre plus *convexe*.
  * **Activer le contrôle de biseau par axe** *booléen*\
    Lorsque *Vrai*, le biseautage peut être appliqué et ajusté *séparément* sur les axes **X** et **Y**.\
    *Remarque* : cette *annulation* de l&#39;effet **Arrondis**.
  * **Distance En Biseau X** *Flotter*\
    Ajuste la distance du biseau sur l&#39;axe **X** *uniquement*. Cette distance dépend de la valeur du paramètre **Mode de distance en biseau**.\
    *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Activer le contrôle de biseau par axe** est défini sur *Vrai*.
  * **Distance en biseau Y** *Flotter*\
    Ajuste la distance du biseau sur l&#39;axe **Y** *uniquement*. Cette distance dépend de la valeur du paramètre **Mode de distance en biseau**.\
    *Remarque* : ce paramètre n&#39;est disponible que lorsque le paramètre **Activer le contrôle de biseau par axe** est défini sur *Vrai*.
* Masque
  * **Inversion aléatoire du masque** *booléen*\
    Inverse le masquage aléatoire des formes.
  * **Démarrage aléatoire du masque** *Flottement*\
    Pour une **valeur de départ aléatoire** donnée, le masquage pseudo-aléatoire est appliqué suivant un *ordre spécifique* d&#39;une forme de début à une forme de fin. Ce paramètre vous permet de *décaler l&#39;index* de la forme *début*.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *supérieure* à la valeur **Fin aléatoire du masque**.
  * **Masquer la fin aléatoire** *Flotter* Pour une **valeur de départ aléatoire** donnée, le masquage pseudo-aléatoire est appliqué suivant un *ordre spécifique* d&#39;une forme de début à une forme de fin. Ce paramètre vous permet de *décaler l&#39;index* de la forme *end*.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *supérieure* à la valeur **Démarrage aléatoire du masque**.
  * **Inversion du masque par zone de cellule** *booléen*\
    Inverse le masquage des formes par la zone de leurs cellules.
  * **Démarrage du masque par zone de cellule** *Flottement*\
    Ajuste le seuil de zone de la cellule *minimum* pour le masquage des formes.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *supérieure* à la valeur **Masquer par fin de zone de cellule**.
  * **Masquer par fin de zone de cellule** *Flotter* Ajuste le seuil de zone de *maximum* cellule pour masquer les formes.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *inférieure* à la valeur **Masquer par début de zone de cellule**.
  * **Inversion d&#39;entrée de mappage de masque** *Booléen*\
    Inverse le masquage des formes par le mappage d&#39;entrée **Mask Map**.
  * **Début de l&#39;entrée de mappage de masque** *Flottant*\
    Ajuste le seuil de *valeur de niveau de gris minimale* dans le mappage d&#39;entrée **Mask Map** pour le masquage des formes.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *supérieure* à la valeur **Fin d&#39;entrée de mappage de masque**.
  * **Fin de l&#39;entrée de mappage de masque** *Flottant* Ajuste le seuil de *valeur maximale de niveaux de gris* dans le mappage d&#39;entrée de **mappage de masque** pour le masquage des formes.\
    *Remarque* : détermine une limite d&#39;une *plage de valeurs* pour le masquage. La valeur peut donc être *inférieure* à la valeur **Début de l&#39;entrée de mappage de masque**.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-inputs.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-demo.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-demo2.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-node.png){width="340px"}

</td>
</tr>
</table>
