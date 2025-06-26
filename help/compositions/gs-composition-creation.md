---
audience: end-user
title: Créer des compositions
description: Découvrir comment créer des compositions
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: b73eba776e3e75f3ff7107bcf48f7b2f60048d08
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 100%

---

# Principes fondamentaux de la création d’une composition {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Propriétés de la composition"
>abstract="Dans cet écran, choisissez le modèle à utiliser pour créer la composition et indiquez un libellé. Développez la section OPTIONS SUPPLÉMENTAIRES pour configurer d’autres paramètres tels que le nom interne de la composition, son dossier, son fuseau horaire et le groupe de personnes responsables. Il est vivement recommandé de sélectionner un groupe de personnes responsables afin d’alerter les opérateurs et opératrices en cas d’erreur."

## Qu’y a-t-il dans une composition ? {#gs-composition-inside}

La composition d’audiences fédérées Experience Platform met à votre disposition une zone de travail visuelle qui vous permet de créer des audiences et de tirer parti de diverses activités (partager, enrichir, etc.).

Le diagramme de composition est une représentation de ce qui est censé se produire. Il décrit les différentes tâches à effectuer et la manière dont elles sont liées.

![](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

Chaque composition comprend :

* des **[!UICONTROL Activités]** : une activité est une tâche à effectuer. Les différentes activités disponibles sont représentées sur le diagramme par des icônes. Chaque activité possède des propriétés spécifiques et d’autres propriétés communes à toutes les activités.
* **[!UICONTROL Transitions]** : les transitions relient une activité source à une activité de destination et définissent leur ordre.
* **[!UICONTROL Tables de travail]** : la table de travail contient toutes les informations véhiculées par la transition. Chaque composition utilise plusieurs tables de travail. Les données transmises dans ces tables peuvent être utilisées tout au long du cycle de vie de la composition.

## Étapes clés de la création dʼune composition {#gs-composition-steps}

Voici les étapes principales de création dʼune composition :

1. [Créer et configurer la composition](../compositions/create-composition.md)
1. [Orchestrer les activités](../compositions/orchestrate-activities.md)
1. [Exécuter la composition et effectuer le suivi de son exécution](../compositions/start-monitor-composition.md)
