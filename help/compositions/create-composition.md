---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 23%

---


# Création et exécution d’une composition {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Propriétés du workflow"
>abstract="Dans cet écran, choisissez le modèle à utiliser pour créer le workflow et indiquez un libellé. Développez la section Options supplémentaires pour configurer d’autres paramètres tels que le nom interne du workflow, son dossier, son fuseau horaire et le groupe de personnes responsables. Il est vivement recommandé de sélectionner un groupe de personnes responsables afin d’alerter les opérateurs et opératrices en cas d’erreur."

## Création de la composition {#create}

Pour créer une composition, procédez comme suit :

1. Accédez au **[!UICONTROL Audiences]** et sélectionnez **[!UICONTROL Compositions fédérées]** .

1. Cliquez sur le bouton **[!UICONTROL Création d’une composition]** bouton .

1. Dans le **[!UICONTROL Propriétés]** , spécifiez un libellé pour votre composition, puis cliquez sur **[!UICONTROL Créer]**.

1. Le canevas de composition s’affiche. Vous pouvez maintenant configurer votre composition en ajoutant autant d’activités que nécessaire en fonction de vos besoins avant de l’exécuter. Vous pouvez également configurer des paramètres supplémentaires tels que le libellé de la composition ou les options liées à la gestion des erreurs à l’exécution de la composition.

En savoir plus dans ces sections :

* [Configuration des paramètres de la composition](#starting-audience)
* [Ajouter des activités](#action-activities)
* [Exécuter la composition et suivre son exécution](#save)

## Configuration des paramètres de la composition {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Propriétés de composition"
>abstract="Cette section fournit des propriétés de composition génériques qui sont également accessibles lors de la création de la composition."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentation de composition"
>abstract="Par défaut, seules les tables de travail de la dernière exécution de la composition sont conservées. Vous pouvez activer cette option pour conserver les tables de travail à des fins de test. Il doit être utilisé. **only** sur les environnements de développement ou d’évaluation. Elle ne doit jamais être vérifiée dans un environnement de production."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Paramètres de gestion des erreurs"
>abstract="Dans cette section, vous pouvez définir comment gérer les erreurs au cours de l&#39;exécution. Vous pouvez choisir de suspendre le processus, d&#39;ignorer un certain nombre d&#39;erreurs ou d&#39;arrêter l&#39;exécution de la composition."

Cliquez sur le bouton **Paramètres** pour accéder aux options supplémentaires de la composition :

* **[!UICONTROL Libellé]**: modifiez le libellé de la composition.

* **[!UICONTROL Conserver le résultat des populations intermédiaires entre deux exécutions]**: par défaut, seules les tables de travail de la dernière exécution de la composition sont conservées. Les tables de travail des exécutions précédentes sont purgées par un workflow technique qui s’exécute quotidiennement.

  Si cette option est activée, les tables de travail seront conservées même après l&#39;exécution de la composition. Vous pouvez l’utiliser à des fins de test. N’utilisez donc cette option **que** dans les environnements de développement ou d’évaluation. Cette option ne doit jamais être activée dans un workflow de production.

* **[!UICONTROL Gestion des erreurs]**: cette section vous permet de définir les actions à effectuer en cas d&#39;erreur dans une activité de composition. Trois choix s’offrent à vous :

   * **[!UICONTROL Suspendre le processus]**: la composition est automatiquement suspendue et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, reprenez la composition à l’aide de la fonction **[!UICONTROL Reprendre]** des boutons.
   * **[!UICONTROL Ignorer]**: l’état de la tâche qui a déclenché l’erreur passe à **[!UICONTROL En échec]**, mais la composition conserve la propriété **[!UICONTROL Démarré]** statut.
   * **[!UICONTROL Abandonner le processus]**: la composition est automatiquement arrêtée et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, redémarrez la composition à l’aide de la fonction **[!UICONTROL Début]** bouton .

* **[!UICONTROL Erreurs consécutives]**: indiquez le nombre d’erreurs qui peuvent être ignorées avant l’arrêt du processus. Une fois ce nombre atteint, l’état de la composition passe à **[!UICONTROL En échec]**. Si la valeur de ce champ est 0, la composition ne sera jamais arrêtée, quel que soit le nombre d&#39;erreurs.

## Ajouter des activités {#activities}

Le canevas de composition vous permet de configurer pour ajouter autant d’activités que nécessaire dans la composition en fonction de vos besoins.

Pour ce faire, cliquez sur le bouton + sur le chemin de la composition, puis ajoutez l’activité souhaitée. Le volet de droite s’ouvre, vous permettant de configurer l’activité nouvellement ajoutée. [En savoir plus sur les activités dans les compositions et comment les configurer](../compositions/activities/about-activities.md)

Pour supprimer une activité de la zone de travail, sélectionnez-la et cliquez sur le bouton de suppression dans le volet de droite. Si l’activité que vous souhaitez supprimer est parente d’autres activités de la composition, un message s’affiche et vous permet d’indiquer si vous souhaitez supprimer uniquement l’activité sélectionnée ou toutes ses activités enfant.

## Exécuter la composition {#execute}

Une fois votre composition prête, cliquez sur le bouton **[!UICONTROL Début]** pour l’exécuter et enregistrer les audiences obtenues dans Adobe Experience Platform. &quot;Vous pouvez suivre l&#39;exécution du workflow à l&#39;aide de la fonction **Journaux** bouton . Trois onglets sont disponibles pour vous aider à surveiller l’exécution :

* **[!UICONTROL Journaux]**:
* **[!UICONTROL Tâche]**:
* **[!UICONTROL Variables]**:
