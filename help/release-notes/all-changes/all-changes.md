---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/all-changes.html"
breadcrumb-title: ''
description: Passez en revue toutes les modifications et mises à jour des versions de Substance 3D Designer pour suivre l’évolution et les améliorations des fonctionnalités.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > All changes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Toutes les modifications
user-guide-description: ''
user-guide-title: ''
source-git-commit: 470ce4ff25b81c710c4b446b160c29663c31d356
workflow-type: tm+mt
source-wordcount: '32107'
ht-degree: 0%

---


# Toutes les modifications

## Version 16

### 16.0.6

*(Publié le 4 septembre 2026)*

**Fixe :**

* [Stabilité] Correction d’un crash lors de la fermeture de l’application lors de la compilation des shaders
* [Stabilité] Correction d’un crash lors de l’exportation d’une image vers un chemin contenant des caractères non ASCII
* [Sécurité] Correction d’une vulnérabilité de lecture hors limites dans l’analyse des fichiers TGA.
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de fichier de TIFF
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de fichier TGA

### 16.0.5

*(Publié le 26 août 2026)*

**Ajouté :**

* [vue 3D] Ajout d’un bouton pour sélectionner l’AOV actif
* [Contenu] bruit Perlin/gaussien : paramètre d’échelle unclamp
* [Contenu] Masquer les ressources bitmap inutiles de la bibliothèque
<!--
* &#91;Legal&#93; To meet generative AI transparency legal requirements, this version is updated to automatically attach Content Credentials to qualifying content created or edited with generative AI tools.  
-->

**Fixe :**

* [vue 3D] Les modifications de visibilité de l’environnement effectuées dans OpenGL ne sont pas répercutées dans les rendus Eclair
* [Baker] Le contexte de Baking n&#39;a pas été détruit après l&#39;actualisation des bakes pour une ressource bitmap UDIM supprimée
* [Baker] Correction d’un crash lors de la suppression d’une ressource bitmap UDIM lors de l’actualisation de ses bakes
* [Contenu] Éclaboussure de forme v2 : l’height de forme du cylindre n’est pas correct
* [Contenu] Éclaboussure de forme v2 : la map density ne fonctionne pas correctement lorsque la taille du nœud dépasse 4 096
* [Contenu] Éclaboussure de forme v2 : l’utilisation du fichier SDF « Rock » derrière un If/Else peut entraîner une boucle infinie
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de Fichier AxF
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de fichiers GLB
* [Sécurité] Correction des vulnérabilités d’écriture hors limites dans l’analyse de Fichier sbsar
* [Sécurité] Correction d’une vulnérabilité de corruption de segment de mémoire dans l’analyse de fichier DDS
* [Sécurité] Correction d’une vulnérabilité de corruption du tas dans l’analyse de fichiers GLB
* [Sécurité] Correction d’une vulnérabilité de corruption de segment de mémoire dans l’analyse du fichier TGA
* [Sécurité] Correction d’une vulnérabilité de corruption de segment de mémoire dans l’analyse de fichier de TIFF
* [Sécurité] Correction d’une vulnérabilité de corruption de segment de mémoire dans l’analyse de fichiers USDA
* [Sécurité] Correction d’une vulnérabilité de corruption de tas dans l’analyse de fichiers WEBP
* [UI] La liste des éléments des menus à cocher persistants ne s&#39;étend que sur le texte de l&#39;élément


### 16.0.4

*(Publié le 2 juillet 2026)*

**Ajouté :**

* [vue 3D] Verrouillez la résolution de rendu sur 4 096 dans X et Y
* [Baker] Mise à jour du kit de développement baker vers la version 3.22.3
* [Moteur] Mettre à jour le moteur de Substance vers la version 9.4.4
* [OpenGL][OpenPBR] Réduction du bruit dans le lobe de specular pour une rugosité élevée + anisotropie
* [Scènes] Conserver le mode d’interpolation UV primvar

**Fixe :**

* [vue 3D] Exportation USD : les chemins des ressources sont stockés avec un chemin absolu
* [Baker] Échec de Baker lorsque le chargement de maillage high poly est annulé (Windows)
* [Bakers] La liste des scènes 3D à poly élevé n’inclut pas les ressources ayant le même identifiant que le poly faible
* [Bakers] espace monde normal : une normale WS est toujours retournée lorsqu&#39;il y a une normale d&#39;entrée
* [Contenu] Normale incorrecte lors de la mise à l’échelle non uniforme du motif dans l’éclaboussure de forme V2
* [Contenu] Éclaboussure de forme V2 : normales noires pour les formes « Plan » et « Disque »
* [Contenu] Éclaboussure de forme v2 : la première forme n’est pas correctement fusionnée avec l’arrière-plan
* [Crash] crash aléatoire éventuellement lié à la vidéo (info-bulles riches)
* [Graphe] Crash lors du collage d&#39;un nœud copié à partir d&#39;un nouveau graphe avec un identifiant vide
* [PSD] Les fichiers de PSD sont chargés trop de fois

### 16.0.3

*(Publié Le 29 Mai 2026)*

**Fixe :**

* [Crash] Correction d’une régression introduite dans la version 16.0.2 entraînant un crash au lancement pour certains utilisateurs

### 16.0.2

*(Publié Le 28 Mai 2026)*

**Ajouté :**

* [OpenPBR] Prise en charge des constantes Base color/AO

**Fixe :**

* [vue 3D] Fuite de VRAM dans le traceur de chemin GPU lorsque le displacement est activé
* [vue 3D] Le thread principal reste occupé lorsque la vue 3D existe
* [vue 3D][OpenPBR] OpenGL : les widgets de poids semblent être bridés, mais acceptent des valeurs hors plage
* [Crash] Crash lors du déplacement d’une entrée référencée à plusieurs endroits à la fois
* [Crash] Crash lors de l’agrandissement d’une fenêtre
* [Crash] Crash lors de l’écriture de TARGA ou BMP à partir du baker
* [Crash] crash aléatoire lors de l’affichage de la vue 3D
* [Graphe] Ordre incorrect des épingles E/S lors du déplacement des E/S après la modification des identifiants
* [Linux][Exporter] Les boîtes de dialogue « Publish sbsar » et « Envoyer à » n’ajoutent pas d’extension de fichier

### 16.0.1

*(Publié Le 5 Mai 2026)*

**Ajouté :**

* [Échantillons] Ajoutez un échantillon de Matériau dédié à SDF / Shape Splatter
* Visionneuse 3D [Contenu] : modification de l’état par défaut
* [Contenu] Visionneuse 3D : ajout d’un environnement par défaut
* [Contenu] Mappeur de forme v2 : ajout d’un paramètre de centre de projection par axe pour le mappage triplanaire
* [Content] Mappeur d&#39;éclaboussures de forme v2 : paramètre Ajouter une répétition
* [Contenu] Éclaboussure de forme v2 : active l’extrusion de forme par défaut
* [3DView] Prise en charge des GPU Intel Panther Lake dans le traceur
* [vue 3D] Amélioration de la mise en forme des info-bulles contextuelles Displacement
* [Moteur] Mise à jour vers la Substance Engine v9.4.3
* [OpenPBR] geometry_tangente : prise en charge des constantes
* [Préférences] Ajoutez une option pour TGA/BMP pour écrire le canal Alpha s’il est entièrement opaque
* [Tiers] Mise à jour vers « Adobe Color Engine » (ACE) 7.0
* [UI] Rendre la fenêtre du gestionnaire de plug-ins toujours visible (modale)

**Fixe :**

* [vue 3D] La mise à l’échelle par Viewport est appliquée lors de l’utilisation d’une résolution fixe
* [vue 3D][OpenPBR] Blocage lors du chargement d’une scène GLTF exportée depuis Designer et de l’utilisation d’un matériau
* [vue 3D][OpenPBR] Les Matériaux exportés depuis Painter ne peuvent pas être remplacés dans Designer
* [Contenu] Visionneuse 3D : shape.id n’est pas initialisé et génère des messages dans la console
* [Contenu] Mappeur d’éclaboussures de forme v2 en niveaux de gris : l’entrée de motif 4 n’est pas utilisée dans la projection triplanaire
* [Contenu] Mappeur v2 d’éclaboussures de forme : l’ID SDF est décalé de -1 lors de l’utilisation du mode « 1 image par ID de matériau »
* [Eclair][USD] résultat incorrect lors de l’application d’un matériau sur un USD généré par Designer
* [Moteur] Calcul d&#39;un nouveau nœud Niveaux Forme éclaboussure graphe principal V2 brouillé calculs suivants
* [Moteur] Le Modulo d’une variable par rapport à sa valeur égale ne renvoie pas 0 avec le moteur GPU dans certains cas
* [Moteur][Contenu] Arc tangente 2 renvoie 0 ou Pi pour les vecteurs X-right dans un cas spécifique
* [Moteur][Ubuntu][SSE2] Crash lors du chargement de SBSAR spécifiques dans le graphe
* [Graphe] Crash lors de la connexion de la sortie du Processeur de valeurs en entrée bitmap
* [Graphe] Crash lors du branchement de la valeur dans l’entrée d’image dans certains cas
* [Graphe] Le Graphe est automatiquement calculé à chaque enregistrement automatique lors de l&#39;utilisation des maps bakées
* [GraphRender] Crash lors de la connexion d’une sortie de valeur d’Atlas scatter à une entrée d’image d’Atlas splitter
* [Linux][Exporter] Le format de fichier modifié est ignoré dans les boîtes de dialogue d’enregistrement de fichier
* [Mac][Steam] Une fenêtre contextuelle de sécurité s’affiche lorsque nous démarrons Designer
* [Maillage] Les matériaux OBJ ne sont pas importés correctement
* [PSD] L’importateur de PSDS demande d’extraire des calques du fichier PSD à chaque enregistrement automatique

### 16.0.0

*(Publié Le 14 Avril 2026)*

**Ajouté :**

* [Contenu] Nœud Shape splatter v2
* [Contenu] Nœuds de couleur/niveaux de gris du mappeur d’éclaboussures de forme v2
* [Contenu] Éclaboussure de forme v2 sur le nœud de masque
* Nœuds d&#39;Atlas en grille [Contenu]
* [Contenu] Nœud de la visionneuse 3D
* [Content] Nœuds de l&#39;opérateur 3D SDF
* [Content] Nœuds primitifs 3D SDF
* [Content] Nœuds de transforme 3D SDF
* [Content] Nœuds de matériau 3D SDF
* [Contenu] Nœud d’angle par rapport au vecteur
* [Content] Nœuds à valeur constante
* [vue 3D] OpenPBR pour le moteur de rendu OpenGL
* [vue 3D] OpenPBR pour la pixellisation et les systèmes de rendu de Pathtracer GPU
* Fenêtre de Displacement [vue 3D] pour définir l’échelle d’height, le niveau d’height et la tessellation
* [vue 3D] Réorganisation des éléments de la barre d’outils
* [vue 3D] Définir OpenPBR comme modèle de matériau par défaut dans vue 3D
* [vue 3D] Demander à la vue 3D de prendre en compte l’attribut de graphe « Modèle de matériau »
* [vue 3D] Synchronisation des modèles de matériau lors du basculement entre les modes de rendu Pixellisation/Pathtracer GPU et OpenGL
* [vue 3D] Assurez-vous que le modèle de matériau est persistant lors de la synchronisation des changements de rendu 3D et des modifications de définition de matériau
* [vue 3D] Pathtracer GPU : activer le cycle de pixels bruit bleu
* [vue 3D] Exposer le contrôle d’opacité Ambient occlusion
* [vue 3D] Définissez la plage de paramètres « Répétition » sur [0, 10] pour tous les shaders
* [vue 3D] Renommez l’action « Focus » en « Cadre ».
* [vue 3D] Gère le nouveau paramètre refineLevel qui remplace tessellationFactor
* [vue 3D] Ajouter un compteur IPS
* [vue 3D] Déplacez la barre de progression dans la même barre d’outils horizontale que l’espace colorimétrique en bas
* [Bakers] Afficher l’UV du baker sélectionné dans l’aperçu
* [Graphe] Ajouter un nouvel attribut « Modèle de matériau » aux graphes de Substance
* [NewGraph] Ajout de séparateurs dans la vue Miniatures
* [Paramètres] Définissez la valeur constante par défaut pour les paramètres d&#39;entrée avec l’éditeur « Function ».
* [Paramètres] Remplir la zone de liste déroulante de `Set` et `Is defined` paramètres de nœud avec des variables disponibles
* [Préférences] Supprimer l’option obsolète « Facteur de mise à l’échelle » dans l’onglet « vue 3D »
* Boîte de dialogue Publish de [Publish] : inclure le modèle de matériau dans les informations de graphe
* [Python] Ajoutez une nouvelle classe SDMaterialModelDescription pour obtenir les informations d&#39;un modèle de matériau
* [Python] Autoriser à obtenir/définir la propriété de modèle de matériau des objets SDSBSCompGraph
* [Éditeur Python] Augmentez la taille de la police à 12
* [Modèles] Ajouter des modèles d’OpenPBR
* [Modèles] Convertir des échantillons de matériau en OpenPBR
* [Tiers] Mise à jour de Boost vers la version 1.88
* [Tiers] Mise à jour de l’API C++ vers C++20
* [ThirdParty] Mettre à jour NGL vers 1.42
* [ThirdParty] Mise à jour oneTBB vers la version 2022.x
* [Tiers] Mise à jour d’OpenColorIO vers la version 2.5.x
* [Tiers] Mise à jour OpenEXR à la version 3.4.x
* [ThirdParty] Mettre à jour Qt &amp; QtForPython vers la version 6.8.x et Python vers la version 3.13.x
* [ThirdParty] Mettre à jour TBB vers oneTBB 2021.x
* [Dépréciation] Supprimer l’Iray et l’éditeur MDL

**Fixe :**

* [vue 2D] La plage de sélection de l’histogramme n’est pas conservée lorsque la largeur du widget devient petite
* [Exportation 3D] Les Maillages exportés à partir de Designer ne sont pas rendus de la même manière en mode usdview
* [vue 3D] L’affectation d’éléments non-udim à vue 3D laisse le mode de rendu mosaïque unique
* [vue 3D] Résultat Verrouillé lors de l&#39;utilisation d&#39;OCIO
* [vue 3D] Crash lors de l&#39;application d&#39;une texture de graphe sur un matériau non remplacé pour une scène spécifique
* crash [vue 3D] lors de la création de buffers cadres
* [vue 3D] Pathtracer GPU Eclair : géométrie rompue et performances réduites lors du rendu d’un modèle spécifique
* [vue 3D] Transformation de texture incorrecte pour des scènes spécifiques
* [vue 3D] Cadrage incohérent de la scène/sélection lors de l’utilisation d’une résolution de rendu fixe
* [vue 3D] Couleur diffuse incorrecte lors du rendu de certains fichiers GLTF
* [vue 3D] Environnement invisible lors du changement de moteur de rendu dans un cas spécifique
* [vue 3D] Les Matériaux ne sont pas détectés correctement lors de l&#39;importation de certains fichiers .fbx
* [vue 3D] Le remplacement de matériaux plusieurs fois réinitialise la répétition sur 1
* [vue 3D] Les propriétés de la catégorie « UV » ne sont pas enregistrées dans les fichiers SBSSCN
* [vue 3D] « Réinitialiser et afficher les sorties en vue 3D » à partir de graphes à sortie unique ne réinitialise pas les matériaux
* [vue 3D] &#39;Enregistrer le rendu&#39; : le format d’image modifié n’est pas conservé
* [vue 3D] La sélection ne fonctionne pas sur les GPU AMD
* [vue 3D] La Scène 3D autonome n&#39;est pas actualisée en cas de modification sur le disque
* [vue 3D] Certaines propriétés de matériau de couleur ne sont pas gérées correctement lorsqu’elles sont remplacées
* [vue 3D] Les textures UDIM ne sont pas appliquées correctement sur un maillage spécifique
* [vue 3D] La Scène USD avec le matériau MaterialX ne s’affiche plus correctement
* [Bakers] Crashs avec certains maillages
* [Bakers] Transfert de Texture : Crash dans bkBufferViewCopy
* [Cooker] Boucle infinie dans le nœud While Loop dans un cas qui pourrait être empêché
* [Moteur] Arrêter le moteur de Substance lors de la fermeture de l’application
* [Général] Éviter les crashs aléatoires lors de la fermeture de l’application (Windows uniquement)
* [Graphe] graphe de fonction : la propagation de type ne fonctionne pas correctement dans certaines situations
* [Graphe] Les liens de Graphe sont supprimés lorsqu’un noeud d&#39;entrée d’image est renommé
* [Graphe] Les liens et les épingles affichent parfois des artefacts
* [Préférences] La mise à l’échelle du Viewport est inversée
* [Propriétés] Crash lors de la modification de l’ajustement d’entrée de graphe lors de l’affichage de ses paramètres d’instance
* [Python] Impossible d&#39;importer les modules PySide6 (conflit possible avec l&#39;installation existante de PySide6)
* [Python] Les modules PySide et Shiboken existants sont en conflit avec Designer
* [UI] Le style de survol disparaît sur les boutons dans un cas spécifique (Windows uniquement)
* [UI] Le style de survol n’est pas visible sur les boutons déroulants lorsque vous cliquez dessus (macOS uniquement)
* [UI] Le bouton « En savoir plus » dans l’info-bulle « ? » ne fonctionne pas lorsque l’info-bulle est en dehors des limites de la boîte de dialogue (Windows uniquement)

**Problèmes connus :**

* [Graphe] Les icônes générées pour les OpenPBR ne sont pas précises
* [vue 3D] Les Scènes avec des primitives animées ne sont pas correctement prises en charge
* [vue 3D] Le traceur de tracé n’est pas pris en charge sur toutes les cartes graphiques AMD

## Version 15

### 15.1.3

*(Publié Le 10 Mars 2026)*

**Ajouté :**

* [Bakers] Ajout d’une macro outputsize pour le nom de fichier
* [Bakers] Éviter de charger le maillage highpoly avant le baking
* [Baker] CLI : mettre à jour la description de l’option « output-size » avec des macros de taille
* [Bakers] Convertir le format de texture d’entrée au format demandé
* [Bakers] Désactiver l’option « Décalage » lorsque l’option « Utiliser la cage » est cochée
* [Bakers] L’affichage prend déjà map bakée lorsque la fenêtre de baking est rouverte
* [Bakers] Laissez la fenêtre de baking ouverte jusqu’à ce que tous les processus de baking soient effectivement annulés.
* [Baker] Fonction Migrate BindTexture
* [Baker] [Paramètres] Définissez la valeur par défaut « mode de filtrage de noms » sur « Nom parent (hérité) »
* [Baker] [Info-bulle] Ajoutez la valeur « mode de filtrage de nom » à l’info-bulle du paramètre « Match »
* [Moteur] Mise à niveau du moteur de Substance vers la version 9.3.4

**Fixe :**

* [vue 3D] « Afficher les sorties en vue 3D » ne remplace pas l’affectation existante sur les graphes avec une seule sortie
* [vue 3D] Impossible d’afficher les UV dans certains cas
* [vue 3D] Les tangentes calculées pour USD semblent rompues
* crash [vue 3D] lors de l’ouverture du menu Système de rendu
* [Bakers] Impossible de définir une distance supérieure à 1 lorsque l’option Relative à la case n’est pas cochée
* [Bakers] Le baker des couleurs prend beaucoup trop de temps dans certains cas
* [Bakers] Couleur : Crash lorsque le baking s’Îlot UV
* [Bakers] Les plages de paramètres de distance et de rayon sont trop étroites lorsque la valeur est absolue
* [Bakers] Défaillance lors du baking à partir de tangentes manquantes et de bitangents en poly élevés qui ne sont pas nécessaires
* [Baker] Couleurs de Matériau incorrectes dans la ligne de commande baker
* [Bakers] Dans certaines situations, les multiples maillages en poly élevé sont ignorés
* [Baker] Normal : sortie noire lors de l’utilisation du lissage et de la diffusion (macOS uniquement)
* [Baker] La vérification du chemin de mappage de décalage signale des échecs inattendus lors de l’utilisation des ressources du package bitmap
* L&#39;info-bulle de mappage de décalage [Baker] est incorrecte
* [Bakers] Le placement de la ressource dans un dossier spécifique au maillage ne fonctionne pas
* [Baker] Transfert de Texture : la valeur « Ensemble d&#39;UV » n’est pas restaurée comme elle l’était lors de la réouverture de la fenêtre de baking
* [Bakers] Transfert de Texture : une entrée en niveaux de gris n’entraîne pas une sortie en niveaux de gris
* [Bakers] L’avertissement pour le baker hérité désactivé n’est pas effacé lors de la modification de la source de texture dans le baker cible
* [Bakers] [UDIM] Le mappage de décalage s’applique uniquement à l’UDIM 1001
* [Graphe] L&#39;UDIM 1001 est toujours calculé quel que soit le UVTile utilisé

### 15.1.2

*(Publié Le 3 Février 2026)*

**Fixe :**

* [Moteur] Niveaux : les Valeurs de point flottant sont toujours serrées à [0, 1]
* [Bakers] La correspondance de la géométrie par nom de parent (hérité) ne fonctionne pas pour les sous-maillages
* [Bakers] Couleur : les modifications apportées aux couleurs du matériau dans l’interface utilisateur sont ignorées
* [vue 3D][Baker] Le chargement du fichier OBJ prend beaucoup de temps

### 15.1.1

*(Publié Le 20 Janvier 2026)*

**Ajouté :**

* [Échantillons] Ajoutez deux échantillons pour créer des sections afin d’alimenter l’outil ruban Painter
* [Moteur] Mise à jour vers la Substance Engine v9.3.2
* [Moteur][Métal] Améliorer les performances
* [Moteur] L’interpolation Bilinéaire des textures d’entier est désormais effectuée avec une précision accrue (back-end du processeur)
* [Bakers] Consigner un avertissement si la couleur du Vertex est absente de maillage high poly
* [Branding] Mise à jour des icônes de types de fichiers
* [NewGraph] Appliquer les styles de survol sur l’icône (i) en modes d’affichage « Liste », « Packs » et « Répertoires »

**Fixe :**

* [3DView] Les maillages UDIM ne restituent plus un seul carreau
* [3DView] Crash lorsqu&#39;aucun renderDevice n&#39;est détecté
* [Branding] Correction des icônes des fichiers .SBS sous Linux
* [Contenu] RGB à la fonction TSL : résultat incorrect pour près de 0 entrée
* [Graphe] Le générateur d’icônes de Graphe/de vignettes ne fonctionne pas
* [Graphe] Menu Nœud : les éléments regroupés sans vignette n’ont pas de retrait
* [Moteur][Contenu] Couleur pour masquer v2 : artefacts sur le moteur SSE2 lors de l’utilisation de l’espace colorimétrique de distance Lab
* [Moteur][Contenu] Couleur pour masquer v2 : artefacts sur les moteurs GPU arm64 lors de l’utilisation de l’espace colorimétrique de distance Lab
* [Moteur][Métal] Sortie d&#39;irradiance noire pour nœud de Rendu PBR
* [Moteur][Mac] Résultat incorrect dans une fonction de processeur de pixels sur Metal
* [Moteur][Mac] Améliorez la précision de certaines instructions utilisées dans les Processeurs de pixels sur les GPU Apple Silicon M1/M2.
* [Moteur] Le redimensionnement des Images d&#39;entrée (ou des ressources incorporées) n’introduira plus d’artefacts de bordure (back-end du processeur)
* [Moteur] Le filtre Niveaux ne verrouille plus ses valeurs d’entrée en virgule flottante lors de la sortie de textures 8I/16I (back-end CPU)
* [Moteur] Correction d’un bug FxMaps où les images d&#39;entrée en niveaux de gris consommées par les nœuds FxMaps pouvaient être échantillonnées de manière incorrecte (back-end du processeur)
* [Moteur] Correction de certains artefacts dans la version à 1 amorce du filtre Distance (principaux GPU)

### 15.1.0

*(Publié Le 11 Décembre 2025)*

**Ajouté :**

* [NewGraph] Modification de la fenêtre du nouveau graphe
* [NewGraph] Ajout d’échantillons de matériaux et d’échantillons avancés
* [NewGraph] Ajouter un nouvel attribut pour le graphe des données du modèle (catégorie et sous-titre)
* [NewGraph] Option Supprimer le format de sortie
* [Contenu] Ajout de fonctions de hachage
* [Contenu] Ajout de mappeurs de tonalité à features.sbs
* [Contenu] bruit anisotrope v2 : ajouter le format de sortie par défaut, ajouter un désordre
* [Content] Appliquer la casse de la phrase aux étiquettes de nœuds et de paramètres
* [Contenu] Points BnW 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Points BnW 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Points BnW 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Cellules 1, 2, 3, 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions, options de désordre
* [Contenu] Clouds 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Clouds 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Clouds 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Couleur au masque v2
* [Contenu] Bruit directionnel 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Bruit directionnel 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Rayures directionnelles v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dirt 5 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Dégradé de Dirt v2 : ajout du format de sortie par défaut, nouvelles options de désordre
* [Contenu] Somme fractale Base v2 : ajout du format de sortie par défaut, désordre, pas de prise en charge des répétitions
* [Content] Somme fractale 1,2,3,4 v2 : ajout du format de sortie par défaut
* [Contenu] bruit gaussien v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Taches gaussiennes 1&amp;2 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Fibres désordonnées 1,2,3 v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions, options de désordre
* [Contenu] bruit d’humidité v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* [Contenu] Nouveau nœud « Moisture bruit 2 »
* bruits [Content] : mettre à jour pour ajouter le format de sortie par défaut
* [Contenu] Perlin bruit v2 : ajout du format de sortie par défaut, pas de prise en charge des répétitions
* Mappeur de formes [Contenu] : ajouter un mode de filtrage
* [Content] UV mapper : ajouter un mode de filtrage
* [Contenu] Forme d’onde 1 v2 : utilisation du format de sortie par défaut + nouvelles options
* [Contenu] bruit blanc v2 : utilisation du format de sortie par défaut, ajout d’options de distribution
* [Bakers] Afficher uniquement les UV du maillage sélectionné
* [Bakers] Ajoutez une option pour sélectionner la méthode de correspondance de la géométrie par nom
* [Bakers] Sélectionner le Baker le plus proche lorsqu’un baker est supprimé
* [Bakers] UDIM : définissez une liste d’UV à baker
* [Baker] Mise à jour du kit de développement logiciel baking vers la version 3.15.4
* [vue 3D/SceneBrowser] Évitez de sélectionner un élément UsdPrimitive lorsque vous effectuez un clic droit dessus
* [ColorManagement] Prise en charge d&#39;ACE 2.0
* [Graphe de composition] Autoriser à définir un nœud de sortie comme « Sortie par défaut »
* [Cooker] Supprimer l&#39;avertissement sur les entrées non connectées des instances de fonction¬†
* [Fonctions] Opérateur Add isDefined
* [Par Graphe] Regroupez les éléments par attribut &#39;group&#39; dans le menu du nœud
* [Graphe] Amélioration du rendu des vignettes

**Fixe :**

* [vue 3D] La texture Niveaux de gris L16 s’affiche avec une teinte rouge lorsqu’elle est connectée à l’environnement ou à la baseColor
* [vue 3D] La modification de la liaison de matériau d’une scène sans matériau crée un nouveau matériau « par défaut »
* [vue 3D] Les normales calculées ne sont pas correctes pour des maillages OBJ spécifiques
* [vue 3D] L’environnement personnalisé de SBSSCN n’est pas visible lors du chargement dans Pathtracer
* [vue 3D] Erreurs dans la console lors de la rotation d’un environnement désactivé
* Le Specular level [vue 3D] n&#39;est pas appliqué correctement
* [vue 3D] Le Specular edge color ne fonctionne pas lors de l’utilisation de la pixellisation Eclair
* [vue 3D] Le matériau ajouté par l&#39;utilisateur n&#39;est pas appliqué aux scènes par défaut
* [vue 3D][Bakers] La couleur du Matériau est trop sombre une fois remplacée ou lors de l’utilisation d’un baker « Couleur »
* [vue 3D][Bakers] Aucune couleur de matériau du fichier FBX
* [Bakers] Les couleurs de Matériau dans les fichiers FBX ne sont pas correctement détectées
* [Baker] L’option « recompute\_tangentes » a toujours la valeur « false » dans les exportations de paramètres prédéfinis JSON
* [Baker] CLI : Crash lors de l’exécution du même baker de manière consécutive à travers le Fichier JSON
* [Bakers] La mise à jour du paramètre « color-generator » ne fonctionne pas pour « Grayscale »
* [Contenu] Masquage sur tracés : échec dans les rapports non carrés
* [Contenu] Rendu Rendu PBR/Icône : fonction incorrecte du lobe de specular
* [Contenu] Tracés vers la spline : définissez la « Taille de sortie » sur « Relatif au parent » par défaut.
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Mappeur de spline : problème de ligne de 1 px dans des cas aléatoires
* [Content] Spline mapper : étire les UV dans certains cas lorsque le thickness est à 0
* [Graphe] Crash lors de la suppression de la sortie d&#39;un sous-graphe de fonction
* [Graphe] Le type de couleur de Noeud d&#39;entrée peut être modifié dans les packages en lecture seule
* [Graphe] L’entrée principale peut être modifiée dans les packages en lecture seule
* [Propriétés] La couleur du widget d’aperçu de couleur ne correspond pas à l’état du bouton sRVB
* [Scène] Impossible de charger un fichier OBJ de plus de 2 Go
* [UI] Les états d&#39;ancrage de la console et du gestionnaire de dépendances ne sont pas restaurés après le redémarrage

### 15.0.3

*(Publié Le 23 Octobre 2025)*

**Fixe :**

* [Contenu] La sortie d’aperçu des nœuds Outils spline ne s’affiche pas par défaut
* [Graphe] Crash lors de la suppression de la sortie d&#39;un sous-graphe de fonction

### 15.0.2

*(Publié Le 18 Septembre 2025)*

**Ajouté :**

* [vue 3D/OpenGL] Supprime l’effet structure filaire appliqué au Maillage sélectionné
* [vue 3D] Permet d’utiliser la touche F pour se concentrer sur un maillage sélectionné lorsque l’Explorateur de Scènes est activé
* [vue 3D] Le rendu n’est pas actualisé lors de la modification du format de map normal
* [BakersCLI] Option permettant de contrôler la taille de la mémoire cache de la surface
* [BakersCLI] Renommez l’option « use\_cache » en « keep\_meshes\_in\_cache ».
* [UI] Icône Actualiser pour les scènes 3D dans la bibliothèque

**Fixe :**

* [vue 3D] Crash lors de l&#39;affectation d&#39;un nœud de matériau à une scène à matériaux multiples
* [vue 3D] Le Graphe créé à partir des entrées de texture est toujours affiché dans vue 3D, quelles que soient les préférences
* [vue 3D] Utilisation incorrecte dans une info-bulle de badge « Consulté dans vue 3D » dans un cas spécifique
* [vue 3D] Beaucoup d’erreurs USD lors du remplacement de scènes spécifiques
* [vue 3D] Artefacts d’ombre lors de l’utilisation du displacement sur une Scène plate dans la pixellisation
* [vue 3D] Certaines scènes spécifiques ne sont pas visibles lors de l’utilisation du rendu OpenGL
* [vue 3D] La boîte de dialogue utilisée pour « Sélectionner le Graphe Substance de destination » comporte toujours l’icône de Graphe « En attente »
* [vue 3D] Le menu contextuel du viewport ne s’affiche pas pour des scènes spécifiques
* [vue 3D] Les badges « Consulté en vue 3D » ne sont pas effacés lors du changement de scènes dans un cas spécifique
* [vue 3D] Couleurs délavées dans vue 3D lors de l’utilisation de la gestion des couleurs Adobe ACE
* [vue 3D][Linux] Plusieurs scènes s’affichent en noir dans le moteur de rendu OpenGL
* [vue 3D][Explorateur de Scènes] Les touches fléchées déplacent la sélection à la racine
* [BakerCLI] Impossible de remplacer certains paramètres
* [Bakers] Artefacts en dilatation lors de l’utilisation de bakers normaux avec antialiasing
* [Bakers] Le processus de Baking s&#39;est brusquement arrêté dans la CLI tout en bakant une grande quantité d&#39;UDIM en 4K
* [Bakers] Crash lors de la poussée du baker vers le bas dans la liste des bakers dans un cas spécifique
* [Bakers] La sélection du format passe de .surface à .dds
* [Bakers] Geler tout en bakant une grande quantité d&#39;UDIM à 4K
* [Bakers][macOS] Crash lors du baking du transfert de Texture avec l’anticrénelage
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Afficher la palette de couleurs : les nœuds internes sont calculés à des résolutions trop élevées
* [Données] Crash lors du renommage de la sortie pour corriger la sortie du fantôme dans l&#39;instance
* [Moteur] Distance : la luminance du masque de saisie est modifiée
* [FxMap] $répétition n’a aucun effet si le FX-Map se trouve dans un sous-graphe
* [Graphe] La recherche floue renvoie des résultats non pertinents
* [Éditeur Python] Les scripts chargés ne sont pas rouverts entre les sessions

### 15.0.1

*(Publié Le 22 Juillet 2025)*

**Ajouté :**

* [vue 3D] Autoriser la texture des Maillages USD qui ont displayColor et aucune liaison de Matériau
* [vue 3D] Ne créez pas automatiquement un matériau par maillage sans liaison de matériau
* [vue 3D] Renommez « Echantillons de pixels convergés » en « Echantillons ».
* [vue 3D] Renommez le paramètre « Échelle UV activée » en « Activer la Taille physique à partir du Graphe »
* [vue 3D] Diminuez l’intensité du displacement en fonction du paramètre « Répétition »
* [vue 3D/OpenGL/Iray] Ajouter un message dans le viewport lorsque l’environnement par défaut est désactivé
* [Bakers] Utilisez des icônes pour les boutons afin de réorganiser les lignes dans la liste de rendu des Bakers
* [Préférences] Ajoutez une option pour définir le moteur de rendu vue 3D par défaut
* [Propriétés] Faites en sorte que « Rétablir la valeur par défaut » utilise les valeurs par défaut créées le cas échéant.

**Fixe :**

* [vue 3D] Artefacts sur une scène spécifique lors du rendu avec OpenGL
* [vue 3D] L&#39;environnement par défaut n&#39;est pas désactivé lors du chargement d&#39;une ressource Scène 3D USD qui en contient une
* [vue 3D] L’affichage du menu contextuel par viewport prend plusieurs secondes en grandes scènes
* [vue 3D] &#39;intensité d&#39;Emissive&#39; est égal à 0 lors du remplacement de matériaux non USD à l&#39;aide de &#39;couleur d&#39;Emissive&#39; uniquement
* [vue 3D] Les canaux rouge et bleu sont permutés dans une texture 8 bits utilisée comme environnement.
* [vue 3D] Le glisser-déposer RMB ne fonctionne pas de manière cohérente en raison du registre par clic droit
* [vue 3D] « Afficher uniquement » sur le sous-ensemble masque son maillage parent
* [vue 3D] Les Scènes par défaut chargées à partir d’un fichier apparaissent avec une base color incorrecte
* [vue 3D] La propriété « Échelle UV » est réinitialisée lors du passage d’OpenGL à un autre moteur de rendu et inversement
* [vue 3D][Iray] Les rendus sont souvent flous et pixellisés
* [Bakers] Artefacts lors de l’utilisation de la diffusion sur un GPU AMD
* [Bakers] Le Baking échoue avec certaines scènes pour les Ensembles d&#39;UV autres que 0
* [Bakers] « texture transférée » : la liste « Ensemble d&#39;UV » ne prend pas en compte l’option « Utiliser un niveau de poly faible ou élevé »
* [Baker] La sélection des UV est toujours réinitialisée sur « Tous »
* [Graphe] Crash lors de la suppression d&#39;un nœud dans le contexte
* [Mac OS][vue 3D] Résolution de rendu incorrecte sur les écrans mac
* [Paramètres] Les paramètres modifiés ne sont pas stylisés lors du premier affichage
* [UX] Les éléments désactivés dans le menu déroulant sont invisibles

### 15.0.0

*(Publié Le 15 Juillet 2025)*

**Ajouté :**

* [vue 3D] Nouveau système de rendu, avec modes pixelliseur et traceur de tracé
* [vue 3D] Ajout d’un outil de sélection pour sélectionner un objet dans la Scène 3D
* [vue 3D] Ajouter la nouvelle option « Exporter la scène avec les calques... » action dans le menu « Scène »
* [vue 3D] Ajouter de nouveaux boutons de barre d’outils
* [vue 3D] Ajout de la possibilité de basculer entre plusieurs caméras contenues dans une scène USD
* [vue 3D] Permet de se concentrer sur l’objet sélectionné en appuyant sur la touche F dans le viewport
* [vue 3D] Autoriser à générer un Graphe de composition de Substance à partir d&#39;un matériau existant
* [vue 3D] Permet d’envoyer un Graphe SBS Comp dans vue 3D et d’affecter sa sortie unique à l’utilisation d’Environnement/Panorama
* [vue 3D] Effacez la sélection en cours en appuyant sur la touche Échap
* [vue 3D] Afficher une Scène 3D importée avec des textures
* [vue 3D] Distinguer les commandes de répétition de texture X et Y
* [vue 3D] Activer/désactiver les tons foncés
* [vue 3D] Activer/désactiver le plan de sol
* [vue 3D] Dans le menu « Matériaux », ajoutez « Supprimer » uniquement pour les Matériaux qui ont été ajoutés manuellement et qui sont inutilisés
* [vue 3D] Dans le menu « Matériaux », supprimez l’action « Tout supprimer »
* [vue 3D] Rendre les fichiers USDZ exportés autonomes
* [vue 3D] Rendre les propriétés de rendu persistantes lors du changement de mode de rendu
* [vue 3D] Conserver les entrées de matériau existantes lors du remplacement d’un Matériau
* [vue 3D] Réorganisation des propriétés de Caméra
* [vue 3D] Supprimer les actions « Caméra/Enregistrement de la capture d’écran... » et « Caméra/Copier la capture d’écran dans le presse-papiers »
* [vue 3D] Supprimez l’action de menu « Matériau/Tout reconstruire ».
* [vue 3D] Supprimez le préfixe « Par défaut » de l’étiquette de la caméra par défaut
* [vue 3D] Définissez l’action de menu « Rétablir la valeur par défaut » comme dernière action dans le menu hamburger de la propriété d’entrée de matériau
* [vue 3D] Réglages du Raccourci
* [vue 3D] Prise en charge des tons foncés et du translucency en mode temps réel
* [vue 3D] Prise en charge des nuanciers MaterialX à partir d&#39;une scène USD importée
* [vue 3D / OpenGL] Renommez le paramètre « Échelle UV activée » en « Activer la Taille physique à partir du Graphe ».
* [vue 3D / Effets de post-traitement] Fleur
* [vue 3D / Effets de post-traitement] Profondeur de champ
* [vue 3D / Effets de post-traitement] Mappage de tonalité
* [vue 3D / Scène Browser] Permet d’afficher les propriétés du Matériau lors de sa sélection dans SceneBrowser
* [vue 3D / Scène Browser] Masquer la colonne « Matériau »
* [vue 3D / Scène Browser] Mettre en gras les primitives USD qui sont contrôlées par une entité prédéfinie
* [Bakers] Ajout d’un menu contextuel dans l’arborescence avec des actions « Tout sélectionner »/« Tout désélectionner »
* [Bakers] Ajout d’une option pour contrôler l’interpolation bitangente
* [Bakers] Ajout d’un séparateur horizontal dans l’interface utilisateur graphique
* [Bakers] Ajout d’une macro UDIM par défaut dans le nom de la sortie lorsque la scène est udim
* [Bakers] Autoriser à recalculer la tangente
* [Bakers] Autoriser à renommer un baker sans rompre les liens
* [Bakers] Modification de la taille par défaut du panneau central
* [Baker] texture de saisie pour le workflow UDIM
* [Bakers] Faire correspondre l’ordre de liste des cartes vue 2D à l’ordre de liste de rendu des Bakers
* [Bakers] Rendre la fenêtre de baking modale
* [Baker] Gestion des paramètres de mappage de tonalité
* [Bakers] Supprimer la sélection de plugin de repère tangent
* [Bakers] Statut d’enregistrement « activé » ou « désactivé » pour les Bakers lors de l’enregistrement d’un paramètre prédéfini
* [Bakers] Sélectionner le matériau par défaut dans le widget de sélection
* [Bakers] Définir l’orientation par défaut de la texture de sortie normale par rapport à la préférence
* [Baker] Définissez UV tiles sur Tous par défaut
* [Baker] Option d’ajout FromTexture/FromValue dans WordSpaceDirection
* [Bakers] World to tangente : définissez l’entrée par défaut sur « from texture »
* [SBSBaker] Création d’une option pour contrôler l’ordre du back-end
* [SBSBaker] Amélioration de l’utilisation de l’argument StringList
* [SBSBaker] Renommez « match\_source\_instance » en « match\_maillage\_name »
* [SBSBaker] Renommez « Submesh » en « GeomSubset ».
* [SBSBaker] Renommer en substance3d\_baker
* [Contenu] Ajouter une forme « Hémisphère » aux nœuds de générateur exposant des formes de quadrant
* [Interop] Prise en charge du format de fichier GLTF
* [Interop] Prise en charge du format de fichier PLY
* [Interop] Prise en charge du format de fichier STL
* [Bibliothèque] Uniformiser les info-bulles pour les noeuds atomiques
* [Mac] Ne plus prendre en charge les plates-formes MacIntel
* [Nodes] Ajouter des info-bulles riches pour les noeuds atomiques
* [Paramètres] Fermer la section « Attributs » par défaut
* [Paramètres] Permet à l’utilisateur de spécifier les valeurs par défaut des paramètres de base pour les nouvelles instances
* [Préférences] Bakers : ajoutez une option booléenne pour calculer l’espace de tangente par fragment
* [Préférences] Supprimer les plug-ins d’espace de tangente
* [Préférences] Stockez les préférences par version mineure de SD (XX.X).
* [VFX] Mise à jour de Boost vers 1.85.0
* [VFX] Mise à jour de MacOS version minimale vers la version 12.0
* [VFX] Mise à jour d’OpenColorIO vers la version 2.4.2
* [VFX] Mise à jour d’OpenColorIO vers la version 2.4.x
* [VFX] Mettre à jour OpenExr vers la version 3.3.x
* [VFX] Mise à jour de Qt vers la version 6.5.8

**Fixe :**

* Les Textures [vue 3D] de la scène USD exportée ne sont pas correctement appliquées
* [vue 3D] [UDIM] Impossible d&#39;afficher les sorties du graphe UDIM dans vue 3D lorsque l&#39;affichage automatique à l&#39;ouverture du graphe est désactivé dans les préférences de graphe
* [Bakers] &#39;Anticrénelage.&#39; et &#39;Moy. les cellules des normales pour les bakers non applicables sont vides et modifiables
* [Bakers] L’action « Actualiser » utilise le back-end raytracing lorsqu’elle est désactivée dans les préférences
* [Bakers] Bakers bloqués comme occupés après l&#39;échec du processus « Actualiser toutes les maps bakées »
* [Bakers] Crash à plus de 180 UDIM lors du baking du mappage de position OpenGL sur un maillage spécifique
* [Bakers] Crash lors de l’ouverture de la boîte de dialogue « Informations sur le modèle Baker » plusieurs fois de suite (macOS uniquement)
* [Bakers] Dans l’exportation du paramètre prédéfini JSON, la valeur « udim » est remplacée par « 1001 » lorsqu’elle était définie sur « Tout ».
* [Bakers] La mémoire n&#39;est pas correctement détectée sous Linux
* [Bakers] La dépendance d’entrée de mappage manquante ne déclenche pas d’avertissement et/ou de rendu de bloc
* [Bakers] Aucun libellé d’erreur lorsque le nom de la sortie est vide
* [Bakers] Le remplacement du maillage high poly du fichier n’a aucun effet
* [Bakers] Le baker cible n’est pas sélectionné par défaut lors de l’utilisation de l’action « Rebake »
* [Moteur] Distance : « coupe » visible dans certaines situations
* [Moteur] Fx-Map : les couleurs négatives ne sont pas prises en charge lorsque la profondeur de bit est de 8 bits (moteurs GPU uniquement)
* [Localisation] La saisie des caractères revient du japonais au latin dans le menu des nœuds
* [Security] Vulnérabilité d&#39;analyse de fichier USDC hors écriture liée
* [Sécurité] Vulnérabilité II d’écriture hors limites lors de l’analyse du fichier NEF
* [Sécurité] Vulnérabilité de lecture III hors limites lors de l’analyse du fichier DNG
* [Préférences] Problèmes UX dans les paramètres de projet pour les projets en lecture seule
* [Ressources] Les Ensembles d&#39;UV multiples ne s’affichent pas lors de l’ouverture de fichiers FBX
* [UI] Libellés qui se chevauchent dans la barre d’état
* [UI] Les info-bulles du menu déroulant « Mode de création de lien » ne sont pas affichées

## Version 14

### 14.1.2

*(Publié Le 15 Avril 2025)*

**Ajouté :**

* [Graphe] Utilisez le moteur GPU par défaut pour générer des vignettes pour le graphe actif
* [Bibliothèque] Utilisez le moteur GPU par défaut pour générer des vignettes pour la bibliothèque

**Fixe :**

* [Graphe] Impossible de déplacer les connexions dans certains cas en mode de création de lien « Standard »
* [Contenu] Artefacts dans la sortie du filtre MLV dans un cas spécifique
* [Contenu] Atlas splitter/dispersion : seule la première cellule est dessinée correctement (macOS + moteur GPU uniquement)
* [Contenu] Bevel smooth : format absolu 32f
* [Contenu] Fibres 1 : artefacts visuels lors de la conversion en map normal
* [Contenu] Le rendu de RT AO, Shadows, Bent Normal est incorrect dans certains cas
* [Bakers] Les éléments de menu avec sous-menus ne comportent pas une marge à droite du texte
* [MacArm][sbsrender] moteur CPU incorrect lorsque le moteur GPU est introuvable
* [Mac/Linux][sbsrender] moteur GPU par défaut incorrect

### 14.1.1

*(Publié Le 20 Février 2025)*

**Ajouté :**

* [Graphe] Outils d’alignement des nœuds : rétablir les raccourcis clavier, activer l’empilement par défaut
* [MDL] Avertir les utilisateurs que le terme « Graphes MDL » sera abandonné dans une version ultérieure
* [Préférences] Avertissez les utilisateurs que les « plug-ins d’espace de tangente personnalisé » seront obsolètes dans une version ultérieure

**Fixe :**

* [vue 2D] Afficher les coordonnées des pixels au centre plutôt que dans le coin supérieur gauche
* [Contenu] Niveaux de gris anisotropes de Kuwahara : avertissement du cuiseur pour variable « ignore\_alpha » manquante
* [Contenu] Avertissements relatifs aux cookies dans certains nœuds Usure/salissures
* [Content] Erreurs de cuisson pour le paramètre manquant dans le nœud &#39;Niveaux automatiques&#39;
* [Contenu] Erreurs de cuisson dans la console lors du rendu des vignettes de certains packs
* [Contenu] Edge Notch : avertissement de cuisson dans la console
* [Content] Couleur MLV : Couleur à fond perdu malgré l&#39;utilisation de l&#39;option Aucune Répétition dans un cas spécifique
* [Contenu] Masquer sur les tracés : dans certains cas, les tracés peuvent être trop nombreux, trop peu nombreux ou avoir une longueur nulle
* [Contenu] Rendu PBR v1 : certains graphes utilitaires sont exposés dans la bibliothèque
* [Contenu] Dispersion sur la spline : un motif est dessiné même s&#39;il n&#39;y a pas d&#39;entrée de spline
* [Paramètres] Libellé de « valeur de Fantôme » lors du collage d’un paramètre de liste avec un index non concordant
* [UI] Crash lors de la fermeture de Designer via l’action « Quitter » dans le dock macOS (macOS uniquement)
* [UI] Les tracés de Texture dans les propriétés de shader ne sont pas recadrés à la largeur du dock

### 14.1.0

*(Publié Le 14 Janvier 2025)*

**Ajouté :**

* [vue 2D] Ajout d’un affichage de pixels épinglés dans le panneau Informations
* [API] Exposer la taille de la zone BBox des nœuds dans la scène de Vue du graphe de données
* [Contenu] &#39;Fusion d&#39;Height de Matériau&#39; : ajouter une sortie &#39;Masque d&#39;Height&#39;
* [Contenu] &#39;Processeur de Vertex de chemin&#39; : utilisez le bouton &#39;Modifier la fonction&#39; pour le paramètre &#39;Fonction par sommet&#39;
* [Contenu] Niveaux automatiques : nettoyage des paramètres inutilisés, ajustement des libellés et de l’info-bulle
* [Contenu] Masquage sur tracés v2
* [Content] Nouvelle moyenne du nœud de moindre écart (MLV)
* [Contenu] Nouveau Noeud de filtrage médian
* [Contenu] Quantifier la couleur : ajout d’une option de filtrage « Au plus proche »
* [Content] Liste des ponts splines : ajout aléatoire de paramètres de décalage de spline
* [Contenu] Outils spline : nouveau nœud spline (quadratique)
* [Contenu] Triangle Grid : modification de la méthode de triangulation et utilisation de boucles
* [Contenu] Nouvelles splines de Dispersion sur le nœud Splines
* [Cooker] Exposer le paramètre de base « Pixel ratio » comme variable statique « $pixelratio »
* [CrashReport] Fenêtre Intégrer un nouveau rapport de crash
* [Moteur] Ajout de la version Vulkan/Metal du moteur de fusion
* [Graphe] Mode de matériau : permet à la connexion d’entrer des données sans utilisation lorsqu’un seul lien est sélectionné
* [Graphe] Lien de Matériau : permet les connexions standard lorsque la connexion n’est pas ambiguë
* [Graphe] Outils d’alignement des nœuds : ajoutent des distributions horizontales/verticales, des alignements gauche/droite/haut/bas et prennent en charge les nœuds empilés
* [Bibliothèque] Correction de la couleur du texte dans les menus contextuels
* [Paramètres] Copie des paramètres d&#39;un nœud vers un autre
* [Propriétés] « Tout réinitialiser » : Supprimer la fenêtre contextuelle de confirmation
* [Ressources] Définissez le format sur « Tous les formats » dans la boîte de dialogue « Lier Bitmap »
* [Search] Ajouter un moyen d&#39;activer/désactiver un mode récursif
* [Search] Ajouter un moyen d&#39;activer/désactiver la recherche floue
* [Search] Toujours afficher et définir le focus sur le champ de terme de recherche lors de l’activation du Finder de nœuds à l’aide de son raccourci clavier
* [Rechercher] Retravailler l’option de filtre
* [Raccourcis] Autoriser l’attribution des touches « V », « H » et « S »
* [Tiers] Mise à niveau vers Qt 6.5.7
* [UX] Les boîtes de dialogue modales ne doivent pas être réduites au minimum
* [UX] Supprimer le défilement horizontal sur la boîte de dialogue d’alerte

**Fixe :**

* [Contenu] Biseau : le format normal n’est pas affecté par la préférence globale
* [Contenu] Le nœud de couleur à masquer n’ignore pas les caractères alpha
* directional distance [Contenu] : résultat incorrect lorsque l’entrée a un rapport d’image vertical
* Mappeur de Flood Fill [Content] : Avertissement déclenché pour la variable absente
* [Contenu] Histogramme Calculer : le résultat est 16 fois supérieur à ce qu’il devrait être
* [Contenu] RT caustics ne fonctionne pas en résolution non carrée
* [Content] Liste des ponts splines : résultat incorrect lors de l&#39;utilisation des décalages de début/fin
* [Content] Spline Select : la quantité de spline de sortie peut être supérieure à la quantité de spline d&#39;entrée
* [Contenu] La déformation spline produit un résultat noir avec le moteur SSE
* Triangle Grid [Contenu] : le motif n’est pas correctement répétition
* Triangle Grid [Contenu] : la Répétition est rompue dans un cas spécifique
* [Données] Crash lors de la modification de l&#39;identifiant d&#39;entrée du graphe dans un cas spécifique
* [Graphe de fonction] Les valeurs longues apparaissent chevauchées sur les nœuds « Flottant »
* [Fx-Map] Crash lors de l&#39;affichage des propriétés de nœud de quadrant
* [Graphe] [UDIM] Le fait d’avoir une barre de défilement dans la liste des UDIM entraîne 1..1 1..2 entrées
* [Graphe][Raccourcis] Le nœud créé à l&#39;aide d&#39;un raccourci n&#39;est pas placé sur le lien existant après la duplication du nœud
* [Propriétés] Affichage incorrect des paramètres lorsque la valeur n’est pas valide
* [Publish] Les dépendances réciproques entraînent une boucle infinie lors de la publication d’un pack
* [Publish] Échec silencieux lors de l’utilisation de l’action « Publish » sur un pack avec une dépendance déchargée
* [UI] Le widget « Taille du gabarit » ne s’affiche pas correctement lorsqu’il est développé et peut bloquer l’interface (macOS uniquement)
* [UI] Dans certains cas, la fenêtre principale se trouve derrière d’autres applications (Windows uniquement)

### 14.0.2

*(Publié Le 10 Octobre 2024)*

<b>Ajouté :</b>

* [graphe de fonction] Améliorer l’alignement du texte au sein des nœuds
* [MacOS] Réautoriser l’installation sur la version Big Sur (11.0)
* [Windows] Réautoriser l’installation sur Windows 10 19H2

<b>Fixe :</b>

* [Bitmap] Les contours de Peinture sur la ressource bitmap ne marquent pas le package hôte comme modifié
* [Graphe de fonction] Crash lors de la fermeture d’un pack avec un graphe de fonction hébergeant un instancier
* [graphe de fonction] Crash lors de l’annulation de deux ajustements de nœud Sample Color sur une ligne

### 14.0.1

*(Publié Le 24 Septembre 2024)*

<b>Ajouté :</b>

* [Moteur] Mise à jour vers la Substance Engine 9.1.4
* [Contenu] Triangle Grid : modification de la méthode de triangulation et utilisation de boucles

<b>Fixe :</b>

* [API] Impossible de charger à nouveau les plug-ins déchargés
* [Contenu] Histogramme Calculer : le résultat est 16 fois supérieur à ce qu’il devrait être
* Triangle Grid [Contenu] : le motif n’est pas correctement répétition
* [Données] Crash lors de la modification de l&#39;identifiant d&#39;entrée du graphe dans un cas spécifique
* [Moteur] Le nœud Distance produit des artefacts lors de l’utilisation de tailles de pixels très faibles
* [Moteur] Résultat du nœud Distance incorrect à une résolution de 8K sur le moteur SSE2
* [Graphe de fonction] Les valeurs longues apparaissent chevauchées sur les nœuds « Flottant »
* [Graphe][Raccourcis] Le nœud créé à l&#39;aide d&#39;un raccourci n&#39;est pas placé sur le lien existant après la duplication du nœud
* [Propriétés] Affichage incorrect des paramètres lorsque la valeur n’est pas valide

### 14.0.0

*(Publié Le 30 Juillet 2024)*

<b>Ajouté :</b>

* [Contenu] Nouveau filtre Kuwahara anisotrope
* [Contenu] Nouveau nœud de Bevel smooth
* [Contenu] Nouveau nœud Courbure Lisse v2
* [Contenu] Nouveau nœud de Directional distance
* [Contenu] Nouveaux outils d’histogramme : calcul, égalisation, rendu
* [Contenu] Nouvel ID vers le nœud de masque
* [Content] Nouveau nœud de décombinaison normal
* [Contenu] Nouveaux nœuds de palette : Créer, Appliquer, Modifier, Afficher
* [Contenu] Nouveau nœud Quantize Color
* [Contenu] Déformation directionnelle non uniforme : définissez la valeur par défaut de la carte d’intensité sur 1
* [Contenu] Ajoutez le suffixe « Color » ou « Grayscale » à tous les libellés de nœuds qui ont ces versions
* [Contenu] Les anciens « Bruit blanc » conservent uniquement « Bruit blanc rapide »
* [Contenu] Nœud « Negate Flottant 1 » déconseillé dans le graphe de fonction de Substance
* [Contenu] Renommez « Quantize Color » en « Quantize Color (Simple) ».
* [vue 2D] Valeurs d’affichage dans le panneau Informations pour les pixels en dehors de la plage 0-1
* [Moteur][Texte] Nouveau crénage pour certaines polices
* [Graphe] Amélioration du temps d’invalidation lors de l’édition de sous-graphes profonds lors de l’utilisation de l’édition contextuelle
* [Linker] Ne pas dupliquer les bitmaps dans SBSASM
* [Paramètres] Ajouter un nouveau widget « fonction » pour tous les types de paramètre d&#39;entrée
* [Propriétés] Amélioration de l’affichage des paramètres hérités
* [UX] Amélioration de la prise en charge du pavé tactile (Mac uniquement)
* [UX] Moderniser le panoramique lorsque vous atteignez la bordure du graphe lors de la sélection
* [UX] Supprimer la fonctionnalité « Désactiver la haute résolution »
* [Branding] Nouveau branding pour l&#39;écran de démarrage et la fenêtre À propos
* [Map de dégradé] Ajout d’un moyen de déplacer toutes les touches et de créer une boucle
* [Bibliothèque] Basculer tous les filtres par défaut en casse de phrase
* [API] Ajout d’une méthode pour mettre en cadre un nœud spécifique dans le viewport de Vue du graphe
* [API] Ajout d’une méthode pour l’ouverture d’une ressource de package dans son éditeur (par exemple, un graphe de Substance dans la Vue du graphe)
* [API] Ajout d’une méthode pour sélectionner une ressource de package dans l’Explorateur (par exemple, un graphe de Substance)
* [API] Ajout de méthodes pour obtenir et définir le type de graphe d’un graphe de composition de Substances
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2023
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2024
* [Tiers] Mise à jour de Boost vers 1.82.0 + USD vers 23.08
* [Tiers] Mise à jour NGL vers 1.38
* [Tiers] Mise à jour d’OpenColorIO vers la version 2.3.x
* [Tiers] Mise à jour d’OpenExr vers la version 3.2.x
* [ThirdParty] Mettre à jour OpenSubdiv vers la version 3.6.x
* [ThirdParty] Mettre à jour Python vers 3.11.x
* [Tiers] Mise à jour de Qt vers la version 6.5.x
* [ThirdParty] Mettre à jour gcc vers la version 11.2.1
* [ThirdParty] Mettre à jour glibc vers 2.28
* [Tiers] Mettez à jour libstdc++ ABI vers C++11 one
* [Documentation] Nouvelle page Glossaire

<b>Fixe :</b>

* [Bakers] Crash lors de la modification de la scène dont le nom de fichier a été modifié
* [Bakers] Crash lors de l’enregistrement du paramètre prédéfini bakers dans Fichier JSON
* [Contenu] &#39;Dispersion sur la spline&#39; : Exposer le paramètre alpha de l&#39;Image d&#39;entrée
* [Contenu] « Couleur Sampler de la vignette » : expression visible manquante
* [Contenu] Bruit anisotrope : une valeur négative pour la quantité X/Y produit un résultat erroné
* [Contenu] Bruit anisotrope : problème de répétition lors de l’utilisation de valeurs impaires comme quantité X et sans smoothness
* [Contenu] Fonction de distribution normale : max() mal placé peut conduire à NaN
* [Content] Les ombres RTAO, Bent Normal et RT ne fonctionnent pas correctement sur certaines plateformes
* [Contenu] Couleur de la Fusion des éclaboussures de forme : les maps normal OpenGL ne sont pas fusionnées correctement
* [Contenu] Espace non garanti après le préfixe « Multi » dans les étiquettes de nœuds
* [Dépendances] Crash lors du déplacement de graphe dans ou entre les packages
* [Moteur] Erreur de précision dans les nœuds de déformation affectant les nœuds de flou de Pente
* [Moteur] Le calque SBSAR dans SD ne peut pas lire SBSAR avec du contenu SBSASM > 2 Go
* [graphe de fonction] Résultat incorrect pour 0^n
* [Graphe] L&#39;option « Afficher la taille du nœud » est mal étiquetée
* [Graphe] Crash lors de la copie d’un commentaire parent vers un autre graphe
* [Graphe] Blocage lorsque l’option Alt fait glisser un nœud Point
* [Graphe] La recherche de nœud peut manquer des correspondances évidentes dans certains cas
* [Graphe] Problème de performances lors de la modification d’un graphe de fonction instancié plusieurs fois avec un supergraphe ouvert
* [Graphe] Trop d’invalidations lors de la création d’une sortie
* [Security] Vulnérabilité d&#39;écriture hors limites d&#39;analyse ICO
* [Sécurité] Certains formats d’image inutilisés sont obsolètes
* [Paramètres] Le chemin de la ressource Bitmap PKG ne doit pas être modifiable
* [Paramètres] Correction des problèmes liés à l’expose/l’expose par lots du paramètre d’un processeur de valeurs
* [Paramètres] Les paramètres de chaîne sont ignorés lors de l&#39;expose par lots
* [Propriétés] Problème de performances lors de la modification d’un graphe de fonction instancié plusieurs fois avec des propriétés ouvertes
* [SVG] Les modifications apportées aux formes ne sont pas appliquées à l’image pixellisée
* [UI] Correction de certains bugs/incohérences avec les widgets défilants (Windows uniquement)
* [UI] Ordre incohérent des formats de fichier Scène 3D dans les listes d’importation/exportation
* [UI] Les actions de la fenêtre sont dupliquées dans l’interface utilisateur
* [Gestion de versions] Le script &#39;perforce.py&#39; ne fonctionne pas sur Python 3

## Version 13

### 13.1.2

*(Publié Le 16 Avril 2024)*

<b>Ajouté :</b>

* [Graphe] Ne placez pas de nœuds dupliqués au-dessus du nœud d&#39;origine
* [Graphe] Améliorer l’alignement des commentaires joints aux nœuds
* [Graphe] Amélioration du déplacement des commentaires
* [Graphe] Contraindre les cadres collés/dupliqués et les commentaires à la grille
* [Cadre] Contraindre de nouveaux cadres et commentaires à la grille
* [Contenu] « Courbure fluide » : ajoutez une note sur la prise en charge des répétitions dans la description
* [3DView][Iray] Autoriser l&#39;affectation de la sortie int au paramètre enum
* [AxF] Ajout de propriétés concernant le modèle de pelage transparent
* [AxF] Amélioration de la gestion des erreurs lors de l’exportation
* [AxF] Amélioration de la GLSLFX et des Matériaux MDL pour la représentation « SVBRDF » telle que stockée dans un Fichier AxF
* [AxF] Supprimer la propriété « CC No Refraction » du modèle « AxF vers AxF »
* [AxF] Renommez les propriétés « properties.has\_xxx » en « properties.has\_xxx ».
* [AxF] Mettez à jour le modèle pour inclure toutes les propriétés utilisées par nos shaders SVBRDF

<b>Fixe :</b>

* [vue 3D] Crash lors de la réinitialisation d&#39;un paramètre MDL Int mappé à une énumération MDL
* [vue 3D] Widgets incorrects pour les propriétés SVBRDF shader lorsque le matériau est réinitialisé après la modification de Scène 3D
* [vue 3D] Widgets incorrects pour les propriétés SVBRDF shader lorsqu’aucun graphe n’est appliqué.
* [vue 3D] Le bouton Afficher l&#39;environnement est désactivé pour les nouvelles vues sans fichier SBSSCN par défaut
* [vue 3D] Le passage d’un moteur de rendu Iray à OpenGL déconnecte une sortie du graphe
* [AxF] La variante Fresnel n&#39;est pas mise à jour par sortie du graphe
* [AxF] Le format des libellés des propriétés de shader AxF est incohérent
* [AxF] Les avertissements relatifs aux ressources inchangées n’apparaissent que dans la console
* [Contenu] « Non uniforme » n’est pas écrit de manière cohérente dans tous les nœuds.
* [Contenu] Dispersion sur la spline : motifs manquants sur les splines de pont
* [Contenu] Mappeur de splines : se bloque lors de la définition d’une valeur négative « Quantité de segment »
* [Contenu] « Symétrie » : les libellés sont manquants et incohérents
* [Graphe] Les commentaires existants sont légèrement décalés
* [Security] Vulnérabilité de lecture hors limites d&#39;analyse de fichier RAS

### 13.1.1

*(Publié Le 8 Février 2024)*

<b>Ajouté :</b>

* [AxF] Ajout de propriétés booléennes hasClearCoat, hasSheen, etc.
* [AxF] Ajout de propriétés manquantes
* [AxF] Autoriser l’importation de fichiers EP-SVBRDF
* [AxF] Renommer les propriétés « anisotropic », « fresnel » et « fresnel variant »
* [AxF] Mise à jour vers AxF-Editing 1.0.0
* [Graphe] Coller à la position de la souris si elle se trouve à l’intérieur de la Vue du graphe
* [UX] Augmenter l&#39;height du champ de texte « Description » du Cadre et du commentaire
* [UX] Mise en évidence des champs d’édition de texte lors de la création de Cadres, de commentaires ou d’Épingles

<b>Fixe :</b>

* [AxF] Les valeurs de mappage « Couleur Specular » sont incorrectes lors de l’exportation.
* [AxF] L’aperçu et les textures ne s’affichent pas correctement dans la boîte de dialogue « Importer AxF »
* [AxF] La propriété « CC No Refraction » n&#39;est pas injectée correctement dans le modèle « AxF to AxF »
* [Contenu] « Flood Fill à la position » est absent de la bibliothèque
* [Contenu] « Splatter Circular » : les valeurs négatives « Pattern Amount » entraînent des calculs très longs et intenses
* [Contenu] &#39;Liste de fusion spline&#39; : ordre d&#39;entrée incorrect
* [Dépendances] La dépendance est remappée sur sa copie après avoir été enregistrée en tant que copie
* [Cadre] Le bouton Activer le balisage de HTML n’est pas activé lors de l’annulation de son utilisation
* [Cadres] La sélection d’un cadre et de son contenu via l’outil Rectangle de sélection entraîne le déplacement de l’ensemble du contenu du cadre lors de la décomposition automatique
* [Graphe] Les commentaires dupliqués à partir de commentaires parents sont toujours placés à l’origine du graphe
* [Graphe] Le saut de ligne dans Commentaire est plus dur à la création
* [Publish] Définir le chemin par défaut pour la publication SBSAR sur le dossier « Mes documents »
* [SBSAR] Le rétablissement de la charge SBSAR la rend modifiable et ses données peuvent être perdues

### 13.1.0

*(Publié Le 12 Décembre 2023)*

<b>Ajouté :</b>

* [Cadre] Développement automatique
* [Cadres] Modification des règles pour définir quand un objet appartient à un cadre
* [Cadre] Désactiver la mise à l’échelle du texte pour la description cadre
* [Cadre] Taille adaptée au contenu
* [Cadre] Nouveaux états par défaut, survol et sélectionné
* [Cadre] Contraindre sur Grande Grille
* [Cadre] Code de HTML de prise en charge pour la description Cadre
* [Cadre] Mise à jour des zones d’interaction
* [Cadre] Mise à jour de l’aspect visuel
* [Graphe] Crée le nœud au milieu du lien visible au lieu du milieu du lien
* [Graphe] Afficher les propriétés d’un élément s’il est le seul élément avec des propriétés disponibles dans une sélection
* [Graphe] Supprimer l’option « Mise à l’échelle » pour les commentaires dans le graphe
* [Graphe] Contraindre les nœuds sur la grille principale lors du copier/coller
* [UX] Autoriser la recherche floue dans le menu Nœud et la recherche dans la bibliothèque
* [UX] Effectuer une boucle dans la liste du menu Nœud
* [AxF] Prise en charge de l’exportation AxF
* [AxF] Désactiver AxF sous Linux
* [API] Définissez la propriété « Visible if » des paramètres, entrées et sorties de graphe à l’aide de l’API Python
* [API] Définition de l’ordre des E/S de graphe à l’aide de l’API Python
* [Dépendances] Mettre à jour Boost vers 1.80.0
* [Dépendances] Mettre à jour OpenSubdiv vers la version 3.5.x
* [Dépendances] Mise à jour gcc vers la version 11.2.1 - Problème Iray/MDL C++20
* [Dépendances] Mise à jour du SDK FBX vers 2020.3
* [Dépendances] Mettre à jour NGL vers 1.35.0.20
* [Gestion des couleurs] Ajout de la prise en charge des écrans OCIO ICC
* [Levels] Ajouter un moyen de réinitialiser l&#39;histogramme
* [Python] Avertir les utilisateurs si QtForPython ne peut pas être importé
* [Vue 2D] Enregistrement de l’état des options d’affichage
* [vue 3D] Ajout d’une technique de positionnement au shader Informations sur le maillage
* [Exporter] Ajoutez un bouton « Enregistrer les paramètres » pour enregistrer les modifications apportées aux options d’exportation.

<b>Fixe :</b>

* [vue 3D] Impossible d&#39;attribuer une texture à une entrée de type texture\_2d d&#39;un Matériau MDL
* [AxF] Les identifiants de Graphe dans la liste des modèles peuvent être vides
* [AxF] Le champ de modèle de graphe de Substance est vide par défaut
* atlas scatter [Contenu] : comportement incorrect dans des cas spécifiques
* [Contenu] Mappeur de Flood Fill : sortie vide lorsque toutes les formes ont la même taille de boîte de dialogue
* [Content] FloodFill à la position : artefacts d’imprécision dans certaines situations
* [Contenu] Sortie « Specular » incorrecte dans le nœud « BaseColor/Métallique/Rugosité converter »
* [Contenu] L’option Masquer sur tracé ne fonctionne pas à la verticale
* [Contenu] Description manquante pour les nœuds Valeur d’entrée, Niveaux de gris en entrée, Couleur d’entrée et Sortie
* [Contenu] Description manquante pour les nœuds Set et Sequence
* [Contenu] Éclaboussure de forme : artefacts d’imprécision dans la sortie « Splatter data 2 »
* [Moteur] Les valeurs booléennes dans les Processeurs de valeurs sont toujours évaluées sur « False » (Apple Silicon uniquement).
* [Explorateur] L’ordre des boutons de la barre d’outils est incohérent entre les systèmes d’exploitation
* [Cadres] N’attrapez pas les nœuds lorsque vous déplacez un cadre avec le modificateur CTRL
* [Map de dégradé] l’option réinitialiser tout doit également réinitialiser le widget de dégradé
* [GraphRender] Certains nœuds deviennent noirs lors de l’ajustement en mode aperçu
* [Graphe] L’aperçu de « Valeur d’entrée » est bloqué sur « False » lors de l’ajustement de la valeur booléenne par défaut (Apple Silicon uniquement)
* [Graphe] Les nœuds de point proches du bord Cadre ne sont pas déplacés par le Cadre
* [Interopérabilité] L’icône Renvoyer n’est pas mise à jour après l’envoi à Substance 3D Stager
* [MDL] Impossible de modifier la Rugosité dans les nœuds où ce paramètre est disponible
* [MDL] Connexions non valides dans le modèle « AxF to Métallique rugosité »
* [UI] La fenêtre « Exporter les sorties » peut être réduite (Windows uniquement)
* [UI] Les images apparaissent pixellisées dans l’écran À propos lors de l’utilisation de la mise à l’échelle de l’affichage
* [UI] Les outils d’alignement de nœud de la barre d’outils graphe créent plusieurs étapes d’annulation.

### 13.0.2

*(Publié Le 27 Juillet 2023)*

<b>Ajouté :</b>

* [graphe de fonction] Ajouter une variable système $getPhysicalSize
* [Écran d’accueil] Prise en charge de l’ouverture des fichiers SBS par glisser-déposer
* [Content] Mappeur de spline/Mappeur de flux de spline : ajout d’un paramètre de correction non carrée

<b>Fixe :</b>

* [Écran d’accueil] Ne pas afficher l’écran d’accueil lorsqu’un fichier est envoyé à partir d’un autre logiciel
* [Écran d’accueil] État incorrect de l’icône Designer dans la barre d’outils Windows
* atlas splitter de [Content] : description incorrecte
* [Contenu] Valeur de référence incorrecte dans la fonction « Linéaire à sRVB (luminance) »
* [Contenu] L’outil d’affichage des nombres ne prend pas en charge les résolutions non carrées
* [Contenu] Liste de points : la valeur minimale du paramètre « Numéro de point » est incorrecte
* [Contenu] Ombre portée de la forme : l’ombre peut disparaître lorsque la répétition est désactivée
* [Contenu] Spline (polyquadratique) : tangentes et thickness de prévisualisation incorrects dans les résolutions non carrées non corrigées
* [Contenu] Spline (polyquadratique) : les libellés de points ne sont pas masqués lors de l’utilisation des options de connexion de début/fin
* [Contenu] Pont spline (liste) : le paramètre Correction non carrée n&#39;a aucun effet
* [Contenu] Spline cubique : le paramètre Correction non carrée n’a aucun effet sur la sortie Aperçu
* [Contenu] Mappeur de splines : rendu incorrect lorsque la spline a un très petit thickness
* [Content] Nœuds splines : description du signe alpha inversé dans l’info-bulle des couleurs splines
* [Contenu] Nœuds splines : le paramètre Correction non carrée n’a aucun effet sur la sortie de l’aperçu
* [Contenu] Rendu spline : format de sortie absolu 32F
* [Contenu] Rendu spline : la sortie est verrouillée dans une plage [0, 1]
* [Contenu] Exemple de Thickness spline : la spline peut être soustraite en valeurs négatives
* [Contenu] Sélection de splines : par défaut, les splines sont fermées par un seul segment
* [Crash][Cuiseur] Crash lors du chargement de graphes spécifiques
* [Crash][Interface utilisateur] Crash lors de l’activation des menus après le chargement du package depuis l’écran d’accueil
* Le lien [API] « Documentation de l’utilisateur » dans la référence des scripts est obsolète
* [Propriétés] Impossible d&#39;ouvrir la fonction de Processeur de valeurs sur un graphe verrouillé
* [Publish] Impossible de publier des packages contenant des Graphes MDL
* [UI] L’option « Gérer mon compte... » est désactivée dans le menu Aide
* [UI] Entrées manquantes dans le menu Aide lors de l’ouverture de Designer via un fichier

### 13.0.1

*(Publié Le 27 Juin 2023)*

<b>Ajouté :</b>

* [Contenu] Spline (polyquadratique), Liste de points : ajoutez le nom des points dans la sortie d’aperçu
* [Content] Spline Mapper : ajoute un paramètre pour décaler le centre du profil du cylindre
* [DotNode] Trie la liste des portails d’entrée par ordre alphabétique

<b>Fixe :</b>

* [Content] Résultat incorrect dans plusieurs nœuds Spline lors de l&#39;utilisation d&#39;une distribution uniforme
* [Contenu] Erreurs mineures dans les info-bulles des nœuds Spline et Tracé
* [Contenu] Quad Transforme on Path : les valeurs par défaut p01 et p10 sont permutées
* [Contenu] Quad Transforme : résultat incorrect dans une situation spécifique
* [Contenu] Cercle spline : le résultat « Inverser la direction » est incorrect lorsque la distribution uniforme n’est pas utilisée
* [Contenu] Cercle spline : les tangentes sont incorrectes lors du réglage des paramètres de spirale et de taille
* [Contenu] Spline Flow Mapper : des traînées noires apparaissent lorsque la puissance en spirale est élevée dans Spline Circle
* [Contenu] Mappeur de spline/Mappeur d’UV : la couleur d’arrière-plan ne fonctionne pas
* [Contenu] Spline Mapper : l’height de base est 0, ce qui entraîne un écrêtage
* [Content] Mappeur de spline : l&#39;height de la spline est modifié par le multiplicateur d&#39;entrée même lorsque cette entrée n&#39;est pas connectée
* [Content] Mappeur de splines : les extrémités de splines qui rencontrent un bord d&#39;image ne sont pas mappées
* [Contenu] Mappeur de spline : l’Échelle UV Y n’a aucun effet lors de l’utilisation d’une forme non plane
* [Content] Mappeur de splines : combat contre les Z lors du rendu de splines se chevauchant du même height
* [Contenu] Poly quadratique spline : le résultat « Inverser la direction » est incorrect lorsque la distribution uniforme n’est pas utilisée
* [Contenu] Rendu spline : les liaisons ne sont pas gérées de manière cohérente dans les options de style de spline
* [Contenu] Rendu spline : le dernier segment n’est pas dessiné
* [Contenu] Rendu spline : correction non carrée non appliquée correctement
* La couleur du mappeur d&#39;UV [Contenu] apparaît deux fois dans la bibliothèque
* [DotNode] La zone de contraint de connexion n&#39;est pas mise à jour après la désactivation de la limite de mise à l&#39;échelle du texte
* [DotNode] La création via le menu contextuel est interrompue
* [DotNode] La position du nom de portail d&#39;entrée n&#39;est pas ajustée après l&#39;annulation/la répétition d&#39;un changement de nom
* [GraphRender] Trop d’invalidations lors de la modification d’un graphe de fonction
* [Graphe] La position du widget de transformation n’est pas mise à jour visuellement correctement
* [Localisation] Les champs « Plage souple » et « Plage dure » ne sont pas localisés dans les Graphes MDL
* [Paramètres] Les modifications de texte consécutives ne sont pas enregistrées dans la pile de données d’historique
* [Paramètres] Hitbox pour déplacer des paramètres d&#39;entrée de graphe dans la liste n&#39;est pas fiable
* [Propriétés] Le clic simple est considéré comme double sur le widget de zone de rotation pour les projets lourds
* [Publish] L’ordre des ressources dans le package n’est pas conservé dans la ressource publiée

### 13.0.0

*(Publié Le 6 Juin 2023)*

<b>Ajouté :</b>

* [Graphe] Nœud de portail
* [Intégration] Nouvel écran d’accueil
* [Content] Nœud spline (cubique)
* [Contenu] Nœud spline (polyquadratique)
* [Contenu] Nœud de cercle spline
* Nœud Liste de points [Contenu]
* [Content] Nœud Spline Bridge (2 splines)
* [Content] Nœud Spline Bridge (List)
* [Content] Nœud Spline Append
* [Contenu] Nœud de sélection de spline
* [Contenu] Nœud de la liste de fusion spline
* [Content] Nœud de Transforme Spline 2D
* [Contenu] Nœud de déformation de spline
* [Content] Nœud d&#39;Height d&#39;échantillon spline
* [Content] Nœud de Thickness d&#39;exemple de spline
* [Contenu] Nœud de rendu spline
* [Contenu] Dispersion sur le nœud Couleur de spline
* [Contenu] Dispersion sur le nœud Niveaux de gris spline
* [Content] Nœud Couleur du mappeur de spline
* [Contenu] Nœud Niveaux de gris du mappeur de spline
* [Content] Nœud de couleur du mappeur de pont spline
* [Content] Nœud Niveaux de gris du mappeur de pont spline
* [Content] Nœud du mappeur de flux spline
* Nœud Couleur du mappeur d&#39;UV [Content]
* [Contenu] Nœud Niveaux de gris du mappeur d&#39;UV
* [Contenu] Nœud Tracés vers splines
* [Contenu] Nœud Masques vers tracés
* [Contenu] Tracés 2D Transforme nodenode
* [Contenu] Tracés Nœud Polygone
* [Contenu] Nœud Chemins d’accès d’aperçu
* [Contenu] Nœud Déformation des tracés
* [Contenu] Nœud de sélection des tracés
* [Contenu] Chemins d&#39;accès Nœud Processeur de Vertex
* [Content] Chemins Processeur de Vertex Nœud simple
* [Contenu] Quad Transforme sur le nœud de chemin
* [Contenu] Ambient occlusion Lancer de rayon v2
* [Contenu] Courbure Lancer De Rayon Normal v2
* [Contenu] Ombres vectorisées avec rayon v2
* [Moteur] Mise à jour vers la version 9
* [Moteur] Nœud de boucle dans les graphes de fonction
* [Moteur] Ajouter le mode solide au dégradé
* [Moteur] Nœud pow() atomique dans le Graphe de fonction
* [Moteur] Ajout d’options d’habillage de bordure (serrage sur le contour/répétition) dans le nœud Sampler
* [Moteur] Échantillonnage le plus proche dans le nœud de déformation et de Déformation directionnelle
* [Moteur] Ajout d’un mode « alpha pénétrant » au filtre Netteté pour les entrées de couleur
* [Moteur] FxMap : morphlet de l&#39;hémisphère
* [Moteur] Opérations Get/Set atomiques dans les graphes de fonction
* [Moteur] Fonctions : utiliser la fonction précise de log/log2/exp, 2pow - Unifier les fonctions entre le cuiseur et le moteur
* [Moteur] Ajout d’un paramètre « décalage d’intensité » au filtre Déformation directionnelle
* [API] Prise en charge de la gestion des paramètres prédéfinis pour les graphes de composition
* [Fonctions] Modifier le nom d&#39;entrée pour les noeuds atomiques de fonctions
* [Localisation] Ajouter Portugais (Brésil), Italien (Italie) et Espagnol (Espagne)
* [Localisation] Respectez la règle « Langue (Pays) » dans la liste des langues
* [Paramètres prédéfinis] Désactiver les panneaux « Aperçu » et « Paramètres prédéfinis » dans les propriétés de graphe lors de l’utilisation de l’édition contextuelle
* [Substance models graphe] Fin de la prise en charge des modèles de Substance graphes

<b>Fixe :</b>

* [vue 3D] L’affichage des chaînes longues dans les statistiques de scène est coupé (macOS uniquement)
* Le module [API] &#39;structure::Structure&#39; est toujours inclus dans la référence API
* [API] Les nœuds point dans les Graphes MDL n’ont aucune définition ni propriété
* [API] Comportement incorrect lors de la définition du paramètre des noeuds de fonction
* [Contenu] 3D Voronoi et 3D voronoi fractal nodes génèrent un avertissement de cuisson
* [Moteur] Le paramètre « Décalage de la carte d’intensité » n’a aucun effet sur les données en niveaux de gris dans le moteur SSE2
* [Explorateur] les e/s de Graphe peuvent être supprimées
* [Graphe] Le bitmap est ignoré lorsqu’il est utilisé dans des occurrences
* [Graphe] Position de nœud de point incorrecte lors de la création d&#39;un nœud à partir d&#39;un nœud
* [Graphe] Focus incorrect dans la boîte de dialogue « Exposer le paramètre » lors de l&#39;utilisation de la touche « Entrée »
* [Graphe] Résultat incorrect lors de la numérisation d’histogramme avec un bitmap dans l’édition du contexte
* [Localisation] Correction de divers problèmes d’écrêtage
* [Paramètres] Crash lors de la suppression d’un paramètre d&#39;entrée
* [Publish] Les Graphes des dossiers sont déplacés à la racine dans le package publié
* [Ressources] Crash lors de la mise à jour d&#39;une ressource chargée sur le disque
* [VisibleIf] Correction de la régression dans l’évaluation de la visibilité conditionnelle

## Version 12

### 12.4.1

*(Publié Le 30 Mars 2023)*

**Ajouté :**

* [Cooker][Graphe] Prendre en compte les balises de transformation EXIF dans le fichier JPEG
* [Sécurité] Mise à niveau vers USD 23.02
* [Sécurité] Supprimer la prise en charge de l’importation de format de fichier Collada (.dae)
* [Modèles de Substance] Avertissement concernant la fin de vie des Graphes Substance models dans la prochaine version majeure

**Fixe :**

* [vue 3D][ASM] Artefact de rugosité de revêtement lors de l’utilisation d’un CoatNormal
* [Contenu] Le paramètre « Cellules avec dégradé » du nœud Alveolus est inversé
* [Contenu] Le nombre d&#39;entrées des nœuds à commutateurs multiples n&#39;est pas verrouillé
* [Contenu] Avertissement de cuisson dans le nœud Normal de Scratches Generator
* [Données] Crash lors du chargement manuel du package après l&#39;annulation de son chargement précédent
* [Données] Crash lors de l’annulation rapide de plusieurs opérations de graphe jusqu’au chargement du package

### 12.4.0

*(Publié Le 31 Janvier 2023)*

**Ajouté :**

* [vue 3D] Ajouter toutes les options dans le menu Afficher sous forme de boutons de barre d’outils
* [API] Autoriser l’ajout d’actions aux barres d’outils de vue du graphe
* [API] Autoriser à créer/modifier/évaluer un Graphe Substance model à partir de l’API
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D bakées en mode ACE
* [Documentation] Exemples de projets pour les graphes de composition de Substances
* [Documentation] Projet d’exemple pour les graphes de fonction
* [Explorateur] Autoriser le déplacement du Graphe et des ressources d’un parent à un autre sans fermer ni invalider les widgets
* [Éditeur de dégradé] Sélectionnez l’épingle sélectionnée lors de l’affichage de l’éditeur de dégradé
* [Graphe] Ajouter une option dans le menu contextuel d’un nœud pour sélectionner tous ses enfants
* [Graphe] Nettoyer l&#39;outil de graphe pour détecter et supprimer les nœuds inutilisés dans tous les types de graphes et graphes de propriétés
* [Graphe] Transformer l’entrée d’image sur couleur/niveaux de gris
* [Paramètres] Ajouter un verrou sur les widgets entier 2
* [Paramètres] Permet de saisir des formules de base comme paramètre
* [Substance] Basculez entre les valeurs et les icônes pour les nœuds de valeur.
* [UI] Bouton permettant de générer une valeur aléatoire lorsqu’un générateur aléatoire est requis
* [UI] L&#39;élément ciblé n&#39;est pas mis en surbrillance dans le navigateur de Scènes
* [UX] Réinitialiser les plages de curseur lorsque leur valeur est réinitialisée

**Fixe :**

* [API] SDProperty.getDefaultValue() renvoie presque toujours None
* [vue 3D] La valeur de la propriété « Normal » n’est pas partagée entre les moteurs de rendu
* [vue 3D] L&#39;affichage des statistiques de Scène est étiré lorsque le viewport est petit
* [vue 3D] La propriété d&#39;affichage Structure filaire n&#39;est pas enregistrée
* [Contenu] Les paramètres Couleur de flou radial n’ont aucun effet sur le canal Alpha
* [Localisation] Des curseurs et des boutons supplémentaires s’affichent dans les propriétés OpenGL de l’environnement.
* crash [MDL][modèle de Substance] lors de la suppression de nœuds exposés
* [Préférences] Le fichier par défaut\_config n’est jamais recréé s’il est supprimé
* Paramètre de réorganisation de Crash [modèle de Substance] qui n&#39;apparaît pas au niveau de l&#39;instance

### 12.3.1

*(Publié Le 24 Novembre 2022)*

**Ajouté :**

* [3DView] Rendu optimisé pour les scènes avec de nombreux matériaux
* [3DView] Affichage des sorties d’un Graphe Substance model en le déposant de l’Explorateur
* [Licence] Système hérité propre pour les utilisateurs de Linux
* [Intégration] Mettre à jour la transparence de l’arrière-plan
* [Modèles de Substance] Affiche un avertissement dans la Vue du graphe lorsque l’entrée et la sortie partagent le même identifiant

**Fixe :**

* [Ressources 3D] « Aide > Ressources Substance 3D » cible par erreur le bureau Creative Cloud sous Linux
* [vue 3D] Les Matériaux ne sont pas créés lorsque le maillage est chargé
* [vue 3D] La liste Matériaux s’ouvre lors de la suppression de Graphe Substance model dans le viewport
* [Explorateur] Impossible de supprimer la sélection avec le clavier si un Graphe Substance model est inclus
* [Explorateur] Crash lors de l’ouverture du menu contextuel d’un élément de matériau d’une ressource de maillage sur Mac
* [Graphe] Les instances dont les Images d&#39;entrée dépendent de valeurs génèrent un résultat erroné dans les nœuds suivants
* [Graphe] Résultat incorrect lors de l’utilisation de la chaîne de sous-graphes avec l’édition de graphe contextuelle activée
* [MDL] Crash lors du chargement d’un Graphe MDL faisant référence à un graphe de composition avec des sorties obsolètes
* [MDL] Le nœud 2D de Texture ne fonctionne plus
* [Intégration] Texte recadré et non localisé
* [Intégration] Les panneaux ne s’affichent pas correctement lors du lancement de l’application via l’ouverture d’un fichier
* [Préférences] Le cache d’image ignore l’emplacement des fichiers temporaires défini par l’utilisateur
* [Propriétés] Les réglages effectués dans les panneaux Aperçu/Paramètres prédéfinis sont fusionnés dans la pile Annuler
* [Raccourci] Le Raccourci attribué sur des nœuds obsolètes crée des conflits et ne peut pas être nettoyé
* crash [modèles de Substance] lors de la fermeture d’un pack après avoir effectué des actions spécifiques
* [modèles de Substance] Les Instanciers et les liens des packages redéfinis l&#39;emplacement ne sont pas actualisés correctement
* [Modèles de Substance] L’annulation de la suppression des sous-graphes n’actualise pas les instanciers et les liens de manière cohérente
* [Modèles de Substance] La valeur augmente soudainement trop vite sur le nœud de transforme
* [UI] Les icônes d’avertissement de la propriété « Visible si » n’ont pas d’info-bulle
* [UI] Le texte des informations de l’image est trop sombre dans le viewport de vue 2D
* [Annuler] Le déplacement d’un widget de position en mode aperçu stocke toutes les valeurs intermédiaires

### 12.3.0

*(Publié Le 6 Octobre 2022)*

**Ajouté :**

* [Général] Panneau d’intégration pour accueillir les nouveaux utilisateurs
* [Général] Panneau Nouveautés pour améliorer la découvrabilité des nouvelles fonctionnalités
* [Modèle de Substance] Prise en charge des sous-graphes et des instances
* [Substance] Prise en charge visible si pour les paramètres exposés
* [Modèle de Substance] Ajout de la prise en charge des nœuds de sortie
* [modèle de Substance] Nœud de décalage de courbe
* [modèle de Substance] Nœud de retournement de courbe
* [modèle de Substance] Nœud de lissage de courbe
* [modèle de Substance] Nœud de subdivision de courbe
* [modèle de Substance] Nœud de greffe
* [Substance model] Mettre à jour le nœud « Filter Scène »
* [Substance] Rendre les non-noeuds atomiques détectables dans le menu Nœud
* [Substance] Ajouter l’action « Ouvrir la référence » dans le menu contextuel d’un instancier
* [Modèle de Substance] Ajoutez une action « Afficher dans 3DView » dans le menu contextuel des nœuds pouvant être envoyés à 3DView
* [Modèle de Substance] Affiche automatiquement les propriétés d&#39;un nœud après l&#39;avoir exposé
* [Substance] Création d’une fenêtre « Nouveau Graphe Substance model » avec la liste des modèles
* [UI] Amélioration de la cohérence des options d’enregistrement d’images dans vue 2D et vue 3D
* [UI] Renommez « Lien > maillage 3D » en « Lien > scène 3D » dans le menu contextuel de l’Explorateur
* [UI] La réinitialisation de la disposition s’applique désormais à toutes les fenêtres flottantes
* [UI] Utiliser le libellé « Afficher les sorties en vue 3D » dans les menus contextuels pour les graphes
* [Library] Prise en charge des Graphes Substance models non atomiques
* [SBSAR] Description des sorties du graphe de soutien dans le SBSAR
* [Shader] Définir la valeur par défaut du facteur de Tessellation sur 1 pour tous les ombrages
* [UI] Exposer le widget à 2 boutons pour les paramètres booléens
* [Moteur] Mise à jour vers la version 8.6.4
* [Steam] Version optimisée pour le chipset Apple Silicon (Apple M1/M2)

**Fixe :**

* [UI] Résolution des problèmes de mise à l’échelle des écrans haute résolution
* [UI] Modèle &#39;$(udim)&#39; manquant dans la liste de la fenêtre de baking
* [UI] Crash lors de l’affichage du menu Nœud sur la bordure droite de l’écran (macOS uniquement)
* [UI] Le bouton Extension dans le menu de la vue 3D n’est pas visible
* [UI] Le menu d&#39;extension de la barre d&#39;outils Graphe est incomplet
* [UI] Valeur de widget de paramètre incorrecte après l’annulation de l’activation de la plage fixe
* [Vue 3D] Le paramètre de shader non par défaut est perdu lors de l’Iray d’une session à une autre
* [Bakers] Crash lors du chargement de la fenêtre de baking avec une scène sans maillages
* [Fonction] Crash lors de la copie d&#39;une instance dans son graphe référencé
* [Fonction] Correction des crashs possibles lors de la manipulation des nœuds
* [Globalisation] L’italique n’est pas toujours correctement désactivé en japonais/coréen/chinois
* [Graphe] identifiant de secours incorrect pour les nouveaux fichiers MDL et Graphes Substance models
* [Graphe] Les paramètres hérités pilotés par des valeurs sont parfois calculés de manière incorrecte
* [GraphRender] Crash lors du changement de moteur lors du calcul du graphe haute résolution (macOS uniquement)

### 12.2.1

*(Publié Le 4 Août 2022)*

**Fixe :**

* [Graphe] Résultats incorrects lors de la modification de la taille parent du graphe
* [Crash] Crash lors du calcul du graphe de composition de Substances à très haute résolution
* [Crash] Crash lorsque la mémoire est insuffisante lors du chargement du pack
* [Crash] Crash lors de l’utilisation de crochets dans les annotations d’un paramètre exposé dans un Graphe Substance model
* [Crash] Amélioration de la stabilité des graphes de composition de Substances de rendu
* [Iray] Mise à jour vers la version 2021.1.6

### 12.2.0

*(Publié Le 19 Juillet 2022)*

**Ajouté :**

* [Apple] Prise en charge native d’Apple Silicon (M1) (version pour Creative Cloud uniquement)
* [Graphe Substance model] Afficher les info-bulles des nœuds dans la Vue du graphe
* [Graphe Substance model] Afficher les info-bulles des nœuds dans la bibliothèque
* [Graphe Substance model] Ajout d’une entrée de menu contextuel pour prévisualiser les nœuds
* [Graphe Substance model] Autoriser l’utilisateur à créer des raccourcis pour la création de nœuds
* [UI] Ajouter l’option « Afficher la sortie en vue 2D » dans le menu contextuel du graphe de composition
* [UI] Fractionner le paramètre « Affichage automatique des sorties » en paramètres spécifiques à vue 2D/vue 3D
* [UI] Ajouter une flèche déroulante et une info-bulle au bouton « Afficher la sortie » dans la barre d’outils vue 2D
* [UI] Reformulation et réorganisation des éléments dans le panneau Informations de l’Explorateur
* [Gestion des couleurs] Ajoutez les espaces colorimétriques d’exportation Adobe RVB linéaire (1998) et Adobe RVB (1998) pour Adobe ACE.
* [Gestion des couleurs] Ajouter l’espace colorimétrique de travail « Linear Adobe RGB (1998) » pour Adobe ACE
* [Gestion des couleurs] Prise en charge des écrans OCIO ICC
* [Gestion des couleurs] Masquer l’espace colorimétrique de travail d’Adobe RGB dans les préférences ACE
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D bakées en mode ACE
* [Gestion des couleurs] Utiliser le nouveau back-end GPU dans la visionneuse 3D
* [Localisation] Mise à jour complète de la langue coréenne
* [Moteur] Mise à jour vers la version 8.6.0
* [Graphe] Affectez un identifiant de graphe par défaut lorsque cette propriété reste vide
* [Bibliothèque] Désactiver les hyperliens des info-bulles pour les non-instanciers
* [NewProject] Mise à jour de la résolution par défaut
* [Modèles] Ajouter un modèle CLO
* [API] Exposer la propriété defaultParentSize pour les objets SDSBSCompGraph
* [Dépendances] Mettre à jour Alembic vers la version 1.8.3
* [Dépendances] Mettre à jour AXF vers la version 1.9.0
* [Dépendances] Mettre à jour Boost vers la version 1.76
* [Dépendances] Mise à jour de FBX vers la version 2020.2.1
* [Dépendances] Mise à jour de l’Iray version 2021.1.0
* [Dépendances] Mettre à jour OpenColorIO vers la version 2.1.1
* [Dépendances] Mise à jour de l’OpenEXR version 3.1.5
* [Dépendances] Mettre à jour TBB vers la version 2020.3
* [Dépendances] Mettre à jour USD vers la version 0.22.3
* [Supprimer] Désactiver la fonction effets de post-traitement (Yebis)
* [Supprimer] Supprimer la commande « Enregistrer le rendu dans Artstation » du menu vue 3D

**Fixe :**

* [Modèles de Substance] La plage fixe définie sur le paramètre exposé est enregistrée lors de la désexposition
* [modèles de Substance] l&#39;Identifiant n&#39;est pas convivial sur les nœuds constants
* [Modèles de Substance] Améliorer la recherche en fonction de la compatibilité des nœuds
* [UI] L’ordre des sous-menus « Nouveau » est incorrect pour les ressources de dossier
* [UI] La taille par défaut de la fenêtre principale est très petite
* [UI] Les barres d’outils ne sont pas affectées par l’option « Réinitialiser la mise en page »
* [UI] grille de transparence visible sur l’icône de ressource de police dans Explorateur
* [Cuiseur] Les graphes de composition instanciés dans le Graphe MDL sont toujours entièrement recuits
* [Graphe] Crash lors du collage d&#39;un nœud copié à partir d&#39;un graphe avec un identifiant vide
* [MDL] Crash lors de la fermeture d&#39;un Graphe MDL spécifique
* [Performances] L’application ne répond pas lors du chargement de packs très volumineux
* [Resources] La ressource scène 3D peut être importée dans un cas spécifique

### 12.1.1

*(Publié Le 7 Juin 2022)*

**Fixe :**

* [Content] La ressource « bluenoise\_256 » a un attribut « colorspace » défini dans certains nœuds
* [Contenu] Les nœuds « Obtenir la taille » n’apparaissent pas dans la bibliothèque et la version en niveaux de gris est mal étiquetée
* [Contenu] Le paramètre « Random Color Seed » dans les nœuds 2D Voronoi n&#39;a aucun effet
* [SBSRender] L’exportation d’un graphe vers EXR ne génère pas le même bpc que Designer
* [Modèles de Substance] « Type de gamma » ne doit pas apparaître dans les propriétés du paramètre exposé
* [modèles de Substance] Crash lors de l’utilisation de crochets dans les annotations du paramètre exposé

### 12.1.0

*(Publié Le 26 Avril 2022)*

**Ajouté :**

* [Main] Nouveau contenu pour les graphes de matériau
* [Main] Envoyer des Matériaux à Stager
* [Principal] Prise en charge des fichiers USD
* [Principal] Amélioration du signalement des erreurs dans l’interface utilisateur
* [Principal] Nœuds de gestion des Scènes pour les graphes models
* [Contenu] Ajout d’options supplémentaires aux Bruits Perlin 3D (répétition, absolu...)
* [Contenu] Nouveau nœud fractal Bruit 3D ridged
* [Contenu] Nouveau nœud Décalage de Texture 3D
* [Contenu] Nouveau nœud de position de Texture 3D
* [Contenu] Nouveau nœud de surface de rendu de Texture 3D
* [Contenu] Nouveau nœud de volume de rendu de Texture 3D
* [Contenu] Nouveau nœud de Champ de distance signée de Texture 3D
* [Contenu] Nouveau nœud de recadrage automatique
* [Contenu] Nouvelles fonctions d’accélération
* [Contenu] Nouveaux nœuds Extend Shape
* [Contenu] Nouvelles Cartes D’Usure/salissures
* [Content] Nouveau nœud de rotation non uniforme
* [Content] Nouveau filtre Tableau de zones de somme
* [Contenu] Nouveau générateur Tile Random 2
* [Contenu] Nouveau générateur de motif de Triangle Grid
* [Content] Nouvelle version du nœud Quantize Grayscale
* [Contenu] Nouveaux Bruits fractaux Voronoi et Voronoi (2D/3D)
* [Contenu] Seuil : ajout du mode de comparaison « Inférieur » et « Inférieur et égal »
* [Content][vue 3D] Ajoutez un ajustement de maillage pour afficher les fabric dans les ressources livrées
* [Modèles de Substance] Nouveau nœud Développer les instances de groupe
* [Modèles de Substance] Nouveau nœud de Fuse
* [Modèles de Substance] Nouveau nœud Renommer
* [Modèles de Substance] Nouveau nœud Reparent
* [Modèles de Substance] Nouveau nœud Définir le pivot
* [Substance models] Mise à jour vers SDK 1.6.0
* [UI] Amélioration du comportement du menu Nœud en cas de clic incorrect
* [UI] Ouvrir les sous-graphes dans le même onglet, même épinglés
* [UI] Supprimer le bouton d’Épingle de la barre de titre du panneau Explorateur
* [UI] Enregistrer l’option « Ne plus afficher » sur l’écran de bienvenue dans toutes les versions
* [ThirdParty] Mettre à niveau Qt (et QtForPython) vers 5.15.8
* [Tiers] Mise à niveau de Python vers la version 3.9.9
* [Tiers] Mise à niveau d’OpenSSL vers la version 1.1.1m
* [vue 3D] Affichez l’unité de Grille dans le viewport lorsque l’assistant Axe est activé
* [Automatisation] Fournir l’outil de ligne de commande sbsbaker avec Designer
* [Gestion des couleurs] Implémentation d’un nouveau back-end GPU pour Adobe ACE
* [Cooker] Ajouter une option pour cuisiner un paquet sans horodatage
* [Graphe] Ajout de badges dans le graphe FxMap
* [Bibliothèque] Ajout d’un nouveau filtre pour les fonctions d’accélération
* Prise en charge d’USD par [Player]
* [Properties] Ajoutez une erreur d&#39;avertissement sur le paramètre « PKG Resource Path » d&#39;un nœud Bitmap lorsque la ressource est introuvable
* [Substance Engine] Mise à niveau vers la version 8.4.1
* [Yebis] Avertissez l&#39;utilisateur que les effets de post-traitement Yebis seront supprimés dans la prochaine version
* [Documentation] Nouvelle page « Avertissements et erreurs »
* [Documentation] Nouvelle page décrivant l’héritage dans les graphes de composition de Substances
* [Documentation] Mise à jour de la section « Iray »
* [Documentation] Mise à jour de la section « Graphes MDL »

**Fixe :**

* [UI] Problèmes d’écrêtage dans les info-bulles des modèles dans la nouvelle fenêtre de graphe
* [UI] Texte blanc difficile à lire dans les nœuds lors de l’utilisation du mode sombre dans macOS
* [UI] Problème de disposition dans certaines boîtes de dialogue
* [UI] Le message d&#39;avertissement s&#39;affiche tronqué lors de la création du graphe de fonction de Substance dans Explorateur.
* [UX] Le sélecteur de couleurs descend à chaque nouvelle ouverture
* [UX] La fenêtre de l’éditeur de dégradé s’ouvre à chaque apparition
* [UX] Les propriétés de Graphe ne s&#39;affichent pas automatiquement pour les packages chargés
* Mappeur de Flood Fill [Content] : sélection d&#39;entrée incorrecte dans un cas spécifique
* [Contenu] Flood Fill : fond perdu de texte dans les boutons de paramètres booléens
* [Contenu] Plage incorrecte pour le paramètre Angle du premier échantillon de lumière du nœud Plusieurs angles vers Normal
* [Modèles de Substance] Les propriétés du nœud affichent identifiant au lieu de libellé
* [Modèles de Substance][Vue 3D] Problème d’actualisation lors de la réouverture d’un projet
* [Modèles de Substance][3Dview] Problème d’actualisation lors de l’utilisation de l’aperçu structure filaire
* [Paramètres] Crash lors de la suppression d’entrées de graphe en succession rapide dans un cas spécifique
* [Paramètres] Crash lors de la réinitialisation d&#39;un paramètre d&#39;instance lors de la modification de sa description de référence
* [Bitmap] La détection UDIM n&#39;est pas déclenchée pour les fichiers bitmap déposés dans le graphe
* [Graphe] Les nœuds de bitmap/SVG ne sont pas invalidés lorsque la ressource est modifiée sur le disque après le chargement du package
* [GraphRender] Fuite de mémoire lorsque l’évaluation du graphe de Substance est annulée
* [Localisation] La chaîne « Rebake all maps for this resource » apparaît non localisée
* [MDL] Paramètre exposé initialisé à 0 si l&#39;entrée est connectée à un nœud Point non connecté
* [Préférences] Les info-bulles s’affichent même lorsque le curseur se trouve dans un espace vide
* [Propriétés] L’annulation d’une modification de la valeur d’espace colorimétrique définit la valeur par défaut dans un cas spécifique
* [Text] Impossible d&#39;annuler le changement de police vers une ressource de police manquante

## Version 11

### 11.3.3

*(Publié Le 1Er Février 2022)*

**Fixe :**

* [modèles de Substance] Les plages peuvent être perdues dans certains cas
* [Modèles de Substance][Exporter] L’échelle est différente selon le type de fichier
* [Modèles de Substance][Exportation] Maillages dupliqués

### 11.3.2

*(Publié Le 25 Janvier 2022)*

**Ajouté :**

* [Documentation] Mise à jour de la section « Iray »

**Fixe :**

* [modèles de Substance] Impossible de publier un package contenant des graphes de modèles de Substance
* [Modèles de Substance] Impossible d’exporter un graphe model dans certains cas spécifiques
* [Modèles de Substance] Amélioration de la cohérence des plages de paramètres
* [MDL] Crash lors de l’exportation d’un fichier MDLE
* [MDL] Fichier .mdl incorrect généré lorsqu&#39;un Graphe MDL contient des nœuds Point connectés à des Paramètres exposés
* [vue 2D] Optimisation de l’affichage des outils de peinture
* [Contenu] Paramètre de taille de sortie incohérent configuré dans les graphes source du modèle
* [Propriétés] Les libellés des plages souples/dures sont incorrects dans le panneau de propriétés pour les nœuds exposés aux modèles MDL et de Substance
* [Modèles] Mettre à jour les valeurs par défaut des entrées dans le modèle « Filtre Sampler »

### 11.3.1

*(Publié Le 13 Décembre 2021)*

**Ajouté :**

* [Graphe] Ajout d’un avertissement lors de la suppression d’un graphe utilisé dans un autre graphe/pack

**Fixe :**

* [UI] L’éditeur de couleurs est trop petit lors de l’utilisation d’une disposition d’interface utilisateur spécifique
* [UI] Crash lors de la mise à jour de la liste des modèles récemment utilisés
* [UI] Mise en surbrillance incorrecte dans les préférences de raccourcis
* [UI] La taille de la fenêtre principale est trop petite après le redémarrage d’une session en fenêtre (macOS uniquement)
* [UI] Le dock agrandi n’est pas réduit en sortie (Windows uniquement)
* [UI] Espace manquant dans l’info-bulle du paramètre « Sortie haute du niveau »[3DView] L’Axe dans la vue 3D est trop petit lorsque le cadre de sélection de la scène est fin
* [UI] Problème de style sur certains textes dans les paramètres du projet en français
* [modèles de Substance] Les Verrouilles de paramètres exposés ne sont pas enregistrées entre les sessions
* [Modèles de Substance] Le modificateur Maj est toujours activé après l’utilisation du raccourci Aperçu des nœuds
* [Modèles de Substance] Certains nœuds supprimés restent dans le SBSM exporté
* [Modèles de Substance] Les nœuds cibles de l’évaluation s’accumulent et ne sont pas supprimés[API] Crash lors du rendu des nœuds Courbe dont les propriétés ont été définies via l’API
* [Baker] le widget « Couleur du Matériau » n’est pas visible et ne fonctionne pas comme prévu
* [Contenu] Nœud Rendu PBR : calcul interne non effectué à la résolution du nœud
* [Graphe de fonction] Les messages affichant les types attendus sont erronés dans certains cas
* [Graphe] Entrée relative à l’entrée : les paramètres hérités sont incorrects avec les instances connectées
* [MDL] Les instances de graphe de Substance ne sont pas mises à jour de manière fiable dans les Graphes MDL
* [Publish] Échec du graphe de publication contenant des dépendances circulaires
* [Raccourcis] Les touches Maj + Espace ne doivent pas être un raccourci de clavier assignable pour les nœuds
* [Modèles] Le format de sortie des modèles personnalisés est ignoré

### 11.3.0

*(Publié Le 24 Novembre 2021)*

**Ajouté :**

* [Modèles de Substance] Ajout d’info-bulles pour les paramètres des nœuds
* [Modèles de Substance] Permet d&#39;afficher en superposition dans le viewport 3D le résultat d&#39;un nœud intermédiaire
* [Modèles de Substance] Amélioration de l’affichage des bases
* [Modèles de Substance] Conservez la hiérarchie des objets lors de l’exportation d’un Graphe Substance model au format .fbx
* [Modèles de Substance] Prise en charge de plusieurs matériaux lors de l’exportation FBX/OBJ à partir du Graphe Substance model
* [Modèles de Substance][Contenu] Nœud de Particule
* [Modèles de Substance][Contenu] Nœud de Transforme générative
* [Modèles de Substance][Contenu] Nœud Motif organique
* [Modèles de Substance][Contenu] Particules du nœud Instances
* [Modèles de Substance][Contenu] Nœud d&#39;élagage de Particule
* [Modèles de Substance][Contenu] Nœud de tour
* [Modèles de Substance][Contenu] Nœud Shell
* [Modèles de Substance][Contenu] Nœud de Projection
* [Modèles de Substance][Contenu] Nœud de rognage de courbe
* [Modèles de Substance][Contenu] Mettre à jour le nœud Curve Sampler
* [Modèles de Substance][Contenu] Mettre à jour le nœud Sampler du Maillage
* [Modèles de Substance][Contenu] Mettre à jour le nœud de Variation
* [UX] Bouton pour agrandir la vue actuelle
* [UX] Mettre à jour la fenêtre Nouveau Graphe
* [UX] Ajouter l&#39;option « Télécharger le lecteur » dans le menu Outils et l&#39;agréger avec « Localiser le lecteur »
* [UX] Ajouter l’entrée « Tout fermer » au menu Fichier
* [UX] Appliquer la même casse dans tout le menu principal
* [UX] Afficher automatiquement les propriétés des éléments de graphe dupliqués
* [UX] Ajoutez des boutons dans la barre d’outils graphe pour désactiver la taille d’écran constante pour les titres / commentaires / Épingles du Cadre
* [UX] Boutons pour copier les informations de version dans le Presse-papiers dans la boîte de dialogue À propos
* [Matériaux] Entrées relatives aux entrées
* [Contenu] Ajout de l’option « Répétition » sur les Bruits Perlin 3D
* [Contenu] Nouveau nœud de processus de Diffusion
* [Contenu] Nouvelle version du nœud de Rendu PBR
* [Interopérabilité] Recevoir SBS et SBSAR de Sampler
* [Interopérabilité] Envoyer SBSM à Stager
* [vue 3D] Ajout d’une option pour désactiver backface culling
* [vue 3D] Ajout d’une option pour afficher l’espace de tangente du Vertex
* [Explorateur] Mettez en surbrillance le graphe dans l’Explorateur lorsque vous double-cliquez sur l’arrière-plan de la Vue du graphe
* [Explorateur] Supprimer l’option « Explorer » dans les menus contextuels
* [Bakers] Masquer les bakers obsolètes
* [Gestion des couleurs] Prise en charge des règles du fichier de configuration OCIO v2
* [Bibliothèque] Renommer les catégories en fonction des types de graphe
* [Préférences] Désactivez automatiquement le processeur dans les préférences de Périphériques pour Iray si un GPU CUDA pris en charge est détecté

**Fixe :**

* [modèles de Substance] Crash sur Mac lors de l’utilisation de l’option « as sudb » sur .fbx
* [modèles de Substance] Crash lors de l’exportation vers SBSM dans un cas spécifique
* [Modèles de Substance] Échec de l’exportation lors de l’exportation de paramètres exposés dont les widgets n’ont jamais été créés
* [Modèles de Substance] crash aléatoire lors de l’ouverture d’un graphe faisant référence à plusieurs fichiers .fbx
* [Modèles de Substance] Les plages ne sont pas appliquées dynamiquement dans les widgets de paramètre exposé
* [Modèles de Substance] L’option Recharger le maillage ne fonctionne pas sur les ressources utilisées dans le graphe des modèles de Substance
* [modèles de Substance] les Scènes ne sont pas affichées dans une vue 3D disponible dans un cas spécifique
* [UI] La zone Désactiver est trop grande dans les options de matériau
* [UI] Problème de style dans la boîte de dialogue « Fichier de package non enregistré »
* [UI] Appuyez deux fois sur la touche de tabulation pour naviguer entre les valeurs.
* [UI] Le zoom avec le glissement de la souris est inversé entre vue 3D et les autres Viewports
* [UI] Le chargement d’un fichier SBS déjà ouvert à l’aide de la liste « Fichiers récents » déclenche une invite « Package introuvable »
* [UI][macOS] Disposition d’interface par défaut incorrecte après le démarrage de l’application
* [UI] Les packages ne peuvent pas être enregistrés à la racine d’un lecteur (Windows uniquement)
* [Graphe] L’option « Afficher automatiquement dans vue 2D » est incohérente dans un cas spécifique.
* [Graphe] L’option « Ouvrir la référence » est disponible pour les instanciers SBSAR
* [Graphe] Les propriétés d’Épingle ne s’affichent que lors de la création de l’élément
* [Graphe] Les règles de chaîne d&#39;Épingle sont appliquées de manière incohérente
* [Graphe] Crash lors de l’enregistrement d’un graphe vide
* [vue 3D] Anisotropy angle inversée dans ASM shader
* [vue 3D] Shader ASM : problèmes de linéarisation avec les cartes liées à SSS
* [vue 3D] Rendu OpenGL rompu après la fermeture de vues 3D supplémentaires dans un cas spécifique
* [vue 3D] Les positions des caméras prédéfinies ne sont pas correctes dans la vue 3D avec certains fichiers .fbx
* [MDL] L’option « Ajouter un nœud » du menu contextuel ne fonctionne pas pour les Graphes MDL
* [MDL] Bogue : la connexion du nœud échoue lors de l’utilisation de composants float2.x et similaires (SD 11.1.2)
* [MDL] Crash à l’ouverture du fichier specific.sbs
* [MDL] Unités de Scène par mètre en Iray non définies au début de la session de rendu
* [MDL] Se bloque lors de l’ajustement d’un nœud lerp dans le Graphe MDL
* [MDL] Ordre des paramètres dans le code MDL exporté
* [Explorateur] un dossier de ressources vide est créé après l&#39;annulation de la création de la ressource
* [Explorateur] Seul le premier élément d’un pack peut être déplacé au bas de la liste
* [Content] RT Bent Normal et RT AO déclenchent un calcul de nœud dans les graphes imbriqués
* [Noeud d&#39;entrée] Le bitmap dans Noeud d&#39;entrée n’est pas mis à jour lorsque l’UDIM change
* [Iray] L&#39;affichage d&#39;une Scène de modèles de Substance de données avec beaucoup d&#39;instances prend beaucoup de temps
* [Préférences] Ligne vide lors de l’annulation de l’ajout d’un fichier de projet
* [Éditeur Python] L’option « Fermer » reste activée après la fermeture du dernier script et inclut toujours son nom e

### 11.2.2

*(Publié Le 28 Septembre 2021)*

**Ajouté :**

* [Propriétés] Ajoutez de nouveaux types de graphes pour les décalcomanies, les atlas, les Éclairages d&#39;environnement et les textures claires

**Fixe :**

* [UI] Disposition d’interface incorrecte après le démarrage de l’application
* [Stabilité] Correction des crashs lors de la sortie du mode veille sous Windows et lors du branchement/débranchement d’écrans
* [vue 3D] La création d&#39;une ressource scène 3D à partir de la Scène Graphe Substance model n&#39;a aucun effet
* [Fusion] Les valeurs d&#39;énumération sont manquantes lors de l&#39;expose du mode de fusion
* [Export] L&#39;exportation de Scènes de modèles de Substance entraîne une géométrie dupliquée
* [MDL] Crash lors de l’ouverture d’un fichier SBS spécifique
* [Maillage] Crash lors de la liaison d&#39;un maillage spécifique avec une géométrie défectueuse
* [Modèles de Substance] L’exportation échoue lorsque la valeur par défaut du paramètre exposé est hors des limites souples

### 11.2.1

*(Publié Le 27 Juillet 2021)*

**Ajouté :**

* [modèle de Substance] Mise à jour vers la version 1.0.3
* [Modèle de Substance] Compléter et améliorer la documentation des Graphes Substance models
* [Substance de données] Afficher les journaux dans la console
* [Substance][ScatterOnCurves] Modifier la valeur par défaut pour espacement
* [Modèle de Substance][ScatterOnCurves] Supprimer le paramètre HalfSpaceOddEVEN superflu
* [Substance][Transforme] Mettre à jour la plage graduelle de rotation d&#39;Euler
* [Publish] Mémoriser les paramètres dans la fenêtre Publish
* [Publish] Avertissez l’utilisateur lorsqu’au moins une dépendance comporte des modifications non enregistrées
* [Publish] Champ Initialiser le chemin d’accès au fichier
* [Publish] Ajout de commentaires visuels pendant la publication
* [Interopérabilité] Ajout de la commande « Envoyer au lecteur » au menu « Envoyer à »
* [Interopérabilité] Simplification du workflow d’envoi/de renvoi vers Sampler et Painter
* [API] Ajoutez SDApplication.getVersion() pour permettre la récupération de la version de l’application hôte
* [Explorateur] Ajout d’une action Ouvrir aux éléments de Graphe Substance model
* [Graphe] Désactiver les actions « Afficher en vue 3D » pour les instanciers de fantôme

**Fixe :**

* [Substance model] Crash lors de la suppression d&#39;une séquence
* [Substance] Les bases ne sont pas tracées correctement dans certains cas
* [modèle de Substance] Échec de l’exportation de projets spécifiques
* [modèle de Substance] l’affectation de Matériau a échoué lors de l’ouverture d’un projet avec Iray activé
* [Substance] La plage fixe minimale ne fonctionne pas correctement dans certaines circonstances
* [Modèle de Substance][Primitif] Le premier niveau de subdivision de l&#39;icosphère ne fonctionne pas
* [Substance][RandomFloat] Gère correctement le cas où Min >= Max
* [Vue 3D] Crash lors du glisser-déposer de cartes
* [vue 3D] Les chaînes Exposées dans les Matériaux MDL utilisent le widget d’espace colorimétrique
* [vue 3D][Bakers] Les objets parents ne sont pas traités correctement
* [vue 3D] Message d’avertissement concernant le nom d’utilisation « heightScale » pour le fichier .glslfx hérité
* [Content] Avertissements de cuisson dans Height Extrude
* [Contenu] Le nœud Irradiance RT n&#39;apparaît pas dans la bibliothèque
* [Contenu] RT Shadows : messages d&#39;avertissement de cuisson dans la console
* [Graphe] Crash lors de l’ouverture d’un fichier avec des nœuds désactivés
* [Graphe] Le nœud point ne fonctionne pas correctement dans Graphe MDL lorsqu’un lien est sélectionné
* [Graphe] La Vue du graphe n’est pas automatiquement rouverte après le rechargement d’un pack
* [Interopérabilité] Boîte de dialogue d’erreur lors de la sélection de « Télécharger... » lors de l’envoi au Lecteur
* [Interopérabilité] Le renvoi après suppression de toutes les sorties entraîne des erreurs d’API
* [Interopérabilité] Le renvoi juste après la fermeture de l’application cible entraîne des erreurs d’API
* [Explorateur] [Graphe] Après le rechargement d’un pack, le premier graphe ouvert n’est pas le premier graphe du pack
* [Explorateur] Les nouveaux graphes d’un pack ne sont pas placés de la même manière selon leur type
* [Explorateur] Impossible d’ouvrir un Graphe Substance model ou une ressource de Scène après l’avoir déplacé dans l’explorateur
* [Explorateur] Crash/blocage lors du déplacement d’un Graphe Substance model dans la hiérarchie du package
* [Bibliothèque] Les fichiers SBSAR restent à l’emplacement des fichiers temporaires
* [Bibliothèque] Les fichiers XML restent à l’emplacement des fichiers temporaires
* [Player] Le Matériau n’a aucun impact dans vue 3D lorsque la langue est définie sur Japonais
* Le lien de téléchargement de la Substance Player [Player] est obsolète
* [Widget Couleur] La fenêtre de l’éditeur de couleurs se déplace vers le haut de l’écran
* [Iray] Correction du chargement d’un module Iray sous Windows lorsque le répertoire d’applications contient des caractères non ascii
* [Préférences] Le panneau MDL s’affiche deux fois dans Project
* [API] Les nœuds FxMap ne prennent pas en charge getPropertyGraph()

### 11.2.0

*(Publié Le 23 Juin 2021)*

**Ajouté :**

* [Branding] La Substance Designer devient Adobe Substance 3D Designer
* [Modèles de Substance] Nouveaux Graphes Substance models pour créer des modèles 3D procéduraux
* [Content] Ajout de nouvelles maps d&#39;environnement HDR
* [Contenu] Nouveau nœud Courbé normal
* [Content] Nouveau nœud d&#39;Ambient occlusion RT
* [Content] Nouveau nœud RT Caustics
* [Content] Nouveau nœud RT Caustics
* [Contenu] Nouveau nœud d&#39;irradiation RT
* [Contenu] Nouveau nœud Ombres RT
* [Interopérabilité] Envoyer la ressource vers Painter, lance Painter et ajoute ou met à jour la ressource dans la bibliothèque (nécessite une formule Substance 3D Adobe)
* [Interopérabilité] Envoyer la ressource vers Sampler, lance Sampler et ajoute ou met à jour la ressource dans la bibliothèque (nécessite une formule Substance 3D Adobe)
* [Interopérabilité] Parcourez votre ressource dans Adobe Bridge et lancez Bridge à l’emplacement de la ressource (nécessite une formule Substance 3D Adobe).
* [ASM] Soutien du nouvel Adobe Standard Material (ASM) dans le Graphe Substance et le Graphe MDL
* [ASM] Ajouter des modèles ASM
* [ASM] Ajout de Shader OpenGL pour ASM
* [ASM] Définir le shader ASM comme Shader par défaut
* [Général] Agréger tous les fichiers temporaires dans le répertoire temporaire défini par l’utilisateur
* [Général] Nouvelle commande Enregistrer une copie sous
* [Général] Menu Fichier de mise à jour
* [Général] Mettre à jour le menu Aide
* [Publish] Nouvelle fenêtre de publication
* [Publish] Ajoutez une option dans les préférences afin de ne pas enregistrer le fichier SBS lors de la publication d’un Fichier sbsar
* [Propriétés] Ajouter un champ de type de graphe aux propriétés du graphe
* [Propriétés] Réorganisez les propriétés des graphes de manière plus pertinente
* [Branding] Nouvelle fenêtre À propos
* [Branding] Mise à jour du style d&#39;application
* [GLSLFX] Ajout d’un libellé aux techniques
* [GLSLFX] Ajouter la possibilité de définir le label d&#39;un shader GLSLFX
* [Métadonnées] Ajouter des métadonnées aux ressources du package
* [Métadonnées] Autoriser l’édition de métadonnées pour les graphes, les entrées, les sorties et les ressources
* [Localisation] Nouvelles traductions en allemand, français et chinois simplifié
* [UX] Inversez le zoom dans la vue 3D en cas de glissement de la souris
* [AXF] Mise à jour vers la version 1.8.0
* [Journaux] Ajout des plug-ins installés aux journaux
* [VFX] Ajout de la configuration OpenColorIO ACE 1.2
* [API Python] Ajout d’une méthode pour interroger le répertoire tmp spécifié dans les paramètres
* [API Python] Ajoutez une méthode isModified à SDPackage pour vérifier si un pack est enregistré
* [API Python] Ajout de méthodes de conversion de couleurs à SDColorManagementEngine
* [API Python] Supprimer des objets de graphe (commentaires, épingles, cadres, ...)
* [API Python] propriété de Taille physique d&#39;Expose pour les nœuds d&#39;instance de graphe
* [API Python] Exposez d’enregistrer une copie sous
* [API Python] Correction de la méthode SDPackageMgr.savePackage
* [API Python] Obtenir une liste des objets de graphe sélectionnés
* [API Python] Introduction de nouveaux noms de méthode pour travailler avec des sélections de graphe
* [API Python] Les plug-ins ne peuvent pas ajouter d’actions au premier panneau explorateur créé

**Fixe :**

* [Paramètres] Les valeurs négatives sur les paramètres Entier déroulant 1 entraînent un comportement incongru dans l&#39;instance
* [Paramètres] Problème lors de l’incrémentation d’une valeur sur un widget d’angle
* [Graphe] Problèmes de minutage lorsque la sortie est affichée dans la vue 2D ou 3D.
* [Internationalisation] Certains caractères spécifiques sont transformés en espaces dans les identifiants de fichier
* [Préférences] Le libellé du fichier « Projet utilisateur » n’est pas translaté en japonais
* [API Python] Erreur de récurrence lors de l&#39;exécution de la méthode SDUIMgr.getCurrentGraphSelectedNodes()
* [API Python] SDApplication.getPath(SDApplicationPath.InstallationDir) ne renvoie rien
* [API Python] SDSBSARExporter n’envoie pas de notifications d’enregistrement de fichiers

### 11.1.2 (2021.1.2)

*(Publié Le 17 Mars 2021)*

**Fixe :**

* [Bibliothèque] Les vignettes ne sont pas actualisées de manière cohérente
* [Contenu] La propriété « Format des pixels » de « Vector morph » graphes est définie sur « Étirer (absolu) ».
* [Contenu] Les bitmaps utilisés dans les outils de peinture apparaissent dans le menu Nœud
* [Contenu] Sortie NaN pour entrée de couleur plate dans le nœud Niveaux automatiques à la précision en virgule flottante
* [Moteur][SSE2] Une valeur « Entrée moyenne du niveau » autre que 0,5 génère une sortie 1,0
* [Vignette] Maps d&#39;entrée réduites à 256
* [UI] Les info-bulles des Noeuds atomiques ont un saut de ligne incorrect

### 11.1.1 (2021.1.1)

*(Publié Le 10 Février 2021)*

**Fixe :**

* [Vue 3D] Problème de rendu lors de l’utilisation de fichiers SBS qui ont des fréquences élevées en map normal
* [vue 3D] Les images ne sont pas appliquées si la propriété de sortie « Component » n’est pas définie sur RVBA ou RGB
* Les Scènes [vue 3D] ne sont pas chargées correctement dans certaines situations spécifiques
* [UI] Le champ de saisie « Fichier de Texture » dans l’éditeur de pinceaux est mis à l’échelle verticalement
* [UI] Les boutons Épingle et Ancrage disparaissent de l&#39;onglet lorsque l&#39;onglet actif est fermé
* [Bakers] Résultat incorrect lorsque la Bbox globale des maillages high poly n&#39;inclut pas l&#39;origine de la scène
* [Gestion des couleurs] La propriété de matériau de Texture de Base color sRVB n&#39;est pas remplacée dans un état de Scène personnalisé
* [Console] Le message du journal « GPU disponibles » ne répertorie pas les GPU et s’affiche de manière aléatoire
* [Console] Chaîne incorrecte consignée lors de l’utilisation de l’exportation par lots
* Le paramètre « Format normal d’entrée » de l’Atlas splitter [Contenu] a un impact sur la couche rouge au lieu du vert
* [Cooker] Crash ou sortie NaN lors de l&#39;utilisation de \*.surface bitmaps dans SBSAR
* [Moteur] Les valeurs de sortie hors plage de la courbe de transfert de dégradé bouclent autour de 0 lorsque le format de sortie est compris entre 0 et 1
* [Paramètres] Les curseurs Min/Max/Par défaut ne s’ajustent pas automatiquement dans la fenêtre Exposer le paramètre
* [SBSAR] Crash lors de l’importation de certains SBSAR
* crash [SVG] lors de l’annulation de l’importation de ressources

### 11.1.0 (2021.1.0)

*(Publié Le 28 Janvier 2021)*

**Ajouté :**

* [Tons directs] Prise en charge des couleurs Pantone dans Designer
* [Graphe] Désactiver les nœuds
* [vue 3D] Exportation de Maillages facettisés à partir du Viewport
* [Internationalisation] Mettre à jour la version japonaise
* [vue 3D] Optimisation de la consommation de mémoire lorsque vous n’utilisez pas Iray
* [API Python] Ajout de la méthode SDResource.delete() pour supprimer une source SDR
* [API Python] Ajout de la prise en charge des tons directs à l’API Python
* [API Python] Nouveau rappel à déclencher lorsqu’un pack est fermé
* [vue 2D] Conversion de la base de données brush de SQLite au format Json
* [vue 2D] Amélioration des performances de rendu et de la fiabilité (calcul CPU)
* [Bibliothèque] Option « Exclure le modèle » ajoutée dans les paramètres du projet
* [Bibliothèque] Renommez « Exclure le modèle » en « Exclure les extensions de fichier » dans les paramètres du projet
* [UX] Supprimer le bouton « ? » dans les barres de titre des fenêtres sous Windows
* [UX] Déplacez le raccourci Ctrl+E vers « Ouvrir la référence » lorsque l’édition contextuelle est désactivée
* [Baker] Supprimer le cache d’aperçu lors de la suppression d’un baker dans la liste de baking
* [Performances] Optimisation du budget de la mémoire cache des images sur le matériel avec GPU avec mémoire partagée
* [Préférences] Adapter la valeur « Limite du cache GPU » au pool de mémoire disponible
* [Properties] Afficher l&#39;attribut de Taille physique sur l&#39;instance de nœud
* [Scripting] Marquer le système de script externe comme obsolète
* [Share] Supprimer les fonctionnalités « Exporter vers la Substance share »

**Fixe :**

* [Contenu] Ordre des E/S incohérent sur les nœuds de Matériau
* [Contenu] L’entrée principale sur les nœuds de déformation est incohérente
* [Contenu] Résoudre les avertissements de l’outil Cuisinière à partir du nœud Flou radial
* [Export] L&#39;exportation par lots avec moteur CPU utilise VRAM pour déterminer le budget mémoire
* [Exporter] L’exportation vers un chemin d’accès qui n’existe pas crée les dossiers
* [Export] Le budget de mémoire est trop faible lors de l’exportation par lots
* [vue 2D] Artefacts/effets de bande lors de la copie d’images HDR dans le presse-papiers
* [vue 2D] L’exportation d’images à partir de ressources exporte toujours 8 bits
* [vue 3D] Iray : la modification de la valeur normale à l’aide de l’éditeur donne un résultat étrange
* [vue 3D] Iray : la désactivation du canal normal ne produit pas le bon résultat
* [Bibliothèque] Le Filtrage par URL ne fonctionne pas correctement
* [Bibliothèque] Les ressources correspondant à un modèle exclu de la bibliothèque ne peuvent pas être importées manuellement
* [Bakers] Le fait de renommer un baker n’a aucune incidence sur son entrée dans la liste d’aperçu vue 2D
* [Explorateur] Perte de synchronisation entre les données Explorateur et de graphe
* [graphe de fonction] Crash lors de la définition du noeud de fonction avec un type de sortie non concordant en tant que sortie
* [MDL] Les instanciers SBS n’ont pas d’aperçu, génèrent la sortie 0 et ne déclenchent pas de calcul de graphe
* [API Python] Impossible de modifier la propriété &#39;editor&#39; du Paramètre d&#39;entrée
* [Python] La réinitialisation de la mise en page ne réinitialise pas correctement les docks créés par Python
* [Ressources] Impossible de lier/importer un document de PSD 32 bits

## Version 10

### 10.2.2 (2020.2.2)

*(Publié Le 17 Décembre 2020)*

**Ajouté :**

* [vue 3D] Restauration de la position de la caméra stockée dans une ressource de Scène de données
* [Graphe] Supprimer « noeuds d&#39;entrée » dans le menu contextuel pour FXMap et processeur de valeurs

**Fixe :**

* [Contenu] Ordre des E/S incohérent sur les nœuds de Matériau
* [Contenu] Rendu PBR : échantillonnage IBL incorrect pour la contribution specular
* [Contenu] Rendu PBR : certains pixels sont toujours transparents
* [Contenu] Rendu PBR : la sortie UV est incorrecte pour la forme de cylindre
* [Contenu] Le paramètre « Pattern Specific » de Splatter Circular n’a aucun effet
* [MDL] Crash lors de la création et de la connexion d&#39;un nœud
* [MDL] Crash lors de la duplication d&#39;un constructeur de tableau color[] avec son entrée de valeur exposée connectée
* [MDL] Crash lors de la reconnexion d&#39;une connexion non valide
* [MDL] Les MDL exportées ont des paramètres en double
* [MDL] Les Paramètres exposés ne sont pas exportés vers un fichier .mdl
* [Paramètres] Un paramètre de nœud peut être défini deux fois dans le SBS dans un cas spécifique
* [Paramètres] Crash lors de la récupération du type de sortie du Graphe de fonction d&#39;un paramètre
* [Paramètres] Crash lors de la sélection de l’option « Modifier l’entrée de graphe exposée » lorsqu’il n’existe aucune entrée correspondante
* [vue 3D] L’utilisation de l’« environnement » n’est pas correctement prise en compte par le moteur de rendu OpenGL
* [vue 3D] IOR a la valeur 0 et doit être réinitialisé dans un cas spécifique
* [vue 3D] Les UV du plan/plan haute résolution sont décalés
* [Bitmap] Crash lors de l’annulation de l’importation de ressources
* [Bitmap] Crash lors de la création d&#39;un nouveau nœud Bitmap avec un type de fichier non pris en charge
* [Dépendances] Crash lors de l’annulation de « Redéfinir l&#39;emplacement » pour résoudre une instance de Fantôme
* [Graphe de fonction] Crash lors de l&#39;ouverture du graphe de fonction pour un paramètre
* [Éditeur de dégradé] Le déplacement des curseurs et des touches enregistre trop d’actions dans la pile d’historique
* [Licence] Crash lors de l’analyse d’un fichier license.key non valide
* [SBSAR] Impossible de créer des instanciers SBSAR à partir de la bibliothèque si les graphes exposés se trouvent dans des dossiers

### 10.2.1 (2020.2.1)

*(Publié Le 4 Novembre 2020)*

**Fixe :**

* [Général] Crash lors de la sortie du mode veille Windows
* [Général] Crash sur Annuler après le chargement d&#39;une ressource scène 3D
* [Moteur] Les lignes d’artefact apparaissent dans la sortie du nœud Distance sur Direct3D
* [Moteur] Crash lors de la sélection du nœud de Map de dégradé dans un graphe mis à jour
* [Moteur] Aucun avertissement lorsque la valeur par défaut Entrée est différente de 0 en mode de compatibilité Moteur v7
* [vue 3D] L’option « Tout supprimer » laisse les maillages avec des matériaux prédéfinis sans matériau
* [vue 3D] L’option « Réinitialiser la Scène » supprime toutes les textures du maillage dans Iray
* [vue 3D] OpenGL : la modification de la valeur par défaut d’un sampler dans un fichier .glslfx n’est pas correctement reflétée dans l’interface utilisateur
* [vue 3D] Pixels rouges et noirs sur le bord le plus à droite des images rendues OpenGL
* [Dependencies] Impossible de redéfinir l&#39;emplacement les dépendances manquantes de type « Other »
* crash [Dépendances] à la fermeture lorsque le visualiseur de dépendances est ouvert
* [Graphe] Crash lors de la duplication d’un Instancier de Fantôme
* [Graphe] L’édition contextuelle est disponible par frappe de touche lorsqu’elle est désactivée dans Préférences
* [UI] La fenêtre d’avertissement « Localiser le lecteur » a un titre incorrect
* [UI] L&#39;Assistant Activation a un comportement incorrect
* [Explorateur] Les packs groupés sont toujours modifiables sous Windows
* [MDL] Crash lors du chargement d’un graphe d’une version précédente avec des connexions non valides
* [Propriétés] Couleur par défaut du noeud d&#39;entrée non mise à jour lors de l’annulation
* [SBSRender] Les profils ICC des bitmaps injectés ne sont pas utilisés

### 10.2.0 (2020.2.0)

*(Publié Le 12 Octobre 2020)*

**Ajouté :**

* [Contenu] Ajouter un nœud « Section transversale »
* [Contenu] Ajouter la fonction « Cross product vec2 » à features.sbs
* [Contenu] Ajouter un nœud de valeur « Obtenir la taille »
* [Contenu] Ajouter la fonction « Orthogonal vec2 » à features.sbs
* [Contenu] Ajouter des fonctions Moyenne à des fonctions.sbs
* [Contenu] Ajouter un filtre Seuil
* [Contenu] Correspondance des couleurs : ajoutez une entrée de masque pour spécifier où appliquer le filtre
* [Contenu] Tile Generator/Sampler : ajout de nouvelles options pour contrôler la taille du motif
* [Contenu] Mise à jour du nœud Rendu PBR avec la valeur par défaut pour les entrées d’image
* [Paramètres] Ajoutez des icônes d’avertissement pour mettre en évidence les problèmes dans Paramètres de l’instance
* [Paramètres] Ignorer les instructions If visibles pour les entrées/sorties impliquant des paramètres auxquels une fonction est appliquée
* [Paramètres] Améliorer l&#39;UX pour l&#39;association de groupe
* [Paramètres] Reformulation de la façon d&#39;exposer un seul paramètre
* [Paramètres] Mettre en surbrillance les paramètres exposés
* [Paramètres] Améliorer le nettoyage des paramètres inutilisés
* [Moteur] Nœud de courbe : nouvelle option pour générer la texture de courbe
* [Moteur] Valeurs par défaut sur les images d&#39;entrée
* [Moteur] Nœud de distance : nouveaux modes de distance (distances de Manhattan et de Tchebychev)
* [Moteur] Nœud de dégradé : nouveau mode d’interpolation pour avoir un mélange plus naturel entre les couleurs
* [UX] Certains paramètres sont désormais grisés en fonction d’autres paramètres
* [UX] Accepter les couleurs RGB à 6 chiffres dans le champ hexadécimal du sélecteur de couleurs
* [UX] Évitez d’afficher les propriétés des commentaires dès qu’elles sont sélectionnées
* [UX] Afficher les groupes pertinents au début de l’écriture d’un nom de groupe
* [UX] Raccourci pour réexporter les sorties du graphe
* [UX] Différencier toutes les zones de texte déroulantes des zones de liste déroulante standard
* [GraphRender] Affiche les nœuds une par une et pas seulement lorsqu’ils sont tous calculés.
* [GraphRender] Amélioration du délai d’annulation pendant le rendu du graphe
* [GraphRender] Amélioration de la précision de la barre de progression du rendu
* [Vignettes] calcul automatique des vignettes (icônes)
* [Vignettes] Modification de l’interface utilisateur pour ajouter une vignette (icône) à un pack
* [Préférences] Activer le GPU raytracing par défaut pour les nouveaux utilisateurs
* [Préférences] 3DView / OpenGL / Quality : remplacez le curseur du nombre d’échantillons par une liste de choix plus intuitive
* [Bakers] Amélioration des performances post-traitement
* [Gestion des couleurs] Afficher l’espace colorimétrique de travail actuel dans la boîte de dialogue des préférences.
* [Iray] Basculer automatiquement en mode CPU en l’absence de GPU compatible
* [Performances] Améliorer le temps de réponse pour calculer le nœud qui nous intéresse (maintenant calculé en premier)
* [API Python] Nouvelle méthode addActionToExplorerToolbar pour ajouter des icônes à la barre d’outils de l’explorateur
* [Ressources] Mise à niveau vers FBX 2020.0.1
* [iRay] Mise à jour vers Iray 2020.1.0
* [API] Ajout d’un accès Python aux paramètres et propriétés de gestion des couleurs

**Fixe :**

* [Graphe] La modification de la taille du gabarit ou de la mosaïque uv n’annule pas le rendu en cours
* [Graphe] Crash lors du déplacement d’une connexion de sortie, puis en appuyant sur Alt+LMB
* [Graphe] Crash lors du déplacement de connexions dans Matériau ou Compact Mode de matériau
* [Graphe] Les Noeuds d&#39;entrée ne peuvent pas prévisualiser les ressources Bitmap
* [Graphe] Compatibilité des nœuds rompue sur les instances
* [Graphe] Trop de nœuds sont invalidés lors de la modification d&#39;un paramètre de graphe
* [Contenu] La forme de sortie « Extrusion de forme » est inversée dans des cas spécifiques : nouvelle version requise, l’ancienne est obsolète
* [Contenu] Résultat incorrect à l’aide de la variation de couleur personnalisée dans le nœud Correspondance de couleur
* [Contenu] Le rapport Taille par quantité X/Y en Atlas scatter a l’effet inverse
* [Contenu] Le rapport entre la taille et la quantité sur X/Y dans Shape Splatter a l’effet inverse
* [vue 3D] Crash lors de l&#39;opération Annuler après le chargement d&#39;une Scène à partir d&#39;un package
* [vue 3D] Environnement personnalisé non enregistré dans SBSSCN si le chemin a un alias avec des caractères spéciaux
* [vue 3D] Le changement de format normal dans les paramètres de Matériau entraîne des états inversés
* [UI] Le texte du bouton « Définir comme principal » déborde de la zone d’affichage
* [UI] La position de la fenêtre principale n’est pas correctement restaurée lorsque vous travaillez en mode fenêtré
* [UI] Le texte de la barre d’état est décalé lorsque la fenêtre est en plein écran ou déplacée près du bord de l’écran
* crash [Iray] avec message « Balise non valide » lors du basculement entre les moteurs de rendu
* [Iray] faces visibles sur des surfaces non opaques
* [Paramètres prédéfinis] Crash lors de l’application de paramètres prédéfinis dans des instances de certains graphes de Substance Source
* [Paramètres prédéfinis] nom erroné affiché après l&#39;annulation sur l&#39;instance sbs
* [Rendu] Mauvais rendu lors de l’ajustement d’un paramètre en mode aperçu
* [Bakers] L’actualisation de plusieurs maps bakées entraîne des avertissements qui bloquent certains bakes
* [Cooker] L’ajustement des nœuds SBSAR dans les instances SBS entraîne une sortie de 0 de l’instance
* [Explorateur] Les alias personnalisés ne sont pas transmis lors de l’utilisation de « Enregistrer et ouvrir dans la Substance Player »
* [Éditeur de dégradé] Le choix de couleur absolu n’affecte pas toutes les touches sélectionnées

### 10.1.3 (2020.1.3)

*(Publié Le 11 Juin 2020)*

**Ajouté :**

* [Contenu] Exposer le paramètre « Couleur de cache » dans le nœud Transformer en niveaux de gris sans échec
* [Contenu] Rendu PBR : ajout d’une option personnalisée Entrée d’arrière-plan
* [Contenu] Nœuds Lumière de panorama : nouvelle option pour prélever la couleur de l’image d’arrière-plan
* [Paramètres] Masquer les paramètres avec l’indicateur « non pris en charge » dans la liste de la fenêtre Exposer les paramètres

**Fixe :**

* [vue 3D] Crash lors du changement de maillages personnalisés dans un cas spécifique
* [vue 3D] Le format normal est toujours DirectX au démarrage
* [Contenu] bruit Worley 3D : rendu d’un artefact lors de l’utilisation d’une valeur de taille de grille élevée
* [Contenu] La fusion des nœuds de fondu est incorrecte
* [Contenu] Rendu PBR : supprimer l’avertissement de l’outil de cuisson
* [Contenu] Rendu PBR : résultat contient des couleurs négatives dans certains cas
* [Cooker] Problème d&#39;injection du cache pour les instanciers à sorties multiples
* [Explorateur] Crash lors de la fermeture d’un pack contenant un Graphe MDL affiché
* [Graphe] Cuisson en 2 passes : le changement de type de nœud ne déclenche pas de recook
* [Graphe] Crash lors de la suppression d’entrées lors de l’utilisation de sa connexion
* [Graphe] Les points de terminaison de lien peuvent être déplacés vers un espace vide
* [MDL] Crash lors de l’annulation de l’exportation MDL à partir du graphe MaterialX
* [MDL] Erreur lors de l’annulation de l’exportation vers MDLE
* [Paramètres prédéfinis] Crash dans l’onglet Paramètres prédéfinis après la modification du type de paramètre inclus dans le paramètre prédéfini
* [Ressources] La liste de Matériaux est vide dans le menu contextuel du graphe pour les maillages liés comme non UDIM

### 10.1.2 (2020.1.2)

*(Publié Le 27 Avril 2020)*

**Ajouté :**

* [Contenu] Ajouter un modèle de filtre Alchemist
* [Contenu] Rendu PBR : ajoutez des paramètres pour contrôler les intensités des ombres de diffusion/specular
* [Contenu] Nœuds Shape Light : ajout d&#39;un paramètre de position de caméra
* [Actualités] Le style « Flèche » du groupe ne fonctionne pas la première fois que la fenêtre s’affiche
* [Bakers] Ajoutez le raccourci Z à la vue 2D pour afficher l’image au format 1:1
* [Projet] Masquer l’alias $(PROJECT\_DIR) de la liste
* [Explorateur] Ne créez pas de ressource personnalisée pour les ressources qui ne sont pas un fichier sur le disque

**Fixe :**

* [Player] Signaler les alias manquants lors du chargement des packages SBS
* [Player] Afficher la valeur de générateur aléatoire sous forme de base décimale
* [Player] Regrouper toutes les maps d&#39;environnement incluses dans Substance Designer
* crash [Player] à la sortie dans macOS High Sierra
* [Player] Impossible de charger les packages utilisant sbs://
* [Contenu] bruit Worley 3D : rendu d’un artefact lors de l’utilisation d’une valeur de taille de grille élevée
* [Contenu] L’entrée « supérieur à zéro » dans le nœud « Onde » n’est pas utilisée
* [Contenu] Éclairage plan : le mode de position Espace monde ne fonctionne pas
* [Contenu] Lumière sphérique : la position d’éclairage interne ne fonctionne pas correctement
* [Bakers] Crash lors du baking avec la fenêtre de baking pendant l’exécution d’une option « Actualiser toutes les maps bakées »
* [Bakers] Le Baking échoue sur Optix pour AO à partir du Maillage en utilisant Faible comme Élevé avec une Map normal
* [Bakers] La résolution de l’aperçu des fichiers UVT ne correspond pas à la taille de l’écran
* [vue 3D] Le bitmap attribué est remplacé lors du chargement d&#39;une MDL si la valeur par défaut n&#39;est pas une texture 2d
* [vue 3D] Les widgets Propriétés du Matériau changent après la réinitialisation d’une propriété
* [vue 3D] La préférence globale Format normal ne fonctionne plus
* [MatX] Bibliothèque : la catégorie de Graphe MaterialX n&#39;affiche pas tous les nœuds disponibles
* [MatX] Le menu contextuel d’un Graphe personnalisé peut contenir des sous-dossiers vides dans le dossier « Ajouter un nœud »
* [SBSAR] L’entrée principale est restaurée à la première entrée de la liste
* [Bibliothèque] Seul le premier graphe est inclus à partir de SBSAR avec plusieurs graphes
* [CustomGraph] Dans certains cas, les nœuds qui ne font pas partie du type de graphe actif sont créés automatiquement
* [Iray] Le paramètre « Profondeur » de la projection Box ne fonctionne pas correctement
* [Préférences] Amélioration de la mise en page dans les paramètres du projet
* [Paramètres] Crash lors du déplacement d’un widget de position après avoir supprimé un paramètre
* [UI] Crash lors de la modification de la hiérarchie des utilisations dans le nœud sorties
* [Graphe] Crash lors de l’utilisation d’une zone de sélection sur un commentaire et un nœud badgé

### 10.1.1 (2020.1.1)

*(Publié Le 10 Avril 2020)*

**Fixe :**

* [vue 3D] L’utilisation de la mémoire est trop élevée lors du travail sur le graphe de composition
* [Contenu] Formes inattendues dans la sortie non carrée des nœuds « Polygone »
* [Contenu] Rendu PBR : la caméra Orthographique ne fonctionne pas correctement lors de l’utilisation d’une résolution non carrée
* [Contenu] Rendu PBR : Swirly bokeh augmente la luminosité de la bordure de l’image
* [Gestion des couleurs] Le sélecteur de couleurs dans la boîte de dialogue Nouveau bitmap ne gère pas les couleurs.
* [Gestion des couleurs] Les sélecteurs de couleurs dans les outils peinture et Vecteur de la vue 2D ne prennent pas en charge la gestion des couleurs.

### 10.1.0 (2020.1.0)

*(Publié Le 9 Avril 2020)*

**Ajouté :**

* [Raccourcis] Gestionnaire de raccourcis pour la création de nœuds
* [Contenu] Nouveau nœud de Rendu PBR
* [Contenu] Nouveau filtre FXAA
* [Contenu] Nouveau filtre Hald CLUT
* [Contenu] Exposer le filtrage dans les nœuds « Recadrer »
* [vue 3D] Amélioration des paramètres de Shader/du workflow d’affectation des textures
* [vue 3D] Nouveau shader non éclairé
* [vue 3D] Ajout d’une « valeur zéro scalaire » aux ombrages de displacement
* [vue 3D] Ajout d’une option permettant de réduire la résolution du viewport lorsque la haute résolution est activée
* [vue 3D] GLSLFX : permet de définir des informations d’interface graphique sur sampler (par défaut, min, max, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup)
* [vue 3D] Ajoutez l’option Charger l’état avec le Maillage... dans le menu Scène
* [vue 3D] Ajout du transforme de sortie ACE tonemapped en mode de gestion des couleurs hérité
* [Bakers] Nouvelle méthode d&#39;échantillonnage dans les bakers AO, Courbure, Courbure normale, Thickness
* [Baker] Nouvelles options de normalisation dans les bakers Height et Thickness
* [Gestion des couleurs] Intégrer Adobe ACE (Adobe Color Engine)
* [Gestion des couleurs] Ajoutez des options pour définir le comportement par défaut lorsque le profil ICC est manquant
* [Paramètres] Incrémenter les curseurs en fonction de la Substance Painter
* [Packaging] Regroupez autant de DLL Qt que possible pour les scripts Python
* [Projet] Désactivez les paramètres pour les fichiers de projet en lecture seule et communiquez clairement cet état
* [Préférences] Masquer des paramètres non clairs spécifiques liés aux périodes de réactivité et de calcul
* [UI] Renommer Pow2 -> 2Pow
* [Propriétés] Optimisation de l’affichage des propriétés du graphe de composition
* [AXF] Mise à jour vers AXF SDK 1.7.1

**Fixe :**

* [vue 3D] Les paramètres Lumière ambiante ne sont pas visibles même s’ils sont activés
* [vue 3D] glslfx : le widget de couleur est toujours un vec3 sans alpha
* [vue 3D] Le jeu de Maps d&#39;environnement d&#39;une ressource n&#39;est pas enregistré dans la ressource scène
* [vue 3D] Iray : la lumière ambiante est convertie en lumière ponctuelle à l’origine de la scène
* [vue 3D] glslfx : le widget de couleur est toujours un vec3 sans alpha
* [Paramètres] L&#39;URL du package d&#39;instance est incorrecte dans le groupe d&#39;attributs
* [Paramètres] Crash lors de l’expose de paramètres
* [Paramètres] Les icônes ne sont pas correctement alignées dans les paramètres des nœuds de courbe
* [Paramètres] La chaîne de nœud &#39;Text&#39; s&#39;affiche uniquement en mode &#39;Preview&#39; lorsqu&#39;elle est exposée
* [Paramètres] Crash lors du changement de nom d&#39;un paramètre d&#39;entrée utilisé dans l&#39;instruction &#39;Visible If&#39;
* [Paramètres] Crash lors de la suppression d&#39;un nœud Levels dont une fonction est définie dans l&#39;un de ses paramètres
* [UI] L’icône d’avertissement dans la liste des paramètres d&#39;entrée est placée sur un bouton existant
* [UI] Les avertissements ne sont pas effacés sur l&#39;élément de paramètre d&#39;entrée correct dans un cas spécifique
* [UI] Empêcher le message « Le maillage est-il UDIM ? » pop-up pour apparaître lorsque les UV maillages sont strictement dans la mosaïque [0,1]
* [UI] Les listes déroulantes des paramètres prédéfinis peuvent défiler avec la molette de la souris en passant simplement la souris au-dessus
* [UI] L’option « calcul des sorties » dans les attributs de graphe n’est pas nommée correctement
* [MDL] Crash lors du placement d&#39;une ressource de graphe SBS dans un Graphe MDL
* [MDL] Le nœud SBS avec entrée d’image ne fonctionne pas correctement
* [MDL] Liaisons de texture et noms d&#39;utilisation incorrects
* [Graphe] Le groupe de valeurs d’entrée et l’utilisation sont ignorés dans le mode de création de lien « Matériau »
* [Graphe] Les valeurs d’entrée utilisent la valeur par défaut au lieu des données d’entrée pour les booléens
* [Bakers] Des normales incorrectes dans le baker Normales des espaces monde à l’aide d’une Map normal tangente dans des cas spécifiques
* [Bakers] Utilisation excessive de la mémoire lors du baking avec la fenêtre Aperçu ouverte
* [Paramètres prédéfinis] les paramètres prédéfinis corrompus rendent le rendu crash
* [Paramètres prédéfinis] Le paramètre de Booléen de l’ancien SBS n’est pas affecté par le paramètre prédéfini
* [Bibliothèque] Les ressources du premier package ouvert sont répertoriées dans le menu flottant de création de nœud
* [Publish] La publication sur SBSAR renvoie le code d’erreur 13 dans SBSCooker sur macOS
* [Publish] Avertissement d’argument obsolète dans SBSCooker lors de la publication dans SBSAR
* [API] Impossible d’obtenir les métadonnées d’un package provenant d’un fichier .fichier sbsar
* [Export] En mode hérité, l’option d’espace colorimétrique revient aux valeurs par défaut pour des sorties spécifiques
* [vue 2D] La copie dans le Presse-papiers ne prend pas en compte l’état de gestion des couleurs
* [Unix] Designer ignore les signaux système
* [Bibliothèque] Certains filtres de la bibliothèque ne fonctionnent pas correctement en raison de balises translatées
* [Cooker] La racine carrée des nombres négatifs doit renvoyer 0 au lieu de NaN
* [vue 2D] Les couches rouge et bleue sont permutées après l’annulation du premier tracé de peinture
* [Console] Message d&#39;avertissement trop long dans la console : « QPixmap::scaled: Pixmap est un pixmap nul »
* [Contenu] « Shape Glow » : avertissement culinaire
* [Dépendances] L’affectation d’un graphe situé dans un autre package à un maillage ne crée pas de dépendances
* [Iray] Les propriétés du Matériau deviennent inactives après le changement de géométrie

## Version 9

### 9.3.3 (2019.3.3)

*(Publié Le 14 Février 2020)*

**Ajouté :**

* [Batchtools] Livrer les profils OCIO par défaut avec des outils par lots

**Fixe :**

* atlas scatter de [Contenu] : problèmes lors de l’utilisation de couleurs aléatoires/normales dans certaines situations

### 9.3.2 (2019.3.2)

*(Publié Le 4 Février 2020)*

**Ajouté :**

* [SBSRender] Prise en charge de la gestion des couleurs

**Fixe :**

* [Contenu] Nœud sRVB linéaire vers ACEScg : les libellés d’E/S sont incorrects
* [Content] Nœud ACEScg vers sRGB : les libellés de sortie sont incorrects
* [Contenu] Nœuds Lumière de panorama : réglage de la plage de température
* [Graphe] Baisse et blocage importants des performances lors de l’ajustement d’un graphe imbriqué avec l’option « In-Context Editing » activée
* [Graphe] Crash lors de la suppression de plusieurs nœuds dans FX-Map
* [Performances] Le processus de Designer peut rester actif après la fermeture

### 9.3.1 (2019.3.1)

*(Publié Le 27 Janvier 2020)*

**Fixe :**

* [Graphe] Baisse et blocage importants des performances lors de l’ajustement d’un graphe imbriqué avec l’option « Modification contextuelle » activée
* [Graphe] Impossible de saisir une valeur enum sur [0, 99] dans Entier 1 tweak
* [Graphe] Le commentaire n’est pas déplacé lorsque le cadre correspondant est déplacé
* [Graphe] Les noms d’entrée sont manquants sur l’instancier personnalisé
* [Graphe] Le rendu des vignettes peut être effectué lors du chargement du graphe, même si l’option correspondante est désactivée dans les Préférences
* [vue 2D] La valeur alpha négative affiche le correcteur quelle que soit l’option d’affichage
* [vue 2D] La conversion de surface de 32f en 8bits échoue avec des valeurs élevées
* [vue 2D] Les options Inclinaison haut/gauche et Créer un carré définissent certaines coordonnées sur des valeurs énormes dans les matrices de transformation avant
* [vue 2D] Les UV de tous les objets de maillage ne sont pas affichés sur les Ensembles d&#39;UV autres que « 0 »
* [Contenu] Biseau : le mode Angular ne fonctionne pas correctement sur le masque de répétition
* [Contenu] Flood Fill au dégradé : la valeur de l&#39;image de pente n&#39;est pas échantillonnée au milieu de la forme
* [Contenu] Fonction ; « Booléen d’égalité » rompu
* [Bakers] Artefacts lors de l’utilisation du mappage automatique des tonalités dans le baker « Courbure à partir du Maillage » dans des cas spécifiques
* [Bakers] Crash dans DXR lors du baking alors qu’aucun matériau n’est sélectionné
* [Bakers] Problème de performances dans la vue 2D lors de l’activation de l’option « info »
* [Moteur] La fonction « Pow » génère des valeurs énormes lors de l’utilisation de valeurs d’entrée très faibles et d’un exposant élevé sur le moteur SSE2
* [Moteur] Crash lors de l’utilisation d’une compression jpg élevée sur des ressources bitmap
* [Moteur] Le Processeur de valeurs renvoie une valeur $size incorrecte à l&#39;intérieur d&#39;un sous-graphe
* [Paramètres] Une fenêtre contextuelle vide s’affiche lors de la sélection d’un instancier avec un grand nombre de paramètres
* [Paramètres] La valeur d’Entier n’est pas affichée dans les éléments de paramètre de la liste déroulante
* [Paramètres] Le bouton Modifier de la Matrice de transformation n&#39;est pas disponible en mode Aperçu
* [Cooker] $size dans ValueProcessor est incorrect à l&#39;intérieur d&#39;une instance de graphe
* [Cooker] La taille de sortie est incorrecte lorsque le lien de valeur passe par un nœud point vers un noeud atomique
* [UI] Le bouton permettant d’afficher tous les éléments de la barre inférieure de vue 2D n’est pas visible
* [UI] L’aperçu des valeurs de RGB sélectionnées affiche des nombres incorrects lors de l’utilisation de la gestion des couleurs
* [Export] Les images RVBA 16f sont exportées en niveaux de gris
* [vue 3D] Impossible d’importer un fichier OBJ avec plusieurs espaces
* [Gestion des couleurs] La configuration OCIO n’est pas prise en compte lors de la publication de sbsar
* [Color Widget] Les plages de curseurs de couleur peuvent se développer de manière exponentielle dans un cas spécifique
* [Doc] La section « paramValue » est incomplète dans la référence au format Sbs
* [MDL] Le widget de couleur dans les instances sbsar est incorrect
* [Paramètres prédéfinis] Crash lors de la mise à jour des paramètres prédéfinis dans un cas spécifique
* [PSD] Erreur FreeImage lors du chargement de fichiers PSD à partir de versions récentes de Photoshop
* [Ressources] Crash lors de l’annulation de la liaison Bitmap directement dans graphe
* [SVG] Les nœuds de SVG ne se mettent pas à jour automatiquement lors de l’utilisation des outils vectoriels

### 9.3.0 (2019.3.0)

*(Publié Le 19 Décembre 2019)*

**Ajouté :**

* [Général] Prise en charge de la gestion des couleurs avec le fichier de configuration OpenColorIO
* [Paramètres prédéfinis] Améliorer la gestion des paramètres prédéfinis
* [Paramètres prédéfinis] Synchroniser les widgets vue 2D et les curseurs d’aperçu
* [Paramètres prédéfinis] Restauration des valeurs d’aperçu lors du retour au mode Aperçu
* [Paramètres prédéfinis] Le mode Aperçu reste actif lors de la modification d’autres nœuds, ressources ou graphes
* [Paramètres prédéfinis] L’option Annuler fonctionne correctement lors de la navigation entre les 3 onglets de paramètres prédéfinis
* [Paramètres prédéfinis] Autoriser à réinitialiser les paramètres à la valeur par défaut du Graphe ou à la valeur du paramètre prédéfini en mode Aperçu
* [Paramètres prédéfinis] Amélioration de l’épinglage des paramètres
* [Paramètres prédéfinis] Importer/exporter tous les paramètres prédéfinis d’un graphe dans un fichier
* [Bakers] Nouvelle Courbure à partir du baker du maillage en fonction du raytracing
* [Bakers] Ajout d’une option de plan de sol dans « AO » à partir du baker du Maillage
* [Bakers] Option Ajouter la correspondance par nom pour ignorer la face arrière dans « AO » à partir du baker du Maillage
* [Contenu] Nouveau nœud d’Atlas scatter
* [Contenu] Nouveaux nœuds et fonctions de conversion de l’espace colorimétrique (ACEScg)
* [Contenu] Amélioration de la cohérence des noms pour les nœuds avec des versions en couleurs/niveaux de gris
* [Graphe] Amélioration des performances en mode Aperçu des paramètres prédéfinis
* [Graphe] Ajouter la macro $(colorspace) à l&#39;option d&#39;exportation des sorties du graphe
* [Paramètres] Lorsqu&#39;un paramètre est défini sur invisible, masquez le widget correspondant dans la vue 2D
* [Paramètres] N’ajoutez pas « Groupe d’entrée de Graphe » comme préfixe lorsque vous exposez des paramètres
* [Paramètres] Ajouter une info-bulle pour VisibleIf dans les paramètres de Graphe
* [AXF] Mise à jour du SDK AXF vers la version 1.6

**Fixe :**

* [Linux] Designer ne se lance pas sur CentOS 8 en raison d’un échec de chargement de la plateforme Qt.
* [Linux] AVERTISSEMENT : la bibliothèque Freetype a été supprimée de l&#39;application SD : les utilisateurs avec CentOS version &lt;= 7.5 doivent l&#39;installer manuellement.
* [AxF] Crash lors de l’importation de fichiers créés avec des versions AxF plus récentes
* [2DView] Les textures de pinceau alimentées par une ressource ne sont pas appliquées
* [2DView] Crash lors de la modification des entrées du graphe instancié avec ajustement de position
* [3DView] Crash lors de l&#39;annulation du chargement... action
* [3DView] Option Ajouter un espace colorimétrique pour les textures d’émission dans les nuanceurs GLSLFX
* [Bakers] Les mappages transmis par les ressources sont ignorés lors du baking
* [Bakers] Les options de Direction dans l&#39;espace monde ne sont pas correctement verrouillées
* [Bitmap] Les bitmaps EXR avec valeurs de point flottant sont rendus sous forme d’image noire
* [Contenu] Flood Fill à l’index : la détection de forme échoue dans un cas particulier
* [Contenu] Recadrage : problème d’échantillonnage lorsque le nœud de recadrage a une résolution inférieure à l’entrée
* [Général] Crash lors de la fermeture de Designer lors de la génération de la bibliothèque
* [Graphe] Les nœuds bitmap ne reflètent pas la compression du bitmap associé
* [Graphe] Le cache n’est pas effacé lors de l’effacement des vignettes de nœud après le premier rendu
* [Graphe] Taille de nœud incorrecte
* [Graphe] Crash lorsque, dans certains cas, lors de la modification des connexions d’entrée sur un nœud de Processeur de pixels
* [Graphe MDL] Échec lors de la restauration d&#39;une valeur par défaut d&#39;appel de fonction
* [Propriétés] Les boutons « Modifier » et « Matrice » dans les paramètres de matrice de transformation prêtent à confusion

### 9.2.3 (2019.2.3)

*(Publié Le 26 Novembre 2019)*

**Ajouté :**

* [MacOS] Authentifiez le logiciel pour respecter les nouvelles exigences de distribution de MacOS Catalina

**Fixe :**

* [Bakers] Crash lors du baking à l’aide d’une ressource de mappage incliné avec un lien non valide
* [Bakers] Les Ensembles d&#39;UV autres que 0 ne sont pas pris en compte sur Embree
* [Bakers] &#39;Bents normals des sorties du Maillage résultats incorrects avec des Ensembles d&#39;UV autres que 0 sur DXR
* [Bakers] La valeur 0 des paramètres Ensemble d&#39;UV est réinitialisée lors de la réouverture de la fenêtre de baking.
* [Bakers] « Position » génère une image noire avec des Ensembles d&#39;UV autres que 0
* [Contenu] Mosaïque automatique intelligente : problème d’échantillonnage dans 8k
* atlas splitter de [Content] : la détection de forme échoue dans certains cas, le paramètre de précision doit être exposé
* [Contenu] Pow ne renvoie pas la bonne valeur dans certains cas
* [Contenu] Flood Fill vers index : résultat incorrect lors de la publication sur sbsar
* crash [Library] lors du chargement du premier package SBS de la session
* [Bibliothèque] Le paramètre Afficher les ressources dans la bibliothèque par défaut est ignoré pour les ressources importées directement dans le panneau Explorateur
* [Console] Message inattendu dans la console lors de l’utilisation du menu des nœuds
* [Paramètres] Impossible de supprimer une seule entrée dans la liste d&#39;utilisation de la sortie
* [3DView] la scène n&#39;est pas rechargée correctement lorsque le fichier de scène est modifié sur le disque[Graphe] Le filtrage du menu Nœud est incorrect lors de l&#39;utilisation des sorties Valeur

### 9.2.2 (2019.2.2)

*(Publié Le 23 Octobre 2019)*

**Fixe :**

* [Graphe] Le filtrage du menu Nœud est incorrect lors de l’utilisation des sorties Valeur
* [Graphe] Crash lors de l’affichage du menu des nœuds
* [Graphe] L’outil de recherche s’affiche lors de l’utilisation du raccourci Maj
* [Graphe] Crash lors de la génération consécutive de menus de nœuds à partir du connecteur d&#39;entrée de valeur
* [Graphe] Les commentaires contenant de longues chaînes sont recadrés
* [Graphe] La mise en surbrillance du flux est incorrecte lors de la création d’un nœud à l’aide du menu Faire glisser depuis le connecteur
* [Graphe] Crash lors de la suppression de tous les éléments de graphe de la scène lors du chargement d&#39;un autre graphe
* [Graphe] Crash lors de l’utilisation pour créer un nœud lors de l’utilisation de cliquer-faire glisser depuis le connecteur
* [Graphe] Crash lors de l’utilisation de l’outil « Node Finder »
* [Graphe] La couleur de l&#39;épingle de sortie est incorrecte en mode « Compact Matériau »
* [Cooker] Les nœuds en aval des nœuds à sorties multiples ne se mettent pas à jour correctement
* [Cooker] Problème avec les sorties Value et les nœuds passthrough
* [Cooker] Le Processeur de valeurs génère des résultats incorrects lorsqu&#39;un seul nœud &#39;Get&#39; est utilisé
* [Contenu] Le nœud « Contraste/Luminosité » génère une valeur d’Alpha de 1,0
* [Contenu] Le modèle « Panorama Studio » ne contient aucune description
* [Contenu] Flood Fill à indexer : résultat incorrect lorsque l’entrée contient une forme d’enchaînement
* [Contenu] « Fusion HDR » : le calcul d’exposition interne est incorrect
* [Point Node] Crash lors de l’utilisation d’un niveau et d’un nœud en points
* [Gestionnaire de dépendances] L’action « Aller à » ne fonctionne plus
* [PSD] Crash lors de l&#39;annulation de la suppression de plusieurs nœuds qui étaient inclus dans l&#39;Exporteur PSD
* [UI] Crash lors de la fermeture du graphe à l’aide du menu « Fenêtre » et de l’ouverture d’un nouveau  lorsque l’un est épinglé
* [Éditeur de dégradé] Le bouton « Supprimer la clé » est trop grand
* [Moteur] Problème de précision avec sqrt() acos() et asin()
* [Bakers] AO À partir du Maillage : le curseur « Angle de répartition » a une plage de valeurs incorrecte lorsqu’il est modifié

### 9.2.1 (2019.2.1)

*(Publié Le 20 Septembre 2019)*

**Ajouté :**

* [Modèles] Ajout de noeuds d&#39;entrée par défaut à Specular/Brillance et à d’autres modèles
* [Modèles] Ajouter un modèle d’Anisotropie PBR
* [vue 3D] Augmenter les distances automatiques du plan de l’élément
* [vue 3D] PBR Coated : modifier la valeur par défaut pour l&#39;héritage du Coat normal
* atlas splitter [Contenu] : ajouter une option pour la fonction « Recadrage automatique »
* [Menu Nœud] Ne pas effectuer de noeuds de filtrage sans saisie

**Fixe :**

* atlas splitter [Contenu] : certaines sorties ne sont pas recadrées correctement lors de l’utilisation de l’option « Recadrage automatique »
* [Contenu] Fusion d&#39;Height du Matériau : erreur de cuisson liée à un paramètre inexistant
* [Contenu] « Lumière plane » : le mode d’UV du motif ne fonctionne pas correctement
* [Contenu] « Height à l’unité normale » : l’entrée est forcée sur 16 bits
* [Contenu] Formes inattendues lors de l’utilisation du nœud « Biseau » d’angular sans répétition sur les petites formes
* [Bibliothèque] Les icônes pour sbsar ne sont pas visibles dans la bibliothèque
* [Bibliothèque] L’utilisation de « \ » pour l’URL filtrage ne fonctionne plus
* [Bibliothèque] Les valeurs de filtre sont sensibles à la casse.
* Le filtre de recherche [Bibliothèque] ne fonctionne pas lorsque l’option « Composition » est cochée
* [Bakers] Si vous double-cliquez sur des cellules spécifiques et que vous ignorez la modification, elles reprennent des valeurs incorrectes
* [Bakers] Le texte d’état du serveur principal dans la fenêtre bakers affiche toujours « Accélération GPU : activer »
* [Cooker] Crash lors du traitement d&#39;une dépendance &#39;impostor&#39; dans un graphe
* [Cooker] la conversion en niveaux de gris a une taille de sortie incorrecte lors de l’utilisation de la valeur
* [Explorateur] Crash lors du traitement de « Publish sur le partage »
* [Graphe] Crash lors de l’ouverture d’un pack spécifique
* crash [MDL] lors de l’utilisation de l’opérateur de convertit
* [Modèles] Les identifiants de sortie ne sont pas corrects dans le modèle recouvert PBR

### 9.2.0 (2019.2.0)

*(Publié Le 29 Août 2019)*

**Ajouté :**

* [Contenu] Nouvelles formes « Lumière panoramique »
* [Contenu] Nouveau filtre « Nadir patch de panorama »
* [Contenu] Nouveau filtre « Nadir extract panorama »
* [Contenu] Nouveau filtre « Redresser l’horizon en panorama »
* [Contenu] Nouveau filtre « Rotation du panorama »
* [Contenu] Nouveau nœud « Position du panorama »
* [Contenu] Nouveau nœud « Panorama Physical Sun and Sky »
* [Contenu] Nouveaux nœuds « Dégradés en panorama »
* [Contenu] Nouveau filtre « Fusion HDR »
* [Contenu] Nouveau filtre « Aperçu HDR »
* [Contenu] Nouveau filtre « Color temperature adjustment »
* [Contenu] Nouveau nœud « Blackbody »
* [Contenu] Nouveau filtre « Exposition »
* [UI] Menu de création de nœud : afficher et gérer les favoris dans le menu
* [UI] Ajout/suppression d&#39;un nœud dans les favoris à partir du menu de création de nœud
* [UI] Menu de création de nœud : affiche le menu lorsque vous cliquez/faites glisser un lien à partir d&#39;une sortie
* [UI] Menu de création de nœud : filtrer le contenu en fonction du type de sélection actuel
* [vue 3D] Anisotropie de support
* [vue 3D] Effet Revêtement de support
* subsurface scattering de support [vue 3D]
* [Graphe] Nœud point
* [Graphe] Optimisation du rendu des graphes en mettant en cache les résultats de la cuisson
* [Préférences] Remplacez la valeur par défaut « Cooking Size Limit » par 8192
* [Préférences] Ajoutez un bouton à bascule pour activer/désactiver la nouvelle fonctionnalité de touche de tabulation
* [API] Méthode Add SDResource.getPackage()
* [Iray] Mise à jour vers le SDK NVIDIA Iray RTX 2019.1.3 (317500.3714)
* [Explorateur] Autoriser à lier n’importe quel type de fichier en tant que ressource dans le package
* [GradientNode] Appuyez sur Échap pour annuler le choix du dégradé
* [Paramètres] Supprimer les majuscules automatiques sur les identifiants
* [Projet] Ajoutez une option pour spécifier si les graphes et les ressources sont « visibles dans la bibliothèque » par défaut
* [Paramètres prédéfinis] épingle automatique des paramètres modifiés

**Fixe :**

* [MDL] Impossible d’exporter le module en raison d’un problème de type de paramètre
* [MDL] L&#39;entier Exposé n&#39;est pas visible lors du chargement
* crash [MDL] survenant lors de l’exportation MDL
* [MDL] Crash lors de la modification de la couleur d’un nœud de surface de matériau
* [MDL] void MDLGraphNodeControllerSelector::updateSelectorCurrentMember(const DataMessage&amp; msg) est rompu
* [Graphe] thickness de lien incorrect dans l’affichage du graphe
* [Graphe] Trop d’invalidations sont déclenchées lors de l’ajustement des paramètres.
* [Graphe] Crash lors de la fermeture d’un pack alors que deux fenêtres de celui-ci sont ouvertes et à l’aide de l’édition contextuelle
* [Graphe de fonction] L’avertissement n’apparaît pas lors de la fermeture de la vue de fonction
* [vue 3D] Crash lors de l&#39;initialisation de vue 3D lorsque la projection de caméra de données est définie comme orthographique comme état de scène par défaut
* [vue 3D] Le mode DOF post-effets reste activé dans Iray
* [Vue 2D] La fenêtre de sélection du pinceau disparaît lors de la modification de l’épaisseur du pinceau
* [vue 2D] Panneau Informations : les valeurs sont recadrées selon une disposition spécifique
* [vue 2D] L’image est décalée lors de la réduction et de la restauration de la fenêtre principale
* [Bakers] La liste de sélection « De la ressource » n&#39;est pas filtrée correctement
* [Bakers] Crash lors de l’enchaînement de bakers « Map de couleur à partir du maillage » et « Map normal depuis le maillage » sur Embree
* [Bakers] Courbure Par baking de Vertex entraîne des artefacts sévères
* [Explorateur] Impossible d’importer les ressources de l’UDIM en les faisant glisser dans l’explorateur
* [Explorateur] La fenêtre de l’Explorateur n’est pas correctement filtrée lors de la liaison de maillages et de polices après la liaison de formats de fichiers inhabituels
* [Explorateur] Les ressources sont visibles lorsque le paramètre « afficher dans la bibliothèque » du graphe est défini sur « non »
* [Contenu] Les entrées « Pow » et « clamp » ne sont pas dans le bon ordre
* [Contenu] Les entrées de nœud « Fusion RVBA » ne sont pas étiquetées
* [Cooker] Les connexions non valides des valeurs numériques sont quand même évaluées
* [Cooker] Assertion lors de la connexion d&#39;une entrée d&#39;image à une valeur d&#39;entrée
* [UI] Le curseur de la souris reste bloqué dans l’état « redimensionner » dans certains cas particuliers
* [UI] Le clic droit dans la vue du pack n&#39;affiche pas le menu correct sous Linux
* [Dépendances] Le chemin de fichier des ressources temporaires n&#39;est pas correct
* [Dépendances] L’avertissement de ressource bitmap manquante reste actif après le déplacement
* [Bibliothèque] Certaines vignettes ne sont pas générées
* [Bibliothèque] Les fichiers MDL sont affichés dans la bibliothèque
* [Paramètres] Crash lors de l’expose de paramètres
* crash [Paramètres] après la recréation d’un nouvel élément dans la liste déroulante
* [Export] Échec de l&#39;exportation par lots 8K
* [Paramètres prédéfinis] Crash lors de l’application d’un paramètre prédéfini impliquant des booléens dans les instances SBS
* [Scripting] L’écran « Bienvenue » apparaît toujours lors de l’utilisation de l’argument de ligne de commande « —quit »

### 9.1.3 (2019.1.3)

*(Publié Le 19 Août 2019)*

**Fixe :**

* [Bakers] Crash dans DXR lorsque les rapports L/H de la sortie baker et de la carte d’inclinaison ne correspondent pas
* [Bakers] L’Ambient occlusion du baker du Maillage génère des résultats incorrects avec Optix ou DXR lors de l’utilisation d’une Map normal
* [Bakers] Le baker « Courbure » génère des résultats incorrects lors de l’utilisation du paramètre « Par Vertex »
* [Bakers] Les messages d’erreur indiquent le back-end qui a échoué au lieu de la cause de l’erreur
* [Bakers] Crash lors du traitement d’un baker de mappage de détail sans maillage high poly
* [Bakers] Le mappage d’inclinaison ne semble pas affecter toutes les sorties lorsque DXR est activé
* [Content] mg\_leaks : faute de frappe dans le nom des paramètres
* [Contenu] « Forme » renvoie un avertissement de cuisson
* [Contenu] Les polygones 1 et 2 ne prennent pas en charge les fonctions aléatoires
* [Contenu] Les polygones 1 et 2 peuvent avoir moins de 3 côtés
* [Contenu] Normal à l’Height HQ ne fonctionne pas correctement dans un format non carré
* [Paramètres] paramètres d&#39;entrée d&#39;Entier : la liste déroulante n&#39;affiche pas les valeurs

### 9.1.2 (2019.1.2)

*(Publié Le 2 Juillet 2019)*

**Fixe :**

* [vue 3D] L’exportation vue 3D avec la profondeur de champ activée semble incorrecte
* [vue 3D] Le Canal Alpha des images de PSD est incorrect lors de l’utilisation du rendu d’enregistrement
* [vue 3D] Le PNG et le PSD sont rompus lors de l’utilisation de l’option Enregistrer le rendu avec Iray
* [Vue 3D] Le format dds ne fonctionne pas lors de l’enregistrement du rendu
* [Graphe] Les nœuds sont décalés lors de la combinaison des clics droit et gauche de manière spécifique
* [Graphe] La modification d&#39;instances de fonction ne met plus à jour le résultat du nœud
* [Graphe] Crash lors de l’affichage du menu de la barre d’espace
* [Contenu] Extrusion de forme : problème de qualité lorsque la forme n’a pas de rotation.
* [Contenu] L’ombre portée de forme (et les niveaux de gris) ne produit pas d’ombre sans répétition H et V
* [Contenu] Problème de recadrage Matériau normal
* [Bakers] Les paramètres prédéfinis de bakers JSON ne sont pas chargés correctement
* [Bakers] Crash lors du baking de maillages lourds à l’aide d’Optix ou de DXR (il peut désormais échouer en raison d’une Vram insuffisante, mais il ne crash pas)
* [Éditeur de bitmap] Les outils de peinture bitmap décalent les contours et les redessinent dans le cadre de sélection des contours
* [Éditeur de bitmap] Outils de peinture bitmap rompus dans OSX
* [UI] Le menu de certains boutons est à peine accessible
* [UI] Crash lors du glisser-déposer d&#39;une instance de baker
* [SVG] Les outils de modification de SVG intégrés ne sont pas fiables
* [Paramètres] Crash lors de l&#39;application d&#39;un paramètre prédéfini avec des paramètres booléens dans une instance SBSAR
* crash [Réseau] parfois lorsqu&#39;une erreur se produisait dans une connexion chiffrée SSL

### 9.1.1 (2019.1.1)

*(Publié Le 28 Mai 2019)*

**Ajouté :**

* [Intégration Python] Enregistrement et restauration de l’état du gestionnaire de plug-ins
* [Préférences][Dépendances] Ajoutez une option pour déterminer comment le chemin du fichier de dépendances est stocké
* Mappeur de Flood Fill [Content] : ajout d’une option « Adapter la forme BBox »

**Fixe :**

* [Contenu] Mappeur de Flood Fill : « Rotation Auto Scale » a l’effet inverse
* [Contenu] L’entrée « luminance\_offset\_map » n’est pas utilisée par « Couleur du mappeur de Flood Fill »
* [Contenu] Le nœud « Niveaux de gris du mappeur de Flood Fill » génère des artefacts d’étape
* [Content] Impossible de publier l&#39;Height Extrude
* [Paramètres] Les paramètres prédéfinis incorporés dans sbsar ne sont pas chargés dans Designer
* Le nom du Baker [Baker] ne s&#39;affiche pas correctement dans la liste des bakers
* [vue 3D] « Afficher les sorties en vue 3D » ne fonctionne pas pour les valeurs
* [Cooker] Crash lors de la correction d’un type de paramètre incorrect
* [API] La fonction SDResource.setInputPropertyFromId ne fonctionne pas sur les paramètres d&#39;entrée SDSBSCompGraph
* [Updater] certains sbs ne peuvent pas être mis à jour en 2019
* [Explorateur] Crash lors de l’importation d’un fichier .obj spécifique
* [Intégration Python] Les barres obliques inverses ne s&#39;affichaient pas correctement sous Windows lors de l&#39;initialisation de PYTHONPATH
* Problème de valeur [UI] avec certains curseurs dans les bakers
* [Linux] Designer ne peut pas être exécuté sous CentOS &lt; 7.6

### 9.1.0 (2019.1.0)

*(Publié Le 9 Mai 2019)*

**Ajouté :**

* [API] Ajoutez le paramètre « updatePackages » à la méthode SDPackageMGR.loadUserPackage() pour contrôler si les programmes de mise à jour doivent être appliqués ou non lors du chargement
* [API] Ajout de la possibilité de déconnecter une connexion SDConnection
* [API] Ajout de la classe SDSBSARExporter pour publier un package SDP
* [API] Ajoutez la classe SDHistoryUtils pour gérer les commandes annulables.
* [API] Ajout d’une définition de noeud d&#39;entrée en niveaux de gris dans le Graphe de composition de Substances (sbs::compositing::input\_grayscale)
* [API] Ajout d’une définition de noeud d&#39;entrée de valeur dans le Graphe de composition de Substances (sbs::compositing::input\_value)
* [API] Méthode Add SDProperty.isFunctionOnly()
* [API] Ajout de la prise en charge du paramètre d&#39;entrée personnalisé sur SDSBSCompNode
* [API] Ajoutez le paramètre reloadIfModified à la méthode SDPackageMGR.loadUserPackage() pour contrôler si un package doit être rechargé en cas de modification
* [API] Méthode Add SDPackageMgr.getPackages()
* [API] Ajout de la possibilité d’obtenir/d’ajouter/de supprimer des chemins racines de SDModuleMgr
* [API] Permet d’obtenir le pointeur du buffer des pixels et la hauteur de ton d’une texture SDT
* [API] Autoriser à récupérer le pointeur de la fenêtre principale
* [API] Permet de créer des menus personnalisés dans le menu principal
* [API] Autoriser à créer des DockWidgets personnalisés dans la fenêtre principale
* [API] Utilisation des noms d’objet pour rechercher des menus dans les barres d’outils
* [API] Fournir un système permettant de gérer les notifications d’application à l’API
* [Intégration Python] Ajout d’une variable d’environnement par défaut pour rechercher les plug-ins Python
* [Intégration Python] Ajout de la recherche de texte et remplacement dans l’éditeur Python
* [Intégration Python] Instanciation des plug-ins Python au démarrage
* [Intégration Python] Prise en compte de la variable d’environnement PYTHONPATH
* [PythonIntegration] Autoriser la création de barres d’outils dans les widgets de graphe
* [Intégration Python] Prise en charge des threads Python
* [Intégration Python] Ajout d’un gestionnaire de plug-ins (dans le menu Outils )
* [Contenu] Rotation vectorielle normale : ajoutez une entrée d’image facultative pour déterminer l’angle
* [Contenu] Nouveau filtre Min/Max
* [Contenu] Nouveau filtre « Flood Fill vers index »
* [Contenu] Nouveau filtre « Mappeur de Flood Fill »
* Filtre Nouvel Atlas splitter [Contenu]
* [Contenu] Amélioration du filtre Tri Planaire
* [Contenu] Nouveau filtre de Non Uniform Directional Warp
* [Contenu] Nouvelle Déformation directionnelle multiple
* [Contenu] Nouveau filtre d’Height Extrude
* [Moteur] Fxmap : nouveau modèle « Graduation avec décalage »
* [Moteur] Prise en charge du traitement uniforme des valeurs (nouveau nœud de Processeur de valeurs)
* [vue 3D][Bakers] Améliorer les performances du chargeur OBJ
* [vue 3D] Augmentez les distances des plans du clip de caméra
* [Préférences] Ajout de paramètres pour les Bakers
* [Graphe] Accélérez l&#39;invalidation en évitant les comparaisons de chaînes
* [MDL] Prise en charge des baies MDL
* [UI] Améliorations de l&#39;interface utilisateur de sélection de Moteur
* [Iray] Mise à niveau vers Iray SDK 2018.1.4
* [Gestionnaire de dépendances] Utilisez le « dernier chemin » pour redéfinir l&#39;emplacement une ressource.
* [Cuisine] Ajouter la prise en charge des étiquettes de Booléen dans le sbsar
* Intégration de Qt 5.12.2

**Fixe :**

* [Graphe] Les connexions sont rompues lors de la modification du nom de l’entrée
* [Graphe] Trop d’invalidations sont déclenchées lors de l’ajustement des paramètres.
* [Graphe] L’action « Copier dans le Presse-papiers » ne fonctionne pas si nous faisons un clic droit sur un badge
* [Graphe] Le déplacement d’un cadre à l’aide d’Alt n’est pas stocké dans le fichier .sbs
* [MDL] Le Profil colorimétrique n’est pas automatiquement mis à jour dans l’éditeur MDL
* [MDL] crash lors de l&#39;exportation d&#39;un module contenant une configuration spécifique
* [MDL] Échec de l’exportation d’un Graphe MDL contenant un LightProfile ou une ressource MBSDF
* [UI] Les raccourcis ne s’affichent plus dans les menus contextuels
* [UI] La fenêtre flottante devient ancrable après le redémarrage
* [Scripting] L’option Annuler ne fonctionne pas dans l’éditeur Python
* [Scripting] L’option « oui à tout » dans le menu Enregistrer ne fonctionne pas
* La liste déroulante [Paramètres] ne s’affiche pas correctement après la copie
* [Explorateur] Les ressources de Redéfini l&#39;emplacement doivent ouvrir le dernier chemin redéfini l&#39;emplacement par défaut
* [Bibliothèque] Le contenu de la bibliothèque est toujours reconstruit lors du passage d’une version à une autre
* [Bibliothèque] Les bitmaps importés sont invalidés lors de l’enregistrement
* [Iray] L&#39;espace de Tangente n&#39;est pas calculé correctement / mappage normal incorrect
* [Fonction] Crash ou échec lors de la création d&#39;un nouveau graphe à partir de la sélection
* [API] la valeur par défaut des propriétés n’est pas définie

## Version 8

### 8.3.4 (2018.3.4)

*(Publié Le 12 Avril 2019)*

**Ajouté :**

* [Contenu] Transforme normal/Transforme de Matériau : ajoutez une option pour activer la transformation Échelle et Inclinaison

**Fixe :**

* [Contenu] Le filtre Tourbillon ne fonctionne pas correctement lorsque des fonctions aléatoires sont utilisées dans les fonctions de paramètres
* [Contenu] Transforme normale/Transforme de Matériau : la normale n’est pas normalisée après une transformation d’échelle
* [Contenu] Le tourbillon donne des résultats incorrects lorsque la quantité est aléatoire
* [Graphe] Crash lorsque vous faites glisser une sortie tout en maintenant la touche maj enfoncée, puis que vous passez en maintenant la touche ctrl enfoncée
* [Graphe] Crash lors de la manipulation de points de fractionnement
* [Graphe] Baisse des performances lors de l’affichage des badges de nœud
* [Scripting] L’utilisation d’actions personnalisées peut avoir un crash après 30 secondes.
* [Préférences/Projets] Les scripts activés de tous les projets doivent être exécutés (dans la section « Scripts »).
* [MDL] crash lors de la liaison d&#39;un Graphe MDL à un autre Graphe MDL
* [Paramètres] Les nœuds ne sont pas mis à jour après avoir défini la valeur de départ aléatoire du graphe sur un paramètre exposé
* [PSD] L’affectation d’un nœud de couleur modifie la taille des vignettes de calque, contrairement à l’affectation d’un nœud en niveaux de gris
* [API] Exception non gérée avec SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Publié Le 19 Février 2019)*

**Fixe :**

* [Contenu] Les sorties de Matériau de base PBR n&#39;ont pas le bon nom de groupe

### 8.3.2 (2018.3.2)

*(Publié Le 19 Février 2019)*

**Ajouté :**

* [Bakers] Ajoutez un libellé indiquant le paramètre de suffixe actuel pour « Correspondance par nom ».

**Fixe :**

* [Graphe] Crash lors de la manipulation de points de fractionnement
* [Graphe] Problème d’invalidation lors de la modification de la résolution de noeud d&#39;entrée
* [Graphe] Les options de calcul des vignettes ne fonctionnent plus
* [Graphe] Un espace vide est affiché sous le chemin de navigation avec une disposition d’interface utilisateur spécifique
* [Graphe] Le style de lien est incorrect dans le contexte
* [Graphe] Les vignettes ne s’affichent pas correctement dans les graphes de fonction/mdl sur les écrans Hi DPI
* [Contenu] Couleur de la Fusion des éclaboussures de forme : aucune option pour spécifier le format de map normal
* [Contenu] Faute d’orthographe dans l’info-bulle de l’interpolation linéaire
* [Contenu] Le Transforme Normal ne gère pas correctement les transformations de symétrie et d’inclinaison
* [Contenu] Les dégradés axiaux, radiaux et circulaires ne prennent pas en charge les fonctions aléatoires
* [Contenu] Le dégradé radial ne fonctionne pas correctement dans un format non carré
* [API] output\_exporteur.sbs doit toujours être mis à jour lors de l’utilisation du script export\_output
* crash [API] après utilisation du script export\_output
* [API] Impossible de définir la valeur numérique des annotations sur les entrées du Graphe de composition
* [Explorateur] crash aléatoire lors de l’enregistrement d’un projet
* [Explorateur] Impossible d’ouvrir les fichiers sbs avec l’extension en majuscules
* [UI] La taille de la fenêtre « Nouvelle Substance » n&#39;est pas persistante
* [UI] Le menu contextuel sur l&#39;instance de fonction n&#39;est pas cohérent avec le graphe de composition
* [Bakers] Crash lors de l’ouverture des bakers sur un maillage spécifique
* [Bakers] calcul incorrect pour les bakers DXR lorsque les UV ont une valeur d’ordonnée de 0
* [Updater] Crash lors de l’annulation du programme de mise à jour
* [vue 3D] Les UV de la sphère primitive sont décalés de 1 unité
* [Cuiseur] dithering aléatoire lors de la cuisson d’images bitmap
* [Lecteur] Les boutons de commande des fenêtres sont petits
* [Lecteur] Les icônes des boutons ne fonctionnent plus

### 8.3.1 (2018.3.1)

*(Publié Le 20 Décembre 2018)*

**Ajouté :**

* [API] Ajouter SDConnection.getOutputProperty() et SDConnection.getOutputPropertyNode()
* [API] Ajout d’un document sur toutes les définitions de ressources
* [API] Pour des raisons de cohérence, remplacez la propriété d&#39;annotation SDSBSCompNode « visible if » par « visible\_if »

**Fixe :**

* [Graphe] Appuyer une deuxième fois sur la touche TAB ne ferme pas le menu Nœud
* [Graphe] les badges vue 3D ne fonctionnent pas correctement dans certaines situations
* [Graphe] Les packages en lecture seule peuvent être modifiés.
* [Bakers] La barre de progression agit de manière étrange lors du chargement d&#39;un très maillage high poly
* [Bakers] Artefacts sur le maillage avec des normales orientées vers l’intérieur
* [Bakers] impossible de réduire la sortie des Bakers et le widget de paramètres
* [Explorateur] Les ressources 3D sont chargées à l’ouverture d’un pack
* [CmdLineArgs] « —news hide\_changelog:true » ne fonctionne plus

### 8.3.0 (2018.3.0)

*(Publié Le 5 Décembre 2019)*

**Ajouté :**

* [Graphe] Ajout d’un chemin de navigation lors de la modification de sous-graphes/fonctions
* [Graphe] Ajoutez TAB comme raccourci pour générer le « menu des nœuds »
* [Graphe] Surligneur de nœud pour les nœuds parents de la sélection
* [Graphe] Ajoutez Ctrl+E en tant que raccourci pour ouvrir la fonction de Processeur de pixels et les sous-graphes
* [Graphe] Connecter le nouveau nœud à la première sortie visible du nœud sélectionné
* [Graphe] Ajouter un nœud « Badges »
* [Graphe] Ajout d’un avertissement sur les nœuds de composition via des badges
* [Graphe] Ajouter la possibilité de rechercher un nœud par son nom, ses attributs ou son UID
* [API] Autoriser à créer et à modifier des données
* [API] Autoriser l’exportation de SDPackage et de SDMDLGraph vers les Modules MDL (voir SDMDLExporter)
* [API] Permet de récupérer tous les nœuds, énumérations et définitions de structure (voir SDModuleMgr)
* [vue 3D] Basculer vers les cubes pour le moteur de rendu OpenGL
* [vue 3D] Exportation d’une image hdr linéaire lors de l’enregistrement au format .exr ou .hdr
* [Bakers] Intégration de la technologie DXR raytracing
* [Iray] Intégration d’Iray SDK 2018.1
* [Moteur] Prise en charge du Moteur SSE (CPU) pour le traitement d’image en virgule flottante hdr
* [Moteur] Ajoutez une option de ligne de commande (—gpu x) pour spécifier le périphérique GPU dédié au moteur de Substance
* [Contenu] Nouveau nœud de Rendu PBR
* [UI] Onglets de retouche et barre de titre
* [Gestionnaire de dépendances] Empêcher la mise à jour de la liste des dépendances lorsque les actions utilisateur n&#39;affectent pas les dépendances

**Fixe :**

* [Graphe] Crash lors de l&#39;instancie d&#39;un graphe sur lui-même
* [Graphe] Le nœud dupliqué n&#39;est pas sélectionné
* [Graphe] problème de calcul lors de l&#39;utilisation d&#39;une même instance de nœud dans 2 Graphes MDL différents
* [Graphe] la touche Z doit centrer la vue au centre de la zone de scène
* [Graphe] Ignorer l’espace colorimétrique dans les règles de connexion lors de l’utilisation du lien de matériau
* [Graphe] Évitez d’ouvrir les sorties en vue 3D lors de l’ouverture d’un graphe dans conli
* [Graphe] Le collage des nœuds est lent lorsque l’option « Ouvrir le nœud nouvellement créé » est activée
* [Vue 3D] Affirmation lors du glisser-déposer d’un maillage spécifique
* [Vue 3D] L’option Échelle UV activée ne fonctionne pas sur la map height
* [Content] Tri-Planaire : Divers problèmes concernant l&#39;axe et les transformes
* [Contenu] Flou de Pente Niveaux de gris : l’un des échantillons n’a pas le mode de fusion approprié lors de l’utilisation de min ou max
* [Contenu] Dégradé linéaire 2 mauvais résultat en basse résolution
* [API] SDPackage.findResourceFromUrl() peut également récupérer des ressources situées dans un autre SDPackage
* [API] SDPackage.getChildrenResources() renvoie toujours le premier élément en mode non récursif
* [API] [Documentation] Les énumérations, structs situés dans le dossier « généré » ne sont pas reflétés dans la documentation
* [UI] La largeur de Vue 2D ne doit pas être contrainte
* [Dégradé] Crash en sélectionnant Mac
* [Explorateur] Crash lors de la fermeture et de la réouverture d’un graphe
* [Mac] Le sélecteur de couleurs ne fonctionne pas sur plusieurs écrans
* [Paramètres] Le compteur sur les paramètres d’entier ne fonctionne pas
* [Cooker] Crash lors de la création de certains nœuds sous OSX 10.13
* [Filtre de courbe] Les touches et les points de contrôle peuvent se retrouver avec une valeur -0,0 ou une valeur bizarre « presque zéro » dans l’éditeur de courbe
* [vue 2D] Le widget Position n’est pas disponible pour les graphes provenant de sbsar
* [PSD] Problème de calque après l’exportation avec des dépendances

### 8.2.2 (2018.2.2)

*(Publié Le 4 Octobre 2019)*

**Fixe :**

* [Contenu] L’ombre de la forme ne fonctionne pas correctement lorsque la répétition est désactivée
* [Contenu] Le remplissage par diffusion aléatoire en niveaux de gris/couleur ne fonctionne pas correctement dans certains cas
* [Contenu] Le Flood Fill est incorrect dans les caractères non carrés
* [Contenu] Le Flood Fill de Couleur/Niveaux de gris est rompu
* [Contenu] QuadTransform est irrégulier dans le processeur
* [Contenu] La forme en étoile génère un mode de répétition « Pas de Répétition »
* [Contenu] Couleur de la Fusion des éclaboussures de forme avec une résolution absolue de 32f bits
* [Contenu] La couleur de Fusion des éclaboussures de forme est longue à calculer si son format n’est pas défini sur 32F
* [Graphe] Crash lors de la liaison d’une image en tant qu’entrée d’une Fx-Map lorsque les propriétés Itérer sont affichées
* [Graphe] Le minutage semble incorrect lors de la modification du graphe en contexte
* [Graphe] crash aléatoire lors de l’enregistrement du graphe
* [Graphe] Le mode de matériau ne fonctionne pas avec sbsar
* [vue 3D] L&#39;affectation de Matériau n&#39;est pas restaurée correctement
* [vue 3D] Certains paramètres du fichier d’état 3Dview ne sont pas chargés correctement
* Affichage de l’Alpha [vue 2D] toujours en noir
* [vue 2D] Le bouton Afficher l’image en niveaux de gris ne fonctionne pas pour les images avec alpha
* [UI] Le gestionnaire de dépendances apparaît au démarrage même lorsqu’il n’est pas activé sur Mac
* [UI] Certains boutons effectuent des actions même lorsque vous relâchez la souris à l’extérieur
* crash [API] lors de la tentative de maintien d’un élément de tableau en dehors de la portée du tableau d’où il provient
* [Graphe MDL] L’aperçu du nœud est inversé
* [Graphe MDL] Le Displacement du nœud de prévisualisation est différent de celui de la vue 3DV
* [Console] Les performances sont très lentes lorsque la console contient de nombreux messages
* [Console] Alertes Qt lors du lancement de Designer sous CentOS
* [FX-Map] Crash lors de la suppression des liens entre les entrées et FX-map
* [Functions] Impossible de définir un nœud de type chaîne comme sortie dans la ressource de fonction
* [Préférences] Le menu Préférences n’est pas activé. L’utilisateur peut accidentellement modifier une valeur lors du défilement
* [FX-Map] La zone de liste déroulante Index d’Image d&#39;entrée n’est pas mise à jour correctement lors de l’ajout/la suppression d’entrées
* crash [Dépendances] lors de la suppression de ressources UDIM utilisées dans un graphe
* [API] SDLocationContext.getCurrentGraph() renvoie toujours la valeur null
* [Publish] URL de Substance Player de la page de téléchargement incorrecte

### 8.2.1 (2018.2.1)

*(Publié Le 17 Août 2018)*

**Ajouté :**

* [UI] Ajoutez un message dans la barre des tâches lorsque l’option « Édition contextuelle » est activée
* [Préférences] Reformulation de l’étiquette de l’option « Modification contextuelle »

**Fixe :**

* [Graphe] Le raccourci Coller sans lien ne fonctionne pas dans le graphe de composition
* [Graphe] L’invalidation est très longue lorsque l’édition contextuelle est activée
* [Graphe] Crash lors de la liaison de nœuds
* [Graphe] Réassociation de nœuds de Crash
* [Graphe] Crash déplacement des cadres
* [Graphe] Le Crash lors du basculement de UVTile dans graphe et maillage n&#39;est plus udim
* [Graphe] Crash lors de l’utilisation de ctrl+z après le collage des nœuds
* [Graphe] La sélection des nœuds parents est très lente
* [Bakers] Le déplacement de mappages vers le haut/vers le bas permet à l’utilisateur de redimensionner la ligne
* [Baker] Le chemin d’enregistrement ou de chargement du paramètre prédéfini n’est jamais enregistré.
* La Cage [Baker] est utilisée même lorsqu’elle n’est pas sélectionnée dans la fenêtre de baking
* La Correction des déviations [Baker] ne fonctionne pas correctement
* [Bakers] Performances très lentes lorsque l’espace UV est négatif dans la vue
* [Bakers] Cliquer sur le bouton Annuler n’annule pas le chargement du maillage
* [Bakers] Impossible de baker à l’aide d’une cage si la carte d’inclinaison est vide et définie sur true
* [Contenu] Le Flood Fill est lent en 4K
* [Contenu] La fonction Linéaire à sRVB est rompue
* [Contenu] Carreau Arrière-plan aléatoire en niveaux de gris piloté par un flotteur4 au lieu d’un flotteur, empêche la cuisson
* [Contenu] Éclaboussure de forme : le multiplicateur de position/mappage vectoriel ne fonctionne pas correctement
* [Scripts] Ctrl + o ne fonctionne pas dans l’éditeur Python
* [Scripting] L’éditeur Python envoie des invites même après la fermeture
* [Scripting] Blocage lors de la création de plusieurs nouveaux scripts
* [UI] Les icônes de la bibliothèque sont pixellisées
* [UI] Les panneaux flottants par défaut se comportent mal
* [Explorateur] Crash importation d’un maillage sous CentOS
* [Explorateur] maillage UDIM chargé deux fois
* [Cooker] Aucune durée pour les nœuds dans le contexte
* [Cuiseur] Débordement de Pile lors de la cuisson
* [Licence] Authentification incorrecte avec des informations d’identification valides
* [Licence] Licence flottante signalée plusieurs fois pour le même utilisateur
* [Vue 3D] La valeur V par défaut du matériau UV est incorrecte
* [vue 3D] Régression des performances par rapport à 2018.1.x
* [Préférences] Crash lors de l’utilisation d’un fichier de configuration à partir d’un serveur
* [Bibliothèque] Crash de suppression d’un filtre à l’intérieur de la bibliothèque
* [SVG] Problème de dépendance lors de l’utilisation de l’alias
* [Niveaux] Les bitmaps HDR 32 bits font clignoter l’éditeur de niveau lors du déplacement de la position des widgets
* [PSD] La fenêtre du PSD d&#39;importation lié s&#39;affiche deux fois
* [Iray] La Scène est mise à jour lorsqu’un éclairage désactivé est modifié
* [MDL] Crash lors de la suppression de tous les nœuds d&#39;un modèle MDL
* [Moteur] Une grande quantité de décalage dans FX-Map peut bloquer le SD
* Crashs du crashpad au démarrage
* La variable d’environnement Python rend Designer crash au lancement

### 8.2.0 (2018.2.0)

*(Publié Le 19 Juillet 2018)*

**Ajouté :**

* [UI] Nouveau style
* [UI] Nouveaux curseurs
* [UI] Rendre les fenêtres flottantes vraiment flottantes
* [UI] Modification de la disposition de la fenêtre Préférences
* [UI] Bibliothèque : supprimer la barre de filtre
* [UI] Bibliothèque : supprimer l&#39;incrustation d&#39;affichage de la sélection
* [UI] Ajoutez un message dans la barre des tâches lorsque l’application enregistre automatiquement un pack
* [UX] Propriétés : fusionner les menus « function » et « reset to default »
* [Contenu] Nouveaux nœuds Shape Splatter (+ filtres compagnon)
* [Contenu] Ajout d’un Flood Fill aux filtres Couleur/Niveaux de gris
* [Contenu] Nouvelle prise en charge du Flood Fill : prise en charge des formes avec des trous
* [Contenu] Flood Fill au dégradé : ajout d’une entrée d’image Pente et angle
* [Contenu] Optimisation du filtre Niveau automatique
* [Contenu] Nouveau filtre Extrusion de forme
* [Contenu] Transforme de Matériau : ajout de la prise en charge des maps normal pivotées
* [Contenu] Nouveaux filtres Rotation vectorielle normale et Transforme normal
* [Contenu] Normaliser : améliore la qualité des résultats.
* [Contenu] Nouveau Transforme Trapezoid
* [Contenu] Nouveau filtre Transforme Quad
* [Contenu] Ajout d’un motif hémisphère au nœud Shape
* [Contenu] Ajout de nouveaux dégradés avec des commandes dans la vue 2D
* [Contenu] Ajouter une sortie UV au nœud « Cube GBuffers »
* [Graphe] Cadre : ignore le texte du titre plus grand que la zone du cadre pour la sélection
* [Graphe] Ajout de la prise en charge de l’édition contextuelle des sous-graphes (expérimental)
* [Graphe] La création du Cadre/Commentaire doit affecter le nœud sous le curseur lors de l&#39;utilisation de RMB
* [Graphe] Cadre : ignore le texte du titre plus grand que la zone du cadre pour la sélection
* [Graphe] Réutilisation de l’onglet existant lors de l’ouverture d’une fonction déjà ouverte
* [Graphe] Création d’un nouvel onglet lorsque « Ouvrir la référence » est utilisé
* [Graphe] Fonction : n’affichez pas les propriétés de la fonction lorsque vous cliquez sur l’arrière-plan
* [Paramètres] Supprimer le bouton « Exposer » des graphes fxmap
* [Paramètres] Niveau : Ajouter un bouton « Inverser »
* [Paramètres] Développez le groupe « Paramètres d&#39;entrée » lors de la création d’un nouveau paramètre d&#39;entrée
* [Propriétés] Ajoutez les informations d’URL du package dans les attributs de graphe
* [Propriétés] Augmentez la taille du champ de description pour les nœuds de sortie
* [Propriétés] Autoriser à entrer la fonction par pixel du Processeur de pixels même pour les packages en lecture seule
* [Scripts] Nouvelle API Python / Éditeur Python (première itération)
* [Bakers] Optimisation du transfert de géométrie pendant le rendu
* [vue 3D] Basculer vers le profil OpenGL Core
* [vue 3D] Prise en charge de la testation/du displacement sur Mac
* [Fonctions] Ressource de fonction : répertorie les entrées d’image dans les nœuds d’échantillonnage

**Fixe :**

* [Graphe] crash lors de la liaison d&#39;un nœud à un autre
* [Graphe] l’obtention de variables dans la fonction de générateur aléatoire de graphe ne fonctionne pas
* [Graphe] crash lors du glisser-déposer de bruit dans un graphe
* [Graphe] crash lors de l’ouverture d’un graphe spécifique
* [Contenu] Le résultat est différent entre Couleur aléatoire des carreaux et Niveaux de gris
* [Contenu] Mosaïque aléatoire : le résultat change lors de la modification du « Mode aléatoire de Symétrie »
* [Contenu] La détection des contours ne fonctionne pas avec des résolutions non carrées
* [Bakers] Artefacts lors du baking de la courbure à l’aide d’un maillage UDIM
* [Bakers] La carte d&#39;Ambient occlusion du maillage est inversée lors de l&#39;utilisation d&#39;une map normal
* [Bakers] la liste des Ensembles d&#39;UV doit être restreinte aux Ensembles d&#39;UV disponibles
* [Explorateur] crash lors de la suppression de ressources lors du baking
* [Transforme 2D] Crash lors de l’expose du niveau de mappage Mip et des paramètres de couleur d’arrière-plan
* [Transforme 2D] Comportement incorrect lors de l’expose d’un Niveau du mipmap de Transforme
* [PSDExport] L’exporteur de PSD n’exporte pas correctement les niveaux de gris 32F
* [vue 2D] Le calcul d&#39;histogramme ne fonctionne pas avec les nœuds 16F
* [PSD] Le PSD lié est rompu
* [Cooker] La fonction dans le paramètre outputsize n&#39;est pas évaluée correctement
* [Export] Le chemin des sorties d&#39;exportation doit être le même que le chemin du package
* [Export] Le chemin d&#39;exportation n&#39;est pas enregistré avec un motif vide
* [Modèles] Groupe manquant pour Position dans le modèle Painter
* [Aide] l’aide de la ligne de commande n’affiche pas —news sur Mac
* [Dépendances] L’exportation à deux reprises après la modification d’un nom de dossier ne fonctionne pas

### 8.1.2 (2018.1.2)

*(Publié Le 31 Mai 2018)*

**Ajouté :**

* [vue 3D] Autoriser à définir l’état d’éclairage par défaut dans les paramètres du projet
* [Gestion de versions] Supprimer le délai d’expiration de 30 s lors de l’appel des scripts python

**Fixe :**

* [Contenu] Base de Somme fractale : résultat incorrect avec le troisième niveau (un nouveau graphe a été ajouté)
* [Contenu] Fractal du Bruit Perlin 3D forcé à 32 bits
* [Contenu] Le dégradé linéaire 3 ne donne pas le bon résultat lors de l&#39;utilisation d&#39;une taille non uniforme
* [Contenu] Sobel normal ne prend pas en charge les options de répétition
* [Contenu] Le vérificateur\_1 est forcé à 8 bits.
* [Contenu] Multiangle vers la normale : problème du calcul intérieur
* [Contenu] Le motif Stripe ne prend pas en charge les valeurs négatives « Maj » (crash par moteur)
* crash [MDL] lors de la tentative d’ouverture d’un projet MDL spécifique
* [MDL] Le Graphe MDL n&#39;est pas calculé après une opération de fermeture/réouverture
* [Exporter] Les sorties des graphes non attribués sont exportées à l’aide de l’outil de traitement par lots
* [Export] L&#39;exportation de C16F dans exr génère une image en niveaux de gris
* [Baker] Les fonctionnalités d’inclinaison ne sont pas désactivées dans l’interface utilisateur lors du baking avec une cage
* [Bakers] Crash lorsque la cage n’a pas l’Ensemble d&#39;UV correspondant
* [Cooker] sbscookie : erreur de cuisson liée à « blend\_switch.sbs »
* [Cooker] Le graphe publié ne s’affiche pas correctement
* [Moteur] Transformation 2D : couleur de cache incorrecte
* crash [Explorateur] lors de la réimportation d’un maillage FBX
* [Color Widget] Le sélecteur de couleurs en niveaux de gris sélectionne uniquement la valeur de la couche rouge
* [vue 3D] L’utilisation de « textcoordN » ne fonctionne plus
* [Iray] La Map normal est appliquée deux fois pour les diélectriques

### 8.1.1 (2018.1.1)

*(Publié Le 12 Avril 2018)*

**Ajouté :**

* [vue 3D] Définir la plage par défaut du « Facteur de tessation » sur [0, 16]

**Fixe :**

* [vue 3D] Artefact visuel étrange avec un GPU AMD spécifique
* [vue 3D] Blocage avec des GPU AMD spécifiques
* [vue 3D][Bakers] Les normales générées à partir de .obj ont des contours nets à l&#39;UV
* [vue 3D] Crash lors du calcul des harmoniques sphériques
* [Baker] Impossible de définir la ressource comme « incorporée »
* [Bakers] crash lors du baking
* [Bakers] Le Baking de 2 versions différentes d&#39;un mappage à partir du maillage UDIM est rompu
* [Bakers] crash lors du basculement entre le graphe contextuel et non contextuel
* [Bakers] Si vous avez le même baker deux fois, ils seront synchronisés
* [Bakers] renommer la macro $(custom) empêche de baker correctement
* [Bakers] L’actualisation d’une map bakée devrait bloquer l’interface utilisateur
* [Bakers] L’option Actualiser toutes les maps bakées crée des ressources vides
* [Bakers] Appuyer sur « Entrée » pour confirmer une valeur de paramètre supprime le poly élevé
* [Contenu] Tile Generator : erreur aléatoire de rotation lorsque les valeurs X et Y sont différentes
* [Contenu] certains mappages usure/salissures contiennent des instances de fantôme
* [Contenu] Cube 3D : l’utilisation de fonctions aléatoires dans les paramètres ne donne pas le résultat attendu
* [Contenu] Les bruits fractaux ne sont pas rendus correctement lorsque l’Extension non carrée est désactivée
* [Contenu] Les Cellules 2 et 4 ne se comportent pas correctement lorsque l’Extension non carrée est désactivée
* [Graphe] La mise à jour d’une instance sbsar crée un graphe de fantôme
* [Graphe] L’affectation par clic droit ne doit pas afficher le sous-menu UV pour les maillages non UDIM
* [Graphe] Sbsar republié n&#39;est pas correctement mis à jour
* [Graphe] Les nœuds ne sont pas invalidés correctement lors de la modification des ressources
* [Cooker] Le paramètre de la simulation de transparence prémulte n&#39;est pas correctement récupéré de sbsar
* Le filtre Niveaux [Cuiseur] ne saisit pas les valeurs lorsqu’il est cuit dans une barre oblique
* [Cooker] Les transformes implicites sont effectuées avant les nœuds FX-Map
* [Explorateur] Appuyer sur la touche Suppr d&#39;un pack demande à l&#39;utilisateur s&#39;il veut le supprimer
* Problème de Redéfinit l&#39;emplacement [Explorateur][Baker]
* [Courbe] crash aléatoire lors de la manipulation des touches dans l’éditeur de courbes
* [MDL] Type de gamma mal défini pour une utilisation personnalisée
* crash [Parameters] exposant un paramètre avec le même identifiant qu&#39;une entrée existante
* [Propriétés] L’utilisation de la sortie est modifiée avec une casse non sensible

### 8.1.0 (2018.1.0)

*(Publié Le 9 Mars 2018)*

**Ajouté :**

* [Bakers] Optimisation du baking en polypropylène
* [Bakers] Amélioration du résultat sur les seams pour le baker de Courbure
* [Baker] mappages Baker pour le maillage basé sur un UDIM
* [Bakers] Ajoutez une Vue 2D dédiée dans la fenêtre du Baker
* [Graphe] Prise en charge pour les UDIM
* [Graphe] Optimisation des performances du cuiseur
* [Graphe] Amélioration de la vitesse de génération des vignettes de nœud
* [Graphe] Conserver le cache de nœud uniquement pour les graphes ouverts
* [Graphe] Ajoutez une barre d’outils dans le graphe de composition pour contrôler le mode de génération des vignettes
* [vue 3D] Ajout d’un cache de géométrie pour optimiser l’affichage des maillages haute définition
* [vue 3D] Prise en charge de l’affichage de l’UDIM (affichage de la vignette active)
* [vue 3D] Mise à jour du cube arrondi avec une topologie uniforme
* [vue 3D] Éviter d’enregistrer la scène en permanence
* [Contenu] Ajout de nœuds de Bruits 3D (Perlin, Perlin Fractal, Worley, Simplex)
* [Contenu] Ajouter un nœud de masque de volume 3D
* [Content] Ajouter un nœud de 3D linear gradient
* [Contenu] Ajouter un nœud de tampons de cube 3D (utile pour prévisualiser les nœuds 3D)
* [Contenu] Ajouter un nœud de Projection Planaire 3D
* [Contenu] Ajouter un filtre Flou radial
* [Paramètres] Afficher les propriétés d’entrée/sortie de l’image dans les propriétés du graphe
* [Paramètres] Autoriser l’édition du chemin d’accès aux ressources
* [Moteur] Prise en charge de textures jusqu’à 8 Ko avec le moteur CPU (SSE2)
* [Moteur] Autoriser le convertisseur Niveaux de gris à utiliser des pondérations HDR pour le moteur HDR
* [Préférences] Ajout d’une option pour désactiver la création automatique de nœuds de conversion
* [Préférences] Définissez la compression par défaut pour le format png sur « vitesse maximale ».
* [UI] prend en charge le lien html dans les propriétés du Graphe
* [UI] Centrez les boutons « Oui / Non / Annuler » dans la boîte de dialogue de confirmation d’enregistrement
* [Explorateur] Amélioration de l’affichage de la hiérarchie des Maillages
* [Iray] Intégration d’Iray SDK 2017.1.4

**Fixe :**

* [Bakers] L’ajout d’une macro dans le champ de nom de sortie ne l’ajoute pas à la position du curseur
* [Bakers] Aucun matériau ne s’affiche dans la liste si l’objet n’a pas de matériau
* [Bakers] Appuyez sur Entrée pour confirmer les paramètres de baker pour ouvrir un menu déroulant
* [Baker] Les textures de Baking ne doivent pas générer de commandes dans la pile annuler
* [Bakers] Crash bakant une Texture transférée à partir du maillage sans spécifier de texture
* [Explorateur] « Enregistrer sous » doit utiliser le nom du fichier au lieu du nom de la première ressource.
* [Explorateur] Comportement incorrect lors du glisser-déposer d’une ressource d’un package vers un autre
* [Explorateur] Le clic droit de la souris ne doit pas ouvrir les données dans les propriétés
* [Explorateur] L’icône des éléments de Scène n’a pas le bon arrière-plan
* [Graphe] Ctrl + D ne fonctionne pas sous Linux
* [Graphe] La fonction de réédition de liens multiples ne branche parfois qu’un seul lien
* [Graphe] Les touches Ctrl + Maj + D doivent supprimer uniquement les liens externes, pas les liens internes.
* [Graphe] Le lien entre les niveaux de gris et la couleur est incorrect
* [vue 3D] Impossible de définir une ressource en tant que mappage env
* [vue 3D] Le shader Informations sur le Maillage n’affiche pas les résultats dans le bon espace colorimétrique.
* [Paramètres] Les paramètres non exposés sont toujours exposés à l’aide de CTRL+P
* [Paramètres] Les champs de texte ne sont pas mis à jour correctement lors de l’annulation/la restauration
* [Contenu] Artefacts dans Usure/salissures Map 003
* [Contenu] L’entrée principale en niveaux de gris de la morphologie vectorielle semble incorrecte
* [Cooker] sbscookie génère une erreur lorsqu’une ressource est manquante
* [Cuisson] Crash avec débordement de pile lorsque la chaîne de nœuds est trop longue
* [UI] Le bouton « Quitter » dans la gestion des licences ne fonctionne pas

## Version 7

### 7.2.5 (2017.2.5)

*(Publié Le 19 Février 2018)*

**Ajouté :**

* [Contenu] Fautes de frappe dans function.sbs
* [Contenu] Réduction de la plage par défaut du bruit perlin et du bruit gaussien
* [vue 3D] Ajuster la plage par défaut pour le paramètre « Échelle d’Height »
* [AXF] Mise à jour des modèles mdl

**Fixe :**

* [vue 3D][Bakers] Les normales ne sont pas recalculées si le modèle n&#39;a pas de normales
* [Graphe] La ressource bitmap non carrée est vide une fois instanciée
* [Contenu] Le bruit Perlin donne des résultats différents entre le moteur CPU et le modèle GPU

### 7.2.4 (2017.2.4)

*(Publié Le 8 Février 2018)*

**Ajouté :**

* [Importation AXF] Permet de spécifier le mode de filtrage sur les bitmaps d’entrée
* [vue 2D] Ne modifiez pas le rapport de l’image dans la Vue 2D lorsque la taille physique est activée

**Fixe :**

* [Bibliothèque] crash lors de l’activation/la désactivation du chemin dans les préférences
* [Baker] Correspondance par nom ignore certains maillages portant des noms spécifiques
* [Contenu] Le filtre Ajuster à droite supprime le canal Alpha

### 7.2.3 (2017.2.3)

*(Publié Le 19 Janvier 2018)*

**Fixe :**

* Frappe [Contenu] dans le nœud « PBR Basecolor Validate »
* [Contenu] Le paramètre Disorder ne fonctionne pas dans les Cellules 2
* [Content] Les Cellules 3 sont inversées lors de l&#39;utilisation de valeurs spécifiques dans les paramètres
* [Contenu] Polygone 2 : artefacts visuels avec paramètres spécifiques
* [Contenu] Par défaut, les niveaux de gris du Tile Generator sont de 8 bits
* [Contenu] Échantillonneur de mosaïque : le paramètre aléatoire spécifique au motif ne fonctionne pas
* [Contenu] Mappeur de forme : les fonctions aléatoires ne peuvent pas être utilisées pour piloter la quantité, le rayon, la largeur du motif, etc.
* [Contenu] Polygone 2 : les fonctions aléatoires ne peuvent pas être utilisées pour piloter la quantité de côtés
* [Contenu] Certains bruits/générateurs de motifs génèrent des avertissements dans la console
* [Contenu] Les niveaux de gris sans Transforme carrée génèrent une taille de pixel incorrecte
* [Contenu] Le filtre Tourbillon ne prend pas en compte le mode répétition
* [Graphe] Le glisser-déposer de la ressource bitmap vers le Noeud d&#39;entrée de l’image ne fonctionne plus
* [Graphe] CTRL+R (rechargement) ne fonctionne plus
* [Graphe] Problème lors de l’utilisation du cadre dans un autre cadre
* [Graphe] Crash lors du déplacement de cadres contenant des Épingles
* [Graphe] L’instance « Forme (héritée) » est transformée en « Forme » lors de l’enregistrement
* [Baker] crash lors de l’utilisation d’images sans puissance de 2
* [Bakers] Couleur du maillage : Polygroupe, ID de sous-filet renvoient toujours une image noire
* [Bakers] AO à partir du Maillage : la Distance d&#39;occlusion est fixée à 1 quelle que soit la valeur d’entrée
* [Iray] Basculement du Crash vers l’Iray
* [Iray] La valeur de Répétition doit affecter l’intensité de heighScale
* [Iray] Échec du chargement de l&#39;Iray sur l&#39;ordinateur Windows où VCCOMP110.dll n&#39;était pas présent
* [vue 3D][Bakers] Les UV ne peuvent pas être décodés à partir de l’obj exporté depuis Modo
* [vue 3D] Les intensités de Displacement ne sont pas cohérentes entre Opengl et Iray
* [vue 3D] L’intensité Occlusion Displacement/Parallaxe est deux fois supérieure à ce qu’elle devrait être
* Décalage [vue 2D] lors de l’affichage de l’image alpha
* [Cooker] Le paramètre Constant ($répétition) est introuvable lorsqu&#39;il est utilisé dans une instance de graphe
* [Cooker] Mauvaise évaluation de la variable dans les instances chaînées
* [Paramètres] Le chemin de la ressource Bitmap PKG ne doit pas être modifiable
* [Paramètres] Les paramètres d&#39;un même groupe sont invisibles si la visibilité d&#39;un seul paramètre est définie sur false
* [PSD] Impossible d’importer/de lier un fichier de PSD à partir d’un dossier nommé avec des caractères spéciaux
* [Fonctions] Les paramètres des fonctions ne doivent pas avoir d&#39;option de visibilité
* [LicenseService] Exception levée lors de l&#39;obtention d&#39;informations sur les nœuds
* [UI] La sélection de texte dans le champ de description le met en surbrillance

### 7.2.2 (2017.2.2)

*(Publié Le 23 Novembre 2017)*

**Fixe :**

* [Contenu] Fautes de frappe dans « Directionnel... » nœuds
* [Contenu] Diverses fautes de frappe
* [Contenu] La vignette Sampler est définie sur « 32 bits absolus ».
* [Contenu] Mappeur de forme : artefacts visibles sur la bordure de la forme dans certains cas
* Les paramètres répétition et « Expansion non carrée » de [Content] dans Polygone 1 sont rompus
* [Contenu] Les options « Générateur aléatoire » et « Expansion non carrée » ne fonctionnent pas sur le Bruit anisotrope
* [Contenu] Instance « Shape » rompue dans certains mappages Usure/salissures
* [vue 3D] La mise à l’échelle UV n’est pas appliquée si l’échelle height est définie sur 0
* [vue 3D] La réflexion avec shader blinn ne fonctionne plus
* [vue 2D] La mise en page de la fenêtre d&#39;informations est rompue
* [Graphe] problème lors du contrôle de la taille de la sortie avec la fonction sur une instance de bitmap lié dans un graphe
* [Fonction] Graphe non invalidé lorsqu’un lien est supprimé
* [Bibliothèque] Les favoris ne fonctionnent pas
* [Exportation de PSD] Le contenu du fichier PSD change chaque fois qu’une exportation est effectuée
* [Dégradé] Crash lors de la manipulation des touches dans l’éditeur de dégradé
* [Modèles] Le mappage de position pour les modèles de Substance Painter est incorrect
* [AxF] height physique incorrect
* [MDL] La mise à l&#39;échelle UVW de la taille physique est inversée dans les nœuds SBS MDL
* [Baker] $custom ne fonctionne plus
* [Préférences] crash au démarrage sur Mac

### 7.2.1 (2017.2.1)

*(Publié Le 20 Octobre 2017)*

**Fixe :**

* [Moteur] Crash lors du rendu de texte avec le moteur GPU
* [Contenu] Sampler de mosaïque : l’ID de ligne/colonne ne fonctionne pas correctement avec un format non carré
* [Contenu] Couleur Sampler de la vignette : le paramétrage des couleurs est incorrect
* [Contenu] Sampler de mosaïque : valeur par défaut incorrecte pour la quantité de motif X / Y
* [Export] Les métadonnées sont manquantes dans le PSD exporté

### 7.2.0 (2017.2.0)

*(Publié Le 19 Octobre 2017)*

**Ajouté :**

* [Contenu] Ajout d’un remplissage et de filtres associés (conversion d’un noir et d’un masque blanc en dégradés, couleurs aléatoires, etc.)
* [Contenu] Ajout de nouveaux Bruits, de cartes d’Usure/salissures et de générateurs de motifs prenant en charge le format non carré (l’ancienne version est marquée comme « héritée »)
* [Contenu] Ajout d’une nouvelle circulaire à éclaboussures avec beaucoup plus de fonctionnalités
* [Content] Ajouter un générateur de Scratches
* [Contenu] Ajouter un filtre Tourbillon
* [Contenu] Ajouter une sélection d’histogramme
* [Contenu] Ajouter un motif d’étoile
* [Contenu] Ajouter un filtre Mappeur de forme
* [Contenu] Ajouter un filtre d’interpolation vectorielle
* [Contenu] Ajouter un dégradé linéaire 3
* [Contenu] Mosaïque aléatoire/Tile Generator : ajouter le mode symétrie (h+v, h, v)
* Tile Generator [Contenu] : ajout d’une entrée d’image multiple
* [Contenu] Renommez « Fusion RGB-A » en « Fusion Alpha »
* [vue 2D] affichage de la sortie du nœud de commutateur à l&#39;aide de la touche C
* [vue 2D] Optimisation de la mise en page des histogrammes/informations en fonction de leur rapport d’affichage
* [vue 2D] Ajout d’un bouton pour activer/désactiver l’affichage des répétitions
* [3DView] Optimisation de la vitesse de calcul des harmoniques sphériques
* [vue 3D] Mise à jour des nuanciers PBR pour utiliser l’échantillonnage Fibonacci au lieu de Hammersley
* [vue 3D] Ajout d’une option pour enregistrer l’état de scène actif par défaut
* [vue 3D][Baker] Sérialiser les données dans un format lisible par l&#39;homme
* [Baker] Ajout de paramètres prédéfinis export/import (json)
* [Publish] Création de l’archive sbsar comme non solide
* [Publish] Stockez l’image/la vignette du graphe dans le fichier sbsar
* [Publish] Afficher une barre de progression lors de la publication d’un package
* [Dépendances] Affichez le fichier .sbs demandant une dépendance dans la « fenêtre Dépendances manquantes »
* [Dépendances] Fenêtre de rapport : affiche une icône verte lorsque le problème a été résolu
* [Dépendances] Ajoutez une option pour ouvrir les dépendances personnalisées du package dans l’explorateur de package
* [Préférences] Ajoutez une option pour définir l’état de scène par défaut dans les paramètres du projet
* [Préférences] Ajouter une option pour activer/désactiver le chemin d’accès à la bibliothèque
* [Graphe] Ajoutez une option pour faire une capture d’écran (à l’échelle 1:1) du graphe
* [Graphe] Supprimer l’info-bulle de l’arrière-plan des graphes de composition
* [Scripts] Rappels Add onBeforeFileLoaded et onAfterFileLoaded
* [Moteur] Ajout d’un paramètre de base pour régler le mode Rapport pixel
* [Console] Amélioration des performances de la console
* [Paramètres] Nouveau widget Position (XY)
* [Iray] Mise à niveau vers Iray SDK 2017.1
* [PSD] Enregistrer l’état du widget de PSD en tant que texte au lieu d’un état binaire
* [Library] Utiliser les pouces de sbsar s&#39;il existe
* [Explorateur] Renommez « Dependencies ». entrée « Gestionnaire de dépendances »
* Importation de fichiers AxF

**Fixe :**

* [MDL] Échec de l’exportation du Module MDL si la texture est connectée à un paramètre exposé
* [MDL] Essayer d&#39;enregistrer une dépendance pour les variables de chaîne MDL (nœud constant)
* crash [MDL] après la fermeture du package
* [MDL] crash lors de la connexion d’un élément flottant 3 à un nœud de couleur
* [MDL] ne peut pas ouvrir la bibliothèque de nœuds lors de la libération d&#39;un nœud de lien dans un cadre
* [MDL] crash lors de l’utilisation d’une texture de fichiers
* [MDL] Le comportement de dépendance enregistre trop d&#39;opérandes
* [Graphe] Les noms de Connecteur sont désactivés après la modification de FX-Map
* [Graphe] crash lors de l’annulation
* [Graphe] Comportement étrange avec des liens entre les nœuds
* [Graphe] Réduction de la dispersion et du détachement des nœuds lors de l’annulation
* [Graphe] Les instances de fonction ne sont pas mises à jour lorsque la référence est modifiée
* [Gestion de versions] Le package est rechargé lorsqu’une action personnalisée de Gestion de versions est déclenchée
* [Gestion de versions] Les espaces de travail de gestion de versions désactivés sont toujours disponibles dans le menu contextuel d’un pack
* [Gestion de versions] Supprimer l’action personnalisée ne la supprimez pas du menu contextuel d’un pack
* [Propriétés] L’aperçu du paramètre n’est pas mis à jour lors de l’utilisation de l’objet
* [Iray] Problème d’affichage de l’heure max.
* [Iray] Problème d’option de pause
* [Bakers] crash lors de la conversion du baking en UV à l’aide de la traduction coréenne/japonaise
* [Bakers] la modification du tracé après un premier baking ne fonctionne pas
* [Exporteur PSD] problème d’annulation
* [PSD] et les calques sont verrouillés dans Photoshop CS5
* [UI] Le curseur de couleur est toujours défini sur blanc lors de la création du nœud de couleur uniforme
* [UI] L’ouverture d’un onglet existant doit l’afficher au lieu de le dupliquer.
* [Préconfigurations] crash lors de la modification du type de paramètre utilisé dans une préconfiguration
* Les échantillonneurs [vue 3D] ayant la même utilisation sont fusionnés
* [vue 2D] Les informations sur les pixels ne fonctionnent pas pour les images dont la résolution n’est pas une puissance de 2
* Problème [Library] lors du changement de nom des filtres
* [Données] Correction de diverses fautes de frappe dans les fichiers SBS
* [Paramètres] nœud de niveau - problème de précision de niveau automatique
* [Préférences] Les boutons Répertoires de modèles doivent être désactivés pour « Projet par défaut ».

### 7.1.4 (2017.1.4)

*(Publié Le 2 Octobre 2017)*

**Ajouté :**

* [Bakers] Ajoutez la Courbure en partant du maillage arrière
* [Vérificateur de nouvelle version] Ajoutez une option de ligne de commande pour désactiver la vérification de la nouvelle version (—news hide\_changelog:true)
* [Scripts] Désactiver le délai d&#39;attente de Qprocess

**Fixe :**

* [Baker] impossible de modifier la couleur du matériau dans UV SVG
* [UI] ne peut pas fermer la vue du graphe à l’aide du clic sur la roue
* [Contenu] Certains bruits sont en 8 bits au lieu de 16 bits
* [Contenu] Courbure Lisse donne un résultat erroné lorsque la répétition est désactivée
* [Texte] crash lors du redimensionnement de polices spécifiques

### 7.1.3 (2017.1.3)

*(Publié Le 31 Août 2017)*

**Fixe :**

* [vue 3D] crash lors de la tentative d’affichage des options d’affichage 3D dans Mac 10.10.5
* [vue 3D] Les informations de texte ne s’affichent pas dans la vue 3D lors de l’utilisation de l’écran à haute résolution
* [vue 3D] La préférence globale pour OpenGL/DirectX n’est pas prise en compte lorsque le matériau est réinitialisé
* [Contenu] Height à la normale : la normale est inversée lors de l’utilisation de l’échantillonnage de Sobel
* L’Ambient occlusion [Contenu] (hbao\_2) ne se comporte pas correctement lorsqu’il est défini sur un paramètre non carré
* [Contenu] Les entrées Générateur de masque ne sont pas dans le même ordre que « Maillage Data Combiner »
* [vue 2D] Histogramme : les informations de sélection ne sont pas mises à jour lors du changement d’image
* [vue 2D] Histogramme : les informations de plage utilisées ne sont pas affichées pour les images en niveaux de gris
* [Paramètres prédéfinis] crash lors du changement de nom d’un paramètre prédéfini d’un graphe utilisé dans un autre graphe
* [Graphe] X et Y sont inversés dans la barre d’outils Taille du gabarit

### 7.1.2 (2017.1.2)

*(Publié Le 3 Août 2017)*

**Fixe :**

* [Contenu] Problème de Filtrage dans les filtres « Mosaïque automatique dynamique » et « Recadrage des niveaux de gris »
* [Contenu] Les filtres de bibliothèque ne tiennent pas compte de la préférence OpenGL/DirectX
* [Contenu] Impossible de cuisiner un SBSAR sans\_carré\_transforme
* [Contenu] Forme du panorama : la zone réactive est mise en miroir dans le canal du RGB
* [Contenu] Sampler de mosaïque : le paramétrage de la couleur de position n’est pas normalisé
* [Contenu] Mosaïque Sampler : les motifs sont invisibles si la répétition est désactivée
* [Graphe] Le commutateur $normal\_map\_format ne fonctionne pas lorsque nous utilisons le menu de la barre de bibliothèque/espace
* [Graphe] Format incorrect dans le nœud bitmap lors du glisser-déposer d’une ressource RGBxxF
* [Bakers] La couleur du maillage avec la couleur du matériau est cassée
* [vue 3D] chaque modification dans la vue 3D génère des actions dans la pile Annuler
* crash [Dépendances] lorsqu&#39;un graphe a des ressources manquantes dans la bibliothèque personnalisée
* [Iray] Le crash au démarrage sur la version OSX est antérieur à la version 10.11

### 7.1.1 (2017.1.1)

*(Publié Le 18 Juillet 2017)*

**Ajouté :**

* [Baker] Ajouter une action « Réinitialiser » sur les champs de ressources
* [Bakers] Utiliser la couleur noire lorsqu’aucune couleur de vertex n’est trouvée
* [Paramètres prédéfinis] Masquer le widget de paramètre prédéfini sur les instances lorsqu’aucun paramètre prédéfini n’est disponible
* [Préférences] Supprimez l’option « Calculer le binormal par fragment » dans les paramètres du projet (désormais, cette option est gérée dans le plug-in du cadre de tangentes).
* réglages de sbsupater.exe

**Fixe :**

* [Bakers] Le système « error » ne fonctionne plus
* [Baker] options sérialisation : les anciennes clés restent
* crash [Baker] lors de la modification du nom d’un baker
* [Bakers] Problèmes d’interface utilisateur
* [Contenu] Filtre Correspondance des couleurs - Différence entre le processeur/GPU
* [Contenu] Certains GrungeMaps produisent des images 8 bits au lieu de 16 bits
* [Graphe] Crash lors de l&#39;utilisation du X « switch links » sur le nœud fx-map
* [vue 3D] crash aléatoire lors de l’ouverture de vue 3D
* [vue 3D] Le Binormal est toujours calculé par fragment, quel que soit le plugin de repère tangent
* [Updater] Erreur XML lors de l’utilisation d’une police spécifique
* [Cooker] Le modulo sur un nombre négatif ne renvoie pas le même résultat que le moteur
* Problème d’interface [UI] lors de l’utilisation du dégradé de sélection sur un écran à haute résolution
* [MDL] Le nœud de couleur ne conserve pas cette valeur
* [Packaging] Mikkt Unreal plugin de repère tangent est manquant

### 7.1.0 (2017.1.0)

*(Publié Le 29 Juin 2017)*

**Ajouté :**

* [Baker] Nouvelle interface utilisateur
* [Bakers] Conservez un cache de maillage haute définition jusqu’à la fermeture de la fenêtre de baker
* [Bakers] Ajout d’une option pour corriger l’inclinaison à l’aide d’un masque en niveaux de gris
* [Bakers] Prise en charge de l&#39;utilisation-poly-haut-comme-poly-bas-poly dans les bakers hors maillage
* [Bakers] Rendre la fenêtre Bakers non modale
* [Baker] État de stockage dans un fichier .sbs dans un format lisible par l&#39;homme
* [Paramètres] Copier/coller des paramètres d’un graphe à un autre
* [Paramètres] Ajoutez une option pour copier un seul Paramètre d&#39;entrée (et le coller par la suite)
* [Paramètres] Supprimer le bouton de fonction sur le paramètre « Mode colorimétrique »
* [Paramètres] Modifier/Enregistrer/Afficher les paramètres prédéfinis intégrés
* [Paramètres] Permet à l’utilisateur de copier les attributs de paramètres lorsqu’un package est verrouillé
* [vue 3D] Ne stocke plus les paramètres de la vue 3D de la dernière session dans le Registre
* [vue 3D] Création d’une ressource 3D à partir de la scène active
* [vue 3D] Ne stocke plus l’état de la vue 3D d’une session à une autre dans le Registre
* [vue 3D] Fusionner les menus Scène et Géométrie
* [vue 3D] Conversion sRVB séparée du shader du fragment (vous devrez mettre à jour vos shaders personnalisés !)
* [vue 3D] Ajout d’une option permettant de créer une ressource 3D à partir de l’état actuel
* [vue 3D] Amélioration du message d’erreur généré lorsque #include échouez dans un code de shader
* [vue 3D][Explorateur] Créer une Scène 3D à partir de primitives
* [vue 3D] Afficher le numéro de ligne correct lorsque la compilation du shader GLSL échoue et que le code contient des directives #include
* [Graphe] Possibilité de redimensionner un cadre à partir de tous les coins/bordures
* [Graphe] Stockez les informations relatives à la taille du gabarit dans la ressource graphe plutôt que dans le registre local.
* [Graphe] Optimiser la vitesse de génération des vignettes de nœud
* [Graphe] Exposez le budget du cache de mémoire dans les Préférences
* [Graphe] Ajouter une option « Réinitialiser et afficher dans vue 3D » sur les nœuds
* [Contenu] Convertisseur PBR : ajout de nouveaux paramètres prédéfinis Arnold 4/5, Corona 1.6 et Renderman
* [Content] Optimisation du nœud AutoLevel et prise en charge de l&#39;entrée HDR
* [Contenu] Optimisation du filtre HBAO lorsque l’optimisation GPU est désactivée, ajout de 16 exemples de version
* [Cooker] fonctionnalité non prise en charge par le SVG de sortie dans le journal
* [Cooker] Ne supprimez pas toutes les ressources du SVG si une seule fonction n&#39;est pas prise en charge
* [UI] Augmenter la taille du bloc Description
* [UI] Ajout d’informations sur le chemin d’accès au fichier dans les instances de graphe
* [Fonctions] Ajouter « Ouvrir la référence » sur les instances de fonction
* [Fonctions] Afficher la liste des graphes de fonction lors du glisser-déposer du fichier .sbs dans un graphe de fonction
* [Explorateur] Création d’une nouvelle ressource 3D à partir d’un fichier primitif
* [Moteur] Ajouter une variable $répétition
* [Courbe] Ajoutez des options pour retourner la courbe horizontalement/verticalement
* [Gestion des couleurs] Lire le profil ICC sur les bitmaps
* [Exporter] Ajoutez « Libellé », « Groupe » et « Données utilisateur » dans la liste des macros de modèle
* [Préférences] ajouter la possibilité de modifier le chemin d’accès pour les fichiers temporaires
* [Doc] Ajout d’un format de Graphe MDL à la documentation sur le format SBS

**Fixe :**

* [Graphe] Problème de cache : l’affichage des sorties dans vue 3D ne fonctionne plus
* [Graphe] Problème d’effacement du cache
* [Graphe] Les demandes de génération de miniatures de nœud ne sont pas annulées lorsque le graphe est invalidé
* [Graphe] Problèmes de résolution après l’utilisation de F5
* [Graphe] vue du graphe manquante au lancement
* [Graphe] La modification d’un paramètre génère plusieurs appels de rendu
* [Graphe] crash lors de l’utilisation d’un modèle personnalisé qui contient des maps bakées
* [Graphe] Crash lorsque les nœuds sont liés dans une fonction de graphe
* [vue 3D] Chargement parallèle désordonné avec ProgressManager
* [vue 3D] Rendu avec iray à une image de résolution personnalisée non cadre complet
* La définition de Matériau [vue 3D][Iray] n&#39;est pas conservée
* [vue 2D] L’histogramme est vide sur les images LDR
* [vue 2D] Problème d’affichage lorsque le mode répétition est activé
* Paramètres [MDL] non exposés
* [MDL] crash lors du déplacement d’un fichier MDL d’un package vers un autre pendant le rendu
* [MDL] Ne vous demandez pas où attribuer la liste MDL lorsque vous double-cliquez sur graphe
* [Bakers] Crash lors du baking de fichiers .obj spécifiques
* [Bakers] Texture transférée à partir du maillage / normal donne un résultat erroné
* [Transformation 2D] Impossible d’utiliser les touches fléchées pour modifier le décalage dans le nœud de transforme 2D
* Problème d’artefact [Transformation 2D] avec une faible résolution
* [Utilitaire de mise à jour] Le rapport de mise à jour ne s’affiche pas avec lorsque Ctrl+o/open
* [Propriétés][Format] Certains caractères sont mis en échappement deux fois dans UserTags
* [Nœud bitmap] Ctrl Z ne fonctionne pas sur vue 2D
* [Préférence] Espace vide inutile dans l’onglet Alias
* [Programme d’installation] L’installation d’une version précédente ne fonctionne pas la première fois
* Liste déroulante [Paramètres] : placer certains espaces sur le libellé de la dernière valeur fige SD indéfiniment
* [UI][MAC] « À propos de la Substance » affiche Iray info
* [SVG] crash lors de l’importation d’un SVG spécifique
* Filtre HBAO [Content] : le paramètre Radius se comporte différemment en fonction de la résolution (un nouveau hbao\_2.sbs a été ajouté, l’ancien hbao.sbs est désormais obsolète)

## Version 6

### 6.0.4

*(Publié Le 21 Juin 2017)*

**Fixe :**

* [Graphe] crash avec X raccourci
* [Graphe] crashs après la suppression d&#39;un lien entre les nœuds
* [Graphe] La suppression d’un point de scission rend SD crash
* [Contenu] Faute de frappe dans mg\_surface\_brush
* [Contenu] Qualité inférieure sur HBAO par rapport à 6.0.2
* [Bibliothèque] Les icônes des filtres personnalisés ne sont pas enregistrées
* [Explorateur] Crash lors de l’ouverture d’une ressource 3d référençant un fichier manquant
* [Bakers] La Texture de transfert du Maillage est mise en miroir si l’option « Normal » est activée.

### 6.0.3

*(Publié Le 1Er Juin 2017)*

**Ajouté :**

* [Export] Enregistrer la taille physique en ppp dans les textures exportées
* [vue 2D] Afficher le libellé du paramètre de matrice dans le menu Transformation

**Fixe :**

* [Contenu] Sampler de mosaïque : le paramétrage de la couleur de position n’est pas normalisé
* [Contenu] Recadrage : graphe Fantôme dans processeur de pixels
* [Contenu] Forme du panorama : la zone réactive est mise en miroir dans le canal du RGB
* [Contenu] Le filtre HBAO peut générer une résolution négative
* [Contenu] Le rendu du filtre Correspondance de couleur est incorrect dans certaines situations
* [Contenu] L’option « Pré-multiplié vers Direct » supprime le canal Alpha
* [Contenu] Fautes de frappe dans diverses étiquettes
* [Graphe] Les informations de Nombre de bits par pixel sont coupées lorsque l’échelle PPP est définie sur 125 1520 ou 175 %
* [Graphe] Lorsqu’une sélection contenant un cadre est collée, le cadre n’est pas sélectionné
* [Graphe] Lorsqu’une sélection contient un commentaire, les éléments collés sont déplacés dans le graphe
* Problème de points de fractionnement [Graphe]
* [Graphe] Certains Connecteurs d’Épingle ne contraignent pas lorsqu’ils sont survolés
* [Graphe] vue du graphe manquante au lancement
* [Export] bitmaps manquants après l’exportation
* [Export] N&#39;exporte pas les dépendances sur la version de la vapeur
* [Bakers] crash au maillage trop chargé en Ensembles d&#39;UV
* [Bakers] crash de baker UV map lors du baking de maillages sans Ensembles d&#39;UV
* [Moteur] Bogue de Sampler avec Fxmap+HDR
* [Moteur] crash avec images jpeg haute résolution
* [vue 2D] Widget de Transformé manquant dans vue 2D lorsque le mode Aperçu de la répétition est activé
* [vue 3D] L&#39;Instance de graphe avec utilisation personnalisée n&#39;est pas correctement envoyée à vue 3D
* [Préférences] Chemin incorrect pour mikktspace.dll
* [Explorateur] le déplacement d’une ressource bitmap dans un package fait apparaître le menu « link/embed »
* [Paramètres] crash lors de l&#39;utilisation de &#39;répétition&#39; comme nom de paramètre
* [MDL] aucun lien coloré entre les nœuds
* [Linker] Processeur de pixels : génération de nuanceurs GLSL incorrecte
* Problème de Nombre de bits par pixel avec [Cooker]

### 6.0.2

*(Publié Le 17 Mars 2017)*

**Ajouté :**

* [Moteur] Intégration du dernier moteur avec l’optimisation de la décompression JPEG

**Fixe :**

* [Contenu] Le correctif de Clone ne fonctionne plus
* [Contenu] La sortie Height ne fait pas partie du groupe de matériaux dans les modèles
* [MDL] Crash lors de la suppression d’une instance de graphe
* [MDL] Aucun avertissement entre les nœuds en conflit
* [MDL] Messages d’avertissement inutiles lors de l’exportation
* [Courbe] L&#39;exposition des paramètres ne doit pas être exposée
* [Moteur] Crash d’importation d’un fichier sbsar contenant un bitmap HDR
* [Text Node] La spécification de police génère un fichier XML non valide
* [Éditeur de dégradé] Les valeurs ne sont pas bridées correctement
* crash [vue 3D] lors de l’utilisation d’un HDRi personnalisé (haute résolution) comme environnement

### 6.0.1

*(Publié Le 3 Mars 2017)*

**Ajouté :**

* [Bakers] Améliorer la gestion des tâches de progression
* [Bakers] Modifier l’info-bulle d’erreur lorsqu’aucun maillage n’est sélectionné
* [Propriétés] Les paramètres de l’effet de post-traitement 3DView doivent être désactivés lorsque l’option Post-traitement est désactivée dans les préférences.
* [Licence] Autoriser la spécification d’un chemin personnalisé pour la licence Substance Designer 6
* [Dégradé] Désactivez le curseur « précision » si aucun prélèvement de dégradé n’a été effectué
* [Cooker] Ignorer la ressource manquante dans la saisie de l&#39;image pour empêcher l&#39;échec de la cuisson
* [vue 3D] Modification de la gestion des fuites de reflets de specular
* [Graphe] Ajoutez d&#39;autres paramètres pour la compatibilité avec moteur v6

**Fixe :**

* [Bakers] La Map normal du maillage (espace monde) est inversée sur l’axe Y
* [Bakers] Baker un maillage sans UV ne permet pas de signaler une erreur
* [Bakers] La normale moyenne ne fonctionne pas
* [Bakers] crashs SD lors du baking d&#39;AO avec un maillage spécifique
* [Baker] Le format de sortie n’est pas restauré correctement
* La police personnalisée de [Texte] ne fonctionne pas dans le lecteur
* [Texte] avertissement de police non valide lors de la réouverture d’un pack avec une police dans les ressources
* La saisie de texte [Texte] ne fonctionne pas en mode Aperçu
* Le paramètre de police [Text] peut être exposé
* [Texte] figé/crash lors de la création d&#39;une fonction dans le paramètre de texte
* [Texte] Crashs lors de l’expose de la taille de la police
* [vue 2D] Le pourcentage de zoom ne s’affiche pas correctement lors de l’utilisation de la touche F
* [vue 2D] L’image est décalée lorsque la taille est modifiée
* [vue 2D] Discontinuité lors de l’affichage de la répétition
* [vue 2D] Le widget de transformation n’est pas visible/modifiable en mode aperçu
* [vue 3D] Taille physique non prise en compte par PBR Parralax shader
* [vue 3D] Le paramètre de fréquence d’actualisation n’est pas correctement restauré d’une session à une autre
* [Graphe] multiangle\_to\_normal empêche la publication
* [Graphe] La taille de sortie du filtre pow est verrouillée
* [Graphe] Impossible d&#39;instancier aux fichiers .sbsar
* Interface utilisateur [Courbe] recadrée
* [Courbe] L’affichage des nombres est légèrement recadré
* [Courbe] Le widget disparaît lorsque la barre d’outils est redimensionnée
* [Contenu] Le nœud Rayonnement est rompu
* [Contenu] Mosaïque Sampler : les motifs sont invisibles si la répétition est désactivée
* [Contenu] MG Constructeur de masque - Paramètres de contraste de Courbure inversée
* [Content] Color Equalizer : paramètre de groupe personnalisé\_color\_variation non connecté
* [Contenu] Correctif de Clone : zone de correctif non visible lorsqu’elle est positionnée dans les coins
* [Explorateur] Le rechargement d’un package pendant l’ouverture de sa dépendance rompt le package de dépendance
* [Explorateur] Impossible d’importer une ressource psd 32 bits
* [Publish] échec de la cuisson (ERR:No héritage (absolu))
* [Dégradé] Le dégradé doit être affiché comme linéaire lorsque l’option sRVB est décochée
* [Transformation2D] Impression de décalage lors du déplacement d’un widget avec contrainte d’axe
* [Paramètres] La sélection de la souris est volée par la liste déroulante
* [Moteur] Aucune Répétition n’a d’effet sur le nœud de distance sur le moteur GPU
* [Export] Crash lors de l&#39;exportation de sorties en tant que TGA
* [MDL] le paramètre prédéfini d’exportation ne fonctionne pas

### 6.0.0

*(Publié Le 14 Février 2017)*

<b>Ajouté :</b>

* [Moteur] Nouveau nœud de courbe
* [Moteur] Nouveau nœud de texte
* [Moteur] Composition de nombre de bits par pixel 16f/32f
* [Moteur] instanciation pour GPU FX-maps
* [Moteur] Fonction Add log2
* [Bakers] baking de carte 8k
* [Bakers] Baking par Matériau / « Jeu de textures »
* [Bakers] Affiche le message de chargement lorsque la sortie bitmap est codée/écrite sur le disque
* [Baker] Ajout d’une option d’annulation pendant le baking
* [Nœud de dégradé] ajouter des réglages globaux pour plusieurs touches sélectionnées
* [Nœud de dégradé] Options du sélecteur de dégradé simplifié
* [Graphe] Ajout d’une option permettant de modifier la taille du gabarit par défaut
* [Graphe] Afficher la profondeur des pixels de l’image sous le nœud
* [Préférences] Préférences globales pour DirectX/OpenGL
* [Préférences] Utiliser les onglets dans Préférences/Interface utilisateur du projet
* [Préférences] supprimer le paramètre MaxTextureSize situé dans les préférences « 3DView »
* [Préférences] Afficher une courte aide sur l’enregistrement automatique
* [Préférences] Exposer les options de format d’image
* [Préférences] Ajout d’une option permettant de masquer la Map d&#39;environnement dans vue 3D par défaut
* [Préférences] Ajout d’une option pour l’option alpha par défaut du filtre map normal
* [vue 2D] Ajout de la possibilité de panoramiser à l’écart des limites de la texture
* [vue 2D] Interprétation du rapport taille physique X/Y
* [vue 3D] Amélioration de la gestion des Textures
* [vue 3D] Désactiver les Effets de post-traitement par défaut (pour empêcher le crash sur le gpu bas de gamme)
* [Graphe MDL] Gestion de l’indicateur masqué sur le paramètre Iray
* [Graphe MDL] Autoriser à définir le constructeur &#39;matériau()&#39; comme nœud racine
* [Graphe MDL] Créer un aperçu du nœud d&#39;Instance de graphe SBS
* [Contenu] Ajout de nouveaux filtres de Traitement des numérisations
* [Contenu] Ajout de nouveaux filtres de réglage (Verrouille, Pow, Visionneuse de plage HDR)
* [Contenu] Ajouter un Bruit bleu (approximation rapide)
* [Contenu] Ajout de nouveaux effets de forme (Lueur, Ombre portée, Contour)
* [Publish] Ajoutez une action « Exporter comme précédent » pour republier le dernier package sélectionné
* [Publish] Amélioration de la génération SBSAR lors de l’utilisation d’images bitmap haute résolution
* [Publish] Avertir l’utilisateur du paramètre de graphe non « relatif au parent x1 » lors de la publication ou du téléchargement sur Share
* [Properties] Ajouter l’attribut « Taille physique » sur les Graphes SBS
* [Paramètres] Supprimer les actions de fonction sur les chemins de ressources PKG
* [Paramètres] Supprimer la fenêtre contextuelle « Valeurs de prévisualisation modifiées »

<b>Fixe :</b>

* [Graphe] L’utilisation de la mémoire augmente régulièrement à chaque ouverture du menu contextuel
* [Graphe] [Dans SSE2] Les nœuds du polygone n’affichent pas les formes lorsque le paramètre « Scale » est en négatif
* [Graphe] Crash lors du passage de « Entier » à « Flottant » sur un paramètre exposé
* [Graphe] Le déplacement de nœuds alors qu’un point de fractionnement est sélectionné recalcule les nœuds.
* [Graphe] Les points de fractionnement ne prennent pas en charge « Annuler »
* [Graphe] info-bulle vide affichée lorsque la description du graphe contient des caractères non imprimables
* [Graphe MDL] Crash lorsque le nœud actif affiché dans la vue de la propriété est supprimé
* [Graphe MDL] Le Graphe MDL qui utilise la fonction constructeur matériau() comme racine n&#39;est pas rendu correctement dans vue 3D
* [MDL] Impossible d’exporter le Module MDL lors de l’utilisation d’un opérateur conditionnel avec un paramètre d’expose booléen uniforme
* [MDL] Crash lors du chargement d&#39;un modèle de Graphe MDL deux fois
* Les Matériaux [MDL Archive] qui utilisent une texture ne sont pas correctement gérés
* [vue 3D] L&#39;Iray n&#39;est pas modifié lorsque le nœud racine du MDLGraph change
* [vue 3D] crash aléatoire lors de la fermeture de la vue 3D pendant le chargement d&#39;un maillage
* [vue 3D] Yebis n’est pas réactivé après l’enregistrement du rendu
* [vue 3D] Fichier de PSD non valide généré lors de l’enregistrement du rendu de la scène iray
* [vue 3D] la lumière ponctuelle 1 ne s’allume pas
* [UI] La zone de détection des cases à cocher est trop large dans les paramètres « Bakers du Maillage »
* [UI] Problème esthétique dans les paramètres « Bakers à partir du Maillage »
* [Mac] L’ouverture du SD en double-cliquant sur un sbs n’envoie pas la sortie vers la vue 3D
* [Mac] [Iray] Le rendu de Cluster Photoreal ne fonctionne pas sur MacOS
* [Moteur] Atan2(0, 0) crée le crash moteur
* [Moteur] Problème de synchronisation critique
* [Baker] Impossible de désactiver la normalisation automatique pour le baker Height
* [Paramètres] lors de la conversion des niveaux de gris en rvba, la valeur alpha doit être 255
* [Fonctions] Il est possible de définir une fonction comme nœud de sortie même si elle n&#39;est pas compatible
* [Export] Dépendances non valides après l&#39;exportation d&#39;un package avec les ressources du PSD
* [Console] La désactivation de la console rend le crash SD

## Version 5

### 5.6.2

*(Publié Le 8 Février 2017)*

**Fixe :**

* [Préférences] Le shader par défaut n’est pas pris en compte
* [vue 3D] Crash si le shader par défaut est modifié lors de l’exécution
* [Moteur] obtenir un problème de taille de $size

### 5.6.1

*(Publié Le 17 Janvier 2017)*

**Ajouté :**

* [vue 3D] Définir la taille des primitives sur 100 cm
* [Contenu] Ajouter « Filtrage d’entrée d’image » à « Splatter Circular » et « Splatter »
* [Bakers] « Courbure à partir du Maillage » Ajouter des avertissements de console sous le canal « Vérification de l’intégrité du Maillage »

**Fixe :**

* [vue 3D] Disparaître en cas de désancrage
* [Graphe] Les paramètres de Map de dégradé « Bruit » et « Précision » ne fonctionnent plus
* [vue 3D] Alt+R ne fonctionne pas après l’enregistrement du rendu
* [Bakers] crash « Courbure du Maillage » avec certains maillages ZBrush

### 5.6.0

*(Publié Le 15 Décembre 2016)*

**Ajouté :**

* [Contenu] Ajout du nouveau filtre « AO (Ambient occlusion de base de l’horizon) »
* [Contenu] Ajout d’un nouveau filtre « Fusion Height »
* [Contenu] Ajout du nouveau filtre « Height à la normale (unités universelles) »
* [Contenu] Ajout d’un nouveau filtre « Fusion Height Matériau »
* [Contenu] Ajout d’un nouveau filtre « Couverture de Snow »
* [Contenu] Ajout d’un nouveau filtre « Niveau d’eau »
* [Contenu] Ajout d’un nouveau filtre Correspondance des couleurs
* [Contenu] Ajout du nouveau filtre « Histogramme numérisé (non uniforme) »
* [Préférences] [Interface utilisateur] Ajoutez une option dans Préférences pour désactiver la détection haute résolution
* [Vue 3D] Ajoutez une option « Réinitialiser la position de la caméra »
* [Iray] Prise en charge de l’architecture Iray SDK 2016.2 pour Pascal
* [Graphe] Ajouter l’option « Copier les informations de nœud dans le Presse-papiers » dans le menu contextuel

**Fixe :**

* [MDL] La racine du matériau alg n’est pas supprimée du paramètre prédéfini exporté
* [Graphe MDL] les liens des ressources manquantes ne sont pas supprimés dans le Graphe MDL
* [Bibliothèque] La création d’un filtre crée deux conditions de base
* [Bibliothèque] Les dossiers ne filtrent plus le contenu de la bibliothèque
* [Bakers] La barre de progression va et vient
* [Bakers] Une ressource de cage inexistante empêche le baking
* [Contenu] Diverses erreurs dans « Functions.sbs »
* [Export] Le format de fichier est toujours redéfini sur png
* [UI] Problème de mise à l&#39;échelle de l&#39;interface utilisateur de Substance Designer
* [Graphe] Crash lors du déplacement du package d’origine d’une instance de graphe
* [Préférences] si le plug-in shader/tangente/.. par défaut est introuvable, utilisez ceux définis dans le projet par défaut
* [Paramètres] Les curseurs ont trop de précision sur Mac
* [Explorateur] Le déplacement du Maillage 3D d’un dossier vers un autre corrompt cette ressource
* Fermer la fenêtre ne tue pas le processus SD
* La boîte de dialogue d’ouverture de fichier n’affiche pas les fichiers avec le filtre « Tous les formats »

### 5.5.3

*(Publié Le 28 Octobre 2016)*

**Fixe :**

* crash [Étagère] lors de la création du dossier
* [Bakers] La direction du monde\_espace\_ne fonctionne plus

### 5.5.2

*(Publié Le 18 Octobre 2016)*

**Ajouté :**

* [Graphe MDL] Propager les valeurs par défaut du Graphe SBS à l&#39;instance SBS Graphe Node dans le Graphe MDL
* [MDL] Prise en charge du glisser-déposer du graphe SBSAR
* [Iray] mise à niveau vers SDK 2016.1.6 (261500.16187)
* [sbsrender] Optimiser la gestion de la mémoire de sbsrender pour correspondre aux performances du lecteur
* [vue 3D] Permet au widget d’avoir une taille inférieure à celle de la barre de menus supérieure
* [Console] Autoriser à copier certaines lignes dans le Presse-papiers

**Fixe :**

* [Lecteur] Crash lors de la lecture d’un pack directement dans Designer à l’aide du « bouton Lecture »
* [Démarrage] fichier nvcuvid.dll manquant dans l’affichage contextuel
* [Environment init] un double-clic sur un fichier .sbs ne le charge pas dans SD
* [Export] Exporter avec le crash des dépendances
* [MDL] Problème de synchronisation entre un Graphe et son instance
* [MDL] Les instanciers sbsar sortent texture\_return au lieu des valeurs
* [Iray] Dans Iray Renderer, le « Canal d’Height » n’est pas mis à jour correctement lorsque vous changez de map height
* [vue 3D non ancrée] « Caméra>Enregistrer le rendu » ne fonctionne pas après avoir masqué l’application dans la barre des tâches de Windows
* [Mac Iray] GPU NVIDIA plus détecté par Iray
* [Bakers] Crash de Texture transférée à partir du maillage lors du baking des textures non POT
* [Crash] Crash lors de l’exportation d’un graphe sur Substance share
* crash [Graphe] lors de la sélection d&#39;une instance de fantôme
* [vue 3D] Impossible de réaliser un zoom avant ou arrière sur la caméra orthographique en mode Iray
* [UI] Le sélecteur de couleurs ne gère pas l’affichage à haute résolution
* [Graphe] (MacOS 10.11.06) calcul infini avec nœud de fusion à matériaux multiples
* [Graphe] Copier/Coller le contenu du Graphe ==> coller dans le contenu et également une référence à ce graphe
* [Graphe] Plusieurs fusions à matériaux multiples dans la scène, elle sélectionne automatiquement les mauvaises sorties
* [Graphe] L&#39;Edge Wear Metal bloque le PC
* [Bibliothèque] Les fichiers « SBSAR » affichent le logo « S » au lieu des vignettes
* [Bibliothèque] Les dossiers dans .sbsar sont affichés dans la bibliothèque

### 5.5.1

*(Publié Le 8 Septembre 2016)*

**Ajouté :**

* [Iray] Ajout du mode « IQ » pour le rendu cloud
* [Iray] Mise à jour vers Iray SDK 2016.1.5

**Fixe :**

* [MDL] La vue en vue 3D ne fonctionne pas correctement la première fois
* [MDL] Le dégradé\_interpolation\_linéaire n’est pas exporté avec le chemin complet.
* [MDL] Le coin inférieur droit du cadre nouvellement créé est exactement aligné avec le nœud associé
* [MDL] La vignette du matériau racine ne se met pas à jour dans certains cas
* [MDL] Crash lors de la suppression de tous les nœuds et de la restauration
* [MDL] Baisse des performances dans l’affichage du graphe par rapport au Graphe Substance
* [MDL] Impossible d’exporter le Module MDL en raison du paramètre IOR
* [MDL] Les paramètres affichés ne correspondent pas au nœud sélectionné
* [vue 3D] Le Matériau MDL provenant d&#39;un Graphe MDL n&#39;est pas réinitialisé lorsque le nœud racine est supprimé
* [vue 3D] Le cadrage de caméra par défaut est perdu après le chargement du maillage de fbx
* [vue 3D] L&#39;affectation des Textures n&#39;est pas conservée lors du passage à Iray
* [Iray] Message d’avertissement de l’Iray lors du déplacement de la caméra
* crash [Iray] lors du passage à Iray
* [Iray] Le mot de passe VCA n&#39;est pas enregistré
* [Graphe] Crash lors de la suppression de nœuds
* [Graphe] Appuyer sur CTRL pour copier le lien ne fonctionne pas avec Mode de matériau
* [Graphe] Crash lors de la suppression d&#39;un nœud de sortie dans un matériau d&#39;instancier
* [Bakers][vue 3D] Impossible de charger le maillage haute définition
* crash [Mac][vue 3D] lors de la tentative de restauration de windows détaché sur le moniteur secondaire
* [Paramètres] Impossible de modifier une valeur dans un spinboxedit sans supprimer le suffixe
* [UI] Utiliser « Annuler » lors de la fermeture de la boîte de message SD doit s&#39;arrêter
* Crash lors de l’ouverture de deux vues 3D
* Crash dans Alg::Scripting::Moteur lors de l&#39;utilisation de beaucoup de conditions VisibleIf
* Les fichiers sont supprimés par enregistrement automatique s’il existe un fichier .algautosave

### 5.5.0

*(Publié Le 25 Août 2016)*

<b>Ajouté :</b>

* Substance Designer est maintenant disponible sur Linux
* Nouvel éditeur MDL (Matériau Definition Language)
* [Bakers] Nouvelle Courbure à partir du baker de maillage
* [Bibliothèque] Utiliser des icônes de SVG au lieu de fichiers bitmap
* [Bibliothèque] Ajoutez une option pour filtrer le résultat pour MDL, Composition, Fonction et Fxmap
* [Graphe] Étendez l&#39;option « Afficher le nœud nouvellement créé » pour copier/coller/dupliquer les nœuds
* [Nouveau document] Créer un widget de sélection de modèle lors de la création d’un nouveau Graphe MDL
* [vue 3D][Iray] Affichage Mode de rendu + nœuds VCA en regard d’itérations/heure
* [vue 3D] Amélioration des performances du menu « matériau » à l’ouverture
* [3DView][Baker] Mise à jour vers FBX SDK 2017
* [vue 3D] Ajout de la possibilité d’afficher/masquer les informations de rendu (résolution, itérations, etc.) dans le menu d’affichage de vue 3D
* [Iray] Exposer de nouveau les paramètres de facettisation au montage de scène
* [Projet] Ajouter un alias généré automatiquement pour le répertoire de fichiers du projet
* [Projet] Spécifiez la texture d&#39;environnement par défaut dans les paramètres du projet
* [Contenu] Nouveau studio HDRi ajouté
* [Contenu] Ajout d’un nœud de transforme non carré à la bibliothèque
* Lancez SD avec un fichier .sbscfg spécifique

<b>Fixe :</b>

* [Graphe] Les entrées ne se connectent pas automatiquement aux sorties avec la même utilisation.
* [Graphe] Les entrées de nœud insérées ne sont pas connectées correctement
* [Graphe] La désélection doit également sélectionner un nœud sous la souris
* [Graphe] L’insertion de nœud ne se connecte pas à tous les liens
* [Bakers] diffusion incorrecte dans le baker de courbure
* [Bakers] crashs de « Texture transférée à partir du maillage » si le maillage haute définition ne comporte pas d&#39;UV
* [UI] L&#39;icône de fonction sur les paramètres n&#39;est pas modifiée lorsqu&#39;une fonction est définie
* [UI] Les info-bulles des paramètres sont coupées
* [vue 3D] plus de 1 000 lumières sont affichées dans la scène
* [vue 3D] GLSL Lambert shader ne gère pas correctement la texture srvb
* [vue 3D] Paramètres de Répétition manquants lors du raccordement de substances dans l&#39;Iray
* [Iray] L’exportation prédéfinie de mdl ne fonctionne pas lorsque les espaces dans le nom
* [Iray] Les paramètres de subdivision ne sont pas pris en compte
* [Paramètres] L&#39;identifiant des paramètres n&#39;est plus affiché
* [Paramètres] Crash lors de la modification de l&#39;URL de la ressource à partir de la ressource « De la ressource... » action
* [Paramètres] Conversion incorrecte du caractère &amp;
* [Explorateur] le fait de double-cliquer sur un « grand » graphe échoue souvent à l&#39;ouvrir dans la vue du graphe
* [Explorateur] Les mots de SVG incorporés sont affichés comme manquants dans l&#39;Explorateur
* [Explorateur] Crash lors du changement de nom d&#39;un élément avec le caractère &#39;&amp;&#39;
* [Contenu] La répétition du dégradé 1 est incorrecte lors de l’utilisation d’une rotation de 90/180°
* [Perforce] L’intégration ne semble pas fonctionner si l’espace de travail se trouve à la racine du disque dur
* [Données] Les UID générés pour les nœuds ne sont pas uniques
* [Préférences] L’ajout d’un alias ciblant la racine du disque dur gâche les chemins dans sbsprj
* [FUITE DE MÉMOIRE] Certaines boîtes de dialogue QD ne sont pas détruites lorsqu&#39;elles sont fermées

### 5.4.0

*(Publié Le 29 Avril 2016)*

**Ajouté :**

* Ajout d’un lien à la boutique de Substances
* [UI] Prise en charge des résolutions haute résolution
* [UI] Autoriser la réorganisation des onglets
* [vue 3D] Autoriser l’exportation du rendu vers ArtStation
* [vue 3D] Ajout du shader par défaut dans la liste shader
* [Graphe] Afficher le nom de la ressource au-dessus du nœud bitmap
* [Graphe] Amélioration de l’ordre des listes dans le menu de recherche de la barre d’espace
* [Bakers] Nouveau baker « Position à partir du Maillage »
* [Bakers] Nouveau paramètre « map normal » pour Texture Transfert baker
* [Bakers] Nouveau paramètre « Tangente » &amp; « Binormal » pour le baker de Normale de l&#39;espace monde
* [Scripts] Autoriser l’exécution de scripts pendant les actions Enregistrer, Exporter et Publish
* [Dépendances] Ajouter une option Réduire/Développer en fonction de la sélection
* Ajout d’un avertissement concernant les conflits d’extension de shell

**Fixe :**

* Crash à la sortie
* Le processus de Substance Designer peut encore être en cours d’exécution après la fermeture
* [Iray] Les sorties ne sont pas envoyées aux matériaux MDL lors du changement de moteur de rendu
* [Contenu] Échantillonneur de mosaïque : la rotation aléatoire du motif ne doit pas faire pivoter la forme

### 5.3.5

*(Publié Le 6 Avril 2016)*

**Fixe :**

* [vue 2D] L&#39;option de menu contextuel Transformation 2D est disponible sur tous les nœuds
* [vue 2D] widget de transformation 2d toujours modifiable après la suppression du nœud de transformation
* [vue 3D] Le chemin d&#39;accès de l&#39;environnement ne doit pas être affiché dans Paramètres d&#39;environnement
* [vue 3D] Les paramètres Effets de post-traitement ne sont pas enregistrés dans les ressources 3D
* [vue 3D] Le menu de la barre d’outils ne se comporte pas comme un menu ordinaire
* [Préférences] Impossible de définir une « limite de cache par Moteur » supérieure à 4 095
* [Préférences] La définition d’un shader par défaut n’est pas prise en compte
* [Iray] Les paramètres de couleur ne sont pas récupérés correctement
* [Iray] Les couleurs du Matériau MDL sont réinitialisées
* [Iray] Les bitmaps ne sont pas exportés avec le paramètre prédéfini MDL
* [Iray/Mac] Le redimensionnement de vue 3D rend la station de travail Mac crash
* [Graphe] Échec de l&#39;exportation du document de PSD
* [Graphe] Taille de nœud affichée incorrecte
* [Graphe de fonction] L’exemple d’image d&#39;entrée de nœud n’est pas modifiable si une seule image est branchée
* [Moteur] Crash lors du calcul du graphe Fxmap
* [Moteur OGL] Erreur lors de la génération du processeur de pixels
* [Dégradé] Le sélecteur de dégradé ne fonctionne pas sous Mac
* [PSD] image 8 bits non correctement convertie en 16 bits
* [Paramètres] Le widget d’histogramme de niveau n’a pas le même height en couleurs et en niveaux de gris
* [Console] Cliquer sur une cellule fait défiler la vue horizontalement
* [Explorateur] les ressources 3d Redéfinies l&#39;emplacement ne sont pas correctement ouvertes dans la vue 3d

### 5.3.4

*(Publié Le 16 Janvier 2016)*

**Fixe :**

* [Iray] tangente/binormal ne sont pas correctement pris en compte
* [Explorateur] Le package est marqué comme étant enregistré juste après son ouverture
* [vue 3D] Le reflet IBL est trop fort
* [vue 3D] Crash lors du glisser&amp;déposer d’une image 8 bits d’explorateur vers vue 3D
* Crashs de candidature depuis 2016 1er janvier

### 5.3.3

*(Publié Le 10 Novembre 2015)*

**Ajouté :**

* [Contenu] Ajouter « Bruit blanc rapide » (en fonction du processeur de pixels)
* [Content] Ajouter « Décalage global horizontal/vertical » sur Tile Samplers

**Fixe :**

* Crash lors de la création de nouvelles Substances dans certaines situations
* [Bakers] Crash lorsque les maps bakées mettent à jour le graphe
* [Baker] OBJ provenant de zbrush doit utiliser le nom de fichier pour Match By name
* [Paramètres] Crash lors de l’annulation/la restauration/l’annulation dans le graphe de fonction
* [Graphe] Les points de fractionnement ne sont pas collés à l’emplacement correct

### 5.3.2

*(Publié Le 30 Octobre 2015)*

**Ajouté :**

* [Contenu] Ajout d’un contrôle de filtrage pour l’entrée de motif sur les Tile Generator

**Fixe :**

* [vue 3D] Point de mise au point mal initialisé
* [vue 3D] Mauvais plan de clip lointain lors de la commutation de plusieurs fois de ressources de Maillage 3D
* [vue 3D] Artefact de rendu bref lors du chargement d’un maillage
* [vue 3D] La Map d&#39;environnement est noire lorsque le fichier est introuvable -> retour au mappage d’enveloppe par défaut
* [vue 3D] Crash après utilisation d’une image Latitude/Longitude personnalisée
* [vue 3D] Crash lors du chargement d&#39;un fichier obj spécifique
* [vue 3D] La recharge automatique du maillage ne fonctionne pas correctement
* [Iray] Impossible d&#39;attribuer une texture sur le mdl externe
* [Iray] Impossible d’attribuer des textures au canal d’anisotropie après la réinitialisation du matériau
* [UI] Le menu contextuel Windows apparaît lorsque le bouton droit de la souris est relâché après un déplacement dans 3DView
* [vue 2D] L’outil Info ne renvoie pas la valeur chromatique du pixel situé sous le curseur
* [Baker] les Images en niveaux de gris sont enregistrées sous forme indexée au format tga
* [Graphe] Les sorties en vue 3D doivent réinitialiser les canaux avant d’envoyer les sorties en vue 3D
* [Paramètres] Le nom d’entrée du paramètre est vide lorsqu’il est exposé de « Exposer les paramètres de nœud »
* [Performances] Définissez le rappel onSubstanceCallbackProfileEvent en moteur UNIQUEMENT si les minutages sont activés

### 5.3.1

*(Publié Le 21 Octobre 2015)*

**Ajouté :**

* [vue 3D] Afficher le nom du maillage dans la scène/modification au lieu de « Entité »
* [vue 3D] Rétablissement de la couleur par défaut à l’ouverture d’une nouvelle vue 3D
* [vue 3D] caméra de mise au point lors du passage de la scène à la primitive
* [vue 3D] Affiche la résolution du viewport de rendu lorsque la résolution personnalisée est utilisée
* [Iray] Ajuster la présentation des paramètres de subdivision
* [Iray] Sortie des informations d’Iray du journal dans le journal SD
* [Baker] Lire correctement les fichiers OBJ pour rendre la correspondance par nom compatible

**Fixe :**

* [vue 3D] Affichage incorrect des maillages ayant une échelle différente de 1.0
* [vue 3D] Le calcul automatique près du plan de clip ne fonctionne pas bien pour les objets volumineux
* [vue 3D] le mode Structure filaire affiche des fils trop épais
* [vue 3D] La fenêtre de rendu Enregistrer ne s’affiche pas si les effets de post-traitement sont désactivés
* crash [vue 3D] lors du changement de géométrie
* [vue 3D] Message « QOpenGLWidget : Cannot make uninitialized widget current » dans le journal
* [vue 3D] L’éclairage n’est pas calculé si la map d&#39;environnement est modifiée pendant l’exécution d’Iray
* [vue 3D] Crash lors de l’affichage du maillage 3d
* [vue 3D] Très mauvaises performances OpenGL après avoir utilisé Iray
* [vue 3D] Les plans de clip ne sont pas correctement calculés
* [vue 3D] La modification de la map d&#39;environnement n’actualise pas la vue 3D
* Les Textures [vue 3D] ne sont pas mises à jour lors de la modification du graphe
* [vue 3D] Les échantillonnages masqués GLSLFX sont toujours affichés dans le menu de sélection
* matériau [vue 3D] non restauré correctement lors de l&#39;ouverture de la ressource maillage
* [vue 3D] Fuite de mémoire RAM/VRAM lors de l’ouverture de divers maillages et de l’affectation de plusieurs graphes
* [vue 3D] Focus ne prend pas en compte la distance focale
* [Iray] nvcuvid.dll est manquant (désinstallez la version précédente pour vous débarrasser du message)
* [Iray] Le bouton « ... » de la boîte de dialogue Exportation des paramètres prédéfinis n’ouvre pas la fenêtre de dialogue
* [Iray] La réfraction/diffusion ne fonctionne pas correctement en mode physique\_diffusion\_specular
* [Iray] Mdl par défaut introuvable (couleur magenta)
* [Iray] Ne connectez pas les textures par défaut au matériau mdl pour activer le mode valeur dans le matériau d&#39;édition
* [Iray] La réduction à l&#39;échelle n&#39;est pas déclenchée lorsqu&#39;une texture est mise à jour
* [Bakers] Le baker normal de Worldspace effectue le rendu d’une image noire
* [Bakers] Crash lors du baking d’une map normal avec une vue 3d non ancrée
* [Bakers] Le Baking avec la méthode « Embedded » alors qu&#39;un chemin non valide est défini pour « link » empêche d&#39;enregistrer la ressource
* [Baker] Le Baking avec la méthode « Embedded » et la modification du format de fichier ne modifient pas l’extension sur le disque
* [Bakers] Les noms aléatoires des ressources incorporées ont tous un nom XXX..
* [Bakers] Les objets multiples dans .obj ne sont pas importés correctement
* fusion du Matériau [Content] : la sortie de couleur de base n’est pas masquée lorsque la couche est désactivée
* [Contenu] Le blanc\_bruit et les fichiers dérivés ne sont pas rendus correctement à 8k
* [Graphe] Baisse des performances dans le graphe
* [Graphe] Crash lors du glisser-déposer d&#39;un élément de fonction de la bibliothèque vers le Graphe de fonction
* [Graphe] « Afficher les sorties en vue 3D » ne doit envoyer que la sortie visible du nœud dans la vue 3D
* [Préférences] L’utilisateur par défaut\_project a un « Suffixe de nom » vide pour la fonctionnalité de baker de correspondance par nom
* [Moteur] La conversion des couleurs -> niveaux de gris entraîne une perte de précision
* [Console] La console/le journal est pollué par de nombreux messages
* [Partager] Crash lors de la tentative de partage d’un pack
* [UI] L’info-bulle est bloquée au-dessus du menu Fichiers récents
* Crash à la sortie

### 5.3.0

*(Publié Le 1Er Octobre 2015)*

<b>Ajouté :</b>

* [vue 3D] Ajout d’un module de rendu d’Iray Nvidia
* [vue 3D] Faire pivoter l’environnement à l’aide des touches CTRL + Maj + RMB
* [vue 3D] Effectuer le rendu du viewport 3D à une résolution personnalisée (Ogl / Iray)
* [vue 3D] Rendre le chargement de la scène asynchrone
* [vue 3D] Afficher la scène globale dans l’Explorateur de scènes
* [vue 3D] Désactivation de la grille par défaut
* [vue 3D] Ajout d’une atténuation de distance carrée inverse pour les éclairages ponctuels
* [vue 3D] Afficher le paramètre de couleur dans le RGB au lieu de RVBA
* [vue 3D] Paramètres Lumières/Caméra/Environnement distincts
* [Share] Améliorations de la fenêtre de téléchargement de Substance share

<b>Fixe :</b>

* [vue 3D] Erreur de normalisation des nuanceurs PBR
* [vue 3D] par Crash lorsque vous cliquez avec le bouton droit de la souris sur la racine dans le navigateur de scènes
* [vue 3D] nuanceurs PBR : économie d’énergie diffuse ou spécifications et éclairages ponctuels
* [vue 3D] Réinitialiser les couches par Matériau/Réinitialiser réinitialise également les couches à la couleur par défaut
* [Bakers] Position avec la normalisation Bsphere non centrée
* [UI] État flottant Windows non enregistré lors de la fermeture de l’application
* [Cooker] Impossible de publier lorsque le sbs est situé dans un chemin contenant un caractère spécial
* [Publication] Appuyez sur « Entrée » dans le champ de nom après la publication pour annuler la boîte de dialogue
* [Share] Export sbs ne conserve pas l&#39;alias sbs://

### 5.2.5

*(Publié Le 15 Septembre 2015)*

**Ajouté :**

* [Partager] Publish d’un pack à Substance share
* [UI] Ajouter un lien de Substance share dans le menu Aide

**Fixe :**

* [Cooker] « Taille hors limites » est une erreur au lieu d&#39;un avertissement
* [Cooker] « Impossible de trouver la sortie du sous-graphe » est une erreur au lieu d’un avertissement
* [vue 3D] PBR diffus/spec préfère la couleur de base à la diffusion
* [vue 3D] La Répétition ne fonctionne pas correctement avec les ombrages de tessation
* [Moteur] Crash lors de l’instancie d’un fichier sbsar spécifique
* [Moteur] Les fonctions Sizelog2 / pow2 ne fonctionnent pas correctement
* [Moteur] « définir » dans la taille de la sortie ne fonctionne pas
* [Moteur] Le Niveau du mipmap n&#39;est pas bridé pour les valeurs négatives
* [Contenu] Impossible de publier un graphe contenant trois filtres planaires

### 5.2.1

*(Publié Le 27 Août 2015)*

**Fixe :**

* [Graphe] Crash lors du calcul de sbsar spécifiques
* [Graphe] Crash lors de l’instancie de fxmap avec plusieurs entrées d’image
* [Moteur] Crash avec sizelog2
* [Moteur] La valeur par défaut du Paramètre exposé est ignorée avec DX10 Moteur
* [Bibliothèque] Le calcul des vignettes est rompu lorsque le projet contient un alias non valide
* [Cuisson] Définissez les paramètres « inconnu\_paramètre » et « paramètre dupliqué » comme avertissement au lieu des erreurs
* [Préférences] La limite du cache de Moteur est bloquée à 4 095 Mo.
* [Fonction] L&#39;étiquette de paramètre d&#39;entrée est interprétée comme un identifiant

### 5.2.0

*(Publié Le 18 Août 2015)*

**Ajouté :**

* [Bibliothèque] Ajout d’une option dans les préférences pour masquer/afficher les calques de PSD
* [Paramètres] Autoriser les données utilisateur sur plusieurs lignes
* [Graphe] Ajoutez une option de préférence pour afficher les commentaires à taille constante
* [Graphe] Ajout d’une option de préférence pour désactiver l’affichage des nouveaux nœuds dans vue 2D
* [Performances] Les performances de Processeur de pixels augmentent sur le moteur DX10
* [vue 3D] Ajout de tessellation aux nuanciers PBR
* [vue 3D] Ajout d’une opacité simple aux nuanciers PBR (pas de tri par face)
* [Contenu] Ajout de cibles Vray/Corona/Redshift/Arnold au filtre du convertisseur PBR (pour convertir les cartes pour ces systèmes de rendu)
* [Contenu] Ajout de la technique « axée sur les détails » au filtre Combinaison normale

**Fixe :**

* Crash lors de l&#39;ouverture de sbs avec une dépendance vide
* Le lien vers les calques de PSD est rompu après le rechargement du pack
* [Fonctions] Sécurité du type de rupture des fonctions imbriquées
* [Fonctions] Les libellés et les groupes et les descriptions ne sont pas affichés
* [Fonctions] Crash lors du copier/coller à partir d&#39;une fonction supprimée
* [Graphe] lien de Matériau rompu avec les graphes sbsar
* [Graphe] La création de plusieurs nœuds bitmap à partir de ressources empile les nœuds les uns sur les autres
* [Graphe] élément de commentaire non créé à la bonne position lors de l&#39;enfant d&#39;un nœud
* [Graphe] Les commentaires longs bloquent la sélection de la région
* [Bakers] La Map normal dans le repère tangent bake en noir sur Mac
* [Paramètres] Visible Si ne fonctionne pas lorsque le nom d&#39;entrée contient « - »
* [Paramètres] Valeur d’étape en Paramètres d&#39;entrée ignorée si elle est inférieure à 0,01
* [Bibliothèque] La balise « Visible dans la bibliothèque » n’est pas prise en compte pour sbsar

### 5.1.1

*(Publié Le 4 Juin 2015)*

**Ajouté :**

* [Graphe] Réduction de l’espace entre deux nœuds lors de l’utilisation de la connexion automatique
* [Graphe] Désactiver le paramètre Autoconnecter lors de l’utilisation du glisser-déposer dans le graphe
* [Graphe] contraignez le cadre sur la grille
* [Graphe] Désactiver l&#39;insertion de nœud sur/sur le lien sélectionné pour le lien de matériau
* [Préférences] Définissez la valeur maximale de la taille de texture maximale sur 8 192
* [Contenu] Ajout d’options de symétrie au nœud « Transforme sécurisée »

**Fixe :**

* [Graphe] Le nouveau nœud n&#39;est pas contraint sur la grille
* [Graphe] La permutation de liens peut générer des boucles/crashs
* [Graphe] Problème d’affichage lorsque la taille des nœuds/le minutage sont désactivés
* [Bakers] Crash lors du baking vers une ressource qui utilise le même nom que la scène
* [Baker] Le nom de ressource par défaut n&#39;est pas extrait du fichier de projet correct
* [Moteur] Problème de fonction Pow2/log
* [Moteur] Erreur dans l&#39;évaluation de la fonction
* [Fxmaps] Crash lors de la réinitialisation du paramètre à sa valeur par défaut
* [FxMaps] Mauvaise évaluation des fonctions
* [Préférences] Cliquer sur l’onglet du projet crashs SD
* [vue 3D] L’utilisation personnalisée est convertie en minuscules
* [Paramètres] Impossible de réorganiser les éléments dans les listes déroulantes
* [Explorateur] Crash lors du déplacement d’un graphe de fonction dans l’explorateur

### 5.1.0

*(Publié Le 28 Mai 2015)*

**Ajouté :**

* [Graphe] Rechercher/Afficher le contenu de la bibliothèque via le menu de la barre d’espace
* [Graphe] Afficher/ouvrir le nœud nouvellement créé
* [Graphe] redirection de lien (alt + maj)
* [Graphe] sélectionner les parents de nœuds
* [Graphe] Permuter 2 liens (X)
* [Graphe] Insertion d’un nœud sur un lien par glisser-déposer
* [Graphe] Créer un graphe à partir d&#39;une sélection de nœuds
* [Graphe] Supprimer le lien lors de l’utilisation d’Alt + LMB sur une épingle de nœud
* [Graphe] Ne connectez pas le nouveau nœud au précédent à l’aide de Maj
* [Graphe] Ajout d’une barre d’outils pour les filtres de base
* [Graphe] Améliorer la grille (contraint et résolution)
* [Graphe] Déplacez le commentaire/Cadre/Épingle vers le menu contextuel.
* [Graphe] Créer un nœud sur un lien sélectionné
* [Graphe] Ajout d’icônes aux éléments de fonction
* [Graphe] Modification des couleurs d’épingle dans le graphe de fonction
* [Graphe] Utiliser la touche Maj pour désactiver la connexion automatique des nœuds
* [Graphe] Effectuer le dessin du lien sélectionné sur les autres liens
* [Graphe] Ajout d’icônes aux nœuds Fxmap
* [Graphe] Ajout d’une option pour dessiner des liens courbes ou rectangulaires
* [Fonction] Accentuez la distinction entre les différents types de vecteurs dans le graphe de fonction (couleurs d’épingle/de liaison)
* [Fonctions] ajouter des icônes sur les nœuds et afficher des valeurs pour constante / set / get
* [Fonctions] Ajout de couleurs au titre du nœud
* [Fonction] Améliorer les performances pour l&#39;évaluation des fonctions (utiliser le code généré par SSE)
* [Fonction] Afficher un avertissement si le nœud Set/Get est vide
* [Bakers][Graphe] Image bitmap de tramage lors de la conversion en 8bpc
* [Bakers] Normales de vertex moyennes dans le fichier OBJ si le maillage ne contient aucune
* [Bakers] Correspondance par nom : utiliser le suffixe comme séparateur
* [Paramètres] Ajouter une option pour basculer entre RGB et HSV sur le widget de couleur
* [Paramètres] Ajouter le bouton Pipette dans le widget de couleur
* [Bibliothèque] Ajoutez une catégorie pour le contenu de base (nœuds de composition, fxmap, fonction...)
* [vue 2D] Infos : ajouter un affichage dans la plage [0, 1] et HSV
* [Vue 3D] Ajout de la prise en charge de mipmap pour l’environnement
* [Dépendances] Nettoyer les dépendances inutilisées avec le programme de mise à jour
* [Updater] N’enregistre pas les packs automatiquement

**Fixe :**

* [Crash] lors de la fermeture du pack
* [Crash] lors de l’ouverture du gestionnaire de dépendances sur un pack non enregistré
* [Crash] Exemple de bug coloré
* [Moteur] Blocage de la région de Répétition FxMap
* [Moteur] problème de précision avec le moteur SSE avec le nœud de flou et/ou de fusion
* [Moteur] Le Calcul ne s’arrête pas lorsque vous divisez par 0
* [Explorateur] crash lors de l’exportation d’un package avec dépendance s’il contient des cycles de dépendance
* [Explorateur] Le glisser-déposer de ressources échoue souvent
* [Bakers] La normale Bakée est rendue noire si elle est supérieure à 256\*256
* [Baker] L’enregistrement d’un pack au même emplacement que le chemin d’exportation entraîne la rupture du chemin
* [Bakers] Chemin cible par défaut incorrect lorsque le package n’a pas encore été enregistré
* [Moteur] Résultat de taille de pixel incorrect lorsqu’il est hérité de la fonction parent
* [Dépendances] La dépendance inutilisée n&#39;est pas supprimée
* crash [Dependencies] lors de l&#39;ouverture de la fenêtre de dépendances d&#39;un package qui contient des cycles de package
* [Graphe] la sélection est redimensionnée en fonction du zoom
* [Graphe] lien ne pas « contraindre » vers l’entrée/la sortie la plus proche
* [Graphe] pile d’annulation incorrecte (peut générer des crashs)
* [Graphe] La connexion multiple avec Ctrl ne fonctionne pas si l’épingle est déjà branchée
* [vue 3D] La couleur de Grille est affectée par la couleur d’arrière-plan
* le nœud de sortie [vue 3D][Graphe] contenant plusieurs utilisations n’est pas envoyé correctement à la vue 3d
* [vue 3D] shader de tesselage : bug de compilation sur les GPU AMD
* [vue 2D] problème de système d&#39;Épingle
* [Fonctions] Bogue de compilation de fonction (si autre)
* [Préférences] suffixe bas/haut non lu correctement dans sbsprj
* [Bibliothèque] Le fait de glisser-déposer un dossier sur un autre le supprime
* [Windows] Plusieurs sessions de SD peuvent être exécutées
* [Licence] L’ancienne licence n’est pas conservée
* [Contenu] Problème de filtre Détection des contours

### 5.0.3

*(Publié Le 1Er Avril 2015)*

**Ajouté :**

* [Préférences][Bakers] Ajoutez une option pour calculer tbn par vertex ou par pixel pour correspondre à UE4
* [Library] Utiliser le filtrage bilinéaire pour les vignettes
* [Bakers] Permet de réduire la fenêtre à moins de 800 px d’height
* [3DView] Égaliser l’exposition des maps d&#39;environnement/normaliser la rotation pour obtenir un éclair cohérent
* Nommer le raccourci de l’application avec la version majeure

**Fixe :**

* [Graphe] Crash lors de la suppression de certains nœuds de fantôme
* [Graphe] le nœud ancré reste ancré lors de la duplication du nœud
* [Graphe] Crash lors de la suppression de nœuds
* [Graphe] Les paramètres des sorties d’exportation ne sont pas stockés par graphe
* [Graphe] État d&#39;ancrage de nœud non valide lors de la suppression du nœud
* [Bakers] Les erreurs ne s’affichent plus dans une boîte de dialogue
* [Bakers] La ressource manquante ne s&#39;affiche pas comme manquante dans la fenêtre de baking
* La fenêtre [Publication] qui a échoué ne doit pas être modifiable
* [Publication] Sbsar Résultat incorrect
* [vue 3D] Les matériaux multiples des maillages FBX mis à jour ne sont pas rechargés correctement
* [vue 3D] Diffuse peut produire des valeurs négatives dans certains cas dans les nuanciers PBR
* [vue 2D] Le nombre de bits par pixel affiché pour les images de ressources est toujours de 8 bpc
* [Paramètres] Les paramètres ne sont pas toujours affichés dans les propriétés du graphe
* [Menu] « Exporter le fichier journal... » action ne parvenez pas à localiser le fichier log.txt
* [Batchtools] Erreur de sous-lecteur
* [Explorateur] Le chargement des packages met en surbrillance
* [Properties] Crash lors de l&#39;effacement d&#39;une fonction sur un paramètre enum
* [Préférences] Mikkt plugin de repère tangent n’est pas défini sur la valeur par défaut dans user\_project
* [Évaluation/Activation] Impossible d’évaluer/d’activer en ligne sous Windows
* La barre d’état de calcul déplace l’interface lors de l’actualisation
* Lancer plusieurs SD en même temps
* Mettre à jour l’URL du lecteur lorsque .exe est introuvable
* La modification du fichier sur le disque n’a pas été détectée correctement

### 5.0.2

*(Publié Le 17 Mars 2015)*

**Ajouté :**

* [Bibliothèque] Ajout du contrôle normal dans matériau\_adjustment\_blend
* [Bibliothèque] Ajout d’une option de fusion pour obtenir un dégradé normal dans matériau\_color\_blend
* Mettre à niveau vers Qt 5.4.1

**Fixe :**

* [Crash] OSX 10.9 et 10.10 dans FreeImage
* [Crash] Lors de l’ouverture d’un fichier fbx contenant des éléments sans aucun vertex
* [Graphe] Problèmes de glisser-déposer
* [Graphe] Le raccourci d’effacement du cache est rompu
* [Graphe] La balise apparaît en noir/transparent dans SD
* [Bibliothèque] Entrée normale en niveaux de gris triplanaires incorrecte
* [Bibliothèque] Le nœud de détection des contours ne fonctionne pas correctement avec le moteur du processeur
* [Paramètres] Gamme de curseur incorrecte pour float2/3/4
* [Paramètres] Exécution de la commande « Exposer les paramètres » deux fois par crash dans Designer
* [Console] N’est pas redimensionné correctement
* [Console] Duplication dans la liste des canaux : View3D et 3DView
* [3DView] L&#39;ordre des paramètres défini dans glslfx n&#39;est pas conservé dans l&#39;interface graphique
* crash [Explorateur] lors de l’actualisation des textures manquantes sur le disque
* [Fonction] Changer la valeur et modifier les pistes vers le crash
* [Baker] Crash lors de l’ouverture de la fenêtre de baking sur une ressource 3d manquante
* [PSD] crash Psdparse (MSVCR120.dll manquant)
* [Fenêtre À propos de] Saut de ligne manquant avec la version de Steam
* [Sbs] Nouvelles fonctionnalités de moteur inutilisées dans sbs
* [Sbsar] Nouvelles fonctionnalités non prises en charge en cas d’utilisation dans SD
* [Ui] La barre de progression ne s’efface pas une fois l’exportation terminée avec les dépendances
* vcomp100.dll introuvable lors du lancement de SD sur un Windows 7 fraîchement installé

**Problèmes Connus :**

* [Windows 8] Le glisser-déposer ne fonctionne pas au premier lancement. Le redémarrage du SD devrait résoudre le problème.

### 5.0.1

*(Publié Le 5 Mars 2015)*

**Fixe :**

* Correction d’un bug lors de l’exportation de bitmaps sous Windows.

### 5.0.0

*(Publié Le 4 Mars 2015)*

**Ajouté :**

* [Export] Jeter le Canal Alpha pour TGA et BMP quand il est complètement opaque
* [Vue 3D] Définition du shader PBR par défaut
* [vue 2D] Basculer pour afficher l’image en tant que prémultipliée alpha
* [Paramètres] Taille : ajoutez une valeur de verrouillage/affichage de largeur/Height dans les listes déroulantes
* [Dépendances] Nouveau gestionnaire de dépendances
* [Dependencies] affiche/recherche l&#39;instance de nœud correspondant à une dépendance
* [Dépendance] Ouverture d’un pack de dépendances dans l’explorateur de pack
* [Moteur] Fusion : prend en charge le paramètre Opacité lorsqu’un masque est utilisé
* [Moteur] Fusion : ajout de nouveaux modes de fusion (incrustation, écran, lumière tamisée, division)
* [Moteur] Fusion : simulation de transparence droite de support
* [Moteur] Nouveau nœud de Dégradé dynamique
* [Moteur] Nouveau nœud Distance
* [Moteur] Nouveau nœud de Processeur de pixels
* [Moteur] Fxmap : prise en charge de la fonction dynamique pour les images d&#39;entrée
* [Moteur] Fonction Sampler : prise en charge de l&#39;échantillonnage bilinéaire
* [Moteur] Fxmap : prise en charge du filtrage bilinéaire/le plus proche pour les images d&#39;entrée
* [Moteur] Fxmap : prise en charge de l’image d&#39;entrée alpha directe/prémultipliée
* [Bakers] Ajoutez une option pour faire correspondre la géométrie par nom de maillage entre les maillages basse et haute définition
* [Modèles] Création d’une substance de modèle pour la Substance Painter
* [Bakers] Nouvelle feuille de Texture à partir du baker maillage
* [Graphe] Ajoutez une « vérification de compatibilité » pour mettre en évidence les nœuds qui ne sont pas compatibles avec le moteur précédent
* [UI] Ajustements du menu Aide
* [Préférences] définissez Mikkt plugin de repère tangent sur la valeur par défaut (réinitialisez la valeur par défaut dans les préférences si SD4 est installé)
* [Bibliothèque] Ajout de nouveaux mappages HDR
* Nouvelle Substance à partir du modèle
* Basculer vers Qt5
* Mise à jour du système de licences vers SD5

**Fixe :**

* [Mac uniquement] Problème de sélecteur de couleurs avec l’écran Retina
* [Mac uniquement] Glissez-déposez sur la vue 3D sous Mac OS et faites-la pivoter
* [Bakers] Baker un mappage sans dossier de sortie produit une texture vide
* [Graphe] Les nœuds ancrés en cadre se déplacent de manière étrange
* [Paramètres] Le chemin de bibliothèque personnalisé n&#39;est pas chargé à partir des fichiers sbsprj
* [vue 3D] CTRL+R pour recharger tout le shader déclenche également la réinitialisation de la vue 3D
* [vue 3D] Env. Basculement uniforme mipmap height vers la valeur par défaut lors du chargement de shader
* [vue 3D] shader PBR : typo Diffuse vs baseColor
* [Library] Le chemin de bibliothèque non récursif casse les textures liées dans les packages
* Les Maps d&#39;environnement [Library] n’affichent pas .hdr
* [Explorateur] « Copier/Coller » sur la substance ne devrait pas être possible
* [Explorateur] Cliquez avec le bouton droit sur l’option « Coller » toujours disponible sur un graphe
* [Fonction] l’info-bulle de l’échantillonneur est incorrecte
* [Graphe] En mode compact, les instances n’affichent pas tous les noms de lien lorsqu’elles sont développées automatiquement pour ajouter un convertisseur de niveaux de gris
