---
audience: end-user
title: Commencer avec les modèles de données
description: Découvrir comment commencer avec les modèles de données
badge: label="Disponibilité limitée" type="Informative"
exl-id: 8f9e9895-dcd7-4718-8922-4f7fefe9ed94
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: ht
source-wordcount: '380'
ht-degree: 100%

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


## Qu’est-ce qu’un modèle de données ? {#data-model-start}

Un modèle de données désigne un ensemble de schémas et d’audiences, ainsi que les liens qui existent entre eux. Il est utilisé pour fédérer les audiences avec des données de base de données.

En savoir plus sur les [schémas](../customer/schemas.md#schema-start).

En savoir plus sur les [Audiences](../start/audiences.md).

Voici un exemple de représentation d’un modèle de données : les tableaux avec leur nom et les liens qui existent entre elles.

![](assets/datamodel.png){zoomable="yes"}

La composition d’audiences fédérées permet de créer de nombreux modèles de données.

Leur création dépend du cas d’utilisation, en ce que vous choisissez les tableaux nécessaires et les reliez selon vos besoins.

## Créer un modèle de données {#data-model-create}

Pour créer un modèle de données, procédez comme suit :

1. Dans la section **[!UICONTROL DONNÉES FÉDÉRÉES]**, accédez au lien **[!UICONTROL Modèles]**, puis à l’onglet **[!UICONTROL Modèle de données]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Cliquez sur le bouton **[!UICONTROL Créer un modèle de données]** pour nommer votre modèle de données, puis cliquez sur le bouton **[!UICONTROL Créer]**.

   ![](assets/datamodel_name.png){zoomable="yes"}

1. Ajoutez ensuite les schémas, les audiences et les liens de votre modèle de données.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

### Créer des liens {#data-model-links}

Pour créer des liens entre les tableaux de votre modèle de données, procédez comme suit :

1. Cliquez sur le menu **[!UICONTROL Créer un lien]** de l’une des tables ou sur le bouton **[!UICONTROL Créer des liens]**, puis sélectionnez les 2 tableaux suivants :

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Renseignez le formulaire donné pour définir le lien.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalité**

   * 1-N : à une occurrence du tableau source peuvent correspondre plusieurs occurrences du tableau cible, mais à une occurrence du tableau cible peut correspondre au plus une occurrence du tableau source.

   * N-1 : à une occurrence du tableau cible peuvent correspondre plusieurs occurrences du tableau source, mais à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

   * 1-1 : à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

Tous les liens définis pour votre modèle de données seront répertoriés comme ci-dessous :

![](assets/datamodel_alllinks.png){zoomable="yes"}

## Vidéo pratique {#data-model-video}

Découvrez comment créer un modèle de données dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
