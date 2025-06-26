---
audience: end-user
title: Utiliser l’activité Créer une audience
description: Découvrir comment utiliser l’activité Créer une audience
exl-id: 6fad3e49-e654-4f68-a125-50056c4ae980
source-git-commit: 2c706e8c7d7d282f8ef2f00875608f06e35ffdf8
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 94%

---

# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Créer une audience** permet de définir l’audience qui va entrer dans la composition."

L’activité **Créer une audience** permet de définir l’audience qui va entrer dans la composition. Pour définir la population de l’audience, vous pouvez :

* sélectionner une audience Adobe Experience Platform existante ;
* créer une audience à l’aide du concepteur de requête en définissant et en combinant des critères de filtrage.

## Configurer l’activité Créer une audience {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="Sélectionnez votre audience."

Pour configurer l’activité **Créer une audience**, procédez comme suit :

1. Ajoutez une activité **Créer une audience**.
1. Définissez un libellé.
1. Indiquez si vous souhaitez créer une audience ou en sélectionner une existante.
1. Configurez votre audience en suivant les étapes présentées dans les onglets ci-dessous.

>[!BEGINTABS]

>[!TAB Créer une audience]

Pour créer votre propre audience, procédez comme suit :

1. Sélectionnez **Créer une audience**.
1. Sélectionnez le **schéma**, ou dimension de ciblage. Le schéma permet de définir la population ciblée par l’opération : personnes destinataires, personnes bénéficiaires d’un contrat, opérateurs et opératrices, personnes abonnées, etc. Par défaut, le schéma est sélectionné parmi les personnes destinataires.

   ![](../assets/build-audience-create.png)

1. Cliquez sur **Continuer**.
1. Utilisez le concepteur de requête pour définir votre requête, puis confirmez. [Découvrir comment utiliser le concepteur de requête](../../query/query-modeler-overview.md)

>[!TAB Lecture d’audience]

Pour sélectionner une audience existante, procédez comme suit :

1. Sélectionnez **Lecture d’audience**.
1. Cliquez sur **Continuer**.

   ![](../assets/build-audience-read.png)

1. Sélectionnez votre audience.

>[!ENDTABS]

>[!NOTE]
>
>L’option **Générer une transition sortante** permet d’ajouter une transition sortante qui sera activée à la fin de l’exécution de l’activité si la population de l’audience est vide.

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
