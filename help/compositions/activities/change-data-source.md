---
audience: end-user
title: Activité Modifier la source de données
description: Découvrez comment utiliser l’activité Modifier la source de données pour modifier la source de données utilisée par votre composition, ce qui offre plus de flexibilité dans la gestion des données au sein d’une composition.
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 4d377c51150535e3d12f085b472e189818186163
workflow-type: ht
source-wordcount: '165'
ht-degree: 100%

---

# Modifier la source de données

>[!IMPORTANT]
>
>Les activités **[!UICONTROL Changement de dimension]** et **[!UICONTROL Modifier la source de données]** **ne doivent pas** être ajoutées sur une même ligne. Si vous devez utiliser les deux activités consécutivement, incluez une activité **[!UICONTROL Enrichissement]** entre les deux. Cela garantit une bonne exécution et évite les erreurs et conflits potentiels.

L’activité **[!UICONTROL Modifier la source de données]** permet de modifier la source de données utilisée par votre composition.

## Configuration {#configure}

Après avoir ajouté une activité **[!UICONTROL Modifier la source de données]** à la zone de travail, vous pouvez définir la source de données du workflow.

![L’option de source de données est mise en surbrillance dans l’espace de travail Composition d’audiences fédérées.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}{align="center"}

| Source | Description |
| ------ | ----------- |
| Compte externe FDA | Base de données cloud externe connectée à Adobe Campaign via la Composition d’audiences fédérées. |

Après avoir sélectionné **[!UICONTROL Compte externe FDA]**, vous pouvez choisir le compte externe auquel vous souhaitez vous connecter.

![La fenêtre contextuelle affichant les options du compte externe s’affiche.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}{align="center"}
