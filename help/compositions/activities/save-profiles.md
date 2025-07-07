---
audience: end-user
title: Utiliser l’activité Enregistrer les profils
description: Découvrir comment utiliser l’activité Enregistrer les profils
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: c76ef4b64a58d3d43e78b489a1efe1a97a8c09f7
workflow-type: ht
source-wordcount: '563'
ht-degree: 100%

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
>abstract="Les modes de mise à jour disponibles pour l’activité Enregistrer le profil incluent la mise à jour complète et la mise à jour incrémentielle."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Mise à jour complète"
>abstract="Le mode de mise à jour complète actualise l’ensemble complet des profils pour l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Mise à jour incrémentielle"
>abstract="Le mode de mise à jour incrémentielle actualise les profils qui ont été modifiés depuis la dernière exécution de l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Champ d’identité principale"
>abstract="Le champ Identité principale indique la source de vérité lors de la fusion des profils pour l’enrichissement."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Critères des champs obligatoires"
>abstract="Un champ obligatoire est un attribut qui doit être renseigné pour chaque profil ou enregistrement lors de l’export de données. S’il manque un champ obligatoire, l’export ne sera ni complet ni valide."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Critères du champ d’identité principale"
>abstract="Identifiant unique de chaque profil ou enregistrement. Cela permet de s’assurer que chaque enregistrement peut être reconnu et mis en correspondance, ce qui évite la duplication des données."

L’activité **[!UICONTROL Enregistrer les profils]** permet d’enrichir les profils Adobe Experience Platform avec des données fédérées à partir d’entrepôts de données externes.

Cette activité est généralement utilisée pour améliorer les profils clientèle en ajoutant des attributs et des informations sans déplacer ni dupliquer physiquement les données sur la plateforme.

## Configurer l’activité [!UICONTROL Enregistrer les profils] {#save-profile-configuration}

>[!IMPORTANT]
>
>L’activité **Enregistrer les profils** nécessite un jeu de données et un schéma activés pour les profils. Pour savoir comment activer votre jeu de données pour les profils, consultez le [guide d’utilisation des jeux de données](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}.
>
>En outre, si l’upsert n’est **pas** activé pour le jeu de données sélectionné, les données des profils seront **remplacées**. Pour savoir comment activer l’upsert pour vos jeux de données, consultez le [guide d’activation de l’upsert](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/enable-upsert).

Pour configurer l’activité **[!UICONTROL Enregistrer les profils]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Enregistrer les profils]** à votre composition.

   ![Le bouton Enregistrer les profils est mis en surbrillance dans les activités.](../assets/save-profiles/save-profiles.png){width="1500" zoomable="yes"}

1. Indiquez le libellé des profils à créer.

   >[!IMPORTANT]
   >
   >Le libellé de l’audience doit être unique dans le sandbox actuel. Il ne peut pas s’agir du même libellé qu’une audience existante.

1. Sélectionnez le schéma Adobe Experience Platform à utiliser.

   ![Les schémas disponibles s’affichent.](../assets/save-profiles/select-schema.png){width="1500" zoomable="yes"}

1. Sélectionnez le jeu de données dans lequel vous souhaitez enregistrer l’enrichissement.

   ![La liste déroulante du jeu de données est mise en surbrillance.](../assets/save-profiles/select-dataset.png){width="300" zoomable="yes"}

1. Après avoir sélectionné le jeu de données, vous pouvez voir le champ d’identité principale qui sera utilisé pour identifier les profils dans la base de données.

1. Sélectionnez **[!UICONTROL Ajouter des champs]** pour ajouter les champs d’identités principales et obligatoires.

   ![Le bouton Ajouter des champs est mis en surbrillance.](../assets/save-profiles/add-fields.png){width="300" zoomable="yes"}

   Vous pouvez spécifier le champ **Source** (données externes) et le champ **Destination** (champ de schéma) pour chaque attribut à mapper.

   ![Les champs Source et Destination sont mis en surbrillance, indiquant où créer le mappage entre les champs.](../assets/save-profiles/specify-mapping.png){width="300" zoomable="yes"}

1. Vous pouvez également spécifier le mode de mise à jour de l’enrichissement.

   ![Les types de mode de mise à jour s’affichent.](../assets/save-profiles/select-update-mode.png){width="300" zoomable="yes"}

   | Mode de mise à jour | Description |
   | ----------- | ----------- |
   | Mises à jour complètes | L’ensemble complet des profils est mis à jour pour l’enrichissement. |
   | Mises à jour incrémentielles | Seuls les profils qui ont été modifiés depuis la dernière exécution d’enrichissement sont mis à jour pour l’enrichissement. |

   Si vous sélectionnez [!UICONTROL Mises à jour incrémentielles], vous devez également choisir la date de dernière modification pour déterminer les données envoyées.

1. Une fois la configuration effectuée, sélectionnez **Démarrer**.
