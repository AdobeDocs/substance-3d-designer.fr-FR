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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# Mosaïque Sampler

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

<b>Entrée :</b> Générateurs de textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Tile Sampler est le nœud de génération de motif de mosaïque ultime. Il s&#39;agit d&#39;une version évoluée et plus complexe de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). À partir de 2017 2.1, les différences sont beaucoup plus faibles entre Tile Sampler et [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Les principales différences se situent désormais uniquement dans les sept emplacements de mappage disponibles pour le pilotage de l&#39;échelle, de la position, de la rotation, de la taille, de la couleur et du masquage. Leur effet peut être fusionné séparément.

Tile Sampler est utile pour créer des modèles procéduraux artificiels, avec un contrôle supplémentaire sur certains paramètres pilotés par des cartes d&#39;entrée externes.

Familiarisez-vous avec le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) avant de passer à la vignette Sampler. Dans la plupart des cas, vous trouverez que le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) est suffisant et vous n&#39;aurez pas besoin de la complexité supplémentaire de Tile Sampler.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée de motif 1-6</b> <i>Entrée Niveaux de gris/Entrée couleur</i> | Image de motif personnalisée, utilisée lorsque le paramètre « Motif » est défini sur « Entrée image ».<br><br>La quantité d&#39;entrées disponibles est déterminée par le paramètre <b>Numéro d&#39;entrée de motif</b>. |
| <b>Entrée de mappage d&#39;échelle</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris pour piloter la mise à l’échelle des carreaux. |
| <b>Entrée de mappage de Displacement</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris pour piloter le displacement des carreaux. |
| <b>Entrée Map rotation</b> <i>Entrée en niveaux de gris</i> | Mappage en niveaux de gris pour piloter la rotation des carreaux. |
| <b>Entrée de mappage vectoriel</b> <i>Entrée couleur</i> | Image vectorielle en couleurs pour une mise à l’échelle non uniforme. |
| <b>Entrée de mappage colorimétrique</b> <i>Entrée Niveaux de gris/Entrée couleur</i> | Mappez pour générer une teinte par carreau. |
| <b>Entrée de mappage de masque</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer certaines mosaïques. |
| <b>Entrée de mappage de distribution de motif</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour gérer plusieurs entrées de motif personnalisées. |
| <b>Entrée en arrière-plan</b> <i>Entrée Niveaux de gris/Entrée couleur</i> | Image d’arrière-plan facultative. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>X Quantité</b> <i>0 - 64</i> | Quantité de répétitions X du motif. |
| <b>Quantité Y</b> <i>0 - 64</i> | Quantité de répétitions Y du motif. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Permet la compensation de la courbure et de l’étirement avec des proportions non carrées. |
| <b>Motif</b> |  |
| <b>Motif</b> <i>Entrée de motif, Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Graduation, Ondes, Demi-cloche, Cloche striée, Croissant, Capsule, Cône</i> | Sélectionne la forme de motif à utiliser. |
| <b>Numéro d&#39;entrée de motif</b> <i>1 - 6</i> | Quantité de motifs personnalisés parmi lesquels choisir de manière aléatoire. |
| <b>Distribution d&#39;entrée de motif</b> <i>Aléatoire, Numéro De Modèle, Carte De Distribution</i> | Définit le mode de sélection des entrées de motif multiples. Aléatoire signifie qu’un élément aléatoire est choisi, Numéro de motif signifie qu’ils sont simplement placés dans une séquence en boucle. La carte de distribution utilise une entrée de carte en niveaux de gris pour piloter le placement. |
| <b>Filtrage d’entrée de motif (Moteur > v4)</b> <i>Bilinéaire + Mipmaps, Bilinéaire, Nearest</i> |  |
| <b>Spécifique Au Motif</b> <i>0.0 - 1.0</i> | Permet de modifier la forme du motif sélectionné. L’effet dépend du motif sélectionné. |
| <b>Aléatoire Spécifique Au Motif</b> <i>0.0 - 1.0</i> | L’effet de randomisation dépend du motif sélectionné. |
| <b>Rotation</b> <i>0, 90, 180, 270</i> | Rotation par paliers (90 degrés). |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Rotation libre aléatoire par carreau. |
| <b>Symétrie aléatoire</b> <i>0.0 - 1.0</i> | Définit le nombre de vignettes qui doivent être retournées/mises en miroir de manière aléatoire en fonction du comportement ci-dessous. |
| <b>Mode aléatoire de Symétrie</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Détermine le comportement de mise en miroir des symétries. |
| <b>Taille</b> |  |
| <b>Mode Taille</b> <i>Normal, Conserver le rapport, Absolu, Pixel</i> | Définit le comportement général de la taille du motif.<br><br>Normal vous permet de définir la taille des éléments de motif. Elle est affectée par les valeurs X et Y.<br><br>Conserver le rapport vous permet de définir une taille affectée par les valeurs X et Y, mais le rapport X et Y entre les deux reste intact.<br><br>Absolue vous permet de définir une taille absolue qui n&#39;est pas affectée par les valeurs X et Y.<br><br>Pixel vous permet de définir une taille absolue en pixels, qui n’est pas affectée par les valeurs X et Y. La modification de la résolution affecte la taille des éléments. |
| <b>Taille (Absolue/Pixel)</b> <i>0.0 - 1.0</i> | Modifie les proportions non uniformes des carreaux. Le comportement exact dépend du mode Taille. |
| <b>Taille aléatoire</b> <i>0.0 - 1.0</i> | Rend aléatoire les proportions par carreau. |
| <b>Échelle</b> <i>0.0 - 10.0</i> | Définit l’échelle globale des vignettes. |
| <b>Échelle aléatoire</b> <i>0.0 - 1.0</i> | Echelle aléatoire par carreau. |
| <b>Multiplicateur de carte d&#39;échelle</b> <i>0.0 - 1.0</i> | Fusions dans l’effet de la carte d’échelle. |
| <b>Multiplicateur de mappage vectoriel d&#39;échelle</b> <i>0.0 - 1.0</i> | Fusions dans l’effet de la carte vectorielle d’échelle pour entraîner une mise à l’échelle non uniforme. |
| <b>Effet de paramétrage d&#39;échelle</b> <i>X et Y, X, Y</i> | Définit les axes affectés par le paramétrage de l’échelle. Peut être utilisé pour que le mappage d’échelle affecte uniquement X ou Y des éléments. |
| <b>Position</b> |  |
| <b>Position aléatoire</b> <i>0.0 - 10.0</i> | Aléatoire la position des carreaux sur les deux axes. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Décale les carreaux en fonction du type de décalage. |
| <b>Type de décalage</b> <i>quincux horizontal, quincux vertical, global horizontal, global vertical</i> | Modifie la direction dans laquelle le décalage est appliqué. |
| <b>Décalage global</b> <i>0.0 - 1.0</i> | Décale globalement toutes les mosaïques sur l’axe X ou Y. |
| <b>Intensité de la carte du Displacement</b> <i>0.0 - 1.0</i> | Fusions dans la force de la carte de Displacement sur le décalage. |
| <b>Angle De Displacement</b> <i>0.0 - 1.0</i> | Définit l’angle de déplacement. |
| <b>Displacement de mappage vectoriel</b> <i>0.0 - 1.0</i> | Utilise la carte vectorielle pour piloter le displacement et l’angle. |
| <b>Rotation</b> |  |
| <b>Rotation</b> <i>0.0 - 1.0</i> | Fait pivoter toutes les mosaïques de manière globale. |
| <b>Rotation aléatoire</b> <i>0.0 - 1.0</i> | Permet une rotation aléatoire par mosaïque. |
| <b>Multiplicateur de Map rotation</b> <i>0.0 - 1.0</i> | Fusions dans l’effet de Map rotation sur la rotation par mosaïque. |
| <b>Multiplicateur de mappage vectoriel</b> <i>0.0 - 1.0</i> | Utilise le mappage vectoriel pour piloter la rotation par mosaïque. |
| <b>Couleur</b> |  |
| <b>Seuil de mappage de masque</b> <i>0.0 - 1.0</i> | Seuil du mappage de masque lorsque vous commencez à masquer les vignettes. |
| <b>Inversion du mappage de masque</b> <i>Faux/Vrai</i> | Inverse l’effet de mappage de masque. |
| <b>Technique D&#39;Échantillonnage De Mappage De Masque</b> <i>Centre du motif, cadre de sélection du motif (plus lent)</i> | Indique si le masquage doit être déterminé par un point unique ou par un cadre de sélection. Permet d’éviter que des pixels isolés ne provoquent des effets étranges. |
| <b>Masquer aléatoirement</b> <i>0.0 - 1.0</i> | Le masquage aléatoire fonctionne parallèlement au mappage de masque. |
| <b>Inverser le masque</b> <i>Faux/Vrai</i> | Inverse le masquage aléatoire. |
| <b>Mode de fusion</b> <i>Ajouter/Sub, Max (Tile Sampler) / Ajouter/Sub, Fusion Alpha (Tile Sampler Color)</i> | Mode fusion pour les mosaïques sur l’arrière-plan et entre elles. |
| <b>Couleur</b> <i>(Valeur Niveaux de gris) / (Valeur de couleur)</i> | Couleur globale unie des carreaux. |
| <b>Couleur/Luminance aléatoire</b> <i>0.0 - 1.0</i> | Aléatoire des couleurs, par carreau. |
| <b>Mode De Paramétrage Des Couleurs</b> <i>Entrée de couleur, Échelle, Index de ligne, Index de ligne, Index de motif (Sampler de mosaïque) / table des couleurs, Échelle, Index de ligne, Index de ligne, Index de motif, Position au centre du motif, Position au centre du motif (RG) Taille de la sphère de la mosaïque (B) (Couleur Sampler de mosaïque)</i> | Définit le paramétrage exact de la randomisation des couleurs. |
| <b>Multiplicateur de paramétrage des couleurs</b> <i>0.0 - 1.0</i> | Fusions de l’effet Paramétrage ci-dessus. |
| <b>Effet de paramétrage des couleurs (couleur uniquement)</b> <i>RGB+Alpha, RGB uniquement, Alpha uniquement</i> | Définit la façon dont le paramétrage affecte la couleur. |
| <b>Opacité globale (niveaux de gris uniquement)</b> <i>0.0 - 1.0</i> | Définit l’opacité globale des carreaux. |
| <b>Couleur d&#39;arrière-plan</b> <i>(Valeur Niveaux de gris) / (Valeur de couleur)</i> | Définit la couleur d’arrière-plan unie. |
| <b>Inverser l&#39;ordre de rendu</b> <i>Faux/Vrai</i> | Inverse l’ordre de rendu pour passer de l’arrière vers l’avant. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilesampler-ex2.png" /><br><i>L'exemple montre comment les paramètres sont pilotés par les maps d'entrée (répartition du motif, échelle, rotation).</i>
        </td>
    </tr>
</table>
