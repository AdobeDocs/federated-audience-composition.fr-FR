---
audience: end-user
title: Utilisation de l’activité Sauvegarde d’audience
description: Découvrez comment utiliser l’activité Sauvegarde d’audience
badge: label="Disponibilité limitée" type="Informative"
exl-id: fa67b1ee-8de6-4a71-b597-ade3f5587a38
source-git-commit: 6aec8f5d9e8550ece2b50234d86ed59938f1b028
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 30%

---

# Enregistrer l’audience {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Enregistrer une audience"
>abstract="Utilisez cette activité pour créer une nouvelle audience à partir de la population calculée en amont dans la composition. Les audiences créées sont ajoutées à la liste des audiences et sont disponibles dans le menu **Audiences**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Générer une transition sortante"
>abstract="Utilisez cette option pour ajouter une transition après l’activité **Enregistrer l’audience**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Champ d’identité principale"
>abstract="Sélectionnez l’identité principale à utiliser pour les profils."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="En savoir plus dans la documentation d’Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Espace de noms d’identité"
>abstract="Sélectionnez l’espace de noms à utiliser pour les profils."
>additional-url="https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces" text="En savoir plus dans la documentation d’Experience Platform"

L&#39;activité **Sauvegarde d&#39;audience** permet de créer une nouvelle audience à partir de la population calculée en amont dans une composition. Les audiences créées sont ajoutées à la liste des audiences Adobe Experience Platform et sont disponibles via le menu **Audiences** . [Découvrez comment utiliser les audiences](../../start/audiences.md)

Cette activité est essentiellement utilisée pour conserver les groupes de population calculés dans la même composition, en les convertissant en audiences réutilisables. Connectez-la à d’autres activités de ciblage telles que **Créer une audience** ou **Combiner**.

## Configurer l’activité Enregistrer l’audience {#save-audience-configuration}

Pour configurer l’activité **Enregistrer l’audience**, procédez comme suit :

1. Ajoutez une activité **Sauvegarde d&#39;audience** à votre composition.

   ![](../assets/save-audience.png)

1. Indiquez le libellé de l’audience à créer.

   >[!IMPORTANT]
   >
   >Le libellé de l’audience doit être unique dans l’environnement de test actuel. Il ne peut pas s’agir du même libellé qu’une audience existante.

1. Utilisez la section Mappages d’audience pour sélectionner les champs que vous souhaitez apporter à l’audience nouvellement créée. Pour ce faire, cliquez sur **Ajouter le mappage d’audience** , puis sélectionnez les champs d’audience source et cible.

   Répétez l’opération pour ajouter autant de mappages d’audience que nécessaire.

1. Sélectionnez l&#39;identité principale et l&#39;espace de noms à utiliser pour identifier les profils ciblés dans la base de données :

   * **Champ d’identité de Principal** : sélectionnez le champ à utiliser pour identifier les profils. Par exemple, son adresse électronique ou son numéro de téléphone.
   * **Espace de noms d’identité** : sélectionnez l’espace de noms à utiliser pour identifier les profils, c’est-à-dire le type de données à utiliser comme clé d’identification. Par exemple, si l’adresse électronique a été sélectionnée comme champ d’identité principal, l’espace de noms d’identité **Email** doit être sélectionné. Si l’identifiant unique est le numéro de téléphone, l’espace de noms d’identité **Téléphone** doit être sélectionné.

Après l’exécution de la composition, l’audience obtenue est enregistrée dans Adobe Experience Platform et rendue accessible dans le menu **Audiences** . L’audience créée comprend tous les champs sélectionnés dans la section Mappages d’audience . Vous pouvez activer l’audience vers n’importe quelle destination prise en charge par Adobe Experience Platform.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
