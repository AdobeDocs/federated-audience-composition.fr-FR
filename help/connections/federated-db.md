---
audience: end-user
title: Commencer avec les bases de données fédérées
description: Découvrez comment créer et gérer vos bases de données fédérées
source-git-commit: 847da9a5eeb28199010f8491f7eebba4a60a83f1
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 87%

---

# Commencer avec les bases de données fédérées {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Bases de données fédérées"
>abstract="Les connexions existantes à des bases de données fédérées sont répertoriées dans cet écran. Pour créer une connexion, cliquez sur le bouton **Ajouter une base de données fédérée**."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Propriétés de la base de données fédérée"
>abstract="Saisissez le nom de la nouvelle base de données fédérée et sélectionnez son type."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Détails de la base de données fédérée"
>abstract="Renseignez les paramètres de connexion à la nouvelle base de données fédérée. Utilisez le bouton **Tester la connexion** pour valider votre configuration."

Créer, configurer, tester et enregistrer la connexion à une base de données externe.

Bases de données externes prises en charge :

* Snowflake
* Google BigQuery
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL Serveur]**:

* **[!UICONTROL Utilisateur]**: nom de l’utilisateur.

* **[!UICONTROL Mot de passe]** : mot de passe du compte d’utilisateur.

* **[!UICONTROL Base]**:

* **[!UICONTROL Schéma de travail]**:

* **[!UICONTROL Clé privée]**: seuls les fichiers .pem sont acceptés

* **[!UICONTROL Options]**: le connecteur prend en charge les options présentées dans le tableau ci-dessous.

| Option | Description |
|---|---|
| workschema | Schéma de base de données à utiliser pour les tables de travail. |
| warehouse | Nom de l&#39;entrepôt par défaut à utiliser. Il remplace la valeur par défaut de l&#39;utilisateur. |
| TimeZoneName | Vide par défaut. C&#39;est le fuseau horaire système du serveur applicatif Campaign Classic qui est utilisé. Il est possible d&#39;utiliser cette option pour forcer le paramètre de session TIMEZONE. <br>Pour plus d&#39;informations à ce sujet, consultez [cette page](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | Paramètre de session WEEK_START. Par défaut, cette valeur est définie sur 0. <br>Pour plus d&#39;informations à ce sujet, consultez [cette page](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start). |
| UseCachedResult | Paramètre de session USE_CACHED_RESULTS. Par défaut, cette valeur est définie sur TRUE. Cette option peut être utilisée pour désactiver les résultats mis en cache du Snowflake. <br>Pour plus d’informations à ce sujet, consultez [cette page](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Nombre de threads à utiliser pour le chargeur en masse de Snowflake ; plus de threads signifient de meilleures performances pour les chargements en masse plus volumineux. Par défaut, cette valeur est définie sur 1. Le nombre peut être ajusté en fonction du nombre de threads de la machine. |
| chunkSize | Détermine la taille de fichier du bloc de chargeur en masse. Par défaut, cette valeur est définie sur 128 Mo. Peut être modifiée pour des performances plus optimales, lorsqu’elle est utilisée avec bulkThreads. Plus de threads actifs simultanément signifie de meilleures performances. <br>Pour plus d’informations à ce propos, consultez la [documentation Snowflake](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| StageName | Nom de l’étape interne préconfigurée. Elle sera utilisée en chargement massif au lieu de créer une nouvelle étape temporaire. |

## Google BigQuery {#google-big-query}

* **[!UICONTROL Compte Service]** : adresse e-mail de votre **[!UICONTROL compte Service]**. Pour plus d&#39;informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL Projet]** : nom de votre **[!UICONTROL projet]**. Pour plus d&#39;informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL Jeu de données]** : nom de votre **[!UICONTROL jeu de données]**. Pour plus d&#39;informations à ce propos, consultez la [documentation Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL Chemin du fichier clé]**: téléchargez votre fichier de clé sur le serveur. Seuls les fichiers .json sont acceptés.

* **[!UICONTROL Options]**: le connecteur prend en charge les options présentées dans le tableau ci-dessous.

| Option | Description |
|:-:|:-:|
| ProxyType | Type de proxy utilisé pour se connecter à BigQuery par le biais des connecteurs ODBC et SDK. </br>HTTP (par défaut), http_no_tunnel, socks4 et socks5 sont actuellement pris en charge. |
| ProxyHost | Nom d’hôte ou adresse IP où le proxy peut être atteint. |
| ProxyPort | Numéro de port sur lequel le proxy s’exécute, par exemple 8080 |
| ProxyUid | Nom d’utilisateur utilisé pour le proxy authentifié |
| ProxyPwd | Mot de passe ProxyUid |
| bqpath | Notez que cela s’applique uniquement à l’outil de chargement en masse (SDK Cloud). </br> Pour éviter d’utiliser la variable PATH ou si le répertoire google-cloud-sdk doit être déplacé vers un autre emplacement, vous pouvez spécifier avec cette option le chemin exact du répertoire bin du sdk cloud sur le serveur. |
| GCloudConfigName | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> Le SDK Google Cloud utilise des configurations pour charger les données dans les tableaux BigQuery. La configuration nommée `accfda` stocke les paramètres pour le chargement des données. Cependant, cette option permet aux personnes de spécifier un nom différent pour la configuration. |
| GCloudDefaultConfigName | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> La configuration active du SDK Google Cloud ne peut pas être supprimée sans transférer au préalable la balise active vers une nouvelle configuration. Cette configuration temporaire est nécessaire pour recréer la configuration principale de chargement des données. Le nom par défaut de la configuration temporaire est `default`, et peut être modifié si nécessaire. |
| GCloudRecreateConfig | Notez que cela s’applique uniquement à partir de la version 7.3.4 et à l’outil de chargement en masse (SDK Cloud).</br> Lorsqu’il est défini sur `false`, le mécanisme de chargement en masse évite de tenter de recréer, de supprimer ou de modifier les configurations du SDK Google Cloud. Au lieu de cela, il procède au chargement des données à l’aide de la configuration existante sur la machine. Cette fonctionnalité est utile lorsque d’autres opérations dépendent des configurations du SDK Google Cloud. </br> Si la personne active cette option de moteur sans une configuration appropriée, le mécanisme de chargement en masse émet un message d’avertissement : `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Pour éviter d’autres erreurs, le mécanisme de chargement en masse par défaut du tableau ODBC est rétabli. |

## Azure synapse Redshift {#azure-synapse-redshift}

* **[!UICONTROL Serveur]** : URL du serveur Azure Synapse

* **[!UICONTROL Compte]** : nom de l&#39;utilisateur

* **[!UICONTROL Mot de passe]** : mot de passe du compte d’utilisateur

* **[!UICONTROL Base de données]** : nom de la base de données

* **[!UICONTROL Options]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL Serveur]** : URL du serveur [!DNL Vertica Analytics]

* **[!UICONTROL Compte]** : nom de l&#39;utilisateur

* **[!UICONTROL Mot de passe]** : mot de passe du compte d’utilisateur

* **[!UICONTROL Base de données]** : nom de la base de données

* **[!UICONTROL Schéma de travail]**: nom de votre schéma de travail.

* **[!UICONTROL Options]**: le connecteur prend en charge les options présentées dans le tableau ci-dessous.

Le connecteur prend en charge les options suivantes :

| Option | Description |
|---|---|
| TimeZoneName | Vide par défaut. C&#39;est le fuseau horaire système du serveur applicatif Campaign Classic qui est utilisé. Il est possible d’utiliser cette option pour forcer le paramètre de session TIMEZONE. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL Serveur]** : nom du DNS

* **[!UICONTROL Compte]** : nom de l’utilisateur

* **[!UICONTROL Mot de passe]** : mot de passe du compte d’utilisateur

* **[!UICONTROL Base de données]** : nom de la base de données s’il n’est pas spécifié dans le DSN. Il peut rester vide s’il est spécifié dans le DSN

* **[!UICONTROL Schéma de travail]** : nom de votre schéma de travail. [En savoir plus](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

