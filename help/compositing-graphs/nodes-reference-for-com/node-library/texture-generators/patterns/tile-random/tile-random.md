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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# Mosaïque aléatoire

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

<b>Entrée :</b> Générateurs > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Tile Random génère un motif de mosaïque procédural qui a un peu plus de chaos dans les formes de mosaïque que son homologue, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Pour ce faire, il scinde aléatoirement certains carreaux en carreaux plus petits. Nous vous conseillons de commencer par contourner le Tile Generator avant de vous attaquer à Tile Random, car de nombreux concepts sont similaires.

L&#39;option Mosaïque aléatoire est utilisée à la place de l&#39;option [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) lorsque l&#39;objectif est un motif plus ancien, moins organisé. Il a toutefois ses limites, alors envisagez de [juxtaposer Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) pour tout autre besoin avancé.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée de motif</b> <i>Entrée Niveaux De Gris (Entrée Couleur)</i> | Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ». |
| <b>Entrée en arrière-plan</b> <i>Entrée niveaux de gris (entrée couleur)</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>X Quantité</b> <i>1 - 64</i> | Quantité de répétitions X du motif. |
| <b>Quantité Y</b> <i>1 - 64</i> | Quantité de répétitions Y du motif. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Active la compensation de la courbure et de la étire avec des proportions non carrées. |
| <b>Motif</b> |  |
| <b>Motif</b> <i>Entrée de motif, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Graduation, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône</i> | Sélectionne la forme de motif à utiliser. |
| <b>Filtrage d’entrée d’image (Moteur > v4)</b> <i>Bilinéaire + Mipmaps, Bilinéaire, Nearest</i> |  |
| <b>Spécifique Au Motif</b> <i>0.0 - 1.0</i> | Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné. |
| <b>Aléatoire Spécifique Au Motif</b> <i>0.0 - 1.0</i> | L’effet de randomisation dépend du motif sélectionné. |
| <b>Rotation</b> <i>0, 90, 180, 270, horizontal aléatoire, vertical aléatoire</i> | Permet une rotation par incréments de 90 degrés, avec une randomisation facultative. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Ajoute une rotation libre aléatoire. |
| <b>Symétrie aléatoire</b> <i>0.0 - 1.0</i> | Applique une symétrie aléatoire à certains motifs selon le mode aléatoire de la Symétrie sélectionnée. Plus cette valeur est élevée, plus les motifs seront mis en miroir. |
| <b>Mode aléatoire de Symétrie</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Détermine le comportement de mise en miroir lorsque le nombre aléatoire de Symétries est supérieur à 0. |
| <b>Fractionner</b> |  |
| <b>Mode</b> <i>aucun, automatique, horizontal automatique, vertical automatique, aléatoire h+v</i> | Définit la règle de fractionnement des vignettes. |
| <b>Seuil</b> <i>0.0 - 1.0</i> | Seuil de taille pour le fractionnement d’une mosaïque. |
| <b>Multiplicateur</b> <i>0 - 10</i> | Multiplicateur de fractionnement. Plus cette valeur est élevée, plus le fractionnement est important. |
| <b>Taille</b> |  |
| <b>X aléatoire</b> <i>0.0 - 1.0</i> | Aléatoire la mise à l’échelle non uniforme sur l’axe X. |
| <b>Aléatoire Y</b> <i>0.0 - 1.0</i> | Répartit de manière aléatoire la mise à l’échelle non uniforme sur l’axe Y. |
| <b>Interstice</b> |  |
| <b>Mode</b> <i>Relative à la plus petite brique, relative à la plus grande brique</i> | Définit l’interstice de taille de brique relatif. |
| <b>Quantité</b> <i>0.0 - 1.0</i> | Définit la taille des espaces entre les briques. |
| <b>Forme</b> |  |
| <b>Échelle</b> <i>0.0 - 1.0</i> | Redimensionne globalement chaque carreau. |
| <b>Échelle aléatoire</b> <i>0.0 - 1.0</i> | Mise à l’échelle aléatoire par mosaïque. |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Rotation globale pour chaque carreau. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Permet une rotation aléatoire par carreau. |
| <b>Contrainte de rotation</b> <i>Faux/Vrai</i> | Contraint l’échelle afin que les carreaux pivotés ne se chevauchent jamais. |
| <b>Position</b> |  |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Déplace ou translate les carreaux globalement, en les faisant glisser uniquement sur l’axe X |
| <b>Décalage aléatoire</b> <i>0.0 - 1.0</i> | Décalage aléatoire par carreau, diapositives sur l’axe X uniquement |
| <b>Aléatoire</b> <i>0.0 - 1.0</i> | Aléatoire de la position, les carreaux se déplacent sur les axes X et Y. |
| <b>Contraintes aléatoires</b> <i>Faux/Vrai</i> | Réduit l’échelle pour que les mosaïques se touchent, sans se chevaucher. Atténue considérablement l’effet Position aléatoire. |
| <b>Couleur</b> |  |
| <b>Couleur</b> <i>(Valeur Niveaux de gris) / (Valeur de couleur)</i> | Définit une couleur unie pour toutes les mosaïques. |
| <b>Color Random</b> <i>0.0 - 1.0</i> | Rend les couleurs aléatoires par mosaïque. |
| <b>Paramétrage Des Couleurs</b> <i>aucune, zone, taille x, taille y</i> | Rend la variation de couleur dépendante de l’un de ces paramètres. |
| <b>Intensité de paramétrage des couleurs</b> <i>0.0 - 1.0</i> | Multiplicateur pour l’effet Paramétrage ci-dessus. |
| <b>Effet de paramétrage des couleurs (pour la couleur uniquement)</b> <i>RGB+Alpha, RGB uniquement, Alpha uniquement</i> | Détermine l’effet de paramétrage de la couleur uniquement. |
| <b>Couleur d&#39;arrière-plan</b> <i>(Valeur Niveaux de gris) / (Valeur de couleur)</i> | Définit la couleur d’arrière-plan unie. |
| <b>Mode de fusion</b> <i>Ajouter/Sub, Max / Ajouter/Sub, Fusion Alpha (Couleur)</i> | Définit le mode de fusion des carreaux sur l’arrière-plan. |
| <b>Masquer</b> |  |
| <b>Aléatoire</b> <i>0.0 - 1.0</i> | Début aléatoire du masquage des vignettes. Plus la valeur est élevée, plus les carreaux disparaissent. |
| <b>Inverser</b> <i>Faux/Vrai</i> | Inverse le résultat du masque. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tile-random-1.png" />
        </td>
    </tr>
</table>
