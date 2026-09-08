---
helpx_url: ""
breadcrumb-title: ''
description: Découvrez les nœuds de Fonction SDF disponibles dans Designer, qui vous permettent de créer des Fonctions SDF pour générer des formes 3D dans les nœuds de la projection de formes éclaboussées v2 et 3D.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des Fonctions SDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '2573'
ht-degree: 0%

---


# Utilisation des Fonctions SDF

Dans la version 16.0.0, Substance 3D Designer a introduit un ensemble puissant de nœuds pour créer des Fonctions SDF, qui peuvent être utilisées pour créer et manipuler des formes 3D procédurales.

Les fonctions SDF sont des graphes de fonction de Substance qui associent des nœuds SDF disponibles dans l&#39;ensemble d&#39;outils et sont appliquées à des paramètres dédiés dans les nœuds qui prennent en charge les Fonctions SDF.

Comme point de départ, gardez à l’esprit que le workflow de base se présente comme suit :

1. Créez une Fonction SDF dans un nœud de [visionneuse 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) pour visualiser le résultat.
2. Copiez-le dans le graphe de fonction final (ou [instanciez-le](../../../../glossary/glossary.md#instance-node)) dans le paramètre de Fonction SDF d&#39;un nœud qui prend en charge les Fonctions SDF, tel que [Shape splatter v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).

<img style="display: block; margin: auto;" src="working-with-sdf-functions.resources/working-with-sdf-mograph.gif" alt="Monographie de la fonction Nœuds de Fonctions SDF 3D dans Substance 3D Designer" />

## Qu’est-ce qu’une Fonction SDF ?

<table style="border: none">
    <tr style="border: 0">
        <td style="border: 0; vertical-align: top">
            <p>Tout comme les fonctions mathématiques peuvent être tracées en 2D en tant que courbes, elles peuvent être tracées en 3D en tant que surfaces.</p><p>Un champ de distance signé est une fonction mathématique qui définit une surface dans un espace 3D en calculant la distance entre un point quelconque de l'espace et le point le plus proche de la surface.</p><p>Décomposons le nom « champ de distance signé » pour mieux le comprendre :<ul><li><b>Signé</b> signifie que la fonction renvoie une valeur positive si le point est à l'extérieur/devant la surface, une valeur négative si le point est à l'intérieur/derrière la surface et zéro si le point est exactement sur la surface.</li><li><b>Distance</b> fait référence au fait que la fonction calcule la distance entre n'importe quel point de l'espace et le point *le plus* de la surface.</li><li><b>Champ</b> signifie que la fonction décrit un champ de valeurs, car chaque point dans l'espace a une valeur correspondante qui représente sa distance à la surface la plus proche.</li></ul></p>
        </td>
        <td style="border: 0; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-what-is-an-sdf.gif" alt="Visualisation de la forme produite par une Fonction SDF, avec des isolignes de balayage." />
        </td>
    </tr>
</table>

Ces fonctions ont de nombreuses applications dans l&#39;infographie, telles que le dessin de surfaces, le converti d&#39;ombre, le masquage de contour, la détection de collision et plus encore.

Dans Substance 3D Designer, les Fonctions SDF sont utilisées pour créer et manipuler des formes 3D de manière procédurale.

### Sortie et utilisation prévue d&#39;une Fonction SDF

Les nœuds de fonction SDF génèrent une seule valeur flottante : la distance signée à la surface la plus proche.

Mais ils ne sont pas les seuls : ils obtiennent et définissent en interne les valeurs des variables que les nœuds hôtes doivent définir et/ou connaître pour manipuler et dessiner les formes obtenues.

Cela signifie que ces nœuds doivent être utilisés dans le cadre de nœuds qui *prennent en charge des Fonctions SDF*, car il connaît ces variables et les intègre en mode natif.

Les nœuds incluent [Shape splatter v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) et [Visualiseur 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md).

### Graphique de la fonction Substance

Les nœuds de fonction SDF sont destinés à être utilisés dans des graphes de fonction de Substance dédiés et ne sont donc disponibles que dans ce type de graphe.
Les paramètres de nœud destinés à être exprimés en tant que fonction utilisent un bouton « Modifier la fonction ».

Ce que vous devez savoir sur les graphes de fonction de Substance :
* Comme les graphes de Substance, les connecteurs de nœuds sont *spécialisés*, ce qui signifie qu&#39;ils ne peuvent être connectés qu&#39;à d&#39;autres connecteurs de *couleur correspondante* [représentant leur type](../../function-nodes-overview/function-nodes-overview.md#color-coding).
* Les nœuds n&#39;ont pas de paramètres, ils ne peuvent avoir que des entrées. (À quelques exceptions près)
* Le graphe a un seul nœud de sortie. Cliquez avec le bouton droit de la souris sur un nœud et sélectionnez `Set as output` pour le désigner comme nœud de sortie.
* De même que les graphes de Substance, il existe des nœuds *atomiques* (les composantes de base) et des nœuds *d&#39;instance* qui représentent d&#39;autres graphes de fonction de Substance.
* Il existe des opérateurs distincts (algébrique, logique et de comparaison) qui vous permettent d&#39;effectuer des opérations sur les valeurs du graphe, mais les nœuds SDF ont [leurs propres opérateurs](#operators)

+++ Exemple de graphe de fonction définissant une Fonction SDF

![working-with-sdf-function-graphe.png](working-with-sdf-functions.resources/working-with-sdf-function-graph.png)

+++

## Prise en main

Pour créer des Fonctions SDF, nous devons d&#39;abord les visualiser afin de comprendre l&#39;effet des nœuds et des paramètres que nous ajustons.

Le nœud de la [visionneuse 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) dispose d&#39;un mode dédié pour visualiser les formes créées à l&#39;aide de Fonctions SDF : définissez le paramètre <b>Type de Scène</b> du nœud sur `SDF function` et cliquez sur le bouton **Modifier la fonction** pour ouvrir le graphe de fonction qui hébergera la Fonction SDF elle-même.

Le nœud offre des fonctionnalités dédiées pour visualiser les aspects de la Fonction SDF qui nous permettront de les construire de manière plus intuitive et efficace, telles qu’un cadre de délimitation et des lignes d’isolement.

Le nœud [Soleil/ciel physique](../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/physical-sun-sky/physical-sun-sky.md) peut être utilisé pour configurer rapidement l&#39;éclairage de l&#39;environnement dans la visionneuse 3D.

<img style="margin-top: 32px; margin-bottom: 32px;" src="./working-with-sdf-functions.resources/working-with-sdf-setup.gif" alt="Configuration du nœud de la visionneuse 3D pour la visualisation des Fonctions SDF." />

>[!TIP]
> 
> <table style="border: none"><tr style="border: none"><td style="border: none; vertical-align: top"><p>Tous les nœuds de Fonction SDF de données, ainsi que leurs connecteurs d’entrée, disposent d’info-bulles qui vous permettent d’en savoir plus sur leur objectif et leur utilisation.</p><p>N'oubliez pas de les vérifier !</p></td><td style="border: none; width: 33%; vertical-align: top"><img src="./working-with-sdf-functions.resources/working-with-sdf-tooltips.png" alt="Info-bulle du connecteur d’entrée sur le nœud de Fonction SDF." /></td></tr></table>

### Définition des valeurs de nœud

Comme pour tous les nœuds des graphes de fonction de Substance, les nœuds de Fonction SDF n&#39;ont pas de paramètres, mais uniquement des connecteurs d&#39;entrée qui sont utilisés comme paramètres.

Pour définir la valeur de ces entrées, vous pouvez utiliser des [nœuds constants](../../atomic-function-nodes/constant-nodes/constant-nodes.md) tels que **Flottant**, **Flottant 3** et **Entier 3**.\
Vous pouvez les créer de la manière habituelle via le menu Nœud ou vous pouvez faire glisser une nouvelle connexion à partir des connecteurs pour bénéficier d&#39;une liste filtrée de nœuds de types correspondants.

La plupart des connecteurs d’entrée des nœuds de Fonction SDF ont une valeur par défaut, qui est indiquée dans son infobulle.

<img style="margin-top: 32px; margin-bottom: 32px" src="working-with-sdf-functions.resources/working-with-sdf-constants.gif" alt="Nœuds constants utilisés pour modifier les primitives SDF." />

>[!TIP]
> 
> <table style="border: none"><tr style="border: none"><td style="border: none; vertical-align: top"><p>Si vous n'avez pas besoin de toujours afficher certaines valeurs, ancrez les nœuds à l'aide de la touche <code>D</code> pour économiser de l'espace et désencombrer le graphe.</p><p>Vous pouvez également utiliser des commentaires pour suivre les valeurs.</p></td><td style="border: none; width: 67%; vertical-align: top"><img src="./working-with-sdf-functions.resources/working-with-sdf-docked-nodes.png" alt="Info-bulle du connecteur d’entrée sur le nœud de Fonction SDF." /></td></tr></table>


### Cadre de délimitation

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>Le cadre de contour est une zone dans l'espace 3D qui définit les <i>limites</i> dans lesquelles la Fonction SDF est évaluée et dessinée dans le nœud <a href="../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md">Forme éclaboussée v2</a>.</p><p>Si le cadre de délimitation est trop petit, des parties de la forme peuvent être rognées. S'il est trop volumineux, il peut entraîner des calculs inutiles et des délais de traitement plus longs.</p><p>Le paramètre <b>cadre de délimitation</b> vous permet d'activer la visualisation du cadre de délimitation. Vous pouvez ensuite ajuster la taille du cadre de sélection en modifiant les valeurs du paramètre <b>Taille du cadre de sélection</b>.</p><p>Utilisez le paramètre <b>Coloriser hors cadre</b> pour visualiser les zones en dehors du cadre de délimitation en rouge vif afin de pouvoir ajuster le cadre en conséquence.</p>
        </td>
        <td style="border: none; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-bounding-frame.jpg" alt="Fonction Cadre de délimitation du nœud de la visionneuse 3D, pour les Fonctions SDF." />
        </td>
    </tr>
</table>

### Isolignes

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>Comme le transformé des formes implique de *transformer l'espace* dans lequel elles sont dessinées, le résultat des nœuds utilisés après certaines transformations peut être surprenant.<br>Dans ce cas, il est utile de visualiser l'espace lui-même. Pour ce faire, <i>visualisez le champ de distance</i> de la forme.</p><p>Pour cela, le nœud de la visionneuse 3D utilise des <i>isolignes</i>, qui répètent des lignes de contour représentant une distance donnée de la surface de la forme. Le paramètre <b>SDF isolines</b> active cette visualisation.<br>Les isolignes sont dessinées sur un plan horizontal placé à l'height spécifié par le paramètre <b>Position des isolignes SDF</b>.</p><p>Voir comment les lignes d’isolement sont déformées par les transformations appliquées à la forme peut vous aider à comprendre comment la forme elle-même est transformée et à ajuster les paramètres des nœuds en conséquence.</p>
        </td>
        <td style="border: none; width: 33%; vertical-align: top">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-isolines.jpg" alt="Fonction Cadre de délimitation du nœud de la visionneuse 3D, pour les Fonctions SDF." />
        </td>
    </tr>
</table>

## Catégories de nœuds de fonction SDF

Les nœuds de fonctions SDF sont classés dans la bibliothèque en fonction de leur fonction et de leur objectif.

Vous pouvez créer autant de vues Bibliothèque que nécessaire pour organiser votre espace de travail de sorte que l’ensemble d’outils Fonctions SDF soit organisé par catégorie tout en gardant le tout à portée de main. Accédez à la vue **Windows > Nouvelle bibliothèque** pour ajouter des vues distinctes et indépendantes de la bibliothèque.

+++ Exemple d’espace de travail

![working-with-sdf-workspace.png](working-with-sdf-functions.resources/working-with-sdf-workspace.png)

+++

### Primitives

Les blocs de construction de base de Fonctions SDF, qui vous permettent de créer des formes de base telles que des sphères, des boîtes, des cylindres et plus encore.

+++ Nœuds

[Cône coiffé](./sdf-functions-primitives/3d-sdf-capped-cone/3d-sdf-capped-cone.md)\
[Cône coiffé (2 points)](././sdf-functions-primitives/3d-sdf-capped-cone-2-points/3d-sdf-capped-cone-2-points.md)\
[Torus coiffé](./sdf-functions-primitives/3d-sdf-capped-torus/3d-sdf-capped-torus.md)\
[Capsule](./sdf-functions-primitives/3d-sdf-capsule/3d-sdf-capsule.md)\
[Cône](./sdf-functions-primitives/3d-sdf-cone/3d-sdf-cone.md)\
[Cube](./sdf-functions-primitives/3d-sdf-cube/3d-sdf-cube.md)\
[Cylindre](./sdf-functions-primitives/3d-sdf-cylinder/3d-sdf-cylinder.md)\
[Cylindre (2 points)](./sdf-functions-primitives/3d-sdf-cylinder-2-points/3d-sdf-cylinder-2-points.md)\
[Ellipsoïde](./sdf-functions-primitives/3d-sdf-ellipsoid/3d-sdf-ellipsoid.md)\
[Cylindre allongé](./sdf-functions-primitives/3d-sdf-elongated-cylinder/3d-sdf-elongated-cylinder.md)\
[Plan au sol](./sdf-functions-primitives/3d-sdf-ground-plane/3d-sdf-ground-plane.md)\
[Hélice](./sdf-functions-primitives/3d-sdf-helix/3d-sdf-helix.md)\
[Prisme hexagonal](./sdf-functions-primitives/3d-sdf-hexagonal-prism/3d-sdf-hexagonal-prism.md)\
[Plan infini](./sdf-functions-primitives/3d-sdf-infinite-plane/3d-sdf-infinite-plane.md)\
[Plan](./sdf-functions-primitives/3d-sdf-plane/3d-sdf-plane.md)\
[Pyramide](./sdf-functions-primitives/3d-sdf-pyramid/3d-sdf-pyramid.md)\
[Pyramide carrée](./sdf-functions-primitives/3d-sdf-pyramid-square/3d-sdf-pyramid-square.md)\
[Rock](./sdf-functions-primitives/3d-sdf-rock/3d-sdf-rock.md)\
[Sphère](./sdf-functions-primitives/3d-sdf-sphere/3d-sdf-sphere.md)\
[Torus](./sdf-functions-primitives/3d-sdf-torus/3d-sdf-torus.md)

+++

### Opérateurs

Ces nœuds vous permettent de combiner et de modifier des formes créées avec des primitives. Il s&#39;agit notamment :
* Les opérateurs **booléens droits** tels que [Union](sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md), [Intersection](sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md) et [Soustraction](sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md) vous permettent d&#39;associer des formes de différentes manières.
* Opérateurs **booléens de déformation** tels que [Arrondi](sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md) et [Morphe](sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md) qui vous permettent d&#39;associer des formes avec un effet de fusion.
* **Autres opérateurs spécialisés** tels que [Shell](sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md) et [Symétrie](sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md) qui vous permettent de modifier et/ou de dupliquer une forme.

+++ Nœuds

[Intersection](./sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md)\
[Intersection lisse](./sdf-functions-operators/3d-sdf-op-intersection-smooth/3d-sdf-op-intersection-smooth.md)\
[Surface d&#39;intersection](./sdf-functions-operators/3d-sdf-op-intersection-surface/3d-sdf-op-intersection-surface.md)\
[Morphe](./sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md)\
[Répéter le miroir](./sdf-functions-operators/3d-sdf-op-repeat-mirror/3d-sdf-op-repeat-mirror.md)\
[Arrondi](./sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md)\
[Shell](./sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md)\
[Soustraction](./sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md)\
[Soustraction lisse](./sdf-functions-operators/3d-sdf-op-subtraction-smooth/3d-sdf-op-subtraction-smooth.md)\
[Symétrie](./sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md)\
[Union](./sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md)\
[Chanfrein d&#39;union](./sdf-functions-operators/3d-sdf-op-union-chamfer/3d-sdf-op-union-chamfer.md)\
[Union fluide](./sdf-functions-operators/3d-sdf-op-union-smooth/3d-sdf-op-union-smooth.md)

+++

### Transformations

Les formes peuvent être transformées de différentes manières, par exemple en étant [translatées](sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md), [tournées](sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md), [mises à l’échelle](sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md), [torsadées](sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md) et plus encore.
Ces nœuds vous permettent d&#39;effectuer ces transformations en *transformant l&#39;espace lui-même* dans lequel les surfaces sont définies.

Cet espace est appelé `P`. Passez à la section suivante pour en savoir plus sur ce que cela signifie et sur le fonctionnement de la transformation d&#39;espace.

+++ Nœuds

[Courbure](./sdf-functions-transforms/3d-sdf-transform-bend/3d-sdf-transform-bend.md)\
[Allongé](./sdf-functions-transforms/3d-sdf-transform-elongate/3d-sdf-transform-elongate.md)\
[Symétrie](./sdf-functions-transforms/3d-sdf-transform-flip/3d-sdf-transform-flip.md)\
[Décalage](./sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md)\
[Décalage P](./sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md)\
[Rotation](./sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md)\
[Rotation P](./sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md)\
[Échelle](./sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md)\
[Torsion](./sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md)

+++

### Matériau

La gestion de matériau de base est disponible pour les formes créées à l’aide de Fonctions SDF.

Vous pouvez définir des attributs de matériau de base : couleur, rugosité et métallisation, à utiliser pour la visualisation directe dans le nœud de la visionneuse 3D ou comme base pour le travail de matériau dans les nœuds Shape Splatter v2.\
Vous pouvez également attribuer des ID de matériau à différentes parties d’une forme pour les séparer.

En savoir plus sur les applications de ces nœuds [ci-dessous](#material-id).

+++ Nœuds

* [Définir l’ID de matériau](./sdf-functions-material/set-id/set-id.md)
* [Définir le matériau](./sdf-functions-material/set-material/set-material.md)
* [Définir la couleur](./sdf-functions-material/set-color/set-color.md)
* [Définir la métallisation](./sdf-functions-material/set-metalness/set-metalness.md)
* [Définir la rugosité](./sdf-functions-material/set-roughness/set-roughness.md)

+++

## Entrée « P »

Lorsque nous appliquons une transformation à une forme, telle qu’un décalage ou une rotation, nous transformons en fait l’espace dans lequel la forme est définie.

Si nous voulons qu’une transformation se propage à d’autres formes, par exemple si nous voulons faire pivoter plusieurs formes de la même manière, nous devons nous assurer qu’elles utilisent toutes le même espace transformé.

Un espace transformé est partagé entre les nœuds à l&#39;aide de leur entrée `P` dédiée, disponible dans la plupart des nœuds SDF.\
Le « P » signifie espace monde **P** osition : un vecteur 3D représentant les coordonnées d&#39;un point dans l&#39;espace monde.

Les nœuds [Décalage P](sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md) et [Rotation P](sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md) transforment l&#39;espace et vous permettent de propager cette transformation à tous les nœuds qui doivent l&#39;hériter.\
Par exemple, plusieurs formes peuvent être tournées ensemble en connectant leur entrée `P` au même nœud Rotation P.

Il ne s&#39;agit pas simplement d&#39;une question de commodité, il s&#39;agit de s&#39;assurer que les nœuds SDF fonctionnent avec les mêmes positions dans l&#39;espace.

Voici un exemple :

![working-with-sdf-p-input.gif](working-with-sdf-functions.resources/working-with-sdf-p-input.gif)

Une sphère est créée pour visualiser l’espace sous la forme d’une grille 3D. Il est répété en *répétant l&#39;espace*.\
Sans `P` partagé, le cylindre recourbé utilise l&#39;espace de répétition utilisé par la sphère.\
Avec un `P` partagé, les formes peuvent être correctement définies dans un espace partagé pivoté.</p>

## Utilisation de Fonctions SDF dans les nœuds « Shape splatter v2 »

Une fois que vous avez terminé une Fonction SDF dans le contexte du nœud de la visionneuse 3D, vous pouvez copier l&#39;intégralité de la fonction et la coller dans le nœud [Shape splatter v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) pour l&#39;utiliser comme générateur de forme pour ce nœud.

Définissez le paramètre **Type de forme** sur `SDF function`, puis accédez au paramètre **Fonction SDF de motif** et cliquez sur le bouton **Modifier la fonction** pour ouvrir le graphe de fonction du paramètre.
Vous pouvez ensuite coller la fonction que vous avez copiée à partir du nœud de la visionneuse 3D dans ce graphe. (N&#39;oubliez pas de redéfinir le nœud de sortie du graphe de fonction !)

Assurez-vous d&#39;ajuster la taille du cadre de délimitation **SDF** pour qu&#39;elle corresponde au [cadre de délimitation](#the-bounding-frame) que vous utilisiez dans le nœud de la visionneuse 3D, et assurez-vous que la forme est dessinée correctement.

![working-with-sdf-shape-splatter-v2.png](working-with-sdf-functions.resources/working-with-sdf-shape-splatter-v2.png)\
*Forme éclaboussée v2 avec un **type de forme**&#x200B;défini sur `SDF function`. Notez que la taille du cadre de délimitation **SDF**&#x200B;a été ajustée pour s&#39;adapter à la forme.*

>[!TIP]
> 
> Pour réutiliser facilement une Fonction SDF, copiez-la dans un nouveau graphe de fonction de Substance et utilisez ce graphe comme **instancier** dans les nœuds de la visionneuse 3D et de l&#39;éclaboussure de forme v2.
> 
> Cela présente plusieurs avantages :
> * Toute mise à jour de la fonction sera répercutée sur les deux nœuds sans qu’il soit nécessaire de la copier-coller à nouveau. Il s’agit d’une excellente amélioration de la qualité de vie pour les formes complexes.
> * Le graphe peut avoir un nom descriptif qui sera visible dans les instanciers, ce qui rendra l’utilisation de votre propre bibliothèque de formes SDF beaucoup plus facile à gérer et vos graphes plus lisibles.
> * Vous pouvez créer des entrées pour le graphe de fonction que vous pouvez utiliser avec les nœuds [Get](../../atomic-function-nodes/get-nodes/get-nodes.md). Ces entrées seront exposées en tant que connecteurs d’entrée dans l’instancier et vous permettront de modifier facilement vos formes.

### ID de matériau

Un ID de matériau peut être attribué à une forme SDF. Il s&#39;agit d&#39;une valeur d&#39;entier qui peut être utilisée pour différencier des parties de la forme et leur attribuer différents matériaux dans les nœuds [Visualiseur 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md) et [Éclaboussure de forme v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).

Notez que les surfaces dotées d&#39;ID de matériau différents sont divisées par un bord net entre les formes dégradées, comme le montre l&#39;exemple ci-dessous.

Utilisez le nœud [Définir l&#39;ID de matériau](./sdf-functions-material/set-id/set-id.md) après la partie d&#39;une forme que vous souhaitez baliser avec un ID de matériau spécifique, et utilisez un nœud constant [Entier](../../atomic-function-nodes/constant-nodes/constant-nodes.md) pour définir la valeur d&#39;ID de matériau souhaitée.\
Dans le nœud de la visionneuse 3D, définissez le paramètre **Sortie** sur `Material ID` pour visualiser les ID de matériau des formes.

![working-with-sdf-matériau-id.png](working-with-sdf-functions.resources/working-with-sdf-material-id-01.png)\
*À droite, la sortie de deux nœuds de visualiseur 3D est composée pour afficher la forme (à gauche) et ses ID de matériau (à droite) afin d&#39;illustrer comment, dans les formes fusionnées, les matériaux sont interpolés tandis que les ID de matériau sont divisés.*

Les ID de matériau peuvent être exploités par les nœuds compagnon Shape Splatter v2 :
* [Les nœuds du mappeur v2 d&#39;éclaboussures de forme](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md) peuvent utiliser ces ID de matériau pour attribuer différents modèles.
* [L&#39;éclaboussure de forme v2 pour masquer](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md) peut masquer une partie des formes en fonction de leur ID de matériau.

<table style="border: none; margin-top: 32px">
    <tr style="border: 0">
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-06.jpg" alt="ID de matériau SDF pour le mappage des couleurs dans le nœud de couleurs du mappeur Shape Splatter v2."/><i>ID de Matériau utilisés pour le mappage des couleurs<br>dans la couleur du mappeur Shape splatter v2</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-04.jpg" alt="ID de matériau SDF pour le mappage triplanaire dans le nœud de couleur du mappeur Shape Splatter v2."/><i>ID de Matériau utilisés pour le mappage triplanaire<br>dans la couleur du mappeur Shape splatter v2</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-material-id-05.jpg" alt="ID de matériau SDF pour le masquage dans Shape splatter v2 vers le nœud de masque."/><br><i>ID de Matériau utilisés pour le masquage<br>dans Shape splatter v2 to mask</i>
        </td>
    </tr>
</table>

### Couleur, rugosité et métallurgie

Les nœuds [Définir la couleur](./sdf-functions-material/set-color/set-color.md), [Définir la rugosité](./sdf-functions-material/set-roughness/set-roughness.md) et [Définir la métallisation](./sdf-functions-material/set-metalness/set-metalness.md) vous permettent de définir ces attributs de matériau pour les formes de la Fonction SDF.

Ensuite, lorsque vous utilisez cette Fonction SDF comme type de forme dans le nœud [Shape splatter v2](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md), ces attributs de matériau seront disponibles en tant que mappages dans les sorties **SDF color**, **SDF rugosité** et **SDF metalness** du nœud. Ces mappages peuvent servir de base à des travaux de matériau plus complexes utilisant d&#39;autres nœuds.

Notez que, contrairement aux ID de matériau, les valeurs sont *interpolées* entre les formes fusionnées sous la forme d&#39;un dégradé, comme le montrent les exemples ci-dessous.

<table style="border: none; margin-top: 32px">
    <tr style="border: 0">
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-color.jpg" alt="Sortie de couleur SDF du nœud Shape splatter v2."/><i>Sortie couleur SDF</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-roughness.jpg" alt="Rugosité SDF du nœud Shape splatter v2."/><br><i>Sortie de rugosité SDF</i>
        </td>
        <td style="border: 0; width: 33%">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-metalness.jpg" alt="Métallique SDF du nœud Shape splatter v2."/><i>Sortie de métallurgie SDF</i>
        </td>
    </tr>
</table>

### échantillon de matériau

<table style="border: none">
    <tr style="border: none">
        <td style="border: none; vertical-align: top">
            <p>L'<b>échantillon de matériau</b> <a href="../../../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md">boulons rouillés</a> est disponible pour passer aux Fonctions SDF appliquées dans le contexte du nœud Shape splatter v2.</p><p>Le graphe est organisé et annoté pour vous guider à travers sa structure, les paramètres de nœud et les configurations de Fonction SDF.</p><p>Il est également <i>entièrement modifiable</i>. Il peut donc être utilisé comme sandbox pour mieux comprendre de manière pratique les outils Shape splatter v2 et Fonctions SDF. Vous pouvez créer autant de graphes d'exemple que vous le souhaitez, alors n'hésitez pas à jouer !</p>
        </td>
        <td style="border: none; width: 20%; vertical-align: top; text-align: right">
            <img src="./working-with-sdf-functions.resources/working-with-sdf-functions-material-sample.png" alt="Fonction de cadre de délimitation du nœud de la visionneuse 3D, pour les Fonctions SDF." />
        </td>
    </tr>
</table>
