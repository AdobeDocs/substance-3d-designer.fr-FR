---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Utilisez le nœud Aléatoire de mosaïque pour créer des motifs de mosaïque aléatoires avec une variation procédurale pour les effets de texture organique.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque aléatoire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# Mosaïque aléatoire

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## Mosaïque aléatoire (couleur)

**Entrée :** *Générateurs/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Tile Random génère un motif de mosaïque procédural qui a un peu plus de chaos dans les formes de mosaïque que son homologue, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Pour ce faire, il scinde aléatoirement certains carreaux en carreaux plus petits. Nous vous conseillons de commencer par contourner le Tile Generator avant de vous attaquer à Tile Random, car de nombreux concepts sont similaires.

L&#39;option Mosaïque aléatoire est utilisée à la place de l&#39;option [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) lorsque l&#39;objectif est un motif plus ancien, moins organisé. Il a toutefois ses limites, alors envisagez de [juxtaposer Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) pour tout autre besoin avancé.

## Paramètres

### Entrées

* **Entrée de motif** :*Entrée en niveaux de gris (entrée couleur)*\
  Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ».
* **Entrée d&#39;arrière-plan** : *Entrée en niveaux de gris (entrée couleur)*

### Paramètres

* **X Quantité** : *1 - 64*\
  Quantité de répétitions X du motif.
* **Quantité Y** : *1 - 64*\
  Quantité de répétitions Y du motif.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.
* **Motif**
  * **Motif** :*Entrée de motif, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradation, Ondes, Demi-Cloche, Cloche striée, Croissant, Capsule, Cône*\
    Sélectionne la forme de motif à utiliser.
  * **Filtrage d&#39;entrée d&#39;image (moteur > v4)** : *Bilinéaire + Mipmaps, Bilinéaire, Au plus proche*
  * **Spécifique Au Motif** : *0.0 - 1.0*\
    Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné.
  * **Aléatoire spécifique au motif** : l&#39;effet d&#39;aléatoire *0.0 - 1.0* dépend du motif sélectionné.
  * **Rotation** :*0, 90, 180, 270, aléatoire horizontale, aléatoire verticale* définit la rotation par paliers de 90 degrés, avec une randomisation facultative.
  * **Rotation aléatoire** : *0.0 - 1.0* ajoute une rotation libre aléatoire.
  * **Aléatoire de symétrie** : **0.0 - 1.0** reflète aléatoirement certains motifs par le mode aléatoire de symétrie sélectionné. Plus cette valeur est élevée, plus les motifs seront mis en miroir.
  * **Mode aléatoire de symétrie** : *Horizontal + Vertical, Horizontal, Vertical* Détermine le comportement de mise en miroir lorsque le mode aléatoire de symétrie est supérieur à 0.
* **Fractionner**
  * **Mode** : *aucun, automatique, horizontal automatique, vertical automatique, aléatoire h+v* Définit la règle sur la division des vignettes.
  * **Seuil** : *0,0 - 1,0* Seuil de taille pour savoir quand diviser une mosaïque.
  * **Multiplicateur** : *0 - 10* Multiplicateur de fractionnement. Plus cette valeur est élevée, plus le fractionnement est important.
* **Taille**
  * **X aléatoire** :*0,0 - 1,0* aléatoire une mise à l&#39;échelle non uniforme sur l&#39;axe X.
  * **Y aléatoire** :*0.0 - 1.0* aléatoire une mise à l&#39;échelle non uniforme sur l&#39;axe Y.
* **Interstice**
  * **Mode** : *Relatif à la plus petite brique, Relatif à la plus grande brique* Définit l’interstice de taille de brique relatif à.
  * **Quantité** : *0,0 - 1,0* définit la taille de l&#39;espace entre les briques.
* **Forme**
  * **Échelle** : *0.0 - 1.0* L’échelle globale de chaque carreau.
  * **Mise à l’échelle aléatoire** : *0.0 - 1.0* Mise à l’échelle aléatoire par carreau.
  * **Rotation** : *0.0 - 1.0* Rotation globale pour chaque carreau.
  * **Rotation aléatoire** : *0.0 - 1.0* Rotation aléatoire par carreau.
  * **Contrainte de rotation** :*Faux/Vrai* Contraint l’échelle afin que les carreaux pivotés ne se chevauchent jamais.
* **Position**
  * **Décalage** : *0,0 - 1,0*\
    Déplace ou traduit les carreaux globalement, en glissant uniquement sur l’axe X
  * **Décalage aléatoire** :*0,0 - 1,0* décale de manière aléatoire par carreau, les diapositives se trouvant uniquement sur l’axe X
  * **Aléatoire** :*0,0 - 1,0* aléatoire la position, les carreaux se déplacent sur les axes X et Y.
  * **Contraintes aléatoires** :*Faux/Vrai* Les contraintes d’échelle font que les vignettes se touchent, mais ne se chevauchent pas. Atténue considérablement l’effet Position aléatoire.
* **Couleur**
  * **Couleur** : *(Valeur Niveaux de gris) / (Valeur de couleur)*Définit une couleur unie pour toutes les mosaïques.
  * **Aléatoire des couleurs** :*0.0 - 1.0* aléatoire des couleurs par carreau.
  * **Paramétrage des couleurs** :*aucun, zone, taille x, taille y* rend la variation de couleur dépendante de l’un de ces paramètres.
  * **Intensité du paramétrage des couleurs** : *Multiplicateur 0.0 - 1.0* pour l’effet de paramétrage ci-dessus.
  * **Effet de paramétrage des couleurs (pour la couleur uniquement) :** **RGB+Alpha, RGB uniquement, Alpha uniquement** détermine l&#39;effet de paramétrage de la couleur uniquement.
  * **Couleur d&#39;arrière-plan** : *(Valeur Niveaux de gris) / (Valeur de couleur)*Définit la couleur d&#39;arrière-plan unie.
  * **Mode de fusion** : *Ajouter/Sub, Max /* Ajouter/Sub, Fusion Alpha (Couleur)**définit le mode de fusion des mosaïques sur l’arrière-plan.
* **Masquer**
  * **Aléatoire** :*0.0 - 1.0* Commence de manière aléatoire à masquer les vignettes. Plus la valeur est élevée, plus les carreaux disparaissent.
  * **Inverser** : *Faux/Vrai*\
    Inverse le résultat du masque.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
