---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Utilisez le nœud Shape Splatter pour dispersion des formes entre les textures afin de créer des motifs et des détails procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure de forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# Éclaboussure de forme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## Éclaboussure de forme

**Entrée :** *Générateurs de textures**/Motifs*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Nœud très complexe, conçu pour être utilisé avec les nœuds associés [Fusion d&#39;éclaboussures de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Éclaboussures de forme à masquer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) et [Extraction de données d&#39;éclaboussures de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Utilisé pour éclabousser des formes de la même manière que dans [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mais avec un processus dynamique et non destructif qui permet de contrôler chaque étape, via un système multiniveau similaire à [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Alors que Flood Fill utilise un mappage d&#39;entrée de base à partir d&#39;une source externe, Shape Splatter génère le mappage et les données qui en découlent en une seule étape, comme une version plus avancée de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Son objectif principal est de permettre le placement de formes sur et pilotées par une carte d’height, puis de générer diverses cartes à partir des données de projection. Par exemple, placer des rochers, des brindilles et des feuilles sur un paysage, orienté et conduit par diverses cartes. Différentes cartes peuvent ensuite être utilisées pour l’height, la normale, la couleur de base, la rugosité et tout autre canal, alors que toutes sont toujours basées sur les mêmes données d’éclaboussures partagées.

## Paramètres

### Entrées

* **Height de l&#39;arrière-plan** :*height de l&#39;entrée en niveaux de gris* pour placer des carreaux sur divers effets et les piloter.
* **Motif 1-8** : *Motif en niveaux de gris**facultatif*
* **Distribution des motifs** : *entrée en niveaux de gris* mappage en niveaux de gris à
* **Échelle de forme** : *entrée en niveaux de gris* carte en niveaux de gris pour piloter la mise à l&#39;échelle des carreaux.
* **Rotation de forme** : *entrée en niveaux de gris* mappage en niveaux de gris pour piloter la rotation des carreaux.
* **Décalage de l&#39;Height** : *Mappage en niveaux de gris*&#x200B;à utiliser comme décalage pour l&#39;height de la mosaïque.
* **Échelle de l&#39;Height** : *Grayscale Input* Grayscale map à utiliser comme décalage pour l&#39;height de la mosaïque.
* **Masquage Aléatoire** :*Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud.
* **Carte vectorielle** : *entrée de couleur* carte vectorielle de couleur pour piloter le positionnement et la rotation des mosaïques.

### Paramètres

* **X Quantité** : *1 - 64*\
  Quantité de répétitions X du motif.
* **Quantité Y** : *1 - 64*\
  Nombre de répétitions Y du motif.
* **Motif**
  * **Numéro d’entrée du motif** : *1 - 8* Définissez la quantité de motifs différents à utiliser. Déverrouille les nouveaux emplacements d&#39;entrée de motif.
  * **Mode de distribution de motif** : *Aléatoire, Index de motif, Index de ligne, Index de colonne* Définissez comment déterminer le motif à utiliser. Aléatoire ou par motif, ligne ou colonne.
  * **Multiplicateur de carte de distribution de motif** : *0.0 - 1.0* Définissez l’influence de la carte de distribution facultative pour le placement des motifs.
  * **Rotation du motif** :*0, 90, 180, 270* Définir le paramètre prédéfini, rotation de 90 degrés des motifs.
  * **Rotation aléatoire du motif** : *0,0 - 1,0* Définissez la quantité de rotation aléatoire par paliers de 90 degrés pour les motifs.
* **Taille**
  * **Échelle** : *0.0 - 5.0*\
    Définissez l’échelle uniforme pour chaque carreau.
  * **Échelle aléatoire** :*0,0 - 1,0* aléatoire l’échelle uniforme pour chaque carreau.
  * **Pas de chevauchement d&#39;échelle** :*0.0 - 1.0* Redimensionner aléatoirement de manière uniforme, mais uniquement vers le bas, pour éviter le chevauchement des éléments. Ne doit pas être utilisé en conjonction avec les deux paramètres précédents.
  * **Multiplicateur de carte d&#39;échelle** : *0.0 - 1.0* Définir l&#39;influence de la carte d&#39;échelle.
  * **Taille** :*0.0 - 1.0* Permet une mise à l’échelle non uniforme des carreaux.
  * **Rapport de taille de la Pente Bg** : *0,0 - 1,0* utilise la pente de mappage d’arrière-plan (normale calculée) pour mettre les carreaux à l’échelle de manière non uniforme. Simule la déformation de perspective.
  * **Rapport Taille par quantité X/Y** : *mise à l’échelle non uniforme 0,0 - 1,0* pour compenser un rapport différent dans les quantités X et Y.
* **Position**
  * **Position aléatoire** :*0.0 - 2.0* position de décalage aléatoire pour chaque carreau.
  * **Distribution aléatoire** : *gaussien, uniforme* définit le calcul à utiliser pour le paramètre précédent. Ne fait pas une énorme différence, plus visible avec des nombres élevés. La méthode gaussienne tend à donner une répartition plus uniforme.
  * **Multiplicateur de carte vectorielle** : *0.0 - 1.0* Influence de la carte d’entrée vectorielle sur les décalages.
  * **Décalage horizontal** : *-2.0 - 2.0* Décalage horizontal global.
  * **Décalage vertical** : *-2.0 - 2.0* Décalage vertical global.
  * **Option hors limites** : *Mise à l’échelle de la forme, contraindre la position* Action à effectuer lorsqu’un carreau semble hors limites.
* **Rotation**
  * **Rotation** :*0.0 - 1.0* fait pivoter globalement toutes les mosaïques.
  * **Rotation aléatoire** : *0.0 - 1.0* Rotation aléatoire par carreau.
  * **Rotation à partir de la Pente Bg** : *0.0 - 1.0* utilise la pente de la carte d&#39;arrière-plan (normale calculée) pour faire pivoter les carreaux. Peut être utilisé pour que les formes pointent vers le haut ou vers le bas sur des pentes.
  * **Multiplicateur de Map rotation** : *0.0 - 1.0* Mélanges dans l’effet de Map rotation sur la rotation par carreau.
  * **Multiplicateur de carte vectorielle** : *0.0 - 1.0* Mélanges dans l’effet de Map rotation sur la rotation par carreau.
* **Height**
  * **Réglage automatique de l&#39;échelle d&#39;Height** : *Faux/Vrai* Ajustez automatiquement la plage d&#39;heights par rapport à l&#39;arrière-plan, au lieu de définir une plage absolue. Permet un contrôle plus ou moins important.
  * **Décalage de l’Height** : *-1.0 - 1.0* Modificateur pour décaler/déplacer toutes les mosaïques de manière uniforme dans la plage d’heights.
  * **Décalage aléatoire de l&#39;Height** :*0,0 - 1,0* Le décalage aléatoire de l&#39;height est modifié par carreau.
  * **Multiplicateur de carte de décalage d&#39;Height** : *0.0 - 1.0* Modificateur pour définir l&#39;influence de la carte de décalage.
  * **Échelle de l’Height** : *0.0 - 1.0* Modifiez pour mettre à l’échelle/étendre toutes les mosaïques de manière uniforme sur la plage d’heights. L’option Opposé à ce décalage écarte davantage les valeurs, comme le contraste.
  * **Échelle d&#39;Height aléatoire** :*0,0 - 1,0* change l&#39;échelle d&#39;height de manière aléatoire par carreau.
  * **Multiplicateur de carte d&#39;échelle d&#39;Height** : *0.0 - 1.0* Modificateur pour définir l&#39;influence de la carte d&#39;échelle.
  * **Se conformer à l’arrière-plan** :*0.0 - 1.0* affecte la fusion des carreaux avec l’arrière-plan. Aucune uniformisation signifie que les images en hauteur restent rigides, uniformisation signifie que la forme d’arrière-plan suit. Bon pour les feuilles par rapport aux bâtons par exemple.
  * **Arrière-plan lissé conforme** : *0.0 - 2.0* valeur de lissage pour l’effet précédent, afin d’éviter des variations incorrectes ou extrêmes.
  * **Inclinaison par rapport à la Pente de l’arrière-plan** : *0,0 - 1,0* L’height des carreaux de réglage/pente dépend de la pente de l’arrière-plan (normale calculée).
  * **Smoothness de Pente d&#39;arrière-plan** : *0.0 - 2.0* valeur de lissage pour l&#39;effet précédent, pour éviter les variations incorrectes ou extrêmes.
  * **Découpage des pixels noirs** :*faux/vrai* basculez pour ignorer le noir complet (0) pixels des formes de base des carreaux.
  * **Aplatir la base du motif** : *Faux/Vrai* ajuste le comportement de fusion des carreaux avec l’arrière-plan : les carreaux intersecteront l’arrière-plan (Faux) ou remplaceront l’arrière-plan lorsqu’il sera plus bas.
* **Masquage**
  * **Aléatoire du masque** :*0.0 - 1.0* Masque aléatoirement les vignettes. Plus cette valeur est élevée, plus le nombre de carreaux disparaîtra.
  * **Multiplicateur de mappage aléatoire de masque** : *0.0 - 1.0* Seuil pour le mappage de masque lorsque vous commencez à masquer les vignettes.
  * **Masquer à partir de la Pente principale** : *-1.0 - 1.0* Utilise la pente de mappage d&#39;arrière-plan (normale calculée) pour masquer les vignettes.

## Exemples d’images

</td>
</tr>
</table>
