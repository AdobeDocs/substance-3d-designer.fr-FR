---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Apprenez à utiliser les mappages FXM dans Substance 3D Designer pour appliquer des graphiques de fonction aux textures en vue de la génération de motifs procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---


# FXMaps

**Le nœud FX-Map permet la création d&#39;images procédurales**. C&#39;est l&#39;une des caractéristiques les plus puissantes de la technologie de Substance.

Une FX-Map représente un type spécial de graphique, appelé chaîne de Markov. Les chaînes de Markov représentent un processus de base simple : répliquer et subdiviser une image à plusieurs reprises. À chaque étape, une image peut être pivotée, traduite et fusionnée à volonté. Les résultats peuvent aller de simples motifs à des bruits complexes. FX-Maps constitue la base de nombreuses Substances d’exemple installées avec Substance 3D Designer.

## Création de graphiques FX-Map

Si vous voulez voir un graphique FX-Map, ajoutez simplement un [nœud FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) à un [graphique de Substance](../../compositing-graphs/substance-compositing-graphs.md), puis cliquez avec le bouton droit sur le nœud et appuyez sur CMD + E (OS X) ou CTRL + E (Windows) pour ouvrir son graphique. Ce graphique FX-Map apparaît dans un nouvel onglet du panneau Graphiques. Vous pouvez basculer entre ce graphique et le graphique de Substance en cliquant sur l’onglet.

## À quoi servent les FX-Maps ?

Les utilisations les plus courantes des cartes FX-Maps sont la création de motifs répétitifs, tels que des bandes et des briques, et de bruits, tels que des bruits de Perlin, de Brownien et de gaussien. Les bruits sont particulièrement utiles pour créer des textures organiques et naturelles comme du dirt, du dust, des bétons, des surfaces en pierre, des éclaboussures de liquide, etc.

Les graphiques FX-Map ne fonctionnent pas de la même manière que les graphiques Substance : dans les graphiques Substance, chaque nœud est indépendant et ne connaît pas sa position dans le graphique global, pas plus qu’il ne se soucie de la provenance ou de la destination des données de l’image.

Nous examinerons plus en détail chacun des trois nœuds de graphique FX-Map dans le chapitre suivant, mais brièvement, chaque nœud FX-Map offre l&#39;une des trois opérations suivantes :

### Quadrant

À cette étape du graphique, l’image est divisée en quatre quadrants. Il s&#39;agit du type de nœud le plus courant. Une chaîne de nœuds de quadrant peut créer des images très complexes, ainsi que des motifs complexes.

En fait, les nœuds du quadrant représentent un niveau (ou **octave**) dans un graphique en quadrilatère. Les graphiques FX-Map masquent cette structure arborescente en représentant chaque niveau de l&#39;arborescence par un seul quadrant : chaque fois que vous connectez un nœud de quadrant à un autre, vous créez en fait un niveau d&#39;arborescence complet.

La raison de cette technique de « triche » est de supprimer la nécessité de représenter chaque nœud à chaque niveau d&#39;un arbre individuellement : après seulement quatre couches de profondeur, vous auriez besoin d&#39;utiliser 4 x 4 x 4 x 4 nœuds, ce qui représente 256 nœuds individuels ! Au lieu de cela, chaque nœud du quadrant « sait » à quel niveau il se trouve dans l&#39;arbre et génère son imagerie en conséquence.

Cela n&#39;aura probablement pas beaucoup de sens pour de nombreux lecteurs, mais nous allons entrer dans les détails sous peu.

### Itérer

Répète l&#39;image passée dans le connecteur de droite sur l&#39;image passée dans le connecteur de gauche selon le nombre d&#39;itérations défini.

Ce nœud est le plus souvent utilisé avec un ou plusieurs graphiques de fonctions dynamiques pour déplacer ou faire pivoter l&#39;image d&#39;entrée d&#39;une manière ou d&#39;une autre à chaque itération.

### Basculer

Il prend deux entrées et bascule simplement entre l’une ou l’autre, comme défini par son paramètre Sélecteur. Comme pour le nœud Itérer, le paramètre Sélecteur est souvent choisi par une fonction dynamique.

## Variables système FX-Maps

FX-Maps prend en charge les variables système. Ces variables commencent toujours par un symbole de dollar (« $ ») et sont les suivantes :

| Nom | Particularité | Type de données | Objectif |
| --- | --- | --- | --- |
| $time | - | float1 | Cette variable renvoie le temps en secondes depuis le démarrage du moteur de rendu de Substance.Il est idéal pour les Substances qui doivent s’animer en fonction du temps. (E.g. .)Dans certaines applications, y compris Substance Player, une Substance qui utilise $time entraîne l&#39;affichage d&#39;un journal dans l&#39;interface utilisateur. |
| $profondeur | - | float1 | Renvoie le nombre d’octaves (niveau) du nœud FX-Map. Cela permet à un nœud de modifier son comportement en fonction du niveau qu&#39;il représente dans l&#39;arborescence quadruple. |
| $depthpow2 | - | float1 | Comme ci-dessus, mais renvoie 2 élevé à la puissance de l&#39;octave (niveau). Il s’agit d’une valeur d’assistant utile pour certains calculs courants. |
| $number | Itérer les nœuds uniquement | float1 | Renvoie le numéro du motif dessiné. Les graphiques de fonction dynamique contrôlant un nœud itéré peuvent y accéder pour modifier son comportement à chaque étape d&#39;itération. (Notez que $number commence à compter à partir de 0, et non à partir de 1.) |
| $size | - | float2 | Renvoie la taille du nœud actif (en pixels). |
| $sizelog2 | - | float2 | Comme ci-dessus, mais renvoie la taille en tant que valeurs de puissance de 2 (par exemple : pour l’image 2048\*2048, $sizelog2 renvoie 11). |
| $pos | Nœuds du quadrant uniquement | float2 | Renvoie la position de naissance du motif. Le résultat est toujours une valeur comprise entre 0 et 1. |
