---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 36%

---


# Orchestration des activités de composition {#activities}

Une fois que vous avez créé une composition, vous pouvez commencer à orchestrer les différentes tâches qu’elle exécutera. Pour ce faire, un canevas visuel vous permet de construire votre diagramme de composition d’audience. Dans ce diagramme, vous pouvez ajouter différentes activités et les enchaîner dans un ordre séquentiel.

## Ajouter des activités {#add}

A ce stade de la configuration, le diagramme s&#39;affiche avec une icône de départ, représentant le début de votre composition. Pour ajouter votre première activité, cliquez sur le bouton **+** associé à l’icône de démarrage.

La liste des activités pouvant être ajoutées au diagramme s’affiche. Les activités disponibles dépendent de votre position dans le diagramme de composition. Par exemple, lorsque vous ajoutez votre première activité, vous pouvez démarrer votre composition en ciblant une audience, en divisant le chemin de la composition, en configurant un planificateur pour retarder l’exécution de la composition ou en définissant une activité **Attente** pour retarder l’exécution de la composition. D’un autre côté, après une activité **Créer une audience** , vous pouvez affiner votre cible avec des activités de ciblage ou organiser le processus de composition avec des activités de contrôle de flux.

Une fois qu’une activité a été ajoutée au diagramme, un volet s’affiche à droite. Il vous permet de définir des paramètres spécifiques pour l’activité. Des informations détaillées sur la configuration de chacune des activités sont disponibles dans [cette section](activities/about-activities.md).

![](assets/composition-create-add.png)

Répétez ce processus pour ajouter autant d’activités que vous le souhaitez en fonction des tâches que votre composition doit exécuter. Vous pouvez également insérer une nouvelle activité entre deux activités. Pour ce faire, cliquez sur le bouton **+** sur la transition entre les activités, puis sélectionnez l’activité souhaitée et configurez-la dans le volet de droite.

>[!TIP]
>
>Vous pouvez personnaliser le nom des transitions entre chaque activité. Pour ce faire, sélectionnez la transition et modifiez son libellé dans le volet de droite.

## Barre d’outils de la zone de travail {#toolbar}

La barre d’outils située dans le coin supérieur droit de la zone de travail fournit des options pour manipuler facilement les activités et naviguer dans la zone de travail.

![](assets/canvas-toolbar.png)

Les actions disponibles sont les suivantes :

* **[!UICONTROL Multi selection]** : sélectionnez plusieurs activités pour les supprimer toutes en même temps ou copiez-les et collez-les. Consultez [cette section](#copy).
* **[!UICONTROL Faire pivoter]** : retournez la zone de travail verticalement.
* **[!UICONTROL Ajuster à l’écran]** : adaptez le niveau de zoom de la zone de travail à votre écran.
* **[!UICONTROL Zoom arrière]**/**[!UICONTROL Zoom avant]** : effectuez un zoom arrière ou avant dans la zone de travail.
* **[!UICONTROL Afficher la carte]** : ouvre un instantané de la zone de travail indiquant où vous vous trouvez.

## Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le volet des propriétés, ce qui vous permet d’effectuer plusieurs opérations.

![](assets/activity-actions.png)

Vous pouvez :

* **[!UICONTROL Supprimer]** l’activité à partir de la zone de travail.
* **[!UICONTROL Désactiver]/[!UICONTROL Activez]** l’activité. Lorsque la composition est exécutée, les activités désactivées et les activités suivantes situées sur le même chemin ne sont pas exécutées et la composition est arrêtée.
* **[!UICONTROL Pause]/[!UICONTROL Reprendre]** l’activité. Lorsque la composition est exécutée, elle s’arrête à l’activité suspendue. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.
* **[!UICONTROL Copiez]** l’activité pour la coller à un autre emplacement de la composition. Pour ce faire, cliquez sur le bouton **+** d&#39;une transition et sélectionnez **[!UICONTROL Paste X activity]**. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configurez les **[!UICONTROL options d&#39;exécution]** pour l&#39;activité sélectionnée. Développez la section ci-dessous pour en savoir plus sur les options disponibles.

  +++ Options d’exécution disponibles

  La section **[!UICONTROL Propriétés]** vous permet de configurer des paramètres génériques concernant l’exécution de l’activité :

   * **[!UICONTROL Exécution]** : définissez l’action à effectuer au démarrage de la fonction.
   * **[!UICONTROL Durée d’exécution maximale]** : spécifiez une durée de type &quot;30s&quot; ou &quot;1h&quot;. Si l’activité n’est pas terminée une fois cette durée écoulée, une alerte est déclenchée, Cela n’a aucun impact sur le fonctionnement de la composition.
   * **[!UICONTROL Fuseau horaire]** : sélectionnez le fuseau horaire de l’activité. La composition d’audiences fédérées vous permet de gérer les différences de temps entre plusieurs pays sur la même instance. La configuration appliquée est paramétrée lors de la création de l’instance.
   * **[!UICONTROL Affinité]** : force l’exécution de l’activité de composition sur une machine particulière. Pour cela, vous devez définir une ou plusieurs affinités pour l&#39;activité en question.
   * **[!UICONTROL Comportement]** : définissez la procédure à suivre en cas de tâches asynchrones.

  La section **[!UICONTROL Gestion des erreurs]** vous permet de spécifier l’action à effectuer si l’activité rencontre une erreur.

  La section **[!UICONTROL Script d&#39;initialisation]** vous permet d&#39;initialiser des variables ou de modifier des propriétés d&#39;activité. Cliquez sur le bouton **[!UICONTROL Modifier le code]** et saisissez l’extrait de code à exécuter. Le script est appelé lors de l’exécution de l’activité.

+++

* Accédez aux **Journaux et tâches** de l’activité.
