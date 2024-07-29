---
title: Accès à la composition d’audiences fédérées
description: Découvrez comment accéder à la composition d’audiences fédérées.
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 618d1675c28213d7a316f40cd624d282e01297f1
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 2%

---

# Accès à la composition d’audiences fédérées {#fac-access}

## Modules et modules complémentaires {#package}

La composition d’audiences fédérées requiert les packages Adobe Real-Time Customer Data Platform et Adobe Journey Optimizer Prime ou Ultimate. Pour accéder à cette fonctionnalité, vous devez avoir acheté le module complémentaire Composition d’audience fédérée .

>[!AVAILABILITY]
>
>Une fois que vous avez reçu la notification par e-mail de bienvenue d’Adobe, il peut s’écouler quelques heures de plus avant que l’interface ne soit mise à jour et que les fonctionnalités soient mises à votre disposition.

## Autorisations {#permissions}

Lorsque vous achetez le module complémentaire de composition d’audiences fédérées, un profil de produit est créé pour chaque environnement de test actif à ce moment-là. Ce profil de produit est créé dans l’Admin Console sous la carte de produit **Adobe Experience Platform** et suit cette convention d’affectation des noms : `ACP_FAC - <<SandboxName>> - admin.` Pour accéder à la composition d’audience fédérée pour un environnement de test spécifique, les utilisateurs doivent être ajoutés au profil de produit créé pour cet environnement de test.

Par exemple, si un nouvel environnement de test nommé &quot;fac-test&quot; est activé, un profil de produit correspondant &quot;ACP_FAC - fac-test - admin&quot; est créé. Pour accéder à la composition d’audiences fédérées avec cet environnement de test, les utilisateurs doivent être ajoutés à ce profil de produit.

## Listes autorisées des adresses IP {#ip}

Vos adresses IP doivent être ajoutées à la liste autorisée pour permettre l’accès à votre entrepôt de données et utiliser la composition d’audiences fédérées. Pour ajouter vos adresses IP à la liste autorisée, contactez votre représentant d’Adobe.

## Mécanismes de sécurisation et limitations {#fac-guardrails}

* La composition d’audience fédérée est compatible avec Privacy &amp; Security Shield et peut être utilisée dans tous les secteurs verticaux, à l’exception des secteurs de la santé. Actuellement, la composition d’audiences fédérées ne peut pas être sous licence pour les clients qui souhaitent ingérer des données d’intégrité. [En savoir plus](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Les droits, les limites de produit et les barrières aux performances répertoriés dans la [documentation Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} s’appliquent à ce module complémentaire.