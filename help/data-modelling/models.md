---
audience: end-user
title: Commencer avec les modèles de données
description: Découvrir comment commencer avec les modèles de données
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: a91474bc1f552f5c5f84c028fd60bb7e1b8a4f24
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 98%

---


# Modèles - Aperçu

>[!AVAILABILITY]
>
>Pour accéder aux modèles de données, vous devez disposer de l’une des autorisations suivantes :
>
>-**Gestion du modèle de données fédérées**
>-**Affichage du modèle de données fédérées**
>
>Pour plus d’informations sur les autorisations requises, lisez le [guide du contrôle d’accès](/help/governance-privacy-security/access-control.md).

Un modèle de données désigne un ensemble de schémas et d’audiences, ainsi que les liens qui existent entre eux. Vous pouvez utiliser des modèles pour combiner les données de votre base de données dans vos audiences.

Dans la composition d’audiences fédérées, vous pouvez créer et gérer des modèles de données directement dans la vue Zone de travail. Cela inclut l’ajout de schémas et d’audiences, ainsi que la définition des liens entre eux en fonction de votre cas d’utilisation.

En savoir plus sur les [schémas](../data-modelling/schemas.md#schema-start) et les [audiences](../start/audiences.md).

Voici un exemple de représentation d’un modèle de données : les tables avec leur nom et les liens qui les relient.

![](assets/models/datamodel.png){zoomable="yes"}

## Créer un modèle de données {#data-model-create}

Pour créer un modèle de données, procédez comme suit :

1. Dans la section **[!UICONTROL Federated Data]**, accédez au menu **[!UICONTROL Modèles]**, puis à l’onglet **[!UICONTROL Modèle de données]**.

   Sélectionnez le bouton **[!UICONTROL Créer un modèle de données]**.

   ![](assets/models/datamodel_create.png){zoomable="yes"}

2. Définissez le nom de votre modèle de données, puis sélectionnez le bouton **[!UICONTROL Créer]**.

3. Dans le tableau de bord de votre modèle de données, sélectionnez **[!UICONTROL Ajouter des schémas]** pour choisir le schéma associé à votre modèle de données.

   ![](assets/models/datamodel_schemas.png){zoomable="yes"}

4. De plus, vous pouvez ajouter des audiences à votre modèle de données. Sélectionnez **[!UICONTROL Ajouter des audiences]** pour définir vos groupes cibles.

   ![](assets/models/datamodel-audiences.png){zoomable="yes"}

5. Établissez des connexions entre les tableaux de votre modèle de données pour garantir des relations de données précises. Pour plus d’informations, consultez la [section Créer des liens](#data-model-links).

6. Une fois la configuration terminée, sélectionnez **[!UICONTROL Enregistrer]** pour appliquer les modifications.

## Créer des liens {#data-model-links}

>[!NOTE]
>
>Si vous créez un lien avec plusieurs jointures, vous ne pouvez utiliser la même combinaison de schémas source et cible qu’une seule fois.

>[!BEGINTABS]

>[!TAB Vue Tableau]

Pour créer des liens entre les tableaux de votre modèle de données à partir de l’onglet Vue Tableau, procédez comme suit :

1. Sélectionnez l’![icône des points de suspension](/help/assets/icons/more.png) suivie de **[!UICONTROL Créer un lien]** en regard de l’un des tableaux, ou sélectionnez **[!UICONTROL Créer des liens]** dans la section **[!UICONTROL Liens]** :

   ![](assets/models/datamodel_createlinks.png){zoomable="yes"}

2. Renseignez le formulaire donné pour définir le lien.

   ![](assets/models/datamodel_link.png){zoomable="yes"}

   **Cardinalité**

   * **1-N** : à une occurrence du tableau source peuvent correspondre plusieurs occurrences du tableau cible, mais à une occurrence du tableau cible peut correspondre au plus une occurrence du tableau source.

   * **N-1** : à une occurrence du tableau cible peuvent correspondre plusieurs occurrences du tableau source, mais à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

   * **1-1** : à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

   Pour créer un lien à jointure multiple, sélectionnez l’icône plus. Vous pouvez désormais créer plusieurs jointures entre les champs de schéma.

   ![Le bouton Plus est mis en surbrillance, ce qui vous permet de créer un lien à jointure multiple pour le modèle.](assets/models/multi-join.png){zoomable="yes"}

Tous les liens définis pour votre modèle de données seront répertoriés comme ci-dessous :

![](assets/models/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Vue Zone de travail]

Pour créer des liens entre les tableaux de votre modèle de données à partir de l’onglet Vue Zone de travail, procédez comme suit :

1. Accédez à la vue Zone de travail de votre modèle de données et sélectionnez les deux tableaux à lier.

2. Sélectionnez le bouton ![](assets/models/do-not-localize/Smock_AddCircle_18_N.svg) en regard de la jointure source, puis faites glisser la flèche vers la jointure cible pour établir la connexion.

   ![](assets/models/datamodel.gif){zoomable="yes"}

3. Remplissez le formulaire donné pour définir le lien et sélectionnez **[!UICONTROL Appliquer]** une fois la configuration terminée.

   ![](assets/models/datamodel-canvas-1.png){zoomable="yes"}

   **Cardinalité**

   * **1-N** : à une occurrence du tableau source peuvent correspondre plusieurs occurrences du tableau cible, mais à une occurrence du tableau cible peut correspondre au plus une occurrence du tableau source.

   * **N-1** : à une occurrence du tableau cible peuvent correspondre plusieurs occurrences du tableau source, mais à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

   * **1-1** : à une occurrence du tableau source peut correspondre au plus une occurrence du tableau cible.

4. Tous les liens définis dans votre modèle de données sont représentés par des flèches dans la vue Zone de travail. Cliquez sur une flèche entre deux tableaux pour afficher les détails, apporter des modifications ou supprimer le lien selon les besoins.

   ![](assets/models/datamodel-canvas-2.png){zoomable="yes"}

5. Utilisez la barre d’outils pour personnaliser et ajuster la zone de travail.

   ![](assets/models/datamodel-canvas-3.png)

   * **[!UICONTROL Zoom avant]** : agrandissez la zone de travail pour afficher plus clairement les détails de votre modèle de données.
   * **[!UICONTROL Zoom arrière]** : réduisez la taille de la zone de travail pour obtenir une vue plus large de votre modèle de données.
   * **[!UICONTROL Ajuster la vue]** : ajustez le zoom pour qu’il s’adapte à l’ensemble des schémas et/ou audiences dans la zone visible.
   * **[!UICONTROL Activer/désactiver l’interactivité]** : activez ou désactivez l’interaction de la personne avec la zone de travail.
   * **[!UICONTROL Filtre]** : choisissez le schéma à afficher dans la zone de travail.
   * **[!UICONTROL Forcer la disposition automatique]** : organisez automatiquement les schémas et/ou les audiences pour une meilleure organisation.

>[!ENDTABS]

## Vidéo pratique {#data-model-video}

Découvrez comment créer un modèle de données dans cette vidéo :

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
