---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Utilisez le nœud Circulaire à éclaboussures pour effectuer une dispersion de formes circulaires entre les textures afin de créer des motifs organiques et aléatoires.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Éclaboussure circulaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 8%

---


# Éclaboussure circulaire

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Splatter Circular génère un motif en anneau avec différentes commandes. Il peut utiliser des formes prédéfinies ou des entrées personnalisées. Il est similaire à [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mais avec un placement circulaire au lieu d&#39;une grille.

Cette option est utile lorsque vous souhaitez placer des formes de manière circulaire avec diverses options de randomisation.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

Les deux entrées sont facultatives.

|  |  |
|:---|:---|
| <b>Entrée d’image de motif 1-6</b> <i>Entrée niveaux de gris (entrée couleur)</i> | Splatter Circular uniquement : image de motif personnalisé, utilisée lorsque le paramètre « Pattern » est défini sur « Image Input ». |
| <b>Arrière-plan</b> <i>Entrée niveaux de gris (entrée couleur)</i> |  |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité du motif</b> <i>1 - 64</i> | Quantité de carreaux de motif à placer sur un anneau. |
| <b>Quantité aléatoire du motif</b> <i>0.0 - 1.0</i> | Randomisation de la quantité de motifs à placer. À utiliser de préférence avec une quantité d’anneau supérieure à 1. |
| <b>Quantité aléatoire de motif min</b> <i>1 - 10</i> | Définit la quantité minimale de motifs pour la randomisation. |
| <b>Quantité De Sonnerie</b> <i>1 - 10</i> | Définit le nombre d&#39;anneaux à remplir. Les anneaux sont toujours placés à l&#39;intérieur de l&#39;anneau extérieur, et l&#39;espace uniformément. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |
| <b>Motif</b> |  |
| <b>Motif</b> <i>Entrée d&#39;image, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Graduation, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône</i> | Sélectionne la forme de motif à utiliser. |
| <b>Numéro d&#39;entrée de motif</b> <i>1 - 6</i> | Définit le nombre d’entrées Image différentes à utiliser. Disponible uniquement lorsque l&#39;option <i>Entrée d&#39;image</i> est sélectionnée ci-dessus. |
| <b>Distribution d&#39;entrée de motif</b> <i>Aléatoire, Par Numéro De Motif, Par Numéro D&#39;Anneau</i> | Définit le mode de sélection des entrées de motif multiples. Aléatoire signifie qu’un anneau aléatoire est choisi, Numéro de motif signifie qu’ils sont simplement placés dans une séquence en boucle, Par numéros d’anneau signifie que chaque anneau a un différent dans l’ordre. |
| <b>Filtrage d&#39;entrée d&#39;image</b> <i>Bilinéaire + Mipmaps, Bilinéaire, Nearest</i> |  |
| <b>Spécifique Au Motif</b> <i>0.0 - 1.0</i> | Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné. |
| <b>Symétrie aléatoire</b> <i>0.0 - 1.0</i> | Définit le nombre de vignettes qui doivent être retournées/mises en miroir de manière aléatoire en fonction du comportement ci-dessous. |
| <b>Mode aléatoire de Symétrie</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Détermine le comportement de mise en miroir des symétries. |
| <b>Position</b> |  |
| <b>Rayon</b> <i>0.0 - 1.0</i> | Définit le rayon à partir du centre auquel les motifs sont placés. |
| <b>Rayon aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire le rayon de chaque carreau de motif. |
| <b>Multiplicateur de rayon en anneau</b> <i>0.0 - 1.0</i> | Affecte l&#39;espacement de plusieurs anneaux. |
| <b>Angle aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire l’angle de chaque motif. Plus les montants sont élevés, plus la rotation est importante. |
| <b>Facteur de spirale</b> <i>0.0 - 1.0</i> | Transforme les anneaux en spirales, où chaque carreau est placé à un rayon légèrement croissant. |
| <b>Répartition</b> <i>0.0 - 2.0</i> | Définit le nombre de tours effectués par un anneau. Cela peut être augmenté au-delà de ses limites. |
| <b>Décalage dans la direction</b> <i>0.0 - 1.0</i> | Éloigne chaque motif du centre selon son angle. L’effet dépend en grande partie de l’option Angle aléatoire ou ressemble simplement à un multiplicateur pour le rayon. |
| <b>Décalage global</b> <i>0.0 - 1.0</i> | Translate la forme entière. |
| <b>Taille</b> |  |
| <b>Connecter les motifs</b> <i>Faux/Vrai</i> | Rend la longueur des éléments de motif dépendante du rayon, ce qui signifie que chaque forme doit toucher la précédente et la suivante. |
| <b>Taille (Connectée)</b> <i>0.0 - 1.0</i> | Modifie la taille globale de chaque motif. Une fois connecté, il est relatif au rayon total. |
| <b>Taille aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire la taille de chaque motif individuellement. |
| <b>Échelle</b> <i>0.0 - 2.0</i> | Redimensionne uniformément chaque motif. |
| <b>Échelle aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire la mise à l’échelle uniforme. |
| <b>Mise à l&#39;échelle par numéro de motif</b> <i>0.0 - 1.0</i> | Rend l’échelle du motif dépendante de la position sur l’anneau. |
| <b>Inverser le numéro de motif</b> <i>Faux/Vrai</i> | Utilisée avec l’option précédente, cette option permet d’inverser la mise à l’échelle de petite à grande et vice versa. |
| <b>Mise à l&#39;échelle par numéro d&#39;anneau</b> <i>0.0 - 1.0</i> | Rend l&#39;échelle dépendante du nombre d&#39;anneaux. |
| <b>Inverser la sonnerie</b> <i>Faux/Vrai</i> | Utilisée avec l’option précédente, elle permet d’inverser la mise à l’échelle de petite à grande et vice versa. |
| <b>Rotation</b> |  |
| <b>Rotation du motif</b> <i>0.0 - 1.0</i> | Fait pivoter tous les motifs de manière uniforme. |
| <b>Rotation aléatoire du motif</b> <i>0.0 - 1.0</i> | Rend aléatoire la rotation du motif. |
| <b>Pivot de rotation du motif</b> <i>Centre, Min X, Max X, Min Y, Max Y</i> | Définit la position du point pivot autour duquel faire pivoter chaque motif individuellement. |
| <b>Centrer l&#39;orientation</b> <i>Faux/Vrai</i> | Fait pivoter chaque motif de sorte qu’il soit orienté vers le centre de l’anneau. La désactiver leur donne la même orientation, ce qui peut produire des effets indésirables avec Décalage dans la direction. |
| <b>Rotation en anneau</b> <i>0.0 - 1.0</i> | Fait pivoter l’anneau entier autour du centre. |
| <b>Rotation Aléatoire De L&#39;Anneau</b> <i>0.0 - 1.0</i> | Rend aléatoire la rotation par anneau. |
| <b>Décalage de rotation de l&#39;anneau</b> <i>0.0 - 1.0</i> | Décale la rotation par anneau. |
| <b>Couleur</b> |  |
| <b>Couleur</b> <i>(valeur Niveaux de gris)</i> | Couleur à multiplier avec le motif sélectionné. |
| <b>Luminance aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire la couleur ou la Luminance de chaque mosaïque de motif. |
| <b>Luminance Par Échelle</b> <i>0.0 - 1.0</i> | Rend la Luminance dépendante de l’échelle du motif individuel. |
| <b>Luminance par numéro de motif</b> <i>0.0 - 1.0</i> | Rend la Luminance dépendante de la séquence de motif. Peut par exemple être utilisé avec des spirales. |
| <b>Inverser le numéro de motif</b> <i>Faux/Vrai</i> | Inverse l’option précédente. |
| <b>Luminance par sonnerie</b> <i>0.0 - 1.0</i> | Rend la Luminance dépendante de la séquence d&#39;anneau. |
| <b>Inverser la sonnerie</b> <i>Faux/Vrai</i> | Inverse l’option précédente. |
| <b>Masque Aléatoire</b> <i>0.0 - 1.0</i> | Masque les motifs de manière aléatoire. |
| <b>Couleur d&#39;arrière-plan</b> <i>(valeur Niveaux de gris)</i> | Modifie la couleur d’arrière-plan unie. |
| <b>Mode de fusion</b> <i>Ajouter, Max, Ajouter Sub</i> | Définit le mode de fusion des motifs qui se chevauchent. |
| <b>Opacité globale</b> <i>0.0 - 1.0</i> | Définit l’opacité globale de l’ensemble du résultat. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/circularsplatter-ex.png" />
        </td>
    </tr>
</table>
