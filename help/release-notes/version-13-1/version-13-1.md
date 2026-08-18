---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-13-1.html"
breadcrumb-title: ''
description: Consultez les notes de mise à jour de Substance 3D Designer version 13.1 pour en savoir plus sur les améliorations des graphiques de nœuds et la prise en charge de l’exportation AxF.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Version 13.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---


# Version 13.1

<b>Substance 3D Designer 13.1</b> apporte de nombreuses améliorations à la qualité de vie du graphique de nœuds, principalement en ce qui concerne les images, afin d&#39;améliorer l&#39;expérience de création de matière. L’exportation AxF a également été ajoutée, ce qui permet un workflow d’interopérabilité pour les utilisateurs qui travaillent avec le format AxF. 

*Date de publication : 12 décembre 2023*

![Bannière Substance 3D Designer 13.1](../../assets/24-library-hero-1920x620.png "Bannière Substance 3D Designer 13.1")

## Améliorations en matière de cadres

Les cadres sont un outil obligatoire pour que votre graphique reste bien organisé et lisible. C&#39;est pourquoi nous avons décidé de les peaufiner dans cette nouvelle version.

### Développement automatique

Au fur et à mesure que le graphique se développe, le contenu des blocs peut devoir être réorganisé. Les nœuds peuvent se déplacer pour faire de la place pour les ajouts ou le contenu peut devoir être plus espacé pour promouvoir la lisibilité. Pour faciliter ces réglages, il est désormais possible de développer automatiquement un cadre lors du déplacement d&#39;objets inclus : maintenez la touche <b>Maj</b> enfoncée tout en déplaçant un objet pour que les bordures du cadre s&#39;ajustent automatiquement afin de maintenir cet objet dans leurs limites.

![développement automatique](../../assets/autoexpand.gif)

### Ajuster la taille au contenu

Lorsque vous effectuez des réglages dans votre graphique, il se peut qu’un bloc ne soit plus ajusté de manière élégante à son contenu. Cette nouvelle commande vous permet d’ajuster automatiquement la position et la taille du bloc afin qu’il s’ajuste à l’étendue de son contenu, avec un remplissage d’une cellule de grille moyenne. Si le cadre comporte une description, il est ajusté pour utiliser tout espace vide en regard de la description, si possible.

![fitsize](../../assets/fitsize.gif)

### Descriptions améliorées

Grâce au code de HTML, vous pouvez désormais avoir du texte formaté dans la description d’un cadre. Cela s&#39;applique également aux commentaires.

![richtext](../../assets/description-3.png)

### <b>... Et bien plus encore !</b>

Beaucoup de choses ont été repensées, comme les règles d&#39;appartenance pour être plus tolérantes, les zones d&#39;interaction pour redimensionner facilement les images, l&#39;accrochage des règles pour ne pas mal aligner vos nœuds sur la grille, et l&#39;aspect visuel pour apporter un peu de fraîcheur. N&#39;hésitez pas à consulter la [documentation](../../interface/the-graph-view/graph-items/frame/frame.md) des cadres pour en savoir plus.

## Amélioration de la qualité de vie

* <b>Améliorations du menu Nœud :</b>afin de gagner du temps lors de la recherche du nœud dont vous avez besoin, nous avons légèrement amélioré le menu Nœud. La recherche est maintenant plus indulgente et vous donnera un résultat même s&#39;il n&#39;y a pas de correspondance parfaite. En outre, vous pouvez désormais utiliser la flèche vers le haut pour accéder directement au dernier élément de la liste.
* <b>Position des nœuds :</b>si vous souhaitez avoir une disposition parfaite pour votre graphique, ces deux petits changements vous feront plaisir ! Lorsque vous copiez/collez des nœuds d’un graphique vers un autre, les nœuds collés sont désormais alignés sur la grille principale. Et lorsque vous ajoutez un nœud sur un lien long, celui-ci sera désormais placé au milieu de la partie visible du lien, afin de le rendre visible dans toutes les situations.
* <b>Options d&#39;affichage 2D :</b>si vous êtes un utilisateur intensif de la [vue 2D](../../interface/2d-view/2d-view.md), vous gagnerez du temps car des options telles que « Afficher le damier », « Conserver la taille de l&#39;affichage », « Utiliser la taille physique » et « Afficher la mosaïque » sont désormais enregistrées, de sorte que vous n&#39;avez pas à les redéfinir lors de la création d&#39;une nouvelle vue 2D ou même au redémarrage de Designer.

## Exportation AxF

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

Icône de fichier ![AxF](../../assets/axf-file-icon.png "AxF")

</td>
<td width="100.00%" style="border: 0;" valign="top">

AxF est un format de [X-Rite](https://www.xrite.com/axf). Il permet de capturer, de stocker, de modifier et de communiquer les caractéristiques de matériaux complexes à l’aide de données numériques tout au long du processus de conception numérique. Dans les versions précédentes de Designer, vous pouviez [importer des fichiers AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md), puis améliorer la juxtaposition ou ajouter des effets de procédure, mais vous étiez ensuite contraint d’exporter les modifications sous la forme d’un nouveau fichier .sbsar.

Dans cette nouvelle version, nous introduisons la possibilité de modifier les matériaux AxF sur place, puis [exportez vos modifications](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) en tant que nouveau calque dans le fichier AxF importé.

</td>
</tr>
</table>

![Exporter AxF](../../assets/exportaxf.gif)

## API

Enfin, cette version 13.1 continue d’améliorer l’API Python en ajoutant deux possibilités supplémentaires :

* <b>&#39;Propriétés Visible if&#39; : </b>vous pouvez désormais définir cette propriété pour les paramètres de graphiques, les entrées et les sorties.
* <b>Ordre des entrées/sorties des graphiques :</b> utilisez sdsbscompgraph::reorderGraphInput et sdsbscompgraph::reorderGraphOutput pour organiser les paramètres selon vos besoins.

>[!NOTE]
>
> Designer 13.1 est la dernière version majeure basée sur Qt5, les prochaines versions majeures seront mises à niveau vers Qt6. Cela peut avoir un impact sur vos plug-ins personnalisés.

## Notes de mise à jour

### 13.1.0

*(Publié le 12 décembre 2023)*

### Ajouté

* [Images] Développement automatique
* [Cadres] Modification des règles pour définir à quel moment un objet appartient à un cadre
* [Cadres] Désactiver la mise à l’échelle du texte pour la description des cadres
* [Images] Taille adaptée au contenu
* [Images] Nouveaux états par défaut, survol et sélectionné
* [Cadres] Magnétisme de la grande grille
* [Images] Prise en charge du code de HTML pour la description des images
* [Images] Mise à jour des zones d’interaction
* [Images] Mise à jour de l’aspect visuel
* [Graphique] Créer le nœud au milieu du lien visible au lieu du milieu du lien
* [Graphique] Affiche les propriétés d’un élément s’il est le seul élément avec des propriétés disponibles dans une sélection
* [Graphique] Supprimer l’option « Mise à l’échelle » pour les commentaires dans le graphique
* [Graphique] Accrocher les nœuds sur la grille principale lors du copier/coller
* [UX] Autoriser la recherche floue dans le menu Nœud et la recherche dans la bibliothèque
* [UX] Effectuer une boucle N dans la liste du menu Nœud
* [AxF] Prise en charge de l’exportation AxF
* [AxF] Désactiver AxF sous Linux
* [API] Définissez la propriété « Visible if » des paramètres, entrées et sorties du graphique à l’aide de l’API Python
* [API] Définition de l’ordre des E/S de graphiques à l’aide de l’API Python
* [Dépendances] Mettre à jour Boost vers 1.80.0
* [Dépendances] Mettre à jour OpenSubdiv vers la version 3.5.x
* [Dépendances] Mise à jour du SDK FBX vers 2020.3
* [Dépendances] Mettre à jour NGL vers 1.35.0.20
* [Gestion des couleurs] Prise en charge supplémentaire des écrans ICC OCIO
* [Levels] Ajouter un moyen de réinitialiser l&#39;histogramme
* [Python] Avertir les utilisateurs si QtForPython ne peut pas être importé
* [Vue 2D] Enregistrer l&#39;état des options d&#39;affichage
* [Vue 3D] Ajout d’une technique de positionnement au nuanceur d’informations de maillage
* [Exporter] Ajoutez un bouton « Enregistrer les paramètres » pour enregistrer les modifications apportées aux options d’exportation.

### Correctifs

* [Vue 3D] Impossible d&#39;attribuer une texture à une entrée de type texture\_2d d&#39;un matériau MDL
* [AxF] Les identificateurs de graphique dans la liste des modèles peuvent être vides
* [AxF] Le champ de modèle de graphique de Substance est vide par défaut
* atlas scatter [Contenu] : comportement incorrect dans des cas spécifiques
* [Contenu] Mappeur de Flood Fill : sortie vide lorsque toutes les formes ont la même taille de boîte de dialogue
* [Content] FloodFill à la position : artefacts d’imprécision dans certaines situations
* [Contenu] Sortie « Specular » incorrecte dans le nœud « Convertisseur couleur de base/métallique/rugosité »
* [Contenu] L’option Masquer sur tracé ne fonctionne pas à la verticale
* [Contenu] Description manquante pour les nœuds Valeur d’entrée, Niveaux de gris en entrée, Couleur d’entrée et Sortie
* [Contenu] Description manquante pour les nœuds Set et Sequence
* [Contenu] Éclaboussure de forme : artefacts d’imprécision dans la sortie « Splatter data 2 »
* [Moteur] Les valeurs booléennes dans les processeurs de traitement des valeurs sont toujours évaluées sur « False » (Apple Silicon uniquement)
* [Explorer] L’ordre des boutons de la barre d’outils est incohérent entre les systèmes d’exploitation
* [Images] N’accrochez pas les nœuds lorsque vous déplacez une image avec le modificateur CTRL
* [Courbe de transfert de dégradé] réinitialiser tout doit également réinitialiser le widget de dégradé
* [GraphRender] Certains nœuds deviennent noirs lors de l’ajustement en mode aperçu
* [Graphique] L’aperçu de « Valeur d’entrée » est bloqué sur « Faux » lors de l’ajustement de la valeur booléenne par défaut (Apple Silicon uniquement)
* [Graphique] Les nœuds de point proches du bord de l’image ne sont pas déplacés par l’image
* [Interopérabilité] L’icône Renvoyer n’est pas mise à jour après l’envoi à Substance 3D Stager
* [MDL] Impossible de modifier la rugosité dans les nœuds où ce paramètre est disponible
* [MDL] Connexions non valides dans le modèle « AxF to Metallic Roughness »
* [UI] La fenêtre « Exporter les sorties » peut être réduite (Windows uniquement)
* [UI] Les images apparaissent pixellisées dans l’écran À propos lors de l’utilisation de la mise à l’échelle de l’affichage
* [UI] Les outils d’alignement de nœud de la barre d’outils graphique créent plusieurs étapes d’annulation.

### PROBLÈMES CONNUS

* [AxF OpenGL Shader] Largeur incorrecte pour la distribution anisotrope
* [AxF OpenGL Shader] Rugosité par défaut incorrecte
* [AxF OpenGL Shader] Rotation de base d’ombrage incorrecte
* [AxF OpenGL Shader] Détection incorrecte du rayon sous l&#39;hémisphère
* [AxF OpenGL Shader] Détection de contribution incorrecte
* [AxF] Les valeurs de mappage « Couleur Specular » sont incorrectes lors de l’exportation.
* [AxF] L’aperçu et les textures ne s’affichent pas correctement dans la boîte de dialogue « Importer AxF »
* [AxF] La propriété « cc no refraction » n&#39;est pas injectée correctement dans le modèle AxF vers AxF
