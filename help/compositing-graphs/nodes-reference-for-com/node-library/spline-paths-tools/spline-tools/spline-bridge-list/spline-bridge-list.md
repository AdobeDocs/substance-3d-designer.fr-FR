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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Spline Bridge (Liste)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de nœud](spline-bridge-list.resources/spline-bridge-list-01.png "Icône de nœud")

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

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines d’entrée sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines d&#39;entrée codés dans les canaux RVBA d&#39;une image couleur :<br><b>R</b> - position X<br><b>G</b> - position Y<br><b>B</b> - Height<br><b>A</b> - données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines d&#39;entrée codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines d&#39;entrée. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> <i>Niveaux de gris</i> | Aperçu des splines de sortie sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> <i>Couleur</i> | Coordonnées des points des splines de sortie codés dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Position X<br><b>G</b> - Position Y<br><b>B</b> - Height<br><b>A</b> - Données compressées :<br>- Signe : la spline est fermée (négative) ou ouverte (positive);<br>- Valeur absolue : Thickness + 1. |
| <b>Données splines</b> <i>Couleur</i> | Données supplémentaires des splines de sortie codées dans les canaux RVBA d&#39;une image couleur.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Inutilisé<br><b>A</b> - Inutilisé |
| <b>Quantité de spline</b> <i>Nombre entier</i> | Nombre de splines de sortie. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Quantité de spline du pont</b> <i>Nombre entier</i> | Nombre de splines générées sur les splines d&#39;entrée. |
| <b>Type de splines Bridge</b> <i>Nombre entier</i> | Type de spline générée :<br><br>- Linéaire : spline nette reliant les splines intermédiaires avec des trajectoires droites du début à la fin ;<br>- Bézier quadratique : spline courbe reliant les splines intermédiaires avec des trajectoires lisses du début à la fin.<br><br>Remarque : au moins 3 splines d&#39;entrée sont requises pour calculer une spline de Bézier quadratique. |
| <b>Les splines d&#39;entrée sont fermées</b> <i>Booléen</i> | Détermine si le premier et le dernier point des splines d&#39;entrée doivent être traités comme un point unique. Cela permet d&#39;éviter la duplication des première et dernière splines traversantes. |
| <b>Inverser la direction</b> <i>Booléen</i> | Inverse la direction de la spline. |
| <b>Fermer la spline du pont</b> <i>Booléen</i> | Étend les splines traversantes pour les relier à la première spline de la liste d&#39;entrée. |
| <b>Décalage de la spline du premier pont</b> <i>Float2</i> | Applique un décalage au début de toutes les splines traversées. La valeur est la longueur normalisée des splines d&#39;entrée.<br>Les splines générées qui correspondent au début ou à la fin des splines traversées y sont laissées. |
| <b>Décalage spline du dernier pont</b> <i>Float2</i> | Applique un décalage à l&#39;extrémité de toutes les splines traversées. La valeur est la longueur normalisée des splines d&#39;entrée.<br>Les splines générées qui correspondent au début ou à la fin des splines traversées y sont laissées. |
| <b>Plage de décalage aléatoire</b> <i>Nombre entier</i> | Distance maximale utilisée pour le décalage aléatoire appliqué sur les splines.<br><br>- <i>spline parent :</i> Toute la longueur des splines parentes est utilisée. Peut entraîner des chevauchements.<br>- <i>Intervalle :</i> L&#39;intervalle entre les splines du pont est utilisé. Cela atténue les chevauchements. Cette distance diminue lorsque la quantité de splines du pont augmente. |
| <b>Décalage aléatoire de début</b> <i>Flotter</i> | Multiplicateur du décalage aléatoire appliqué à la position de départ des splines de pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>. |
| <b>Décalage aléatoire de fin</b> <i>Flotter</i> | Multiplicateur du décalage aléatoire appliqué à la position d&#39;extrémité des splines de pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>. |
| <b>Décalage aléatoire global</b> <i>Flotter</i> | Multiplicateur pour le *montant égal* de décalage aléatoire appliqué sur *les deux* positions de début et de fin des splines de pont, où la distance maximale est spécifiée par le paramètre <b>Plage de décalage aléatoire</b>. |
| <b>Distribution uniforme</b> <i>Booléen</i> | Lorsque la valeur est True, les points des splines générées sont espacés de manière régulière du début à la fin. |
| <b>Thickness</b> |  |
| <b>Mode Thickness</b> <i>Nombre entier</i> | Méthode d&#39;acquisition de la valeur de thickness pour les splines de pont.<br><br>- <i>Hériter des splines parentes :</i> Le thickness des splines parentes aux positions de début et de fin des splines de pont est utilisé<br>- <i>Remplacement :</i> La valeur arbitraire que vous spécifiez dans le paramètre <b>Thickness</b> est utilisée |
| <b>Thickness</b> <i>Flotter</i> | Valeur de thickness absolue appliquée aux splines du pont. |
| <b>Thickness aléatoire</b> <i>Flotter</i> | Un multiplicateur aléatoire pour le thickness des splines de pont, où le thickness initial auquel ce multiplicateur est appliqué est spécifié par le paramètre <b>mode de Thickness</b>. |
| <b>Height</b> |  |
| <b>Mode Height</b> <i>Nombre entier</i> | Méthode d&#39;acquisition de la valeur d&#39;height pour les splines de pont.<br><br>- <i>Hériter des splines parentes :</i> L&#39;height des splines parentes aux positions de début et de fin des splines de pont est utilisé<br>- <i>Remplacement :</i> La valeur arbitraire que vous spécifiez dans le paramètre <b>Height</b> est utilisée |
| <b>Décalage Height</b> <i>Flotter</i> | Spécifie le décalage appliqué à l&#39;height hérité des splines parentes, avant l&#39;application de cet height aux splines du pont. |
| <b>Height</b> <i>Flotter</i> | Valeur d&#39;height absolue appliquée aux splines du pont. |
| <b>Height aléatoire</b> <i>Flotter</i> | Une quantité aléatoire d&#39;ajustement de l&#39;height des splines du pont, où cet ajustement dépend du paramètre <b>mode d&#39;Height</b> sélectionné :<br><br>- <i>Hériter des splines parentes :</i> La valeur est un multiplicateur pour l&#39;height hérité.<br>- <i>Remplacement :</i> La valeur est un décalage ajouté à l&#39;height. |
| <b>Correction Non Carrée</b> <i>Booléen</i> | Ajustez la position et le thickness des points pour conserver la forme de la spline dans des résolutions autres que carrées. Cela a également un impact sur la distribution uniforme. |
| <b>Aperçu</b> |  |
| <b>Afficher l&#39;assistant de direction</b> <i>Booléen</i> | Affiche un point au début de la spline et une flèche à sa fin dans la sortie Aperçu. |
| <b>Afficher l&#39;enveloppe de Thickness</b> <i>Booléen</i> | Affiche des lignes supplémentaires sur les bords du thickness de la spline. |
| <b>Quantité de segments</b> <i>Nombre entier</i> | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie Aperçu. Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Thickness (px)</b> <i>Flotter</i> | Règle le thickness de visualisation de la spline en pixels dans la sortie Aperçu. |
| <b>Intensité de l&#39;aperçu de l&#39;arrière-plan</b> <i>Flotter</i> | Intensité de la visualisation de l’aperçu. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Avant</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Après</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemple de nœud 2](spline-bridge-list.resources/spline-bridge-list-04.gif "Exemple de nœud 2")

</td>
</tr>
</table>

![Nœud dans le graphique](spline-bridge-list.resources/spline-bridge-list-05.jpg "Nœud dans le graphique")
