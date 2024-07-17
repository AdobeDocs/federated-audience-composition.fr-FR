---
audience: end-user
title: Utilisation de l’activité Attente
description: Découvrez comment utiliser l’activité Attente
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 70%

---

# Attente {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Activité Attente"
>abstract="L’activité **Attente** est utilisée pour retarder la transition d’une activité à une autre."

L&#39;activité **Attente** laisse un certain temps s&#39;écouler entre l&#39;exécution de deux activités. Par exemple, elle permet d’attendre plusieurs jours après une activité de diffusion e-mail puis d’analyser les ouvertures et les clics générés pendant ce laps de temps avant d’appliquer d’autres traitements (e-mail de rappel, création d’audience, etc.).

## Configuration{#wait-configuration}

Pour configurer l’activité d’**attente**, procédez comme suit :

1. Ajoutez une activité **Attente** à votre composition.

1. Spécifiez la **durée** de l’attente entre les transitions entrante et sortante.

1. Sélectionnez l’unité de temps dans le champ **Périodes** : secondes, minutes, heures, jours.


