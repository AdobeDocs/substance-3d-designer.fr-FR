---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-splines-on-splines.html"
breadcrumb-title: ''
description: Utilisez le nœud Splines de Dispersion sur splines pour répartir les splines enfants le long des tracés de splines parents.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter Splines on Splines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersion de splines sur des splines
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '2832'
ht-degree: 0%

---


# Dispersion de splines sur des splines

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Splines de Dispersion sur splines : icône](../../../../../../assets/scatter-splines-on-splines-icon.png "Splines de Dispersion sur splines : icône")

<b>Entrée :</b> Outils Spline Et Tracé > Outils spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Place des splines le long des splines d&#39;entrée du gabarit.

Le nœud offre des options de personnalisation avancées pour contrôler la façon dont les splines sont dispersées et vous permet de mettre en dispersion des splines droites simples ou vos propres splines personnalisées.

Le nœud vous permet de créer des structures complexes pour mapper des couleurs et des images à l&#39;aide des nœuds du [mappeur de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md), ou utilisé comme squelette pour placer des formes à l&#39;aide des nœuds de la [Dispersion sur la spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Tutoriel

Cliquez sur l&#39;image à droite pour accéder à notre <b>tutoriel dédié</b>, afin de bénéficier d&#39;une visite guidée des capacités du nœud et de son utilisation dans le contexte d&#39;un workflow basé sur une spline.

</td>
<td style="border: 0;" valign="top">

[![Nœuds Spline vidéo](../../../../../../assets/video_spline.png)](https://youtu.be/aUUWV1dYQdI)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entrées

|  |  |
|:---|:---|
| <b>Aperçu</b> *Niveaux de gris* | Aperçu des splines d’entrée sous forme d’image en niveaux de gris. |
| <b>Couleurs splines</b> *Couleur* | Coordonnées des points des splines parentes codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Position X <b>G</b> - Position Y <b>B</b> - Height <b>A</b> - Données compressées : - Signe : la spline est fermée (négative) ou ouverte (positive) - Valeur absolue : Thickness + 1 |
| <b>Données splines</b> *Couleur* | Données supplémentaires des splines parentes codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Inutilisées |
| <b>Quantité de spline</b> *Nombre entier* | Nombre de splines parentes. |
| <b>Cordes splines personnalisées</b> *Couleur* | Coordonnées des points des splines personnalisées codés dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Position X <b>G</b> - Position Y <b>B</b> - Height <b>A</b> - Données compressées : - Signe : la spline est fermée (négative) ou ouverte (positive) - Valeur absolue : Thickness + 1 |
| <b>Données Spline Personnalisées</b> *Couleur* | Données supplémentaires des splines personnalisées codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Inutilisées |
| <b>Quantité de spline personnalisée</b> *Nombre entier* | Nombre de splines personnalisées. |
| <b>Mappage d&#39;échelle</b> *Niveaux de gris* | La texture en niveaux de gris contrôle l&#39;échelle des splines dispersées.  L&#39;effet de cette carte est contrôlé par le paramètre <b>Multiplicateur d&#39;entrée de carte d&#39;échelle</b> et est combiné aux autres paramètres du groupe <b>Taille</b>. |
| <b>Map rotation</b> *Niveaux de gris* | La texture en niveaux de gris contrôle la rotation des splines dispersées.  L&#39;effet de cette carte est contrôlé par le paramètre <b>Multiplicateur d&#39;entrée de Map rotation</b> et est combiné aux autres paramètres du groupe <b>Rotation</b>. |

<a name="outputs"></a>

## Sorties

|  |  |
|:---|:---|
| <b>Aperçu</b> *Niveaux de gris* | Aperçu des splines dispersées sous forme d&#39;image en niveaux de gris. |
| <b>Couleurs splines</b> *Couleur* | Coordonnées des points des splines dispersées codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Position X <b>G</b> - Position Y <b>B</b> - Height <b>A</b> - Données compressées : - Signe : la spline est fermée (négative) ou ouverte (positive) - Valeur absolue : Thickness + 1 |
| <b>Données splines</b> *Couleur* | Données supplémentaires des splines dispersées codées dans les canaux RVBA d&#39;une image couleur : <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Inutilisé <b>A</b> - Inutilisé |
| <b>Quantité de spline</b> *Nombre entier* | Nombre de splines dispersées. |

<a name="parameters"></a>

## Paramètres

|  |  |
|:---|:---|
| <b>Côté</b> *Nombre entier* | Détermine le ou les côtés des splines parentes sur lesquels les splines doivent être dispersées, en tenant compte du fait que « vers l&#39;avant » est la direction des splines *parentes* :<br><br>- <b>à gauche</b> placez les splines sur le côté gauche.<br>- <b>à droite</b> placez les splines sur le côté droit.<br>- <b>à gauche + à droite</b> placez les splines des deux côtés.<br>- <b>À gauche / à droite - en alternance</b> placez les splines à gauche puis à droite alternativement (par exemple, toutes les autres côté).<br>- <b>Gauche/Droite - Aléatoire</b> Choisissez le côté de manière aléatoire pour chaque spline. |
| <b>Mode Quantité</b> *Nombre entier* | Méthode de diffusion des splines le long des splines parentes, qui a un impact sur la quantité de splines diffusées sur chaque spline parente :<br><br>- <b>Quantité fixe par spline</b> La quantité spécifiée de splines à espacement régulier est diffusée.<br>- <b>Espacement</b> La quantité de splines est automatiquement ajustée pour s&#39;adapter à l&#39;espacement pair spécifié.<br><br>Dans les deux cas, la première et la dernière spline diffusée se trouvent exactement au début et à la fin de chaque spline parent, respectivement. |
| <b>Quantité De Spline Par Spline</b> *Nombre entier* | Nombre de splines régulièrement espacées et réparties le long de chaque spline parent. |
| <b>Espacement spline</b> *Flotter* | Distance minimale le long des splines parentes par laquelle les splines doivent être espacées, tout en plaçant la première et la dernière spline respectivement au début et à la fin de chaque spline parente. |
| <b>Type de spline</b> *Nombre entier* | Sélectionne le type de spline à disperser sur les splines parentes :<br><br>- <b>Droite</b> Une spline simple et droite.<br>- <b>Spline personnalisée</b> La ou les splines fournies aux entrées <b>Spline personnalisée</b>. Les splines multiples sont prises en charge lorsqu&#39;elles sont ajoutées ensemble dans une liste. |
| <b>Sélection Spline Personnalisée</b> *Nombre entier* | Lorsque vous utilisez plusieurs splines personnalisées ajoutées ensemble dans une liste, ce paramètre vous permet de sélectionner la façon dont ces splines doivent être distribuées dans la diffusion.<br><br>-<b>Liste complète</b> Toutes les splines sont dispersées ensemble en tant que groupe.<br>- <b>Séquentielle</b> Chaque spline individuelle est dispersée dans l&#39;ordre, en boucle autour de la liste.<br>- <b>Aléatoire</b> Une spline aléatoire est sélectionnée dans la liste pour chaque spline dispersée. |
| <b>Démarrer</b> *Flotter* | Décale le point à partir du début des splines parentes à l&#39;endroit où commence la diffusion. Cette valeur correspond à la longueur normalisée de chaque spline parent. |
| <b>Fin</b> *Flotter* | Décale le point à partir du début des splines parentes à l&#39;extrémité de la diffusion. Cette valeur correspond à la longueur normalisée de chaque spline parent. |
| <b>Inverser la direction</b> *Booléen* | Inverse la direction des splines dispersées. |
| <b>Mode De Symétrie Gauche/Droite</b> *Nombre entier* | Méthode de symétrie appliquée aux splines dispersées de chaque côté des splines parentes.<br><br>-<b>Désactivé</b> Aucune symétrie n&#39;est appliquée, les splines sont placées de chaque côté par une simple symétrie.<br>-<b>À gauche</b> La spline de gauche est symétrique à celle de droite par rapport à la spline parente.<br>-<b>À droite</b> La spline de droite est symétrique à celle de gauche par rapport à la spline parente. |
| <b>Lien Aléatoire Gauche/Droite</b> *Booléen* | Contrôle si les splines de chaque côté de la spline parent doivent utiliser les mêmes valeurs lors de l&#39;utilisation de la rotation aléatoire, de la mise à l&#39;échelle aléatoire, etc. En d&#39;autres termes :<br><br>-<i>False:</i> chaque spline utilise des valeurs aléatoires distinctes<br>-<i>True:</i> les deux splines partagent les mêmes valeurs aléatoires |
| <b>Mode Spline Pivot</b> *Nombre entier* | Définit la méthode de positionnement du pivot des splines dispersées, qui a un impact sur la rotation et la mise à l&#39;échelle.<br>Notez que le pivot est *toujours placé sur la spline parente* et que ses contrôles ont un impact sur la spline dispersée. En d&#39;autres termes : le pivot ne se déplace pas, c&#39;est la spline diffusée qui se déplace et se met à l&#39;échelle par rapport à lui.<br><br>-<b>Position le long de la spline</b> Déplacez le pivot le long de la spline diffusée.<br>-<b>Position absolue</b> Définissez une position arbitraire pour le pivot. |
| <b>Position de pivot le long de la spline</b> *Flotter* | La position normalisée du pivot le long de la spline diffusée, où 0 est son début et 1 son extrémité.<br>Notez que le pivot suit la *direction* de la spline diffusée et que l&#39;orientation de la spline peut changer pour préserver la position et la rotation du pivot par rapport à la spline parente. |
| <b>Pivot de la position absolue</b> *Float2* | Position du pivot dans l&#39;espace UV. |
| <b>Correction Non Carrée</b> *Booléen* | Ajustez la position et le thickness des splines pour conserver leur forme dans des résolutions autres que carrées.<br><i>Remarque :</i> lors de l&#39;utilisation de splines personnalisées, la spline personnalisée doit utiliser *le même rapport d&#39;image* que les nœuds <b>splines de Dispersion sur splines</b>. |
| <b>Taille</b> |  |
| <b>Échelle Spline</b> *Flotter* | Contrôle global de la taille de toutes les splines, où 1 correspond à leur taille d&#39;origine complète.<br>La mise à l&#39;échelle est appliquée par rapport au pivot d&#39;une spline. La position de pivot peut être décalée à l&#39;aide du paramètre <b>Spline Pivot</b>. |
| <b>Échelle Spline Aléatoire</b> *Flotter* | Applique un multiplicateur aléatoire jusqu&#39;à la valeur spécifiée pour réduire la taille des splines. |
| <b>Multiplicateur d&#39;entrée de mappage d&#39;échelle</b> *Flotter* | Contrôle l&#39;intensité de l&#39;entrée de la <b>carte d&#39;échelle</b>. Cette carte agit comme un multiplicateur pour la taille actuelle des motifs.<br>L&#39;effet de ce mappage est combiné aux autres paramètres du groupe <b>Taille</b>. |
| <b>Mode D&#39;Échantillonnage D&#39;Entrée De Mappage À L&#39;Échelle</b> *Nombre entier* | Méthode de mappage des valeurs de la <b>carte d&#39;échelle</b> aux splines :<br><br>-<b>espace de Texture</b> Les valeurs sont appliquées aux splines là où elles seraient si elles étaient placées dans une texture à l&#39;aide des coordonnées d&#39;UV de la texture. Cela applique efficacement la valeur aux splines « en place »<br>- <b>Horizontales le long de la spline</b>. Les valeurs sont appliquées directement aux coordonnées des splines codées (voir l&#39;entrée <b>Spline Coords</b>), où chaque ligne est appliquée à une spline différente de haut en bas<br>- <b>Heure. le long de la spline (rand. offset X)</b> Les valeurs sont appliquées directement aux coordonnées des splines codées (voir l&#39;entrée <b>Spline Coords</b>), avec un décalage horizontal aléatoire dans la <b>Scale Map</b> pour chaque spline (c&#39;est-à-dire chaque ligne dans <b>Spline Coords</b>)<br>- <b>Hor. le long de la spline (rand. offset Y)</b> Les valeurs sont appliquées directement aux coordonnées des splines codées (voir <b>Spline Coords</b> input), avec un décalage vertical aléatoire dans la <b>Scale Map</b> pour chaque spline (c&#39;est-à-dire chaque ligne dans <b>Spline Coords</b>) |
| <b>Atténuation Début/Fin</b> *Float2* | Tient compte de la distance entre le milieu de la spline et ses <b>début</b> et <b>fin</b> lors de la mise à l&#39;échelle des splines.<br>Cela signifie que la taille est réduite pour les splines plus proches des extrémités d&#39;une spline. |
| <b>Position</b> |  |
| <b>Décalage local</b> *Float2* | Applique un décalage aux positions des splines le long de la tangente (parallèle) et de la normale (perpendiculaire) de la spline parente. |
| <b>Décalage sur la plage de spline</b> *Nombre entier* | Définit la plage de décalage appliquée aux splines diffusées le long des splines parentes.<br><br>- <b>Intervalle</b> La plage s&#39;étend sur l&#39;intervalle *entre* chaque spline diffusée.<br>- <b>La spline parente</b> La plage s&#39;étend sur *toute la longueur* de la spline parente. |
| <b>Décalage sur la spline</b> *Flotter* | Applique un décalage de position aux splines le long des splines parentes. |
| <b>Plage de décalage aléatoire</b> *Nombre entier* | Définit la plage de décalage aléatoire appliquée aux splines diffusées le long des splines parentes.<br><br>- <b>Intervalle</b> La plage s&#39;étend sur l&#39;intervalle *entre* chaque spline diffusée.<br>- <b>La spline parente</b> La plage s&#39;étend sur *toute la longueur* de la spline parente. |
| <b>Décalage aléatoire sur la spline</b> *Flotter* | Applique un décalage de position supplémentaire aux splines le long des splines parentes. |
| <b>Décalage par Thickness</b> *Flotter* | Applique un décalage aux splines diffusées le long de la normale des splines parentes, jusqu&#39;au thickness des splines parentes.<br>En fait, la valeur 1 vous permet de placer les splines diffusées sur la *surface* de l&#39;enveloppe des splines parentes. |
| <b>Rotation</b> |  |
| <b>Alignement Spline Personnalisé</b> *Entier* | Contrôle l&#39;orientation initiale de la ou des splines personnalisées sur les splines parentes.<br><br>- <b>tangente du premier point</b> Les splines sont orientées en fonction de la tangente de leur premier point. En d&#39;autres termes, elles s&#39;éloignent des splines parentes dans la direction définie par leur premier point.<br>-<b>Espace de l&#39;image</b> Les splines sont placées telles qu&#39;elles apparaissent à l&#39;origine, sans aucun réglage supplémentaire de leur position ou de leur orientation, comme si l&#39;image qui les représente reposait sur la spline parente. |
| <b>Mode Rotation</b> *Entier* | Définit l&#39;orientation initiale des splines dispersées.<br><br>- <b>À partir d&#39;une spline</b> Les splines sont orientées pour correspondre à la *normale* des splines parentes à leur emplacement.<br>-<b>Absolue</b> Les splines sont toutes orientées de la *même façon*, quelle que soit la direction des splines parentes. |
| <b>Rotation</b> *Flottant* | Fait pivoter les splines autour de leurs pivots, en nombre de tours. La position de pivot peut être décalée à l&#39;aide du paramètre <b>Spline Pivot</b>. |
| <b>Rotation aléatoire</b> *Flottant* | Applique une rotation aléatoire supplémentaire aux splines autour de leurs pivots, en nombre de tours. La position de pivot peut être décalée à l&#39;aide du paramètre <b>Spline Pivot</b>. |
| <b>Angle Gauche/Droit</b> *Flottant* | Définit l&#39;angle de rotation symétrique appliqué aux splines de chaque côté des splines parentes, en nombre de tours. |
| <b>Angle gauche/droit aléatoire</b> *Flottant* | Ajoute une quantité aléatoire de rotation symétrique aux splines de chaque côté des splines parentes, en nombre de tours. |
| <b>Multiplicateur d&#39;entrée de Map rotation</b> *Flottant* | Contrôle l&#39;intensité de l&#39;entrée de <b>Map rotation</b>. Cette carte agit comme un multiplicateur pour la rotation actuelle des motifs.<br>L&#39;effet de cette carte est combiné aux autres paramètres du groupe <b>Rotation</b>. |
| <b>Mode D&#39;Échantillonnage D&#39;Entrée De Map rotation</b> *Nombre entier* | Méthode de mappage des valeurs de la <b>Map rotation</b> aux splines :<br><br>-<b>espace de Texture</b> Les valeurs sont appliquées aux splines où elles seraient si elles étaient placées dans une texture à l&#39;aide des coordonnées d&#39;UV de la texture. Cela applique efficacement la valeur aux splines « en place »,<br>- <b>Horizontales le long de la spline</b>. Les valeurs sont appliquées directement aux coordonnées des splines codées (voir l&#39;entrée <b>Spline Coords</b>), où chaque ligne est appliquée à une spline différente de haut en bas,<br>- <b>Heure. le long de la spline (rand. offset X)</b> Les valeurs sont directement appliquées aux coordonnées des splines codées (voir la section <b>Entrée Spline Coords</b>), avec un décalage horizontal aléatoire dans la <b>Map rotation</b> pour chaque spline (c&#39;est-à-dire chaque ligne dans <b>Spline Coords</b>).<br>- <b>Hor. le long de la spline (rand. offset Y)</b> Les valeurs sont directement appliquées aux coordonnées des splines codées (voir <b>Spline Coords</b> input), avec un décalage vertical aléatoire dans la <b>Map rotation</b> pour chaque spline (c&#39;est-à-dire chaque ligne dans <b>Spline Coords</b>)<b>.</b> |
| <b>L&#39;Entrée De Map rotation Affecte</b> *Nombre entier* | Sélectionne le paramètre de rotation qui est affecté par la <b>Map rotation</b>:<br><br>-<b>rotation de la spline</b> La carte affecte la rotation globale des splines dans le sens horaire.<br>-<b>Angle gauche/droit</b> La carte affecte la rotation symétrique des splines <b>Gauche/Droite</b>. |
| <b>Height</b> |  |
| <b>Mode Height de démarrage</b> *Nombre entier* | Méthode de calcul de l&#39;height de départ des splines diffusées.<br><br>- <b>Manuel</b> Définissez la même valeur absolue pour toutes les splines diffusées.<br>- <b>À partir de la spline parent (+ spline personnalisée)</b> Utilisez l&#39;height de la spline parent, puis ajoutez l&#39;height de la spline personnalisée à l&#39;aide du <b>mult d&#39;height de départ de spline personnalisée.</b> <br>- <b>À partir d&#39;une spline personnalisée</b> Utilisez l&#39;height de la spline personnalisée telle quelle.<br><br><i>Remarque :</i> définissez <b>Type de spline</b> sur &#39;Spline personnalisée&#39; et connectez les entrées <b>Spline personnalisée</b> pour utiliser l&#39;height des splines personnalisées. |
| <b>Height de début de spline personnalisé multiple.</b> *Flotter* | Contrôle la contribution de l&#39;height de départ de la spline personnalisée à l&#39;height de départ des splines dispersées, où 1 signifie que l&#39;height complet de la spline personnalisée est utilisé.<br>L&#39;height de la spline personnalisée est utilisé différemment selon le <b>mode d&#39;Height de départ</b> :<br>- <i>à partir de la spline parent (+ spline personnalisée) :</i> l&#39;height est ajouté à la spline parent<br>- <i>à partir de la spline personnalisée :</i> l&#39;height est utilisé directement |
| <b>Décalage de l&#39;Height de début</b> *Flotter* | Applique un décalage absolu à l&#39;height de départ de la spline. |
| <b>Height de démarrage</b> *Flottant* | Définit une valeur absolue pour l&#39;height de départ de la spline diffusée. |
| <b>Mode d&#39;Height final</b> *Entier* | Méthode de calcul de l&#39;height de fin des splines diffusées.<br><br>- <b>Manuel</b> Définissez la même valeur absolue pour toutes les splines diffusées.<br>- <b>À partir de la spline parent (+ spline personnalisée)</b> Utilisez l&#39;height de la spline parent, puis ajoutez l&#39;height de la spline personnalisée à l&#39;aide de l&#39;<b>Height d&#39;extrémité personnalisé Mult.</b> <br>- <b>À partir d&#39;une spline personnalisée</b> Utilisez l&#39;height de la spline personnalisée telle quelle.<br><br><i>Remarque :</i> définissez <b>Type de spline</b> sur Spline personnalisée et connectez les entrées <b>Spline personnalisée</b> pour utiliser l&#39;height des splines personnalisées. |
| <b>Height d&#39;extrémité de spline personnalisé multiple.</b> *Flottant* | Contrôle la contribution de l&#39;height de fin de la spline personnalisée à l&#39;height de fin des splines dispersées, où 1 signifie que l&#39;height complet de la spline personnalisée est utilisé.<br>L&#39;height de la spline personnalisée est utilisé différemment selon le <b>mode d&#39;Height final</b> :<br>- <i>à partir de la spline parent (+ spline personnalisée) :</i> l&#39;height est ajouté à la spline parent<br>- <i>à partir de la spline personnalisée :</i> l&#39;height est utilisé directement |
| <b>Décalage de l&#39;Height de fin</b> *Flottant* | Applique un décalage absolu à l&#39;height d&#39;arrivée de la spline diffusée. |
| <b>Height final</b> *Flottant* | Définit une valeur absolue pour l&#39;height d&#39;arrivée de la spline diffusée. |
| <b>Thickness</b> |  |
| <b>Démarrer le mode de Thickness</b> *Entier* | Méthode de calcul du thickness de départ des splines dispersées.<br><br>- <b>Manuel</b> Définissez la même valeur absolue pour toutes les splines dispersées.<br>- <b>À partir de la spline parent</b> Utilisez le thickness de la spline parent.<br>- <b>À partir d&#39;une spline personnalisée</b> Utilisez le thickness de la spline personnalisée.<br><br><i>Remarque :</i> Définissez <b>Type de spline</b> sur Spline personnalisée et connectez les entrées <b>Spline personnalisée</b> pour utiliser le thickness de splines personnalisées. |
| <b>Démarrer le multiplicateur de Thickness</b> *Flottant* | Met à l&#39;échelle le thickness de départ des splines dispersées, où 1 représente le thickness entier. |
| <b>Décalage du Thickness de début</b> *Flottant* | Applique un décalage absolu au thickness de départ de la spline. |
| <b>Démarrer le Thickness</b> *Flotter* | Définit une valeur absolue pour le thickness de départ de la spline. |
| <b>Fin du mode de Thickness</b> *Nombre entier* | Méthode de calcul du thickness de fin des splines dispersées.<br><br>- <b>Manuel</b> Définissez la même valeur absolue pour toutes les splines dispersées.<br>- <b>À partir de la spline parent</b> Utilisez le thickness de la spline parent.<br>- <b>À partir d&#39;une spline personnalisée</b> Utilisez le thickness de la spline personnalisée.<br><br><i>Remarque :</i> Définissez <b>Type de spline</b> sur Spline personnalisée et connectez les entrées <b>Spline personnalisée</b> pour utiliser le thickness de splines personnalisées. |
| <b>Multiplicateur de Thickness de fin</b> *Flotter* | Met à l&#39;échelle le thickness de départ des splines dispersées, où 1 représente le thickness entier. |
| <b>Décalage du Thickness de fin</b> *Flotter* | Applique un décalage absolu au thickness d&#39;arrivée de la spline diffusée. |
| <b>Fin de Thickness</b> *Flotter* | Définit une valeur absolue pour le thickness de fin de la spline diffusée. |
| <b>Aperçu</b> |  |
| <b>Afficher l&#39;assistant de direction</b> *Booléen* | Affiche un point au début de la spline et une flèche à sa fin dans la sortie <b>Aperçu</b>. |
| <b>Afficher l&#39;enveloppe de Thickness</b> *Booléen* | Affiche des lignes supplémentaires sur les bords du thickness de la spline. |
| <b>Thickness (px)</b> *Flotter* | Ajuste le thickness de la visualisation de la spline dans la sortie <b>Aperçu</b>, en nombre de pixels. |
| <b>Quantité de segments</b> *Nombre entier* | Ajuste le nombre de segments utilisés pour dessiner la visualisation de la spline dans la sortie <b>Aperçu</b>. Plus la valeur est élevée, plus la ligne est lisse. |
| <b>Intensité de l&#39;arrière-plan</b> *Flotter* | Intensité de l&#39;entrée <b>Aperçu</b> dans la visualisation de la sortie <b>Aperçu</b>. |

## Exemples

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : Exemple 1](../../../../../../assets/scatter-splines-on-splines-example-1.png "Splines de Dispersion sur splines : exemple 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : Exemple 1](../../../../../../assets/scatter-splines-on-splines-example-2.png "Splines de Dispersion sur splines : exemple 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : Exemple 3](../../../../../../assets/scatter-splines-on-splines-example-4.png "Splines de Dispersion sur splines : Exemple 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : Exemple 4](../../../../../../assets/scatter-splines-on-splines-example-3.png "Splines de Dispersion sur splines : Exemple 4"){zoomable="yes"}

</td>
</tr>
</table>

## Rendus

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : rendu 1](../../../../../../assets/scatter-splines-on-splines-demo-1.png "Les splines de Dispersion sur splines : rendu 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersion sur splines : rendu 2](../../../../../../assets/scatter-splines-on-splines-demo-3.png "Les splines de Dispersion sur splines : rendu 2"){zoomable="yes"}

</td>
</tr>
</table>

![Splines de Dispersion sur splines : rendu 3](../../../../../../assets/scatter-splines-on-splines-demo-2.png "Les splines de Dispersion sur splines : rendu 3"){zoomable="yes"}
