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
source-git-commit: 668654bbe14817873413cc80743c53ee2045f48a
workflow-type: tm+mt
source-wordcount: '32039'
ht-degree: 0%

---


# Toutes les modifications

## Version 16

### 16.0.5

*(Publié le 26 août 2026)*

**Ajouté :**

* [Vue 3D] Ajout d’un bouton pour sélectionner l’AOV actuel
* [Contenu] Bruit de Perlin/Gaussien : paramètre d’échelle unclamp
* [Contenu] Masquer les ressources bitmap inutiles de la bibliothèque
<!--
* &#91;Legal&#93; To meet generative AI transparency legal requirements, this version is updated to automatically attach Content Credentials to qualifying content created or edited with generative AI tools.  
-->

**Fixe :**

* [Vue 3D] Les modifications de visibilité de l’environnement effectuées dans OpenGL ne sont pas répercutées dans les rendus Eclair
* [Boulangers] Le contexte de boulangerie n&#39;a pas été détruit après l&#39;actualisation des boulangeries pour une ressource bitmap UDIM supprimée
* [Bakers] Correction d’un crash lors de la suppression d’une ressource bitmap UDIM pendant l’actualisation de ses bakes
* [Contenu] Éclaboussure de forme v2 : l’height de forme du cylindre n’est pas correct
* [Contenu] Éclaboussure de forme v2 : la map density ne fonctionne pas correctement lorsque la taille du nœud dépasse 4 096
* [Contenu] Éclaboussure de forme v2 : l’utilisation du fichier SDF « Rock » derrière un If/Else peut entraîner une boucle infinie
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de fichier AXF
* [Sécurité] Correction d’une vulnérabilité de déréférence de pointeur NULL dans l’analyse de fichiers GLB
* [Sécurité] Correction des vulnérabilités d’écriture hors limites dans l’analyse de fichiers SBSAR
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

* [Vue 3D] Rapprochez la résolution de rendu à 4 096 en X et en Y
* [Bakers] Mise à jour de bake-sdk vers 3.22.3
* [Engine] Mettez à jour le moteur de Substance vers la version 9.4.4
* [OpenGL][OpenPBR] Réduction du bruit dans le lobe de specular pour une rugosité et une anisotropie élevées
* [Scènes] Conserver le mode d’interpolation UV primaire

**Fixe :**

* [Vue 3D] Exportation USD : les chemins des ressources sont stockés avec un chemin absolu
* [Boulangers] La cuisson échoue lorsque le chargement du maillage poly élevé est annulé (Windows)
* [Boulangers] La liste des scènes 3D en poly élevé n&#39;inclut pas les ressources avec le même identifiant que le poly faible
* [Boulangers] Espace universel normal : une normale WS est toujours retournée lorsqu’il y a une normale d’entrée
* [Contenu] Normale incorrecte lors de la mise à l’échelle non uniforme du motif dans l’éclaboussure de forme V2
* [Contenu] Éclaboussure de forme V2 : normales noires pour les formes « Plan » et « Disque »
* [Contenu] Éclaboussure de forme v2 : la première forme n’est pas correctement fusionnée avec l’arrière-plan
* [Crash] Blocage aléatoire éventuellement lié à la vidéo (info-bulles riches)
* [Graphique] Blocage lors du collage d’un nœud copié à partir d’un nouveau graphique avec un identifiant vide
* [PSD] Les fichiers de PSD sont chargés trop de fois

### 16.0.3

*(Publié Le 29 Mai 2026)*

**Fixe :**

* [Blocage] Correction d’une régression introduite dans la version 16.0.2 qui entraînait un blocage au lancement pour certains utilisateurs

### 16.0.2

*(Publié Le 28 Mai 2026)*

**Ajouté :**

* [OpenPBR] Prise en charge des constantes de couleur de base/AO

**Fixe :**

* [Vue 3D] Fuite de VRAM dans le traceur de chemin du GPU lorsque le displacement est activé
* [Vue 3D] Le thread principal reste occupé lorsque la vue 3D existe
* [Vue 3D][OpenPBR] OpenGL : les widgets « Épaisseur » semblent être bridés, mais acceptent des valeurs hors plage
* [Crash] Blocage lors du déplacement de l’entrée référencée à plusieurs endroits à la fois
* [Crash] Blocage lors de l’agrandissement d’une fenêtre
* [Crash] Blocage lors de l’écriture de TARGA ou BMP à partir du boulanger
* [Blocage] Blocage aléatoire lors de l’affichage de la vue 3D
* [Graphique] Ordre incorrect des épingles d’E/S lors du déplacement des E/S après la modification des identificateurs
* [Linux][Exporter] Les boîtes de dialogue « Publish sbsar » et « Envoyer à » n’ajoutent pas d’extension de fichier

### 16.0.1

*(Publié Le 5 Mai 2026)*

**Ajouté :**

* [Échantillons] Ajouter un échantillon de matière dédié à SDF / Shape Splatter
* Visionneuse 3D [Contenu] : modification de l’état par défaut
* [Contenu] Visionneuse 3D : ajout d’un environnement par défaut
* [Contenu] Mappeur de forme éclaboussure v2 : ajoutez un paramètre de centre de projection par axe pour le mappage triplanaire
* [Content] Mappeur d&#39;éclaboussures de forme v2 : ajouter un paramètre de mosaïque
* [Contenu] Éclaboussure de forme v2 : active l’extrusion de forme par défaut
* [3DView] Prise en charge des GPU Intel Panther Lake dans le traceur
* [Vue 3D] Amélioration de la mise en forme des info-bulles contextuelles « Displacement »
* [Moteur] Mise à jour vers la Substance Engine v9.4.3
* [OpenPBR] geometry_tangent : ajouter la prise en charge des constantes
* [Préférences] Ajoutez une option pour que TGA/BMP écrive la couche alpha si elle est entièrement opaque
* [Tiers] Mise à jour vers « Adobe Color Engine » (ACE) 7.0
* [UI] Rendre la fenêtre du gestionnaire de plug-ins toujours visible (modale)

**Fixe :**

* [Vue 3D] La mise à l’échelle de la fenêtre est appliquée lors de l’utilisation d’une résolution fixe
* [Vue 3D][OpenPBR] Blocage lors du chargement d’une scène GLTF exportée à partir de Designer et de l’utilisation d’une matière OpenPBR
* [Vue 3D][OpenPBR] Les matières exportées depuis Painter ne peuvent pas être remplacées dans Designer
* [Contenu] Visionneuse 3D : shape.id n’est pas initialisé et génère des messages dans la console
* [Contenu] Mappeur d’éclaboussures de forme v2 en niveaux de gris : l’entrée de motif 4 est inutilisée dans la projection triplanaire
* [Contenu] Mappeur d’éclaboussures de forme v2 : l’ID SDF est décalé de -1 lors de l’utilisation du mode « 1 image par ID de matériau »
* [Eclair][USD] résultat incorrect lors de l’application d’une matière sur un USD généré par Designer
* [Moteur] Calcul d&#39;un nouveau nœud Niveaux Forme éclaboussure V2 graphique principal brouillé suite aux calculs
* [Engine] Le module d’une variable par rapport à sa valeur égale ne renvoie pas 0 avec le moteur GPU dans certains cas
* [Engine][Content] Arc tangent 2 renvoie 0 ou Pi pour les vecteurs X-right dans un cas spécifique
* [Moteur][Ubuntu][SSE2] Blocage lors du chargement d’un SBSAR spécifique dans le graphique
* [Graphique] Blocage lors de la connexion de la sortie du processeur de valeurs à l’entrée bitmap
* [Graphique] Blocage lors du branchement de la valeur dans l’entrée d’image dans certains cas
* [Graphique] Le graphique est automatiquement calculé à chaque enregistrement automatique lors de l’utilisation des maps bakées
* [GraphRender] Blocage lors de la connexion de la sortie de valeur d’Atlas scatter à l’entrée d’image d’Atlas splitter
* [Linux][Exporter] Le format de fichier modifié est ignoré dans les boîtes de dialogue d’enregistrement de fichier
* [Mac][Steam] Une fenêtre contextuelle de sécurité s’affiche lorsque nous démarrons Designer
* [Filet] Les matériaux OBJ ne sont pas importés correctement
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
* [Contenu] Nœuds de transformation 3D SDF
* [Contenu] Nœuds de matière 3D SDF
* [Contenu] Nœud d’angle par rapport au vecteur
* [Content] Nœuds à valeur constante
* [Vue 3D] OpenPBR shader pour le moteur de rendu OpenGL
* [Vue 3D] Ombrage d’OpenPBR pour la pixellisation et les systèmes de rendu de Pathtracer GPU
* Fenêtre de Displacement [Vue 3D] pour définir l’échelle d’height, le niveau d’height et la facettisation
* [Vue 3D] Réorganisation des éléments de la barre d’outils
* [Vue 3D] Définir OpenPBR comme modèle de matériau par défaut dans la vue 3D
* [Vue 3D] Veillez à ce que la vue 3D prenne en compte l’attribut de graphique « Modèle de matériau ».
* [Vue 3D] Synchronisation des modèles de matériau lors du basculement entre les modes de rendu Pixellisation/Pathtracer GPU et OpenGL
* [Vue 3D] Assurez-vous que le modèle de matériau est persistant lors de la commutation des rendus 3D et de la synchronisation des modifications de définition de matière
* [Vue 3D] Pathtracer GPU : activer le cycle de pixels du bruit bleu
* [Vue 3D] Exposer le contrôle d’opacité de l’occlusion ambiante
* [Vue 3D] Définissez la plage de paramètres de mosaïque sur [0, 10] pour tous les ombrages
* [Vue 3D] Renommer l’action « Focus » en « Image »
* [Vue 3D] Gérer le nouveau paramètre refineLevel qui remplace tessellationFactor
* [Vue 3D] Ajouter un compteur IPS
* [Vue 3D] Déplacez la barre de progression dans la même barre d’outils horizontale que l’espace colorimétrique en bas
* [Boulangers] Afficher l’UV du boulanger sélectionné dans l’aperçu
* [Graphique] Ajouter un nouvel attribut « Modèle de matériau » aux graphiques de Substance
* [NewGraph] Ajout de séparateurs dans la vue Miniatures
* [Paramètres] Définissez la valeur constante par défaut pour les paramètres d’entrée avec l’éditeur « Function ».
* [Paramètres] Remplir la zone de liste déroulante de `Set` et `Is defined` paramètres de nœud avec des variables disponibles
* [Préférences] Supprimer l’option obsolète « Facteur de mise à l’échelle » dans l’onglet « Vue 3D »
* [Publish] Boîte de dialogue Publish : Inclure le modèle de matériau dans les informations sur le graphique
* [Python] Ajoutez une nouvelle classe SDMaterialModelDescription pour obtenir les informations d&#39;un modèle de matériau
* [Python] Autoriser à obtenir/définir la propriété de modèle de matériau des objets SDSBSCompGraph
* [Éditeur Python] Augmentez la taille de la police à 12
* [Modèles] Ajouter des modèles d’OpenPBR
* [Templates] Convertir des échantillons de matière en OpenPBR
* [Tiers] Mise à jour de Boost vers la version 1.88
* [Tiers] Mise à jour de l’API C++ vers C++20
* [ThirdParty] Mettre à jour NGL vers 1.42
* [ThirdParty] Mise à jour oneTBB vers la version 2022.x
* [ThirdParty] Mettre à jour OpenColorIO vers la version 2.5.x
* [Tiers] Mise à jour OpenEXR à la version 3.4.x
* [ThirdParty] Mettre à jour Qt &amp; QtForPython vers la version 6.8.x et Python vers la version 3.13.x
* [ThirdParty] Mettre à jour TBB vers oneTBB 2021.x
* [Dépréciation] Supprimer Iray et l’éditeur MDL

**Fixe :**

* [Vue 2D] La plage de sélection de l’histogramme n’est pas conservée lorsque la largeur du widget devient petite
* [Exportation 3D] Les filets exportés depuis Designer ne sont pas rendus de la même manière en mode d’affichage utilisateur
* [Vue 3D] L’affectation d’éléments non-udim à la vue 3D laisse le mode de rendu en mosaïque unique
* [Vue 3D] Résultat serré lors de l’utilisation d’OCIO
* [Vue 3D] Blocage lors de l’application d’une texture de graphique sur un matériau non remplacé pour une scène spécifique
* [Vue 3D] Blocage lors de la création de tampons d’image
* [Vue 3D] Pathtracer GPU Eclair : géométrie rompue et performances réduites lors du rendu d’un modèle spécifique
* [Vue 3D] Transformation de texture incorrecte pour des scènes spécifiques
* [Vue 3D] Cadrage incohérent de la scène/sélection lors de l’utilisation d’une résolution de rendu fixe
* [Vue 3D] Couleur diffuse incorrecte lors du rendu de certains fichiers GLTF
* [Vue 3D] Environnement invisible lors du changement de moteur de rendu dans un cas spécifique
* [Vue 3D] Les matières ne sont pas détectées correctement lors de l’importation de certains fichiers .fbx
* [Vue 3D] Le remplacement des matériaux plusieurs fois réinitialise la mosaïque à 1
* [Vue 3D] Les propriétés de la catégorie « UV » ne sont pas enregistrées dans les fichiers SBSSCN
* [Vue 3D] L’option « Réinitialiser et afficher les sorties en vue 3D » à partir de graphiques à sortie unique ne réinitialise pas les matières
* [Vue 3D] &#39;Enregistrer le rendu&#39; : le format d’image modifié n’est pas conservé
* [Vue 3D] La sélection ne fonctionne pas sur les GPU AMD
* [Vue 3D] La scène 3D autonome n’est pas actualisée en cas de modification sur le disque
* [Vue 3D] Certaines propriétés de matériau de couleur ne sont pas gérées correctement lorsqu’elles sont remplacées
* [Vue 3D] Les textures UDIM ne sont pas appliquées correctement sur un maillage spécifique
* [Vue 3D] La scène USD avec la matière MaterialX ne s’affiche plus correctement
* [Bakers] Blocages avec certains maillages
* [Boulangers] Transfert de texture : blocage dans bkBufferViewCopy
* [Cooker] Boucle infinie dans le nœud While Loop dans un cas qui pourrait être empêché
* [Moteur] Arrêter le moteur de Substance lors de la fermeture de l&#39;application
* [Général] Éviter les blocages aléatoires lors de la sortie de l’application (Windows uniquement)
* [Graphique] Graphique de fonction : la propagation de type ne fonctionne pas correctement dans certaines situations
* [Graphique] Les liens de graphique sont supprimés lorsqu’un nœud d’entrée d’image est renommé
* [Graphique] Les liens et les épingles affichent parfois des artefacts
* [Préférences] La mise à l’échelle de la fenêtre d’affichage est inversée
* [Propriétés] Blocage lors de la modification du réglage d’entrée de graphique lors de l’affichage de ses paramètres d’instance
* [Python] Impossible d&#39;importer les modules PySide6 (conflit possible avec l&#39;installation existante de PySide6)
* [Python] Les modules PySide et Shiboken existants sont en conflit avec Designer
* [UI] Le style de survol disparaît sur les boutons dans un cas spécifique (Windows uniquement)
* [UI] Le style de survol n’est pas visible sur les boutons déroulants lorsque vous cliquez dessus (macOS uniquement)
* [UI] Le bouton « En savoir plus » dans l’info-bulle « ? » ne fonctionne pas lorsque l’info-bulle est en dehors des limites de la boîte de dialogue (Windows uniquement)

**Problèmes connus :**

* [Graphique] Les icônes générées pour les OpenPBR ne sont pas précises
* [Vue 3D] Les scènes avec des primitives animées ne sont pas prises en charge correctement
* [Vue 3D] Le traceur de tracé n’est pas pris en charge sur toutes les cartes graphiques AMD

## Version 15

### 15.1.3

*(Publié Le 10 Mars 2026)*

**Ajouté :**

* [Bakers] Ajout d’une macro outputsize pour le nom de fichier
* [Boulangers] Évitez de charger le filet Highpoly avant la cuisson
* [Bakers] CLI : mettre à jour la description de l’option « output-size » avec des macros de taille
* [Bakers] Convertir le format de texture d’entrée au format demandé
* [Bakers] Désactiver l’option « Décaler la carte » lorsque l’option « Utiliser la cage » est cochée
* [Boulangers] Affichez les maps bakées déjà présentes lorsque la fenêtre de cuisson est rouverte
* [Boulangers] Gardez la fenêtre de cuisson ouverte jusqu’à ce que tous les processus de cuisson soient effectivement annulés
* [Bakers] Fonction Migrate BindTexture
* [Boulangers] [Paramètres] Définissez la valeur par défaut du « Mode de filtrage des noms » sur « Nom parent (hérité) »
* [Bakers] [Info-bulle] Ajoutez la valeur « Mode de filtrage de nom » à l’info-bulle du paramètre « Match »
* [Engine] Mettez à niveau le moteur de Substance vers la version 9.3.4

**Fixe :**

* [Vue 3D] « Afficher les sorties en vue 3D » ne remplace pas l’affectation existante sur les graphiques avec une seule sortie
* [Vue 3D] Impossible d’afficher les UV dans certains cas
* [Vue 3D] Les tangentes calculées semblent brisées pour USD
* [Vue 3D] Blocage lors de l’ouverture du menu Système de rendu
* [Bakers] Impossible de définir une distance supérieure à 1 lorsque l&#39;option Relative à la boîte n&#39;est pas cochée
* [Boulangers] Le boulanger de couleur prend trop de temps à finir dans des cas spécifiques
* [Boulangers] Couleur : Blocage lors de la cuisson d&#39;Îlots UV
* [Bakers] Les plages de paramètres de distance et de rayon sont trop étroites lorsque la valeur est absolue
* [Boulangers] Échec lors de la cuisson à partir de tangentes et bitangentes manquantes à poly élevé qui ne sont pas requises
* [Boulangers] Couleurs de matériau incorrectes dans la ligne de commande du boulanger
* [Boulangers] Dans certaines situations, les multiples maillages en poly élevés sont ignorés
* [Boulangers] Normal : sortie noire lors de l’utilisation du lissage et de la diffusion (macOS uniquement)
* [Bakers] La vérification du chemin de mappage décalé signale des échecs inattendus lors de l’utilisation des ressources du package bitmap
* [Bakers] L’info-bulle de la carte de décalage est incorrecte
* [Bakers] Le placement de la ressource dans un dossier spécifique au maillage ne fonctionne pas
* [Boulangers] Transfert de texture : la valeur « réglage UV » n&#39;est pas restaurée comme elle l&#39;était lors de la réouverture de la fenêtre de cuisson
* [Bakers] Transfert de texture : une entrée en niveaux de gris n’entraîne pas une sortie en niveaux de gris
* [Baker] L’avertissement pour le baker hérité désactivé n’est pas effacé lors du changement de source de texture dans le baker cible
* [Bakers] [UDIM] La carte de décalage est uniquement appliquée à UDIM 1001
* [Graphique] UDIM 1001 est toujours calculé quel que soit le fichier UVT utilisé

### 15.1.2

*(Publié Le 3 Février 2026)*

**Fixe :**

* [Moteur] Niveaux : les valeurs à virgule flottante sont toujours serrées sur [0, 1]
* [Bakers] La correspondance de la géométrie par nom de parent (hérité) ne fonctionne pas pour les sous-maillages
* [Boulangers] Couleur : les modifications apportées aux couleurs de matière dans l’interface utilisateur sont ignorées
* [Vue 3D][Bakers] Le chargement du fichier OBJ prend beaucoup de temps

### 15.1.1

*(Publié Le 20 Janvier 2026)*

**Ajouté :**

* [Échantillons] Ajoutez deux échantillons pour créer des sections afin d’alimenter l’outil ruban Painter
* [Moteur] Mise à jour vers la Substance Engine v9.3.2
* [Moteur][Métal] Améliorer les performances
* [Moteur] L’interpolation bilinéaire des textures entières est désormais effectuée avec une précision accrue (back-end du processeur).
* [Boulangers] Consigner un avertissement si la couleur du sommet est absente du maillage poly élevé
* [Branding] Mise à jour des icônes de types de fichiers
* [NewGraph] Appliquer les styles de survol sur l’icône (i) en modes d’affichage « Liste », « Packs » et « Répertoires »

**Fixe :**

* [3DView] Les maillages UDIM ne génèrent plus un seul carreau
* [3DView] Blocage lorsqu’aucun renderDevice n’est détecté
* [Branding] Correction des icônes des fichiers .SBS sous Linux
* [Contenu] RGB à la fonction TSL : résultat incorrect pour près de 0 entrée
* [Graphique] Le générateur d’icônes/de vignettes de graphique ne fonctionne pas
* [Graphique] Menu Nœud : les éléments regroupés sans vignette n’ont pas de retrait.
* [Moteur][Contenu] Couleur pour masquer v2 : artefacts sur le moteur SSE2 lors de l’utilisation de l’espace colorimétrique de distance Lab
* [Moteur][Contenu] Couleur pour masquer v2 : artefacts sur les moteurs GPU arm64 lors de l’utilisation de l’espace colorimétrique de distance Lab
* [Moteur][Métal] Sortie d&#39;irradiance noire pour nœud de Rendu PBR
* [Moteur][Mac] Résultat incorrect dans une fonction de processeur de pixels sur Metal
* [Moteur][Mac] Améliorez la précision de certaines instructions utilisées dans les processeurs pixellisés sur les GPU Apple Silicon M1/M2
* [Moteur] Le redimensionnement des images d’entrée (ou des ressources intégrées) n’introduira plus d’artefacts de bordure (back-end du processeur)
* [Moteur] Le filtre Niveaux ne verrouille plus ses valeurs d’entrée en virgule flottante lors de la sortie de textures 8I/16I (back-end du processeur)
* [Engine] Correction d’un bug FxMaps où les images d’entrée en niveaux de gris consommées par les nœuds FxMaps pouvaient être échantillonnées de manière incorrecte (back-end du processeur)
* [Moteur] Correction de certains artefacts dans la version à 1 amorce du filtre Distance (principaux GPU)

### 15.1.0

*(Publié Le 11 Décembre 2025)*

**Ajouté :**

* [Nouveau graphique] Modification de la fenêtre du nouveau graphique
* [NewGraph] Ajout d’échantillons de matériaux et d’échantillons avancés
* [NewGraph] Ajouter un nouvel attribut pour le graphique pour les données du modèle (catégorie et sous-titre)
* [NewGraph] Option Supprimer le format de sortie
* [Contenu] Ajout de fonctions de hachage
* [Contenu] Ajout de mappeurs de tonalité à features.sbs
* [Contenu] Bruit anisotrope v2 : ajout du format de sortie par défaut, ajout de désordre
* [Content] Appliquer la casse de la phrase aux étiquettes de nœuds et de paramètres
* [Contenu] Points BnW 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Points BnW 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Points BnW 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Content] Cellules 1,2,3,4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques, options de désordre
* [Contenu] Clouds 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Clouds 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Clouds 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Couleur au masque v2
* [Contenu] Bruit directionnel 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Bruit directionnel 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Rayures directionnelles v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 1 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 3 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 4 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dirt 5 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Dégradé de Dirt v2 : ajout du format de sortie par défaut, nouvelles options de désordre
* [Content] Somme fractale Base v2 : ajout du format de sortie par défaut, désordre, pas de prise en charge des mosaïques
* [Content] Somme fractale 1,2,3,4 v2 : ajout du format de sortie par défaut
* [Contenu] Bruit gaussien v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Taches gaussiennes 1&amp;2 v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Fibres désordonnées 1,2,3 v2 : ajout du format de sortie par défaut, pas de prise en charge de la mosaïque, options de désordre
* [Contenu] Bruit d’humidité v2 : ajout du format de sortie par défaut, pas de prise en charge des mosaïques
* [Contenu] Nouveau nœud « Bruit d&#39;humidité 2 »
* [Contenu] Bruits : mettre à jour pour ajouter le format de sortie par défaut
* [Contenu] Bruit de perlin v2 : ajout du format de sortie par défaut, pas de prise en charge de la juxtaposition
* [Contenu] Mappeur de formes : ajouter un mode de filtrage
* [Contenu] Mappeur UV : ajouter un mode de filtrage
* [Contenu] Forme d’onde 1 v2 : utilisation du format de sortie par défaut + nouvelles options
* [Contenu] Bruit blanc v2 : utilisation du format de sortie par défaut, ajout d’options de distribution
* [Boulangers] Afficher uniquement les UV du maillage sélectionné
* [Bakers] Ajoutez une option pour sélectionner la méthode de correspondance de la géométrie par nom
* [Boulangers] Sélectionner le boulanger le plus proche lorsqu’un boulanger est supprimé
* [Boulangers] UDIM : définissez une liste de tuiles UV à cuire
* [Bakers] Mise à jour du kit de développement de bake vers la version 3.15.4
* [3D View/SceneBrowser] Évitez de sélectionner un élément UsdPrimitive lorsque vous effectuez un clic droit dessus
* [ColorManagement] Prise en charge d&#39;ACES 2.0
* [Graphique de composition] Autoriser à définir un nœud de sortie comme « Sortie par défaut »
* [Cooker] Supprimer l&#39;avertissement sur les entrées non connectées des instances de fonction¬†
* [Fonctions] Opérateur Add isDefined
* [Graphique] Regrouper les éléments par attribut « groupe » dans le menu du nœud
* [Graphique] Amélioration du rendu des vignettes

**Fixe :**

* [Vue 3D] La texture en niveaux de gris L16 s’affiche avec une teinte rouge lorsqu’elle est connectée à l’environnement ou à la baseColor
* [Vue 3D] La modification de la liaison de matière d’une scène sans matière crée une nouvelle matière par défaut
* [Vue 3D] Les normales calculées ne sont pas correctes pour des maillages OBJ spécifiques
* [Vue 3D] L’environnement personnalisé de SBSSCN n’est pas visible lors du chargement dans le traceur de chemin
* [Vue 3D] Erreurs dans la console lors de la rotation d’un environnement désactivé
* Le Specular level [Vue 3D] n’est pas appliqué correctement
* [Vue 3D] Le Specular edge color ne fonctionne pas lors de l’utilisation de la pixellisation Eclair
* [Vue 3D] La matière ajoutée par l’utilisateur n’est pas appliquée aux scènes par défaut
* [Vue 3D][Boulangers] La couleur du matériau est trop sombre une fois remplacée ou lors de l’utilisation d’un boulanger « Color »
* [Vue 3D][Bakers] Aucune couleur de matière du fichier FBX
* [Boulangers] Les couleurs de matériau dans les fichiers FBX ne sont pas correctement détectées
* [Bakers] L’option « recalculer\_tangentes » est toujours « false » dans les exportations de paramètres prédéfinis JSON
* [Bakers] CLI : Blocage lors de l’exécution du même baker de manière consécutive via un fichier JSON
* [Bakers] La mise à jour du paramètre « color-generator » ne fonctionne pas pour « Grayscale »
* [Contenu] Masquage sur tracés : échec dans les rapports non carrés
* [Contenu] Rendu Rendu PBR/Icône : fonction incorrecte du lobe de specular
* [Contenu] Tracés vers la spline : définissez la « Taille de sortie » sur « Relative au parent » par défaut.
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Mappeur de spline : problème de ligne de 1 px dans des cas aléatoires
* [Contenu] Spline mapper : UV étirés dans certains cas lorsque le thickness est de 0
* [Graphique] Blocage lors de la suppression de la sortie d’un sous-graphe de fonction
* [Graphique] Le type de couleur du nœud d’entrée peut être modifié dans les packages en lecture seule
* [Graphique] L’entrée principale peut être modifiée dans les packages en lecture seule
* [Propriétés] La couleur du widget d’aperçu de couleur ne correspond pas à l’état du bouton sRVB
* [Scène] Impossible de charger un fichier OBJ de plus de 2 Go
* [UI] Les états d&#39;ancrage de la console et du gestionnaire de dépendances ne sont pas restaurés après le redémarrage

### 15.0.3

*(Publié Le 23 Octobre 2025)*

**Fixe :**

* [Contenu] La sortie d’aperçu des nœuds Outils spline ne s’affiche pas par défaut
* [Graphique] Blocage lors de la suppression de la sortie d’un sous-graphe de fonction

### 15.0.2

*(Publié Le 18 Septembre 2025)*

**Ajouté :**

* [3D View/OpenGL] Supprime l’effet de structure filaire appliqué au filet sélectionné
* [Vue 3D] Permet d’utiliser la touche F pour se concentrer sur un filet sélectionné lorsque l’Explorateur de scènes est activé
* [Vue 3D] Le rendu n’est pas actualisé lors de la modification du format de map normal
* [BakersCLI] Option permettant de contrôler la taille de la mémoire cache de la surface
* [BakersCLI] Renommez l’option « use\_cache » en « keep\_meshes\_in\_cache ».
* [UI] Icône d’actualisation pour les scènes 3D dans la bibliothèque

**Fixe :**

* [Vue 3D] Blocage lors de l’affectation d’un nœud de matériau à une scène multi-matériau
* [Vue 3D] Le graphique créé à partir des entrées de texture est toujours affiché dans la vue 3D, quelles que soient les préférences.
* [Vue 3D] Utilisation incorrecte dans l’info-bulle du badge « Vu en vue 3D » dans un cas spécifique
* [Vue 3D] Beaucoup d’erreurs USD lors du remplacement de scènes spécifiques
* [Vue 3D] Artefacts d’ombre lors de l’utilisation du displacement sur une scène plate dans la pixellisation
* [Vue 3D] Certaines scènes spécifiques ne sont pas visibles lors de l’utilisation du rendu OpenGL
* [Vue 3D] La boîte de dialogue utilisée pour « Sélectionner le Graphe Substance de destination » comporte toujours l’icône de graphique « En attente ».
* [Vue 3D] Le menu contextuel de la clôture ne s’affiche pas pour des scènes spécifiques
* [Vue 3D] Les badges « Vu en vue 3D » ne sont pas effacés lors du changement de scène dans un cas spécifique
* [Vue 3D] Couleur délavée dans la vue 3D lors de l’utilisation de la gestion des couleurs ACE Adobe
* [Vue 3D][Linux] Plusieurs scènes s’affichent en noir dans le moteur de rendu OpenGL
* [Vue 3D][Scene Browser] Les touches fléchées déplacent la sélection à la racine
* [BakerCLI] Impossible de remplacer certains paramètres
* [Boulangers] Artefacts en dilatation lors de l&#39;utilisation de boulangers normaux avec anticrénelage
* [Boulangers] Le processus de cuisson s&#39;est brusquement arrêté dans l&#39;interface de ligne de commande tout en cuisant une grande quantité d&#39;UDIM à 4K
* [Boulangers] Blocage lors de l’enfoncement du boulanger dans la liste des boulangers dans un cas spécifique
* [Bakers] La sélection du format passe de .surface à .dds
* [Boulangers] Geler pendant la cuisson d&#39;une grande quantité d&#39;UDIM à 4K
* [Boulangers][macOS] Blocage lors du transfert de texture au four avec l’anticrénelage
* [Contenu] Liste de points : les points ne sont pas dans le bon ordre lorsque la texture des données n’est pas carrée
* [Contenu] Afficher la palette de couleurs : les nœuds internes sont calculés à des résolutions trop élevées
* [Données] Blocage lors du changement de nom de la sortie pour corriger la sortie fantôme dans l’instance
* [Moteur] Distance : la luminance du masque d’entrée est modifiée
* [FxMap] $tiling n’a aucun effet si le FX-Map est à l’intérieur d’un sous-graphe
* [Graphique] La recherche floue renvoie des résultats non pertinents
* [Éditeur Python] Les scripts chargés ne sont pas rouverts entre les sessions

### 15.0.1

*(Publié Le 22 Juillet 2025)*

**Ajouté :**

* [Vue 3D] Autoriser à texturer les maillages USD qui ont displayColor et aucune liaison de matière
* [Vue 3D] Ne créez pas automatiquement une matière par filet qui ne possède pas de reliure de matière
* [Vue 3D] Renommez « Echantillons de pixels convergés » en « Echantillons ».
* [Vue 3D] Renommez le paramètre « Échelle UV activée » en « Activer la Taille physique à partir du graphique ».
* [Vue 3D] Réduisez l’intensité du displacement en fonction du paramètre Limites.
* [3D View/OpenGL/Iray] Ajout d’un message dans la clôture lorsque l’environnement par défaut est désactivé
* [Bakers] Utilisez des icônes pour les boutons afin de réorganiser les lignes dans la liste de rendu Bakers
* [Préférences] Ajoutez une option pour définir le moteur de rendu de vue 3D par défaut
* [Propriétés] Faites en sorte que « Rétablir la valeur par défaut » utilise les valeurs par défaut créées le cas échéant.

**Fixe :**

* [Vue 3D] Artefacts sur une scène spécifique lors du rendu avec OpenGL
* [Vue 3D] L’environnement par défaut n’est pas désactivé lors du chargement d’une ressource de scène 3D USD qui en contient une
* [Vue 3D] L’affichage du menu contextuel de la fenêtre d’affichage prend plusieurs secondes dans les scènes de grande taille
* [Vue 3D] L’intensité émissive est définie sur 0 lors du remplacement de matériaux autres que les USD en utilisant uniquement la couleur émissive.
* [Vue 3D] Les couches rouge et bleue sont permutées dans une texture 8 bits utilisée comme environnement.
* [Vue 3D] Le glisser-déposer RMB ne fonctionne pas de manière cohérente en raison du registre par clic droit
* [Vue 3D] L’option « Afficher uniquement » sur le sous-ensemble masque son filet parent
* [Vue 3D] Les scènes par défaut chargées à partir d’un fichier apparaissent avec une couleur de base incorrecte
* [Vue 3D] La propriété « Échelle UV » est réinitialisée lors du passage d’OpenGL à un autre moteur de rendu et inversement
* [Vue 3D][Iray] Les rendus sont souvent flous et pixellisés
* [Bakers] Artefacts lors de l’utilisation de la diffusion sur un GPU AMD
* [Boulangers] La cuisson échoue avec certaines scènes pour les jeux UV autres que 0
* [Boulangers] &#39;Texture transférée&#39; : La liste &#39;UV Set&#39; ne prend pas en compte l&#39;option &#39;Utiliser low as high poly&#39;
* [Bakers] La sélection des tuiles UV est toujours réinitialisée sur &#39;Tous&#39;
* [Graphique] Blocage lors de la suppression d’un nœud en contexte
* [Mac OS][Vue 3D] Résolution de rendu incorrecte sur les écrans mac
* [Paramètres] Les paramètres modifiés ne sont pas stylisés lors du premier affichage
* [UX] Les éléments désactivés dans le menu déroulant sont invisibles

### 15.0.0

*(Publié Le 15 Juillet 2025)*

**Ajouté :**

* [Vue 3D] Nouveau système de rendu, avec modes pixelliseur et traceur de tracé
* [Vue 3D] Ajout d’un outil de sélection pour choisir un objet dans la scène 3D
* [Vue 3D] Ajouter la nouvelle option « Exporter la scène avec les calques... » action dans le menu Scène
* [Vue 3D] Ajouter de nouveaux boutons de barre d’outils
* [Vue 3D] Ajoutez la possibilité de basculer entre plusieurs caméras contenues dans une scène USD
* [Vue 3D] Permet de se concentrer sur l’objet sélectionné en appuyant sur la touche F dans la clôture
* [Vue 3D] Permet de générer un graphique de composition de Substance à partir d&#39;un matériau existant
* [Vue 3D] Permet d’envoyer un graphique de composition SBS dans la vue 3D et d’affecter sa sortie unique à l’utilisation de l’environnement/du panorama
* [Vue 3D] Effacez la sélection actuelle en appuyant sur la touche Échap
* [Vue 3D] Afficher une scène 3D importée avec des textures
* [Vue 3D] Distinguer les commandes de répétition de texture X et Y
* [Vue 3D] Activer/désactiver les ombres
* [Vue 3D] Activer/désactiver le plan au sol
* [Vue 3D] Dans le menu « Matières », ajoutez « Supprimer » uniquement pour la Matière qui a été ajoutée manuellement et qui est inutilisée
* [Vue 3D] Dans le menu « Matières », supprimez l’action « Tout supprimer »
* [Vue 3D] Rendre les fichiers USDZ exportés autonomes
* [Vue 3D] Rendre les propriétés du rendu persistantes lors du changement de mode de rendu
* [Vue 3D] Conserver les entrées de matériau existantes lors du remplacement d’un matériau
* [Vue 3D] Réorganisation des propriétés de la caméra
* [Vue 3D] Supprimer les actions « Camera/Save screenshot... » et « Copier la capture d’écran dans le presse-papiers »
* [Vue 3D] Supprimez l’action de menu « Matière/Tout reconstruire ».
* [Vue 3D] Supprimez le préfixe « Par défaut » de l’étiquette de la caméra par défaut
* [Vue 3D] Définissez l’action de menu « Rétablir la valeur par défaut » comme dernière action dans le menu hamburger de la propriété d’entrée du matériau
* [Vue 3D] Réglages des raccourcis
* [Vue 3D] Prise en charge des ombres et de la translucidité en mode temps réel
* [Vue 3D] Prise en charge des ombrages MaterialX à partir d&#39;une scène USD importée
* [Vue 3D / OpenGL] Renommez le paramètre « Échelle UV activée » en « Activer la Taille physique à partir du graphique ».
* [Vue 3D / Effets postérieurs] Fleur
* [Vue 3D / Effets de post] Profondeur de champ
* [Vue 3D / Effets postérieurs] Mappage de tonalité
* [Vue 3D / Scene Browser] Permet d&#39;afficher les propriétés de la matière lors de sa sélection dans SceneBrowser
* [Vue 3D / Explorateur de scènes] Masquer la colonne « Matière »
* [Vue 3D / Scene Browser] Mettez en gras les primitives USD qui sont contrôlées par une entité prédéfinie
* [Boulangers] Ajoutez un menu contextuel dans l’arborescence avec des actions « Tout sélectionner »/« Tout désélectionner »
* [Bakers] Ajouter une option pour contrôler l’interpolation bitangente
* [Bakers] Ajouter un séparateur horizontal dans l’interface utilisateur graphique
* [Bakers] Ajouter une macro UDIM par défaut dans le nom de la sortie lorsque la scène est udim
* [Bakers] Autoriser à recalculer la tangente
* [Boulangers] Permet de renommer un boulanger sans rompre les liens
* [Boulangers] Modification de la taille par défaut du panneau central
* [Bakers] Texture d’entrée pour le workflow UDIM
* [Bakers] Faire correspondre l&#39;ordre de liste des cartes de vue 2D à l&#39;ordre de liste de rendu des Bakers
* [Boulangers] Rendre la fenêtre de cuisson modale
* [Bakers] Gestion des paramètres de mappage de tonalité
* [Bakers] Supprimer la sélection du plug-in d’espace tangent
* [Boulangers] Statut d&#39;enregistrement « activé » ou « désactivé » pour les Boulangers lors de l&#39;enregistrement d&#39;un Paramètre prédéfini
* [Boulangers] Sélectionner la matière par défaut dans le widget de sélection
* [Bakers] Définir l’orientation par défaut de la texture de sortie normale par rapport aux préférences
* [Bakers] Définir les tuiles UV sur Tout par défaut
* [Bakers] Option d’ajout FromTexture/FromValue dans WordSpaceDirection
* [Bakers] World to tangent : définissez l’entrée par défaut sur « from texture »
* [SBSBaker] Création d’une option pour contrôler l’ordre du back-end
* [SBSBaker] Amélioration de l’utilisation de l’argument StringList
* [SBSBaker] Renommez « match\_source\_instance » en « match\_mesh\_name »
* [SBSBaker] Renommez « Submesh » en « GeomSubset ».
* [SBSBaker] Renommer en substance3d\_baker
* [Contenu] Ajout d’une forme « Hémisphère » aux nœuds de générateur exposant les formes de quadrant
* [Interop] Prise en charge du format de fichier GLTF
* [Interop] Prise en charge du format de fichier PLY
* [Interop] Prise en charge du format de fichier STL
* [Bibliothèque] Uniformisation des info-bulles pour les nœuds atomiques
* [Mac] Ne plus prendre en charge les plates-formes MacIntel
* [Nodes] Ajouter des info-bulles riches pour les nœuds atomiques
* [Paramètres] Fermer la section « Attributs » par défaut
* [Paramètres] Permet à l’utilisateur de spécifier les valeurs par défaut des paramètres de base pour les nouvelles instances
* [Préférences] Boulangers : ajoutez une option booléenne pour calculer l’espace tangent par fragment
* [Préférences] Supprimer les plug-ins d’espace tangent
* [Préférences] Stockez les préférences par version mineure de SD (XX.X).
* [VFX] Mise à jour de Boost vers 1.85.0
* [VFX] Mise à jour de MacOS version minimale vers la version 12.0
* [VFX] Mettre à jour OpenColorIO vers la version 2.4.2
* [VFX] Mettre à jour OpenColorIO vers la version 2.4.x
* [VFX] Mettre à jour OpenExr vers la version 3.3.x
* [VFX] Mise à jour de Qt vers la version 6.5.8

**Fixe :**

* [Vue 3D] Les textures de la scène USD exportée ne sont pas correctement appliquées
* [Vue 3D] [UDIM] Impossible d’afficher les sorties graphiques UDIM dans la vue 3D lorsque l’affichage automatique à l’ouverture du graphique est désactivé dans les préférences de graphique
* [Boulangers] &#39;Anti-alias.&#39; et &#39;Moy. les cellules normales pour les boulangers non applicables sont vides et modifiables
* [Bakers] L’action « Actualiser » utilise le moteur de lancer de rayons lorsqu’elle est désactivée dans les préférences
* [Boulangers] Les boulangers bloqués comme occupés après l&#39;échec lors du processus &#39;Actualiser toutes les maps bakées&#39;
* [Bakers] Blocage à plus de 180 UDIM lors du baking OpenGL Position map sur un maillage spécifique
* [Boulangers] Blocage lors de l’ouverture de la boîte de dialogue « Informations sur le modèle de four » plusieurs fois de suite (macOS uniquement)
* [Boulangers] Dans l’exportation du paramètre prédéfini JSON, la valeur « udim » est remplacée par « 1001 » lorsqu’elle était définie sur « Tout »
* [Bakers] La mémoire n&#39;est pas correctement détectée sous Linux
* [Bakers] La dépendance d’entrée de mappage manquante ne déclenche pas d’avertissement et/ou de rendu de bloc
* [Bakers] Aucun libellé d’erreur lorsque le nom de la sortie est vide
* [Bakers] Le remplacement du filet en poly élevé du fichier n’a aucun effet
* [Boulangers] Le boulanger cible n&#39;est pas sélectionné par défaut lors de l&#39;utilisation de l&#39;action &#39;Rebake&#39;
* [Moteur] Distance : « coupe » visible dans certaines situations
* [Engine] Fx-Map : les couleurs négatives ne sont pas prises en charge lorsque la profondeur de bit est de 8 bits (moteurs GPU uniquement)
* [Localisation] La saisie des caractères revient du japonais au latin dans le menu des nœuds
* [Security] Vulnérabilité d&#39;analyse de fichier USDC hors écriture liée
* [Sécurité] Vulnérabilité II d’écriture hors limites lors de l’analyse du fichier NEF
* [Sécurité] Vulnérabilité de lecture III hors limites lors de l’analyse du fichier DNG
* [Préférences] Problèmes UX dans les paramètres de projet pour les projets en lecture seule
* [Ressources] Les jeux UV multiples ne sont pas affichés lors de l&#39;ouverture des fichiers FBX
* [UI] Libellés qui se chevauchent dans la barre d’état
* [UI] Les info-bulles du menu déroulant « Mode de création de lien » ne sont pas affichées

## Version 14

### 14.1.2

*(Publié Le 15 Avril 2025)*

**Ajouté :**

* [Graphique] Utilisez le moteur GPU par défaut pour générer des vignettes pour le graphique actuel
* [Bibliothèque] Utilisez le moteur GPU par défaut pour générer des vignettes pour la bibliothèque

**Fixe :**

* [Graphique] Impossible de déplacer les connexions dans certains cas en mode de création de lien « Standard »
* [Contenu] Artefacts dans la sortie du filtre MLV dans un cas spécifique
* [Contenu] Atlas splitter/dispersion : seule la première cellule est dessinée correctement (macOS + GPU Engine uniquement)
* [Contenu] Bevel smooth : format absolu 32f
* [Contenu] Fibres 1 : artefacts visuels lors de la conversion en carte normale
* [Contenu] Le rendu de RT AO, Shadows, Bent Normal est incorrect dans certains cas
* [Boulangers] Les éléments de menu avec sous-menus ne laissent pas une marge à droite du texte
* [MacArm][sbsrender] Moteur processeur incorrect lorsque le moteur GPU est introuvable
* [Mac/Linux][sbsrender] Moteur GPU par défaut incorrect

### 14.1.1

*(Publié Le 20 Février 2025)*

**Ajouté :**

* [Graphique] Outils d’alignement des nœuds : rétablir les raccourcis clavier, activer l’empilement par défaut
* [MDL] Avertissez les utilisateurs que les « graphiques MDL » seront obsolètes dans une version ultérieure
* [Préférences] Avertissez les utilisateurs que les « plug-ins d’espace tangent personnalisés » seront obsolètes dans une version ultérieure

**Fixe :**

* [Vue 2D] Afficher les coordonnées des pixels au centre plutôt que dans le coin supérieur gauche
* [Contenu] Niveaux de gris anisotropes de Kuwahara : avertissement du cuiseur pour variable « ignore\_alpha » manquante
* [Contenu] Avertissements relatifs aux cookies dans certains nœuds Usure/salissures
* [Content] Erreurs de cuisson pour le paramètre manquant dans le nœud &#39;Niveaux automatiques&#39;
* [Contenu] Erreurs de cuisson dans la console lors du rendu des vignettes de certains packs
* [Contenu] Edge Notch : avertissement de cuisson dans la console
* [Content] Couleur MLV : Couleur à fond perdu malgré l&#39;utilisation de l&#39;option Pas de mosaïque dans un cas spécifique
* [Contenu] Masquer sur les tracés : dans certains cas, les tracés peuvent être trop nombreux, trop peu nombreux ou avoir une longueur nulle
* [Contenu] Rendu PBR v1 : certains graphiques d’utilité s’affichent dans la bibliothèque
* [Contenu] Dispersion sur la spline : un motif est dessiné même s&#39;il n&#39;y a pas d&#39;entrée de spline
* [Paramètres] Libellé « Valeur fantôme » lors du collage d’un paramètre de liste avec un index non concordant
* [UI] Blocage lors de la fermeture de Designer via l’action « Quitter » dans le dock macOS (macOS uniquement)
* [UI] Les tracés de texture dans les propriétés de l’ombrage ne sont pas recadrés à la largeur du dock

### 14.1.0

*(Publié Le 14 Janvier 2025)*

**Ajouté :**

* [Vue 2D] Ajout d’un affichage en pixels épinglés dans le panneau Informations
* [API] Afficher la taille de la zone des nœuds dans la scène Vue graphique
* [Contenu] « Fusion d’Height de matière » : ajouter une sortie « Masque d’Height »
* [Contenu] &#39;Processeur de sommets de tracé&#39; : utilisez le bouton &#39;Modifier la fonction&#39; pour le paramètre &#39;Fonction par sommet&#39;
* [Contenu] Niveaux automatiques : nettoyage des paramètres inutilisés, ajustement des libellés et de l’info-bulle
* [Contenu] Masquage sur tracés v2
* [Content] Nouvelle moyenne du nœud de moindre écart (MLV)
* [Contenu] Nouveau nœud de filtre médian
* [Contenu] Quantifier la couleur : ajoutez une option de filtrage « Au plus près »
* [Content] Liste des ponts splines : ajout aléatoire de paramètres de décalage de spline
* [Contenu] Outils spline : nouveau nœud spline (quadratique)
* [Contenu] Triangle Grid : modification de la méthode de triangulation et utilisation de boucles
* [Contenu] Nouvelles splines de Dispersion sur le nœud Splines
* [Cooker] Exposer le paramètre de base « Pixel ratio » comme variable statique « $pixelratio »
* [CrashReport] Intégrer une nouvelle fenêtre de rapport d’incident
* [Engine] Ajoutez la version Vulkan/Metal du moteur de fusion
* [Graphique] Mode matière : permet à la connexion d’entrer des données sans utilisation lorsqu’un seul lien est sélectionné
* [Graphique] Lien de matériau : autorise les connexions standard lorsque la connexion n’est pas ambiguë.
* [Graphique] Outils d’alignement des nœuds : ajoutent des distributions horizontales/verticales, des alignements gauche/droite/haut/bas et prennent en charge les nœuds empilés
* [Bibliothèque] Correction de la couleur du texte dans les menus contextuels
* [Paramètres] Copie des paramètres d&#39;un nœud vers un autre
* [Propriétés] « Tout réinitialiser » : Supprimer la fenêtre contextuelle de confirmation
* [Ressources] Définissez le format sur « Tous les formats » dans la boîte de dialogue « Lier Bitmap »
* [Search] Ajouter un moyen d&#39;activer/désactiver un mode récursif
* [Search] Ajouter un moyen d&#39;activer/désactiver la recherche floue
* [Recherche] Toujours afficher et définir le focus sur le champ de terme de recherche lors de l’activation du Finder de nœuds à l’aide de son raccourci clavier
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
* [Content] La déformation spline produit un résultat noir avec le moteur SSE
* Triangle Grid [Contenu] : le motif ne s’affiche pas correctement
* Triangle Grid [Contenu] : la mosaïque est rompue dans un cas spécifique
* [Données] Blocage lors de la modification de l’identifiant d’entrée du graphique dans un cas spécifique
* [Graphique de fonction] Les valeurs longues apparaissent chevauchées sur les nœuds &#39;Float&#39;
* [Fx-Map] Blocage lors de l’affichage des propriétés du nœud de quadrant
* [Graphique] [UDIM] Avoir une barre de défilement dans la liste UDIM donne 1..1 1..2 entrées
* [Graphique][Raccourcis] Le nœud créé à l’aide d’un raccourci n’est pas placé sur le lien existant après la duplication du nœud
* [Propriétés] Affichage incorrect des paramètres lorsque la valeur n’est pas valide
* [Publish] Les dépendances réciproques entraînent une boucle infinie lors de la publication d’un pack
* [Publish] Échec silencieux lors de l’utilisation de l’action « Publish » sur un pack avec une dépendance déchargée
* [UI] Le widget « Taille du gabarit » ne s’affiche pas correctement lorsqu’il est développé et peut bloquer l’interface (macOS uniquement)
* [UI] Dans certains cas, la fenêtre principale se trouve derrière d’autres applications (Windows uniquement)

### 14.0.2

*(Publié Le 10 Octobre 2024)*

<b>Ajouté :</b>

* [Graphique de fonction] Améliorer l’alignement du texte au sein des nœuds
* [MacOS] Réautoriser l’installation sur la version Big Sur (11.0)
* [Windows] Réautoriser l’installation sur Windows 10 19H2

<b>Fixe :</b>

* [Bitmap] Les tracés de peinture sur la ressource bitmap ne marquent pas le package hôte comme étant modifié
* [Graphique de fonction] Blocage lors de la fermeture d’un pack avec un graphique de fonction hébergeant un nœud d’instance
* [Graphique de fonction] Blocage lors de l’annulation de deux ajustements de nœud Sample Color sur une ligne

### 14.0.1

*(Publié Le 24 Septembre 2024)*

<b>Ajouté :</b>

* [Moteur] Mise à jour vers la Substance Engine 9.1.4
* [Contenu] Triangle Grid : modification de la méthode de triangulation et utilisation de boucles

<b>Fixe :</b>

* [API] Impossible de charger à nouveau les plug-ins déchargés
* [Contenu] Histogramme Calculer : le résultat est 16 fois supérieur à ce qu’il devrait être
* Triangle Grid [Contenu] : le motif ne s’affiche pas correctement
* [Données] Blocage lors de la modification de l’identifiant d’entrée du graphique dans un cas spécifique
* [Moteur] Le nœud Distance produit des artefacts lors de l’utilisation de tailles de pixels très faibles
* [Engine] Résultat de nœud de distance incorrect à une résolution de 8K sur le moteur SSE2
* [Graphique de fonction] Les valeurs longues apparaissent chevauchées sur les nœuds &#39;Float&#39;
* [Graphique][Raccourcis] Le nœud créé à l’aide d’un raccourci n’est pas placé sur le lien existant après la duplication du nœud
* [Propriétés] Affichage incorrect des paramètres lorsque la valeur n’est pas valide

### 14.0.0

*(Publié Le 30 Juillet 2024)*

<b>Ajouté :</b>

* [Contenu] Nouveau filtre Kuwahara anisotrope
* [Contenu] Nouveau nœud de Bevel smooth
* [Contenu] Nouveau nœud v2 Courbure lisse
* [Contenu] Nouveau nœud de Directional distance
* [Contenu] Nouveaux outils d’histogramme : calcul, égalisation, rendu
* [Contenu] Nouvel ID vers le nœud de masque
* [Content] Nouveau nœud de décombinaison normal
* [Contenu] Nouveaux nœuds de palette : Créer, Appliquer, Modifier, Afficher
* [Contenu] Nouveau nœud Quantize Color
* [Contenu] Déformation directionnelle non uniforme : définissez la valeur par défaut de la courbe d’intensité sur 1
* [Contenu] Ajoutez le suffixe « Color » ou « Grayscale » à tous les libellés de nœuds qui ont ces versions
* [Contenu] La désactivation de l’option « Bruit blanc » ne permet de conserver que « Bruit blanc rapide »
* [Content] Nœud « Negate Float1 » obsolète dans le graphique de fonction de Substance
* [Contenu] Renommez « Quantize Color » en « Quantize Color (Simple) ».
* [Vue 2D] Valeurs d’affichage dans le panneau Informations pour les pixels en dehors de la plage 0-1
* [Moteur][Texte] Nouveau crénage pour certaines polices
* [Graphique] Amélioration du temps d’invalidation lors de l’édition de sous-graphes profonds lors de l’utilisation de l’édition contextuelle
* [Linker] Ne pas dupliquer les bitmaps dans SBSASM
* [Paramètres] Ajout d’un nouveau widget « fonction » pour tous les types de paramètres d’entrée
* [Propriétés] Amélioration de l’affichage des paramètres hérités
* [UX] Amélioration de la prise en charge du pavé tactile (Mac uniquement)
* [UX] Moderniser le panoramique lorsque vous atteignez la bordure du graphique lors de la sélection
* [UX] Supprimer la fonctionnalité « Désactiver la haute résolution »
* [Branding] Nouveau branding pour l&#39;écran de démarrage et la fenêtre À propos
* [Courbe de transfert de dégradé] Ajout d’un moyen de déplacer toutes les touches et de créer une boucle
* [Bibliothèque] Basculer tous les filtres par défaut en casse de phrase
* [API] Méthode Add pour cadrer un nœud spécifique dans la fenêtre Vue graphique
* [API] Ajout d’une méthode pour ouvrir un package dans son éditeur (par exemple, un graphique de Substance dans la vue Graphique)
* [API] Ajout d’une méthode pour sélectionner une ressource de package dans l’Explorateur (par exemple, un graphique de Substance)
* [API] Ajout de méthodes pour obtenir et définir le type de graphique d’un graphique de composition de Substances
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2023
* [Tiers] Suivez les recommandations sur les plateformes d’effets spéciaux pour 2024
* [Tiers] Mettre à jour Boost à 1.82.0 + USD à 23.08
* [Tiers] Mise à jour NGL vers 1.38
* [ThirdParty] Mettre à jour OpenColorIO vers la version 2.3.x
* [Tiers] Mise à jour d’OpenExr vers la version 3.2.x
* [ThirdParty] Mettre à jour OpenSubdiv vers la version 3.6.x
* [ThirdParty] Mettre à jour Python vers 3.11.x
* [Tiers] Mise à jour de Qt vers la version 6.5.x
* [ThirdParty] Mettre à jour gcc vers la version 11.2.1
* [ThirdParty] Mettre à jour glibc vers 2.28
* [Tiers] Mettez à jour libstdc++ ABI vers C++11 one
* [Documentation] Nouvelle page Glossaire

<b>Fixe :</b>

* [Boulangers] Blocage lors de la modification du nom de fichier d’une scène
* [Boulangers] Blocage lors de l’enregistrement du paramètre prédéfini boulangers dans le fichier JSON
* [Content] &#39;Dispersion sur la spline&#39; : Exposer le paramètre alpha de l&#39;image d&#39;entrée
* [Contenu] « Couleur Sampler de la vignette » : expression visible manquante
* [Contenu] Bruit anisotrope : une valeur négative pour la quantité X/Y produit un résultat erroné
* [Contenu] Bruit anisotrope : problème de mosaïque lors de l’utilisation de valeurs impaires comme quantité X et sans smoothness
* [Contenu] Fonction de distribution normale : max() mal placé peut conduire à NaN
* [Content] Les ombres RTAO, Bent Normal et RT ne fonctionnent pas correctement sur certaines plateformes
* [Contenu] Couleur de fusion des éclaboussures de forme : les cartes normales OpenGL ne sont pas fusionnées correctement
* [Contenu] Espace non garanti après le préfixe « Multi » dans les étiquettes de nœuds
* [Dépendances] Blocage lors du déplacement d’un graphique au sein d’un ou entre plusieurs packages
* [Moteur] Erreur de précision dans les nœuds de déformation affectant les nœuds de flou de Pente
* [Moteur] Le calque SBSAR dans SD ne peut pas lire SBSAR avec le contenu SBSASM > 2 Go
* [Graphique de fonction] Résultat incorrect pour 0^n
* [Graphique] L’option « Afficher la taille du nœud » est mal étiquetée
* [Graphique] Blocage lors de la copie d’un commentaire parent vers un autre graphique
* [Graphique] Blocage lorsque vous faites glisser un nœud Point tout en maintenant la touche Alt enfoncée
* [Graph] La recherche de nœud peut manquer des correspondances évidentes dans certains cas
* [Graphique] Problème de performances lors de l’édition d’un graphique de fonction instancié plusieurs fois avec un supergraphe ouvert
* [Graphique] Trop d’invalidations lors de la création d’une sortie
* [Security] Vulnérabilité d&#39;écriture hors limites d&#39;analyse ICO
* [Sécurité] Certains formats d’image inutilisés sont obsolètes
* [Paramètres] Le chemin de la ressource Bitmap PKG ne doit pas être modifiable
* [Paramètres] Correction des problèmes liés à l’exposition/l’exposition par lots du paramètre d’un processeur de valeurs
* [Paramètres] Les paramètres de chaîne sont ignorés lors de l’exposition par lots
* [Propriétés] Problème de performances lors de la modification d’un graphique de fonction instancié plusieurs fois avec les propriétés ouvertes
* [SVG] Les modifications apportées aux formes ne sont pas appliquées à l’image pixellisée
* [UI] Correction de certains bugs/incohérences avec les widgets défilants (Windows uniquement)
* [UI] Ordre incohérent des formats de fichiers de scène 3D dans les listes d’importation/exportation
* [UI] Les actions de la fenêtre sont dupliquées dans l’interface utilisateur
* [Version Control] Le script &#39;perforce.py&#39; ne fonctionne pas sur Python 3

## Version 13

### 13.1.2

*(Publié Le 16 Avril 2024)*

<b>Ajouté :</b>

* [Graphique] Ne placez pas de nœuds dupliqués au-dessus du nœud d’origine
* [Graphique] Améliorer l’alignement des commentaires joints aux nœuds
* [Graphique] Améliorer le déplacement des commentaires
* [Graphique] Ancrage des images et des commentaires collés/dupliqués à la grille
* [Images] Accrocher les nouvelles images et les nouveaux commentaires à la grille
* [Contenu] « Courbure lisse » : ajoutez une note sur la prise en charge des mosaïques dans la description
* [3DView][IRay] Autoriser l&#39;affectation de la sortie int au paramètre enum
* [AxF] Ajout de propriétés concernant le modèle de pelage transparent
* [AxF] Amélioration de la gestion des erreurs lors de l’exportation
* [AxF] Amélioration des matériaux GLSLFX et MDL pour la représentation « SVBRDF » telle que stockée dans un fichier AXF
* [AxF] Supprimer la propriété « CC No Refraction » du modèle « AxF vers AxF »
* [AxF] Renommez les propriétés « properties.has\_xxx » en « properties.has\_xxx ».
* [AxF] Mettez à jour le modèle pour inclure toutes les propriétés utilisées par nos shaders SVBRDF.

<b>Fixe :</b>

* [Vue 3D] Blocage lors de la réinitialisation d’un paramètre MDL Int mappé à une énumération MDL
* [Vue 3D] Widgets incorrects pour les propriétés de l’ombrage SVBRDF lorsque le matériau est réinitialisé après avoir modifié la scène 3D
* [Vue 3D] Widgets incorrects pour les propriétés du nuanceur SVBRDF lorsqu’aucun graphique n’est appliqué
* [Vue 3D] Le bouton Afficher l’environnement est désactivé pour les nouvelles vues sans fichier SBSSCN par défaut
* [Vue 3D] Le passage d’un moteur de rendu Iray à OpenGL déconnecte une sortie graphique
* [AxF] La variante Fresnel n&#39;est pas mise à jour par la sortie graphique
* [AxF] Le format des libellés des propriétés de nuanceur AxF est incohérent
* [AxF] Les avertissements relatifs aux ressources inchangées n’apparaissent que dans la console
* [Contenu] « Non uniforme » n’est pas écrit de manière cohérente dans tous les nœuds.
* [Contenu] Dispersion sur la spline : motifs manquants sur les splines de pont
* [Contenu] Mappeur de splines : se bloque lors de la définition d’une valeur négative « Quantité de segment »
* [Contenu] « Symétrie » : les libellés sont manquants et incohérents
* [Graphique] Les commentaires existants sont légèrement décalés
* [Security] Vulnérabilité de lecture hors limites d&#39;analyse de fichier RAS

### 13.1.1

*(Publié Le 8 Février 2024)*

<b>Ajouté :</b>

* [AxF] Ajout de propriétés booléennes hasClearCoat, hasSheen, etc.
* [AxF] Ajout de propriétés manquantes
* [AxF] Autoriser l’importation de fichiers EP-SVBRDF
* [AxF] Renommer les propriétés « anisotropic », « fresnel » et « fresnel variant »
* [AxF] Mise à jour vers AxF-Editing 1.0.0
* [Graphique] Coller en position de la souris si elle se trouve dans la vue Graphique
* [UX] Augmenter l&#39;height du champ de texte « Description » de Frame and Comment
* [UX] Mise en évidence des champs d’édition de texte lors de la création de blocs, de commentaires ou d’épingles

<b>Fixe :</b>

* [AxF] Les valeurs de mappage « Couleur Specular » sont incorrectes lors de l’exportation.
* [AxF] L’aperçu et les textures ne s’affichent pas correctement dans la boîte de dialogue « Importer AxF »
* [AxF] La propriété « CC No Refraction » n&#39;est pas injectée correctement dans le modèle « AxF to AxF »
* [Contenu] « Flood Fill à la position » est absent de la bibliothèque
* [Contenu] &#39;Splatter Circular&#39; : les valeurs négatives de &#39;Pattern Amount&#39; entraînent des calculs très longs et intensifs
* [Contenu] &#39;Liste de fusion spline&#39; : ordre d&#39;entrée incorrect
* [Dépendances] La dépendance est remappée sur sa copie après avoir été enregistrée en tant que copie
* [Images] Le bouton « Activer le balisage de HTML » ne bascule pas lorsque vous annulez son utilisation
* [Images] La sélection d’une image et de son contenu à l’aide de l’outil Rectangle de sélection entraîne le déplacement de l’ensemble du contenu de l’image lors de la décomposition automatique
* [Graphique] Les commentaires dupliqués à partir de commentaires parents sont toujours placés à l’origine du graphique.
* [Graphique] Le saut de ligne dans Commentaire est plus dur à la création
* [Publish] Définir le chemin par défaut pour la publication SBSAR sur le dossier « Mes documents »
* [SBSAR] Le rétablissement de la charge SBSAR la rend modifiable et ses données peuvent être perdues

### 13.1.0

*(Publié Le 12 Décembre 2023)*

<b>Ajouté :</b>

* [Images] Développement automatique
* [Cadres] Modification des règles pour définir à quel moment un objet appartient à un cadre
* [Cadres] Désactiver la mise à l’échelle du texte pour la description des cadres
* [Images] Taille adaptée au contenu
* [Images] Nouveaux états par défaut, survol et sélectionné
* [Cadres] Magnétisme de la grande grille
* [Images] Prise en charge du code de HTML pour la description des images
* [Images] Mise à jour des zones d’interaction
* [Images] Mise à jour de l’aspect visuel
* [Graphique] Créer le nœud au milieu du lien visible au lieu du milieu du lien
* [Graphique] Affiche les propriétés d’un élément s’il est le seul élément avec des propriétés disponibles dans une sélection
* [Graphique] Supprimer l’option « Mise à l’échelle » pour les commentaires dans le graphique
* [Graphique] Accrocher les nœuds sur la grille principale lors du copier/coller
* [UX] Autoriser la recherche floue dans le menu Nœud et la recherche dans la bibliothèque
* [UX] Effectuer une boucle dans la liste du menu Nœud
* [AxF] Prise en charge de l’exportation AxF
* [AxF] Désactiver AxF sous Linux
* [API] Définissez la propriété « Visible if » des paramètres, entrées et sorties du graphique à l’aide de l’API Python
* [API] Définition de l’ordre des E/S de graphiques à l’aide de l’API Python
* [Dépendances] Mettre à jour Boost vers 1.80.0
* [Dépendances] Mettre à jour OpenSubdiv vers la version 3.5.x
* [Dépendances] Mise à jour gcc vers la version 11.2.1 - Problème Iray/MDL C++20
* [Dépendances] Mise à jour du SDK FBX vers 2020.3
* [Dépendances] Mettre à jour NGL vers 1.35.0.20
* [Gestion des couleurs] Prise en charge supplémentaire des écrans ICC OCIO
* [Levels] Ajouter un moyen de réinitialiser l&#39;histogramme
* [Python] Avertir les utilisateurs si QtForPython ne peut pas être importé
* [Vue 2D] Enregistrer l&#39;état des options d&#39;affichage
* [Vue 3D] Ajout d’une technique de positionnement au nuanceur d’informations de maillage
* [Exporter] Ajoutez un bouton « Enregistrer les paramètres » pour enregistrer les modifications apportées aux options d’exportation.

<b>Fixe :</b>

* [Vue 3D] Impossible d&#39;attribuer une texture à une entrée de type texture\_2d d&#39;un matériau MDL
* [AxF] Les identificateurs de graphique dans la liste des modèles peuvent être vides
* [AxF] Le champ de modèle de graphique de Substance est vide par défaut
* atlas scatter [Contenu] : comportement incorrect dans des cas spécifiques
* [Contenu] Mappeur de Flood Fill : sortie vide lorsque toutes les formes ont la même taille de boîte de dialogue
* [Content] FloodFill à la position : artefacts d’imprécision dans certaines situations
* [Contenu] Sortie « Specular » incorrecte dans le nœud « Convertisseur couleur de base/métallique/rugosité »
* [Contenu] L’option Masquer sur tracé ne fonctionne pas à la verticale
* [Contenu] Description manquante pour les nœuds Valeur d’entrée, Niveaux de gris en entrée, Couleur d’entrée et Sortie
* [Contenu] Description manquante pour les nœuds Set et Sequence
* [Contenu] Éclaboussure de forme : artefacts d’imprécision dans la sortie « Splatter data 2 »
* [Moteur] Les valeurs booléennes dans les processeurs de traitement des valeurs sont toujours évaluées sur « False » (Apple Silicon uniquement)
* [Explorer] L’ordre des boutons de la barre d’outils est incohérent entre les systèmes d’exploitation
* [Images] N’accrochez pas les nœuds lorsque vous déplacez une image avec le modificateur CTRL
* [Courbe de transfert de dégradé] réinitialiser tout doit également réinitialiser le widget de dégradé
* [GraphRender] Certains nœuds deviennent noirs lors de l’ajustement en mode aperçu
* [Graphique] L’aperçu de « Valeur d’entrée » est bloqué sur « Faux » lors de l’ajustement de la valeur booléenne par défaut (Apple Silicon uniquement)
* [Graphique] Les nœuds de point proches du bord de l’image ne sont pas déplacés par l’image
* [Interopérabilité] L’icône Renvoyer n’est pas mise à jour après l’envoi à Substance 3D Stager
* [MDL] Impossible de modifier la rugosité dans les nœuds où ce paramètre est disponible
* [MDL] Connexions non valides dans le modèle « AxF to Metallic Roughness »
* [UI] La fenêtre « Exporter les sorties » peut être réduite (Windows uniquement)
* [UI] Les images apparaissent pixellisées dans l’écran À propos lors de l’utilisation de la mise à l’échelle de l’affichage
* [UI] Les outils d’alignement de nœud de la barre d’outils graphique créent plusieurs étapes d’annulation.

### 13.0.2

*(Publié Le 27 Juillet 2023)*

<b>Ajouté :</b>

* [Graphique de fonction] Ajouter une variable système $getPhysicalSize
* [Écran d’accueil] Prise en charge de l’ouverture des fichiers SBS par glisser-déposer
* [Content] Mappeur de spline/Mappeur de flux de spline : ajout d’un paramètre de correction non carrée

<b>Fixe :</b>

* [Écran d’accueil] Ne pas afficher l’écran d’accueil lorsqu’un fichier est envoyé à partir d’un autre logiciel
* [Écran d’accueil] État incorrect de l’icône Designer dans la barre d’outils Windows
* atlas splitter de [Content] : description incorrecte
* [Contenu] Valeur de référence incorrecte dans la fonction &#39;Linéaire à sRVB (luminance)&#39;
* [Contenu] L’outil d’affichage des nombres ne prend pas en charge les résolutions non carrées
* [Contenu] Liste de points : la valeur minimale du paramètre « Numéro de point » est incorrecte
* [Contenu] Ombre portée de la forme : l’ombre peut disparaître lorsque la mosaïque est désactivée
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
* [Blocage][Cooker] Blocage lors du chargement de graphiques spécifiques
* [Blocage][UI] Blocage lors de l’activation des menus après le chargement du package depuis l’écran d’accueil
* Le lien [API] « Documentation de l’utilisateur » dans la référence des scripts est obsolète
* [Propriétés] Impossible d’ouvrir la fonction de processeur de valeurs sur un graphique verrouillé
* [Publish] Impossible de publier des packages contenant des graphiques MDL
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
* [Contenu] Quad Transform on Path : les valeurs par défaut p01 et p10 sont permutées
* [Contenu] Quad Transform : résultat incorrect dans une situation spécifique
* [Contenu] Cercle spline : le résultat « Inverser la direction » est incorrect lorsque la distribution uniforme n’est pas utilisée
* [Contenu] Cercle spline : les tangentes sont incorrectes lors du réglage des paramètres de taille et de spirale
* [Contenu] Spline Flow Mapper : des traînées noires apparaissent lorsque la puissance en spirale est élevée dans Spline Circle
* [Contenu] Spline Mapper / UV Mapper : la couleur d’arrière-plan ne fonctionne pas
* [Contenu] Spline Mapper : l’height de base est 0, ce qui entraîne un écrêtage
* [Content] Mappeur de spline : l&#39;height de la spline est modifié par le multiplicateur d&#39;entrée même lorsque cette entrée n&#39;est pas connectée
* [Content] Mappeur de splines : les extrémités de splines qui rencontrent un bord d&#39;image ne sont pas mappées
* [Contenu] Mappeur de spline : l’Échelle UV Y n’a aucun effet lors de l’utilisation d’une forme non plane
* [Content] Mappeur de splines : combat contre les Z lors du rendu de splines se chevauchant du même height
* [Contenu] Poly quadratique spline : le résultat « Inverser la direction » est incorrect lorsque la distribution uniforme n’est pas utilisée
* [Contenu] Rendu spline : les liaisons ne sont pas gérées de manière cohérente dans les options de style de spline
* [Contenu] Rendu spline : le dernier segment n’est pas dessiné
* [Contenu] Rendu spline : correction non carrée non appliquée correctement
* [Contenu] La couleur du mappeur UV apparaît deux fois dans la bibliothèque
* [DotNode] La zone d&#39;ancrage de connexion n&#39;est pas mise à jour après la désactivation de la limite de mise à l&#39;échelle du texte
* [DotNode] La création via le menu contextuel est interrompue
* [DotNode] La position du nom de portail d&#39;entrée n&#39;est pas ajustée après l&#39;annulation/la répétition d&#39;un changement de nom
* [GraphRender] Trop d’invalidations lors de la modification d’un graphique de fonction
* [Graphique] La position du widget de transformation n’est pas mise à jour visuellement correctement
* [Localisation] Les valeurs « Plage souple » et « Plage dure » ne sont pas localisées dans les graphiques MDL
* [Paramètres] Les modifications de texte consécutives ne sont pas enregistrées dans la pile d’historique
* [Paramètres] La boîte de dialogue permettant de déplacer les paramètres d’entrée du graphique dans la liste n’est pas fiable
* [Propriétés] Le clic simple est considéré comme double sur le widget de zone de rotation pour les projets lourds
* [Publish] L’ordre des ressources dans le package n’est pas conservé dans la ressource publiée

### 13.0.0

*(Publié Le 6 Juin 2023)*

<b>Ajouté :</b>

* [Graph] Nœud du portail
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
* [Content] Nœud de transformation 2D spline
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
* [Contenu] Nœud de couleur du mappeur UV
* [Contenu] Nœud Niveaux de gris du mappeur UV
* [Contenu] Nœud Tracés vers splines
* [Contenu] Nœud Masques vers tracés
* [Contenu] Tracés 2D Transform nodenode
* [Contenu] Tracés Nœud Polygone
* [Contenu] Nœud Chemins d’accès d’aperçu
* [Contenu] Nœud Déformation des tracés
* [Contenu] Nœud de sélection des tracés
* [Content] Nœud Processeur de sommets de tracés
* [Contenu] Processeur de sommets de tracés Nœud simple
* [Contenu] Quad Transform sur le nœud de chemin
* [Contenu] Occlusion ambiante avec lancer de rayon v2
* [Contenu] Courbure Lancer De Rayon Normal v2
* [Contenu] Ombres vectorisées avec rayon v2
* [Moteur] Mise à jour vers la version 9
* [Moteur] Nœud de boucle dans les graphiques de fonction
* [Moteur] Ajouter le mode solide au dégradé
* [Moteur] Nœud Pow() atomique dans le graphique de fonctions
* [Moteur] Ajout d’options d’habillage de bordure (serrage sur le bord/répétition) dans le nœud Sampler
* [Moteur] Échantillonnage le plus proche dans le nœud Déformation et Déformation directionnelle
* [Moteur] Ajout d’un mode « alpha pénétrant » au filtre Netteté pour les entrées de couleur
* [Engine] FxMap : morphlet de l&#39;hémisphère
* [Engine] Opérations Get/Set atomiques dans les graphiques de fonction
* [Moteur] Fonctions : utiliser la fonction précise de log/log2/exp, 2pow - Unifier les fonctions entre le cuiseur et le moteur
* [Moteur] Ajoutez un paramètre « décalage d’intensité » au filtre Déformation directionnelle
* [API] Prise en charge de la gestion des paramètres prédéfinis pour la composition de graphiques
* [Fonctions] Modification du nom d&#39;entrée des fonctions nœuds atomiques
* [Localisation] Ajouter Portugais (Brésil), Italien (Italie) et Espagnol (Espagne)
* [Localisation] Respectez la règle « Langue (Pays) » dans la liste des langues
* [Paramètres prédéfinis] Désactiver les panneaux « Aperçu » et « Paramètres prédéfinis » dans les propriétés du graphique lors de l’utilisation de l’édition contextuelle
* [Graphique des modèles de Substance] Fin de la prise en charge des graphiques des modèles de Substance

<b>Fixe :</b>

* [Vue 3D] L’affichage des chaînes longues dans les statistiques de scène est coupé (macOS uniquement)
* Le module [API] &#39;structure::Structure&#39; est toujours inclus dans la référence API
* [API] Les nœuds de point dans les graphiques MDL n&#39;ont aucune définition ni propriété
* [API] Comportement incorrect lors de la définition du paramètre des nœuds de fonction
* [Contenu] 3D Voronoi et 3D voronoi fractal nodes génèrent un avertissement de cuisson
* [Moteur] Le paramètre « Décalage de la carte d’intensité » n’a aucun effet sur les données en niveaux de gris dans le moteur SSE2
* [Explorer] L’e/s du graphique peut être supprimée
* [Graphique] Le bitmap est ignoré lorsqu’il est utilisé dans des instances
* [Graphique] Position de nœud de point incorrecte lors de la création d&#39;un nœud à partir d&#39;un nœud
* [Graphique] Focus incorrect dans la boîte de dialogue « Exposer le paramètre » lors de l’utilisation de la touche « Entrée »
* [Graphique] Résultat incorrect dans la numérisation d’histogramme avec un bitmap dans l’édition du contexte
* [Localisation] Correction de divers problèmes d’écrêtage
* [Paramètres] Blocage lors de la suppression d’un paramètre d’entrée
* [Publish] Les graphiques dans les dossiers sont déplacés à la racine dans le package publié
* [Ressources] Blocage lors de la mise à jour d’une ressource chargée sur le disque
* [VisibleIf] Correction de la régression dans l’évaluation de la visibilité conditionnelle

## Version 12

### 12.4.1

*(Publié Le 30 Mars 2023)*

**Ajouté :**

* [Cooker][Graph] Prendre en compte les balises de transformation EXIF dans le fichier JPEG
* [Sécurité] Mise à niveau vers 23,02 USD
* [Sécurité] Supprimer la prise en charge de l’importation de format de fichier Collada (.dae)
* [Modèles de Substance] Avertissement concernant la fin de vie des graphiques de modèles de Substance dans la prochaine version majeure

**Fixe :**

* [Vue 3D][ASM] Artefact de rugosité de revêtement lors de l’utilisation d’une CoatNormal
* [Contenu] Le paramètre « Cellules avec dégradé » du nœud Alveolus est inversé
* [Contenu] Le nombre d&#39;entrées des nœuds à commutateurs multiples n&#39;est pas verrouillé
* [Contenu] Avertissement de cuisson dans le nœud Normal de Scratches Generator
* [Données] Blocage lors du chargement manuel du package après l’annulation de son chargement précédent
* [Données] Blocage lors de l’annulation rapide de plusieurs opérations de graphique jusqu’au chargement du package

### 12.4.0

*(Publié Le 31 Janvier 2023)*

**Ajouté :**

* [Vue 3D] Ajouter toutes les options dans le menu Afficher sous forme de boutons de barre d’outils
* [API] Autoriser l’ajout d’actions aux barres d’outils d’affichage des graphiques
* [API] Autoriser la création/modification/évaluation d’un graphique de modèle de Substance à partir de l’API
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D cuites en mode ACE
* [Documentation] Exemples de projets pour les graphiques de composition de Substances
* [Documentation] Exemple de projet pour les graphiques de fonction
* [Explorer] Autoriser le déplacement du graphique et des ressources d’un parent à un autre sans fermer ni invalider les widgets
* [Éditeur de dégradé] Sélectionner l’épingle sur laquelle vous avez cliqué lors de l’affichage de l’éditeur de dégradé
* [Graphique] Ajouter une option dans le menu contextuel d’un nœud pour sélectionner tous ses enfants
* [Graphique] Nettoyer l’outil de graphique pour détecter et supprimer les nœuds inutilisés dans tous les types de graphiques et graphiques de propriétés
* [Graphique] Transformation de l’entrée d’image en couleur/niveaux de gris
* [Paramètres] Ajouter un verrou sur les widgets integer2
* [Paramètres] Permet de saisir des formules de base comme paramètre
* [Substance] Basculez entre les valeurs et les icônes pour les nœuds de valeur.
* [UI] Bouton permettant de générer une valeur aléatoire lorsqu’un générateur aléatoire est requis
* [UI] L’élément ciblé n’est pas mis en surbrillance dans le navigateur de scènes
* [UX] Réinitialiser les plages de curseur lorsque leur valeur est réinitialisée

**Fixe :**

* [API] SDProperty.getDefaultValue() renvoie presque toujours None
* [Vue 3D] La valeur de la propriété « DirectX normal » n’est pas partagée entre les moteurs de rendu
* [Vue 3D] L’affichage des statistiques de scène est étiré lorsque la fenêtre est petite
* [Vue 3D] La propriété d&#39;affichage Structure filaire n&#39;est pas enregistrée
* [Contenu] Les paramètres Couleur de flou radial n’ont aucun effet sur la couche alpha
* [Localisation] Des curseurs et des boutons supplémentaires s’affichent dans les propriétés OpenGL de l’environnement.
* [MDL][Substance de données] Blocage lors de la suppression de nœuds exposés
* [Préférences] Le fichier par défaut\_config n’est jamais recréé s’il est supprimé
* [modèle de Substance] Paramètre de réorganisation de blocage qui n&#39;apparaît pas au niveau de l&#39;instance

### 12.3.1

*(Publié Le 24 Novembre 2022)*

**Ajouté :**

* [3DView] Rendu optimisé pour les scènes avec de nombreux matériaux
* [3DView] Affichage des sorties d’un graphique de Substance de données en le déposant de l’Explorateur
* [Licence] Système hérité propre pour les utilisateurs de Linux
* [Intégration] Mettre à jour la transparence de l’arrière-plan
* [Modèles de Substance] Avertissement d’affichage dans la vue Graphique lorsque l’entrée et la sortie partagent le même identifiant

**Fixe :**

* [Ressources 3D] « Aide > Ressources Substance 3D » cible par erreur le bureau Creative Cloud sous Linux
* [Vue 3D] Les matières ne sont pas créées lorsque le filet est chargé
* [Vue 3D] La liste Matières s’ouvre lors de la dépose du graphique du modèle de Substance dans la clôture
* [Explorer] Impossible de supprimer la sélection avec le clavier si un graphique de Substance est inclus
* [Explorer] Blocage lors de l’ouverture du menu contextuel de l’élément de matériau d’une ressource de maillage dans Mac
* [Graphique] Les instances dont les images d’entrée dépendent de valeurs génèrent un résultat incorrect dans les nœuds suivants
* [Graphique] Résultat incorrect lors de l’utilisation de la chaîne de sous-graphes avec l’édition de graphique contextuelle activée
* [MDL] Blocage lors du chargement d’un graphique MDL référençant un graphique de composition avec des sorties obsolètes
* [MDL] Le nœud 2D de texture ne fonctionne plus
* [Intégration] Texte recadré et non localisé
* [Intégration] Les panneaux ne s’affichent pas correctement lors du lancement de l’application via l’ouverture d’un fichier
* [Préférences] Le cache d’image ignore l’emplacement des fichiers temporaires défini par l’utilisateur
* [Propriétés] Les réglages effectués dans les panneaux Aperçu/Paramètres prédéfinis sont fusionnés dans la pile des annulations
* [Raccourci] Le raccourci attribué sur des nœuds obsolètes crée des conflits et ne peut pas être nettoyé
* [Modèles de Substance] Blocage lors de la fermeture d’un pack après avoir effectué des actions spécifiques
* [Modèles de Substance de données] Les nœuds d’instance et les liens des packages déplacés ne sont pas actualisés correctement
* [Modèles de Substance de données] L’annulation de la suppression des sous-graphes n’actualise pas les nœuds et les liens d’instance de manière cohérente
* [Modèles de Substance] La valeur augmente soudainement trop vite sur le nœud de transformation
* [UI] Les icônes d’avertissement de la propriété « Visible si » n’ont pas d’info-bulle
* [UI] Le texte des informations de l&#39;image est trop sombre dans la fenêtre d&#39;affichage de la vue 2D
* [Annuler] Le déplacement d’un widget de position en mode aperçu stocke toutes les valeurs intermédiaires

### 12.3.0

*(Publié Le 6 Octobre 2022)*

**Ajouté :**

* [Général] Panneau d’intégration pour accueillir les nouveaux utilisateurs
* [Général] Panneau Nouveautés pour améliorer la découvrabilité des nouvelles fonctionnalités
* [Modèle de Substance] Prise en charge des sous-graphes et des instances
* [Modèle de Substance] Prise en charge Visible Si pour les paramètres exposés
* [Modèle de Substance] Ajout de la prise en charge des nœuds de sortie
* [modèle de Substance] Nœud de décalage de courbe
* [modèle de Substance] Nœud de retournement de courbe
* [modèle de Substance] Nœud de lissage de courbe
* [modèle de Substance] Nœud de subdivision de courbe
* [modèle de Substance] Nœud de greffe
* [Substance model] Mettre à jour le nœud « Filter Scene »
* [Modèle de Substance] Rendre les nœuds non atomiques détectables dans le menu Nœud
* [Substance de données] Ajoutez l&#39;action « Ouvrir la référence » dans le menu contextuel d&#39;un nœud d&#39;instance
* [Modèle de Substance] Ajoutez une action « Afficher dans 3DView » dans le menu contextuel des nœuds pouvant être envoyés à 3DView
* [Modèle de Substance] Affiche automatiquement les propriétés d&#39;un nœud après l&#39;avoir exposé
* [Modèle de Substance] Création d’une fenêtre « Nouveau graphique de modèle de Substance » avec la liste des modèles
* [UI] Amélioration de la cohérence des options d’enregistrement d’image dans les vues 2D et 3D
* [UI] Renommez « Lien > Filet 3D » en « Lien > Scène 3D » dans le menu contextuel de l’Explorateur
* [UI] La réinitialisation de la disposition s’applique désormais à toutes les fenêtres flottantes
* [UI] Utiliser le libellé « Afficher les sorties en vue 3D » dans les menus contextuels des graphiques
* [Library] Prise en charge des graphiques de modèles de Substance non atomiques
* [SBSAR] Prise en charge de la description des sorties graphiques dans le SBSAR
* [Shader] Définissez la valeur par défaut Facteur de facettisation sur 1 pour tous les shaders
* [UI] Exposer le widget à 2 boutons pour les paramètres booléens
* [Engine] Mise à jour vers la version 8.6.4
* [Steam] Version optimisée pour le chipset Apple Silicon (Apple M1/M2)

**Fixe :**

* [UI] Résolution des problèmes de mise à l’échelle des écrans haute résolution
* [UI] Modèle &#39;$(udim)&#39; manquant dans la liste de la fenêtre de restauration
* [UI] Blocage lors de l’affichage du menu Nœud sur la bordure droite de l’écran (macOS uniquement)
* [UI] Le bouton Extension dans le menu de la vue 3D n’est pas visible
* [UI] Le menu d&#39;extension de la barre d&#39;outils Graphique est incomplet
* [UI] Valeur de widget de paramètre incorrecte après l’annulation de l’activation de la plage fixe
* [Vue 3D] Le paramètre de nuanceur non par défaut est perdu sur Iray d’une session à une autre
* [Boulangers] Blocage lors du chargement d’une fenêtre de boulangerie avec une scène sans maillages
* [Fonction] Blocage lors de la copie d’une instance dans son graphique référencé
* [Fonction] Correction d’un blocage possible lors de la manipulation des nœuds
* [Globalisation] L’italique n’est pas toujours correctement désactivé en japonais/coréen/chinois
* [Graphique] Identificateur de secours incorrect pour les nouveaux graphiques de modèles de Substance et MDL.
* [Graphique] Les paramètres hérités pilotés par des valeurs sont parfois calculés de manière incorrecte
* [GraphRender] Blocage lors du changement de moteur lors du calcul d’un graphique haute résolution (macOS uniquement)

### 12.2.1

*(Publié Le 4 Août 2022)*

**Fixe :**

* [Graphique] Résultats incorrects lors de la modification de la taille parent du graphique
* [Blocage] Blocage lors du calcul du graphique de composition de Substances à très haute résolution
* [Crash] Blocage lorsque la mémoire est insuffisante lors du chargement du pack
* [Blocage] Blocage lors de l’utilisation du crochet dans les annotations du paramètre exposé dans un graphique de modèle de Substance
* [Blocage] Amélioration de la stabilité du rendu des graphiques de composition de Substances
* [Iray] Mise à jour vers la version 2021.1.6

### 12.2.0

*(Publié Le 19 Juillet 2022)*

**Ajouté :**

* [Apple] Prise en charge native d’Apple Silicon (M1) (version pour Creative Cloud uniquement)
* [Graphique de modèle de Substance] Afficher les info-bulles des nœuds dans la vue Graphique
* [Graphique de modèle de Substance] Afficher les info-bulles des nœuds dans la bibliothèque
* [Substance model graph] Ajouter une entrée de menu contextuel pour prévisualiser les nœuds
* [Graphique de Substance de données] Autoriser l’utilisateur à créer des raccourcis pour la création de nœuds
* [UI] Ajoutez l’option « Afficher la sortie en vue 2D » dans le menu contextuel du graphique de composition
* [UI] Fractionner le paramètre « Affichage automatique des sorties » en paramètres spécifiques à la vue 2D/vue 3D
* [UI] Ajouter une flèche déroulante et une info-bulle au bouton « Afficher la sortie » dans la barre d’outils Vue 2D
* [UI] Réécrivez et réorganisez les éléments dans le panneau Informations de l’Explorateur
* [Gestion des couleurs] Ajout des espaces colorimétriques d’exportation Adobe RVB linéaire (1998) et Adobe RVB (1998) pour Adobe ACE
* [Gestion des couleurs] Ajouter l’espace colorimétrique de travail « Linear Adobe RGB (1998) » pour Adobe ACE
* [Gestion des couleurs] Prise en charge supplémentaire des écrans ICC OCIO
* [Gestion des couleurs] Masquer l’espace colorimétrique de travail d’Adobe RGB dans les préférences ACE
* [Gestion des couleurs] Amélioration de la qualité des tables LUT 3D cuites en mode ACE
* [Gestion des couleurs] Utiliser le nouveau back-end GPU dans la visionneuse 3D
* [Localisation] Mise à jour complète de la langue coréenne
* [Engine] Mise à jour vers la version 8.6.0
* [Graphique] Attribuez un identificateur de graphique par défaut lorsque cette propriété reste vide
* [Bibliothèque] Désactivation des hyperliens d’info-bulle pour les nœuds autres que les instances
* [NewProject] Mise à jour de la résolution par défaut
* [Modèles] Ajouter un modèle CLO
* [API] Afficher la propriété defaultParentSize pour les objets SDSBSCompGraph
* [Dépendances] Mettre à jour Alembic vers la version 1.8.3
* [Dépendances] Mettre à jour AXF vers la version 1.9.0
* [Dépendances] Mettre à jour Boost vers la version 1.76
* [Dépendances] Mettre à jour FBX vers la version 2020.2.1
* [Dépendances] Mettre à jour IRay vers la version 2021.1.0
* [Dépendances] Mettez à jour OpenColorIO vers la version 2.1.1
* [Dépendances] Mise à jour de l’OpenEXR version 3.1.5
* [Dépendances] Mettre à jour TBB vers la version 2020.3
* [Dépendances] Mettre à jour USD vers la version 0.22.3
* [Supprimer] Désactiver la fonction Effets de post-traitement (Yebis)
* [Supprimer] Supprimer la commande « Enregistrer le rendu dans Artstation » du menu Vue 3D

**Fixe :**

* [Modèles de Substance] La plage fixe définie sur le paramètre exposé est enregistrée lors de la désexposition
* [Substance models] L&#39;identificateur n&#39;est pas convivial sur les nœuds constants
* [Modèles de Substance] Améliorer la recherche en fonction de la compatibilité des nœuds
* [UI] L’ordre des sous-menus « Nouveau » est incorrect pour les ressources de dossier
* [UI] La taille par défaut de la fenêtre principale est très petite
* [UI] Les barres d’outils ne sont pas affectées par l’option « Réinitialiser la mise en page »
* [UI] Grille de transparence visible sur l’icône de ressource de police dans l’Explorateur
* [Cooker] Les graphiques de composition instanciés dans un graphique MDL sont toujours entièrement recouverts
* [Graphique] Blocage lors du collage d’un nœud copié à partir d’un graphique avec un identifiant vide
* [MDL] Blocage lors de la fermeture d’un graphique MDL spécifique
* [Performances] L’application ne répond pas lors du chargement de packs très volumineux
* [Ressources] La ressource Scène 3D peut être importée dans un cas spécifique

### 12.1.1

*(Publié Le 7 Juin 2022)*

**Fixe :**

* [Content] La ressource « bluenoise\_256 » a un attribut « colorspace » défini dans certains nœuds
* [Contenu] Les nœuds « Obtenir la taille » n’apparaissent pas dans la bibliothèque et la version en niveaux de gris est mal étiquetée
* [Contenu] Le paramètre « Random Color Seed » dans les nœuds 2D Voronoi n&#39;a aucun effet
* [SBSRender] L’exportation d’un graphique vers EXR ne génère pas le même bpc que Designer
* [Modèles de Substance] « Type de gamma » ne doit pas apparaître dans les propriétés du paramètre exposé
* [Modèles de Substance] Blocage lors de l’utilisation du crochet dans les annotations du paramètre exposé

### 12.1.0

*(Publié Le 26 Avril 2022)*

**Ajouté :**

* [Main] Nouveau contenu pour les graphiques de matériaux
* [Main] Envoyer des matériaux à Stager
* [Main] Prise en charge des fichiers USD
* [Principal] Amélioration du signalement des erreurs dans l’interface utilisateur
* [Principal] Nœuds de gestion de scène pour les graphiques modèles
* [Contenu] Ajout d’options supplémentaires aux bruits de perlin 3D (mosaïque, absolu...)
* [Contenu] Nouveau nœud fractal 3D Ridged Noise
* [Contenu] Nouveau nœud Décalage de texture 3D
* [Contenu] Nouveau nœud de position de texture 3D
* [Contenu] Nouveau nœud de surface de rendu de texture 3D
* [Contenu] Nouveau nœud de volume de rendu de texture 3D
* [Contenu] Nouveau nœud de Champ de distance signée de texture 3D
* [Contenu] Nouveau nœud de recadrage automatique
* [Contenu] Nouvelles fonctions d’accélération
* [Contenu] Nouveaux nœuds Extend Shape
* [Contenu] Nouvelles Cartes D’Usure/salissures
* [Content] Nouveau nœud de rotation non uniforme
* [Content] Nouveau filtre Tableau de zones de somme
* [Contenu] Nouveau générateur Tile Random 2
* [Contenu] Nouveau générateur de motif de Triangle Grid
* [Content] Nouvelle version du nœud Quantize Grayscale
* [Contenu] Nouveaux bruits fractaux Voronoi et Voronoi (2D/3D)
* [Contenu] Seuil : ajout du mode de comparaison « Inférieur » et « Inférieur et égal »
* [Contenu][Vue 3D] Ajoutez un ajustement de maillage pour afficher les tissus aux ressources expédiées
* [Modèles de Substance] Nouveau nœud Développer les instances de groupe
* [Modèles de Substance] Nouveau nœud de Fuse
* [Modèles de Substance] Nouveau nœud Renommer
* [Modèles de Substance] Nouveau nœud Reparent
* [Modèles de Substance] Nouveau nœud Définir le pivot
* [Substance models] Mise à jour vers SDK 1.6.0
* [UI] Amélioration du comportement du menu Nœud en cas de clic incorrect
* [UI] Ouvrir les sous-graphes dans le même onglet, même épinglés
* [UI] Bouton Supprimer l’épingle de la barre de titre du panneau Explorateur
* [UI] Enregistrer l’option « Ne plus afficher » sur l’écran de bienvenue dans toutes les versions
* [ThirdParty] Mettre à niveau Qt (et QtForPython) vers 5.15.8
* [Tiers] Mise à niveau de Python vers la version 3.9.9
* [Tiers] Mise à niveau d’OpenSSL vers la version 1.1.1m
* [Vue 3D] Afficher l’unité de grille dans la clôture lorsque l’assistant « Axe » est activé
* [Automatisation] Fournir l’outil de ligne de commande sbsbaker avec Designer
* [Gestion des couleurs] Implémentation d’un nouveau back-end GPU pour Adobe ACE
* [Cooker] Ajouter une option pour cuisiner un paquet sans horodatage
* [Graphique] Ajout de badges dans le graphique FxMap
* [Bibliothèque] Ajout d’un nouveau filtre pour les fonctions d’accélération
* Prise en charge de [Player] USD
* [Properties] Ajoutez une erreur d&#39;avertissement sur le paramètre « PKG Resource Path » d&#39;un nœud Bitmap lorsque la ressource est introuvable
* [Substance Engine] Mise à niveau vers la version 8.4.1
* [Yebis] Avertissez l’utilisateur que les effets de post-traitement Yebis seront supprimés dans la prochaine version.
* [Documentation] Nouvelle page « Avertissements et erreurs »
* [Documentation] Nouvelle page décrivant l’héritage dans les graphiques de composition de Substances
* [Documentation] Mise à jour de la section « Iray »
* [Documentation] Mise à jour de la section « Graphiques MDL »

**Fixe :**

* [UI] Problèmes d’écrêtage dans les info-bulles des modèles dans la nouvelle fenêtre graphique
* [UI] Texte blanc difficile à lire dans les nœuds lors de l’utilisation du mode sombre dans macOS
* [UI] Problème de disposition dans certaines boîtes de dialogue
* [UI] Le message d’avertissement s’affiche tronqué lors de la création du graphique de fonction de Substance dans l’Explorateur.
* [UX] Le sélecteur de couleurs descend à chaque nouvelle ouverture
* [UX] La fenêtre de l’éditeur de dégradé s’ouvre à chaque apparition
* [UX] Les propriétés du graphique ne s&#39;affichent pas automatiquement pour les packages chargés
* Mappeur de Flood Fill [Content] : sélection d&#39;entrée incorrecte dans un cas spécifique
* [Contenu] Flood Fill : fond perdu de texte dans les boutons de paramètres booléens
* [Contenu] Plage incorrecte pour le paramètre Angle du premier échantillon de lumière du nœud Plusieurs angles vers Normal
* [Modèles de Substance] Les propriétés du nœud affichent l&#39;identificateur au lieu de l&#39;étiquette
* [Modèles de Substance][Vue 3D] Problème d’actualisation lors de la réouverture d’un projet
* [Modèles de Substance][3Dview] Problème d’actualisation lors de l’utilisation de l’aperçu structure filaire
* [Paramètres] Blocage lors de la suppression rapide des entrées de graphique dans un cas spécifique
* [Paramètres] Blocage lors de la réinitialisation d’un paramètre d’instance lors de la modification de sa description de référence
* [Bitmap] La détection UDIM n&#39;est pas déclenchée pour les fichiers bitmap déposés dans le graphique
* [Graphique] Les nœuds de bitmap/SVG ne sont pas invalidés lorsque la ressource est modifiée sur le disque après le chargement du package
* [GraphRender] Fuite de mémoire lorsque l’évaluation du graphique de Substance est annulée
* [Localisation] La chaîne « Rebake all maps for this resource » apparaît non localisée
* [MDL] Paramètre exposé initialisé à 0 si l&#39;entrée est connectée à un nœud Dot non connecté
* [Préférences] Les info-bulles s’affichent même lorsque le curseur se trouve dans un espace vide
* [Propriétés] L’annulation d’une modification de la valeur d’espace colorimétrique définit la valeur par défaut dans un cas spécifique
* [Text] Impossible d&#39;annuler le changement de police vers une ressource de police manquante

## Version 11

### 11.3.3

*(Publié Le 1Er Février 2022)*

**Fixe :**

* [modèles de Substance] Les plages peuvent être perdues dans certains cas
* [Modèles de Substance][Exporter] L’échelle est différente selon le type de fichier
* [Modèles de Substance][Exporter] Les maillages sont dupliqués

### 11.3.2

*(Publié Le 25 Janvier 2022)*

**Ajouté :**

* [Documentation] Mise à jour de la section « Iray »

**Fixe :**

* [modèles de Substance] Impossible de publier le package contenant les graphiques de modèles de Substance
* [Modèles de Substance] Impossible d’exporter un graphique modélisé dans certains cas spécifiques
* [Modèles de Substance] Amélioration de la cohérence des plages de paramètres
* [MDL] Blocage lors de l’exportation du fichier MDLE
* [MDL] Fichier .mdl incorrect généré lorsqu’un graphique MDL contient des nœuds Point connectés à des paramètres Exposés
* [Vue 2D] Optimisation de l’affichage des outils de peinture
* [Contenu] Paramètre de taille de sortie incohérent configuré dans les graphiques sources du modèle
* [Propriétés] Les libellés des plages souples/dures sont incorrects dans le panneau de propriétés pour les nœuds exposés des modèles MDL et de Substance
* [Modèles] Mettre à jour les valeurs par défaut des entrées dans le modèle « Filtre Sampler »

### 11.3.1

*(Publié Le 13 Décembre 2021)*

**Ajouté :**

* [Graphique] Ajouter un avertissement lors de la suppression d’un graphique utilisé dans un autre graphique/pack

**Fixe :**

* [UI] L’éditeur de couleurs est trop petit lors de l’utilisation d’une disposition d’interface utilisateur spécifique
* [UI] Blocage lors de la mise à jour de la liste des modèles récemment utilisés
* [UI] Mise en surbrillance incorrecte dans les préférences de raccourcis
* [UI] La taille de la fenêtre principale est trop petite après le redémarrage d’une session en fenêtre (macOS uniquement)
* [UI] Le dock agrandi n’est pas réduit en sortie (Windows uniquement)
* [UI] Espace manquant dans l’info-bulle du paramètre « Niveau supérieur »[3DView] L’axe en vue 3D est trop petit lorsque le cadre de sélection de la scène est fin
* [UI] Problème de style sur certains textes dans les paramètres du projet en français
* [Modèles de Substance] Le verrouillage des paramètres exposés n’est pas enregistré entre les sessions
* [Modèles de Substance] Le modificateur Maj est toujours activé après l’utilisation du raccourci Aperçu du nœud
* [Modèles de Substance] Certains nœuds supprimés restent dans le SBSM exporté
* [Modèles de Substance] Les nœuds cibles de l’évaluation s’accumulent et ne sont pas supprimés[API] Blocage lors du rendu du nœud Courbe dont les propriétés ont été définies via l’API
* [Bakers] Le widget « Couleur de matière » n’est pas visible et ne fonctionne pas comme prévu
* [Contenu] Nœud de Rendu PBR : calcul interne non effectué à la résolution du nœud
* [Graphique de fonction] Les messages affichant les types attendus sont erronés dans certains cas
* [Graphique] Entrée relative à l’entrée : les paramètres hérités sont incorrects avec les instances connectées
* [MDL] Les instances de graphiques de Substance ne sont pas mises à jour de manière fiable dans les graphiques MDL
* [Publish] Échec de la publication du graphique contenant des dépendances circulaires
* [Raccourcis] Maj + Espace ne doit pas être un raccourci clavier assignable pour les nœuds
* [Modèles] Le format de sortie des modèles personnalisés est ignoré

### 11.3.0

*(Publié Le 24 Novembre 2021)*

**Ajouté :**

* [Modèles de Substance] Ajout d’info-bulles pour les paramètres des nœuds
* [Modèles de Substance] Permet d&#39;afficher dans l&#39;incrustation dans la fenêtre 3D le résultat d&#39;un nœud intermédiaire
* [Modèles de Substance] Amélioration de l’affichage des bases
* [Modèles de Substance] Conservez la hiérarchie des objets lors de l’exportation d’un graphique de modèle de Substance au format .fbx
* [Modèles de Substance] Prise en charge de plusieurs matériaux dans l’exportation FBX/OBJ à partir du graphique Modèle de Substance
* [Modèles de Substance][Contenu] Nœud de particule
* [Modèles de Substance][Contenu] Nœud Transformation générative
* [Modèles de Substance][Contenu] Nœud Motif organique
* [Modèles de Substance][Contenu] Particules du nœud Instances
* [Modèles de Substance][Contenu] Nœud de taille des particules
* [Modèles de Substance][Contenu] Nœud de tour
* [Modèles de Substance][Contenu] Nœud Shell
* [Modèles de Substance][Contenu] Nœud de projection
* [Modèles de Substance][Contenu] Nœud de rognage de courbe
* [Modèles de Substance][Contenu] Mettre à jour le nœud Curve Sampler
* [Modèles de Substance][Contenu] Mettre à jour le nœud Mesh Sampler
* [Modèles de Substance][Contenu] Mettre à jour le nœud de variation
* [UX] Bouton pour agrandir la vue actuelle
* [UX] Mettre à jour la fenêtre Nouveau graphique
* [UX] Ajouter l&#39;option « Télécharger le lecteur » dans le menu Outils et l&#39;agréger avec « Localiser le lecteur »
* [UX] Ajouter l’entrée « Tout fermer » au menu Fichier
* [UX] Appliquer la même casse dans tout le menu principal
* [UX] Afficher automatiquement les propriétés des éléments de graphique dupliqués
* [UX] Ajoutez des boutons dans la barre d’outils du graphique pour désactiver la taille d’écran constante pour les titres d’image / commentaires / épingles
* [UX] Boutons pour copier les informations de version dans le Presse-papiers dans la boîte de dialogue À propos
* [Matières] Entrées relatives aux entrées
* [Contenu] Ajout de l’option Limites sur les bruits Perlin 3D
* [Contenu] Nouveau nœud de processus de diffusion
* [Contenu] Nouvelle version du nœud de Rendu PBR
* [Interopérabilité] Recevoir SBS et SBSAR de Sampler
* [Interopérabilité] Envoyer SBSM à Stager
* [Vue 3D] Ajout d’une option pour désactiver l’abattage du dos
* [Vue 3D] Ajout d’une option pour afficher l’espace tangent des sommets
* [Explorateur] Mettre en surbrillance le graphique dans l’Explorateur lorsque vous double-cliquez sur l’arrière-plan de la vue Graphique
* [Explorer] Supprimer l’option « Explorer » dans les menus contextuels
* [Boulangers] Masquer les boulangers obsolètes
* [Gestion des couleurs] Ajout de la prise en charge des règles du fichier de configuration OCIO v2
* [Bibliothèque] Renommer les catégories en fonction des types de graphiques
* [Préférences] Désactivez automatiquement le processeur dans les préférences matérielles d’Iray si un GPU CUDA pris en charge est détecté

**Fixe :**

* [Modèles de Substance] Blocage sur Mac lors de l’utilisation de l’option « as sudb » sur .fbx
* [Modèles de Substance] Blocage lors de l’exportation vers SBSM dans un cas spécifique
* [Modèles de Substance] Échec de l’exportation lors de l’exportation des paramètres exposés dont les widgets n’ont jamais été créés
* [Modèles de Substance] Blocage aléatoire lors de l’ouverture d’un graphique faisant référence à plusieurs fichiers .fbx
* [modèles de Substance] Les plages ne sont pas appliquées dynamiquement dans les widgets des paramètres exposés
* [Modèles de Substance] L’option Recharger le filet ne fonctionne pas sur les ressources utilisées dans le graphique des modèles de Substance
* [Modèles de Substance] Les scènes ne s’affichent pas dans une vue 3D disponible dans un cas spécifique
* [UI] La zone de désactivation est trop grande dans les options de matière
* [UI] Problème de style dans la boîte de dialogue « Fichier de package non enregistré »
* [UI] Appuyez deux fois sur la touche de tabulation pour naviguer entre les valeurs.
* [UI] Le zoom avec la souris est inversé entre la vue 3D et les autres fenêtres.
* [UI] Le chargement d’un fichier SBS déjà ouvert à l’aide de la liste « Fichiers récents » déclenche une invite « Package introuvable »
* [UI][macOS] Disposition d’interface par défaut incorrecte après le démarrage de l’application
* [UI] Les packages ne peuvent pas être enregistrés à la racine d’un lecteur (Windows uniquement)
* [Graphique] L’option « Afficher automatiquement dans la vue 2D » est incohérente dans un cas spécifique.
* [Graphique] L&#39;option « Ouvrir la référence » est disponible pour les nœuds d&#39;instance SBSAR
* [Graphique] Les propriétés des épingles ne s’affichent que lors de la création d’un élément
* [Graphique] Les règles de chaîne d’épingles sont appliquées de manière incohérente
* [Graphique] Blocage lors de l’enregistrement d’un graphique vide
* [Vue 3D] L’angle d’Anisotropie est inversé dans le shader ASM
* [Vue 3D] ASM Shader : problèmes de linéarisation avec les mappages associés à SSS
* [Vue 3D] Rendu OpenGL rompu après la fermeture de vues 3D supplémentaires dans un cas spécifique
* [Vue 3D] Les positions de caméra prédéfinies ne sont pas correctes dans la vue 3D avec certains fichiers .fbx
* [MDL] L’option « Ajouter un nœud » du menu contextuel ne fonctionne pas pour les graphiques MDL.
* [MDL] Bogue : la connexion du nœud échoue lors de l’utilisation de composants float2.x et similaires (SD 11.1.2)
* [MDL] Blocage lors de l’ouverture d’un fichier .sbs spécifique
* [MDL] Unités de scène par mètre en iris non définies au début de la session de rendu
* [MDL] Se bloque lors de l’ajustement d’un nœud LDAP dans le graphique MDL
* [MDL] Ordre des paramètres dans le code MDL exporté
* [Explorer] un dossier de ressources vide est créé après l&#39;annulation de la création de la ressource
* [Explorateur] Seul le premier élément d’un package peut être déplacé vers le bas de la liste
* [Content] RT Bent Normal et RT AO déclenchent le calcul des nœuds dans les graphiques imbriqués
* [Nœud d’entrée] Le bitmap dans Nœuds d’entrée n’est pas mis à jour lorsque l’UDIM est modifié
* [Iray] L’affichage d’une scène de modèles de Substance avec de nombreuses instances prend beaucoup de temps
* [Préférences] Ligne vide lors de l’annulation de l’ajout d’un fichier de projet
* [Éditeur Python] L’option « Fermer » reste activée après la fermeture du dernier script et inclut toujours son nom e

### 11.2.2

*(Publié Le 28 Septembre 2021)*

**Ajouté :**

* [Propriétés] Ajoutez de nouveaux types de graphiques pour les décalcomanies, les atlas, les éclairages de l’environnement et les textures lumineuses

**Fixe :**

* [UI] Disposition d’interface incorrecte après le démarrage de l’application
* [Stabilité] Correction des blocages lors de la sortie du mode veille sous Windows et lors du branchement/débranchement d’écrans
* [Vue 3D] La création d’une ressource Scène 3D à partir d’un graphique de Substance de modèle Scène n’a aucun effet
* [Fusion] Les valeurs d&#39;énumération sont manquantes lors de l&#39;exposition du mode de fusion
* [Export] L&#39;exportation de scène des modèles de Substance entraîne une géométrie dupliquée
* [MDL] Blocage lors de l’ouverture d’un fichier SBS spécifique
* [Filet] Blocage lors de la liaison d’un filet spécifique avec une géométrie défectueuse
* [Modèles de Substance] L&#39;exportation échoue lorsque la valeur par défaut du paramètre exposé est hors de la plage souple

### 11.2.1

*(Publié Le 27 Juillet 2021)*

**Ajouté :**

* [modèle de Substance] Mise à jour vers la version 1.0.3
* [Modèle de Substance] Compléter et améliorer la documentation sur les graphiques de modèle de Substance
* [Substance de données] Afficher les journaux dans la console
* [Modèle de Substance][ScatterOnCurves] Modifier la valeur par défaut pour l&#39;espacement
* [Modèle de Substance][ScatterOnCurves] Supprimer le paramètre HalfSpaceOddEVEN superflu
* [Substance][Transformation] Mettre à jour la plage graduelle de rotation d&#39;Euler
* [Publish] Mémoriser les paramètres dans la fenêtre Publish
* [Publish] Avertissez l’utilisateur lorsqu’au moins une dépendance comporte des modifications non enregistrées
* [Publish] Champ Initialiser le chemin d’accès au fichier
* [Publish] Ajout de commentaires visuels pendant la publication
* [Interopérabilité] Ajout de la commande « Envoyer au lecteur » au menu « Envoyer à »
* [Interopérabilité] Simplification du workflow d’envoi/de renvoi vers Sampler et Painter
* [API] Ajoutez SDApplication.getVersion() pour permettre la récupération de la version de l’application hôte
* [Explorateur] Ajout d’une action Ouvrir aux éléments d’un graphique de modèle de Substance
* [Graphique] Désactiver les actions « Afficher en vue 3D » pour les nœuds d’instance fantômes

**Fixe :**

* [Modèle de Substance] Blocage lors de la suppression d’une séquence
* [Substance] Les bases ne sont pas tracées correctement dans certains cas
* [modèle de Substance] Échec de l’exportation de projets spécifiques
* [Modèle de Substance] L’affectation de matériau a échoué lors de l’ouverture d’un projet avec Iray activé
* [Substance] La plage fixe minimale ne fonctionne pas correctement dans certaines circonstances
* [Modèle de Substance][Primitif] Le premier niveau de subdivision de l&#39;icosphère ne fonctionne pas
* [Substance][RandomFloat] Gère correctement le cas où Min >= Max
* [Vue 3D] Blocage lors du glisser-déposer de cartes
* [Vue 3D] Les chaînes exposées dans les matières MDL utilisent un widget d’espace colorimétrique.
* [Vue 3D][Bakers] Les objets parents ne sont pas traités correctement
* [Vue 3D] Message d’avertissement concernant le nom d’utilisation « heightScale » pour le fichier .glslfx hérité
* [Content] Avertissements de cuisson dans Height Extrude
* [Contenu] Le nœud Irradiance RT n&#39;apparaît pas dans la bibliothèque
* [Contenu] RT Shadows : messages d&#39;avertissement de cuisson dans la console
* [Graphique] Blocage lors de l’ouverture d’un fichier avec certains nœuds désactivés
* [Graphique] Le nœud de point ne fonctionne pas correctement dans le graphique MDL lorsqu’un lien est sélectionné
* [Graphique] La vue Graphique n’est pas automatiquement rouverte après le rechargement d’un pack
* [Interopérabilité] Boîte de dialogue d’erreur lors de la sélection de « Télécharger... » lors de l’envoi au Lecteur
* [Interopérabilité] Le renvoi après suppression de toutes les sorties entraîne des erreurs d’API
* [Interopérabilité] Le renvoi juste après la fermeture de l’application cible entraîne des erreurs d’API
* [Explorateur] [Graphique] Après le rechargement d’un pack, le premier graphique ouvert n’est pas le premier du pack
* [Explorer] Les nouveaux graphiques d’un package ne sont pas placés de la même manière selon leur type
* [Explorer] Impossible d’ouvrir un graphique de modèle de Substance ou une ressource de scène après l’avoir déplacé dans l’explorateur
* [Explorer] Blocage lors du déplacement d’un graphique de modèle de Substance dans la hiérarchie du package
* [Bibliothèque] Les fichiers SBSAR restent à l’emplacement des fichiers temporaires
* [Bibliothèque] Les fichiers XML restent à l’emplacement des fichiers temporaires
* [Player] La matière n’a aucun impact dans la vue 3D lorsque la langue est définie sur le japonais
* Le lien de téléchargement de la Substance Player [Player] est obsolète
* [Widget Couleur] La fenêtre de l’éditeur de couleurs se déplace vers le haut de l’écran
* [IRay] Correction du chargement du module IRay sous Windows lorsque le répertoire d’applications contient des caractères non ascii
* [Préférences] Le panneau MDL s’affiche deux fois dans Project
* [API] Les nœuds FxMap ne prennent pas en charge getPropertyGraph()

### 11.2.0

*(Publié Le 23 Juin 2021)*

**Ajouté :**

* [Branding] La Substance Designer devient Adobe Substance 3D Designer
* [Modèles de Substance] Nouveaux graphiques de modèles de Substance pour créer des modèles 3D procéduraux
* [Contenu] Ajout de nouveaux mappages d’environnement HDR
* [Contenu] Nouveau nœud Courbé normal
* [Content] Nouveau nœud d&#39;Occlusion ambiante RT
* [Content] Nouveau nœud RT Caustics
* [Content] Nouveau nœud RT Caustics
* [Contenu] Nouveau nœud d&#39;irradiation RT
* [Contenu] Nouveau nœud Ombres RT
* [Interopérabilité] Envoyer la ressource vers Painter, lance Painter et ajoute ou met à jour la ressource dans la bibliothèque (nécessite une formule Substance 3D Adobe)
* [Interopérabilité] Envoyer la ressource vers Sampler, lance Sampler et ajoute ou met à jour la ressource dans la bibliothèque (nécessite une formule Substance 3D Adobe)
* [Interopérabilité] Parcourez votre ressource dans Adobe Bridge et lancez Bridge à l’emplacement de la ressource (nécessite une formule Substance 3D Adobe).
* [ASM] Prise en charge du nouveau matériau Adobe Standard Material (ASM) dans Graphe Substance et MDL Graph
* [ASM] Ajouter des modèles ASM
* [ASM] Ajouter OpenGL Shader pour ASM
* [ASM] Définir ASM Shader comme shader par défaut
* [Général] Agréger tous les fichiers temporaires dans le répertoire temporaire défini par l’utilisateur
* [Général] Nouvelle commande Enregistrer une copie sous
* [Général] Menu Fichier de mise à jour
* [Général] Mettre à jour le menu Aide
* [Publish] Nouvelle fenêtre de publication
* [Publish] Ajoutez une option dans les préférences afin de ne pas enregistrer le fichier SBS lors de la publication d’un fichier SBSAR
* [Properties] Ajouter un champ de type de graphique aux propriétés du graphique
* [Propriétés] Réorganisez les propriétés des graphiques de manière plus pertinente.
* [Branding] Nouvelle fenêtre À propos
* [Branding] Mise à jour du style d&#39;application
* [GLSLFX] Ajout d’un libellé aux techniques
* [GLSLFX] Ajouter la possibilité de définir le libellé d&#39;un shader GLSLFX
* [Métadonnées] Ajouter des métadonnées aux ressources du package
* [Métadonnées] Autoriser l’édition de métadonnées pour les graphiques, les entrées, les sorties et les ressources
* [Localisation] Nouvelles traductions en allemand, français et chinois simplifié
* [UX] Inversez le zoom dans la vue 3D en cas de glissement de la souris
* [AXF] Mise à jour vers la version 1.8.0
* [Journaux] Ajout des plug-ins installés aux journaux
* [VFX] Ajouter la configuration ACES 1.2 OpenColorIO
* [API Python] Ajout d’une méthode pour interroger le répertoire tmp spécifié dans les paramètres
* [API Python] Ajoutez une méthode isModified à SDPackage pour vérifier si un pack est enregistré
* [API Python] Ajout de méthodes de conversion de couleurs à SDColorManagementEngine
* [API Python] Supprimer des objets graphiques (commentaires, épingles, cadres, ...)
* [API Python] Exposer la propriété de Taille physique pour les nœuds d&#39;instance de graphe
* [API Python] Exposer Enregistrer une copie sous
* [API Python] Correction de la méthode SDPackageMgr.savePackage
* [API Python] Obtenir une liste des objets graphiques sélectionnés
* [API Python] Introduction de nouveaux noms de méthode pour travailler avec des sélections de graphiques
* [API Python] Les plug-ins ne peuvent pas ajouter d’actions au premier panneau d’explorateurs créé

**Fixe :**

* [Paramètres] Les valeurs négatives sur les paramètres Entier1 déroulants entraînent un comportement incongru dans l&#39;instance
* [Paramètres] Problème lors de l’incrémentation d’une valeur sur un widget d’angle
* [Graphique] Problèmes de synchronisation lorsque la sortie est affichée dans la vue 2D ou 3D.
* [Internationalisation] Certains caractères spécifiques sont transformés en espaces dans les identificateurs de fichiers
* [Préférences] Le libellé du fichier « Projet utilisateur » n’est pas retraduit du japonais
* [API Python] Erreur de récurrence lors de l&#39;exécution de la méthode SDUIMgr.getCurrentGraphSelectedNodes()
* [API Python] SDApplication.getPath(SDApplicationPath.InstallationDir) ne renvoie rien
* [API Python] SDSBSARExporter n’envoie pas de notifications d’enregistrement de fichiers

### 11.1.2 (2021.1.2)

*(Publié Le 17 Mars 2021)*

**Fixe :**

* [Bibliothèque] Les vignettes ne sont pas actualisées de manière cohérente
* [Contenu] La propriété « Pixel ratio » des graphes « Vector morphing » est définie sur « Stretch (Absolute) ».
* [Contenu] Les bitmaps utilisés dans les outils de peinture apparaissent dans le menu Nœud
* [Contenu] Sortie NaN pour entrée de couleur plate dans le nœud Niveaux automatiques à la précision en virgule flottante
* [Moteur][SSE2] Valeur « Niveau intermédiaire » autre que 0,5 pour une sortie 1,0
* [Vignette] Les cartes d’entrée sont réduites à 256.
* [UI] Les info-bulles des nœuds atomiques ont un saut de ligne incorrect

### 11.1.1 (2021.1.1)

*(Publié Le 10 Février 2021)*

**Fixe :**

* [Vue 3D] Problème de rendu lors de l’utilisation de fichiers SBS qui ont des fréquences élevées dans la carte normale
* [Vue 3D] Les images ne sont pas appliquées si la propriété de sortie « Component » n’est pas définie sur RVBA ou RGB
* [Vue 3D] Les scènes ne sont pas chargées correctement dans certaines situations spécifiques
* [UI] Le champ de saisie « Fichier de texture » dans l’éditeur de pinceaux est mis à l’échelle verticalement
* [UI] Les boutons Épingler et Ancrer disparaissent de l’onglet lorsque l’onglet actif est fermé
* [Boulangers] Résultat incorrect lorsque la Bbox globale des maillages poly élevés n&#39;inclut pas l&#39;origine de la scène
* [Gestion des couleurs] La propriété de matière Texture de couleur de base sRVB n’est pas remplacée dans l’état Scène personnalisé
* [Console] Le message du journal « GPU disponibles » ne répertorie pas les GPU et s’affiche de manière aléatoire
* [Console] Chaîne incorrecte consignée lors de l’utilisation de l’exportation par lots
* Le paramètre « Format normal d’entrée » de l’Atlas splitter [Contenu] a un impact sur la couche rouge au lieu du vert
* [Cooker] Blocage ou sortie NaN lors de l&#39;utilisation de \*.surface bitmaps dans SBSAR
* [Moteur] Les valeurs de sortie hors plage de la courbe de transfert de dégradé bouclent autour de 0 lorsque le format de sortie est compris entre 0 et 1
* [Paramètres] Les curseurs Min/Max/Par défaut ne s’ajustent pas automatiquement dans la fenêtre des paramètres d’exposition
* [SBSAR] Blocage lors de l’importation de certains fichiers SBSAR
* [SVG] Blocage lors de l’annulation de l’importation des ressources

### 11.1.0 (2021.1.0)

*(Publié Le 28 Janvier 2021)*

**Ajouté :**

* [Tons directs] Prise en charge des couleurs Pantone dans Designer
* [Graphique] Désactiver les nœuds
* [Vue 3D] Exporter des filets facettisés à partir de la fenêtre d’affichage
* [Internationalisation] Mettre à jour la version japonaise
* [Vue 3D] Optimisation de la consommation de mémoire lorsque vous n’utilisez pas Iray
* [API Python] Ajout de la méthode SDResource.delete() pour supprimer une source SDR
* [API Python] Ajout de la prise en charge des tons directs à l’API Python
* [API Python] Nouveau rappel à déclencher lorsqu’un pack est fermé
* [Vue 2D] Conversion de la base de données de pinceaux de SQLite au format Json
* [Vue 2D] Amélioration des performances de rendu et de la fiabilité (calcul du processeur)
* [Bibliothèque] Option « Exclure le modèle » ajoutée dans les paramètres du projet
* [Bibliothèque] Renommez « Exclure le modèle » en « Exclure les extensions de fichier » dans les paramètres du projet
* [UX] Supprimer le bouton « ? » dans les barres de titre des fenêtres sous Windows
* [UX] Déplacez le raccourci Ctrl+E vers « Ouvrir la référence » lorsque l’édition contextuelle est désactivée
* [Boulangers] Supprimer le cache d&#39;aperçu lors de la suppression d&#39;un boulanger dans la liste des boulangers
* [Performances] Optimisation du budget de la mémoire cache des images sur le matériel avec GPU avec mémoire partagée
* [Préférences] Adapter la valeur « Limite du cache GPU » au pool de mémoire disponible
* [Properties] Afficher l&#39;attribut de Taille physique sur l&#39;instance de nœud
* [Scripting] Marquer le système de script externe comme obsolète
* [Share] Supprimer les fonctionnalités « Exporter vers la Substance share »

**Fixe :**

* [Contenu] Ordre des E/S incohérent sur les nœuds Matériau
* [Contenu] L’entrée principale sur les nœuds de déformation est incohérente
* [Contenu] Résoudre les avertissements de l’outil Cuisinière à partir du nœud Flou radial
* [Export] L&#39;exportation par lots avec le moteur CPU utilise VRAM pour déterminer le budget de la mémoire
* [Exporter] L’exportation vers un chemin d’accès qui n’existe pas crée les dossiers
* [Export] Le budget de mémoire est trop faible lors de l’exportation par lots
* [Vue 2D] Artefacts/effets de bande lors de la copie d’images HDR dans le Presse-papiers
* [Vue 2D] L’exportation d’images à partir de ressources exporte toujours 8 bits
* [Vue 3D] Iray : modifier la valeur normale à l’aide de l’éditeur donne un résultat étrange
* [Vue 3D] Iray : la désactivation de la couche normale ne produit pas le bon résultat
* [Bibliothèque] Le filtrage par URL ne fonctionne pas correctement
* [Bibliothèque] Les ressources correspondant à un modèle exclu de la bibliothèque ne peuvent pas être importées manuellement
* [Boulangers] Le fait de renommer un boulanger n&#39;a aucune incidence sur son entrée dans la liste d&#39;aperçu de la vue 2D
* [Explorer] Perte de la synchronisation entre les données de l’Explorateur et du graphique
* [Graphique de fonction] Blocage lors de la définition du nœud de fonction avec un type de sortie non concordant en tant que sortie
* [MDL] Les nœuds d’instance SBS n’ont pas d’aperçu, génèrent la sortie 0 et ne déclenchent pas le calcul du graphique
* [API Python] Impossible de modifier la propriété &#39;editor&#39; du paramètre d&#39;entrée
* [Python] La réinitialisation de la mise en page ne réinitialise pas correctement les docks créés par Python
* [Ressources] Impossible de lier/importer un document de PSD 32 bits

## Version 10

### 10.2.2 (2020.2.2)

*(Publié Le 17 Décembre 2020)*

**Ajouté :**

* [Vue 3D] Restauration de la position de la caméra stockée dans une ressource Scène
* [Graphique] Supprimer les « nœuds d’entrée » dans le menu contextuel pour FXMap et le processeur de valeurs

**Fixe :**

* [Contenu] Ordre des E/S incohérent sur les nœuds Matériau
* [Contenu] Rendu PBR : échantillonnage IBL incorrect pour la contribution specular
* [Contenu] Rendu PBR : certains pixels sont toujours transparents
* [Contenu] Rendu PBR : la sortie UV est incorrecte pour la forme du cylindre
* [Contenu] Le paramètre « Pattern Specific » de Splatter Circular n’a aucun effet
* [MDL] Blocage lors de la création et de la connexion d’un nœud
* [MDL] Blocage lors de la duplication d’un constructeur de tableau color[] avec son entrée de valeur exposée connectée
* [MDL] Blocage lors de la reconnexion d’une connexion non valide
* [MDL] Les MDL exportées ont des paramètres en double
* [MDL] Les paramètres exposés ne sont pas exportés dans un fichier .mdl
* [Paramètres] Un paramètre de nœud peut être défini deux fois dans le SBS dans un cas spécifique
* [Paramètres] Blocage lors de la récupération du type de sortie du graphique de fonction d&#39;un paramètre
* [Paramètres] Blocage lors de la sélection de l’option « Modifier l’entrée de graphique exposée » lorsqu’il n’existe aucune entrée correspondante
* [Vue 3D] L’utilisation de l’« environnement » n’est pas correctement prise en compte par le moteur de rendu OpenGL
* [Vue 3D] IOR a la valeur 0 et doit être réinitialisé dans un cas spécifique
* [Vue 3D] Les UV du plan/plan haute résolution sont décalés
* [Bitmap] Blocage lors de l’annulation de l’importation des ressources
* [Bitmap] Blocage lors de la création d’un nouveau nœud Bitmap avec un type de fichier non pris en charge
* [Dépendances] Blocage lors de l’annulation de « Relocaliser » pour résoudre une instance fantôme
* [Graphique de fonction] Blocage lors de l’ouverture du graphique de fonction pour un paramètre
* [Éditeur de dégradé] Le déplacement des curseurs et des touches enregistre trop d’actions dans la pile d’historique
* [Licence] Blocage lors de l’analyse d’un fichier license.key non valide
* [SBSAR] Impossible de créer des nœuds d’instance SBSAR à partir de la bibliothèque si les graphiques exposés se trouvent dans des dossiers

### 10.2.1 (2020.2.1)

*(Publié Le 4 Novembre 2020)*

**Fixe :**

* [Général] Blocage lors de la sortie du mode veille Windows
* [Général] Blocage lors de l’annulation après le chargement d’une ressource Scène 3D
* [Moteur] Les lignes d’artefact apparaissent dans la sortie du nœud Distance sur Direct3D.
* [Moteur] Blocage lors de la sélection du nœud Courbe de transfert de dégradé dans un graphique mis à jour
* [Moteur] Aucun avertissement lorsque la valeur par défaut Entrée est différente de 0 en mode de compatibilité Moteur v7
* [Vue 3D] L’option Tout supprimer permet de conserver les filets avec des matériaux prédéfinis sans matériau appliqué
* [Vue 3D] L’option « Réinitialiser la scène » supprime toutes les textures du filet en Iray
* [Vue 3D] OpenGL : la modification de la valeur par défaut d’un échantillonnage dans un fichier .glslfx n’est pas correctement reflétée dans l’interface utilisateur
* [Vue 3D] Pixels rouges et noirs sur le bord le plus à droite des images rendues OpenGL
* [Dependencies] Impossible de déplacer les dépendances manquantes de type « Other »
* [Dépendances] Blocage à la sortie lorsque le visualiseur de dépendances est ouvert
* [Graphique] Blocage lors de la duplication d’un nœud d’instance fantôme
* [Graphique] L’édition contextuelle est disponible par frappe de touche lorsqu’elle est désactivée dans Préférences
* [UI] La fenêtre d’avertissement « Localiser le lecteur » a un titre incorrect
* [UI] L&#39;Assistant Activation a un comportement incorrect
* [Explorer] Les packages groupés sont toujours modifiables sous Windows
* [MDL] Blocage lors du chargement d’un graphique d’une version précédente avec des connexions non valides
* [Propriétés] Couleur par défaut du nœud d’entrée non mise à jour lors de l’annulation
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
* [Paramètres] Reformulation de la façon d’exposer un seul paramètre
* [Paramètres] Mettre en surbrillance les paramètres exposés
* [Paramètres] Améliorer le nettoyage des paramètres inutilisés
* [Engine] Nœud de courbe : nouvelle option pour générer la texture de courbe
* [Moteur] Valeurs par défaut sur les images d’entrée
* [Moteur] Nœud de distance : nouveaux modes de distance (distances de Manhattan et de Tchebychev)
* [Moteur] Nœud de dégradé : nouveau mode d’interpolation pour avoir un mélange plus naturel entre les couleurs
* [UX] Certains paramètres sont désormais grisés en fonction d’autres paramètres
* [UX] Accepter les couleurs RGB à 6 chiffres dans le champ hexadécimal du sélecteur de couleurs
* [UX] Évitez d’afficher les propriétés des commentaires dès qu’elles sont sélectionnées
* [UX] Afficher les groupes pertinents au début de l’écriture d’un nom de groupe
* [UX] Raccourci vers la réexportation des sorties graphiques
* [UX] Différencier toutes les zones de texte déroulantes des zones de liste déroulante standard
* [GraphRender] Affiche les nœuds une par une et pas seulement lorsqu’ils sont tous calculés.
* [GraphRender] Amélioration du délai d’annulation pendant le rendu des graphiques
* [GraphRender] Amélioration de la précision de la barre de progression du rendu
* [Vignettes] Calcul automatique des vignettes (icône)
* [Vignettes] Modification de l’interface utilisateur pour ajouter une vignette (icône) à un pack
* [Préférences] Activer le GPU raytracing par défaut pour les nouveaux utilisateurs
* [Préférences] 3DView / OpenGL / Quality : remplacez le curseur du nombre d’échantillons par une liste de choix plus intuitive
* [Boulangers] Améliorer les performances post-traitement
* [Gestion des couleurs] Afficher l’espace colorimétrique de travail actuel dans la boîte de dialogue des préférences.
* [Iray] Basculer automatiquement en mode CPU lorsqu’il n’y a pas de GPU compatible
* [Performances] Améliorer le temps de réponse pour calculer le nœud qui nous intéresse (maintenant calculé en premier)
* [API Python] Nouvelle méthode addActionToExplorerToolbar pour ajouter des icônes à la barre d’outils de l’explorateur
* [Ressources] Mise à niveau vers FBX 2020.0.1
* [iRay] Mise à jour vers Iray 2020.1.0
* [API] Ajout d’un accès Python aux paramètres et propriétés de gestion des couleurs

**Fixe :**

* [Graphique] La modification de la taille du gabarit ou du carreau uv n’annule pas le rendu actuel
* [Graphique] Blocage lors du déplacement d’une connexion de sortie en appuyant ensuite sur Alt+LMB
* [Graphique] Blocage lors du déplacement de connexions en mode Matériau ou Matériau compact
* [Graphique] Les nœuds d’entrée ne peuvent pas prévisualiser les ressources Bitmap
* [Graphique] Compatibilité des nœuds rompue sur les instances
* [Graphique] Trop de nœuds sont invalidés lors de la modification d’un paramètre de graphique
* [Contenu] La forme de sortie « Extrusion de forme » est inversée dans des cas spécifiques : nouvelle version requise, l’ancienne est obsolète
* [Contenu] Résultat incorrect à l’aide de la variation de couleur personnalisée dans le nœud Correspondance de couleur
* [Contenu] Le rapport Taille par quantité X/Y en Atlas scatter a l’effet inverse
* [Contenu] Le rapport entre la taille et la quantité sur X/Y dans Shape Splatter a l’effet inverse
* [Vue 3D] Blocage lors de l’opération Annuler après le chargement d’une ressource Scène à partir d’un package
* [Vue 3D] Environnement personnalisé non enregistré dans SBSSCN si le chemin a un alias avec des caractères spéciaux
* [Vue 3D] Le changement de format normal dans les paramètres de matière entraîne des états inversés
* [UI] Le texte du bouton « Définir comme principal » déborde de la zone d’affichage
* [UI] La position de la fenêtre principale n’est pas correctement restaurée lorsque vous travaillez en mode fenêtré
* [UI] Le texte de la barre d’état est décalé lorsque la fenêtre est en plein écran ou déplacée près du bord de l’écran
* [Iris] Blocage avec message « Balise non valide » lors du basculement entre les systèmes de rendu
* [Iray] Faces visibles sur les surfaces non opaques
* [Paramètres prédéfinis] Blocage lors de l’application de paramètres prédéfinis dans des instances de certains graphiques de Substance Source
* [Paramètres prédéfinis] nom erroné affiché après l&#39;annulation sur l&#39;instance sbs
* [Rendu] Mauvais rendu lors de l’ajustement d’un paramètre en mode aperçu
* [Boulangers] L’actualisation de plusieurs maps bakées entraîne des avertissements bloquant certains boulangers
* [Cooker] L’ajustement des nœuds SBSAR dans les instances SBS entraîne une sortie de 0 de l’instance
* [Explorer] Les alias personnalisés ne sont pas transmis lors de l’utilisation de « Enregistrer et ouvrir dans la Substance Player »
* [Éditeur de dégradé] La sélection de couleur absolue n’a pas d’impact sur toutes les touches sélectionnées

### 10.1.3 (2020.1.3)

*(Publié Le 11 Juin 2020)*

**Ajouté :**

* [Contenu] Exposer le paramètre « Couleur de cache » dans le nœud Niveaux de gris de transformation sécurisée
* [Contenu] Rendu PBR : ajout d’une option personnalisée Entrée d’arrière-plan
* [Contenu] Nœuds Lumière de panorama : nouvelle option pour prélever la couleur de l’image d’arrière-plan
* [Paramètres] Masquer les paramètres avec l’indicateur « non pris en charge » dans la liste de la fenêtre Exposer les paramètres

**Fixe :**

* [Vue 3D] Blocage lors du changement de maillages personnalisés dans un cas spécifique
* [Vue 3D] Le format normal est toujours DirectX au démarrage
* [Contenu] Bruit Worley 3D : rendu d’un artefact lors de l’utilisation d’une valeur de taille de grille élevée
* [Contenu] La fusion des nœuds de fondu est incorrecte
* [Contenu] Rendu PBR : supprimer l’avertissement de l’outil de cuisson
* [Contenu] Rendu PBR : résultat contient des couleurs négatives dans certains cas
* [Cooker] Problème d&#39;injection du cache pour les nœuds d&#39;instance à sorties multiples
* [Explorer] Blocage lors de la fermeture d’un pack contenant un graphique MDL affiché
* [Graphique] Cuisson en 2 passes : le changement de type de nœud ne déclenche pas de recook
* [Graphique] Blocage lors de la suppression d’entrées lors de l’utilisation de sa connexion
* [Graphique] Les extrémités de lien peuvent être déplacées vers un espace vide
* [MDL] Blocage lors de l’annulation de l’exportation MDL à partir du graphique MaterialX
* [MDL] Erreur lors de l’annulation de l’exportation vers MDLE
* [Paramètres prédéfinis] Blocage dans l’onglet Paramètres prédéfinis après la modification du type de paramètre inclus dans le paramètre prédéfini
* [Ressources] La liste des matériaux est vide dans le menu contextuel du graphique pour les maillages liés comme non-UDIM

### 10.1.2 (2020.1.2)

*(Publié Le 27 Avril 2020)*

**Ajouté :**

* [Contenu] Ajouter un modèle de filtre Alchemist
* [Contenu] Rendu PBR : ajoutez des paramètres pour contrôler les intensités des ombres de diffusion/specular
* [Contenu] Formez les nœuds Lumière : ajoutez un paramètre de position de caméra
* [Actualités] Le style « Flèche » du groupe ne fonctionne pas la première fois que la fenêtre s’affiche
* [Bakers] Ajoutez le raccourci Z à la vue 2D pour afficher l’image au format 1:1
* [Projet] Masquer l’alias $(PROJECT\_DIR) de la liste
* [Explorer] Ne créez pas de ressource personnalisée pour les ressources qui ne sont pas un fichier sur le disque

**Fixe :**

* [Player] Signaler les alias manquants lors du chargement des packages SBS
* [Player] Afficher la valeur de générateur aléatoire sous forme de base décimale
* [Player] Regrouper tous les mappages d’environnement inclus dans la Substance Designer
* [Player] Blocage à la sortie dans macOS High Sierra
* [Player] Impossible de charger les packages utilisant sbs://
* [Contenu] Bruit Worley 3D : rendu d’un artefact lors de l’utilisation d’une valeur de taille de grille élevée
* [Contenu] L’entrée « supérieur à zéro » dans le nœud « Onde » n’est pas utilisée
* [Contenu] Lumière plane : le mode Position dans l’espace universel ne fonctionne pas
* [Contenu] Lumière sphérique : la position d’éclairage interne ne fonctionne pas correctement
* [Boulangers] Blocage lors de la cuisson avec la fenêtre de cuisson alors qu&#39;une option « Actualiser toutes les maps bakées » est en cours d&#39;exécution
* [Boulangers] Échec de cuisson sur Optix pour AO à partir de Mesh en utilisant Faible comme Élevé avec une carte Normale
* [Bakers] La résolution de l’aperçu des fichiers UVT ne correspond pas à la taille de l’écran
* [Vue 3D] Le bitmap attribué est remplacé lors du chargement d’une MDL si la valeur par défaut n’est pas une texture2d
* [Vue 3D] Les widgets Propriétés des matériaux changent après la réinitialisation d’une propriété
* [Vue 3D] La préférence globale Format normal ne fonctionne plus
* [MatX] Bibliothèque : la catégorie Graphe MaterialX n&#39;affiche pas tous les nœuds disponibles
* [MatX] Le menu contextuel d’un graphique personnalisé peut contenir des sous-dossiers vides dans le dossier « Ajouter un nœud »
* [SBSAR] L’entrée principale est restaurée à la première entrée de la liste
* [Bibliothèque] Seul le premier graphique est inclus à partir de SBSAR avec plusieurs graphiques
* [CustomGraph] Les nœuds qui ne font pas partie du type de graphique actuel sont créés automatiquement dans certains cas
* [Iray] Le paramètre « Profondeur » de projection de boîte ne fonctionne pas correctement
* [Préférences] Amélioration de la mise en page dans les paramètres du projet
* [Paramètres] Blocage lors du déplacement d’un widget de position après avoir supprimé un paramètre
* [UI] Blocage lors de la modification de la hiérarchie des utilisations dans le nœud de sorties
* [Graphique] Blocage lors de l’utilisation d’une zone de sélection sur un commentaire et un nœud badgé

### 10.1.1 (2020.1.1)

*(Publié Le 10 Avril 2020)*

**Fixe :**

* [Vue 3D] L’utilisation de la mémoire est trop élevée lors de la composition de graphiques
* [Contenu] Formes inattendues dans la sortie non carrée des nœuds « Polygone »
* [Contenu] Rendu PBR : la caméra orthographique ne fonctionne pas correctement lors de l’utilisation d’une résolution non carrée
* [Contenu] Rendu PBR : Swirly bokeh augmente la luminosité de la bordure de l’image
* [Gestion des couleurs] Le sélecteur de couleurs dans la boîte de dialogue Nouveau bitmap ne gère pas les couleurs.
* [Gestion des couleurs] Les sélecteurs de couleurs des outils de peinture et vectoriels de la vue 2D ne prennent pas en charge la gestion des couleurs.

### 10.1.0 (2020.1.0)

*(Publié Le 9 Avril 2020)*

**Ajouté :**

* [Raccourcis] Gestionnaire de raccourcis pour la création de nœuds
* [Contenu] Nouveau nœud de Rendu PBR
* [Contenu] Nouveau filtre FXAA
* [Contenu] Nouveau filtre Hald CLUT
* [Contenu] Exposer le filtrage dans les nœuds « Recadrer »
* [Vue 3D] Amélioration des paramètres de l’ombrage/du workflow d’affectation de texture
* [Vue 3D] Nouveau nuanceur non éclairé
* [Vue 3D] Ajoutez une « valeur zéro scalaire » aux ombrages de displacement
* [Vue 3D] Ajout d’une option permettant de réduire la résolution de l’aire d’affichage lorsque la haute résolution est activée
* [Vue 3D] GLSLFX : permet de définir les informations d’interface graphique sur sampler (par défaut, min, max, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup)
* [Vue 3D] Ajoutez l’option « Charger l’état avec le filet... » dans le menu Scène
* [Vue 3D] Ajout de la transformation de sortie mappée à la tonalité ACES en mode de gestion des couleurs hérité
* [Boulangers] Nouvelle méthode d&#39;échantillonnage en AO, Courbure, Bent Normal, Thickness bakers
* [Boulangers] Nouvelles options de normalisation dans les boulangers d&#39;Heights et de Thickness
* [Gestion des couleurs] Intégrer Adobe ACE (Adobe Color Engine)
* [Gestion des couleurs] Ajoutez des options pour définir le comportement par défaut lorsque le profil ICC est manquant
* [Paramètres] Incrémenter les curseurs en fonction de la Substance Painter
* [Packaging] Regroupez autant de DLL Qt que possible pour les scripts Python
* [Projet] Désactivez les paramètres pour les fichiers de projet en lecture seule et communiquez clairement cet état
* [Préférences] Masquer des paramètres non clairs spécifiques liés à la réactivité et aux périodes de calcul
* [UI] Renommer Pow2 -> 2Pow
* [Propriétés] Optimisation de l’affichage des propriétés du graphique de composition
* [AXF] Mise à jour vers AXF SDK 1.7.1

**Fixe :**

* [Vue 3D] Les paramètres Lumière ambiante ne sont pas visibles même s’ils sont activés
* [Vue 3D] glslfx : le widget de couleur est toujours un vec3 sans alpha
* [Vue 3D] La carte d’environnement définie à partir d’une ressource n’est pas enregistrée dans la ressource de scène
* [Vue 3D] Iris : la lumière ambiante est convertie en lumière ponctuelle à l’origine de la scène
* [Vue 3D] glslfx : le widget de couleur est toujours un vec3 sans alpha
* [Paramètres] L&#39;URL du package d&#39;instance est incorrecte dans le groupe d&#39;attributs
* [Paramètres] Blocage lors de l’exposition des paramètres
* [Paramètres] Les icônes ne sont pas correctement alignées dans les paramètres des nœuds de courbe
* [Paramètres] La chaîne de nœud &#39;Text&#39; s&#39;affiche uniquement en mode &#39;Preview&#39; lorsqu&#39;elle est exposée
* [Paramètres] Blocage lors du changement de nom d’un paramètre d’entrée utilisé dans l’instruction « Visible If »
* [Paramètres] Blocage lors de la suppression d’un nœud Levels dont une fonction est définie dans l’un de ses paramètres
* [UI] L&#39;icône d&#39;avertissement dans la liste des paramètres d&#39;entrée est placée sur un bouton existant
* [UI] Les avertissements ne sont pas effacés sur l&#39;élément de paramètre d&#39;entrée correct dans un cas spécifique
* [UI] Empêcher le message « Is mesh UDIM ? » pop-up pour apparaître lorsque les UV du maillage sont strictement dans la mosaïque [0,1]
* [UI] Les listes déroulantes des paramètres prédéfinis peuvent défiler avec la molette de la souris en passant simplement la souris au-dessus
* [UI] L’option « Calcul des sorties » dans les attributs de graphique n’est pas nommée correctement
* [MDL] Blocage lors du placement d’une ressource de graphique SBS dans un graphique MDL
* [MDL] Le nœud SBS avec entrée d’image ne fonctionne pas correctement
* [MDL] Liaisons de texture et noms d’utilisation incorrects
* [Graphique] Le groupe de valeurs d’entrée et l’utilisation sont ignorés dans le mode de création de lien « Matériau »
* [Graphique] Les valeurs d’entrée utilisent la valeur par défaut au lieu des données d’entrée pour les booléens
* [Bakers] Normales incorrectes dans World Space Normals baker utilisant une carte de normales de tangente dans des cas spécifiques
* [Bakers] Utilisation excessive de la mémoire lors de la cuisson avec la fenêtre Aperçu ouverte
* [Paramètres prédéfinis] paramètre prédéfini corrompu entraînant un blocage du rendu
* [Paramètres prédéfinis] Le paramètre booléen de l’ancien SBS n’est pas affecté par le paramètre prédéfini
* [Bibliothèque] Les ressources du premier package ouvert sont répertoriées dans le menu flottant de création de nœud
* [Publish] La publication sur SBSAR renvoie le code d’erreur 13 dans SBSCooker sur macOS
* [Publish] Avertissement d’argument obsolète dans SBSCooker lors de la publication dans SBSAR
* [API] Impossible d’obtenir les métadonnées d’un package provenant d’un fichier .sbsar
* [Export] En mode hérité, l’option d’espace colorimétrique revient aux valeurs par défaut pour des sorties spécifiques
* [Vue 2D] La copie dans le Presse-papiers ne prend pas en compte l&#39;état de gestion des couleurs
* [Unix] Designer ignore les signaux système
* [Bibliothèque] Certains filtres de la bibliothèque ne fonctionnent pas correctement en raison de balises traduites
* [Cooker] La racine carrée des nombres négatifs doit renvoyer 0 au lieu de NaN
* [Vue 2D] Les couches rouge et bleue sont permutées après l’annulation du premier tracé de peinture
* [Console] Message d&#39;avertissement trop long dans la console : « QPixmap::scaled: Pixmap est un pixmap nul »
* [Contenu] « Shape Glow » : avertissement culinaire
* [Dépendances] L’affectation d’un graphique situé dans un package différent à un maillage ne crée pas de dépendances
* [Iray] Les propriétés de matériau deviennent inactives après le changement de géométrie

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
* [Graphique] Les performances chutent et se bloquent lorsque vous ajustez un graphique imbriqué avec l’option « In-Context Editing » active
* [Graph] Blocage lors de la suppression de plusieurs nœuds dans FX-Map
* [Performances] Le processus de Designer peut rester actif après la fermeture

### 9.3.1 (2019.3.1)

*(Publié Le 27 Janvier 2020)*

**Fixe :**

* [Graphique] Baisse et blocage importants des performances lors de l’ajustement d’un graphique imbriqué avec l’option « In-Context Editing » active
* [Graphique] Impossible de saisir une valeur enum sur [0, 99] dans Entier1 tweak
* [Graphique] Le commentaire n’est pas déplacé lorsque le cadre correspondant est déplacé
* [Graphique] Les noms d&#39;entrée sont manquants sur le nœud d&#39;instance personnalisé
* [Graphique] Les vignettes peuvent être rendues lors du chargement du graphique même si l’option correspondante est désactivée dans les Préférences
* [Vue 2D] La valeur alpha négative affiche le correcteur quelle que soit l’option d’affichage
* [Vue 2D] La conversion de surface de 32f à 8bits échoue avec des valeurs élevées
* [Vue 2D] Les options Inclinaison haut/gauche et Créer un carré définissent certaines coordonnées sur des valeurs énormes dans les matrices de transformation avant
* [Vue 2D] Les UV de tous les objets de maillage ne sont pas affichés sur les jeux UV autres que « 0 »
* [Contenu] Biseau : le mode Angular ne fonctionne pas correctement sur le masque de mosaïque
* [Contenu] Flood Fill au dégradé : la valeur de l&#39;image de pente n&#39;est pas échantillonnée au milieu de la forme
* [Content] Fonction ; « Equality Boolean » est rompu
* [Boulangers] Artefacts lors de l’utilisation du mappage de tonalité automatique dans le boulanger « Courbure à partir du filet » dans des cas spécifiques
* [Boulangers] Blocage dans DXR lors de la cuisson alors qu’aucun matériau n’est sélectionné
* [Boulangers] Problème de performances dans la vue 2D lors de l’activation de l’info
* [Moteur] La fonction « Pow » génère des valeurs énormes lors de l’utilisation de valeurs d’entrée très faibles et d’un exposant élevé sur le moteur SSE2
* [Moteur] Blocage lors de l’utilisation d’une compression jpg élevée sur des ressources bitmap
* [Moteur] Le processeur de valeurs renvoie une valeur $size incorrecte à l&#39;intérieur d&#39;un sous-graphe
* [Paramètres] Une fenêtre contextuelle vide s&#39;affiche lors de la sélection d&#39;un nœud d&#39;instance avec un nombre élevé de paramètres
* [Paramètres] La valeur entière n&#39;est pas affichée dans les éléments de paramètre du menu déroulant
* [Paramètres] Le bouton Modifier de la Matrice de transformation n&#39;est pas disponible en mode Aperçu
* [Cooker] $size dans ValueProcessor est incorrect à l’intérieur d’une instance de graphique
* [Cooker] La taille de sortie est incorrecte lorsque le lien de valeur passe par un nœud point vers un nœud atomique
* [UI] Le bouton permettant d&#39;afficher tous les éléments de la barre inférieure de la vue 2D n&#39;est pas visible
* [UI] L’aperçu des valeurs de RGB sélectionnées affiche des nombres incorrects lors de l’utilisation de la gestion des couleurs
* [Export] Les images RVBA 16f sont exportées en niveaux de gris
* [Vue 3D] Impossible d’importer OBJ avec plusieurs espaces
* [Gestion des couleurs] La configuration OCIO n’est pas prise en compte lors de la publication de sbsar
* [Color Widget] Les plages de curseurs de couleur peuvent se développer de manière exponentielle dans un cas spécifique
* [Doc] La section « paramValue » est incomplète dans la référence au format Sbs
* [MDL] Le widget de couleur dans les instances sbsar est incorrect
* [Paramètres prédéfinis] Blocage lors de la mise à jour des paramètres prédéfinis dans un cas spécifique
* [PSD] Erreur FreeImage lors du chargement de fichiers PSD à partir de versions récentes de Photoshop
* [Ressources] Blocage lors de l’annulation de la liaison bitmap directement dans le graphique
* [SVG] Les nœuds de SVG ne se mettent pas à jour automatiquement lors de l’utilisation des outils vectoriels

### 9.3.0 (2019.3.0)

*(Publié Le 19 Décembre 2019)*

**Ajouté :**

* [Général] Prise en charge de la gestion des couleurs avec le fichier de configuration OpenColorIO
* [Paramètres prédéfinis] Améliorer la gestion des paramètres prédéfinis
* [Paramètres prédéfinis] Synchroniser les gadgets d’affichage 2D et les curseurs d’aperçu
* [Paramètres prédéfinis] Restauration des valeurs d’aperçu lors du retour au mode Aperçu
* [Paramètres prédéfinis] Maintenez le mode d’aperçu actif lors de la modification d’autres nœuds, ressources ou graphiques
* [Paramètres prédéfinis] L’option Annuler fonctionne correctement lors de la navigation entre les 3 onglets de paramètres prédéfinis
* [Paramètres prédéfinis] Autoriser à réinitialiser les paramètres à la valeur par défaut du graphique ou à la valeur du paramètre prédéfini en mode Aperçu
* [Paramètres prédéfinis] Amélioration de l’épinglage des paramètres
* [Paramètres prédéfinis] Importer/exporter tous les paramètres prédéfinis d’un graphique dans un fichier
* [Bakers] Nouveau baker « Courbure à partir d’un filet » basé sur le lancer de rayons
* [Boulangers] Ajouter l&#39;option de plan au sol dans le boulanger « AO from Mesh »
* [Boulangers] Ajouter l&#39;option de correspondance par nom pour ignorer le dos dans &#39;AO from Mesh&#39; baker
* [Contenu] Nouveau nœud d’Atlas scatter
* [Contenu] Nouveaux nœuds et fonctions de conversion de l’espace colorimétrique (ACEScg)
* [Contenu] Amélioration de la cohérence des noms pour les nœuds avec des versions en couleurs/niveaux de gris
* [Graphique] Amélioration des performances en mode Aperçu des paramètres prédéfinis
* [Graphique] Option Ajouter $(colorspace) macro à l’exportation des sorties de graphique
* [Paramètres] Lorsqu&#39;un paramètre est défini sur invisible, masquez l&#39;objet correspondant dans la vue 2D
* [Paramètres] N’ajoutez pas « Groupe d’entrée de graphique » comme préfixe lors de l’exposition des paramètres
* [Paramètres] Ajout d’une info-bulle pour les paramètres VisibleIf dans Graph
* [AXF] Mise à jour du SDK AXF vers la version 1.6

**Fixe :**

* [Linux] Designer ne se lance pas sur CentOS 8 en raison d’un échec de chargement de la plateforme Qt.
* [Linux] AVERTISSEMENT : la bibliothèque Freetype a été supprimée de l&#39;application SD : les utilisateurs avec CentOS version &lt;= 7.5 doivent l&#39;installer manuellement.
* [AxF] Blocage lors de l’importation de fichiers créés avec des versions AxF plus récentes
* [2DView] Les textures de pinceau alimentées par une ressource ne sont pas appliquées
* [2DView] Blocage lors de la modification des entrées d’un graphique instancié avec ajustement de position
* [3DView] Blocage lors de l’annulation du chargement... action
* [3DView] Option Ajouter un espace colorimétrique pour les textures d’émission dans les nuanceurs GLSLFX
* [Boulangers] Les cartes alimentées par les ressources sont ignorées pendant la cuisson
* [Bakers] Les options « Direction de l’espace universel » ne sont pas correctement verrouillées
* [Bitmap] Les bitmaps EXR avec des valeurs en virgule flottante sont rendus sous forme d’image noire
* [Contenu] Flood Fill à l’index : la détection de forme échoue dans un cas particulier
* [Contenu] Recadrage : problème d’échantillonnage lorsque le nœud de recadrage a une résolution inférieure à l’entrée
* [Général] Blocage lors de la fermeture de Designer lors de la génération de la bibliothèque
* [Graphique] Les nœuds bitmap ne reflètent pas la compression du bitmap associé
* [Graphique] Le cache n’est pas effacé lors de l’effacement des vignettes de nœud après le premier rendu
* [Graphique] Taille de nœud incorrecte
* [Graphique] Blocage lors de la modification des connexions d’entrée sur un nœud de processeur de pixels dans certains cas
* [Graphique MDL] Échec lors de la restauration d’une valeur par défaut d’appel de fonction
* [Propriétés] Les boutons « Modifier » et « Matrice » dans les paramètres de matrice de transformation prêtent à confusion

### 9.2.3 (2019.2.3)

*(Publié Le 26 Novembre 2019)*

**Ajouté :**

* [MacOS] Authentifiez le logiciel pour respecter les nouvelles exigences de distribution de MacOS Catalina

**Fixe :**

* [Bakers] Blocage lors de la restauration à l’aide d’une ressource de mappage incliné avec un lien non valide
* [Boulangers] Les ensembles UV autres que 0 ne sont pas pris en compte sur Embree
* [Boulangers] &#39;Bent Normals from Mesh&#39; génère des résultats incorrects avec des réglages UV autres que 0 sur DXR
* [Boulangers] Les paramètres &#39;UV Set&#39; sont réinitialisés à la valeur &#39;0&#39; lors de la réouverture de la fenêtre de cuisson
* [Bakers] &#39;Position&#39; génère une image noire avec des jeux UV autres que 0
* [Contenu] Mosaïque automatique intelligente : problème d’échantillonnage dans 8k
* atlas splitter de [Content] : la détection de forme échoue dans certains cas, le paramètre de précision doit être exposé
* [Contenu] Pow ne renvoie pas la bonne valeur dans certains cas
* [Contenu] Flood Fill vers index : résultat incorrect lors de la publication sur sbsar
* [Library] Blocage lors du chargement du premier package SBS de la session
* [Bibliothèque] Le paramètre Afficher les ressources dans la bibliothèque par défaut est ignoré pour les ressources importées directement dans le panneau Explorateur
* [Console] Message inattendu dans la console lors de l’utilisation du menu des nœuds
* [Paramètres] Impossible de supprimer une seule entrée dans la liste d&#39;utilisation de la sortie
* [3DView] la scène n&#39;est pas rechargée correctement lorsque le fichier de scène est modifié sur le disque[Graph] Le filtrage du menu Nœud est incorrect lors de l&#39;utilisation des sorties Valeur

### 9.2.2 (2019.2.2)

*(Publié Le 23 Octobre 2019)*

**Fixe :**

* [Graphique] Le filtrage du menu Nœud est incorrect lors de l’utilisation des sorties Valeur
* [Graphique] Blocage lors de l’affichage du menu des nœuds
* [Graphique] L’outil Recherche s’affiche lors de l’utilisation du raccourci Maj
* [Graphique] Blocage lors de la génération consécutive de menus de nœuds à partir du connecteur d’entrée de valeur
* [Graphique] Les commentaires contenant de longues chaînes sont recadrés
* [Graphique] La mise en surbrillance du flux est incorrecte lors de la création d’un nœud à l’aide du menu Faire glisser du connecteur
* [Graphique] Blocage lors du retrait de tous les éléments de graphique de la scène lors du chargement d’un autre graphique
* [Graphique] Blocage lors de l’utilisation de pour créer un nœud lors de l’utilisation du clic et du glissement à partir du connecteur
* [Graphique] Blocage lors de l’utilisation de l’outil « Node Finder »
* [Graphique] La couleur de l’épingle de sortie est incorrecte en mode « Matériau compact »
* [Cooker] Les nœuds en aval des nœuds à sorties multiples ne se mettent pas à jour correctement
* [Cooker] Problème avec les sorties Value et les nœuds passthrough
* [Cooker] Le processeur de valeurs génère des résultats incorrects lorsqu&#39;un seul nœud &#39;Get&#39; est utilisé
* [Contenu] Le nœud « Contraste/Luminosité » génère une valeur d’Alpha de 1,0
* [Contenu] Le modèle « Panorama Studio » ne contient aucune description
* [Contenu] Flood Fill à indexer : résultat incorrect lorsque l’entrée contient une forme d’enchaînement
* [Contenu] « Fusion HDR » : calcul de l’exposition interne incorrect
* [Point Node] Blocage lors de l’utilisation d’un niveau et d’un point Node
* [Gestionnaire de dépendances] L’action « Aller à » ne fonctionne plus
* [PSD] Blocage lors de l’annulation de la suppression de plusieurs nœuds qui étaient inclus dans l’exportateur de PSD
* [UI] Blocage lors de la fermeture d’un graphique à l’aide du menu « Fenêtre » et de son ouverture une nouvelle fois avec un graphique épinglé
* [Éditeur de dégradé] Le bouton « Supprimer la clé » est trop grand
* [Moteur] Problème de précision avec sqrt() acos() et asin()
* [Bakers] AO À partir du maillage : le curseur « Angle de dispersion » a une plage de valeurs incorrecte lorsqu’il est modifié

### 9.2.1 (2019.2.1)

*(Publié Le 20 Septembre 2019)*

**Ajouté :**

* [Modèles] Ajout de nœuds d’entrée par défaut à Specular/brillance et à d’autres modèles
* [Modèles] Ajouter un modèle d’Anisotropie PBR
* [Vue 3D] Augmentez les distances automatiques du plan de l’élément
* [Vue 3D] PBR Coated : modifier la valeur par défaut pour l&#39;héritage normal de la couche
* atlas splitter [Contenu] : ajouter une option pour la fonction « Recadrage automatique »
* [Menu Nœud] Ne filtrez pas les nœuds sans entrée

**Fixe :**

* atlas splitter [Contenu] : certaines sorties ne sont pas recadrées correctement lors de l’utilisation de l’option « Recadrage automatique »
* [Contenu] Mélange d’Heights de matière : erreur de cuisson liée à un paramètre inexistant
* [Contenu] « Lumière plane » : le mode UV du motif ne fonctionne pas correctement
* [Contenu] « Height à l’unité normale » : l’entrée est forcée sur 16 bits
* [Contenu] Formes inattendues lors de l’utilisation du nœud « Biseau » d’angular sans mosaïque sur les petites formes
* [Bibliothèque] Les icônes pour sbsar ne sont pas visibles dans la bibliothèque
* [Bibliothèque] L’utilisation de « \ » pour filtrer l’URL ne fonctionne plus
* [Bibliothèque] Les valeurs de filtre sont sensibles à la casse.
* Le filtre de recherche [Bibliothèque] ne fonctionne pas lorsque l’option « Composition » est cochée
* [Bakers] Si vous double-cliquez sur des cellules spécifiques et que vous ignorez la modification, elles reprennent des valeurs incorrectes
* [Bakers] Le texte d’état du serveur principal dans la fenêtre Bakers affiche toujours « Accélération GPU : activer »
* [Cooker] Blocage lors du traitement d’une dépendance « imposteur » dans un graphique
* [Cooker] la conversion en niveaux de gris a une taille de sortie incorrecte lors de l’utilisation de la valeur
* [Explorer] Blocage lors du traitement de « Publish sur le partage »
* [Graphique] Blocage lors de l’ouverture d’un pack spécifique
* [MDL] Blocage lors de l’utilisation de l’opérateur cast
* [Modèles] Les identificateurs de sortie ne sont pas corrects dans le modèle recouvert PBR

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
* [Vue 3D] Anisotropie de la prise en charge
* [Vue 3D] Effet de revêtement de support
* [Vue 3D] Prise en charge de la diffusion sous la surface
* [Graph] Nœud point
* [Graphique] Optimisation du rendu des graphiques en mettant en cache les résultats de cuisson
* [Préférences] Remplacez la valeur par défaut « Cooking Size Limit » par 8192
* [Préférences] Ajoutez un bouton à bascule pour activer/désactiver la nouvelle fonctionnalité de touche de tabulation
* [API] Méthode Add SDResource.getPackage()
* [Iray] Mise à jour du SDK NVIDIA Iray RTX 2019.1.3 (317500.3714)
* [Explorer] Autoriser à lier tout type de fichier en tant que ressource dans le package
* [GradientNode] Appuyez sur Échap pour annuler le choix du dégradé
* [Paramètres] Supprimer les majuscules automatiques sur les identificateurs
* [Projet] Ajoutez une option pour spécifier si les graphiques et les ressources sont « visibles dans la bibliothèque » par défaut
* [Paramètres prédéfinis] Épingler automatiquement les paramètres modifiés

**Fixe :**

* [MDL] Impossible d’exporter le module en raison d’un problème de type de paramètre
* [MDL] L’entier exposé n’est pas visible lors du chargement
* [MDL] Blocage survenant lors de l’exportation MDL
* [MDL] Blocage lors de la modification de la couleur d’un nœud de surface de matériau
* [MDL] void MDLGraphNodeControllerSelector::updateSelectorCurrentMember(const DataMessage&amp; msg) est rompu
* [Graphique] thickness de lien incorrect dans l’affichage du graphique
* [Graphique] Trop d’invalidations sont déclenchées lors de l’ajustement des paramètres.
* [Graphique] Blocage lors de la fermeture d’un pack alors que deux fenêtres de celui-ci sont ouvertes et lors de l’utilisation de l’édition contextuelle
* [Graphique de fonction] L’avertissement n’apparaît pas lors de la fermeture de la vue de fonction
* [Vue 3D] Blocage lors de l’initialisation de la vue 3D lorsque la projection de la caméra est définie comme « orthographique » comme état de scène par défaut
* [Vue 3D] La fonction DOF post-effets reste activée en Iray
* [Vue 2D] La fenêtre de sélection du pinceau disparaît lors de la modification de l’épaisseur du pinceau
* [Vue 2D] Panneau Informations : les valeurs sont recadrées selon une disposition spécifique
* [Vue 2D] L’image est décalée lors de la réduction et de la restauration de la fenêtre principale
* [Boulangers] La liste de sélection « De la ressource » n&#39;est pas filtrée correctement
* [Boulangers] Blocage lors de l’enchaînement des boulangers « Color Map from Mesh » et « Normal Map from Mesh » sur Embree
* [Boulangers] La courbure par sommet résulte en artefacts sévères
* [Explorateur] Impossible d’importer les ressources UDIM par glisser-déposer dans l’explorateur
* [Explorer] La fenêtre de l’Explorateur n’est pas correctement filtrée lors de la liaison de maillages et de polices après la liaison de formats de fichiers inhabituels
* [Explorateur] Les ressources sont visibles lorsque l’option « afficher dans la bibliothèque » du graphique est définie sur « non »
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
* [Paramètres] Blocage lors de l’exposition des paramètres
* [Paramètres] Blocage après avoir recréé un nouvel élément dans la liste déroulante
* [Export] Échec de l&#39;exportation par lots 8K
* [Paramètres prédéfinis] Blocage lors de l’application d’un paramètre prédéfini impliquant des booléens dans des instances SBS
* [Scripting] L’écran « Bienvenue » apparaît toujours lors de l’utilisation de l’argument de ligne de commande « —quit »

### 9.1.3 (2019.1.3)

*(Publié Le 19 Août 2019)*

**Fixe :**

* [Boulangers] Blocage dans DXR lorsque les rapports L/H de la sortie du boulanger et de la carte d’inclinaison ne correspondent pas
* [Boulangers] Le boulanger « Occlusion ambiante à partir d&#39;un filet » génère des résultats incorrects avec Optix ou DXR lors de l&#39;utilisation d&#39;une carte de normales
* [Boulangers] Le boulanger « Courbure » génère des résultats incorrects lors de l’utilisation du paramètre « Par sommet »
* [Bakers] Les messages d’erreur indiquent le back-end qui a échoué au lieu de la cause de l’erreur
* [Boulangers] Blocage lors du traitement d&#39;un boulanger de carte de détail sans maillage poly élevé
* [Bakers] Le mappage incliné ne semble pas affecter toutes les sorties avec DXR activé
* [Content] mg\_leaks : faute de frappe dans le nom des paramètres
* [Contenu] « Forme » renvoie un avertissement de cuisson
* [Contenu] Les polygones 1 et 2 ne prennent pas en charge les fonctions aléatoires
* [Contenu] Les polygones 1 et 2 peuvent avoir moins de 3 côtés
* [Contenu] Normal à l’Height HQ ne fonctionne pas correctement dans un format non carré
* [Paramètres] Paramètres d&#39;entrée d&#39;entier : la liste déroulante n&#39;affiche pas les valeurs

### 9.1.2 (2019.1.2)

*(Publié Le 2 Juillet 2019)*

**Fixe :**

* [Vue 3D] L’exportation de la vue 3D avec la profondeur de champ activée semble incorrecte
* [Vue 3D] La couche Alpha des images PSD est incorrecte lors de l’utilisation du rendu d’enregistrement
* [Vue 3D] Le PNG et le PSD sont rompus lors de l’utilisation de l’option de rendu Enregistrer avec Iray
* [Vue 3D] Le format dds ne fonctionne pas lors de l’enregistrement du rendu
* [Graphique] Les nœuds sont décalés lors de la combinaison des clics droit et gauche de manière spécifique
* [Graphique] La modification d’instances de fonction ne met plus à jour le résultat du nœud
* [Graphique] Blocage lors de l’affichage du menu de la barre d’espace
* [Contenu] Extrusion de forme : problème de qualité lorsque la forme n’a pas de rotation.
* [Contenu] L’ombre portée de forme (et les niveaux de gris) ne produit pas d’ombre sans mosaïque H et V
* [Contenu] Problème de recadrage normal de la matière
* [Boulangers] Les boulangers JSON prédéfinis ne sont pas chargés correctement
* [Boulangers] Blocage lors de la cuisson de maillages lourds à l&#39;aide d&#39;Optix ou DXR (maintenant, il peut échouer en raison d&#39;une Vram insuffisante, mais il ne se bloquera pas)
* [Éditeur de bitmap] Les outils de peinture bitmap décalent les contours et les redessinent dans le cadre de sélection des contours
* [Éditeur de bitmap] Outils de peinture bitmap rompus dans OSX
* [UI] Le menu de certains boutons est à peine accessible
* [UI] Blocage lors du glisser-déposer d’une instance de boulanger
* [SVG] Les outils de modification de SVG intégrés ne sont pas fiables
* [Paramètres] Blocage lors de l’application d’un paramètre prédéfini avec des paramètres booléens dans une instance SBSAR
* [Réseau] Blocage parfois lorsqu’une erreur se produit dans une connexion chiffrée SSL

### 9.1.1 (2019.1.1)

*(Publié Le 28 Mai 2019)*

**Ajouté :**

* [Intégration Python] Enregistrement et restauration de l’état du gestionnaire de plug-ins
* [Préférences][Dépendances] Ajoutez une option pour déterminer comment le chemin du fichier de dépendances est stocké
* Mappeur de Flood Fill [Content] : ajout d’une option « Adapter la forme BBox »

**Fixe :**

* [Contenu] Mappeur de Flood Fill : « Rotation Auto Scale » a l’effet inverse
* [Contenu] L’entrée « luminance\_offset\_map » n’est pas utilisée par « Flood Fill Mapper Color »
* [Contenu] Le nœud « Niveaux de gris du mappeur de Flood Fill » génère des artefacts d’étape
* [Content] Impossible de publier l&#39;Height Extrude
* [Paramètres] Les paramètres prédéfinis incorporés dans sbsar ne sont pas chargés dans Designer
* [Boulangers] Le nom du boulanger ne s&#39;affiche pas correctement dans la liste des boulangers
* [Vue 3D] « Afficher les sorties en vue 3D » ne fonctionne pas pour les valeurs
* [Cooker] Blocage lors de la correction d’un type de paramètre incorrect
* [API] La fonction SDResource.setInputPropertyFromId ne fonctionne pas sur les paramètres d&#39;entrée SDSBSCompGraph
* [Updater] certains sbs ne peuvent pas être mis à jour en 2019
* [Explorer] Blocage lors de l’importation d’un fichier .obj spécifique
* [Intégration Python] Les barres obliques inverses ne s&#39;affichaient pas correctement sous Windows lors de l&#39;initialisation de PYTHONPATH
* Problème de valeur [UI] avec certains curseurs dans les boulangers
* [Linux] Designer ne peut pas être exécuté sous CentOS &lt; 7.6

### 9.1.0 (2019.1.0)

*(Publié Le 9 Mai 2019)*

**Ajouté :**

* [API] Ajoutez le paramètre « updatePackages » à la méthode SDPackageMGR.loadUserPackage() pour contrôler si les programmes de mise à jour doivent être appliqués ou non lors du chargement
* [API] Ajout de la possibilité de déconnecter une connexion SDConnection
* [API] Ajout de la classe SDSBSARExporter pour publier un package SDP
* [API] Ajoutez la classe SDHistoryUtils pour gérer les commandes annulables.
* [API] Ajout d’une définition de nœud d’entrée en niveaux de gris dans le graphique de composition de Substances (sbs::compositing::input\_grayscale)
* [API] Ajout d’une valeur à la définition du nœud d’entrée dans le graphique de composition de Substances (sbs::compositing::input\_value)
* [API] Méthode Add SDProperty.isFunctionOnly()
* [API] Ajout de la prise en charge du paramètre d’entrée personnalisé sur SDSBSCompNode
* [API] Ajoutez le paramètre reloadIfModified à la méthode SDPackageMGR.loadUserPackage() pour contrôler si un package doit être rechargé en cas de modification
* [API] Méthode Add SDPackageMgr.getPackages()
* [API] Ajout de la possibilité d’obtenir/d’ajouter/de supprimer des chemins racines de SDModuleMgr
* [API] Permet d’obtenir le pointeur du tampon de pixels et la hauteur de ton d’une texture SDT
* [API] Autoriser à récupérer le pointeur de la fenêtre principale
* [API] Permet de créer des menus personnalisés dans le menu principal
* [API] Autoriser à créer des DockWidgets personnalisés dans la fenêtre principale
* [API] Utilisation des noms d’objet pour rechercher des menus dans les barres d’outils
* [API] Fournir un système permettant de gérer les notifications d’application à l’API
* [Intégration Python] Ajout d’une variable d’environnement par défaut pour rechercher les plug-ins Python
* [Intégration Python] Ajout de la recherche de texte et remplacement dans l’éditeur Python
* [Intégration Python] Instanciation des plug-ins Python au démarrage
* [Intégration Python] Prise en compte de la variable d’environnement PYTHONPATH
* [Intégration Python] Autoriser la création de barres d’outils dans les widgets de graphique
* [Intégration Python] Prise en charge des threads Python
* [Intégration Python] Ajout d’un gestionnaire de plug-ins (dans le menu Outils )
* [Contenu] Rotation vectorielle normale : ajoutez une entrée d’image facultative pour déterminer l’angle
* [Contenu] Nouveau filtre Min/Max
* [Contenu] Nouveau filtre « Flood Fill vers index »
* [Contenu] Nouveau filtre « Mappeur de Flood Fill »
* Filtre Nouvel Atlas splitter [Contenu]
* [Contenu] Amélioration du filtre Triplan
* [Contenu] Nouveau filtre de Non Uniform Directional Warp
* [Contenu] Nouvelle déformation multidirectionnelle
* [Contenu] Nouveau filtre d’Height Extrude
* [Moteur] Fxmap : nouveau modèle « Grading with offset »
* [Engine] Prise en charge du traitement de la valeur uniforme (nœud Nouveau processeur de valeur)
* [Vue 3D][Bakers] Améliorer les performances du chargeur OBJ
* [Vue 3D] Augmentez les distances des plans de l’élément de caméra
* [Préférences] Ajouter des paramètres pour Bakers
* [Graphique] Accélérez l’invalidation en évitant les comparaisons de chaînes
* [MDL] Prise en charge des baies MDL
* [UI] Améliorations de l&#39;interface utilisateur de sélection du moteur
* [IRay] Mise à niveau vers IRay SDK 2018.1.4
* [Gestionnaire de dépendances] Utiliser le « dernier chemin » lors de la relocalisation d’une ressource
* [Cuisine] Ajouter la prise en charge des étiquettes booléennes dans la barre oblique
* Intégration de Qt 5.12.2

**Fixe :**

* [Graphique] Les connexions sont rompues lors de la modification du nom de l’entrée
* [Graphique] Trop d’invalidations sont déclenchées lors de l’ajustement des paramètres.
* [Graphique] L’action « Copier dans le Presse-papiers » ne fonctionne pas si nous faisons un clic droit sur un badge
* [Graphique] Le déplacement d’une image à l’aide d’Alt n’est pas stocké dans le fichier .sbs
* [MDL] Le profil colorimétrique n’est pas automatiquement mis à jour dans l’éditeur MDL
* [MDL] blocage lors de l’exportation d’un module contenant une configuration spécifique
* [MDL] Impossible d’exporter un graphique MDL contenant un profil clair ou une ressource MBSDF
* [UI] Les raccourcis ne s’affichent plus dans les menus contextuels
* [UI] La fenêtre flottante devient ancrable après le redémarrage
* [Scripting] L’option Annuler ne fonctionne pas dans l’éditeur Python
* [Scripting] L’option « oui à tout » dans le menu Enregistrer ne fonctionne pas
* La liste déroulante [Paramètres] ne s’affiche pas correctement après la copie
* [Explorer] La relocalisation des ressources doit ouvrir le dernier chemin relocalisé par défaut
* [Bibliothèque] Le contenu de la bibliothèque est toujours reconstruit lors du passage d’une version à une autre
* [Bibliothèque] Les bitmaps importés sont invalidés lors de l’enregistrement
* [IRay] L’espace tangent n’est pas calculé correctement / mappage normal incorrect
* [Fonction] Blocage ou échec lors de la création d’un graphique à partir de la sélection
* [API] la valeur par défaut des propriétés n’est pas définie

## Version 8

### 8.3.4 (2018.3.4)

*(Publié Le 12 Avril 2019)*

**Ajouté :**

* [Contenu] Transformation normale/Transformation de matière : ajoutez une option pour activer la transformation Échelle et Inclinaison

**Fixe :**

* [Contenu] Le filtre Tourbillon ne fonctionne pas correctement lorsque des fonctions aléatoires sont utilisées dans les fonctions de paramètres
* [Contenu] Transformation normale/Transformation de matière : la normale n’est pas normalisée après une transformation d’échelle
* [Contenu] Le tourbillon donne des résultats incorrects lorsque la quantité est aléatoire
* [Graphique] Blocage lorsque vous faites glisser une sortie tout en maintenant la touche Maj enfoncée, puis que vous passez à Ctrl en faisant glisser
* [Graphique] Blocage lors de la manipulation de points de fractionnement
* [Graphique] Baisse des performances lors de l’affichage des badges de nœud
* [Scripting] L’utilisation d’actions personnalisées peut se bloquer après 30 secondes.
* [Préférences/Projets] Les scripts activés de tous les projets doivent être exécutés (dans la section « Scripts »).
* [MDL] blocage lors de la liaison d’un graphique MDL à un autre graphique MDL
* [Paramètres] Les nœuds ne sont pas mis à jour après avoir défini la valeur de départ aléatoire du graphique sur un paramètre exposé
* [PSD] L’affectation d’un nœud de couleur modifie la taille des vignettes de calque, contrairement à l’affectation d’un nœud en niveaux de gris
* [API] Exception non gérée avec SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Publié Le 19 Février 2019)*

**Fixe :**

* [Contenu] Les sorties de Matériau de base PBR n&#39;ont pas le bon nom de groupe

### 8.3.2 (2018.3.2)

*(Publié Le 19 Février 2019)*

**Ajouté :**

* [Bakers] Ajouter un libellé indiquant le paramètre de suffixe actuel pour « Match By Name »

**Fixe :**

* [Graphique] Blocage lors de la manipulation de points de fractionnement
* [Graphique] Problème d’invalidation lorsque la profondeur de bit du nœud d’entrée est modifiée
* [Graphique] Les options de calcul des vignettes ne fonctionnent plus
* [Graphique] Un espace vide est affiché sous le chemin de navigation avec une disposition d’interface utilisateur spécifique
* [Graphique] Le style de lien est incorrect dans le contexte
* [Graphique] Les vignettes ne s’affichent pas correctement dans les graphiques de fonction/mdl sur les écrans Hi DPI
* [Contenu] Couleur de fusion des éclaboussures de forme : aucune option pour spécifier le format de map normal
* [Contenu] Erreur d’orthographe dans l’info-bulle d’interpolation linéaire
* [Content] La transformation normale ne gère pas correctement la transformation en miroir et inclinée
* [Contenu] Les dégradés axiaux, radiaux et circulaires ne prennent pas en charge les fonctions aléatoires
* [Contenu] Le dégradé radial ne fonctionne pas correctement dans un format non carré
* [API] output\_exporter.sbs doit toujours être mis à jour lors de l’utilisation du script export\_output
* [API] Blocage après utilisation du script export\_output
* [API] Impossible de définir la valeur numérique des annotations sur les entrées du graphique de composition
* [Explorer] Blocage aléatoire lors de l’enregistrement d’un projet
* [Explorer] Impossible d’ouvrir les fichiers .sbs avec une extension en majuscules
* [UI] La taille de la fenêtre « Nouvelle Substance » n&#39;est pas persistante
* [UI] Le menu contextuel sur l&#39;instance de fonction n&#39;est pas cohérent avec le graphique de composition
* [Boulangers] Blocage lors de l’ouverture des boulangers sur un maillage spécifique
* [Boulangers] Mauvais calcul pour les boulangers DXR lorsque les UV ont une valeur d&#39;ordonnée de 0
* [Updater] Blocage lors de l’annulation du programme de mise à jour
* [Vue 3D] Les UV de la sphère primitive sont décalés de 1 unité
* [Cooker] Tramage aléatoire lors de la cuisson d’images bitmap
* [Lecteur] Les boutons de commande des fenêtres sont petits
* [Lecteur] Les icônes des boutons ne fonctionnent plus

### 8.3.1 (2018.3.1)

*(Publié Le 20 Décembre 2018)*

**Ajouté :**

* [API] Ajouter SDConnection.getOutputProperty() et SDConnection.getOutputPropertyNode()
* [API] Ajout d’un document sur toutes les définitions de ressources
* [API] Pour des raisons de cohérence, remplacez la propriété d&#39;annotation SDSBSCompNode « visible if » par « visible\_if »

**Fixe :**

* [Graphique] Appuyer une deuxième fois sur la touche TAB ne ferme pas le menu Nœud
* [Graphique] Les badges Vue 3D ne fonctionnent pas correctement dans certaines situations
* [Graphique] Les packages en lecture seule peuvent être modifiés
* [Boulangers] La barre de progression agit de manière étrange lors du chargement d&#39;un maillage poly très élevé
* [Boulangers] Artefacts sur le maillage avec normales orientées vers l’intérieur
* [Bakers] Le widget de sortie et de paramètres Bakers ne peut pas être réduit
* [Explorer] Les ressources 3D sont chargées lorsqu’un pack est ouvert
* [CmdLineArgs] « —news hide\_changelog:true » ne fonctionne plus

### 8.3.0 (2018.3.0)

*(Publié Le 5 Décembre 2019)*

**Ajouté :**

* [Graphique] Ajouter un chemin de navigation lors de la modification des sous-graphiques / fonctions
* [Graphique] Ajouter une tabulation comme raccourci pour générer le « menu des nœuds »
* [Graphique] Surligneur de nœud pour les nœuds parents de la sélection
* [Graphique] Ajoutez Ctrl+E comme raccourci pour ouvrir la fonction et les sous-graphes du processeur de pixels
* [Graphique] Connecter le nouveau nœud à la première sortie visible du nœud sélectionné
* [Graphique] Ajouter des badges de nœud
* [Graphique] Ajouter un avertissement sur les nœuds de composition via des badges
* [Graphique] Ajouter la possibilité de rechercher un nœud par son nom, ses attributs ou son UID
* [API] Autoriser à créer et à modifier des données
* [API] Autoriser l’exportation de SDPackage et de SDMDLGraph vers des modules MDL (voir SDMDLExporter)
* [API] Permet de récupérer tous les nœuds, énumérations et définitions de structure (voir SDModuleMgr)
* [Vue 3D] Basculer vers les cubemaps pour le rendu OpenGL
* [Vue 3D] Exporter une image Hdr linéaire lors de l’enregistrement en .exr ou .hdr
* [Bakers] Intégration de la technologie de lancer de rayons DXR
* [IRay] Intégration du SDK IRay 2018.1
* [Moteur] Prise en charge du moteur SSE (CPU) pour le traitement d’image en virgule flottante hdr
* [Engine] Ajoutez une option de ligne de commande (—gpu x) pour spécifier le périphérique GPU dédié au moteur de Substance
* [Contenu] Nouveau nœud de Rendu PBR
* [UI] Onglets de retouche et barre de titre
* [Gestionnaire de dépendances] Empêcher la mise à jour de la liste des dépendances lorsque les actions utilisateur n&#39;affectent pas les dépendances

**Fixe :**

* [Graphique] Blocage lors de l’instanciation d’un graphique sur lui-même
* [Graphique] Le nœud dupliqué n&#39;est pas sélectionné
* [Graph] problème de calcul lors de l’utilisation d’une même instance de nœud dans 2 graphiques MDL différents
* [Graphique] la touche Z doit centrer la vue au centre de la zone de scène
* [Graphique] Ignorer l’espace colorimétrique dans les règles de connexion lors de l’utilisation de lien de matériau
* [Graphique] Évitez d’ouvrir les sorties en mode 3D lors de l’ouverture d’un graphique dans conli
* [Graphique] Le collage des nœuds est lent lorsque l’option « Ouvrir le nœud nouvellement créé » est activée
* [Vue 3D] Affirmation lors du glisser-déposer d’un filet spécifique
* [Vue 3D] L’option Échelle UV activée ne fonctionne pas sur la carte d’height
* [Contenu] Tri-planaire : divers problèmes concernant l’axe et les transformations
* [Contenu] Flou de Pente Niveaux de gris : l’un des échantillons n’a pas le mode de fusion approprié lors de l’utilisation de min ou max
* [Contenu] Dégradé linéaire 2 mauvais résultat en basse résolution
* [API] SDPackage.findResourceFromUrl() peut également récupérer des ressources situées dans un autre SDPackage
* [API] SDPackage.getChildrenResources() renvoie toujours le premier élément en mode non récursif
* [API] [Documentation] Les énumérations, structs situés dans le dossier « généré » ne sont pas reflétés dans la documentation
* [UI] La largeur de la vue 2D ne doit pas être contrainte
* [Dégradé] Blocage lors de l’utilisation de Mac
* [Explorer] Blocage lors de la fermeture et de la réouverture d’un graphique
* [Mac] Le sélecteur de couleurs ne fonctionne pas sur plusieurs écrans
* [Paramètres] La zone de rotation sur les paramètres entiers ne fonctionne pas
* [Cooker] Blocage lors de la création de certains nœuds sous OSX 10.13
* [Filtre de courbe] Les touches et les points de contrôle peuvent se retrouver avec une valeur -0,0 ou une valeur bizarre « presque zéro » dans l’éditeur de courbe
* [Vue 2D] Le widget Position n&#39;est pas disponible pour les graphiques provenant de sbsar
* [PSD] Problème de calque après l’exportation avec des dépendances

### 8.2.2 (2018.2.2)

*(Publié Le 4 Octobre 2019)*

**Fixe :**

* [Contenu] L’ombre de la forme ne fonctionne pas correctement lorsque la mosaïque est désactivée
* [Contenu] Le remplissage par diffusion aléatoire en niveaux de gris/couleur ne fonctionne pas correctement dans certains cas
* [Contenu] Le Flood Fill est incorrect dans les caractères non carrés
* [Contenu] Le Flood Fill de Couleur/Niveaux de gris est rompu
* [Contenu] QuadTransform est irrégulier dans le processeur
* [Contenu] La forme en étoile génère un mode de mosaïque Sans mosaïque
* [Contenu] Couleur de mélange de formes éclaboussées avec résolution absolue de 32f bits
* [Contenu] La couleur de fusion des éclaboussures de forme est longue à calculer si son format n’est pas défini sur 32F
* [Graphique] Blocage lors de la liaison d’une image en tant qu’entrée d’une Fx-Map lorsque les propriétés Itérer sont affichées
* [Graphique] Le minutage semble incorrect lors de l’édition du graphique en contexte
* [Graphique] Blocage aléatoire lors de l’enregistrement du graphique
* [Graphique] le mode Matériau ne fonctionne pas avec sbsar
* [Vue 3D] L&#39;affectation de matière n&#39;est pas restaurée correctement
* [Vue 3D] Certains paramètres du fichier d’état de vue 3D ne sont pas chargés correctement
* [Vue 2D] L&#39;affichage de l&#39;Alpha est toujours noir
* [Vue 2D] Le bouton Afficher l’image en niveaux de gris ne fonctionne pas pour les images avec alpha
* [UI] Le gestionnaire de dépendances apparaît au démarrage même lorsqu’il n’est pas activé sur Mac
* [UI] Certains boutons effectuent des actions même lorsque vous relâchez la souris à l’extérieur
* [API] Blocage lors de la tentative de maintien d’un élément de tableau en dehors de la portée du tableau d’où il provient
* [Graphique MDL] L’aperçu du nœud est inversé
* [Graphique MDL] Le Displacement du nœud de prévisualisation est différent de celui de la vue 3DV
* [Console] Les performances sont très lentes lorsque la console contient de nombreux messages
* [Console] Alertes Qt lors du lancement de Designer sous CentOS
* [FX-Map] Blocage lors de la suppression des liens entre les entrées et FX-map
* [Functions] Impossible de définir un nœud de type chaîne comme sortie dans la ressource de fonction
* [Préférences] Le menu Préférences n’est pas activé. L’utilisateur peut accidentellement modifier une valeur lors du défilement
* [FX-Map] La zone de liste déroulante Index d&#39;image d&#39;entrée n&#39;est pas mise à jour correctement lors de l&#39;ajout/la suppression d&#39;entrées
* [Dépendances] Blocage lors de la suppression de ressources UDIM utilisées dans un graphique
* [API] SDLocationContext.getCurrentGraph() renvoie toujours la valeur null
* [Publish] URL de Substance Player de la page de téléchargement incorrecte

### 8.2.1 (2018.2.1)

*(Publié Le 17 Août 2018)*

**Ajouté :**

* [UI] Ajoutez un message dans la barre des tâches lorsque l’option « Édition contextuelle » est activée
* [Préférences] Reformulation de l’étiquette de l’option « Modification contextuelle »

**Fixe :**

* [Graphique] Le raccourci Coller sans lien ne fonctionne pas dans le graphique de composition
* [Graphique] L’invalidation est très longue lorsque l’édition contextuelle est activée
* [Graphique] Blocage lors de la liaison de nœuds
* [Graphique] Blocage lors du rétablissement de la liaison des nœuds
* [Graphique] Blocage d’images en mouvement
* [Graph] Blocage lors du changement de fichier UVT dans le graphe et le maillage n’est plus udim
* [Graphique] Blocage lors de l’utilisation de ctrl+z après le collage des nœuds
* [Graphique] La sélection des nœuds parents est très lente
* [Bakers] Le déplacement de cartes vers le haut/vers le bas permet à l’utilisateur de redimensionner la ligne
* [Bakers] Le chemin pour enregistrer ou charger le paramètre prédéfini n’est jamais enregistré
* [Boulangers] Cage est utilisé même lorsqu&#39;il n&#39;est pas sélectionné dans la fenêtre de cuisson
* [Boulangers] La correction de l’inclinaison ne fonctionne pas correctement
* [Boulangers] Performances très lentes lorsque l&#39;espace UV négatif est dans la vue
* [Bakers] Cliquer sur le bouton Annuler n&#39;annule pas le chargement du maillage
* [Boulangers] Impossible d&#39;utiliser une cage si la carte d&#39;inclinaison est vide et définie sur true
* [Contenu] Le Flood Fill est lent en 4K
* [Contenu] La fonction Linéaire à sRVB est rompue
* [Contenu] Carreau Arrière-plan aléatoire en niveaux de gris piloté par un flotteur4 au lieu d’un flotteur, empêche la cuisson
* [Contenu] Éclaboussure de forme : le multiplicateur de position/mappage vectoriel ne fonctionne pas correctement
* [Scripts] Ctrl + o ne fonctionne pas dans l’éditeur Python
* [Scripting] L’éditeur Python envoie des invites même après la fermeture
* [Scripting] Blocage lors de la création de plusieurs nouveaux scripts
* [UI] Les icônes de la bibliothèque sont pixellisées
* [UI] Les panneaux flottants par défaut se comportent mal
* [Explorer] Blocage lors de l’importation d’un filet sur CentOS
* [Explorer] Le maillage UDIM est chargé deux fois
* [Cooker] Aucune durée pour les nœuds dans le contexte
* [Cuisinière] Débordement d&#39;empilement lors de la cuisson
* [Licence] Authentification incorrecte avec des informations d’identification valides
* [Licence] Licence flottante signalée plusieurs fois pour le même utilisateur
* [Vue 3D] La valeur V par défaut du matériau de carreau UV est incorrecte
* [Vue 3D] Régression des performances par rapport à 2018.1.x
* [Préférences] Blocage lors de l’utilisation d’un fichier de configuration depuis un serveur
* [Bibliothèque] Blocage lors de la suppression d’un filtre dans la bibliothèque
* [SVG] Problème de dépendance lors de l’utilisation de l’alias
* [Niveaux] Les bitmaps HDR 32 bits font clignoter l’éditeur de niveau lors du déplacement de la position des widgets
* [PSD] La fenêtre du PSD d&#39;importation lié s&#39;affiche deux fois
* [Iray] La scène est mise à jour lorsqu’un éclairage désactivé est modifié
* [MDL] Blocage lors de la suppression de tous les nœuds d’un modèle MDL
* [Moteur] Une grande quantité de décalage dans FX-Map peut bloquer le SD
* Crashpad se bloque au démarrage
* La variable d’environnement Python bloque Designer au lancement

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
* [Contenu] Transformation de la matière : ajout de la prise en charge des cartes de normales pivotées
* [Contenu] Nouveaux filtres Rotation vectorielle normale et Transformation normale
* [Contenu] Normaliser : améliore la qualité des résultats.
* [Contenu] Nouveau filtre Transformation trapézoïdale
* [Content] Nouveau filtre Quad Transform
* [Contenu] Ajout d’un motif hémisphère au nœud Shape
* [Contenu] Ajout de nouveaux dégradés avec des commandes dans la vue 2D
* [Contenu] Ajouter une sortie UV au nœud « Cube GBuffers »
* [Graphique] Cadre : ignore le texte du titre plus grand que la zone de cadre pour la sélection
* [Graphique] Prise en charge de l’édition contextuelle des sous-graphiques (expérimentale)
* [Graphique] La création d’un cadre/commentaire doit affecter le nœud sous le curseur lors de l’utilisation du RMB
* [Graphique] Cadre : ignore le texte du titre plus grand que la zone de cadre pour la sélection
* [Graphique] Réutiliser l’onglet existant lors de l’ouverture d’une fonction déjà ouverte
* [Graphique] Créer un nouvel onglet lorsque « Ouvrir la référence » est utilisé
* [Graphique] Fonction : n’affichez pas les propriétés de la fonction lorsque vous cliquez sur l’arrière-plan
* [Paramètres] Supprimer le bouton « Exposer » des graphiques fxmap
* [Paramètres] Niveau : Ajouter un bouton « Inverser »
* [Paramètres] Développez le groupe « Paramètres d’entrée » lors de la création d’un nouveau paramètre d’entrée.
* [Properties] Ajout des informations d’URL de package dans les attributs de graphe
* [Propriétés] Augmentez la taille du champ de description pour les nœuds de sortie
* [Propriétés] Autoriser à entrer la fonction par pixel du processeur de pixels même pour les packs en lecture seule
* [Script] Nouvelle API Python / Éditeur Python (première itération)
* [Bakers] Optimisation du transfert de géométrie pendant le rendu
* [Vue 3D] Passer au profil de base OpenGL
* [Vue 3D] Prise en charge de la tessation/du displacement sur Mac
* [Fonctions] Ressource de fonction : répertorie les entrées d’image dans les nœuds d’échantillonnage

**Fixe :**

* [Graph] blocage lors de la liaison d’un nœud à un autre
* [Graphique] l’obtention de variables dans la fonction de générateur aléatoire de graphiques ne fonctionne pas
* [Graphique] blocage lors du glisser-déposer de bruit dans un graphique
* [Graphique] blocage lors de l’ouverture d’un graphique spécifique
* [Contenu] Le résultat est différent entre Couleur aléatoire des carreaux et Niveaux de gris
* [Contenu] Mosaïque aléatoire : le résultat change lors de la modification du « Mode aléatoire de symétrie »
* [Contenu] La détection des contours ne fonctionne pas avec des résolutions non carrées
* [Boulangers] Artefacts lors du boulonnage de courbure à l’aide d’un filet UDIM
* [Bakers] La carte d&#39;Occlusion ambiante du maillage est inversée lors de l&#39;utilisation d&#39;une carte normale
* [Bakers] La liste des jeux UV doit être restreinte aux jeux UV disponibles
* [Explorer] blocage lors de la suppression de ressources lors de la restauration
* [Transform2D] Blocage lors de l’exposition du niveau de mappage Mip et des paramètres de couleur d’arrière-plan
* [Transform2D] Comportement incorrect lors de l’exposition d’un Niveau du mipmap de transformation
* [PSDExport] L’exportateur de PSD n’exporte pas correctement les niveaux de gris 32F
* [Vue 2D] Le calcul de l&#39;histogramme ne fonctionne pas avec les nœuds 16F
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

* [Vue 3D] Permet de définir l’état d’éclairage par défaut dans les paramètres du projet
* [Version Control] Supprimer le délai d’expiration de 30 s lors de l’appel des scripts python

**Fixe :**

* [Contenu] Base de Somme fractale : résultat incorrect avec le troisième niveau (un nouveau graphique a été ajouté)
* [Contenu] 3D Perlin Noise Fractal est forcé à 32 bits
* [Contenu] Le dégradé linéaire 3 ne donne pas le bon résultat lors de l&#39;utilisation d&#39;une taille non uniforme
* [Contenu] Sobel normal ne prend pas en charge les options de mosaïque
* [Contenu] Le vérificateur\_1 est forcé à 8 bits.
* [Content] Multiangle vers Normal : problème de calcul interne
* [Contenu] Le modèle Stripe ne prend pas en charge les valeurs négatives « Maj » (blocage du moteur).
* [MDL] Blocage lors de la tentative d’ouverture d’un projet MDL spécifique
* [MDL] Le graphique MDL n&#39;est pas calculé après une opération fermée/rouverte
* [Exporter] Les sorties des graphiques non attribués sont exportées à l’aide de l’outil de traitement par lots
* [Export] L&#39;exportation de C16F dans exr génère une image en niveaux de gris
* [Boulangers] Les fonctions d’inclinaison ne sont pas désactivées dans l’interface utilisateur lors de la cuisson avec une cage
* [Boulangers] Blocage lorsque la cage n&#39;a pas de réglage UV correspondant
* [Cooker] sbscookie : erreur de cuisson liée à « blend\_switch.sbs »
* [Cooker] Le graphique publié ne s’affiche pas correctement
* [Moteur] Transformation 2D : couleur de cache incorrecte
* [Explorer] Blocage lors de la réimportation d’un filet FBX
* [Color Widget] Le sélecteur de couleurs en niveaux de gris sélectionne uniquement la valeur de la couche rouge
* [Vue 3D] L’utilisation de « textcoordN » ne fonctionne plus
* [Iray] La texture normale est appliquée deux fois pour les diélectriques

### 8.1.1 (2018.1.1)

*(Publié Le 12 Avril 2018)*

**Ajouté :**

* [Vue 3D] Définissez la plage par défaut du « Facteur de tessélation » sur [0, 16]

**Fixe :**

* [Vue 3D] Artefact visuel étrange avec un GPU AMD spécifique
* [Vue 3D] Gel avec des GPU AMD spécifiques
* [Vue 3D][Bakers] Les normales générées à partir de .obj ont des bords nets sur la couture UV
* [Vue 3D] Blocage lors du calcul des harmoniques sphériques
* [Boulangers] Impossible de définir la ressource comme « incorporée »
* [Boulangers] plantage lors de la cuisson
* [Bakers] La cuisson de 2 versions différentes d&#39;une carte à partir d&#39;un maillage UDIM est rompue
* [Bakers] blocage lors du basculement entre le graphique contextuel et non contextuel
* [Boulangers] Avoir le même boulanger deux fois les fera synchroniser
* [Bakers] renommer la macro $(custom) empêche la cuisson correcte
* [Boulangers] L’actualisation d’une map bakée devrait bloquer l’interface utilisateur
* [Bakers] L’option Actualiser toutes les maps bakées crée des ressources vides
* [Boulangers] Appuyer sur « Entrée » pour confirmer une valeur de paramètre supprime le poly élevé
* [Contenu] Tile Generator : erreur aléatoire de rotation lorsque les valeurs X et Y sont différentes
* [Contenu] certains mappages usure/salissures contiennent des instances fantômes
* [Contenu] Cube 3D : l’utilisation de fonctions aléatoires dans les paramètres ne donne pas le résultat attendu
* [Contenu] Les bruits fractaux ne sont pas rendus correctement lorsque l’Extension non carrée est désactivée
* [Contenu] Les Cellules 2 et 4 ne se comportent pas correctement lorsque l’Extension non carrée est désactivée
* [Graphique] La mise à jour d’une instance sbsar crée un graphique fantôme
* [Graphique] L’affectation par clic droit ne doit pas afficher le sous-menu Carreaux UV pour les maillages non UDIM
* [Graphique] Le fichier sbsar republié n&#39;est pas correctement mis à jour
* [Graphique] Les nœuds ne sont pas invalidés correctement lors de la modification des ressources
* [Cooker] Le paramètre de fusion alpha prédéfini n’est pas correctement récupéré dans sbsar
* Le filtre Niveaux [Cuiseur] ne saisit pas les valeurs lorsqu’il est cuit dans une barre oblique
* [Cooker] Les transformations implicites sont effectuées avant les nœuds FX-Map
* [Explorer] Appuyer sur la touche Suppr d’un pack demande à l’utilisateur s’il souhaite le supprimer
* [Explorer][Boulangers] Problème de déplacement
* [Courbe] Blocage aléatoire lors de la manipulation des touches dans l’éditeur de courbes
* [MDL] Type de gamma mal défini pour une utilisation personnalisée
* [Paramètres] Blocage lors de l’exposition d’un paramètre avec le même identifiant qu’une entrée existante
* [Propriétés] L’utilisation de la sortie est modifiée avec une casse non sensible

### 8.1.0 (2018.1.0)

*(Publié Le 9 Mars 2018)*

**Ajouté :**

* [Boulangers] Optimiser la cuisson en polypropylène
* [Boulangers] Améliorer le résultat sur les coutures pour Curvature baker
* [Bakers] Cartes de cuisson pour filet basé sur UDIM
* [Boulangers] Ajoutez une vue 2D dédiée dans la fenêtre Boulanger
* [Graph] Prise en charge des UDIM
* [Graphique] Optimisation des performances du cuiseur
* [Graphique] Amélioration de la vitesse de génération des vignettes de nœud
* [Graphique] Conserver le cache de nœud uniquement pour les graphiques ouverts
* [Graphique] Ajoutez une barre d’outils dans le graphique de composition pour contrôler le mode de génération des vignettes
* [Vue 3D] Ajout d’une mémoire cache de géométrie pour optimiser l’affichage des maillages haute définition
* [Vue 3D] Prise en charge de l’affichage UDIM (affichage de la mosaïque actuelle)
* [Vue 3D] Mise à jour du cube arrondi avec une topologie uniforme
* [Vue 3D] Évitez d’enregistrer une scène en permanence
* [Contenu] Ajout de nœuds de bruits 3D (Perlin, Perlin Fractal, Worley, Simplex)
* [Contenu] Ajouter un nœud de masque de volume 3D
* [Content] Ajouter un nœud de 3D linear gradient
* [Contenu] Ajouter un nœud de tampons de cube 3D (utile pour prévisualiser les nœuds 3D)
* [Content] Ajouter un nœud de projection planaire 3D
* [Contenu] Ajouter un filtre Flou radial
* [Paramètres] Afficher les propriétés d’entrée/sortie de l’image dans les propriétés du graphique
* [Paramètres] Autoriser l’édition du chemin d’accès aux ressources
* [Engine] Prise en charge de textures jusqu’à 8k avec le moteur CPU (SSE2)
* [Moteur] Autoriser le convertisseur de niveaux de gris à utiliser des poids HDR pour le moteur HDR
* [Préférences] Ajout d’une option pour désactiver la création automatique de nœuds de conversion
* [Préférences] Définissez la compression par défaut pour le format png sur « vitesse maximale ».
* [UI] prend en charge le lien html dans les propriétés du graphique
* [UI] Centrez les boutons « Oui / Non / Annuler » dans la boîte de dialogue de confirmation d’enregistrement
* [Explorer] Améliorer l’affichage de la hiérarchie du filet
* [IRay] Intégration du SDK IRay 2017.1.4

**Fixe :**

* [Bakers] L’ajout d’une macro dans le champ Nom de la sortie ne l’ajoute pas à la position du curseur
* [Boulangers] Aucune matière ne s’affiche dans la liste si l’objet n’a pas de matière
* [Boulangers] Appuyez sur Entrée pour confirmer les paramètres du boulanger pour ouvrir un menu déroulant
* [Bakers] Les textures de cuisson ne doivent pas générer de commandes dans la pile d’annulation
* [Bakers] Blocage lors de la cuisson d’une texture transférée à partir d’un filet sans spécifier de texture
* [Explorer] « Enregistrer sous » doit utiliser le nom de fichier existant au lieu du nom de la première ressource
* [Explorateur] Comportement incorrect lors du glisser-déposer d’une ressource d’un package vers un autre
* [Explorer] Le clic droit de la souris ne doit pas ouvrir les données dans les propriétés
* [Explorateur] L’icône des éléments de scène n’a pas l’arrière-plan correct
* [Graphique] Ctrl + D ne fonctionne pas sous Linux
* [Graphique] La fonction de réédition de liens multiples ne branche parfois qu’un seul lien
* [Graphique] Les touches Ctrl + Maj + D doivent supprimer uniquement les liens externes, pas les liens internes.
* [Graphique] Le lien entre les niveaux de gris et la couleur est incorrect
* [Vue 3D] Impossible de définir une ressource en tant que mappage env
* [Vue 3D] Le nuanceur d’informations de maillage n’affiche pas les résultats dans le bon espace colorimétrique.
* [Paramètres] Les paramètres non exposés sont toujours exposés à l’aide de CTRL+P
* [Paramètres] Les champs de texte ne sont pas mis à jour correctement lors de l’annulation/la restauration
* [Contenu] Artefacts dans Usure/salissures Map 003
* [Contenu] L’entrée principale en niveaux de gris de la morphologie vectorielle semble incorrecte
* [Cooker] sbscookie génère une erreur lorsqu’une ressource est manquante
* [Cuisson] Blocage avec débordement de la pile lorsque la chaîne de nœuds est trop longue
* [UI] Le bouton « Quitter » dans la gestion des licences ne fonctionne pas

## Version 7

### 7.2.5 (2017.2.5)

*(Publié Le 19 Février 2018)*

**Ajouté :**

* [Contenu] Fautes de frappe dans function.sbs
* [Contenu] Réduction de la plage par défaut du bruit de perline et du bruit gaussien
* [Vue 3D] Ajuster la plage par défaut pour le paramètre « Échelle d’Height »
* [AXF] Mise à jour des modèles mdl

**Fixe :**

* [Vue 3D][Bakers] Les normales ne sont pas recalculées si le modèle n&#39;a pas de normales
* [Graphique] La ressource bitmap non carrée est vide une fois instanciée
* [Contenu] Le bruit de fonctionnement donne un résultat différent entre le processeur et le moteur GPU

### 7.2.4 (2017.2.4)

*(Publié Le 8 Février 2018)*

**Ajouté :**

* [Importation AXF] Permet de spécifier le mode de filtrage sur les bitmaps d’entrée
* [Vue 2D] Ne modifiez pas le rapport de l’image dans la vue 2D lorsque la taille physique est activée

**Fixe :**

* Blocage de [Library] lors de l’activation/la désactivation du chemin dans les préférences
* [Baker] Correspondance par nom ignore certains maillages portant des noms spécifiques
* [Contenu] Le filtre Prédéfini sur Droit supprime la couche alpha

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
* [Contenu] Certains générateurs de bruits/motifs génèrent des avertissements dans la console
* [Content] Non-Square-Transform-Grayscale génère une taille de pixel incorrecte
* [Contenu] Le filtre Tourbillon ne prend pas en compte le mode Mosaïque
* [Graphique] Le glisser-déposer de ressource bitmap vers le nœud d’entrée d’image ne fonctionne plus
* [Graphique] CTRL+R (rechargement) ne fonctionne plus
* [Graphique] Problème lors de l’utilisation d’une image dans une autre image
* [Graphique] Blocage lors du déplacement d’images contenant des épingles
* [Graphique] L’instance « Forme (héritée) » est transformée en « Forme » lors de l’enregistrement
* [Baker] blocage lors de l’utilisation de 2 images sans puissance
* [Boulangers] Couleur du filet : Polygroup, ID de sous-filet renvoient toujours une image noire
* [Bakers] AO à partir du maillage : la distance d&#39;occlusion est fixée à 1 quelle que soit la valeur d&#39;entrée
* [Iray] Blocage lors du passage à Iray
* [Iray] La valeur du carrelage doit affecter l’intensité de l’échelle élevée
* [Iray] Impossible de charger IRay sur un ordinateur Windows où VCCOMP110.dll n’était pas présent
* [Vue 3D][Bakers] Les UV ne peuvent pas être décodés à partir d’un obj exporté depuis Modo
* [Vue 3D] Les intensités de Displacement ne sont pas cohérentes entre Opengl et Iray
* [Vue 3D] L’intensité d’Occlusion Displacement/Parallaxe est deux fois supérieure à ce qu’elle devrait être
* Décalage [Vue 2D] lors de l’affichage de l’image alpha
* [Cooker] Le paramètre Constant ($tiling) est introuvable lorsqu’il est utilisé dans une instance de graphique
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
* Les paramètres de mosaïque et d’expansion « non carrée » de [Content] dans le polygone 1 sont rompus
* [Contenu] Les options Générateur aléatoire et Expansion non carrée ne fonctionnent pas sur le bruit anisotrope
* [Contenu] Instance « Shape » rompue dans certains mappages Usure/salissures
* [Vue 3D] La mise à l’échelle UV n’est pas appliquée si l’échelle d’height est définie sur 0
* [Vue 3D] La réflexion avec le blinn du shader ne fonctionne plus
* [Vue 2D] La mise en page de la fenêtre d&#39;informations est rompue
* [Graphique] problème lors du contrôle de la taille de la sortie avec la fonction sur une instance de bitmap lié dans un graphique
* [Fonction] Graphique non invalidé lorsqu’un lien est supprimé
* [Bibliothèque] Les favoris ne fonctionnent pas
* [Exportation de PSD] Le contenu du fichier PSD change chaque fois qu’une exportation est effectuée
* [Dégradé] Blocage lors de la manipulation des touches dans l’éditeur de dégradé
* [Modèles] Le mappage de position pour les modèles de Substance Painter est incorrect
* [AxF] height physique incorrect
* [MDL] La mise à l’échelle UVW à partir de la taille physique est inversée dans les nœuds SBS MDL
* [Boulangers] $custom ne fonctionne plus
* [Préférences] blocage au démarrage sur Mac

### 7.2.1 (2017.2.1)

*(Publié Le 20 Octobre 2017)*

**Fixe :**

* [Moteur] Blocage lors du rendu de texte avec le moteur GPU
* [Contenu] Sampler de mosaïque : l’ID de ligne/colonne ne fonctionne pas correctement avec un format non carré
* [Contenu] Couleur Sampler de la vignette : le paramétrage des couleurs est incorrect
* [Contenu] Sampler de mosaïque : valeur par défaut incorrecte pour la quantité de motif X / Y
* [Export] Les métadonnées sont manquantes dans le PSD exporté

### 7.2.0 (2017.2.0)

*(Publié Le 19 Octobre 2017)*

**Ajouté :**

* [Contenu] Ajouter un remplissage et des filtres associés (convertir un masque noir et blanc en dégradés, couleurs aléatoires, etc.)
* [Contenu] Ajout de nouveaux générateurs de bruits, de cartes d’Usure/salissures et de motifs prenant en charge le format non carré (l’ancienne version est marquée comme « héritée »)
* [Contenu] Ajout d’une nouvelle circulaire à éclaboussures avec beaucoup plus de fonctionnalités
* [Content] Ajouter un générateur de Scratches
* [Contenu] Ajouter un filtre Tourbillon
* [Contenu] Ajouter une sélection d’histogramme
* [Contenu] Ajouter un motif d’étoile
* [Contenu] Ajouter un filtre Mappeur de forme
* [Contenu] Ajouter un filtre d’interpolation vectorielle
* [Contenu] Ajouter un dégradé linéaire 3
* [Contenu] Mosaïque aléatoire/Tile Generator : ajouter un mode de symétrie (h+v, h, v)
* Tile Generator [Contenu] : ajout d’une entrée d’image multiple
* [Contenu] Renommez « Fusion RGB-A » en « Fusion Alpha »
* [Vue 2D] affichage de la sortie du nœud de commutateur à l&#39;aide de la touche C
* [Vue 2D] Optimisation de la mise en page des histogrammes/informations en fonction de leur rapport d’affichage
* [Vue 2D] Ajouter un bouton pour activer/désactiver l’affichage des mosaïques
* [3DView] Optimisation de la vitesse de calcul des harmoniques sphériques
* [Vue 3D] Mettez à jour les nuanceurs PBR pour utiliser l’échantillonnage Fibonacci au lieu de Hammersley
* [Vue 3D] Ajoutez une option pour enregistrer l’état actuel de la scène comme état par défaut
* [Vue 3D][Bakers] Sérialiser les données dans un format lisible par l&#39;homme
* [Boulangers] Ajout de paramètres prédéfinis export/import (json)
* [Publish] Création de l’archive sbsar comme non solide
* [Publish] Stockez l’image/la vignette du graphique dans la barre d’outils d’élément rapide
* [Publish] Afficher une barre de progression lors de la publication d’un package
* [Dépendances] Affichez le fichier .sbs demandant une dépendance dans la « fenêtre Dépendances manquantes »
* [Dépendances] Fenêtre de rapport : affiche une icône verte lorsque le problème a été résolu
* [Dépendances] Ajoutez une option pour ouvrir les dépendances personnalisées du package dans l’explorateur de packages
* [Préférences] Ajoutez une option pour définir l’état de scène par défaut dans les paramètres du projet
* [Préférences] Ajouter une option pour activer/désactiver le chemin d’accès à la bibliothèque
* [Graphique] Ajoutez une option pour faire une capture d’écran (à l’échelle 1:1) du graphique
* [Graphique] Supprimer l’info-bulle de l’arrière-plan des graphiques composites
* [Scripts] Rappels Add onBeforeFileLoaded et onAfterFileLoaded
* [Moteur] Ajout d’un paramètre de base pour régler le mode Rapport pixel
* [Console] Amélioration des performances de la console
* [Paramètres] Nouveau widget Position (XY)
* [Iray] Mise à niveau vers IRay SDK 2017.1
* [PSD] Enregistrer l’état du widget de PSD en tant que texte au lieu d’un état binaire
* [Library] Utiliser les pouces de sbsar s&#39;il existe
* [Explorateur] Renommer « Dépendances ». entrée « Gestionnaire de dépendances »
* Importation de fichiers AXF

**Fixe :**

* [MDL] Impossible d’exporter le module MDL si la texture est connectée à un paramètre exposé
* [MDL] Essayer d&#39;enregistrer une dépendance pour les variables de chaîne MDL (nœud constant)
* Blocage de [MDL] après la fermeture du package
* [MDL] Blocage lors de la connexion d’un élément flottant 3 à un nœud de couleur
* [MDL] ne peut pas ouvrir la bibliothèque de nœuds lors de la libération d&#39;un nœud de lien dans une image
* [MDL] blocage lors de l’utilisation d’une texture de fichier
* [MDL] Le comportement de dépendance enregistre trop d&#39;opérandes
* [Graph] Les noms des connecteurs sont désactivés après la modification de FX-Map
* [Graphique] blocage lors de l’annulation
* [Graphique] Comportement étrange avec des liens entre les nœuds
* [Graphique] Réduction de la dispersion et du détachement des nœuds lors de l’annulation
* [Graphique] Les instances de fonction ne sont pas mises à jour lorsque la référence est modifiée
* [Version Control] Le package est rechargé lorsqu’une action personnalisée Version Control est déclenchée
* [Contrôle de version] Les espaces de travail de contrôle de version désactivés sont toujours disponibles dans le menu contextuel d’un pack
* [Contrôle de version] La suppression d’une action personnalisée ne la supprime pas du menu contextuel d’un pack
* [Propriétés] L’aperçu du paramètre n’est pas mis à jour lors de l’utilisation de l’objet
* [Iray] Problème d’affichage de l’heure max.
* [Iris] Problème d’option Pause
* [Boulangers] Blocage lors de la cuisson convertir les UV en SVG à l&#39;aide de la traduction coréenne/japonaise
* [Boulangers] changer le chemin après une première cuisson ne fonctionne pas
* Problème d’annulation de [PSD Exporter]
* [PSD] et les calques sont verrouillés dans Photoshop CS5
* [UI] Le curseur de couleur est toujours défini sur blanc lors de la création d’un nœud de couleur uniforme
* [UI] L’ouverture d’un onglet existant doit l’afficher au lieu de le dupliquer.
* [Paramètres prédéfinis] blocage lors de la modification du type de paramètre utilisé dans un paramètre prédéfini
* Les échantillonnages [Vue 3D] ayant la même utilisation sont fusionnés
* [Vue 2D] Les informations sur les pixels ne fonctionnent pas pour les images dont la résolution n’est pas une puissance de 2
* Problème [Library] lors du changement de nom des filtres
* [Données] Correction de diverses fautes de frappe dans les fichiers SBS
* [Paramètres] nœud de niveau - problème de précision de niveau automatique
* [Préférences] Les boutons Répertoires de modèles doivent être désactivés pour « Projet par défaut ».

### 7.1.4 (2017.1.4)

*(Publié Le 2 Octobre 2017)*

**Ajouté :**

* [Bakers] Ajouter la courbure du filet en arrière
* [Vérificateur de nouvelle version] Ajoutez une option de ligne de commande pour désactiver la vérification de la nouvelle version (—news hide\_changelog:true)
* [Scripts] Désactiver le délai d&#39;attente de Qprocess

**Fixe :**

* [Les boulangers] ne peuvent pas changer la couleur du matériau dans UV en SVG
* [UI] ne peut pas fermer l’affichage des graphiques à l’aide du clic sur la roue
* [Contenu] Certains bruits sont en 8 bits au lieu de 16 bits
* [Contenu] Le lissage de courbure donne un résultat erroné lorsque la mosaïque est désactivée
* Blocage de [Text] lors du redimensionnement de polices spécifiques

### 7.1.3 (2017.1.3)

*(Publié Le 31 Août 2017)*

**Fixe :**

* [Vue 3D] blocage lors de la tentative d’affichage des options de vue 3D dans Mac 10.10.5
* [Vue 3D] Les informations de texte ne s’affichent pas dans la vue 3D lors de l’utilisation de l’écran à haute résolution
* [Vue 3D] La préférence globale pour OpenGL/DirectX n’est pas prise en compte lorsque la matière est réinitialisée
* [Contenu] Height à la normale : la normale est inversée lors de l’utilisation de l’échantillonnage de Sobel
* [Contenu] L’Occlusion ambiante (hbao\_2) ne se comporte pas correctement lorsqu’elle est définie sur non carré
* [Contenu] Les entrées des générateurs de masques ne sont pas dans le même ordre que celles du combineur de données de maillage
* [Vue 2D] Histogramme : les informations de sélection ne sont pas mises à jour lors du changement d&#39;image
* [Vue 2D] Histogramme : les informations de plage utilisées ne sont pas affichées pour les images en niveaux de gris
* [Paramètres prédéfinis] blocage lors du changement de nom d’un paramètre prédéfini d’un graphique utilisé dans un autre graphique
* [Graphique] X et Y sont inversés dans la barre d’outils Taille du gabarit

### 7.1.2 (2017.1.2)

*(Publié Le 3 Août 2017)*

**Fixe :**

* [Contenu] Problème de filtrage dans les filtres « Mosaïque automatique dynamique » et « Recadrage des niveaux de gris »
* [Contenu] Les filtres de bibliothèque ne tiennent pas compte de la préférence OpenGL/DirectX
* [Contenu] Impossible de cuisiner un fichier SBSAR sans\_square\_transform
* [Contenu] Forme du panorama : la zone réactive est mise en miroir dans le canal du RGB
* [Contenu] Sampler de mosaïque : le paramétrage de la couleur de position n’est pas normalisé
* [Contenu] Mosaïque Sampler : les motifs sont invisibles si la mosaïque est désactivée
* [Graphique] Le commutateur $normal\_map\_format ne fonctionne pas lorsque nous utilisons le menu de la bibliothèque/barre d’espace
* [Graphique] Format incorrect dans le nœud bitmap lors du glisser-déposer d’une ressource RGBxxF
* [Boulangers] La couleur du filet avec la couleur du matériau est cassée
* [Vue 3D] chaque modification de la vue 3D génère des actions dans la pile d’annulation
* [Dépendances] se bloque lorsqu’un graphique a des ressources manquantes dans la bibliothèque personnalisée
* [Iray] Le blocage au démarrage sur la version OSX est antérieur à la version 10.11

### 7.1.1 (2017.1.1)

*(Publié Le 18 Juillet 2017)*

**Ajouté :**

* [Boulangers] Ajouter une action « Réinitialiser » sur les champs de ressources
* [Bakers] Utiliser la couleur noire lorsqu’aucune couleur de sommet n’est trouvée
* [Paramètres prédéfinis] Masquer le widget de paramètre prédéfini sur les instances lorsqu’aucun paramètre prédéfini n’est disponible
* [Préférences] Supprimez l’option « Calculer binormal par fragment » dans les paramètres du projet (désormais, cette option est gérée dans le plug-in Tangent Frame).
* réglages de sbsupater.exe

**Fixe :**

* [Bakers] Le système « error » ne fonctionne plus
* [Bakers] options sérialisation : les anciennes clés restent
* [Boulangers] blocage lors du changement de nom d’un boulanger
* [Bakers] Problèmes d’interface utilisateur
* [Contenu] Filtre Correspondance des couleurs - Différence entre le processeur/GPU
* [Contenu] Certains GrungeMaps produisent des images 8 bits au lieu de 16 bits
* [Graph] Blocage lors de l’utilisation du X « switch links » sur le nœud fx-map
* [Vue 3D] Blocage aléatoire lors de l’ouverture de la vue 3D
* [Vue 3D] Les valeurs binormales sont toujours calculées par fragment, quel que soit le plug-in d’espace tangent
* [Updater] Erreur XML lors de l’utilisation d’une police spécifique
* [Cooker] modulo sur nombre négatif ne renvoie pas le même résultat que le moteur
* Problème d’interface [UI] lors de l’utilisation du dégradé de sélection sur un écran à haute résolution
* [MDL] Le nœud de couleur ne conserve pas cette valeur
* [Packaging] Le plug-in d’espace tangent Mikkt Unreal est manquant

### 7.1.0 (2017.1.0)

*(Publié Le 29 Juin 2017)*

**Ajouté :**

* [Boulangers] Nouvelle interface utilisateur
* [Baker] Conservez un cache de filet haute définition jusqu’à ce que la fenêtre du boulanger soit fermée
* [Baker] Ajout d’une option pour corriger la déformation en biais à l’aide d’un masque en niveaux de gris
* [Boulangers] Soutenir l&#39;utilisation-haut-poly-comme-bas-poly dans les boulangers à partir de maille
* [Boulangers] Démodaliser la fenêtre Boulangers
* [Bakers] Enregistrer l&#39;état dans un fichier .sbs dans un format lisible par l&#39;homme
* [Paramètres] Copier/coller des paramètres d’un graphique à un autre
* [Paramètres] Ajoutez une option pour copier un seul paramètre d’entrée (et le coller par la suite)
* [Paramètres] Supprimer le bouton de fonction sur le paramètre « Mode colorimétrique »
* [Paramètres] Modifier/Enregistrer/Afficher les paramètres prédéfinis intégrés
* [Paramètres] Permet à l’utilisateur de copier les attributs de paramètres lorsqu’un package est verrouillé
* [Vue 3D] Ne stocke plus les paramètres de vue 3D de la dernière session dans le registre
* [Vue 3D] Créer une nouvelle ressource 3D à partir de la scène actuelle
* [Vue 3D] Ne stocke plus l’état de la vue 3D d’une session à une autre dans le registre
* [Vue 3D] Fusionner les menus Scène et Géométrie
* [Vue 3D] Conversion sRVB séparée du nuanceur de fragments (vous devrez mettre à jour vos nuanceurs personnalisés !)
* [Vue 3D] Ajoutez une option pour créer une ressource 3D à partir de l’état actuel
* [Vue 3D] Amélioration du message d’erreur généré lorsque #include échouez dans un code de nuanceur
* [Vue 3D][Explorateur] Créer une scène 3D à partir de primitives
* [Vue 3D] Afficher le numéro de ligne correct lorsque la compilation du nuanceur GLSL échoue et que le code contient des directives #include
* [Graphique] Pouvoir redimensionner un cadre à partir de tous les coins/bordures
* [Graphique] Stockez les informations de taille du gabarit sur la ressource de graphique plutôt que sur le registre local.
* [Graphique] Optimiser la vitesse de génération des vignettes de nœud
* [Graphique] Afficher le budget du cache de mémoire dans les Préférences
* [Graphique] Ajouter une option « Réinitialiser et afficher dans la vue 3D » sur les nœuds
* [Contenu] Convertisseur PBR : ajout de nouveaux paramètres prédéfinis Arnold 4/5, Corona 1.6 et Renderman
* [Content] Optimisation du nœud AutoLevel et prise en charge de l’entrée HDR
* [Contenu] Optimisation du filtre HBAO lorsque l’optimisation GPU est désactivée, ajout de 16 exemples de version
* [Cooker] fonctionnalité non prise en charge par le SVG de sortie dans le journal
* [Cooker] Ne supprimez pas toutes les ressources du SVG si une seule fonction n&#39;est pas prise en charge
* [UI] Augmenter la taille du bloc Description
* [UI] Ajout d’informations de chemin de fichier sur les instances de graphiques
* [Fonctions] Ajouter « Ouvrir la référence » sur les instances de fonction
* [Fonctions] Afficher la liste des graphiques de fonction lorsque vous faites glisser .sbs dans un graphique de fonction
* [Explorer] Créer une nouvelle ressource 3D à partir de primitive
* [Moteur] Ajouter une variable $tiling
* [Courbe] Ajoutez des options pour retourner la courbe horizontalement/verticalement
* [Gestion des couleurs] Lire le profil ICC sur les bitmaps
* [Exporter] Ajoutez « Libellé », « Groupe » et « Données utilisateur » dans la liste des macros de modèle
* [Préférences] ajouter la possibilité de modifier le chemin d’accès pour les fichiers temporaires
* [Doc] Ajout du format MDL Graph à la documentation sur le format SBS

**Fixe :**

* [Graphique] Problème de cache : la vue des sorties en vue 3D ne fonctionne plus
* [Graphique] Problème d’effacement du cache
* [Graphique] Les demandes de génération de vignettes de nœud ne sont pas annulées lorsque le graphique est invalidé.
* [Graphique] Problèmes de résolution après l’utilisation de F5
* Affichage de graphique [Graph] manquant au lancement
* [Graphique] La modification d’un paramètre génère plusieurs appels de rendu.
* [Graph] blocage lors de l’utilisation d’un modèle personnalisé qui contient des maps bakées
* [Graphique] Blocage lorsque les nœuds liés dans une fonction de graphique
* [Vue 3D] Chargement parallèle en désordre avec ProgressManager
* [Vue 3D] Rendu avec iray à une image de résolution personnalisée non plein format
* [Vue 3D][Iray] La définition de matière n&#39;est pas conservée
* [Vue 2D] L’histogramme est vide sur les images LDR
* [Vue 2D] Problème d’affichage lorsque le mode de mosaïque est activé
* Paramètres [MDL] non exposés
* [MDL] Blocage lors du déplacement d’un fichier MDL d’un package vers un autre pendant le rendu
* [MDL] Ne vous demandez pas où attribuer la liste MDL lorsque vous double-cliquez sur le graphique
* [Bakers] Blocage lors de la cuisson de fichiers .obj spécifiques
* [Bakers] La texture transférée du maillage / normal donne un mauvais résultat
* [Transformation 2D] Impossible d’utiliser les touches fléchées pour modifier le décalage dans le nœud de transformation 2D
* Problème d’artefact [Transformation 2D] avec une faible résolution
* [Utilitaire de mise à jour] Le rapport de mise à jour ne s’affiche pas avec lorsque Ctrl+o/open
* [Propriétés][Format] Certains caractères sont mis en échappement deux fois dans UserTags
* [Nœud bitmap] Ctrl Z ne fonctionne pas sur la vue 2D
* [Préférence] Espace vide inutile dans l’onglet Alias
* [Programme d’installation] L’installation d’une version précédente ne fonctionne pas la première fois
* Liste déroulante [Paramètres] : placer certains espaces sur le libellé de la dernière valeur fige SD indéfiniment
* [UI][MAC] L’option « À propos de la Substance » affiche les informations Iray
* [SVG] blocage lors de l’importation d’un SVG spécifique
* Filtre HBAO [Content] : le paramètre Radius se comporte différemment en fonction de la résolution (un nouveau hbao\_2.sbs a été ajouté, l’ancien hbao.sbs est désormais obsolète)

## Version 6

### 6.0.4

*(Publié Le 21 Juin 2017)*

**Fixe :**

* [Graph] blocage lors de l’utilisation d’un raccourci X
* [Graph] se bloque après la suppression d’un lien entre les nœuds
* [Graphique] La suppression d’un point de scission entraîne le blocage de SD
* [Contenu] Faute de frappe dans mg\_surface\_brush
* [Contenu] Qualité inférieure sur HBAO par rapport à 6.0.2
* [Bibliothèque] Les icônes des filtres personnalisés ne sont pas enregistrées
* [Explorer] Blocage lors de l’ouverture d’une ressource 3D référençant un fichier manquant
* [Bakers] La texture de transfert à partir du filet est mise en miroir si l’option « Normal » est activée.

### 6.0.3

*(Publié Le 1Er Juin 2017)*

**Ajouté :**

* [Export] Enregistrer la taille physique en ppp dans les textures exportées
* [Vue 2D] Afficher le libellé du paramètre de matrice dans le menu Transformation

**Fixe :**

* [Contenu] Sampler de mosaïque : le paramétrage de la couleur de position n’est pas normalisé
* [Contenu] Recadrage : graphique fantôme dans un processeur de pixels
* [Contenu] Forme du panorama : la zone réactive est mise en miroir dans le canal du RGB
* [Contenu] Le filtre HBAO peut générer une résolution négative
* [Contenu] Le rendu du filtre Correspondance de couleur est incorrect dans certaines situations
* [Contenu] L’option « Pré-multiplié vers redressé » supprime la couche alpha
* [Contenu] Fautes de frappe dans diverses étiquettes
* [Graphique] Les informations de Nombre de bits par pixel sont coupées lorsque l’échelle PPP est définie sur 125 1520 ou 175 %
* [Graphique] Lorsqu’une sélection contenant un bloc est collée, le bloc n’est pas sélectionné
* [Graphique] Lorsqu’une sélection contient un commentaire, les éléments collés sont décalés dans le graphique
* Problème de points de fractionnement [Graph]
* [Graphique] Certains connecteurs d’épingle ne s’accrochent pas lorsque vous survolez
* Affichage de graphique [Graph] manquant au lancement
* [Export] bitmaps manquants après l’exportation
* [Export] N&#39;exporte pas les dépendances sur la version de la vapeur
* [Bakers] crash avec un filet qui a trop de jeux UV
* [Bakers] Baker de carte UV crash lors de la cuisson de maillages sans réglages UV
* [Moteur] Bogue Sampler avec Fxmap+HDR
* [Moteur] plantage avec des images jpeg haute résolution
* [Vue 2D] Widget de transformation manquant dans la vue 2D lorsque le mode Aperçu de la mosaïque est activé
* [Vue 3D] L’instance de graphique avec utilisation personnalisée n’est pas correctement envoyée à la vue 3D
* [Préférences] Chemin incorrect pour mikktspace.dll
* [Explorer] le déplacement d’une ressource bitmap dans un package fait apparaître le menu « link/embed »
* [Paramètres] blocage lors de l’utilisation de « tiling » comme nom de paramètre
* [MDL] aucun lien coloré entre les nœuds
* [Linker] Processeur de pixels : génération de nuanceurs GLSL incorrecte
* Problème de Nombre de bits par pixel avec [Cooker]

### 6.0.2

*(Publié Le 17 Mars 2017)*

**Ajouté :**

* [Engine] Intégrez le dernier moteur avec l’optimisation de la décompression jpeg

**Fixe :**

* [Contenu] Le correctif de clonage ne fonctionne plus
* [Contenu] La sortie Height ne fait pas partie du groupe de matières dans les modèles
* [MDL] Blocage lors de la suppression d’une instance de graphique
* [MDL] Aucun avertissement entre les nœuds en conflit
* [MDL] Messages d’avertissement inutiles lors de l’exportation
* [Courbe] L&#39;exposition des paramètres ne doit pas être exposée
* [Moteur] Blocage lors de l’importation d’un fichier sbsar contenant un bitmap HDR
* [Text Node] La spécification de police génère un fichier XML non valide
* [Éditeur de dégradé] Les valeurs ne sont pas bridées correctement
* [Vue 3D] Blocage lors de l’utilisation d’un environnement HDRi personnalisé (haute résolution)

### 6.0.1

*(Publié Le 3 Mars 2017)*

**Ajouté :**

* [Boulangers] Améliorer la gestion des tâches de progression
* [Bakers] Modifier l’info-bulle d’erreur lorsqu’aucun filet n’est sélectionné
* [Propriétés] Les paramètres de l’effet de post-traitement 3DView doivent être désactivés lorsque l’option Post-traitement est désactivée dans les préférences.
* [Licence] Autoriser la spécification d’un chemin personnalisé pour la licence Substance Designer 6
* [Dégradé] Désactivez le curseur « précision » si aucun prélèvement de dégradé n’a été effectué
* [Cooker] Ignorer la ressource manquante dans la saisie de l&#39;image pour empêcher l&#39;échec de la cuisson
* [Vue 3D] Modification de la gestion des fuites de reflets de specular
* [Graphique] Ajout de paramètres supplémentaires pour la compatibilité avec le moteur v6

**Fixe :**

* [Bakers] La carte des normales du maillage (espace universel) est inversée sur l’axe Y
* [Bakers] La cuisson d&#39;un filet sans UV ne signale pas d&#39;erreur
* [Boulangers] La normale moyenne ne fonctionne pas
* [Bakers] SD se bloque lors de la cuisson d&#39;AO avec un maillage spécifique
* [Bakers] Le format de sortie n’est pas restauré correctement
* La police personnalisée de [Texte] ne fonctionne pas dans le lecteur
* [Texte] avertissement de police non valide lors de la réouverture d’un pack avec une police dans les ressources
* La saisie de texte [Texte] ne fonctionne pas en mode Aperçu
* Le paramètre de police [Text] peut être exposé.
* [Texte] blocage lors de la création d’une fonction dans le paramètre de texte
* [Text] Se bloque lors de l’exposition de la taille de police
* [Vue 2D] Le pourcentage de zoom ne s’affiche pas correctement lors de l’utilisation de la touche F
* [Vue 2D] L’image est décalée lorsque la taille est modifiée
* [Vue 2D] Discontinuité lors de l’affichage de la mosaïque
* [Vue 2D] Le widget de transformation n’est pas visible/modifiable en mode aperçu
* [Vue 3D] Taille physique non prise en compte par PBR Parralax shader
* [Vue 3D] Le paramètre de la fréquence d’actualisation n’est pas correctement restauré d’une session à une autre
* [Graphe] multiangle\_to\_normal empêche la publication
* [Graphique] La taille de sortie du filtre de puissance est verrouillée
* [Graph] Impossible d’instancier les fichiers .sbsar
* Interface utilisateur [Courbe] recadrée
* [Courbe] L’affichage des nombres est légèrement recadré
* [Courbe] Le widget disparaît lorsque la barre d’outils est redimensionnée
* [Contenu] Le nœud Rayonnement est rompu
* [Contenu] Mosaïque Sampler : les motifs sont invisibles si la mosaïque est désactivée
* [Contenu] MG Concepteur de masque - Paramètres de contraste de courbure inversée
* [Content] Color Equalizer : paramètre de groupe personnalisé\_color\_variation non connecté
* [Contenu] Pièce dupliquée : zone de pièce non visible lorsqu’elle est positionnée dans les coins
* [Explorer] Le rechargement d’un package alors que sa dépendance est ouverte rompt le package de dépendance
* [Explorer] Impossible d’importer une ressource psd 32 bits
* [Publish] échec de la cuisson (héritage ERR:No (absolu))
* [Dégradé] Le dégradé doit être affiché comme linéaire lorsque l’option sRVB est décochée
* [Transformation2D] Impression de décalage lors du déplacement d’un widget avec contrainte d’axe
* [Paramètres] La sélection de la souris est volée par la liste déroulante
* [Moteur] Aucune mosaïque n’a aucun effet sur le nœud de distance sur le moteur GPU
* [Export] Blocage lors de l’exportation de sorties en tant que TGA
* [MDL] le paramètre prédéfini d’exportation ne fonctionne pas

### 6.0.0

*(Publié Le 14 Février 2017)*

<b>Ajouté :</b>

* [Moteur] Nouveau nœud de courbe
* [Moteur] Nouveau nœud de texte
* [Moteur] Composition de nombre de bits par pixel 16f/32f
* [Moteur] instanciation pour les cartes FX GPU
* [Engine] Fonction Add log2
* [Bakers] 8k map baking
* [Boulangers] Cuisson par matériau / « Ensemble de texture »
* [Bakers] Affiche le message de chargement lorsque la sortie bitmap est codée/écrite sur le disque
* [Boulangers] Ajouter une option d’annulation pendant la cuisson
* [Nœud de dégradé] ajouter des réglages globaux pour plusieurs touches sélectionnées
* [Nœud de dégradé] Options du sélecteur de dégradé simplifié
* [Graphique] Ajouter une option pour modifier la taille du gabarit par défaut
* [Graphique] Afficher la profondeur des pixels de l’image sous le nœud
* [Préférences] Préférences globales pour DirectX/OpenGL
* [Préférences] Utiliser les onglets dans Préférences/Interface utilisateur du projet
* [Préférences] supprimer le paramètre MaxTextureSize situé dans les préférences « 3DView »
* [Préférences] Afficher une courte aide sur l’enregistrement automatique
* [Préférences] Exposer les options de format d’image
* [Préférences] Ajouter une option pour masquer la carte d’environnement dans la vue 3D par défaut
* [Préférences] Ajouter une option pour l’option alpha par défaut du filtre de mappage normal
* [Vue 2D] Ajout de la possibilité de panoramiser loin des limites de la texture
* [Vue 2D] Interprétation du rapport taille physique X/Y
* [Vue 3D] Améliorer la gestion des textures
* [Vue 3D] Désactiver les effets postaux par défaut (pour éviter un blocage sur le processeur graphique bas de gamme)
* [Graphique MDL] Gérer l’indicateur masqué sur le paramètre IRay
* [Graphique MDL] Autoriser à définir le constructeur « material() » comme nœud racine
* [MDL Graph] Aperçu du nœud Créer une instance de graphique SBS
* [Contenu] Ajout de nouveaux filtres de traitement de numérisation
* [Content] Ajout de nouveaux filtres de réglage (Clamp, Pow, Visualiseur de plage HDR)
* [Contenu] Ajout de bruit bleu (approximation rapide)
* [Contenu] Ajout de nouveaux effets de forme (Lueur, Ombre portée, Contour)
* [Publish] Ajoutez une action « Exporter comme précédent » pour republier le dernier package sélectionné
* [Publish] Amélioration de la génération SBSAR lors de l’utilisation d’images bitmap haute résolution
* [Publish] Avertir l’utilisateur du paramètre de graphique non « relatif à x1 parent » lors de la publication ou du téléchargement sur Share
* [Properties] Ajouter l&#39;attribut « Taille physique » sur SBS Graphs
* [Paramètres] Supprimer les actions de fonction sur les chemins de ressources PKG
* [Paramètres] Supprimer la fenêtre contextuelle « Valeurs de prévisualisation modifiées »

<b>Fixe :</b>

* [Graphique] L’utilisation de la mémoire augmente régulièrement à chaque ouverture du menu contextuel
* [Graphique] [Dans SSE2] Les nœuds du polygone n’affichent pas les formes lorsque le paramètre « Scale » est en négatif
* [Graphique] Blocage lors du passage de « Nombre entier » à « Flottant » sur un paramètre exposé
* [Graphique] Le déplacement des nœuds alors qu’un point de fractionnement est sélectionné recalcule les nœuds.
* [Graphique] Les points de fractionnement ne prennent pas en charge « Annuler »
* [Graphique] info-bulle vide affichée lorsque la description du graphique contient des caractères non imprimables
* [Graphique MDL] Blocage lorsque le nœud actuel affiché dans la vue de la propriété est supprimé
* [Graphique MDL] Les graphiques MDL qui utilisent la fonction constructeur Material() comme racine ne sont pas rendus correctement dans la vue 3D
* [MDL] Impossible d&#39;exporter le module MDL lors de l&#39;utilisation d&#39;un opérateur conditionnel avec un paramètre d&#39;exposition booléen uniforme
* [MDL] Blocage lors du chargement d’un modèle de graphique MDL à deux reprises
* [MDL Archive] Les matières qui utilisent une texture ne sont pas correctement gérées
* [Vue 3D] La matière IRay n&#39;est pas modifiée lorsque le nœud racine du MDLGraph change
* [Vue 3D] blocage aléatoire lors de la fermeture de la vue 3D pendant le chargement d’un filet
* [Vue 3D] Yebis n’est pas réactivé après l’enregistrement du rendu
* [Vue 3D] Fichier de PSD non valide généré lors de l’enregistrement du rendu de la scène iray
* [Vue 3D] La lumière de point 1 ne s’illumine pas
* [UI] La zone de détection des cases à cocher est trop large dans les paramètres « Bakers from Mesh »
* [UI] Problème esthétique dans les paramètres « Bakers from Mesh »
* [Mac] L’ouverture du SD en double-cliquant sur un sbs n’envoie pas la sortie vers la vue 3D
* [Mac] [Iray] Le rendu de cluster photoréal ne fonctionne pas sur MacOS
* [Moteur] Atan2(0, 0) provoque le crash du moteur
* [Moteur] Problème de synchronisation critique
* [Bakers] Impossible de désactiver la normalisation automatique pour Height baker
* [Paramètres] lors de la conversion des niveaux de gris en rvba, la valeur alpha doit être 255
* [Fonctions] Il est possible de définir une fonction comme nœud de sortie même si elle n&#39;est pas compatible
* [Export] Dépendances non valides après l&#39;exportation d&#39;un package avec les ressources du PSD
* [Console] La suppression de la console entraîne un blocage du SD

## Version 5

### 5.6.2

*(Publié Le 8 Février 2017)*

**Fixe :**

* [Préférences] Le shader par défaut n’est pas pris en compte
* [Vue 3D] Blocage si le nuanceur par défaut est modifié lors de l’exécution
* [Moteur] Obtenir $size problème

### 5.6.1

*(Publié Le 17 Janvier 2017)*

**Ajouté :**

* [Vue 3D] Définir la taille des primitives sur 100 cm
* [Contenu] Ajouter « Filtrage d’entrée d’image » à « Éclaboussure circulaire » et « Éclaboussure »
* [Boulangers] « Courbure à partir du maillage » Ajouter des avertissements de console sous le canal « Mesh Sanity Check »

**Fixe :**

* [Vue 3D] Disparaître lorsque vous n’êtes pas ancré
* [Graphique] Les paramètres de Courbe de transfert de dégradé « Bruit » et « Précision » ne fonctionnent plus
* [Vue 3D] Alt+R ne fonctionne pas après l’enregistrement du rendu
* [Boulangers] « Courbure From Mesh » se bloque avec certains maillages ZBrush

### 5.6.0

*(Publié Le 15 Décembre 2016)*

**Ajouté :**

* [Contenu] Ajout d’un nouveau filtre « AO (Occlusion ambiante de base horizontale) »
* [Contenu] Ajout d’un nouveau filtre « Dégradé de formes Height »
* [Contenu] Ajout du nouveau filtre « Height à la normale (unités universelles) »
* [Contenu] Ajout d’un nouveau filtre « Fusion d’Height de matière »
* [Contenu] Ajout d’un nouveau filtre « Couverture de Snow »
* [Contenu] Ajout d’un nouveau filtre « Niveau d’eau »
* [Contenu] Ajout d’un nouveau filtre Correspondance des couleurs
* [Contenu] Ajout du nouveau filtre « Histogramme numérisé (non uniforme) »
* [Préférences] [Interface utilisateur] Ajoutez une option dans Préférences pour désactiver la détection haute résolution
* [Vue 3D] Ajout d’une option « Réinitialiser la position de la caméra »
* [Iray] Prise en charge de l’architecture Pascal avec le SDK IRay 2016.2 intégré
* [Graphique] Ajouter l’option « Copier les informations de nœud dans le Presse-papiers » dans le menu contextuel

**Fixe :**

* [MDL] La racine de matière de l’alg n’est pas supprimée du paramètre prédéfini exporté
* [Graphique MDL] Les liens des ressources manquantes ne sont pas supprimés dans le graphique MDL
* [Bibliothèque] La création d’un filtre crée deux conditions de base
* [Bibliothèque] Les dossiers ne filtrent plus le contenu de la bibliothèque
* [Boulangers] La barre de progression va et vient
* [Boulangers] Une ressource de cage inexistante empêche le cuisson
* [Contenu] Diverses erreurs dans « Functions.sbs »
* [Export] Le format de fichier est toujours redéfini sur png
* [UI] Problème de mise à l&#39;échelle de l&#39;interface utilisateur de Substance Designer
* [Graphique] Blocage lors du déplacement du package d’origine d’une instance de graphique
* [Préférences] si le module externe shader/tangent/... par défaut est introuvable, utilisez ceux définis dans le projet par défaut
* [Paramètres] Les curseurs ont trop de précision sur Mac
* [Explorer] Le déplacement d’un filet 3D d’un dossier vers un autre corrompt cette ressource
* Fermer la fenêtre ne tue pas le processus SD
* La boîte de dialogue d’ouverture de fichier n’affiche pas les fichiers avec le filtre « Tous les formats »

### 5.5.3

*(Publié Le 28 Octobre 2016)*

**Fixe :**

* [Shelf] Blocage lors de la création du dossier
* [Boulangers] World\_Space\_Direction ne fonctionne plus

### 5.5.2

*(Publié Le 18 Octobre 2016)*

**Ajouté :**

* [MDL Graph] Propager les valeurs par défaut de SBS Graph à l’instance de nœud SBS Graph dans MDL Graph
* [MDL] Prise en charge du glisser-déposer du graphique SBSAR
* [IRay] Mise à niveau vers SDK 2016.1.6 (261500.16187)
* [sbsrender] Optimiser la gestion de la mémoire de sbsrender pour correspondre aux performances du lecteur
* [Vue 3D] Permet au widget d’avoir une taille inférieure à celle de la barre de menus supérieure
* [Console] Autoriser à copier certaines lignes dans le Presse-papiers

**Fixe :**

* [Lecteur] Blocage lors de la lecture d’un pack directement dans Designer à l’aide du « bouton Lecture »
* [Démarrage] fichier nvcuvid.dll manquant dans l’affichage contextuel
* [Environment init] un double-clic sur un fichier .sbs ne le charge pas dans SD
* [Export] L’exportation avec les dépendances se bloque
* [MDL] Problème de synchronisation entre un graphique et son instance
* [MDL] Les nœuds d&#39;instance sbsar produisent texture\_return au lieu de valeurs.
* [Vue 3D IRay] Dans Iray Renderer, le « Canal d’Height » n’est pas mis à jour correctement lorsque vous changez de courbe d’height
* [IRay Vue 3D non ancrée] « Caméra > Enregistrer le rendu » ne fonctionne pas après avoir masqué l’application dans la barre des tâches de Windows
* [Mac IRay] Le GPU NVIDIA n’est plus détecté par IRay
* [Boulangers] Texture transférée de Bash de maille lors de la cuisson de textures non POT
* [Blocage] Blocage lors de l’exportation d’un graphique sur une Substance share
* [Graphique] Blocage lors de la sélection d’une instance fantôme
* [Vue 3D] Impossible de faire pivoter (zoom avant ou zoom arrière) la caméra orthographique en mode Iray
* [UI] Le sélecteur de couleurs ne gère pas l’affichage à haute résolution
* [Graph] (MacOS 10.11.06) Calcul infini avec nœud de fusion multi-matériaux
* [Graphique] Copier/Coller le contenu du graphique ==> coller dans le contenu et également une référence à ce graphique
* [Graphique] Plusieurs fusions de matériaux dans la scène, elle sélectionne automatiquement les mauvaises sorties
* [Graph] L&#39;Edge Wear Metal bloque le PC
* [Bibliothèque] Les fichiers « SBSAR » affichent le logo « S » au lieu des vignettes
* [Bibliothèque] Les dossiers dans .sbsar sont affichés dans la bibliothèque

### 5.5.1

*(Publié Le 8 Septembre 2016)*

**Ajouté :**

* [Iray] Ajout du mode « IQ » pour le rendu cloud
* [Iray] Mise à jour vers Iray SDK 2016.1.5

**Fixe :**

* [MDL] La vue 3D ne fonctionne pas correctement la première fois
* [MDL] Le dégradé\_interpolation\_linéaire n’est pas exporté avec le chemin complet.
* [MDL] Le coin inférieur droit de l’image nouvellement créé est exactement aligné avec le nœud associé
* [MDL] La vignette de la matière racine ne se met pas à jour dans certains cas
* [MDL] Blocage lors de la suppression de tous les nœuds et de la restauration
* [MDL] Performances lentes dans l’affichage des graphiques par rapport au Graphe Substance
* [MDL] Impossible d&#39;exporter le module MDL en raison du paramètre IOR
* [MDL] Les paramètres affichés ne correspondent pas au nœud sélectionné
* [Vue 3D] La matière MDL provenant d&#39;un graphique MDL n&#39;est pas réinitialisée lorsque le nœud racine est supprimé
* [Vue 3D] Le cadrage par défaut de la caméra est perdu après le chargement du filet du fbx
* [Vue 3D] L’affectation de texture n’est pas conservée lors du passage à Iray
* [Iray] Message d’avertissement d’IRay lors du déplacement de la caméra
* [Iray] Blocage lors du passage à Iray
* [Iray] Le mot de passe VCA n&#39;est pas enregistré
* [Graph] Blocage lors de la suppression de nœuds
* [Graphique] Appuyer sur CTRL pour copier le lien ne fonctionne pas avec le mode Matière
* [Graphique] Blocage lors de la suppression d’un nœud de sortie dans un matériau de nœud d’instance
* [Bakers][Vue 3D] Impossible de charger le filet haute définition
* [Mac][Vue 3D] Blocage lors de la tentative de restauration de fenêtres détachées sur le moniteur secondaire
* [Paramètres] Impossible de modifier une valeur dans un spinboxedit sans supprimer le suffixe
* [UI] Utiliser « Annuler » lors de la fermeture de la boîte de message SD doit s&#39;arrêter
* Blocage lors de l’ouverture de deux vues 3D
* Blocage dans Alg::Scripting: : moteur lors de l&#39;utilisation de beaucoup de conditions VisibleIf
* Les fichiers sont supprimés par enregistrement automatique s’il existe un fichier .algautosave

### 5.5.0

*(Publié Le 25 Août 2016)*

<b>Ajouté :</b>

* Substance Designer est maintenant disponible sur Linux
* Nouvel éditeur MDL (Material Definition Language)
* [Boulangers] Nouvelle courbure du boulanger de filet
* [Bibliothèque] Utiliser des icônes de SVG au lieu de fichiers bitmap
* [Bibliothèque] Ajoutez une option pour filtrer le résultat pour MDL, Composition, Fonction et Fxmap
* [Graphique] Étendez l&#39;option « Afficher le nœud nouvellement créé » pour copier/coller/dupliquer les nœuds
* [Nouveau document] Créer un widget de sélection de modèle lors de la création d’un graphique MDL
* [Vue 3D][Iray] Mode de rendu d’affichage + nœuds VCA en regard des itérations/du temps
* [Vue 3D] Amélioration des performances du menu « Matériau » à l’ouverture
* [3DView][Bakers] Mise à jour vers FBX SDK 2017
* [Vue 3D] Ajout de la possibilité d’afficher/masquer les informations de rendu (résolution, itérations, etc.) dans le menu d’affichage de la vue 3D
* [Iris] Réexposition des paramètres de pixellisation dans le montage de scène
* [Projet] Ajouter un alias généré automatiquement pour le répertoire de fichiers du projet
* [Projet] Spécifiez la texture d’environnement par défaut dans les paramètres du projet
* [Contenu] Nouveau studio HDRi ajouté
* [Contenu] Ajout d’un nœud de transformation non carré à la bibliothèque
* Lancez SD avec un fichier .sbscfg spécifique

<b>Fixe :</b>

* [Graphique] Les entrées ne se connectent pas automatiquement aux sorties avec la même utilisation.
* [Graphique] Les entrées de nœud insérées ne sont pas connectées correctement
* [Graphique] La désélection doit également sélectionner un nœud sous la souris
* [Graphique] L’insertion de nœud ne se connecte pas à tous les liens
* [Boulangers] Diffusion incorrecte dans le boulanger de courbure
* [Bakers] « Texture transférée du maillage » se bloque si le maillage haute définition ne contient pas d’UV.
* [UI] L&#39;icône de fonction sur les paramètres n&#39;est pas modifiée lorsqu&#39;une fonction est définie
* [UI] Les info-bulles des paramètres sont coupées
* [Vue 3D] plus de 1 000 lumières sont affichées dans la scène
* [Vue 3D] Le nuanceur GLSL Lambert ne gère pas correctement la texture srvb
* [Vue 3D] Paramètres de mosaïque manquants lors de la connexion de substances en iris
* [Iray] L’exportation prédéfinie de mdl ne fonctionne pas lorsque les espaces sont dans le nom
* [Iray] Les paramètres de subdivision ne sont pas pris en compte
* [Paramètres] L&#39;identificateur de paramètre n&#39;est plus affiché
* [Paramètres] Blocage lors de la modification de l’URL de la ressource à partir de « De la ressource... » action
* [Paramètres] Conversion incorrecte du caractère &amp;
* [Explorateur] un double-clic sur un graphique « grand » échoue souvent à l’ouvrir dans la vue graphique
* [Explorer] Les SVG incorporés sont affichés comme manquants dans l&#39;Explorateur
* [Explorer] Blocage lors du changement de nom d’un élément avec le caractère &#39;&amp;&#39;
* [Contenu] La mosaïque Dégradé 1 est incorrecte lors de l’utilisation d’une rotation de 90/180°
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
* [Vue 3D] Autoriser l’exportation du rendu vers ArtStation
* [Vue 3D] Ajout du shader par défaut dans la liste des shaders
* [Graphique] Afficher le nom de la ressource au-dessus du nœud bitmap
* [Graphique] Amélioration de l’ordre des listes dans le menu de recherche de la barre d’espace
* [Boulangers] Nouveau boulanger « Position from Mesh »
* [Boulangers] Nouveau paramètre « normal map » pour Texture Transfert baker
* [Boulangers] Nouveau réglage « Tangent » &amp; « Binormal » pour World Space Normal baker
* [Scripts] Autoriser l’exécution de scripts pendant les actions Enregistrer, Exporter et Publish
* [Dépendances] Ajouter une option Réduire/Développer en fonction de la sélection
* Ajout d’un avertissement concernant les conflits d’extension de shell

**Fixe :**

* Blocage à la sortie
* Le processus de Substance Designer peut encore être en cours d’exécution après la fermeture
* [Iray] Les sorties ne sont pas envoyées aux matériaux mdl lors du changement de moteur de rendu
* [Contenu] Échantillonneur de mosaïque : la rotation aléatoire du motif ne doit pas faire pivoter la forme

### 5.3.5

*(Publié Le 6 Avril 2016)*

**Fixe :**

* [Vue 2D] L’option de menu contextuel Transformation 2D est disponible sur n’importe quel nœud
* [Vue 2D] transformation widget 2D toujours modifiable après la suppression du nœud de transformation
* [Vue 3D] Le chemin d&#39;accès de l&#39;environnement ne doit pas être affiché dans les paramètres d&#39;environnement
* [Vue 3D] Les paramètres des effets postérieurs ne sont pas enregistrés dans les ressources 3D
* [Vue 3D] Le menu de la barre d’outils ne se comporte pas comme un menu normal
* [Préférences] Impossible de définir une « limite du cache du moteur » supérieure à 4 095
* [Préférences] La définition d’un nuanceur par défaut n’est pas prise en compte
* [Iray] Les paramètres de couleur ne sont pas récupérés correctement
* Les couleurs de matière MDL sont réinitialisées.
* [Iris] Les bitmaps ne sont pas exportés avec le paramètre prédéfini MDL
* [IRay/Mac] Le redimensionnement de la vue 3D entraîne le blocage de la station de travail Mac
* [Graphique] Échec de l’exportation du document de PSD
* [Graphique] Taille de nœud affichée incorrecte
* [Graphique de fonction] L’exemple d’image d’entrée de nœud n’est pas modifiable si une seule image est branchée
* [Moteur] Blocage lors du calcul du graphique Fxmap
* [Engine OGL] Erreur lors de la génération du processeur de pixels
* [Dégradé] Le sélecteur de dégradé ne fonctionne pas sous Mac
* [PSD] image 8 bits non correctement convertie en 16 bits
* [Paramètres] Le widget d’histogramme de niveau n’a pas le même height en couleurs et en niveaux de gris
* [Console] Cliquer sur une cellule fait défiler la vue horizontalement
* [Explorer] Les ressources 3D déplacées ne sont pas correctement ouvertes dans la vue 3D

### 5.3.4

*(Publié Le 16 Janvier 2016)*

**Fixe :**

* [Iray] tangente/binormale ne sont pas correctement prises en compte
* [Explorer] Le package est marqué comme étant enregistré juste après son ouverture
* [Vue 3D] La réflexion diffuse IBL est trop forte
* [Vue 3D] Blocage lors du glisser&amp;déposer d’une image 8 bits de l’explorateur vers la vue 3D
* L’application se bloque depuis le 1er janvier 2016

### 5.3.3

*(Publié Le 10 Novembre 2015)*

**Ajouté :**

* [Contenu] Ajouter « White Noise Fast » (basé sur le processeur de pixels)
* [Content] Ajouter « Décalage global horizontal/vertical » sur Tile Samplers

**Fixe :**

* Blocage lors de la création d’une nouvelle Substance dans certaines situations
* [Bakers] Blocage lors de la mise à jour du graphique par les maps bakées
* [Boulangers] OBJ provenant de zbrush doit utiliser le nom de fichier pour Match By name
* [Paramètres] Blocage lors de l’opération Annuler/Rétablir/Annuler dans un graphique de fonction
* [Graphique] Les points de fractionnement ne sont pas collés à l’emplacement correct

### 5.3.2

*(Publié Le 30 Octobre 2015)*

**Ajouté :**

* [Contenu] Ajout d’une commande de filtrage pour l’entrée de motif sur les Tile Generator

**Fixe :**

* [Vue 3D] Point de mise au point mal initialisé
* [Vue 3D] Mauvais plan de clip lointain lors du basculement de plusieurs fois de ressources de maillage 3D
* [Vue 3D] Artefact de rendu bref lors du chargement d’un filet
* [Vue 3D] La carte d’environnement est noire lorsque le fichier est introuvable -> retour à la carte d’environnement par défaut
* [Vue 3D] Blocage après utilisation d’une image Latitude/Longitude personnalisée
* [Vue 3D] Blocage lors du chargement d’un fichier obj spécifique
* [Vue 3D] la recharge automatique du maillage ne fonctionne pas correctement
* [Iray] Impossible d’attribuer une texture sur le mdl externe
* [Iray] Impossible d’attribuer des textures à la couche d’anisotropie après la réinitialisation de la matière
* [UI] Le menu contextuel Windows apparaît lorsque le bouton droit de la souris est relâché après un déplacement dans 3DView
* [Vue 2D] L’outil Info ne renvoie pas la valeur de couleur du pixel sous le curseur
* [Baker] Les images en niveaux de gris sont enregistrées sous forme indexée avec le format Tag
* [Graphique] Les sorties en vue 3D doivent réinitialiser les canaux avant d’envoyer les sorties en vue 3D
* [Paramètres] Le nom d’entrée du paramètre est vide lorsqu’il est exposé à partir de « Exposer les paramètres du nœud »
* [Performances] Définissez le rappel onSubstanceCallbackProfileEvent sur le moteur UNIQUEMENT si les minutages sont activés

### 5.3.1

*(Publié Le 21 Octobre 2015)*

**Ajouté :**

* [Vue 3D] Afficher le nom du filet dans la scène/modification au lieu de « Entité »
* [Vue 3D] Rétablir la couleur par défaut lorsqu’une nouvelle vue 3D est ouverte
* [Vue 3D] Caméra de mise au point lors du passage de la scène à la primitive
* [Vue 3D] Affiche la résolution de la fenêtre de rendu lorsque la résolution personnalisée est utilisée
* [Iray] Ajuster la présentation des paramètres de subdivision
* [Iray] Sortie des informations du journal IRay dans le journal SD
* [Bakers] Lire correctement les fichiers OBJ pour rendre la correspondance par nom compatible

**Fixe :**

* [Vue 3D] Affichage incorrect des maillages dont l’échelle est différente de 1
* [Vue 3D] Le calcul automatique des plans proches de l’élément ne fonctionne pas bien pour les grands objets
* [Vue 3D] Le mode Structure filaire affiche des fils trop épais
* [Vue 3D] La fenêtre de rendu Enregistrer ne s’affiche pas si les effets de publication sont désactivés
* [Vue 3D] Blocage lors du changement de géométrie
* [Vue 3D] Message « QOpenGLWidget : Impossible de rendre actif le widget non initialisé » dans le journal
* [Vue 3D] L’éclairage n’est pas calculé si la carte d’environnement est modifiée pendant l’exécution d’Iray
* [Vue 3D] Blocage lors de l’affichage du filet 3D
* [Vue 3D] Très mauvaises performances OpenGL après avoir utilisé Iray
* [Vue 3D] Plans d’élément mal calculés
* [Vue 3D] La modification de la carte d’environnement n’actualise pas la vue 3D
* [Vue 3D] Les textures ne sont pas mises à jour lors du changement de graphique
* [Vue 3D] Les échantillonnages masqués GLSLFX sont toujours affichés dans le menu de sélection
* [Vue 3D] La matière n’a pas été restaurée correctement lors de l’ouverture de la ressource de maillage
* [Vue 3D] Fuite de mémoire RAM/VRAM lors de l’ouverture de divers maillages et de l’affectation de plusieurs graphiques dessus
* [Vue 3D] La mise au point ne prend pas en compte la distance focale
* [Iray] nvcuvid.dll est manquant (désinstallez la version précédente pour vous débarrasser du message)
* [Iris] Le bouton « ... » de la boîte de dialogue Exportation des paramètres prédéfinis n’ouvre pas la fenêtre de dialogue
* [Iray] La réfraction/diffusion ne fonctionne pas correctement en mode physique\_diffusion\_specular
* [Couleur orange] Mdl par défaut introuvable (couleur magenta)
* [Iray] Ne connectez pas les textures par défaut au matériau mdl pour activer le mode valeur dans le matériau d’édition
* [Iris] La déséchelle n’est pas déclenchée lorsqu’une texture est mise à jour
* [Boulangers] Le boulanger normal de Worldspace produit une image noire
* [Boulangers] Blocage lors du boulonnage d’une carte normale avec une vue 3D non ancrée
* [Bakers] La baking avec la méthode « Embedded » alors qu&#39;un chemin non valide est défini pour « link » empêche l&#39;enregistrement de la ressource
* [Bakers] Baking avec la méthode « Embedded » et modification du format de fichier ne modifie pas l’extension sur le disque
* [Boulangers] Les noms aléatoires des ressources intégrées ont tous un nom XXX..
* [Bakers] Les objets multiples dans .obj ne sont pas importés correctement
* [Contenu] Fusion de matériaux : la sortie de couleur de base n’est pas masquée lorsque la couche est désactivée
* [Contenu] Le blanc\_bruit et les bruits dérivés ne sont pas rendus correctement à 8k
* [Graphique] Performances lentes dans le graphique
* [Graphique] Blocage lors du glisser-déposer d’un élément de fonction de la bibliothèque vers le graphique de fonctions
* [Graphique] « Afficher les sorties en vue 3D » doit uniquement envoyer la sortie visible du nœud dans la vue 3D
* [Préférences] L’utilisateur par défaut\_project a un « Suffixe de nom » vide pour la fonctionnalité Correspondance par nom du boulanger
* [Moteur] La conversion des couleurs -> niveaux de gris entraîne une perte de précision
* [Console] La console/le journal est pollué par de nombreux messages
* [Partager] Blocage lors de la tentative de partage d’un pack
* [UI] L’info-bulle est bloquée au-dessus du menu Fichiers récents
* Blocage à la sortie

### 5.3.0

*(Publié Le 1Er Octobre 2015)*

<b>Ajouté :</b>

* [Vue 3D] Ajout d’un moteur de rendu Nvidia Iray
* [Vue 3D] Faire pivoter l’environnement à l’aide des touches CTRL + Maj + RMB
* [Vue 3D] Effectuer le rendu de la fenêtre d’affichage 3D à une résolution personnalisée (Ogl/Iray)
* [Vue 3D] Rendre le chargement de la scène asynchrone
* [Vue 3D] Afficher la scène globale dans le navigateur de scènes
* [Vue 3D] Désactiver la grille par défaut
* [Vue 3D] Ajout d’une atténuation de distance carrée inverse pour les lumières ponctuelles
* [Vue 3D] Afficher le paramètre de couleur dans le RGB au lieu de RVBA
* [Vue 3D] Paramètres d’éclairage/de caméra/d’environnement distincts
* [Share] Améliorations de la fenêtre de téléchargement de Substance share

<b>Fixe :</b>

* [Vue 3D] Erreur de normalisation des nuanceurs PBR
* [Vue 3D] Blocage lors d’un clic droit sur la racine dans le navigateur de scènes
* [Vue 3D] Ombrages PBR : économie d’énergie diffuse ou spécifications et éclairages ponctuels
* [Vue 3D] Réinitialiser « Matière/Réinitialiser » réinitialise également les couches à la couleur par défaut
* [Bakers] Position avec normalisation de la sphère non centrée
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
* [Vue 3D] PBR diffus/spec préfère la couleur de base à la diffusion
* [Vue 3D] Les limites ne fonctionnent pas correctement avec les ombrages de tessation
* [Moteur] Blocage lors de l’instanciation d’un fichier sbsar spécifique
* [Moteur] Les fonctions Sizelog2 / pow2 ne fonctionnent pas correctement
* [Moteur] « définir » dans la taille de la sortie ne fonctionne pas
* [Moteur] Le Niveau du mipmap n&#39;est pas serré pour les valeurs négatives
* [Contenu] Impossible de publier un graphique contenant un filtre triplan

### 5.2.1

*(Publié Le 27 Août 2015)*

**Fixe :**

* [Graphique] Blocage lors du calcul d’un sbsar spécifique
* [Graphique] Blocage lors de l’instanciation de fxmap avec plusieurs entrées d’image
* [Moteur] Blocage avec sizelog2
* [Engine] La valeur par défaut du paramètre exposé est ignorée avec le moteur DX10
* [Bibliothèque] Le calcul des vignettes est interrompu lorsque le projet contient un alias non valide
* [Cuisson] Définissez les paramètres « inconnu\_paramètre » et « paramètre dupliqué » comme avertissement au lieu des erreurs
* [Préférences] La limite du cache du moteur est bloquée à 4 095 Mo.
* [Fonction] Le libellé du paramètre d&#39;entrée est interprété comme identifiant

### 5.2.0

*(Publié Le 18 Août 2015)*

**Ajouté :**

* [Bibliothèque] Ajout d’une option dans les préférences pour masquer/afficher les calques de PSD
* [Paramètres] Autoriser les données utilisateur sur plusieurs lignes
* [Graphique] Ajoutez une option de préférence pour afficher les commentaires à taille constante
* [Graphique] Ajout d’une option de préférence pour désactiver l’affichage des nouveaux nœuds dans la vue 2D
* [Performances] Les performances du processeur en pixels augmentent sur le moteur DX10
* [Vue 3D] Ajout d’une facettisation aux nuanciers PBR
* [Vue 3D] Ajout d’une opacité simple aux nuanciers PBR (pas de tri des visages)
* [Contenu] Ajout de cibles Vray/Corona/Redshift/Arnold au filtre du convertisseur PBR (pour convertir les cartes pour ces systèmes de rendu)
* [Contenu] Ajout de la technique « axée sur les détails » au filtre Combinaison normale

**Fixe :**

* Blocage lors de l&#39;ouverture de sbs avec une dépendance vide
* Le lien vers les calques de PSD est rompu après le rechargement du pack
* [Fonctions] Sécurité du type de rupture des fonctions imbriquées
* [Fonctions] Les libellés et les groupes et les descriptions ne sont pas affichés
* [Fonctions] Blocage lors du copier/coller à partir d’une fonction supprimée
* [Graphique] Lien de matière rompu avec les graphiques sbsar
* [Graphique] La création de plusieurs nœuds bitmap à partir de ressources empile les nœuds les uns sur les autres
* [Graphique] élément de commentaire non créé à la bonne position lorsqu’il est enfant d’un nœud
* [Graphique] Les commentaires longs bloquent la sélection de la région
* [Bakers] La carte de l’espace tangent devient noire sur Mac
* [Paramètres] Visible Si ne fonctionne pas lorsque le nom d&#39;entrée contient « - »
* [Paramètres] La valeur d’étape dans Paramètres d’entrée est ignorée si elle est inférieure à 0,01
* [Bibliothèque] La balise « Visible dans la bibliothèque » n’est pas prise en compte pour sbsar

### 5.1.1

*(Publié Le 4 Juin 2015)*

**Ajouté :**

* [Graphique] Réduction de l’espace entre deux nœuds lors de l’utilisation de la connexion automatique
* [Graphique] Désactiver le paramètre Autoconnecter lors de l’utilisation du glisser-déposer dans le graphique
* [Graphique] Positionner le cadre sur la grille
* [Graphique] Désactiver l’insertion de nœud sur/sur le lien sélectionné pour le lien de matériau
* [Préférences] Définissez la valeur maximale de la taille de texture maximale sur 8 192.
* [Contenu] Ajout d’options de symétrie au nœud « Transformation sécurisée »

**Fixe :**

* [Graphique] Le nouveau nœud n’est pas ancré sur la grille
* [Graphique] Le remplacement des liens peut générer des boucles/un blocage
* [Graphique] Problème d’affichage lorsque la taille des nœuds/le minutage sont désactivés
* [Bakers] Blocage lors de la sauvegarde sur une ressource qui utilise le même nom que la scène
* [Bakers] Le nom de ressource par défaut n&#39;est pas extrait du fichier de projet correct
* [Moteur] Problème de fonction Pow2/log
* [Moteur] Erreur dans l&#39;évaluation de la fonction
* [Fxmaps] Blocage lors de la réinitialisation du paramètre à la valeur par défaut
* [FxMaps] Mauvaise évaluation des fonctions
* [Préférences] Cliquer sur l’onglet du projet bloque le SD
* [Vue 3D] L’utilisation personnalisée est convertie en minuscules
* [Paramètres] Impossible de réorganiser les éléments dans les listes déroulantes
* [Explorer] Blocage lors du déplacement d’un graphique de fonction dans l’explorateur

### 5.1.0

*(Publié Le 28 Mai 2015)*

**Ajouté :**

* [Graphique] Rechercher/Afficher le contenu de la bibliothèque via le menu de la barre d’espace
* [Graphique] Afficher/ouvrir le nœud nouvellement créé
* [Graphique] redirection de lien (Alt + Maj)
* [Graphique] sélectionner les parents de nœuds
* [Graphique] Permuter 2 liens (X)
* [Graphique] Insérer un nœud sur un lien à l’aide du glisser-déposer
* [Graphique] Créer un graphique à partir d’une sélection de nœuds
* [Graphique] Supprimer le lien lors de l’utilisation d’Alt + LMB sur une épingle de nœud
* [Graphique] Ne connectez pas le nouveau nœud au précédent à l’aide de la touche Maj
* [Graphique] Ajouter une barre d’outils pour les filtres de base
* [Graphique] Améliorer la grille (accrochage et résolution)
* [Graphique] Déplacer le commentaire/cadre/épingle vers le menu contextuel
* [Graphique] Créer un nœud sur un lien sélectionné
* [Graphique] Ajout d’icônes aux éléments de fonction
* [Graphique] Modification des couleurs des épingles dans le graphique de fonction
* [Graphique] Utiliser Maj pour désactiver la connexion automatique des nœuds
* [Graphique] Placer le lien sélectionné sur les autres liens
* [Graphique] Ajouter des icônes aux nœuds Fxmap
* [Graphique] Ajoutez un commutateur pour dessiner des liens courbes ou rectangulaires
* [Fonction] Accentuez la distinction entre les différents types de vecteurs dans le graphique de fonction (couleurs des broches/liens)
* [Fonctions] ajouter des icônes sur les nœuds et afficher des valeurs pour constante / set / get
* [Fonctions] Ajout de couleurs au titre du nœud
* [Fonction] Améliorer les performances pour l&#39;évaluation des fonctions (utiliser le code généré par SSE)
* [Fonction] Afficher un avertissement si le nœud Set/Get est vide
* [Bakers][Graph] Image bitmap de tramage lors de la conversion en 8bpc
* [Bakers] Normales moyennes des sommets dans le fichier OBJ si le maillage ne contient aucune
* [Bakers] Correspondance par nom : utiliser le suffixe comme séparateur
* [Paramètres] Ajouter une option pour basculer entre RGB et HSV sur le widget de couleur
* [Paramètres] Ajouter le bouton Pipette dans le widget de couleur
* [Bibliothèque] Ajoutez une catégorie pour le contenu de base (nœuds de composition, fxmap, fonction...)
* [Vue 2D] Infos : ajouter un affichage dans la plage [0, 1] et HSV
* [Vue 3D] Ajout de la prise en charge mipmap pour l’environnement
* [Dépendances] Nettoyer les dépendances inutilisées avec le programme de mise à jour
* [Updater] N’enregistre pas les packs automatiquement

**Fixe :**

* [Blocage] lors de la fermeture du pack
* [Blocage] lors de l’ouverture du gestionnaire de dépendances sur un pack non enregistré
* [Crash] Exemple de bogue de couleur
* [Engine] Blocage de la région de mosaïque FxMap
* [Moteur] problème de précision avec le moteur SSE avec un nœud de flou et/ou de fusion
* [Moteur] Le calcul ne s’arrête pas lorsqu’il est divisé par 0
* [Explorer] blocage lors de l’exportation d’un package avec dépendance s’il contient des cycles de dépendance
* [Explorer] Le glisser-déposer des ressources échoue souvent
* [Boulangers] La normale cuite est rendue noire si elle est supérieure à 256\*256
* [Bakers] L’enregistrement d’un pack au même emplacement que le chemin d’exportation interrompt le chemin
* [Bakers] Chemin cible par défaut incorrect lorsque le package n’a pas encore été enregistré
* [Moteur] Résultat de taille de pixel incorrect lorsqu’il est hérité de la fonction parent
* [Dépendances] La dépendance inutilisée n&#39;est pas supprimée
* Blocage de [Dependencies] lors de l’ouverture de la fenêtre de dépendances d’un pack contenant des cycles de pack
* [Graphique] les rectangles de sélection sont redimensionnés en fonction du zoom
* [Graphique] ne pas « accrocher » le lien à l’entrée/sortie la plus proche
* [Graphique] Pile d’annulation incorrecte (peut générer des blocages)
* [Graphique] La connexion multiple avec Ctrl ne fonctionne pas si le coin est déjà branché
* [Vue 3D] La couleur de la grille est affectée par la couleur d’arrière-plan
* Le nœud de sortie [Vue 3D][Graphique] contenant plusieurs utilisations n’est pas envoyé correctement à la vue 3D
* [Vue 3D] Tesselling shader : bug de compilation sur les GPU AMD
* [Vue 2D] Problème de système d&#39;épingles
* [Fonctions] Bogue de compilation de fonction (si autre)
* [Préférences] suffixe bas/haut non lu correctement dans sbsprj
* [Bibliothèque] Le fait de glisser-déposer un dossier sur un autre le supprime
* [Windows] Plusieurs sessions de SD peuvent être exécutées
* [Licence] L’ancienne licence n’est pas conservée
* [Contenu] Problème de filtre Détection des contours

### 5.0.3

*(Publié Le 1Er Avril 2015)*

**Ajouté :**

* [Préférences][Bakers] Ajouter une option pour calculer tbn par sommet ou par pixel pour correspondre à UE4
* [Library] Utiliser le filtrage bilinéaire pour les vignettes
* [Boulangers] Permettre à la fenêtre d&#39;être réduite à moins de 800px height
* [3DView] Égaliser l&#39;exposition de la carte d&#39;environnement / normaliser la rotation pour obtenir un éclair cohérent
* Nommer le raccourci de l’application avec la version majeure

**Fixe :**

* [Graphique] Blocage lors de la suppression de certains nœuds fantômes
* [Graphique] le nœud ancré reste ancré lors de la duplication du nœud
* [Graph] Blocage lors de la suppression de nœuds
* [Graphique] Les paramètres des sorties d’exportation ne sont pas stockés par graphique
* [Graphique] État d&#39;ancrage de nœud non valide lors de la suppression du nœud
* [Bakers] Les erreurs ne s&#39;affichent plus dans une boîte de dialogue
* [Boulangers] La ressource manquante n&#39;est pas affichée comme manquante dans la fenêtre de boulangerie
* La fenêtre [Publication] qui a échoué ne doit pas être modifiable
* [Publication] Sbsar Résultat incorrect
* [Vue 3D] Les matériaux multiples des maillages FBX mis à jour ne sont pas rechargés correctement
* [Vue 3D] La diffusion SH peut produire des valeurs négatives dans certains cas dans les nuanceurs PBR
* [Vue 2D] Le nombre de bits par pixel affiché pour les images de ressources est toujours de 8 bpc
* [Paramètres] Les paramètres ne sont pas toujours affichés dans les propriétés du graphique
* [Menu] « Exporter le fichier journal... » action ne parvenez pas à localiser le fichier log.txt
* [Batchtools] Erreur de sous-lecteur
* [Explorer] Le chargement des packages met en surbrillance
* [Properties] Blocage lors de l’effacement d’une fonction sur un paramètre enum
* [Préférences] Le plug-in Mikkt tangent space n’est pas défini sur la valeur par défaut dans user\_project
* [Évaluation/Activation] Impossible d’évaluer/d’activer en ligne sous Windows
* La barre d’état de calcul déplace l’interface lors de l’actualisation
* Lancer plusieurs SD en même temps
* Mettre à jour l’URL du lecteur lorsque .exe est introuvable
* La modification du fichier sur le disque n’a pas été détectée correctement

### 5.0.2

*(Publié Le 17 Mars 2015)*

**Ajouté :**

* [Bibliothèque] Ajout d&#39;un contrôle normal dans la matière\_adjustment\_blend
* [Bibliothèque] Ajouter une option de fusion pour obtenir une matière normale\_color\_blend
* Mettre à niveau vers Qt 5.4.1

**Fixe :**

* [Crash] OSX 10.9 et 10.10 dans FreeImage
* [Crash] Lors de l’ouverture d’un fichier fbx contenant des éléments sans aucun sommet
* [Graphique] Problèmes de glisser-déposer
* [Graphique] Le raccourci Effacer le cache est rompu
* [Graphique] La balise apparaît en noir/transparent dans SD
* [Bibliothèque] Entrée normale en niveaux de gris triplanaires incorrecte
* [Bibliothèque] Le nœud de détection des contours ne fonctionne pas correctement avec le moteur du processeur
* [Paramètres] Gamme de curseur incorrecte pour float2/3/4
* [Paramètres] L’action « Exposer les paramètres » entraîne deux blocages de Designer
* [Console] N’est pas redimensionné correctement
* [Console] Duplication dans la liste des canaux : View3D et 3DView
* [3DView] L&#39;ordre des paramètres défini dans glslfx n&#39;est pas conservé dans l&#39;interface graphique
* [Explorer] Blocage lors de l’actualisation des textures manquantes sur le disque
* [Fonction] Changer la valeur et modifier les pistes entraîne un blocage
* [Baker] Blocage lors de l’ouverture de la fenêtre de cuisson sur une ressource 3D manquante
* [PSD] Blocage de Psdparse (MSVCR120.dll manquant)
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

* [Export] Supprimer le canal Alpha pour TGA et BMP lorsqu&#39;il est complètement opaque
* [Vue 3D] Définition du nuanceur PBR par défaut
* [Vue 2D] Basculer pour afficher l’image sous forme de prémultipliée alpha
* [Paramètres] Taille : ajoutez une valeur de verrouillage/affichage de largeur/Height dans les listes déroulantes
* [Dépendances] Nouveau gestionnaire de dépendances
* [Dependencies] affiche/recherche l&#39;instance de nœud correspondant à une dépendance
* [Dépendance] Ouvrez un pack de dépendances dans l’explorateur de packs
* [Engine] Blend : prend en charge le paramètre Opacité lorsqu’un masque est utilisé
* [Moteur] Fusion : ajoutez de nouveaux modes de fusion (incrustation, écran, lumière tamisée, division)
* [Engine] Blend : prend en charge la fusion alpha directe
* [Moteur] Nouveau nœud de dégradé dynamique
* [Moteur] Nouveau nœud Distance
* [Engine] Nouveau nœud de processeur de pixels
* [Engine] Fxmap : prise en charge de la fonction dynamique pour les images d’entrée
* [Moteur] Fonction Sampler : prise en charge de l&#39;échantillonnage bilinéaire
* [Moteur] Fxmap : prise en charge du filtrage bilinéaire/le plus proche pour les images en entrée
* [Moteur] Fxmap : prise en charge Alpha de l’image d’entrée directe/prémultipliée
* [Bakers] Ajoutez une option pour faire correspondre la géométrie par nom de maillage entre les maillages basse et haute définition
* [Modèles] Création d’une substance de modèle pour la Substance Painter
* [Bakers] Nouvelle carte de texture de mesh baker
* [Graphique] Ajoutez une « vérification de compatibilité » pour mettre en évidence les nœuds qui ne sont pas compatibles avec le moteur précédent
* [UI] Ajustements du menu Aide
* [Préférences] définissez le module externe Mikkt tangent space sur celui par défaut (réinitialisé à la valeur par défaut dans les préférences si SD4 est installé)
* [Bibliothèque] Ajout de nouveaux mappages HDR
* Nouvelle Substance à partir du modèle
* Basculer vers Qt5
* Mise à jour du système de licences vers SD5

**Fixe :**

* [Mac uniquement] Problème de sélecteur de couleurs avec l’écran Retina
* [Mac uniquement] Glissez-déposez sur la vue 3D sous Mac OS et faites-la pivoter
* [Bakers] La cuisson d’une carte sans dossier de sortie produit une texture vide
* [Graphique] Les nœuds ancrés dans l’image se déplacent de manière étrange
* [Paramètres] Le chemin de bibliothèque personnalisé n&#39;est pas chargé à partir des fichiers sbsprj
* [Vue 3D] CTRL+R pour recharger tous les shaders déclenche également la réinitialisation de la vue 3D
* [Vue 3D] Env. Basculement uniforme de l&#39;height Mipmap vers la valeur par défaut lors du chargement du shader
* [Vue 3D] Nuanceur PBR : typo Diffuse vs baseColor
* [Library] Le chemin de bibliothèque non récursif casse les textures liées dans les packages
* [Bibliothèque] Les mappages d&#39;environnement n&#39;affichent pas .hdr
* [Explorer] L’option « Copier/Coller » sur la substance ne doit pas être possible
* [Explorateur] Cliquez avec le bouton droit sur l’option Coller qui est toujours disponible sur un graphique.
* [Fonction] l’info-bulle de l’échantillonneur est incorrecte
* [Graphique] En mode compact, les instances n’affichent pas tous les noms de lien lorsqu’elles sont développées automatiquement pour ajouter un convertisseur de niveaux de gris
