---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
source-git-commit: 4a73702c99762a5e9ab73485fa46916b9c28fcc3
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 31%

---


# Démarrage et suivi de votre composition {#start-monitor}

Une fois que vous avez créé votre composition et conçu les tâches à effectuer dans la zone de travail, vous pouvez la lancer et contrôler son exécution.

## Démarrer la composition {#start}

Pour commencer une composition, cliquez sur le bouton **[!UICONTROL Début]** dans le coin supérieur droit de l’écran. Lorsque la composition est en cours d’exécution, chaque activité de la zone de travail est exécutée dans un ordre séquentiel, jusqu’à ce que la fin de la composition soit atteinte.

Vous pouvez suivre la progression des profils ciblés en temps réel à l’aide du flux visuel. Vous pouvez ainsi identifier rapidement le statut de chaque activité et le nombre de profils qu’elle contient.

![](assets/composition-visual-flow.png)

## Transitions de composition {#transitions}

Dans les compositions, les données transportées d&#39;une activité à l&#39;autre via les transitions sont stockées dans une table de travail temporaire. Ces données peuvent être affichées pour chaque transition. Pour cela, sélectionnez une transition pour ouvrir ses propriétés dans la partie droite de l’écran.

* Cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail.
* Cliquez sur **[!UICONTROL Aperçu des résultats]** pour visualiser les données véhiculées dans la transition sélectionnée.

![](assets/transition-preview.png)

## Surveiller l’exécution des activités {#activities}

Les indicateurs visuels situés dans le coin supérieur droit de chaque activité vous permettent de vérifier leur exécution :

| Indicateur visuel | Description |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’activité est en cours d’exécution. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’activité nécessite votre attention. Vous devez, par exemple, confirmer l’envoi d’une diffusion ou prendre une mesure nécessaire. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’activité a rencontré une erreur. Pour résoudre ce problème, ouvrez les journaux de composition pour plus d’informations. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’activité a été exécutée correctement. |

## Surveiller les logs et les tâches {#logs-tasks}

La surveillance des logs et des tâches de composition est une étape clé pour analyser vos compositions et s’assurer qu’elles s’exécutent correctement. Elles sont accessibles à partir du **[!UICONTROL Journaux]** qui est disponible dans la barre d’outils d’action et dans le volet des propriétés de chaque activité.

![](assets/logs-button.png)

La variable **[!UICONTROL Logs et tâches de composition]** fournit un historique de l’exécution de la composition, en enregistrant toutes les actions de l’utilisateur et les erreurs rencontrées.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

L&#39;historique est organisé en plusieurs onglets, présentés ci-dessous :

* La variable **[!UICONTROL Journal]** contient l&#39;historique d&#39;exécution de toutes les activités de composition. Il répertorie par ordre chronologique les opérations réalisées et les erreurs d’exécution.
* L’onglet **[!UICONTROL Tâches]** permet de voir le séquencement de l’exécution des activités. Le bouton situé à la fin de chaque tâche vous permet de répertorier les variables d’événements transmises par l’activité.
* La variable **[!UICONTROL Variables]** répertorie toutes les variables transmises dans la composition. Elle est disponible uniquement lors de l’accès aux journaux et aux tâches à partir du canevas de composition. Elle est désormais disponible lors de l’accès aux journaux à partir du volet des propriétés d’une activité.  <!-- à confirmer-->

![](assets/logs-tasks.png)

Dans tous les onglets, vous pouvez choisir les colonnes affichées et leur ordre, appliquer des filtres et utiliser le champ de recherche pour trouver rapidement les informations souhaitées.

## Commandes d’exécution de composition {#execution-commands}

La barre d’actions située dans le coin supérieur droit fournit des commandes qui vous permettent de gérer l’exécution de la composition.

![](assets/execution-actions.png)

Les actions disponibles sont les suivantes :

* **Début**: démarre l’exécution de la composition, qui prend ensuite en charge la fonction **En cours** statut. La composition est lancée et les activités initiales sont activées.

* **[!UICONTROL Reprendre]**: relance l’exécution de la composition qui avait été suspendue. La composition prend en charge la fonction **En cours** statut.

* **[!UICONTROL Pause]** l&#39;exécution de la composition, qui prend ensuite en charge **En pause** statut. Aucune nouvelle activité ne sera activée jusqu’à la prochaine reprise, mais les opérations en cours ne sont pas suspendues.

* **[!UICONTROL Arrêter]** une composition en cours d’exécution, qui prend alors en charge la fonction **Terminé** statut. Les opérations en cours sont interrompues si possible. Vous ne pouvez pas reprendre à partir de la composition à l’endroit où elle a été arrêtée.

* **Redémarrer**: arrête puis redémarre une composition. Dans la plupart des cas, cela vous permet de redémarrer plus rapidement, car l’arrêt prend un certain temps et l’événement **Début** n’est disponible que lorsque l’arrêt est effectif.