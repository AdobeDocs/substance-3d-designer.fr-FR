---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Ajoutez des commentaires aux graphes Substance 3D Designer pour documenter votre workflow et expliquer les connexions de nœuds.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Commentaire
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Commentaire

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icône de commentaire](comment.resources/comment-01.png "Icône de commentaire")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Un commentaire est simplement un fragment de texte flottant qui peut être placé n’importe où dans un graphe.

Il est destiné à annoter et expliquer des parties d’un graphe. Sa propriété <b>Description</b> contient le texte affiché.

</td>
</tr>
</table>

>[!NOTE]
>
> Les commentaires ont un saut de ligne automatique qui vise à minimiser leur empreinte dans un graphe.

## Création de commentaires

Le type de commentaire par défaut est placé indépendamment des nœuds dans le graphe.

Il peut être créé de la manière suivante :

+++Menu Nœud
Appuyez sur la <b>barre d&#39;espace</b> dans la Vue du graphe pour ouvrir le <b>menu Nœud</b>, puis sélectionnez l&#39;élément « Commenter » dans la liste.

Tapez « comment » dans le champ de recherche pour faire apparaître l’élément et le trouver plus rapidement.

+++

+++Raccourci
Si un raccourci du clavier est mappé à l&#39;élément « Commentaire » dans les [Préférences](../../../../interface/preferences-window/preferences-window.md), appuyez sur ce raccourci lorsque la Vue du graphe est active.

+++

+++Menu contextuel
En Vue du graphe de compte, appuyez sur <b>RMB</b> sur n&#39;importe quel objet ou dans un espace vide et sélectionnez l&#39;option <b>Ajouter un commentaire</b>.

+++

+++Barre d’outils Graphique
Dans la barre d&#39;outils Vue du graphe, cliquez sur le bouton Commentaire dans la <b>Palette de noeuds</b>.

+++

+++Bibliothèque
Dans la bibliothèque, sélectionnez la catégorie <b>Éléments de Graphe</b>, puis faites glisser l&#39;élément « Commentaire » dans la Vue du graphe de données.

+++

>[!TIP]
>
> Lorsqu&#39;un commentaire est créé, sa propriété « Description » est automatiquement mise en avant afin que vous puissiez immédiatement modifier le texte du commentaire.

## Commentaires parents

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Un commentaire parent est un commentaire *joint à un nœud spécifique* dans le graphe de sorte que lorsque le nœud est déplacé, le commentaire suit et que lorsque le nœud est supprimé, le commentaire est supprimé avec lui.

Les commentaires qui sont créés lorsqu&#39;un nœud *unique* est actuellement sélectionné, ou via le menu contextuel d&#39;un nœud unique, sont apparentés à ce nœud.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Commentaires : commentaires parentés](comment.resources/comment-02.gif "Commentaires : commentaires parentés")

</td>
</tr>
</table>

## formatage de HTML

Le texte peut être formaté à l’aide d’étiquettes de HTML. Cette mise en forme est basculée à l&#39;aide du bouton ![](comment.resources/comment-03.png) <b>Annotation de HTML</b> dans la propriété <b>Description</b> du commentaire.

>[!TIP]
>
> Pour en savoir plus sur cette fonctionnalité, consultez la section <b>Description</b> de la documentation [Images](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Commentaires : balisage de HTML](comment.resources/comment-04.gif "Commentaires : balisage de HTML")
