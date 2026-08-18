---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Découvrez comment déboguer les plug-ins Substance 3D Designer Python à l’aide du code Visual Studio pour un développement efficace.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Débogage de plug-ins à l'aide de Visual Studio Code
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Débogage de plug-ins à l&#39;aide de Visual Studio Code

En tant que norme de workflow pour de nombreux développeurs, l&#39;**IDE de code Visual Studio** est disponible pour déboguer les plug-ins Python.

>[!WARNING]
>
> La méthode <b>debugpy.look()</b> peut permettre à toute personne qui peut se connecter au port spécifié d&#39;exécuter du code arbitraire dans le processus débogué.
> 
> Par conséquent, le débogage ne doit *<b>être configuré</b>* que sur *réseaux sécurisés*.

Afin de configurer la synergie entre Visual Studio Code et Substance 3D Designer, procédez comme suit :

1. Installez **[Visual Studio Code](https://code.visualstudio.com/)** et l&#39;**[extension Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**.
1. Installez le **[module Debugpy Python](https://github.com/microsoft/debugpy)**.

   >[!NOTE]
   >
   > Assurez-vous que l&#39;interpréteur Python dans Designer peut trouver le module &#39;*debugpy*&#39;. Le moyen le plus simple consiste à ajouter le répertoire dans lequel le module &#39;*debug*&#39; est à la variable d&#39;environnement **PYTHONPATH**. Vous pouvez également modifier sys.path dans votre script pour ajouter le chemin d&#39;accès au module de débogage.
1. Lancez l&#39;application, ouvrez l&#39;éditeur Python et **exécutez le code suivant** :

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. Dans Visual Studio Code, ouvrez votre projet et créez un fichier **launch.json**. Ajoutez les éléments suivants dans le fichier :

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. Cliquez sur l&#39;icône <b>Déboguer</b>, créez ou modifiez votre configuration de débogueur, si nécessaire.
1. Sélectionnez la configuration **Python : Attach to Designer** et cliquez sur **Démarrer le débogage**.

   Vous devriez maintenant être en mesure de définir des points d&#39;arrêt, de parcourir le code et d&#39;utiliser toutes les autres fonctionnalités du débogueur de Visual Studio Code.
