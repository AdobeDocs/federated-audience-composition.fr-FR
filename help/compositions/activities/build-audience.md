---
audience: end-user
title: Utilisation de l’activité Créer une audience
description: Découvrez comment utiliser l’activité Créer une audience
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 54%

---


# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Créer une audience** permet de définir l’audience qui va entrer dans la composition."

L’activité **Créer une audience** permet de définir l’audience qui va entrer dans la composition.

Pour définir la population de l’audience, vous pouvez :

<!--* Select an existing audience, created as a list in the client console.-->
* sélectionner une audience Adobe Experience Platform ;
* Créez une audience à l’aide du concepteur de requêtes en définissant et combinant des critères de filtrage.

L&#39;activité **Créer l&#39;audience** peut être placée au début de la composition ou après toute autre activité. Toute activité peut être placée après la **création d’audience**.

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

Pour créer votre propre audience, procédez comme suit :

1. Sélectionnez **Créer une audience**.
1. Sélectionnez le **Schéma**, également appelé dimension de ciblage. Le schéma permet de définir la population ciblée par l&#39;opération : destinataires, bénéficiaires de contrats, opérateur, abonnés, etc. Par défaut, le schéma est sélectionné parmi les destinataires.
1. Cliquez sur **Continuer**.
1. Utilisez le modèle de requête pour définir votre requête. [Découvrez comment utiliser le concepteur de requêtes](../../query/query-modeler-overview.md).

>[!TAB Lecture d’audience]

Pour sélectionner une audience existante, procédez comme suit :

1. Sélectionnez **Lecture d’audience**.
1. Cliquez sur **Continuer**.
1. Sélectionnez votre audience.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
