---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Accédez aux noeuds de fonction dans les graphes de fonction Substance 3D Designer pour appeler et exécuter des graphes de fonction personnalisés.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fonction
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Nœuds de fonction

Les noeuds de fonction transforment la valeur d’entrée en fonction de la fonction mathématique qu’ils représentent.

Bien que leurs connecteurs d’entrée ne soient généralement pas typés, ils ne prennent pas en charge tous les types valeur.

## Liste des nœuds

+++Pow
![Icône de nœud Pow](function-nodes.resources/Pow_Node.jpg "Icône de nœud Pow")



Retourne la première entrée élevée à la puissance de la deuxième entrée : <b>X^Y</b>.

+++

+++2Pow
![Icône de 2nœud Pow](function-nodes.resources/2Pow_Node.jpg "Icône de 2nœud Pow")



Renvoie 2 à la puissance de sa valeur d&#39;entrée : <b>2^X</b>.

+++

+++Racine carrée
![Icône de nœud racine carrée](function-nodes.resources/SquareRoot_Node.jpg "Icône de nœud racine carrée")



Renvoie la racine carrée de sa valeur d&#39;entrée : <b>√X</b>.

+++

+++Exponentiel
![Icône de nœud exponentiel](function-nodes.resources/Exponential_Node.jpg "Icône de nœud exponentiel")



Renvoie la valeur exponentielle de sa valeur d&#39;entrée : <b>e^X</b>

<b>e</b> est approximativement égal à 2,7182818.

+++

+++Logarithme
![Icône de nœud de logarithme](function-nodes.resources/Logarithm_Node.jpg "Icône de nœud de logarithme")



Renvoie le logarithme naturel de sa valeur d&#39;entrée : <b>ln(X)</b>.

+++

+++Logarithme base 2
Icône ![Logarithme de base 2 de nœud](function-nodes.resources/LogarithmBase2_Node.jpg "Logarithme de base 2 de nœud")



Renvoie le logarithme de base 2 de sa valeur d&#39;entrée : <b>log2(X)</b>.

+++

+++Absolu
![Icône de nœud absolu](function-nodes.resources/Absolute_Node.jpg "Icône de nœud absolu")



Retourne la valeur absolue de son entrée : <b>abs(X)</b>.

+++

+++Ceil
![Icône de nœud de cellule](function-nodes.resources/Ceil_Node.jpg "Icône de nœud de cellule")



Arrondit sa valeur d’entrée à une valeur supérieure. Elle renvoie la plus petite valeur d&#39;entier non inférieure à X : <b>ceil(X)</b>.

+++

+++Arrondi à l’inférieur
![icône de nœud d&#39;Arrondi aux inférieurs](function-nodes.resources/Floor_Node.jpg "icône de nœud d&#39;Arrondi aux inférieurs")



Arrondit sa valeur d’entrée vers le bas. Elle renvoie la plus grande valeur d&#39;entier ne dépassant pas X : <b>floor(X)</b>.

+++

+++Interpolation linéaire
![icône de nœud d&#39;Interpolation linéaire](function-nodes.resources/LinearInterpolation_Node.jpg "icône de nœud d&#39;Interpolation linéaire")



Renvoie l&#39;interpolation linéaire entre deux valeurs en fonction d&#39;une valeur flottante : <b>(1 - X)\*A + X\*B</b>.

+++

+++Minimum
![Icône de nœud minimale](function-nodes.resources/Minimum_Node.jpg "Icône de nœud minimale")



Renvoie la plus faible des deux valeurs d&#39;entrée : <b>min(A, B)</b>.

+++

+++Maximum
![Icône de nœud maximale](function-nodes.resources/Maximum_Node.jpg "Icône de nœud maximale")



Renvoie la plus élevée des deux valeurs d&#39;entrée : <b>max(A, B)</b>.

+++

+++Cosinus
![Icône de nœud cosinus](function-nodes.resources/Cosine_Node.jpg "Icône de nœud cosinus")



Renvoie le cosinus de sa valeur d&#39;entrée en radians : <b>cos(X)</b>.

+++

+++Sinus
![Icône de nœud sinus](function-nodes.resources/Sine_Node.jpg "Icône de nœud sinus")



Renvoie le sinus de sa valeur d&#39;entrée en radians : <b>sin(X)</b>.

+++

+++Tangente
![Icône de nœud de Tangente](function-nodes.resources/Tangent_Node.jpg "Icône de nœud de Tangente")



Renvoie la tangente de sa valeur d&#39;entrée en radians : <b>tan(X)</b>.

+++

+++Arc tangente 2
Icône de nœud ![Arc tangente 2](function-nodes.resources/ArcTangent2_Node.jpg "Arc tangente 2")



Renvoie l’angle entre le vecteur 2D d’entrée et l’horizontale.

C&#39;est l&#39;inverse de la fonction <b>Cartésien</b>.

Il n&#39;est pas nécessaire de permuter les composantes X et Y du vecteur d&#39;entrée comme dans la fonction <b>atan2</b> habituelle.

+++

+++Cartésien
![Icône de nœud absolu](function-nodes.resources/Absolute_Node.jpg "Icône de nœud absolu")



Convertit les coordonnées polaires en coordonnées cartésiennes.

Il s&#39;agit de l&#39;inverse de la fonction <b>tangente d&#39;arc 2 </b> : <b>Longueur \* Flottant 2(cos(Angle), sin(Angle).</b>

Les coordonnées polaires sont une distance depuis l’origine et un angle en radians depuis l’horizontale.

+++

+++Aléatoire
![Icône de nœud aléatoire](function-nodes.resources/Random_Node.jpg "Icône de nœud aléatoire")



Renvoie une valeur aléatoire comprise entre 0 et la valeur d&#39;entrée <b>X</b>.

+++
