---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Utilisez le nœud de liste de ponts de spline pour relier des textures entre plusieurs splines dans une liste pour des motifs complexes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge (Liste)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# Spline Bridge (Liste)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](../../../../../../assets/spline-bridge-list-icon.png "Icône de nœud")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Génère des splines traversant toutes les splines de la liste d&#39;entrée, le long de ces splines.

Les splines générées peuvent être linéaires (droites) ou quadratiques (courbes).

</td>
</tr>
</table>

>[!TIP]
>
> Les splines générées vont de la première spline de la liste à la dernière et traversent les splines intermédiaires en suivant rigoureusement l&#39;ordre de ces splines dans la liste.
> 
> Par conséquent, vous devez être attentif à l&#39;ordre dans lequel vous ajoutez des splines ensemble au préalable.

## Connecteurs d’entrée

<b>Aperçu</b> *Niveaux de gris* Aperçu des splines d&#39;entrée sous la forme d&#39;une image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points des splines d&#39;entrée codées dans les couches RVBA d&#39;une image couleur :\
<b> R</b> - Position X\
<b> G</b> - Position Y\
<b> B</b> - Height\
    <b>A</b> - Données compressées :\
        * Signe : la spline est fermée (négative) ou ouverte (positive);\
        * Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Inutilisé\
<b> A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines d&#39;entrée.

## Connecteurs de sortie

<b>Aperçu</b> *Niveaux de gris* L’aperçu des splines de sortie sous forme d’image en niveaux de gris.

<b>Couleurs splines</b> *Couleur* Les coordonnées des points splines de sortie sont codées dans les couches RVBA d&#39;une image couleur.\
    <b>R</b> - Position X\
    <b>G</b> - Position Y\
    <b>B</b> - Height\
    <b>A</b> - Données compressées :\
        * Signe : la spline est fermée (négative) ou ouverte (positive);\
        * Valeur absolue : Thickness + 1.

<b>Données splines</b> *Couleur* Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.\
    <b>R</b> - Tangentes X\
    <b>G</b> - Tangentes Y\
    <b>B</b> - Inutilisé\
    <b>A</b> - Inutilisé

<b>Quantité de spline</b> *Nombre entier* Nombre de splines de sortie.

## Paramètres

<b>Quantité de spline du pont</b> *Nombre entier* Nombre de splines générées entre les splines d&#39;entrée.

<b>Type de splines Bridge</b> *Nombre entier* Type de spline généré :
* Linéaire : une spline nette reliant les splines intermédiaires avec des trajectoires droites du début à la fin ;
* Bézier quadratique : spline courbe reliant les splines intermédiaires avec des trajectoires lisses du début à la fin.\
  Remarque : Au moins 3 splines d&#39;entrée sont requises pour calculer une spline de Bézier quadratique.

<b>Les splines d&#39;entrée sont fermées</b> *Booléen* Contrôle si le premier et le dernier point des splines d&#39;entrée doivent être traités comme un point unique. Cela permet d&#39;éviter la duplication des première et dernière splines traversantes.

<b>Inverser la direction</b> *Booléen* Inverse la direction de la spline.

<b>Fermer la spline du pont</b> *Booléen*&#x200B;Étend les splines traversantes pour se connecter à la première spline de la liste d&#39;entrée.

<b>Décalage de la spline du premier pont </b>*Flottant2* Applique un décalage au début de toutes les splines traversées. La valeur est la longueur normalisée des splines d&#39;entrée.\
Les splines générées qui correspondent au début ou à la fin des splines traversées y sont laissées.

<b>Décalage spline du dernier pont </b>*Float2*\
Applique un décalage à l&#39;extrémité de toutes les splines traversées. La valeur est la longueur normalisée des splines d&#39;entrée.\
Les splines générées qui correspondent au début ou à la fin des splines traversées y sont laissées.

<b>Plage de décalage aléatoire</b> *Nombre entier* Distance maximale utilisée pour le décalage aléatoire appliqué sur les splines.\
*- Spline parente :* la longueur totale des splines parentes est utilisée. Peut entraîner des chevauchements.\
*- Intervalle :* L&#39;intervalle entre les splines du pont est utilisé. Cela atténue les chevauchements. Cette distance diminue lorsque la quantité de splines du pont augmente.

<b>Décalage aléatoire de départ</b> *Flottant* Un multiplicateur pour le décalage aléatoire appliqué sur la position de départ des splines du pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>.

<b>Décalage aléatoire de fin</b> *Flottant* Un multiplicateur pour le décalage aléatoire appliqué sur la position d&#39;extrémité des splines du pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>.

<b>Décalage aléatoire global</b> *Flotter* Un multiplicateur pour la *quantité égale* de décalage aléatoire appliquée sur *les deux* positions de début et de fin des splines du pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>.

<b>Distribution uniforme</b> *Booléen* Lorsque la valeur est True, les points des splines générées sont espacés de manière régulière du début à la fin.

+++Épaisseur
<b>Mode Thickness</b> *Entier* Méthode d&#39;acquisition de la valeur de thickness pour les splines du pont.\
*- Hériter des splines parentes :* Le thickness des splines parentes aux positions de début et de fin des splines de pont est utilisé\
*- Remplacement :* la valeur arbitraire que vous spécifiez dans le paramètre <b>Thickness</b> est utilisée

<b>Thickness</b> *Flottant* Valeur de thickness absolue appliquée aux splines du pont.

<b>Thickness aléatoire</b> *Float* Un multiplicateur aléatoire pour le thickness des splines du pont, où le thickness initial auquel ce multiplicateur est appliqué est spécifié par le paramètre <b>mode Thickness</b>.

+++

+++Hauteur
<b>Mode d&#39;Height</b> *Entier* Méthode d&#39;acquisition de la valeur d&#39;height pour les splines du pont.\
*- Hériter des splines parentes :* L&#39;height des splines parentes aux positions de début et de fin des splines de pont est utilisé\
*- Remplacement :* La valeur arbitraire que vous spécifiez dans le paramètre <b>Height</b> est utilisée

<b>Décalage de l&#39;Height</b> *Flottant* Le décalage appliqué à l&#39;height hérité des splines parentes, avant l&#39;application de cet height aux splines du pont.

<b>Height</b> *Flottant* Valeur d&#39;height absolue appliquée aux splines du pont.

<b>Height aléatoire</b> *Flotter* Une quantité aléatoire d&#39;ajustement de l&#39;height des splines du pont, où cet ajustement dépend du paramètre <b>mode Height</b> sélectionné :\
*- Hériter des splines parentes :* La valeur est un multiplicateur pour l&#39;height hérité.\
*- Remplacement :* La valeur est un décalage ajouté à l&#39;height.

+++

<b>Correction Non Carrée </b>*Booléenne*

Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées.\
Cela a également un impact sur la distribution uniforme.

+++Prévisualiser
<b>Afficher l&#39;assistant de direction</b> *Booléen* Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu.

<b>Afficher l&#39;enveloppe de Thickness</b> *Booléen*\
Affiche des lignes supplémentaires sur les thickness de la spline.

<b>Quantité de segments</b> *Nombre entier* Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie d&#39;aperçu.\
Plus la valeur est élevée, plus la ligne est lisse.

<b>Thickness (px)</b> *Flottant* Ajuste le thickness de la visualisation de la spline en pixels dans la sortie d&#39;aperçu.

<b>Intensité de l&#39;aperçu de l&#39;arrière-plan</b> *Variation* L’intensité de la visualisation de l’aperçu.

+++

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_Before.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_After.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](../../../../../../assets/SplineBridge-List_Demo.gif "Exemple de nœud 2")

</td>
</tr>
</table>

![Nœud dans le graphique](../../../../../../assets/SplineBridge-List_Graph.jpg "Nœud dans le graphique")
