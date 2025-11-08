---
title: Nouveautés de la composition d’audiences fédérées Experience Platform
description: Dernières mises à jour et notes de mise à jour
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: aabe96fc223af5841c7b77ab914745d08d82ce49
workflow-type: tm+mt
source-wordcount: '1740'
ht-degree: 98%

---

# Notes de mise à jour {#rn-new}

[!DNL Federated Audience Composition] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées dans ces notes de mise à jour. [!DNL Federated Audience Composition] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version du 25 octobre {#fac-25-10}

### Nouvelles fonctionnalités {#fac-25-10-feature}

<!-- 
<table>
<thead>
<tr>
<th><strong>Availability for Adobe Experience Platform customers on Amazon Web Services (AWS)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use Federated Audience Composition if your Experience Platform instance is on AWS.</p>
<p>For more information about Experience Platform on AWS, please read the <a href="https://experienceleague.adobe.com/fr/docs/experience-platform/landing/multi-cloud">multi-cloud overview</a>.</p>
</br>
</td>
</tr>
</tbody>
</table> 
-->

<table>
<thead>
<tr>
<th><strong>Authentification OAuth pour Google BigQuery et Snowflake</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais vous connecter à Google BigQuery et Snowflake à l’aide d’OAuth.</p>
<p>Pour plus d’informations sur la création de connexions, consultez la <a href="../connections/home.md#create">présentation des connexions</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

## Version du 25 août {#fac-25-8}

### Nouvelles fonctionnalités {#fac-25-08-feature}

<table>
<thead>
<tr>
<th><strong>Prise en charge des clés composites dans la découverte de schémas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais combiner des colonnes pour créer une clé composite pour votre schéma.</p>
<p>Pour plus d’informations sur les schémas, consultez la <a href="../customer/schemas.md#create">vue d’ensemble des schémas</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Ajout de plusieurs jointures dans un lien pour les modèles</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter plusieurs jointures en un seul lien pour vos modèles.</p>
<p>Pour plus d’informations sur les modèles, consultez la <a href="../data-management/gs-models.md#create">vue d’ensemble des modèles</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Améliorations {#fac-25-8-improvements}

Cette version comprend les améliorations suivantes :

* **Ajout d’une fonction `StringAgg`**

  Vous pouvez désormais utiliser la fonction `StringAgg` pour les bases de données à spectre Redshift d’Amazon lors de l’accés à l’éditeur d’expression.

* Fonction **`Replace`**

  La description et la syntaxe de la fonction `Replace` ont été clarifiées dans la documentation.

### Compatibilité {#fac-25-8-compatibility}

* **Bases de données Azure Synapse**

  Vous pouvez désormais vous connecter en toute sécurité aux bases de données Azure Synapse avec PrivateLink ou un VPN. Pour plus dʼinformations, contactez l’assistance clientèle Adobe.

* **Base de données Oracle**

  Vous pouvez désormais vous connecter en toute sécurité aux bases de données Oracle. Pour plus dʼinformations, contactez l’assistance clientèle Adobe.

Pour plus d’informations sur les bases de données prises en charge dans la composition d’audiences fédérées, consultez la [vue d’ensemble des connexions](../connections/home.md).

## Version de juillet 2025 {#fac-25-7}

### Nouvelles fonctionnalités {#fac-25-07-feature}

<table>
<thead>
<tr>
<th><strong>Nouveau connecteur : Oracle</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le connecteur Oracle est désormais disponible pour utilisation avec la composition d’audiences fédérées.</p>
<p>Vous pouvez utiliser le connecteur Oracle pour les cas d’utilisation de création et d’enrichissement d’audiences.</p>
<p>Pour plus d’informations sur la connexion Oracle, consultez la <a href="../connections/home.md#create">vue d’ensemble des connexions</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertes de composition</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais vous abonner à des alertes pour en savoir plus sur les exécutions réussies et en échec de votre composition.</p>
<p>Pour plus d’informations sur l’abonnement aux notifications des exécutions de votre composition, consultez le <a href="../compositions/start-monitor-composition.md#alerts">guide de démarrage et de surveillance de votre composition</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Améliorations {#fac-25-07-improvements}

Cette version comprend l’amélioration suivante :

* **Augmentation de la longueur des caractères du serveur**

  Lors de la configuration de vos bases de données fédérées, vous pouvez désormais utiliser jusqu’à 255 caractères, contre 80 auparavant.

## Version de juin 2025 {#fac-25-6}

### Améliorations {#fac-25-06-improvements}

Cette version comprend les améliorations suivantes :

* **Disponibilité générale pour la clientèle Adobe Healthcare Shield**

  La composition d’audiences fédérées sera disponible pour la clientèle d’Adobe Healthcare Shield pour la création d’audiences, l’enrichissement et l’enrichissement des profils d’ici la fin juin.

  Vous trouverez plus d’informations sur la confidentialité et la sécurité dans la composition d’audiences fédérées dans le [guide de gouvernance des données, de confidentialité et de sécurité](/help/governance-privacy-security/home.md).

* **Contrôle d’accès au niveau de l’objet**

  La composition d’audiences fédérées prend désormais en charge le contrôle d’accès au niveau de l’objet pour appliquer des libellés d’accès aux compositions spécifiées.

  Vous trouverez plus d’informations sur l’utilisation des libellés d’accès au niveau de l’objet dans le [guide des compositions](/help/compositions/gs-compositions.md).

* **Rôles par défaut**

  Vous pouvez désormais utiliser l’un des rôles par défaut afin de gérer les autorisations d’utilisation pour l’accès à la composition d’audiences fédérées.

  Vous trouverez plus d’informations sur les rôles par défaut dans le [guide d’accès à la composition d’audiences fédérées](/help/governance-privacy-security/access-control.md).

* **Mises à jour incrémentielles dans les cas d’utilisation d’enrichissement des profils**

  L’activité Enregistrer les profils prend désormais en charge les mises à jour incrémentielles. Grâce aux mises à jour incrémentielles, vous pouvez interroger et actualiser des données incrémentielles tout en enrichissant les profils avec des données provenant d’entrepôts de données externes.

  Vous trouverez plus d’informations sur l’utilisation de l’activité d’enregistrement des profils dans le [guide de l’activité d’enregistrement des profils](/help/compositions/activities/save-profiles.md).

## Version de mai 2025 {#fac-25-5}

### Nouvelles fonctionnalités {#fac-25-05-feature}

<table>
<thead>
<tr>
<th><strong>Vue Zone de travail du modèle de données (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le modèle de données avec la vue Zone de travail est désormais disponible pour l’ensemble des clientes et clients.</p>
<p>La vue Zone de travail de la section Modèles de données améliore l’expérience en permettant la visualisation des modèles de données et de leurs liens dans une disposition de zone de travail, à côté de la vue tabulaire existante. </p>
<p>Pour plus d’informations sur cette fonctionnalité, consultez la <a href="../data-management/gs-models.md">vue d’ensemble des modèles de données</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Améliorations {#fac-25-5-improvements}

Cette version comprend les améliorations suivantes :

* **Contrôle d’accès basé sur les rôles**

  À compter de la version de mai, [!DNL Federated Audience Composition] prend en charge de nouvelles autorisations granulaires pour le contrôle d’accès. Les utilisateurs et utilisatrices peuvent attribuer ces autorisations aux rôles pour un accès plus précis à la [!DNL Federated Audience Composition].

  Pour en savoir plus sur les nouvelles autorisations, veuillez lire le [guide d’accès relatif à la composition d’audiences fédérées](/help/governance-privacy-security/access-control.md).

## Version d’avril 2025 {#fac-25-4}

### Nouvelles fonctionnalités {#fac-25-04-feature}

<table>
<thead>
<tr>
<th><strong>Vue Zone de travail du modèle de données (version Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La vue Zone de travail de la section Modèles de données améliore l’expérience en permettant la visualisation des modèles de données et de leurs liens dans une disposition de zone de travail, à côté de la vue tabulaire existante. </p>
<p>Le modèle de données avec la vue Zone de travail est actuellement disponible en version Beta pour certaines personnes uniquement.</p>
<p>Pour plus d’informations, consultez la <a href="../data-management/gs-models.md">documentation détaillée</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de l’Assistant IA pour la connaissance des produits</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant IA est une fonctionnalité de l’interface d’utilisation qui vous permet de parcourir et de comprendre les concepts Adobe et d’obtenir des informations opérationnelles sur votre environnement spécifique. Il est disponible dans plusieurs produits Adobe Experience Cloud, y compris la composition d’audiences fédérées.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-assistant.md">documentation détaillée</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité Enregistrer les profils</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> La composition d’audiences fédérées prend désormais en charge le cas d’utilisation d’enrichissement des profils, ce qui permet aux clientes et clients d’améliorer les profils Experience Platform existants avec les données de leurs entrepôts de données externes.
</p>
<p>Pour plus d’informations, consultez la <a href="../compositions/activities/save-profiles.md">documentation détaillée</a>.</p>
</br>
</td>
</tr>
</tbody>
</table>

### Améliorations {#fac-25-4-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Nom du modèle de données**

  Dans le menu Audiences, l’onglet **Compositions fédérées** affiche désormais le nom du modèle de données au lieu de l’identifiant, ce qui améliore la clarté et la simplicité d’utilisation globale.

* **Audience**

  Le menu Audience affiche désormais le nom ou le libellé du modèle de données sélectionné lorsqu’une personne sélectionne un modèle de données sans audiences associées.

* **Export d’audiences volumineuses**

  La composition d’audiences fédérées prend désormais en charge l’export d’audiences volumineuses, avec des tailles de fichier supérieures à 1 Go.

* **Activité Enregistrer l’audience**

  Une note a été ajoutée à l’activité **Enregistrer l’audience**, rappelant aux utilisateurs et utilisatrices de collaborer avec un administrateur ou une administratrice de données pour appliquer des libellés de gouvernance aux nouveaux schémas et jeux de données créés lors de la création et de l’enrichissement de l’audience.
  [En savoir plus sur les libellés d’utilisation des données](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/user-guide)

### Compatibilité {#fac-25-4-compat}

* **Connexion sécurisée Amazon Redshift**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge les connexions de liens privées sécurisées aux bases de données Amazon Redshift. [En savoir plus](../connections/home.md#amazon-redshift)

* **Google BigQuery**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge les connexions VPN sécurisées aux bases de données Google BigQuery. [En savoir plus](../connections/home.md#google-bigquery)

## Version de mars 2025 {#fac-25-3}

### Améliorations {#fac-25-3-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Autorisations de la composition d’audiences fédérées**

  À compter de la version de mars, [!DNL Federated Audience Composition] commencera à appliquer l’accès aux interfaces **Gestion des données fédérées** et **Compositions fédérées** aux utilisateurs et utilisatrices qui disposent de l’autorisation **Gérer les données fédérées**.

  Nous recommandons aux utilisateurs et utilisatrices de contacter les administrateurs et administratrices pour que cette autorisation soit ajoutée à leur rôle afin de continuer à accéder à l’interface d’utilisation [!DNL Federated Audience Composition].

  Pour savoir comment attribuer cette autorisation, consultez la [documentation détaillée](/help/governance-privacy-security/access-control.md).

### Compatibilité {#fac-25-3-compat}

* **Connexion à Databricks**

  Avec cette nouvelle version, la composition d’audiences fédérées prend désormais en charge la connectivité de lien privé pour les connexions à la base de données Databricks.
Cela inclut des connexions sécurisées aux bases de données Databricks hébergées sur Amazon Web Services (AWS) via un lien privé et aux bases de données Databricks hébergées sur Microsoft Azure via un VPN. [En savoir plus](../connections/home.md#databricks)

* **Prise en charge des clientes et clients B2B CDP**

  La composition d’audiences fédérées est désormais disponible pour les clientes et clients Business-to-Business (B2B) Customer Data Platform (CDP) pour les cas d’utilisation d’audience basés sur les personnes.

* **Connexion sécurisée à Snowflake**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge les connexions de liens privées sécurisées vers des bases de données Snowflake hébergées sur Microsoft Azure. [En savoir plus](../connections/home.md#snowflake)

## Version de février 2025 {#fac-25-2}

Cette version est fournie avec les modifications répertoriées ci-dessous.

* **Prise en charge de Microsoft Fabric**

  Vous pouvez désormais établir des connexions à des bases de données Microsoft Fabric par le biais de la composition d’audiences fédérées. [En savoir plus](../connections/home.md)

* **Prise en charge d’Amazon Redshift Spectrum**

  Amazon Redshift Spectrum est désormais pris en charge pour les connexions Amazon Redshift Database. [En savoir plus](../connections/home.md#amazon-redshift)

* **Expérience améliorée de création de schéma**

  Le processus de création de schéma a été amélioré grâce à une interface d’utilisation mise à jour, conçue pour être plus intuitive et plus facile à parcourir. Ces améliorations offrent aux personnes utilisant des données un moyen plus fluide et plus efficace de développer des modèles de données. [En savoir plus](../customer/schemas.md)

* **Prise en charge de l’enrichissement de l’audience pour Databricks**

  Vous pouvez désormais utiliser Databricks dans le flux Lecture d’audience, ce qui active les bases de données Databricks et permet de les configurer en tant que nouvelle destination. [En savoir plus](../connections/destinations.md)

## Version de novembre 2024 {#fac-24-11}

### Améliorations {#fac-24-11-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Liste autorisée d’adresses IP**

  Lors de l’ajout d’une base de données fédérée dans l’interface d’utilisation d’Adobe Experience Platform, vous pouvez désormais afficher directement les adresses IP associées à vos instances de composition d’audiences fédérées. Vous pouvez ainsi facilement copier et autoriser ces adresses IP pour vous connecter à votre base de données afin d’améliorer la sécurité et la flexibilité. [En savoir plus](../connections/home.md)

## Version d’octobre 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Auparavant disponible pour un ensemble d’organisations (LA), la composition d’audiences fédérées Adobe Experience Platform est désormais disponible pour tous les utilisateurs et utilisatrices (GA). Cette fonctionnalité est activée en fonction de votre offre et n’est visible qu’avec les autorisations associées. [En savoir plus](access-prerequisites.md)

### Compatibilité {#fac-24-10-compat}

Avec cette nouvelle version, la composition d’audiences fédérées est désormais compatible avec les systèmes répertoriés ci-dessous.

* **Prise en charge de Databricks**

  Vous pouvez désormais établir des connexions à des bases de données Databricks par le biais de la composition d’audiences fédérées. [En savoir plus](../connections/home.md#databricks)

* **Prise en charge de l’accès sécurisé à Snowflake via AWS PrivateLink**

  L’accès sécurisé à votre entrepôt de données Snowflake externe par le biais d’un lien privé est désormais pris en charge. Notez que votre compte Snowflake doit être hébergé sur Amazon Web Services (AWS) et situé dans la même région que votre environnement de composition d’audiences fédérées. Veuillez contacter votre représentant ou représentante Adobe pour obtenir de l’aide sur la configuration de l’accès sécurisé à votre compte Snowflake. [En savoir plus](../connections/home.md#snowflake)

* **Prise en charge d’Amazon Redshift sans serveur**

  Avec cette nouvelle version, la composition d’audiences fédérées prend en charge [Amazon Redshift sans serveur](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Améliorations {#fac-24-10-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

* **Actualiser les schémas existants**

  Lorsqu’une colonne est créée, modifiée ou supprimée dans une base de données fédérée, vous pouvez désormais détecter et appliquer les modifications en cliquant sur le bouton **[!UICONTROL Actualiser le schéma]** dans le schéma correspondant. [En savoir plus](../customer/schemas.md#schema-refresh)

* **Associer un modèle de données à une nouvelle composition**

  Lors de la création d’une composition, vous pouvez désormais sélectionner le modèle de données à y associer. Avec cette nouvelle option, la configuration de vos activités est plus facile, car seuls les tableaux du modèle de données associé sont disponibles. [En savoir plus](../compositions/create-composition.md)

## Version de juillet 2024 : composition d’audiences fédérées (disponibilité limitée) {#fac-la}

La composition d’audiences fédérées permet aux entreprises d’accéder de manière flexible et étendue aux entrepôts de données d’entreprise, afin de composer des audiences à l’aide de jeux de données d’entreprise critiques et d’optimiser des expériences initiées par la marque et en temps réel. Grâce à cette nouvelle approche, en tant qu’utilisateur ou utilisatrice d’[Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/home){target="_blank"} et/ou d’[Adobe Journey Optimizer](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/ajo-home){target="_blank"}, vous pouvez fédérer les données d’audience directement à partir de votre entrepôt de données existant pour enrichir les audiences Adobe Experience Platform dans un seul système.

La composition d’audiences fédérées répond aux demandes croissantes du marché pour les entreprises qui ont besoin de la flexibilité nécessaire pour composer des audiences avec des jeux de données d’entrepôt. Elle permet aux entreprises de réduire le mouvement des données tout en mettant les données d’audience critiques à la disposition des équipes marketing pour répondre aux besoins des cas d’utilisation et alimenter les expériences personnalisées.

Pour en savoir plus sur les fonctionnalités de la composition d’audiences fédérées, reportez-vous à [cette page](get-started.md) et aux [questions fréquentes](faq.md).

Pour plus d’informations sur les conditions préalables à l’accès aux compositions d’audiences fédérées et aux mécanismes de sécurisation actuels, consultez [cette page](access-prerequisites.md).
