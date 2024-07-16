---
audience: end-user
title: Utilisation des activités
description: Découvrez comment utiliser les activités
source-git-commit: 9f84502684c7cd0e174b1fcad4b9c811f50965f1
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 35%

---


# Utilisation des activités {#activities}

Dans la composition d’audiences fédérées, vous pouvez créer des compositions à l’aide de deux types d’activités :

* Les **activités de ciblage** vous permettent de créer une ou plusieurs cibles en définissant une audience et en partitionnant ou en combinant ces audiences à l’aide des opérations d’intersection, d’union ou d’exclusion.
* Les activités **Contrôle de flux** sont spécifiques à l’organisation et à l’exécution des compositions. Leur tâche principale est de coordonner les autres activités.

## Activités de ciblage

* [ Activité Créer une audience](build-audience.md) : définissez votre population cible. Vous pouvez sélectionner une audience existante ou utiliser le concepteur de requête pour définir votre propre requête.
* [Changement de dimension](change-dimension.md) : modifiez le schéma, également appelé dimension de ciblage, à mesure que vous créez votre composition.
* [Combiner](combine.md) : effectuez une segmentation sur votre population entrante. Vous pouvez utiliser une union, une intersection ou une exclusion.
* [Déduplication](deduplication.md) : supprimez les doublons dans le ou les résultats des activités entrantes.
* [Enrichissement](enrichment.md) : définissez des données supplémentaires à traiter dans votre composition. Avec cette activité, vous pouvez utiliser la transition entrante et configurer l’activité pour ajouter des données supplémentaires à la transition sortante.
* [Réconciliation](reconciliation.md) : définissez le lien entre les données de la base et les données d&#39;une table de travail, par exemple les données chargées à partir d&#39;un fichier externe.
* [Sauvegarde d&#39;audience](save-audience.md) : mettez à jour une audience existante ou créez une nouvelle audience à partir de la population calculée en amont dans une composition.
* [Partage](split.md) : segmentez la population entrante en plusieurs sous-ensembles.

## Activités de contrôle de flux

* [AND-join](and-join.md) : synchronisez plusieurs branches d’exécution d’une composition.
* **Fin** : marque la fin d’une composition sous forme graphique. Cette activité n’a aucun impact fonctionnel et est donc facultative.
* [Branchement](fork.md) : créez des transitions sortantes afin de lancer plusieurs activités en parallèle.
* [Planificateur](scheduler.md) : planifiez le démarrage de la composition.
* [Attente](wait.md) : interrompez momentanément l’exécution d’une partie d’une composition.
