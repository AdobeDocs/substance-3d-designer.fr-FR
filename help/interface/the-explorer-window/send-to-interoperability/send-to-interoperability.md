---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Utilisez la fonction Envoyer vers l’interopérabilité de Substance 3D Designer pour exporter des matériaux vers d’autres applications.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Envoyer à...  Interopérabilité
user-guide-description: ''
user-guide-title: ''
source-git-commit: 16eb8a173e984f842c820f3b8f0c3e140040bdfa
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# Envoyer à...  Interopérabilité

![Envoyer de Designer vers les applications Substance 3D](send-to-interoperability.resources/explorer-interop.png "Envoyer de Designer vers les applications Substance 3D"){width="512px"}

Adobe Substance 3D Designer est en interopérabilité avec [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) et [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html). Cela vous permet d&#39;*envoyer* et de *renvoyer* votre travail rapidement, ce qui facilite l&#39;itération dans l&#39;écosystème Substance 3D.

Le workflow est généralement le suivant :

1. Définir l&#39;attribut <b>Type</b> dans les [propriétés d&#39;un graphe de Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md)
1. Dans le panneau [Explorateur](../the-explorer-window.md), sélectionnez le pack que vous souhaitez envoyer
1. Dans la liste déroulante <b>Publish/Envoyer</b> de l&#39;Explorateur, sélectionnez l&#39;application cible
1. Apporter des modifications aux graphes
1. Répétez l’étape 3 pour renvoyer le package et mettre à jour la ressource envoyée existante avec vos modifications

>[!WARNING]
>
> Les fonctionnalités d&#39;interopérabilité ne sont *pas* disponibles dans la version <b>Steam</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Définition du type de graphe

Les graphes de Substance peuvent avoir de nombreuses fonctionnalités. Vous devrez définir à l&#39;avance la fonctionnalité exacte d&#39;un graphe, pour vous assurer qu&#39;il peut être envoyé correctement.

Dans la section <b>Attributs </b> des [propriétés d&#39;un graphe de Substance de données](../../../compositing-graphs/graph-parameters/graph-parameters.md), il y a une option <b>Type</b>, avec une liste déroulante qui comporte les options suivantes :

</td>
<td style="border: 0;" valign="top">

![Attribut Type du graphe de Substance](send-to-interoperability.resources/type-attribute.jpg "Attribut Type du graphe de Substance")

</td>
</tr>
</table>

* **Non spécifié** est le type par défaut si vous ne l&#39;avez pas défini. En fonction de l’application à laquelle vous envoyez l’accord, celui-ci peut être interprété différemment. Par exemple, [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) sera défini par défaut sur Matériau ;
* **Le Matériau standard** est destiné aux matériaux PBR multicanaux, avec des [sorties](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) correctement étiquetées ;
* **Matériau de décalcomanie** est destiné à un matériau PBR multicanal avec canal Alpha, à appliquer en tant que décalcomanie dans [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) ou [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html) ;
* **Matériau Atlas** est destiné à un matériau PBR multicanal composé de plusieurs images d&#39;atlas, à utiliser avec le [nœud d&#39;Atlas scatter](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md) dans Designer ou [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html) ;
* **Filtre** est destiné aux filtres universels, tous deux utilisés dans [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) ou [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html) ;
* **Le générateur basé sur le Maillage** est destiné aux générateurs de masque à entrées multiples. Ce paramètre est utilisé uniquement par [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) ;
* **Le générateur de Textures** est destiné aux cartes à canal unique, comme les procédures et les bruits 2D ;
* **L&#39;Éclairage d&#39;environnement** est destiné à un environnement d&#39;éclairage à canal unique, utilisé pour éclairer des scènes et des objets ;
* La **texture de lumière** correspond à une texture de canal unique appliquée à une lumière physique.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menu « Envoyer à »

Le processus d&#39;envoi a impliqué la [publication](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) d&#39;un ou plusieurs packages dans des fichiers de ressources Substance 3D (SBSAR) situés derrière les scènes.

L’envoi de contenu peut s’effectuer de la manière suivante :

* Cliquez avec le bouton droit de la souris sur un pack et ouvrez le sous-menu <b>Envoyer à...</b> dans le menu contextuel, puis choisissez l’option <b>Envoyer à...</b> pour l’application cible ;
* Cliquez sur le bouton ![](send-to-interoperability.resources/sendto-icon.jpg) <b>Publish/Envoyer</b> en haut du panneau Explorateur, puis choisissez l’option <b>Envoyer à...</b> pour l’application cible.

</td>
<td style="border: 0;" valign="top">

![Menu Publish/Envoyer vers dans Explorateur](send-to-interoperability.resources/explorer-sendto-displayed.jpg "Publish/Envoyer vers dans Explorateur")

</td>
</tr>
</table>

### Renvoi

Lors du nouvel envoi d&#39;un package *déjà envoyé* à la *même application cible*, la ressource sera *mise à jour* dans l&#39;application cible avec la nouvelle version.

## Envoyer à Player

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) prend en charge *les* <b>fichiers Substance 3D</b> (SBS) et <b>actifs Substance 3D</b> (SBSAR).

L&#39;envoi au lecteur nécessite que l&#39;exécutable de la Substance Player de données soit *localisé manuellement* par l&#39;utilisateur, ce qui peut être fait :

* Lorsque vous êtes invité à confirmer que le lecteur n&#39;a *jamais été localisé* depuis l&#39;installation de Designer ;
* À tout moment dans le menu <b>Outils</b>, en utilisant l&#39;option <b>Substance Player > Localiser...</b>.

Dans Player, la réception depuis Designer nécessite que le répertoire d&#39;installation de Substance 3D Designer *1&rbrace; soit localisé manuellement par l&#39;utilisateur, ce qui peut être fait :*

* Lorsque vous êtes invité à confirmer que Designer n&#39;a *jamais été localisé* depuis l&#39;installation de Player ;
* À tout moment dans le menu <b>Options</b>, à l&#39;aide de l&#39;option <b>Localiser Adobe Substance 3D Designer</b>.

>[!NOTE]
>
> Lors de l&#39;envoi de fichiers Substance 3D (SBS) à Player, une ressource Substance 3D (SBSAR) est publiée en tant que *fichier temporaire*.

## Problèmes

Des erreurs peuvent se produire lors de l’envoi de packs, par exemple :

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


Cela est généralement dû à une erreur standard et à des avertissements. Corrigez-les pour résoudre le problème :

* Aucun [nœud de sortie](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)défini dans votre graphe. Ajoutez des nœuds de sortie et connectez-y quelque chose ;
* Variables manquantes ou endommagées dans [Get nodes](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) dans [function graphes](../../../function-graphs/function-graphs.md). Suivez-les à l&#39;aide de la *pastille d&#39;avertissement jaune* sur les nœuds concernés.
