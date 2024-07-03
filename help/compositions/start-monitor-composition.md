---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 47%

---


# Démarrage et suivi de votre composition {#start-monitor}

Une fois que vous avez créé votre composition et conçu les tâches à effectuer dans la zone de travail, vous pouvez la lancer et contrôler son exécution.

## Démarrer la composition {#start}

Pour démarrer la composition, accédez à la **[!UICONTROL Compositions]** ou l&#39;opération associée, puis cliquez sur le bouton **[!UICONTROL Début]** dans le coin supérieur droit de la zone de travail.

Une fois la composition en cours d’exécution, chaque activité de la zone de travail est exécutée dans un ordre séquentiel, jusqu’à ce que la fin de la composition soit atteinte.

Vous pouvez suivre la progression des profils ciblés en temps réel à l’aide du flux visuel. Vous pouvez ainsi identifier rapidement le statut de chaque activité et le nombre de profils qu’elle contient.

## Transitions de composition {#transitions}

Dans les compositions, les données transportées d&#39;une activité à l&#39;autre via les transitions sont stockées dans une table de travail temporaire. Ces données peuvent être affichées pour chaque transition. Pour cela, sélectionnez une transition pour ouvrir ses propriétés dans la partie droite de l’écran.

* Cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail.
* Cliquez sur **[!UICONTROL Aperçu des résultats]** pour visualiser les données véhiculées dans la transition sélectionnée.

## Surveiller l’exécution des activités {#activities}

Les indicateurs visuels situés dans le coin supérieur droit de chaque activité vous permettent de vérifier leur exécution :

| Indicateur visuel | Description |
|-----|------------|
|  | L’activité est en cours d’exécution. |
|  | L’activité nécessite votre attention. Vous devez, par exemple, confirmer l’envoi d’une diffusion ou prendre une mesure nécessaire. |
|  | L’activité a rencontré une erreur. Pour résoudre ce problème, ouvrez les journaux de composition pour plus d’informations. |
|  | L’activité a été exécutée correctement. |

## Surveiller les logs et les tâches {#logs-tasks}

La surveillance des logs et des tâches de composition est une étape clé pour analyser vos compositions et s’assurer qu’elles s’exécutent correctement. Les logs sont accessibles à partir de l’icône **[!UICONTROL Logs]**, située dans la barre d’outils d’actions et dans le volet des propriétés de chaque activité.

La variable **[!UICONTROL Logs et tâches]** fournit un historique de l’exécution de la composition, en enregistrant toutes les actions de l’utilisateur et les erreurs rencontrées. Cet historique est conservé pendant la durée spécifiée dans la composition. [options d’exécution](composition-settings.md). Pendant cette durée, tous les messages sont enregistrés, même après un redémarrage de la composition. Si vous ne souhaitez pas conserver les messages d’une exécution précédente, cliquez sur le bouton **[!UICONTROL Purger l’historique]**.

Deux types d’informations sont disponibles :

* La variable **[!UICONTROL Journal]** contient l&#39;historique d&#39;exécution de toutes les activités de composition. Il répertorie par ordre chronologique les opérations réalisées et les erreurs d’exécution.
* L’onglet **[!UICONTROL Tâches]** permet de voir le séquencement de l’exécution des activités.

Sous les deux onglets, vous pouvez choisir les colonnes à afficher et leur ordre, appliquer des filtres et trouver rapidement des informations à l’aide du champ de recherche.

## Commandes d’exécution de composition {#execution-commands}

La barre d’actions située dans le coin supérieur droit fournit des commandes qui vous permettent de gérer l’exécution de la composition. Vous pouvez :

* **[!UICONTROL Début]** / **[!UICONTROL Reprendre]** l&#39;exécution de la composition, qui prend alors le statut En cours . Si la composition a été mise en pause, elle reprend, sinon elle est lancée et les activités initiales sont alors activées.

* **[!UICONTROL Pause]** l&#39;exécution de la composition, qui prend alors le statut En pause . Aucune nouvelle activité ne sera activée jusqu’à la prochaine reprise, mais les opérations en cours ne sont pas suspendues.

* **[!UICONTROL Arrêter]** une composition en cours d’exécution, qui prend alors le statut Terminé . Les opérations en cours sont interrompues si possible. Vous ne pouvez pas reprendre à partir de la composition à l’endroit où elle a été arrêtée.
