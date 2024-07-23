---
audience: end-user
title: Commencer avec les schémas
description: Découvrez comment commencer avec les schémas
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: d168a67fb14644dab5d33e0e9d17c850d2a66262
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 20%

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


## Qu’est-ce qu’un schéma ? {#schema-start}

Un schéma est une représentation d’une table de votre base de données. Il s’agit d’un objet de l’application qui définit la manière dont les données sont liées aux tables de base de données.

En créant un schéma, vous pourrez manipuler une représentation de votre table dans FAC :

- Donnez-lui un nom et une description conviviaux pour simplifier la compréhension de l’utilisateur.
- Déterminer la visibilité de chaque champ en fonction de son utilisation réelle
- Sélectionnez sa clé primaire, afin de lier les schémas entre eux, selon les besoins dans le [modèle de données](../data-management/gs-models.md#data-model-start)

## Créer un schéma {#schema-create}

Pour créer des schémas dans FAC, procédez comme suit :
Dans la section **[!UICONTROL FEDERATED DATA]** , accédez au lien **[!UICONTROL Modèles]** . Vous y trouverez l’onglet **[!UICONTROL Schéma]** .
Cliquez sur le bouton **[!UICONTROL Créer un schéma]** .

![](assets/schema_create.png){zoomable="yes"}

Vous aurez accès à une nouvelle interface avec une liste déroulante dans laquelle vous trouverez
toutes les bases de données connectées à votre application. En savoir plus sur la [connexion à la base de données](../connections/connections.md#connections-fdb).
Sélectionnez votre base de données source dans la liste et cliquez sur l&#39;onglet **[!UICONTROL Ajouter des tables]**

![](assets/schema_tables.png){zoomable="yes"}

Vous aurez accès à la liste de toutes les tables de la base.

En ajoutant les tables, pour lesquelles vous souhaitez créer le schéma, vous avez accès à leurs champs comme ci-dessous.

![](assets/schema_fields.png){zoomable="yes"}

Pour chaque tableau, vous pouvez :

- renommer le libellé du schéma donné
- ajouter une description
- renommez tous les champs et décidez de leur visibilité.
- sélectionner la clé primaire du schéma

Par exemple, voici une table importée, juste après l’ajout :

![](assets/schema_lumaorder.png){zoomable="yes"}

Le schéma peut être défini comme suit :

![](assets/schema_lumaorders.png){zoomable="yes"}

## Modification d’un schéma {#schema-edit}

Pour éditer un schéma, cliquez sur son nom dans le dossier schémas. Vous aurez accès à la page ci-dessous.
Cliquez sur le bouton **[!UICONTROL Modifier]** .

![](assets/schema_edit.png){zoomable="yes"}

Vous aurez accès à la même possibilité que lors de la création du schéma :

- renommer le libellé du schéma donné
- ajouter une description
- renommez tous les champs et décidez de leur visibilité.
- sélectionner la clé primaire du schéma

![](assets/schema_edit_orders.png){zoomable="yes"}

## Aperçu des données dans un schéma {#schema-preview}

Pour prévisualiser les données de la table représentée par votre schéma, accédez à l&#39;onglet **[!UICONTROL Data]** comme ci-dessous.
Vous pouvez obtenir le nombre total d’enregistrements en cliquant sur le lien **[!UICONTROL Calculer]** .

![](assets/schema_data.png){zoomable="yes"}

Vous pouvez modifier la présentation des données en cliquant sur le bouton **[!UICONTROL Configurer les colonnes]** .

![](assets/schema_columns.png){zoomable="yes"}

## Supprimer un schéma {#schema-delete}

Pour supprimer un schéma, cliquez sur le bouton **[!UICONTROL Plus]**, puis **[!UICONTROL Supprimer]**.

![](assets/schema_delete.png){zoomable="yes"}
