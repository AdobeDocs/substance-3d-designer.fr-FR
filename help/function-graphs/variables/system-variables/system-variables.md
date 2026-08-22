---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: Découvrez les variables système intégrées disponibles dans les graphiques fonctionnels Substance 3D Designer pour les workflows avancés.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variables intégrées
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# Variables intégrées

Vous pouvez utiliser des variables intégrées dans les [graphiques de fonction de Substance](../../../function-graphs/function-graphs.md) afin d&#39;accéder à des valeurs spécifiques. Ils commencent toujours par un symbole `$` (dollar).

Certaines variables ne sont disponibles que dans des contextes spécifiques.

<b>Tous les nœuds</b>

Variables système

| Nom | Type | Objectif |
| --- | --- | --- |
| $size | Flottant2 | Renvoie la taille du nœud actif en pixels.   Si elle est utilisée dans le paramètre [Taille de sortie](../../../compositing-graphs/output-size/output-size.md) défini sur une méthode d&#39;héritage *Relative à...* [&#128279;](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), renvoie la *valeur héritée*. |
| $sizelog2 | Flottant2 | Comme ci-dessus, mais renvoie la taille en tant que valeurs de puissance de 2 (par exemple : pour l&#39;image 2048\*2048, `$sizelog2` renvoie 11).   Si elle est utilisée dans le paramètre [Taille de sortie](../../../compositing-graphs/output-size/output-size.md) défini sur une méthode d&#39;héritage *Relative à...* [&#128279;](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), renvoie la *valeur héritée*. |
| $pixelratio | Entier | Renvoie une valeur entière correspondant au rapport de pixels du nœud actuel (hérité ou absolu) : 0 : Étirement 1 : Carré |
| $tiling | Entier | Renvoie une valeur entière correspondant au mode de mosaïque du nœud actuel (hérité ou absolu) : 0 : Aucun mosaïque 1 : Mosaïque horizontale 2 : Mosaïque verticale 3 : Mosaïque H et V |
| $physicalsize | Flottant3 | Renvoie la valeur de la propriété <b>Taille physique</b> du [graphe](../../../compositing-graphs/graph-parameters/graph-parameters.md). |
| $uvtile | Entier2 | Lors de l’utilisation de workflows UDIM, cette variable renvoie l’index de l’UDIM actuel dans U et V.   Par exemple, (2, 0) pour la mosaïque 1003, (7, 11) pour la mosaïque 1118, ... |

<b>FX-Map</b>

Variables système

| Nom | Type | Objectif |
| --- | --- | --- |
| $pos | Flottant2 | Renvoie la position de naissance du motif. L’origine (0, 0) se trouve dans le coin supérieur gauche de l’image. |
| $profondeur | Flottant | Renvoie le numéro d&#39;octave (niveau) du nœud [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md). Cela permet à un nœud de modifier son comportement en fonction du niveau qu&#39;il représente dans l&#39;arborescence quadruple. |
| $depthpow2 | Flottant | Comme ci-dessus, mais renvoie l&#39;inverse multiplicatif de 2 élevé à la puissance du nombre d&#39;octave (niveau) - c&#39;est-à-dire 1/(2^octave). Il s’agit d’une valeur d’assistant utile pour certains calculs courants. |
| $number | Flottant | Renvoie le numéro du motif dessiné. Les graphiques de fonction dynamique contrôlent un nœud [Itérer](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) pour modifier son comportement à chaque étape d&#39;itération.   Notez que `$number` commence à compter à partir de 0, et non 1.   Lors de l&#39;utilisation d&#39;une chaîne de nœuds d&#39;itération, la variable `$number` renvoie le numéro d&#39;itération du dernier nœud d&#39;itération connecté avant le paramètre de fonction utilisé. Si vous souhaitez récupérer le numéro d&#39;itération à partir de plusieurs nœuds Itérer, vous devez utiliser des « variables personnalisées » via des nœuds [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md). |

<b>Processeur de pixels</b>

Variables système

| Nom | Type | Objectif |
| --- | --- | --- |
| $pos | Flottant2 | Renvoie la position du pixel en cours d’évaluation. |

<b>Global</b>

Variables système

| Nom | Type | Objectif |
| --- | --- | --- |
| $time | Flottant | Cette variable renvoie le temps en secondes depuis le démarrage de la Substance Engine. Il peut être utilisé dans des graphiques dont le résultat doit changer en fonction du temps écoulé.  **Remarque :** bien qu&#39;il n&#39;y ait actuellement aucun moyen de modifier cette valeur dans Designer, les applications qui intègrent la Substance Engine peuvent l&#39;exploiter, telles que [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) pour l&#39;animation ou [Substance 3D Painter](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/home) pour [traits dynamiques](https://experienceleague.adobe.com/fr/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes). |
| $normalformat | Entier | Format normal (c’est-à-dire DirectX ou OpenGL) utilisé dans l’environnement actuel.  **Remarque :** cette variable n&#39;a aucun effet dans Designer et peut être utilisée par d&#39;autres applications qui intègrent la Substance Engine. |
