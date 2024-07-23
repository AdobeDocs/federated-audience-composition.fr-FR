---
audience: end-user
title: Créer et gérer des connexions avec des bases de données fédérées
description: Découvrez comment créer et gérer des connexions avec des bases de données fédérées
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# Création de connexions {#connections-fdb}

L’utilisation d’une base de données fédérée directement dans AEP implique d’établir une connexion avec cette base.

Pour configurer une connexion à votre base de données, accédez à la section **[!UICONTROL DONNÉES FÉDÉRÉES]**, puis, dans le lien **[!UICONTROL Bases de données fédérées]**, cliquez sur le bouton **[!UICONTROL Ajouter une base de données fédérée]**.

![](assets/connections_list.png){zoomable="yes"}

Vous accédez à la fenêtre pour la connexion **[!UICONTROL Properties]**, avec le nom et le type de votre base de données.

![](assets/connections_name.png){zoomable="yes"}

La sélection de son type vous donne accès à d’autres propriétés à remplir. [En savoir plus sur les bases de données prises en charge](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

En fonction du type de votre base de données, découvrez dans les liens ci-dessous les informations dont vous avez besoin pour configurer la connexion :

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google BigQuery](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Une fois les détails renseignés, cliquez sur le bouton **[!UICONTROL Tester la connexion]** et sur le bouton **[!UICONTROL Déployer les fonctions]** .
Terminez la création de votre connexion en cliquant sur le bouton **[!UICONTROL Enregistrer]** .

![](assets/connections_testdeploy.png){zoomable="yes"}

Vous obtiendrez un aperçu de votre connexion à la base de données fédérée comme ceci :

![](assets/connections_overview.png){zoomable="yes"}
