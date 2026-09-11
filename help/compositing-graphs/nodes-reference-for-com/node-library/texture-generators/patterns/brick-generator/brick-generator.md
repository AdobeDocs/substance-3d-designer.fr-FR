---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Utilisez le nœud Générateur de Briques pour créer des motifs de brique procéduraux avec des propriétés personnalisables de taille, de décalage et de mortier.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Générateur de briques
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# Générateur de briques

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

<b>Entrée :</b> Générateurs De Textures > Motifs

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Générateur de motif de Brique avancé. Propose de nombreuses options pour générer spécifiquement des motifs de brique artificiels

Pour plus d&#39;options, voir [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Briques</b> <i>1 - 64</i> | Définit la quantité de briques dans les axes X et Y. |
| <b>Biseau</b> <i>0.0 - 1.0</i> | Modifie le profil de biseau des briques, permet de le modifier dans deux directions et définit le profil de retrait et l’arrondi des angles. |
| <b>Conserver le rapport</b> <i>Faux/Vrai</i> | Rend le profil de biseau lié ou non à la taille de la brique. |
| <b>Écart</b> <i>0.0 - 1.0</i> | Espace à laisser entre les briques. Gardez à l’esprit que Biseau introduit également un espace. Par conséquent, définir également des biseaux signifie que vous devez compenser avec ce paramètre. |
| <b>Taille moyenne</b> <i>0.0 - 1.0</i> | Décalage du motif de brique, modifie la taille d’une colonne ou ligne sur deux. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Modifie les profils d’height. Permet l&#39;introduction d&#39;une variation de Luminance et toutes sortes de randomisation. |
| <b>Pente</b> <i>-1.0 - 1.0</i> | Introduit une pente par brique, comme si certaines briques étaient inclinées d’un certain angle. |
| <b>Décalage</b> <i>0.0 - 1.0</i> | Décale les briques ligne par ligne et affecte l’espacement ligne par ligne. |
| <b>Extension non carrée</b> <i>Faux/Vrai</i> | Active la compensation de la courbure et de la étire avec des proportions non carrées. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>
