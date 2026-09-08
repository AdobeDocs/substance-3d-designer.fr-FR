---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Utilisez le nœud Quadrant dans FXMaps pour diviser les textures en quatre sections afin de créer des motifs et des variations en mosaïque.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nœud du quadrant
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# Nœud du quadrant

De nombreuses FX-Maps se composent entièrement de chaînes de nœuds de quadrant. Les nœuds du quadrant sont les nœuds les plus puissants et les plus flexibles du groupe FX-Map, il est donc utile de comprendre comment fonctionne ce nœud.

La chose la plus importante à propos des nœuds de quadrant est qu&#39;ils sont le seul nœud qui peut augmenter la profondeur ou *octave*, du graphique FX-Map. Chaque nœud du quadrant s&#39;ajoute au graphique sous-jacent en quadrilatère ; aucun des autres nœuds ne le fait.

Le nœud de quadrant comporte un certain nombre de paramètres :

## Couleur/Luminosité

Lorsque le nœud ajoute une image à la FX-Map, ces paramètres définissent la façon dont les couches sont fusionnées avec les autres images de la chaîne. Les paramètres *Couleur/Luminosité* s&#39;appliquent à toutes les images rendues par ce nœud particulier.

### Décalage de branche

Décale l’image du nœud. Le décalage est appliqué à toutes les autres images rendues par les nœuds suivants dans le graphique. Le décalage de branche applique la translation au nœud actuel du quadrant et à tous les nœuds situés en dessous dans la même branche du graphique.

Ce paramètre peut être contrôlé avec une fonction dynamique.

### Motif

Définit l&#39;image (le cas échéant) à ajouter au FX-Map par ce nœud.

Les nœuds de quadrant prennent en charge une longue liste de motifs, qui sont décrits plus loin dans cette rubrique.

>[!WARNING]
>
> Ce paramètre ne peut pas être contrôlé par une fonction dynamique dans un fichier sbsar.

### Décalage du motif

Décale l&#39;image du nœud selon la valeur spécifiée, mais n&#39;affecte pas les nœuds suivants. Ce paramètre peut être contrôlé avec une fonction dynamique.

### Taille du motif

Définit la taille de l’image (le cas échéant) à ajouter au FX-Map. Ce paramètre peut être contrôlé avec une fonction dynamique.

### Rotation du motif

Définit la rotation de l’image (le cas échéant) à ajouter au FX-Map. Ce paramètre peut être contrôlé avec une fonction dynamique.

### Variation de motif

Certains motifs ont des variantes. Ce paramètre vous permet de choisir la variante à utiliser. Ce paramètre peut être contrôlé avec une fonction dynamique.

### Mode de fusion

Spécifie le processus de fusion à utiliser lors du mélange de l&#39;image de ce nœud (le cas échéant) avec l&#39;image FX-Map. Ce paramètre peut être contrôlé avec une fonction dynamique.

### Graine aléatoire

Valeur de départ pour le générateur de nombres aléatoires.

Le générateur utilise cette valeur de départ pour créer une séquence de nombres qui semblent être aléatoires. L’avantage de cette approche est que, contrairement au monde réel, vous pouvez vous assurer que la même séquence exacte de nombres aléatoires est générée à chaque fois, produisant des résultats prévisibles, répétables, mais aléatoires.

Ce paramètre peut être contrôlé avec une fonction dynamique.

### Hériter aléatoirement

Si la valeur est Oui, la valeur de départ du générateur de nombres aléatoires est héritée du nœud précédent du graphique (c&#39;est-à-dire le nœud situé au-dessus de celui-ci dans l&#39;arbre quadruple). S&#39;il s&#39;agit du premier nœud, il prend sa valeur de départ aléatoire du [graphique de Substance](../../../compositing-graphs/substance-compositing-graphs.md).

## Motifs

Chaque nœud de quadrant peut éventuellement ajouter une image à la FX-Map finale.

Par défaut, l’option Aucun motif est sélectionnée et aucune image n’est rendue. Le nœud de quadrant ne fait que subdiviser l&#39;image FX-Map, la divisant en quatre pour le nœud suivant de la chaîne.

L&#39;option suivante, *Image d&#39;entrée*, consiste à utiliser une image fournie au nœud FX-Map. Le nœud FX-Map accepte les images en couleurs ou en niveaux de gris à utiliser comme arrière-plan ou en remplacement de l’un des motifs intégrés. Notez que le nœud de quadrant ne peut effectuer le rendu d’une image d’entrée en niveaux de gris que dans une FX-Map en niveaux de gris, et inversement, il ne peut effectuer le rendu d’une image d’entrée en couleurs que dans une FX-Map en couleurs. Si vous souhaitez mélanger les types de couleurs, vous devez convertir vos entrées avant dans le graphique.

Enfin, vous pouvez choisir parmi l&#39;un des motifs intégrés : Carré, Disque, Paraboloïde, Cloche, Gaussien, Épine, Pyramide, Brique, Gradation, Ondes, Demi-cloche, Cloche striée, Croissant et Capsule.

Remarque supplémentaire : vous avez la possibilité de créer une fonction dynamique dans ce paramètre, mais elle ne fonctionnera que dans Substance 3D Designer. Pour avoir accès à l’image saisie par une fonction dynamique, vous devez utiliser des valeurs allant de 256 (entrée d’image 1) à des valeurs plus élevées (257 pour l’entrée d’image 2, etc.).

### Types de motif.

Les motifs sont tous en niveaux de gris. Certaines peuvent être légèrement modifiées à l&#39;aide du paramètre *Variation de motif*.

La plupart des motifs intégrés possèdent une forme de fond en dégradé radial ou similaire. Cela les rend très utiles pour de nombreux types de bruits et de motifs. D’autres motifs, tels que la brique, le disque et le carré, sont des formes simples et plates.

Le paramètre Variation de motif ajuste une fonction définie du motif.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../assets/fxmap-quadrants.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](../../../assets/quadrant-parameters.jpg)

</td>
</tr>
</table>
