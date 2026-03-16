---
layout: default
title: Receive
parent: Bank / Cash
nav_order: 6
---

# Receive
{: .no_toc }

Manage receive batches and record receive transactions against Chart of Accounts.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Receive module allows authorized users to manage receive batches and record receive transactions against Chart of Accounts entries.

### Navigation

{: .note }
📍 **Path:** Bank/Cash → Receive

---

## 2. Receive Batch List

When you navigate to Receive, the system displays a list of all existing receive batches.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Show** | Blue | Opens the batch and displays all associated receive records. |
| **Edit** | Yellow / Orange | Opens the batch edit modal pre-filled with existing values. |
| **Delete** | Red | Permanently removes the batch after confirmation. |

---

## 3. Creating a New Receive Batch

Click the green **"New Receive Batch"** button in the top-right corner.

### Batch Form Fields

| Field | Required? | Description |
|-------|-----------|-------------|
| **Batch Name** | Yes * | Descriptive name for the receive batch. |
| **Transaction Type** | Yes * | Select the transaction type applicable to this batch. |
| **Is Lock** | No | Toggle to lock the batch — no further receives can be added or modified when locked. |

{: .note }
💡 Use **Is Lock** to close a batch once all receives are finalised. This prevents accidental modifications to completed periods.

---

## 4. Viewing the Receive List

Click **Show** on any batch row to open it and display all associated receive records. The **New Receive** button inside automatically links any new receive to the current batch.

---

## 5. Creating a New Receive

Click **New Receive** to open the receive creation form.

### Receive Form Fields

| Field | Description |
|-------|-------------|
| **Receive ID** | Auto-generated. Shows "New" when creating. |
| **Receive Date** | Date of the receive transaction. |
| **Receive Batch** | Auto-selected from the batch. Read-only. |
| **Transaction Type** | Auto-selected from the batch. Read-only. |
| **Financial Year & Period** | Auto-populated based on the receive date. Read-only. |
| **Bank Account** | Select the bank account for this receive. |
| **Amount** | Enter the receive amount. |
| **Remarks** | Notes or particulars for this receive. |
| **Receive For** | Reference type — controls additional fields shown. |

### Receive For — Reference Types

- **Other** — no additional fields.
- **PO, GRN, Employee, Customer, or Supplier** — displays a reference selection field.

---

## 6. Saving and Printing

Click **Submit** to save the receive. After saving, **Print** and **Update** options become available. Click **Close** to return to the list.

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts](../accounting/chart-of-accounts) | Each receive is posted to a GL account. |
| [Financial Year](../accounting/financial-year) | The receive date determines the financial year and period. |
| [General Ledger](../accounting/general-ledger) | Receive transactions post to the General Ledger. |
