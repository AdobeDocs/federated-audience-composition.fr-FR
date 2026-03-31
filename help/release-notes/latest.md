---
title: Notes De Mise À Jour De La Composition D’Audiences Fédérées
description: Dernières mises à jour et notes de mise à jour pour la composition d’audiences fédérées.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: d3a97b5887778f910ca8f09f7cb8fa99360a612c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 8%

---


# Notes de mise à jour

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version du 26 mars {#fac-26-03}

La version de mars de la composition de l’audience fédérée prend en charge les fonctionnalités suivantes :

### Nouvelles fonctionnalités {#fac-26-03-feature}

| Segmentation optimisée par l’IA |
| --- |
| Vous pouvez désormais créer des compositions d’audiences fédérées de manière autonome dans l’assistant AI. Lors de l’utilisation de l’assistant AI pour créer l’audience, l’assistant AI génère un plan qui, une fois que vous l’avez approuvé, sera exécuté dans votre navigateur. Pour plus d’informations sur l’utilisation de l’assistant AI pour créer des audiences, consultez la présentation de l’assistant [ AI](/help/start/ai-assistant.md). |

| Assistant IA pour les informations opérationnelles |
| --- |
| Vous pouvez maintenant poser des questions à l’assistant AI sur les informations opérationnelles de la composition des audiences fédérées. Les domaines pris en charge sont les connexions, les schémas et les modèles de données. Les compositions fédérées ne sont **pas** prises en charge dans cette version. Pour plus d’informations sur l’assistant AI dans la composition d’audiences fédérées, consultez la présentation de l’assistant [AI](/help/start/ai-assistant.md). |

## Version du 26 février {#fac-26-02}

La version de février de Federated Audience Composition prend en charge les fonctionnalités suivantes :

### Nouvelles fonctionnalités {#fac-26-02-feature}

| Prise en charge de l’enrichissement des champs |
| --- |
| Vous pouvez maintenant utiliser l’activité Enregistrer le champ dans vos compositions. L&#39;activité d&#39;enregistrement de champ permet d&#39;enrichir les schémas Experience Platform en fédérant les données d&#39;entrepôts externes, ce qui permet d&#39;enrichir les schémas Experience Platform avec des attributs supplémentaires. L’activité Enregistrer le champ prend en charge les schémas B2B et B2C. Pour plus d’informations sur l’utilisation de cette activité, veuillez lire la [présentation des activités](../compositions/activities.md#save-fields). |

| Prise en charge de l’authentification avancée des briques de données |
| --- |
| Vous pouvez désormais vous connecter à la composition d’audiences fédérées avec des briques de données à l’aide de l’authentification principale du service ou d’OAuth 2.0. Pour plus d’informations sur la création d’une connexion, consultez la [présentation des connexions](../connections/home.md#create). |

## Version du 26 janvier {#fac-26-01}

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
