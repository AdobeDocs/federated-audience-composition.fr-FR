---
title: Se connecter à la composition d’audiences fédérées à l’aide d’une connexion privée
description: Découvrez comment configurer la composition d’audience fédérée et vous y connecter à l’aide d’une connexion privée. Cela inclut PrivateLink ou un VPN de site à site.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Connectivité privée à la composition d’audiences fédérées

La composition d’audiences fédérées prend en charge les connexions privées à plusieurs bases de données. Les connexions privées vous permettent de vous connecter à des entrepôts de données hébergés par le client sans traverser l’Internet public.

## Bases de données prises en charge {#supported-databases}

Les bases de données suivantes prennent en charge la connectivité privée à la composition d’audiences fédérées :

| Base de données | Cloud | Type de connexion privée |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée de l’interface VPC) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (point d’entrée privé) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée Managed VPC) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée de l’interface VPC) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | VPN de site à site |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | VPN de site à site |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | VPN de site à site |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | VPN de site à site |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Pour utiliser la connectivité privée avec [!DNL Snowflake], vous **devez** être au moins au niveau Business Critical ou supérieur sur [!DNL Snowflake]. Pour plus d’informations sur la connectivité privée avec [!DNL Snowflake], consultez le guide [connectivité privée) dans la documentation de Snowflake](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound).

L’utilisation de la connectivité privée avec [!DNL Snowflake] dépend du fournisseur de cloud sur lequel se trouve votre instance [!DNL Snowflake].

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Avant de poursuivre, vérifiez que vous obtenez votre identifiant de compte AWS auprès de l’assistance clientèle d’Adobe. Une fois que vous avez obtenu votre identifiant de compte AWS, contactez l’assistance [!DNL Snowflake] afin [!DNL Snowflake]’autoriser votre compte AWS à utiliser PrivateLink.

Une fois que votre compte AWS a été autorisé à être utilisé avec [!DNL Snowflake], vous devez obtenir des valeurs, y compris les `privatelink-vpce-id`, `privatelink-account-url` et `privatelink_ocsp-url`, afin de pouvoir obtenir le point d’entrée de l’interface VPC.

Vous pouvez obtenir ces valeurs en exécutant les commandes suivantes dans votre compte [!DNL Snowflake] en tant qu’ADMINISTRATEUR DE COMPTE :

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Une fois que vous avez exécuté ces commandes, vous pouvez envoyer la sortie SQL complète à l’assistance clientèle d’Adobe afin qu’Adobe puisse créer le point d’entrée de l’interface VPC pour vous.

Pour plus d’informations sur la création d’une connexion PrivateLink avec AWS, consultez le [guide d’AWS PrivateLink](https://docs.snowflake.com/en/user-guide/admin-security-privatelink).

Si vous souhaitez autoriser PrivateLink à utiliser avec un environnement d’évaluation interne, contactez l’assistance clientèle d’Adobe pour activer l’environnement.

Pour plus d’informations sur la création d’une connexion PrivateLink avec AWS pour les environnements d’évaluation internes, consultez le guide [Points d’entrée de l’interface VPC AWS pour les étapes internes ](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Pour Microsoft Azure, vous devez obtenir des valeurs, y compris les `privatelink-pls-id`, `privatelink-account-url` et `privatelink_ocsp-url`, pour créer le point d’entrée privé Azure.

Vous pouvez obtenir ces valeurs en exécutant les commandes suivantes dans votre compte Snowflake :

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Une fois que vous avez exécuté ces commandes, vous pouvez envoyer la sortie SQL complète à l’assistance clientèle d’Adobe afin qu’Adobe puisse créer pour vous le point d’entrée privé Azure.

Une fois qu’Adobe a créé le point d’entrée privé Azure, vous pouvez obtenir votre identifiant de ressource de point d’entrée privé. Maintenant que vous disposez de l’identifiant de ressource de point d’entrée privé, contactez l’assistance [!DNL Snowflake] pour autoriser votre compte [!DNL Snowflake], tout en fournissant l’identifiant de ressource.

Pour plus d’informations sur la création d’une connexion PrivateLink avec Azure, consultez le [guide d’Azure PrivateLink](https://docs.snowflake.com/en/user-guide/privatelink-azure).

Si vous souhaitez autoriser PrivateLink à utiliser avec un environnement d’évaluation interne, exécutez la commande suivante dans [!DNL Snowflake], tout en fournissant l’identifiant de ressource d’évaluation interne fourni par l’assistance clientèle d’Adobe :

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Pour plus d’informations sur la création d’une connexion PrivateLink avec Azure pour les environnements d’évaluation internes, consultez le guide [Points d’entrée privés Azure pour les étapes internes ](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Les clusters configurés et Redshift Serverless prennent en charge les connexions privées avec la composition d’audiences fédérées.

>[!IMPORTANT]
>
>Avant de commencer, contactez l’assistance clientèle d’Adobe pour recevoir votre identifiant de compte Amazon Web Services (AWS) et votre identifiant de cloud privé virtuel (VPC). Vous aurez besoin **des deux** ces valeurs pour obtenir un accès aux points d’entrée entre comptes. Pour plus d’informations sur l’octroi de l’accès à VPC, consultez le guide [octroi de l’accès à un VPC](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Une fois que vous disposez des identifiants AWS et VPC, accédez à la console de gestion AWS pour accorder un accès entre comptes à un point d’entrée VPC géré.

Pour un cluster configuré, notez les valeurs **Identifiant du cluster Redshift** et **Identifiant de compte AWS du propriétaire du cluster**. Pour un modèle Redshift sans serveur, notez les valeurs **nom du groupe de travail** et **ID du compte AWS propriétaire**.

Après avoir obtenu ces valeurs, partagez ces détails avec l’assistance clientèle d’Adobe afin qu’Adobe puisse créer le point d’entrée VPC géré. Adobe vous communiquera alors les informations de connexion suivantes : **URL du point d’entrée Redshift**, **URL JDBC Redshift** et **URL ODBC Redshift**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Pour utiliser la connectivité privée avec les briques de données, vous **devez** être sur un plan d’entreprise sur les briques de données. Pour plus d’informations sur la connectivité privée avec les briques de données, consultez le guide [private link concepts guide](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

L’utilisation de la connectivité privée avec Databricks dépend du fournisseur de cloud sur lequel se trouve votre instance de Databricks.

### Amazon Web Services {#databricks-aws}

Avant la configuration d’avec Amazon Web Services, contactez l’assistance clientèle d’Adobe afin qu’elle puisse créer un point d’entrée front-end (entrant) de l’interface VPC pointant vers des briques de données. Ce point d’entrée couvre la connectivité ODBC de Federated Audience Composition à votre espace de travail des briques de données.

Une fois que vous avez obtenu votre identifiant de point d’entrée VPC et votre région AWS auprès de l’assistance clientèle Adobe, vous devez enregistrer votre point d’entrée VPC avec les informations fournies par Adobe.

Après avoir enregistré votre point d’entrée VPC, vous devez créer un objet Paramètres d’accès privé (PAS) . Lorsque vous créez le point d’entrée, définissez le niveau **Niveau d’accès privé** sur un niveau **Point d’entrée** et sélectionnez le point d’entrée VPC créé précédemment. Pour plus d’informations sur la création de paramètres d’accès privé, consultez le guide [configurer un lien privé entrant](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Après avoir configuré vos paramètres d’accès privé, vous pouvez joindre le point d’entrée VPC à votre espace de travail. Pour plus d’informations sur la création de votre espace de travail avec PrivateLink, consultez le guide [configurer un lien privé entrant](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Maintenant que tous les paramètres ont été configurés, vous pouvez partager l’URL de votre espace de travail des briques de données avec l’assistance clientèle d’Adobe. Une fois que vous avez partagé l’URL de l’espace de travail Blocs de données, Adobe peut configurer les paramètres DNS requis pour acheminer les requêtes vers le point d’entrée de l’espace de travail.

### Microsoft Azure {#databricks-azure}

Un VPN de site à site est utilisé pour se connecter en toute sécurité d’Adobe à l’espace de travail Databricks sur Azure. Vous devez configurer une passerelle VPN Azure pour établir le tunnel VPN afin de transmettre vos données en toute sécurité à Adobe.

Une fois que vous avez configuré votre passerelle VPN Azure et votre point d’entrée privé Databricks, partagez les détails suivants avec votre représentant de l’assistance clientèle Adobe : **Passerelle de réseau virtuel Azure**, **IP de point d’entrée privé Databricks**, **URL de Workspace Databricks** et **numéro de système autonome (ASN)**.

Avec ces détails, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les adresses IP publiques et privées **VPN-Tunnel**, **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre passerelle VNet Azure. Pour plus d’informations, consultez le guide [connecter AWS et Azure à l’aide d’une passerelle VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Un VPN de site à site est utilisé pour se connecter en toute sécurité d’Adobe à l’espace de travail Databricks sur Google Cloud Platform. Vous devez configurer une passerelle VPN haute disponibilité Google Cloud Platform et un routeur cloud pour établir le tunnel VPN afin de transmettre vos données en toute sécurité à Adobe.

Une fois que vous avez configuré votre passerelle VPN HA GCP et votre routeur cloud, partagez les informations suivantes avec votre représentant de l’assistance clientèle Adobe : **passerelle VPN HA GCP**, **URL Workspace Databricks**, **IP Private Service Connect (PSC)** et le **numéro de système autonome (ASN)**.

Avec ces détails, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les adresses IP publiques et privées **VPN-Tunnel**, **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre compte Google Cloud Platform. Pour plus d&#39;informations, consultez le guide [Créer des connexions VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Pour vous connecter à Azure Synapse Analytics, vous devez d’abord créer une passerelle de réseau virtuel Azure et un point d’entrée privé Synapse. La passerelle de réseau virtuel Azure vous permet d&#39;envoyer du trafic chiffré entre un réseau virtuel Azure à Synapse, tandis que le point d&#39;entrée privé Synapse vous permet d&#39;avoir une connexion privée pour transmettre vos données en toute sécurité.

Une fois que vous avez configuré votre passerelle de réseau virtuel Azure et votre point d’entrée privé Synapse, partagez les informations suivantes avec votre représentant de l’assistance clientèle Adobe : **Passerelle de réseau virtuel Azure**, **adresse IP du point d’entrée privé Synapse**, **URL de Workspace Synapse** et **numéro de service autonome (ASN)**.

Avec ces détails, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les **paires VPN-tunnel**, **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre passerelle VNet Azure. Pour plus d’informations, consultez le guide [connecter AWS et Azure à l’aide d’une passerelle VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google BigQuery {#gbq}

Pour vous connecter à Google BigQuery, vous devez d&#39;abord créer une passerelle VPN haute disponibilité Google Cloud Platform et un routeur cloud.

Une fois que vous avez configuré votre passerelle VPN HA GCP et votre routeur cloud, partagez les informations suivantes avec votre représentant de l’assistance clientèle Adobe : **passerelle VPN HA GCP**, **adresse IP Private Service Connect (PSC)** et le **numéro de système autonome (ASN)**.

Avec ces détails, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les adresses IP publiques et privées **VPN-Tunnel**, **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre compte Google Cloud Platform. Pour plus d&#39;informations, consultez le guide [Créer des connexions VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
