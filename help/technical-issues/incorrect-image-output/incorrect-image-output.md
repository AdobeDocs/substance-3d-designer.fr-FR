---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/incorrect-image-output.html"
breadcrumb-title: ''
description: Résolvez les problèmes d’image en sortie incorrecte dans Substance 3D Designer et découvrez comment résoudre les problèmes de rendu.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Incorrect image output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sortie d’image incorrecte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 0%

---


# Sortie d’image incorrecte

Cette page répertorie les problèmes techniques dans Substance 3D Designer qui entraînent une image en sortie incorrecte ou inattendue et propose des étapes de dépannage pour chacun d’eux.

## Pas/bandes visibles

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(erreur)](incorrect-image-output.resources/error.svg) Problème**

Les dégradés de l’image en sortie sont étagés au lieu d’être lisses. Le pas est causé par la plage de valeurs *utilisée par l&#39;image trop étroite*.\
Cela signifie qu’il n’y a pas assez de valeurs pour effectuer une transition en douceur d’une étape d’un dégradé à l’autre.

Les valeurs luminance/RVBA peuvent être codées à l&#39;aide de l&#39;entier ou des valeurs de point flottant, ce qui affecte leur *précision* :

* L&#39;**Entier** offre une précision de 8 bits (0-255, soit 256 valeurs possibles) et une précision de 16 bits (0-65535 soit 65536 valeurs possibles) pour stocker une valeur comprise entre 0 et 1.
* **Le virgule flottante** offre une précision de 16 bits (HDR 16F) et de 32 bits (HDR 32F), avec la possibilité de stocker des valeurs en dehors de la plage 0-1, y compris des valeurs négatives. Cela vous permet de travailler avec des images de plage dynamique élevée (HDR), où la valeur de luminance peut aller bien au-delà de 1.0.

Si vous n’avez pas besoin de travailler spécifiquement avec des images HDR, la plupart de vos nœuds génèreront probablement une valeur dans la plage 0-1 codée à l’aide d’entiers. Si le format de sortie de l’image est de 8 bits, l’image ne peut utiliser que 256 valeurs, ce qui se traduit souvent par des pas visibles sur les dégradés. Cela peut avoir un impact particulier sur la sortie des nœuds normaux.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/demo-stepping-8-bit.png){width="256px"}![](incorrect-image-output.resources/demo-stepping-8-bit-2.png){width="256px"}![](incorrect-image-output.resources/demo-stepping-8-bit-3.png){width="256px"}

</td>
</tr>
</table>

**![(coche)](incorrect-image-output.resources/check.svg) Étapes recommandées**

Vérifiez le **format de sortie** (c&#39;est-à-dire la profondeur de bits) du nœud et de tous les nœuds en amont et assurez-vous que ces nœuds utilisent une *précision d&#39;Entier d&#39;au moins 16 bits*.

Le paramètre Format de sortie est souvent défini sur la méthode d&#39;héritage *Relative à l&#39;entrée* [3}, qui peut propager la faible précision dans tout le graphe. ](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)Idéalement, en remontant dans le graphe, vous trouverez la cause première du problème.

Vous pouvez rapidement identifier la précision de la sortie d&#39;un nœud en examinant les informations textuelles affichées sous le nœud :

* **L/C** fait référence à l&#39;image en niveaux de gris (c&#39;est-à-dire la Luminance) ou en couleur
* **8/16** signifie codage entier
* **16F/32F** désigne le codage en virgule flottante

Par exemple :

* L8 : entier 8 bits en niveaux de gris
* C16 : entier couleur 16 bits
* C32F : virgule flottante couleur 32 bits (HDR)

## Perte de qualité dans le SBSAR publié

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

<b>![(erreur)](incorrect-image-output.resources/error.svg) Problème</b>

La qualité des images produites par une archive Substance 3D (SBSAR) est nettement inférieure au graphe à partir duquel le fichier Substance 3D est publié, comme le montre l’image de droite.\
La sortie semble basse résolution.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/issues-sbsar-bitmap-relative-to.jpg){width="256px"}

</td>
</tr>
</table>

<b>![(coche)](incorrect-image-output.resources/check.svg) Étapes recommandées</b>

Assurez-vous que la propriété [Taille de sortie](../../compositing-graphs/output-size/output-size.md) de tous les nœuds [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) est définie sur la [méthode d&#39;héritage](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) *absolue*.

Si ce n&#39;est pas le cas, leur [ressource Bitmap](../../resources/bitmap-resource/bitmap-resource.md) référencée sera enregistrée à la résolution 256\*256 par défaut dans l&#39;archive Substance 3D publiée, ce qui* impactera la qualité* d&#39;une ou plusieurs sorties.

## L’image est floue

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(erreur)](incorrect-image-output.resources/error.svg) Problème**

Les formes sont légèrement floues après l&#39;utilisation de certains nœuds, tels que [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) ou [Fusion](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md).

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](incorrect-image-output.resources/issues-bilinear.jpg){width="256px"}

</td>
</tr>
</table>

**![(coche)](incorrect-image-output.resources/check.svg) Étapes recommandées**

Lors de la réorganisation des pixels dans une image, par exemple lors du redimensionnement d&#39;une forme ou de la modification de la résolution d&#39;une image, il existe deux façons de déterminer comment les pixels de la source doivent être *mappés* vers la destination :

* **Le plus proche** : le pixel sera mappé à la cible *tel quel* à la coordonnée correspondante. Si la cible est de résolution inférieure, le pixel peut être totalement ignoré. Si la cible est d’une résolution plus élevée, elle sera mappée à tous les pixels couvrant sa plage. La sortie est *plus nette* et sera légèrement *crénelée*.
* **filtrage Bilinéaire** : un processus de filtrage est appliqué à l&#39;image source afin que ses pixels soient mappés à la résolution cible de manière à *lisser* les transitions entre les pixels. La sortie est *plus lisse* et sera légèrement *floue*.

Le nœud [Transformation 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) fournit une option de méthode **Filtrage** pour sélectionner laquelle de ces deux méthodes de mappage doit être utilisée.

La plupart des nœuds (par exemple, [Fusion](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)) utilisent par défaut *filtrage bilinéaire* lors de l&#39;échantillonnage d&#39;une texture d&#39;entrée de résolution différente, ce qui peut introduire un flou indésirable.\
Le nœud Transformation 2D étant *atomique*, donc très léger, il peut être utilisé *même si aucune transformation n&#39;est nécessaire* pour modifier la résolution d&#39;une texture à l&#39;aide de sa propriété [Taille de sortie](../../compositing-graphs/output-size/output-size.md) avant d&#39;envoyer la texture à un autre nœud, de sorte que vous pouvez *contrôler l&#39;impact* de ce redimensionnement.

Dans le [graphe de fonction](../../function-graphs/function-graphs.md) du nœud [Processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), les nœuds **Sample** incluent la *même option* pour contrôler la façon dont la texture échantillonnée doit être mappée à la résolution du nœud.
