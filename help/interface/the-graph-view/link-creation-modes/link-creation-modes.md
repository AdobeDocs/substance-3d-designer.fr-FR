---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/the-graph-view/link-creation-modes.html"
breadcrumb-title: ''
description: Découvrez les modes de création de liens dans la vue graphique de Substance 3D Designer pour connecter efficacement des nœuds.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Link creation modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modes de création de liens
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# Modes de création de liens

Dans les [graphes de Substance](../../../compositing-graphs/substance-compositing-graphs.md), vous pouvez connecter des nœuds à l&#39;aide de l&#39;un des 3 <b>modes de création de liens</b> :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Mode de création de lien : standard](../../../assets/link-creation-mode-standard.gif "Mode de création de lien : standard"){zoomable="yes"}

*Cliquer pour agrandir*

<b>![](../../../assets/image2020-10-6-19-40-25.png) Standard</b> (1)

Aucune condition n&#39;est imposée.

</td>
<td style="border: 0;" valign="top">

![Mode de création de lien : matériau](../../../assets/link-creation-mode-material.gif "Mode de création de lien : matériau"){zoomable="yes"}

*Cliquer pour agrandir*

![](../../../assets/image2020-10-6-17-11-20.png) <b>Matière</b> (2)

Les entrées et les sorties sont mises en correspondance en fonction de leur utilisation.

Si un seul des deux a une utilisation, la connexion est effectuée comme en mode Standard.

</td>
<td style="border: 0;" valign="top">

![Mode de création de lien : matériau compact](../../../assets/link-creation-mode-compact-material.gif "Mode de création de lien : matériau compact"){zoomable="yes"}

*Cliquer pour agrandir*

![](../../../assets/image2020-10-6-19-40-46.png) <b>Matériau compact</b> (3)

Identique à la matière.

Les entrées et les sorties appartenant au même *groupe* sont réduites.

</td>
</tr>
</table>

Vous pouvez basculer entre les modes à tout moment dans la barre d&#39;outils du graphique en cliquant sur le bouton ![](../../../assets/link-creation-mode.png) <b>Mode de création de lien</b> ou à l&#39;aide des raccourcis clavier répertoriés ci-dessus.

Dans les modes <b>Matériau</b> et <b>Matériau compact</b>, les connexions entre les entrées et les sorties avec *utilisations non correspondantes* sont interdites.

## Les modes

|  | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-25.png"/></div> Standard | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-17-11-20.png"/></div> Compacter | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-46.png"/></div> Matériau compact |
| --- | --- | --- | --- |
| <b>Entrées</b> | Toutes les entrées sont visibles | Toutes les entrées sont visibles | Seulement 1 entrée par groupe |
| <b>Sorties</b> | Toutes les sorties sont visibles | Toutes les sorties sont visibles | Une seule sortie par groupe |
| <b>Liens</b> | Tous les liens sont visibles | Tous les liens sont visibles | Un seul lien par groupe (vert) |
| <b>Connexions</b> | Vous connectez les liens un par un | Vous connectez des liens en tant que groupe de matériaux à liens multiples en fonction des utilisations correspondantes.   Lorsqu’une utilisation est présente à une extrémité, la connexion est une connexion standard. | Vous connectez des liens en tant que groupe de matériaux à lien unique. |

## Affectation de groupes

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Vous devez affecter des groupes aux nœuds <b>Entrée</b> et <b>Sortie</b> du graphique afin d&#39;utiliser les modes <b>Matériau</b> et <b>Matériau compact</b>.

Vous attribuez un groupe dans les paramètres <b>Attributs</b> du nœud en remplissant le nom du groupe dans la propriété <b>Groupe</b>. Un groupe peut correspondre à n&#39;importe quelle valeur de chaîne et les liens seront regroupés s&#39;ils partagent *exactement le même* nom de groupe sensible à la casse.

Les entrées et sorties groupées d&#39;un graphique sont indiquées visuellement en étant *entourées d&#39;une capsule sombre* sur les instances de nœuds référençant ce graphique.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Capsule de groupe sur le nœud](../../../assets/link-creation-mode-group-node.png "Capsule de groupe sur le nœud"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![Attribut de groupe](../../../assets/link-creation-mode-group.png "Attribut de groupe"){zoomable="yes"}

*Cliquer pour agrandir*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## Correspondance des liens avec l’utilisation

Une fois les liens regroupés, les entrées individuelles doivent être mises en correspondance avec les sorties. Cela se fait via l&#39;attribut <b>Utilisation</b> des nœuds <b>Entrée</b> et <b>Sortie</b>. Si l&#39;utilisation entre l&#39;entrée et la sortie *correspond*, un lien sera créé. Si aucune utilisation correspondante n’est trouvée, aucun lien n’est établi.

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![Attribut d&#39;utilisation](../../../assets/link-creation-mode-usage.png "Attribut d&#39;utilisation"){zoomable="yes"}

*Cliquer pour agrandir*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>
