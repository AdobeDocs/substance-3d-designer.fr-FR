---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/working-with-3d-scenes/extracting-materials-values-and-textures.html"
breadcrumb-title: ''
description: Extrayez les propriétés de matériau des scènes 3D pour les utiliser dans les graphes de Substance pour les workflows de création de matériaux.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Extracting materials values and textures
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extraction de valeurs et de textures de matériaux
user-guide-description: ''
user-guide-title: ''
source-git-commit: fa12f0ba789f700924fa0a6f3cbc0726c5f468e9
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 0%

---


# Extraction de valeurs et de textures de matériaux

Les propriétés des matériaux peuvent être extraites pour être utilisées dans des graphes de Substance.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Nouveau graphe à partir des textures

</td>
<td style="border: 0;" valign="top">

### Extraire la texture

</td>
<td style="border: 0;" valign="top">

### Extraire une valeur

</td>
</tr>
</table>

## Nouveau graphe à partir des textures

L’action Créer un graphe à partir des données de texture crée un graphe de Substance avec toutes les textures utilisées par un matériau

Voici quelques opérations qui peuvent se produire lorsque vous utilisez cette action :

* Un graphe de Substance portant le nom du matériau est créé à l’emplacement sélectionné.
* Une [ressource bitmap](../../resources/bitmap-resource/bitmap-resource.md) est créée pour chaque texture utilisée par le matériau et placée dans un dossier nommé d&#39;après le matériau, sous un dossier « Resources ».
* Dans le graphe, des nœuds [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) sont créés pour chacune de ces ressources bitmap et automatiquement connectés aux nœuds [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configurés après les propriétés du matériau à l&#39;aide des textures.
* Si chaque canal d&#39;une même texture est utilisé pour piloter différentes propriétés de matériau (cette technique est appelée [packing de canal](../../glossary/glossary.md)), des nœuds de [conversion en niveaux de gris](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md) sont automatiquement ajoutés pour sélectionner les canaux appropriés.
* Le graphe est automatiquement connecté au matériau et son apparence ne doit pas changer tant que vous n’avez pas effectué de modifications dans le graphe.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Créer un graphe à partir des entrées de texture - Action dans le viewport « vue 3D »](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionViewport.png "Créer un graphe à partir des entrées de texture - Action dans le viewport « vue 3D »"){zoomable="yes"}

*Action dans le viewport vue 3D*

</td>
<td style="border: 0;" valign="top">

![Créer un graphe à partir des entrées de texture - Action dans le menu « Matériaux »](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionMaterials.png "Créer un graphe à partir des entrées de texture - Action dans le menu « Matériaux »"){zoomable="yes"}

*Action dans le menu Matériaux*

</td>
<td style="border: 0;" valign="top">

![Créer un graphe à partir des entrées de texture - Action dans le dock « Propriétés »](extracting-materials-values-and-textures.resources/createGraphFromTexturesActionProps.png "Créer un graphe à partir des entrées de texture - Action dans le dock « Propriétés »"){zoomable="yes"}

*Action dans le dock des propriétés*

</td>
</tr>
</table>

![Résultat de la création de graphe à partir de textures de matériau](extracting-materials-values-and-textures.resources/createGraphFromTexturesResult.png "Résultat de la création de graphe à partir de textures de matériau"){zoomable="yes"}

*Résultat de la création du graphe à partir des textures de matériau*

+++Démonstration
![Créer un graphe à partir d&#39;entrées de texture - Démonstration](extracting-materials-values-and-textures.resources/createGraphFromTextures.gif "Créer un graphe à partir d&#39;entrées de texture - Démonstration"){zoomable="yes"}



+++

>[!TIP]
>
> Vous pouvez accéder à l&#39;action rapidement et directement dans le viewport vue 3D en plaçant le curseur sur l&#39;objet et en appuyant sur <b>Maj+LMB</b> pour le sélectionner. puis en cliquant sur RMB pour accéder à un menu contextuel hébergeant l’action.

>[!NOTE]
>
> Pour les formats utilisant des *textures intégrées* (par exemple : USDZ), les textures doivent être extraites et copiées sur le disque. Cela entraîne une étape supplémentaire pour sélectionner l’emplacement vers lequel les textures doivent être extraites.

## Extraire la texture

L’action Extraire la texture vers le graphe crée un nouveau nœud Bitmap dans un graphe existant pour une texture utilisée par un matériau.

Voici quelques opérations qui peuvent se produire lorsque vous utilisez cette action :

* Une [ressource bitmap](../../resources/bitmap-resource/bitmap-resource.md) est créée pour la texture utilisée par le matériau et placée dans un dossier nommé d&#39;après le matériau, sous un dossier « Resources ».
* Dans le graphe sélectionné, un nœud [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) est créé pour cette texture bitmap et automatiquement connecté à un nœud [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configuré après la propriété matériau à l&#39;aide de ces ressources.

Si une sortie configurée pour la propriété de matériau *existe déjà* dans le graphe, alors *aucun nœud n&#39;est créé* et seule la création de ressource bitmap est effectuée.

Par exemple : l’extraction d’une texture pour la propriété « Base color » vers un graphe hébergeant déjà un nœud de sortie configuré pour « Base color » n’entraîne la création d’aucun nœud dans le graphe.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Extraire la texture vers le graphe - Action dans le dock des propriétés](extracting-materials-values-and-textures.resources/extractTextureAction.png "Extraire la texture vers le graphe - Action dans le dock des propriétés"){zoomable="yes"}

Action pour la propriété de matériau dans le dock Propriétés

</td>
<td style="border: 0;" valign="top">

![Extraire la texture vers le graphe - boîte de dialogue « Sélectionner le graphe de destination »](extracting-materials-values-and-textures.resources/extractTextureSelectGraph.png "Extraire la texture vers le graphe - boîte de dialogue « Sélectionner le graphe de destination »"){zoomable="yes"}

Boîte de dialogue Sélectionner le graphe de destination

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

![Résultat de l&#39;extraction de texture](extracting-materials-values-and-textures.resources/extractTextureResult.png "Résultat de l&#39;extraction de texture"){zoomable="yes"}

Résultat de l&#39;extraction de texture

+++Démonstration
![Extraire la texture vers le graphe - Démonstration](extracting-materials-values-and-textures.resources/extractTextureToGraph.gif "Extraire la texture vers le graphe - Démonstration"){zoomable="yes"}



+++

L’action Extraire la texture sous forme de ressource crée uniquement une ressource bitmap pour la texture utilisée par le matériau et la place dans un dossier nommé d’après le matériau, sous un dossier « Ressources ».

>[!NOTE]
>
> Pour les formats utilisant des *textures intégrées* (par exemple : USDZ), la texture doit être extraite et copiée sur le disque. Cela entraîne une étape supplémentaire pour sélectionner l’emplacement vers lequel la texture doit être extraite.

## Extraire une valeur

L&#39;action Extraire la valeur vers le graphe crée un nouveau nœud [Processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) dans un graphe existant pour une valeur de propriété de matériau.

Voici quelques opérations qui peuvent se produire lorsque vous utilisez cette action :

* Dans le graphe sélectionné, un nœud [Processeur de valeurs](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) est créé pour cette valeur de propriété et automatiquement connecté à un nœud [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) configuré après cette propriété de matériau.
* Dans le [graphe de la fonction de Substance](../../function-graphs/function-graphs.md) du nœud de Processeur de valeurs, un [nœud constant](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) correspondant au type de valeur est créé, défini sur la valeur extraite telle que définie comme sortie du graphe.

Si une sortie configurée pour la propriété de matériau *existe déjà* dans le graphe, alors *aucun nœud n&#39;est créé*.

Par exemple : l’extraction d’une valeur pour la propriété « Anisotropy level » vers un graphe hébergeant déjà un nœud de sortie configuré pour « Anisotropy level » n’entraîne la création d’aucun nœud dans le graphe.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Extraire la valeur vers le graphe - Action dans le dock des propriétés](extracting-materials-values-and-textures.resources/extractValueAction.png "Extraire la valeur vers le graphe - Action dans le dock des propriétés"){zoomable="yes"}

Action pour la propriété de matériau dans le dock Propriétés

</td>
<td style="border: 0;" valign="top">

![Extraire la valeur vers le graphe - boîte de dialogue « Sélectionner le graphe de destination »](extracting-materials-values-and-textures.resources/extractValueSelectGraph.png "Extraire la valeur vers le graphe - boîte de dialogue « Sélectionner le graphe de destination »"){zoomable="yes"}

Boîte de dialogue Sélectionner le graphe de destination

</td>
<td style="border: 0;" valign="top">

![Extraire la valeur vers le graphe - Nœud constant dans la fonction du nœud de Processeur de valeurs](extracting-materials-values-and-textures.resources/extractValueResult2.png "Extraire la valeur vers le graphe - Nœud constant dans la fonction du nœud de Processeur de valeurs"){zoomable="yes"}

Nœud constant dans la fonction du nœud de Processeur de valeurs

</td>
</tr>
</table>

![Résultat de l&#39;extraction de valeur](extracting-materials-values-and-textures.resources/extractValueResult.png "Résultat de l&#39;extraction de valeur"){zoomable="yes"}

Résultat de l’extraction de valeur

+++Démonstration
![Extraire la valeur vers le graphe - Démonstration](extracting-materials-values-and-textures.resources/extractValueToGraph.gif "Extraire la valeur vers le graphe - Démonstration"){zoomable="yes"}



+++
