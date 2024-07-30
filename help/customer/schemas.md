---
audience: end-user
title: Commencer avec les schémas
description: Découvrez comment commencer avec les schémas
badge: label="Disponibilité limitée" type="Informative"
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 741f73443471872025f63142e627ca1ed5b428ae
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 23%

---

# Commencer avec les schémas {#schemas}

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Sélectionner des tables"
>abstract="Sélectionnez les tables à ajouter au modèle de données."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Clé"
>abstract="Sélectionnez une clé pour la réconciliation des données."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Nom du schéma"
>abstract="Saisissez le nom du schéma."


>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Description du schéma"
>abstract="La description du schéma répertorie les colonnes, les types et les libellés. Vous pouvez également vérifier la clé de réconciliation du schéma. Pour mettre à jour la définition du schéma, cliquez sur l’icône représentant un crayon."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Sélectionner la base de données source à filtrer"
>abstract="Vous pouvez filtrer les schémas en fonction de leur source. Sélectionnez une ou plusieurs bases de données fédérées pour afficher leurs schémas."

## Qu’est-ce qu’un schéma ? {#schema-start}

Un schéma est une représentation d’une table de votre base de données. Il s’agit d’un objet de l’application qui définit la manière dont les données sont liées aux tables de base de données.

En créant un schéma, vous pouvez définir une représentation de votre table dans Composition d’audience fédérée Experience Platform :

* Donnez-lui un nom et une description conviviaux pour simplifier la compréhension de l’utilisateur.
* Déterminer la visibilité de chaque champ en fonction de leur utilisation réelle
* Sélectionnez sa clé primaire, afin de lier les schémas entre eux, selon les besoins dans le [modèle de données](../data-management/gs-models.md#data-model-start)

## Créer un schéma {#schema-create}

Pour créer des schémas dans la composition d’audiences fédérées, procédez comme suit :

1. Dans la section **[!UICONTROL FEDERATED DATA]** , accédez au lien **[!UICONTROL Modèles]** . Accédez à l’onglet **[!UICONTROL Schéma]** et cliquez sur le bouton **[!UICONTROL Créer un schéma]**.

   ![](assets/schema_create.png){zoomable="yes"}

   Cette étape permet d&#39;accéder à un nouvel écran avec une liste déroulante où se trouvent les bases de données connectées à votre environnement. Pour en savoir plus sur la connexion à la base de données, consultez [cette section](../connections/connections.md#connections-fdb).

1. Sélectionnez votre base de données source dans la liste, puis cliquez sur l’onglet **[!UICONTROL Ajouter des tables]** .

   ![](assets/schema_tables.png){zoomable="yes"}

   Vous pouvez alors voir la liste de toutes les tables de la base.

1. En ajoutant les tables pour lesquelles vous souhaitez créer le schéma, vous avez accès à leurs champs comme ci-dessous :

   ![](assets/schema_fields.png){zoomable="yes"}

   Pour chaque tableau, vous pouvez :

   * modifier le libellé du schéma ;
   * ajouter une description
   * renommez tous les champs et définissez leur visibilité.
   * sélectionner la clé primaire du schéma

   Par exemple, pour le tableau suivant importé :

   ![](assets/schema_lumaorder.png){zoomable="yes"}

   Le schéma peut être défini comme suit :

   ![](assets/schema_lumaorders.png){zoomable="yes"}

## Modification d’un schéma {#schema-edit}

Pour modifier un schéma :

1. Cliquez sur le nom de votre schéma dans le dossier des schémas.

1. Cliquez sur le bouton **[!UICONTROL Modifier]** .

   ![](assets/schema_edit.png){zoomable="yes"}

   Vous pouvez accéder aux mêmes options que lors de la [création d’un schéma](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Aperçu des données dans un schéma {#schema-preview}

Pour prévisualiser les données de la table représentées par votre schéma, accédez à l&#39;onglet **[!UICONTROL Data]** comme ci-dessous.

Cliquez sur le lien **[!UICONTROL Calculer]** pour prévisualiser le nombre total d&#39;enregistrements.

![](assets/schema_data.png){zoomable="yes"}

Cliquez sur le bouton **[!UICONTROL Configurer les colonnes]** pour modifier l’affichage des données.

![](assets/schema_columns.png){zoomable="yes"}

## Supprimer un schéma {#schema-delete}

Pour supprimer un schéma, cliquez sur le bouton **[!UICONTROL Plus]**, puis choisissez **[!UICONTROL Supprimer]**.

![](assets/schema_delete.png){zoomable="yes"}
