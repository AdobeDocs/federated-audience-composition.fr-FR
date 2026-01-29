---
title: Notes De Mise À Jour De La Composition D’Audiences Fédérées
description: Dernières mises à jour et notes de mise à jour pour la composition d’audiences fédérées.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 77591055e0561de07053c1ca5a0c6ab9551a5dfe
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 24%

---


# Notes de mise à jour

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

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
