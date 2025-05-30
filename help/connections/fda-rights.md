---
title: Autorisations d’accès à une base de données externe
description: Découvrir les droits spécifiques à chaque moteur de base de données
exl-id: 287fb4a4-5767-4337-96be-dceca55f756d
source-git-commit: f778f3367c5e19a3052e1055005b6c84f3a55a57
workflow-type: ht
source-wordcount: '560'
ht-degree: 100%

---

# Matrice des droits FDA {#fda-rights}

Le tableau ci-dessous décrit les privilèges de base de données requis pour chaque système, ce qui permet aux utilisateurs et utilisatrices d’effectuer des opérations sur des bases de données externes via FDA.

|   | Snowflake | Redshift | Google BigQuery | Databricks |
|:-:|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | Privilèges USAGE ON WAREHOUSE, USAGE ON DATABASE et USAGE ON SCHEMA | Création d&#39;un utilisateur lié au compte AWS | Créer un compte de service et accorder l’accès principal au projet | Privilège USE CATALOG sur Catalog et privilège CAN_USE sur SQL Warehouse |
| **Création de tables** | Privilège CREATE TABLE ON SCHEMA  | Privilège CREATE | Le rôle affecté au compte de service doit contenir les éléments suivants : autorisations bigquery.jobs.create et bigquery.tables.create. | Privilèges USE SCHEMA et CREATE TABLE |
| **Création d&#39;index** | S/O | Privilège CREATE | BigQuery ne prend en charge que les index de recherche. Le rôle affecté au compte de service doit contenir les éléments suivants : autorisations bigquery.jobs.create, bigquery.tables.getData et bigquery.tables.createIndex. | S/O |
| **Création de fonctions** | Privilège CREATE FUNCTION ON SCHEMA | Privilège USAGE ON LANGUAGE plpythonu pour pouvoir appeler des scripts Python externes | Le rôle affecté au compte de service doit contenir les éléments suivants : autorisations bigquery.jobs.create et bigquery.routines.create. | Privilège CREATE FUNCTION |
| **Création de procédures** | S/O | Privilège USAGE ON LANGUAGE plpythonu pour pouvoir appeler des scripts Python externes | Le rôle affecté au compte de service doit contenir les éléments suivants : autorisations bigquery.jobs.create et bigquery.routines.create. |  S/O |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | Propriété de l&#39;objet | Être propriétaire de l&#39;objet ou être un super-utilisateur | Le rôle affecté au compte de service doit contenir les éléments suivants : autorisations bigquery.jobs.create, bigquery.routines.delete, bigquery.tables.delete et bigquery.tables.deleteIndex. |
| **Surveillance des exécutions** | Privilège MONITOR sur l&#39;objet requis | Aucun privilège requis pour utiliser la commande EXPLAIN | Rôle monitoring.viewer | Privilège CAN_VIEW |
| **Écriture de données** | Privilèges INSERT et/ou UPDATE (selon l&#39;opération d&#39;écriture) | Privilèges INSERT et UPDATE | Le rôle affecté au compte de service doit contenir les éléments suivants : bigquery.jobs.create et bigquery.tables.updateData. | Privilège MODIFY |
| **Chargement de données dans des tables** | Privilèges CREATE STAGE ON SCHEMA, SELECT et INSERT sur la table ciblée | Privilèges SELECT et INSERT | Le rôle affecté au compte de service doit contenir les éléments suivants : bigquery.jobs.create, bigquery.tables.getData et bigquery.tables.updateData. | Privilèges SELECT et MODIFY |
| **Accès aux données clientes** | Privilège(s) SELECT sur (FUTURE) TABLE(S) ou VIEW(S) | Privilège SELECT | Le rôle affecté au compte de service doit contenir les éléments suivants : bigquery.jobs.create et bigquery.tables.getData pour les tables ou le rôle bigquery.dataViewer. | Privilège SELECT |
| **Accès aux métadonnées** | Privilège SELECT sur INFORMATION_SCHEMA SCHEMA | Privilège SELECT | Rôle bigquery.metadataViewer | Privilège SELECT sur INFORMATION_SCHEMA SCHEMA |


|   | Microsoft Fabric | Azure Synapse Analytics | Vertica |
|:-:|:-:|:-:|:-:|
| **Connexion à une base de données distante** | Autorisation de lecture (par défaut) | Autorisation CONNECT | Aucun privilège requis |
| **Création de tables** | CREATE TABLE ON DATABASE (entrepôt de données) et ALTER ON SCHEMA | Autorisation CREATE TABLE | Privilège CREATE ON SCHEMA |
| **Création d&#39;index** | S/O | Autorisation ALTER | S/O |
| **Création de fonctions** | S/O | Autorisation CREATE FUNCTION | Privilège CREATE ON SCHEMA |
| **Création de procédures** | CREATE PROCEDURE ON DATABASE (entrepôt de données) et ALTER ON SCHEMA | Autorisation CREATE PROCEDURE | Privilège CREATE ON SCHEMA |
| **Suppression d&#39;objets (tables, index, fonctions, procédures)** | ALTER ON SCHEMA | Autorisation ALTER | Propriété de l’objet ou autorisation DROP sur l’objet |
| **Surveillance des exécutions** | Autorisations de niveau Contributeur ou contributrice Workspace ou supérieur (queryinsights.exec_requests_history) | Autorisation CONTROL | Aucun privilège requis pour utiliser l’instruction EXPLAIN |
| **Écriture de données** | INSERT et/ou UPDATE ON OBJECT | Autorisations INSERT et UPDATE | Privilèges INSERT et UPDATE |
| **Chargement de données dans des tables** | SELECT ON OBJECT et INSERT ON OBJECT | Autorisations CREATE TABLE, EXECUTE, SELECT, INSERT, UPDATE, ALTER | Privilège INSERT sur la table, privilège USAGE sur le schéma |
| **Accès aux données clientes** | SELECT ON OBJECT | Autorisation SELECT | Privilège SELECT |
| **Accès aux métadonnées** | SELECT ON INFORMATION_SCHEMA | Aucune autorisation requise pour décrire la table | USAGE ON SCHEMA, SELECT sur TABLE et également les privilèges sur les tables v_catalog.columns et v_catalog.view_columns |
