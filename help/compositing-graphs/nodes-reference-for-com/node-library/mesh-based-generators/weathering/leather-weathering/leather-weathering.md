---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Utilisez le nœud Usure du cuir pour ajouter des motifs d'usure et des effets de vieillissement aux matériaux en cuir en fonction de la courbure du maillage.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Météo du cuir
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Météo du cuir

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## Météo du cuir

**Entrée :** *Générateurs À Maillage**/Résilience*

**Complexe**

</td>
<td style="border: 0;" valign="top">

## Description

Il s’agit d’un effet matériel qui fonctionne sur plusieurs canaux à la fois. Il ajoute un effet d&#39;usure aléatoire du cuir, avec un contrôle de l&#39;âge et de la saleté. Elle est similaire à la [altération du tissu](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), mais adaptée spécifiquement pour le cuir.\
Cet effet ne fonctionne pas très bien à moins que vous n’ayez branché les cartes AO et World Space Normalmaps correctement préparées, car elles sont nécessaires pour calculer et générer correctement tout.

Assurez-vous de bien comprendre les [modes de création de liens](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) lorsque vous travaillez avec des matériaux complets.

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
  * **Utilisé** :*0.0 - 1.0* Mélanges dans un look global de cuir usé.
  * **Âge** :*0,0 - 1,0* Mélange dans un look de cuir usé avec des plis basés sur l&#39;AO. Le placement est beaucoup influencé par le seuil d&#39;âge.
  * **Seuil d’âge** : *0,0 - 1,0* définit le seuil d’apparence de l’effet Âge.
  * **Échelle des Fissures** :*1.0 - 16.0* définit la profondeur du cuir usé à partir de l’effet Utilisé et Âge.
  * **Intensité de déformation des Fissures** : *0,0 - 1,0* définit l’intensité du cuir usé à partir de l’effet Utilisé et Age.
  * **Échelle Scratches Des Contours Nets** : *1.0 - 32.0*
  * **Intensité de la déformation Scratches des bords nets** : *0.0 - 1.0*
  * **Désaturation du cuir usagé** :*0.0 - 1.0* Définit la saturation de l&#39;aspect du cuir usé à partir des effets Âge et Utilisé.
  * **Luminosité du cuir usagé** :*0.0 - 1.0* Définit la luminosité de l&#39;aspect du cuir usé à partir des effets Âge et Utilisé.
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
