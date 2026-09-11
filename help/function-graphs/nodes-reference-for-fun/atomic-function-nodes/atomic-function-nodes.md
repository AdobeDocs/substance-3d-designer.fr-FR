---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Découvrez les noeuds de fonction atomiques, les plus petites unités de nœud dans les graphes de fonction de Substance pour créer des fonctions personnalisées.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Noeuds de fonction atomiques
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 17%

---


# Noeuds de fonction atomiques

Comme pour les [noeuds atomiques dans les graphes de Substance](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), les noeuds atomiques dans les graphes de fonction de Substance sont les plus petites unités de nœud de ce type de graphe.

Ils peuvent être triés en plusieurs catégories selon leur objectif :

| Catégorie | Nœud | Type(s) d’entrée | Type de sortie | Description |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Constant](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Flottant | - | Flottant | Définit une valeur flottante constante, par exemple 0,1 |
|                                                                                                                                        | Flottant2 | - | Flottant2 | Définit un vecteur constant de 2 valeurs flottantes, par exemple (0,1, 0,2) |
|                                                                                                                                        | Flottant3 | - | Flottant3 | Définit un vecteur constant de 3 valeurs flottantes, par exemple (0,1, 0,2, 0,3) |
|                                                                                                                                        | Flottant4 | - | Flottant4 | Définit un vecteur constant de 4 valeurs flottantes, par exemple (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Entier | - | Entier | Définit une valeur d&#39;entier constante, par exemple 1 |
|                                                                                                                                        | Entier2 | - | Entier2 | Définit un vecteur constant de 2 valeurs d’entier, par exemple (1, 2) |
|                                                                                                                                        | Entier3 | - | Entier3 | Définit un vecteur constant de 3 valeurs d’entier, par exemple (1, 2, 3) |
|                                                                                                                                        | Entier4 | - | Entier4 | Définit un vecteur constant de 4 valeurs d’entier, par exemple (1, 2, 3 ,4) |
|                                                                                                                                        | Booléen | - | Booléen | Définit une valeur booléenne constante, par exemple True ou False |
|                                                                                                                                        | Chaîne | - | Chaîne | Définit une valeur constante de type String, par exemple « Substance » |
| [Vecteur](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vecteur flottant2 | FLOTTANT 1 | Flottant 2 | Convertit 2 valeurs flottantes dans un vecteur avec 2 coordonnées |
|                                                                                                                                        | Vecteur flottant3 | FLOTTANT 1 / FLOTTANT 2 | Flottant 3 | Convertit 2 valeurs flottantes dans un vecteur avec 3 coordonnées |
|                                                                                                                                        | Vecteur flottant4 | FLOTTANT 1 / 2 / 3 | Flottant 4 | Convertit 2 valeurs flottantes dans un vecteur de 4 coordonnées |
|                                                                                                                                        | Swizzle flottant1 | Vecteur flottant | FLOTTANT 1 | Extrait une coordonnée flottante d’un vecteur |
|                                                                                                                                        | Swizzle flottant2 | Vecteur flottant | Flottant2 | Extraction de 2 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Swizzle flottant3 | Vecteur flottant | Flottant3 | Extraction de 3 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Swizzle flottant4 | Vecteur flottant | Flottant4 | Extrait 4 coordonnées flottantes d’un vecteur |
|                                                                                                                                        | Vecteur entier2 | Entier2 | Vecteur entier2 | Convertit 2 valeurs d’entier dans un vecteur de 2 coordonnées |
|                                                                                                                                        | Vecteur entier3 | Entier3 | Entier3 | Convertit 2 valeurs d’entier dans un vecteur de 3 coordonnées |
|                                                                                                                                        | Vecteur entier4 | Entier4 | Entier4 | Convertit 2 valeurs d’entier dans un vecteur de 4 coordonnées |
|                                                                                                                                        | Swizzle entier1 | Entier vectoriel | ENTIER 1 | Extrait une coordonnée d’entier d’un vecteur |
|                                                                                                                                        | Swizzle entier2 | Entier vectoriel | Entier2 | Extrait les coordonnées de 2 entiers d’un vecteur |
|                                                                                                                                        | Swizzle entier3 | Entier vectoriel | Entier3 | Extraction de 3 coordonnées d’entier d’un vecteur |
|                                                                                                                                        | Swizzle entier4 | Entier vectoriel | Entier4 | Extrait 4 coordonnées d’entier d’un vecteur |
| [Variables](../../../function-graphs/variables/variables.md) | Définir | tout | type d’entrée | Définit une variable |
|                                                                                                                                        | Obtenir Entier 1 | - | ENTIER 1 | Obtenir une entrée de valeur d&#39;Entier de fonction ou de graphe |
|                                                                                                                                        | Obtenir entier2 | - | Entier2 | Obtenir une entrée de valeur Entier 2 de fonction ou de graphe |
|                                                                                                                                        | Obtenir entier3 | - | Entier3 | Obtenir une entrée de valeur Entier 3 de fonction ou de graphe |
|                                                                                                                                        | Obtenir entier4 | - | Entier4 | Obtenir une entrée de valeur Entier 4 de fonction ou de graphe |
|                                                                                                                                        | Obtenir Flottant 1 | - | FLOTTANT 1 | Obtenir une entrée de valeur flottante de fonction ou de graphe |
|                                                                                                                                        | Obtenir flottant2 | - | Flottant2 | Obtenir une entrée de valeur Flottant 2 de fonction ou de graphe |
|                                                                                                                                        | Obtenir Flottant3 | - | Flottant3 | Obtenir une entrée de valeur Flottant 3 de fonction ou de graphe |
|                                                                                                                                        | Obtenir flottant4 | - | Flottant4 | Obtenir une entrée de valeur Flottant 4 de fonction ou de graphe |
|                                                                                                                                        | Obtenir booléen | - | Booléen | Obtenir une entrée de valeur booléenne de fonction ou de graphe |
| Échantillonnages | Échantillon gris | Vecteur flottant2 | Flottant4 | Renvoie la valeur de niveaux de gris d’une image d&#39;entrée aux coordonnées UV données (float2) |
|                                                                                                                                        | Échantillon de couleur | Vecteur flottant2 | Flottant4 | Renvoie la valeur chromatique d’une image d&#39;entrée aux coordonnées UV données (float2) |
| Convertir | Vers Flottant | ENTIER 1 | FLOTTANT 1 | Convertit un entier en objet flottant |
|                                                                                                                                        | Vers flottant2 | Entier2 | Flottant2 | Convertit un Entier 2 dans un Flottant 2 |
|                                                                                                                                        | Vers flottant3 | Entier3 | Flottant3 | Convertit un Entier 3 dans un Flottant 3 |
|                                                                                                                                        | Vers flottant4 | Entier4 | Flottant4 | Convertit un Entier 4 dans un Flottant 4 |
|                                                                                                                                        | Vers entier | FLOTTANT 1 | ENTIER 1 | Convertit un Flottant dans un Entier |
|                                                                                                                                        | Vers entier2 | Flottant2 | Entier2 | Convertit un Flottant 2 dans un Entier 2 |
|                                                                                                                                        | Vers entier3 | Flottant3 | Entier3 | Convertit un Flottant 3 dans un Entier 3 |
|                                                                                                                                        | Vers entier4 | Flottant4 | Entier4 | Convertit un Flottant 4 dans un Entier 4 |
| [Opérateur](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Addition | Vecteur flottant/Entier | Type de a et b | Ajoute 2 valeurs du même type : a + b |
|                                                                                                                                        | Soustraction | Vecteur flottant/Entier | Type de a et b | Soustrait 2 valeurs du même type : a - b |
|                                                                                                                                        | Multiplication | Vecteur flottant/Entier | Type de a et b | Multiplie 2 valeurs du même type : a \* b |
|                                                                                                                                        | Multiplication scalaire | Vecteur flottant | Type de | Multiplie une valeur par une valeur flottante : un scalaire \* |
|                                                                                                                                        | Division | FLOTTANT 1 / ENTIER 1 | Type de a et b | Divise 2 valeurs du même type : a / b |
|                                                                                                                                        | Négation | FLOTTANT 1 / ENTIER 1 | Type de | Renvoie la valeur négative : -a |
|                                                                                                                                        | Modulo | FLOTTANT 1 / ENTIER 1 | Type de | Renvoie la valeur par modulo : mod(a, diviseur) |
|                                                                                                                                        | Produit scalaire | Vecteur flottant | Type de a et b | Renvoie le produit de 2 valeurs du même type : dot(a, b) |
| [Logique](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | Et | Booléen | Booléen | Renvoie true (vrai) si les 2 entrées booléennes sont true (vrai). Renvoie la valeur false si l&#39;une des entrées est false. |
|                                                                                                                                        | Ou | Booléen | Booléen | Renvoie true (vrai) si 1 des entrées booléennes est true (vrai). Renvoie la valeur false dans les deux cas. |
|                                                                                                                                        | Non | Booléen | Booléen | Renvoie le booléen de négation de l&#39;entrée : !a |
| [Comparaison](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Égal à | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true (vrai) si a = b |
|                                                                                                                                        | Non égal à | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true si un != b |
|                                                                                                                                        | Supérieur | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true (vrai) si a > b |
|                                                                                                                                        | Supérieur ou égal | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true (vrai) si a >= b |
|                                                                                                                                        | Inférieur | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true si a &lt; b |
|                                                                                                                                        | Inférieur ou égal | FLOTTANT 1 / ENTIER 1 | Booléen | Renvoie true (vrai) si a &lt;= b |
| Fonction | Absolu | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur absolue de a : abs(a) |
|                                                                                                                                        | Arrondi à l’inférieur | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur la plus élevée inférieure ou égale à a : floor(a) |
|                                                                                                                                        | Ceil | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la plus petite valeur supérieure ou égale à a : ceil(a) |
|                                                                                                                                        | Cosinus | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur cosinus de a : cos(a) |
|                                                                                                                                        | Sinus | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur sinus de a : sin(a) |
|                                                                                                                                        | Tangente | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur de tangente de a : tan(a) |
|                                                                                                                                        | Arc tangente 2 | Vecteur flottant2 | FLOTTANT 1 | Renvoie la valeur de l’arc tan2 d’une entrée vector2 : arctan2(xa, ya) |
|                                                                                                                                        | Cartésien | FLOTTANT 1 | Flottant2 | Convertit 2 coordonnées polaires en coordonnées cartésiennes : carth(rho, theta) |
|                                                                                                                                        | Racine carrée | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur de racine carrée d&#39;un |
|                                                                                                                                        | Logarithmique | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur logarithmique de a : log(a) |
|                                                                                                                                        | Exponentiel | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la valeur exponentielle de a : exp(a) |
|                                                                                                                                        | Pow 2 | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie la puissance de la valeur 2 d’un |
|                                                                                                                                        | Interpolation linéaire | FLOTTANT 1 / ENTIER 1 | FLOTTANT 1 | Renvoie l’interpolation linéaire entre 2 valeurs, selon une valeur flottante : (1-x)a + x \* b |
|                                                                                                                                        | Minimum | FLOTTANT 1 / ENTIER 1 | Type de a et b | Renvoie la valeur minimale entre a et b |
|                                                                                                                                        | Maximum | FLOTTANT 1 / ENTIER 1 | Type de a et b | Renvoie la valeur maximale comprise entre a et b |
| Aléatoire |                       | FLOTTANT 1 | FLOTTANT 1 | Génère une valeur flottante comprise entre 0 et a |
| [Contrôle](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Séquence | tout | Type d’entrée | Permet de choisir la valeur à calculer en premier entre 2 valeurs. |
|                                                                                                                                        | If...Else | Booléen / a et b | Type de a et b | Renvoie true (vrai) si la condition dans If est true (vrai). Renvoie la valeur false si elle est false. |
