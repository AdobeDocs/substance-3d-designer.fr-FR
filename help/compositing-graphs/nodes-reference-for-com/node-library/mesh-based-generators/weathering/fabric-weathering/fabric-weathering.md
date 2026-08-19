---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du tissu pour ajouter des effets d'usure et de vieillissement aux matériaux du tissu en fonction de la géométrie et de la courbure du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altération Du Tissu
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# Altération Du Tissu

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## Altération Du Tissu

**Entrée :** *Générateurs À Maillage**/Résilience*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il ajoute un effet d&#39;usure aléatoire du tissu, avec un contrôle de l&#39;âge et de la saleté.\
Cet effet ne fonctionne pas très bien à moins que vous n&#39;ayez branché les cartes AO et World Space Normalmaps correctement préparées, car elles nécessitent que celles-ci calculent et génèrent tout de manière adéquate.

Assurez-vous de bien comprendre les [modes de création de liens](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) lorsque vous travaillez avec des matériaux complets.

## Paramètres

### Entrées

* **Occlusion ambiante** : *Entrée en niveaux de gris*\
  Map bakée utilisée pour les effets internes et le masquage.
* **Espace Mondial Normal** : *Entrée Couleur*
* **Masque** : *Entrée En Niveaux De Gris*\
  Emplacement de masque utilisé pour masquer les effets du nœud. Peut être basculé avec le paramètre « Mask ».

### Paramètres

* **Canaux**
  * Activez et désactivez les canaux de matériau dans ce groupe, par exemple lorsque vous utilisez des cartes de Specular/brillance au lieu de cartes de métal/rugosité.
* **Avancé**
  * **Format normal** : *DirectX, OpenGL*\
    Bascule entre différents formats de mappage normal (inverse la couche verte).
  * **Masque** : *Faux/Vrai*\
    Active ou désactive l&#39;utilisation de la carte de masque.
* **Effet**
  * **Dust** :*0.0 - 1.0* crée un effet de dust plus sombre, en fonction des zones orientées vers le haut dans la carte normale de l&#39;espace universel.
  * **Sale** :*0.0 - 1.0* Mélange dans un effet global de dirt/maculage, basé principalement sur les zones occultées (sombres) dans l&#39;AO.
  * **Usure des bords** :*0.0 - 1.0* Ajoute un effet de netteté/intensification aux bords, en fonction de la normale de la matière.
  * **Utilisé** :*0,0 - 1,0* Mélanges dans le dirt accumulé très foncé avec des plis, en fonction de l’AO. Les valeurs Maximale et Minimale ont tendance à être très extrêmes. Utilisez-les avec précaution.
  * **Âge** :*0,0 - 1,0* se fond sur un motif d’usure global du carrelage. Le contrôle du seuil en dessous contrôle l’influence de l’IA. Les valeurs maximales et minimales ont tendance à être très extrêmes.
  * **Seuil d&#39;âge** : *0.0 - 1.0* Définit la mesure dans laquelle l&#39;AO affecte le paramètre Âge.
  * **Plis par âge** :*0,0 - 1,0* contrôle le mélange de légers plis supplémentaires dans l&#39;effet Âge.
  * **Échelle Scratches des contours nets** :*1.0 - 32.0* définit l’échelle des petites rayures, qui éliminent principalement l’effet Utilisé et Âge.
  * **Intensité de la déformation Scratches des contours nets** : *0.0 - 1.0* Définit l’intensité de la déformation pour les petites rayures ci-dessus.
  * **Désaturation de l’ancien tissu** :*0.0 - 1.0* contrôle la désaturation de l’effet Age.
  * **Luminosité de l’ancien tissu** :*0.0 - 1.0* contrôle la luminosité de l’effet Age. *Il s&#39;agit d&#39;un paramètre très important à modifier pour obtenir l&#39;aspect que vous souhaitez, mais les résultats peuvent être extrêmes : à utiliser avec des modifications subtiles.*
* **Fusion**
  * **Intensité diffuse** : *0,0 - 1,0*\
    Intensité de fusion du diffus.
  * **Intensité des couleurs de base** : *0.0 - 1.0*\
    Intensité de fusion de la couleur de base.
  * **Intensité normale** : *0,0 - 1,0*\
    Intensité de fusion de la normale.
  * **Intensité du Specular** : *0,0 - 1,0*\
    Intensité de fusion du Specular.
  * **Intensité du brillant** : *0.0 - 1.0*\
    Intensité de fusion du brillant.
  * **Intensité de la rugosité** : *0.0 - 1.0*\
    Intensité de fusion de la rugosité.
  * **Intensité de l&#39;Occlusion ambiante** : *0,0 - 1,0*\
    Intensité de fusion de l&#39;Occlusion ambiante.
  * **Intensité des Heights** : *0,0 - 1,0*\
    Intensité de fusion de l&#39;Height.

## Exemples d’images

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
