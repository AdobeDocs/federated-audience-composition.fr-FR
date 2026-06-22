---
title: Autorisations d’accès à une base de données externe
description: Découvrez les autorisations dont vous avez besoin pour accéder à chaque moteur de base de données et y effectuer des tâches.
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
TQID: https://experienceleague.adobe.com/LI7H7b6iM3TAsPy00wDwNj3-D0Z7mIrH9MKW8g9QDsk
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 2f08e668fafcde9df941313f912c5cb2037ef691
workflow-type: ht
source-wordcount: 445
ht-degree: 100%

---

# Matrice des droits Federated Data Access (FDA) {#fda-rights}

Le tableau suivant décrit les autorisations de base de données requises pour chaque système. Elles vous permettent d’effectuer des opérations sur des bases de données externes via Federated Data Access (FDA).

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | Privilèges `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` et `USAGE ON SCHEMA` | Créer un utilisateur ou une utilisatrice lié au compte AWS | Créer un compte de service et accorder l’accès principal au projet | Autorisation `USE CATALOG` sur le catalogue et autorisation `CAN_USE` sur l’entrepôt de données SQL |
| **Création de tables** | Privilège `CREATE TABLE ON SCHEMA` | Autorisation `CREATE` | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create` et `bigquery.tables.create`. | Autorisations `USE SCHEMA` et `CREATE TABLE` |
| **Création d&#39;index** | S.O. | Autorisation `CREATE` | BigQuery ne prend en charge que les index de recherche. Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create`, `bigquery.tables.getData` et `bigquery.tables.createIndex`. | S.O. |
| **Création de fonctions** | Privilège `CREATE FUNCTION ON SCHEMA` | Autorisation `USAGE ON LANGUAGE plpythonu` pour appeler des scripts Python externes | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create` et `bigquery.routines.create`. | Autorisation `CREATE FUNCTION` |
| **Création de procédures** | S.O. | Autorisation `USAGE ON LANGUAGE plpythonu` pour appeler des scripts Python externes | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create` et `bigquery.routines.create`. |  S/O |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | Propriété de l&#39;objet | Être propriétaire de l’objet ou être un super-utilisateur | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` et `bigquery.tables.deleteIndex`. | S.O. |
| **Surveillance des exécutions** | Privilège `MONITOR` sur l’objet requis | Aucune autorisation requise pour utiliser la commande `EXPLAIN` | Rôle `monitoring.viewer` | Autorisation `CAN_VIEW` |
| **Écriture de données** | Privilèges `INSERT` et/ou `UPDATE` (selon l’opération d’écriture) | Autorisations `INSERT` et `UPDATE` | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create` et `bigquery.tables.updateData`. | Autorisation `MODIFY` |
| **Chargement de données dans des tables** | Privilèges `CREATE STAGE ON SCHEMA`, `Create file FORMATGRANT CREATE FILE FORMAT ON SCHEMA <SCHEMA> to ROLE <ROLE>` `SELECT`, et `INSERT` pour la table cible | Autorisations `SELECT` et `INSERT` | Le rôle affecté au compte de service doit avoir les autorisations `bigquery.jobs.create`, `bigquery.tables.getData` et `bigquery.tables.updateData`. | Autorisations `SELECT` et `MODIFY` |
| **Accès aux données clientes** | Privilège `SELECT on (FUTURE) TABLE(S)` ou `VIEW(S)` | Autorisation `SELECT` | Le rôle affecté au compte de service doit inclure les autorisations `bigquery.jobs.create`, `bigquery.readsessions.create` et `bigquery.tables.getData` pour les tables ou le rôle `bigquery.dataViewer`. | Autorisation `SELECT` |
| **Accès aux métadonnées** | Privilège `SELECT on INFORMATION_SCHEMA SCHEMA` | Autorisation `SELECT` | Rôle `bigquery.metadataViewer` |  Autorisation `SELECT on INFORMATION_SCHEMA SCHEMA` |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica | Teradata |
|:-:|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | Autorisation de lecture (par défaut) | Autorisation `CONNECT` | Aucun privilège requis | Privilège `CONNECT` |
| **Création de tables** | `CREATE TABLE ON DATABASE` (entrepôt de données) et `ALTER ON SCHEMA` | Autorisation `CREATE TABLE` | Privilège `CREATE ON SCHEMA` | Mot-clé `CREATE TABLE` ou `TABLE` |
| **Création d&#39;index** | S.O. | Autorisation `ALTER` | S.O. | Mot-clé `CREATE INDEX` ou `INDEX` |
| **Création de fonctions** | S.O. | Autorisation `CREATE FUNCTION` | Privilège `CREATE ON SCHEMA` | Mot-clé `CREATE FUNCTION` ou `FUNCTION` |
| **Création de procédures** | `CREATE PROCEDURE ON DATABASE` (entrepôt de données) et `ALTER ON SCHEMA` | Autorisation `CREATE PROCEDURE` | Privilège `CREATE ON SCHEMA` | Mot-clé `CREATE PROCEDURE` ou `PROCEDURE` |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | `ALTER ON SCHEMA` | Autorisation `ALTER` | Propriété de l’objet ou du privilège `DROP` sur l’objet | `DROP` pour le type d’objet ou le mot-clé associé |
| **Surveillance des exécutions** | Autorisations de niveau Contributeur ou contributrice Workspace ou supérieur (`queryinsights.exec_requests_history`) | Autorisation `CONTROL` | Aucun privilège requis pour utiliser l’instruction `EXPLAIN` | Aucun privilège supplémentaire requis pour utiliser l’instruction `EXPLAIN` |
| **Écriture de données** | `INSERT` et/ou `UPDATE ON OBJECT` | Autorisations `INSERT` et `UPDATE` | Privilèges `INSERT` et `UPDATE` | Privilèges `INSERT` et `UPDATE` |
| **Chargement de données dans des tables** | `SELECT ON OBJECT` et `INSERT ON OBJECT` | Autorisations `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` et `ALTER` | Privilège `INSERT` sur la table, privilège `USAGE` sur le schéma | `SELECT` et `INSERT` (par exemple `COPY TO`/`COPY FROM`) |
| **Accès aux données clientes** | `SELECT ON OBJECT` | Autorisation `SELECT` | Privilège `SELECT` | Privilège `SELECT` |
| **Accès aux métadonnées** | `SELECT ON INFORMATION_SCHEMA` | Aucune autorisation requise pour décrire la table | `USAGE ON SCHEMA`, `SELECT on TABLE` et privilèges sur les tables `v_catalog.columns` et `v_catalog.view_columns` | Privilège `SHOW` |
