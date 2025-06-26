---
audience: end-user
title: Commencer avec les compositions
description: Découvrir comment démarrer avec les compositions
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 16%

---

# Commencer avec les compositions {#compositions}

>[!AVAILABILITY]
>
>Pour accéder aux compositions, vous devez disposer de l’une des autorisations suivantes :
>
>-**Gestion des compositions fédérées**
>>-**Affichage des compositions fédérées**
>
>Pour plus d’informations sur les autorisations requises, veuillez lire le [guide du contrôle d’accès](/help/governance-privacy-security/access-control.md).

La composition d’audience fédérée vous permet de créer des compositions, où vous pouvez exploiter diverses activités dans une zone de travail visuelle pour créer des audiences. Une fois votre composition créée, les audiences obtenues sont enregistrées dans Adobe Experience Platform et peuvent être utilisées dans les destinations Experience Platform et Adobe Journey Optimizer pour cibler les clients.

![Un exemple de workflow de composition s’affiche dans la composition d’audiences fédérées.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Accéder aux compositions et les gérer {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Compositions"
>abstract="Dans cet écran, vous pouvez accéder à la liste complète des compositions, vérifier leur statut actuel, les dates de dernière exécution et de prochaine exécution, et créer une composition."

Les compositions sont accessibles à partir du menu Adobe Experience Platform **[!UICONTROL Audiences]**, dans l’onglet **[!UICONTROL Compositions fédérées]** de la section **[!UICONTROL Clients]**.

Dans cet écran, vous pouvez accéder aux compositions existantes ou en créer de nouvelles. Vous pouvez également dupliquer ou supprimer une composition existante en sélectionnant le bouton ![trois points de suspension](/help/assets/icons/more.png) en regard de son nom.

Vous pouvez également afficher des informations sur les compositions, notamment le nom, le statut, le créateur et la date de dernière modification.

| État | Description |
| ------ | ----------- |
| **[!UICONTROL Brouillon]** | La composition a été créée et enregistrée. |
| **[!UICONTROL En cours]** | La composition a été exécutée et est en cours d’exécution. |
| **[!UICONTROL Arrêté]** | L’exécution de la composition est terminée et s’est arrêtée. |
| **[!UICONTROL En pause]** | L’exécution de la composition a été suspendue. |
| **[!UICONTROL Erroné]** | L’exécution de la composition a rencontré une erreur. Pour afficher plus d’informations sur l’erreur, ouvrez la composition et accédez aux journaux. |

Vous pouvez apprendre à démarrer ou arrêter une composition dans le guide de [démarrage et surveillance de la composition](./start-monitor-composition.md).

![Une liste des compositions disponibles s’affiche.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

Pour affiner la liste et trouver la composition que vous recherchez, vous pouvez effectuer une recherche dans la liste et filtrer les compositions selon leurs statuts ou leurs dates de dernier traitement.

Vous pouvez également personnaliser la liste en ajoutant ou en supprimant des colonnes. Pour ce faire, sélectionnez le bouton **[!UICONTROL Configurer les colonnes]** et ajoutez ou supprimez les colonnes de sortie de votre choix.

![Une liste des colonnes disponibles que vous pouvez ajouter à la page de navigation des compositions s’affiche.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### Appliquer les libellés d’accès {#access-labels}

Pour appliquer des libellés d’accès à une composition spécifique, sélectionnez la composition, puis **[!UICONTROL Gérer l’accès]**.

![Le bouton « Gérer l’accès » est mis en surbrillance dans la zone de travail de composition.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

La fenêtre contextuelle **[!UICONTROL Gérer l’accès]** s’affiche. Sur cette page, vous pouvez appliquer les libellés de gouvernance de l’accès et des données applicables à votre composition.

![ La fenêtre contextuelle Gérer l’accès s’affiche. Vous voyez ici une liste de tous les libellés disponibles que vous pouvez appliquer à la composition.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| Type de libellé | Description |
| ---------- | ----------- |
| Étiquettes Contrat | Les libellés de contrat (libellés « C ») sont utilisés pour classer les données contenant des obligations contractuelles ou liées aux politiques de gouvernance des données de votre entreprise. |
| Étiquettes Identité | Les libellés d’identité (libellés « I ») sont utilisés pour classer les données permettant d’identifier ou de contacter une personne spécifique. |
| Étiquettes Sensibles | Les libellés sensibles (libellés « S ») sont utilisés pour vous catégoriser et/ou votre organisation considère comme sensibles. |
| Libellés de réseau partenaire | Les libellés d’écosystème partenaire servent à catégoriser les données provenant de sources externes à votre organisation. |

Pour plus d’informations sur l’accès et les libellés de gouvernance des données, consultez le [glossaire des libellés d’utilisation des données](https://experienceleague.adobe.com/en/docs/experience-platform/data-governance/labels/reference).

## Étapes suivantes

Après lecture de ce guide, vous avez appris à accéder à vos compositions, à les gérer et à en créer des libellés d’accès. Pour plus d’informations sur l’utilisation des audiences dans leur ensemble, veuillez lire le [guide des audiences](../start/audiences.md).
