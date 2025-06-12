---
audience: end-user
title: Utiliser l’activité Enregistrer les profils
description: Découvrir comment utiliser l’activité Enregistrer les profils
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 55%

---

# Enregistrer les profils {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Enregistrer les profils"
>abstract="L’activité Enregistrer les profils vous permet d’enrichir les profils Experience Platform en fédérant les données d’entrepôts externes, ce qui vous permet d’améliorer les profils clientèle avec des attributs supplémentaires. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Sélectionner le schéma Experience Platform"
>abstract="Choisissez le schéma Experience Platform pour les profils."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Sélectionner le champ d’identité principale"
>abstract="Sélectionnez l’identité principale à utiliser pour identifier les profils ciblés dans la base de données."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Sélectionner le schéma Experience Platform"
>abstract="Choisissez le schéma Experience Platform pour les profils."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Enregistrer le mode de mise à jour du profil"
>abstract="Les modes de mise à jour disponibles pour l’activité d’enregistrement de profil incluent la mise à jour complète et la mise à jour incrémentielle."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Mise à jour complète"
>abstract="Le mode de mise à jour complète met à jour l’ensemble complet des profils pour l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Mise à jour incrémentielle"
>abstract="Le mode de mise à jour incrémentielle met à jour les profils qui ont été modifiés depuis la dernière exécution de l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Champ d’identité principale"
>abstract="Le champ Identité principale indique la source de vérité lors de la fusion des profils pour l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Critères des champs obligatoires"
>abstract="Un champ obligatoire est un attribut qui doit être renseigné pour chaque profil ou enregistrement lors de l’exportation de données. Si un champ obligatoire est manquant, l’exportation ne sera pas terminée ou valide."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Critères des champs d’identité de Principal"
>abstract="Identifiant unique de chaque profil ou enregistrement. Cela permet de s’assurer que chaque enregistrement peut être distinctement reconnu et mis en correspondance, ce qui évite la duplication des données."

L’activité **Enregistrer les profils** permet d’enrichir les profils Adobe Experience Platform avec des données fédérées à partir d’entrepôts externes.

Cette activité est généralement utilisée pour améliorer les profils client en apportant des attributs et des informations supplémentaires sans déplacer ou dupliquer physiquement les données dans la plateforme.

## Configurer l’activité Enregistrer les profils {#save-profile-configuration}

Pour configurer l’activité **Enregistrer les profils**, procédez comme suit :

1. Ajoutez une activité **Enregistrer les profils** à votre composition.

   ![](../assets/save-profile.png)

1. Indiquez le libellé des profils à créer.

   >[!IMPORTANT]
   >
   >Le libellé de l’audience doit être unique dans le sandbox actuel. Il ne peut pas s’agir du même libellé qu’une audience existante.

1. Sélectionnez le schéma Adobe Experience Platform à utiliser.

   ![](../assets/save-profile-2.png)

1. Sélectionnez le champ d’identité principale qui sera utilisé pour identifier les profils dans la base de données.

1. Pour réconcilier des attributs de données supplémentaires, cliquez sur **Ajouter des attributs**.

   Spécifiez ensuite le champ **Source** (données externes) et le champ **Destination** (champ de schéma) pour chaque attribut à mapper.

   ![](../assets/save-profile-3.png)

1. Une fois la configuration effectuée, cliquez sur **Démarrer**.
