---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/cross-section.html"
breadcrumb-title: ''
description: Utilisez le nœud Section transversale pour créer des masques de section transversale basés sur des maps height d’effets de coupe et de découpe.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Cross Section
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Section transversale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Section transversale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

Icône de nœud ![&#39;Cross section&#39;](cross-section.resources/cross-section-2.png "&#39;Cross section&#39; icon"){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Trace le profil en coupe d&#39;une entrée. Peut être ajusté à la verticale ou à l’horizontale et dispose de commandes pour le style de dessin, le décalage de graphe et la mise à l’échelle.

</td>
</tr>
</table>

Ce nœud est particulièrement utile pour le débogage et l&#39;analyse des images de hauteur. vous offrant une vue de profil au pixel près, sans avoir besoin de nœuds complexes ou d’une configuration longue et moins précise dans la vue 3D.

Il peut également être utilisé pour créer des formes et des silhouettes 2D difficiles à réaliser autrement. Combiné avec un [nœud de courbe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)il peut visualiser directement le profil de courbe appliqué à un dégradé linéaire.

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Coordonnée de la section transversale</b> *Flottant* | Définissez la coordonnée d’échantillonnage de la tranche. Il peut s’agir de coordonnées X ou Y en fonction de l’Axe de la section. |
| <b>axe de section</b> *Entier* | Définissez si la tranche est verticale ou horizontale. |
| <b>Afficher l&#39;assistant</b> *Booléen* | Active une incrustation affichant la position de la section sur l&#39;image d&#39;entrée. |
| <b>Paramètres d&#39;Assistant</b> |  |
| <b>Échelle d&#39;Assistant</b> *Flottant* | Taille de l’incrustation exprimée sous la forme d’un multiple, où 1,0 représente l’image entière. |
| <b>Position Assistant</b> *Flottant 2* | Position (X, Y) de l’incrustation dans l’image de sortie, où (0,0, 0,0) est en haut à gauche et (1,0, 1,0) est en bas à droite. |
| <b>Échelle d&#39;Height</b> *Flottant* | Réduit la taille du graphe entier. Utile pour l’affichage HDR. |
| <b>Décalage de l&#39;Height</b> *Flottant* | Décale le graphe entier vers le haut ou vers le bas. Utile pour l’affichage HDR. |
| <b>Style de dessin</b> *Entier* | Basculer entre le remplissage uni et le dessin au trait. |
| <b>Inverser le dégradé</b> *Booléen* | Si le style de dessin est défini sur *Dégradé* ou *Dégradé miroir*, vous permet d&#39;inverser ce dégradé sans affecter l&#39;arrière-plan.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Gradient&#39; ou &#39;Gradient mirrored&#39;. |
| <b>Lisse/Polygonale</b> *Booléen* | Bascule la forme entre un profil lisse parfait ou un polygone irrégulier.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Solid&#39;, &#39;Gradient&#39; ou &#39;Gradient mirrored&#39;. |
| <b>Quantité de segment</b> *Entier* | Définit le nombre de segments utilisés pour dessiner dans le style polygonal ou le style de ligne.<br><br>*Remarque :* disponible uniquement lorsque le paramètre Lisser/Polygonal est défini sur Polygonal ou lorsque le paramètre Style de dessin est défini sur Ligne. |
| <b>thickness de ligne</b> *Flottant* | Définit le thickness de la ligne.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Line. |
| <b>Style de ligne</b> *Entier* | Permet de choisir la coloration et l&#39;atténuation de la ligne.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Line. |
| <b>smoothness de ligne</b> *Flottant* | Définit le retrait de dégradé de la ligne.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Line. |
| <b>Couleur</b> *Flottant* | Couleur en niveaux de gris de la ligne ou de la forme.<br><br>*Remarque :* disponible uniquement lorsque &#39;Drawing style&#39; est défini sur &#39;Solid&#39; ou que &#39;Line&#39; et &#39;Line style&#39; sont définis sur &#39;Smooth&#39; ou &#39;Solid&#39;. |
| <b>Couleur d&#39;arrière-plan</b> *Flottant* | Couleur en niveaux de gris de l&#39;arrière-plan.<br><br>*Remarque :* non disponible lorsque &#39;Drawing style&#39; est défini sur &#39;Line&#39; et &#39;Line style&#39; est défini sur &#39;Segment ID&#39; ou &#39;Gradient along line&#39;. |

## Exemples

![Section transversale : exemple 1](cross-section.resources/cross-section-example-01.gif "Section transversale : exemple 1")

![Section transversale : exemple 2](cross-section.resources/cross-section-example-02.gif "Section transversale : exemple 2")

![Section transversale : exemple 3](cross-section.resources/cross-section-example-03.png "Section transversale : exemple 3")

![Section transversale : exemple 4](cross-section.resources/cross-section-example-04.png "Section transversale : exemple 4")
