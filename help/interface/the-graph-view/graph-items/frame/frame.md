---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/frame.html"
breadcrumb-title: ''
description: Utilisez des images dans le mode graphique Substance 3D Designer pour organiser et regrouper les nœuds afin d’obtenir une meilleure clarté visuelle.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Frame
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cadre
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 1%

---


# Cadre

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icône d’image](../../../../assets/graphatomic-frame_1.png "Icône d’image")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Un bloc facilite la lisibilité et la mise en page des graphiques en regroupant visuellement les objets dans ce graphique et en vous permettant de déplacer facilement tous ces objets ensemble.

Par exemple, les blocs peuvent être nommés et colorés de sorte que la structure du graphique ressorte clairement lors d’une présentation, ce qui est très utile à mesure que la complexité du graphique augmente.

Ils peuvent également être annotés et fonctionnent ainsi comme un outil de documentation pour expliquer pourquoi certains nœuds ont été configurés d&#39;une manière spécifique.

</td>
</tr>
</table>

## Apparence

Selon la position du curseur de la souris ou s’il fait partie d’une sélection, un cadre se présente dans différents styles visuels pour vous permettre de savoir si vous pouvez interagir avec lui et comment.

+++Par défaut
Par défaut, le cadre est un rectangle avec des coins arrondis remplis avec la couleur sélectionnée dans sa propriété <b>Couleur de cadre</b>. Une teinte plus foncée de cette couleur est appliquée sur le contour du bloc.

Le titre défini dans la propriété <b>Titre</b> est gris dans le coin supérieur gauche de l&#39;image.

![Image (état par défaut)](../../../../assets/graph-frames-default.png "Image (état par défaut)")



+++

+++Survol de l’en-tête
Lorsque vous survolez le haut de l’image, une barre d’en-tête s’affiche.

Le cadre peut être déplacé en faisant glisser cette barre d’en-tête ou son titre.

![Image (état de survol)](../../../../assets/graph-frames-hover.png "Image (état de survol)")



+++

+++Sélection
Lorsque cette option est sélectionnée, le titre et le contour du cadre sont mis en surbrillance en blanc. Le contour s’épaissit.

![Image (état sélectionné)](../../../../assets/graph-frames-selected.png "Image (état sélectionné)")



+++

## Création d’images

Les blocs peuvent être ajoutés dans n’importe quel type de graphique, de l’une des manières suivantes :

+++Menu Nœud
Appuyez sur la <b>barre d&#39;espace</b> dans la vue Graphique pour ouvrir le <b>menu Nœud</b>, puis sélectionnez l&#39;élément Cadre dans la liste.

Tapez « frame » dans le champ de recherche pour faire apparaître l’élément et le trouver plus rapidement.

+++

+++Raccourci
Si un raccourci clavier est mappé à l’élément « Cadre » dans les [Préférences](../../../../interface/preferences-window/preferences-window.md), appuyez sur ce raccourci lorsque la vue Graphique est active.

+++

+++Menu contextuel
Dans la vue Graphique, appuyez sur <b>RMB</b> sur n&#39;importe quel objet ou dans un espace vide et sélectionnez l&#39;option <b>Ajouter une image</b>.

+++

+++Barre d’outils Graphique
Dans la barre d&#39;outils du mode Graphique, cliquez sur le bouton Cadre dans la <b>Palette de noeuds</b>.

+++

+++Bibliothèque
Dans la bibliothèque, sélectionnez la catégorie <b>Éléments de graphique</b>, puis faites glisser l&#39;élément « Cadre » dans la vue Graphique.

+++

### Sélections de cadrage

Si une sélection est active dans un graphique lors de la création d’un bloc, ce bloc est automatiquement ajusté pour inclure entièrement les objets sélectionnés.

En gardant cela à l’esprit, la création d’images à l’aide d’un raccourci clavier rend le cadrage du contenu d’un graphique encore plus rapide.

![Images : Méthodes de création](../../../../assets/graph-frames_creation.gif "Images : Méthodes de création"){width="480px"}

>[!TIP]
>
> Lorsqu’un bloc est créé, sa propriété Titre devient automatiquement active afin que vous puissiez immédiatement modifier le titre du bloc.

## Manipulation d’images

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Les blocs peuvent être <b>panoramiques</b> en faisant glisser leur barre de titre ou d’en-tête et <b>redimensionnés</b> en faisant glisser l’une de leurs bordures ou de leurs angles.

L’illustration met en évidence les zones d’interaction pour le panoramique (bleu) et le redimensionnement (jaune).

</td>
<td style="border: 0;" valign="top">

![Images : zones d’interaction](../../../../assets/graph-frames_interaction-zones.png "Images : zones d’interaction")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Magnétisme de la grille

Par défaut, un cadre s’aligne sur la grille moyenne lorsqu’il est déplacé ou redimensionné.

Maintenez la touche <b>Ctrl</b> (Windows) / <b>Cmd</b> (macOS) enfoncée pour déplacer cet alignement sur la petite grille afin d’effectuer des réglages plus fins.

</td>
<td style="border: 0;" valign="top">

![Images : Magnétisme de la grille](../../../../assets/graph-frames_grid-snapping.gif "Images : Magnétisme de la grille")

</td>
</tr>
</table>

## Propriétés

Lorsqu&#39;un bloc est sélectionné, les propriétés suivantes sont disponibles dans le dock [Propriétés](../../../../interface/properties/properties.md) :

+++Titre
Le <b>Titre</b> se trouve en haut à gauche de l&#39;image. Sa visibilité du titre peut être activée ou désactivée à l&#39;aide de la propriété <b>Titre visible</b>.

La taille du titre peut être verrouillée à une taille d’écran minimale afin qu’il reste lisible lors d’un zoom arrière sur le graphique. Pour ce faire, cochez l&#39;option « Titres des images » dans la liste déroulante <b>Informations</b> de la barre d&#39;outils [Vue graphique](../../../../interface/the-graph-view/the-graph-view.md).

![Images : Titre](../../../../assets/graph_frames_title.gif "Images : Titre"){width="640px"}



+++

+++Description
La <b>Description</b> est une partie de texte supplémentaire facultative qui peut être utilisée pour annoter le contenu du bloc.

Le texte peut être mis en forme à l’aide d’étiquettes de HTML. Cette mise en forme est basculée en cliquant sur le bouton ![](../../../../assets/graph-frames_html-markup-button.png) <b>Annotation de HTML</b>.

Pour en savoir plus, consultez la section Description ci-dessous.

![Images : Description](../../../../assets/graph-frames_description.gif "Images : Description"){width="640px"}



+++

+++Couleur
La <b>couleur d&#39;image</b> est utilisée pour remplir le cadre dans la vue Graphique. Utilisez le sélecteur de couleurs pour sélectionner une couleur.

La couche alpha de la couleur contrôle l&#39;*opacité* de l&#39;image, où une valeur de 0 signifie que l&#39;image est entièrement transparente.

![Images : Color](../../../../assets/graph-frames_colour.gif "Images : Color"){width="640px"}



+++

## Description

Un bloc peut être annoté avec un texte qui sera placé à l’intérieur du bloc. Le texte est aligné à gauche et commence dans le coin supérieur gauche du bloc. Utilisez la propriété [Description](#properties) du cadre pour modifier ce texte.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Standard

Le <b>Titre</b> s&#39;affiche dans une police en gras située en haut à gauche de l&#39;image. La visibilité du titre peut être activée ou désactivée.

Sa taille peut être verrouillée à une taille d’écran minimale afin qu’il reste lisible lors d’un zoom arrière sur le graphique. Pour ce faire, cochez l&#39;option « Titres des images » dans la liste déroulante <b>Informations</b> de la barre d&#39;outils [Vue graphique](../../../../interface/the-graph-view/the-graph-view.md).

</td>
<td style="border: 0;" valign="top">

![Image (description par défaut)](../../../../assets/graph-frames-descr.png "Image (description par défaut)"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### formatage de HTML

Le texte peut être formaté à l&#39;aide d&#39;étiquettes de HTML dans la propriété <b>Description</b> du cadre. La mise en forme doit être activée à l&#39;aide du bouton ![](../../../../assets/graph-frames_html-markup-button.png) <b>Annotation de HTML</b> dans cette même propriété.

</td>
<td style="border: 0;" valign="top">

![Image (description au format HTML)](../../../../assets/graph-frames-descr-html.png "Image (description au format HTML)"){zoomable="yes"}

</td>
</tr>
</table>

Vous pouvez copier et coller cet exemple dans la propriété Description de l&#39;image pour tester cette fonctionnalité par vous-même :

```
<h2>HTML formatting</h2>

<p>This is a description formatted using <b>HTML markup</b>.</p>

<p>Formattig text makes it more <i>pleasant</i>, <font color="#CC8822">impactful</font> and <code>clearly structured</code> for users.</p>

<p><img src="image_filepath">  Images are also supported! <sup>How nice!</sup></p>
```


Voici une liste de balises utiles pour la mise en forme du texte :

+++balises de formatage de HTML

|  |  |
| --- | --- |
| Gras | &lt;b>...&lt;/b> |
| Italique | &lt;i>...&lt;/i> |
| Couleur | &lt;font color=« #4A567C« >...&lt;/font> |
| Paragraphe | &lt;p>...&lt;/p> |
| Saut de ligne | &lt;br> |
| Intitulés | &lt;h1>...&lt;/h1>, &lt;h2>...&lt;/h2>, etc. |
| Image | &lt;img src=« {path\_to\_image}« > |
| Exposant | &lt;sub>...&lt;/sub> |
| Liste non triée (puces) | &lt;ul> &lt;li>...&lt;/li> &lt;li>...&lt;/li> &lt;/ul> |
| Liste triée (numéros) | &lt;ol> &lt;li>...&lt;/li> &lt;li>...&lt;/li> &lt;/ol> |
| Code | &lt;code>...&lt;/code> |


+++

## Règles d’inclusion

Un objet est considéré comme inclus dans une image s’il répond à sa règle d’inclusion. Ces règles varient en fonction de l’objet et du cas particulier. Ils sont répertoriés ci-dessous.

Le symbole jaune de chaque illustration représente le point ou la zone qui doit se trouver entièrement à l’intérieur des limites d’un cadre pour qu’un objet soit inclus dans ce cadre.

+++Nœuds
Le <b>point central</b> est utilisé.

Les badges, les connecteurs et les informations affichés sous le nœud sont tous ignorés.

Les nœuds peuvent être d&#39;heights différents, selon leur nombre de connecteurs d&#39;entrée ou de sortie.

Lorsque des connecteurs sont affichés ou masqués, ajoutés ou supprimés, l&#39;height du nœud s&#39;ajuste à partir de son *centre*.

Par conséquent, l&#39;emplacement du point central d&#39;un nœud ne doit pas être modifié tant qu&#39;il n&#39;a pas *été délibérément déplacé*.

![Inclusion d’image : nœuds de grande taille](../../../../assets/frame_inclusion_node_tall.png "Inclusion d’image : nœuds de grande taille")



Le <b>point d&#39;entrée</b><b></b> du nœud *hôte* est utilisé.

Le nœud hôte est le nœud auquel un nœud est ancré.

Si plusieurs nœuds sont ancrés dans une chaîne, le nœud hôte du dernier nœud ancré est utilisé pour toute la chaîne.

Les badges, les connecteurs et les informations affichés sous le nœud sont tous ignorés.

![Inclusion d’image : nœuds ancrés](../../../../assets/frame_inclusion_node_docked.png "Inclusion d’image : nœuds ancrés")



![Inclusion d’image : nodes](../../../../assets/frame_inclusion_node.png "Inclusion d’image : nodes")



+++

+++Nœuds point
Le <b>point central</b> du point est utilisé.

Les connecteurs, les icônes de portail et les noms sont tous ignorés.

![Inclusion d’image : nœuds de point](../../../../assets/frame_inclusion_dot.png "Inclusion d’image : nœuds de point")



+++

+++Commentaires
Le <b>point central</b> du *cadre de sélection* du commentaire (contour jaune) est utilisé.

Les commentaires parents ne suivent pas les règles d’inclusion des commentaires.

À la place, le <b>point central</b> du nœud *parent* est utilisé.

Les badges, les connecteurs et les informations affichés sous le nœud sont tous ignorés.



![Inclusion d’image : commentaires parents](../../../../assets/frame_inclusion_comment_parented.png "Inclusion d’image : commentaires parents")



![Inclusion d’image : commentaires](../../../../assets/frame_inclusion_comment.png "Inclusion d’image : commentaires")



+++

+++Épingles
Le <b>conseil</b> de l&#39;icône en forme d&#39;épingle est utilisé.

![Inclusion d’image : épingles de navigation](../../../../assets/frame_inclusion_pin.png "Inclusion d’image : épingles de navigation")



+++

+++Images
Le <b>cadre de sélection</b> de l’image imbriquée est utilisé.

Cela signifie qu’une image imbriquée doit se trouver entièrement à l’intérieur des limites d’une autre image pour être incluse dans cette dernière.

Le titre est ignoré.

![Inclusion d’image : images imbriquées](../../../../assets/frame_inclusion_frame.png "Inclusion d’image : images imbriquées")



+++

## Ajuster la taille au contenu

![Images : Taille adaptée au contenu](../../../../assets/graph-frames_fit-size-to-content.png "Images : Taille adaptée au contenu")

Lorsque vous effectuez des réglages dans votre graphique, il se peut qu’un bloc ne soit plus ajusté de manière élégante à son contenu. Dans ce cas, il est possible d’ajuster automatiquement la position et la taille de l’image afin qu’elle s’adapte à l’étendue de son contenu, avec un remplissage d’une cellule de grille moyenne.

Pour ce faire, cliquez sur <b>RMB</b> sur la barre de titre ou d&#39;en-tête du cadre (voir [Apparence](#appearance)) et sélectionnez l&#39;option <b>Adapter à la taille du contenu</b> dans le menu contextuel.

>[!NOTE]
>
> L&#39;option est disponible si au moins *un* objet graphique respecte les [règles d&#39;inclusion](../../../../interface/the-graph-view/graph-items/frame/frame.md) du cadre.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Ajustement du texte de description

Si le cadre comporte une description, sa valeur est ajustée pour utiliser tout espace vide en regard de la description, si possible.

Si aucun objet inclus ne peut être placé dans cet espace, l’height du cadre est ajusté pour tenir compte de la description.

</td>
<td style="border: 0;" valign="top">

![Images : Taille adaptée au contenu (avec description)](../../../../assets/graph-frames_fit-description.png "Images : Taille adaptée au contenu (avec description)")

</td>
</tr>
</table>

+++Exemple
![Images : Taille adaptée au contenu (GIF)](../../../../assets/graph-frames_fit-size-to-content.gif "Images : Taille adaptée au contenu (GIF)"){width="640px"}



+++

## Développement automatique

![Images : Développement automatique](../../../../assets/graph-frames_auto-expand.png "Images : Développement automatique")

Au fur et à mesure que le graphique se développe, le contenu des blocs peut devoir être réorganisé. Les nœuds peuvent se déplacer pour faire de la place pour les ajouts ou le contenu peut devoir être plus espacé pour promouvoir la lisibilité.

Pour faciliter ces réglages, il est possible de développer automatiquement un cadre lors du déplacement de [objets inclus](#inclusion-rules) : maintenez la touche <b>Maj</b> enfoncée tout en déplaçant un objet pour que les bordures du cadre s&#39;ajustent automatiquement afin de maintenir cet objet dans leurs limites.

Cela s’applique également aux sélections qui peuvent inclure plusieurs objets. Dans ce cas, l’image hôte de chaque objet sera ajustée simultanément.

Si un objet n&#39;est pas entièrement entouré par les limites du cadre, mais qu&#39;il respecte toujours sa [règle d&#39;inclusion](#inclusion-rules), le cadre est ajusté pour l&#39;entourer entièrement avec un remplissage supplémentaire d&#39;une cellule de grille moyenne dès que la touche <b>Maj</b> est enfoncée.

>[!NOTE]
>
> Bien que la touche <b>Maj</b> puisse être enfoncée ou relâchée à tout moment pendant le déplacement pour déclencher ou annuler le réglage automatique de l&#39;image, elle *doit* être maintenue pendant la réalisation du déplacement pour appliquer efficacement le réglage.

+++Exemple
![Images : Développement automatique (GIF)](../../../../assets/graph-frames_auto-expand.gif "Images : Développement automatique (GIF)"){width="640px"}



+++
