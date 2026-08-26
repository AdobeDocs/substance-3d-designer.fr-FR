---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Découvrez les consignes à suivre pour réduire la taille des fichiers de graphiques en Substance afin d’optimiser les performances et les besoins de stockage.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Directives de réduction de la taille des fichiers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# Vue d’ensemble

Dans certains cas, la taille totale des fichiers de [ressources Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) peut être un facteur important. Cette page couvre quelques domaines et paramètres importants à garder à l’esprit lorsque vous tentez de réduire la taille des fichiers.

La taille des fichiers est principalement déterminée par les [bitmaps incorporés](../../resources/bitmap-resource/bitmap-resource.md). Ce sont des fichiers liés, incorporés ou préparés et ajoutés au fichier [Substance 3D Designer](https://www.adobe.com/fr/products/substance3d-designer.html) (SBS) en tant que ressource. Seules les images bitmap utilisées dans un graphique (c’est-à-dire connectées à une sortie directement ou via la chaîne de nœuds) sont publiées dans la ressource Substance 3D. Dans un fichier Substance 3D, les bitmaps n’ont aucun impact sur la taille du fichier, car toutes les ressources bitmap sont toujours stockées en dehors du fichier.

>[!IMPORTANT]
>
> Assurez-vous que la propriété [Taille de sortie](../../compositing-graphs/output-size/output-size.md) de tous les nœuds [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) est définie sur la [méthode d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) *absolue*. Si ce n&#39;est pas le cas, leur [ressource Bitmap](../../resources/bitmap-resource/bitmap-resource.md) référencée sera enregistrée à la résolution 256\*256 par défaut dans le fichier de ressources Substance 3D publié, ce qui* impactera la qualité* d&#39;une ou plusieurs sorties.

## Facteurs de taille de fichier

Il y a quelques facteurs différents qui affectent la taille totale des fichiers du SBSAR. Ils sont répertoriés ci-dessous avec une brève explication.

+++Résolution
De toute évidence, cela a un effet important. Utilisez la plus petite résolution possible, en gardant à l’esprit que vous pouvez également souhaiter que votre fichier de Substance fonctionne avec des résolutions plus importantes. Vous pouvez utiliser des astuces de masquage de résolution standard pour faire paraître des bitmaps plus petits plus grands.

*Détecté dans : un logiciel externe ou un bitmap d&#39;importation/réexportation dans Designer.*

+++

+++Mode colorimétrique du fichier
Défini dans votre éditeur d’image avant l’exportation, le mode colorimétrique a également un effet sur la taille des fichiers lors de l’utilisation du format bitmap Raw. Seules les images bitmap en niveaux de gris sont plus petites que les images RGB(A).

*Détecté dans : un logiciel externe ou un bitmap d&#39;importation/réexportation dans Designer lors de la configuration correcte de [nœuds de sortie](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).*

+++

+++Format du fichier
Le format de fichier de vos images fait une différence, bien qu’elle puisse être ignorée dans certains cas. Un programme comme Photoshop permet un peu plus de contrôle sur la compression JPG et peut parfois offrir un juste milieu.

*Détecté dans : un logiciel externe ou un bitmap d&#39;importation/réexportation dans Designer.*

+++

+++Utilisation dans le graphique
Le mode défini pour le nœud Bitmap influe également sur la manière dont Designer compresse le fichier. L’utilisation d’un fichier en mode Niveaux de gris comme image bitmap couleur dans le graphique produit des fichiers plus volumineux. Assurez-vous de les définir correctement !

*Trouvé dans :[Propriétés du nœud bitmap.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++Format bitmap dans le package
Dans les propriétés de la ressource, vous pouvez choisir entre la compression « Brut » et « Jpeg ». Cela peut avoir un effet considérable sur le résultat final.

*Trouvé dans : Propriétés de la ressource Bitmap, via la fenêtre de l&#39;Explorateur.*

+++

+++Qualité de compression bitmap dans le package
Lors de l’utilisation du format bitmap « Jpeg », le curseur ci-dessous peut affecter la qualité et la taille du fichier. Ce curseur n&#39;a pas un comportement très prévisible, mais 1 tend à correspondre à la compression JPG de qualité la plus élevée, et 0,5 tend à donner la plus petite taille.

*Trouvé dans : Propriétés de la ressource Bitmap, via la fenêtre de l&#39;Explorateur.*

+++

+++Mode de compression lors de la publication
Lors de la publication sur SBSAR, vous avez le choix entre « Auto », « Optimal » et « Aucun » pour la compression ; ces choix peuvent faire une différence considérable si vous utilisez le format bitmap « Raw ». A également un impact important sur la vitesse d&#39;exportation. Généralement déconseillé d&#39;utiliser « aucun » car il n&#39;offre aucune amélioration de la qualité.

*Trouvé dans : paramètres de publication finaux pour un package SBSAR.*

+++

## Comparaison des tailles de fichiers

Le tableau ci-dessous illustre l’influence réciproque de tous les paramètres. L’image bitmap utilisée est une image 4 096 x 4 096 de bruit généré, exportée à partir de Photoshop en tant que TGA 24 bits ou JPG en qualité 8. Les balises ont également été exportées en mode Niveaux de gris et RVBA.

Le graphique ne place qu’un seul nœud Bitmap connecté à une seule sortie. Le mode Bitmap est défini en fonction du mode du fichier source.

Bien que le tableau de droite ne soit pas entièrement concluant, voici ce qui peut être appris en comparant les résultats visuels et les tailles de fichiers :

* L’option Optimale pour le bitmap brut et la compression offre la meilleure qualité avec une taille de fichier acceptable.
* Les fichiers source précompressés permettent dans la plupart des cas de réduire la taille des fichiers, mais à un coût de qualité réduit.
* Les fichiers de plus petite taille, mais de moins bonne qualité sont obtenus avec le format d’assemblage JPG à la qualité 0.5.
* Les niveaux de gris ne sont pas toujours plus petits dans la taille des fichiers, mais ils sont de meilleure qualité que les couleurs dans des paramètres similaires.

>[!NOTE]
>
> **Format Bitmap Jpeg**
> 
> Il est important de noter que les cartes spéciales qui nécessitent une grande précision, telles que les cartes de normales, les cartes vectorielles et autres, ne doivent probablement pas être définies sur la compression Jpeg, car cela conduira à des artefacts beaucoup plus visibles !

| Image source | Balise de couleur | Mot de passe JPG couleur | Grayscale TGA | Mot de passe JPG Niveaux de gris |
| --- | --- | --- | --- | --- |
| Mode de compression <b>Raw Bitmap Format</b> : *Aucun* | 48 Mo | 48 Mo | 16 Mo | 16 Mo |
| Mode de compression <b>Raw Bitmap Format</b> : *Optimal* | 9,11 Mo | 3,37 Mo | 5,06 Mo | 4,75 Mo |
| Qualité De Compression <b>Jpeg Bitmap Format</b> : *1* | 5,09 Mo | 1,94 Mo | 6,30 Mo | 2,49 Mo |
| Qualité De Compression <b>Jpeg Bitmap Format</b> : *0.5* | 231 KO | 230 KO | 626 KO | 569 KO |
| Qualité De Compression <b>Jpeg Bitmap Format</b> : *0* | 407 KO | 433 Ko | 990 KO | 808 KO |
