---
audience: end-user
title: Prise en main des compositions
description: Découvrez comment commencer avec des compositions
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 16%

---

# Prise en main des compositions {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Propriétés de composition"
>abstract="Cette section fournit des propriétés de composition génériques qui sont également accessibles lors de la création de la composition."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentation de composition"
>abstract="Par défaut, seules les tables de travail de la dernière exécution de la composition sont conservées. Vous pouvez activer cette option pour conserver les tables de travail à des fins de test. Il doit être utilisé. **only** sur les environnements de développement ou d’évaluation. Elle ne doit jamais être vérifiée dans un environnement de production."




## Qu&#39;est-ce qu&#39;une composition ? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Compositions"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des compositions, vérifier leur état actuel, les dates de dernière exécution/prochaine et créer une nouvelle composition."


## Paramètres de gestion des erreurs  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Paramètres de gestion des erreurs"
>abstract="Dans cette section, vous pouvez définir comment gérer les erreurs au cours de l&#39;exécution. Vous pouvez choisir de suspendre le processus, d&#39;ignorer un certain nombre d&#39;erreurs ou d&#39;arrêter l&#39;exécution de la composition."

* **[!UICONTROL Gestion des erreurs]**: ce champ vous permet de définir les actions à effectuer en cas d&#39;erreur dans une activité de composition.
Trois choix s’offrent à vous :

   * **[!UICONTROL Suspendre le processus]**: la composition est automatiquement suspendue et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, reprenez la composition à l’aide de la fonction **[!UICONTROL Reprendre]** des boutons.
   * **[!UICONTROL Ignorer]**: l’état de la tâche qui a déclenché l’erreur passe à **[!UICONTROL En échec]**, mais la composition conserve la propriété **[!UICONTROL Démarré]** statut.
   * **[!UICONTROL Abandonner le processus]**: la composition est automatiquement arrêtée et son état passe à **[!UICONTROL En échec]**. Une fois le problème résolu, redémarrez la composition à l’aide de la fonction **[!UICONTROL Début]** bouton .

* **[!UICONTROL Erreurs consécutives]** : ce champ est disponible lorsque la valeur **[!UICONTROL Ignorer]** est sélectionnée dans le champ **[!UICONTROL En cas d’erreur]**. Vous pouvez indiquer le nombre d’erreurs qui peuvent être ignorées avant l’arrêt du processus. Une fois ce nombre atteint, l’état de la composition passe à **[!UICONTROL En échec]**. Si la valeur de ce champ est 0, la composition ne sera jamais arrêtée, quel que soit le nombre d&#39;erreurs.
