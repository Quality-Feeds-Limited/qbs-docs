---
layout: default
title: General Ledger
parent: Accounting
nav_order: 1
---

# General Ledger — Voucher
{: .no_toc }

Manage ledger batches and post debit/credit voucher entries against Chart of Accounts.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The General Ledger module allows authorized users to manage ledger batches and post voucher entries against Chart of Accounts. Each voucher is linked to a batch and records debit or credit transactions for financial reporting.

### Purpose
- Organize journal entries into manageable ledger batches.
- Post debit and credit voucher transactions to GL accounts.
- Link vouchers to purchase orders, GRNs, employees, customers, or suppliers.
- Print vouchers directly from the system after creation.

### Navigation

{: .note }
📍 **Path:** Accounting → General Ledger

---

## 2. Ledger Batch List

When you navigate to General Ledger, the system displays a list of all existing ledger batches.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Show** | Blue | Opens the batch and displays all its associated vouchers. |
| **Edit** | Yellow / Orange | Opens the batch edit modal pre-filled with existing values. |
| **Delete** | Red | Permanently removes the batch after confirmation. |

---

## 3. Creating a New Batch

Click the green **New Batch** button in the top-right corner.

### Batch Form Fields

| Field | Required? | Description |
|-------|-----------|-------------|
| **Batch Name** | Yes * | Enter a descriptive name for the ledger batch. |
| **User** | Yes * | Select the user(s) who will have permission to work with this batch. |
| **Is Lock** | No | Toggle to lock the batch — no further entries or edits can be made when locked. |

{: .note }
💡 Use **Is Lock** to close a batch once all entries are finalised. This prevents accidental edits to completed periods.

---

## 4. Viewing the Voucher List

Click **Show** on any batch row to open it and display all associated vouchers. The **New Voucher** button inside the batch automatically links any new voucher to that batch.

---

## 5. Creating a New Voucher

Click **New Voucher** to open the voucher creation form.

### Voucher Form Fields

| Field | Description |
|-------|-------------|
| **Voucher ID** | Auto-generated. Shows "New" when creating. |
| **Voucher Date** | Date of the transaction. |
| **Voucher Type** | Select from dropdown. |
| **Financial Year, Period & Batch** | Auto-populated from voucher date and batch. Read-only. |
| **Chart of Account** | Select the GL account for the debit or credit entry. |
| **Debit / Credit** | Enter a value in either field — both cannot be filled simultaneously. |
| **Remarks** | Notes or particulars for this entry. |
| **Payment For** | Reference type — controls additional fields shown. |

### Payment For — Reference Types

- **Other** — no additional fields.
- **PO, GRN, Employee, Customer, or Supplier** — displays a reference selection field to link the voucher to the related record.

---

## 6. Saving and Printing a Voucher

Click **Submit** to save the voucher. After saving, the form remains open with **Print** and **Update** options available. Click **Close** to return to the voucher list.

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts](chart-of-accounts) | Each voucher line is posted to a GL account. |
| [Voucher Type](voucher-type) | Vouchers must be assigned a Voucher Type. |
| [Financial Year](financial-year) | The voucher date determines the financial year and period. |
| Purchase Order / GRN | Vouchers can be linked to POs or GRNs via the Payment For field. |
