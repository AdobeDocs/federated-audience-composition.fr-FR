---
audience: end-user
title: Utiliser l’activité Planificateur
description: Découvrir comment utiliser l’activité Planificateur
exl-id: 3e8be2a2-2227-42f4-a512-b9e686ba0f66
source-git-commit: 8fa60d20dc574bbddc0106508d57a1cd3f3d3db8
workflow-type: ht
source-wordcount: '456'
ht-degree: 100%

---

# Planificateur {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Activité Planificateur"
>abstract="L’activité **Planificateur** vous permet de planifier le démarrage de la composition d’audiences. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité d’une composition."

L’activité **Planificateur** est une activité de **contrôle de flux**. Elle permet de planifier le démarrage de la composition. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité de la composition.

Si vous avez configuré une connexion à la destination de la composition d’audiences fédérées, vous pouvez utiliser cette activité pour envoyer des audiences Adobe Experience Platform à des fréquences régulières. [Découvrir comment enrichir les audiences Adobe Experience Platform avec des données externes](../../connections/destinations.md)

![](../assets/scheduler.png)

## Configurer l’activité Planificateur {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validité du planificateur"
>abstract="Vous pouvez définir une période de validité pour le planificateur. Elle peut être permanente (par défaut) ou valide jusqu’à une date spécifique."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Options du planificateur"
>abstract="Définissez la fréquence du planificateur. Il peut être exécuté à un moment précis, ou encore une ou plusieurs fois par jour, semaine ou mois."

Pour configurer l’activité **Planificateur**, procédez comme suit :

1. Ajoutez une activité **Plafinicateur** à votre composition.

1. Configurez la **Fréquence d’exécution** :

   * **Une seule fois** : la composition n’est exécutée qu’une seule fois.
   * **Quotidienne** : la composition est exécutée à une heure précise, une fois par jour.
   * **Plusieurs fois par jour** : la composition est exécutée de manières régulière plusieurs fois par jour. Vous pouvez configurer des exécutions à des heures et dates spécifiques ou périodiquement.

     >[!NOTE]
     >
     >Ne planifiez pas l’exécution d’une composition à une fréquence supérieure à toutes les 15 minutes, car cela peut nuire aux performances générales du système et créer des blocages dans la base de données.

   * **Hebdomadaire** : la composition est exécutée à un instant défini, une ou plusieurs fois par semaine.
   * **Mensuelle** : la composition est exécutée à un instant défini, une ou plusieurs fois par mois. Vous pouvez sélectionner les mois au cours desquels la composition doit être exécutée. Vous pouvez également configurer des exécutions un jour de semaine spécifié du mois, comme le deuxième mardi du mois.

1. Définissez les détails de l’exécution en fonction de la fréquence sélectionnée. Les champs de détail peuvent varier en fonction de la fréquence d’utilisation (heure, fréquence de répétition, jours spécifiques, etc.).

1. Cliquez sur **Prévisualiser les heures de lancement** pour vérifier le planning des dix prochaines exécutions de votre composition.

1. Définissez la période de validité du planificateur :

   * **Permanent (n’expire jamais)** : la composition est exécutée selon la fréquence définie, sans limite de période ou de nombre d’itérations.

   * **Période de validité** : la composition est exécutée selon la fréquence définie, jusqu’à une date spécifique. Vous devez spécifier les dates de début et de fin.

>[!NOTE]
>
>Pour démarrer immédiatement la composition, cliquez sur **Exécuter la tâche en attente** dans la barre d’actions supérieure du planificateur. Ce bouton n’est disponible que lorsque vous avez démarré la composition.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->
