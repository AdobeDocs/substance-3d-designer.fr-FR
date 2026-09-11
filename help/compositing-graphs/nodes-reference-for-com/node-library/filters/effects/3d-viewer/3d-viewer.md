---
title: Visionneuse 3D
description: Designer > graphes de composition de Substance > Référence des nœuds pour les graphes de composition de Substance > Bibliothèque de nœuds > Filtre > Effet > Visualiseur 3D
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 0%

---


# Visionneuse 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icône de la visionneuse 3D](./3d-viewer.resources/3d-viewer.png "3D")

<b>Entrée :</b> Filtre > Effet

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

Calcule un rendu 3D pour un fichier SDF spécifié ou une scène d’intersection définie par un graphe de fonction, avec une caméra et un éclairage d&#39;environnement personnalisés.<br><br>Ce nœud est utile pour la création et la visualisation de [Fonctions SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) à utiliser dans le nœud [Shape splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) .<br><br>Des Assistants sont disponibles pour visualiser les attributs essentiels des formes dans l&#39;espace.<br><br>Pour les utilisateurs expérimentés, des fonctions personnalisées peuvent être créées pour configurer la caméra et/ou le rendu 3D par pixel.

</td>
</tr>
</table>

>[!INFO]
> 
> Pour en savoir plus sur les concepts et les workflows impliquant des Fonctions SDF, consultez la page dédiée : [Utilisation des Fonctions SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entrées

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Environnement</b> *Couleur* | Image à projeter sur la sphère infinie utilisée comme environnement de la scène et utilisée pour l&#39;éclairage de l&#39;environnement.<br><br>La projection est <i>équirectangulaire</i>, identique à celle utilisée par les maps d&#39;environnement par défaut de Designer disponibles dans la catégorie <b>Environnements vue 3D > HDRI</b> de la bibliothèque.<br><br>Sans connexion, un environnement par défaut est utilisé.<br><br><i>Conseil :</i> utilisez une image HDR (32 bits) pour un éclairage précis. |
| <b>Entrée 1</b> *Couleur* | Image qui peut être échantillonnée dans le graphe de fonction <b>Sortie personnalisée</b> lorsque le paramètre <b>Sortie</b> est défini sur « Personnalisée ».<br><br>Utilisez un nœud [Échantillon de couleur](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) défini sur « Entrée image 0 » pour échantillonner cette image. |
| <b>Entrée 2</b> *Couleur* | Image qui peut être échantillonnée dans le graphe de fonction <b>Sortie personnalisée</b> lorsque le paramètre <b>Sortie</b> est défini sur « Personnalisée ».<br><br>Utilisez un nœud [Échantillon de couleur](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) défini sur « Entrée d&#39;image 1 » pour échantillonner cette image. |

<a name="outputs"></a>

## Sorties

|               |                                                                                                                                                                                                                                    |
|:--------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Sortie</b> | Scène rendue, à l&#39;aide de l&#39;AOV sélectionné dans le paramètre <b>Sortie</b>.<br><br><i>Remarque :</i> pour des lectures précises dans certains AOV, assurez-vous que la vue 2D utilise un espace colorimétrique linéaire et que le nœud utilise un format de sortie HDR 32 bits. |

<a name="parameters"></a>

## Paramètres

|                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Type de Scène</b> *Entier* | Type de fonction utilisé pour décrire les surfaces et les formes à rendre :<br>- <b>SDF:</b> Utilisez une fonction de champ de distance signé (SDF), qui peut décrire des formes complexes.<br>- <b>Intersection :</b> Utilisez des fonctions d&#39;intersection, qui sont plus rapides lorsque seules des formes primitives simples sont nécessaires. |
| <b>scène SDF</b> *Flottant* | Fonction SDF (signed Distance Field) décrivant les surfaces et les formes de la scène.<br><br>Utilisez les nœuds de la catégorie [Fonctions SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) de la bibliothèque pour créer la fonction. |
| <b>Intersection de la scène</b> *Flottant* | Fonction d&#39;intersection décrivant les surfaces et les formes de la scène.Les fonctions d&#39;<br><br>intersection pour les primitives et opérateurs simples sont disponibles dans les dossiers <b>3d_intersection</b> du package de bibliothèque <b>3d_features.sbs</b>.<br><br><i>Conseil :</i> vous pouvez accéder au package en déposant n&#39;importe quel nœud SDF de la bibliothèque dans l&#39;Explorateur. |
| <b>Sortie</b> *Entier* | Type de rendu 3D qui doit être généré par le nœud, généralement appelé AOV (Variables de sortie arbitraires).<br><br>Les AOV disponibles sont les suivants :<br>- <b>Beauté :</b> Résultat final du rendu 3D, avec des couleurs et des effets orientés vers l’art.<br>-<b>WS normaux :</b> normales des espaces monde des formes dans la scène.<br>- <b>TS normaux :</b> Normales de l’espace de tangente des formes dans la scène.<br>-<b>Position :</b> Position espace monde des surfaces les formes de la scène.<br>- <b>Distance :</b> Distance brute entre la caméra et les formes de la scène<br>- <b>Profondeur :</b> Distance signée entre les formes et le plan cible de la caméra, où le plan face toujours la caméra.<br>- <b>Couleur :</b> base color des formes (utilisez le nœud « Définir la couleur » pour attribuer des couleurs aux formes dans la fonction de scène)<br>- <b>ID de Matériau :</b> ID de matériau appliqué aux surfaces de forme (Utilisez le nœud « Définir l&#39;ID de matériau » pour attribuer des ID de matériau aux formes dans la fonction scène)<br>- <b>Étapes de vectorisation de sphère :</b> visualisation de la quantité d&#39;étapes requises pour définir la surface d&#39;une forme. Des valeurs plus claires signifient que davantage d&#39;étapes étaient nécessaires.<br>- <b>Personnalisé:</b> Créez une fonction personnalisée pour calculer la couleur du rendu par pixel.<br><br><i>Remarque :</i> Pour des lectures précises dans certains AOV, assurez-vous que la vue 2D utilise un espace colorimétrique linéaire et que le nœud utilise un format de sortie HDR 32 bits. |
| <b>Sortie personnalisée</b> *Flottant4* | Graphe de fonction définissant les couleurs RVBA par pixel de la scène rendue, sous la forme d’une valeur Flottant 4.<br><br>Variables disponibles :<br>- <code>scène.position</code> (Flottant 3) Position espace monde des surfaces de la scène.<br>- <code>scène.normal</code> (Flottant 3) normales des espaces monde des surfaces de la scène.<br>- <code>scène.hit</code> (Booléen) Retourne &#39;True&#39; lorsqu&#39;une surface est frappée par un rayon de caméra.<br>- <code>view.origin</code> (Flottant 3) Position espace monde par pixel de la vue caméra.<br>- <code>view.direction</code> (Flottant 3) Vecteur avant par pixel de la vue caméra, en fonction du mode projection. (E.g. perspective ou orthographique)<br>- <code>matériau.color</code> (Flottant 3) base color des surfaces de la scène.<br>- <code>matériau.metalness</code> (Flottant) La métallisation des surfaces de la scène.<br>- <code>matériau.rugosité</code> (Flottant) rugosité des surfaces de la scène.<br>- <code>matériau.id</code> (Entier) ID de matériau des surfaces de la scène.<br><br>Les entrées d&#39;image du nœud peuvent être échantillonnées en sélectionnant les emplacements de nœud [Exemple de couleur](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) suivants :<br>-<b>Entrée d&#39;image 0</b> échantillons Entrée 1.<br>- <b>Entrée d&#39;image 1</b> échantillons Entrée 2. |
| <b>Rotation de l&#39;environnement</b> *Flottant* | Rotation de l&#39;<b>environnement</b>, en nombre de tours. |
| <b>Mode Arrière-plan</b> *Entier* | Spécifie la source de l&#39;arrière-plan de la scène, dessinée là où aucune surface de forme n&#39;est visible.<br><br>- <b>Couleur :</b> &#39;Couleur d&#39;arrière-plan&#39; plate.<br>- <b>Environnement :</b> Image fournie à l&#39;entrée &#39;Environnement&#39;, appliquée à une sphère infinie à l&#39;aide d&#39;une projection équirectangulaire.  (Lorsque l’entrée n’est pas connectée, un environnement par défaut est utilisé.) |
| <b>Couleur d&#39;arrière-plan</b> *Flottant4* | Couleur plate utilisée comme arrière-plan de la scène. |
| <b>Échantillons IBL</b> *Entier* | Quantité d&#39;échantillons de lumière effectuée par échantillon de caméra.<br><br>Une valeur plus élevée permet un éclairage plus fluide et plus précis au détriment des performances. |
| <b>Échantillons de Caméra</b> *Entier* | Nombre d’échantillons de caméra effectués par pixel.<br><br>Ce paramètre affecte la qualité de l’anticrénelage et la profondeur de l’effet de champ.<br><br>Plus la valeur est élevée, plus l’image est claire et moins bruyante, au détriment des performances. |
| <b>Marche des rayons</b> *Entier* | Le nombre d&#39;étapes effectuées dans le processus de tracé de sphère, la technique de lancer de rayons utilisée pour détecter et dessiner les surfaces des formes.<br><br>Une valeur plus élevée donne des surfaces précises et cohérentes (en particulier pour les formes complexes), au détriment des performances.<br><br><i>Conseil :</i> Définissez le paramètre <b>Sortie</b> sur l&#39;AOV des étapes de tracé de sphère pour visualiser les zones des formes qui nécessitent plus d&#39;étapes. La réduction du nombre d&#39;étapes aura d&#39;abord une incidence sur ces secteurs. |
| <b>Étapes de défilement du rayon secondaire</b> *Entier* | Nombre d&#39;étapes effectuées dans le processus de vectorisation de sphère pour calculer l&#39;occlusion de diffusion et de specular afin de dessiner des ombres convertissez.<br><br>Une valeur plus élevée donne des ombres plus précises au détriment des performances. |
| <b>Mode Caméra</b> *Entier* | Méthode de projection de la scène sur l&#39;image de rendu :<br><br>- <b>Perspective :</b> Cette projection véhicule la profondeur et permet des effets d&#39;objectif tels que la profondeur de champ.<br>- <b>Orthographique :</b> Cette projection aplatit la scène, annulant la profondeur.<br>- <b>Fonction personnalisée :</b> Créez un graphe de fonction pour configurer une caméra personnalisée. |
| <b>Fonction de Caméra</b> *Flottant3* | Graphe de fonction définissant la transforme de la caméra. Il peut être utilisé pour configurer une caméra personnalisée.<br><br>La fonction doit <b>définir</b> ces variables :<br>- <code>view.origin</code> (Flottant 3) Position espace monde par pixel de la vue caméra.<br>- <code>view.direction</code> (Flottant 3) Vecteur avant par pixel de la vue caméra, en fonction du mode projection. (E.g. perspective ou orthographique)<br><br>Les variables suivantes sont disponibles pour <b>get</b>:<br>- <code>caméra.origin</code> (Flottant 3) Position espace monde de la caméra. (caméra.direction * distance_caméra + caméra.cible)<br>- <code>caméra.direction</code> (Flottant 3) direction dans l&#39;espace monde de la caméra, c&#39;est-à-dire le vecteur Y vers l&#39;avant de la caméra.<br>- <code>caméra.right</code> (Flottant 3) Vecteur X-right de la caméra.<br>- <code>caméra.up</code> (Flottant 3) Vecteur Z-up de la caméra.<br>- <code>caméra.target</code> (Flottant 3) Position espace monde de la cible de caméra. |
| <b>UV</b> *Flottant 2* | Position dans l&#39;espace d&#39;image 2D utilisée pour déduire la position et la direction de la caméra en orbite autour de la <b>position cible</b>.<br><br><i>Conseil :</i> ce paramètre peut être ajusté de manière intuitive à l&#39;aide du <i>gadget de position</i> disponible dans la vue 2D lorsque le nœud est sélectionné. |
| <b>FOV</b> *Flottant* | Le champ de vision de la caméra orthographique (FOV), qui affecte le facteur de zoom. |
| <b>Distance focale</b> *Flottant* | La distance focale de la caméra, qui a un impact sur le facteur de zoom et la profondeur de l’effet de champ. |
| <b>Distance par rapport à la cible</b> *Flottant* | Distance sur laquelle la caméra doit reposer à partir de la <b>position cible</b>.<br><br>Le réglage de cette option déplace la caméra dans le sens caméra-cible. |
| <b>Position cible</b> *Flottant3* | Position de la cible de caméra vers laquelle la caméra est toujours orientée. |
| <b>Mappeur de tonalité</b> *Entier* | Algorithme de mappage de tonalité qui doit être appliqué au rendu de la scène.<br><br>- <b>Aucun(e) (Raw)<br>- <b>sRGB</b><br>- <b>AgX</b><br>- <b>ACE</b> |
| <b>Activer la profondeur du champ</b> *Booléen* | Simule l’effet d’objectif de caméra de profondeur de champ pour la caméra de perspective.<br><br>Utilisez les paramètres <b>F number</b> et <b>Distance de mise au point</b> pour régler l&#39;ouverture et le point focal de l&#39;effet respectivement.<br><br>Le résultat est également affecté par la <b>Distance focale</b>. |
| <b>Numéro-F</b> *Flottant* | L&#39;<i>ouverture</i> de la caméra.<br><br>Une valeur inférieure entraîne une <i>profondeur de champ</i> plus courte, c&#39;est-à-dire une plage de distance plus courte pour les objets nets et un effet de flou plus fort à mesure que la distance à partir de cette plage augmente. |
| <b>Distance de mise au point</b> *Flottant* | Définit la distance du point focal comme distance par rapport à la caméra le long de son vecteur avant.<br><br>Les surfaces situées dans la plage de cette distance apparaîtront nettes. Cette plage (la <i>profondeur de champ </i>) est définie par le <b>numéro F</b>. |
| <b>Exposition (EV)</b> *Flottant* | Quantité de lumière atteignant le capteur de caméra, c&#39;est-à-dire l&#39;intensité de l&#39;éclairage dans le rendu.<br><br>Une valeur inférieure entraîne une scène rendue plus sombre.<br><br>La valeur d&#39;exposition (EV) fait spécifiquement référence à la quantité de lumière à laquelle le capteur de caméra est <i>exposé</i>. |
| <b>Base color</b> *Flottant3* | Base color par défaut pour les surfaces où cette couleur n&#39;est pas définie par sa fonction SDF ou intersection. |
| <b>Rugosité</b> *Flottant* | Valeur de rugosité par défaut pour les surfaces où cette valeur n&#39;est pas définie par sa fonction SDF ou d&#39;intersection. |
| <b>Métallique</b> *Flottant* | Valeur de métal par défaut pour les surfaces où cette valeur n&#39;est pas définie par sa fonction SDF ou d&#39;intersection. |
| <b>Opacité des Assistants</b> *Flottant* | L’opacité des assistants 3D, où une valeur plus faible entraîne des assistants plus flous. |
| <b>cadre de délimitation</b> *Booléen* | Visualisation d’une cage à six côtés définissant les limites de la scène entière. Doit idéalement être la plus petite taille possible qui inclut entièrement la scène.<br><br>Utilisez le paramètre <b>Taille du cadre de délimitation</b> pour ajuster la taille de la cage.<br><br>Le paramètre <b>Coloriser hors cadre</b> vous permet de visualiser facilement les surfaces en dehors de cette cage, ce qui a un impact sur le résultat de l&#39;utilisation de cette scène dans le nœud [Shape splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md). (Voir l’info-bulle « Taille du cadre de délimitation ») |
| <b>Taille du cadre de délimitation</b> *Flottant3* | Définit la taille XYZ du cadre de délimitation.<br><br>Ajustez le cadre à votre scène, puis appliquez les mêmes valeurs au paramètre <b>Taille du cadre liée au SDF</b> du nœud [Shape splatter v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) pour vous assurer que toutes les formes de la scène sont correctement incluses et dessinées par ce nœud. |
| <b>Coloriser sans cadre</b> *Booléen* | Applique une couleur rouge aux surfaces en dehors du cadre de délimitation.<br><br>Cela permet de vérifier que la scène est entièrement incluse dans son cadre de délimitation. |
| <b>Axe</b> *Booléen* | Affichage des axes XYZ de la scène sous forme de lignes colorées commençant à l’origine de la scène. |
| <b>Grille</b> *Booléen* | Visualisation d’une grille posée sur les axes XY, où la taille d’une cellule en X et Y est d’une unité de scène. |
| <b>Transformer les assistants</b> *Booléen* | Visualisation de la dernière rotation appliquée.<br><br>La visualisation comprend<br>-<b>une flèche</b> représentant le vecteur de direction de l&#39;axe de rotation, et colorée après les poids de chaque axe d&#39;espace monde.<br>-<b>un arc</b> représentant l&#39;angle de rotation, orthogonal à la flèche correspondant à sa couleur. |
| <b>Isolines SDF</b> *Booléen* | Visualisation colorée des isolignes de la fonction SDF (signed distance field).<br><br>Les isolignes répètent régulièrement des lignes représentant le <i>champ de distance</i> de la forme sur le plan XY à un height donné.<br><br>Ils sont utiles pour vérifier l&#39;<i>uniformité de l&#39;espace</i> défini par la Fonction SDF.<br><br>Utilisez les paramètres de <b>fréquence des isolignes SDF</b> et de <b>position des isolignes SDF</b> pour ajuster la densité et l&#39;height des isolignes. |
| <b>Fréquence des isolignes SDF</b> *Flottant* | Nombre de répétitions d&#39;isolignes sur une distance donnée.<br><br>Une valeur plus élevée donne des lignes plus denses et plus fines. |
| <b>Position des isolignes SDF</b> *Flottant* | Height espace monde du plan XY utilisé pour tracer les isolignes.<br><br>Utilisez cette option pour vérifier le champ de distance de la forme à différentes altitudes. |
| <b>Min. distance d&#39;accès</b> *Flottant* | Définit la distance minimale qui translate en un accès pour le processus de lancer de rayon SDF.<br><br>Une valeur faible augmentera le nombre d&#39;étapes de lancer de rayon. |

## Exemples

<table style="border: none;">
    <tr style="width: 50%;">
        <td style="text-align: center">
            <img src="3d-viewer.resources/3d-viewer-example-01.jpg" alt="Exemple 1" />
        </td>
        <td style="width: 50%;">
            <table style="border: none;">
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02a.jpg" alt="Exemple 1" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02b.jpg" alt="Exemple 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02c.jpg" alt="Exemple 3" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02d.jpg" alt="Exemple 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>
