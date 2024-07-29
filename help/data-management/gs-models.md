---
audience: end-user
title: Commencer avec les modèles de données
description: Découvrez comment commencer avec les modèles de données
badge: label="Disponibilité limitée" type="Informative"
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: 2eef334ccc5b6c342a26dc452b76dc61f272ba84
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 17%

---

# Commencer avec les modèles de données {#data-model}

>[!CONTEXTUALHELP]
>id="dc_model_menu"
>title="Utiliser des modèles"
>abstract="Les schémas et les modèles de données sont répertoriés dans cet écran. Vous pouvez créer des schémas et des modèles de données à partir du bouton **Créer**."

>[!CONTEXTUALHELP]
>id="dc_datamodel_add_schema"
>title="Sélectionner des schémas"
>abstract="Sélectionnez les schémas du modèle de données."


>[!CONTEXTUALHELP]
>id="dc_datamodel_add_audience"
>title="Sélectionner une audience"
>abstract="Sélectionnez l’audience du modèle de données."

>[!CONTEXTUALHELP]
>id="dc_datamodel_properties"
>title="Propriétés du modèle de données"
>abstract="Saisissez le libellé du modèle de données."


## Qu’est-ce qu’un modèle de données ? {#data-model-start}

Un modèle de données est un ensemble de schémas, d’audiences et de liens entre eux. Il est utilisé pour fédérer les audiences avec des données de base de données.

En savoir plus sur les [schémas](../customer/schemas.md#schema-start).

En savoir plus sur [audiences](../start/audiences.md).

Par exemple, vous pouvez voir ci-dessous une représentation d’un modèle de données : les tables avec leur nom et les liens entre elles.

![](assets/datamodel.png){zoomable="yes"}

Dans la composition d’audiences fédérées, il est possible de créer de nombreux modèles de données.

Leur création dépendra du cas d&#39;utilisation : vous choisissez les tables nécessaires et vous les reliez selon vos besoins.

## Création d’un modèle de données {#data-model-create}

Pour créer un modèle de données, procédez comme suit :

1. Dans la section **[!UICONTROL FEDERATED DATA]** , accédez au lien **[!UICONTROL Modèles]** et accédez à l’onglet **[!UICONTROL Modèle de données]** .

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Cliquez sur le bouton **[!UICONTROL Créer un modèle de données]** pour définir le nom de votre modèle de données, puis cliquez sur le bouton **[!UICONTROL Créer]** .

   ![](assets/datamodel_name.png){zoomable="yes"}

1. Ajoutez ensuite les schémas, les audiences et les liens de votre modèle de données.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### Créer des liens {#data-model-links}

Pour créer des liens entre les tables de votre modèle de données, procédez comme suit :

1. Cliquez sur le menu **[!UICONTROL Créer un lien]** de l’une des tables, ou cliquez sur le bouton **[!UICONTROL Créer des liens]** et sélectionnez les 2 tables suivantes :

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Renseignez le formulaire donné pour définir le lien.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalité**

   * 1-N : une occurrence de la table source peut avoir plusieurs occurrences correspondantes de la table cible, mais une occurrence de la table cible peut avoir au plus une occurrence correspondante de la table source.

   * N-1 : une occurrence de la table cible peut avoir plusieurs occurrences correspondantes de la table source, mais une occurrence de la table source peut avoir au plus une occurrence correspondante de la table cible.

   * 1-1 : une occurrence de la table source peut avoir au plus une occurrence correspondante de la table cible.

Tous les liens définis pour votre modèle de données sont répertoriés comme ci-dessous :

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Vidéo - Comment {#data-model-video}

Découvrez comment créer un modèle de données dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
