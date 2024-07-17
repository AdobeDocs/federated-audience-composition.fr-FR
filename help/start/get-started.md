---
title: Prise en main de la composition d’audiences fédérées
description: Découvrez ce qu’est la composition d’audiences fédérées Adobe et comment l’utiliser dans Adobe Experience Platform
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 63192ea583aca7bc4a30b4a9d2071b83d0a46406
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 8%

---


# Prise en main de la composition d’audiences fédérées {#gs-fac}

La composition d’audiences fédérées de Adobe Experience Platform offre une solution simple et puissante pour connecter directement votre entrepôt de données d’entreprise dans Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer et exécuter des requêtes sur les tables de votre entrepôt de données.

Adobe Federated Audience Composition permet aux utilisateurs d’applications Adobe Experience Platform d’accéder aux données de leurs clients stockées dans leur entrepôt de données d’entreprise. Les données client peuvent se trouver dans plusieurs entrepôts de données et sont désormais accessibles instantanément, sans réplication.


## Cas d’utilisation {#rn-uc}

Dans une interface utilisateur conviviale pour le marketing, créez des règles de segmentation qui recherchent dans votre entrepôt de données une liste d’utilisateurs qualifiés pour un segment spécifique nécessaire aux campagnes marketing, accédez aux audiences existantes de l’entrepôt pour activation ou enrichissez les audiences Adobe Experience Platform avec des points de données supplémentaires qui existent dans l’entrepôt.

Dans cette version, deux cas d’utilisation sont disponibles : Segmentation d’audience et Enrichissement d’audience. L’enrichissement de profil sera disponible dans une prochaine version.

![diagramme](assets/fac-use-cases.png){zoomable="yes"}

## Principales étapes {#gs-steps}

Adobe la composition des audiences fédérées vous permet de créer et de mettre à jour des audiences Adobe Experience Platform directement à partir de votre base de données, sans processus d’ingestion.

![diagramme](assets/steps-diagram.png){zoomable="yes"}

Principales étapes :

* **Configuration**

   1. Connectez Adobe Experience Platform et votre entrepôt de données d’entreprise.
Les bases de données suivantes sont prises en charge : Snowflake, Google Big Query, Azure Synapse, Redshift.
En savoir plus sur [cette page](../connections/federated-db.md)
   1. Créez des schémas pour sélectionner les données qui doivent être accessibles à partir de l’interface utilisateur.
En savoir plus sur [cette page](../customer/schemas.md)
   1. Créez des liens pour votre modèle de données.
En savoir plus sur [cette page](../data-management/gs-models.md)

* **Composer les audiences**

   1. Concevez et exécutez des compositions pour créer des audiences.
En savoir plus sur [cette page](../compositions/gs-compositions.md)
   1. Mise à jour ou réutilisation d’audiences existantes via le portail d’audience Adobe Experience Platform et les destinations.
En savoir plus sur [cette page](../connections/destinations.md)

## Questions fréquentes {#faq}

Vous trouverez ci-dessous une liste des questions fréquentes sur la composition des audiences fédérées. Une FAQ globale est également disponible pour Adobe Experience Platform Segmentation Service dans [cette page](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quelles sont les autorisations requises pour accéder à la composition d’audiences fédérées ?

Il n’existe aucune autorisation spécifique pour la composition d’audiences fédérées. La seule condition préalable pour accéder à cette fonctionnalité est d’avoir acheté le module complémentaire de composition d’audiences fédérées .

+++

+++Quels entrepôts cloud sont pris en charge ?

Pour cette version, la composition d’audiences fédérées est compatible avec :

* Snowflake
* Google BigQuery
* Azure synapse
* Amazon Redshift

+++


+++Plusieurs entrepôts de données peuvent-ils être interrogés dans la même composition ?

Oui, plusieurs entrepôts peuvent être interrogés dans la même composition et peuvent combiner des données provenant de plusieurs sources.  En règle générale, chaque [activité de composition](../compositions/orchestrate-activities.md) (requête, enrichissement, division, etc.) exécute une ou plusieurs instructions SQL en fonction de la configuration de l&#39;activité, des bases de données ciblées (il peut y avoir plusieurs cas d&#39;accès aux données fédérées) et des sorties d&#39;une ou de plusieurs tables de travail avec le résultat de l&#39;exécution. Ces tables de travail sont utilisées comme entrée pour les activités consécutives.

+++

+++ Puis-je accéder à l’ensemble de ma base de données à l’aide de la composition d’audiences fédérées ?

Non, c&#39;est à vous de configurer l&#39;accès à une base/un schéma dédié ou partagé. Nous vous recommandons de créer un schéma dédié pour la composition d’audiences fédérées et de copier/partager uniquement les jeux de données de cas d’entreprise.
+++



+++Ai-je accès à toutes les tables du schéma dédié ?

Oui, une fois connecté, la composition d’audience fédérée peut être utilisée pour découvrir toutes les tables en fonction des droits initiaux définis, puis vous pouvez utiliser l’éditeur de schéma visuel pour :

* Découvrir les colonnes et les clés primaires de vos tables
* Création de libellés conviviaux pour ces tableaux
* Créer des libellés conviviaux pour chaque colonne
* Masquer les colonnes inutiles
* Description de l’enregistrement de ces tableaux
+++


+++Existe-t-il un stockage temporaire dans la composition d’audiences fédérées ?

Non, la composition d’audiences fédérées stocke uniquement les métadonnées (descriptions de schéma). Aucune donnée client n’est en cours de transition. Le flux d’exportation d’audience est effectué directement à partir de Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) vers la base de données client. Le flux de création et de mise à jour s’effectue directement de votre base de données de l’entrepôt de données vers Adobe Experience Platform Audience Portal.

+++

+++La composition d’audiences fédérées stocke-t-elle une copie physique de cette liste de personnes à envoyer aux systèmes en aval ?

La composition d’audiences fédérées ne conserve pas de copie physique des données. La fréquence est paramétrée dans la composition pour définir la fréquence d&#39;actualisation de ces données. Les données d’audience qui en résultent ne sont pas stockées par Adobe Experience Platform plus longtemps que ne l’exigent les cas d’utilisation ou l’action du client.

Par exemple :

* Dans le cas d’une segmentation d’audience, l’audience est créée dans votre entrepôt. Vous pouvez utiliser la composition d’audiences fédérées pour d’autres tâches de composition et de manipulation de données avant de publier l’audience résultante et les attributs associés via Adobe Experience Platform Audience Portal. La définition de l’audience et les attributs associés sont transmis à Adobe Experience Platform.
Notez que l’expiration des données actuelles pour les audiences générées en externe est de 30 jours. Cette expiration des données réduit la quantité de données excédentaires stockées au sein d’une organisation. Une fois la période d’expiration des données écoulée, le jeu de données associé est toujours visible dans l’inventaire du jeu de données, mais vous ne pouvez pas activer l’audience et le nombre de profils s’affiche comme nul. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Dans le cas d’un enrichissement d’audience, le point de départ est une audience Adobe Experience Platform existante. Deux scénarios peuvent être présentés ici :
   1. Importation d’attributs de payload d’audience supplémentaires à partir de l’entrepôt de données fédéré : dans ce cas, les attributs supplémentaires qui sont ajoutés seront repris dans le cadre de cette définition d’audience. L’expiration des données pour les audiences générées en externe est la même que celle décrite ci-dessus : 30 jours.
   1. Affinez l’audience Adobe Experience Platform existante en fonction d’attributs supplémentaires existant dans votre entrepôt de données. Par exemple, vous avez une audience de clients qui ont manifesté de l’intérêt pour un produit particulier sur le site web au cours des deux derniers mois. Vous souhaitez maintenant prendre cette audience en compte et la segmenter davantage à l’aide de la Composition de l’audience fédérée afin de n’inclure que les clients ayant un score de crédit élevé. Le score de crédit est considéré comme sensible, et les points de données de score de crédit individuels ne sont pas copiés depuis l’entrepôt de données.
+++

+++Si les modèles de cas d’utilisation de la segmentation d’audience et de l’enrichissement d’audience ne sont pas conservés, comment est-il stocké temporairement ?

Les données d’audience résultantes ne persistent pas indéfiniment dans Adobe Experience Platform ou dans la composition d’audience fédérée. Elle ne sera pas conservée plus longtemps que ce qui est requis par votre cas d’utilisation. Les attributs d’audience apportés dans le cadre de la charge utile de l’audience ne sont conservés que dans le cadre de la définition de l’audience. La durée de persistance est basée sur la durée de vie (TTL) pour n’importe quelle audience ; la valeur par défaut est de 30 jours.

+++

+++Puis-je supprimer une audience chargée personnalisée ?

Vous pouvez supprimer les audiences qui ne sont pas utilisées dans l’activation en aval directement dans Audience Portal en sélectionnant simplement Supprimer dans le menu d’actions. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.

+++

+++Si je combine des données provenant de plusieurs sources, comment joignons-nous les données ? Utilisons-nous le service Identity ?

Non, Identity Service n’est pas utilisé pendant une composition. Les données entre les différentes sources utilisées dans la composition sont unies par une logique définie par l’utilisateur (telle qu’elle est exprimée dans le modèle sous-jacent), par exemple l’identifiant CRM, le numéro de compte d’utilisateur, etc. Vous devez sélectionner l’identité utilisée comme identifiant dans l’audience à sélectionner dans votre entrepôt de données. Sur une audience résultante de la composition d’audience fédérée, vous devez identifier l’espace de noms d’identité de l’identité dans le jeu de données résultant.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->

## En savoir plus {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Paramètres d’exécution"
>abstract="Dans cette section, vous pouvez paramétrer les paramètres relatifs à l&#39;exécution du workflow, par exemple le nombre de jours pendant lesquels l&#39;historique de la composition est conservé."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activité non modifiable"
>abstract="Lorsqu’une activité **Requête** ou **Enrichissement** est paramétrée avec des données supplémentaires dans la console, les données d’enrichissement sont prises en compte et transmises à la transition sortante, mais elles ne peuvent pas être modifiées."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Créer un lien"
>abstract="Définissez les paramètres du lien."
