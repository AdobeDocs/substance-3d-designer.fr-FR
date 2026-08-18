---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Utilisez le nœud Sampler de mosaïque pour échantillonner et organiser les mosaïques à partir des textures d’entrée afin de créer des motifs en mosaïque dans Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaïque Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# Mosaïque Sampler

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## Mosaïque Sampler (couleur)

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Tile Sampler est le nœud de génération de motif de mosaïque ultime. Il s&#39;agit d&#39;une version évoluée et plus complexe de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). À partir de 2017 2.1, les différences sont beaucoup plus faibles entre Tile Sampler et [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Les principales différences se situent désormais uniquement dans les sept emplacements de mappage disponibles pour le pilotage de l&#39;échelle, de la position, de la rotation, de la taille, de la couleur et du masquage. Leur effet peut être fusionné séparément.

Tile Sampler est utile pour créer des modèles procéduraux artificiels, avec un contrôle supplémentaire sur certains paramètres pilotés par des cartes d&#39;entrée externes.

Familiarisez-vous avec le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) avant de passer à la vignette Sampler. Dans la plupart des cas, vous trouverez que le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) est suffisant et vous n&#39;aurez pas besoin de la complexité supplémentaire de Tile Sampler.

## Paramètres

### Entrées

* **Entrée de motif 1-6** : *Entrée niveaux de gris/Entrée couleur*\
  Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ».\
  La quantité d&#39;entrées disponibles est déterminée par le paramètre **Numéro d&#39;entrée de motif**.
* **Entrée de mappage d&#39;échelle** : *entrée en niveaux de gris* mappage en niveaux de gris pour gérer la mise à l&#39;échelle des mosaïques.
* **Entrée de mappage de Displacement** : *Entrée en niveaux de gris* Mappage en niveaux de gris pour générer le displacement des carreaux.
* **Entrée Map rotation** :*Entrée Niveaux De Gris*\
  Mappage en niveaux de gris pour piloter la rotation des carreaux.
* **Entrée de mappage vectoriel** : *Entrée de couleur*\
  Image vectorielle en couleurs pour une mise à l’échelle non uniforme.
* **Entrée de mappage des couleurs** :*Entrée en niveaux de gris/Entrée en couleurs* Mappage pour piloter la teinte par mosaïque.
* **Entrée de mappage de masque** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour masquer certaines mosaïques.
* **Entrée de mappage de distribution de motif** : *Entrée en niveaux de gris*\
  Emplacement de masque utilisé pour gérer plusieurs entrées de motif personnalisées.
* **Entrée d&#39;arrière-plan** : *Entrée en niveaux de gris/Entrée en couleurs* Image d&#39;arrière-plan facultative.

### Paramètres

* **X Amount** : *0 - 64*\
  Quantité de répétitions X du motif.
* **Quantité Y** : *0 - 64*\
  Quantité de répétitions Y du motif.
* **Extension non carrée** : *Faux/Vrai*\
  Permet la compensation de la courbure et de l’étirement avec des proportions non carrées.
* **Motif**
  * **Motif** :*Entrée de motif, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradation, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône*\
    Sélectionne la forme de motif à utiliser.
  * **Nombre d’entrées de motif** : *1 - 6* Nombre de motifs personnalisés parmi lesquels choisir aléatoirement.
  * **Distribution des entrées de motif** : *aléatoire, numéro de motif, carte de distribution* définit la façon dont plusieurs entrées de motif sont choisies. Aléatoire signifie qu’un élément aléatoire est choisi, Numéro de motif signifie qu’ils sont simplement placés dans une séquence en boucle. La carte de distribution utilise une entrée de carte en niveaux de gris pour piloter le placement.
  * **Filtrage d&#39;entrée de motif (moteur > v4)** : *Bilinéaire + Mipmaps, Bilinéaire, Au plus proche*
  * **Spécifique Au Motif** : *0.0 - 1.0*\
    Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné.
  * **Aléatoire spécifique au motif** : *0.0 - 1.0* L’effet de randomisation dépend du motif sélectionné.
  * **Rotation** :*0, 90, 180, 270* Rotation par paliers (90 degrés).
  * **Rotation aléatoire** : *0.0 - 1.0* Rotation libre aléatoire par carreau.
  * **Aléatoire de symétrie** : *0.0 - 1.0* Définit le nombre de carreaux qui doivent être retournés/mis en miroir de manière aléatoire selon le comportement ci-dessous.
  * **Mode aléatoire de symétrie** : *Horizontal + Vertical, Horizontal, Vertical* Détermine le comportement de mise en miroir de la symétrie.
* **Taille**
  * **Mode Taille** : *Normal, Conserver le rapport, Absolu, Pixel* Définit le comportement général de la taille du motif.\
    Normal vous permet de définir la taille des éléments de motif. Elle est affectée par les valeurs X et Y.\
    L’option Conserver le rapport vous permet de définir une taille affectée par les valeurs X et Y, mais le rapport X et Y entre les deux reste intact.\
    Absolue vous permet de définir une taille absolue qui n&#39;est pas affectée par les valeurs X et Y.\
    Pixel vous permet de définir une taille absolue en pixels, qui n’est pas affectée par les valeurs X et Y. La modification de la résolution affecte la taille des éléments.
  * **Taille (absolue/pixel)** : *0,0 - 1,0* modifie les proportions non uniformes des carreaux. Le comportement exact dépend du mode Taille.
  * **Taille aléatoire** :*0,0 - 1,0* aléatoire les proportions par carreau.
  * **Échelle** : *0.0 - 10.0* Définit l’échelle globale des vignettes.
  * **Échelle aléatoire** :*0.0 - 1.0* rend l’échelle aléatoire par carreau
  * **Multiplicateur de mise à l&#39;échelle** : *0.0 - 1.0* Fusions dans l&#39;effet de la carte d&#39;échelle.
  * **Multiplicateur de mappage vectoriel d&#39;échelle** : *0.0 - 1.0* Mélange l&#39;effet du mappage vectoriel d&#39;échelle pour générer une mise à l&#39;échelle non uniforme.
  * **Effet de paramétrage d&#39;échelle** : *X et Y, X, Y* définit les axes affectés par le paramétrage d&#39;échelle. Peut être utilisé pour que le mappage d’échelle affecte uniquement X ou Y des éléments.
* **Position**
  * **Position aléatoire** :*0.0 - 10.0* aléatoire la position des carreaux sur les deux axes.
  * **Décalage** : *0,0 - 1,0*\
    Décale les carreaux en fonction du type de décalage.
  * **Type de décalage** : *quincux horizontal, quincux vertical, global horizontal, global vertical* change la direction dans laquelle le décalage s’opère.
  * **Décalage global** : *0.0 - 1.0* Décale globalement toutes les mosaïques sur l’axe X ou Y.
  * **Intensité de la courbe de Displacement** : *0,0 - 1,0* Mélange de l&#39;intensité de la courbe de Displacement sur le décalage.
  * **Angle du Displacement** : *0.0 - 1.0* Définit l’angle selon lequel effectuer le déplacement.
  * **Displacement vectoriel** : *0.0 - 1.0* Utilise le mappage vectoriel pour déterminer le displacement et l’angle.
* **Rotation**
  * **Rotation** :*0.0 - 1.0* fait pivoter globalement toutes les mosaïques.
  * **Rotation aléatoire** : *0.0 - 1.0* Rotation aléatoire par carreau.
  * **Multiplicateur de Map rotation** : *0.0 - 1.0* Mélanges dans l’effet de Map rotation sur la rotation par carreau.
  * **Multiplicateur de mappage vectoriel** : *0.0 - 1.0* utilise le mappage vectoriel pour piloter la rotation par carreau.
* **Couleur**
  * **Seuil du mappage de masque** : *0.0 - 1.0* Seuil pour le mappage de masque lorsque vous commencez à masquer les vignettes.
  * **Inversion de la carte de masque** :*Faux/Vrai* inverse l&#39;effet de carte de masque.
  * **Technique d&#39;échantillonnage de carte de masque** : *Centre du motif, cadre de sélection du motif (plus lent)*Si le masquage doit être déterminé par un point unique ou par un cadre de sélection. Permet d’éviter que des pixels isolés ne provoquent des effets étranges.
  * **Masquage aléatoire** : *0.0 - 1.0* Le masquage aléatoire fonctionne parallèlement au mappage de masque.
  * **Inverser le masque** :*Faux/Vrai* inverse le masquage aléatoire.
  * **Mode de fusion** : *Mode de fusion Ajouter/Sub, Max (Mosaïque Sampler) /* Ajouter/Sub, Alpha Blend* (Mosaïque Sampler Color)*Mode de fusion pour les mosaïques sur l’arrière-plan et entre elles.
  * **Couleur** : *(Valeur Niveaux de gris) / (Valeur de couleur)*Couleur de mosaïque unie et globale.
  * **Aléatoire couleur/luminance** : *0.0 - 1.0* Aléatoire de couleur, par carreau.
  * **Mode De Paramétrage Des Couleurs** : *Entrée De Couleur, Échelle, Index De Ligne, Index De Ligne, Index De Motif (Mosaïque Sampler)*\
    */ *Table des couleurs, Échelle, Index de lignes, Index de lignes, Index de motifs, Position au centre du motif, Position au centre du motif (RG) Taille de la sphère (B) (Couleur Sampler de la mosaïque)**Définit le paramétrage exact de la randomisation des couleurs.
  * **Multiplicateur de paramétrage des couleurs** : *0.0 - 1.0* Mélanges dans l’effet de paramétrage ci-dessus.
  * **Effet de paramétrage des couleurs (couleur uniquement) :** **RGB+Alpha, RGB uniquement, Alpha uniquement** Définit la façon dont le paramétrage affecte les couleurs.
  * **Opacité globale (niveaux de gris uniquement)** : *0.0 - 1.0* définit l’opacité globale des carreaux.
  * **Couleur d&#39;arrière-plan** : *(Valeur Niveaux de gris) / (Valeur de couleur)*Définit la couleur d&#39;arrière-plan unie.
  * **Inverser l&#39;ordre de rendu** :*Faux/Vrai* Inverse l&#39;ordre de rendu pour passer de l&#39;arrière vers l&#39;avant.

## Exemples d’images

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*L&#39;exemple montre comment les paramètres sont pilotés par les cartes d&#39;entrée (distribution de motif, échelle, rotation).*

</td>
</tr>
</table>
