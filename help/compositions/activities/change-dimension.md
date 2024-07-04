---
audience: end-user
title: Utilisation de l’activité Changement de dimension
description: Découvrez comment utiliser l’activité « Changement de dimension ».
source-git-commit: 44be467650e2329a1fce6c5adb6d266d94efd1e2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 44%

---


# Changement de dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Générer un complémentaire"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **Générer le complémentaire**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Activité Changement de dimension"
>abstract="Cette activité permet de modifier la dimension de ciblage, c&#39;est-à-dire le schéma, au fur et à mesure de la construction d&#39;une audience. Elle déplace l’axe en fonction du modèle de données et de la dimension d’entrée. Par exemple, vous pouvez passer de la dimension « contrats » à la dimension « clientèle »."

La variable **Changement de dimension** l&#39;activité permet de modifier la dimension de ciblage, c&#39;est-à-dire le schéma, au fur et à mesure de la construction de votre audience. Il déplace l’axe en fonction du modèle de données et de la dimension d’entrée. <!--[Learn more on targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **Changement de dimension**, procédez comme suit :

1. Ajouter un **Changement de dimension** à votre composition.

   ![](../assets/change-dimension.png)

1. Définissez la variable **Nouveau schéma**. Lors de la modification du schéma, tous les enregistrements sont conservés.

1. Exécutez la composition pour visualiser le résultat. Comparez les données des tableaux avant et après l’activité de changement de dimension et comparez la structure des tableaux de composition.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->



<!-- on parle de dimension, mais dans UI "schema", va rester comme ça ?-->