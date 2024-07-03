---
audience: end-user
title: Créer des compositions
description: Découvrez comment créer des compositions
source-git-commit: fd92c280094989cb64ff5151fb00b4a8b0e650f7
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 82%

---


# Orchestration des activités de composition {#activities}

Une fois que vous avez créé une composition, vous pouvez commencer à orchestrer les différentes tâches qu’elle exécutera. Pour ce faire, un canevas visuel vous permet de construire votre diagramme de composition. Dans ce diagramme, vous pouvez ajouter différentes activités et les enchaîner dans un ordre séquentiel.

## Ajouter des activités {#add}

À ce stade de la configuration, le diagramme comporte une icône de démarrage, qui représente le début de votre workflow. Pour ajouter votre première activité, cliquez sur le bouton **+** associé à l’icône de démarrage.

La liste des activités pouvant être ajoutées au diagramme s’affiche. Les activités disponibles dépendent de votre position dans le diagramme de composition. Par exemple, lorsque vous ajoutez votre première activité, vous pouvez commencer votre composition en ciblant une audience, en divisant le chemin du workflow ou en définissant une **Attente** pour retarder l&#39;exécution du workflow. D’un autre côté, après une **Créer une audience** activité, vous pouvez affiner votre cible avec des activités de ciblage, envoyer une diffusion à votre audience avec des activités de canal ou organiser le processus de composition avec des activités de contrôle de flux.

Une fois qu’une activité a été ajoutée au diagramme, un volet s’affiche à droite. Il vous permet de définir des paramètres spécifiques pour l’activité. Des informations détaillées sur la configuration de chacune des activités sont disponibles dans [cette section](activities/about-activities.md).

Répétez ce processus pour ajouter autant d’activités que vous le souhaitez en fonction des tâches que votre composition doit exécuter. Vous pouvez également insérer une nouvelle activité entre deux activités. Pour ce faire, cliquez sur le bouton **+** sur la transition entre les activités, puis sélectionnez l’activité souhaitée et configurez-la dans le volet de droite.

Pour supprimer une activité, sélectionnez-la dans la zone de travail et cliquez sur l’icône **Supprimer** dans les propriétés de l’activité.

>[!TIP]
>
>Vous pouvez personnaliser le nom des transitions entre chaque activité. Pour ce faire, sélectionnez la transition et modifiez son libellé dans le volet de droite.

## Barre d’outils {#toolbar}

La barre d’outils située dans le coin supérieur droit de la zone de travail fournit des options permettant de manipuler facilement les activités et de naviguer dans la zone de travail :

* **Mode de sélection multiple** : sélectionnez plusieurs activités pour les supprimer toutes en même temps ou pour les copier et les coller. Consultez [cette section](#copy).
* **Faire pivoter** : retournez la zone de travail verticalement.
* **Ajuster à l’écran** : adaptez le niveau de zoom de la zone de travail à votre écran.
* **Zoom arrière**/**Zoom avant** : effectuez un zoom arrière ou avant dans la zone de travail.
* **Afficher la carte** : ouvre un instantané de la zone de travail indiquant où vous vous trouvez.


## Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le panneau des propriétés, vous permettant d’effectuer plusieurs opérations. Vous pouvez :

* **Supprimer** l’activité à partir de la zone de travail.
* **Désactivez/activez** l’activité. Lorsque le workflow est exécuté, les activités désactivées et les activités qui suivent sur le même chemin ne sont pas exécutées et le workflow est arrêté.
* **Copiez** l’activité. Consultez [cette section](#copy).
* Accédez aux **Journaux et tâches** de l’activité.
* **Mettez en pause/Reprenez** l’activité. Lorsque le workflow est exécuté, il s’arrête quand l’activité est en pause. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.

Plusieurs activités de **Ciblage**, telles que **Combiner** ou **Déduplication**, vous permettent de traiter la population restante et de l’inclure dans une transition de sortie supplémentaire. Par exemple, si vous utilisez une activité **Partage**, le complément est constitué de la population qui ne correspond à aucun des sous-ensembles définis précédemment. Pour utiliser cette fonctionnalité, activez l’option **Générer le complément**.

## Copier des activités {#copy}

Vous pouvez copier des activités de workflow et les coller dans n’importe quel workflow. Le workflow de destination peut se trouver dans un autre onglet du navigateur.

Pour copier des activités, vous avez deux possibilités :

* Copier une activité à l’aide du bouton d’action.

* Copier plusieurs activités à l’aide du bouton de la barre d’outils.

Pour coller les activités copiées, cliquez sur le bouton **+** sur une transition et sélectionnez « Coller l’activité X ».

## Options d’exécution {#execution}

Toutes les activités permettent de gérer les options d’exécution. Sélectionnez une activité et cliquez sur le bouton **Options d’exécution**. Vous pouvez ainsi définir le mode d’exécution et le comportement de l’activité en cas d’erreur.

### Propriétés

Le champ **Exécution** vous permet de définir l’action à effectuer au moment du déclenchement de la tâche.

Le champ **Durée d’exécution maximum** vous permet d’indiquer une durée de type « 30 s » ou « 1 h ». Si l’activité n’est pas terminée une fois cette durée écoulée, une alerte est déclenchée, ce qui n’a par ailleurs aucun impact sur le fonctionnement du workflow.

Le champ **Fuseau horaire** vous permet de sélectionner le fuseau horaire de l’activité. Adobe Campaign vous permet de gérer les différences de temps entre plusieurs pays sur la même instance. La configuration appliquée est paramétrée lors de la création de l’instance.

Le champ **Affinité** vous permet de forcer l’exécution d’un workflow ou d’une activité de workflow sur une machine en particulier. Vous devez pour cela définir une ou plusieurs affinités au niveau du workflow ou de l’activité concernée.

Le champ **Comportement** vous permet de définir la marche à suivre en cas de tâches asynchrones.

### Gestion des erreurs

Le champ **En cas d’erreur** vous permet de définir l’action à effectuer lorsque l’activité a rencontré une erreur.

### Script d’initialisation

Ce **script d’initialisation** vous permet d’initialiser des variables ou de modifier des propriétés d’activité. Cliquez sur le bouton **Modifier le code** et saisissez l’extrait de code à exécuter. Le script est appelé lors de l’exécution de l’activité.

## Exemple {#example}

Voici un exemple de workflow permettant d’envoyer un e-mail à l’ensemble de la clientèle (autres que les clientes et clients VIP) qui s’intéresse aux machines à café.

Dans le cadre de ce workflow, les activités suivantes ont été ajoutées :

* une activité **[!UICONTROL Branchement]** qui divise le workflow en trois chemins (un pour chaque ensemble de clients et clientes)
* des activités **[!UICONTROL Créer une audience]** destinées à cibler les trois ensembles de clients et clientes :

   * les clients et clientes disposant d’une adresse e-mail
   * les clients et clientes appartenant à l’audience préexistante « Intéressés par la ou les machines à café »
   * les clients et clientes appartenant à l’audience préexistante « VIP ou récompense »

* une activité **[!UICONTROL Combiner]** qui regroupe les clients et clientes disposant d’une adresse e-mail et ceux ou celles intéressés par les machines à café
* une activité **[!UICONTROL Combiner]** qui exclut les clients et clientes VIP
* une activité **[!UICONTROL Diffusion e-mail]** qui envoie un e-mail aux clients et clientes correspondants

Une fois le workflow terminé, ajoutez l’activité **[!UICONTROL Fin]** à la fin du diagramme. Cette activité permet d’illustrer la fin d’un workflow et n’a aucun impact sur celui-ci.

Une fois le diagramme de workflow conçu, vous pouvez l’exécuter et suivre l’avancement de ses différentes tâches.