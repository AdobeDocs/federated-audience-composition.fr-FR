---
audience: end-user
title: Vue d’ensemble des schémas
description: Découvrez comment créer et utiliser des schémas pour la composition d’audiences fédérées dans l’interface utilisateur de Adobe Experience Platform.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 35%
---
# Vue d’ensemble des schémas {#schemas}

>[!AVAILABILITY]
>
>La nouvelle expérience de schémas n’est disponible que pour certains clients. Pour plus d’informations, contactez l’Assistance clientèle d’Adobe.
>
>Si vous n’avez pas accès à la nouvelle expérience des schémas, lisez la [présentation des schémas](./schemas.md).
>
>Pour accéder aux schémas, vous devez disposer de l’une des autorisations suivantes :
>
>-**Gérer Le Schéma Fédéré**
>-**Affichage du schéma fédéré**
>
>Pour plus d’informations sur les autorisations requises, lisez le [guide du contrôle d’accès](/help/governance-privacy-security/access-control.md).

Un schéma est une représentation d’un tableau de votre base de données. Il s’agit d’un objet de l’application qui définit la manière dont les données sont liées aux tableaux de base de données.

En créant un schéma, vous pouvez définir une représentation de votre tableau dans la composition d’audiences fédérées Experience Platform :

* Donnez-lui un nom et une description simples à retenir pour simplifier la compréhension.
* Déterminez la visibilité de chaque champ en fonction de son utilisation réelle.
* Sélectionnez sa clé primaire afin de lier les schémas entre eux selon les besoins dans le [modèle de données](../data-modelling/models.md#data-model-start).

>[!CAUTION]
>
>Lors de la connexion de plusieurs sandbox à la même base de données, vous devez utiliser des schémas de travail distincts.

## Création d’un schéma {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="Gérer la configuration"
>abstract="Contenu vide temporaire."

Pour créer un schéma dans la composition d’audiences fédérées, sélectionnez **[!UICONTROL Schémas]** dans la section **[!UICONTROL Gestion des données]** de l’interface utilisateur d’Experience Platform. Dans l’interface utilisateur des schémas, sélectionnez **[!UICONTROL Créer un schéma]**.

![Les boutons Schémas et Créer un schéma sont tous deux mis en surbrillance dans l’interface utilisateur des schémas.](/help/data-modelling/assets/integrated/select-create-schema.png)

Une fois que la fenêtre contextuelle Créer un schéma s’affiche, sélectionnez **[!UICONTROL Relationnel]**, puis **[!UICONTROL Découvrir les schémas]** et **[!UICONTROL Suivant]** pour créer un schéma pour la composition d’audiences fédérées.

![Le bouton Découvrir les schémas est mis en surbrillance dans la fenêtre contextuelle Créer un schéma relationnel](/help/data-modelling/assets/integrated/select-discover-schemas.png).

La fenêtre contextuelle **[!UICONTROL Sélectionner une base de données fédérées]** s’affiche. Sur cette fenêtre contextuelle, vous pouvez sélectionner la [base de données source](/help/connections/home.md), puis **[!UICONTROL Suivant]**.

![La fenêtre contextuelle Sélectionner la base de données fédérée s’affiche.](/help/data-modelling/assets/integrated/select-federated-database.png)

## Définition du schéma {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="Clé composite"
>abstract="Clé de schéma composée de plusieurs colonnes. Marquez les colonnes à utiliser comme clé composite."

Après avoir choisi la base de données fédérée, vous pouvez maintenant définir votre schéma. L’écran **[!UICONTROL Ajouter des données]** s’affiche. Sur cette page, vous pouvez sélectionner **[!UICONTROL Ajouter une table]** pour choisir les tables à ajouter au schéma.

![Le bouton Ajouter un tableau est mis en surbrillance dans l’écran Ajouter des données.](/help/data-modelling/assets/integrated/select-add-table.png)

La fenêtre contextuelle **[!UICONTROL Sélectionner un tableau]** s’affiche. Dans cette fenêtre contextuelle, vous pouvez sélectionner les tableaux à utiliser pour créer le schéma.

![La fenêtre contextuelle Sélectionner un tableau s’affiche.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

Chaque tableau sélectionné génère un schéma avec les colonnes choisies. Pour chaque tableau, vous pouvez modifier l’étiquette du schéma, ajouter une description, renommer l’étiquette du champ, définir la visibilité de l’étiquette du champ et sélectionner la clé primaire du schéma.

![Les tableaux sélectionnés s’affichent dans la page Ajouter des données.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>Si vous choisissez **[!UICONTROL Clé composite]** mais ne sélectionnez qu’une seule clé à utiliser, celle-ci est traitée comme une clé primaire de schéma standard.

De plus, vous pouvez créer une clé composée de plusieurs colonnes de schéma. Sélectionnez **[!UICONTROL Clé composite]** et marquez les clés que vous souhaitez utiliser comme votre clé composite.

![Le bouton (bascule) Clé composite et les schémas sont sélectionnés.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

Une fois la configuration terminée, sélectionnez **[!UICONTROL Terminé]** pour terminer la création du schéma.

## Modifier un schéma {#schema-edit}

Pour modifier un schéma, cliquez sur l’icône ![des points de suspension](/help/assets/icons/more.png) en regard du schéma précédemment créé sur la page **Schémas**, puis sur **[!UICONTROL Modifier]**.

![Le bouton Modifier le schéma est mis en surbrillance.](/help/data-modelling/assets/integrated/edit-schema.png)

Dans la fenêtre **[!UICONTROL Modifier le schéma]**, l’éditeur de schémas s’affiche. Pour plus d’informations sur l’utilisation de l’éditeur de schémas, consultez le [guide de l’interface utilisateur des schémas](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#customize-schema).

![L’éditeur de schémas s’affiche.](/help/data-modelling/assets/integrated/schema-editor.png)

### Modifier les relations {#relationship-edit}

Pour modifier les relations d’un schéma, sélectionnez **[!UICONTROL Afficher le diagramme d’entité]** dans l’éditeur de schémas.

![Le bouton Afficher le diagramme d&#39;entité est mis en surbrillance.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

La page du diagramme d’entités s’affiche. Sur cette page, vous pouvez créer des liens pour établir des relations entre vos schémas.

![Le diagramme d’entité s’affiche.](/help/data-modelling/assets/integrated/entity-diagram.png)

Pour plus d’informations sur la création de liens, consultez l’onglet Vue de la zone de travail de la [présentation des modèles de données](/help/data-modelling/models.md#data-model-links).

## Prévisualiser les données dans un schéma {#schema-preview}

Pour prévisualiser les données dans le tableau représenté par votre schéma, accédez à la section **[!UICONTROL Jeux de données]**, puis sélectionnez **[!UICONTROL Parcourir]**.

![Les boutons Jeux de données et Parcourir sont mis en surbrillance.](/help/data-modelling/assets/integrated/datasets-browse.png)

Sélectionnez les ![points de suspension](/help/assets/icons/more.png), puis **[!UICONTROL Aperçu du jeu de données]** pour afficher un aperçu des données dans le schéma.

![Le bouton Prévisualiser le jeu de données est mis en surbrillance.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## Actualiser un schéma {#schema-refresh}

Les tableaux d’une base de données fédérée peuvent être mis à jour, ajoutés ou supprimés. Dans de tels cas, vous devez actualiser le schéma dans Adobe Experience Platform pour vous aligner sur les dernières modifications. Pour actualiser le schéma, sélectionnez le bouton **[!UICONTROL Plus]**, puis **[!UICONTROL Gérer la configuration]**.

![Le bouton Gérer la configuration est mis en surbrillance.](/help/data-modelling/assets/integrated/manage-configuration.png)

La fenêtre contextuelle **[!UICONTROL Modifier la configuration]** s’affiche. Sélectionnez **[!UICONTROL Actualiser]** pour actualiser le schéma.

![Le bouton Actualiser le schéma est mis en surbrillance.](/help/data-modelling/assets/integrated/refresh-schema.png)

## Supprimer un schéma {#schema-delete}

Pour supprimer un schéma dans l’éditeur de schémas, sélectionnez **[!UICONTROL Plus]**, puis **[!UICONTROL Supprimer]**.

![Le bouton Supprimer le schéma est mis en surbrillance.](/help/data-modelling/assets/integrated/delete-schema.png)
