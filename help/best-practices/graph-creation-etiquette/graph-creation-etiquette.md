---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/best-practices/graph-creation-etiquette.html"
breadcrumb-title: ''
description: Découvrez les bonnes pratiques et les règles de création de graphes de Substance pour assurer des workflows propres, maintenables et efficaces.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Graph Creation Etiquette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Règles de création des graphes
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---


# Règles de création des graphes

La création de graphes volumineux et complexes peut rapidement devenir déroutante et compliquée à explorer. Un certain nombre d&#39;outils peuvent être utilisés pour atténuer ces problèmes, et il y a de bonnes habitudes à prendre pour éviter les problèmes plus tard. Cette page fournit une liste concluante des techniques que nous recommandons d&#39;utiliser pour des Graphes propres, efficaces et fonctionnels qui sont faciles à partager et à comprendre.

## Général

### Organisation du graphe

#### Éléments du graphe

Les éléments de graphe sont des objets assistants qui peuvent être placés à côté et autour de vos nœuds dans [la Vue du graphe](../../interface/the-graph-view/the-graph-view.md). Des trois, le Cadre offre les avantages les plus rapides et les plus importants, tandis que l’Épingle Commentaire et Navigation est plus adaptée à des scénarios spécifiques.

#### Cadre

La principale chose qui rend les graphes plus propres et plus faciles à lire, c&#39;est le placement des Cadres autour des groupes de base de votre graphe. Sans Cadres, un grand Graphe est presque illisible, et même les petits Graphes deviennent beaucoup plus faciles à comprendre une fois les cadres dessinés. Un avantage énorme des Cadres est que leurs <b> noms sont toujours rendus à la même échelle</b>, même si vous effectuez un zoom arrière très loin.

![Cadres dans les graphes de Substance](graph-creation-etiquette.resources/frames.gif "Cadres dans les graphes de Substance")

Les cadres permettent de comprendre beaucoup plus facilement ce qui se passe dans un graphe. Ils peuvent vous aider, en tant qu’auteur, à reprendre votre travail des mois plus tard, ou aider un autre utilisateur, tel qu’un collègue, à trouver son chemin dans un Graphe auquel il n’est pas habitué.

Utilisez les critères suivants lors de l’importation de mots de Cadre :

* Identifiez **les blocs de fonctionnalité** (par exemple, 8 nœuds qui, ensemble, produisent un effet de dirt) et regroupez-les à l&#39;aide de Cadre.
* Essayez toujours d&#39;**utiliser des couleurs différentes** pour vos Cadres : les Cadres avec la même couleur bleue par défaut ne se démarquent pas beaucoup les uns des autres.
* Utilisez des **noms clairs et descriptifs** qui ne sont pas trop longs (voir la section ci-dessous pour obtenir plus de conseils)
* Ne mettez pas **trop ou trop peu** dans un Cadre, car cela n&#39;améliore pas la lisibilité. Le montant exact diffère évidemment entre les graphes et les fonctionnalités.
* Si nécessaire, **ajoutez du texte dans la description** pour mieux comprendre ce qui se passe dans un cadre.

#### Commentaires et Épingles

Les commentaires et les épingles sont secondaires par rapport aux Cadres et ne sont pas indispensables pour les graphes bien rédigés. Ils peuvent être utilisés dans les scénarios suivants :

* Les commentaires permettent d’ajouter du texte au-delà de ce que permet la description d’un Cadre. Vous pouvez ajouter de petits morceaux de texte par nœud, principalement pour des informations peu détaillées. Les commentaires ne sont pas correctement mis à l’échelle et ne sont pas lus à un niveau de zoom éloigné.
* Les Épingles de navigation vous permettent de parcourir des zones spécifiques du Graphe à l&#39;aide du raccourci F2. Cela peut être utile pour les très grands graphes où il faut souvent sauter entre deux zones qui sont très éloignées l&#39;une de l&#39;autre.

### Emplacement d’entrée et de sortie

Les entrées et les sorties doivent être placées aux extrémités des Graphes : toutes les sorties à droite, toutes les entrées à gauche, chacune alignée verticalement. Cela facilite leur recherche et leur identification.

![Position des entrées et sorties](graph-creation-etiquette.resources/inout.gif "Position des entrées et sorties")

L’exemple ci-dessus est un cas extrême : les Cadres ne sont pas toujours nécessaires ou possibles, mais il doit être clair que l’alignement vertical des Entrées et Sorties est beaucoup plus clair que le placement aléatoire et mélangé.

### Réacheminement des liens

Dans les grands Graphes très longs, des liens sont parfois établis sur une très grande étendue. Cela conduit à des fils de liaison confus traversant le Graphe sans beaucoup de contrôle. Le raccourci « Alt + Maj + Faire glisser » vous permet de réorganiser ces liens, de les rediriger sur un chemin différent en subdivisant un lien et en ajoutant une poignée supplémentaire au milieu. Il est recommandé de l’utiliser dans les scénarios où cela est logique.

![Réacheminement des liens](graph-creation-etiquette.resources/linkjreroute.gif "Réacheminement des liens")

### Étiquette, identificateur et utilisation

Tout Graphe destiné au partage ou à la publication doit faire l’objet d’une attention particulière dans les métadonnées supplémentaires afin d’améliorer la convivialité. Les points suivants sont importants :

Les étiquettes suggérées par défaut ne sont jamais suffisantes. Prenez le temps et les efforts nécessaires pour ajouter des étiquettes personnalisées aux paramètres exposés et à vos entrées et sorties.

![Identifiant et étiquette](graph-creation-etiquette.resources/output-label.png "Identifiant et étiquette")

Essayez de ne pas trop avoir de différences entre identifiant et Étiquette : si l&#39;Identifiant est utilisé ailleurs (dans plusieurs fonctions), il peut être très difficile de déterminer quelle propriété d&#39;interface utilisateur est liée à quelle variable.

![Clarté de l&#39;Identifiant](graph-creation-etiquette.resources/labelvsidentifier.png "Clarté de l&#39;Identifiant")

Essayez de faire correspondre vos étiquettes aux termes que vous utilisez dans les Cadres (étiquettes de Cadre) et les commentaires. Il est ainsi plus facile de savoir quelle section du graphe est liée à quel paramètre exposé

![Étiquettes de cadre et de paramètre correspondantes](graph-creation-etiquette.resources/match-labels.png "Étiquettes de cadre et de paramètre correspondantes")

### Paramètres

Lorsque vous exposez des paramètres, il est important de ne pas se limiter à l’étiquette et à l’Identifiant. Gardez à l’esprit les points suivants :

* Sélectionnez le type d’éditeur approprié. Un Slider n&#39;a pas toujours de sens : un élément Angle ou Dropdown Ui sont également possibles.
* Définissez les valeurs Min et Max appropriées et décidez si leur verrouillage est judicieux.
* Choisissez une valeur par défaut logique : les valeurs par défaut qui ne servent à rien doivent être évitées.
* Envisagez de remapper la plage via une [fonction](../../function-graphs/function-graphs.md)si nécessaire : un curseur de 0,125 à 0,357 n&#39;a aucun sens, vous pouvez facilement remapper cela avec une Interpolation linéaire et faire en sorte que l&#39;élément d&#39;interface utilisateur utilise une plage de 0 à 1.

## Graphes Substance

### Gestion des couleurs et des niveaux de gris

Une grande prudence est requise lors de l’utilisation des données de couleur et de niveaux de gris, car il est difficile de mélanger les deux types à la volée. Il convient de garder à l’esprit les points suivants :

* Les graphes ne doivent jamais contenir de liens (d’erreur) en pointillés rouges.
* Il ne doit pas y avoir de conversions inutiles entre la couleur et les niveaux de gris et vice versa. Dans certains cas, l’option « Insérer automatiquement le nœud de conversion couleur/niveaux de gris » dans les préférences par Graphe peut entraîner de longues chaînes inutiles de nœuds de conversion ancrés.
* Les données sont idéalement conservées le plus longtemps possible en niveaux de gris, et converties uniquement en cas de nécessité absolue. Cela réduit la complexité et réduit les performances.
* Les entrées et les sorties doivent être créées ou configurées avec le type approprié à l&#39;esprit : par exemple, il n&#39;est pas logique d&#39;avoir une entrée « masque » définie sur couleur si elle sera convertie en niveaux de gris pour une utilisation comme masque binaire.

![Conversions de couleurs et de niveaux de gris](graph-creation-etiquette.resources/colorgray01.png "Conversions de couleurs et de niveaux de gris")

### Contrôle de la résolution

Le contrôle de la résolution d&#39;un [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md) peut être déroutant. Vous devez donc faire preuve de prudence pour le faire correctement. En commettant des erreurs, vous risquez d’affecter gravement les performances ou de générer des résultats inutilisables de mauvaise qualité.

[Pour bien comprendre cette rubrique, assurez-vous de connaître les tailles de sortie absolues et relatives.](../../compositing-graphs/output-size/output-size.md)

* Un graphe doit être réglé sur une résolution « Relative au parent » dans presque tous les cas, à moins qu&#39;il n&#39;y ait une exception très spécifique où elle n&#39;est pas requise (très rare).
* Les nœuds ne doivent généralement pas avoir de paramètres de remplacement pour la taille de sortie. Dans la plupart des cas, il est préférable de contrôler la résolution via les propriétés Parent ou Graphe.
* Pour les bitmaps, veillez tout particulièrement à ce que la taille de sortie absolue par défaut ne s’étende pas à l’ensemble du Graphe. Dans ce cas, elle doit être remplacée par la taille Relatif au parent. Il s&#39;agit de l&#39;une des rares exceptions à la règle ci-dessus.
