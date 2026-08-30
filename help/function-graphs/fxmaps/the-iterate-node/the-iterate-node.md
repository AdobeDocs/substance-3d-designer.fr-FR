---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: Utilisez le nœud Itérer dans FXMaps pour créer des répétitions et des variations de procédure dans vos matériaux.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nœud itéré
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# Nœud itéré

Le nœud Itérer vous permet de multiplier les images d’un nœud de quadrant et est essentiellement un nœud « répétitif ». Un nœud de quadrant à une profondeur de 1 produirait normalement 4 quadrants. Le nœud Itérer vous permet de répéter son image de sortie autant de fois que vous le souhaitez, chaque ensemble de répétitions étant traité séparément.

Le nœud Itérer n&#39;a pas d&#39;autres propriétés qu&#39;un paramètre « How repétitions do you want ? ». Il en résulte que les nouvelles images sont, par défaut, simplement superposées et fusionnées avec celles produites par le nœud de quadrant.

Le nœud Itérer répète l&#39;image d&#39;entrée reçue. Le nombre de répétitions est défini par sa propriété Itérations :

La clé de l&#39;utilisation du nœud Itérer est que toutes les fonctions dynamiques attachées à chaque image répétée seront également traitées. Cela signifie que chaque répétition peut avoir son propre ensemble de réglages uniques. Vous pouvez utiliser la propriété Générateur aléatoire du nœud Itérer pour modifier le fonctionnement de cette fonction. Vous pouvez également accéder à la variable système *$number* dans vos fonctions dynamiques pour déterminer quelle répétition est en cours de rendu et modifier le résultat de la fonction en conséquence.

Par exemple : si vous appliquez une rotation aléatoire à chaque image d&#39;un nœud de quadrant, puis que vous appliquez la sortie de ce nœud de quadrant à l&#39;entrée active d&#39;un nœud itéré, chacune des images répétées aura également sa propre rotation aléatoire.

Toutes les fonctions dynamiques disponibles sur le nœud de quadrant s&#39;appliquent également aux images répétées produites par le nœud itéré. C’est comme si le nœud dupliquait le nœud du quadrant au même niveau, au lieu d’ajouter un autre niveau de profondeur.

## Connecteur direct

Chaque nœud itéré a deux connecteurs le long de sa base. Le connecteur de gauche est un connecteur direct. L’image qu’il reçoit est transmise directement au connecteur de sortie du nœud, où elle est fusionnée avec les images répétées :

Notez que l’image directe est toujours transmise sans modification, quel que soit le paramètre Itération.

![](the-iterate-node.resources/iterate.jpg)
