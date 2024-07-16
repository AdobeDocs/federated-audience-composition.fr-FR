---
title: Prise en main de la composition d’audiences fédérées
description: Découvrez ce qu’est la composition d’audiences fédérées Adobe et comment l’utiliser dans Adobe Experience Platform
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Prise en main de la composition d’audiences fédérées {#gs-fac}

Adobe Federated Audience Composition permet aux utilisateurs d’applications Adobe Experience Platform d’accéder aux données de leurs clients stockées dans leur entrepôt de données d’entreprise. Les données client peuvent se trouver dans plusieurs entrepôts de données et doivent être accessibles instantanément, sans réplication.

La composition d’audiences fédérées Adobe Experience Platform offre une solution simple et puissante pour connecter directement votre entrepôt de données d’entreprise dans Adobe Real-Time Customer Data Platform et exécuter des requêtes sur les tables de votre entrepôt de données.

## Principales étapes {#gs-steps}

Adobe la composition des audiences fédérées vous permet de créer et de mettre à jour des audiences Adobe Experience Platform directement à partir de votre base de données, sans processus d’ingestion.

![diagramme](assets/FAC-diagram.png)

Principales étapes :

* **Configuration**

   1. Connectez Adobe Experience Platform et votre entrepôt de données d’entreprise.
Les bases de données suivantes sont prises en charge : Snowflake, Google Big Query, Azure Synapse, Redshift.
En savoir plus sur [cette page](../connections/federated-db.md)
   1. Créez des schémas pour sélectionner les données qui doivent être accessibles à partir de l’interface utilisateur.
En savoir plus sur [cette page](../customer/schemas.md)
   1. Créez des liens pour votre modèle de données.
En savoir plus sur [cette page](../data-management/gs-models.md)

* **Composer les audiences**

   1. Concevez et exécutez des compositions pour créer des audiences.
En savoir plus sur [cette page](../compositions/gs-compositions.md)
   1. Mise à jour ou réutilisation d’audiences existantes via le portail d’audience Adobe Experience Platform et les destinations.
En savoir plus sur [cette page](../connections/destinations.md)

## En savoir plus {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Paramètres d’exécution"
>abstract="Dans cette section, vous pouvez définir les paramètres relatifs à l’exécution du workflow, par exemple le nombre de jours pendant lesquels l’historique du workflow est conservé."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activité non modifiable"
>abstract="Lorsqu’une activité **Requête** ou **Enrichissement** est paramétrée avec des données supplémentaires dans la console, les données d’enrichissement sont prises en compte et transmises à la transition sortante, mais elles ne peuvent pas être modifiées."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Créer un lien"
>abstract="Définissez les paramètres du lien."
