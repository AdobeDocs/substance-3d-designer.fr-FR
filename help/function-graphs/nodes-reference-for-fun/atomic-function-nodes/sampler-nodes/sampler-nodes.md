---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Accédez aux nœuds d’échantillonnage dans les graphiques fonctionnels Substance 3D Designer pour échantillonner des textures et extraire des valeurs chromatiques.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Échantillonnages
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Nœuds Sampler

![Nœuds Sampler](sampler-nodes.resources/image2016-1-12-14-45-43.png "Nœuds Sampler")

Ces nœuds échantillonnent une valeur dans une image d’entrée aux coordonnées 2D fournies :

L&#39;option <b>Échantillon de gris</b> échantillonne une valeur de luminance à l&#39;entrée <b>Position</b> dans une image en niveaux de gris et la génère en tant que valeur <b>Float</b>.

<b>Échantillon de couleur</b> échantillonne une valeur RVBA à l&#39;entrée <b>Position </b> dans une image couleur et la génère en tant que valeur <b>Float4</b> où les composantes R, V, B et A sont mappées aux composantes X, Y, Z et W respectivement.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Les coordonnées commencent dans le coin supérieur gauche d’une entrée et sont comprises entre 0 et 1 horizontalement et verticalement.

Les positions hors de cette plage sont traitées selon le <b>mode d&#39;adressage</b> sélectionné (voir ci-dessous).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Coordonnées des pixels](sampler-nodes.resources/samplercoords.png "Coordonnées des pixels")

</td>
</tr>
</table>

>[!NOTE]
>
> L&#39;entrée <b>Position</b> doit être une valeur Float2 où les coordonnées X et Y de l&#39;image sont mappées respectivement aux composantes X et Y de la valeur

## Paramètres

+++Image d&#39;entrée
Permet de sélectionner l&#39;entrée de nœud à utiliser pour l&#39;échantillonnage.

La liste s’adapte dynamiquement aux entrées actuellement connectées. Cela signifie que des entrées sont ajoutées lorsque vous connectez des entrées de nœud.

La numérotation des entrées commence à 0, de sorte qu&#39;une image connectée à la première entrée du nœud est répertoriée comme *Image d&#39;entrée 0*.

+++

+++Mode de filtrage
Permet de définir le mode d’interpolation lorsque les pixels de l’image échantillonnée ne sont pas mappés exactement à l’image de sortie, en raison de différences de résolution.

<b>Le Plus Proche</b>\
Le pixel sera mappé à la cible *tel quel* à la coordonnée correspondante. Si la cible est de résolution inférieure, le pixel peut être totalement ignoré. Si la cible est d’une résolution plus élevée, elle sera mappée à tous les pixels couvrant sa plage. La sortie est *plus nette* et sera légèrement *crénelée*.

<b>Filtrage bilinéaire</b>\
Un processus de filtrage est appliqué à l&#39;image source afin que ses pixels soient mappés à la résolution cible de manière à *lisser* les transitions entre les pixels. La sortie est *plus lisse* et sera légèrement *floue*.

+++

+++Mode d&#39;adressage
Contrôle la gestion des valeurs de position en dehors de la plage [0;1].

<b>Répéter</b>\
Effectue une boucle sur la plage [0;1] à mesure que la valeur augmente.\
Par exemple : 3,4 est 0,4, -1,7 est 0,3.

<b>Fixer au bord</b>\
Permet de fixer les valeurs hors plage [0;1] à la limite la plus proche.\
Par exemple : .3.4 est 1, -1.7 est 0.

+++
