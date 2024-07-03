---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 7%

---


# Configuration des paramètres de la composition {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Propriétés de composition"
>abstract="Cette section fournit des propriétés de composition génériques qui sont également accessibles lors de la création de la composition."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentation de composition"
>abstract="Par défaut, seules les tables de travail de la dernière exécution de la composition sont conservées. Vous pouvez activer cette option pour conserver les tables de travail à des fins de test. Il doit être utilisé. **only** sur les environnements de développement ou d’évaluation. Elle ne doit jamais être vérifiée dans un environnement de production."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Paramètres de gestion des erreurs"
>abstract="Dans cette section, vous pouvez définir comment gérer les erreurs au cours de l&#39;exécution. Vous pouvez choisir de suspendre le processus, d&#39;ignorer un certain nombre d&#39;erreurs ou d&#39;arrêter l&#39;exécution de la composition."

Lors de l’accès à une composition, vous pouvez accéder à des paramètres avancés qui vous permettent, par exemple, de définir le comportement de la composition en cas d’erreur ou de gérer le délai après lequel l’historique de la composition doit être purgé.

Pour accéder à d’autres options de votre composition, cliquez sur le **Paramètres** située au-dessus de la zone de travail.

![](assets/composition-create-settings.png)

Les paramètres disponibles sont les suivants :

* **[!UICONTROL Libellé]**: modifiez le libellé de la composition.

* **[!UICONTROL Conserver le résultat des populations intermédiaires entre deux exécutions]**: par défaut, seules les tables de travail de la dernière exécution de la composition sont conservées. Les tables de travail des exécutions précédentes sont purgées par une composition technique qui s’exécute quotidiennement.

  Si cette option est activée, les tables de travail seront conservées même après l&#39;exécution de la composition. Vous pouvez l’utiliser à des fins de test. N’utilisez donc cette option **que** dans les environnements de développement ou d’évaluation. Elle ne doit jamais être vérifiée dans une composition de production.

* **[!UICONTROL Gestion des erreurs]**: cette section vous permet de définir les actions à effectuer en cas d&#39;erreur dans une activité de composition. Trois choix s’offrent à vous :

   * **[!UICONTROL Suspendre le processus]**: la composition est automatiquement suspendue et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, reprenez la composition à l’aide de la fonction **[!UICONTROL Reprendre]** des boutons.
   * **[!UICONTROL Ignorer]**: l’état de la tâche qui a déclenché l’erreur passe à **[!UICONTROL En échec]**, mais la composition conserve la propriété **[!UICONTROL Démarré]** statut.
   * **[!UICONTROL Abandonner le processus]**: la composition est automatiquement arrêtée et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, redémarrez la composition à l’aide de la fonction **[!UICONTROL Début]** bouton .

* **[!UICONTROL Erreurs consécutives]**: indiquez le nombre d’erreurs qui peuvent être ignorées avant l’arrêt du processus. Une fois ce nombre atteint, l’état de la composition passe à **[!UICONTROL En échec]**. Si la valeur de ce champ est 0, la composition ne sera jamais arrêtée, quel que soit le nombre d&#39;erreurs.
