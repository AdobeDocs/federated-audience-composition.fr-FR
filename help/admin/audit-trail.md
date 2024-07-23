---
audience: end-user
title: Commencer avec le journal d’audit
description: Découvrez comment surveiller vos bases de données avec le journal d’audit
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 0208da1a1897f166db9124ed6b014828fbe17484
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 69%

---

# Commencer avec le journal d’audit {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Journal d’audit"
>abstract="La fonctionnalité de journal d’audit fournit un enregistrement détaillé et chronologique de toutes les actions et tous les événements qui ont été réalisés en temps réel sur votre environnement."

La fonctionnalité Suivi fournit un enregistrement détaillé et chronologique de toutes les actions et tous les événements qui ont été réalisés dans votre environnement en temps réel.

La fonction **[!UICONTROL Suivi]** enregistre constamment en temps réel un journal détaillé des actions et événements qui se produisent dans l’instance Adobe de composition fédérée. Elle offre une méthode pratique d’accès à un enregistrement chronologique des données, en répondant à des requêtes telles que : le statut des workflows, les dernières personnes qui les modifient ou les activités effectuées par les utilisateurs et utilisatrices au sein de l’instance.

+++ En savoir plus sur les entités disponibles du journal d’audit

* Le **Suivi des schémas Source** vous permet de surveiller les activités et les modifications récentes apportées à vos schémas dans l’instance Adobe Federated Audience Composition.

  Pour plus d&#39;informations sur les schémas, consultez cette [page](../customer/schemas.md).

* Le **Journal d’audit des workflows** permet de suivre les activités et les modifications récentes apportées aux workflows, y compris leurs statuts actuels, telles que :

   * Démarrer
   * Pause
   * Arrêter
   * Redémarrer
   * Nettoyer qui correspond à l’action Purge de l’historique
   * Simuler qui correspond à l’action Démarrer en mode simulation
   * Réveiller qui correspond à l’action Traitement anticipé des tâches en attente
   * Arrêt inconditionnel

  Pour plus d’informations sur les workflows, consultez [cette page](../compositions/gs-compositions.md).

* **Compte externe** vous permet de vérifier les modifications apportées aux comptes externes dans l’instance Composition d’audience Adobe.

  Pour plus d’informations sur les comptes externes, consultez cette [page](../connections/federated-db.md).

+++

## Accéder au journal d’audit {#accessing-audit-trail}

Pour accéder au **[!UICONTROL journal d’audit]** de votre instance, procédez comme suit :

1. Dans le menu **[!UICONTROL Données fédérées]**, sélectionnez **[!UICONTROL Suivi]**.

1. La fenêtre **[!UICONTROL Journal d’audit]** s’ouvre avec la liste de vos entités. L’interface d’utilisation d’Adobe Campaign Web réalise l’audit des actions de création, de modification et de suppression pour les workflows, les options, les diffusions et les schémas.

   ![](assets/audit_trail.png)

1. La fenêtre **[!UICONTROL Entité d’audit]** vous donne des informations plus détaillées sur l’entité choisie, telles que :

   * **[!UICONTROL Type]** : workflow, options, diffusions ou schémas.
   * **[!UICONTROL Entité]** : nom interne de vos activités.
   * **[!UICONTROL Modifié par]** : nom d’utilisateur de la dernière personne à avoir modifié cette entité.
   * **[!UICONTROL Action]** : dernière action réalisée sur cette entité (création, modification ou suppression).
   * **[!UICONTROL Date de modification]** : date de la dernière action effectuée sur cette entité.
