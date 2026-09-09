---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Résolvez les problèmes liés aux paramètres du graphe de Substance qui ne fonctionnent pas comme prévu et trouvez des solutions.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Les paramètres ne fonctionnent pas comme prévu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---


# Les paramètres ne fonctionnent pas comme prévu

Cette page répertorie les causes courantes de dysfonctionnement des paramètres dans Substance 3D Designer et propose des étapes de dépannage pour chacune d’elles.

## Le paramètre ne fonctionne pas en mode Aperçu et l’actif Substance 3D publié (SBSAR)

<b> ![(error)](../../assets/error.svg) Problème</b>

Certains paramètres exposés d&#39;un graphe ne sont *pas répertoriés* lors de l&#39;utilisation du [mode Aperçu](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) dans Designer, ou dans la liste de paramètres des ressources Substance 3D (SBSAR) [publiées](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) sur ce graphe.

<b> ![(tick)](../../assets/check.svg)Étapes recommandées</b>

Les paramètres manquants sont probablement des [paramètres statiques](../../glossary/glossary.md), qui *ne peuvent pas être modifiés à la volée* une fois le graphe *cuit*, c&#39;est-à-dire traité afin d&#39;exécuter son algorithme rapidement et efficacement. La cuisson a lieu dans Designer chaque fois que le graphe est *modifié* ou *publié*. Les paramètres affectés par ces limitations sont répertoriés dans la section [Limitations](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de la page [Exposer un paramètre](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) de cette documentation.

Ainsi, les paramètres statiques sont visibles et modifiables dans Designer, mais sont *masqués* dans une ressource Substance 3D publiée. Vous pouvez utiliser le [mode Aperçu](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) pour voir ces limitations en vigueur avant de publier sur une ressource Substance 3D.

Voici une liste des paramètres statiques :

| Nœud | Paramètre |
| --- | --- |
| Tous les nœuds | Mode répétition Format des pixels |
| [Couleur uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Mode colorimétrique |
| [Processeur de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Mode colorimétrique |
| [Fusion](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Zone de recadrage de Simulation de transparence du mode de fusion |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Mode de fusion |
| [Quadrant](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Filtrage d’Image d&#39;entrée alpha de motif |

## Résultat incorrect pour le graphe de fonction de Substance appliqué au paramètre

<b> ![(error)](../../assets/error.svg) Problème</b>

Un graphe de fonction de Substance appliqué à un paramètre de nœud ne produit pas la valeur attendue lorsqu&#39;un entier négatif est utilisé.

<b> ![(tick)](../../assets/check.svg) Étapes recommandées</b>

Les entiers négatifs ne sont actuellement pas pris en charge correctement. Pour contourner le problème, utilisez la valeur entière négative dans une valeur [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) et extrayez-la à l&#39;aide d&#39;un nœud [Swizzle Integer](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md).
