---
helpx_url: ""
breadcrumb-title: ''
description: Utilisez la fenêtre contextuelle Displacement pour régler rapidement le displacement et la facettisation appliqués aux maillages dans une scène 3D.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vue 3D - fenêtre contextuelle Displacement
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# Fenêtre contextuelle displacement

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>La fenêtre contextuelle Displacement disponible dans la barre d’outils Vue 3D offre des commandes directes pour le displacement et la facettisation des filets.</p>
            <p>Il existe trois paramètres :<ul>
                <li>Échelle de height</li>
                <li>Niveau de height</li>
                <li>Tessellation</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="Fenêtre contextuelle displacement dans la vue 3D" />
        </td>
    </tr>
</table>

## Échelle de height

Distance maximale de displacement des sommets du filet le long de leur normale, en unités de scène.<br>
Il s’agit de la distance parcourue pour une valeur de 1,0 dans la carte des heights.

Lorsqu&#39;un graphique de Substance est connecté à un matériau et qu&#39;il inclut un [nœud de sortie](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) avec
<code>heightScale</code> utilisation, alors le paramètre d&#39;échelle d&#39;Height dans la fenêtre contextuelle est *désactivé* pour ce matériau
car il est actuellement piloté par le graphique.

>[!TIP]
> 
>Utilisez le nœud [Height aux unités universelles normales](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) et faites correspondre son paramètre « profondeur de l&#39;Height » à la valeur « Échelle de l&#39;Height »
>pour assurer un ombrage correct lors de l’utilisation de displacement.

## Niveau de height

Valeur de niveaux de gris dans la carte d&#39;height utilisée comme *point médian* pour l&#39;height de displacement.
C&#39;est-à-dire la valeur de seuil utilisée comme altitude de 0,0.

Les valeurs inférieures à ce seuil entraînent le déplacement des sommets vers l&#39;arrière, tandis que les valeurs supérieures à ce seuil entraînent
sommets déplacés vers l&#39;avant.

## Tessellation

La facettisation consiste à subdiviser des faces maillées individuelles en ajoutant un sommet sur leurs segments, puis en se connectant
tous les sommets vers un nouveau sommet à leur centre, de sorte qu&#39;une face devienne **6**.

Le paramètre définit le nombre de fois où les faces doivent être subdivisées de manière récursive.

L&#39;*étendue* du paramètre de facettisation varie en fonction du *moteur de rendu* actuellement utilisé : il peut être appliqué
par maille ou par matière.

### Par filet

Lors de l&#39;utilisation du rendu [Pixelliseur](../3d-renderers/3d-renderers.md#rasterizer) ou [Pathtracer GPU](../3d-renderers/3d-renderers.md#gpu-pathtracer), chaque objet filet de la scène a un *séparateur*
valeur de subdivision.

La subdivision est contextuelle : elle est optimisée de sorte que seule une surface présente une *valeur d&#39;height non uniforme* ou
une *map height non plate* sera subdivisée, quelle que soit la valeur du paramètre.

### Par matériau

Lors de l&#39;utilisation du moteur de rendu [OpenGL](../3d-renderers/3d-renderers.md#opengl), chaque matériau de la scène a une valeur de subdivision *distincte*, qui
est appliqué à *toutes les faces utilisant ce matériau*.

La subdivision n&#39;est pas contextuelle : les surfaces sont subdivisées le nombre de fois spécifié indépendamment de leur courant
Valeur ou texture height.

## Visualisation de la tessellation

Vous pouvez visualiser le résultat de la tessellation en vérifiant la **structure filaire** du maillage.<br>
Les étapes permettant d’afficher la structure filaire de chaque moteur de rendu sont décrites ci-dessous :

### Pixellisation/Pathtracer GPU

Utilisez la commande <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **Paramètres de rendu**
 , puis dans le dock Propriétés, accédez à **Paramètres de rendu > Mode diagnostic** et sélectionnez la **Structure filaire
 Option (espace monde)**.

### OpenGL

Utilisez la commande <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Structure filaire**
 bouton.
