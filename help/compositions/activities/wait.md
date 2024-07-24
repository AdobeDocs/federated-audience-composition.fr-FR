---
audience: end-user
title: Utilisation de l’activité Attente
description: Découvrez comment utiliser l’activité Attente
badge: label="Disponibilité limitée" type="Informative"
exl-id: 59857bd2-2a0b-4c97-ba4e-048dfd9af8f2
source-git-commit: 122bd469e04d72d2dac0f606c8ab4e195100d4a4
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 60%

---

# Attente {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Activité Attente"
>abstract="L’activité **Attente** est utilisée pour retarder la transition d’une activité à une autre."

L&#39;activité **Attente** laisse un certain temps s&#39;écouler entre l&#39;exécution de deux activités.

## Configuration{#wait-configuration}

Pour configurer l’activité d’**attente**, procédez comme suit :

1. Ajoutez une activité **Attente** à votre composition.

1. Spécifiez la **durée** de l’attente entre les transitions entrante et sortante.

1. Sélectionnez l’unité de temps dans le champ **Périodes** : secondes, minutes, heures, jours.

   ![](../assets/wait.png)
