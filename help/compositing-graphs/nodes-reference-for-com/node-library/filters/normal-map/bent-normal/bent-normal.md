---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Utilisez le nœud Normale courbée pour générer des cartes de normales courbées qui tiennent compte de l'occlusion ambiante et de l'éclairage indirect.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale courbée
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# Normale courbée

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

Icône de nœud ![Normale courbée](../../../../../../assets/rt-bent-normal.png "Icône de nœud Normale courbée")

<b>Entrée :</b> *Filtres/Mappage de normales*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Description

Génère une courbe de normales en fonction d&#39;une courbe d&#39;height. Une courbe de normales est une version spéciale de [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) et de [Occlusion ambiante (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), qui génère une courbe de normales avec une occlusion ambiante intégrée.\
Ceci peut être utilisé dans les moteurs en temps réel pour que l&#39;Occlusion ambiante soit intégrée dans la carte normale, par exemple pour des réflexions d&#39;occlusion plus précises sur les métaux.

Ce nœud ne doit pas être utilisé en combinaison avec le moteur CPU (SSE) en raison du temps de calcul.

</td>
</tr>
</table>

## Paramètres

<b>Utiliser la Taille physique</b> *Booléen*\
Activez/désactivez cette option pour utiliser les paramètres de Taille physique afin de déterminer l’échelle d’height.

<b>Taille physique</b> *Float3* (disponible lorsque l&#39;option <b>Utiliser la Taille physique</b> est définie sur *True*)\
Ajuste l’échelle d’height en fonction de la taille physique réelle de la surface.

<b>Exemples</b> *Nombre entier*\
Nombre de rayons utilisés pour calculer la normale courbée.\
Plus la valeur est élevée, plus le résultat obtenu est fluide et précis, au détriment des performances.

<b>Échelle d&#39;Height</b> *Flottant (disponible lorsque l&#39;option Utiliser la Taille physique est définie sur Faux)*\
Multiplicateur de l’intensité de l’entrée de courbe de transfert d’height.

<b>Distribution</b> *Nombre entier*\
Définit la méthode de distribution. Affecte la réduction vers les zones ombrées.

<b>Distance Maximale</b> *Flotter*\
Définit la distance maximale que les rayons peuvent parcourir pour être occultés.

<b>Angle de répartition</b> *Flotter*\
Définit l’angle d’étalement des rayons sur lesquels la prise de vue doit être effectuée. Une valeur de 1 correspond à un hémisphère entier.

<b>Format normal</b> *Nombre entier*\
Inverse la couche verte de la sortie.

## Exemples d’images

![Nœud normal plié - Exemple 1](../../../../../../assets/bent-normal-ex-1.jpg "Nœud normal plié - Exemple 1")
