---
audience: end-user
title: Commencer avec les compositions
description: Découvrez comment commencer avec des compositions
source-git-commit: 0d6930b15be5013b57b8859dd3d21a5d3367ecae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 14%

---

# Commencer avec les compositions {#compositions}

## Qu’est-ce qu’une composition ? {#what}

La Composition des données d’Adobe vous permet de créer des compositions, dans lesquelles vous pouvez exploiter différentes activités (fractionner, exclure..) dans un canevas visuel pour créer des audiences. Une fois cette opération terminée, les audiences résultantes sont enregistrées dans Adobe Experience Platform avec les audiences existantes et peuvent être exploitées dans des destinations telles que Journey Optimizer pour cibler des clients.

![](assets/composition-example.png)

## Accéder aux compositions et les gérer {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Compositions"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des compositions, vérifier leur statut actuel, les dates de dernière exécution et de prochaine exécution, et créer une composition."

Les compositions sont accessibles à partir du menu **[!UICONTROL Audiences]** de Adobe Experience Platform, dans l’onglet **Compositions fédérées**.

Dans cet écran, vous pouvez créer de nouvelles compositions et accéder à celles existantes. Vous pouvez également dupliquer ou supprimer une composition existante en cliquant sur le bouton représentant des points de suspension en regard de son nom.

![](assets/compositions-list.png)

Pour affiner la liste et trouver facilement la composition que vous recherchez, vous pouvez rechercher la liste et filtrer les compositions selon leur statut ou leur date de dernier traitement.

Vous pouvez également personnaliser la liste en ajoutant ou en supprimant des colonnes. Pour ce faire, cliquez sur le bouton **Configurer les colonnes** s et ajoutez ou supprimez les colonnes de sortie de votre choix.

![](assets/compositions-columns.png)

## Statuts des compositions {#status}

Les compositions peuvent avoir plusieurs statuts :

* **[!UICONTROL Version préliminaire]** : la composition a été créée et enregistrée.
* **[!UICONTROL En cours]** : la composition a été exécutée et est en cours d’exécution.
* **[!UICONTROL Stoppé]** : l’exécution de la composition s’est arrêtée.
* **[!UICONTROL En pause]** : l’exécution de la composition a été suspendue.
* **[!UICONTROL En erreur]** : l’exécution de la composition a rencontré une erreur. Ouvrez la composition et accédez aux logs et tâches pour identifier l&#39;erreur et la résoudre.

Des informations détaillées sur le démarrage et le suivi d&#39;une composition sont disponibles dans [cette section](../compositions/start-monitor-composition.md).