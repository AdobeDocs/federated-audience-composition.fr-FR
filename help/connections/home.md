---
audience: end-user
title: Créer et gérer des connexions avec des bases de données fédérées
description: Découvrir comment créer et gérer des connexions avec des bases de données fédérées
exl-id: ab65cd8a-dfa0-4f09-8e9b-5730564050a1
source-git-commit: f0a66632e90526c450e45430d4bdf8a73f2bad49
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 96%

---

# Créer des connexions {#connections-fdb}

>[!AVAILABILITY]
>
>Pour accéder aux connexions, vous devez disposer de l’une des autorisations suivantes :
>
>-**Gestion de la base de données fédérées**
>>-**Affichage de la base de données fédérées**
>
>Pour plus d’informations sur les autorisations requises, lisez le [guide du contrôle d’accès](/help/governance-privacy-security/access-control.md).

La composition d’audiences fédérées Experience Platform permet de créer et d’enrichir des audiences à partir d’entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform.

## Bases de données prises en charge {#supported-databases}

Pour travailler avec votre base de données fédérée et Adobe Experience Platform, vous devez d’abord établir une connexion entre les deux sources. Avec la composition d’audiences fédérées, vous pouvez vous connecter aux bases de données suivantes.

* Amazon Redshift
* Azure Synapse Analytics
* Databricks
* Google BigQuery
* Microsoft Fabric
* Oracle
* Snowflake
* Vertica Analytics

## Créer une connexion {#create}

Pour créer une connexion, sélectionnez **[!UICONTROL Bases de données fédérées]** dans la section Données fédérées.

![Le bouton Bases de données fédérées est mis en surbrillance dans le volet de navigation de gauche.](assets/home/select-federated.png){zoomable="yes" width="70%" align="center"}

La section Bases de données fédérées s’affiche. Sélectionnez **[!UICONTROL Ajouter une base de données fédérée]** pour créer une connexion.

![Le bouton Ajouter une base de données fédérée est mis en surbrillance dans la page d’affichage de la base de données fédérée.](assets/home/add-federated.png){zoomable="yes" width="70%" align="center"}

La fenêtre contextuelle Propriétés de connexion s’affiche. Vous pouvez nommer votre connexion ainsi que sélectionner le type de base de données à créer.

![Les types de bases de données fédérées s’affichent.](assets/home/select-type.png){zoomable="yes" width="70%" align="center"}

Après avoir sélectionné un type, la section **[!UICONTROL Détails]** s’affiche. Cette section diffère en fonction du type de base de données précédemment choisi.

>[!BEGINTABS]

>[!TAB Amazon Redshift]

>[!AVAILABILITY]
>
>Seuls Amazon Redshift AWS, Amazon Redshift Spectrum et Amazon Redshift sans serveur sont pris en charge.

Après avoir sélectionné Amazon Redshift, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | Nom de la source de données. |
| Compte | Nom d’utilisateur ou d’utilisatrice du compte. |
| Mot de passe | Mot de passe du compte. |
| Base de données | Nom de la base de données. Si ce champ est spécifié dans le nom du serveur, vous pouvez le laisser vide. |
| Schéma de travail | Nom du schéma de base de données à utiliser pour les tables de travail. Vous trouverez plus d’informations sur cette fonctionnalité dans la [documentation des schémas Amazon](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html){target="_blank"}.<br/><br/>**Note :** vous pouvez utiliser n’importe quel schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez des autorisation requises pour vous connecter à ce schéma. Cependant, vous **devez** utiliser des schémas de travail distincts lors de la connexion de plusieurs sandbox à la même base de données. |

>[!TAB Azure Synapse Analytics]

>[!NOTE]
>
>Si vous souhaitez créer une connexion sécurisée à l’aide d’Azure Synapse Analytics, contactez votre représentant ou représentante de l’assistance clientèle Adobe.

Après avoir sélectionné Azure Synapse Analytics, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | URL du serveur Azure Synapse. |
| Compte | Nom d’utilisateur ou d’utilisatrice du compte Azure Synapse. |
| Mot de passe | Mot de passe du compte Azure Synapse. |
| Base de données | Nom de la base de données. Si ce champ est spécifié dans le nom du serveur, vous pouvez le laisser vide. |
| Options | Options supplémentaires pour la connexion. Pour Azure Synapse Analytics, vous pouvez spécifier le type d’authentification pris en charge par le connecteur. Actuellement, la composition d’audiences fédérées prend en charge `ActiveDirectoryMSI`. Pour plus d’informations sur les chaînes de connexion, consultez la section [Exemple de chaîne de connexion de la documentation Microsoft](https://learn.microsoft.com/fr-fr/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings){target="_blank"}. |

>[!TAB Databricks]

>[!NOTE]
>
>L’accès sécurisé à votre entrepôt de données Databricks externe par le biais d’un lien privé est pris en charge. Cela inclut des connexions sécurisées aux bases de données Databricks hébergées sur Amazon Web Services (AWS) via un lien privé et aux bases de données Databricks hébergées sur Microsoft Azure via un VPN. Contactez votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé.

Après avoir sélectionné Databricks, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | Nom du serveur Databricks. |
| Chemin HTTP | Chemin d’accès à votre cluster ou entrepôt de données. Pour plus d’informations sur le chemin d’accès, consultez la [documentation de Databricks sur les détails de connexion](https://docs.databricks.com/aws/en/integrations/compute-details){target="_blank"}. |
| Mot de passe | Jeton d’accès du serveur Databricks. Pour plus d’informations sur cette valeur, consultez la [documentation de Databricks sur les jetons d’accès personnel](https://docs.databricks.com/aws/en/dev-tools/auth/pat){target="_blank"}. |
| Catalogue | Nom du catalogue Databricks. Pour plus d’informations sur les catalogues dans Databricks, consultez la [documentation de Databricks sur les catalogues](https://docs.databricks.com/aws/en/catalogs/){target="_blank"}. |
| Schéma de travail | Nom du schéma de base de données à utiliser pour les tables de travail. <br/><br/>**Note :** vous pouvez utiliser **n’importe quel** schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez des autorisation requises pour vous connecter à ce schéma. Cependant, vous **devez** utiliser des schémas de travail distincts lors de la connexion de plusieurs sandbox à la même base de données. |
| Options | Options supplémentaires pour la connexion. Les options disponibles sont répertoriées dans le tableau suivant. |

Pour Databricks, vous pouvez définir les options supplémentaires suivantes :

| Options | Description |
| ------- | ----------- |
| TimeZoneName | Nom du fuseau horaire à utiliser. Cette valeur représente le paramètre de session `TIMEZONE`. Pour plus d’informations sur les fuseaux horaires, consultez la [documentation de Databricks sur les fuseaux horaires](https://docs.databricks.com/aws/en/sql/language-manual/parameters/timezone#:~:text=The%20system%20default%20is%20UTC%20.){target="_blank"}. |

>[!TAB Google BigQuery]

Après avoir sélectionné Google BigQuery, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Compte de service | Adresse e-mail de votre compte de service. Pour plus d’informations, consultez la [documentation sur le compte de service Google Cloud](https://cloud.google.com/iam/docs/service-accounts-create){target="_blank"}. |
| Projet | ID de votre projet. Pour plus d’informations, consultez la [documentation sur le compte de service Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects){target="_blank"}. |
| Jeu de données | Nom du jeu de données. Pour plus d’informations, consultez la [documentation sur le jeu de données Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro){target="_blank"}. |
| Chemin d’accès au fichier de clé | Fichier de clé pour le serveur. Seuls les fichiers `json` sont pris en charge. |
| Options | Options supplémentaires pour la connexion. Les options disponibles sont répertoriées dans le tableau suivant. |

Pour Google BigQuery, vous pouvez définir les options supplémentaires suivantes :

| Options | Description |
| ------- | ----------- |
| ProxyType | Type de proxy utilisé pour la connexion à BigQuery. Les valeurs acceptées comprennent `HTTP`, `http_no_tunnel`, `socks4` et `socks5`. |
| ProxyHost | Nom d’hôte ou adresse IP où le proxy peut être atteint. |
| ProxyUid | Numéro de port sur lequel le proxy s’exécute. |
| ProxyPwd | Mot de passe du proxy. |
| bgpath | **Note :** cela s’applique uniquement à l’**outil de chargement en masse** (SDK Cloud). <br/><br/> Chemin d’accès au répertoire bin du SDK Cloud sur le serveur. Vous ne devez le définir que si vous avez déplacé le répertoire `google-cloud-sdk` vers un autre emplacement ou si vous souhaitez éviter d’utiliser la variable PATH. |
| GCloudConfigName | **Note :** cela s’applique uniquement à l’**outil de chargement en masse** (SDK Cloud) au-dessus de la version 7.3.4. <br/><br/> Nom de la configuration qui stocke les paramètres pour charger les données. Par défaut, la valeur est `accfda`. |
| GCloudDefaultConfigName | **Note :** cela s’applique uniquement à l’**outil de chargement en masse** (SDK Cloud) au-dessus de la version 7.3.4. <br/><br/> Nom de la configuration temporaire pour recréer la configuration principale pour le chargement des données. Par défaut, la valeur est `default`. |
| GCloudRecreateConfig | **Note :** cela s’applique uniquement à l’**outil de chargement en masse** (SDK Cloud) au-dessus de la version 7.3.4. <br/><br/> Valeur booléenne qui vous permet de décider si le mécanisme de chargement en masse doit recréer, supprimer ou modifier automatiquement les configurations du SDK Google Cloud. Si cette valeur est définie sur `false`, le mécanisme de chargement en masse charge les données à l’aide d’une configuration existante sur la machine. Si cette valeur est définie sur `true`, assurez-vous que votre configuration est correctement définie. Dans le cas contraire, l’erreur `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option` s’affiche et le mécanisme de chargement revient au mécanisme de chargement par défaut. |

>[!TAB Microsoft Fabric]

Après avoir sélectionné Microsoft Fabric, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | URL du serveur Microsoft Fabric. |
| ID de l’application | ID de l’application pour Microsoft Fabric. Pour plus d’informations sur l’ID de l’application, consultez la [documentation de Microsoft Fabric sur la configuration de l’application](https://learn.microsoft.com/fr-fr/fabric/workload-development-kit/create-entra-id-app){target="_blank"}. |
| Secret client | Secret client de l’application. Pour plus d’informations sur le secret client, consultez la [documentation de Microsoft Fabric sur la configuration de l’application](https://learn.microsoft.com/fr-fr/fabric/workload-development-kit/create-entra-id-app#step-8-generate-a-secret-for-your-application){target="_blank"}. |
| Options | Options supplémentaires pour la connexion. Les options disponibles sont répertoriées dans le tableau suivant. |

Pour Microsoft Fabric, vous pouvez définir les options supplémentaires suivantes :

| Option | Description |
| ------ | ----------- |
| Authentification | Type d’authentification utilisé par le connecteur. Les valeurs prises en charge comprennent : `ActiveDirectoryMSI`. Pour plus d’informations, consultez la [documentation de Microsoft sur la connectivité de l’entrepôt de données](https://learn.microsoft.com/fr-fr/fabric/data-warehouse/connectivity){target="_blank"}. |

>[!TAB Oracle]

>[!IMPORTANT]
>
>La composition de l’audience fédérée prend en charge la configuration des connexions fédérées avec la base de données Oracle version 11g ou ultérieure et hébergée sur AWS, Azure, Exadata ou un cloud privé (à condition qu’elle soit accessible par un réseau externe). Si vous avez d’autres questions relatives à la configuration de la base de données Oracle ou si vous devez créer une connexion sécurisée à Oracle, contactez votre représentant de l’assistance clientèle d’Adobe.

Après avoir sélectionné Oracle, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | URL du serveur Oracle. |
| Compte | Nom d’utilisateur ou d’utilisatrice du compte. |
| Mot de passe | Mot de passe du compte. |

>[!TAB Snowflake]

>[!NOTE]
>
>L’accès sécurisé à votre entrepôt de données Snowflake externe par le biais d’un lien privé est pris en charge. Notez que votre compte Snowflake doit être hébergé sur Amazon Web Services (AWS) ou Azure et être situé dans la même région que votre environnement de composition d’audiences fédérées. Veuillez contacter votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé à votre compte Snowflake.

Après avoir sélectionné Snowflake, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | Nom du serveur. |
| Utilisateur ou utilisatrice | Nom d’utilisateur ou d’utilisatrice du compte. |
| Mot de passe | Mot de passe du compte. |
| Base de données | Nom de la base de données. Si ce champ est spécifié dans le nom du serveur, vous pouvez le laisser vide. |
| Schéma de travail | Nom du schéma de base de données à utiliser pour les tables de travail. <br/><br/>**Note :** vous pouvez utiliser **n’importe quel** schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez des autorisation requises pour vous connecter à ce schéma. Cependant, vous **devez** utiliser des schémas de travail distincts lors de la connexion de plusieurs sandbox à la même base de données. |
| Clé privée | Clé privée de la connexion à la base de données. Vous pouvez charger un fichier `.pem` à partir de votre système local. |
| Options | Options supplémentaires pour la connexion. Les options disponibles sont répertoriées dans le tableau suivant. |

Pour Snowflake, vous pouvez définir les options supplémentaires suivantes :

| Options | Description |
| ------- | ----------- |
| workschema | Nom du schéma de base de données à utiliser pour les tables de travail. |
| TimeZoneName | Nom du fuseau horaire à utiliser. Cette valeur représente le paramètre de session `TIMEZONE`. Le fuseau horaire du système est utilisé par défaut. Pour plus d’informations sur les fuseaux horaires, consultez la [documentation de Snowflake sur les fuseaux horaires](https://docs.snowflake.com/fr/sql-reference/parameters#timezone){target="_blank"}. |
| WeekStart | Jour auquel vous voulez que la semaine commence. Cette valeur représente le paramètre de session `WEEK_START`. Pour plus d’informations sur le début de la semaine, consultez la [documentation de Snowflake sur le paramètre de début de semaine](https://docs.snowflake.com/fr/sql-reference/parameters#week-start){target="_blank"}. |
| UseCachedResult | Valeur booléenne qui détermine si les résultats mis en cache de Snowflake seront utilisés. Cette valeur représente le paramètre de session `USE_CACHED_RESULTS`. Par défaut, cette valeur est définie sur true. Pour plus d’informations sur ce paramètre, consultez la [documentation de Snowflake sur les résultats persistants](https://docs.snowflake.com/fr/user-guide/querying-persisted-results){target="_blank"}. |
| bulkThreads | Nombre de threads à utiliser pour le chargeur en masse de Snowflake. Plus il y a de threads ajoutés, meilleures seront les performances pour les chargements en masse plus volumineux. Par défaut, cette valeur est définie sur 1. |
| chunkSize | Taille de fichier du bloc de chaque chargeur en masse. Lors de l’utilisation avec d’autres threads, vous pouvez améliorer les performances de vos chargements en masse. Par défaut, cette valeur est définie sur 128 Mo. Pour plus d’informations sur les tailles des blocs, consultez la [documentation de Snowflake sur la préparation des fichiers de données](https://docs.snowflake.com/fr/user-guide/data-load-considerations-prepare){target="_blank"}. |
| StageName | Nom d’un environnement d’évaluation interne préconfiguré. Il peut être utilisé dans les chargements en masse au lieu de créer une nouvelle étape temporaire. |

>[!TAB Vertica Analytics]

Après avoir sélectionné Vertica Analytics, vous pouvez ajouter les détails suivants :

| Champ | Description |
| ----- | ----------- |
| Serveur | URL du serveur Vertica Analytics. |
| Compte | Nom d’utilisateur ou d’utilisatrice du compte. |
| Mot de passe | Mot de passe du compte. |
| Base de données | Nom de la base de données. Si ce champ est spécifié dans le nom du serveur, vous pouvez le laisser vide. |
| Schéma de travail | Nom du schéma de base de données à utiliser pour les tables de travail. <br/><br/>**Note :** vous pouvez utiliser **n’importe quel** schéma de la base de données, y compris les schémas utilisés pour le traitement temporaire des données, à condition que vous disposiez des autorisation requises pour vous connecter à ce schéma. Cependant, vous **devez** utiliser des schémas de travail distincts lors de la connexion de plusieurs sandbox à la même base de données. |
| Options | Options supplémentaires pour la connexion. Les options disponibles sont répertoriées dans le tableau suivant. |

Pour Vertica Analytics, vous pouvez définir les options supplémentaires suivantes :

| Options | Description |
| ------- | ----------- |
| TimeZoneName | Nom du fuseau horaire à utiliser. Cette valeur représente le paramètre de session `TIMEZONE`. Pour plus d’informations sur les fuseaux horaires, consultez la [documentation de Vertica Analytics sur les fuseaux horaires](https://docs.vertica.com/24.1.x/en/admin/configuring-db/config-procedure/using-time-zones-with/){target="_blank"}. |

>[!ENDTABS]

Après avoir ajouté les détails de la connexion, notez les paramètres supplémentaires suivants :

>[!NOTE]
>
>Pour utiliser la composition d’audiences fédérées pour une base de données, vous devez ajouter à la liste autorisée **toutes** les adresses IP associées à cette base de données.

| Paramètres | Détails |
| -------- | ------- |
| Activer la connexion | Bouton (bascule) booléen qui détermine si la connexion sera automatiquement activée. |
| Adresses IP du serveur | Fenêtre contextuelle qui affiche les adresses IP à placer sur la liste autorisée pour se connecter à la base de données. |
| Connexion de test | Permet de vérifier les détails de votre configuration. |

Vous pouvez maintenant sélectionner **[!UICONTROL Déployer les fonctions]**, puis **[!UICONTROL Ajouter]** pour finaliser la connexion entre la base de données fédérée et Experience Platform.
