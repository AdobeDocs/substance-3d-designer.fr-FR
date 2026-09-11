---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/anisotropic-kuwahara.html"
breadcrumb-title: ''
description: Utilisez le filtre Anisotropic Kuwahara Color pour créer des effets de couleur stylisés et picturaux avec lissage directionnel.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Anisotropic Kuwahara Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Couleur kuwahara anisotrope
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---


# Couleur kuwahara anisotrope

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de couleur anisotrope Kuwahara](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/AnisotropicKuwaharaColor.png "Icône Couleur anisotrope Kuwahara"){width="200px"}

<b>Entrée :</b> Filtres > Effets

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Applique un flou directionnel anisotrope conforme aux détails de l’image. Le résultat est une image qui semble *s&#39;écouler* dans la direction des formes qu&#39;elle contient.

Ce flou réglable calcule ou reçoit une *map direction* pour déterminer ce flux, qui peut être accentué pour former des zones plus plates et plus clairement définies.

</td>
</tr>
</table>

L&#39;écoulement peut également être rompu par rotation de la direction dans laquelle le flou est appliqué. De même, une map direction personnalisée peut être utilisée pour remplacer celle calculée à partir de l’image.

Ce filtre peut produire un effet pictural et est utile pour la stylisation.

<b>Anisotropie</b>

L&#39;intensité du flux est principalement contrôlée par le paramètre [Anisotropie](#parameters), comme le montre l&#39;image ci-dessous.

Gauche : Anisotropie 0,0 / Droite : Anisotropie 1,0

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Un bol de fruits avec le filtre kuwahara appliqué avec 0 anisotropie.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_color_example_3_before.jpg){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Un bol de fruits avec le filtre kuwahara appliqué avec 0 anisotropie.](https://helpx.adobe.com/content/dam/substance-3d-designer/substance-graphs/nodes/filters/effects/anisotropic-kuwahara/anisotropic_kuwahara_color_example_3_after.jpg){zoomable="yes"}

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Entrée</b> <i>Couleur</i> Principale | Image couleur à traiter. |
| <b>Mappage d&#39;Anisotropy angle</b> <i>Niveaux de gris</i> | Image en niveaux de gris décrivant la rotation supplémentaire appliquée à la direction calculée, où la valeur de niveaux de gris correspond à un nombre de tours.   Le mappage a toujours un effet lorsque le paramètre « Anisotropie » est défini sur 0, car il affecte la rotation du noyau utilisé par le filtre Kuwahara. |
| <b>feuille de Pente</b> <i>Niveaux de gris</i> | Mappage représentant les pentes auxquelles la map direction est conforme, en fonction de la valeur du paramètre Multiplicateur d&#39;entrée de mappage de Pente. |
| <b>Mappage de rayon (facultatif)</b> <i>Niveaux de gris</i> | Une fois connecté, le « rayon » de flou est multiplié par rapport à l’image d&#39;entrée. |
| <b>Map direction</b> <i>Couleur</i> | Carte décrivant la direction utilisée par le noyau du filtre anisotrope.   Le mappage a toujours un effet lorsque le paramètre « Anisotropie » est défini sur 0, car il affecte la rotation du noyau utilisé par le filtre Kuwahara.   Remarque : cette entrée est utilisée uniquement lorsque le paramètre « Utiliser la Map direction d’entrée » est défini sur « Vrai ». |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Sortie</b> <i>Couleur</i> | Résultat du flou anisotrope appliqué par le nœud sur l’image d&#39;entrée. |
| <b>Map direction</b> <i>Couleur</i> | Map direction calculée à partir de l’image d&#39;entrée et utilisée pour appliquer le flou anisotrope.   Si le paramètre « Utiliser la Map direction d’entrée » est défini sur « Vrai », l’image fournie à l’entrée « Map direction » est utilisée et la sortie telle quelle. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Rayon</b> *Flottant* | Le rayon d’atténuation, où une valeur plus élevée produit un effet d’atténuation plus intense.   La valeur maximale est 32. |
| <b>Smoothness</b> *Flottant* | Règle la quantité de fusion des couleurs dans la direction calculée.   Lorsque cette valeur est définie sur 0, les couleurs sont principalement déplacées dans cette direction et il se produit très peu de fusion. |
| <b>Netteté</b> *Flottant* | Augmente le contraste des zones floues, les rendant plus plates et plus clairement définies. |
| <b>Anisotropie</b> *Flottant* | Ajuste la contribution de la map direction dans le flou.   La map direction et tous ses modificateurs (à la fois les paramètres et les maps d&#39;entrée) ont toujours un effet lorsque cette valeur de paramètre est 0, car la map direction est utilisée dans le noyau de filtre Kuwahara. |
| <b>Utiliser la map direction d&#39;entrée</b> *Booléen* | Lorsque la valeur est True, aucune map direction n&#39;est calculée à partir de l&#39;image d&#39;entrée, et l&#39;image reliée à l&#39;entrée Map direction est utilisée pour appliquer le flou anisotrope à la place. |
| <b>smoothness de capteur</b> *Flottant* *Disponible lorsque &#39;Utiliser la map direction d&#39;entrée&#39; est défini sur &#39;Faux&#39;* | Règle l’intensité du flou appliquée aux directions calculées à partir de l’image et stockées dans la map direction.   L’augmentation de cette valeur garantit un résultat plus lisse lorsque l’image présente de nombreux détails de hautes fréquences. |
| <b>Anisotropy angle</b> *Flottant* *Disponible lorsque &#39;Utiliser la map direction d&#39;entrée&#39; est défini sur &#39;Faux&#39;* | Permet d’ajouter une rotation à la map direction, en nombre de tours.   Cette rotation supplémentaire est *cumulative* avec celle spécifiée par l&#39;entrée &#39;Anisotropy angle Map&#39;. |
| <b>multiplicateur de mappage d&#39;Anisotropy angle</b> *Flottant* *Disponible lorsque &#39;Utiliser la map direction d&#39;entrée&#39; est défini sur &#39;Faux&#39;* | Règle l’intensité des valeurs de l’entrée Cartographie, qui sont ensuite ajoutées au-dessus de la map direction, en nombre de tours.   Cette rotation supplémentaire est *cumulative* avec celle spécifiée par le paramètre « Anisotropy angle ». |
| <b>multiplicateur d&#39;entrée de mappage de Pente</b> *Flottant* *Disponible lorsque &#39;Utiliser la map direction d&#39;entrée&#39; est défini sur &#39;Faux&#39;* | Règle l’intensité d’uniformisation de la map direction par rapport aux pentes fournies par l’entrée « Pente ». |
| <b>Ignorer alpha</b> *Booléen* | Lorsque la valeur est True, le canal Alpha de l’image n’est pas affecté par le filtre.   Lorsque la valeur est False, le filtre est également appliqué au canal Alpha. |

## Exemples

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_2_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_2_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_4_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="https://helpx.adobe.com/libs/settings/wcm/designs/default/resources/0.gif" alt="anisotropic_kuwahara_color_example_4_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>
