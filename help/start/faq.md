---
title: Questions fréquentes
description: Questions fréquentes sur la composition d’audiences fédérées Adobe Experience Platform
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 1bdab901b7aae3019b672a34eab184405c927f56
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 82%

---

# Questions fréquentes {#faq}

Vous trouverez ci-dessous les questions fréquentes sur la composition d’audiences fédérées Adobe Experience Platform. Une section globale de Questions fréquentes est également disponible pour le service de segmentation Adobe Experience Platform dans [cette page](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/faq){target="_blank"}.


+++Quelles sont les autorisations requises pour accéder à la composition d’audiences fédérées ?

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer Prime ou Ultimate. Vous devez avoir acheté le module complémentaire Composition d’audiences fédérées.

Pour utiliser la composition d’audiences fédérées, chaque personne doit être ajoutée à un profil spécifique créé pour chaque sandbox. Pour plus d’informations, consultez la page [Accéder à la composition d’audiences fédérées](access-prerequisites.md).

+++

+++Quels entrepôts cloud sont pris en charge ?

La liste des systèmes pris en charge avec la composition d’audiences fédérées est disponible sur [cette page](../start/access-prerequisites.md#supported-systems).

+++


+++Plusieurs entrepôts de données peuvent-ils être interrogés dans la même composition ?

Oui, plusieurs entrepôts peuvent être interrogés dans la même composition et peuvent combiner des données provenant de plusieurs sources.  Généralement, chaque [activité de composition](../compositions/orchestrate-activities.md) (requête, enrichissement, partage etc.) exécute une ou plusieurs instructions SQL en fonction de la configuration de l’activité, des bases de données ciblées (il peut y avoir plusieurs cas d’accès aux données fédérées) et des sorties d’une ou de plusieurs tables de travail avec le résultat de l’exécution. Ces tables de travail sont utilisées comme entrée pour les activités consécutives.

+++

+++ Puis-je accéder à l’ensemble de ma base de données à l’aide de la composition d’audiences fédérées ?

Non, c’est à vous de configurer l’accès à une base ou à un schéma dédié ou partagé. Nous vous recommandons de créer un schéma dédié pour la composition d’audiences fédérées et de copier ou partager uniquement les jeux de données d’analyse de rentabilité.
+++

+++Ai-je accès à tous les tableaux du schéma dédié ?

Oui, une fois la connexion établie, la composition d’audiences fédérées peut être utilisée pour détecter tous les tableaux en fonction des droits initiaux définis. Vous pouvez ensuite utiliser l’éditeur de schéma visuel pour :

* détecter les colonnes et les clés primaires de vos tableaux ;
* créer des libellés conviviaux pour ces tableaux ;
* créer des libellés conviviaux pour chaque colonne ;
* masquer les colonnes inutiles ;
* enregistrer la description de ces tableaux.
+++

+++Existe-t-il un enregistrement temporaire dans la composition d’audiences fédérées ?

Non, la composition d’audiences fédérées enregistre uniquement les métadonnées (descriptions de schéma). Aucune donnée de clientèle ne transite. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++La composition d’audiences fédérées enregistre-t-elle une copie physique de cette liste de personnes à envoyer aux systèmes en aval ?

La composition d’audiences fédérées ne conserve pas de copie physique des données. La fréquence est configurée dans la composition pour définir la fréquence d’actualisation de ces données. Les données de l’audience obtenue ne sont pas enregistrées par Adobe Experience Platform plus longtemps que ne l’exigent les cas d’utilisation ou l’action du client ou de la cliente.

Par exemple :

* Dans le cas d’une création d’audience, l’audience est créée dans votre entrepôt de données. Vous pouvez utiliser la composition d’audiences fédérées pour d’autres tâches de composition et de manipulation de données avant de publier l’audience obtenue et les attributs associés via le portail d’audience Adobe Experience Platform. La définition de l’audience et les attributs associés sont transmis à Adobe Experience Platform.
Notez que l’expiration des données actuelles pour les audiences générées en externe est de 30 jours. Cette expiration de données réduit la quantité de données excédentaires enregistrées au sein d’une organisation. Une fois la période d’expiration des données écoulée, le jeu de données associé est toujours visible dans l’inventaire du jeu de données, mais vous ne pouvez pas activer l’audience et le nombre de profils s’affiche comme nul. Pour en savoir plus, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* Dans le cas d’un enrichissement d’audience, le point de départ est une audience Adobe Experience Platform existante. Deux scénarios peuvent être envisagés ici :
   1. Importer des attributs de payload d’audience supplémentaires à partir de l’entrepôt de données fédérées : dans ce cas, les attributs supplémentaires qui sont ajoutés seront repris dans le cadre de cette définition d’audience. L’expiration des données pour les audiences générées en externe est la même que celle décrite ci-dessus : 30 jours.
   1. Affinez l’audience Adobe Experience Platform existante en fonction d’attributs supplémentaires existant dans votre entrepôt de données. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Si les données pour les cas d’utilisation Création d’audience et Enrichissement d’audience ne sont pas conservées, comment sont-elles enregistrées temporairement ?

Les données de l’audience obtenues ne sont pas conservées indéfiniment dans Adobe Experience Platform ou dans la composition d’audiences fédérées. Elles ne seront pas conservées plus longtemps que ce qui est requis par votre cas d’utilisation. Les attributs d’audience importés dans le cadre du payload d’audience ne sont conservés que pour définir l’audience. La durée de conservation est basée sur la durée de vie de n’importe quelle audience. La valeur par défaut est de 30 jours.

+++

+++Puis-je supprimer une audience chargée personnalisée ?

Non, dans la version actuelle, vous ne pouvez pas supprimer les audiences chargées personnalisées.

+++

+++Si je combine des données provenant de plusieurs sources, comment les données sont-elles jointes ? Le Service d’identités est-il utilisé ?

Non, le Service d’identités n’est pas utilisé pendant une composition. Les données entre les différentes sources utilisées dans la composition sont jointes par une logique définie par l’utilisateur ou l’utilisatrice (telle qu’elle est exprimée dans le modèle sous-jacent), par exemple l’identifiant CRM, le numéro de compte d’utilisateur ou d’utilisatrice, etc. Vous devez sélectionner l’identité utilisée comme identifiant dans l’audience pour la sélection dans votre entrepôt de données. Sur une audience obtenue de la composition d’audiences fédérées, vous devez identifier l’espace de noms d’identité de l’identité dans le jeu de données obtenu.

+++

+++Comment les préférences de consentement des clients sont-elles respectées pour les audiences générées en externe qui sont importées dans la composition d’audiences fédérées ?

À mesure que les données client sont capturées à partir de plusieurs canaux, les politiques de combinaison et de fusion d’identités permettent de consolider ces données dans un profil client en temps réel unique. Les informations sur les préférences de consentement des clients sont stockées et évaluées au niveau du profil.

Les destinations Real-Time CDP et Journey Optimizer en aval vérifient les préférences de consentement de chaque profil avant l’activation. Les informations de consentement de chaque profil sont comparées aux exigences de consentement pour une destination particulière. Si le profil ne répond pas aux exigences, il n’est pas envoyé à une destination.

Lorsqu’une audience externe est ingérée dans la composition d’audience fédérée, elle est réconciliée avec les profils existants à l’aide d’un identifiant principal, tel qu’un e-mail ou un ECID. Par conséquent, les politiques de consentement existantes resteront en vigueur tout au long de l’activation.

>[!NOTE]
>
>Étant donné que les variables de payload ne sont pas stockées dans le profil, mais dans le lac de données, vous ne devez pas inclure d’informations de consentement dans les audiences générées en externe. Utilisez plutôt d’autres canaux d’ingestion Adobe Experience Platform où les données de profil sont importées.

+++