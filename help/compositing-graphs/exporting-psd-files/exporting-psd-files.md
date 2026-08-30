---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Découvrez comment exporter des graphiques de composition de Substances sous forme de fichiers de PSD pour les utiliser dans Adobe Photoshop et d’autres workflows de retouche d’images.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Export de fichiers PSD
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# Export de fichiers PSD

Substance 3D Designer permet d’exporter des textures vers un document Adobe Photoshop ou un fichier PSD.Cette page explique l’interface spéciale utilisée pour convertir les nœuds d’un graphique en calques.**Ce processus n&#39;est pas automatique : vous avez beaucoup de contrôle, mais il est limité et souvent impossible d&#39;obtenir une correspondance précise entre les nœuds et les calques.** En outre, rien ne garantit que votre PSD contienne les mêmes sorties que votre graphique, sauf si vous le configurez explicitement à cet effet. En règle générale, plus vous souhaitez être précis et correct, plus l’utilisateur doit fournir d’efforts. En général, la seule chose qui peut être répliquée de près de manière non destructive est [Nœuds de fusion](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Les calques de réglage ne sont pas pris en charge, de même que les styles de calque et tout ce qui est autre que les modes de fusion de calque.

[Substance 3D Designer peut également exporter des fichiers au format bitmap.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## Boîte de dialogue Exportation de PSD

La boîte de dialogue d’exportation par PSD ne peut être ouverte que par une seule méthode. Dans la [vue Graphique](../../interface/the-graph-view/the-graph-view.md) du graphique que vous souhaitez exporter vers PSD, cliquez sur le bouton ![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>Outils</b> et sélectionnez <b>Exportateur de PSDS</b>. L&#39;interface devient visible dans la <b>Vue graphique</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Interface utilisateur de l&#39;exportateur de PSDS](exporting-psd-files.resources/psd-dialog.png "Interface utilisateur de l&#39;exportateur de PSDS")

</td>
<td style="border: 0;" valign="top">

1. <b>Nom et emplacement du fichier :</b> configurez ici le dossier et le nom de fichier à exporter. Appuyez sur le bouton Exporter pour exécuter le processus d’exportation.
1. <b>Ajouter un groupe :</b> ajoute un groupe de calques
1. <b>Liste déroulante Ajouter un calque :</b> choisissez l&#39;une des deux méthodes pour ajouter un calque. Les calques peuvent également être ajoutés en *faisant glisser les nœuds avec le bouton droit de la souris* dans la pile.
1. <b>Liste déroulante Supprimer le calque :</b> supprimez tous les calques ou ceux sélectionnés.
1. <b>Layerstack :</b> la plupart du travail de configuration s&#39;effectue ici. L’interface reflète les options limitées de Photoshop. Configurez le nom du calque, le mode de fusion et l’opacité ici. Si un calque comporte deux vignettes, la seconde représente la couche Alpha.

</td>
</tr>
</table>

## Workflow

Comme Photoshop ne prend pas directement en charge les matériaux à sorties multiples, il existe plusieurs façons de configurer votre PSD. Vous trouverez ci-dessous un aperçu de la méthode la plus courante.

* Configurez un certain nombre de dossiers pour toutes vos sorties. Un dossier pour Couleur de base, un pour Normal, un pour Rugosité, etc.
* Cliquez avec le bouton droit de la souris et glissez-déposez vos sorties dans le groupe approprié. Si vous voulez que les choses restent simples, le PSD peut être laissé à ce seul endroit.
* Pour développer davantage le PSD : replacez-vous à gauche du graphique, en déposant les étapes intermédiaires pertinentes de votre graphique dans le groupe approprié. Il ne sera pas possible de partager des calques entre les sorties/groupes.

Dans les rares cas où votre PSD est la sortie la plus importante, vous pouvez construire votre graphique de sorte que vous n’utilisiez que des modes de fusion. Dans ce cas, il devrait être possible de recréer une version plus modifiable de votre graphique sous la forme d’un document multicalque.
