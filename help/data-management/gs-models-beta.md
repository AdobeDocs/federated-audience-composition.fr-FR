---
audience: end-user
title: Commencer avec les modèles de données
description: Découvrir comment commencer avec les modèles de données
hide: true
hidefromtoc: true
source-git-commit: c3025f4682696352dd5d0999268b4413befe1d66
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 26%

---

# Commencer avec les modèles de données {#data-model-beta}

>[!AVAILABILITY]
>
>Le modèle de données avec la vue Zone de travail est actuellement disponible en version bêta pour certains utilisateurs uniquement.

## Qu’est-ce qu’un modèle de données ? {#data-model-start}

Un modèle de données désigne un ensemble de schémas et d’audiences, ainsi que les liens qui existent entre eux. Il est utilisé pour fédérer les audiences avec des données de base de données.

En savoir plus sur les [schémas](../customer/schemas.md#schema-start) et [audiences](../start/audiences.md).

Voici un exemple de représentation d’un modèle de données : les tableaux avec leur nom et les liens qui existent entre elles.

![](assets/datamodel.png){zoomable="yes"}

La composition d’audiences fédérées permet de créer de nombreux modèles de données.

Leur création dépend du cas d’utilisation, en ce que vous choisissez les tableaux nécessaires et les reliez selon vos besoins.

## Créer un modèle de données {#data-model-create}

Pour créer un modèle de données, procédez comme suit :

1. Dans la section **[!UICONTROL Données fédérées]**, accédez au menu **[!UICONTROL Modèles]** et accédez à l’onglet **[!UICONTROL Modèle de données]**.

   Cliquez sur le bouton **[!UICONTROL Créer un modèle de données]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Définissez le nom de votre modèle de données, puis cliquez sur le bouton **[!UICONTROL Créer]**.

1. Dans le tableau de bord de votre modèle de données, cliquez sur **[!UICONTROL Ajouter des schémas]** pour choisir le schéma associé à votre modèle de données.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Cliquez sur **[!UICONTROL Ajouter des audiences]** pour définir vos groupes cibles.

1. Établissez des connexions entre les tables de votre modèle de données pour garantir des relations de données précises. [En savoir plus](#data-model-links)

1. Une fois la configuration terminée, cliquez sur **[!UICONTROL Enregistrer]** pour appliquer vos modifications.

## Créer des liens {#data-model-links}

>[!BEGINTABS]

>[!TAB Vue Tableau]

Pour créer des liens entre les tableaux de votre modèle de données à partir de l’onglet Vue Tableau , procédez comme suit :

1. Cliquez sur le menu **[!UICONTROL Créer un lien]** de l’une des tables ou sur le bouton **[!UICONTROL Créer des liens]**, puis sélectionnez les 2 tableaux suivants :

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Renseignez le formulaire donné pour définir le lien.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalité**

   * **1-N** : à une occurrence de la table source peuvent correspondre plusieurs occurrences de la table cible, mais à une occurrence de la table cible peut correspondre au plus une occurrence de la table source.

   * **N-1** : à une occurrence de la table cible peuvent correspondre plusieurs occurrences de la table source, mais à une occurrence de la table source peut correspondre au plus une occurrence de la table cible.

   * **1-1** : à une occurrence de la table source peut correspondre au plus une occurrence de la table cible.

Tous les liens définis pour votre modèle de données seront répertoriés comme ci-dessous :

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Vue Zone de travail]

Pour créer des liens entre les tableaux de votre modèle de données à partir de l’onglet Vue Zone de travail , procédez comme suit :

1. Accédez à la vue Zone de travail de votre modèle de données et sélectionnez les deux tables à lier

1. Cliquez sur le bouton ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) en regard de la jointure Source, puis faites glisser la flèche vers la jointure Target pour établir la connexion.

   ![](assets/datamodel.gif){zoomable="yes"}

1. Remplissez le formulaire donné pour définir le lien et cliquez sur **[!UICONTROL Appliquer]** une fois configuré.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **Cardinalité**

   * **1-N** : à une occurrence de la table source peuvent correspondre plusieurs occurrences de la table cible, mais à une occurrence de la table cible peut correspondre au plus une occurrence de la table source.

   * **N-1** : à une occurrence de la table cible peuvent correspondre plusieurs occurrences de la table source, mais à une occurrence de la table source peut correspondre au plus une occurrence de la table cible.

   * **1-1** : à une occurrence de la table source peut correspondre au plus une occurrence de la table cible.

1. Tous les liens définis dans votre modèle de données sont représentés par des flèches dans la vue de la zone de travail. Cliquez sur une flèche entre deux tableaux pour afficher les détails, apporter des modifications ou supprimer le lien selon les besoins.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

1. Utilisez la barre d’outils pour personnaliser et ajuster la zone de travail.

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL Zoom avant]** : agrandissez la zone de travail pour afficher plus clairement les détails de votre modèle de données.
   * **[!UICONTROL Zoom arrière]** : réduisez la taille de la zone de travail pour obtenir une vue plus large de votre modèle de données.
   * **[!UICONTROL Ajuster la vue]** : ajustez le zoom pour qu’il s’adapte à tous les schémas et/ou audiences dans la zone visible.
   * **[!UICONTROL Activer/désactiver l’interactivité]** : activez ou désactivez l’interaction de l’utilisateur avec la zone de travail.
   * **[!UICONTROL Filtre]** : choisissez le schéma à afficher dans la zone de travail.
   * **[!UICONTROL Forcer la disposition automatique]** : organiser automatiquement les schémas et/ou les audiences pour une meilleure organisation.

>[!ENDTABS]

## Vidéo pratique {#data-model-video}

Découvrez comment créer un modèle de données dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
