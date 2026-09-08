---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Altération du fabric pour ajouter des effets d’usure et de vieillissement aux matériaux du fabric en fonction de la géométrie et de la courbure du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération du tissu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# Altération du tissu

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

<b>Entrée :</b> Générateurs basés sur le Maillage > Altération

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il ajoute un effet d&#39;usure aléatoire du tissu, avec un contrôle de l&#39;âge et de la saleté.<br>Cet effet ne fonctionne pas très bien à moins que vous n&#39;ayez branché les cartes AO et Normal d&#39;Espace monde bakées appropriées, car elles les nécessitent pour calculer et générer correctement l&#39;ensemble.

Assurez-vous de bien comprendre les [modes de création de liens](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) lorsque vous travaillez avec des matériaux complets.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Occlusion ambiante</b> <i>Entrée en niveaux de gris</i> | Map bakée utilisée pour les effets internes et le masquage. |
| <b>Espace normal</b> <i>Entrée couleur</i> |  |
| <b>Masquer</b> <i>Entrée en niveaux de gris</i> | Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ». |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Canaux</b> | Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité. |
| <b>Avancé</b> |  |
| <b>Format normal</b> <i>DirectX, OpenGL</i> | Bascule entre différents formats de mappage normal (inverse la couche verte). |
| <b>Masquer</b> <i>Faux/Vrai</i> | Active ou désactive l&#39;utilisation de la carte de masque. |
| <b>Effet</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | Fusions dans un effet de dust plus sombre, en fonction des zones orientées vers le haut dans l’Espace monde Normalmap. |
| <b>Sale</b> <i>0.0 - 1.0</i> | Fusions dans un effet global de dirt/doigt, reposant principalement sur les zones occultées (sombres) dans l’AO. |
| <b>Usure Des Bords</b> <i>0.0 - 1.0</i> | Ajoute un effet de netteté/intensification aux contours, en fonction de la Normale au Matériau. |
| <b>Utilisé</b> <i>0.0 - 1.0</i> | Fusions dans le dirt accumulé très sombre dans les plis, selon AO. Les valeurs Maximale et Minimale ont tendance à être très extrêmes. Utilisez-les avec précaution. |
| <b>Âge</b> <i>0.0 - 1.0</i> | Fusions sur un motif global d&#39;usure de répétition. Le contrôle du seuil en dessous contrôle l’influence de l’IA. Les valeurs maximales et minimales ont tendance à être très extrêmes. |
| <b>Seuil d&#39;âge</b> <i>0.0 - 1.0</i> | Définit la mesure dans laquelle l&#39;objet AOP affecte le paramètre Age. |
| <b>Plis d&#39;âge</b> <i>0.0 - 1.0</i> | Contrôle la fusion de légers plis supplémentaires dans l’effet Age. |
| <b>Échelle Scratches Des Contours Nets</b> <i>1.0 - 32.0</i> | Définit l’échelle des petites rayures, qui éliminent principalement l’effet Utilisé et Age. |
| <b>Intensité de déformation Scratches des contours nets</b> <i>0.0 - 1.0</i> | Définit l’intensité de la déformation pour les petites rayures ci-dessus. |
| <b>Ancienne désaturation du fabric</b> <i>0.0 - 1.0</i> | Contrôle la désaturation de l’effet Age. |
| <b>Luminosité de l&#39;ancienne structure</b> <i>0.0 - 1.0</i> | Contrôle la luminosité de l’effet Age. *Il s&#39;agit d&#39;un paramètre très important à modifier pour obtenir l&#39;aspect que vous souhaitez, mais les résultats peuvent être extrêmes : à utiliser avec des modifications subtiles.* |
| <b>Fusion</b> |  |
| <b>Intensité de Diffuse</b> <i>0.0 - 1.0</i> | Intensité de fusion du diffus. |
| <b>Intensité de la Base color</b> <i>0.0 - 1.0</i> | Intensité de fusion de la couleur de base. |
| <b>Intensité normale</b> <i>0.0 - 1.0</i> | Intensité de fusion de la normale. |
| <b>Intensité du Specular</b> <i>0.0 - 1.0</i> | Intensité de fusion du Specular. |
| <b>Intensité de la Brillance</b> <i>0.0 - 1.0</i> | Intensité de fusion du brillant. |
| <b>Intensité de la Rugosité</b> <i>0.0 - 1.0</i> | Intensité de fusion de la rugosité. |
| <b>Intensité de l&#39;Ambient occlusion</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;Occlusion ambiante. |
| <b>Intensité de l&#39;Height</b> <i>0.0 - 1.0</i> | Intensité de fusion de l&#39;Height. |

## Exemples

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/fabric-ex.gif" />
        </td>
    </tr>
</table>
