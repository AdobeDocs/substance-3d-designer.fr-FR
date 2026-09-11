---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: Découvrez comment exporter des textures et des bitmaps à partir de graphes de composition de Substances pour les utiliser dans des applications et des workflows externes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportation d’images bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Exportation d’images bitmap

Cette page explique comment Substance 3D Designer peut exporter vers de nombreux formats de fichiers Bitmap différents et comment exporter plusieurs mosaïques d’UV par lots.Si vous souhaitez [exporter vers des fichiers PSD](../exporting-psd-files/exporting-psd-files.md), une page distincte est dédiée à cette opération.

![Exportation simplifiée](exporting-bitmaps.resources/exportflow.png "Exportation simplifiée")

## Exportation de concepts

Il est bon de garder à l’esprit les points suivants lors de l’export d’un bitmap :

* Vous<b> exportez à partir d&#39;un Graphe</b>, et non d&#39;un pack. Un pack ne génère pas de contenu image par lui-même.
* Le nombre (et la résolution) de bitmaps exportés sont déterminés par les <b>Sorties</b> d&#39;un Graphe.
* Le type de fichier est défini pour toutes les sorties/bitmaps.
* L&#39;exportation est différente de la [publication](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md). Assurez-vous de bien comprendre la différence !

## Méthodes d’exportation

Une fois que vous êtes prêt à exporter, il existe deux façons d’accéder à la boîte de dialogue Exporter :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Dans la fenêtre [Explorateur](../../interface/the-explorer-window/the-explorer-window.md), cliquez avec le bouton droit de la souris sur le Graphe à exporter et sélectionnez **« Exporter les sorties sous forme d&#39;images bitmap »**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

Dans la [Vue du graphe](../../interface/the-graph-view/the-graph-view.md), en cliquant sur le bouton Outils ![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png) et en choisissant **« Exporter les sorties... »**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## Boîte de dialogue Exporter

La boîte de dialogue Exporter vous présente quelques options pour personnaliser votre exportation.

La version affichée à droite est la boîte de dialogue standard, le changement de résolution se produit soit sur le Graphe, les Sorties ou en définissant la résolution parent avant d’ouvrir la boîte de dialogue.

1. <b>Destination : </b>emplacement de tous les fichiers à enregistrer.
1. <b>Format :</b> type de fichier utilisé pour tous les fichiers exportés.
1. <b>Motif</b> : méthode générique pour générer des types de fichiers basés sur des mots-clés de métadonnées. Un exemple de nom de fichier basé sur la première sortie est indiqué ci-dessous, à des fins de vérification.\
   Toutes les options disponibles sont répertoriées ci-dessous :
   1. *$(graphe)* - nom du Graphe actuel
   1. *$(identifiant)* - identifiant de la sortie actuelle
   1. *$(description)* - description de la sortie actuelle
   1. *$(label)* - libellé de la sortie actuelle
   1. *$(user\_data)* - données utilisateur personnalisées de la sortie actuelle
   1. *$(groupe)* - groupe de sortie de la sortie actuelle
   1. *$(colorspace)* - espace colorimétrique de la sortie actuelle (disponible uniquement pour les modes *OCIO* et *ACE Adobe* [gestion des couleurs](../../color-management/color-management.md))
1. <b>Sorties :</b> Activez ou désactivez des sorties et des groupes de sorties spécifiques à partir de votre Graphe. Les boutons activent ou désactivent tous les éléments. Utile lorsqu’une seule image bitmap a été modifiée.
1. <b>Exportation automatique :</b> bouton bascule pour activer la réexportation automatique des Sorties du graphe dès qu&#39;une modification est apportée. Uniquement pour le graphe actif. Peut être lourd et lent en fonction des paramètres.
1. <b>Bouton Exporter :</b> exporte avec les paramètres actuels ou ferme la boîte de dialogue.

![Boîte de dialogue Exporter les sorties](exporting-bitmaps.resources/fromgraph-1.png "Boîte de dialogue Exporter les sorties")

## Boîte de dialogue Exporter (Lot/UV)

Lorsque vous travaillez avec des maillages UV-Tile dans Designer, la boîte de dialogue Exporter peut être utilisée d’une manière légèrement différente qui permet l’exportation par lots de plusieurs UV-Tile à la fois. Assurez-vous de bien comprendre ce workflow et d&#39;avoir correctement attribué un [graphe de Substance](../../compositing-graphs/substance-compositing-graphs.md) à une ou plusieurs UV-Tiles.\
L’onglet Lot permet également d’exporter plus rapidement votre graphe à une résolution différente de la résolution de travail (parent).

Démarrez la boîte de dialogue avec les mêmes méthodes que celles décrites ci-dessus, en vous assurant simplement d&#39;avoir *fait un clic droit sur le graphe attribué par UV-Tile dans l&#39;Explorateur*, ou d&#39;avoir *ouvert le Graphe attribué par UV-Tile* dans la Vue du graphe lors de l&#39;utilisation du bouton Outils.

1. <b>Onglet Traitement par lots</b> : assurez-vous de sélectionner cet onglet au lieu de la méthode <b>Par Graphe</b> standard, sinon les options 2 à 3 ne seront pas disponibles.
1. <b>Tuiles UV :</b> tout comme pour les sorties, vous pouvez activer ou désactiver l&#39;exportation de Tuiles UV spécifiques.
1. <b>[Taille de sortie](../../compositing-graphs/output-size/output-size.md) : </b>Remplacez la résolution d&#39;exportation, ce qui vous permet de travailler plus petit et plus efficace, tout en exportant à la taille maximale.

![Boîte de dialogue Sorties d’exportation par lot](exporting-bitmaps.resources/batch.png "Boîte de dialogue Sorties d’exportation par lot")
