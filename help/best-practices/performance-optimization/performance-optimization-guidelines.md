---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: Découvrez les directives d’optimisation des performances de Substance 3D Designer pour améliorer les performances des graphiques et réduire le temps de traitement.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Directives d’optimisation des performances
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1051'
ht-degree: 0%

---


# Directives d’optimisation des performances

## Graphes Substance

Plus vos [graphes de Substances](../../compositing-graphs/substance-compositing-graphs.md) sont complexes, plus la puissance de traitement nécessaire à leur rendu est importante. Essayez de <b>trouver un équilibre entre complexité et vitesse de rendu</b>.\
Ceci est *particulièrement* important si vous comptez les utiliser dans des applications graphiques en temps réel, telles que des jeux.

En règle générale, les nœuds présentant des paramètres personnalisés (qui peuvent être modifiés au moment de l&#39;exécution) <b>doivent être placés le plus près possible de la fin du graphique</b>.

Cela est dû au fait que la sortie de chaque nœud est mise en cache chaque fois que possible. Par conséquent, plus votre nœud personnalisable se trouve haut dans le graphique, plus le nombre de sorties à traiter est élevé chaque fois que l’un de ces paramètres exposés est modifié. Si le nœud exposé est proche de la fin du graphique, seuls les quelques nœuds situés entre lui et les nœuds de sortie doivent être recalculés.

Par exemple, si vous modifiez une couleur uniforme au début de votre graphique, tous les nœuds suivants seront recalculés. Si vous modifiez un nœud TSL placé juste avant la sortie, seul ce nœud sera recalculé, ce qui améliore considérablement les performances du graphique.

Veuillez prendre bonne note des directives suivantes :

### PARAMÈTRES GÉNÉRAUX LIÉS AUX PERFORMANCES

+++Le moteur GPU est beaucoup plus rapide que le moteur CPU
À moins que vous ne disposiez d’une carte graphique non prise en charge (intégrée), utilisez le moteur Substance du GPU (à modifier avec la touche de raccourci F9).

+++

+++Le changement de la résolution parent du graphique est lent
Il recalcule le graphique, le cache et toutes les vignettes. Il est préférable d&#39;utiliser [l&#39;onglet <b>Lot</b>de la boîte de dialogue d&#39;exportation](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md), car cela évite un recalcul important et inutile (par exemple lors de l&#39;exportation en résolution 8192).

+++

+++Dans des cas extrêmes, une augmentation de la mémoire cache peut être nécessaire
L&#39;application [limite la quantité de RAM pouvant être utilisée](../../interface/preferences-window/preferences-window.md) pour le cache d&#39;image, mais vous pouvez la remplacer et l&#39;augmenter (avec précaution).

+++

### OPTIMISATION DU GRAPHIQUE

+++Faites attention aux résolutions des nœuds et à l&#39;héritage en général !
Les valeurs élevées affectent considérablement les performances. Pensez donc à la manière dont le matériau est susceptible d&#39;être utilisé et à la possibilité de réduire la taille des données concernées.

Nous vous recommandons d&#39;en savoir plus sur la [résolution des nœuds (taille de sortie)](../../compositing-graphs/output-size/output-size.md) et l&#39;[héritage dans les graphiques de Substances](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

+++

+++Utiliser des niveaux de gris lorsqu’aucune couleur n’est nécessaire
Les opérations colorimétriques prennent quatre fois plus de temps que les opérations en niveaux de gris. Essayez également de réduire les conversions de texte entre la couleur et les niveaux de gris.

+++

+++Utiliser 8 bits lorsque le mode 16 bits n’est pas nécessaire
La version CPU de la Substance Engine (SSE2) *ne prend pas* en charge les niveaux de gris 16 bits ou 8 bits. Le moteur GPU prend en charge les 4 combinaisons de 8/16 bits et niveaux de gris/couleur. *Actuellement, seul le moteur CPU est utilisé dans les plug-ins Unity et Unreal Engine*.

+++

+++Réduire autant que possible la taille de la sortie du nœud
Parfois, la réduction de certains nœuds n’affecte pas le résultat final, mais affecte les performances. Par exemple, l’utilisation d’un nœud Couleur uniforme défini sur la même taille de sortie que le document est inutile : la couleur uniforme doit être définie sur Absolue [16px x 16px] et le nœud suivant sur Relative au parent. En général, cette astuce fonctionne bien pour les images basse fréquence, telles que le bruit de Perlin.

+++

+++N’utilisez pas d’images inférieures à 16*16 pixels
Cela ralentit les performances de rendu.

+++

+++Lorsque vous utilisez le nœud Fusion, désactivez Fusion Alpha lorsqu’il n’est pas nécessaire


+++

+++Les flous et les déformations sont les nœuds qui sollicitent le plus le processeur


+++

+++Certains générateurs de bruit sont affectés par la quantité de motifs dessinés
Par exemple, le nœud [Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) sera plus lent à traiter le plus de motifs que vous y ajouterez.

+++

+++Certains bruits sont affectés par un facteur d’échelle
Ce facteur va en fait dessiner davantage de schémas. Les nœuds affectés sont les bruits, les modèles de Cellules, etc. Si vous avez besoin d&#39;un motif de bruit blanc, n&#39;utilisez pas un bruit avec une valeur d&#39;échelle très élevée et utilisez plutôt les nœuds [Bruit blanc](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md) ou [Bruit blanc accéléré](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md).

+++

+++A l&#39;inverse, il existe des générateurs de bruit très rapides
Il s&#39;agit notamment de [bruit blanc rapide](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md), de [bruit de Somme fractale](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md) et de [bruit anisotrope](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md).

+++

+++Méfiez-vous des lourdes fonctions d’échantillonnage d’image dans certains cas
Les fonctions sont exécutées sur le moteur CPU, sauf dans les [processeurs pixellisés](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md). Si vous effectuez beaucoup d&#39;échantillonnage d&#39;image lourd (modification des coordonnées $pos) dans [Value Processors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) ou [FXmaps](../../function-graphs/fxmaps/fxmaps.md), il y aura beaucoup de permutation entre la VRAM et la RAM du processeur, ce qui entraînera des retards de performances.

+++

### OPTIMISATIONS POUR UNE UTILISATION MOBILE

+++Il n’est pas recommandé d’utiliser les Déformations et les FX-Maps
Elles sont très coûteuses.

+++

+++Éviter les nœuds de flou
Utilisez plutôt des transformations de réduction d’échelle.

+++

+++Travaillez autant que possible en niveaux de gris
Basculez en mode colorimétrique à la fin du graphique.

+++

+++Partage des nœuds autant que possible entre les sorties


+++

### OPTIMISATION DE LA TAILLE POUR LES BITMAPS INCORPORÉS

La [taille de sortie](../../compositing-graphs/output-size/output-size.md) de [bitmaps](../../resources/bitmap-resource/bitmap-resource.md) est définie sur [&#39;Absolue&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) par défaut. Cela signifie que si le bitmap est connecté à une sortie via la chaîne de nœuds, il force alors la sortie finale à avoir la taille du bitmap incorporé.\
La taille de sortie d&#39;un nœud que vous insérez après l&#39;image bitmap sera définie sur [&#39;Relative à l&#39;entrée&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Cela signifie que le nœud va également inhérenter la taille du bitmap et transporter cette taille le long de la chaîne de nœuds jusqu&#39;aux sorties. Pour corriger cela, vous devez définir le nœud après l&#39;image bitmap pour que sa taille de sortie soit définie sur [&#39;Relative au parent&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

Si le graphique est défini pour avoir une résolution dynamique, vous pouvez modifier la Taille de sortie sur l’image bitmap incorporée pour qu’elle soit Relative au parent.\
De cette façon, la taille du bitmap change en fonction du graphique parent et vous n’obtenez pas une situation où le graphique traite une résolution supérieure à celle nécessaire dans le bitmap.

>[!WARNING]
>
> Définir un nœud [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) sur « Relatif au parent » et [publier](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) le graphique sur une ressource Substance 3D (SBSAR) enregistrera le bitmap à une résolution de **256x256** au lieu de sa taille d&#39;origine. Il est plutôt conseillé de conserver la [méthode d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) des [tailles de sortie](../../compositing-graphs/output-size/output-size.md) des nœuds Bitmap comme &#39;Absolue&#39; et d&#39;utiliser un nœud [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) défini sur &#39;Relative au parent&#39; juste après le nœud Bitmap.

![Optimisation des bitmaps incorporés 1](../../assets/input-1.jpg "Optimisation des bitmaps incorporés 1")

![Optimisation des bitmaps incorporés 2](../../assets/relativetoparent.jpg "Optimisation des bitmaps incorporés 2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Il est également conseillé de définir le format des ressources Bitmap sur Jpeg pour réduire la taille des ressources Substance 3D [publiées](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) (SBSAR).

</td>
<td style="border: 0;" valign="top">

![Optimisation des bitmaps incorporés 3](../../assets/format.jpg "Optimisation des bitmaps incorporés 3")

</td>
</tr>
</table>
