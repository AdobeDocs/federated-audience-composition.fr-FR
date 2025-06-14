---
audience: end-user
title: Configurer vos bases de données fédérées
description: Découvrir comment configurer vos bases de données fédérées
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: d99bd98b5d63af55db223cf2e8dd3996d8012d24
workflow-type: ht
source-wordcount: '2128'
ht-degree: 100%

---

# Configurer vos bases de données fédérées {#federated-db}

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Bases de données fédérées"
>abstract="Les connexions existantes à des bases de données fédérées sont répertoriées sur cet écran. Pour créer une connexion, cliquez sur le bouton **[!UICONTROL Ajouter une base de données fédérée]**."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Propriétés de la base de données fédérée"
>abstract="Saisissez le nom de la nouvelle base de données fédérée et sélectionnez son type."

>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Détails de la base de données fédérée"
>abstract="Renseignez les paramètres de connexion à la nouvelle base de données fédérée. Utilisez le bouton **[!UICONTROL Tester la connexion]** pour valider votre configuration."

La composition d’audiences fédérées Experience Platform permet au client ou à la cliente de créer et d’enrichir des audiences à partir d’entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform.

Découvrez comment créer, configurer, tester et enregistrer la connexion à votre base de données externe sur [cette page](connections.md). Vous trouverez ci-dessous la liste des bases de données prises en charge et les paramètres détaillés à configurer pour chacune d’elles.

## Bases de données prises en charge {#supported-db}

Avec la composition d’audiences fédérées, vous pouvez vous connecter aux bases de données suivantes. La configuration de chaque base de données est présentée ci-dessous.

* [Amazon Redshift](#amazon-redshift)
* [Azure Synapse Analytics](#azure-synapse)
* [Google BigQuery](#google-bigquery)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)
* [Databricks](#databricks)
* [Microsoft Fabric](#microsoft-fabric)

## Amazon Redshift {#amazon-redshift}

>[!NOTE]
>
>* Seuls Amazon Redshift AWS, Amazon Redshift Spectrum et Amazon Redshift sans serveur sont pris en charge.
>
>* L’accès sécurisé à vos bases de données externes Amazon Redshift par le biais d’un lien privé est pris en charge.

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Amazon Redshift.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Amazon Redshift.

   ![](assets/federated_database_6.png)

1. Configurez les paramètres d’authentification Amazon Redshift :

   * **[!UICONTROL Serveur]** : ajoutez le nom du DNS.

   * **[!UICONTROL Compte]** : ajoutez le nom d’utilisateur ou d’utilisatrice.

   * **[!UICONTROL Mot de passe]** : ajoutez le mot de passe du compte.

   * **[!UICONTROL Base de données]** : nom de la base de données s’il n’est pas spécifié dans le DSN. Il peut rester vide s’il est spécifié dans le DSN

   * **[!UICONTROL Schéma de travail]** : nom du schéma de base de données à utiliser pour les tableaux de travail. En savoir plus dans la [Documentation Amazon](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}

     >[!NOTE]
     >
     >Vous pouvez utiliser n’importe quel schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez de l’autorisation requise pour vous connecter à ce schéma.
     >
     >**Des schémas de travail distincts** doivent être utilisés lors de la connexion de plusieurs sandbox à la même base de données.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

## Azure Synapse Analytics {#azure-synapse}

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Azure Synapse Analytics.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Azure Synapse Analytics.

   ![](assets/federated_database_4.png)

1. Configurez les paramètres d’authentification Azure Synapse Analytics :

   * **[!UICONTROL Serveur]** : saisissez l’URL du serveur Azure Synapse

   * **[!UICONTROL Compte]** : saisissez le nom d’utilisateur ou d’utilisatrice.

   * **[!UICONTROL Mot de passe]** : saisissez le mot de passe du compte.

   * **[!UICONTROL Base de données]** (facultatif) : saisissez le nom de la base de données s’il n’est pas spécifié dans le DSN.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

| Option | Description |
|---|---|
| Authentification | Type d’authentification pris en charge par le connecteur. Valeur actuelle prise en charge : ActiveDirectoryMSI. Pour plus d’informations, consultez la [documentation Microsoft SQL](https://learn.microsoft.com/fr-fr/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"} (exemple n° 8 de chaînes de connexion). |

## Google BigQuery {#google-bigquery}

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Google BigQuery.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Google BigQuery.

   ![](assets/federated_database_3.png)

1. Configurez les paramètres d’authentification Google BigQuery :

   * **[!UICONTROL Compte de service]** : saisissez l’adresse e-mail de votre **[!UICONTROL compte de service]**. Pour plus d’informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts){target="_blank"}.

   * **[!UICONTROL Projet]** : saisissez l’ID de votre **[!UICONTROL projet]**. Pour plus d’informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}.

   * **[!UICONTROL Jeu de données]** : saisissez le nom de votre **[!UICONTROL jeu de données]**. Pour plus d’informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}.

   * **[!UICONTROL Chemin d’accès au fichier de clé]** : chargez votre fichier de clé sur le serveur. Seuls les fichiers .json sont pris en charge.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

| Option | Description |
|---|---|
| ProxyType | Type de proxy utilisé pour se connecter à BigQuery par le biais des connecteurs ODBC et SDK. </br>HTTP (par défaut), http_no_tunnel, socks4 et socks5 sont actuellement pris en charge. |
| ProxyHost | Nom d’hôte ou adresse IP où le proxy peut être atteint. |
| ProxyPort | Numéro de port sur lequel le proxy s’exécute, par exemple 8080 |
| ProxyUid | Nom d’utilisateur utilisé pour le proxy authentifié |
| ProxyPwd | Mot de passe ProxyUid |
| bqpath | Notez que cela s’applique uniquement à l’outil de chargement en masse (SDK Cloud). </br> Pour éviter d’utiliser la variable PATH ou si le répertoire google-cloud-sdk doit être déplacé vers un autre emplacement, vous pouvez spécifier avec cette option le chemin exact du répertoire bin du sdk cloud sur le serveur. |
| GCloudConfigName | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> Le SDK Google Cloud utilise des configurations pour charger les données dans les tableaux BigQuery. La configuration nommée `accfda` stocke les paramètres pour le chargement des données. Cependant, cette option permet aux personnes de spécifier un nom différent pour la configuration. |
| GCloudDefaultConfigName | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> La configuration active du SDK Google Cloud ne peut pas être supprimée sans transférer au préalable la balise active vers une nouvelle configuration. Cette configuration temporaire est nécessaire pour recréer la configuration principale de chargement des données. Le nom par défaut de la configuration temporaire est `default`, et peut être modifié si nécessaire. |
| GCloudRecreateConfig | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> Lorsqu’il est défini sur `false`, le mécanisme de chargement en masse évite de tenter de recréer, de supprimer ou de modifier les configurations du SDK Google Cloud. Au lieu de cela, il procède au chargement des données à l’aide de la configuration existante sur la machine. Cette fonctionnalité est utile lorsque d’autres opérations dépendent des configurations du SDK Google Cloud. </br> Si la personne active cette option de moteur sans une configuration appropriée, le mécanisme de chargement en masse émet un message d’avertissement : `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Pour éviter d’autres erreurs, le mécanisme de chargement en masse par défaut du tableau ODBC est rétabli. |

## Snowflake {#snowflake}

>[!NOTE]
>
>L’accès sécurisé à votre entrepôt de données Snowflake externe par le biais d’un lien privé est pris en charge. Notez que votre compte Snowflake doit être hébergé sur Amazon Web Services (AWS) ou Azure et être situé dans la même région que votre environnement de composition d’audiences fédérées. Veuillez contacter votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé à votre compte Snowflake.
>

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Snowflake.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Snowflake.

   ![](assets/federated_database_2.png)

1. Configurer les paramètres d’authentification Snowflake

   * **[!UICONTROL Serveur]** : saisissez le nom de votre serveur.

   * **[!UICONTROL Utilisateur ou utilisatrice]** : saisissez votre nom d’utilisateur ou d’utilisatrice.

   * **[!UICONTROL Mot de passe]** : saisissez le mot de passe de votre compte.

   * **[!UICONTROL Base de données]** (facultatif) : saisissez le nom de votre base de données s’il n’est pas spécifié dans le DSN.

   * **[!UICONTROL Schéma de travail]** (facultatif) : saisissez le nom du schéma de base de données à utiliser pour les tableaux de travail.

     >[!NOTE]
     >
     >Vous pouvez utiliser n’importe quel schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez de l’autorisation requise pour vous connecter à ce schéma.
     >
     >**Des schémas de travail distincts** doivent être utilisés lors de la connexion de plusieurs sandbox à la même base de données.

   * **[!UICONTROL Clé privée]** : cliquez sur le champ **[!UICONTROL Clé privée]** pour sélectionner vos fichiers .pem dans votre dossier de paramètres régionaux.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

Le connecteur prend en charge les options suivantes :

| Option | Description |
|---|---|
| workschema | Schéma de base de données à utiliser pour les tables de travail. |
| warehouse | Nom de l&#39;entrepôt par défaut à utiliser. Il remplace la valeur par défaut de l&#39;utilisateur. |
| NomFuseauHoraire | Vide par défaut. Le serveur applicatif du fuseau horaire est utilisé. Il est possible d’utiliser cette option pour forcer le paramètre de session TIMEZONE. <br>Pour en savoir plus à ce sujet, consultez [cette page](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone){target="_blank"}. |
| WeekStart | Paramètre de session WEEK_START. Par défaut, cette valeur est définie sur 0. <br>Pour en savoir plus à ce sujet, consultez [cette page](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start){target="_blank"}. |
| UseCachedResult | Paramètre de session USE_CACHED_RESULTS. Par défaut, cette valeur est définie sur TRUE. Cette option peut être utilisée pour désactiver les résultats mis en cache de Snowflake. <br>Pour en savoir plus à ce sujet, consultez [cette page](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html){target="_blank"}. |
| bulkThreads | Nombre de threads à utiliser pour le chargeur en masse de Snowflake ; plus de threads signifient de meilleures performances pour les chargements en masse plus volumineux. Par défaut, cette valeur est définie sur 1. Le nombre peut être ajusté en fonction du nombre de threads de la machine. |
| chunkSize | Détermine la taille de fichier du bloc de chargeur en masse. Par défaut, cette valeur est définie sur 128 Mo. Peut être modifiée pour des performances plus optimales, lorsqu’elle est utilisée avec bulkThreads. Plus de threads actifs simultanément signifie de meilleures performances. <br>Pour plus d’informations à ce propos, consultez la [documentation Snowflake](https://docs.snowflake.net/manuals/sql-reference/sql/put.html){target="_blank"}. |
| StageName | Nom de l’étape interne préconfigurée. Elle sera utilisée en chargement massif au lieu de créer une nouvelle étape temporaire. |

## Vertica Analytics {#vertica-analytics}

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Vertica Analytics.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Vertica Analytics.

   ![](assets/federated_database_5.png)

1. Configurez les paramètres d’authentification Vertica Analytics :

   * **[!UICONTROL Serveur]** : ajoutez l’URL du serveur [!DNL Vertica Analytics].

   * **[!UICONTROL Compte]** : ajoutez le nom d’utilisateur ou d’utilisatrice.

   * **[!UICONTROL Mot de passe]** : ajoutez le mot de passe du compte.

   * **[!UICONTROL Base de données]** (facultatif) : saisissez le nom de votre base de données s’il n’est pas spécifié dans le DSN.

   * **[!UICONTROL Schéma de travail]** (facultatif) : saisissez le nom du schéma de base de données à utiliser pour les tableaux de travail.

     >[!NOTE]
     >
     >Vous pouvez utiliser n’importe quel schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez de l’autorisation requise pour vous connecter à ce schéma.
     >
     >**Des schémas de travail distincts** doivent être utilisés lors de la connexion de plusieurs sandbox à la même base de données.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

Le connecteur prend en charge les options suivantes :

| Option | Description |
|---|---|
| NomFuseauHoraire | Vide par défaut. Le serveur applicatif du fuseau horaire est utilisé. Il est possible d’utiliser cette option pour forcer le paramètre de session TIMEZONE. |

## Databricks {#databricks}

>[!NOTE]
>
>L’accès sécurisé à votre entrepôt de données Databricks externe par le biais d’un lien privé est pris en charge. Cela inclut des connexions sécurisées aux bases de données Databricks hébergées sur Amazon Web Services (AWS) via un lien privé et aux bases de données Databricks hébergées sur Microsoft Azure via un VPN. Contactez votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé.

Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Databricks.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Databricks.

   ![](assets/databricks-config.png)

1. Configurez les paramètres d’authentification de Databricks :

   * **[!UICONTROL Serveur]** : ajoutez le nom du serveur Databricks.

   * **[!UICONTROL Chemin HTTP]** : ajoutez le chemin à votre cluster ou à votre entrepôt de données. [En savoir plus](https://docs.databricks.com/fr/integrations/compute-details.html){target="_blank"}

   * **[!UICONTROL Mot de passe]** : ajoutez le jeton d’accès du compte. [En savoir plus](https://docs.databricks.com/fr/dev-tools/auth/pat.html){target="_blank"}

   * **[!UICONTROL Catalogue]** : ajoutez le champ du catalogue Databricks.

   * **[!UICONTROL Schéma de travail]** : nom du schéma de base de données à utiliser pour les tableaux de travail.

     >[!NOTE]
     >
     >Vous pouvez utiliser n’importe quel schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez de l’autorisation requise pour vous connecter à ce schéma.
     >
     >**Des schémas de travail distincts** doivent être utilisés lors de la connexion de plusieurs sandbox à la même base de données.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

Le connecteur prend en charge les options suivantes :

| Option | Description |
|---|---|
| NomFuseauHoraire | Vide par défaut. Le serveur applicatif du fuseau horaire est utilisé. Il est possible d’utiliser cette option pour forcer le paramètre de session TIMEZONE. |

## Microsoft Fabric {#microsoft-fabric}


Utilisez des bases de données fédérées pour traiter les informations stockées dans une base de données externe. Suivez les étapes ci-dessous pour configurer l’accès à Microsoft Fabric.

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Bases de données fédérées]**.

1. Cliquez sur **[!UICONTROL Ajouter une base de données fédérée]**.

   ![](assets/federated_database_1.png)

1. Saisissez un **[!UICONTROL nom]** pour votre base de données fédérée.

1. Dans la liste déroulante **[!UICONTROL Type]**, sélectionnez Microsoft Fabric.

   ![](assets/microsoft-config.png)

1. Configurez les paramètres d’authentification Microsoft Fabric :

   * **[!UICONTROL Serveur]** : saisissez l’URL du serveur Microsoft Fabric.

   * **[!UICONTROL ID de l’application]** : saisissez votre ID d’application Microsoft Fabric.

   * **[!UICONTROL Secret client]** : saisissez votre secret client.

   * **[!UICONTROL Options]** : le connecteur prend en charge les options présentées dans le tableau ci-dessous.

1. Cliquez sur **[!UICONTROL Adresses IP du serveur]** pour sélectionner les adresses IP du serveur à autoriser.

1. Sélectionnez l’option **[!UICONTROL Tester la connexion]** pour vérifier votre configuration.

1. Cliquez sur le bouton **[!UICONTROL Déployer les fonctions]** pour créer les fonctions.

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Ajouter]** pour créer votre base de données fédérée.

| Option | Description |
|---|---|
| Authentification | Type d’authentification pris en charge par le connecteur. Valeur actuelle prise en charge : ActiveDirectoryMSI. Pour plus d’informations, consultez la [documentation Microsoft SQL](https://learn.microsoft.com/fr-fr/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"} (exemple n° 8 de chaînes de connexion). |

