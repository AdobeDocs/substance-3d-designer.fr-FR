---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Découvrez les nœuds de fonction atomique, les plus petites unités de nœuds dans les graphiques de fonction de Substance pour créer des fonctions personnalisées.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nœuds de fonction atomique
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 17%

---


# Nœuds de fonction atomique

De la même manière que pour les [nœuds atomiques dans les graphes de Substances](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), les nœuds atomiques dans les graphes de fonctions de Substance sont les plus petites unités de nœuds de ce type de graphe.

Ils peuvent être triés en plusieurs catégories selon leur objectif :

| Catégorie | Nœud | Type(s) d’entrée | Type de sortie | Description |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Constant](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Flottant | - | Flottant | Définit une valeur flottante constante, par exemple 0,1 |
|                                                                                                                                        | Flottant2 | - | Flottant2 | Définit un vecteur constant de 2 valeurs flottantes, par exemple (0,1, 0,2) |
|                                                                                                                                        | Flottant3 | - | Flottant3 | Définit un vecteur constant de 3 valeurs flottantes, par exemple (0,1, 0,2, 0,3) |
|                                                                                                                                        | Flottant4 | - | Flottant4 | Définit un vecteur constant de 4 valeurs flottantes, par exemple (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Entier | - | Entier | Définit une valeur entière constante, par exemple 1 |
|                                                                                                                                        | Entier2 | - | Entier2 | Définit un vecteur constant de 2 valeurs entières, par exemple (1, 2) |
|                                                                                                                                        | Entier3 | - | Entier3 | Définit un vecteur constant de 3 valeurs entières, par exemple (1, 2, 3) |
|                                                                                                                                        | Entier4 | - | Entier4 | Définit un vecteur constant de 4 valeurs entières, par exemple (1, 2, 3 ,4) |
|                                                                                                                                        | Booléen | - | Booléen | Définit une valeur booléenne constante, par exemple True ou False |
|                                                                                                                                        | Chaîne | - | Chaîne | Définit une valeur constante de type String, par exemple « Substance » |
| [Vecteur](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vecteur flottant2 | Float1 | Flottant 2 | Diffuse 2 valeurs flottantes dans un vecteur de 2 coordonnées |
|                                                                                                                                        | Vecteur flottant3 | Float1 / Float2 | Flottant 3 | Diffuse 2 valeurs flottantes dans un vecteur de 3 coordonnées |
|                                                                                                                                        | Vecteur flottant4 | Float1 / 2 / 3 | Flottant 4 | Diffuse 2 valeurs flottantes dans un vecteur de 4 coordonnées |
|                                                                                                                                        | Swizzle flottant1 | Vecteur flottant | Float1 | Extrait une coordonnée flottante d’un vecteur |
|                                                                                                                                        | Swizzle flottant2 | Vecteur flottant | Flottant2 | Extraction de 2 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Swizzle flottant3 | Vecteur flottant | Flottant3 | Extraction de 3 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Swizzle flottant4 | Vecteur flottant | Flottant4 | Extrait 4 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Vecteur entier2 | Entier2 | Vecteur entier2 | Diffuse 2 valeurs entières dans un vecteur de 2 coordonnées |
|                                                                                                                                        | Vecteur entier3 | Entier3 | Entier3 | Diffuse 2 valeurs entières dans un vecteur de 3 coordonnées |
|                                                                                                                                        | Vecteur entier4 | Entier4 | Entier4 | Projeter 2 valeurs entières dans un vecteur de 4 coordonnées |
|                                                                                                                                        | Swizzle entier1 | Vector Integer | Entier1 | Extrait une coordonnée entière d’un vecteur |
|                                                                                                                                        | Swizzle entier2 | Vector Integer | Entier2 | Extraction de 2 coordonnées entières d’un vecteur |
|                                                                                                                                        | Swizzle entier3 | Vector Integer | Entier3 | Extrait 3 coordonnées entières d’un vecteur |
|                                                                                                                                        | Swizzle entier4 | Vector Integer | Entier4 | Extrait 4 coordonnées entières d’un vecteur |
| [Variables](../../../function-graphs/variables/variables.md) | Définir | tout | type d’entrée | Définit une variable |
|                                                                                                                                        | Get Integer1 | - | Entier1 | Obtention d’une entrée de valeur d’entier de fonction ou de graphique |
|                                                                                                                                        | Obtenir entier2 | - | Entier2 | Obtention d’une entrée de valeur de fonction ou de graphique Integer2 |
|                                                                                                                                        | Obtenir entier3 | - | Entier3 | Obtention d’une entrée de valeur de fonction ou de graphique Entier3 |
|                                                                                                                                        | Obtenir entier4 | - | Entier4 | Obtention d’une entrée de valeur de fonction ou de graphique Integer4 |
|                                                                                                                                        | Obtenir Float1 | - | Float1 | Obtenir une entrée de valeur flottante de fonction ou de graphique |
|                                                                                                                                        | Obtenir flottant2 | - | Flottant2 | Obtenir une entrée de valeur de fonction ou de graphique Float2 |
|                                                                                                                                        | Obtenir Flottant3 | - | Flottant3 | Obtention d’une entrée de valeur de fonction ou de graphique Float3 |
|                                                                                                                                        | Obtenir flottant4 | - | Flottant4 | Obtenir une entrée de valeur Float4 de fonction ou de graphique |
|                                                                                                                                        | Obtenir booléen | - | Booléen | Obtenir une entrée de valeur booléenne de fonction ou de graphique |
| Échantillonnages | Échantillon gris | Vecteur flottant2 | Flottant4 | Renvoie la valeur de niveaux de gris d’une image d’entrée aux coordonnées UV données (float2) |
|                                                                                                                                        | Échantillon de couleur | Vecteur flottant2 | Flottant4 | Renvoie la valeur chromatique d’une image d’entrée aux coordonnées UV données (float2) |
| Convertir | Vers Flottant | Entier1 | Float1 | Convertit un nombre entier en nombre flottant |
|                                                                                                                                        | Vers flottant2 | Entier2 | Flottant2 | Convertit un entier2 en float2 |
|                                                                                                                                        | Vers flottant3 | Entier3 | Flottant3 | Convertit un entier3 en float3 |
|                                                                                                                                        | Vers flottant4 | Entier4 | Flottant4 | Convertit un entier4 en float4 |
|                                                                                                                                        | Vers entier | Float1 | Entier1 | Convertit un élément flottant en entier |
|                                                                                                                                        | Vers entier2 | Flottant2 | Entier2 | Convertit un élément Float2 en entier2 |
|                                                                                                                                        | Vers entier3 | Flottant3 | Entier3 | Convertit un élément Float3 en entier3 |
|                                                                                                                                        | Vers entier4 | Flottant4 | Entier4 | Convertit un élément Float4 en entier4 |
| [Opérateur](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Addition | Vecteur Flottant/Entier | Type de a et b | Ajoute 2 valeurs du même type : a + b |
|                                                                                                                                        | Soustraction | Vecteur Flottant/Entier | Type de a et b | Soustrait 2 valeurs du même type : a - b |
|                                                                                                                                        | Multiplication | Vecteur Flottant/Entier | Type de a et b | Multiplie 2 valeurs du même type : a \* b |
|                                                                                                                                        | Multiplication scalaire | Vecteur flottant | Type de | Multiplie une valeur par une valeur flottante : un scalaire \* |
|                                                                                                                                        | Division | Float1 / Entier1 | Type de a et b | Divise 2 valeurs du même type : a / b |
|                                                                                                                                        | Négation | Float1 / Entier1 | Type de | Renvoie la valeur négative : -a |
|                                                                                                                                        | Modulo | Float1 / Entier1 | Type de | Renvoie la valeur du modulo : mod(a, diviseur) |
|                                                                                                                                        | Produit scalaire | Vecteur flottant | Type de a et b | Renvoie le produit de 2 valeurs du même type : dot(a, b) |
| [Logique](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | Et | Booléen | Booléen | Renvoie true (vrai) si les 2 entrées booléennes sont true (vrai). Renvoie la valeur false si l&#39;une des entrées est false. |
|                                                                                                                                        | Ou | Booléen | Booléen | Renvoie true (vrai) si 1 des entrées booléennes est true (vrai). Renvoie la valeur false dans les deux cas. |
|                                                                                                                                        | Non | Booléen | Booléen | Renvoie le booléen de négation de l&#39;entrée : !a |
| [Comparaison](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Égal à | Float1 / Entier1 | Booléen | Renvoie true (vrai) si a = b |
|                                                                                                                                        | Non égal à | Float1 / Entier1 | Booléen | Renvoie true si un != b |
|                                                                                                                                        | Supérieur | Float1 / Entier1 | Booléen | Renvoie true (vrai) si a > b |
|                                                                                                                                        | Supérieur ou égal | Float1 / Entier1 | Booléen | Renvoie true (vrai) si a >= b |
|                                                                                                                                        | Inférieur | Float1 / Entier1 | Booléen | Renvoie true si a &lt; b |
|                                                                                                                                        | Inférieur ou égal | Float1 / Entier1 | Booléen | Renvoie true (vrai) si a &lt;= b |
| Fonction | Absolu | Float1 / Entier1 | Float1 | Renvoie la valeur absolue de a : abs(a) |
|                                                                                                                                        | Arrondi à l’inférieur | Float1 / Entier1 | Float1 | Renvoie la valeur la plus élevée inférieure ou égale à a : floor(a) |
|                                                                                                                                        | Ceil | Float1 / Entier1 | Float1 | Renvoie la plus petite valeur supérieure ou égale à a : ceil(a) |
|                                                                                                                                        | Cosinus | Float1 / Entier1 | Float1 | Renvoie la valeur cosinus de a : cos(a) |
|                                                                                                                                        | Sinus | Float1 / Entier1 | Float1 | Renvoie la valeur sinus de a : sin(a) |
|                                                                                                                                        | Tangente | Float1 / Entier1 | Float1 | Renvoie la valeur tangente de a : tan(a) |
|                                                                                                                                        | Arc tangente 2 | Vecteur flottant2 | Float1 | Renvoie la valeur de l’arc tan2 d’une entrée vector2 : arctan2(xa, ya) |
|                                                                                                                                        | Cartésien | Float1 | Flottant2 | Convertit 2 coordonnées polaires en coordonnées cartésiennes : carth(rho, theta) |
|                                                                                                                                        | Racine carrée | Float1 / Entier1 | Float1 | Renvoie la valeur de racine carrée d&#39;un |
|                                                                                                                                        | Logarithmique | Float1 / Entier1 | Float1 | Renvoie la valeur logarithmique de a : log(a) |
|                                                                                                                                        | Exponentiel | Float1 / Entier1 | Float1 | Renvoie la valeur exponentielle de a : exp(a) |
|                                                                                                                                        | Pow 2 | Float1 / Entier1 | Float1 | Renvoie la puissance de la valeur 2 d’un |
|                                                                                                                                        | Interpolation linéaire | Float1 / Entier1 | Float1 | Renvoie l’interpolation linéaire entre 2 valeurs, selon une valeur flottante : (1-x)a + x \* b |
|                                                                                                                                        | Minimum | Float1 / Entier1 | Type de a et b | Renvoie la valeur minimale entre a et b |
|                                                                                                                                        | Maximum | Float1 / Entier1 | Type de a et b | Renvoie la valeur maximale comprise entre a et b |
| Aléatoire |                       | Float1 | Float1 | Génère une valeur flottante comprise entre 0 et a |
| [Contrôle](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Séquence | tout | Type d’entrée | Permet de choisir la valeur à calculer en premier entre 2 valeurs. |
|                                                                                                                                        | If...Else | Booléen / a et b | Type de a et b | Renvoie true (vrai) si la condition dans If est true (vrai). Renvoie la valeur false si elle est false. |
