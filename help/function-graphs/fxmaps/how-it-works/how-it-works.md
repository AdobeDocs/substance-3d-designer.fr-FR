---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Découvrez comment fonctionnent les mappages FXM dans Substance 3D Designer pour appliquer des graphiques de fonction aux textures pour les effets procéduraux.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fonctionnement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# Fonctionnement

Il est essentiel de comprendre le fonctionnement d’un graphique FX-Map pour maîtriser cette fonctionnalité puissante.

Un graphique FX-Map peut contenir un ou plusieurs des trois types de nœuds FX-Map : Quadrant, Itération et Commutation. Parmi ces nœuds, celui que vous utiliserez probablement le plus souvent est le quadrant, avec le nœud Itérer une seconde près.

Le nœud Parameter Set est le moteur principal de FX-Maps. Il crée le graphique quadruple arbre de la région centrale sur lequel FX-Maps s’appuie, mais il ne s’affiche pas comme tel. Visuellement, le graphique à quatre arbres est représenté sous la forme d&#39;une chaîne de Markov.

Lors du rendu de la FX-Map, le graphique FX-Map simplifié est « déballé » pour ressembler au graphique en forme de grand arbre. Le moteur « marche » tout le quad-tree, travaillant de haut en bas, puis de gauche à droite.

Les nœuds FX-Map ne copient pas et collent aveuglément leurs images. Lorsque chaque image est rendue, toutes les fonctions dynamiques dont elle dispose sont exécutées. Les fonctions affectent chaque image rendue par le nœud. Vous pouvez donc appliquer à chaque image une rotation aléatoire, un facteur d’échelle ou plusieurs autres réglages.
