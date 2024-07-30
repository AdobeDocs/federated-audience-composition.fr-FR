---
audience: end-user
title: Créer et gérer des connexions avec des bases de données fédérées
description: Découvrir comment créer et gérer des connexions avec des bases de données fédérées
badge: label="Disponibilité limitée" type="Informative"
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 19%

---

# Créer des connexions {#connections-fdb}

La composition d’audiences fédérées Experience Platform permet au client de créer et d’enrichir des audiences à partir d’entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform.

Pour travailler avec votre base de données fédérée et Adobe Experience Platform, vous devez d’abord établir une connexion. Cette connexion est configurée dans une interface utilisateur dédiée disponible dans l’interface utilisateur de Adobe Experience Platform, comme décrit dans cette page.

Pour configurer une connexion à votre base de données, procédez comme suit :

1. Accédez à la section **[!UICONTROL FEDERATED DATA]** sur le rail de gauche.

1. Dans le lien **[!UICONTROL Federated Datases]**, cliquez sur le bouton **[!UICONTROL Ajouter une base de données fédérée]** .

   ![](assets/connections_list.png){zoomable="yes"}

1. Définissez la connexion **[!UICONTROL Propriétés]**, avec le nom et le type de votre base de données.

   ![](assets/connections_name.png){zoomable="yes"}

   La sélection de son type vous donne accès à d’autres propriétés à remplir. Pour en savoir plus ici sur les bases de données prises en charge dans [cette page](federated-db.md).

   ![](assets/connections_details.png){zoomable="yes"}

   Les paramètres de configuration dépendent du type de votre base de données. Accédez aux liens ci-dessous pour accéder aux détails dont vous avez besoin pour configurer la connexion :

   * [Amazon Redshift](federated-db.md#amazon-redshift)
   * [Azure Synapse](federated-db.md#azure-synapse-redshift)
   * [Google BigQuery](federated-db.md#google-big-query)
   * [Snowflake](federated-db.md#snowflake)
   * [Vertica Analytics](federated-db.md#vertica-analytics)

1. Une fois les détails renseignés, cliquez sur le bouton **[!UICONTROL Tester la connexion]** et sur le bouton **[!UICONTROL Déployer les fonctions]** .

1. Terminez la création de votre connexion en cliquant sur le bouton **[!UICONTROL Enregistrer]**.

   ![](assets/connections_testdeploy.png){zoomable="yes"}

   Une vue d’ensemble de votre connexion à la base de données fédérée est disponible, comme illustré ci-dessous :

   ![](assets/connections_overview.png){zoomable="yes"}
