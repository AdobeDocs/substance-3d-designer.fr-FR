---
title: Éclaboussure de forme v2 sur le masque
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Générateur > Motif > Éclaboussure de forme v2 au masque
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# Éclaboussure de forme v2 sur le masque

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Éclaboussure de forme v2 sur icône de masque](shape-splatter-v2-to-mask.png "Éclaboussure de forme v2 sur masque")

<b>Entrée :</b> Générateur > Motif

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule un masque à partir d&#39;une sélection de formes générées par le nœud [Forme d&#39;éclaboussure v2](../shape-splatter-v2/shape-splatter-v2.md) .<br><br>Les options disponibles incluent la sélection aléatoire ainsi que la sélection de plages de formes par identifiant unique et/ou ID de matériau/ID de motif*.<br><br>Les formes sont pré-masquées par le nœud [Forme d&#39;éclaboussure v2](../shape-splatter-v2/shape-splatter-v2.md) à partir de leur <i>fusion d&#39;height</i> avec l&#39;height d&#39;arrière-plan.<br>L&#39;arrière-plan et les formes non sélectionnées sont en noir pur. (Valeur de 0)<br><br><b>*:</b> L’une des valeurs extraites de l’entrée UVW d’éclaboussures de forme est l’ID de matériau ou l’ID de motif, selon le <b>type de forme</b> utilisé dans le nœud Shape Splatter v2 :<br>- <i>SDF/primitive</i> : ID de Matériau<br>- <i>Entrée/Atlas en grille de motif :</i> ID de motif, c’est-à-dire l’index du motif dans la liste/l’atlas.

</td>
</tr>
</table>

>[!INFO]
>
> Ce nœud nécessite des données d&#39;entrée générées par le nœud [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Autres nœuds de la famille Shape splatter v2 :
> * [Éclaboussure de forme v2 mapper niveaux de gris](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Couleur du mappeur d&#39;éclaboussures de forme v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)

>[!TIP]
> 
> L&#39;exemple de matériau [&#128279;](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) **&#39;Rusty bolts&#39;** est disponible pour commencer avec les nœuds Shape Splatter v2.
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entrées

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Splatter UVW</b> *Couleur* | <b>R</b> - Composante U des UV des formes.<br><b>G</b> - Composante V des UV des formes.<br><b>B</b> - height des formes. (W)<br><b>A</b> - Données compressées :<br> - <i>Partie Entier :</i> identifiant unique des formes. (ID)<br> - <i>Partie fractionnaire :</i> dépend du <b>type de forme</b> : ID de Matériau si SDF/primitif, ID de modèle* si entrée/atlas en grille de modèle.<br><br><b>* :</b> L’ID de modèle est l’index de la forme dans la liste/l’atlas. |

<a name="outputs"></a>

## Sorties

|               |                                           |
|:--------------|:------------------------------------------|
| <b>Sortie</b> | Masque calculé des formes sélectionnées. |

<a name="parameters"></a>

## Paramètres

|                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Sortie</b> *Entier* | Valeurs utilisées pour les formes sélectionnées dans le masque de sortie.<br><br>- <b>Masque binaire :</b> Les formes sélectionnées utilisent toutes une valeur de 1.<br>- <b>ID de forme (entier) :</b> Les formes sélectionnées utilisent leur identifiant unique. (ID)<br>- <b>ID de Matériau (entier) :</b> les formes sélectionnées utilisent leur ID de matériau.<br>- <b>ID de forme (normalisé) :</b> les formes sélectionnées utilisent leur identifiant (ID) unique mappé sur la plage [0, 1] allant du plus petit ID sélectionné au plus haut.<br>- <b>ID de Matériau (normalisé) :</b> les formes sélectionnées utilisent leur ID de matériau mappé sur la plage [0, 1] allant du plus petit ID de matériau sélectionné au plus haut. |
| <b>Plage de début de l&#39;ID de forme</b> *Entier* | Identifiant (ID) unique de la forme utilisé comme début de la plage de sélection. (Inclus) |
| <b>Plage de fin d’ID de forme</b> *Entier* | Identifiant (ID) unique de la forme utilisé comme fin de la plage de sélection. (Inclus) |
| <b>Décalage de l&#39;ID de forme</b> *Entier* | Décale les identifiants uniques des formes selon la valeur spécifiée, dans le cadre de la plage de sélection.<br><br>Cela permet de décaler facilement la sélection actuelle de la valeur spécifiée sans avoir à ajuster les limites de début et de fin manuellement. |
| <b>combinaison de masques Matériau/id de motif</b> *Entier* | Spécifie l&#39;opérateur logique utilisé pour combiner la sélection par ID d&#39;identifiant unique avec la sélection par ID de matériau/ID de motif.<br><br>- <b>Aucun :</b> Ignorez l&#39;ID de matériau/ID de motif pour la sélection.<br>- <b>AND:</b> Les formes sélectionnées doivent être incluses à la fois dans les plages d&#39;ID et d&#39;ID de matériau/ID de motif. (Comprend moins de formes)<br>- <b>OU :</b> Les formes sélectionnées doivent être incluses dans les plages d&#39;ID ou d&#39;ID de matériau/d&#39;ID de motif. (Inclut d’autres formes) |
| <b>Plage de début de l&#39;ID de Matériau/motif</b> *Entier* | ID de matériau ou ID de motif* utilisé comme début de la plage de sélection. (Inclus)<br><br><b>*:</b> Voir la description du nœud pour plus de détails. |
| <b>Plage de fin d&#39;ID de Matériau/motif</b> *Entier* | ID de matériau ou ID de motif* utilisé comme fin de la plage de sélection. (Inclus)<br><br><b>*:</b> Voir la description du nœud pour plus de détails. |
| <b>Masque aléatoire de forme</b> *Flottant* | Facteur pour le masquage aléatoire des formes, où 1 signifie que toutes les formes sont masquées. |

