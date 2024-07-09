---
audience: end-user
title: Utilisation de l'activité Requête incrémentale
description: Découvrez comment utiliser l’activité Requête incrémentale
hide: true
hidefromtoc: true
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 56%

---

# Requête incrémentale {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Requête incrémentale"
>abstract="La variable **Requête incrémentale** activité vous permet d’interroger la base de données à l’aide du modeleur Query. A chaque nouvelle exécution de cette activité, les résultats des exécutions précédentes sont exclus. Cela vous permet de ne cibler que les nouveaux éléments."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Historique des requêtes incrémentales"
>abstract="Historique des requêtes incrémentales"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Données traitées des requêtes incrémentales"
>abstract="Données traitées des requêtes incrémentales"

La variable **Requête incrémentale** activité vous permet d’interroger la base de données selon un calendrier précis. A chaque nouvelle exécution de cette activité, les résultats des exécutions précédentes sont exclus. Cela vous permet de ne cibler que les nouveaux éléments.

L&#39;activité **[!UICONTROL Requête incrémentale]** peut être utilisée dans plusieurs cas d&#39;utilisation type :

* segmentation d’individus afin de définir la cible d’un message, une audience, etc.
* Exporter des données. Par exemple, vous pouvez utiliser l’activité pour exporter régulièrement les nouveaux journaux dans des fichiers. Cela peut s’avérer utile si vous souhaitez utiliser les données de vos journaux dans des rapports externes ou des outils BI.

La population déjà ciblée par les exécutions précédentes est stockée dans la composition. Cela signifie que deux compositions démarrées à partir du même modèle ne partagent pas le même log. Toutefois, deux tâches basées sur la même requête incrémentale dans la même composition utilisent le même journal.

Si le résultat d&#39;une requête incrémentale est égal à 0 lors de l&#39;une de ses exécutions, la composition est suspendue jusqu&#39;à la prochaine exécution programmée de la requête. Les transitions et les activités qui suivent la requête incrémentale ne sont donc pas traitées avant l’exécution suivante.

## Configurer l’activité Requête incrémentale {#incremental-query-configuration}

Pour configurer l’activité **Requête incrémentale**, procédez comme suit :

1. Ajoutez un **Requête incrémentale** dans votre composition.

1. Dans la section **[!UICONTROL Audience]**, choisissez la **Dimension de ciblage** puis cliquez sur **[!UICONTROL Continuer]**.

   La dimension de ciblage permet de définir la population ciblée par l’opération : destinataires, bénéficiaires d’un contrat, opérateurs ou opératrices, abonné(e)s, etc. Par défaut, la cible est sélectionnée parmi les destinataires. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Utilisez le concepteur de requêtes pour définir votre requête, de la même manière que vous créez une audience lors de la conception d’un nouvel e-mail. [Découvrez comment utiliser le concepteur de requêtes](../../query/query-modeler-overview.md).

1. Dans la section **[!UICONTROL Données traitées]**, sélectionnez le mode d’incrémentation à utiliser :

   * **[!UICONTROL Exclure les résultats de l’exécution précédente]** : à chaque exécution de l’activité, les résultats des exécutions précédentes sont exclus.

     Les enregistrements déjà ciblés dans les exécutions précédentes peuvent être consignés dans un journal selon un nombre maximum de jours à partir du jour où ils ont été ciblés. Pour ce faire, utilisez le champ **[!UICONTROL Historique en jours]**. Si cette valeur est égale à zéro, les personnes destinataires ne sont jamais purgées du journal.

   * **[!UICONTROL Utiliser un champ de date]** : cette option permet d’exclure les résultats des exécutions précédentes en fonction d’un champ de date spécifique. Pour cela, choisissez le champ de date souhaité dans la liste des attributs disponibles pour la dimension de ciblage sélectionnée. Lors des prochaines exécutions de la composition, seules les données qui ont été modifiées ou créées après la date de la dernière exécution seront récupérées.

     Après la première exécution de la composition, la variable **[!UICONTROL Date de dernière exécution]** devient disponible. Il spécifie la date qui sera utilisée pour la prochaine exécution et est automatiquement mis à jour chaque fois que la composition est exécutée. Vous avez toujours la possibilité de remplacer cette valeur en en saisissant manuellement une nouvelle valeur afin qu’elle réponde à vos besoins.

   >[!NOTE]
   >
   >Le mode **[!UICONTROL Utiliser un champ date]** offre davantage de flexibilité selon le champ date sélectionné. Par exemple, si le champ spécifié correspond à une date de modification, le mode du champ date permet de récupérer les données récemment mises à jour, tandis que l&#39;autre mode exclut simplement les enregistrements déjà ciblés dans une exécution précédente, même s&#39;ils ont été modifiés depuis la dernière exécution de la composition.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
