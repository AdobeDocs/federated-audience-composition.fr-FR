---
audience: end-user
title: Créer et gérer des connexions avec des bases de données fédérées
description: Découvrir comment créer et gérer des connexions avec des bases de données fédérées
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 85%

---

# Créer des connexions {#connections-fdb}

La composition d’audiences fédérées Experience Platform permet au client de créer et d’enrichir des audiences à partir d’entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform. Les entrepôts de données pris en charge sont répertoriés dans [cette section](../start/access-prerequisites.md#supported-systems).

Pour travailler avec votre base de données fédérée et Adobe Experience Platform, vous devez d’abord établir une connexion. Cette connexion est configurée dans une interface d’utilisation dédiée disponible dans l’interface d’utilisation Adobe Experience Platform, comme décrit sur cette page.

Pour configurer une connexion à votre base de données, procédez comme suit :

1. Accédez à la section **[!UICONTROL DONNÉES FÉDÉRÉES]** sur le rail de gauche.

1. Dans le lien **[!UICONTROL Bases de données fédérées]**, cliquez sur le bouton **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/connections_list.png){zoomable="yes"}

1. Définissez la connexion **[!UICONTROL Propriétés]** avec le nom et le type de votre base de données.

   ![](assets/connections_name.png){zoomable="yes"}

   La sélection de son type vous donne accès à d’autres propriétés à remplir. Pour en savoir plus sur les bases de données prises en charge, consultez [cette page](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   Les paramètres détaillés dépendent du type de votre base de données. Accédez aux liens ci-dessous pour accéder aux détails dont vous avez besoin pour configurer la connexion :

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Databricks](federated-db.md#databricks)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Une fois les détails renseignés, cliquez sur les boutons **[!UICONTROL Tester la connexion]** et **[!UICONTROL Déployer les fonctions]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

1. Terminez la création de votre connexion en cliquant sur le bouton **[!UICONTROL Enregistrer]**.

   Une vue d’ensemble de votre connexion à la base de données fédérée est disponible, comme illustré ci-dessous :

   ![](assets/connections_overview.png){zoomable="yes"}
