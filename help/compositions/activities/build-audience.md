---
audience: end-user
title: Utilisation de l’activité Créer une audience
description: Découvrez comment utiliser l’activité Créer une audience
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 53%

---


# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="La variable **Créer une audience** l’activité vous permet de définir l’audience qui va entrer dans la composition."

La variable **Créer une audience** l’activité vous permet de définir l’audience qui va entrer dans la composition.

Pour définir la population de l’audience, vous pouvez :

<!--* Select an existing audience, created as a list in the client console.-->
* sélectionner une audience Adobe Experience Platform ;
* Créez une audience à l’aide du concepteur de requêtes en définissant et combinant des critères de filtrage.

La variable **Créer une audience** peut être placée au début de la composition ou après toute autre activité. N’importe quelle activité peut être placée après le **Créer une audience**.

## Configurer l’activité Créer une audience {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="Sélectionnez votre audience."

Pour configurer l’activité **Créer une audience**, procédez comme suit :

1. Ajoutez une activité **Créer une audience**.
1. Définissez un libellé.
1. Définissez le type d’audience : **Créer votre audience** ou **Lecture d’audience**.
1. Configurez votre audience en suivant les étapes présentées dans les onglets ci-dessous.

>[!BEGINTABS]

>[!TAB Créer votre propre (requête)]

Pour créer votre propre requête, procédez comme suit :

1. Sélectionnez **Créer la vôtre (requête)**.
1. Choisissez la **dimension de ciblage**. La dimension de ciblage permet de définir la population ciblée par l’opération : destinataires, bénéficiaires d’un contrat, opérateurs ou opératrices, abonné(e)s, etc. Par défaut, la cible est sélectionnée parmi les destinataires.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Cliquez sur **Continuer**.
1. Utilisez le modèle de requête pour définir votre requête, de la même manière que vous créez une audience lors de la conception d’un nouvel email. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Lecture d’audience]

Pour sélectionner une audience existante, procédez comme suit :

1. Sélectionnez **Lecture d’audience**.
1. Cliquez sur **Continuer**.
1. Sélectionnez votre audience, de la même manière que vous utilisez une audience lors de la conception d&#39;une nouvelle diffusion. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
