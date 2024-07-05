---
audience: end-user
title: Utilisation de l’activité Sauvegarde d’audience
description: Découvrez comment utiliser l’activité Sauvegarde d’audience
source-git-commit: 6b7a0ae164bdb09b1f5fc067a13e304eec9c5201
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 30%

---


# Enregistrer l’audience {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Enregistrer une audience"
>abstract="Utilisez cette activité pour mettre à jour une audience existante ou créer une nouvelle audience à partir de la population calculée en amont dans la composition. Les audiences créées sont ajoutées à la liste des audiences et sont disponibles dans le menu **Audiences**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Générer une transition sortante"
>abstract="Utilisez cette option pour ajouter une transition après l’activité **Enregistrer l’audience**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Champ Identité principale"
>abstract="Sélectionnez l’identité principale à utiliser pour les profils."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="En savoir plus dans la documentation de l’Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Espace de noms d’identité"
>abstract="Sélectionnez l’espace de noms à utiliser pour les profils."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces" text="En savoir plus dans la documentation de l’Experience Platform"

La variable **Sauvegarde d’audience** l&#39;activité permet de mettre à jour une audience existante ou de créer une nouvelle audience à partir de la population calculée en amont dans une composition. Les audiences créées sont ajoutées à la liste des audiences de l’application, disponible via le menu **Audiences**.

Cette activité est essentiellement utilisée pour conserver les groupes de population calculés dans la même composition, en les convertissant en audiences réutilisables. Connectez-la à d’autres activités de ciblage telles que **Créer une audience** ou **Combiner**.

## Configurer l’activité Enregistrer l’audience {#save-audience-configuration}

Pour configurer l’activité **Enregistrer l’audience**, procédez comme suit :

1. Ajouter un **Sauvegarde d’audience** à votre composition.

   ![](../assets/save-audience.png)

1. Indiquez le libellé de l’audience à créer.

1. Cliquez sur **Ajout du mappage d’audience** choisissez ensuite les champs d&#39;audience source et cible :

   * **Champ d’audience Source**:
   * **Champ d’audience cible**:

   Répétez l’opération pour ajouter autant de mappages d’audience que nécessaire.

1. Sélectionnez l&#39;identité principale et l&#39;espace de noms à utiliser pour identifier les profils ciblés dans la base de données :

   * **Champ d’identité du Principal**: sélectionnez le champ à utiliser pour identifier les profils. Par exemple, son adresse électronique ou son numéro de téléphone.
   * **Espace de noms d’identité**: sélectionnez l’espace de noms à utiliser pour identifier les profils, c’est-à-dire le type de données à utiliser comme clé d’identification. Par exemple, si l’adresse électronique a été sélectionnée comme champ d’identité principale, l’espace de noms d’identité **Email** doit être sélectionné. Si l’identifiant unique est le numéro de téléphone, l’espace de noms d’identité **Téléphone** doit être sélectionné.

Une fois la composition exécutée, l’audience obtenue est enregistrée dans Adobe Experience Platform. <!-- to check-->, et rendus accessibles dans le **Audiences** .

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
