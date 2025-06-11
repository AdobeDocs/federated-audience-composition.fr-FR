---
title: Autorisations d’accès à une base de données externe
description: Découvrez les autorisations dont vous avez besoin pour accéder et effectuer des tâches sur chaque moteur de base de données
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: 530a8709a67fabec1a36e1661b922f3e9a9e6996
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 35%

---

# Matrice des droits Federated Data Access (FDA) {#fda-rights}

Le tableau suivant décrit les autorisations de base de données requises pour chaque système, ce qui vous permet d’effectuer des opérations sur des bases de données externes via Federated Data Access (FDA).

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | `USAGE ON WAREHOUSE`, `USAGE ON DATABASE` et droits d’`USAGE ON SCHEMA` | Création d’un utilisateur lié au compte AWS | Créer un compte de service et accorder l’accès principal au projet | `USE CATALOG` l’autorisation Catalogue et `CAN_USE` l’autorisation SQL Warehouse |
| **Création de tables** | privilège `CREATE TABLE ON SCHEMA` | Autorisation `CREATE` | Le rôle affecté au compte de service doit contenir : `bigquery.jobs.create` et `bigquery.tables.create` autorisations | `USE SCHEMA` et `CREATE TABLE` des autorisations |
| **Création d&#39;index** | S/O | Autorisation `CREATE` | BigQuery ne prend en charge que les index de recherche. Le rôle affecté au compte de service doit contenir les autorisations `bigquery.jobs.create`, `bigquery.tables.getData` et `bigquery.tables.createIndex` | S/O |
| **Création de fonctions** | privilège `CREATE FUNCTION ON SCHEMA` | `USAGE ON LANGUAGE plpythonu` autorisation pour pouvoir appeler des scripts Python externes | Le rôle affecté au compte de service doit contenir : autorisations `bigquery.jobs.create` et `bigquery.routines.create` | Autorisation `CREATE FUNCTION` |
| **Création de procédures** | S/O | `USAGE ON LANGUAGE plpythonu` autorisation pour pouvoir appeler des scripts Python externes | Le rôle affecté au compte de service doit contenir : autorisations `bigquery.jobs.create` et `bigquery.routines.create` |  S/O |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | Propriété de l&#39;objet | Être propriétaire de l&#39;objet ou être un super-utilisateur | Le rôle affecté au compte de service doit contenir les autorisations `bigquery.jobs.create`, `bigquery.routines.delete`, `bigquery.tables.delete` et `bigquery.tables.deleteIndex` | S/O |
| **Surveillance des exécutions** | Privilège `MONITOR` sur l’objet requis | Aucune autorisation requise pour utiliser la commande `EXPLAIN` | `monitoring.viewer` le rôle | Autorisation `CAN_VIEW` |
| **Écriture de données** | `INSERT` et/ou `UPDATE` privilèges (selon l’opération d’écriture) | `INSERT` et `UPDATE` des autorisations | Le rôle affecté au compte de service doit contenir : `bigquery.jobs.create` et `bigquery.tables.updateData` | Autorisation `MODIFY` |
| **Chargement de données dans des tables** | `CREATE STAGE ON SCHEMA`, `SELECT` et `INSERT` sur les privilèges de la table cible | `SELECT` et `INSERT` des autorisations | Le rôle affecté au compte de service doit contenir : `bigquery.jobs.create`, `bigquery.tables.getData` et `bigquery.tables.updateData` | `SELECT` et `MODIFY` des autorisations |
| **Accès aux données clientes** | Privilèges `SELECT on (FUTURE) TABLE(S)` ou `VIEW(S)` | Autorisation `SELECT` | Le rôle affecté au compte de service doit contenir : `bigquery.jobs.create` et `bigquery.tables.getData` pour les tables ou le rôle `bigquery.dataViewer` | Autorisation `SELECT` |
| **Accès aux métadonnées** | privilège `SELECT on INFORMATION_SCHEMA SCHEMA` | Autorisation `SELECT` | `bigquery.metadataViewer` le rôle |  autorisation `SELECT on INFORMATION_SCHEMA SCHEMA` |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | Autorisation de lecture (par défaut) | Autorisation `CONNECT` | Aucun privilège requis |
| **Création de tables** | `CREATE TABLE ON DATABASE` (entrepôt) et `ALTER ON SCHEMA` | Autorisation `CREATE TABLE` | privilège `CREATE ON SCHEMA` |
| **Création d&#39;index** | S/O | Autorisation `ALTER` | S/O |
| **Création de fonctions** | S/O | Autorisation `CREATE FUNCTION` | privilège `CREATE ON SCHEMA` |
| **Création de procédures** | `CREATE PROCEDURE ON DATABASE` (entrepôt) et `ALTER ON SCHEMA` | Autorisation `CREATE PROCEDURE` | privilège `CREATE ON SCHEMA` |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | `ALTER ON SCHEMA` | Autorisation `ALTER` | Propriété de l’objet ou du privilège `DROP` sur l’objet |
| **Surveillance des exécutions** | Autorisations de niveau Contributeur de Workspace ou supérieur (`queryinsights.exec_requests_history`) | Autorisation `CONTROL` | Aucun privilège requis pour utiliser l’instruction `EXPLAIN` |
| **Écriture de données** | `INSERT` et/ou `UPDATE ON OBJECT` | `INSERT` et `UPDATE` des autorisations | Privilèges `INSERT` et `UPDATE` |
| **Chargement de données dans des tables** | `SELECT ON OBJECT` et `INSERT ON OBJECT` | Autorisations `CREATE TABLE`, `EXECUTE`, `SELECT`, `INSERT`, `UPDATE` et `ALTER` | `INSERT` sur la table, `USAGE` sur le schéma |
| **Accès aux données clientes** | `SELECT ON OBJECT` | Autorisation `SELECT` | privilège `SELECT` |
| **Accès aux métadonnées** | `SELECT ON INFORMATION_SCHEMA` | Aucune autorisation requise pour décrire la table | `USAGE ON SCHEMA`, `SELECT on TABLE` et privilèges sur les tables `v_catalog.columns` et `v_catalog.view_columns` |
