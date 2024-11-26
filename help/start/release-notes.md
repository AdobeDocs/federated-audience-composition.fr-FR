---
title: Nouveautés de la composition d’audiences fédérées Experience Platform
description: Dernières mises à jour et notes de mise à jour
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: ht
source-wordcount: '461'
ht-degree: 100%

---

# Notes de mise à jour {#rn-new}

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version d’octobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Auparavant disponible pour un ensemble d’organisations (LA), la composition d’audiences fédérées Adobe Experience Platform est désormais disponible pour tous les utilisateurs et utilisatrices (GA). Ce module complémentaire est activé en fonction de votre offre et n’est visible qu’avec les autorisations associées. [En savoir plus](access-prerequisites.md)
>

### Compatibilité {#fac-24-10-compat}

Avec cette nouvelle version, la composition d’audiences fédérées est désormais compatible avec les systèmes répertoriés ci-dessous.

* **Prise en charge de Databricks**

  Vous pouvez désormais établir des connexions à des bases de données Databricks par le biais de la composition d’audiences fédérées. [En savoir plus](../connections/federated-db.md#databricks)

* **Prise en charge de l’accès sécurisé à Snowflake via AWS PrivateLink**

  L’accès sécurisé à votre entrepôt de données Snowflake externe par le biais d’un lien privé est désormais pris en charge. Notez que votre compte Snowflake doit être hébergé sur Amazon Web Services (AWS) et situé dans la même région que votre environnement de composition d’audiences fédérées. Veuillez contacter votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé à votre compte Snowflake. [En savoir plus](../connections/federated-db.md#snowflake)

* **Prise en charge d’Amazon Redshift sans serveur**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge [Amazon Redshift sans serveur](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Améliorations {#fac-24-10-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Actualiser les schémas existants**

  Lorsqu’une colonne est créée, modifiée ou supprimée dans une base de données fédérée, vous pouvez désormais détecter et appliquer les modifications en cliquant sur le bouton **[!UICONTROL Actualiser le schéma]** dans le schéma correspondant. [En savoir plus](../customer/schemas.md#schema-refresh)

* **Associer un modèle de données à une nouvelle composition**

  Lors de la création d’une composition, vous pouvez désormais sélectionner le modèle de données à y associer. Avec cette nouvelle option, la configuration de vos activités est plus facile, car seuls les tableaux du modèle de données associé sont disponibles. [En savoir plus](../compositions/create-composition.md)

## Version de juillet 2024 : composition d’audiences fédérées (disponibilité limitée) {#fac-la}

La composition d’audiences fédérées est une fonctionnalité complémentaire qui permet aux entreprises d’accéder de manière flexible et étendue aux entrepôts de données d’entreprise, afin de composer des audiences à l’aide de jeux de données d’entreprise critiques et d’optimiser des expériences initiées par la marque et en temps réel. Grâce à cette nouvelle approche, en tant qu’utilisateur ou utilisatrice d’[Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/home){target="_blank"} et/ou d’[Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/ajo-home){target="_blank"}, vous pouvez fédérer les données d’audience directement à partir de votre entrepôt de données existant pour enrichir les audiences Adobe Experience Platform dans un seul système.

La composition d’audiences fédérées répond aux demandes croissantes du marché pour les entreprises qui ont besoin de la flexibilité nécessaire pour composer des audiences avec des jeux de données d’entrepôt. Elle permet aux entreprises de réduire le mouvement des données tout en mettant les données d’audience critiques à la disposition des équipes marketing pour répondre aux besoins des cas d’utilisation et alimenter les expériences personnalisées. 

Pour en savoir plus sur les fonctionnalités de la composition d’audiences fédérées, reportez-vous à [cette page](get-started.md) et aux [questions fréquentes](faq.md).

Pour plus d’informations sur les conditions préalables à l’accès aux compositions d’audiences fédérées et aux mécanismes de sécurisation actuels, consultez [cette page](access-prerequisites.md).

