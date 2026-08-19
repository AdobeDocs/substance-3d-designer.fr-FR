---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/release-notes/version-14-0.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 14.0 pour en savoir plus sur les nouveaux nœuds, la navigation dans les graphiques et les améliorations des performances.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 14.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 14.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---


# Version 14.0

<b>Substance 3D Designer 14.0 </b>apporte plusieurs améliorations à la qualité de vie (navigation dans les graphiques, performances, ...) mais surtout, il comprend beaucoup de nouveaux nœuds (manipulation de couleur, filtre Kuwahara, outils d&#39;histogramme, bevel smooth, directional distance, ...). Voir ci-dessous pour plus de détails sur toutes ces modifications. 

*Date de publication : 30 juillet 2024*

![](../../assets/2024-BannerRN.png)

## Nouveau contenu

Cette version 14.0 apporte beaucoup de nouveau contenu avec les nouveaux nœuds répertoriés ci-dessous :

* <b>Nœuds dédiés à la manipulation des couleurs : </b>un nœud <b>(</b>[Quantifiez la couleur](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)<b>) </b>à<b> </b>réduisez le nombre de couleurs dans une image et extrayez une palette à partir de celle-ci, une famille de nœuds d’outils pour créer votre propre palette de couleurs ([Afficher](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md) / [Créer](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md) / [Modifier](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md)<b> </b>la palette de couleurs) et un pour l’appliquer à une autre image à l’aide d’une carte d’identité ([Appliquer la palette de couleurs](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)). Vous trouverez également le nœud [ID pour masquer les niveaux de gris](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/id-to-mask/id-to-mask.md) pour convertir votre mappage d&#39;ID (calculé par Quantize color) en masque de niveaux de gris. Avec cet ensemble complet de nœuds, vous disposez de tout ce dont vous avez besoin pour créer des effets de stylisation à l’aide de couleurs.

![](../../assets/GIF2_2.gif){zoomable="yes"}

![Quantifier la couleur 2](../../assets/GIF3_2.gif){zoomable="yes"}

* <b>Filtre Kuwahara</b> : si vous souhaitez aller encore plus loin avec la stylisation, vous pouvez générer des effets picturaux grâce aux filtres [couleur Kuwahara anisotrope](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/anisotropic-kuwahara/anisotropic-kuwahara.md) / [niveaux de gris](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/anisotropic-kuwahara-gra/anisotropic-kuwahara-grayscale.md). Dans les détails, il applique un flou directionnel anisotrope conforme aux détails de l’image. Le résultat est une image qui semble s’écouler dans la direction des formes qu’elle contient.

Ces nœuds (Quantize color et Anisotropic Kuwahara) sont expliqués dans [ce tutoriel](https://www.adobe.com/go/designer-tutorial-quantize_fr). Il montre comment les utiliser pour styliser les matériaux et gérer les couleurs de manière plus efficace et intuitive !

D&#39;autres nœuds puissants rejoignent le parti :

* [<b>Lissage de courbure</b>](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) : cette nouvelle version prend désormais correctement en charge tous les modes de mosaïque, ajoute deux nouvelles sorties (convexité et concavité) et améliore à la fois la précision et les performances.
* <b>[Histogramme égaliser](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-equalize/histogram-equalize.md) :</b> ce nœud égalise l&#39;histogramme d&#39;une image en niveaux de gris en ajustant les valeurs pour obtenir une distribution égale. Ce nœud est fourni avec deux nœuds compagnons : [Rendu de l&#39;histogramme](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-render/histogram-render.md) pour générer l&#39;histogramme de l&#39;image et [Calcul de l&#39;histogramme](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-compute/histogram-compute.md)<b> </b> pour coder un histogramme sous la forme d&#39;une ligne de pixels.
* <b>[Bevel smooth](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md) :</b> grâce à celui-ci, vous pouvez dessiner un dégradé ou une couleur plate à partir des bordures d&#39;un masque (vers l&#39;extérieur, vers l&#39;intérieur ou les deux). Le nœud [Directional distance](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/directional-distance/directional-distance.md)<b> </b>dessine également un dégradé, mais dans une direction spécifique.
* <b>[Combinaison normale](../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-uncombine/normal-uncombine.md):</b> ce nœud est l&#39;opposé du nœud [Combinaison normale](../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md), il supprime d&#39;une carte normale les détails de surface décrits par une carte d&#39;height.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Lissage de courbure

<table>
  <tr>
    <td>
      <img src="../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_blend_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_blend_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

Histogramme égaliser

<table>
  <tr>
    <td>
      <img src="../../assets/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../assets/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Bevel smooth

<table>
  <tr>
    <td>
      <img src="../../assets/bevel_smooth_example_6_before.jpg" alt="biseau_lisse_exemple_6_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../assets/bevel_smooth_example_6_after.jpg" alt="biseau_lisse_exemple_6_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

Dissociation normale

<table>
  <tr>
    <td>
      <img src="../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

## Amélioration de la qualité de vie

* <b>Les performances </b> et la <b>réactivité</b> lors de l’utilisation de projets volumineux ont été améliorées. Par exemple, la suppression de nœuds peut être jusqu’à 75 fois plus rapide. Le temps de [cuisson](../../glossary/glossary.md) a également été réduit pour les graphiques faisant référence à plusieurs fois la même image bitmap.
* <b>Paramètres hérités</b> : lorsqu&#39;un paramètre est [hérité](../../glossary/glossary.md), au lieu d&#39;afficher la valeur par défaut, nous affichons maintenant la valeur héritée afin que vous connaissiez la valeur actuellement utilisée. En savoir plus sur l&#39;héritage dans [cette page dédiée de notre documentation](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).
* La prise en charge de <b>Trackpad</b> sur MacOS a été entièrement remaniée pour être plus naturelle et conforme aux autres logiciels. Le déplacement des nœuds au-delà des limites de la [vue graphique](../../interface/the-graph-view/the-graph-view.md) a également été repensé afin d&#39;être plus fluide et plus cohérent entre tous les systèmes d&#39;exploitation.

* <b>Vue 2D :</b>lorsque l’affichage en mosaïque est activé dans la [vue 2D](../../interface/2d-view/2d-view.md), vous pouvez désormais obtenir des valeurs même pour les pixels qui ne se trouvent pas sur la mosaïque d’origine : il est très utile de vérifier l’[échantillonnage](../../glossary/glossary.md) et les transitions de valeurs entre les mosaïques.

![Vue 2d](../../assets/2dview.gif){width="320px" zoomable="yes"}

* <b>Courbe de transfert de dégradé</b> : utilisez le clic du milieu de la souris pour déplacer toutes les [touches de dégradé](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) vers la gauche ou vers la droite (et ainsi conserver tous les espaces entre toutes les touches).
* <b>Paramètres</b> : pour injecter des fonctions personnalisées via des paramètres, vous pouvez désormais utiliser le widget de fonction Modifier. C&#39;est une solution puissante pour créer des outils personnalisés où vous souhaitez piloter des paramètres à l&#39;aide d&#39;un [graphique de fonction de Substance](../../function-graphs/the-function-graph/the-function-graph.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Modifier la fonction](../../assets/functionedit.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fonction de modification 2](../../assets/functionedit2.png){zoomable="yes"}

</td>
</tr>
</table>

## Améliorations de l’API

L’API de script comprend quatre nouvelles méthodes :

* Méthodes pour obtenir et définir le type de graphique d’un graphique de composition de Substances : myGraph.setGraphType(« newType ») ; myGraph.getGraphType()
* Méthode d’ouverture d’une ressource de package dans son éditeur (par exemple, un graphique de Substance dans la vue Graphique) : myUIManager.openResourceInEditor(myResource)
* Méthode de sélection d’une ressource de package dans l’Explorateur (graphique de Substance, par exemple) : myUIManager.setExplorerSelection(myResource)
* Méthode pour cadrer un nœud spécifique dans la vue graphique : myUIManager.focusGraphNode(myGraphViewID, myNode)

## Configuration requise pour les plates-formes d’effets spéciaux

Chaque année, la [plateforme de référence pour les effets visuels](https://vfxplatform.com/) publie une liste d&#39;outils et de bibliothèques à utiliser dans chaque logiciel du secteur des effets visuels afin de réduire les incompatibilités entre les logiciels. Comme d&#39;habitude, nous *mettons à jour toutes nos dépendances* afin de respecter toutes ces recommandations.

Notez que ces mises à jour ont deux conséquences majeures :

* <b>La configuration requise pour Linux</b> a changé et Designer nécessite désormais RHEL version 8 ou 9 (CentOS n’est plus pris en charge). Tous les détails se trouvent sur la page [Configuration requise](../../getting-started/system-requirements/system-requirements.md).
* <b>Les plug-ins pour Designer doivent être mis à jour </b>car certaines fonctions ont été déconseillées dans Qt6. Vous trouverez toutes les informations requises pour mettre à jour vos plug-ins sur le [forum de la communauté](https://community.adobe.com/t5/substance-3d-designer-discussions/plugins-required-updates-in-designer-14-0/td-p/14768559).

## Notes de mise à jour

### 14.0.0

*(Publié le 30 juillet 2024)*

### Ajouté

* [Contenu] Nouveau filtre Kuwahara anisotrope
* [Contenu] Nouveau nœud de Bevel smooth
* [Contenu] Nouveau nœud v2 Courbure lisse
* [Contenu] Nouveau nœud de Directional distance
* [Contenu] Nouveaux outils d’histogramme : calcul, égalisation, rendu
* [Contenu] Nouvel ID vers le nœud de masque
* [Content] Nouveau nœud de décombinaison normal
* [Contenu] Nouveaux nœuds de palette : Créer, Appliquer, Modifier, Afficher
* [Contenu] Nouveau nœud Quantize Color
* [Contenu] Déformation directionnelle non uniforme : définissez la valeur par défaut de la courbe d’intensité sur 1
* [Contenu] Ajoutez le suffixe « Color » ou « Grayscale » à tous les libellés de nœuds qui ont ces versions
* [Contenu] La désactivation de l’option « Bruit blanc » ne permet de conserver que « Bruit blanc rapide »
* [Content] Nœud « Negate Float1 » obsolète dans le graphique de fonction de Substance
* [Contenu] Renommez « Quantize Color » en « Quantize Color (Simple) ».
* [Vue 2D] Valeurs d’affichage dans le panneau Informations pour les pixels en dehors de la plage 0-1
* [Moteur]&#x200B;[Texte] Nouveau crénage pour certaines polices
* [Graphique] Amélioration du temps d’invalidation lors de l’édition de sous-graphes profonds lors de l’utilisation de l’édition contextuelle
* [Linker] Ne pas dupliquer les bitmaps dans SBSASM
* [Paramètres] Ajout d’un nouveau widget « fonction » pour tous les types de paramètres d’entrée
* [Propriétés] Amélioration de l’affichage des paramètres hérités
* [UX] Amélioration de la prise en charge du pavé tactile (Mac uniquement)
* [UX] Moderniser le panoramique lorsque vous atteignez la bordure du graphique lors de la sélection
* [UX] Supprimer la fonctionnalité « Désactiver la haute résolution »
* [Branding] Nouveau branding pour l&#39;écran de démarrage et la fenêtre À propos
* [Courbe de transfert de dégradé] Ajout d’un moyen de déplacer toutes les touches et de créer une boucle
* [Bibliothèque] Basculer tous les filtres par défaut en casse de phrase
* [API] Méthode Add pour cadrer un nœud spécifique dans la fenêtre Vue graphique
* [API] Ajout d’une méthode pour ouvrir un package dans son éditeur (par exemple, un graphique de Substance dans la vue Graphique)
* [API] Ajout d’une méthode pour sélectionner une ressource de package dans l’Explorateur (par exemple, un graphique de Substance)
* [API] Ajout de méthodes pour obtenir et définir le type de graphique d’un graphique de composition de Substances
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2023
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2024
* [Tiers] Mettre à jour Boost à 1.82.0 + USD à 23.08
* [Tiers] Mise à jour NGL vers 1.38
* [ThirdParty] Mettre à jour OpenColorIO vers la version 2.3.x
* [Tiers] Mise à jour d’OpenExr vers la version 3.2.x
* [ThirdParty] Mettre à jour OpenSubdiv vers la version 3.6.x
* [ThirdParty] Mettre à jour Python vers 3.11.x
* [Tiers] Mise à jour de Qt vers la version 6.5.x
* [ThirdParty] Mettre à jour gcc vers la version 11.2.1
* [ThirdParty] Mettre à jour glibc vers 2.28
* [Tiers] Mettez à jour libstdc++ ABI vers C++11 one
* [Documentation] Nouvelle page Glossaire

### Correctifs

* [Boulangers] Blocage lors de la modification du nom de fichier d’une scène
* [Boulangers] Blocage lors de l’enregistrement du paramètre prédéfini boulangers dans le fichier JSON
* [Content] &#39;Dispersion sur la spline&#39; : Exposer le paramètre alpha de l&#39;image d&#39;entrée
* [Contenu] « Couleur Sampler de la vignette » : expression visible manquante
* [Contenu] Bruit anisotrope : une valeur négative pour la quantité X/Y produit un résultat erroné
* [Contenu] Bruit anisotrope : problème de mosaïque lors de l’utilisation de valeurs impaires comme quantité X et sans smoothness
* [Contenu] Fonction de distribution normale : max() mal placé peut conduire à NaN
* [Content] Les ombres RTAO, Bent Normal et RT ne fonctionnent pas correctement sur certaines plateformes
* [Contenu] Couleur de fusion des éclaboussures de forme : les cartes normales OpenGL ne sont pas fusionnées correctement
* [Contenu] Espace non garanti après le préfixe « Multi » dans les étiquettes de nœuds
* [Dépendances] Blocage lors du déplacement d’un graphique au sein d’un ou entre plusieurs packages
* [Moteur] Erreur de précision dans les nœuds de déformation affectant les nœuds de flou de Pente
* [Moteur] Le calque SBSAR dans SD ne peut pas lire SBSAR avec le contenu SBSASM > 2 Go
* [Graphique de fonction] Résultat incorrect pour 0^n
* [Graphique] L’option « Afficher la taille du nœud » est mal étiquetée
* [Graphique] Blocage lors de la copie d’un commentaire parent vers un autre graphique
* [Graphique] Blocage lorsque vous faites glisser un nœud Point tout en maintenant la touche Alt enfoncée
* [Graph] La recherche de nœud peut manquer des correspondances évidentes dans certains cas
* [Graphique] Problème de performances lors de l’édition d’un graphique de fonction instancié plusieurs fois avec un supergraphe ouvert
* [Graphique] Trop d’invalidations lors de la création d’une sortie
* [Security] Vulnérabilité d&#39;écriture hors limites d&#39;analyse ICO
* [Sécurité] Certains formats d’image inutilisés sont obsolètes
* [Paramètres] Le chemin de la ressource Bitmap PKG ne doit pas être modifiable
* [Paramètres] Correction des problèmes liés à l’exposition/l’exposition par lots du paramètre d’un processeur de valeurs
* [Paramètres] Les paramètres de chaîne sont ignorés lors de l’exposition par lots
* [Propriétés] Problème de performances lors de la modification d’un graphique de fonction instancié plusieurs fois avec les propriétés ouvertes
* [SVG] Les modifications apportées aux formes ne sont pas appliquées à l’image pixellisée
* [UI] Correction de certains bugs/incohérences avec les widgets défilants (Windows uniquement)
* [UI] Ordre incohérent des formats de fichiers de scène 3D dans les listes d’importation/exportation
* [UI] Les actions de la fenêtre sont dupliquées dans l’interface utilisateur
* [Version Control] Le script &#39;perforce.py&#39; ne fonctionne pas sur Python 3
