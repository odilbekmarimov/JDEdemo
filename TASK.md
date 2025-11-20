# JD Edwards Demo Project

This project guides you to generate realistic fake ERP data, model relationships in Power BI, and build dashboards for **General Ledger**, **Sales**, and **Inventory**, without using JD Edwards table codes.

---

## 1. Project Overview

You will create a small ERP dataset that behaves like a real enterprise system. Your dataset must include:

* **General Ledger data** (accounts, companies, business units, ledger transactions)
* **Sales data** (customers, items, sales orders, sales history)
* **Inventory data** (items, branch inventory, inventory ledger)

After generating your data, you must:

1. Build a relational model in Power BI.
2. Create dashboards for General Ledger, Sales, and Inventory.
3. Add standard financial and operational KPIs.

---

## 2. Required Datasets (Business Names Only)

Below are the datasets you must generate.

### A. General Ledger

1. **Accounts**

   * AccountID
   * Company
   * BusinessUnit
   * Object
   * Subsidiary
   * Description
   * CategoryCodes (optional)

2. **LedgerTransactions**

   * EntryID
   * Company
   * BusinessUnit
   * AccountID (links to Accounts)
   * LedgerType (Actual, Budget)
   * GLDate
   * Amount
   * DocumentNumber
   * Explanation

---

### B. Sales

1. **SalesOrders**

   * OrderNumber
   * CustomerID
   * ItemID
   * Branch
   * OrderDate
   * Quantity
   * Price
   * Cost
   * GrossProfit
   * DocumentType (SO, CR, etc.)

2. **SalesHistory** (completed orders)

   * Same structure as SalesOrders

3. **Customers**

   * CustomerID
   * Name
   * Region
   * City
   * Category

4. **Items**

   * ItemID
   * Description
   * Category
   * UnitOfMeasure

---

### C. Inventory

1. **ItemBranches**

   * ItemID
   * Branch
   * OnHandQuantity
   * ReorderPoint
   * StandardCost

2. **InventoryLedger**

   * LedgerID
   * ItemID
   * Branch
   * GLDate
   * TransactionType (Issue, Receipt, Adjustment, Purchase)
   * Quantity
   * Amount

---

## 3. Your Tasks

You will generate realistic fake ERP data using the required datasets described above. Focus on creating:

* meaningful values,
* correct business logic,
* consistent connections between fields.

Think like an analyst working inside an ERP system.

---

## 4. What You Must Produce

You will prepare the following:

1. All datasets as CSV files
2. A clean Power BI file that loads your data
3. Basic & Advanced calculations
4. Clear labeling and organized fields

---

In this project, you must also refer to the **QuickLaunch for JD Edwards PDF** provided to you. Use it as a reference for creating realistic visual ideas, KPIs, and dashboard layouts for General Ledger, Sales, and Inventory.

For understanding how JD Edwards data is structured, refer to the **official Oracle JD Edwards documentation**:

* [JD Edwards EnterpriseOne Naming Conventions](https://docs.oracle.com/cd/E17984_01/doc.898/e14698/naming_conventions.htm)
* [Table Design and Naming Guide](https://docs.oracle.com/en/applications/jd-edwards/development-tools/9.2.x/eottd/naming-tables.html)
* [Program and Table Naming Conventions](https://docs.oracle.com/en/applications/jd-edwards/supply-chain-manufacturing/9.2/eoadi/understanding-program-and-table-naming-conventions.html)

These sources will help you understand how to name, structure, and connect your data elements when creating the fake ERP dataset and dashboards.
