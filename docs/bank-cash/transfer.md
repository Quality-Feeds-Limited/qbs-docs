---
layout: default
title: Transfer
parent: Bank / Cash
nav_order: 7
---

# Transfer
{: .no_toc }

Manage transfer batches and record transfer transactions against Chart of Accounts.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Transfer module allows authorized users to manage transfer batches and record transfer transactions against Chart of Accounts entries.

### Navigation

{: .note }
📍 **Path:** Bank/Cash → Transfer

---

## 2. Transfer Batch List

When you navigate to Transfer, the system displays a list of all existing transfer batches.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Show** | Blue | Opens the batch and displays all associated transfer records. |
| **Edit** | Yellow / Orange | Opens the batch edit modal pre-filled with existing values. |
| **Delete** | Red | Permanently removes the batch after confirmation. |

---

## 3. Creating a New Transfer Batch

Click the green **"New Transfer Batch"** button in the top-right corner.

### Batch Form Fields

| Field | Required? | Description |
|-------|-----------|-------------|
| **Batch Name** | Yes * | Descriptive name for the transfer batch. |
| **Transaction Type** | Yes * | Select the transaction type applicable to this batch. |
| **Is Lock** | No | Toggle to lock the batch — no further transfers can be added or modified when locked. |

{: .note }
💡 Use **Is Lock** to close a batch once all transfers are finalised. This prevents accidental modifications to completed periods.

---

## 4. Viewing the Transfer List

Click **Show** on any batch row to open it and display all associated transfer records. The **New Transfer** button inside automatically links any new transfer to the current batch.

---

## 5. Creating a New Transfer

Click **New Transfer** to open the transfer creation form.

### Transfer Form Fields

| Field | Description |
|-------|-------------|
| **Transfer ID** | Auto-generated. Shows "New" when creating. |
| **Transfer Date** | Date of the transfer transaction. |
| **Transfer Batch** | Auto-selected from the batch. Read-only. |
| **Transaction Type** | Auto-selected from the batch. Read-only. |
| **Financial Year & Period** | Auto-populated based on the transfer date. Read-only. |
| **Bank Account** | Select the bank account for this transfer. |
| **Amount** | Enter the transfer amount. |
| **Remarks** | Notes or particulars for this transfer. |
| **Transfer For** | Reference type — controls additional fields shown. |

### Transfer For — Reference Types

- **Other** — no additional fields.
- **PO, GRN, Employee, Customer, or Supplier** — displays a reference selection field.

---

## 6. Saving and Printing

Click **Submit** to save the transfer. After saving, **Print** and **Update** options become available. Click **Close** to return to the list.

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts](../accounting/chart-of-accounts) | Each transfer is posted to a GL account. |
| [Financial Year](../accounting/financial-year) | The transfer date determines the financial year and period. |
| [General Ledger](../accounting/general-ledger) | Transfer transactions post to the General Ledger. |
