## **Retail Analytics Project Summary**

This is an end-to-end retail analytics solution built on a structured data warehouse that enables business intelligence and decision-making for a retail organization.

## **Data Architecture**

The project uses a three-layer medallion architecture within the retail_q catalog under the retail_gold schema:

## Gold Layer Tables (analytics-ready):
- dim_calendar - Date dimension
- dim_customer - Customer master data
- dim_product - Product catalog
- fact_sales - Transactional sales data
- fact_inventory - Current inventory positions
-----------------------------------------------------------------------------------------------------------------
## **Source Data Details**
### 1. Sales Transaction Data (fact_sales)
- Total Transactions: 1,100 transactions 1
- Active Customers: 7 customers with transaction history
- Products Sold: 20 unique products
- Store Locations: 5 active stores
- Sales Channels: 2 channels (Online, Store) 2
- Payment Methods: 5 modes (Card, Cash, Net Banking, UPI, Crypto) 3
- Pipeline Stages: Tracks opportunity stages including Proposal/Price Quote, Closed Won, Closed Lost, Negotiation/Review, and Qualification
### 2. Customer Master Data (dim_customer)
- Total Customers: 50 customers 4
- Customer Types: 2 segments (Customer - Direct, Customer - Channel) 5
- Industry Focus: Retail sector
- Geographic Coverage: Multi-city, multi-state coverage across billing locations
- Attributes: Includes annual revenue, employee count, contact details, and website information
### 3. Product Catalog (dim_product)
- Total Products: 20 products 6
- Categories: 4 main categories (Electronics, Fashion, Groceries, Home) 7
- Subcategories: 11 subcategories (Accessories, TV, Dairy, Kitchen, Laptop, etc.)
- Brands: 12 distinct brands
- Suppliers: 12 suppliers (Sony India, Apple India, Samsung India, HP India, Philips India, etc.)
- Product Launch: All products launched on 2025-01-01

### 4. Inventory Data (fact_inventory)
- Inventory Records: 40 inventory records 8
- Products Tracked: 20 products in inventory
- Warehouse Locations: 5 warehouse facilities
- Total Stock: 2,251 units across all locations
- Last Updated: Stock data maintained from January 2026 through July 20, 2026
### 5. Calendar Dimension (dim_calendar)
- Date Range: January 1, 2025 to December 31, 2028 9
- Coverage: 4 years (1,461 calendar days including leap year)
- Granularity: Daily level with pre-calculated aggregations for week, month, quarter, and year
- Business Calendar: Includes weekend/weekday flags and fiscal period boundaries
---------------------------------------------------------------------------------------------------------
## Business Capabilities
The data model supports analysis across multiple dimensions:

### Customer Analytics:
- Customer segmentation (Direct vs Channel)
- Transaction behavior analysis
- Customer lifetime value assessment
- Geographic distribution analysis
### Sales Analytics:
- Revenue and transaction volume tracking
- Sales channel performance (Online vs Store)
- Payment mode preferences and trends
- Opportunity pipeline analysis with stage tracking
- Multi-store performance comparison
### Product Analytics:
- Product performance by category (Electronics, Fashion, Groceries, Home)
- Subcategory and brand analysis
- Pricing and discount effectiveness
- Product segment profitability
- Supplier performance tracking
### Inventory Management:
- Stock level monitoring across 5 warehouses
- Reorder point tracking
- Inventory health status
- Product availability analysis
- Time-Series Analysis:
- Trend analysis with daily, weekly, monthly, quarterly, and yearly granularity
- Seasonality patterns with weekend/weekday segmentation
- Year-over-year and period-over-period comparisons
- 4-year historical and future planning horizon
------------------------------------------------------------------------------------------------------------
### Analysis Performed
During our session, we executed specific queries to answer business questions:

- Customer Count Analysis - Identified total customer base of 50 customers 4
- Top Customer Identification - Found ELITE BAZAAR PVT LTD 39 as the most active customer with 329 transactions 10
- Low-Activity Customer Analysis - Identified the 5 customers with the fewest transactions, ranging from 94 to 124 transactions 11
----------------------------------------------------------------------------------------------------------
### Technical Implementation
- **Platform:** Databricks with Unity Catalog governance
- **Catalog:** retail_q
- **Schema:** retail_gold (Gold layer - analytics-ready)
- **Query Engine:** Spark SQL
- **Data Model:** Star schema with dimension and fact tables
- **Naming Convention:** Standardized with dim_ prefix for dimensions and fact_ prefix for fact tables
- **Data Quality:** Structured with proper data types, constraints, and referential integrity
- **Scalability:** Designed to handle growing transaction volumes and expanding product catalog
--------------------------------------------------------------------------------------------------------
### Key Insights from Source Data
Customer Engagement: Only 7 out of 50 customers (14%) have transaction history, indicating significant opportunity for customer activation

- **Product Portfolio:** Focused catalog of 20 products across 4 major retail categories
- **Omnichannel Presence:** Dual-channel strategy with both online and physical store operations
- **Payment Flexibility:** Modern payment infrastructure supporting 5 payment methods including emerging options like UPI and Crypto
- **Inventory Distribution:** Multi-warehouse strategy with 5 locations managing 2,251 units
- **Data Freshness:** Inventory data maintained through July 2026, indicating active operational tracking
- This project provides a scalable foundation for retail business intelligence, enabling stakeholders to make data-driven decisions across sales, inventory, customer relationships, and product management.

