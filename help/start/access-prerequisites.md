---
title: Conditions préalables et mécanismes de sécurisation pour la composition d’audiences fédérées
description: Découvrez les conditions préalables, les autorisations et les mécanismes de sécurisation pour la composition d’audiences fédérées
badge: label="Disponibilité limitée" type="Informative"
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: de5955ad481061c6f8e488c86fc9666736a2fa1e
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 92%

---

# Conditions préalables et mécanismes de sécurisation {#fac-access}

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer **Prime** ou **Ultimate**. La seule condition préalable pour accéder à cette fonctionnalité est d’avoir acheté le module complémentaire Composition d’audiences fédérées.

>[!AVAILABILITY]
>
>Une fois que vous avez reçu l’e-mail de bienvenue d’Adobe, il peut s’écouler quelques heures de plus avant que l’interface ne soit mise à jour et que les fonctionnalités soient mises à votre disposition.

## Systèmes pris en charge {#supported-systems}

Federated Audience Composition prend en charge les entrepôts cloud suivants :

* Amazon Redshift
* Azure Synapse
* Databricks
* Google BigQuery
* Snowflake
* Vertica Analytics

Découvrez comment créer une connexion avec ces systèmes dans [cette page](../connections/connections.md).

## Autorisations {#permissions}

Lorsque vous achetez le module complémentaire Composition d’audiences fédérées, un profil de produit est créé pour chaque sandbox actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention de nommage : `ACP_FAC - <<SandboxName>> - admin.`. Pour accéder à la composition d’audiences fédérées pour un sandbox spécifique, les personnes doivent être ajoutées au profil de produit créé pour ce sandbox.

Par exemple, si un nouveau sandbox nommé « fac-test » est activé, un profil de produit correspondant « ACP_FAC - fac-test - admin » est créé. Pour accéder à la composition d’audiences fédérées avec ce sandbox, les personnes doivent être ajoutées à ce profil de produit.

## Listes autorisées des adresses IP {#ip}

Pour activer en toute sécurité la composition d’audiences fédérées et accéder à vos bases de données, contactez votre représentant ou représentante Adobe afin d’obtenir les adresses IP des serveurs de composition d’audiences fédérées qui y accéderont.

Ajoutez ces adresses IP à votre liste autorisée pour accorder l’accès à la composition d’audiences fédérées.

## Mécanismes de sécurisation et limitations {#fac-guardrails}

* La composition d’audiences fédérées n’est actuellement pas disponible pour la clientèle qui [ingère des données d’intégrité](https://experienceleague.adobe.com/fr/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} et la clientèle Adobe Journey Optimizer Privacy &amp; Security Shield. [En savoir plus](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Les droits, les limitations de produit et les mécanismes de sécurisation des performances répertoriés dans la [documentation Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent à ce module complémentaire.
