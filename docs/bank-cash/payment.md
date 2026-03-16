---
layout: default
title: Payment
parent: Bank / Cash
nav_order: 5
6
---

# Payment
{: .no_toc }

Manage payment batches and record payment transactions against Chart of Accounts.
{: .fs-6 .fw-300 }

## Table of Contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 1. Overview

The Payment module allows authorized users to manage payment batches and record payment transactions against Chart of Accounts entries.

### Navigation

{: .note }
📍 **Path:** Bank/Cash → Payment
Bank/Cash → Receive

---

## 2. Payment Batch
Receive Batch List

When you navigate to Payment, the system displays a list of all existing payment batches.

### Action Buttons (Per Row)

| Button | Colour | Function |
|--------|--------|----------|
| **Show** | Blue | Opens the batch and displays all associated payment records. |
| **Edit** | Yellow / Orange | Opens the batch edit modal pre-filled with existing values. |
| **Delete** | Red | Permanently removes the batch after confirmation. |

---

## 3. Creating a New Payment Batch
Receive Batch

Click the green **"New Payment Batch
Receive Batch"** button in the top-right corner.

### Batch Form Fields

| Field | Required? | Description |
|-------|-----------|-------------|
| **Batch Name** | Yes * | Descriptive name for the payment batch. |
| **Transaction Type** | Yes * | Select the transaction type applicable to this batch. |
| **Is Lock** | No | Toggle to lock the batch — no further payments can be added or modified when locked. |

{: .note }
💡 Use **Is Lock** to close a batch once all payments are finalised. This prevents accidental modifications to completed periods.

---

## 4. Viewing the Payment List

Click **Show** on any batch row to open it and display all associated payment records. The **New Payment** button inside automatically links any new payment to the current batch.

---

## 5. Creating a New Payment

Click **New Payment** to open the payment creation form.

### Payment Form Fields

| Field | Description |
|-------|-------------|
| **Payment ID** | Auto-generated. Shows "New" when creating. |
| **Payment Date** | Date of the payment transaction. |
| **Payment Batch** | Auto-selected from the batch. Read-only. |
| **Transaction Type** | Auto-selected from the batch. Read-only. |
| **Financial Year & Period** | Auto-populated based on the payment date. Read-only. |
| **Bank Account** | Select the bank account for this payment. |
| **Amount** | Enter the payment amount. |
| **Remarks** | Notes or particulars for this payment. |
| **Payment For** | Reference type — controls additional fields shown. |

### Payment For — Reference Types

- **Other** — no additional fields.
- **PO, GRN, Employee, Customer, or Supplier** — displays a reference selection field.

---

## 6. Saving and Printing

Click **Submit** to save the payment. After saving, **Print** and **Update** options become available. Click **Close** to return to the list.

---

## 7. Related Modules

| Module | Relationship |
|--------|-------------|
| [Chart of Accounts](../accounting/chart-of-accounts) | Each payment is posted to a GL account. |
| [Financial Year](../accounting/financial-year) | The payment date determines the financial year and period. |
| [General Ledger](../accounting/general-ledger) | Payment transactions post to the General Ledger. |
