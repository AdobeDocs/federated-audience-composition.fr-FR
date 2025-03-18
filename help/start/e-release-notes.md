---
title: Nouveautés de la composition d’audiences fédérées Experience Platform
description: Dernières mises à jour et notes de mise à jour
hide: true
hidefromtoc: true
source-git-commit: 016623ed6aa6e3b2c4dafa5733fd6d1a00109271
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 66%

---

# Notes de mise à jour {#rn-new}

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version de mars 2025 {#fac-25-3}

### Améliorations {#fac-25-3-improvements}

Cette version est fournie avec les améliorations ci-dessous.

* **Autorisations de composition d’audiences fédérées**

  À compter de la version de mars, [!DNL Federated Audience Composition] commencera à appliquer l’accès aux interfaces **Federated Data Management** et **Federated Compositions** aux utilisateurs qui disposent de l’autorisation **Gérer les données fédérées**.

  Nous recommandons aux utilisateurs de contacter les administrateurs pour que cette autorisation soit ajoutée à leur rôle afin de continuer à accéder à l’interface utilisateur [!DNL Federated Audience Composition].

  Pour savoir comment attribuer cette autorisation, consultez la [documentation détaillée](feature-access.md).

* **Vue Zone de travail du modèle de données**

  La vue Zone de travail de la section Modèles de données améliore l’expérience en permettant la visualisation des modèles de données et de leurs liens dans une disposition Zone de travail, à côté de la vue tabulaire existante. [En savoir plus](../data-management/gs-models.md)

* **Export d’audience**

  La composition de l’audience fédérée prend désormais en charge l’exportation d’audiences volumineuses, gérant des tailles de fichier allant jusqu’à 20 Go.

* **Assistant IA**

  L’assistant d’IA est une fonctionnalité d’interface utilisateur conçue pour vous aider à parcourir et à comprendre les concepts Adobe et à obtenir des informations opérationnelles pour votre environnement spécifique. Il est disponible dans plusieurs produits dans Adobe Experience Cloud, y compris la composition de l’audience fédérée.

### Compatibilité {#fac-25-3-compat}

* **Connexion Databricks**

  Avec cette nouvelle version, la composition d’audiences fédérées prend désormais en charge la connectivité de lien privé pour les connexions à la base de données Databricks.
Il permet également des connexions sécurisées aux bases de données Databricks hébergées sur Amazon Web Services (AWS) et Azure. [En savoir plus](../connections/federated-db.md#databricks)

* **Prise en charge des clients B2B CDP**

  La composition de l’audience fédérée est désormais disponible pour les clients de la plateforme de données clients (CDP) B2B (Business-to-Business) pour les cas d’utilisation d’audience basés sur les personnes.

* **Connexion sécurisée Snowflake**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge les connexions de liens privées sécurisées vers des bases de données Snowflake hébergées sur Azure. [En savoir plus](../connections/federated-db.md#snowflake)

## Version de février 2025 {#fac-25-2}

Cette version est fournie avec les modifications répertoriées ci-dessous.

* **Prise en charge de Microsoft Fabric**

  Vous pouvez désormais établir des connexions à des bases de données Microsoft Fabric par le biais de la composition d’audiences fédérées. [En savoir plus](../connections/federated-db.md)

* **Prise en charge d’Amazon Redshift Spectrum**

  Amazon Redshift Spectrum est désormais pris en charge pour les connexions Amazon Redshift Database. [En savoir plus](../connections/federated-db.md#amazon-redshift)

* **Expérience améliorée de création de schéma**

  Le processus de création de schéma a été amélioré grâce à une interface d’utilisation mise à jour, conçue pour être plus intuitive et plus facile à parcourir. Ces améliorations offrent aux personnes utilisant des données un moyen plus fluide et plus efficace de développer des modèles de données. [En savoir plus](../customer/schemas.md)

* **Prise en charge de l’enrichissement de l’audience pour Databricks**

  Vous pouvez désormais utiliser Databricks dans le flux Lecture d’audience, ce qui active les bases de données Databricks et permet de les configurer en tant que nouvelle destination. [En savoir plus](../connections/destinations.md)

## Version de novembre 2024 {#fac-24-11}

### Améliorations {#fac-24-11-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Liste autorisée d’adresses IP**

  Lors de l’ajout d’une base de données fédérée dans l’interface d’utilisation d’Adobe Experience Platform, vous pouvez désormais afficher directement les adresses IP associées à vos instances de composition d’audiences fédérées. Vous pouvez ainsi facilement copier et autoriser ces adresses IP pour vous connecter à votre base de données afin d’améliorer la sécurité et la flexibilité. [En savoir plus](../connections/connections.md)

## Version d’octobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Auparavant disponible pour un ensemble d’organisations (LA), la composition d’audiences fédérées Adobe Experience Platform est désormais disponible pour tous les utilisateurs et utilisatrices (GA). Cette fonctionnalité est activée en fonction de votre offre et n’est visible qu’avec les autorisations associées. [En savoir plus](access-prerequisites.md)
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

La composition des audiences fédérées dote les entreprises d’un accès flexible et étendu aux entrepôts de données d’entreprise afin de composer des audiences à l’aide de jeux de données d’entreprise stratégiques et d’alimenter les expériences initiées par la marque et instantanées. Grâce à cette nouvelle approche, en tant qu’utilisateur ou utilisatrice d’[Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/home){target="_blank"} et/ou d’[Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/ajo-home){target="_blank"}, vous pouvez fédérer les données d’audience directement à partir de votre entrepôt de données existant pour enrichir les audiences Adobe Experience Platform dans un seul système.

La composition de l’audience fédérée répond à la demande croissante du marché pour les entreprises qui ont besoin de flexibilité pour composer des audiences avec des jeux de données d’entrepôt. Elle permet aux entreprises de réduire le mouvement des données tout en mettant les données d’audience critiques à la disposition des équipes marketing pour répondre aux besoins des cas d’utilisation et alimenter les expériences personnalisées.

Pour en savoir plus sur les fonctionnalités de la composition d’audiences fédérées, reportez-vous à [cette page](get-started.md) et aux [questions fréquentes](faq.md).

Pour plus d’informations sur les conditions préalables à l’accès aux compositions d’audiences fédérées et aux mécanismes de sécurisation actuels, consultez [cette page](access-prerequisites.md).


