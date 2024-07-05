---
audience: end-user
title: Utilisation de l’activité Changement de dimension
description: Découvrez comment utiliser l’activité « Changement de dimension ».
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 29%

---


# Changement de dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Générer un complémentaire"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **Générer le complémentaire**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Activité Changement de dimension"
>abstract="Cette activité permet de modifier le schéma, également appelé dimension de ciblage, lors de la création d&#39;une audience. Il déplace l’axe en fonction du modèle de données et du schéma d’entrée. Par exemple, vous pouvez passer du schéma &quot;contrats&quot; au schéma &quot;clients&quot;."

La variable **Changement de dimension** l’activité vous permet de modifier le schéma, également appelé dimension de ciblage, lors de la création de votre audience. Il déplace l’axe en fonction du modèle de données et du schéma d’entrée.

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **Changement de dimension**, procédez comme suit :

1. Ajouter un **Changement de dimension** à votre composition.

   ![](../assets/change-dimension.png)

1. Définissez la variable **Nouveau schéma**. Lors de la modification du schéma, tous les enregistrements sont conservés.

1. Exécutez la composition pour visualiser le résultat. Comparer les données des tableaux avant et après l’événement **Changement de dimension** et comparer la structure des tables de composition.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->