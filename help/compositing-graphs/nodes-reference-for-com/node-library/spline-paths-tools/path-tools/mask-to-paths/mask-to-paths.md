---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: Utilisez le nœud Masquer sur tracés pour convertir les textures de masque en données de tracé pour la génération de tracés procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Masquer sur les tracés
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Masquer sur les tracés

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/mask-to-paths-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils De Tracé

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Convertit un motif d&#39;entrée en niveaux de gris <b>Masque</b> en une liste de segments de tracé codés dans la sortie <b>Tracés</b>.

Des commandes permettant de définir la position de départ des tracés générés, ainsi que leur ordre dans la liste, sont disponibles.

Les tracés générés peuvent être traités ultérieurement à l’aide de nœuds dédiés, par exemple [Transformation 2D du tracé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Déformation des tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md), ou convertis en splines à l’aide du nœud [Tracé vers spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour mapper ou dispersion des formes le long de ceux-ci.

</td>
</tr>
</table>

>[!NOTE]
>
> La méthode utilisée pour coder les chemins est expliquée dans la page [Spécifications de format des chemins](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md).

## Connecteurs d’entrée

<b>Masquer</b> *Niveaux de gris*\
Motif d’entrée qui doit être converti en liste de tracés.

## Connecteurs de sortie

<b>Aperçu</b> *Couleur* Un aperçu composé au-dessus du masque pour aider à visualiser les effets des paramètres.

<b>Tracés</b> *Couleur*\
Liste des tracés codés dans une image couleur. chaque chemin décrit une liste de segments codés.\
Le résultat peut être traité à l&#39;aide d&#39;un autre nœud de traitement des tracés ou envoyé à un nœud [Tracés vers spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) pour le traiter davantage en tant que splines.

## Paramètres

<b>Masque lisse</b> *Flotter*\
Appliquez le lissage sur le masque d’entrée.\
Utile lorsque le motif d’entrée a des bords très nets, ce qui provoque généralement des artefacts.

<b>Valeur du seuil du masque</b> *Flotter* La valeur de niveau de gris de <b>Masque</b> qui sera utilisée pour séparer l&#39;extérieur (valeurs &lt; valeur de seuil du masque) et l&#39;intérieur (valeurs > valeur de seuil du masque) de la forme.

<b>Décimer le chemin</b> *Float* contrôle implicitement le nombre de segments qui seront générés.\
Une décimation importante rendra les formes arrondies quelque peu polygonales, tandis qu’aucune décimation ne générera presque un segment par pixel.\
Une quantité raisonnable correspondra mieux à la forme des lignes droites et des courbes sans créer beaucoup de points intermédiaires pour les lignes droites.

<b>Fermer les tracés ouverts</b> *Booléen* Créez un segment entre les sommets de début et de fin des tracés ouverts.\
La désactivation de cette option peut corriger les lignes indésirables traversant votre motif de manière inattendue, mais les tracés ne sont peut-être plus fermés.

<b>Seuil d&#39;angle</b> *Flotter*\
Chaque sommet codé dans des tracés peut contenir un drapeau indiquant s’il est dur (c’est-à-dire s’il s’agit d’un coin) ou lisse.\
Ce paramètre vous permet de marquer plus ou moins d’angles en fonction de l’angle formé par leurs segments adjacents.\
*Remarque :* cet indicateur d&#39;angle n&#39;est actuellement pris en charge par aucun nœud existant, mais peut être utilisé dans un [processeur de sommets de tracé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). Vous pouvez également visualiser les coins avec le nœud [Tracés de prévisualisation](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md).

<b>Mode de démarrage du chemin</b> *Entier* Méthode de sélection du sommet qui doit être le début de chaque tracé généré autour des formes du masque.\
Cela a un impact significatif lors de la conversion des <b>chemins en splines</b> générés à l&#39;aide du nœud dédié, car plusieurs nœuds splines utilisent le début et la fin des splines.\
*- Sommet le plus aigu :* sommet formant l&#39;angle le plus bas avec ses sommets précédent et suivant\
*- Sommet à l&#39;extrême d&#39;une direction spécifiée :* Le dernier sommet dans une direction donnée\
*- Sommet le plus proche d&#39;une position spécifiée
* Sommet le plus éloigné d’une position spécifiée
* Fonction de démarrage personnalisée :* Utilisez une fonction personnalisée pour sélectionner le sommet qui doit être utilisé comme début de chaque tracé

<b>Direction du démarrage</b> *Flottant* L’angle décrivant la direction utilisée pour sélectionner le sommet de démarrage. Pour chaque tracé, le dernier sommet dans cette direction est sélectionné.\
La valeur est un *nombre de tours* utilisé pour faire pivoter un vecteur X-direction gauche. Cela signifie que 0 définit un vecteur de direction de (-1, 0) et 0,25 (90 degrés) définit un vecteur de direction de (0, 1).\
*Remarque :* ce paramètre est disponible lorsque le <b>mode de démarrage du tracé</b> est défini sur « Sommet à l’extrême d’une direction spécifiée »

<b>Position cible au démarrage</b> *Float2* Position dans l’image utilisée pour sélectionner le sommet de démarrage.\
Pour chaque tracé, le sommet le plus proche ou le plus éloigné de cette position est sélectionné, en fonction du <b>mode de démarrage du tracé</b> sélectionné.\
*Remarque :* ce paramètre est disponible lorsque le <b>mode de démarrage du tracé</b> est défini sur « Sommet le plus proche d’une position spécifiée » ou « Sommet le plus éloigné d’une position spécifiée »

<b>Fonction de démarrage</b> *Flottant* Fonction utilisée pour sélectionner le sommet de démarrage. Elle renvoie une valeur de type Float.\
Pour chaque sommet, la fonction est exécutée et le sommet pour lequel la fonction renvoie le *résultat le plus élevé* est sélectionné.\
Variables disponibles :\
*-* vertex.cornerness(Float)*:* Le score du sommet comme candidat à un sommet\
*-* vertex.pos(Float2)*:* Position du sommet dans l&#39;espace d&#39;image\
*Remarque :* ce paramètre est disponible lorsque le mode de démarrage du tracé est défini sur « Sommet le plus proche d&#39;une position spécifiée » ou « Fonction de démarrage personnalisée »

<b>Mode de commande</b> *Entier* Méthode d’ordre des chemins générés.\
La position ou la taille du *cadre de sélection* des Tracés (Bbox) peut être utilisée comme critère pour organiser les Tracés.\
Cela a un impact significatif lors de la conversion des <b>chemins en splines</b> générés à l&#39;aide du nœud dédié, car plusieurs nœuds splines utilisent l&#39;ordre des splines.\
*- Hérité (rapide) :* méthode utilisée dans la version précédente de ce nœud, qui offre des performances nettement supérieures\
*- Par position centrale de la Bbox dans la direction :* les tracés sont ordonnés en fonction de la position du centre de leur Bbox, du premier au dernier le long de la direction spécifiée\
*- Par la position supérieure gauche de la zone de rectangle selon la direction :* les tracés sont ordonnés en fonction de la position de l&#39;angle supérieur gauche de leur zone de rectangle, du premier au dernier, dans la direction spécifiée\
*- Par taille de Bbox - Du plus grand au plus petit :* les chemins sont classés en fonction de la taille de leur Bbox, du plus grand au plus petit\
*- Par taille de Bbox - Du plus petit au plus grand :* les chemins sont classés en fonction de la taille de leur Bbox, du plus petit au plus grand\
*- Fonction d&#39;ordre personnalisée :* Utilisez une fonction personnalisée pour organiser les chemins

<b>Sens de la commande</b> *Flottant* L’angle décrivant la direction utilisée pour ordonner les tracés du premier au dernier dans cette direction.\
La valeur est un *nombre de tours* utilisé pour faire pivoter un vecteur de direction X-gauche. Cela signifie que 0 définit un vecteur de direction de (-1, 0) et 0,25 (90 degrés) définit un vecteur de direction de (0, 1).

<b>Fonction de commande</b> *Float* Fonction utilisée pour organiser les tracés. Elle renvoie une valeur de type Float.\
Les chemins sont classés *par ordre croissant* en fonction de la valeur de cette fonction. En d&#39;autres termes, le résultat de la fonction pour chaque chemin est la *clé de tri* utilisée pour organiser les chemins.\
Variables disponibles :
* bbox.center (Float2) : position du centre de la zone de tracé
* bbox.topleft (Float2) : position du coin supérieur gauche de la zone de tracé
* bbox.size (Float2) : taille de la zone de tracé (X : largeur, Y : height)

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/MaskToPaths-Demo2.gif "Exemple de nœud 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 1](../../../../../../assets/MaskToPaths-Demo1.gif "Exemple de nœud 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemple de nœud 3 : modes de démarrage](../../../../../../assets/MaskToPaths-Demo3.gif "Exemple de nœud 3 : modes de démarrage"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 3 : modes de classement](../../../../../../assets/MaskToPaths-Demo4.gif "Exemple de nœud 3 : modes de classement"){zoomable="yes"}

</td>
</tr>
</table>
