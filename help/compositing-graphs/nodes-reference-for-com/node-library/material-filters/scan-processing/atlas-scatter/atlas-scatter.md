---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Utilisez le nœud Atlas scatter pour dispersion des textures dans un atlas afin de créer des motifs en mosaïque à partir de matériaux numérisés.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter.png){width="200px"}

<b>Entrée :</b> Filtres de matériau > Traitement des numérisations

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Extrayez des éléments d’un atlas et placez-les en dispersion sur un arrière-plan. Les entrées Atlas sont des matériaux complets, composés d&#39;éléments individuels disposés et emballés sur une seule feuille de texture. Ce nœud les divise (à l&#39;aide d&#39;un processus interne d&#39;[Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)) et les dispersion, comme dans le cas de la [dispersion de forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). L’Atlas scatter nécessite au minimum une entrée de mappage d’opacité et une entrée de mappage d’Height pour que l’Atlas fonctionne.

</td>
</tr>
</table>

>[!NOTE]
>
> Des centaines de [atlas](https://source.substance3d.com/allassets?assetType=substanceAtlas), prêts à être utilisés dans le nœud d&#39;Atlas scatter, sont disponibles sur [Substance Source](https://source.substance3d.com/).

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Résolution d&#39;entrée Atlas</b> <i>Résolution, de 1 à 12</i> | Définissez manuellement la résolution de l’atlas d’entrée complet, pour garantir un bon rapport performances/qualité. |
| <b>X Quantité</b> <i>1 - 64</i> | Quantité de répétitions X du motif. |
| <b>Quantité Y</b> <i>1 - 64</i> | Nombre de répétitions Y du motif. |
| <b>Motif</b> |  |
| <b>Plage de motifs</b> <i>0 - 10</i> | Définit la plage de motifs à diffuser. Si cette option est définie sur 0, tous les motifs seront utilisés. |
| <b>Mode de distribution des motifs</b> <i>Aléatoire, Index De Motif, Index De Ligne, Index De Colonne</i> | Définit l’ordre dans lequel les éléments atlas sont utilisés. |
| <b>Multiplicateur de carte de distribution de motif</b> <i>0.0 - 1.0</i> | Sélectionnez le motif de forme en fonction de la valeur de niveaux de gris de l’image d’entrée. |
| <b>Rotation du motif</b> <i>0, 90, 180, 270</i> | Applique une rotation fixe à chaque élément de l’atlas, selon la valeur de degrés sélectionnée. |
| <b>Rotation aléatoire du motif</b> <i>0.0 - 1.0</i> | Applique une rotation aléatoire à la partie définie des éléments de l’atlas. |
| <b>Précision de la détection de forme Atlas</b> <i>Formes simples ou petites, formes complexes ou grandes, aucun mode d&#39;échec</i> | Définit la précision de détection des formes. Plus la précision est grande, plus l’impact sur les performances est important. |
| <b>Réduire l’opacité de l’atlas (détection plus rapide)</b> <i>-4 - 0</i> | Permet de contrôler le taux de réduction de l’opacité de la carte d’atlas d’entrée, qui est utilisée pour la détection de forme. Une résolution inférieure améliore les performances au détriment de la précision. |
| <b>Ignorer la forme inférieure à</b> <i>0.0 - 1.0</i> | Définit la taille minimale qu’une forme doit être détectée, exprimée en tant que rapport de l’image globale |
| <b>Taille</b> |  |
| <b>Échelle</b> <i>0.0 - 5.0</i> | Définit l’échelle relative des formes dispersées. |
| <b>Échelle aléatoire</b> <i>0.0 - 1.0</i> | Définit le multiplicateur pour appliquer une mise à l’échelle aléatoire à chaque forme diffusée. |
| <b>Aucun Chevauchement D&#39;Échelle</b> <i>0.0 - 1.0</i> | Réduit l’échelle de la forme afin qu’elles ne se chevauchent pas. |
| <b>Multiplicateur de carte d&#39;échelle</b> <i>0.0 - 1.0</i> | Multiplie l’échelle de la forme en fonction de la valeur de niveaux de gris de l’image d’entrée. |
| <b>Taille</b> <i>0.0 - 1.0</i> | Définit l’échelle relative des formes dispersées en fonction de leur longueur (X) et de leur largeur (Y). |
| <b>Rapport de taille de la Pente Bg</b> <i>0.0 - 1.0</i> | Modifie le rapport de taille de la forme en fonction de la pente d’height de l’arrière-plan. |
| <b>Conserver le rapport de grandeur</b> <i>0.0 - 1.0</i> | Détermine le degré de conservation des proportions d’origine des formes dispersées, au lieu d’utiliser le rapport des cellules de la grille, c’est-à-dire le rapport des valeurs Quantité X et Quantité Y. |
| <b>Position</b> |  |
| <b>Position aléatoire</b> <i>0.0 - 2.0</i> | Multiplicateur permettant de déplacer chaque forme dans une direction aléatoire à partir de leur point de départ de grille. |
| <b>Distribution Aléatoire</b> <i>Gaussien, Uniforme</i> | Bascule d&#39;une distribution gaussienne à une distribution uniforme pour la position aléatoire. La distribution gaussienne produira un résultat plus organique par rapport à la distribution Uniforme. |
| <b>Multiplicateur de mappage vectoriel</b> <i>0.0 - 1.0</i> | Contrôle l’influence de l’entrée de la carte vectorielle pour déplacer les formes dans la direction du vecteur spécifié par les canaux rouge (X) et vert (Y) de la carte. |
| <b>Décalage Horizontal</b> <i>-2.0 - 2.0</i> | Multiplicateur de décalage le long de l’axe X. |
| <b>Décalage vertical</b> <i>-2.0 - 2.0</i> | Multiplicateur pour le décalage de position le long de l’axe Y. |
| Option <b>Hors limites</b> <i>Mise À L&#39;Échelle De La Forme, Contrainte De Position</i> | En raison de la nature technique de la tache, les formes ne peuvent pas être dessinées à plus de 2 cellules de la taille de leur position d&#39;origine. Si une forme devient trop grande ou est déplacée trop loin, vous avez deux options : - L’option Mise à l’échelle réduit la taille de la forme lorsqu’elle atteint un cadre - L’option Conserver la position déplace la forme vers sa position d’origine |
| <b>Rotation</b> |  |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Permet de contrôler la rotation locale de toutes les formes. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Multiplicateur pour une valeur aléatoire de rotation appliquée par forme. |
| <b>Rotation à partir de la grande Pente</b> <i>0.0 - 1.0</i> | Modifie la rotation de la forme en fonction de la pente d’height de l’arrière-plan. Généralement utilisé en combinaison avec le paramètre « Size Ratio from Bg Pente » |
| <b>Multiplicateur de Map rotation</b> <i>0.0 - 1.0</i> | Multiplie la rotation de la forme en fonction de la valeur de niveaux de gris de l’image entrée. |
| <b>Multiplicateur de mappage vectoriel</b> <i>0.0 - 1.0</i> | Définit la rotation de la forme en fonction de l’entrée d’image vectorielle. |
| <b>Height</b> |  |
| <b>Ajustement automatique de l&#39;échelle de l&#39;Height</b> <i>Faux/Vrai</i> | Ajustez automatiquement l’height en fonction de l’échelle du motif pour conserver un height de forme proportionnel à l’height d’arrière-plan. |
| <b>Mode de fusion</b> <i>Fusion D&#39;Height, Test D&#39;Alpha</i> | Définit la méthode de résolution des chevauchements de formes. |
| <b>Décalage Height</b> <i>-1.0 - 1.0</i> | Applique un décalage global à l’height des formes |
| <b>Décalage Height aléatoire</b> <i>0.0 - 1.0</i> | Multiplicateur d’un décalage d’height aléatoire appliqué par forme |
| <b>Multiplicateur de mappage de décalage d&#39;Height</b> <i>0.0 - 1.0</i> | Multiplie le décalage de l’height de la forme en fonction de la valeur de niveaux de gris de l’image d’entrée. |
| <b>Échelle d&#39;Height</b> <i>0.0 - 1.0</i> | Permet de contrôler l’échelle d’height globale des formes dispersées |
| <b>Échelle d&#39;Height aléatoire</b> <i>0.0 - 1.0</i> | Application d’un multiplicateur pour une échelle d’height aléatoire par forme |
| <b>Multiplicateur de mappage d&#39;échelle d&#39;Height</b> <i>0.0 - 1.0</i> | Multiplie l’échelle d’height de la forme en fonction de la valeur de niveaux de gris de l’image d’entrée. |
| <b>Se conformer à l&#39;arrière-plan</b> <i>0.0 - 1.0</i> | À 0, l’height de forme reste intact, à 1, l’height de forme sera déformé par l’arrière-plan de l’height sous-jacent. |
| <b>Arrière-Plan Conforme Lisse</b> <i>0.0 - 2.0</i> | Permet de contrôler le degré de lissage appliqué à la déformation d’height de la forme lorsqu’elle est uniformisée à son arrière-plan. |
| <b>Inclinaison par rapport à la grande Pente</b> <i>0.0 - 1.0</i> | Déforme l’height de forme en fonction de la pente locale de l’height d’arrière-plan : un dégradé linéaire correspondant à la pente d’arrière-plan est ajouté à l’height de forme. |
| <b>Smoothness de Pente d&#39;arrière-plan</b> <i>0.0 - 2.0</i> | Contrôle le degré de lissage appliqué à la pente d’arrière-plan lorsque la forme est inclinée en fonction de cette pente. |
| <b>Découpage Des Pixels Noirs</b> <i>Faux/Vrai</i> | Ignore la valeur de noir des entrées de motif. |
| <b>Aplatir la base du motif</b> <i>Faux/Vrai</i> | Permet d’aplatir l’height d’arrière-plan sous une forme pour qu’il corresponde à l’height de départ. |
| <b>Masquage</b> |  |
| <b>Masquer aléatoirement</b> <i>0.0 - 1.0</i> | Masque un nombre aléatoire de formes, exprimé sous la forme d’un rapport de la quantité totale. |
| <b>Multiplicateur de mappage aléatoire du masque</b> <i>0.0 - 1.0</i> | Définit le masquage de forme aléatoire en fonction de l’entrée d’image en niveaux de gris. |
| <b>Masquer à partir de la grande Pente</b> <i>-1.0 - 1.0</i> | Contrôle le masquage des formes en fonction de la pente de l’arrière-plan à leur emplacement. |
| <b>Couleur</b> |  |
| <b>Réglage Des Couleurs</b> <i>-1.0 - 1.0</i> | Permet d’ajuster globalement les couleurs des éléments dispersés. |
| <b>Color Random</b> <i>0.0 - 1.0</i> | Multiplicateur permettant de modifier les valeurs chromatiques de façon aléatoire par forme. |
| <b>Couleur d&#39;arrière-plan</b> <i>0.0 - 1.0</i> | Décale les couleurs de la forme en fonction de la couleur d’arrière-plan à leur emplacement. |
| <b>Normal</b> |  |
| <b>Inclinaison par rapport à la grande Pente</b> <i>0.0 - 1.0</i> | Inclinez la forme normalement en fonction de la normale de l’arrière-plan. |
| <b>Aléatoire normal</b> <i>0.0 - 1.0</i> | Multiplicateur permettant d’incliner la normale d’une valeur aléatoire par forme. |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Basculer entre différents Formats de map normaux (inverse la couche verte) |
| <b>Rugosité</b> |  |
| <b>Réglage De La Rugosité</b> <i>-1.0 - 1.0</i> | Permet de décaler la rugosité de forme globale. |
| <b>Rugosité à partir de l&#39;arrière-plan</b> <i>0.0 - 1.0</i> | Déplace la rugosité des formes vers la rugosité d’arrière-plan à leur emplacement. |
| <b>Rugosité aléatoire</b> <i>0.0 - 1.0</i> | Multiplicateur permettant de décaler la rugosité d’une valeur aléatoire par forme. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-11.png" />
        </td>
    </tr>
</table>
