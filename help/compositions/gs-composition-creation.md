---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
badge: label="Disponibilité limitée" type="Informative"
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 59%

---

# Principes fondamentaux de la création de composition {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Propriétés de la composition"
>abstract="Dans cet écran, choisissez le modèle à utiliser pour créer la composition et indiquez un libellé. Développez la section OPTIONS SUPPLÉMENTAIRES pour configurer d’autres paramètres tels que le nom interne de la composition, son dossier, son fuseau horaire et le groupe de personnes responsables. Il est vivement recommandé de sélectionner un groupe de personnes responsables afin d’alerter les opérateurs et opératrices en cas d’erreur."

## Qu&#39;y a-t-il dans une composition ? {#gs-composition-inside}

La composition d’audience fédérée Experience Platform fournit un canevas visuel qui vous permet de créer des audiences en exploitant différentes activités (fractionnement, enrichissement, etc.).

Le diagramme de composition est une représentation de ce qui est censé se produire. Il décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Chaque composition contient :

* des **[!UICONTROL Activités]** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.
* **[!UICONTROL Transitions]** : les transitions relient une activité source à une activité de destination et définissent leur ordre.
* **[!UICONTROL Tables de travail]** : la table de travail contient toutes les informations véhiculées par la transition. Chaque composition utilise plusieurs tables de travail. Les données véhiculées dans ces tableaux peuvent être utilisées tout au long du cycle de vie de la composition.

## Étapes clés de création d’une composition {#gs-composition-steps}

Les principales étapes pour créer une composition sont les suivantes :

1. [Création et configuration de la composition](../compositions/create-composition.md)
1. [Orchestrer les activités](../compositions/orchestrate-activities.md)
1. [Exécuter la composition et suivre son exécution](../compositions/start-monitor-composition.md)
