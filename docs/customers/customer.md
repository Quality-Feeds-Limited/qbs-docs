---
layout: default
title: Customer
parent: Customers & Suppliers
nav_order: 1
---

# Customer
{: .no_toc }

Create and manage all customer (outlet) records across four structured tabs.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Customer module manages all customer and outlet records in QBS. Each customer can be assigned a business type, geographic location, chart of account, and compliance documents. The Add form is organised into four tabs — **Basic Information**, **Location**, **Documents**, and **Additional**.

### Navigation

{: .note }
📍 **Path:** Customer Management → Customer

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **District Name** | The district where the customer is located. |
| **Division Name** | The division where the customer is located. |
| **COA Name** | Chart of account linked to the customer. |
| **Area Name** | The area assigned to the customer. |
| **Business Type** | Business category (e.g., Modern Trade, Horeka). |
| **Customer Name** | Full name of the customer or outlet. |
| **Code** | Unique customer code (e.g., A-00001). |

{: .note }
Each column header includes a **Filter** button and a **sort toggle**. A **Clear Filters** button resets all active filters.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the edit form across all tabs. |
| **Delete** | Red | Deletes the record if not referenced in any transactions. |

{: .warning }
If a customer is referenced in sales orders, invoices, or other transaction modules, the system will block deletion.

---

## 3. Creating a New Customer

Click **"New Customer"** in the top-right corner. The Add modal opens on the Basic Information tab.

### Tab: Basic Information

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Customer Name** | Yes * | Full official name of the customer or outlet. |
| **Customer Code** | Yes * | Unique code (e.g., A-00001). |
| **Party Type** | No | Classifies the customer category. |
| **Ownership Type** | No | Ownership structure (e.g., Sole Proprietorship, Partnership). |
| **Business Type** | No | Select from dropdown (e.g., Modern Trade, Horeka). |
| **Chart of Account** | No | COA to link this customer for accounting purposes. |

### Tab: Location

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Division** | No | Select the division — filters available districts. |
| **District** | No | Select within the chosen division — filters available areas. |
| **Area** | No | Select the specific area within the district. |
| **Address** | No | Full street or postal address. |
| **Latitude** | No | Geographic latitude coordinate. |
| **Longitude** | No | Geographic longitude coordinate. |

{: .note }
Division, District, and Area dropdowns are **cascading** — selecting a Division filters Districts, selecting a District filters Areas.

### Tab: Documents

| Field | Required? | Guidance |
|-------|-----------|----------|
| **BIN Number** | No | Business Identification Number for VAT. |
| **NID Number** | No | National Identity Card number. |
| **Trade License No** | No | Trade licence number. |
| **Company Registration No** | No | Company registration number. |
| **Documents Received** | No | List of physical or digital documents received. |

{: .note }
💡 Enter all available document references even if physical copies are yet to be collected.

### Tab: Additional

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Remarks** | No | Additional notes or internal comments. |
| **Is Active** | No | Toggle to enable or disable the customer. Inactive customers are hidden from transaction dropdowns. |

Click **Save** to create the record, or **Close** to discard.

{: .note }
💡 Complete all four tabs before saving to ensure the customer record is fully populated.

---

## 4. Editing an Existing Record

- Locate the customer → click **yellow Edit button** → update fields across all tabs → click **Save**.

{: .warning }
Editing the Customer Name, Customer Code, or Chart of Account may affect existing sales transactions, invoices, and financial reports.

---

## 5. Deleting a Record

### When Deletion is Allowed
- Created by mistake with no associated sales orders, invoices, or transaction history.

### When Deletion is Blocked
- Referenced in sales orders, delivery notes, invoices, payment records, or ledger entries.

{: .important }
🔒 The system will prevent deletion and display an error if the customer is in use.

---

## 6. Related Modules

| Module | Relationship |
|--------|-------------|
| [Business Type](../setup/business-type) | Customers are classified under a business type. |
| [Area](../setup/area) / [District](../setup/district) / [Division](../setup/division) | Customer location links through the cascading geographic hierarchy. |
| [Chart of Accounts](../accounting/chart-of-accounts) | Each customer can be linked to a COA for receivables tracking. |
| Sales Management | Customers are recipients of sales orders, delivery notes, and invoices. |
