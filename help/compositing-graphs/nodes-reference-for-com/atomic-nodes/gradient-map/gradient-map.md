---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-map.html"
breadcrumb-title: ''
description: Utilisez le nœud de Map de dégradé pour mapper les valeurs de niveaux de gris aux couleurs à l’aide des dégradés de dégradé pour la colorisation et les effets.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Map de dégradé
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# Map de dégradé

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Noeud atomique : Courbe de transfert de dégradé](gradient-map.resources/comp_gradient_1.png "Noeud atomique : Courbe de transfert de dégradé"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Remappe les valeurs de niveaux de gris d’une image à l’aide d’un dégradé personnalisé.

Ce nœud a un double objectif : il peut être simplement utilisé comme <b> </b>nœud de conversion des niveaux de gris en couleurs ou, pour coloriser les niveaux de gris, je les mappe à une gamme de couleurs personnalisée.

</td>
</tr>
</table>

Le nœud offre un éditeur de dégradé avancé et riche en fonctionnalités pour mapper plusieurs couleurs avec précision : accédez à la section [Éditeur de dégradé](#gradient-editor) de cette page pour en savoir plus.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## Exemples

## Paramètres

|  |  |
| --- | --- |
| <b>Mode colorimétrique</b> *Booléen* | Définit le mode de sortie sur Couleur ou Niveaux de gris. |
| <b>Adressage de dégradé</b> *Booléen* | Définit le dégradé sur des valeurs de répétition (carreau) ou de pincement qui sont en dehors de la plage [0, 1]. |
| <b>Dégradé</b> *Tableau de clés de dégradé* | Dégradé personnalisé utilisé pour mapper les valeurs de niveaux de gris d’entrée.   Peut être modifié sur place ou à l&#39;aide de l&#39;[éditeur de dégradé](#gradient-editor). |

## Éditeur de dégradé

Cette fenêtre offre des commandes permettant de modifier le dégradé de référence utilisé par le nœud de Map de dégradé pour mapper les valeurs de niveaux de gris aux couleurs.

Il peut être ouvert à partir des <b>propriétés</b> du nœud de Map de dégradé de données de l&#39;une des manières suivantes :

* Cliquez sur LMB sur le bouton <b>Éditeur de dégradé</b> ;
* Double-cliquez sur LMB sur une épingle dans la barre de dégradé. L’épingle cliquée sera alors automatiquement sélectionnée dans l’Éditeur de dégradé afin que vous puissiez modifier directement ses valeurs.

![Éditeur de dégradé](gradient-map.resources/image2017-2-17-16-13-5.png "Éditeur de dégradé")

### Modification des épingles de dégradé

Les couleurs et leur position le long du dégradé sont contrôlées par des épingles placées le long de la bande de dégradé.

Chaque épingle définit une couleur à sa position le long du dégradé.

Les parties du dégradé avant et après la première et la dernière épingle sont définies respectivement sur les couleurs de ces épingles.

![Éditeur de dégradé - Vue de dégradé](gradient-map.resources/image2017-2-17-17-27-46.png "Éditeur de dégradé - Vue de dégradé")

Les commandes suivantes permettent de modifier les épingles :

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Ajouter une épingle</b>

Cliquez sur LMB sur le dégradé ou juste en dessous pour ajouter une épingle à l’emplacement où vous avez cliqué dans la barre de dégradé.

La nouvelle épingle sera définie sur la couleur du dégradé à cette position.

</td>
<td style="border: 0;" valign="top">

![Éditeur de dégradé - Ajouter une épingle](gradient-map.resources/move-pin.gif "Éditeur de dégradé - Ajouter une épingle")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Déplacer l&#39;épingle</b>

Maintenez la touche LMB enfoncée et faites glisser les épingles sélectionnées le long de la barre de dégradé pour les déplacer.

Vous pouvez également définir la position d&#39;une épingle avec une valeur numérique en la sélectionnant et en utilisant le paramètre <b>Position</b>. La position est une valeur comprise dans la plage [0;1], où 0 correspond au début du dégradé et 1 à sa fin.

![Éditeur de dégradé - paramètre de position d&#39;Épingle](gradient-map.resources/image2015-8-27-13-56-2.png "Éditeur de dégradé - paramètre de position d&#39;Épingle")

</td>
<td style="border: 0;" valign="top">

![Éditeur de dégradé - Déplacer l&#39;épingle](gradient-map.resources/movepin2.gif "Éditeur de dégradé - Déplacer l&#39;épingle")

</td>
</tr>
</table>

Lorsque plusieurs épingles sont sélectionnées, elles peuvent toutes être déplacées *simultanément*. Lorsqu’une ou plusieurs épingles atteignent et terminent le dégradé à mesure qu’elles sont déplacées, deux comportements sont disponibles en fonction du bouton de la souris utilisé pour le déplacement :

* <b>LMB:</b> les Épingles restent à l&#39;extrémité, ce qui signifie qu&#39;elles seront empilées à cet emplacement à mesure qu&#39;elles l&#39;atteignent et que leurs positions relatives sont modifiées ;
* <b>Mo :</b> les Épingles sont bouclées à l&#39;autre extrémité du dégradé, ce qui signifie que leur position relative reste inchangée.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Supprimer l&#39;épingle</b>

Sélectionnez les épingles et appuyez sur Supprimer, ou faites glisser les épingles hors de la bande de dégradé pour les supprimer.

</td>
<td style="border: 0;" valign="top">

![Éditeur de dégradé - Supprimer l&#39;épingle](gradient-map.resources/removepin.gif "Éditeur de dégradé - Supprimer l&#39;épingle")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Inverser les positions</b>

Permet de refléter la position des épingles sélectionnées sur le dégradé.

</td>
<td style="border: 0;" valign="top">

![Éditeur de dégradé : inverser les positions](gradient-map.resources/invert.gif "Éditeur de dégradé : inverser les positions")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Tout effacer</b>

Supprime toutes les épingles de la bande de dégradé.

</td>
<td style="border: 0;" valign="top">

![Éditeur de dégradé - Tout effacer](gradient-map.resources/remove.gif "Éditeur de dégradé - Tout effacer")

</td>
</tr>
</table>

<b>Inverser les couleurs</b>

Ce bouton applique les couleurs négatives aux épingles sélectionnées.

<b>Désaturer</b>

Ce bouton désature les couleurs définies sur les épingles sélectionnées.

### Modes d’interpolation

Une fois les épingles configurées, vous pouvez contrôler la transition des couleurs d’une épingle à l’autre à l’aide des modes d’interpolation disponibles :

+++Linéaire
Mode d’interpolation par défaut : applique une interpolation linéaire simple entre chaque épingle pour que le dégradé progresse uniformément.

+++

+++Tangentes plates
Lorsque vous considérez la transition entre les dégradés comme des courbes de Bézier où les épingles sont des points de la courbe, ce mode définit ces points pour qu’ils aient des tangentes horizontales.

Il en résulte une transition évocatrice d’une interpolation à pas fluide.

Lorsque ce mode est sélectionné, le paramètre <b>Milieu</b> est activé et vous permet de décaler la position horizontale du milieu vertical de la courbe entre les points. Cela fait basculer l&#39;échelle entre les tangentes « out » et « in ».

+++

+++Lisse
Lisse la courbe d’interpolation entre chaque point.

Lorsque ce mode est sélectionné, le paramètre <b>Smoothness</b> est activé et vous permet d&#39;ajuster l&#39;intensité du lissage lorsqu&#39;une valeur de 0 est égale au mode d&#39;interpolation <b>linéaire</b>.

+++

+++Aucune interpolation
La couleur change uniquement à l’emplacement d’une épingle et reste constante jusqu’à l’épingle suivante le long de la bande de dégradé.

Il en résulte des étapes difficiles entre les couleurs, et seules les couleurs définies par les épingles sont présentes sur le dégradé.

+++

### sélecteur de couleurs

![Éditeur de dégradé - Sélecteur de couleurs](gradient-map.resources/image2017-2-17-18-21-29.png "Éditeur de dégradé - Sélecteur de couleurs")

Le sélecteur de couleurs permet de définir une couleur de plusieurs manières :

* <b>Barre de dégradé et de teinte</b>

  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Ajustez la position de l’objet dans le dégradé et de l’encoche dans la barre de teinte pour définir une couleur.

  </td>
  <td style="border: 0;" valign="top">

  ![Sélecteur de couleurs - Zone de dégradé et barre de teinte](gradient-map.resources/colorpalette.gif "Sélecteur de couleurs - Zone de dégradé et barre de teinte")

  </td>
  </tr>
  </table>

* <b>Curseurs RGB, HSV et Alpha</b>

  <table>
  <tr style="border: 0;">
  <td width="100.00%" style="border: 0;" valign="top">

  Les curseurs RGB, TSL et Alpha vous permettent de définir une couleur avec précision, en ajustant les curseurs ou en définissant directement leurs valeurs numériques.

  Vous pouvez également utiliser un code hexadécimal dans le champ de saisie dédié situé sous les curseurs.

  </td>
  <td width="33.33%" style="border: 0;" valign="top">

  ![Sélecteur de couleurs - Curseurs RGB, TSL et Alpha](gradient-map.resources/image2017-2-17-18-31-41.png "Sélecteur de couleurs - Curseurs RGB, TSL et Alpha")

  </td>
  </tr>
  </table>

* <b>Choisir à l&#39;écran</b>

  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Utilisez le bouton <b>Choisir</b> et cliquez sur LMB n&#39;importe où dans l&#39;écran pour échantillonner la couleur à cet emplacement.

  </td>
  <td style="border: 0;" valign="top">

  ![Sélecteur de couleurs - Sélection à l&#39;écran](gradient-map.resources/pick.gif "Sélecteur de couleurs - Sélection à l&#39;écran")

  </td>
  </tr>
  </table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

La couleur sélectionnée est prévisualisée dans la moitié supérieure de la vignette couleur.\
La moitié inférieure affiche la couleur précédemment utilisée. Double-cliquez sur le LMB pour rétablir la couleur modifiée.

</td>
<td width="16.67%" style="border: 0;" valign="top">

![Sélecteur de couleurs - Rétablir la couleur](gradient-map.resources/image2015-8-27-14-40-39.png "Sélecteur de couleurs - Rétablir la couleur")

</td>
</tr>
</table>

Lorsque plusieurs épingles sont sélectionnées, les curseurs RGB, TSL et Alpha se transforment en curseurs delta (Δ), ce qui signifie qu’ils sont utilisés pour décaler la valeur de chaque épingle d’une même valeur.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

En outre, les fonctionnalités suivantes sont disponibles sous la vignette de couleur en tant que boutons :

<b>Inverser :</b> remplace la couleur par son négatif ;

<b>Vers le gris :</b> désature la couleur ;

<b>Copier </b>*:* copier la couleur actuellement sélectionnée dans le Presse-papiers ;

<b>Coller :</b> passez à la couleur actuellement dans le Presse-papiers ;

<b>sRVB</b> : utilisez l&#39;espace colorimétrique sRVB pour afficher les couleurs. Lorsque cette option est désactivée, l’espace colorimétrique linéaire est utilisé ;

<b>Flottant :</b> affichez les valeurs du RGB d&#39;affichage, de la vue HSV et du curseur Alpha en virgule flottante.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Sélecteur De Couleurs - Boutons](gradient-map.resources/invert2.gif "Sélecteur De Couleurs - Boutons")

</td>
</tr>
</table>

### Pipette de dégradé

L’outil Pipette de dégradé est l’une des fonctionnalités les plus utiles de ce nœud, car vous pouvez créer des dégradés complexes en traçant simplement une ligne sur une image de référence.

![Éditeur de dégradé - Sélecteur de dégradé](gradient-map.resources/pickgradient.gif "Éditeur de dégradé - Sélecteur de dégradé")

Le curseur <b>Précision</b> vous aidera à ajuster le dégradé que vous venez de créer en augmentant ou en diminuant le nombre de touches : plus leurs valeurs sont faibles, plus votre dégradé correspondra précisément aux valeurs que vous avez choisies.

## Connecteurs d’entrée

|  |  |
| --- | --- |
| <b>Entrée</b> *Niveaux de gris* PRINCIPAUX | Image en niveaux de gris à traiter. |

## Connecteurs de sortie

|  |  |
| --- | --- |
| <b>Sortie</b> *Niveaux de gris* |  |

## Exemples

*Bientôt disponible.*
