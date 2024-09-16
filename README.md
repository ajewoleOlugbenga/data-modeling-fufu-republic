# Fufu Republic Data Warehouse

## Project Overview
This repository contains the dimensional model for Fufu Republic, a popular restaurant chain in Nigeria. The goal of this project is to provide a data model that supports data-driven decision-making for sales tracking, inventory management, and customer experience enhancements.

### Case Study Summary
Fufu Republic operates multiple outlets across Nigeria, offering a standardized menu with some regional variations. The restaurant supports dine-in, take-out, and online orders, and accepts various payment methods (cash, card via POS, and online payments).



### Business Challenges
1. **Inventory Management**: Variations in customer demand and menu items make it difficult to maintain optimal stock levels across branches.
2. **Customer Experience**: Fufu Republic wants to improve personalized promotions based on purchasing behavior to enhance customer satisfaction.

### Project Objectives
The objective of this project is to create a **dimensional model** that supports:
- Sales trend analysis across locations, payment methods, and dining options (dine-in, take-out, online).
- Efficient stock management to minimize waste and ensure availability.
- Enhanced customer experience through personalized promotions.

## Dimensional Model
The dimensional model in this project is designed to address the following business processes:
- **Sales Tracking**: Understanding sales trends by branch, menu items, and customer preferences.
- **Inventory Management**: Monitoring stock levels based on sales data to optimize supply chain operations.
- **Customer Experience**: Analyzing customer behavior to offer personalized promotions.

### Key Entities:
- **Branches**: Information about each restaurant outlet.
- **Menu Items**: The various dishes offered by Fufu Republic, categorized by type.
- **Customers**: Data about customers, including their order history.
- **Orders**: Details of each customer transaction, including payment method and order type.
- **Order Items**: Specific items in each order, with quantities and prices.
- **Payments**: Payment information for each order.

### Grain, Dimensions, and Facts
- **Grain**: Each record in the sales fact table represents one sales transaction (order).
- **Dimensions**: 
  - `Date`: The time the order was placed.
  - `Branch`: The restaurant where the order was made.
  - `Menu Item`: The specific dish or product ordered.
  - `Customer`: Information about the customer placing the order.
  - `Payment Method`: How the customer paid (cash, card, or online).
  - `Order Type`: Whether the order was dine-in, take-out, or online.
- **Facts**:
  - `Quantity Sold`
  - `Total Amount`
  - `Discount Applied`
  - `Inventory Impact`

## Project Structure
The repository contains the following key files and directories:
- `sql/`: SQL scripts to create the necessary tables and relationships in the database.
- `models/`: Contains the **Entity Relationship Diagram (ERD)**, defining relationships between entities.
- `README.md`: Project overview and instructions.
- `scripts/`: Optional directory for ETL (Extract, Transform, Load) scripts if the model is populated with real data.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/fufu-republic-data-warehouse.git
