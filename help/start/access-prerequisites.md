---
title: Conditions préalables et barrières de sécurité pour la composition d’audiences fédérées
description: Découvrez les conditions préalables, les autorisations et les barrières de sécurité pour la composition d’audiences fédérées
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 61ad8899f7de601b64c7b42cb873a172fcaea145
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# Conditions préalables et mécanismes de sécurisation {#fac-access}

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer **Prime** ou **Ultimate**. Pour accéder à cette fonctionnalité, vous devez avoir acheté le module complémentaire Composition d’audience fédérée .

>[!AVAILABILITY]
>
>Une fois que vous avez reçu l’e-mail de bienvenue d’Adobe, il peut s’écouler quelques heures de plus avant que l’interface ne soit mise à jour et que les fonctionnalités soient mises à votre disposition.

## Autorisations {#permissions}

Lorsque vous achetez le module complémentaire de composition d’audiences fédérées, un profil de produit est créé pour chaque environnement de test actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention d’affectation des noms : `ACP_FAC - <<SandboxName>> - admin.` Pour accéder à la composition d’audience fédérée pour un environnement de test spécifique, les utilisateurs doivent être ajoutés au profil de produit créé pour cet environnement de test.

Par exemple, si un nouvel environnement de test nommé &quot;fac-test&quot; est activé, un profil de produit correspondant &quot;ACP_FAC - fac-test - admin&quot; est créé. Pour accéder à la composition d’audiences fédérées avec cet environnement de test, les utilisateurs doivent être ajoutés à ce profil de produit.

## Listes autorisées des adresses IP {#ip}

Pour activer en toute sécurité Federated Audience Composition et accéder à vos bases de données, contactez votre représentant d’Adobe afin d’obtenir les adresses IP des serveurs Federated Audience Composition qui y accéderont.

Ajoutez ces adresses IP à votre liste autorisée pour accorder l’accès à la composition d’audiences fédérées.

## Mécanismes de sécurisation et limitations {#fac-guardrails}

* L’utilisation d’audiences et d’attributs provenant de la composition d’audiences fédérées n’est actuellement pas disponible avec Healthcare Shield et Privacy and Security Shield.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Les droits, les limites de produit et les barrières aux performances répertoriés dans la [documentation Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent à ce module complémentaire.
