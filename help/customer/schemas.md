---
audience: end-user
title: Commencer avec les schémas
description: Découvrir comment commencer avec les schémas
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 94%

---

# Commencer avec les schémas {#schemas}

>[!AVAILABILITY]
>
>Pour accéder aux schémas, vous devez disposer de l’une des autorisations suivantes :
>
>-**Gérer Le Schéma Fédéré**
>-**Afficher le schéma fédéré**
>
>Pour plus d’informations sur les autorisations requises, veuillez lire le [Guide d’accès à la composition d’audiences fédérées](/help/start/feature-access.md).

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Sélectionner des tableaux"
>abstract="Sélectionnez les tableaux à ajouter au modèle de données."

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

Un schéma est une représentation d’un tableau de votre base de données. Il s’agit d’un objet de l’application qui définit la manière dont les données sont liées aux tableaux de base de données.

En créant un schéma, vous pouvez définir une représentation de votre tableau dans la composition d’audiences fédérées Experience Platform :

* Donnez-lui un nom et une description simples à retenir pour simplifier la compréhension.
* Déterminez la visibilité de chaque champ en fonction de son utilisation réelle.
* Sélectionnez sa clé primaire afin de lier les schémas entre eux selon les besoins dans le [modèle de données](../data-management/gs-models.md#data-model-start).

>[!CAUTION]
>
>Lors de la connexion de plusieurs sandbox à une même base de données, vous devez utiliser des schémas de travail distincts.
>

## Créer un schéma {#schema-create}

Pour créer des schémas dans la composition d’audiences fédérées, procédez comme suit :

1. Dans la section **[!UICONTROL Federated Data]**, accédez au menu **[!UICONTROL Modèles]**. Accédez à l’onglet **[!UICONTROL Schéma]** et cliquez sur le bouton **[!UICONTROL Créer un schéma]**.

   ![](assets/schema_create.png){zoomable="yes"}

   Cette étape permet d’accéder à un nouvel écran avec une liste déroulante où se trouvent les bases de données connectées à votre environnement. En savoir plus sur la connexion de bases de données dans [cette section](../connections/connections.md#connections-fdb).

1. Sélectionnez votre base de données source dans la liste et cliquez sur **[!UICONTROL Suivant]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Vous aurez accès à la liste de tous les tableaux de la base de données.

1. Sélectionnez les tableaux pour lesquels créer un schéma.

1. Chaque tableau sélectionné génère un schéma avec les colonnes choisies. Configurez le schéma et ses colonnes selon vos besoins.

   ![](assets/schema_fields.png){zoomable="yes"}

   Pour chaque tableau, vous pouvez effectuer les actions suivantes :

   * Modifier le libellé du schéma
   * Ajouter une description
   * Renommer tous les champs et définir leur visibilité
   * Sélectionner la clé primaire du schéma

   Le schéma peut être défini comme suit :

   ![](assets/schema_example.png)

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Terminé]**.

## Modifier un schéma {#schema-edit}

Pour modifier un schéma, procédez comme suit :

1. Accédez au schéma créé précédemment.

1. Cliquez sur le bouton **[!UICONTROL Modifier]**.

   ![](assets/schema_edit.png){zoomable="yes"}

1. Dans la fenêtre **[!UICONTROL Modifier le schéma]**, vous pouvez accéder aux mêmes options que lors de la [création d’un schéma](#schema-create) et les configurer.

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Prévisualiser les données dans un schéma {#schema-preview}

Pour prévisualiser les données du tableau représenté par votre schéma, accédez à l’onglet **[!UICONTROL Données]** comme ci-dessous.

Cliquez sur le lien **[!UICONTROL Calculer]** pour prévisualiser le nombre total d’enregistrements.

![](assets/schema_data.png){zoomable="yes"}

Cliquez sur le bouton **[!UICONTROL Configurer les colonnes]** pour modifier l’affichage des données.

![](assets/schema_columns.png){zoomable="yes"}

## Actualiser un schéma {#schema-refresh}

Les tableaux d’une base de données fédérée peuvent être mis à jour, ajoutés ou supprimés. Dans de tels cas, vous devez actualiser le schéma dans Adobe Experience Platform pour vous aligner sur les dernières modifications. Pour ce faire, cliquez sur les trois points en regard du nom du schéma à mettre à jour et sélectionnez **Actualiser le schéma**.

Vous pouvez également mettre à jour la définition de schéma lors de sa modification.

![](assets/schema_refresh.png){zoomable="yes"}


## Supprimer un schéma {#schema-delete}

Pour supprimer un schéma, cliquez sur le bouton **[!UICONTROL Plus]**, puis sur **[!UICONTROL Supprimer]**.

![](assets/schema_delete.png){zoomable="yes"}
