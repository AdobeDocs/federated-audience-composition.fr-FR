---
audience: end-user
title: Utiliser les audiences
description: Découvrez comment utiliser les audiences
badge: label="Disponibilité limitée" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: 4b7645e45b68a7316d9ddc09af1a8253b4e4dd62
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 5%

---

# Utiliser les audiences {#gs-audiences}

La composition d’audience fédérée Experience Platform vous permet de [créer des compositions](../compositions/gs-compositions.md), où vous pouvez exploiter diverses activités dans une zone de travail visuelle pour créer des audiences et les stocker dans Adobe Experience Platform Audience Portal.

Vous pouvez ensuite activer ces audiences vers n’importe quelle destination prise en charge par Adobe Experience Platform.

## Création d’audiences à l’aide de compositions {#creation}

Pour créer des audiences à l’aide de la composition d’audiences fédérées, vous devez créer une composition comprenant une activité **[!UICONTROL Sauvegarde d’audience]** . Cette activité vous permet de sauvegarder l’audience dans Audience Portal et de sélectionner des champs de vos bases de données externes à inclure dans l’audience. [Découvrez comment configurer une activité Enregistrer une audience](../compositions/activities/save-audience.md).

Les audiences créées à l’aide de l’option Adobe la composition de données fédérées incluent tous les champs sélectionnés dans l’activité **[!UICONTROL Sauvegarde d’audience]** et sont stockées dans Audience Portal à côté de toutes les audiences Adobe Experience Platform.

Après l’exécution de la composition, l’audience obtenue est enregistrée dans Adobe Experience Platform en tant qu’audience externe et disponible dans la plateforme de données clients en temps réel d’Adobe et/ou Adobe Journey Optimizer.

Vous pouvez activer ces audiences vers n’importe quelle destination prise en charge par Adobe Experience Platform. [Découvrez comment utiliser les destinations](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home)

>[!NOTE]
>
>Les audiences créées à l’aide de l’option Adobe la composition d’audiences fédérées ne peuvent pas être modifiées. Pour apporter des modifications à l’une de ces audiences, vous devez créer une audience à l’aide d’une composition.

## Accès à votre audience dans Adobe Experience Platform {#access-audience}

Les audiences créées à l’aide de la composition d’audiences fédérées sont accessibles dans Audience Portal, accessible à partir du menu **Audiences** .

L’onglet **[!UICONTROL Parcourir]** répertorie toutes les audiences existantes stockées dans Adobe Experience Platform. Vous pouvez identifier les audiences de composition d’audiences fédérées dans la liste à l’aide de la colonne **[!UICONTROL Origine]** ou des filtres disponibles dans le volet de gauche.

![](assets/audiences-list.png)

Pour plus d’informations sur l’utilisation des audiences dans Adobe Experience Platform, consultez la [documentation d’Audience Portal](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal)

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->