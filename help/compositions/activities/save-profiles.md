---
audience: end-user
title: Utiliser l’activité Enregistrer les profils
description: Découvrez comment utiliser l’activité Enregistrer des profils .
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 9%

---

# Enregistrement des profils {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Enregistrer les profils"
>abstract="L’activité Enregistrement des profils vous permet d’enrichir les profils Experience Platform en fédérant les données d’entrepôts externes, ce qui vous permet d’améliorer les profils client avec des attributs supplémentaires. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Sélectionner le schéma AEP"
>abstract="Choisissez le schéma Experience Platform des profils."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Sélection du champ d’identification du Principal"
>abstract="Sélectionnez l’identité du Principal à utiliser pour identifier les profils ciblés dans la base de données."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Sélectionner le schéma AEP"
>abstract="Choisissez le schéma Experience Platform des profils."

L&#39;activité **Enregistrer les profils** permet d&#39;enrichir les profils Adobe Experience Platform avec des données fédérées à partir d&#39;entrepôts externes.

Cette activité est généralement utilisée pour améliorer les profils client en apportant des attributs et des informations supplémentaires sans déplacer ou dupliquer physiquement les données dans la plateforme

## Configuration de l&#39;activité Enregistrement des profils {#save-profile-configuration}

Pour configurer l’activité **Enregistrement des profils**, procédez comme suit :

1. Ajoutez une activité **Enregistrer des profils** à votre composition.

   ![](../assets/save-profile.png)

1. Indiquez le libellé des profils à créer.

   >[!IMPORTANT]
   >
   >Le libellé de l’audience doit être unique dans le sandbox actuel. Il ne peut pas s’agir du même libellé qu’une audience existante.

1. Sélectionnez le schéma Adobe Experience Platform à utiliser.

   ![](../assets/save-profile-2.png)

1. Sélectionnez le champ Identité principale qui sera utilisé pour identifier les profils dans la base de données.

1. Pour réconcilier des attributs de données supplémentaires, cliquez sur **Ajouter des attributs**.

   Spécifiez ensuite le champ **Source** (données externes) et le champ **Destination** (champ de schéma) pour chaque attribut à mapper.

   ![](../assets/save-profile-3.png)

1. Une fois la configuration effectuée, cliquez sur **Démarrer**.
