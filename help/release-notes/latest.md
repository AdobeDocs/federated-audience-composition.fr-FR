---
title: Notes De Mise À Jour De La Composition D’Audiences Fédérées
description: Dernières mises à jour et notes de mise à jour pour la composition d’audiences fédérées.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
TQID: https://experienceleague.adobe.com/AqtqibUr1TNXwQ9lrtVoQ3CBNwyjSMS64e4s8y4iTSc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
source-git-commit: 8da27489f6767e837828456b2b11c8238ea6a0a4
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 12%

---

# Notes de mise à jour

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version du 26 juin {#fac-26-06}

La version de juin de Federated Audience Composition prend en charge les fonctionnalités suivantes :

| Connecteur API REST avec prise en charge de la passerelle [!DNL Apigee] pour Google [!DNL BigQuery] |
| --- |
| Vous pouvez désormais vous connecter à Google [!DNL BigQuery] à l’aide d’un connecteur d’API REST, avec la possibilité d’acheminer votre connexion via une passerelle [!DNL Apigee] lors de l’utilisation de l’authentification de compte de service. Pour plus d’informations sur la connexion à l’aide de [!DNL Apigee], consultez la [présentation des connexions](/help/connections/home.md#apigee). |

## Version du 26 mai {#fac-26-05}

La version de mai de Federated Audience Composition prend en charge les fonctionnalités suivantes :

| Authentification WIF (Workload Identity Federation) pour les [!DNL BigQuery] Google |
| --- |
| Vous pouvez désormais vous connecter à Google [!DNL BigQuery] à l’aide de l’authentification WIF. Pour plus d’informations sur la connexion à l’aide de l’authentification WIF, veuillez lire la [présentation des connexions](/help/connections/home.md#wif-configuration). |

### Améliorations {#fac-26-05-improvements}

Cette version s’accompagne de l’amélioration suivante.

- **Ciblage d’entités multiples avec audiences de composition d’audiences fédérées dans les parcours Adobe Journey Optimizer Lecture d’audience**

  Vous pouvez désormais utiliser les attributs d’audience FAC comme identifiants supplémentaires dans les parcours Journey Optimizer Lecture d’audience . Vous pouvez ainsi activer les audiences au niveau de plusieurs entités telles que des comptes ou des abonnements.

  Pour plus d’informations, veuillez lire le guide [&#x200B; Utilisation d’identifiants supplémentaires dans parcours &#x200B;](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

## Version d’avril 2026 {#fac-26-04}

La version d’avril de la composition de l’audience fédérée prend en charge les fonctionnalités et améliorations suivantes :

### Nouvelles fonctionnalités {#fac=26-04-feature}

| Nouveau connecteur - Teradata |
| --- |
| Le connecteur Teradata est désormais disponible pour une utilisation avec la composition d’audiences fédérées. Vous pouvez utiliser le connecteur Teradata pour les cas d’utilisation de création et d’enrichissement d’audiences. Pour plus d’informations sur le connecteur Teradata, consultez la [présentation des connexions](/help/connections/home.md). |

### Améliorations {#fac-26-04-improvements}

Cette version s’accompagne de l’amélioration suivante.

- **Prise en charge des clés non chiffrées pour Snowflake**

  Vous pouvez désormais utiliser des clés non chiffrées lors de l’utilisation de l’authentification par paire de clés pour vous connecter aux entrepôts de données Snowflake.

  Pour en savoir plus sur l’utilisation de clés non chiffrées avec Snowflake, consultez la [présentation des connexions](/help/connections/home.md).

## Version de mars 2026 {#fac-26-03}

La version de mars de la composition de l’audience fédérée prend en charge les fonctionnalités suivantes :

### Nouvelles fonctionnalités {#fac-26-03-feature}

| Segmentation optimisée par l’IA |
| --- |
| Vous pouvez désormais créer des compositions d’audiences fédérées de manière autonome dans l’assistant AI. Lors de l’utilisation de l’assistant AI pour créer l’audience, l’assistant AI génère un plan qui, une fois que vous l’avez approuvé, sera exécuté dans votre navigateur. Pour plus d’informations sur l’utilisation de l’assistant AI pour créer des audiences, consultez la présentation de l’assistant [&#x200B; AI](/help/start/ai-assistant.md). |

| Assistant IA pour les informations opérationnelles |
| --- |
| Vous pouvez maintenant poser des questions à l’assistant AI sur les informations opérationnelles de la composition des audiences fédérées. Les domaines pris en charge sont les connexions, les schémas et les modèles de données. Les compositions fédérées ne sont **pas** prises en charge dans cette version. Pour plus d’informations sur l’assistant AI dans la composition d’audiences fédérées, consultez la présentation de l’assistant [AI](/help/start/ai-assistant.md). |

## Version de février 2026 {#fac-26-02}

La version de février de Federated Audience Composition prend en charge les fonctionnalités suivantes :

### Nouvelles fonctionnalités {#fac-26-02-feature}

| Prise en charge de l’enrichissement des champs |
| --- |
| Vous pouvez maintenant utiliser l’activité Enregistrer le champ dans vos compositions. L&#39;activité d&#39;enregistrement de champ permet d&#39;enrichir les schémas Experience Platform en fédérant les données d&#39;entrepôts externes, ce qui permet d&#39;enrichir les schémas Experience Platform avec des attributs supplémentaires. L’activité Enregistrer le champ prend en charge les schémas B2B et B2C. Pour plus d’informations sur l’utilisation de cette activité, veuillez lire la [présentation des activités](../compositions/activities.md#save-fields). |

| Prise en charge de l’authentification avancée des briques de données |
| --- |
| Vous pouvez désormais vous connecter à la composition d’audiences fédérées avec des briques de données à l’aide de l’authentification principale du service ou d’OAuth 2.0. Pour plus d’informations sur la création d’une connexion, consultez la [présentation des connexions](../connections/home.md#create). |

## Version de janvier 2026 {#fac-26-01}

La version de janvier de la composition de l’audience fédérée prend en charge les nouvelles fonctionnalités et améliorations suivantes :

### Nouvelles fonctionnalités {#fac-26-01-feature}

| Prise en charge de l’authentification principale du service Azure Synapse |
| --- |
| Vous pouvez désormais vous connecter à la composition d’audiences fédérées avec Azure Synapse à l’aide d’un principal de service. Pour plus d’informations sur la création d’une connexion, consultez la [présentation des connexions](../connections/home.md#create). |

| Disponibilité pour les clients Adobe Experience Platform sous Amazon Web Services (AWS) |
| --- |
| Vous pouvez désormais utiliser la composition d’audiences fédérées si votre instance Experience Platform se trouve sur AWS. Pour plus d’informations sur Experience Platform sur AWS, consultez la [présentation multi-cloud](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud). |

### Améliorations {#fac-26-01-improvements}

Cette version s’accompagne de l’amélioration suivante.

- **Configuration de l’expiration des données pour les audiences**

  Vous pouvez désormais définir une expiration de données lors de l’utilisation de l’activité **Enregistrer l’audience** dans une composition.

  Pour en savoir plus sur l’expiration des données dans la composition d’audiences fédérées, consultez le guide [activités](../compositions/activities.md#save-audience).
