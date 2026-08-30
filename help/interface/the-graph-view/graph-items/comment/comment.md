---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Ajoutez des commentaires aux graphiques Substance 3D Designer pour documenter votre workflow et expliquer les connexions de nœuds.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Commentaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Commentaire

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icône de commentaire](comment.resources/graphatomic-comment_1.png "Icône de commentaire")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Un commentaire est simplement un fragment de texte flottant qui peut être placé n’importe où dans un graphique.

Il est destiné à annoter et expliquer des parties d’un graphique. Sa propriété <b>Description</b> contient le texte affiché.

</td>
</tr>
</table>

>[!NOTE]
>
> Les commentaires comportent des sauts de ligne automatiques qui visent à réduire leur empreinte dans un graphique.

## Création de commentaires

Le type de commentaire par défaut est placé indépendamment des nœuds du graphique.

Il peut être créé de la manière suivante :

+++Menu Nœud
Appuyez sur la <b>barre d&#39;espace</b> dans la vue Graphique pour ouvrir le <b>menu Nœud</b>, puis sélectionnez l&#39;élément Commentaire dans la liste.

Tapez « comment » dans le champ de recherche pour faire apparaître l’élément et le trouver plus rapidement.

+++

+++Raccourci
Si un raccourci clavier est mappé à l&#39;élément « Commentaire » dans les [Préférences](../../../../interface/preferences-window/preferences-window.md), appuyez sur ce raccourci lorsque la vue Graphique est active.

+++

+++Menu contextuel
Dans la vue Graphique, appuyez sur <b>RMB</b> sur un objet ou dans un espace vide et sélectionnez l&#39;option <b>Ajouter un commentaire</b>.

+++

+++Barre d’outils Graphique
Dans la barre d&#39;outils du mode Graphique, cliquez sur le bouton Commentaire dans la <b>Palette de noeuds</b>.

+++

+++Bibliothèque
Dans la bibliothèque, sélectionnez la catégorie <b>Éléments de graphique</b>, puis faites glisser l&#39;élément « Commentaire » dans la vue Graphique.

+++

>[!TIP]
>
> Lorsqu&#39;un commentaire est créé, sa propriété « Description » est automatiquement mise en avant afin que vous puissiez immédiatement modifier le texte du commentaire.

## Commentaires parents

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Un commentaire parent est un commentaire *associé à un nœud spécifique* dans le graphique. Ainsi, lorsque le nœud est déplacé, le commentaire suit et, lorsque le nœud est supprimé, le commentaire est supprimé avec lui.

Les commentaires qui sont créés lorsqu&#39;un nœud *unique* est actuellement sélectionné, ou via le menu contextuel d&#39;un nœud unique, sont apparentés à ce nœud.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Commentaires : commentaires parentés](comment.resources/graph-comment_parented.gif "Commentaires : commentaires parentés")

</td>
</tr>
</table>

## formatage de HTML

Le texte peut être formaté à l’aide d’étiquettes de HTML. Cette mise en forme est basculée à l&#39;aide du bouton ![](comment.resources/graph-frames_html-markup-button.png) <b>Annotation de HTML</b> dans la propriété <b>Description</b> du commentaire.

>[!TIP]
>
> Pour en savoir plus sur cette fonctionnalité, consultez la section <b>Description</b> de la documentation [Images](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Commentaires : balisage de HTML](comment.resources/graph-comment_html-markup.gif "Commentaires : balisage de HTML")
