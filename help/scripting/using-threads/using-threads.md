---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: Découvrez comment utiliser les threads dans les scripts Substance 3D Designer Python pour le traitement et les performances parallèles.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilisation des threads
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Utilisation des threads

Il est possible pour les plug-ins de <b>créer des threads</b> à l&#39;aide du module de threading de Python *ou* Qt pour les classes liées au threading de Python.

Cela peut être utile pour effectuer des traitements en arrière-plan ou des opérations d’E/S pendant l’exécution de Designer.

Il est important de noter que la plupart des classes et méthodes de l&#39;API Python Designer peuvent *être appelées uniquement* à partir du <b>thread d&#39;application principal</b>. Ainsi, si vous souhaitez apporter des modifications à un graphique actuellement ouvert dans Designer, vous devez les effectuer à partir du thread d’application principal.

Une solution possible consiste à utiliser <b>QThread</b> et <b>les connexions placées en file d&#39;attente</b>, comme dans l&#39;exemple suivant :

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
