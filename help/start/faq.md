---
title: Questions fréquentes
description: Questions fréquentes sur la composition des audiences fédérées Adobe Experience Platform
badge: label="Disponibilité limitée" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 3%

---

# Questions fréquentes {#faq}

Vous trouverez ci-dessous une liste des questions fréquentes sur la composition des audiences fédérées Adobe Experience Platform. Une FAQ globale est également disponible pour Adobe Experience Platform Segmentation Service dans [cette page](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quelles sont les autorisations requises pour accéder à la composition d’audiences fédérées ?

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et Adobe Journey Optimizer Prime ou Ultimate. Il n’existe aucune autorisation spécifique pour la composition d’audiences fédérées. La seule condition préalable pour accéder à cette fonctionnalité est d’avoir acheté le module complémentaire de composition d’audiences fédérées .

+++

+++Quels entrepôts cloud sont pris en charge ?

Pour cette version, la composition d’audiences fédérées est compatible avec :

* Amazon Redshift
* Azure synapse
* Google BigQuery
* Snowflake
* Vertica Analytics

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

Non, la composition d’audiences fédérées stocke uniquement les métadonnées (descriptions de schéma). Aucune donnée client n’est en cours de transition. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++La composition d’audiences fédérées stocke-t-elle une copie physique de cette liste de personnes à envoyer aux systèmes en aval ?

La composition d’audiences fédérées ne conserve pas de copie physique des données. La fréquence est paramétrée dans la composition pour définir la fréquence d&#39;actualisation de ces données. Les données d’audience qui en résultent ne sont pas stockées par Adobe Experience Platform plus longtemps que ne l’exigent les cas d’utilisation ou l’action du client.

Par exemple :

* Dans le cas d’une création d’audience, l’audience est créée dans votre entrepôt. Vous pouvez utiliser la composition d’audience fédérée pour d’autres tâches de composition et de manipulation de données avant de publier l’audience résultante et les attributs associés via Adobe Experience Platform Audience Portal. La définition de l’audience et les attributs associés sont transmis à Adobe Experience Platform.
Notez que l’expiration des données actuelles pour les audiences générées en externe est de 30 jours. Cette expiration des données réduit la quantité de données excédentaires stockées au sein d’une organisation. Une fois la période d’expiration des données écoulée, le jeu de données associé est toujours visible dans l’inventaire du jeu de données, mais vous ne pouvez pas activer l’audience et le nombre de profils s’affiche comme nul. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Dans le cas d’un enrichissement d’audience, le point de départ est une audience Adobe Experience Platform existante. Deux scénarios peuvent être présentés ici :
   1. Importation d’attributs de payload d’audience supplémentaires à partir de l’entrepôt de données fédéré : dans ce cas, les attributs supplémentaires qui sont ajoutés seront repris dans le cadre de cette définition d’audience. L’expiration des données pour les audiences générées en externe est la même que celle décrite ci-dessus : 30 jours.
   1. Affinez l’audience Adobe Experience Platform existante en fonction d’attributs supplémentaires existant dans votre entrepôt de données. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Si les données des modèles de cas d’utilisation Création d’audience et Enrichissement d’audience ne sont pas conservées, comment est-il stocké temporairement ?

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
