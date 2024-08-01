---
audience: end-user
title: Utiliser l’activité Rendez-vous
description: Découvrir comment utiliser l’activité Rendez-vous
badge: label="Disponibilité limitée" type="Informative"
exl-id: 9648f17b-e54c-4bc2-8dff-d35c438eeb8b
source-git-commit: 6aec8f5d9e8550ece2b50234d86ed59938f1b028
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 100%

---

# Rendez-vous {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Activité Rendez-vous"
>abstract="L’activité **Rendez-vous** vous permet de synchroniser plusieurs branches d’exécution d’une composition. Elle est déclenchée une fois toutes les activités précédentes terminées. Vous pouvez ainsi vous assurer que certaines activités sont terminées avant de continuer à exécuter la composition."

L’activité **Rendez-vous** vous permet de synchroniser plusieurs branches d’exécution d’une composition.

L’activité Rendez-vous ne déclenche sa transition sortante qu’une fois toutes les transitions entrantes activées, c’est-à-dire quand toutes les activités précédentes sont terminées. Vous pouvez ainsi vous assurer que certaines activités sont terminées avant de continuer à exécuter la composition.

## Configurer l’activité Rendez-vous {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configurer l’activité Rendez-vous"
>abstract="Sélectionnez les activités auxquelles vous souhaitez adhérer. Dans l’**[!UICONTROL Ensemble principal]**, choisissez la population de transition entrante à conserver."

Pour configurer l’activité **Rendez-vous**, procédez comme suit :

1. Ajoutez plusieurs activités afin de former au moins deux branches d’exécution différentes.
1. Ajoutez une activité **Rendez-vous** à l’une des branches.

   ![](../assets/and-join.png)

1. Dans les **[!UICONTROL Options de fusion]**, cochez les activités précédentes à synchroniser.
1. Dans l’**[!UICONTROL Ensemble principal]**, choisissez la population de transition entrante à conserver. La transition sortante ne peut contenir que l’une des populations des transitions entrantes. Si l’activité n’est pas paramétrée, la transition sortante contiendra aléatoirement l’une des populations entrantes.
