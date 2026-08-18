---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Utilisez le nœud Circulaire éclaboussé pour effectuer une dispersion de formes circulaires entre les textures afin de créer des motifs organiques et aléatoires.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure circulaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Éclaboussure circulaire

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

## Éclaboussure circulaire (couleur)

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Splatter Circular génère un motif en anneau avec différentes commandes. Il peut utiliser des formes prédéfinies ou des entrées personnalisées. Il est similaire à [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mais avec un placement circulaire au lieu d&#39;une grille.

Cette option est utile lorsque vous souhaitez placer des formes de manière circulaire avec diverses options de randomisation.

## Paramètres

### Entrées

Les deux entrées sont facultatives.

* **Entrée d’image de motif 1-6** : *Entrée en niveaux de gris (entrée couleur)*\
  Splatter Circular uniquement : image de motif personnalisé, utilisée lorsque le paramètre « Pattern » est défini sur « Image Input ».
* **Arrière-plan** : *Entrée niveaux de gris (entrée couleur)*

### Paramètres

* **Quantité du motif** : *1 - 64*\
  Quantité de carreaux de motif à placer sur un anneau.
* **Quantité aléatoire du motif** : *0,0 - 1,0*\
  Randomisation de la quantité de motifs à placer. À utiliser de préférence avec une quantité d’anneau supérieure à 1.
* **Quantité aléatoire de motif min** : *1 - 10* définit la quantité minimale de motifs pour la randomisation.
* **Quantité de sonnerie** : *1 - 10*\
  Définit le nombre d&#39;anneaux à remplir. Les anneaux sont toujours placés à l&#39;intérieur de l&#39;anneau extérieur, et l&#39;espace uniformément.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.
* **Motif**
  * **Motif** :*Entrée d&#39;image, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradation, Ondes, Demi-Cloche, Cloche striée, Croissant, Capsule, Cône*\
    Sélectionne la forme de motif à utiliser.
  * **Numéro d’entrée du motif** : *1 - 6* définit le nombre d’entrées d’image différentes à utiliser. Disponible uniquement lorsque l&#39;option *Entrée d&#39;image* est sélectionnée ci-dessus.
  * **Distribution D&#39;Entrée De Motif** : *Aléatoire, Par Numéro De Motif, Par Numéro D&#39;Anneau* Définit La Façon Dont Plusieurs Entrées De Motif Sont Choisies. Aléatoire signifie qu’un anneau aléatoire est choisi, Numéro de motif signifie qu’ils sont simplement placés dans une séquence en boucle, Par numéros d’anneau signifie que chaque anneau a un différent dans l’ordre.
  * **Filtrage D&#39;Entrée D&#39;Image** : *Bilinéaire + Mipmaps, Bilinéaire, Au Plus Proche*
  * **Spécifique Au Motif** : *0.0 - 1.0*\
    Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné.
  * **Aléatoire de symétrie** : *0,0 - 1,0*\
    Définit le nombre de vignettes qui doivent être retournées/mises en miroir de manière aléatoire en fonction du comportement ci-dessous.
  * **Mode aléatoire de symétrie** : *Horizontal + Vertical, Horizontal, Vertical* Détermine le comportement de mise en miroir de la symétrie.
* **Position**
  * **Rayon** : *0,0 - 1,0*\
    Définit le rayon à partir du centre auquel les motifs sont placés.
  * **Rayon aléatoire** : *0.0 - 1.0* aléatoire le rayon de chaque carreau de motif.
  * **Multiplicateur de rayon en anneau** : *0.0 - 1.0*\
    Affecte l&#39;espacement de plusieurs anneaux.
  * **Angle aléatoire** : *0,0 - 1,0* aléatoire l’angle de chaque motif. Plus les montants sont élevés, plus la rotation est importante.
  * **Facteur De Spirale** : *0,0 - 1,0*\
    Transforme les anneaux en spirales, où chaque carreau est placé à un rayon légèrement croissant.
  * **Répartition** : *0.0 - 2.0* Définit le nombre de tours que fait un anneau. Cela peut être augmenté au-delà de ses limites.
  * **Décalage dans la direction** : *0.0 - 1.0*\
    Éloigne chaque motif du centre selon son angle. L’effet dépend en grande partie de l’option Angle aléatoire ou ressemble simplement à un multiplicateur pour le rayon.
  * **Décalage global** : *0,0 - 1,0*\
    Traduit la forme entière.
* **Taille**
  * **Connecter les motifs** :*Faux/Vrai* rend la longueur des éléments de motif dépendante du rayon, ce qui signifie que chaque forme doit toucher la précédente et la suivante.
  * **Taille (Connectée)** : *0.0 - 1.0*\
    Modifie la taille globale de chaque motif. Une fois connecté, il est relatif au rayon total.
  * **Taille aléatoire** : *0,0 - 1,0*\
    Rend aléatoire la taille de chaque motif individuellement.
  * **Échelle** : *0.0 - 2.0*\
    Redimensionne uniformément chaque motif.
  * **Échelle Aléatoire** : *0.0 - 1.0*\
    Rend aléatoire la mise à l’échelle uniforme.
  * **Échelle par numéro de motif** : *0.0 - 1.0* L’échelle du motif dépend de la position le long de l’anneau.
  * **Inverser le numéro de motif** : *Faux/Vrai*\
    Utilisée avec l’option précédente, cette option permet d’inverser la mise à l’échelle de petite à grande et vice versa.
  * **Échelle par numéro d&#39;anneau** : *0.0 - 1.0* rend l&#39;échelle dépendante du numéro d&#39;anneau.
  * **Inverser la sonnerie** :*Faux/Vrai* Utilisé avec l&#39;option précédente, il peut inverser la mise à l&#39;échelle de petit à grand et vice versa.
* **Rotation**
  * **Rotation du motif** : *0.0 - 1.0* Fait pivoter chaque motif uniformément.
  * **Aléatoire de la rotation du motif** : *0.0 - 1.0*\
    Rend aléatoire la rotation du motif.
  * **Pivot De Rotation Du Motif** : *Centre, Min X, Max X, Min Y, Max Y*\
    Définit la position du point pivot autour duquel faire pivoter chaque motif individuellement.
  * **Centrer l&#39;orientation** :*Faux/Vrai*\
    Fait pivoter chaque motif de sorte qu’il soit orienté vers le centre de l’anneau. La désactiver leur donne la même orientation, ce qui peut produire des effets indésirables avec Décalage dans la direction.
  * **Rotation de l&#39;anneau** : *0.0 - 1.0* Fait pivoter l&#39;anneau entier autour du centre.
  * **Rotation aléatoire de l&#39;anneau** : *0.0 - 1.0* aléatoire la rotation par anneau.
  * **Décalage de rotation de l&#39;anneau** : *0,0 - 1,0*\
    Décale la rotation par anneau.
* **Couleur**
  * **Couleur** : *(valeur Niveaux de gris)*Couleur à multiplier avec le motif sélectionné.
  * **Luminance aléatoire** :*0.0 - 1.0* aléatoire la couleur ou la luminance pour chaque carreau de motif.
  * **Luminance par échelle** :*0.0 - 1.0* rend la luminance dépendante de l’échelle du motif individuel.
  * **Luminance par numéro de motif** : *0.0 - 1.0* rend la luminance dépendante de la séquence de motif. Peut par exemple être utilisé avec des spirales.
  * **Inverser le numéro de motif** : *Faux/Vrai* Inverse l’option précédente.
  * **Luminance par numéro d&#39;anneau** :*0.0 - 1.0* rend la luminance dépendante de la séquence d&#39;anneau.
  * **Inverser la sonnerie** :*Faux/Vrai* Inverse l&#39;option précédente.
  * **Masque aléatoire** :*0.0 - 1.0* Masque aléatoirement les motifs.
  * **Couleur d&#39;arrière-plan** : *(valeur Niveaux de gris)*Modifie la couleur d&#39;arrière-plan unie.
  * **Mode de fusion** : *Ajouter, Max, Ajouter sub* Définit la façon de fusionner des motifs qui se chevauchent.
  * **Opacité globale** : *0.0 - 1.0* Définit l’opacité globale de l’ensemble du résultat.

## Exemples d’images

![](../../../../../../assets/circularsplatter-ex.png)

</td>
</tr>
</table>
