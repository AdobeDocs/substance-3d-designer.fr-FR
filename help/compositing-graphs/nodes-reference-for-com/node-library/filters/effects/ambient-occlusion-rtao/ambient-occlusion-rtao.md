---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Utilisez le nœud d'Occlusion ambiante (RTAO) pour générer des cartes d'occlusion ambiante en temps réel à partir de cartes d'height pour un ombrage réaliste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusion ambiante (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Occlusion ambiante (RTAO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icône de nœud RTAO](../../../../../../assets/rt-ao.png "Icône de nœud RTAO")

<b>Entrée :</b> *Filtres/Effets*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Génère une carte d&#39;Occlusion ambiante en fonction d&#39;une entrée de carte d&#39;height.

Ce filtre donne des résultats plus précis que le HBAO, mais ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul.

Voir [Occlusion ambiante (HBAO) (nœud de filtre)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) pour une alternative plus simple et plus rapide.

</td>
</tr>
</table>

## Paramètres

<b>Utiliser la Taille physique</b> *Booléen*\
Activez/désactivez cette option pour utiliser les paramètres de Taille physique afin de déterminer l’échelle d’height.

<b>Taille physique</b> *Float3* (disponible lorsque l&#39;option <b>Utiliser la Taille physique</b> est définie sur *True*)\
Ajuste l’échelle d’height en fonction de la taille physique réelle de la surface

<b>Échantillons </b>*Entier*\
Nombre de rayons utilisés pour calculer l&#39;occlusion ambiante.\
Plus la valeur est élevée, plus le résultat obtenu est fluide et précis, au détriment des performances.

<b>Échelle d&#39;Height</b> *Flottant* (disponible lorsque <b>Utiliser la Taille physique</b> est défini sur *Faux*)\
Multiplicateur de l’intensité de l’entrée de courbe de transfert d’height.

<b>Distribution</b> *Entier* Définit la méthode de distribution. Affecte la réduction vers les zones ombrées,

<b>Distance Maximale</b> *Flotter*\
Définit la distance maximale que les rayons peuvent parcourir pour être occultés.

<b>Angle de répartition</b> *Flotter*\
Définit l’angle d’étalement des rayons sur lesquels la prise de vue doit être effectuée. Une valeur de 1 correspond à un hémisphère entier.

## Exemples d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nœud RTAO - Exemple 1](../../../../../../assets/image2021-6-18-11-7-48.png "Nœud RTAO - Exemple 1")

</td>
<td style="border: 0;" valign="top">

![Nœud RTAO - Exemple 2](../../../../../../assets/image2021-6-18-11-9-0-1.png "Nœud RTAO - Exemple 2")

</td>
</tr>
</table>
