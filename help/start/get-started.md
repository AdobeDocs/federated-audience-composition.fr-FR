---
title: Prise en main de la composition d’audiences fédérées
description: Découvrez ce qu’est la composition d’audiences fédérées Adobe et comment l’utiliser dans Adobe Experience Platform
badge: label="Disponibilité limitée" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 3b4f5284cd65cd5cd30c4223fe2df3ffff7c0905
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 11%

---

# Prise en main de la composition d’audiences fédérées {#gs-fac}

Federated Audience Composition est un module complémentaire d’Adobe Real-Time Customer Data Platform et de Adobe Journey Optimizer qui vous permet de créer et d’enrichir des audiences à partir de vos entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform. Federated Audience Composition offre une solution simple et puissante pour connecter votre entrepôt de données d’entreprise directement dans Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer et exécuter des requêtes sur les tables de votre entrepôt de données.

Adobe Federated Audience Composition permet aux utilisateurs d’applications Adobe Experience Platform d’accéder aux données de leurs clients stockées dans leurs entrepôts de données et plateformes de stockage dans le cloud, telles que Amazon Redshift, Azure Synapse Analytics, etc. Les données client peuvent se trouver dans plusieurs entrepôts de données et sont désormais accessibles instantanément, sans réplication. Les plateformes prises en charge sont répertoriées dans [cette page](../connections/federated-db.md#supported-db).

## Cas d’utilisation {#rn-uc}

Dans une interface utilisateur conviviale pour le marketing, créez des règles de segmentation qui recherchent dans votre entrepôt de données une liste d’utilisateurs qualifiés pour un segment spécifique nécessaire aux campagnes marketing, accédez aux audiences existantes de l’entrepôt pour activation ou enrichissez les audiences Adobe Experience Platform avec des points de données supplémentaires qui existent dans l’entrepôt.

Dans cette version, deux cas d’utilisation sont disponibles : Création d’audience et Enrichissement d’audience.

![diagramme](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Principales étapes {#gs-steps}

Adobe la composition des audiences fédérées vous permet de créer et de mettre à jour des audiences Adobe Experience Platform directement à partir de votre base de données, sans processus d’ingestion.

![diagramme](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}

Principales étapes :

1. **Intégration de données** : rassemble des données provenant de diverses sources et les fusionne dans un jeu de données unifié. Découvrez comment connecter les applications Adobe Experience Platform et votre entrepôt de données d’entreprise, les bases de données prises en charge et comment les configurer sont présentées dans [cette section](../connections/federated-db.md).

2. **Modélisation des données** : concevez et créez des modèles et des schémas de données qui définissent la structure, les relations et les contraintes des données. Pour en savoir plus sur les schémas, consultez [cette page](../customer/schemas.md). Découvrez comment créer des liens pour votre modèle de données dans [cette page](../data-management/gs-models.md).

3. **Transformation des données** : appliquez des techniques de manipulation de données pour modifier le format, la structure ou les valeurs des éléments de données afin de les rendre compatibles ou adaptés à des analyses ou applications spécifiques.

4. **Utilisation des données** : créez, orchestrez et créez des audiences. Découvrez comment composer des audiences dans [cette page](../compositions/gs-compositions.md). Vous pouvez également mettre à jour ou réutiliser des audiences existantes via Adobe Experience Platform Audience Portal et les destinations. En savoir plus sur [cette page](../connections/destinations.md)


>[!NOTE]
>
>Après l’exécution de la composition, l’audience obtenue est enregistrée dans Adobe Experience Platform en tant qu’audience externe et disponible dans la plateforme de données clients en temps réel d’Adobe et/ou Adobe Journey Optimizer. Elle est rendue accessible dans le menu **Audiences** . [En savoir plus](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## En savoir plus {#learn}

<!-- Workflow + Workflow activities-->

Reportez-vous à la section Questions fréquentes sur [cette page](faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Paramètres d’exécution"
>abstract="Dans cette section, vous pouvez paramétrer les paramètres relatifs à l&#39;exécution du workflow, par exemple le nombre de jours pendant lesquels l&#39;historique de la composition est conservé."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activité non modifiable"
>abstract="Lorsqu’une activité **Requête** ou **Enrichissement** est paramétrée avec des données supplémentaires dans la console, les données d’enrichissement sont prises en compte et transmises à la transition sortante, mais elles ne peuvent pas être modifiées."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Créer un lien"
>abstract="Définissez les paramètres du lien."
