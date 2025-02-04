---
title: Conditions préalables et mécanismes de sécurisation pour la composition d’audiences fédérées
description: Découvrez les conditions préalables, les autorisations et les mécanismes de sécurisation pour la composition d’audiences fédérées
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: ed72ae722ffd5fbf14f491630b748a5009f4ebc5
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 90%

---

# Conditions préalables et mécanismes de sécurisation {#fac-access}

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer **Prime** ou **Ultimate**. La seule condition préalable pour accéder à cette fonctionnalité est d’avoir acheté le module complémentaire Composition d’audiences fédérées.

>[!AVAILABILITY]
>
>Une fois que vous avez reçu l’e-mail de bienvenue d’Adobe, il peut s’écouler quelques heures de plus avant que l’interface ne soit mise à jour et que les fonctionnalités soient mises à votre disposition.

## Systèmes pris en charge {#supported-systems}

La composition d’audiences fédérées prend en charge les entrepôts cloud suivants :

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics

Découvrez comment créer une connexion avec ces systèmes sur [cette page](../connections/connections.md).

## Sandbox

Lors de l’achat du module complémentaire Composition d’audiences fédérées, vous avez droit à deux sandbox. Pour toute demande de sandbox supplémentaire, contactez votre représentant ou représentante Adobe.

## Autorisations {#permissions}

Pour accéder à la composition de l’audience fédérée, les utilisateurs doivent être ajoutés au profil de produit spécifique au sandbox créé lors de l’achat et l’autorisation **[!UICONTROL Gérer les données fédérées]** doit leur être attribuée. [En savoir plus](feature-access.md)

## Listes autorisées des adresses IP {#ip}

Pour activer en toute sécurité l’accès de la Composition d’audiences fédérées à vos bases de données, vous devez obtenir les adresses IP des serveurs de Composition d’audiences fédérées qui y accéderont. Ces adresses IP s’affichent lors de l’ajout d’une base de données fédérées dans l’interface d’utilisation d’Adobe Experience Platform. [En savoir plus](../connections/connections.md)

Ajoutez ces adresses IP à votre liste autorisée pour accorder l’accès à la composition d’audiences fédérées.

## Mécanismes de sécurisation et limitations {#fac-guardrails}

* La Composition d’audiences fédérées est actuellement indisponible pour les clientes et clients [ingérant des données sur la santé](https://experienceleague.adobe.com/fr/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}. [En savoir plus](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Les droits, les limitations de produit et les mécanismes de sécurisation des performances répertoriés dans la [documentation Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent à ce module complémentaire.
