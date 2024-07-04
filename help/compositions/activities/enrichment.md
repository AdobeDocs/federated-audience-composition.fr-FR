---
audience: end-user
title: Utilisation de l’activité Enrichissement
description: Découvrez comment utiliser l’activité Enrichissement
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 76%

---


# Enrichissement {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Activité Enrichissement"
>abstract="L’activité **Enrichissement** permet d’enrichir les données ciblées avec des informations supplémentaires provenant de la base de données. Il est généralement utilisé dans une composition après des activités de segmentation."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Activité Enrichissement"
>abstract="Une fois les données d’enrichissement ajoutées à la composition, elles peuvent être utilisées dans les activités ajoutées après la **Enrichissement** pour segmenter les profils en groupes distincts en fonction de leurs comportements, préférences et choix."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Définition de lien"
>abstract="Créez un lien entre les données de la table de travail et la base de données fédérée."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Réconciliation des enrichissements"
>abstract="Définissez les paramètres de réconciliation."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Données d’enrichissement"
>abstract="Sélectionnez les données à utiliser pour enrichir votre composition. Vous pouvez sélectionner deux types de données d’enrichissement : un seul attribut d’enrichissement de la dimension cible ou un lien de collection, qui est un lien avec une cardinalité 1-N entre les tables."

La variable **Enrichissement** activité vous permet d’améliorer les données ciblées avec des informations supplémentaires de la base de données fédérée. Il est généralement utilisé dans des compositions après des activités de segmentation.

Les données d’enrichissement tirent leur origine des sources suivantes :

* **A partir de la même table de travail** comme celui ciblé dans votre composition :

  *Ciblez un groupe de clientes et de clients et ajoutez le champ « Date de naissance » au tableau de travail actuel.*

* **Une autre table de travail** :

  *Ciblez un groupe de clients et de clientes et ajoutez les champs « Montant » et « Type de produit » provenant du tableau « Achat »*.

Une fois que les données d&#39;enrichissement ont été ajoutées à la composition, elles peuvent être utilisées dans les activités ajoutées après la **Enrichissement** pour segmenter les clients en groupes distincts en fonction de leur comportement, de leurs préférences et de leurs choix.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Ajouter une activité Enrichissement {#enrichment-configuration}

Pour configurer l’activité **Enrichissement**, procédez comme suit :

1. Ajoutez des activités telles que **Créer une audience** et **Combiner**.
1. Ajoutez une activité **Enrichissement**.
1. Si plusieurs transitions ont été configurées dans votre composition, vous pouvez utiliser la variable **[!UICONTROL Principal]** champ pour définir la transition à utiliser comme ensemble principal pour enrichir les données.

## Ajouter des données d’enrichissement {#enrichment-add}

1. Cliquez sur **Ajouter des données d’enrichissement** et sélectionnez l’attribut à utiliser pour enrichir les données.

   Vous pouvez sélectionner deux types de données d’enrichissement : un attribut d’enrichissement unique de la dimension cible, ou un lien de collection. Chacun de ces types est détaillé dans les exemples ci-dessous :

   * [Attribut d’enrichissement unique](#single-attribute)
   * [Lien de collection](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## Créer des liens entre les tables {#create-links}

La variable **[!UICONTROL Définition de lien]** permet de créer un lien entre les données de la table de travail et votre base de données. Par exemple, si vous chargez les données d’un fichier contenant le numéro de compte, le pays et l’e-mail des personnes destinataires, vous devez créer un lien vers le tableau des pays afin de mettre à jour cette information dans leur profil.

Plusieurs types de liens sont disponibles :

* **[!UICONTROL Lien simple de cardinalité 1]** : chaque enregistrement de l’ensemble principal peut être associé à un seul enregistrement des données liées.
* **[!UICONTROL Lien simple de cardinalité 0 ou 1]** : chaque enregistrement de l’ensemble principal peut être associé à 0 ou 1 enregistrement des données liées (et pas plus de un).
* **[!UICONTROL Lien de collection de cardinalité N]** : chaque enregistrement de l’ensemble principal peut être associé à 0, 1 ou plus (N) d’enregistrements des données liées.

Pour créer un lien, procédez comme suit :

1. Dans la section **[!UICONTROL Définition du lien]**, cliquez sur le bouton **[!UICONTROL Ajouter un lien]**.

1. Dans la liste déroulante **Type de relation**, sélectionnez le type de lien que vous souhaitez créer.

1. Identifiez la cible à laquelle vous souhaitez lier l’ensemble principal :

   * Pour lier une table existante dans la base de données, choisissez **[!UICONTROL Schéma de base de données]** et sélectionnez la table souhaitée dans le champ **[!UICONTROL Schéma cible]**.
   * Pour créer un lien avec les données de la transition en entrée, choisissez **Schéma temporaire** et sélectionnez la transition dont vous souhaitez utiliser les données.

1. Définissez les critères de réconciliation pour faire correspondre les données de l’ensemble principal avec le schéma lié. Deux types de jointures sont disponibles :

   * **Jointure simple** : sélectionnez un attribut spécifique pour faire correspondre les données des deux schémas. Cliquez sur **Ajouter une jointure** et sélectionnez les attributs **Source** et **Destination** à utiliser comme critères de réconciliation.
   * **Jointure avancée** : créez une jointure à l’aide de conditions avancées. Cliquez sur **Ajouter une jointure** puis sur le bouton **Créer une condition** pour ouvrir le concepteur de requête.

Un exemple de composition utilisant des liens est disponible dans la [Exemples](#link-example) .

## Exemples {#example}

### Attribut d’enrichissement unique {#single-attribute}

Ici, nous ajoutons un seul attribut d’enrichissement, par exemple, la date de naissance. Procédez de la façon suivante :

1. Cliquez dans le champ **Attribut**.
1. Sélectionnez un champ simple dans la dimension de ciblage, la date de naissance dans notre exemple.
1. Cliquez sur **Confirmer**.

### Lien de collecte {#collection-link}

Dans ce cas pratique plus complexe, nous sélectionnons un lien de collecte qui est un lien avec une cardinalité 1-N entre les tableaux. Récupérons les trois derniers achats inférieurs à 100 USD. Pour cela, vous devez définir :

* un attribut d’enrichissement : le champ **Montant total** ;
* le nombre de lignes à récupérer : 3 ;
* un filtre : filtrez les éléments supérieurs à 100 USD ;
* un tri : tri descendant sur le champ **Date de commande**.

#### Ajouter l’attribut {#add-attribute}

C’est là que vous sélectionnez le lien de collecte à utiliser comme données d’enrichissement.

1. Cliquez dans le champ **Attribut**.
1. Cliquez sur **Afficher les attributs avancés**.
1. Sélectionnez le champ **Montant total** dans le tableau **Achats**.

#### Définir les paramètres de la collecte{#collection-settings}

Définissez ensuite la manière dont les données sont collectées et le nombre d’enregistrements à récupérer.

1. Sélectionnez **Collecter des données** dans le menu déroulant **Sélectionner la manière de collecter les données**.
1. Saisissez « 3 » dans le champ **Lignes à récupérer (Colonnes à créer)**.

Si vous souhaitez, par exemple, obtenir le montant moyen des achats d’un client ou une cliente, sélectionnez **Données agrégées**, puis **Moyenne** dans le menu déroulant **Fonction d’agrégat**.

#### Définir des filtres{#collection-filters}

Ici, nous définissons la valeur maximale de l’attribut d’enrichissement. Nous filtrons les éléments qui sont supérieurs à 100$. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. Cliquez sur **Modifier les filtres**.
1. Ajoutez les deux filtres suivants : **Montant total** existe ET **Montant total** est inférieur à 100. Le premier filtre les valeurs NULL, car elles apparaissent comme la valeur la plus élevée.
1. Cliquez sur **Confirmer**.

#### Définir le tri{#collection-sorting}

Nous devons maintenant appliquer un tri pour récupérer les trois **derniers** achats.

1. Activez l’option **Activer le tri**.
1. Cliquez dans le champ **Attribut**.
1. Sélectionnez le champ **Date de commande**.
1. Cliquez sur **Confirmer**.
1. Sélectionnez **Descendant** dans le menu déroulant **Tri**.


### Enrichissement avec des données liées {#link-example}

L&#39;exemple ci-dessous illustre une composition configurée pour créer un lien entre deux transitions. La première transition cible les données de profil à l’aide d’une activité Requête, tandis que la seconde transition inclut les données d’achat stockées dans un fichier chargé via une activité Chargement de fichier.

* La première activité **Enrichissement** lie notre ensemble principal (données issues de l’activité **Requête**) au schéma de l’activité **Chargement de fichier**. Cela nous permet de faire correspondre chaque profil ciblé par la requête avec les données d’achat correspondantes.
* Une seconde **Enrichissement** l’activité est ajoutée afin d’enrichir les données de la table de composition avec les données d’achat provenant du **Chargement de fichier** activité. Cela nous permet d’utiliser ces données dans d’autres activités, par exemple pour personnaliser les messages envoyés aux clientes et clients avec des informations sur leur achat.





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
