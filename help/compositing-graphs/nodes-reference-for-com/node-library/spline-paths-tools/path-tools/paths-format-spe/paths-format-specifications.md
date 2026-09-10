---
helpx_url: "https://helpx.adobe.com/fr/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: Découvrez les spécifications de format des tracés et la structure des données utilisées par les nœuds de tracé et de spline.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spécifications de format des tracés
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# Spécifications de format des tracés

Cette page décrit le format Tracés et fournit des instructions sur la manipulation des données dans ce format à l’aide des fonctions incluses dans les outils Tracés.

## Spécifications de format

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Cette section explique comment un document <b>Chemins d&#39;accès</b> (ou une image) est codé :

Un document Tracés est une liste de tracés, chacun décrivant une liste de segments, codés dans une <b>texture de couleur 32 bits à virgule flottante</b>.

La texture est divisée en parties « supérieure » (*$pos.y &lt; 0.5*) et « inférieure » (*$pos.y > 0.5*).

Toutes les données d&#39;un pixel dans la partie &#39;supérieure&#39; sont sémantiquement étroitement liées au pixel correspondant dans la partie &#39;inférieure&#39;, et vice-versa.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Tracés de données codées en polygone](paths-format-specifications.resources/PathsPolygon_Data.jpg "Tracés de données codées en polygone")

</td>
</tr>
</table>

>[!NOTE]
>
> Les données de tracés nécessitent une précision de 32 bits et une résolution inférieure produira des résultats incorrects.
> 
> Par conséquent, assurez-vous de définir le paramètre « Format de sortie » des nœuds générant des données de chemins sur « Haute précision HDR (32F) ».

Soit `*uv\_pos*` une adresse 2D (telle que *$pos*) d&#39;un pixel de la partie supérieure.

Dans la suite de ce document :

* <b>top[uv\_pos].XYZW</b> fera référence aux 4 flotteurs stockés dans le pixel de la partie supérieure.\
  top[uv\_pos] == sample\_color(paths, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b> fera référence aux 4 flotteurs stockés dans le pixel correspondant de la partie inférieure.\
  bottom[uv\_pos] == sample\_color(paths, uv\_pos + Float2(0, 0.5))

top[uv\_pos] et bottom[uv\_pos] forment ensemble une unité sémantique U[uv\_pos] du document, composée de 8 flotteurs.

### En-tête de document

Chaque document Tracés commence par un en-tête de document. Il s&#39;agit de la toute première unité sémantique U[(0,0)]:

+++Haut
<b>X</b>

Le nombre de chemins (doit être un entier positif dans [0 ; 16777216]).

Si certains tracés sont vides, ils comptent toujours ici. Vous pouvez donc l’envisager comme un « nombre d’en-têtes de chemins à décoder ».

<b>YZ</b>

Taille de pixel de ce document (c&#39;est-à-dire exactement `Float2(1,1) / $size`).

Cela est utile lors de la lecture des tracés à partir d&#39;un [processeur de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) ou d&#39;un [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), par exemple, dont la taille de sortie est différente.

<b>W</b>

1/16 = 0,0625 (indicateur d&#39;en-tête)

+++

+++Bas
<b>XY</b>

Adresse du dernier sommet défini dans ce document. Ceci est utile pour ajouter de nouvelles données.

Il peut donc s&#39;agir en fait de toute adresse supérieure (par ordre de lignes de balayage) à l&#39;adresse du dernier sommet. Il doit être compris entre &rbrack;0, 1[×]0,.5&lbrack;

<b>ZW</b>

Inutilisé, doit être Float2(0, 1)

+++

### En-têtes de tracé

L’en-tête du document est immédiatement suivi de number-of-paths = top[(0,0)].X path-headers, one by semantic unit.\
E.g. s’il y a 3 tracés dans le document, ils seront stockés en U[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size] et U[(0,3)\*pixel\_size] (avec pixel\_size = top[(0,0)].YZ).

S’il y a plus de tracés que ce qu’une ligne de pixels peut contenir, les en-têtes de tracé restants sont écrits sur la ou les lignes suivantes, dans l’ordre des lignes de numérisation.\
Il est autorisé d&#39;avoir des en-têtes de chemin d&#39;accès nuls (`top[...].XYZW = Float4(0,0,0,0)`) ; un tel chemin d&#39;accès peut toujours être vide.

L&#39;en-tête de chemin du Nième chemin sera défini à l&#39;adresse `path\_addr` comme :

+++Haut
<b>X</b>

Nombre de sommets dans ce tracé. Doit être compris dans la plage [0, 16777216].

Si les sommets de début et de fin d’un tracé fermé se trouvent à la même position, ils comptent toujours pour 2 sommets.\
Un tracé avec 0 sommet est un tracé valide.

<b>Y</b>

Indicateur *Est\_fermé* : 1 si le tracé est fermé (par exemple, un cercle), 0 dans le cas contraire (par exemple, une ligne droite).

<b>Z</b>

L&#39;index de chemin *N.* Il doit absolument correspondre à *path\_addr* (voir remarque ci-dessous).

<b>W</b>

Indicateur d’en-tête : 1/16 = 0,0625.

+++

+++Bas
<b>XY</b>

Adresse de début (ou de premier) sommet.

<b>ZW</b>

Adresse de fin (ou de dernier) sommet.

+++

>[!NOTE]
>
> Vous pouvez calculer `path\_addr` à partir de N à l&#39;aide de la fonction `Utils/pixel\_index\_to\_position` dans paths\_tools.sbs : `path\_addr = pixel\_index\_to\_position(N+1)`

### Informations sur les sommets

Les sommets se trouvent n’importe où dans l’image après les en-têtes (en-têtes de document ou de tracé). Les sommets peuvent être de différents « types » (Début, Milieu ou Fin) et ils sont explicitement liés entre eux à l’aide de 2 pointeurs d’adresse (« liens »).

Les sommets <b>Début</b> et <b>Fin</b> sont spéciaux à cet égard : pour permettre la représentation de tracés fermés ou d&#39;un réseau arbitraire de tracés liés entre eux, l&#39;un des liens est en fait utilisé pour former une liste circulaire avant liée de tous les autres sommets Début ou Fin qui représentent le même sommet. Ces sommets correspondants sont appelés « frères ». [Illustration accueillie]

Formellement, chaque sommet à l&#39;adresse `*vert\_addr*` est défini comme ceci :

+++Haut
<b>XY</b>

Position du sommet. Les coordonnées peuvent être n&#39;importe quelle valeur flottante autre que NaN ou ±inf. Il n&#39;y a pas de notion de carrelage à ce niveau (il peut être géré ou non par la mise en œuvre de chaque filtre), donc les chemins sont supposés être définis sur le plan euclidien.

<b>Z</b>

Index de tracé de sommet. Un sommet ne peut appartenir qu’à un seul tracé. (Comme mentionné précédemment, les sommets de début et de fin peuvent toutefois avoir des frères.) L’index de chemin peut être utilisé pour récupérer l’en-tête de chemin (voir la section En-têtes de chemin de section ci-dessus). Assurez-vous donc qu’il est synchronisé.

<b>W</b>

type de vertex. Il est divisé entre le signe de la valeur et sa valeur absolue :

Sur la partie signe, une valeur de 0 signifierait qu&#39;il n&#39;y a pas de vertex ici en fait (tous les autres composants devraient également être 0). Une valeur négative signifie que le vertex est marqué comme un « coin » ; une valeur positive signifie que le vertex est « lisse ». Le vertex d’arrondi et le calque d’arrondi sont des attributs purs et isolés qui n’ont aucun impact ni aucune signification sur le codage des autres tracés.

Sur la partie valeur absolue, le type de pixel (Début, Milieu ou Fin) et un autre drapeau (trivial\_link) sont codés:

* *0.125* : vertex de fin (dernier vertex de la forme ; liens toujours non triviaux, voir ci-dessous)

* *0.25* : vertex de début (premier vertex de la forme ; liens toujours non triviaux, voir ci-dessous)

* *0.5* : vertex moyen avec des liens non triviaux

* *1* : milieu de vertex avec des liens insignifiants

Par « liens non triviaux », on entend le fait que les vertex précédent et suivant (dans la liste des vertex du tracé courant) sont stockés respectivement dans le pixel à gauche (vert\_addr-(0,pixel\_size)) et à droite (vert\_addr+(0,pixel\_size)), tandis que par « liens non triviaux », on entend qu&#39;au moins l&#39;un d&#39;entre eux est stocké ailleurs.

+++

+++Bas
Indépendamment de la « banalité » des liens, les valeurs fiables des liens sont stockées dans la partie inférieure :

<b>XY</b>

Adresse du vertex précédent de ce chemin. Pour les vertex de démarrage, cette option pointe vers le vertex apparenté suivant.\
si |top[vert\_addr].W| = 1, puis bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

Adresse du vertex suivant de ce chemin. Pour les vertex d’extrémité, cette option pointe vers le vertex apparenté suivant.\
si |top[vert\_addr].W| = 1, puis bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## Informations sur les chemins de lecture et d’écriture

Si vous souhaitez créer vos propres nœuds de traitement des tracés, vous disposez de plusieurs outils.

Les bases sont fournies par les nœuds [Processeur de Vertex de tracés](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md) et [Processeur de Vertex de tracés simple](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md), qui peuvent être utilisés de la même manière qu&#39;un [Processeur de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md).

Si vous avez besoin de fonctionnalités au-delà de ce que proposent les nœuds du processeur de sommets de tracés (plus de textures d’entrée, ou plus de sommets précédents ou suivants), la copie de l’implémentation de ce graphique peut être un bon point de départ (en supposant que vous remplacez le nœud <b>Get(« %perVertex »)</b> par votre traitement personnalisé).

Mais au cas où vous voudriez faire quelque chose de plus extraterrestre que d&#39;appliquer une fonction par sommet, voici une explication détaillée des outils que vous pouvez utiliser. Il s&#39;agit généralement de petites fonctions d&#39;assistant qui se trouvent dans le même package que les autres nœuds Chemins (*chemins\_tools.sbs)*. (Ces fonctions ne sont pas affichées dans le [<b>menu Bibliothèque</b>](../../../../../../interface/the-library/the-library.md) et le <b>menu Nœud</b>.)

### Fonctions de lecture

Sous le dossier `Read`, vous trouverez plusieurs de ces éléments, utiles pour collecter des informations sur les Chemins :

Certains peuvent vous donner des informations sur un pixel donné. Ils prennent tous la valeur Float4 échantillonnée dans la partie \*top\* comme entrée. Si vous regardez leur mise en œuvre, ils sont super-simples. Leur but est de donner plus de sens que de simples nœuds atomiques :

+++is_header
Vérifiez que la valeur actuellement échantillonnée est un en-tête de chemin d’accès ou de document.

+++

+++path_is_close
Vérifiez l’indicateur Is\_Closed (.Y) dans un en-tête de chemin. Il \*suppose que vous avez déjà vérifié qu&#39;il s&#39;agit d&#39;un chemin\* avec `is\_header` et que `current\_pixel\_is\_document\_header` a renvoyé la valeur false.

+++

+++is_vertex
Vérifier que la valeur échantillonnée courante est un sommet, c&#39;est-à-dire non un en-tête, ni un pixel vide.

+++

+++is_start_vertex
Vérifiez si une valeur \*échantillonnage de la partie supérieure\* est un sommet de départ (pas besoin de vérifier d&#39;abord `is\_vertex`).

+++

+++is_mid_vertex
Vérifiez si une valeur \*échantillonnage de la partie supérieure\* est un sommet qui n&#39;est pas un sommet de début ou de fin (pas besoin de vérifier d&#39;abord `is\_vertex`).

+++

+++is_end_vertex
Vérifiez si une valeur \*échantillonnage de la partie supérieure\* est un sommet de fin (pas besoin de vérifier d&#39;abord `is\_vertex`).

+++

+++is_segment_start
Abréviation de `is\_start\_vertex || is\_mid\_vertex`. Plus utile pour le traitement basé sur [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), pour traiter chaque segment au plus une fois.

+++

+++is_corner
Vérifiez l&#39;indicateur d&#39;angle du sommet (pas besoin de vérifier d&#39;abord `is\_vertex` : si la réponse est vraie, vous êtes sur un sommet à coup sûr). Rappelez-vous que cet indicateur n&#39;est pas encore pris en charge par les nœuds officiels.

+++

+++has_trivial_links
S&#39;il s&#39;agit d&#39;un sommet, indique si vous pouvez facilement déduire la position des sommets précédent et suivant sans échantillonner la partie inférieure. (Remarque : un non-sommet renvoie toujours la valeur false.)

Vous ne voulez probablement pas l&#39;utiliser directement, mais utilisez plutôt l&#39;une des fonctions `sample\_next\*` ou `sample\_prev\*`, qui s&#39;en occupent pour vous.

+++

+++sample_next, sample_prev
Compte tenu de la valeur échantillonnée de la partie supérieure `*sampled*` et de sa position `*sampled\_position*`, renvoie la valeur échantillonnée de la partie supérieure du sommet suivante (respectivement précédente) et définit une variable Float2 `*next\_sampled\_pos*` à la position (dans la partie supérieure) de ce voisin (c&#39;est-à-dire &lt;valeur renvoyée> = SampleColor(next\_sampl\_pos, image0)). `*input0PixSize*`doit être égal à la taille en pixels du tracé (top[(0,0)].YZ).

Si le pixel actuel (`*sampled*`) est un sommet <b>Début</b>, *sample\_prev* renvoie le prochain frère de ce sommet. De même s&#39;il s&#39;agit d&#39;un sommet <b>Fin</b>, *sample\_next* renvoie le prochain frère de ce sommet (c&#39;est-à-dire peut-être pas ce que vous voulez). Voir `*sample\_next\_advanced*` et `*sample\_prev\_advanced*` ci-dessous pour résoudre ce problème.

Veuillez noter que pour plus de simplicité, les informations sur les <b>chemins d&#39;accès sont supposées être stockées dans input0 !</b> En outre, contrairement à ce qu&#39;indique le document de la fonction, vous n&#39;avez pas besoin de déclarer préalablement `*next\_sampled\_pos*`. `*[out]next\_sampled\_pos*` est un paramètre fictif pour vous rappeler que cette deuxième « valeur renvoyée » existe.

Vous pouvez vérifier le `*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md), dans le paramètre Itérations du troisième nœud Itération, pour obtenir un exemple d&#39;utilisation.

![Cas d’utilisation minimal de sample_next](paths-format-specifications.resources/paths-spec_fxmap-sample-next_02.png "Cas d’utilisation minimal de sample_next")



![Cas d’utilisation de sample_next dans les chemins d’aperçu (path_trace)](paths-format-specifications.resources/paths-spec_fxmap-sample-next_01.png "Cas d’utilisation de sample_next dans les chemins d’aperçu (path_trace)")



+++

+++sample_next_advanced, sample_prev_advanced
Il est destiné à fonctionner sur des tracés fermés. Pour les tracés ouverts, le sommet de début ou de fin n’a pas de frère et, dans ce cas, les deux fonctions renvoient le même et seul voisin. Pour les sommets de début ou de fin avec plusieurs frères (Tracés connectés en tant que réseau), qui renvoie le sommet voisin du frère suivant dans la liste liée.

+++

### Fonctions &#39;Write&#39;

Sous le dossier `Write`, vous trouverez de petits assistants qui créent un fichier Float4 prêt à être écrit <b>par un [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>.

En effet, la [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) multiplie le RGB par Alpha avant de dessiner, de sorte que les valeurs réelles ne sont pas prémultipliées pour compenser. Si vous souhaitez utiliser ces fonctions, par exemple dans un [processeur de pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), nous vous recommandons de réappliquer la prémultiplication vous-même ou d&#39;écrire une version personnalisée (plus optimisée pour votre cas d&#39;utilisation et plus facile à utiliser).

+++document_header
Génère la partie supérieure de l’en-tête du document, en déclarant le nombre de chemins d’accès que vous fournissez.

+++

+++document_last_vertex_spec
Crée la partie \*bottom\* de l’en-tête du document, qui spécifie la dernière adresse de sommet (voir A.1).

+++

+++path_header
Crée la partie supérieure d&#39;un en-tête de tracé, en fonction du nombre de sommets du tracé `*nbVertices*`, de l&#39;indicateur `*isClosed*` et de l&#39;indicateur `*pathIndex*`.

+++

+++start_vertex, mid_vertex, end_vertex
Crée la partie supérieure d’un sommet, en définissant la position, le texte et d’autres options en conséquence.

À propos de *mid\_vertex* et du paramètre *hasTrivialLinks* : idéalement, vous devez définir la valeur appropriée, mais si, pour une raison quelconque, vous ne parvenez pas à dire si les liens seront triviaux ou non, vous pouvez la définir en toute sécurité sur false (au prix d’un traitement plus lent de votre chemin généré).

+++

Il n’existe pas de générateur de partie inférieure pour les en-têtes de tracé ou les sommets : les deux codent deux liens vers la partie supérieure, de sorte que cette fonction serait essentiellement un constructeur Vector Float4 de deux Float2. N&#39;oubliez pas de diviser XYZ par W si vous écrivez à l&#39;aide d&#39;une [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) (W étant le Y d&#39;une adresse, elle ne doit jamais être nulle).

Vous trouverez un exemple pertinent d&#39;utilisation de ces fonctions dans le package <b>*chemins\_polygon.sbs* </b>hébergeant le nœud [polygone des chemins](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md).

### Procédés de traitement de tracés

Vous utiliserez probablement un processeur de pixels ou un Fx-Map pour mettre en œuvre votre traitement personnalisé, chacun ayant ses forces et ses faiblesses :

+++FX-Map
La solution basée sur [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) sera généralement préférée lors de l&#39;exécution d&#39;opérations de haut niveau nécessitant une connaissance globale du (ou des) chemin(s) entier(s), ou cumulative(s) (par exemple, le reconditionnement des sommets après décimation ou facettisation). Il s&#39;agit également de l&#39;approche la plus simple. Par conséquent, si vous effectuez un traitement personnalisé pour la première fois, vous pouvez utiliser une Fx-Map, même si *est peut-être* plus lent.

Vous devez d’abord vous familiariser avec Fx-Map. Si ce n&#39;est pas le cas, consultez la [documentation spécifique](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md).

Nous vous recommandons d’examiner l’implémentation des [chemins d’aperçu](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) dans <b>*chemins\_trace.sbs*</b> et du [polygone des chemins](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md) dans <b>*chemins\_polygone.sbs*</b> pour vous faire une idée de la lecture et de l’écriture (respectivement) d’un chemin à l’aide d’une Fx-Map.

+++

+++Processeur de pixels
La solution de [processeur en pixels](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) conviendra si vous avez uniquement besoin d&#39;informations « locales ». Ici, nous voulons dire « local » non pas spatialement (la distance entre les éléments) mais plutôt topologiquement (les sommets liés entre eux). Voici comment le processeur de sommets est implémenté. Le processeur de pixels est généralement plus rapide que le Fx-Map pour ce type d&#39;opération, car la fonction de chaque pixel est évaluée en parallèle, alors que seule une quantité limitée de données est accessible. L’effort d’implémentation peut être beaucoup plus important, car vous ne pouvez modifier que le pixel actuel.

Nous n&#39;entrerons pas dans les détails, car il y a tant à dire en fonction de votre cas d&#39;utilisation spécifique, mais la première chose à faire est de vérifier où vous êtes :

Êtes-vous dans la partie supérieure ($pos.y &lt; 0,5) ou inférieure ($pos.y > 0,5) ? Nous vous recommandons de ne pas oublier que dans une variable dédiée (par exemple, `*isTop*`) et que vous créez un `*vert.addr*` Float2, cette valeur est `*$pos*` pour la partie supérieure et `$pos - (0,0.5)` pour la partie inférieure.

Qu&#39;en est-il à *vert.addr* ? Échantillonnez-le et vérifiez s&#39;il y a quelque chose (W != 0), puis, s&#39;il y en a, quoi exactement. Un en-tête (W = 0,0625) (cochez avec `*Read/is\_header*`) ou un sommet (cochez avec `Read/is\_vertex`) ? S’il s’agit d’un en-tête, est-ce l’en-tête du document ou un en-tête Chemin ? (Vous pouvez utiliser `*Read/current\_pixel\_is\_document\_header*` pour vérifier cela.) Utilisez une ou plusieurs des fonctions d’assistant pour faire correspondre ce qui vous intéresse.

+++
