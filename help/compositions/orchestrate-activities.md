---
audience: end-user
title: Créer des compositions
description: Découvrir comment créer des compositions
exl-id: 7b9acfc0-99b6-4f83-b774-3652c811868c
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: ht
source-wordcount: '716'
ht-degree: 100%

---

# Orchestrer les activités de composition {#activities}

Une fois que vous avez créé une composition, vous pouvez commencer à orchestrer les différentes tâches qu’elle exécutera. Pour ce faire, une zone de travail visuelle dédiée vous permet de créer un diagramme de votre composition d’audiences. Dans ce diagramme, vous pouvez ajouter différentes activités et les enchaîner dans un ordre séquentiel.

## Ajouter des activités {#add}

À ce stade de la configuration, le diagramme comporte une icône de démarrage, qui représente le début de votre composition. Pour ajouter votre première activité, cliquez sur le bouton **+** associé à l’icône de démarrage.

La liste des activités pouvant être ajoutées au diagramme s’affiche. Les activités disponibles dépendent de votre position dans le diagramme de composition. Par exemple, lorsque vous ajoutez votre première activité pour démarrer votre composition, vous pouvez cibler une audience, fractionner le chemin de la composition ou définir une activité **Attente** pour retarder l’exécution de la composition. D’autres choix s’offrent à vous après une activité **Créer une audience** : vous pouvez affiner votre cible avec des activités de ciblage ou organiser le processus de la composition avec des activités de contrôle de flux.

Une fois qu’une activité a été ajoutée au diagramme, un volet s’affiche à droite. Il vous permet de définir des paramètres spécifiques pour l’activité. Des informations détaillées sur la configuration de chacune des activités sont disponibles dans [cette section](activities/about-activities.md).

![](assets/composition-create-add.png)

Répétez ce processus pour ajouter autant d’activités que vous le souhaitez en fonction des tâches que votre composition doit exécuter. Vous pouvez également insérer une nouvelle activité entre deux activités. Pour ce faire, cliquez sur le bouton **+** sur la transition entre les activités, puis sélectionnez l’activité souhaitée et configurez-la dans le volet de droite.

>[!TIP]
>
>Vous pouvez personnaliser le nom des transitions entre chaque activité. Pour ce faire, sélectionnez la transition et modifiez son libellé dans le volet de droite.

## Barre d’outils de la zone de travail {#toolbar}

La barre d’outils située dans le coin supérieur droit de la zone de travail fournit des options permettant de manipuler facilement les activités et de naviguer dans la zone de travail.

![](assets/canvas-toolbar.png)

Les actions disponibles sont les suivantes :

* **[!UICONTROL Sélection multiple]** : sélectionnez plusieurs activités pour les supprimer toutes en même temps ou pour les copier et les coller. Consultez [cette section](#copy).
* **[!UICONTROL Faire pivoter]** : retournez la zone de travail verticalement.
* **[!UICONTROL Ajuster à l’écran]** : adaptez le niveau de zoom de la zone de travail à votre écran.
* **[!UICONTROL Zoom arrière]**/**[!UICONTROL Zoom avant]** : effectuez un zoom arrière ou avant dans la zone de travail.
* **[!UICONTROL Afficher la carte]** : ouvre un instantané de la zone de travail indiquant où vous vous trouvez.

## Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le panneau des propriétés, vous permettant d’effectuer plusieurs opérations.

![](assets/activity-actions.png)

Vous pouvez effectuer les actions suivantes :

* **[!UICONTROL Supprimer]** l’activité à partir de la zone de travail.
* **[!UICONTROL Désactiver] ou [!UICONTROL activer]** l’activité. Lorsque la composition est exécutée, les activités désactivées et les activités qui suivent sur le même chemin ne sont pas exécutées et la composition est arrêtée.
* **[!UICONTROL Mettre en pause] ou [!UICONTROL reprendre]** l’activité. Lorsque la composition est exécutée, elle s’arrête quand l’activité est en pause. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.
* **[!UICONTROL Copier]** l’activité pour la coller à un autre emplacement de la composition. Pour coller les activités copiées, cliquez sur le bouton **+** sur une transition et sélectionnez **[!UICONTROL Coller l’activité X]**.<!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configurez les **[!UICONTROL options d’exécution]** pour l’activité sélectionnée. Développez la section ci-dessous pour en savoir plus sur les options disponibles.

  +++ Options d’exécution disponibles

  La section **[!UICONTROL Propriétés]** vous permet de configurer des paramètres génériques concernant l’exécution de l’activité :

   * **[!UICONTROL Exécution]** : définissez l’action à effectuer au démarrage de l’activité.
   * **[!UICONTROL Durée d’exécution maximale]** : spécifiez une durée de type « 30 s » ou « 1 h ». Si l’activité n’est pas terminée une fois cette durée écoulée, une alerte est déclenchée, ce qui n’a par ailleurs aucun impact sur le fonctionnement de la composition.
   * **[!UICONTROL Fuseau horaire]** : sélectionnez le fuseau horaire de l’activité. La composition d’audiences fédérées vous permet de gérer les décalages horaires entre plusieurs pays sur la même instance. La configuration appliquée est paramétrée lors de la création de l’instance.
   * **[!UICONTROL Affinité]** : forcez l’exécution de l’activité de composition sur une machine particulière. Vous devez pour cela définir une ou plusieurs affinités au niveau de la composition ou de l’activité concernée.
   * **[!UICONTROL Comportement]** : définissez la procédure à suivre en cas d’utilisation de tâches asynchrones.

  Le champ **[!UICONTROL Gestion des erreurs]** vous permet de définir l’action à effectuer lorsque l’activité a rencontré une erreur.

  La section **[!UICONTROL script d’initialisation]** vous permet d’initialiser des variables ou de modifier des propriétés d’activité. Cliquez sur le bouton **[!UICONTROL Modifier le code]** et saisissez l’extrait de code à exécuter. Le script est appelé lors de l’exécution de l’activité.

+++

* Accédez aux **Journaux et tâches** de l’activité.
