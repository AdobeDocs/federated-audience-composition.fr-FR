---
title: Se connecter à la composition d’audiences fédérées à l’aide d’une connexion privée
description: Découvrez comment configurer la composition d’audiences fédérées et vous y connecter à l’aide d’une connexion privée. Cela inclut PrivateLink ou un VPN de site à site.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: ht
source-wordcount: '1634'
ht-degree: 100%

---


# Connectivité privée à la composition d’audiences fédérées

La composition d’audiences fédérées prend en charge les connexions privées à plusieurs bases de données. Les connexions privées vous permettent de vous connecter à des entrepôts de données hébergés par le client sans passer par l’internet public.

## Bases de données prises en charge {#supported-databases}

Les bases de données suivantes prennent en charge la connectivité privée à la composition d’audiences fédérées :

| Base de données | Cloud | Type de connexion privée |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée d’interface VPC) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (point d’entrée privé) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée VPC géré) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (point d’entrée d’interface VPC) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | VPN de site à site |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | VPN de site à site |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | VPN de site à site |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | VPN de site à site |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Pour utiliser la connectivité privée avec [!DNL Snowflake], vous **devez** être au moins au niveau Business Critical ou supérieur sur [!DNL Snowflake]. Pour plus d’informations sur la connectivité privée avec [!DNL Snowflake], consultez le [guide de connectivité privée dans la documentation de Snowflake](https://docs.snowflake.com/fr/user-guide/private-connectivity-inbound).

L’utilisation de la connectivité privée avec [!DNL Snowflake] dépend du fournisseur de cloud sur lequel se trouve votre instance [!DNL Snowflake].

### Amazon Web Services (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Avant de poursuivre, assurez-vous d’avoir obtenu votre identifiant de compte AWS auprès de l’assistance clientèle Adobe. Une fois que vous avez obtenu votre identifiant de compte AWS, contactez l’assistance [!DNL Snowflake] afin que [!DNL Snowflake] puisse autoriser votre compte AWS à utiliser PrivateLink.

Une fois que votre compte AWS a été autorisé à être utilisé avec [!DNL Snowflake], vous devez obtenir des valeurs, y compris les `privatelink-vpce-id`, `privatelink-account-url` et `privatelink_ocsp-url`, afin de pouvoir obtenir le point d’entrée de l’interface VPC.

Vous pouvez obtenir ces valeurs en exécutant les commandes suivantes dans votre compte [!DNL Snowflake] en tant qu’ACCOUNTADMIN :

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Une fois que vous avez exécuté ces commandes, vous pouvez envoyer la sortie SQL complète à l’assistance clientèle d’Adobe afin qu’Adobe puisse créer le point d’entrée d’interface VPC pour vous.

Pour plus d’informations sur la création d’une connexion PrivateLink avec AWS, consultez le [guide AWS PrivateLink](https://docs.snowflake.com/fr/user-guide/admin-security-privatelink).

Si vous souhaitez autoriser l’utilisation de PrivateLink avec un environnement de préproduction interne, contactez l’assistance clientèle Adobe pour activer l’environnement.

Pour obtenir des informations plus détaillées sur la création d’une connexion PrivateLink avec AWS pour les environnements de préproduction internes, consultez le [guide des points d’entrée d’interface VPC AWS pour les environnements de préproduction internes](https://docs.snowflake.com/fr/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Pour Microsoft Azure, vous devez obtenir des valeurs, y compris les `privatelink-pls-id`, `privatelink-account-url` et `privatelink_ocsp-url`, pour créer le point d’entrée privé Azure.

Vous pouvez obtenir ces valeurs en exécutant les commandes suivantes dans votre compte Snowflake :

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Une fois que vous avez exécuté ces commandes, vous pouvez envoyer la sortie SQL complète à l’assistance clientèle d’Adobe afin qu’Adobe puisse créer pour vous le point d’entrée privé Azure.

Une fois qu’Adobe a créé le point d’entrée privé Azure, vous pouvez obtenir votre identifiant de ressource de point d’entrée privé. Maintenant que vous disposez de l’identifiant de ressource de point d’entrée privé, contactez l’assistance [!DNL Snowflake] pour autoriser votre compte [!DNL Snowflake], tout en fournissant l’identifiant de ressource.

Pour plus d’informations sur la création d’une connexion PrivateLink avec Azure, consultez le [guide d’Azure PrivateLink](https://docs.snowflake.com/fr/user-guide/privatelink-azure).

Si vous souhaitez autoriser l’utilisation de PrivateLink avec un environnement de préproduction interne, exécutez la commande suivante dans [!DNL Snowflake], tout en fournissant l’identifiant de ressource de préproduction interne fourni par l’assistance clientèle d’Adobe :

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Pour plus d’informations sur la création d’une connexion PrivateLink avec Azure pour les environnements de préproduction internes, consultez le [guide des points d’entrée privés Azure pour les environnements de préproduction internes](https://docs.snowflake.com/fr/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Les clusters provisionnés et Redshift Serverless prennent en charge les connexions privées avec la composition d’audiences fédérées.

>[!IMPORTANT]
>
>Avant de commencer, contactez l’assistance clientèle d’Adobe pour recevoir votre identifiant de compte Amazon Web Services (AWS) et votre identifiant de cloud privé virtuel (VPC). Vous aurez besoin de ces **deux** valeurs pour obtenir un accès aux points d’entrée entre comptes. Pour plus d’informations sur l’octroi de l’accès au VPC, consultez le [guide d’octroi de l’accès à un VPC](https://docs.aws.amazon.com/fr_fr/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Une fois que vous disposez des identifiants AWS et VPC, accédez à la console de gestion AWS pour accorder un accès entre comptes à un point d’entrée VPC géré.

Pour un cluster configuré, notez les valeurs **Identifiant du cluster Redshift** et **Identifiant de compte AWS du propriétaire du cluster**. Pour un Redshift Serverless, notez les valeurs **nom du groupe de travail** et **ID du compte AWS propriétaire**.

Après avoir obtenu ces valeurs, partagez ces détails avec l’assistance clientèle d’Adobe afin qu’Adobe puisse créer le point d’entrée VPC géré. Adobe vous communiquera alors les informations de connexion suivantes : **URL du point d’entrée Redshift**, **URL JDBC Redshift** et **URL ODBC Redshift**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Pour utiliser la connectivité privée avec Databricks, vous **devez** disposer d’un plan Enterprise sur Databricks. Pour plus d’informations sur la connectivité privée avec Databricks, consultez le [guide sur les concepts de liaison privée](https://docs.databricks.com/aws/fr/security/network/concepts/privatelink-concepts).

L’utilisation de la connectivité privée avec Databricks dépend du fournisseur de cloud sur lequel se trouve votre instance de Databricks.

### Amazon Web Services {#databricks-aws}

Avant de configurer avec Amazon Web Services, contactez l’assistance clientèle d’Adobe afin qu’elle puisse créer un point d’entrée d’interface VPC frontal (entrant) qui pointe vers Databricks. Ce point d’entrée couvre la connectivité ODBC de la composition d’audiences fédérées à votre espace de travail Databricks.

Une fois que vous avez obtenu votre identifiant de point d’entrée VPC et votre région AWS auprès de l’assistance clientèle Adobe, vous devez enregistrer votre point d’entrée VPC avec les informations fournies par Adobe.

Après avoir enregistré votre point d’entrée VPC, vous devez créer un objet Paramètres d’accès privé (PAS). Lorsque vous créez le point d’entrée, définissez **Niveau d’accès privé** sur un niveau **Point d’entrée** et sélectionnez le point d’entrée VPC créé précédemment. Pour plus d’informations sur la création de paramètres d’accès privé, consultez le [guide de configuration de PrivateLink entrant](https://docs.databricks.com/aws/fr/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Après avoir configuré vos paramètres d’accès privé, vous pouvez associer le point d’entrée VPC à votre espace de travail. Pour plus d’informations sur la création de votre espace de travail avec PrivateLink, consultez le [guide de configuration de PrivateLink entrant](https://docs.databricks.com/aws/fr/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Maintenant que tous les paramètres ont été configurés, vous pouvez partager l’URL de votre espace de travail Databricks avec l’assistance clientèle d’Adobe. Une fois que vous avez partagé l’URL de l’espace de travail Databricks, Adobe peut configurer les paramètres DNS requis pour acheminer les requêtes vers le point d’entrée de l’espace de travail.

### Microsoft Azure {#databricks-azure}

Un VPN de site à site est utilisé pour se connecter en toute sécurité d’Adobe à l’espace de travail Databricks sur Azure. Vous devez configurer une passerelle VPN Azure pour établir le tunnel VPN afin de transmettre vos données en toute sécurité à Adobe.

Une fois que vous avez configuré votre passerelle VPN Azure et votre point d’entrée privé Databricks, partagez les détails suivants avec votre représentant ou représentante de l’assistance clientèle Adobe : **passerelle de réseau virtuel Azure**, **IP de point d’entrée privé Databricks**, **URL d’espace de travail Databricks** et **numéro de système autonome (ASN)**.

Grâce à ces informations, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les **adresses IP publiques et privées du tunnel VPN**, les **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre passerelle VNet Azure. Pour plus d’informations, consultez le [guide de connexion d’AWS et Azure à l’aide d’une passerelle VPN](https://learn.microsoft.com/fr-fr/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Un VPN de site à site est utilisé pour se connecter en toute sécurité d’Adobe à l’espace de travail Databricks sur Google Cloud Platform. Vous devez configurer une passerelle VPN Google Cloud Platform à haute disponibilité et un routeur cloud pour établir le tunnel VPN afin de transmettre vos données en toute sécurité à Adobe.

Une fois que vous avez configuré votre passerelle VPN HA GCP et votre routeur cloud, partagez les informations suivantes avec votre représentant ou représentante de l’assistance clientèle Adobe : **passerelle VPN HA GCP**, **URL d’espace de travail Databricks**, **adresse IP Private Service Connect (PSC)** et le **numéro de système autonome (ASN)**.

Grâce à ces informations, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les **adresses IP publiques et privées VPN-Tunnel**, **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre compte Google Cloud Platform. Pour plus d’informations, consultez le [guide de création de connexions HA VPN](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Pour vous connecter à Azure Synapse Analytics, vous devez d’abord créer une passerelle de réseau virtuel Azure et un point d’entrée privé Synapse. La passerelle de réseau virtuel Azure vous permet d’envoyer du trafic chiffré entre un réseau virtuel Azure et Synapse, tandis que le point d’entrée privé Synapse vous permet d’avoir une connexion privée pour transmettre vos données en toute sécurité.

Une fois que vous avez configuré votre passerelle de réseau virtuel Azure et votre point d’entrée privé Synapse, partagez les informations suivantes avec votre représentant ou représentante de l’assistance clientèle Adobe : **passerelle de réseau virtuel Azure**, **adresse IP du point d’entrée privé Synapse**, **URL d’espace de travail Synapse** et **numéro de service autonome (ASN)**.

Grâce à ces informations, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les **paires VPN-tunnel**, les **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre passerelle VNet Azure. Pour plus d’informations, consultez le [guide de connexion AWS et Azure à l’aide d’une passerelle VPN](https://learn.microsoft.com/fr-fr/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google BigQuery {#gbq}

Pour vous connecter à Google BigQuery, vous devez d’abord créer une passerelle VPN haute disponibilité Google Cloud Platform et un routeur cloud.

Une fois que vous avez configuré votre passerelle VPN HA GCP et votre routeur cloud, partagez les informations suivantes avec votre représentant ou représentante de l’assistance clientèle Adobe : **passerelle VPN HA GCP**, **adresse IP Private Service Connect (PSC)** et le **numéro de système autonome (ASN)**.

Grâce à ces informations, Adobe peut établir les tunnels VPN requis pour votre connexion. Après avoir établi les tunnels VPN, Adobe fournit les **adresses IP publiques et privées du tunnel VPN**, les **clés prépartagées**, ainsi qu’un **numéro de système autonome**.

Vous pouvez désormais configurer vos tunnels VPN dans votre compte Google Cloud Platform. Pour plus d’informations, consultez le [guide de création de connexions VPN HA](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
