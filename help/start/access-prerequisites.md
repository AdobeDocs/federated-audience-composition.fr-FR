---
title: Conditions préalables et mécanismes de sécurisation pour la composition d’audiences fédérées
description: Découvrez les conditions préalables, les autorisations et les mécanismes de sécurisation pour la composition d’audiences fédérées
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
TQID: https://experienceleague.adobe.com/VBIotVn1VyiFJChb3mM0VDLUSbG9aQOmbfGnfGgqvhU
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: tm+mt
source-wordcount: 386
ht-degree: 100%

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
* Google BigQuery
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Vous pouvez découvrir comment créer une connexion avec ces systèmes dans la [vue d’ensemble des connexions](../connections/home.md).

## Sandbox

Lors de l’achat de la composition d’audiences fédérées, vous avez droit à deux sandbox. Pour toute demande de sandbox supplémentaire, contactez votre représentant ou représentante Adobe.

Pour afficher la liste de vos sandbox actifs de composition d’audiences fédérées, procédez comme suit :

1. À partir de la composition d’audiences fédérées, accédez au menu **[!UICONTROL Utilisation des licences]** sous **[!UICONTROL Administration]**.

1. Sélectionnez l’icône ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) de **[!UICONTROL Volume total de sortie de données]** pour accéder aux propriétés de votre sandbox.

   ![](assets/sandbox_1.png)

1. Les informations sur votre sandbox s’affichent dans la fenêtre contextuelle Propriétés.

   ![](assets/sandbox_2.png)

## Autorisations {#permissions}

Pour accéder à la composition d’audiences fédérées, les personnes doivent être ajoutées au profil de produit spécifique au sandbox créé lors de l’achat et l’autorisation **[!UICONTROL Gérer Federated Data]** doit leur être attribuée. [En savoir plus](/help/governance-privacy-security/access-control.md)

## Listes autorisées des adresses IP {#ip}

Pour activer en toute sécurité l’accès de la Composition d’audiences fédérées à vos bases de données, vous devez obtenir les adresses IP des serveurs de Composition d’audiences fédérées qui y accéderont. Ces adresses IP s’affichent lors de l’ajout d’une base de données fédérées dans l’interface d’utilisation d’Adobe Experience Platform. [En savoir plus](../connections/home.md)

Ajoutez ces adresses IP à votre liste autorisée pour accorder l’accès à la Composition d’audiences fédérées.

## Politiques de fusion {#merge-policies}

Si votre sandbox utilise une politique de fusion **Priorité du jeu de données**, contactez l’assistance clientèle d’Adobe pour ajouter le jeu de données `Halos UPS` à votre politique de fusion.

Pour plus d’informations sur les politiques de fusion, consultez la [vue d’ensemble des politiques de fusion](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/merge-policies/overview).

## Mécanismes de sécurisation et limitations {#fac-guardrails}

* Les droits, les limitations de produit et les mécanismes de sécurisation des performances répertoriés dans la [documentation Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent à la composition d’audiences fédérées.

* La composition d’audiences fédérées prend en charge l’export d’audiences volumineuses avec des tailles de fichier supérieures à 1 Go. Pour des performances optimales, la taille de fichier maximale recommandée est de 20 Go.
