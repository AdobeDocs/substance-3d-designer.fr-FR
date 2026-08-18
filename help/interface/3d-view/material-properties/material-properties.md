---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/interface/3d-view/material-properties.html"
breadcrumb-title: ''
description: Configurez les propriétés de la matière dans la vue 3D pour prévisualiser et ajuster l’apparence des matières de Substance sur les objets 3D.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Material properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Propriétés de la matière
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 29%

---


# Propriétés de la matière

La [Vue 3D](../../../interface/3d-view/3d-view.md) restitue la surface des modèles à l&#39;aide d&#39;un programme appelé *shader*. L’ombrage définit le matériau
appliqué au modèle à l&#39;aide d&#39;une liste de propriétés qui ont un impact sur divers aspects de l&#39;apparence du modèle.

Le menu **Matières** de la vue 3D vous permet de vérifier quel nuanceur est utilisé pour chaque matière de la scène.

<a name="openpbr"></a>

## OpenPBR

Designer utilise le modèle de matériau [OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/) par défaut, qui prend en charge plusieurs effets complexes tels que l&#39;anisotropie,
transmission et flou.

Les [modèles de graphique](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#graph-templates) par défaut et les [échantillons de matière](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#material-samples) inclus dans Designer sont tous basés sur le modèle OpenPBR.

Les propriétés de cet ombrage suivent la [référence de paramètre d&#39;OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/#parameterreference) et sont *partagées* sur le pixelliseur,
Pathtracer GPU et OpenGL [rendu 3D](../3d-renderers/3d-renderers.md).

+++ UV

| Paramètre | Type | Par défaut | Description |
|---------------------------------|---------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Répétition | Flottant | 1.0 | Le nombre de répétitions de texture dans une cellule UV, où une valeur plus élevée<br/>entraîne plus de répétitions de texture. |
| Activ. taille physique à partir du graphe | Booléen | False | Ajustez automatiquement la mosaïque en fonction de la [Taille physique](../../../compositing-graphs/graph-parameters/graph-parameters.md)<br/>du graphique afin de représenter le matériau à l&#39;échelle appropriée. |
| Échelle UV | Flottant2 | 1.0, 1.0 | Ajuste l&#39;échelle de la mosaïque par un facteur distinct pour U et V, où<br/>une valeur plus élevée entraîne davantage de répétitions de texture. |

+++

+++ Base

| Paramètre | Type | Par défaut | Description |
|-------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 1.0 | Multiplicateur de l’intensité de la réflexion de la base diffuse et métallique. |
| Couleur | Float3 (RGB) | 0.8, 0.8, 0.8 | Couleur de la réflexion provenant de la base diffuse et métallique. |
| Metalness | Flottant | 0.0 | Indique le degré de métallique du matériau de base. (Compose la base de diélectrique pur à métal pur) |
| Rugosité diffuse | Flottant | 0.0 | Rugosité de la réflexion diffuse. Plus la valeur est élevée, plus la surface paraît plate. |

+++

+++ Spéculaire

| Paramètre | Type | Par défaut | Description |
|------------|--------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 1.0 | Multiplie la réflectivité spéculaire. |
| Couleur | Float3 (RGB) | 1.0, 1.0, 1.0 | Couleur du reflet du specular. (Contrôle la teinte de contour physique pour les métaux,<br/> et une teinte globale non physique pour les diélectriques) |
| Rugosité | Flottant | 0.3 | Rugosité du reflet du specular. Les valeurs faibles produisent des <br/>reflets plus nets, tandis que les valeurs élevées produisent des reflets plus flous. |
| Anisotropie | Flottant | 0.0 | La polarisation directionnelle de la rugosité de la base métallique/diélectrique, ce qui<br/>produit des reflets de plus en plus étirés le long de la tangente. |
| IOR | Flottant | 1.5 | Indice de réfraction de la base diélectrique. |

+++

+++ Transmission

| Paramètre | Type | Par défaut | Description |
|------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 0.0 | Poids du mélange entre la base diélectrique transparente et opaque.<br/>Plus la valeur est élevée, plus le matériau est transparent. |
| Couleur | Float3 (RGB) | 1.0, 1.0, 1.0 | Contrôle la couleur de la base transparente en raison de l&#39;absorption volumétrique<br/>de la loi de Beer sous la surface. |
| Profondeur | Flottant | 0.0 | Spécifie la distance parcourue par la lumière à l&#39;intérieur de la base transparente avant qu&#39;<br/>elle ne devienne exactement la `transmission_color` selon la loi de Beer. |
| Graphique de dispersion | Float3 (RGB) | 0.0, 0.0, 0.0 | Contrôle la couleur de la lumière diffusée volumétriquement à l’intérieur de la base transparente. |
| Anisotropie | Flottant | 0.0 | Valeur de la polarisation directionnelle, ou anisotropie, de la diffusion volumétrique<br/>dans la base transparente. |
| Échelle de dispersion | Flottant | 0.0 | Met à l’échelle de manière linéaire la quantité de dispersion. |
| Nombre d’Abbe | Flottant | 20.0 | Numéro Abbe physique du milieu diélectrique, décrivant la variation<br/>de l&#39;indice diélectrique de réfraction entre les longueurs d&#39;onde. |

+++

+++ Sous-surface

| Paramètre | Type | Par défaut | Description |
|--------------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 0.0 | Poids du mélange qui compose la base diélectrique opaque entre <br/>réflexion diffuse et diffusion sous la surface. |
| Couleur | Float3 (RGB) | 0.8, 0.8, 0.8 | Couleur de réflexion observée pour un milieu avec subsurface scattering. |
| Rayon | Flottant | 1.0 | Échelle de longueur du chemin libre moyen pour le subsurface scattering. |
| Échelle de rayon | Float3 (RGB) | 1.0, 0.5, 0.25 | Multiplicateur RGB à subsurface_radius, donnant la diffusion par canal<br/>tracés sans moyenne. |
| Anisotropie | Flottant | 0.0 | Contrôle la fonction de phase de la diffusion souterraine, où zéro<br/>dispersion la lumière uniformément, les valeurs positives la dispersion vers l&#39;avant et les valeurs négatives la dispersion vers l&#39;arrière.<br/> |

+++

+++ Revêtement

| Paramètre | Type | Par défaut | Description |
|------------|--------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 0.0 | La présence d&#39;une couche réfléchissante de revêtement transparent sur le dessus du matériau.<br/>À utiliser pour des matériaux tels que la peinture automobile ou un calque huileux. |
| Couleur | Float3 (RGB) | 1.0, 1.0, 1.0 | Couleur de la transparence de la couche de revêtement, due à l’absorption dans le revêtement. |
| Rugosité | Flottant | 0.0 | Rugosité des reflets du pelage transparent.<br/>Plus la valeur est faible, plus le reflet est net. |
| Anisotropie | Flottant | 0.0 | Le biais directionnel de la rugosité du calque clear-coat,<br/>résultant en des hautes lumières de plus en plus étirées le long de la direction de la tangente du pelage. |
| IOR | Flottant | 1.6 | Indice de réfraction de la couche de revêtement transparent. |
| Obscurcissement | Flottant | 1.0 | Module l’effet physique d’obscurcissement du revêtement. |

+++

+++ Fibres

| Paramètre | Type | Par défaut | Description |
|-----------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 1.0 | La présence d&#39;une couche de peluche qui peut être utilisée pour approximer les microfibres,<br/>pour des tissus tels que le velours et le satin ainsi que des grains de dust. |
| Couleur | Float3 (RGB) | 1.0, 1.0, 1.0 | Couleur de la couche de fibres. |
| Rugosité | Flottant | 0.5 | Rugosité de la couche de fibres. |

+++

+++ Émission

| Paramètre | Type | Par défaut | Description |
|-----------|--------------|---------------|------------------------------------------------------|
| Luminance | Flottant | 0.0 | Quantité de lumière émise, en tant que luminance en nits. |
| Couleur | Float3 (RGB) | 1.0, 0.0, 0.0 | Couleur de la lumière émise. |

+++

+++ Film mince

| Paramètre | Type | Par défaut | Description |
|-----------|-------|---------|-------------------------------------------------------------------------------------------------------|
| Poids | Flottant | 0.0 | Poids de couverture du film mince.<br/>À utiliser pour des matériaux tels que la peinture de voiture polychrome ou les bulles de savon. |
| Épaisseur | Flottant | 0.5 | Thickness de la couche mince sur le support. (En micromètres) |
| IOR | Flottant | 1.4 | Indice de réfraction du film mince. |

+++

+++ Géométrie

| Paramètre | Type | Par défaut | Description |
|-------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opacité | Flottant | 1.0 | Opacité du matériau entier. |
| Paroi fine | Booléen | False | Si la valeur est true, la surface est à deux côtés et représente une coque infinitésimalement mince.<br/>Convient aux objets très fins géométriquement comme les feuilles ou le papier. |
| Normale | Float3 (RGB) | 0.5, 0.5, 1.0 | Normale géométrique d’entrée pour la surface. |
| Tangente | Float3 (RGB) | 1.0, 0.5, 0.0 | Tangente géométrique d’entrée. |
| Normale du revêtement | Float3 (RGB) | 0.5, 0.5, 1.0 | Normale d’entrée pour la couche de revêtement. |
| Tangente du revêtement | Float3 (RGB) | 1.0, 0.5, 0.0 | Tangente géométrique d’entrée pour la couche de revêtement. |
| Hauteur | Flottant | 0.5 | Displacement (ou bosse) dans la direction de la normale.<br/>Lorsque l&#39;height est égal au niveau de l&#39;height, il n&#39;y a pas de displacement.<br/>Le Displacement est un changement scalaire de la position de la surface vers une surface normale lissée<br/>non perturbée.<br/>Lorsque le displacement tesselé n&#39;est pas possible ou souhaité,<br/>l&#39;height peut être implémenté en tant que carte de relief. |
| Niveau de height | Flottant | 0.5 | Valeur d&#39;height correspondant à l&#39;absence de displacement (valeur de niveau zéro).<br/>Le niveau d&#39;Height décale (mais ne met pas à l&#39;échelle ni ne retourne) le displacement par rapport<br/>à la surface de l&#39;objet non déplacé.<br/>Si le niveau d&#39;height est 0, tout le displacement est au-dessus.<br/>Si le niveau d&#39;height est défini sur 1, tous les displacements se trouvent sous la surface, mais ils conservent<br/>la même échelle et la même direction. |
| Échelle de height | Flottant | 1.0 | Échelle du displacement ou de la relief en unités d’espace de la scène.<br/>L&#39;amplitude et la direction de l&#39;échelle sont indépendantes de la valeur du niveau d&#39;height. |
| Occlusion ambiante | Flottant | 1.0 | Carte d&#39;occlusion ambiante pour obscurcir les zones occultées.<br/>Blanc (1.0) signifie entièrement éclairé, noir (0.0) signifie entièrement occulté. |

+++

### Compatibilité avec les graphiques existants

Certaines propriétés OpenPBR Material ont des identifiants d’utilisation différents de ceux d’autres modèles inclus dans Designer.
Designer fait correspondre automatiquement certains identifiants pour assurer la compatibilité avec OpenPBR comme modèle par défaut.

+++ Mappages hérités à OpenPBR

| Héritage | OpenPBR |
|-------------------------|-----------------------------|
| métallique | métallurgie |
| specularEdgeColor | specularColor |
| rugosité | rugositéspéculaire |
| anisotropyLevel | specularRoughnessAnisotropy |
| IOR | IOR spéculaire |
| absorptionColor | transmissionColor |
| absorptionDistance | transmissionDepth |
| transparence | subsurfaceWeight |
| scatteringColor | subsurfaceColor |
| DistanceDeDiffusion | subsurfaceRadius |
| scatteringDistanceScale | subsurfaceRadiusScale |
| coatOpacity | coatWeight |
| sheenOpacity | fuzzWeight |
| sheenColor | fuzzColor |
| sheenRoughness | fuzzRoughness |
| émissif | emissionColor |

+++

### Lectures complémentaires

Pour en savoir plus sur l’OpenPBR, voici quelques ressources :

* [article de blog sur l’Adobe](https://blog.adobe.com/en/publish/2023/08/08/openpbr-strengthens-interoperability-enabling-enhanced-creativity)
* [Livre blanc](https://academysoftwarefoundation.github.io/OpenPBR/)
* [OpenPBR BSDF d’Adobe sur GitHub](https://github.com/adobe/openpbr-bsdf)
* [Designer 16.0 : prise en charge d’OpenPBR](../../../release-notes/version-16-0/version-16-0.md#openpbr-support)

<a name="adobe-standard-material"></a>

## Adobe Standard Material

Le modèle Adobe Standard Material (ASM) a été introduit dans Designer 11.2 et est devenu le shader par défaut de Designer
jusqu’à la version 15.1.

Designer est passé à OpenPBR en tant que nouveau modèle par défaut, mais ASM est toujours inclus et ses propriétés sont également partagées
dans le module de pixellisation, les modules de rendu Pathtracer GPU et OpenGL [3D](../3d-renderers/3d-renderers.md).

Le modèle est documenté [ici](https://experienceleague.adobe.com/en/docs/substance-3d/general-knowledge/asm/adobe-standard-material).

<a name="usdpreviewsurface"></a>

## UsePreviewSurface

L’objectif du modèle UsdPreviewSurface est de prévisualiser les matériaux avec un ensemble de fonctionnalités de base favorisant la compatibilité
sur les systèmes de rendu qui incluent USD et/ou Hydra.

Dans Designer, ce modèle de matériau est uniquement pris en charge par le pixelliseur et les [rendus 3D par Pathtracer GPU](../3d-renderers/3d-renderers.md).

Le modèle est documenté [ici](https://openusd.org/dev/spec_usdpreviewsurface.html).
