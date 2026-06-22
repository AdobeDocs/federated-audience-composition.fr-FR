---
audience: end-user
title: Ciblage d’entités multiples avec des audiences de la composition d’audiences fédérées dans Adobe Journey Optimizer
description: Découvrez comment cibler des profils à partir d’audiences de la composition d’audiences fédérées dans des parcours Adobe Journey Optimizer.
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: ht
source-wordcount: '496'
ht-degree: 100%

---


# Ciblage d’entités multiples avec des audiences de la composition d’audiences fédérées dans Adobe Journey Optimizer

Avec le ciblage d’entités multiples, vous pouvez utiliser les attributs d’audiences de la composition d’audiences fédérées comme identifiants supplémentaires dans les parcours Adobe Journey Optimizer.Ces attributs vous permettent d’activer des audiences au niveau de plusieurs entités, telles que des comptes ou des abonnements.

## Créer votre audience dans la composition d’audiences fédérées {#create}

Pour commencer à utiliser le ciblage d’entités multiples, vous devez d’abord créer et enregistrer votre audience dans la composition d’audiences fédérées.

Dans l’interface d’utilisation de la composition d’audiences, ajoutez l’activité **Créer une audience** pour créer l’audience dans la zone de travail de la composition fédérée et ajoutez l’activité **Enregistrer l’audience** pour configurer les mappages, l’identité principale et l’expiration des données de l’audience.

![L’interface d’utilisation de la composition d’audiences fédérées s’affiche à l’écran et affiche l’audience.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Une fois les configurations de votre audience terminées, sélectionnez **Démarrer** pour démarrer l’exécution de la composition.Cette audience et son jeu de données correspondant pourront être utilisés dans Experience Platform.

Pour plus d’informations sur la création d’une composition dans la composition d’audiences fédérées, consultez le [guide de création d’une composition](/help/compositions/create-composition.md).

## Activer l’audience dans Adobe Journey Optimizer {#activate}

Une fois l’exécution de votre composition terminée, vous pouvez activer l’audience dans Journey Optimizer.Dans la section **Gestion des parcours** d’Adobe Journey Optimizer, sélectionnez **Parcours**, puis **Créer un parcours** pour ouvrir l’interface d’utilisation du parcours.

![Le bouton Créer un parcours dans Adobe Journey Optimizer est mis en surbrillance.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

Dans l’interface du parcours, ajoutez un nœud **Lecture d’audience**.Vous pouvez configurer ce nœud en indiquant un libellé et en sélectionnant l’audience que vous avez précédemment créée.

![Le nœud Lecture d’audience s’affiche dans l’interface d’utilisation de Journey Optimizer.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Après avoir sélectionné l’audience créée précédemment, activez l’option **Utiliser un identifiant supplémentaire**.

![La case Utiliser un identifiant supplémentaire est mise en surbrillance.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Vous pouvez maintenant choisir un identifiant supplémentaire.Sur l’écran de sélection, sélectionnez **Mode avancé** et accédez à **Experience Platform**.Sur cette page, sélectionnez le nom de l’audience que vous avez précédemment créée, puis choisissez l’identifiant supplémentaire que vous souhaitez utiliser pour l’audience.

![L’éditeur d’expression s’affiche.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Configurer les conditions du parcours {#configure-journey}

Maintenant que vous avez activé et configuré les paramètres de votre audience, vous pouvez continuer à configurer les autres conditions de votre parcours.Pour ce cas d’utilisation, vous aurez besoin d’ajouter un nœud **Optimizer** après le nœud **Lecture d’audience**, suivi d’un nœud **Action**.

Après avoir configuré les nœuds restants, sélectionnez **Publier** pour terminer la création du parcours.

![Le bouton Publier est mis en surbrillance.](/help/connections/assets/multi-entity-targeting/select-publish.png)

Votre parcours cible désormais les profils d’audience en fonction de l’**identifiant supplémentaire** plutôt que l’identifiant principal.Grâce à cette fonctionnalité, vous pouvez désormais cibler plusieurs entités telles que l’identifiant d’abonnement, l’identifiant de compte ou l’identifiant de commande et les activer pour le canal de votre choix.

## Étapes suivantes {#next-steps}

La lecture de ce guide vous a permis de découvrir comment utiliser des identifiants supplémentaires issus de vos audiences de la composition d’audiences fédérées dans les parcours Journey Optimizer.Pour plus d’informations sur l’utilisation de parcours supplémentaires, consultez le [guide d’utilisation d’identifiants supplémentaires dans les parcours](https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

