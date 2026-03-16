---
layout: default
title: Supplier
parent: Customers & Suppliers
nav_order: 2
---

# Supplier
{: .no_toc }

Create and manage all supplier and vendor records across five structured tabs.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Supplier module manages all supplier and vendor records in QBS. Each supplier can be linked to a chart of account, business classification, contact details, and compliance documents. The Add form is organised into five tabs — **Basic Information**, **Company Details**, **Address & Contact**, **Business Information**, and **Documents & Remarks**.

### Navigation

{: .note }
📍 **Path:** Supplier Management → Supplier

---

## 2. Understanding the Screen

### Data Table Columns

| Column | Description |
|--------|-------------|
| **SL** | Auto-generated serial number. |
| **COA Name** | Chart of account linked to the supplier. |
| **Name** | Full registered name of the supplier. |
| **Code** | Unique supplier code (e.g., SUP-00001). |
| **Email** | Email address of the supplier. |
| **Contact No** | Primary contact number. |

{: .note }
Each column header includes a **Filter** button and **sort toggle**. A **Clear Filters** button resets all active filters.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Edit** | Yellow / Orange | Opens the edit form across all tabs. |
| **Delete** | Red | Deletes the record if not referenced in any transactions. |

{: .warning }
If a supplier is referenced in purchase orders, invoices, or other transaction modules, the system will block deletion.

---

## 3. Creating a New Supplier

Click **"New Supplier"** in the top-right corner. The Add modal opens on the Basic Information tab.

### Tab: Basic Information

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Supplier Name** | Yes * | Full registered name of the supplier (e.g., ABCD Raw Materials Ltd.). |
| **Supplier ID** | Yes * | Unique identifier (e.g., SUP-00001). |
| **Email Address** | No | Primary email address. |
| **Contact Number** | Yes * | Primary contact number (e.g., +8801712345678). |
| **Exporting As** | No | Trade or export identity name if operating under a different entity. |
| **Established Year** | No | Year the supplier was established. |
| **Company Overview** | No | Brief description of the supplier's business, products, or services. |

### Tab: Company Details

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Company Registration No** | No | Government-issued company registration number. |
| **BIN Number** | No | Business Identification Number for VAT. |
| **Trade License No** | No | Trade licence number. |
| **Number of Employees** | No | Total employees at the supplier company. |
| **Chart of Account** | No | COA to link this supplier for accounting and payables tracking. |

### Tab: Address & Contact

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Office Address** | No | Full address of the supplier's main office. |
| **Factory Address** | No | Address of the production facility or warehouse. |
| **Website URL** | No | Official website address. |

{: .note }
💡 Enter both office and factory addresses where available — they may be used separately for delivery instructions and correspondence.

### Tab: Business Information

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Supplier Group** | Yes * | Group or segment (e.g., Raw Materials, Packaging, Services). |
| **Business Type** | No | Type of business the supplier operates (e.g., Manufacturer, Trader, Importer). |
| **Product Type** | No | Primary product type or category supplied. |
| **Specialize Area** | No | Supplier's area of specialisation. |
| **Business Category** | Yes * | Broad business category (e.g., Manufacturing, Distribution, Retail). |
| **Credit Rating** | No | Credit rating for financial risk assessment. |
| **Rating** | No | Overall performance or quality rating based on internal evaluation. |

{: .note }
**Supplier Group** and **Business Category** are mandatory for procurement reporting and vendor analysis.

### Tab: Documents & Remarks

| Field | Required? | Guidance |
|-------|-----------|----------|
| **Remarks** | No | Additional notes or internal comments. |
| **Is Active** | No | Toggle to enable or disable. Inactive suppliers are hidden from purchase dropdowns. |

Click **Save** to create the record, or **Close** to discard.

{: .note }
💡 Complete all five tabs before saving. **Supplier Group** and **Business Category** in the Business Information tab must be filled before the record can be saved.

---

## 4. Editing an Existing Record

- Locate the supplier → click **yellow Edit button** → update fields across all tabs → click **Save**.

{: .warning }
Editing the Supplier Name, Supplier ID, or Chart of Account may affect existing purchase orders, invoices, and financial reports.

---

## 5. Deleting a Record

### When Deletion is Allowed
- Created by mistake with no associated purchase orders, invoices, or transaction history.

### When Deletion is Blocked
- Referenced in purchase orders, goods received notes, supplier invoices, payment records, or ledger entries.

{: .important }
🔒 The system will prevent deletion and display an error if the supplier is in use.

---

## 6. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts](../accounting/chart-of-accounts) | Each supplier is linked to a COA for payables tracking. |
| Purchase Management | Suppliers are the source of purchase orders, GRNs, and invoices. |
| Accounts Payable | Outstanding balances and payment records are tracked against supplier accounts. |
| Inventory Management | Goods received from suppliers are tracked in inventory. |
| Reporting | Supplier data is used for procurement analysis and vendor performance reports. |
