---
audience: end-user
title: Utiliser les activités
description: Découvrir comment utiliser les activités
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: e1720d60f542d7f43986dbc7e6e40b83d0a524a1
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 97%

---

# Utiliser les activités {#activities}

Dans la composition d’audiences fédérées, vous pouvez créer des compositions à l’aide de deux types d’activités :

* Les **activités de ciblage** vous permettent de construire une ou plusieurs cibles en définissant une audience, puis en partageant ou en combinant ces audiences à l’aide des opérations d’intersection, d’union ou d’exclusion.
* Les activités de **contrôle de flux** sont spécifiques à l’organisation et à l’exécution des compositions. Leur principale tâche est de coordonner les autres activités.

## Activités de ciblage

* [Créer une activité d’audience](build-audience.md) : définissez votre population cible. Vous pouvez sélectionner une audience existante ou utiliser le concepteur de requête pour définir votre propre requête.
* [Changement de dimension](change-dimension.md) : modifiez le schéma, ou dimension de ciblage, au fur et à mesure que vous créez votre composition.
* [Combiner](combine.md) : effectuez une segmentation sur votre population entrante. Vous pouvez utiliser une union, une intersection ou une exclusion.
* [Déduplication](deduplication.md) : supprimez les doublons dans le ou les résultats des activités entrantes.
* [Enrichissement](enrichment.md) : définissez des données supplémentaires à traiter dans votre composition. Avec cette activité, vous pouvez utiliser la transition entrante et configurer l’activité pour ajouter des données supplémentaires à la transition sortante.
* [Réconciliation](reconciliation.md) : définissez le lien entre les données de la base de données et les données d’une table de travail, par exemple les données chargées à partir d’un fichier externe.
* [Enregistrer l’audience](save-audience.md) : mettez à jour une audience existante ou créez une audience à partir de la population calculée en amont dans une composition.
* [Partage](split.md) : segmentez la population entrante en plusieurs sous-ensembles.

## Activités de contrôle de flux

* [Rendez-vous](and-join.md) : synchronisez plusieurs branches d’exécution d’une composition.
* **Fin** : marquez graphiquement la fin d’une composition. Cette activité n’a aucun impact fonctionnel et est donc facultative.
* [Branchement](fork.md) : créez des transitions sortantes afin de lancer plusieurs activités en parallèle.
* [Planificateur](scheduler.md) : planifiez le démarrage de la composition.
* [Attente](wait.md) : suspendez momentanément l’exécution d’une partie d’une composition.
