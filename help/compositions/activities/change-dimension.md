---
audience: end-user
title: Utiliser l’activité Changement de dimension
description: Découvrir comment utiliser l’activité « Changement de dimension »
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 100%

---

# Changement de dimension {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Générer un complément"
>abstract="Vous pouvez générer une transition sortante supplémentaire avec la population restante, qui a été exclue en tant que doublon. Pour ce faire, activez l’option **[!UICONTROL Générer un complément]**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Activité Changement de dimension"
>abstract="Cette activité vous permet de modifier le schéma, ou dimension de ciblage, à mesure que vous créez une audience. Elle déplace l’axe en fonction du modèle de données et du schéma d’entrée. Par exemple, vous pouvez passer du schéma « contrats » au schéma « clientèle »."

L’activité **Changement de dimension** vous permet de modifier le schéma, ou dimension de ciblage, à mesure que vous créez une audience. Elle déplace l’axe en fonction du modèle de données et du schéma d’entrée.

## Configurer l’activité Changement de dimension {#configure}

Pour configurer l’activité **Changement de dimension**, procédez comme suit :

1. Ajoutez une activité **Changement de dimension** à votre composition.

   ![](../assets/change-dimension.png)

1. Définissez le **nouveau schéma**. Lors du changement de dimension, tous les enregistrements sont conservés.

1. Exécutez la composition pour visualiser le résultat. Comparez les données contenues dans les tableaux avant et après l’activité **Changement de dimension**, puis comparez la structure des tableaux de la composition.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

