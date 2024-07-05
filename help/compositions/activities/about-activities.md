---
audience: end-user
title: Utilisation des activités
description: Découvrez comment utiliser les activités
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 42%

---


# Utilisation des activités {#activities}

Dans la composition d’audiences fédérées, vous pouvez créer des compositions à l’aide de deux types d’activités :

* **Activités de ciblage** vous permet de créer une ou plusieurs cibles en définissant une audience et en partitionnant ou en combinant ces audiences à l’aide des opérations d’intersection, d’union ou d’exclusion.
* **Contrôle de flux** Les activités sont spécifiques à l&#39;organisation et à l&#39;exécution des compositions. Leur tâche principale est de coordonner les autres activités.

## Activités de ciblage

* [Activité Créer une audience](build-audience.md): définissez votre population cible. Vous pouvez sélectionner une audience existante ou utiliser le concepteur de requête pour définir votre propre requête.
* [Changement de dimension](change-dimension.md): modifiez le schéma, également appelé dimension de ciblage, à mesure que vous créez votre composition.
* [Combiner](combine.md) : effectuez une segmentation sur votre population entrante. Vous pouvez utiliser une union, une intersection ou une exclusion.
* [Déduplication](deduplication.md) : supprimez les doublons dans le ou les résultats des activités entrantes.
* [Enrichissement](enrichment.md): définissez des données supplémentaires à traiter dans votre composition. Avec cette activité, vous pouvez utiliser la transition entrante et configurer l’activité pour ajouter des données supplémentaires à la transition sortante.
* [Réconciliation](reconciliation.md): définissez le lien entre les données de la base et les données d&#39;une table de travail, par exemple les données chargées à partir d&#39;un fichier externe.
* [Sauvegarde d’audience](save-audience.md): mettre à jour une audience existante ou créer une nouvelle audience à partir de la population calculée en amont dans une composition.
* [Partage](split.md) : segmentez la population entrante en plusieurs sous-ensembles.

## Activités de contrôle de flux

* [AND-join](and-join.md): synchroniser plusieurs branches d’exécution d’un workflow ;
* **Fin** : marque la fin d’un workflow sous forme graphique. Cette activité n’a aucun impact fonctionnel et est donc facultative.
* [Branchement](fork.md) : créez des transitions sortantes afin de lancer plusieurs activités en parallèle.
* [Planificateur](scheduler.md) : planifiez le moment de démarrage du workflow.
* [Attente](wait.md) : suspendez momentanément l’exécution d’une partie d’un workflow.
