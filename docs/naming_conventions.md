# 🌐 Naming Conventions / Conventions de Nommage

[English](#english) | [Français](#français)

---

## English

# **Naming Conventions**

This document outlines the naming conventions used for schemas, tables, views, columns, and other objects in the data warehouse.

---

## **Table of Contents**

1. [General Principles](#general-principles)
2. [Table Naming Conventions](#table-naming-conventions)
   - [Bronze Rules](#bronze-rules)
   - [Silver Rules](#silver-rules)
   - [Gold Rules](#gold-rules)
3. [Column Naming Conventions](#column-naming-conventions)
   - [Surrogate Keys](#surrogate-keys)
   - [Technical Columns](#technical-columns)
4. [Stored Procedure Naming Conventions](#stored-procedure-naming-conventions)

---

## **General Principles**

- **Naming Conventions**: Use `snake_case`, with lowercase letters and underscores (`_`) to separate words.  
- **Language**: Use English for all names.  
- **Avoid Reserved Words**: Do not use SQL reserved words as object names.  

---

## **Table Naming Conventions**

### **Bronze Rules**
- All names must start with the source system name, and table names must match their original names without renaming.  
- **`<sourcesystem>_<entity>`**  
  - `<sourcesystem>`: Name of the source system (e.g., `crm`, `erp`).  
  - `<entity>`: Exact table name from the source system.  
  - Example: `crm_customer_info` → Customer information from the CRM system.

### **Silver Rules**
- All names must start with the source system name, and table names must match their original names without renaming.  
- **`<sourcesystem>_<entity>`**  
  - `<sourcesystem>`: Name of the source system (e.g., `crm`, `erp`).  
  - `<entity>`: Exact table name from the source system.  
  - Example: `crm_customer_info` → Customer information from the CRM system.

### **Gold Rules**
- All names must use meaningful, business-aligned names for tables, starting with the category prefix.  
- **`<category>_<entity>`**  
  - `<category>`: Describes the role of the table, such as `dim` (dimension) or `fact` (fact table).  
  - `<entity>`: Descriptive name of the table, aligned with the business domain (e.g., `customers`, `products`, `sales`).  
  - Examples:
    - `dim_customers` → Dimension table for customer data.  
    - `fact_sales` → Fact table containing sales transactions.  

#### **Glossary of Category Patterns**

| Pattern     | Meaning        | Example(s)                               |
|------------|----------------|------------------------------------------|
| `dim_`     | Dimension table | `dim_customer`, `dim_product`           |
| `fact_`    | Fact table      | `fact_sales`                            |
| `report_`  | Report table    | `report_customers`, `report_sales_monthly` |

---

## **Column Naming Conventions**

### **Surrogate Keys**  
- All primary keys in dimension tables must use the suffix `_key`.  
- **`<table_name>_key`**  
  - `<table_name>`: Refers to the name of the table or entity the key belongs to.  
  - `_key`: A suffix indicating that this column is a surrogate key.  
  - Example: `customer_key` → Surrogate key in the `dim_customers` table.

### **Technical Columns**
- All technical columns must start with the prefix `dwh_`, followed by a descriptive name indicating the column's purpose.  
- **`dwh_<column_name>`**  
  - `dwh`: Prefix exclusively for system-generated metadata.  
  - `<column_name>`: Descriptive name indicating the column's purpose.  
  - Example: `dwh_load_date` → System-generated column used to store the date when the record was loaded.

---

## **Stored Procedure Naming Conventions**

- All stored procedures used for loading data must follow the naming pattern:  
- **`load_<layer>`**  
  - `<layer>`: Represents the layer being loaded, such as `bronze`, `silver`, or `gold`.  
  - Examples:  
    - `load_bronze` → Stored procedure for loading data into the Bronze layer.  
    - `load_silver` → Stored procedure for loading data into the Silver layer.

---

## Français

# **Conventions de Nommage**

Ce document décrit les conventions de nommage utilisées pour les schémas, tables, vues, colonnes et autres objets dans l’entrepôt de données.

---

## **Table des Matières**

1. [Principes Généraux](#principes-généraux)
2. [Conventions de Nommage des Tables](#conventions-de-nommage-des-tables)
   - [Règles Bronze](#règles-bronze)
   - [Règles Silver](#règles-silver)
   - [Règles Gold](#règles-gold)
3. [Conventions de Nommage des Colonnes](#conventions-de-nommage-des-colonnes)
   - [Clés Surrogates](#clés-surrogates)
   - [Colonnes Techniques](#colonnes-techniques)
4. [Conventions de Nommage des Procédures Stockées](#conventions-de-nommage-des-procédures-stockées)

---

## **Principes Généraux**

- **Conventions de Nommage** : Utiliser le `snake_case` avec des lettres minuscules et des underscores (`_`) pour séparer les mots.  
- **Langue** : Utiliser l’anglais pour tous les noms.  
- **Éviter les mots réservés** : Ne pas utiliser les mots réservés SQL comme noms d’objets.  

---

## **Conventions de Nommage des Tables**

### **Règles Bronze**
- Tous les noms doivent commencer par le nom du système source et les tables doivent conserver leur nom original.  
- **`<sourcesystem>_<entity>`**  
  - `<sourcesystem>` : Nom du système source (ex. : `crm`, `erp`).  
  - `<entity>` : Nom exact de la table dans le système source.  
  - Exemple : `crm_customer_info` → Informations clients provenant du CRM.

### **Règles Silver**
- Tous les noms doivent commencer par le nom du système source et les tables doivent conserver leur nom original.  
- **`<sourcesystem>_<entity>`**  
  - `<sourcesystem>` : Nom du système source (ex. : `crm`, `erp`).  
  - `<entity>` : Nom exact de la table dans le système source.  
  - Exemple : `crm_customer_info` → Informations clients provenant du CRM.

### **Règles Gold**
- Tous les noms doivent être significatifs et alignés sur le domaine métier, avec un préfixe de catégorie.  
- **`<category>_<entity>`**  
  - `<category>` : Décrit le rôle de la table, par exemple `dim` (dimension) ou `fact` (table de faits).  
  - `<entity>` : Nom descriptif de la table, aligné sur le domaine métier (ex. : `customers`, `products`, `sales`).  
  - Exemples :  
    - `dim_customers` → Table dimensionnelle pour les clients.  
    - `fact_sales` → Table de faits contenant les ventes.  

#### **Glossaire des Préfixes de Catégorie**

| Préfixe    | Signification    | Exemple(s)                                |
|------------|-----------------|------------------------------------------|
| `dim_`     | Table dimension | `dim_customer`, `dim_product`            |
| `fact_`    | Table de faits  | `fact_sales`                             |
| `report_`  | Table de rapport | `report_customers`, `report_sales_monthly` |

---

## **Conventions de Nommage des Colonnes**

### **Clés Surrogates**  
- Toutes les clés primaires des tables dimensionnelles doivent utiliser le suffixe `_key`.  
- **`<table_name>_key`**  
  - `<table_name>` : Nom de la table ou de l’entité à laquelle appartient la clé.  
  - `_key` : Suffixe indiquant que c’est une clé surrogate.  
  - Exemple : `customer_key` → Clé surrogate dans la table `dim_customers`.

### **Colonnes Techniques**
- Toutes les colonnes techniques doivent commencer par le préfixe `dwh_` suivi d’un nom descriptif indiquant l’objectif de la colonne.  
- **`dwh_<column_name>`**  
  - `dwh` : Préfixe réservé aux métadonnées générées par le système.  
  - `<column_name>` : Nom descriptif indiquant l’objectif de la colonne.  
  - Exemple : `dwh_load_date` → Colonne générée par le système pour stocker la date de chargement des données.

---

## **Conventions de Nommage des Procédures Stockées**

- Toutes les procédures stockées utilisées pour le chargement des données doivent suivre le modèle :  
- **`load_<layer>`**  
  - `<layer>` : Représente la couche chargée, par exemple `bronze`, `silver` ou `gold`.  
  - Exemples :  
    - `load_bronze` → Procédure pour charger la couche Bronze.  
    - `load_silver` → Procédure pour charger la couche Silver.
