---
title: Présentation de la composition de l’audience fédérée
description: Découvrez la composition d’Adobe Federated Audience et comment l’utiliser dans des services en aval tels que Adobe Experience Platform et Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# Présentation de la composition de l’audience fédérée

La composition de l’audience fédérée vous permet de créer et d’enrichir des audiences à partir de vos entrepôts de données tiers et d’importer les audiences dans Adobe Experience Platform. Vous bénéficiez ainsi d’une solution simple et puissante pour connecter votre entrepôt de données d’entreprise directement au sein de services en aval tels qu’Adobe Real-Time Customer Data Platform ou Adobe Journey Optimizer et exécuter des requêtes sur les tables de votre entrepôt de données. Par conséquent, vous pouvez accéder aux données client stockées dans des entrepôts de données et des plateformes de stockage dans le cloud telles qu’Amazon Redshift et Azure Synapse Analytics.

## Fonctionnalités {#rn-capabilities}

La composition d’audiences fédérées étend la valeur de Real-Time CDP et Journey Optimizer avec une approche globale du traitement et de l’activation des audiences :

* **Élargissez l’accès aux jeux de données critiques basés sur des entrepôts afin de créer des audiences à forte valeur ajoutée** : vous pouvez utiliser les entrepôts de données existants comme système principal d’enregistrement, tout en exploitant les applications les plus performantes pour offrir de superbes expériences client.

* **Prise en charge complète des cas d’utilisation d’engagement** : la composition d’audiences fédérées, associée à Real-Time CDP ou Journey Optimizer, prend en charge les expériences personnalisées initiées par la marque avec des audiences fédérées et fournit des expériences en temps réel déclenchées par des événements en temps réel, associées à des attributs de personne pour répondre aux exigences des cas d’utilisation au sein des équipes.

* **Minimiser le déplacement et la duplication des données** : vous pouvez créer des audiences à partir de jeux de données qui se trouvent dans des entrepôts de données d’entreprise sans copier les données sous-jacentes pour gérer les profils et audiences marketing exploitables.

* **Utiliser un seul système pour les workflows pilotés par l’expérience** : vous pouvez traiter à la fois les audiences ingérées et fédérées dans Adobe Experience Platform et coordonner les expériences sortantes sur tous les canaux.

* **Prise en charge de plusieurs éditions** : les clients B2C et B2B de la plateforme de données clients peuvent tirer parti de la composition d’audiences fédérées pour créer des audiences basées sur les personnes en intégrant des données provenant d’entrepôts de données d’entreprise pris en charge. En outre, elles peuvent enrichir les audiences basées sur les personnes existantes d’Experience Platform en incorporant les attributs pertinents disponibles dans l’entrepôt de données d’entreprise, ce qui améliore leurs profils d’audience pour un engagement plus personnalisé et ciblé.

## Cas d’utilisation {#use-cases}

La Composition d’audiences fédérées prend en charge **trois** catégories de cas d’utilisation : création d’audience, enrichissement d’audience et enrichissement de profil client.

* **Création d’audiences** : vous pouvez créer des audiences à partir d’un entrepôt de données et fédérer ces audiences dans Experience Platform pour les utiliser dans Real-Time CDP ou Journey Optimizer par le biais d’une interface utilisateur conviviale de type glisser-déposer pour les spécialistes du marketing. Par conséquent, vous pouvez interroger vos entrepôts de données sans copier de données sous-jacentes sensibles ni dupliquer des données existantes.
   * **Exemple :** créez une audience d’anciennes personnes acheteuses à forte valeur ajoutée à l’aide de données de transaction historiques dans l’entrepôt, sans copier ces transactions dans Experience Platform.

* **Enrichissement de l’audience** : vous pouvez ajouter plus de détails à vos audiences existantes dans Experience Platform en utilisant des jeux de données supplémentaires issus de vos entrepôts de données et en superposant vos audiences avec ces informations, le tout sans copier les données sous-jacentes dans Experience Platform. Grâce à l’enrichissement d’audience, vous pouvez offrir une personnalisation améliorée avec l’audience enrichie.
   * **Exemple :** enrichissez une audience Experience Platform d’abandons de panier avec l’audience Composition d’audiences fédérées d’anciennes personnes acheteuses à forte valeur ajoutée pour diffuser une offre ciblée.

* **Enrichissement du profil** : vous pouvez sélectionner des attributs de client individuels dans votre entrepôt de données pour améliorer les profils Experience Platform. Grâce aux données fédérées ajoutées à ces profils, vous pouvez améliorer l’alimentation des expériences sur le moment qui sont déclenchées par les signaux clients entrants.
   * **Exemple :** enrichissez un profil Experience Platform avec les informations de l’audience fédérée. Vous pouvez désormais commercialiser auprès d’un visiteur ou d’une visiteuse du site qui appartient à l’audience fédérée des personnes acheteuses précédentes à forte valeur ajoutée une offre ciblée déclenchée par son comportement sur le site.

![Diagramme](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Pour plus d’informations sur les cas d’utilisation de la Composition d’audiences fédérées, consultez l’[article technique Composition d’audiences fédérées](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Principales étapes {#gs-steps}

La composition d’audiences fédérées Adobe vous permet de créer et de mettre à jour des audiences Adobe Experience Platform directement à partir de votre base de données, sans processus d’ingestion.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **Créer une connexion** : rassemblez des données provenant de diverses sources et fusionnez-les dans un jeu de données unifié. Pour plus d’informations sur la connexion des applications Adobe Experience Platform à votre entrepôt de données d’entreprise, sur les bases de données prises en charge et sur la configuration de votre connexion, consultez la [présentation des connexions](./connections/home.md).

2. **Modéliser vos données** : concevez et créez des schémas et des modèles de données qui définissent la structure, les relations et les contraintes des données. Pour plus d’informations sur les schémas, consultez la [présentation des schémas](./data-modelling/schemas.md). Pour plus d’informations sur les modèles de données, consultez la [présentation des modèles de données](./data-modelling/models.md).

3. **Transformer vos données** : appliquez des techniques de manipulation des données pour modifier le format, la structure ou les valeurs des éléments de données afin de les rendre compatibles ou adaptés à des analyses ou des applications spécifiques.

4. **Composer votre audience** : créez, orchestrez et créez des audiences. Pour plus d’informations sur la composition d’audiences, consultez la [présentation de la composition](./compositions/home.md). Vous pouvez également mettre à jour ou réutiliser des audiences existantes via le portail et les destinations Adobe Experience Platform Audience. En savoir plus sur [cette page](./connections/destinations.md)

>[!NOTE]
>
>Après l’exécution de la composition, l’audience obtenue est enregistrée dans Adobe Experience Platform en tant qu’audience externe. Elle est disponible dans Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer. Elle est rendue accessible dans le menu **Audiences**. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Gouvernance, confidentialité et sécurité {#governance-privacy-security}

### Demandes d’accès à des informations personnelles {#gov-privacy-requests}

Une fois la composition créée, les audiences obtenues sont enregistrées dans Adobe Experience Platform.

Vous pouvez ensuite effectuer des demandes d’accès à des informations personnelles et/ou supprimer des données de profil correspondant à ces audiences via Adobe Experience Platform **Privacy Service**, qui fournit une [interface d’utilisation](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=fr){target="_blank"} et une [API RESTful](https://experienceleague.adobe.com/fr/docs/experience-platform/privacy/api/overview){target="_blank"} pour vous aider à gérer les demandes de données des clientes et clients.

>[!NOTE]
>
>Pour plus d’informations sur Privacy Service, consultez la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=fr){target="_blank"}.

Vous pouvez créer et gérer des demandes individuelles d’accès et de suppression de données des clientes et clients de la composition d’audiences fédérées Adobe. Les étapes de soumission des **demandes d’accès** et **demandes de suppression** sont présentées dans la [documentation du profil client en temps réel](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/privacy){target="_blank"}.

### Journal d’audit {#gov-audit-trail}

La fonctionnalité de journal d’audit fournit un enregistrement détaillé et chronologique de toutes les actions et de tous les événements qui ont été effectués sur votre environnement en temps réel. Pour en savoir plus sur le journal d’audit, consultez la [présentation du journal d’audit](./admin/audit-trail.md).

## En savoir plus {#learn}

<!-- Workflow + Workflow activities-->

Découvrez comment accéder à la composition d’audiences fédérées, aux mécanismes de sécurisation et aux limitations sur [cette page](./start/access-prerequisites.md).

Pour obtenir des réponses aux questions fréquentes, lisez le [FAQ sur la composition d’audiences fédérées](./faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Paramètres d’exécution"
>abstract="Dans cette section, vous pouvez configurer les paramètres liés à l’exécution du workflow, tels que le nombre de jours pendant lesquels l’historique de composition est conservé."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Activité non modifiable"
>abstract="Lorsqu’une activité **Requête** ou **Enrichissement** est paramétrée avec des données supplémentaires dans la console, les données d’enrichissement sont prises en compte et transmises à la transition sortante, mais elles ne peuvent pas être modifiées."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Créer un lien"
>abstract="Définissez les paramètres du lien."


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Requête incrémentale"
>abstract="L’activité **Requête incrémentale** vous permet d’interroger la base de données à l’aide du concepteur de requête. À chaque nouvelle exécution de cette activité, les résultats des exécutions précédentes sont exclus. Cela vous permet de ne cibler que les nouveaux éléments."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Historique des requêtes incrémentales"
>abstract="Historique des requêtes incrémentales"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Données traitées des requêtes incrémentales"
>abstract="Données traitées des requêtes incrémentales"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Mode de requête incrémentale"
>abstract="La requête incrémentale permet d’exécuter la même requête plusieurs fois en excluant les résultats des exécutions précédentes pour chaque nouvelle exécution."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Mode de requête incrémentale"
>abstract="La requête incrémentale permet d’exécuter plusieurs fois la même requête en ne prenant en compte que les résultats pour lesquels le champ de date contient une date postérieure ou égale à la date de dernière exécution de l’activité de requête incrémentale."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Sélectionner la dimension de ciblage"
>abstract="La dimension de ciblage permet de définir la population ciblée par l’opération : personnes destinataires, personnes bénéficiaires d’un contrat, opérateurs et opératrices, personnes abonnées, etc. Par défaut, pour les e-mails et les SMS, la cible est sélectionnée à partir du tableau intégré Personnes destinataires. Pour les notifications push, la dimension cible par défaut est Applications des personnes abonnées."

