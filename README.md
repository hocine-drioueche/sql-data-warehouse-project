# 🌐 Data Warehouse and Analytics Project  

[English](#english) | [Français](#français)  

---

## English

# Data Warehouse and Analytics Project

Welcome to the **Data Warehouse and Analytics Project** repository! 🚀  

This project demonstrates a comprehensive data warehousing and analytics solution, from building a data warehouse to generating actionable insights. Designed as a portfolio project, it highlights industry best practices in data engineering and analytics.

---

## 🏗️ Data Architecture

The data architecture for this project follows Medallion Architecture **Bronze**, **Silver**, and **Gold** layers:

![Data Architecture](docs/data_architecture.png)

1. **Bronze Layer**: Stores raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.  
2. **Silver Layer**: Includes data cleansing, standardization, and normalization processes to prepare data for analysis.  
3. **Gold Layer**: Houses business-ready data modeled into a star schema required for reporting and analytics.  

---

## 📖 Project Overview

This project involves:

1. **Data Architecture**: Designing a Modern Data Warehouse using Medallion Architecture **Bronze**, **Silver**, and **Gold** layers.  
2. **ETL Pipelines**: Extracting, transforming, and loading data from source systems into the warehouse.  
3. **Data Modeling**: Developing fact and dimension tables optimized for analytical queries.  
4. **Analytics & Reporting**: Creating SQL-based reports and dashboards for actionable insights.  

---

## 🛠️ Important Tools

- **SQL Server Express**: Lightweight server for hosting your SQL database.  
- **SQL Server Management Studio (SSMS)**: GUI for managing and interacting with databases.  

---

## 🗓️ Project Requirements

### Building the Data Warehouse (Data Engineering)

**Objective**:  
Develop a modern data warehouse using MySQL Workbench to consolidate sales data, enabling analytical reporting and informed decision-making.

**Specifications**:  

- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.  
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.  
- **Integration**: Combine both sources into a single, user-friendly data model designed for analytical queries.  
- **Scope**: Focus on the latest dataset only; historization of data is not required.  
- **Documentation**: Provide clear documentation of the data model to support both business stakeholders and analytics teams.  

---

### 📊 BI: Analytics & Reporting (Data Analysis)

**Objective**:  
Develop SQL-based analytics to deliver detailed insights into:

- **Customer Behavior**  
- **Product Performance**  
- **Sales Trends**  

These insights empower stakeholders with key business metrics, enabling strategic decision-making.  

---

## 🛡️ License

This project is licensed under the MIT License. You are free to use, modify, and share this project with proper attribution.

---

## 🌟 About Me

Hi there! I'm **Hocine DRIOUECHE**

---

## Français

# Projet de Data Warehouse et d’Analyse

Bienvenue dans le dépôt du **Projet de Data Warehouse et d’Analyse** ! 🚀  

Ce projet présente une solution complète de data warehousing et d’analytique, allant de la construction d’un entrepôt de données jusqu’à la génération d’insights exploitables. Conçu comme un projet de portfolio, il met en avant les meilleures pratiques de l’industrie en ingénierie des données et en analyse.

---

## 🏗️ Architecture des Données

L’architecture des données de ce projet suit l’architecture Médaillon avec les couches **Bronze**, **Silver** et **Gold** :

![Data Architecture](docs/data_architecture.png)

1. **Couche Bronze** : Stocke les données brutes telles qu’elles proviennent des systèmes sources. Les données sont importées à partir de fichiers CSV dans une base SQL Server.  
2. **Couche Silver** : Inclut les processus de nettoyage, de standardisation et de normalisation des données pour les préparer à l’analyse.  
3. **Couche Gold** : Contient des données prêtes pour le métier, modélisées en schéma en étoile, nécessaires pour le reporting et l’analytique.  

---

## 📖 Aperçu du Projet

Ce projet comprend :

1. **Architecture des données** : Conception d’un entrepôt de données moderne basé sur l’architecture Médaillon avec les couches **Bronze**, **Silver** et **Gold**.  
2. **Pipelines ETL** : Extraction, transformation et chargement des données des systèmes sources vers l’entrepôt.  
3. **Modélisation des données** : Développement de tables de faits et de dimensions optimisées pour les requêtes analytiques.  
4. **Analytique & Reporting** : Création de rapports SQL et de tableaux de bord pour fournir des insights exploitables.  

---

## 🛠️ Outils Importants

- **SQL Server Express** : Serveur léger pour héberger votre base de données SQL.  
- **SQL Server Management Studio (SSMS)** : Interface graphique pour gérer et interagir avec les bases de données.  

---

## 🗓️ Exigences du Projet

### Construction du Data Warehouse (Ingénierie des Données)

**Objectif** :  
Développer un entrepôt de données moderne avec MySQL Workbench afin de consolider les données de ventes, permettant un reporting analytique et une prise de décision éclairée.

**Spécifications** :  

- **Sources de données** : Importer les données de deux systèmes sources (ERP et CRM) fournis sous forme de fichiers CSV.  
- **Qualité des données** : Nettoyer et résoudre les problèmes de qualité des données avant l’analyse.  
- **Intégration** : Combiner les deux sources dans un modèle de données unique et convivial conçu pour les requêtes analytiques.  
- **Portée** : Se concentrer uniquement sur le jeu de données le plus récent ; l’historisation des données n’est pas requise.  
- **Documentation** : Fournir une documentation claire du modèle de données pour soutenir à la fois les parties prenantes métiers et les équipes analytiques.  

---

### 📊 BI : Analytique & Reporting (Analyse de Données)

**Objectif** :  
Développer des analyses basées sur SQL pour fournir des insights détaillés sur :

- **Comportement des clients**  
- **Performance des produits**  
- **Tendances des ventes**  

Ces insights fournissent aux parties prenantes des indicateurs clés, facilitant la prise de décisions stratégiques.  

---

## 🛡️ Licence

Ce projet est sous licence MIT. Vous êtes libre de l’utiliser, le modifier et le partager avec attribution appropriée.

---

## 🌟 À propos de moi

Bonjour ! Je suis **Hocine DRIOUECHE**
