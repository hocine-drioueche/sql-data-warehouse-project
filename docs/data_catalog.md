# Data Catalog for Gold Layer

## Overview
The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of **dimension tables** and **fact tables** for specific business metrics.

---

### 1. **gold.dim_customers**
- **Purpose:** Stores customer details enriched with demographic and geographic data.
- **Columns:**

| Column Name      | Data Type     | Description                                                                                   |
|------------------|---------------|-----------------------------------------------------------------------------------------------|
| customer_key     | INT           | Surrogate key uniquely identifying each customer record in the dimension table.               |
| customer_id      | INT           | Unique numerical identifier assigned to each customer.                                        |
| customer_number  | NVARCHAR(50)  | Alphanumeric identifier representing the customer, used for tracking and referencing.         |
| first_name       | NVARCHAR(50)  | The customer's first name, as recorded in the system.                                         |
| last_name        | NVARCHAR(50)  | The customer's last name or family name.                                                     |
| country          | NVARCHAR(50)  | The country of residence for the customer (e.g., 'Australia').                               |
| marital_status   | NVARCHAR(50)  | The marital status of the customer (e.g., 'Married', 'Single').                              |
| gender           | NVARCHAR(50)  | The gender of the customer (e.g., 'Male', 'Female', 'n/a').                                  |
| birthdate        | DATE          | The date of birth of the customer, formatted as YYYY-MM-DD (e.g., 1971-10-06).               |
| create_date      | DATE          | The date and time when the customer record was created in the system|

---

### 2. **gold.dim_products**
- **Purpose:** Provides information about the products and their attributes.
- **Columns:**

| Column Name         | Data Type     | Description                                                                                   |
|---------------------|---------------|-----------------------------------------------------------------------------------------------|
| product_key         | INT           | Surrogate key uniquely identifying each product record in the product dimension table.         |
| product_id          | INT           | A unique identifier assigned to the product for internal tracking and referencing.            |
| product_number      | NVARCHAR(50)  | A structured alphanumeric code representing the product, often used for categorization or inventory. |
| product_name        | NVARCHAR(50)  | Descriptive name of the product, including key details such as type, color, and size.         |
| category_id         | NVARCHAR(50)  | A unique identifier for the product's category, linking to its high-level classification.     |
| category            | NVARCHAR(50)  | The broader classification of the product (e.g., Bikes, Components) to group related items.  |
| subcategory         | NVARCHAR(50)  | A more detailed classification of the product within the category, such as product type.      |
| maintenance_required| NVARCHAR(50)  | Indicates whether the product requires maintenance (e.g., 'Yes', 'No').                       |
| cost                | INT           | The cost or base price of the product, measured in monetary units.                            |
| product_line        | NVARCHAR(50)  | The specific product line or series to which the product belongs (e.g., Road, Mountain).      |
| start_date          | DATE          | The date when the product became available for sale or use, stored in|

---

### 3. **gold.fact_sales**
- **Purpose:** Stores transactional sales data for analytical purposes.
- **Columns:**

| Column Name     | Data Type     | Description                                                                                   |
|-----------------|---------------|-----------------------------------------------------------------------------------------------|
| order_number    | NVARCHAR(50)  | A unique alphanumeric identifier for each sales order (e.g., 'SO54496').                      |
| product_key     | INT           | Surrogate key linking the order to the product dimension table.                               |
| customer_key    | INT           | Surrogate key linking the order to the customer dimension table.                              |
| order_date      | DATE          | The date when the order was placed.                                                           |
| shipping_date   | DATE          | The date when the order was shipped to the customer.                                          |
| due_date        | DATE          | The date when the order payment was due.                                                      |
| sales_amount    | INT           | The total monetary value of the sale for the line item, in whole currency units (e.g., 25).   |
| quantity        | INT           | The number of units of the product ordered for the line item (e.g., 1).                       |
| price           | INT           | The price per unit of the product for the line item, in whole currency units (e.g., 25).      |

---

# Catalogue des Données pour la Couche Gold

## Aperçu
La couche Gold est la représentation des données au niveau métier, structurée pour supporter les cas d’utilisation analytiques et de reporting. Elle se compose de **tables de dimensions** et de **tables de faits** pour des indicateurs métier spécifiques.

---

### 1. **gold.dim_customers**
- **Objectif :** Stocke les informations clients enrichies avec des données démographiques et géographiques.
- **Colonnes :**

| Nom de la Colonne | Type de Donnée | Description                                                                                   |
|------------------|----------------|-----------------------------------------------------------------------------------------------|
| customer_key     | INT            | Clé surrogate identifiant de manière unique chaque enregistrement client dans la table dimension. |
| customer_id      | INT            | Identifiant numérique unique attribué à chaque client.                                        |
| customer_number  | NVARCHAR(50)   | Identifiant alphanumérique représentant le client, utilisé pour le suivi et les références.  |
| first_name       | NVARCHAR(50)   | Prénom du client tel qu’enregistré dans le système.                                           |
| last_name        | NVARCHAR(50)   | Nom de famille ou nom du client.                                                              |
| country          | NVARCHAR(50)   | Pays de résidence du client (ex. : 'Australia').                                              |
| marital_status   | NVARCHAR(50)   | Statut marital du client (ex. : 'Married', 'Single').                                         |
| gender           | NVARCHAR(50)   | Sexe du client (ex. : 'Male', 'Female', 'n/a').                                              |
| birthdate        | DATE           | Date de naissance du client, formatée en YYYY-MM-DD (ex. : 1971-10-06).                       |
| create_date      | DATE           | Date et heure de création de l’enregistrement client dans le système.                        |

---

### 2. **gold.dim_products**
- **Objectif :** Fournit des informations sur les produits et leurs attributs.
- **Colonnes :**

| Nom de la Colonne   | Type de Donnée | Description                                                                                   |
|--------------------|----------------|-----------------------------------------------------------------------------------------------|
| product_key         | INT           | Clé surrogate identifiant de manière unique chaque enregistrement produit dans la table dimension. |
| product_id          | INT           | Identifiant unique attribué au produit pour le suivi interne et les références.               |
| product_number      | NVARCHAR(50)  | Code alphanumérique structuré représentant le produit, souvent utilisé pour la catégorisation ou l’inventaire. |
| product_name        | NVARCHAR(50)  | Nom descriptif du produit, incluant les détails clés comme le type, la couleur et la taille.  |
| category_id         | NVARCHAR(50)  | Identifiant unique pour la catégorie du produit, reliant à sa classification de haut niveau. |
| category            | NVARCHAR(50)  | Classification générale du produit (ex. : Bikes, Components) pour regrouper les articles similaires. |
| subcategory         | NVARCHAR(50)  | Classification plus détaillée du produit au sein de la catégorie, comme le type de produit. |
| maintenance_required| NVARCHAR(50)  | Indique si le produit nécessite un entretien (ex. : 'Yes', 'No').                             |
| cost                | INT           | Coût ou prix de base du produit, exprimé en unités monétaires.                                |
| product_line        | NVARCHAR(50)  | Ligne de produit ou série spécifique à laquelle le produit appartient (ex. : Road, Mountain). |
| start_date          | DATE          | Date à laquelle le produit est devenu disponible à la vente ou à l’usage.                     |

---

### 3. **gold.fact_sales**
- **Objectif :** Stocke les données transactionnelles de ventes pour l’analyse.
- **Colonnes :**

| Nom de la Colonne | Type de Donnée | Description                                                                                   |
|-----------------|----------------|-----------------------------------------------------------------------------------------------|
| order_number    | NVARCHAR(50)   | Identifiant alphanumérique unique pour chaque commande (ex. : 'SO54496').                     |
| product_key     | INT            | Clé surrogate reliant la commande à la table dimension produit.                               |
| customer_key    | INT            | Clé surrogate reliant la commande à la table dimension client.                                |
| order_date      | DATE           | Date à laquelle la commande a été passée.                                                     |
| shipping_date   | DATE           | Date à laquelle la commande a été expédiée au client.                                         |
| due_date        | DATE           | Date à laquelle le paiement de la commande était dû.                                          |
| sales_amount    | INT            | Valeur monétaire totale de la vente pour la ligne de commande, en unités monétaires entières (ex. : 25). |
| quantity        | INT            | Nombre d’unités du produit commandées pour la ligne de commande (ex. : 1).                   |
| price           | INT            | Prix par unité du produit pour la ligne de commande, en unités monétaires entières (ex. : 25). |
