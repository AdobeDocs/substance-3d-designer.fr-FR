---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Utilisez le nœud Dispersion de forme pour dispersion des formes entre les textures afin de créer des motifs et des détails procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure de forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# Éclaboussure de forme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Nœud très complexe, conçu pour être utilisé avec les nœuds associés [Fusion d&#39;éclaboussures de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Éclaboussures de forme à masquer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) et [Extraction de données d&#39;éclaboussures de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Utilisé pour éclabousser des formes de la même manière que dans [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mais avec un processus dynamique et non destructif qui permet de contrôler chaque étape, via un système multiniveau similaire à [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). Alors que Flood Fill utilise une map d&#39;entrée de base provenant d&#39;une source externe, Shape Splatter génère la carte et les données qui en découlent en une seule étape, comme une version plus avancée de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Son objectif principal est de permettre le placement de formes sur et pilotées par une map height et de générer ensuite diverses cartes à partir des données de projection. Par exemple, placer des rochers, des brindilles et des feuilles sur un paysage, orienté et conduit par diverses cartes. Différentes cartes peuvent ensuite être utilisées pour l’height, la normale, la couleur de base, la rugosité et tout autre canal, alors que toutes sont toujours basées sur les mêmes données d’éclaboussures partagées.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Height en arrière-plan</b> <i>Entrée en niveaux de gris</i> | Height d’arrière-plan pour placer des vignettes et piloter divers effets. |
| <b>Motif 1-8</b> <i>Entrée en niveaux de gris</i> | Motif facultatif |
| <b>Distribution des motifs</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris vers |
| <b>Échelle de forme</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris pour piloter la mise à l’échelle des carreaux. |
| <b>Rotation de forme</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris pour piloter la rotation des carreaux. |
| <b>Décalage Height</b> <i>Entrée en niveaux de gris</i> | Carte en niveaux de gris à utiliser comme décalage pour l’height de mosaïque. |
| <b>Échelle d&#39;Height</b> <i>Entrée en niveaux de gris</i> | Carte en niveaux de gris à utiliser comme décalage pour l’height de mosaïque. |
| <b>Masquer aléatoirement</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. |
| <b>Carte vectorielle</b> <i>Entrée couleur</i> | Image vectorielle des couleurs pour piloter le positionnement et la rotation des mosaïques. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>X Quantité</b> <i>1 - 64</i> | Quantité de répétitions X du motif. |
| <b>Quantité Y</b> <i>1 - 64</i> | Nombre de répétitions Y du motif. |
| <b>Motif</b> |  |
| <b>Numéro d&#39;entrée de motif</b> <i>1 - 8</i> | Définissez la quantité de motifs différents à utiliser. Déverrouille les nouveaux emplacements d&#39;entrée de motif. |
| <b>Mode de distribution des motifs</b> <i>Aléatoire, Index De Motif, Index De Ligne, Index De Colonne</i> | Définissez le mode de détermination du motif à utiliser. Aléatoire ou par motif, ligne ou colonne. |
| <b>Multiplicateur de carte de distribution de motif</b> <i>0.0 - 1.0</i> | Définissez l’influence de la carte de distribution facultative pour le placement des motifs. |
| <b>Rotation du motif</b> <i>0, 90, 180, 270</i> | Définir le paramètre prédéfini, rotation de 90 degrés des motifs. |
| <b>Rotation aléatoire du motif</b> <i>0.0 - 1.0</i> | Définissez la quantité de rotation aléatoire par paliers de 90 degrés pour les motifs. |
| <b>Taille</b> |  |
| <b>Échelle</b> <i>0.0 - 5.0</i> | Définissez l’échelle uniforme pour chaque carreau. |
| <b>Échelle aléatoire</b> <i>0.0 - 1.0</i> | Échelle uniforme aléatoire pour chaque carreau. |
| <b>Aucun Chevauchement D&#39;Échelle</b> <i>0.0 - 1.0</i> | Redimensionnez aléatoirement de manière uniforme, mais uniquement vers le bas, pour éviter le chevauchement des mosaïques. Ne doit pas être utilisé en conjonction avec les deux paramètres précédents. |
| <b>Multiplicateur de carte d&#39;échelle</b> <i>0.0 - 1.0</i> | Définir l&#39;influence de la carte d&#39;échelle. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Permet une mise à l’échelle non uniforme des carreaux. |
| <b>Rapport de taille de la Pente Bg</b> <i>0.0 - 1.0</i> | Utilise la pente de mappage d’arrière-plan (normale calculée) pour mettre les carreaux à l’échelle de manière non uniforme. Simule la déformation de perspective. |
| <b>Rapport Taille par quantité X/Y</b> <i>0.0 - 1.0</i> | Mise à l’échelle non uniforme pour compenser un rapport différent dans les valeurs X et Y. |
| <b>Position</b> |  |
| <b>Position aléatoire</b> <i>0.0 - 2.0</i> | Décalage aléatoire de la position pour chaque carreau. |
| <b>Distribution Aléatoire</b> <i>Gaussien, Uniforme</i> | Définit le calcul à utiliser pour le paramètre précédent. Ne fait pas une énorme différence, plus visible avec des nombres élevés. La méthode gaussienne tend à donner une répartition plus uniforme. |
| <b>Multiplicateur de mappage vectoriel</b> <i>0.0 - 1.0</i> | Influence de la map d&#39;entrée vectorielle sur les décalages. |
| <b>Décalage Horizontal</b> <i>-2.0 - 2.0</i> | Décalage horizontal global. |
| <b>Décalage vertical</b> <i>-2.0 - 2.0</i> | Décalage vertical global. |
| Option <b>Hors limites</b> <i>Mise À L&#39;Échelle De La Forme, Contrainte De Position</i> | Action à effectuer lorsqu’une vignette apparaîtrait hors limites. |
| <b>Rotation</b> |  |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter toutes les mosaïques de manière globale. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Permet une rotation aléatoire par mosaïque. |
| <b>Rotation à partir de la grande Pente</b> <i>0.0 - 1.0</i> | Utilise la pente de la carte d’arrière-plan (normale calculée) pour faire pivoter les carreaux. Peut être utilisé pour que les formes pointent vers le haut ou vers le bas sur des pentes. |
| <b>Multiplicateur de Map rotation</b> <i>0.0 - 1.0</i> | Fusions dans l’effet de Map rotation sur la rotation par mosaïque. |
| <b>Multiplicateur de mappage vectoriel</b> <i>0.0 - 1.0</i> | Fusions dans l’effet de Map rotation sur la rotation par mosaïque. |
| <b>Height</b> |  |
| <b>Ajustement automatique de l&#39;échelle de l&#39;Height</b> <i>Faux/Vrai</i> | Ajustez automatiquement la plage d’heights par rapport à l’arrière-plan, au lieu de définir une plage absolue. Permet un contrôle plus ou moins important. |
| <b>Décalage Height</b> <i>-1.0 - 1.0</i> | Modificateur permettant de décaler/déplacer toutes les mosaïques de manière uniforme dans la plage d’heights. |
| <b>Décalage Height aléatoire</b> <i>0.0 - 1.0</i> | Change le décalage d’height de manière aléatoire par carreau. |
| <b>Multiplicateur de mappage de décalage d&#39;Height</b> <i>0.0 - 1.0</i> | Modificateur pour définir l’influence de la courbe de décalage. |
| <b>Échelle d&#39;Height</b> <i>0.0 - 1.0</i> | Modificateur pour redimensionner/étendre uniformément toutes les mosaïques sur la plage d’heights. L’option Opposé à ce décalage écarte davantage les valeurs, comme le contraste. |
| <b>Échelle d&#39;Height aléatoire</b> <i>0.0 - 1.0</i> | Change l’échelle d’height de manière aléatoire par carreau. |
| <b>Multiplicateur de mappage d&#39;échelle d&#39;Height</b> <i>0.0 - 1.0</i> | Modificateur pour définir l’influence de la carte d’échelle. |
| <b>Se conformer à l&#39;arrière-plan</b> <i>0.0 - 1.0</i> | Affecte la fusion des carreaux avec l’arrière-plan. Aucune uniformisation signifie que les images en hauteur restent rigides, uniformisation signifie que la forme d’arrière-plan suit. Bon pour les feuilles par rapport aux bâtons par exemple. |
| <b>Arrière-Plan Conforme Lisse</b> <i>0.0 - 2.0</i> | Valeur de lissage pour l’effet précédent, afin d’éviter les variations incorrectes ou extrêmes. |
| <b>Inclinaison par rapport à la grande Pente</b> <i>0.0 - 1.0</i> | Ajustez l’height de la mosaïque de pente en fonction de la pente d’arrière-plan (normale calculée). |
| <b>Smoothness de Pente d&#39;arrière-plan</b> <i>0.0 - 2.0</i> | Valeur de lissage pour l’effet précédent, afin d’éviter les variations incorrectes ou extrêmes. |
| <b>Découpage Des Pixels Noirs</b> <i>Faux/Vrai</i> | Activez/désactivez cette option pour ignorer les pixels noirs complets (0) des formes de base des carreaux. |
| <b>Aplatir la base du motif</b> <i>Faux/Vrai</i> | Ajuste le comportement de fusion des carreaux avec l’arrière-plan : les carreaux intersecteront l’arrière-plan (False) ou remplaceront l’arrière-plan lorsqu’il sera plus bas. |
| <b>Masquage</b> |  |
| <b>Masquer aléatoirement</b> <i>0.0 - 1.0</i> | Masque les vignettes de manière aléatoire. Plus cette valeur est élevée, plus le nombre de carreaux disparaîtra. |
| <b>Multiplicateur de mappage aléatoire du masque</b> <i>0.0 - 1.0</i> | Seuil pour le mappage de masque lorsque vous commencez à masquer les vignettes. |
| <b>Masquer à partir de la grande Pente</b> <i>-1.0 - 1.0</i> | Utilise la pente de mappage d’arrière-plan (normale calculée) pour masquer les vignettes. |
