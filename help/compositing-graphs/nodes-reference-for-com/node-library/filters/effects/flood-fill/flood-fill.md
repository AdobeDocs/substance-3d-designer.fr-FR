---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Utilisez le nœud Flood Fill pour remplir des régions connectées de couleur similaire afin de créer des masques et des effets de traitement de texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill.resources/flood-fill-01.png){width="128px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Flood Fill fait partie d’un ensemble avancé d’effets qui vous permettent d’ajouter beaucoup plus de variation à une texture de carreaux binaires de base. Il n’est pas destiné à être utilisé seul : il s’agit plutôt d’un point de départ pour d’autres effets Flood Fill. Cette division des données permet un flux de production plus dynamique, plus optimisé et moins destructeur.

Les autres effets Flood Fill sont [Flood Fill au dégradé](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [Flood Fill à la couleur/aux niveaux de gris](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [Flood Fill à la nuance de gris aléatoire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [Flood Fill à la couleur aléatoire](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [Flood Fill à la taille de la BBox](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [Flood Fill à la position](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Mappeur Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) et [Flood Fill à l’index](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> La map d&#39;entrée doit être adaptée au Flood Fill pour fonctionner. Idéalement, il s’agit d’une carte binaire (noir/blanc uniquement, pas de niveaux de gris) où chaque carreau est séparé des autres lignes par une bordure entièrement noire (0,0,0) pour chaque pixel. Le [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) est un exemple parfait pour cela.
> 
> Des problèmes surviennent si les carreaux ne sont pas séparés par des pixels noirs entiers, généralement lorsque des valeurs d’inclinaison en niveaux de gris sont utilisées. Vous pouvez identifier cela par un manque global de valeurs rouges dans le résultat, et peut-être par des lignes d&#39;artefact étranges. Dans ce cas, ajustez le contraste de la map d&#39;entrée ou éteignez la map d&#39;entrée. Assurez-vous de modifier le paramètre de compromis Sécurité/Vitesse pour voir si quelque chose s’améliore.

</td>
</tr>
</table>

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Compromis sécurité/vitesse</b> <i>Formes simples ou petites, formes complexes ou grandes, pas de mode d&#39;échec.</i> | Définissez le mode de calcul en fonction des formes d’entrée. Permet d’obtenir des résultats beaucoup plus précis si le mode correct est choisi. |
| <b>Options avancées</b> <i>Afficher les paramètres avancés et Sortie/Masquer les paramètres avancés et la sortie</i> |  |
| <b>Remplacer le compromis sécurité/vitesse</b> <i>-1 - 100</i> | Uniquement visible lorsque les options avancées sont activées. Permet de remplacer les fonctions internes. Très avancé, permet de créer ses propres effets ou de déboguer. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-03.png" />
        </td>
    </tr>
</table>

Bons et mauvais exemples de résultats de Flood Fill.
